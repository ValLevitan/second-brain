**GA Freezing Issue --- Teams Chat Summary**

Segment 1: Initial Investigation

Estimated dates: \~March 9--19, 2026

**Chat participants:** Alexander Biratko, Anton Leshkevich, Efim Podvoiski, Genadi Peari, Irina Shishko, Ivan Shpak, Juan Martinez, Pavel Frolov, Val Levitan

**Executive Summary**

This segment covers the first phase of investigating a critical issue: JVL gaming machines are freezing in the field across multiple markets (Georgia, South Dakota, Nebraska). The machines become completely unresponsive, requiring a physical reboot. The freeze appears random --- it does not always happen under the same conditions and has not been reproduced in the QA lab.

The team explored several theories (Framework/Datacenter communication blocking, printer crashes, CPU overheating, AMD GPU driver issues) and made a key discovery: the hardware watchdog timer that should auto-recover frozen machines is not functioning. No external watchdog is wired, and the CPU-hosted watchdog is not enabled in the current software. A disabled code parameter was found confirming it was intentionally turned off at some point. Requirement REQ-1028 was drafted to address auto-recovery.

**1. The Freeze Problem --- Field Reports**

Machines across three markets are experiencing complete freezes:

- **Florida:** Machines live for 3+ years with no real freezing reported (except cases related to overheating where CPU fans were reversed).

- **South Dakota (VLT):** Not all machines fail to reconnect to the host system each morning. The problem appears random. Machines that auto-reboot after a QR scan do not always auto-reboot.

- **Nebraska:** Only one machine has reported a freeze so far. Denis went on-site and found it completely frozen; location could not confirm how long. After reboot he was able to perform QR scan. Tracked as CS-442 in JIRA.

Val characterized this as \"JVL's silent killer\" and emphasized that resolving it is urgent. The locations sometimes reboot machines on their own without contacting JVL, which means the true scope of the problem may be underreported.

**2. Theories Investigated**

**2a. Framework/Datacenter Communication Blocking (Anton Leshkevich)**

Anton proposed that the Framework's communication with the Datacenter (DC) is synchronous --- the Framework pulls the system state every frame. If the DC stops responding (e.g., waiting for a response from the lottery system), the Framework would appear frozen. This would explain why QA hasn't seen the issue, since debug builds do not start in a locked state like production builds do.

Alexander Biratko pushed back: the DC is not directly connected to SD Lottery; all communication is handled through SAS. He did not see how SAS communication would affect communication with the game. The theory was not fully dismissed but was considered unlikely as a sole explanation.

**2b. Printer / Java Machine Crash (Efim Podvoiski)**

Efim found crash logs showing a Java machine crash when accessing the printer library. The crash timestamp was Tuesday, March 17, 2026 at 7:43:07 PM GMT (2:43 PM local). The crash log was found in dc.log inside a crash archive.

However, Alexander Biratko confirmed that this printer crash was not related to Denis being on-site --- Denis arrived several hours later and a successful audit ticket was printed at that time. The sequence of events was clarified: the machine had frozen before Denis arrived; Denis rebooted it, opened the door (audit ticket printed), collected logs, closed the machine, and it was left in TRACE mode. The machine then took longer than usual to come back online and eventually froze again on the main screen. A second reboot resolved it.

Efim noted that a Java machine crash would leave the DC in a crashed state, and the Framework would be waiting for the DC to answer a request --- a potential explanation for the observed symptoms. The team agreed this was worth testing: Efim proposed killing the DC process manually to see what the Framework does. Pavel Frolov expected the Framework would detect the error and self-terminate under normal conditions, but agreed it should be checked.

**2c. CPU Power Saving / COM Port Sleep (Juan Martinez)**

Juan asked whether the CPU has any built-in power saving features that could cause COM ports to fall asleep, and whether keep-alive messages are sent during SAS communication. Pavel confirmed they do not use any power savings. Juan followed up asking whether it could be a hidden BIOS feature, given the inconsistent behavior across markets.

**2d. AMD GPU Driver Issue (Genadi Peari)**

Genadi shared a link from the Qubes OS forum describing identical freeze/crash behavior on the same AMD Raven Ridge APU platform. The forum discussed kernel-level GPU driver issues. Pavel noted that JVL uses an older stable kernel (4.19) but could try the suggested kernel parameter amdgpu.noretry=0. However, he emphasized that reproducing the issue is priority number one.

Juan also shared AMD kernel parameters that other developers have used to resolve similar freezing: amdgpu.noretry=0 (disables retry on page faults), amdgpu.gpu_recovery=1 (enables GPU recovery), and amdgpu.gfxoff=0 (disables GFXOFF feature).

**3. Watchdog Timer Discovery**

This was the most significant finding in Segment 1. Val asked why the watchdog timer is not working and demanded a clear answer.

**3a. What is the start_game.sh Script?**

Pavel explained that the start_game.sh script functions as a basic software watchdog: if the framework application terminates, the script collects crash logs, attempts to send them to the server, and then forces a reboot. However, Pavel emphasized that they have never seen crash logs collected from an EGM after a freeze --- he believes the Linux operating system itself becomes non-operational during a freeze, meaning this software watchdog cannot help.

**3b. Hardware Watchdog Status**

Val asked three direct questions to Pavel, Genadi, and Alexander:

1.  Do we have the physical watchdog hardware on this board?

2.  Do we speak to this hardware on the software level?

3.  If yes to both, it should be easily testable.

Pavel found a disabled parameter in the IO board code: #define USE_HOPPER_IN_AS_WATCHDOG_RESET 1 (commented out). This was an optional channel line connected in place of a hopper to work as a reset trigger.

**Final answer from Pavel:** \"Currently we do not have external Watchdog wired. CPU hosted watchdog is not enabled on current software.\"

Val confirmed this aligned with his recollection that JVL previously had a standalone hardware watchdog chip, and that it was apparently removed or disconnected at some point during a hardware revision.

**3c. External Watchdog Discussion**

The team discussed how an external watchdog would work. Pavel explained the heartbeat mechanism: the main software sends a \"ping\" command to the watchdog hardware every 10 seconds. The watchdog listens and reinitializes a counter (e.g., 120 seconds) after each ping. If the counter reaches zero (no ping received), it triggers a hardware reset via a physical cable connected to the motherboard reset pin.

Pavel noted a downside: in both approaches (CPU-based or IO-board-based watchdog), the EGM would be physically rebooted without capturing information about the freeze cause. Pavel proposed two options:

4.  Add CPU-based watchdog to all future releases (Linux kernel + HAL)

5.  Implement watchdog on the IO board --- benefit: can be fixed via firmware update without resubmission to regulators. Would require one internal wire connecting the IO board to the motherboard. Alekseev could be asked to do the improvement.

**4. Requirement REQ-1028**

Juan Martinez drafted requirement REQ-1028 (\"EGM Auto-Restart and Watchdog Recovery System for Freeze Detection\") in JIRA, with detailed acceptance criteria and test cases.

Val corrected the framing: the requirement should not prescribe a watchdog timer (that's an engineering solution). Instead, the requirement should state: \"A machine should auto-recover in the event it permanently froze.\" How to achieve that is for the engineers to decide.

**5. Test Machines in Georgia**

Three test machines were set up in the Georgia office to attempt to reproduce the freeze:

  ------------- --------------------- ---------------------- -------------
  **Cabinet**   **Serial Number**     **Software**           **Build**

  FLEX D27      CM08-0825-230234      GCOAM-1.14.2.4.3.4.1   3817

  FLEX D27      CM08-0324-229600      GCOAM-1.14.0.4.3.4     3804

  FLEX V43      CM08-1224.230227      DLKG-1.13.0.4.3.4.2    3847
  ------------- --------------------- ---------------------- -------------

Anton started a CPU load stress script on one machine (v1000b0416f0f0153), spiking utilization to \~90%. This had not caused a freeze at the time of reporting.

**6. Key Decisions and Directives**

- Priority #1 is reproducing the freeze in a test environment.

- Killing the DC process should be tested to see if it causes the same symptoms as the observed freeze.

- REQ-1028 drafted for auto-recovery --- Val corrected its framing to be solution-agnostic.

- Watchdog timer must be re-enabled or re-implemented. Two paths identified (CPU-based or IO-board-based).

- AMD GPU kernel parameters (amdgpu.noretry=0, etc.) should be considered but are not the immediate priority.

**7. Open Questions at End of Segment 1**

- Why has the freeze not been reproduced in the lab despite CPU stress testing?

- Is this a hardware-level issue (AMD GPU driver / kernel) or a software-level issue (DC crash, Framework blocking)?

- Can the IO board watchdog be re-enabled using the existing (commented-out) code path?

- Do production mode vs. demo mode machines behave identically for testing purposes?

- Is the true scope of the problem larger than reported, given that locations sometimes reboot machines without notifying JVL?

*Source: Teams group chat \"GA Freezing Issue\" --- Segment 1 of 3*
