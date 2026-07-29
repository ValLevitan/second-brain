# JVL Freezing Investigation — Comprehensive Report

**Classification:** Internal Engineering — Investigative Record
**Period Covered:** March 9–25, 2026
**Compiled:** March 25, 2026
**Author:** Compiled by Claude Code from meeting transcripts, chat summaries, and email records
**Status:** Living document — to be updated as investigation progresses

---

## 1. Problem Statement

JVL's FLEX-series gaming machines (EGMs) are experiencing **complete, unrecoverable freezes** in the field. When frozen, the screen locks, the machine becomes totally unresponsive, and only a physical power cycle restores operation. No crash logs are recovered after these events, strongly suggesting the **Linux operating system itself becomes non-operational** — not merely an application hang.

The problem has been reported across **multiple markets**: Georgia (primary), South Dakota, Nebraska, and possibly Mexico. It appears random: not every machine is affected, it doesn't correlate to time of day, and it has **never been reproduced in the QA lab**. Locations sometimes reboot machines on their own without contacting JVL, meaning the true scale is likely **larger than reported**.

**Business impact is severe.** Georgia machine sales dropped from ~50/month to 1/month (March 2026). Machines with newer software underperform older versions by up to 50% — potentially explained by unreported freeze downtime. Operator confidence is eroding. Val Levitan characterized this as **"JVL's silent killer."**

---

## 2. Investigation Timeline

### Phase 1: Initial Discovery & Field Reports (March 9)

**Source:** Georgia Machine Freezing Summary meeting (Juan Martinez, Felipe Miranda Giorgi, Genadi Peari, Pavel Frolov)

The first structured investigation meeting established the problem's scope:

- **Georgia:** FLEX D27 machines freezing intermittently, typically 2–3 days after boot. One frozen machine at a field location remained inoperable for **over a week** before anyone noticed (Valentine's Day incident). Of 10 machines prepared in the warehouse, 4 froze within days while 6 did not.
- **Florida:** 3+ years of operation with no real freezing (except reversed CPU fan cases).
- **South Dakota:** Random failures to reconnect to host system each morning. Not all machines affected.
- **Nebraska:** One freeze report (CS-442 in JIRA). Denis went on-site, found machine completely frozen.

**Initial theories explored:**
- **Loose SSD connector** — dismissed (connectors are binary: in or out)
- **Temperature/overheating** — ruled out (tilt system detects high temps correctly; freezes occur even when CPU is cold)
- **Insufficient RAM** — historical factor on 8GB machines, not current issue on 16GB
- **NVMe SSD adapter** (leading theory at this point) — current Tank motherboard uses NVMe-to-PCIe adapter with long wire traces and potentially inadequate capacitors; Sapphire ("Mexico") board with native NVMe slot had not frozen
- **Software-driven SSD access** — Pavel confirmed video files are still read from SSD at runtime; new software may do more intensive reads
- **Memory leak** — Claude AI analysis flagged it, but Pavel confirmed memory stabilizes at ~5.1 GB after boot

**Key data point:** ~250 Altera machines in Georgia with the same motherboard/adapter configuration have **not** had reported freezing — complicating the pure hardware theory.

### Phase 2: Scoping & Market Priorities (March 10)

**Source:** IP-106 alignment scheduling meeting (Val Levitan, Pavel Frolov, Genadi Peari)

Val established market priorities: Texas (#1), Nebraska (#2), Georgia freezing (#3). He emphasized that while the freezing isn't the sole cause of Georgia sales decline, it compounds every other problem.

The team explored a **video resource stress hypothesis**: new software may load more video assets simultaneously, increasing GPU/SSD load. Pavel proposed experiments with the debug build to toggle video resources on/off on affected machines.

**Key observations:**
- Genadi and field reports indicated freezes occur predominantly during **bonus rounds** (when video resource load is highest)
- Pavel proposed a disk stress approach: run a script that continuously reads the same video file to compete with the game's SSD reads, to see if freeze frequency increases
- Discussion of putting FP10 (newer/more powerful) boards in test machines, but software isn't ready for that platform yet

### Phase 3: Monitoring Tool & Troubleshooting Direction (March 13)

**Source:** Georgia Freezing troubleshooting direction meeting (Val Levitan, Pavel Frolov, Anton Leshkevich)

Pavel formalized the diagnostic approach as **IP-1027** (JIRA), a dedicated monitoring tool product with three initial features:
1. **Metric Collector** — gathers system performance data (CPU, memory, disk I/O, SMART parameters)
2. **Data Exporter** — sends metrics to an external collection point (not the machine's own SSD) via network to a laptop or server in the same local network
3. **Disk Stress Loader** — adds controlled additional SSD read load to test the disk-access hypothesis

**Physical setup:** Felipe's laptop in the Georgia warehouse provides remote access (via remote desktop service) to the local network. From there, SSH into any test machine. Anton Leshkevich tasked with writing bash scripts (no Python on production machines; can install on alternate disk partition). Anton estimated 1–2 days full-time for initial framework, then periodic attention.

### Phase 4: Teams Chat Investigation (March 9–19, Segment 1)

**Source:** GA Freezing Issue Teams chat summary — Segment 1

This segment captures the full team's asynchronous investigation across ~10 days. Key developments:

**Theory: Framework/DC Synchronous Blocking (Anton Leshkevich)**
Anton proposed that the Framework pulls system state from DataCenter every frame synchronously. If DC stops responding (e.g., waiting for lottery system response), Framework appears frozen. Alexander Biratko pushed back: DC communicates with lottery only through SAS, not directly. Theory not fully dismissed but considered unlikely as sole cause.

**Theory: Printer / Java Machine Crash (Efim Podvoiski)**
Efim found crash logs showing a Java crash when accessing the printer library (March 17, 2026, 7:43 PM GMT). However, timing didn't match Denis's on-site visit. The sequence: machine froze → Denis rebooted → audit ticket printed successfully → logs collected → machine put in TRACE mode → machine froze again on main screen → second reboot resolved it. Efim proposed killing the DC process manually to test Framework behavior — Pavel expected Framework would detect and self-terminate, but agreed to verify.

**Theory: CPU Power Saving / COM Port Sleep (Juan Martinez)**
Juan asked about hidden BIOS power-saving features putting COM ports to sleep. Pavel confirmed they don't use power savings. Juan wondered about hidden BIOS features.

**Theory: AMD GPU Driver Issue (Genadi Peari)**
Genadi shared a Qubes OS forum post describing **identical freeze behavior on the same AMD Raven Ridge APU platform**. Forum discussed kernel-level GPU driver issues. Juan shared AMD kernel parameters used by other developers:
- `amdgpu.noretry=0` (disables retry on page faults)
- `amdgpu.gpu_recovery=1` (enables GPU recovery)
- `amdgpu.gfxoff=0` (disables GFXOFF feature)

Pavel noted JVL uses kernel 4.19 (older stable) and could try `amdgpu.noretry=0`.

**Critical Discovery: Watchdog Timer Non-Functional**

Val demanded a clear answer on why the watchdog isn't working. Investigation revealed:

- The `start_game.sh` script acts as a **software watchdog**: if framework terminates, it collects crash logs and forces reboot. But Pavel emphasized they've **never seen crash logs from a frozen EGM** — the OS itself is dead, so this watchdog can't help.
- Pavel found a disabled parameter: `#define USE_HOPPER_IN_AS_WATCHDOG_RESET 1` (commented out) — an optional channel using the hopper input as a reset trigger.
- **Final answer from Pavel:** *"Currently we do not have external Watchdog wired. CPU hosted watchdog is not enabled on current software."*
- Val confirmed his recollection that JVL previously had a standalone hardware watchdog chip, removed or disconnected during a hardware revision.

**REQ-1028 Drafted:**
Juan Martinez drafted requirement REQ-1028 in JIRA: "EGM Auto-Restart and Watchdog Recovery System for Freeze Detection." Val corrected the framing: the requirement should state *"A machine should auto-recover in the event it permanently froze"* — not prescribe a watchdog timer (that's an engineering solution, not a requirement).

**Test Machines:**

| Cabinet | Serial Number | Software | Build |
|---------|--------------|----------|-------|
| FLEX D27 | CM08-0825-230234 | GCOAM-1.14.2.4.3.4.1 | 3817 |
| FLEX D27 | CM08-0324-229600 | GCOAM-1.14.0.4.3.4 | 3804 |
| FLEX V43 | CM08-1224.230227 | DLKG-1.13.0.4.3.4.2 | 3847 |

Anton ran CPU stress testing (~90% utilization) — no freeze triggered.

### Phase 5: Manufacturer Response (March 20–24)

**Source:** FP10 Motherboard Manufacturer Email Chain (Genadi Peari ↔ Hilda Huang, Maxtang/Datang)

Genadi contacted the FP10 motherboard manufacturer (Maxtang). Their engineering team responded with:

**Priority 1 — System & Kernel:**
- Confirm whether issue started after kernel/OS upgrade
- Try rolling back to previously stable kernel

**Priority 2 — GPU Driver Stack:**
- Reinstall/update Mesa graphics library and AMD GPU firmware
- Check `dmesg` logs for **"AMDGPU hang"** and **"gpu reset"** keywords
- **Upgrade kernel to Linux 5.10 or 5.15 LTS**

**Critical manufacturer statement:**
> *"The Vega 8 integrated GPU on the FP10 is sensitive to Linux kernel versions. We do not recommend using non-LTS kernels below 5.4 or above 6.0; please prioritize the officially validated 5.10/5.15 LTS versions instead."*

**JVL is running Linux kernel 4.19 — below the manufacturer's minimum recommended version of 5.4.**

**Hardware Watchdog Confirmed:**
The FP10 has an **onboard hardware watchdog** configurable through BIOS (Advanced tab → Watch Dog Configuration → set WDT Timeout Mode). This is the IT8786 SuperIO chip watchdog — separate from the APU's internal watchdog.

**Pavel's response** created a discrepancy: he stated they "currently use internal APU watchdog" — but this appears to conflict with his Teams chat statement that *"CPU hosted watchdog is not enabled on current software."* The actual status of which watchdog is active in production requires clarification.

**Diagnostic available:** Check `dmesg` for "AMDGPU hang" and "gpu reset" — quick, zero-risk check on any machine after a freeze.

### Phase 6: Watchdog Architecture Decision (March 24 AM)

**Source:** FP10 Freezing Issue Watchdog Discussion meeting (Val Levitan, Pavel Frolov, Alexander Biratko)

The team evaluated three watchdog approaches:

1. **CPU-internal (APU) watchdog** — Pavel estimates 95% reliable, but if the CPU itself is the problem (which evidence suggests), it may not trigger.
2. **FP10 SuperIO chip (IT8786) watchdog** — external to CPU, configurable via BIOS. Requires either manual BIOS change per machine or new BIOS firmware from manufacturer flashed via USB.
3. **IO board custom watchdog** (Alexander Biratko's proposal) — leverage existing Framework→DC→IO board heartbeat (every 200ms). Add firmware logic: if heartbeat stops, IO board triggers reset via physical wire to motherboard reset pins. **Most elegant solution: hardware-agnostic, works on any future motherboard.**

**Decision: IO board watchdog (option 3).**

Val's reasoning: the CPU is the suspected problem, so a CPU-internal watchdog is unreliable. The IO board solution is independent of any specific motherboard and survives platform changes.

**Additional decisions:**
- **Linux kernel upgrade to 5.15 LTS** — decided as parallel track. Can be done independently of BIOS changes.
- Alexander Biratko to lead IO board watchdog implementation, with Pavel's support.
- Genadi to identify physical pins on the IO board P2 connector for reset signal.
- Estimated timeline: ~1 week.

### Phase 7: Kernel Logging & Systematic Approach Debate (March 24 PM)

**Source:** IO-centric Watchdog wiring meeting (Val Levitan, Pavel Frolov, Alexander Biratko, Genadi Peari)

Extended discussion about how to capture crash evidence when the OS itself dies:

**Kernel serial console logging:**
Pavel proposed connecting machines to external computers via serial port. The kernel serial console would output register dumps and crash information even when the filesystem is dead. However, Alexander raised a critical point: a **hang** (infinite loop) may produce no crash output at all — unlike a crash (kernel panic), a hang just silently runs in circles.

**Val's scaled proposal:** Build 10 monitoring boxes (~$300 each), deploy them in Georgia machines in the JVL shop with employees playing constantly to generate game activity.

**Genadi's pushback — the "systematic approach" argument:**
Genadi made a sustained argument that the team's approach is unsystematic. Key points:
- *"I don't believe we've done everything that could be done"*
- The IO board-not-found problem (years-long) was solved in 15 minutes after consulting Alekseev — perhaps this freezing problem similarly needs a fresh expert perspective
- Simply upgrading the kernel without understanding why is following manufacturer advice on faith, not systematically
- The team needs a dedicated lead on this — Pavel's bandwidth is spread across too many responsibilities
- The `amdgpu.noretry=0` kernel parameter was already added to the Texas build but never tested for freezing

**5 Bulldog machines being brought to Georgia warehouse** for monitored testing. Alexander proposed splitting them: half on old software, half with the new kernel parameter, to build statistical evidence.

**Genadi's historical correction:** Freezes have existed **since the FLEX product's inception**, not just since the new software version. In casinos, operators knew to reboot; on field locations, machines were inaccessible. The problem looks like it's trending upward, but may be a random distribution with more observation now.

### Phase 8: Software Version Analysis & South Dakota Issue (March 25 AM — 9:32)

**Source:** "Digging into Freezing Issues" meeting (Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko)

Val shifted the investigation approach: instead of only looking at hardware, **chronologically isolate what changed in software** between the working old version and the freezing new version.

**Software architecture context:**
- Stack: HAL (hardware abstraction) → DC (data center / application logic) → SAS protocol → Framework (display/game engine)
- Original releases: ~v1.12/1.17 on "Pech 123" machines
- Current release: **v1.14** — added dual SAS connections, printer support, new skill
- HAL between Class 3 and Georgia is "99.9% identical" — changes were in the **DC layer**
- Printer code was added at DC level, not HAL. Both Sasha (Alexander) and Zhenya contributed.
- In Georgia, **printers are not physically installed**, but the printer code is in the build.

**New observation:** Casino machines are **rebooted daily**, which may mask freezing. Georgia field locations may not power-cycle as frequently, allowing freezes to accumulate visibility.

**Separate issue discovered — South Dakota QR Code Race Condition:**
Machines crash and reboot when scanning QR codes. Root cause identified and reproduced: a **race condition** where all games are disabled via SAS lock, and before the DC can set a tilt state, the Framework queries for available games, sees zero games, and crashes. The game-disable and tilt-activation operations are **sequential rather than transactional**.

**Decision: Claude Code review** of DC and HAL changes between old and new versions. Alexander skeptical of abstract results, but Val argued that engineers with domain knowledge can judge which AI findings are serious vs. noise.

### Phase 9: External Consultant & Monitoring Architecture (March 25 AM — 11:03)

**Source:** Freezing Investigation follow-up with Alekseev (Val Levitan, Pavel Frolov, Evgeniy Alekseev, Alexander Biratko, Genadi Peari)

Val brought in **Evgeniy Alekseev** as an external specialist. Val opened: *"Mistakes are made by those who do things — no finger-pointing, only facts."*

**Alekseev's hypotheses:**
1. **Memory management issues** (90% probability in his estimation) — memory leaks, pointer errors, stack overflows in C++ code
2. **Printer driver async communication** — synchronous printer commands could cause hangs; needs separate thread with command queue
3. **Chip/processor errata** — manufacturer-documented bugs with workarounds should be checked

**Technical debate: Memory errors vs. Linux protection**
- Alekseev: memory corruption can cause hard freeze even on Linux
- Pavel: x86 + Linux hardware memory protection prevents application from corrupting kernel memory; application crashes (segfault) but kernel survives
- Resolution: both agreed to investigate memory as diagnostic exercise; Pavel acknowledged edge cases may exist for their specific kernel/processor combination

**Printer code finding:**
When Pavel opened the actual printer HAL code (`l_printer`), he found **mutex locks throughout** — contradicting Alekseev's assumption of missing thread safety. However, Alekseev's code (based on a template) apparently does **not** have mutexes. Claude Code's AI analysis had independently found potential concurrent access issues.

**New untested hypothesis — DC death → extended Framework freeze:**
Pavel raised: when DataCenter is killed, Framework freezes on its socket read. **They've never tested what happens if DC dies and the machine sits for hours.** The Georgia morning freezes could be this exact scenario: DC dies during the night, Framework hangs on dead socket, machine appears frozen by morning. Alexander noted the old version (Pech 1) should have handled DC death with a reboot or tilt — a behavioral change between versions is a significant clue.

**Decisions:**
- Build a **resource monitoring daemon** (bash utility) — monitors memory, file descriptors, sockets, threads, stack usage. Independent process with unbuffered writes.
- Deploy to all 5 Georgia test machines.
- **Make monitoring part of standard architecture** — pre-release QA gate and production diagnostic, not a one-off tool.
- Connect **SAS emulator** to test machine with stress-test command loop.

---

## 3. Theories — Status Tracker

| # | Theory | First Raised | Status | Evidence For | Evidence Against | Next Step |
|---|--------|-------------|--------|-------------|-----------------|-----------|
| 1 | **NVMe SSD adapter instability** | March 9 (Felipe/Pavel) | **Largely Ruled Out** | Tank board uses adapter with long traces | 250 Altera machines with same adapter haven't frozen; **Sapphire (Mexico) boards confirmed to also freeze** despite native NVMe (no adapter). Both boards share the same AMD APU — the common factor is the GPU/kernel, not the SSD interface. | Deprioritized. Kernel/GPU theory now dominant. |
| 2 | **Temperature/overheating** | March 9 | **Ruled Out** | Historical cases with reversed fans | Tilt system detects temps correctly; freezes occur in cold conditions | None — closed |
| 3 | **Insufficient RAM** | March 9 | **Ruled Out** | Historical 8GB machines had issues | Current 16GB machines still freeze; memory stabilizes at ~5.1GB | None — closed |
| 4 | **AMD Vega 8 GPU / kernel incompatibility** | March ~15 (Genadi) | **Leading Theory** | Identical symptoms on same APU in Qubes OS forum; manufacturer explicitly says Vega 8 is sensitive to kernel version; JVL runs 4.19, manufacturer minimum is 5.4 | Not yet tested; `amdgpu.noretry=0` added to Texas build but not evaluated | Upgrade to kernel 5.15 LTS; check `dmesg` for "AMDGPU hang" |
| 5 | **Framework/DC synchronous blocking** | March ~12 (Anton) | Open | Framework pulls state every frame; if DC hangs, Framework appears frozen | DC communicates with lottery via SAS only, not directly | Test DC-kill extended timeout scenario |
| 6 | **Printer / Java crash cascade** | March ~17 (Efim) | Open | Java crash log found at printer library access; printer DC code may lack mutexes | HAL printer code has mutexes; timing didn't match Denis visit; printers not installed in Georgia | Claude Code review of DC printer code; verify mutex coverage |
| 7 | **CPU power saving / COM port sleep** | March ~15 (Juan) | Open (low priority) | Could explain intermittent COM failures | Pavel says no power savings configured | Check BIOS for hidden features |
| 8 | **Memory management issues (leaks, pointers)** | March 25 (Alekseev) | Open | Common cause of hard freezes; Alekseev rates 90% | Linux memory protection should prevent kernel-level impact; memory appears to stabilize post-boot | Run static analyzer on C++ code (HAL/Framework) |
| 9 | **DC death → Framework socket hang** | March 25 (Pavel) | **Untested — High Priority** | Never tested over extended time; morning freezes in Georgia fit the pattern; old version handled DC death differently | Theoretical — no direct evidence yet | Kill DC, wait hours, monitor Framework behavior; compare old vs. new version |
| 10 | **Video resource load during bonus rounds** | March 10 (Pavel/Genadi) | Open | Field reports indicate freezes predominantly during bonus rounds; new software has more video assets | CPU stress test didn't trigger freeze | Test with debug build toggling video resources |

---

## 4. Architectural Decision Records (ADRs)

### ADR-001: IO Board Watchdog Timer Implementation

**Date:** March 24, 2026
**Status:** Decided — implementation in progress
**Deciders:** Val Levitan (final), Alexander Biratko (proposal), Pavel Frolov (technical validation), Genadi Peari (hardware consultation)

**Context:** The hardware watchdog timer — the safety net that should automatically reboot a frozen machine — is completely non-functional. No external watchdog hardware is wired, and the CPU's built-in watchdog is disabled. A commented-out code parameter (`#define USE_HOPPER_IN_AS_WATCHDOG_RESET 1`) confirmed it was intentionally disabled during a hardware revision.

**Options Considered:**
1. **CPU-internal (APU) watchdog** — simplest to enable but unreliable if the CPU itself is the failure point (which evidence suggests). Pavel estimates 95% reliable.
2. **FP10 SuperIO chip (IT8786) watchdog** — external to CPU, configurable via BIOS. Requires per-machine BIOS modification (manual or via USB firmware flash from manufacturer). Board-specific: won't transfer to future platforms.
3. **IO board custom watchdog** — leverage existing Framework→DC→IO board heartbeat path (200ms interval). IO board firmware monitors heartbeat; if it stops, triggers hardware reset via physical wire from IO board to motherboard reset pins.

**Decision:** Option 3 — IO board watchdog.

**Rationale:**
- **Hardware-agnostic:** Works on any motherboard (current FP10, future Omni platform) — no rework when changing boards
- **Independent of CPU:** If the CPU/GPU is the failure source (as evidence suggests), a CPU-internal watchdog may fail alongside it
- **Leverages existing infrastructure:** The heartbeat path already exists; only firmware modification and one physical wire needed
- **Field-upgradeable:** IO board firmware can be updated without regulatory resubmission

**Implementation:**
- Alexander Biratko leads, Pavel Frolov supports
- Genadi Peari identifies physical pins on IO board P2 connector (already has line buffer on this line)
- One wire connects IO board output pin to motherboard reset pin
- Firmware change: IO board maintains counter, reset on each heartbeat. Counter reaches zero → trigger reset.
- Estimated: ~1 week
- Val directed that Alekseev should **not** be assigned this work (assigned to Alexander instead)

**Trade-off acknowledged:** With any watchdog (CPU-based or IO-based), a frozen machine reboots **without capturing diagnostic information** about the freeze cause. This is accepted as the pragmatic path: user impact is reduced even without root cause identification.

### ADR-002: Linux Kernel Upgrade to 5.15 LTS

**Date:** March 24, 2026
**Status:** Decided — planning in progress
**Deciders:** Val Levitan (final), Pavel Frolov (technical), Alexander Biratko (cautioned on testing)

**Context:** JVL runs Linux kernel 4.19. The FP10 motherboard manufacturer (Maxtang) explicitly states the Vega 8 GPU is sensitive to kernel versions and recommends 5.10 or 5.15 LTS. Independent forum posts describe identical freeze behavior on the same AMD Raven Ridge APU with older kernels.

**Decision:** Upgrade to Linux kernel 5.15 LTS.

**Rationale:**
- Manufacturer's primary recommendation
- Forum evidence of identical symptoms resolved with kernel upgrade
- 5.15 is LTS (long-term support) — stable and well-tested
- The AMD GPU driver for Vega 8 is **built into the kernel** — upgrading the kernel upgrades the GPU driver

**Risks & Mitigations:**
- Alexander cautioned: *"We need to test this well."* Previous kernel upgrades revealed unforeseen hardware compatibility issues that only appeared after extended testing.
- Pavel: *"You can upgrade, everything seems to work, but then you catch unexpected issues with some hardware that you don't see immediately — you need manual testing across everything."*
- Mitigation: thorough manual testing before field deployment; maintain ability to roll back.

**BIOS change NOT required** for the kernel upgrade (contrary to initial concern). The kernel can be upgraded independently of the OS or BIOS.

### ADR-003: Atomic State Transitions in DC/Framework Interface

**Date:** March 25, 2026
**Status:** Identified — needs formal decision
**Context:** South Dakota QR code scanning crash

**Problem:** The game-disable and tilt-activation operations in the DC are **sequential rather than transactional**. Between disabling the last game and setting the tilt state, the Framework can query for available games, see zero games (with no tilt set), and crash.

**Proposed direction:** Game disable + tilt activation must happen atomically (in one transaction). Val questioned the interface architecture: *"The framework should tell the DC 'wait, it's not your time to ask'"* and *"I still insist that our interface between file lock and DC is wrong."*

**Status:** Root cause confirmed and reproduced. Fix approach implied but not formally specified. Alexander Biratko and Zhenya assigned.

### ADR-004: System Resource Monitoring as Architectural Component

**Date:** March 25, 2026
**Status:** Decided — implementation starting immediately
**Deciders:** Val Levitan (proposed and decided), Pavel Frolov, Alexander Biratko (agreed)

**Context:** The team has been unable to diagnose freezes partly because there is no continuous monitoring of system health. Freeze events leave no logs because the OS is dead when they occur.

**Decision:** Build a **system resource monitoring daemon** that becomes a permanent part of the software architecture — not a temporary diagnostic tool.

**Specification:**
- Independent daemon (bash script initially) — not embedded in Framework or DC
- Monitors: memory consumption, file descriptors, sockets, thread count, stack usage
- Unbuffered writes to its own log file (data survives even if system freezes mid-write)
- Lightweight enough for production deployment
- Dual purpose: pre-release QA checkpoint (must run clean for N period before release) and production diagnostic

**Val's architectural philosophy:** *"Roads can work without traffic lights and curbs, but you build them anyway."* Monitoring is a guardrail, not an afterthought.

### ADR-005: Framework Socket Timeout on DataCenter Death (Proposed)

**Date:** March 25, 2026
**Status:** Proposed — pending investigation results
**Context:** Framework hangs indefinitely when DataCenter dies because it blocks on socket reads with no timeout.

**Proposed:** Implement timeout and health check on the Framework→DataCenter socket connection. If DataCenter doesn't respond within a defined period, Framework should enter tilt state or trigger a reboot — not hang indefinitely. The old version (Pech 1) reportedly handled this correctly.

---

## 5. Key Decisions & Directives (Chronological)

| Date | Decision | Decided By | Context |
|------|----------|-----------|---------|
| March 9 | Halt Georgia machine shipments until freezing is resolved | Juan (recommended), Val (approved) | Machines underperforming by 50%; operator confidence eroding |
| March 9 | Priority #1 is reproducing the freeze in test environment | Team consensus | Cannot systematically fix what cannot be reproduced |
| March 10 | Market priorities: Texas #1, Nebraska #2, Georgia freeze #3 | Val | Resource allocation across multiple markets |
| March 13 | Create monitoring tool (IP-1027) as dedicated JIRA product | Pavel | Formalized as Metric Collector + Data Exporter + Disk Stress Loader |
| March ~17 | REQ-1028 drafted: EGM auto-recovery requirement | Juan (drafted), Val (corrected framing) | Val: requirement should be solution-agnostic, not prescribe watchdog |
| March 24 | IO board watchdog (ADR-001) | Val (final), Alexander (proposed) | Hardware-agnostic, independent of CPU, field-upgradeable |
| March 24 | Linux kernel upgrade to 5.15 LTS (ADR-002) | Val (decided), team (agreed with caution) | Manufacturer recommendation; JVL running below minimum |
| March 24 | Request new BIOS firmware from Maxtang with watchdog enabled by default | Val → Genadi | For new boards from manufacturer; existing boards need USB flash |
| March 24 | `amdgpu.noretry=0` kernel parameter added to Texas build | Pavel | Already in a shipped build but never evaluated for freezing |
| March 25 | Claude Code review of DC and HAL changes | Val (decided), Alexander (executing) | Compare old working version vs. new freezing version |
| March 25 | Pull Zhenya off current work to focus on freezing | Val | Both Alexander and Zhenya to concentrate on this |
| March 25 | Listen constructively to Alekseev's concerns | Val (directed) | *"Instead of taking it as an attack, let's say OK, what's the error?"* |
| March 25 | Build resource monitoring daemon (ADR-004) | Val (decided), team (agreed) | Permanent architectural component, not temporary tool |
| March 25 | Connect SAS emulator to test machine for stress testing | Val | Exercise framework with meaningful SAS commands |
| March 25 | Make monitoring a pre-release QA gate | Val / Pavel | Software cannot ship until monitoring runs clean for defined period |

---

## 6. Fundamental Shifts in Policy & Attitude

### Shift 1: From "Reproduce First" to Parallel-Track Investigation

**Before (March 9–19):** The team's position was that reproducing the freeze was the absolute prerequisite: *"Priority #1 is reproducing the freeze."* Without reproduction, all other work was considered speculative.

**After (March 24–25):** Val directed a parallel-track approach:
- Track A: Continue trying to reproduce (monitoring tool, stress testing)
- Track B: Implement watchdog as pragmatic mitigation regardless of root cause
- Track C: Upgrade kernel based on manufacturer recommendation
- Track D: Code review to find potential instabilities

This shift acknowledges that the long feedback cycle (weeks between freeze events) makes a pure "reproduce first" strategy untenable given the business urgency.

### Shift 2: From Defensive to Constructive Reception of External Input

**Before:** When Alekseev raised concerns about printer code quality, Pavel's initial reaction was defensive: *"The same code worked in Class 3."* Similarly, when Genadi cited the manufacturer's email, there was initial resistance: *"We already did that"* or *"That won't work on our kernel."*

**After:** Val explicitly directed constructive engagement: *"Instead of taking it as an attack, let's say OK, what's the error? Let's figure it out."* And: *"Mistakes are made by those who do things — no finger-pointing, only facts."* The March 25 Alekseev meeting demonstrated this shift in practice: despite several of Alekseev's specific claims being challenged, his hypotheses productively guided the investigation.

### Shift 3: Monitoring as Architecture, Not Afterthought

**Before:** Monitoring was an ad-hoc diagnostic tool (IP-1027) — a temporary measure to capture data during the investigation.

**After (March 25):** Val elevated monitoring to a **permanent architectural component**: a pre-release QA gate and production diagnostic tool. *"Roads can work without traffic lights and curbs, but you build them anyway."*

### Shift 4: Genadi's "Systematic Approach" Challenge

**March 24 PM:** Genadi Peari made a sustained argument that the team's approach was unsystematic. His key challenge: the IO-board-not-found problem was years-long and solved in 15 minutes after consulting Alekseev. He pushed for:
- Consulting external experts rather than only relying on internal knowledge
- Dedicated leadership for the freezing investigation (Pavel is spread too thin)
- Capturing kernel logs properly rather than accepting "they can't be captured" at face value
- Testing the manufacturer's recommendations on actual freezing machines before dismissing them

This challenge influenced Val's decision to bring in Alekseev on March 25 and to adopt the parallel-track approach.

---

## 7. Consolidated Undertakings

### Active Undertakings (as of March 25, 2026)

| # | Who | What | Assigned | Priority | Status | Source Meeting |
|---|-----|------|----------|----------|--------|---------------|
| U-01 | Alexander Biratko | Lead IO board watchdog firmware implementation (ADR-001). Identify pins with Genadi, write firmware with Pavel's support. | March 24 | High | In Progress | Watchdog Discussion (AM) |
| U-02 | Genadi Peari | Identify physical pins on IO board P2 connector for watchdog reset signal. Verify line buffer and pin availability. | March 24 | High | In Progress | IO Watchdog Wiring (PM) |
| U-03 | Genadi Peari | Contact Maxtang manufacturer to produce new BIOS firmware with watchdog enabled by default; deliverable as USB-flashable image. | March 24 | High | Assigned | Watchdog Discussion (AM) |
| U-04 | Pavel Frolov | Build Linux kernel 5.15 LTS for the JVL platform. Test thoroughly before field deployment. | March 24 | High | Assigned | Watchdog Discussion (AM) |
| U-05 | Alexander Biratko + Zhenya | Run Claude Code review on DC and HAL changes between old version (Pech 123) and v1.14. | March 25 | High | Assigned | Digging into Freezing (AM) |
| U-06 | Irina Shishko | Provide exact version numbers — version on first Pech 123 machines and currently deployed version — for precise diff. | March 25 | High (blocker for U-05) | Assigned | Digging into Freezing (AM) |
| U-07 | Alexander Biratko + Zhenya | Fix South Dakota QR code race condition — make game disable + tilt activation atomic. | March 25 | High | Assigned | Digging into Freezing (AM) |
| U-08 | Pavel Frolov | Ask Claude Code for comprehensive system monitoring parameters list; circulate to team. | March 25 | High | Assigned (immediate) | Alekseev Follow-up |
| U-09 | Pavel Frolov + Claude Code | Write v1 of bash monitoring daemon based on parameter list. | March 25 | High | Assigned (same day) | Alekseev Follow-up |
| U-10 | Alexander Biratko | Deploy monitoring utility to 5 Georgia field machines via Anton. Unbuffered I/O. | March 25 | High | Pending (after U-09) | Alekseev Follow-up |
| U-11 | Alexander Biratko | Connect SAS emulator to one test machine; create stress-test loop of meaningful SAS commands. | March 25 | High | Assigned | Alekseev Follow-up |
| U-12 | Pavel / Alexander | Test DataCenter-kill extended timeout scenario (kill DC, wait hours, monitor Framework). Compare old vs. new version. | March 25 | High | Assigned (TBD timing) | Alekseev Follow-up |
| U-13 | Team (future) | Run static analyzer on C++ code (HAL/Framework) for memory leaks and out-of-bounds access. | March 25 | Medium | Not started | Alekseev Follow-up |
| U-14 | Pavel Frolov | Review specific commits between old version and v1.14, identifying DC and HAL changes. | March 25 | High | Assigned | Digging into Freezing (AM) |

### Earlier Undertakings (March 9–13, status uncertain)

| # | Who | What | Assigned | Status |
|---|-----|------|----------|--------|
| U-E1 | Juan Martinez | Send company-wide email recommending halt to Georgia shipments | March 9 | Likely completed |
| U-E2 | Felipe Miranda Giorgi | Collect and distribute log files from frozen machine | March 9 | Status unknown |
| U-E3 | Felipe Miranda Giorgi | Contact Camilo in Mexico re: Sapphire board freezing | March 9 | Status unknown |
| U-E4 | Felipe Miranda Giorgi | Implement 3-day burn-in testing protocol | March 9 | Status unknown |
| U-E5 | Pavel Frolov | Experiment: simulate SSD read failures to test freeze reproduction | March 9 | Partially attempted (March 10 — crude test, needs refinement) |
| U-E6 | Genadi Peari | Evaluate hiring specialist for low-level hardware/software debugging | March 9 | Status unknown |
| U-E7 | Anton Leshkevich | Build monitoring tool framework (IP-1027): metric collector, data exporter, disk stress loader | March 13 | In progress (Bash scripts) |

---

## 8. People & Roles

| Person | Title/Role | Involvement |
|--------|-----------|-------------|
| **Val Levitan** | CEO/Director | Investigation sponsor; sets priorities and direction; drives urgency |
| **Pavel Frolov** | Director of Engineering | Deepest technical knowledge; leads most technical analysis; bandwidth constrained |
| **Genadi Peari** | Electromechanical Dept. Manager | Hardware expertise; manufacturer liaison; pushes for systematic approach |
| **Alexander Biratko** | Developer | Proposed IO board watchdog; leads firmware work; DC/Framework architecture knowledge |
| **Anton Leshkevich** | Developer | Monitoring tool implementation; remote machine management in Georgia |
| **Irina Shishko** | Version/Release Manager | Tracks software versions and release history |
| **Evgeniy Alekseev** | External Consultant | Brought in March 25 for outside perspective; printer code author; memory management hypothesis |
| **Juan Martinez** | US Operations | Drafted REQ-1028; field liaison; Claude AI analysis of logs |
| **Felipe Miranda Giorgi** | Georgia Field Operations | Machine setup, log collection, on-site testing |
| **Efim Podvoiski** | Developer | Found Java/printer crash log in dc.log |
| **Zhenya (Evgeniy) Khaletsky** | Developer | SAS emulator work; assigned to freezing analysis March 25 |
| **Denis** | Field Technician | On-site freeze investigation; Nebraska CS-442 |
| **Dima Pikuli** | Original Software Author | Referenced historically (helped with IO board-not-found problem) |
| **Hilda Huang** | Maxtang Sales Manager | Manufacturer contact for FP10 board; relayed engineering team's kernel/watchdog recommendations |

---

## 9. Open Questions

### High Priority
1. **Does killing DataCenter and waiting hours reproduce the morning freeze?** (Pavel's hypothesis — never tested)
2. **What exactly changed in the DC logic between the old and new versions?** (Waiting on Irina's version numbers)
3. **Why does newer software appear to freeze more frequently than older versions?** Freezing has existed since the FLEX product's inception, but newer software may increase frequency. Code review is meant to identify what changed.
4. **What is the final watchdog timer decision?** Three options were discussed progressively (see Edge Case 3 resolution below) but no final implementation path has been locked.
5. **What specific concurrent access issues did Claude Code find in the printer/HAL code?** (Referenced by Pavel on March 25 but not detailed)

### Medium Priority
6. **Are there memory leaks in the C++ framework or HAL?** (Alekseev's primary hypothesis; needs static analyzer)
7. **Can SAS command stress testing trigger the freeze?** (None of the test machines currently have SAS connected)
8. **Does the `amdgpu.noretry=0` kernel parameter help?** (Already in Texas build but never evaluated for freezing)
9. **Could daily power cycling in casinos mask the freezing issue?** (Pavel's hypothesis — not investigated)

### Lower Priority / Long-term
10. **Why do ~250 Altera machines with the same motherboard/adapter configuration not exhibit freezing?**
11. **Why did test machine serial 229600 stop freezing on its own after Jan 29 with no changes?**
12. **Is the 50% revenue underperformance of new nudge machines explained by unreported freezes or a separate software/math issue?**
13. ~~Have machines shipped to Mexico (Sapphire boards) experienced freezing?~~ **Resolved:** Yes, confirmed by Val. Sapphire boards freeze too. NVMe adapter theory largely ruled out.

---

## 10. Edge Cases — Resolved

The following items were ambiguous across the source materials. Resolved with Val's input on March 25.

### Edge Case 1: Freezes have always existed — RESOLVED

**Original ambiguity:** Some meetings framed the problem as "new machines freeze, old machines don't." Genadi stated freezes have existed since the FLEX product's inception.

**Resolution (Val confirmed):** Freezing has always existed. In casinos, operators knew to reboot; on field locations, machines were inaccessible and freezes went unreported. The new software likely **increased the frequency** rather than introduced the problem — possibly by adding more video resources and GPU load, which increases the probability of triggering the underlying AMD/kernel issue.

**Impact on investigation:** The root cause is likely the same AMD Vega 8 / kernel 4.19 incompatibility that has always been present. The code review of DC changes should focus on what increased the trigger frequency, not on finding a newly introduced defect.

### Edge Case 2: Sapphire (Mexico) boards also freeze — RESOLVED

**Original ambiguity:** March 9 meeting stated Sapphire boards "had not exhibited freezing." Genadi later said Mexico reported freezes.

**Resolution (Val confirmed):** Sapphire boards freeze too. This is now confirmed.

**Impact on investigation:** The NVMe SSD adapter theory is **largely ruled out** — both Tank boards (with adapter) and Sapphire boards (native NVMe, no adapter) freeze. The common factor is the AMD Raven Ridge APU and Linux kernel 4.19. This significantly strengthens the kernel/GPU theory (Theory #4) as the primary root cause. Theory #1 (NVMe adapter) has been downgraded accordingly in the Theories Status Tracker.

### Edge Case 3: Pavel's watchdog statements — RESOLVED (progressive, not contradictory)

**Original ambiguity:** Pavel appeared to say different things about watchdog status across three dates.

**Resolution (Val clarified):** The statements are **progressive**, not contradictory — they reflect an evolving situation:

1. **~March 19 (Teams chat):** Pavel confirmed that although the FP10 hardware has watchdog timer chips, **JVL's software was not communicating with any of them.** No watchdog of any kind was active in production software. This was the baseline discovery.

2. **March 24 AM (email reply to manufacturer):** Pavel was **discussing the ways of engaging** one of the hardware watchdog timers — specifically the FP10's SuperIO chip (IT8786) watchdog that the manufacturer confirmed exists in BIOS. He noted they had previously tried to use it but couldn't ping it "due to lack of specification." This was exploration, not a claim of current production status.

3. **March 24 PM (meeting):** Pavel and Alexander further proposed the **IO-board-centric software watchdog** — a different and more elegant approach that would use the existing heartbeat path and a physical wire to the motherboard reset pins.

**Current status:** The final watchdog implementation decision **remains open**. Three options were identified but no single path has been locked. Field machines currently have **no active watchdog protection**. This is a key open question for the team to resolve.

---

## 11. Source Documents

All source materials reside in: `Transcripts/2026/03_March/Freezing/`

| File | Date | Type | Content |
|------|------|------|---------|
| GA_Machine_Freezing_Summary-March-9-2026.md | March 9 | Meeting summary | Initial investigation meeting — field reports, theories, action items |
| Freezing_GA-COAM-scope-March-10-2026.docx | March 10 | Raw transcript | Market priorities meeting — includes freezing scope discussion |
| Georgia_Freezing_troubleshooting_direction.docx | March 13 | Raw transcript | Monitoring tool planning — IP-1027 formalization |
| GA_Freezing_Issue_Segment_1_Initial_Investigation.docx | ~March 9–19 | Chat summary | Teams chat Segment 1 — theories, watchdog discovery, test machines |
| GA_Freezing_Issue_FP10_Manufacturer_Email.docx | March 20–24 | Email summary | Maxtang manufacturer response — kernel recommendation, hardware watchdog |
| FP10_Freezing_Issue_Watchdog_Discussion.docx | March 24 AM | Raw transcript | Watchdog options evaluation, kernel upgrade decision |
| I_O-centric_Watchdog_wiring.docx | March 24 PM | Raw transcript | IO board wiring, kernel logging, systematic approach debate |
| GA_Freezing_Issue_Executive_Summary.docx | March 24 | Executive summary | Summary of March 9–24 investigation (predecessor to this report) |
| Meeting_Notes_Freezing_Issues_Investigation-March-25-2026.md/.docx | March 25 (9:32 AM) | Meeting summary | "Digging into Freezing Issues" — software version analysis, SD race condition |
| Meeting_Notes_Freezing_Investigation-March-25-2026.md/.docx | March 25 (11:03 AM) | Meeting summary | Follow-up with Alekseev — memory hypothesis, monitoring daemon decision |
| transcript_Digging into Freezing issues-March-25-2026.docx | March 25 | Raw transcript | Source transcript for March 25 (9:32 AM) meeting |
| transcript_Freezing investigation-March-25-2026.docx | March 25 | Raw transcript | Source transcript for March 25 (11:03 AM) meeting |
| transcript_Freezing investigation.docx | March 25 | Raw transcript | Duplicate/variant of above transcript |

---

*This report supersedes the GA_Freezing_Issue_Executive_Summary.docx as the authoritative investigative record.*
*Next update due when: Irina provides version numbers, Claude Code review results arrive, or monitoring daemon produces first data.*
