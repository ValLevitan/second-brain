---
type: meeting
title: Georgia freezing troubleshooting direction (Mar 13 2026)
date: 2026-03-13
aliases: [Georgia freezing troubleshooting direction, IP-1027 monitoring tool]
source-count: 1
---

# Georgia freezing troubleshooting direction (Mar 13 2026)

**Date:** 2026-03-13 (header 1:08pm local; recording base `Georgia_Freezing_troubleshooting_direction-20260313_090811`, 15m6s).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] (Russian).

Short working call setting the concrete direction for the Georgia freeze — substance on [[wiki/topics/egm-freezing-investigation.md]]. Pavel presents the JIRA product he formalised from two prior calls with Anton: **IP-1027, a "Monitoring Tool for Gaming Machine"** (split off from the IP-688 diagnostic tool), with initial features **metrics collector, data exporter, disk-stress loader**, and a **watchdog/monitor** — writing data **not to the machine's own SSD** but to an external USB or a Python server on the in-network laptop. A disk-stress load (frequent SSD reads) is added to surface freezes faster. Val agrees the direction and shifts to the physical setup: work remotely against the **3 test machines** in the Georgia (Lawrenceville) office (2 of which freeze reliably ~every 15 min) via Felipe's connected laptop; production builds limit what can be installed, so utilities are pulled from Linux 14.2 repos or run from the non-system disk. Anton to write the scripts first (starting today) and deploy over the coming days; the project is priority #1 but not full-time. Val to reconvene Thursday with Anton.

§11 header date 2026-03-13. §15.8 clear — machine reliability / tooling only, no named-person compensation.

## Sources
- [[raw/Georgia_Freezing_troubleshooting_direction-March-13-2026.md]]
