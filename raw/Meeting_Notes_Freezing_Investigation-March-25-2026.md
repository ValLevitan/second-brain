# Meeting Summary — Freezing Investigation (Follow-up with Alekseev)
**Date:** March 25, 2026, 11:03 AM Eastern
**Duration:** ~52 minutes
**Attendees:** Val Levitan, Pavel Frolov, Evgeniy Alekseev (external consultant), Alexander Biratko, Genadi Peari

## Summary

### Context & Opening

Val opened by stating that mistakes are made by those who do things — he didn't want finger-pointing, only facts. This was the follow-up call bringing in **Evgeniy Alekseev** as an external specialist. Val had sent Alekseev a document describing the field freezing problems the day before, and asked for hypotheses.

### Alekseev's Initial Hypotheses

Alekseev offered three main hypotheses for the freezing:

1. **Memory management issues** (90% probability in his estimation) — memory leaks, pointer errors, or stack overflows in the C++ code are the most common cause of hard freezes.
2. **Printer driver asynchronous communication** — based on his prior work on the printer code, he identified that synchronous commands to the printer could cause machine hangs. He stated the printer interaction needs to use a separate thread with a command queue rather than synchronous calls.
3. **Chip/processor errata** — every chip and GPU has manufacturer-documented bugs with recommended workarounds. These errata documents should be obtained and checked, especially for the specific processor used.

### Debate: Memory Management & Linux Kernel Protection

A significant technical debate occurred between Alekseev and Frolov about whether memory errors in application code could cause a full system freeze:

- **Alekseev's position:** Memory corruption (pointers going out of bounds, stack overflow) can cause a hard freeze, even on Linux. He expressed uncertainty that Linux can fully protect against application-level memory issues.
- **Frolov's position:** On x86 with Linux, hardware memory protection prevents an application from corrupting kernel memory. If an application writes out of bounds, it crashes (segfault) but the kernel remains operational. This is unlike ARM processors without hardware memory protection.
- **Resolution:** Frolov acknowledged his argument is theoretical and there could be edge cases specific to their kernel version or processor. Both agreed to investigate memory leaks as a useful diagnostic exercise, even if kernel protection should theoretically prevent a full freeze.
- **Genadi's intervention:** Genadi pushed back, noting that memory issues remain the #1 suspect and asking what concrete steps had been taken to validate the theory rather than just saying "Linux should handle it."

### Printer Code — Mutexes Found to Be Present

When Pavel opened the actual printer HAL code (`l_printer`), he found that **mutex locks are already implemented throughout** — every function has lock/unlock calls to prevent race conditions between threads. This contradicted Alekseev's assumption that the printer code lacked thread safety.

Alekseev acknowledged this, saying he hadn't seen mutexes in the code he worked with. Pavel pointed out that Alekseev had used a file as a template that already had mutexes — and the printer code Alekseev wrote does not have them.

**Key exchange:** Pavel noted that while the mutex approach is correct, it doesn't guarantee there isn't a missed spot somewhere — Claude Code's AI analysis had already found potential concurrent access issues that need fixing. The existing good pattern doesn't rule out localized errors.

### Framework-DataCenter Interaction as Freeze Cause

Alexander explained the architecture to Alekseev: **DataCenter (Java application) and Framework (C++ application) run as separate processes on the same machine**, communicating via sockets. The framework reads from DataCenter every frame to update the display.

Pavel raised a new untested hypothesis: **when DataCenter crashes/is killed, the Framework freezes** — they've observed this. But they've never tested what happens if you kill DataCenter and then wait several hours. The morning freezes seen in Georgia could be this exact scenario: DataCenter dies at some point during the night, Framework hangs on its socket waiting for a response, and over hours the machine becomes completely unresponsive.

Alexander added that the old version (Pech 1) should have handled DataCenter death with a reboot or tilt — not a freeze. This behavioral change between versions is a significant clue.

### Decision: Build a Resource Monitoring Utility

Val proposed building **guardrails** — architectural safeguards that catch problems proactively. He used the analogy of roads: roads can work without traffic lights and curbs, but you build them anyway.

The team converged on building a **system resource monitoring utility** that would:
- Monitor memory consumption, file descriptors, sockets, thread count, and stack usage
- Run as an independent daemon (not part of framework or DataCenter)
- Write to its own log file with unbuffered writes (so data survives even if the system freezes)
- Be lightweight enough for production deployment
- Serve as a pre-release QA checkpoint and a production diagnostic tool

**Implementation plan:**
1. Pavel asks Claude Code for the comprehensive list of monitoring parameters
2. Claude Code writes the bash monitoring utility (Pavel estimates hours, not days)
3. Alexander deploys it to the Georgia machines Anton is already managing
4. The utility runs on all 5 test machines in the field

### Decision: SAS Emulator Stress Testing

The team noted that none of the 5 Georgia test machines are connected to SAS (the gaming protocol). Val directed:
- Connect a **SAS emulator** (they already have one) to one of the test machines
- Create a **loop of SAS commands** that would stress the framework — not just status queries, but commands that trigger game enable/disable, mode switches, and other state changes
- This is Alexander Biratko's task, building on the SAS emulator work by Zhenya Khaletsky

### Alekseev's Role Assessment

Val wanted to use Alekseev as "an outside voice" to push the team's thinking. While some of Alekseev's specific claims were challenged (printer code quality, Linux memory protection), his hypotheses did productively guide the discussion. Pavel explicitly noted that Alekseev raising the printer topic advanced their investigation, because the AI analysis had independently found concurrent access issues.

Alekseev expressed skepticism about Claude Code's usefulness (he tried it but found it showed "obvious nonsense") — Val suggested it was likely misconfigured and that the paid version is significantly better.

## Decisions Made

- **Build a resource monitoring daemon (bash utility)** — monitors memory, file descriptors, sockets, threads, stack usage. Pavel to get parameter list from Claude Code, then Claude Code writes v1. (Decided by consensus, proposed by Val)
- **Deploy monitoring utility to Georgia field machines** — all 5 machines via Anton. (Decided by Val)
- **Connect SAS emulator to test machine** — create stress test loop with meaningful SAS commands that exercise the framework. (Decided by Val, assigned to Alexander Biratko)
- **Test the DataCenter-kill scenario over extended time** — kill DataCenter, wait several hours, see if machine becomes fully unresponsive. Compare old version behavior. (Proposed by Pavel, agreed by team)
- **Make monitoring utility part of standard architecture** — pre-release QA gate + production diagnostic. Not just a one-off. (Decided by Val, agreed by Alexander and Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Ask Claude Code for comprehensive list of system monitoring parameters (memory, file descriptors, sockets, threads, stack, etc.) and circulate to team. | 2026-03-25 (immediately) | High | Val said "start immediately please, right now." Foundational input for the monitoring utility. |
| 2 | Pavel Frolov + Claude Code | Write v1 of the bash monitoring utility based on the parameter list. | 2026-03-25 (same day, hours) | High | Pavel and Alexander both estimate hours, not days. Claude Code can write 99-100% of it. |
| 3 | Alexander Biratko | Deploy monitoring utility to Georgia field machines via Anton. Write with unbuffered I/O so logs survive freezes. | 2026-03-25 (after utility is ready) | High | 5 machines available. None currently connected to SAS. |
| 4 | Alexander Biratko | Connect SAS emulator to one test machine and create a stress test loop of meaningful SAS commands (game enable/disable, mode switches). | 2026-03-25 | High | Commands must exercise the framework, not just query status. Builds on existing emulator by Zhenya Khaletsky. |
| 5 | Pavel Frolov / Alexander Biratko | Test the DataCenter-kill extended timeout scenario — kill DC, wait several hours, monitor what happens to Framework and system resources. Compare with old version (Pech 1). | TBD | High | New untested hypothesis: morning freezes in Georgia may be Framework hanging on dead DC socket for hours. |
| 6 | Team (future) | Run static analyzer on C++ code (HAL/Framework) to check for memory leaks and out-of-bounds access. | TBD | Medium | Alekseev's #1 hypothesis. Pavel agrees it's worth checking even though Linux memory protection should prevent kernel-level freeze. |

## Engineering Signals

### Confirmed Signals

- **Engineering Solution — Resource monitoring daemon:** Team agreed to build a bash daemon that monitors memory, file descriptors, sockets, threads, and stack usage. To be deployed both for diagnosis and as a permanent architectural component (pre-release QA gate).

- **Confirmed Finding — Printer HAL code has mutexes but printer DC code may not:** Pavel found mutexes throughout the HAL printer code (`l_printer`). However, Claude Code's AI analysis had already found potential concurrent access issues — possibly in the DC layer or in code Alekseev wrote that was based on a template but didn't carry over the mutex pattern.

### Suspected Signals

- **Possible ADR — Framework socket timeout on DataCenter death:** The framework hangs indefinitely when DataCenter dies because it blocks on socket reads. This needs an architectural decision about timeouts, health checks, or watchdog mechanisms on the Framework-DC socket connection.

- **Possible ADR — Monitoring as architectural requirement:** Val pushed for monitoring to be part of the system architecture, not an afterthought. This implies a formal architectural decision about system observability as a first-class concern.

- **Possible REQ — Pre-release resource monitoring QA gate:** Pavel proposed that before submitting software to any lab/regulator, the monitoring utility must be run for a set period with no anomalies detected. This should be formalized as a release requirement.

## Open Questions

- **Does killing DataCenter and waiting hours reproduce the morning freeze?** Pavel's hypothesis — never tested before.
- **Did the old version (Pech 1) handle DataCenter death differently?** Alexander thinks it triggered a reboot or tilt, not a freeze. Needs verification.
- **Are there memory leaks in the C++ framework or HAL?** Pavel says externally memory appears to stabilize, but a static analyzer might find issues.
- **What specific concurrent access issues did Claude Code find in the printer/HAL code?** Referenced by Pavel but not detailed in this meeting.
- **Can SAS command stress testing trigger the freeze?** None of the test machines currently have SAS connected.

---
*Processed from Teams transcript on 2026-03-25*
*Source meeting: Freezing Investigation (with Alekseev)*
