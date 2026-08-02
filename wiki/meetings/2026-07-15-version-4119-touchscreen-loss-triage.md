---
type: meeting
title: Version 4119 touchscreen-loss triage (Jul 15 2026)
date: 2026-07-15
aliases: [Version 4119 touchscreen loss triage, 4119 touchscreen loss, touchscreen stops working after 4119 upgrade, ARC roll-out touchscreen block, touchscreen firmware reflash, USB port mapping touchscreen, July 15 2026 touchscreen triage]
source-count: 1
---

# Version 4119 touchscreen-loss triage (Jul 15 2026)

NOTES-ONLY · 15 July 2026, 11:01 AM ET · ~26m. **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]].

**Purpose:** morning triage of a **field defect — touchscreens stop working after the version-4119 software upgrade**, which is **blocking the roll-out to the Georgia operator ARC**. [[wiki/people/felipe-miranda.md|Felipe Miranda]] (transcribed "Philippe") had sent a list of the affected machines and said he had raised the problem before. Most of the call was Val coaching Pavel and Irina to **triage and theorize root cause themselves before delegating to a specialist** — the earliest moment is the cheapest moment to solve it. The team set aside the first (firmware-version) theory and settled on the leading suspect (a USB-port / touchscreen-to-display **mapping** change in the new Linux), agreeing to reason through the software mapping rather than keep physically reproducing on machines. Val was to rejoin a follow-up call the same afternoon to review theories.

The durable substance — the defect, the triage findings (firmware theory ruled out via passport data, reproduction failed on 3 machines), the leading USB-mapping theory, and the process rule that Pavel and Irina must triage before delegating — lives on:
- [[wiki/projects/georgia-market-rollout.md]] (Jul-15, the ARC roll-out block).

The afternoon follow-up on the same defect is [[wiki/meetings/2026-07-15-gacoam-touchscreen-investigation-check-back.md|the 3:01pm check-back]]. This 11:01am triage and that 3:01pm check-back are **two distinct sessions on the same defect** (morning triage → afternoon findings), not re-transcriptions of one another.

§15.8 clear — field-defect / device / roll-out engineering only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_Version_4119_Touchscreen_Loss_Triage-July-15-2026.md]]
