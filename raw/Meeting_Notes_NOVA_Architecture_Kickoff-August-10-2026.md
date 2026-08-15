# Meeting Summary — NOVA architecture design — kickoff (session 1 of 5)
**Date:** August 10, 2026, 5:15–7:16 AM Eastern
**Duration:** ~2 hours
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Irina Shishko, Evgeny Kharetski, Anton Seregin, Alexey Khamin
**Raw transcript:** [[Meeting_Transcript_NOVA_Architecture_Kickoff-August-10-2026]]

## Summary

This was the first of five planned design sessions on reworking how JVL machines talk to their hardware. The meeting was held in Russian. It ran long and Val called a break near the two-hour mark, moving the follow-up to the next day.

**The problem.** Today the machine uses one large C library (a Hardware Abstraction Layer, HAL) that bridges all the hardware — counter board, IO board, LED board, printer, bill validator, sound, and more — up to the Java-based Local Game Server (LGS) through JNI wrappers. Because it is monolithic, any single module fault crashes the whole machine, and the C code has caused many threading and memory bugs. Changes are heavy and risky.

**The proposal.** Break each hardware library into its own separate service (a set of small services instead of one library), rewritten in Rust. Each service talks to the LGS over a Unix socket; the same channel can be switched to TCP/IP for testing or debugging from another computer. If one service fails, it can be monitored, restarted, and recovered on its own without taking the whole machine down.

**Common service interface.** Every service exposes the same base API — identify itself (info), report its state/health, and list the specific APIs (capabilities) it supports for the exact version installed on that machine. On top of that base, each service adds its own device APIs (for example, the bill validator has "enable money intake," the printer has "print ticket"). The value: the LGS — and Claude — can query a machine, walk its available services and their real capabilities, and produce a fast, accurate report of what works and what does not, instead of trusting documentation.

**Management service.** A small supervisor/management service lists the available services, health-checks them, restarts them, and manages logging levels. Pavel first called it a "mega/super service"; the team walked that back — it is a small, mostly informational service, not a controller of everything.

**Minimum service set.** Printer, bill validator, IO board, counter board, LED board, sound. Optional/next: QR scanner, LTE modem. The digital amplifier / media player is folded into the sound service (it monitors the amplifiers and can restart them). The service set is fixed at setup time (from the RIS config) rather than dynamically detected, so a missing or failed service is visible against the expected list.

**IO board — split or not.** The longest debate. The IO board library currently holds the passport chip, the Dallas chip, storage/memory management, door, battery/time, cooler, and a "passed-through" bill validator. The team (Alexander, Pavel, Evgeny) concluded the IO board should stay as ONE service, because everything on it runs off a single on-board processor and shares one firmware, so it must be tested together — you cannot restart or test the Dallas chip or passport independently of the IO board. Val was skeptical ("60% sure you're wrong") and pushed to justify splitting by device responsibility rather than by which processor or USB port they share, but did not overrule. The bill validator, although it passes through the IO board, becomes its own separate service because it is logically independent (it just mirrors a protocol). Passport stays a dependent sub-module inside the IO board service, with its own logging.

**Val's throughline — "for whom, and where's the money?"** Val repeatedly pushed the team off "how" and onto "who is this for, what are the acceptance criteria, and how does it turn into money." He argued that if a change is not tied to money, JVL does not need it, and that "more reliable" is a generic hand-wave until the benefit chain is concrete. The concrete benefits the team defended under that pressure: (1) a failed service can auto-restart without kicking the player out; (2) a common interface plus AI access lets all software be tested automatically; (3) each service releases separately with its own checksums and tests, so only the changed service needs retesting on real hardware; (4) a hardware emulator can test a single device (e.g. the bill validator: take money / count / return money) without launching the full LGS — impossible today; (5) diagnostics improve — isolate which service failed, auto-enable trace logs on reconnect, collect them, and push small fixes remotely, Linux-style, without a technician visit. The team's split of beneficiaries: ~80% LGS developers and the framework, ~15% QA/testability, ~5% technicians.

**Logging.** Each service gets its own logging, a controllable log level (whole system and per-part via markers), and multiple sinks (local file, remote, console). Log collection should work via USB stick, a Setup button, and QR for offline machines. The team called this the "acceptance criteria for logging."

**Firmware updates.** Add the ability to flash device firmware through the services, including on-the-fly for machines with internet/modem, without a full RIS reinstall or a manual passport re-scan — but only when just the firmware version changes (automatic); a changed serial number is a separate use case. Flagged to think through, because a firmware version change also changes the passport and would otherwise trigger a "register new passport" prompt.

**Multi-platform.** Services/modules must build for both x86 and ARM, so they can be reused in terminal projects or games on other platforms.

## Decisions Made

- **Rewrite the monolithic HAL as separate per-device services in Rust, talking to the LGS over Unix sockets.** TCP/IP or HTTP only in the dev build (or TCP limited to localhost), never exposed on the network in production, for security. (Team consensus; Rust proposed by Alexander, agreed by Pavel and the team.)
- **Keep the IO board as a single service — do not split it into passport/Dallas/memory/door/etc. sub-services.** Everything on it shares one processor and one firmware and must be tested together. Passport remains a dependent module inside the IO board service. (Alexander, Pavel, Evgeny; Val skeptical but did not overrule.)
- **The bill validator is its own separate service,** even though it is passed through the IO board, because it is logically independent.
- **The service set is fixed at setup time (from RIS config), not dynamically detected,** so a missing/failed service shows up against the expected list.
- **A small management/supervisor service** will list services, health-check, restart, and manage logging levels. (The earlier "mega service" framing was walked back to a small informational service.)
- **The digital amplifier / media player is folded into the sound service.**
- **The Rust tech-stack choice is recorded in each service's repo ADR, not written as a formal requirement.** Val's point: the requirement is "reliable, and convenient to develop and test with Claude Code"; Rust is a design/stack decision that belongs in the ADR text so Claude knows what it is working with. (Considered and reframed: "services must be written in Rust" as a requirement → replaced by "record Rust in the ADR; the requirement is reliability + Claude-friendly development.")
- **Each service gets its own Git repository, each with its own ADRs.**

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko (with Pavel Frolov) | Work out the common base API shared by all micro-services — info, status/state, health check, list of supported APIs — with Claude's help; this is the deliverable for the next session | Aug 11, 2026 (next session) | High | Pavel set this as what the next meeting needs |
| 2 | Irina Shishko, Alexey Khamin | Think about and articulate what they specifically need from the new architecture — which hooks/handles would help them in diagnostics and automation | Aug 11, 2026 (next session) | Normal | Pavel asked them directly, since neither had been in the earlier discussion |
| 3 | Alexander Biratko (team) | Feed today's meeting transcript to Claude and have it argue both sides — for and against splitting the IO board and the team's other decisions — objectively, to bring to the next session | Aug 11, 2026 (next session) | Normal | Val's suggestion; Alexander agreed and noted Claude must be set up to argue against, not just agree |
| 4 | Pavel Frolov / Evgeny Kharetski | Pull up and review the IO board library to enumerate exactly what it still contains (storage/memory, Dallas, door, battery/time, cooler, passed-through bill validator) once the splittable parts are removed | TBD | Normal | Evgeny: "need to take the library and look through it" |
| 5 | Team | Create per-service Git repositories, each recording the tech stack (Rust) in its ADRs | TBD | Normal | Follows from the repo/ADR decision |

## Open Questions

- How exactly the money/benefit chain is made concrete — Val's standing challenge, carried to the next session: who is the client and how does the reliability/testability gain translate into dollars (e.g. cutting machine test time, reducing downtime/cashbox loss). Raised by Val.
- Whether a firmware-only update can be pushed automatically (no passport re-scan) while a serial-number change stays a separate flow. Raised by Pavel.
- Whether deferred/late device attachment should be allowed (pass setup without a device, attach it later in production). Raised by Pavel; today's answer is no such capability exists.

## Dispatch Log

---
*Processed from Teams transcript on August 10, 2026 (scheduled meeting-watcher run).*
*Source meeting: NOVA architecture design — kickoff (session 1 of 5)*
