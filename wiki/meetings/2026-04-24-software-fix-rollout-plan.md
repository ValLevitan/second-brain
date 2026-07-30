---
type: meeting
title: JVL Software Fix Rollout Plan (Apr 24 2026)
date: 2026-04-24
aliases: [Software Fix Rollout Plan, freezing fix rollout, free software upgrade, kernel fix rollout, COM ID tracking, uptime equals revenue, watchdog not to be mentioned, flagship operators first, 2065 cabinets, free upgrade letter]
source-count: 2
---

# JVL Software Fix Rollout Plan (Apr 24 2026)

**Date:** 24 April 2026, 8:34pm Eastern (§11 recording header; recording-filename stamp `_163400` differs — header wins); ~1h.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]], [[wiki/people/juan-martinez.md|Juan Martinez]].

Felipe walked Val and Juan through a phased plan to roll the **kernel-fix (freezing) software** out across the Flex field fleet (~2,065 cabinets identified so far, likely more; Irina's Minsk serial list is incomplete). This is the **downstream field-deployment stage of the EGM freezing investigation** — the resolution the freezing corpus pointed at (kernel upgrade 4.19→5.15 LTS plus watchdog/auto-reboot). Val's central rulings: give the ~$2,500 software **free of charge** (no deadline, no carrot-and-stick charging model), because operators respond only to the **uptime-equals-revenue** argument, not pricing pressure; **do not mention the watchdog timer or generic "stability improvements"** in operator-facing communication (they expose an inadequate prior design) — communicate only the specific processor/kernel-incompatibility root cause; **re-upgrade the flagship operators JVL had already put on the freezing build FIRST**, immediately after the bulletin; and accept the **COM ID captured at install** (tied to JVL serial) as the field-tracking mechanism in place of the failed QR-code scanning — the free software offered in exchange for the COM ID. Val will draft the official statement by **Monday Apr 27**. The freezing root cause, the fix, and this rollout live on [[wiki/topics/egm-freezing-investigation.md]] (Apr 24 2026 section); the release-delivery mechanics (per-serial JVL builds + RIS, USB/dongle vs emailed-file delivery) are noted on [[wiki/topics/github-release-management-pipeline.md]]. §15.8 clear — product/market/machine economics only (software price, per-copy charge, USB budget, fleet counts), no named-person compensation. [[raw/Meeting_Notes_software_fix_rollout_plan-April-24-2026.md]]

## Sources
- [[raw/Meeting_Transcript_software_fix_rollout_plan-April-24-2026.md]]
- [[raw/Meeting_Notes_software_fix_rollout_plan-April-24-2026.md]]
