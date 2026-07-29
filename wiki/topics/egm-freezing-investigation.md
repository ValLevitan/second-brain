---
type: topic
title: EGM freezing investigation (Georgia field fleet)
date: 2026-07-29
aliases: [GA freezing, Georgia freezing, machine freezing, EGM freeze, GA Freezing Issue, freezing investigation, JVL silent killer, nudge animation freeze, kernel-panic freeze]
source-count: 6
open-questions: 7
---

# EGM freezing investigation (Georgia field fleet)

This is the home page for JVL's investigation into gaming machines (EGMs) **freezing in the field** — the machine goes completely unresponsive, the screen locks, and only a physical reboot brings it back. Val called it **"JVL's silent killer"** and treated it as urgent, because it hits revenue and operator confidence directly. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]

This page covers **Part 1 of the investigation (March 9–13, 2026)** plus the manufacturer's technical reply that arrived March 20–24. The later work — the March 24 watchdog session, the March 25 investigation meeting, and the V1.3 full report — is expected in later material and this page is left open-ended.

The freeze has come up before across the wiki; see the earlier mentions and the direction the investigation later took:
- [[wiki/meetings/2026-02-12-genadi-echo-printer-freeze-flexport-bom.md]] — an earlier Feb-12 freeze discussion with Genadi.
- [[wiki/meetings/2026-03-10-ip-106-alignment-ga-coam-freezing-scope.md]] — the Mar-10 IP-106 call that opened with the freezing problem.
- [[wiki/meetings/2026-03-13-georgia-freezing-troubleshooting-direction.md]] — the Mar-13 call setting the test-harness direction.
- [[wiki/meetings/2026-03-26-initiative-priority-schedule.md]] — the Mar-26 call that turned the investigation into a shipped fix plan (kernel upgrade + the Option-4 CPU watchdog).
- [[wiki/meetings/2026-03-26-debate-with-efim-system-languages.md]] — the Mar-26 architecture debate, anchored partly to the freeze.
- [[wiki/meetings/2026-03-30-black-horse-invoice-payment-review.md]] — a Mar-30 update on the root cause & fix rollout.
- Home market context: [[wiki/projects/georgia-market-rollout.md]].

> **Note on sources.** Several inputs to this page are **AI-generated secondary/derived analyses** (a meeting summary, an executive summary, and a Teams-chat summary), not raw transcripts. They are marked as such below and their facts are captured once here rather than double-counted. The two underlying meetings have their own thin stubs (linked above).

## The symptom

- Machines freeze **intermittently**, typically **2–3 days after boot / software install**, sometimes never. No consistent trigger has been found. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- When frozen, the machine is **totally unresponsive** — screen locked, no recovery — and needs a physical reboot. [[raw/GA_Freezing_Issue_Executive_Summary.md]]
- It appears **random**: not every machine is affected, it does not happen at the same time of day, and it has **never been reproduced in the Minsk QA lab**. [[raw/GA_Freezing_Issue_Executive_Summary.md]]
- It spans multiple markets — **Georgia, South Dakota, Nebraska** — though Georgia is worst; **Florida** machines have run 3+ years with essentially no freezing (except old reversed-CPU-fan overheating cases). [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- **Underreporting:** locations sometimes just reboot the machine themselves without calling JVL, so the true scale is likely larger than reported. One frozen machine sat dead at a field location for over a week (discovered on Valentine's Day) before anyone noticed. [[raw/GA_Freezing_Issue_Executive_Summary.md]] [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- The freeze has **intensified since the new nudge software (the 38xx build series, e.g. 3804/3817/3847)** was deployed. Genadi noted (Mar-10) that in Georgia and Mexico the freezes mostly happened **in bonus rounds**, which fits a "lots of video playing at once" theory. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]] [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]

## Business impact (market economics)

- Georgia sales collapsed from roughly **50 machines/month to a single machine last month**; freezing is not the only cause but it is not helping. [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]
- Machines on the new nudge are **underperforming by up to ~50%** versus the old software — possibly explained by unreported freezes causing extended downtime. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- Operators are losing confidence and Felipe's sales have declined; Genadi warned customers will stop buying entirely if it isn't resolved. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]

## Leading hypotheses / root-cause candidates

The team explored several theories; **none was confirmed or fully ruled out** during Part 1.

- **NVMe SSD adapter (leading hardware theory as of Mar-9).** The current Tank motherboard connects the SSD through an **NVMe-to-PCIe adapter** with long wire traces and possibly weak capacitors, whereas the Sapphire ("Mexico") board with a **native NVMe slot** has not frozen. Not definitively proven. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- **Runtime SSD reads / video decoding.** After boot most data runs from RAM, but video files are still read from the SSD at runtime; the new software may read more intensively, and the correlation is with **frequency of SSD access** more than video-decode load. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]] [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]
- **AMD Vega 8 / Raven Ridge GPU driver + Linux kernel.** Genadi found a Qubes-OS forum thread describing identical freeze behaviour on the same **AMD Raven Ridge APU**, pointing at kernel-level GPU driver bugs. Suggested kernel parameters: `amdgpu.noretry=0`, `amdgpu.gpu_recovery=1`, `amdgpu.gfxoff=0`. JVL runs an older stable kernel (**4.19**). [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- **Framework/Datacenter communication blocking (Anton Leshkevich).** The Framework polls the Datacenter (DC) synchronously each frame; if the DC stalls, the Framework would look frozen. Biratka pushed back (SAS handles the lottery link), so it was considered unlikely as a sole cause. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- **Printer / Java crash (Efim Podvoiski).** Crash logs showed a Java crash accessing the printer library, which could leave the DC crashed and the Framework waiting on it. Proposed test: kill the DC process and watch the Framework. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- **CPU power-saving / COM-port sleep (Juan Martinez).** Could a power-saving or hidden BIOS feature put COM ports to sleep? Pavel confirmed no power-saving is used. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]

**Theories tested and set aside:**
- **Temperature / overheating** — ruled out; freezes occur with a cold CPU and the tilt system correctly detects high temps. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- **Insufficient RAM (8 GB)** — a historical factor for old cases, not the current issue on 16 GB machines. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- **Loose SSD connector** (Val's suggestion) — dismissed; connectors are in or out. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- **Memory leak** — Claude AI analysis flagged it, but memory stabilises at ~5.1 GB after boot, so not a leak. [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]

**Kernel-level / OS suspicion (the strongest signal):** no crash logs are ever collected after a freeze, which strongly suggests the **Linux OS itself becomes non-operational** — pointing at a hardware or kernel-level problem rather than a pure application bug. [[raw/GA_Freezing_Issue_Executive_Summary.md]]

## The watchdog discovery (the most actionable finding)

- The `start_game.sh` script acts as a basic **software watchdog** (on a framework crash it collects logs, tries to upload them, then reboots) — but since crash logs are never seen after a freeze, the OS is dead and this software watchdog can't help. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Val asked directly whether the board has a working **hardware watchdog**. Pavel's answer: **"Currently we do not have external Watchdog wired. CPU-hosted watchdog is not enabled on current software."** [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Pavel found a **commented-out (disabled) parameter** in the IO-board code — `#define USE_HOPPER_IN_AS_WATCHDOG_RESET 1` — confirming a reset trigger had been intentionally turned off at some point during a hardware revision. Val recalled JVL previously had a standalone hardware watchdog chip that was later removed/disconnected. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Two watchdog paths were identified: **(Option 4) add a CPU-based watchdog to all future releases** (Linux kernel + HAL), or **(Option 5) implement it on the IO board** (fixable by firmware update without regulator resubmission; needs one internal wire; Alekseev could do it). Both would reboot the machine **without capturing the freeze cause**. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- **Requirement REQ-1028** ("EGM Auto-Restart and Watchdog Recovery System for Freeze Detection") was drafted by Juan in JIRA. **Val corrected its framing** — the requirement should say only *"a machine should auto-recover if it permanently freezes,"* leaving the watchdog (the engineering solution) out of the requirement. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]

The later decision to **ship the Option-4 CPU watchdog together with the kernel upgrade** is recorded on the Mar-26 [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|initiative-priority]] stub, and the fix rollout on the Mar-30 [[wiki/meetings/2026-03-30-black-horse-invoice-payment-review.md|Black Horse]] stub.

## The Mar-10 and Mar-13 direction — build a measurement harness, don't "poke blindly"

- On the **Mar-10 IP-106 call** Val pushed the engineers off ad-hoc guessing ("stop poking a finger at the sky") toward a **controlled, measurable approach**: build a "jig"/harness that loads the machine and *measures* what happens, so a hypothesis (e.g. frequent SSD reads trigger the freeze) can be tested by dialling the load up or down and watching the freeze rate. [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]
- Practical steps agreed: put the "38xx" build back on machines that had stopped freezing so they resume; try a **stronger (and separately a weaker) CPU** on the same architecture rather than switching to the FPS board; and hand the problem to **Anton Leshkevich** — explaining the *problem* (not dictating the *solution*) so he can design the measurement jig. Test remotely via Felipe's on-site laptop; Elizabeth/Felipe can power-cycle. [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]]
- On the **Mar-13 call** Pavel formalised this as a JIRA product — **IP-1027, a "Monitoring Tool for Gaming Machine"** (split off from IP-688 diagnostic tool), with initial features: **metrics collector, data exporter, disk-stress loader**, and a **watchdog/"storilzh" (сторож)** — writing collected data **not to the machine's own SSD** but to an external USB or a **Python server on the in-network laptop**. A disk-stress load (frequent SSD reads) is added to make freezes appear more often. Anton to write the scripts first, then deploy to the 2–3 Georgia test machines (2 of which freeze reliably ~every 15 min). [[raw/Georgia_Freezing_troubleshooting_direction-March-13-2026.md]]

## Manufacturer technical response (FP10 motherboard) — investigation evidence

This is a **manufacturer email**, not a JVL meeting — a direct reply from the **FP10 motherboard maker, Maxtang / Datang** (Hilda Huang, Overseas BU sales manager) to Genadi's freezing enquiry, dated **March 20–24, 2026**. Folded here as technical evidence in the investigation. [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]

The manufacturer's diagnosis and recommendation:
- **Kernel version is the primary suspect.** The **Vega 8 integrated GPU on the FP10 is sensitive to the Linux kernel version.** They recommend **upgrading to Linux 5.10 or 5.15 LTS** for best AMD-Vega compatibility, and advise against non-LTS kernels below 5.4 or above 6.0. **JVL's 4.19 kernel falls below their minimum recommended 5.4.** [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]
- **Troubleshooting order:** first confirm whether the issue started after a kernel/OS upgrade and try rolling back to a known-stable kernel; then reinstall/update the matching **Mesa graphics library + AMD GPU firmware**; the GPU driver ships inside the kernel and can be upgraded independently of the OS. [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]
- **Zero-risk diagnostic:** check `dmesg` logs for the keywords **"AMDGPU hang"** and **"gpu reset"** — the telltale entries for a Vega 8 driver freeze. [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]
- **The FP10 does have a hardware watchdog**, configurable in BIOS (Advanced tab → *Watch Dog Configuration* → set *WDT Timeout Mode*). Genadi later clarified the board actually has **two**: one from the **IT8786 SuperIO chip** (the BIOS-configurable one) and one internal to the **APU**. [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]
- **Open thread:** Pavel replied that JVL had tried the BIOS WDT but couldn't ping it "due to lack of specification" and now uses the internal APU watchdog — which appears to conflict with his Friday Teams statement that the CPU-hosted watchdog is *not* enabled. Which watchdog is actually active in production needs clarification. [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]

The manufacturer's kernel-upgrade recommendation lines up with the AMD forum posts Genadi shared, and directly feeds the **Mar-26 decision to upgrade to kernel 5.10/5.15**.

## Test machines (Georgia office)

Three machines were set up in the Georgia office (at Lawrenceville) to try to reproduce the freeze; two of the three freeze reliably. Five frequently-freezing machines were also pulled back from a customer site (Bulldog / "Bulldog Entertainment") for monitored testing. [[raw/GA_Freezing_Issue_Executive_Summary.md]] [[raw/Georgia_Freezing_troubleshooting_direction-March-13-2026.md]]

| Cabinet | Serial | Software | Build |
| --- | --- | --- | --- |
| FLEX D27 | CM08-0825-230234 | GCOAM-1.14.2.4.3.4.1 | 3817 |
| FLEX D27 | CM08-0324-229600 | GCOAM-1.14.0.4.3.4 | 3804 |
| FLEX V43 | CM08-1224.230227 | DLKG-1.13.0.4.3.4.2 | 3847 |

[[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]

## Open questions

- Why do ~250 Altera machines in Georgia (same motherboard/adapter config) **not** freeze? [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- Why have no freezes been reported from South Dakota or Nebraska's larger fleets (30+ machines, same build) beyond the single Nebraska case (tracked as CS-442)? [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]] [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Why did test machine serial 229600 stop freezing on its own after Jan 29 with no changes? [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- Is the ~50% underperformance of new-nudge machines fully explained by unreported freezes, or is there an additional software/math issue? [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]]
- Is this fundamentally a **hardware/kernel** problem (AMD GPU driver, kernel 4.19) or a **software** one (DC crash, Framework blocking)? [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Why can't the freeze be reproduced in the lab despite CPU stress testing? [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]
- Which watchdog (BIOS/SuperIO vs internal APU) is actually active in current production software? [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]]

## Sources

- [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]] — *derived/secondary:* AI summary of the Mar-9 freezing meeting (Juan, Felipe, Genadi, Pavel).
- [[raw/GA_Freezing_Issue_Executive_Summary.md]] — *derived/secondary:* AI executive summary of the "GA Freezing Issue" Teams chat (~Mar 9–24).
- [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]] — *derived/secondary:* AI summary of the Teams chat, Segment 1 (initial investigation).
- [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]] — *reference artifact:* Maxtang/Datang manufacturer email reply (FP10 / V1605B) on kernel + watchdog.
- [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]] — Mar-10 IP-106 call, freezing portion (transcript).
- [[raw/Georgia_Freezing_troubleshooting_direction-March-13-2026.md]] — Mar-13 troubleshooting-direction call (transcript).
