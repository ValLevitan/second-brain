**Initiative Priority Schedule**

Meeting Report

March 26, 2026

**Duration:** Part 1: 28m 30s \| Part 2: 24m 5s

**Participants:** Val Levitan, Irina Shishko, Pavel Frolov

**Objective:** Establish implementation priorities for the next 2 weeks and sketch out tasks in Jira.

Part 1: Priority Definition

Process Notes

- Val emphasized planning at the feature/branch level tied to GitHub, with developers involved earlier in feature writing to avoid architectural misalignment.

- Transition to Kanban (from sprints) is planned but will be gradual. Pavel's current sprint ends next Wednesday.

Three Priorities for the Next 2 Weeks

1\. Fix the Machine Freeze Bug

- Machines crash/freeze when entering Setup mode. The setup process triggers event handling that causes a kernel crash, leaving the machine unresponsive.

- Clients mistakenly attributed the issue to QR code scanning (which they happened to be doing at the time).

- The bug description needs to be updated to reflect the actual root cause (Setup mode event handling, not QR scanning).

2\. Upgrade Linux Kernel to 5.10 or 5.15

- Pavel reproduced the freeze using a kernel-hang function --- confirmed it results in a kernel crash with a hung screen every time.

- Root cause is likely GPU-related kernel bugs in the current version.

- Moving to a newer stable kernel should resolve these.

3\. Implement Watchdog Timer / Crash Recovery

Four options were discussed:

1.  **Option 1:** Internal CPU watchdog (already implemented, shipped to Nebraska & Texas)

2.  **Option 2:** External hardware watchdog chip on the PCB --- Val's initial preference, but Pavel argued against it (different chips per board revision, complications during installation/setup mode)

3.  **Option 3:** Software-based monitoring via data center / aioboard communication

4.  **Option 4:** Enable the standard Linux panic kernel parameter for auto-reboot on kernel panic (e.g., 10-second timeout) --- a well-established parameter that was simply never enabled

**Decision:** Go with Option 4 (kernel panic auto-reboot) combined with Option 1 (built-in watchdog already shipped). Pavel noted this is the simplest, most reliable approach with the fewest edge cases.

Part 2: Release Planning & Execution

Release Strategy

**Key decision:** All three fixes (Setup crash fix, kernel upgrade to 5.15, kernel panic auto-reboot) ship together in ONE release per product --- no piecemeal releases. No new games included; patches apply to currently released software only.

*Val explicitly rejected the idea of shipping only the auto-reboot parameter without the kernel upgrade --- "customers will just see the machine freeze, reset, and freeze again."*

Rollout Order & Timeline

  -------- ---------------------- ---------------------------------------------------------------------------------------------- -----------------
  **\#**   **Product**            **Notes**                                                                                      **Estimate**

  1        **Nebraska & Texas**   Easiest --- no certification required                                                          \~2 weeks

  2        **South Dakota**       Certification needed (GLI commission); old game packages only --- new games would add months   +1 day after #1

  3        **Georgia**            Goes through Eclipse (Alex); new games not until May+                                          +1 day after #2
  -------- ---------------------- ---------------------------------------------------------------------------------------------- -----------------

**Total target: \~3 weeks to complete all three rollouts.**

Effort Estimates

- **Setup crash fix:** 1--2 days

- **Kernel panic timeout parameter** (Option 4 on existing 4.19 kernel): \~1 day (quick fix, but filesystem templates for debug/production need prep)

- **New kernel 5.10/5.15 build:** 2--3 days (Pavel --- source mirroring, config tuning, conflict resolution)

- **Testing after kernel upgrade:** Up to 2 weeks (printers, validators, SAS, games). Pavel suggested simplifying: one printer type is sufficient to validate.

Assignments

  ----------------------- ----------------------------------------------------------------------------------
  **Person**              **Task**

  **Pavel Frolov**        Kernel 5.15 build, config parameter tuning, integration

  **Andrey Bosik**        Mirror Linux kernel sources to GitHub (background, \~1 day)

  **Evgeniy Kharetski**   Setup crash fix (South Dakota task first, then moves to next)

  **Irina Shishko**       Testing coordination, release management

  **Elizabeth**           On-site testing when builds are ready

  **Alexander Biratko**   Reassigned FROM external watchdog timer work TO bill/cash dispenser for FlexFare
  ----------------------- ----------------------------------------------------------------------------------

Secondary Initiative: Maple (Texas)

After the main fixes, as people free up:

- Refit old touchscreen TVs (from Columbia, Mexico) using the same motherboard + Texas framework

- Uses Reliance printers (Val correcting a prior statement to Gennady that Maple might go without one)

- **Team:** Pavel, Evgeniy, Anton (framework support if needed), Vladimir

- **Blocker:** No test hardware available --- Pavel to buy 2 non-standard resolution TVs locally (shipping from elsewhere would take a month)

Undertakings (Action Items)

1.  **Pavel & Irina:** Review the transcript, record audio comments on any deviations/corrections, create a combined transcript

2.  **Pavel & Irina:** Create Jira features from the transcript, break into tasks, assign to people

3.  **Val:** Send Gennady a note correcting yesterday's statement --- Maple most likely WILL need a Reliance printer

4.  **Pavel:** Verify whether the already-shipped CPU watchdog (Option 1, in Nebraska/Texas release) triggers a reset on kernel panic --- can test immediately

5.  **Pavel:** Start kernel 5.15 work immediately (Andrey mirrors sources in parallel)

6.  **Team:** Start assembling a Maple test machine ASAP --- the sooner missing parts are identified, the better
