---
type: topic
title: EGM freezing investigation (Georgia field fleet)
date: 2026-07-29
aliases: [GA freezing, Georgia freezing, machine freezing, EGM freeze, GA Freezing Issue, freezing investigation, JVL silent killer, nudge animation freeze, kernel-panic freeze]
source-count: 9
open-questions: 12
---

# EGM freezing investigation (Georgia field fleet)

This is the home page for JVL's investigation into gaming machines (EGMs) **freezing in the field** — the machine goes completely unresponsive, the screen locks, and only a physical reboot brings it back. Val called it **"JVL's silent killer"** and treated it as urgent, because it hits revenue and operator confidence directly. [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]]

This page covers the investigation from its **March 9 start through the V1.3 full investigation report of March 25, 2026**: the field discovery and early theories (Mar 9–13), the manufacturer's technical reply (Mar 20–24), the **March 24 watchdog-architecture decision** (two working sessions), and the **March 25** software-version analysis, South Dakota race-condition find, and external-consultant (Alekseev) consultation — the last two are captured from Val's consolidated V1.3 report (a derived document; no transcript of those two March-25 meetings is held). The investigation was still active/open at the report's date.

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

## The Mar-24 watchdog architecture decision (two working sessions)

On March 24 the team held two meetings that turned the manufacturer's advice into an engineering plan. The **morning session** (9:19am, Val + Pavel Frolov + Alexander Biratko) — [[wiki/meetings/2026-03-24-fp10-freezing-watchdog-discussion.md]] — and the **afternoon follow-on** (1:46pm, same three + Genadi Peari) — [[wiki/meetings/2026-03-24-io-centric-watchdog-wiring.md]].

**Two parallel tracks confirmed:**
- **Kernel upgrade to Linux 5.15 LTS.** JVL runs 4.19; the manufacturer (Maxtang) recommends 5.10/5.15 and specifically warns *against* going to 6.x — even though JVL already runs kernel 6.12 on the FlexPay platform. Pavel noted the kernel can be raised independently of the BIOS. Once he and Biratko re-read the manufacturer note together they agreed: **it is a Linux-kernel problem, not a BIOS one — so the BIOS does not need to be reflashed.** Alexander cautioned that past kernel bumps surfaced hardware-compatibility surprises only after extended testing, so 5.15 must be tested carefully (Pavel: a build seems to work, "then you catch unexpected issues with some hardware that you don't see immediately"). Pavel would build a 5.15 image on a current market build (e.g. Nebraska) and check every driver/device over a weekend. [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]]
- **A watchdog on the IO board (the preferred permanent design).** Three options were weighed: **(1) the CPU-internal APU watchdog** — already shipped in the build released the day before, Pavel ~95% confident it fires, but Val disliked trusting a watchdog *inside* the very processor suspected of hanging; **(2) the FP10's SuperIO IT8786 watchdog** — configurable in BIOS but impractical to enable across the field fleet (manual per-machine keyboard entry, or a USB BIOS re-flash) and motherboard-specific; **(3) Alexander Biratko's IO-board-centric watchdog** — reuse the existing heartbeat (the Framework pings the Data Center every ~200ms, the DC pings the IO board every ~200ms), rewrite the IO-board firmware to reset an internal counter on each ping, and if the counter expires (e.g. 5 minutes) the IO board pulls the motherboard's **reset pin** low over a single added wire. [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]]

**Why option 3 won.** It is platform-independent (it carries forward to the future Omni board — no re-doing the watchdog per motherboard), needs no BIOS change, ships as a firmware update with no regulator resubmission, and uniquely also catches a **lost USB link between the IO board and motherboard** (a fault JVL had hit before) that the other two watchdogs would miss. Val liked the "simple, elegant" implementation: no full USB driver device — just have the IO board watch the existing 200ms message traffic and trigger reset if it stops. Acceptance-test method: connect over SSH, kill the game framework, watch a black screen, and confirm the machine reboots after the timeout instead of sitting frozen (the real freeze itself can't be forced). [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]]

**Task split (owner direction).** Alexander Biratko leads the IO-board firmware; Pavel Frolov supports and owns the kernel-5.15 track; [[wiki/people/genadi-peari.md|Genadi]] identifies which pins carry the reset signal. Val explicitly **declined** to hand the firmware to Evgeniy Alekseev at first ("let's give this work to someone else"), assigning it to Biratko — though the afternoon meeting reversed course on *consulting* Alekseev (below). In the afternoon, Genadi confirmed the IO board's **P2 connector** already exposes 2 inputs, 2 outputs and 5V with a line buffer in place, so an open-drain / ground pull can drive the reset — "just needs testing." Estimated at roughly a week. [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]] [[raw/I_O-centric_Watchdog_wiring.md]]

**Genadi's "this is unsystematic" challenge (afternoon).** Genadi Peari pushed back hard — his stated habit is to "voice the bad thoughts." His points: the team may be spending large effort on a watchdog (a mitigation) while the *root* kernel cause goes unsolved; he doesn't believe they've done everything possible; Pavel is spread across too many things to lead this; and they should consult an outside expert — recalling that the years-long "IO-board-not-found / freezing-abort" problem was solved in ~15 minutes once he consulted **Alekseev** (an old hand named "Dima Pikuli," the original software author, had also helped historically). He also disputed accepting "we can't read the logs": any Linux freeze should leave traces, so plug in a device and capture them. Val's reply threaded both: keep the watchdog *and* bring in Alekseev. [[raw/I_O-centric_Watchdog_wiring.md]]

**Capturing crash evidence when the OS is dead.** Pavel explained that Linux kernel crash logs almost never reach storage — you can only see them on a **serial console** attached to the machine; and Alexander noted a *hang* (an infinite loop) may leave no crash output at all, unlike a kernel panic. Val's scaled idea: instead of a laptop on each serial port, build ~10 cheap self-contained boxes (a Raspberry Pi / RK3568-class board, ~$300 each) in metal enclosures, drop them into Georgia machines (JVL can connect to machines there), and have JVL staff play them continuously to accumulate game-hours faster than field play. Then Biratko proposed a cleaner idea Val called "the most genius proposal of the meeting": make the **IO board itself the diagnostic co-processor** — when the watchdog fires, the IO board grabs and preserves the last system state / kernel output in its own non-volatile memory (later even relayed by a cellular modem), so each machine carries a built-in "black box." This is a heavier firmware effort flagged as a **second phase**, likely handed to Alekseev, and — since the old IO board is not worth re-engineering — targeted at the new **Omni** board. Security caveat raised: a serial console that also accepts logins is a password-sniffing risk, so command paths must be designed carefully. [[raw/I_O-centric_Watchdog_wiring.md]]

**Test-fleet plan.** The 3 warehouse machines had not frozen; ~2–3 machines from the **Bulldog** customer site (which freeze) were being installed to reproduce first, then take a suspected build, add the `amdgpu` kernel parameter plus a CPU watchdog, and observe. Anton Leshkevich runs the machines to catch a freeze. Val also began pressing a broader want: a **systematic way to black-box-test releases** (hooks on the Data-Center↔Framework path) rather than relying on field reports — he compared trusting operator freeze-reports to doctors and lying patients ("collect the hard logs, don't collect the stories"). [[raw/I_O-centric_Watchdog_wiring.md]]

**Status of the watchdog decision.** As of the March 25 report the IO-board watchdog was the **preferred direction but not formally locked**; the CPU-internal watchdog was already shipped as the interim safety net (see the Mar-26 [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|initiative-priority]] plan, which ships the kernel upgrade plus a kernel-panic auto-reboot parameter alongside that already-shipped CPU watchdog, all fixes in one release).

## Consolidated findings & the March 25 turn (V1.3 full report — derived)

> **Derived/secondary source.** The following is folded from Val's **"EGM Freezing Issue — Full Investigation Report, Version 1.3"** (dated Mar 25, 2026; covers Mar 9–25). It is a consolidated internal + consultant briefing, **not a transcript** — captured once here, cross-investigation facts not double-counted with the primary sources above. The two March-25 meetings it summarizes ("Digging into Freezing Issues," 9:32am; "Freezing Investigation with Alekseev," 11:03am) have **no held transcript**, so their content is carried only via this report.

**Software stack, now named.** The report sets out the stack as **HAL** (hardware abstraction) → **DC** (Data Center, a Java application holding the application logic) → **SAS** protocol → **Framework** (a C++ display/game engine). DC and Framework are separate processes talking over sockets; the Framework reads the DC every frame. The HAL is "99.9% identical" across markets — the meaningful changes between the old and freezing-prone versions live in the **DC layer**. [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

**The NVMe-adapter theory is now largely ruled out.** Sapphire ("Mexico") boards with a *native* NVMe slot (no adapter) were confirmed to also freeze — so the common factor is the **AMD Raven Ridge APU (V1605B) + Vega 8 GPU + Linux kernel**, not the disk interface. This promotes the **kernel/GPU incompatibility** to the leading theory and demotes the adapter theory recorded above. Genadi also corrected the timeline: freezing has existed **since the Flex product's inception** (reported since prototypes), and the new software likely raised the *frequency* (more video/GPU load) rather than introducing the fault; casinos rebooting daily masked it, field locations did not. [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

**Mar-25 software-version analysis + a separate South Dakota bug.** Val convened Pavel, Irina Shishko and Alexander to chronologically isolate what changed in the DC between the old release (~v1.12/1.17 on the "Pech 123" machines) and the current **v1.14** (which added dual SAS connections, printer support, and a new skill; printer work done at DC level, and the printer code is in the Georgia build even though Georgia machines have no physical printer). A **separate** issue was root-caused and reproduced the same day: South Dakota machines crash/reboot when scanning a QR code, due to a **race condition** in the game-disable/tilt sequence — all games are disabled via SAS lock, and before the DC sets a tilt state the Framework queries for available games, sees zero, and crashes. The fix is to make game-disable + tilt-activation **atomic** (transactional), not sequential; assigned to Biratko and Zhenya. Irina was tasked with exact version numbers for a precise diff, and Val ordered a **Claude Code review** of the changed DC and HAL code. [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

*Name note (§4):* the report attributes the SAS-emulator / freezing-analysis and DC-printer work to "**Zhenya (Evgeniy Khaletsky)**." "Khaletsky" reads as a garble of **Kharetski** (the LGS/Omni backend Zhenya, [[wiki/people/evgeny-kharetski.md]]), which fits the backend/DC context; treated as that person pending confirmation.

**Mar-25 Alekseev consultation.** Val brought in external specialist **Evgeniy Alekseev** ("mistakes are made by those who do things — no finger-pointing, only facts"). Alekseev's three hypotheses: **memory-management issues** (leaks/pointer errors/stack overflow — he rated ~90%); **printer-driver synchronous communication** (should use a separate thread with a command queue); and **chip/processor errata** (obtain the vendor errata sheet for the exact APU). A technical debate followed — Alekseev held that memory corruption can hard-freeze even Linux; Pavel countered that x86 Linux memory protection makes an app segfault without taking down the kernel — and when Pavel opened the actual printer HAL code (`l_printer`) it already had **mutex locks throughout**, contradicting Alekseev's assumption (though code Alekseev wrote from a template may lack them, and Claude Code had independently flagged possible concurrent-access issues). A **new high-priority untested theory** emerged: when the **DC process dies, the Framework hangs on its socket read** with no timeout — the Georgia "morning freeze" pattern could be the DC dying overnight and the Framework sitting on a dead socket for hours; the old version reportedly rebooted/tilted instead, so the behavioral change is a clue. [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

**Decisions out of Mar-25.** (a) Build a **permanent system-resource monitoring daemon** — an independent process (not inside Framework/DC) watching memory, file descriptors, sockets, thread count and stack usage, writing **unbuffered** to its own log so data survives a freeze mid-write; Val made it a standing **architectural component** and a pre-release QA gate, not a one-off ("roads work without traffic lights and curbs, but you build them anyway"). (b) Connect a **SAS emulator** to a test machine and loop meaningful state-changing commands (none of the 5 Georgia test machines were on SAS). (c) Run the **Claude Code review** of DC + HAL changes (Zhenya pulled onto it). (d) Fix the South Dakota race condition. A static analyzer over the C++ (HAL/Framework) for leaks/out-of-bounds was flagged as a future step. [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

**Policy shifts the report names.** From "reproduce the freeze first" to a **parallel-track** approach (keep trying to reproduce *and* ship the watchdog as mitigation *and* upgrade the kernel *and* review the code); and from defensive to constructive reception of outside input (Genadi's manufacturer email, Alekseev's critique). [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

*A near-duplicate consolidated report, "JVL Freezing Investigation — Comprehensive Report" (same Mar 9–25 scope, same conclusions, richer tables/ADRs), was **§12-skipped** as a re-titled twin of this V1.3 report — see [[wiki/skipped.md]]; V1.3 is the cited source of record.*

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
- Does killing the Data Center and letting the machine sit for hours reproduce the Georgia "morning freeze"? (Pavel's untested high-priority theory.) [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]
- What exactly changed in the DC layer between the old release and v1.14 that raised the freeze frequency? (Waiting on Irina's exact version numbers for a diff + the Claude Code review.) [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]
- Are there memory leaks / out-of-bounds errors in the C++ Framework or HAL? (Alekseev's ~90% hypothesis; needs a static analyzer.) [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]
- Does the `amdgpu.noretry=0` parameter already in the Texas build actually reduce freezes on kernel 4.19? [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]
- Is the IO-board watchdog the final design, and does the diagnostic-co-processor "black box" get built for the Omni board? (Preferred but not formally locked as of Mar 25.) [[raw/I_O-centric_Watchdog_wiring.md]] [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]]

## Sources

- [[raw/GA_Machine_Freezing_Summary-March-9-2026.md]] — *derived/secondary:* AI summary of the Mar-9 freezing meeting (Juan, Felipe, Genadi, Pavel).
- [[raw/GA_Freezing_Issue_Executive_Summary.md]] — *derived/secondary:* AI executive summary of the "GA Freezing Issue" Teams chat (~Mar 9–24).
- [[raw/GA_Freezing_Issue_Segment_1_Initial_Investigation.md]] — *derived/secondary:* AI summary of the Teams chat, Segment 1 (initial investigation).
- [[raw/GA_Freezing_Issue_FP10_Manufacturer_Email.md]] — *reference artifact:* Maxtang/Datang manufacturer email reply (FP10 / V1605B) on kernel + watchdog.
- [[raw/Freezing_GA-COAM-scope_IP-106-March-10-2026-seg1.md]] — Mar-10 IP-106 call, freezing portion (transcript).
- [[raw/Georgia_Freezing_troubleshooting_direction-March-13-2026.md]] — Mar-13 troubleshooting-direction call (transcript).
- [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]] — Mar-24 morning watchdog-design call (transcript).
- [[raw/I_O-centric_Watchdog_wiring.md]] — Mar-24 afternoon IO-board watchdog wiring + systematic-approach debate (transcript).
- [[raw/EGM_Freezing_Issue_Full_Investigation_Report-V1.3.md]] — *derived/secondary:* Val's consolidated V1.3 full investigation report (Mar 9–25); the sole carrier of the two Mar-25 meetings. Supersedes V1.2 (skip-ledgered); near-duplicate "Comprehensive Report" also skip-ledgered.
