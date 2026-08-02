---
type: meeting
title: GACOAM touchscreen investigation check-back (Jul 15 2026)
date: 2026-07-15
aliases: [GACOAM touchscreen investigation check-back, GA-COAM new software load touchscreen, 4119 touchscreen check-back, old-firmware flash experiment, peripheral device fail install, board flashing during install, duplicate mouse-emulation device, July 15 2026 touchscreen check-back]
source-count: 1
---

# GACOAM touchscreen investigation check-back (Jul 15 2026)

NOTES-ONLY · 15 July 2026, 3:01 PM ET · ~15m. **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]].

**Purpose:** the afternoon follow-up on the **same version-4119 touchscreen-loss defect** first triaged at [[wiki/meetings/2026-07-15-version-4119-touchscreen-loss-triage.md|the 11:01am triage]], reviewing the findings since the morning call. The two leading theories were both dropped (USB port-mapping ruled out by an AI old-vs-new comparison showing identical mapping; a newly-found duplicate mouse-emulation device ruled out as non-interfering), so no code-level cause was confirmed. The team agreed a **new controlled experiment** — flash **old** firmware onto the control boards, install the old software, then install the new version on top — to test whether the **background flashing of all boards during install** is what causes the intermittent failures. [[wiki/people/felipe-miranda.md|Felipe Miranda]] (transcribed "Philippe"), who keeps installing the software himself in the field, was to boot a faulting machine with two USB sticks and capture logs for the team.

The durable substance — the ruled-out USB-mapping and duplicate-device theories, the leading old-firmware-flash board experiment, the "peripheral device fail" install cause (missing/failed iBoard or counter-board, both flashed during install), the installer hiding the background board-flashing, and the field-log collection plan — lives on:
- [[wiki/projects/georgia-market-rollout.md]] (Jul-15, the ARC roll-out block).

This 3:01pm check-back and the 11:01am triage are **two distinct sessions on the same defect** (morning triage → afternoon findings), not re-transcriptions of one another.

§15.8 clear — field-defect / device / roll-out engineering only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_GACOAM_Touchscreen_Investigation_Check_Back-July-15-2026.md]]
