**EGM Freezing Issue**

Full Investigation Report

From Discovery Through Current Action Plan

Period: \~March 9--25, 2026 \| Status: Active Investigation \| Classification: Internal + Consultant Briefing

**Prepared by:** Val Levitan

**Date:** March 25, 2026

**Distribution:** Internal engineering team and external consultant

**Version:** 1.3 --- Updated with March 25 meetings (software version analysis, Alekseev consultation, South Dakota race condition discovery)

**1. Executive Summary**

JVL's gaming machines are freezing completely in the field --- going totally unresponsive, screen locked, no recovery --- across multiple markets including Georgia, South Dakota, and Nebraska. The problem has existed since the FLEX product's inception but its frequency appears to be increasing, particularly with newer software releases that add more video resources and GPU load. The problem appears random: not every machine is affected, it doesn't happen at the same time of day, and it hasn't been reproduced in the lab. Locations sometimes just reboot the machines themselves without calling JVL, which means the true scale of the problem is likely bigger than what's been reported.

The team investigated several possible causes --- synchronous communication between the Framework and Datacenter blocking the system, a Java crash triggered by the printer library, CPU power-saving features putting COM ports to sleep, and a known AMD Raven Ridge GPU driver bug that causes identical freeze behavior on the same processor platform. The NVMe SSD adapter theory, initially the leading hardware suspect, has been largely ruled out after confirming that Sapphire (Mexico) boards with native NVMe slots also freeze --- pointing to the AMD APU and kernel as the common factor, not the disk interface. The fact that no crash logs are ever collected after a freeze strongly suggests the Linux operating system itself becomes non-operational, pointing toward a hardware or kernel-level issue rather than a pure software bug.

The most actionable discovery was that the hardware watchdog timer --- the safety net that should automatically reboot a frozen machine --- is completely non-functional. No external watchdog hardware is wired, and the CPU's built-in watchdog is disabled in the current software. A commented-out code parameter confirmed it was intentionally turned off at some point during a hardware revision. The motherboard manufacturer (Maxtang) has since confirmed that the Vega 8 GPU is kernel-sensitive and recommends upgrading from JVL's current Linux kernel 4.19 to version 5.10 or 5.15 LTS.

On March 25, the investigation expanded in two directions. First, Val shifted the approach to include a software version analysis --- chronologically isolating what changed in the DC (Datacenter) layer between old versions that freeze less and the current v1.14 release. An external consultant (Evgeniy Alekseev) was brought in, contributing three hypotheses: memory management issues as the primary suspect, printer driver thread-safety gaps, and processor errata. The team also discovered a separate but related issue in South Dakota --- a race condition in the game-disable/tilt sequence that causes machines to crash when scanning QR codes. Most significantly, the team decided to build a permanent system resource monitoring daemon as an architectural component, deploy SAS emulator stress testing, and run AI-assisted code review on the changed software layers.

**2. The Problem**

**2.1 What Happens**

Gaming machines (EGMs) freeze completely: the screen locks on whatever was displayed, all inputs stop responding, and the machine does not recover on its own. The only remedy is a physical power cycle (hard reboot). No crash logs are generated. No audit tickets print. The machine simply stops.

**2.2 Where It Happens**

- **Georgia:** Primary market where freezes are most frequently reported. Five machines from a customer site (Bulldog) known to frequently freeze were brought back to the Georgia office for monitored testing on March 24.

- **South Dakota (VLT):** Not all machines fail to reconnect to the host system each morning. The problem appears random. Machines that auto-reboot after a QR scan do not always auto-reboot. **Update (March 25):** A separate issue was discovered --- machines crash and reboot when scanning QR codes due to a race condition in the game-disable/tilt sequence (see Section 3.5).

- **Nebraska:** One confirmed freeze so far (CS-442 in JIRA). Denis found the machine completely frozen on-site; location could not confirm duration.

- **Florida:** Machines live for 3+ years with no real freezing (except cases related to overheating where CPU fans were reversed). This market uses the same platform.

- **Mexico:** Sapphire motherboard machines (native NVMe, no adapter) have also been confirmed to freeze. This rules out the NVMe adapter as a differentiating factor.

**2.3 Scale of the Problem**

Val characterized this as "JVL's silent killer." The true scope is likely larger than reported because locations sometimes reboot machines without notifying JVL. Genadi Peari noted in the March 24 afternoon meeting that freezes have been reported sporadically since the product's launch on the Flex platform and the current FP10 motherboard --- this is not a new issue, but its frequency appears to be increasing. A contributing factor may be that casino machines are rebooted daily (masking the problem), while Georgia field locations may not power-cycle as frequently, allowing freezes to accumulate visibility.

**2.4 What We Know for Certain**

- No crash logs are ever collected from a frozen EGM.

- The Linux operating system itself appears to become non-operational during a freeze (Pavel Frolov's assessment).

- The software watchdog (start_game.sh) cannot help because it requires a functioning OS to execute.

- The hardware watchdog timer is not active in the current production software or hardware configuration.

- The freeze has not been reproduced in the QA lab despite CPU stress testing (90% load) and other attempts.

- The FP10 motherboard uses an AMD Raven Ridge APU with Vega 8 integrated GPU, running Linux kernel 4.19.

- Both Tank (NVMe adapter) and Sapphire (native NVMe) motherboards exhibit freezing --- the common factor is the AMD APU and Linux kernel, not the disk interface.

- The software stack is: HAL (hardware abstraction) → DC (Datacenter / application logic) → SAS protocol → Framework (display/game engine). The HAL between markets is "99.9% identical"; significant changes between old and new versions are in the DC layer.

**3. Investigation Timeline**

**3.1 Phase 1: Initial Theories (\~March 9--19)**

The investigation began in a Teams group chat ("GA Freezing Issue") involving Alexander Biratko, Anton Leshkevich, Efim Podvoiski, Genadi Peari, Irina Shishko, Ivan Shpak, Juan Martinez, Pavel Frolov, and Val Levitan. Four theories were explored:

**Theory A --- Framework/DC Communication Blocking:** Anton Leshkevich proposed that the Framework's synchronous communication with the Datacenter (DC) could cause a visible freeze if the DC stops responding. The Framework pulls system state every frame; if the DC hangs, the screen would appear frozen. This would explain why QA hasn't seen the issue (debug builds don't start in a locked state). Alexander Biratko pushed back: the DC is not directly connected to the lottery system; all communication is through SAS. Theory not dismissed but considered unlikely as sole cause.

**Theory B --- Printer / Java Machine Crash:** Efim Podvoiski found crash logs showing a Java machine crash when accessing the printer library (March 17, 7:43 PM GMT). However, this crash was unrelated to the observed freeze on-site --- Denis arrived hours later and printed a successful audit ticket. The team agreed to test whether killing the DC process manually reproduces the freeze symptoms.

**Theory C --- CPU Power Saving / COM Port Sleep:** Juan Martinez asked whether hidden BIOS power-saving features could put COM ports to sleep. Pavel confirmed JVL does not use power savings. Theory set aside.

**Theory D --- AMD GPU Driver Issue:** Genadi shared a Qubes OS forum post describing identical freeze behavior on the same AMD Raven Ridge APU. The forum discussed kernel-level GPU driver issues. Pavel noted JVL uses kernel 4.19 and could try the kernel parameter amdgpu.noretry=0. Juan also shared additional AMD kernel parameters (amdgpu.gpu_recovery=1, amdgpu.gfxoff=0) used by others to resolve similar freezes. This theory later received strong support from the motherboard manufacturer.

**3.2 Phase 2: Watchdog Timer Discovery (\~March 17--20)**

Val asked a direct question: "Why is the watchdog timer not working?" This led to the investigation's most important finding.

The start_game.sh script functions as a software watchdog: if the framework application terminates, it collects crash logs and forces a reboot. But Pavel emphasized that crash logs have never been collected after a freeze --- the OS itself is dead by that point.

Val asked three questions to Pavel, Genadi, and Alexander: (1) Do we have the physical watchdog hardware on this board? (2) Do we speak to this hardware on the software level? (3) If yes to both, it should be easily testable.

Pavel found a commented-out parameter in the IO board code: #define USE_HOPPER_IN_AS_WATCHDOG_RESET 1. This was an optional channel line repurposed from a hopper input to act as a reset trigger --- intentionally disabled at some point.

Pavel's definitive answer: "Currently we do not have external Watchdog wired. CPU hosted watchdog is not enabled on current software."

Val confirmed this aligned with his recollection that JVL previously relied on a standalone hardware watchdog chip, which was apparently removed or disconnected during a hardware revision. Juan Martinez drafted requirement REQ-1028 ("EGM Auto-Restart and Watchdog Recovery System for Freeze Detection"). Val corrected the framing: the requirement should state "A machine should auto-recover in the event it permanently froze" --- without prescribing the engineering solution.

**3.3 Phase 3: Manufacturer Response (March 20--24)**

On Friday March 20, Genadi contacted Maxtang (the FP10 motherboard manufacturer) directly, describing the freezing issue and asking about watchdog capabilities.

On Monday March 23, the manufacturer's engineering team responded with a structured troubleshooting guide:

**Priority 1 --- System & Kernel:** Confirm whether the issue started after a kernel upgrade. Try rolling back to a stable version.

**Priority 2 --- GPU Driver Stack:** Reinstall and update Mesa graphics and AMD GPU firmware. Check dmesg logs for "AMDGPU hang" and "gpu reset" keywords --- telltale signs of a Vega 8 driver freeze. Upgrade kernel to Linux 5.10 or 5.15 LTS.

Manufacturer's critical note: "The Vega 8 integrated GPU on the FP10 is sensitive to Linux kernel versions. We do not recommend using non-LTS kernels below 5.4 or above 6.0; please prioritize the officially validated 5.10/5.15 LTS versions instead. The kernel version is the key factor for display stability --- the AMD GPU driver for the Vega 8 is built into the kernel."

JVL is currently running Linux kernel 4.19, which falls below the manufacturer's minimum recommended version of 5.4.

The manufacturer also confirmed that the FP10 has an onboard hardware watchdog (configurable in BIOS under Advanced → Watch Dog Configuration). Genadi later clarified that the FP10 actually has two watchdog timers: one provided by the IT8786 SuperIO chip on the board, and one internal to the APU.

**Clarification on Pavel's watchdog statements:** Pavel's statements across the investigation reflect a progressive situation, not a contradiction. On \~March 19, he confirmed that although the FP10 hardware has watchdog timer chips, JVL's software was not communicating with any of them --- no watchdog of any kind was active. On March 24, in his reply to the manufacturer's email, he was discussing the ways of engaging one of the hardware watchdog timers. Later that day, he and Alexander proposed the IO-board-centric watchdog as a superior alternative. The final watchdog implementation decision remains open as of March 25.

**3.4 Phase 4: Watchdog Architecture and Kernel Decisions (March 24)**

Two meetings were held on March 24 to formalize the action plan. The first meeting (9:19 AM EST, 31 minutes) included Val, Pavel, and Alexander Biratko. The second meeting (1:46 PM EST, 58 minutes) added Genadi Peari.

Three watchdog options were evaluated, and the IO board watchdog was proposed as the preferred approach. The Linux kernel upgrade to 5.15 LTS was confirmed as a parallel track. Full details are in Section 4.

During the afternoon meeting, Genadi Peari challenged the team's approach as unsystematic, arguing that: the team needs a dedicated lead on freezing (Pavel is spread too thin); external experts should be consulted (citing the IO-board-not-found problem that was solved in 15 minutes after consulting Alekseev); kernel logs should be captured via serial console rather than accepting they can't be captured; and the manufacturer's recommendations should be tested on actual freezing machines rather than dismissed on theoretical grounds. This challenge directly influenced Val's decision to bring in Alekseev for a consultation meeting on March 25.

**3.5 Phase 5: Software Version Analysis and South Dakota Race Condition (March 25 AM)**

On March 25 at 9:32 AM, Val convened a meeting with Pavel Frolov, Irina Shishko, and Alexander Biratko to shift the investigation from a hardware-only focus to include a chronological software analysis.

**Software architecture and version history:** The original releases (around versions 1.12/1.17) shipped on the "Pech 123" machines. The current release --- approximately version 1.14 --- added support for two SAS connections and a printer, along with a new skill. The printer-related work was done at the DC level, not the HAL level. Pavel clarified that the HAL for the printer is the same as the Florida version; changes were specifically in the DC layer. Irina confirmed that both Alexander (Sasha) and Zhenya (Evgeniy Khaletsky) contributed to these changes. In Georgia specifically, printers are not physically installed, so printer code paths are not directly triggered --- but the code is in the build.

**The core mystery reframed:** New machines with the v1.14 software appear to freeze more frequently than old machines running earlier versions. The hardware is unchanged. Val is attempting to chronologically isolate what changed in the DC layer to identify whether a specific code change increases the freeze probability.

**South Dakota QR Code Race Condition (separate issue):** Irina raised a second issue: machines in South Dakota crash and reboot when scanning QR codes. Denis reported machines going into reboot. Juan sent a video demonstrating the behavior. The team found the cause and successfully reproduced it on March 25. Alexander explained the root cause --- a race condition in the game-disable/tilt sequence:

1.  All games on the machine are disabled via SAS (SAS lock).

2.  Games are then unlocked sequentially.

3.  Before the DC can set a tilt state, the Framework queries for available games.

4.  The Framework sees zero games (they've all been disabled) and crashes.

5.  The timing window between disabling the last game and setting the tilt state is small but occasionally hit.

Val questioned the architecture: "The framework should tell the DC 'wait, it's not your time to ask.'" Alexander explained that the game-disable and tilt-activation operations are sequential rather than transactional --- the Framework can query in the gap between them. The fix requires making these operations atomic.

**Decision --- Claude Code review:** Val proposed running the changed DC and HAL code through Claude Code for automated code review. Alexander expressed initial skepticism, but Val argued that even abstract findings become actionable when reviewed by engineers with domain knowledge: "If Claude Code tells me there are errors, I'd just say 'yes, bad code.' But if it tells you there are errors, you have the practical and academic knowledge to say 'this one is probably harmless, but this one is probably bad.'" Pavel added that the review should approach from two sides: the DC layer changes and the HAL changes, since a crash in the DC could trigger unexpected behavior in the HAL. Irina was tasked with providing exact version numbers for the diff.

**3.6 Phase 6: External Consultant and Monitoring Architecture (March 25 AM)**

At 11:03 AM on March 25, Val brought in Evgeniy Alekseev as an external specialist, joining Pavel Frolov, Alexander Biratko, and Genadi Peari. Val opened the meeting by establishing the tone: "Mistakes are made by those who do things --- no finger-pointing, only facts."

**Alekseev's hypotheses:** Alekseev offered three main hypotheses:

1.  **Memory management issues** (90% probability in his estimation) --- memory leaks, pointer errors, or stack overflows in the C++ code are the most common cause of hard freezes.

2.  **Printer driver asynchronous communication** --- based on his prior work on the printer code, he identified that synchronous commands to the printer could cause machine hangs. He stated the printer interaction needs to use a separate thread with a command queue.

3.  **Chip/processor errata** --- every chip and GPU has manufacturer-documented bugs with recommended workarounds. These errata documents should be obtained and checked for the specific processor used.

**Technical debate --- memory errors vs. Linux protection:** A significant exchange occurred between Alekseev and Frolov. Alekseev maintained that memory corruption (pointers going out of bounds, stack overflow) can cause a hard freeze even on Linux. Frolov countered that on x86 with Linux, hardware memory protection prevents an application from corrupting kernel memory --- an application that writes out of bounds crashes (segfault) but the kernel remains operational. Both agreed to investigate memory leaks as a useful diagnostic exercise, even if kernel protection should theoretically prevent a full system freeze. Genadi pushed back on Frolov, noting that memory issues remain the #1 suspect and asking what concrete steps had been taken to validate the theory rather than dismissing it.

**Printer code finding:** When Pavel opened the actual printer HAL code (l_printer), he found that mutex locks are already implemented throughout --- every function has lock/unlock calls to prevent race conditions between threads. This contradicted Alekseev's assumption that the printer code lacked thread safety. Alekseev acknowledged this, noting he hadn't seen mutexes in the code he worked with. Pavel pointed out that Alekseev had used a file as a template that already had mutexes --- and the printer code Alekseev wrote does not have them. Critically, Claude Code's AI analysis had independently found potential concurrent access issues, suggesting that while the HAL pattern is correct, there may be gaps in the DC layer or in code derived from templates without carrying over the mutex pattern.

**New untested hypothesis --- DC death causing extended Framework freeze:** Pavel raised a significant new theory: when the Datacenter process is killed, the Framework freezes on its socket read. They've never tested what happens if DC dies and the machine sits for hours. The morning freezes seen in Georgia could be exactly this scenario: DC dies at some point during the night, Framework hangs on the dead socket waiting for a response, and over hours the machine becomes completely unresponsive. Alexander added that the old version (Pech 1) should have handled DC death with a reboot or tilt --- not a freeze. This behavioral change between software versions is a significant clue.

**Decision --- resource monitoring daemon:** Val proposed building architectural "guardrails" --- safeguards that catch problems proactively. He used the analogy: "Roads can work without traffic lights and curbs, but you build them anyway." The team converged on building a system resource monitoring daemon that would monitor memory consumption, file descriptors, sockets, thread count, and stack usage. It would run as an independent daemon (not part of Framework or DC), write to its own log file with unbuffered writes (so data survives even if the system freezes), and be lightweight enough for production deployment. Val directed that this should become a permanent part of the architecture --- a pre-release QA checkpoint and a production diagnostic tool, not a one-off.

**Decision --- SAS emulator stress testing:** None of the 5 Georgia test machines are connected to SAS. Val directed Alexander to connect a SAS emulator (already available) to one test machine and create a loop of SAS commands that would stress the Framework --- not just status queries, but commands that trigger game enable/disable, mode switches, and other state changes.

**4. Decisions Made**

**4.1 Linux Kernel Upgrade to 5.15 LTS (March 24)**

The team confirmed upgrading the Linux kernel from 4.19 to 5.15 LTS, following the manufacturer's recommendation. Pavel noted that JVL already runs kernel 6.12 on the Flex Fay platform, but the manufacturer specifically warns against versions above 6.0 for the FP10. The kernel can be upgraded independently without changing the OS or BIOS.

Pavel will build a test image using a current market build (e.g., Nebraska) with the new kernel and have QA verify all device drivers and functionality. Weekend stability testing is planned. The kernel parameter amdgpu.noretry=0 has already been applied to a build sent to Texas.

Alexander cautioned: "We need to test this well." Previous kernel upgrades revealed unforeseen hardware compatibility issues that only appeared after extended testing. Pavel concurred: "You can upgrade, everything seems to work, but then you catch unexpected issues with some hardware that you don't see immediately."

**4.2 IO Board Watchdog Timer (March 24)**

Three watchdog options were evaluated:

- **Option 1 --- CPU-internal watchdog:** Already being used in the latest build. Pavel estimated 95% confidence it would trigger on a freeze. However, Val expressed concern: if the CPU itself is the source of the problem, the internal watchdog may also be affected.

- **Option 2 --- BIOS watchdog (IT8786 SuperIO chip):** Exists on the FP10 and is configurable via BIOS. However, enabling it in the field requires either manual keyboard entry at each machine (impractical) or a BIOS firmware flash via USB stick. Also, this solution is motherboard-specific and would need to be reconfigured for every future platform.

- **Option 3 --- IO board watchdog (proposed):** Alexander Biratko proposed using the existing communication chain: the Framework pings the Datacenter every 200ms, and the Datacenter pings the IO board every 200ms. The IO board firmware would be modified to maintain a countdown counter that resets on each ping. If the counter expires (e.g., 5 minutes with no pings), the IO board triggers a hardware reset by pulling the motherboard's reset pin low via an internal wire.

Option 3 was the preferred approach because it is platform-independent (works on any future motherboard), does not require BIOS changes, can be deployed as a firmware update without regulatory resubmission, and covers additional failure scenarios (e.g., USB communication loss between the IO board and motherboard).

Genadi confirmed that the IO board's existing P2 connector has 2 output and 2 input pins with line buffers already in place. The wiring may require only a single additional wire from the IO board to the motherboard's reset pin. Genadi needs to verify which specific pins are available and whether they can provide the signal level needed (open drain or ground) for reset.

**Implementation approach:** The simpler of two approaches was chosen --- no USB driver or device abstraction. The IO board simply monitors the existing 200ms ping traffic and triggers reset if pings stop. Alexander Biratko leads the firmware work with Pavel Frolov supporting.

**Estimated timeline:** Approximately one week.

**Note:** The final watchdog implementation decision remains open as of March 25. The IO board approach is the preferred direction but has not been formally locked.

**4.3 Diagnostic Co-Processor Concept (Future)**

During the March 24 afternoon meeting, Pavel proposed enhancing the IO board to serve as a diagnostic co-processor: connecting a COM port (serial console) from the main CPU to the IO board's STM32 processor, allowing it to capture kernel crash logs that the main system cannot write to disk during a freeze. When the watchdog triggers, the IO board would preserve the last kernel output in its non-volatile memory for retrieval after reboot.

Val endorsed this concept strongly, noting it eliminates the need for external diagnostic hardware (e.g., laptops or Raspberry Pi units connected to serial ports). The IO board would effectively become a built-in "black box" flight recorder for each machine.

This capability requires a more significant firmware development effort and is planned as a second phase. An external firmware consultant will be engaged to advise on feasibility and potentially lead the implementation.

**4.4 BIOS Changes Not Required (March 24)**

The team confirmed that BIOS modifications are not needed. The kernel upgrade addresses the GPU driver issue at the OS level, and the IO board watchdog bypasses the BIOS-based watchdog entirely. This significantly simplifies field deployment.

**4.5 Claude Code Review of DC and HAL Changes (March 25)**

Val directed Alexander Biratko and Zhenya (Evgeniy Khaletsky) to run the changed code between the old version (Pech 123) and the current v1.14 through Claude Code for automated code review, focusing on potential instabilities and freezing causes. Pavel added that the review should approach from two sides --- both the DC layer changes and the HAL changes. Irina Shishko was tasked with providing the exact version numbers as a prerequisite. Zhenya was pulled off current work to focus on this.

**4.6 System Resource Monitoring Daemon (March 25)**

The team decided to build a permanent system resource monitoring utility:

- Independent bash daemon --- not embedded in Framework or DC

- Monitors memory consumption, file descriptors, sockets, thread count, stack usage

- Unbuffered writes to its own log file (data survives even if system freezes mid-write)

- Lightweight enough for production deployment

- Dual purpose: pre-release QA checkpoint (must run clean for a defined period before release) and production diagnostic

Pavel was directed to ask Claude Code for the comprehensive list of monitoring parameters immediately. Claude Code then writes v1 of the bash utility (estimated hours, not days). Alexander deploys it to the 5 Georgia test machines via Anton.

**4.7 SAS Emulator Stress Testing (March 25)**

Alexander Biratko was directed to connect a SAS emulator to one of the Georgia test machines and create a stress-test loop of meaningful SAS commands --- game enable/disable, mode switches, and state changes that exercise the Framework, not just status queries.

**4.8 South Dakota Race Condition Fix (March 25)**

Alexander Biratko and Zhenya were assigned to fix the QR code race condition by making the game-disable and tilt-activation operations atomic (transactional) rather than sequential. Root cause was confirmed and reproduced on March 25.

**5. Current Status and Next Steps**

**5.1 Immediate Actions (Week of March 25)**

- **Pavel Frolov:** Build and test Linux kernel 5.15 LTS image. Ask Claude Code for monitoring parameter list. Write v1 of monitoring daemon. Review specific commits between old and new software versions.

- **Alexander Biratko:** Lead IO board watchdog firmware implementation. Deploy monitoring utility to Georgia machines. Connect SAS emulator to test machine. Fix South Dakota race condition with Zhenya. Run Claude Code review on DC and HAL changes.

- **Irina Shishko:** Provide exact version numbers --- version on first Pech 123 machines and currently deployed version --- for precise code diff. This is a blocker for the Claude Code review.

- **Genadi Peari:** Confirm which P2 connector pins are available for the watchdog reset signal. Contact Maxtang to produce new BIOS firmware with watchdog enabled by default (for future boards).

- **Pavel / Alexander (joint):** Test the DataCenter-kill extended timeout scenario --- kill DC, wait several hours, monitor what happens to Framework and system resources. Compare behavior on old version (Pech 1) vs. current version.

- **Team (future):** Run static analyzer on C++ code (HAL/Framework) to check for memory leaks and out-of-bounds access.

**5.2 Consultation Outcome (March 25)**

The Alekseev consultation meeting was held on March 25 at 11:03 AM. Key outcomes:

- Alekseev's primary hypothesis (memory management, 90% probability) was noted but debated. Linux memory protection should theoretically prevent application-level memory errors from causing kernel freezes, but edge cases may exist.

- Alekseev's printer code concern was partially validated: the HAL printer code has mutexes, but code Alekseev wrote (from a template) may lack them. Claude Code independently found concurrent access issues.

- The DC-death hypothesis emerged as a high-priority untested theory.

- The monitoring daemon decision and SAS stress testing were direct outcomes of this meeting.

Val's approach to Alekseev was constructive: "Instead of taking it as an attack, let's say OK, what's the error? Let's figure it out."

**5.3 What Remains Unknown**

- The exact root cause of the freeze. The kernel version is the leading theory (supported by the manufacturer), but it has not been proven.

- Whether the amdgpu.noretry=0 kernel parameter (already applied to the Texas build) resolves or reduces freezes on the current kernel 4.19.

- Whether the freeze is reproducible under any specific conditions. The feedback cycle is extremely long --- machines may run for weeks before freezing.

- What exactly changed in the DC logic between old and new software versions. Waiting on Irina's version numbers for a precise diff.

- Whether killing the DataCenter process and waiting hours reproduces the morning freeze pattern seen in Georgia (Pavel's untested hypothesis).

- Whether there are memory leaks in the C++ framework or HAL (Alekseev's primary hypothesis; needs static analyzer).

- Whether kernel dmesg logs contain "AMDGPU hang" or "gpu reset" entries on machines that have frozen (the manufacturer's recommended diagnostic check).

- The final watchdog timer implementation decision. Three approaches were discussed progressively; the IO board approach is preferred but not formally locked.

**6. Technical Reference**

**6.1 Hardware Platform**

- Motherboard: FP10 (manufactured by Maxtang/Datang)

- CPU/APU: AMD Raven Ridge V1605B with Vega 8 integrated GPU

- IO Board: Custom JVL design with STM32 processor, USB connection to motherboard

- OS: Linux (current kernel 4.19; target kernel 5.15 LTS)

**6.2 Software Stack**

- HAL (Hardware Abstraction Layer) --- lowest level, hardware interface

- DC (Datacenter) --- Java application, contains application logic

- SAS --- gaming protocol communications

- Framework --- C++ application, display/game engine

DC and Framework run as separate processes on the same machine, communicating via sockets. The Framework reads from DC every frame to update the display.

**6.3 Watchdog Timers Available**

  ---------------- ------------------ ----------------------------------- ---------------------------------------------------
  **Watchdog**     **Location**       **Status**                          **Notes**

  APU Internal     Inside CPU         Enabled in latest test build        May not trigger if CPU itself freezes

  IT8786 SuperIO   FP10 motherboard   Disabled in BIOS                    Configurable but impractical for field deployment

  IO Board (new)   JVL IO board       Proposed --- in early development   Platform-independent; preferred approach
  ---------------- ------------------ ----------------------------------- ---------------------------------------------------

**6.4 Georgia Test Machines**

  ------------- --------------------- ---------------------- -------------
  **Cabinet**   **Serial Number**     **Software**           **Build**

  FLEX D27      CM08-0825-230234      GCOAM-1.14.2.4.3.4.1   3817

  FLEX D27      CM08-0324-229600      GCOAM-1.14.0.4.3.4     3804

  FLEX V43      CM08-1224.230227      DLKG-1.13.0.4.3.4.2    3847
  ------------- --------------------- ---------------------- -------------

Additionally, 5 machines from Bulldog customer site arrived at the Georgia office on March 24 and are being connected for monitored testing.

**6.5 JIRA References**

- CS-442: Nebraska freeze field report (Denis on-site visit)

- REQ-1028: EGM Auto-Restart and Watchdog Recovery System for Freeze Detection

- IP-1027: Monitoring Tool for Gaming Machine (metric collector, data exporter, disk stress loader)

**6.6 Key Personnel**

- **Val Levitan** --- CEO/Director; investigation sponsor

- **Pavel Frolov** --- Director of Engineering; deepest technical knowledge

- **Genadi Peari** --- Electromechanical Dept. Manager; hardware expertise, manufacturer liaison

- **Alexander Biratko** --- Developer; IO board watchdog lead, DC/Framework architecture

- **Anton Leshkevich** --- Developer; monitoring tool, remote machine management

- **Irina Shishko** --- Version/Release Manager

- **Evgeniy Alekseev** --- External Consultant; printer code author, memory hypothesis

- **Juan Martinez** --- US Operations; REQ-1028, field liaison

- **Zhenya (Evgeniy Khaletsky)** --- Developer; SAS emulator, assigned to freezing analysis March 25

*Sources: Teams group chat "GA Freezing Issue"; Email chain "FP10 based V1605B; Freezing Investigation"; Meeting transcripts March 24 2026 (9:19 AM and 1:46 PM); Meeting transcript March 25 2026 "Digging into Freezing Issues" (9:32 AM); Meeting transcript March 25 2026 "Freezing Investigation with Alekseev" (11:03 AM)*
