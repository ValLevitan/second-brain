# Georgia Machine Freezing — Meeting Summary

**Date:** March 9, 2026  |  **Duration:** 1 hr 23 min

**Attendees:** Juan Martinez, Felipe Miranda Giorgi, Genadi Peari, Pavel Frolov

---

## Executive Summary

The team convened to address a critical and recurring issue: JVL FLEX D27 gaming machines freezing intermittently in the Georgia field, typically 2–3 days after boot. The freezing has been reported across multiple software versions (Peach 1, Peach 2, Peach 3, Diamond Link) and has intensified since the deployment of the new nudge software (38xx series). The issue is directly impacting field revenue—machines with the new nudge are underperforming by up to 50% compared to old software—and is damaging operator confidence in JVL products, threatening future sales.

A frozen machine was discovered at a field location on Valentine's Day and remained inoperable for over a week before being noticed, representing a total loss of revenue for that period. Felipe confirmed that out of 10 machines prepared in the warehouse, 4 froze within a few days while 6 did not—demonstrating the inconsistent, hard-to-reproduce nature of the problem.

The root cause remains unidentified. Temperature was previously suspected but has been ruled out through testing. RAM (8 GB vs. 16 GB) was a historical factor for some older cases but is not the current issue. The leading hypothesis centers on the NVMe SSD adapter: the current Tank motherboard uses an NVMe-to-PCIe adapter to connect the SSD, whereas a Sapphire ("Mexico") motherboard with a native NVMe slot has not exhibited freezing. However, this has not been definitively proven. Log files have not yielded actionable diagnostics despite years of investigation, and the Minsk QA lab cannot reproduce the issue (open-bench setups in cold conditions vs. enclosed cabinets in warm Georgia environments).

---

## Key Discussion Points

### Freezing Pattern & Business Impact

- Freezing occurs 2–3 days after boot/software install, or sometimes never. No consistent trigger identified.
- New nudge software (38xx series) machines underperforming by up to 50% vs. old software—potentially explained by unreported freezes causing extended downtime.
- Operators are losing confidence; Felipe's machine sales have declined. Genadi warned that customers will stop buying entirely if unresolved.

### Root Cause Theories Explored

- **Loose SSD connector** (Val's suggestion): Dismissed as unlikely by the team; connectors are either in or out.
- **Temperature/overheating:** Ruled out. Tilt system correctly detects high temps; freezes occur even when CPU is cold.
- **Insufficient RAM:** Historical factor (8 GB machines), but not the current issue on 16 GB machines.
- **NVMe SSD adapter (leading theory):** Current Tank motherboard uses a PCIe-to-NVMe adapter with long wire traces and potentially inadequate capacitors. The Sapphire ("Mexico") board with native NVMe slot has not frozen.
- **Software-driven SSD access:** Pavel confirmed that after boot, most data runs from RAM, but video files are still read from SSD at runtime. New software may do more intensive read operations.
- **Memory leak:** Claude AI analysis flagged it, but Pavel confirmed memory stabilizes at ~5.1 GB after boot—not a leak.

### Log File Analysis Limitations

- Three years of log review have not yielded a root cause. Genadi stated the logs lack the right information because developers didn't instrument for this failure mode.
- SSD communication failures would not appear in application logs. Improving logging would require a software rewrite—unhelpful for already-deployed field software.
- Juan's Claude AI analysis of a log file surfaced 10 overheating events, WebSocket blocking errors, and a power warning from the I/O board. Pavel assessed these as normal operational events, not root causes.

### QA & Testing Gaps

- Minsk QA has 3 machines, all open-bench (no cabinets), in a cold environment. Freezing has never been reproduced there.
- Genadi called the current practice of testing in the field "the worst practice" and emphasized the need for proper QA with fully assembled cabinets.
- Approximately 250 Altera machines in Georgia (same motherboard/adapter config) have not had reported freezing—a significant data point that complicates the pure hardware theory.

### Possible Remediation Paths Discussed

- **Switch to Sapphire (Mexico) motherboard:** Native NVMe, no adapter. ~$100 more per unit. Already GLI-approved. Val reportedly resistant to this approach.
- **Switch to SATA SSD on current board (eliminate adapter):** Requires software HAL changes + new installer scripts + GLI re-certification (~$10K per software version, ~45 days each, 5 new software packages). Slower boot only; no gameplay impact.
- **Test alternate NVMe adapters:** Pavel noted current adapter has long wire traces and small capacitors. Replacement adapters may improve stability, though the existing adapter is glued to the motherboard (removable with effort).
- **Software experiment to halt post-boot SSD reads:** Pavel will test in Minsk whether blocking NVMe reads replicates the freeze, which would confirm or rule out the SSD communication theory.

---

## Action Items by Assignee

### Juan Martinez

| #   | Action Item                                                                                                    | Priority   |
| --- | -------------------------------------------------------------------------------------------------------------- | ---------- |
| 1   | Send company-wide email recommending a halt to Georgia machine shipments until the freezing issue is resolved. | **URGENT** |
| 2   | Update Val Levitan on the call outcomes, action plan, and severity of the situation.                           | **URGENT** |
| 3   | Share Claude AI log-file analysis findings with the engineering team for review.                               | HIGH       |

### Felipe Miranda Giorgi

| #   | Action Item                                                                                                         | Priority |
| --- | ------------------------------------------------------------------------------------------------------------------- | -------- |
| 1   | Collect and distribute log files from the recently rebooted frozen machine to the team.                             | HIGH     |
| 2   | Confirm with Elizabeth that the rebooted machine is unfrozen and operational; report status to the group.           | HIGH     |
| 3   | Contact Camilo in Mexico/Colombia to inquire whether machines with Sapphire motherboards have experienced freezing. | HIGH     |
| 4   | Implement a 3-day minimum burn-in testing protocol for all machines prior to customer shipment.                     | MEDIUM   |
| 5   | If directed, set up additional test machines using the Sapphire (Mexico) motherboard for comparative testing.       | MEDIUM   |

### Pavel Frolov

| #   | Action Item                                                                                                                                               | Priority |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 1   | Conduct experiments to simulate SSD read failures by removing/blocking NVMe file access during runtime to determine if it replicates the freeze behavior. | HIGH     |
| 2   | Test whether re-establishing SSD communication after a simulated failure auto-resolves the freeze or requires a full reboot.                              | HIGH     |
| 3   | Compare log files from different dates (pre-freeze vs. post-reboot) for anomalies not visible in static analysis.                                         | MEDIUM   |
| 4   | Investigate whether reducing or eliminating runtime SSD read operations (e.g., video file reads) could prevent freezes.                                   | MEDIUM   |

### Genadi Peari

| #   | Action Item                                                                                                                                                                                                               | Priority |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 1   | Evaluate the feasibility of hiring a specialist with low-level hardware/software debugging expertise to investigate the root cause.                                                                                       | HIGH     |
| 2   | Coordinate with Val on the contingency plan: if freezing persists, assess switching production to the Sapphire motherboard (native NVMe slot, no adapter) or modifying software to support SATA SSD on the current board. | HIGH     |
| 3   | Define expanded testing requirements for Minsk QA, including shipping fully assembled cabinets (not open-bench setups) to replicate field conditions.                                                                     | MEDIUM   |

### Genadi Peari / Pavel Frolov (Joint)

| #   | Action Item                                                                                                                                   | Priority |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------- | -------- |
| 1   | Determine whether a software modification to stop post-boot NVMe communication is viable and testable without requiring GLI re-certification. | HIGH     |
| 2   | Assess alternate NVMe-to-PCIe adapters (shorter wire lengths, better capacitors) as a potential interim hardware fix.                         | MEDIUM   |

---

## Open Questions

- Why do ~250 Altera machines with the same motherboard/adapter configuration not exhibit freezing?
- Why have no freezing reports come from South Dakota or Nebraska (30+ machines, same build process)?
- Why did one test machine (serial 229600) stop freezing on its own after Jan 29 with no changes made?
- Is the 50% revenue underperformance of new nudge machines explained by unreported freezes, or is there an additional software/math issue?
- Have the machines shipped to Mexico (with Sapphire boards) experienced any freezing over their operational lifetime?
