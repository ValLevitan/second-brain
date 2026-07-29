---
type: meeting
title: I/O-centric watchdog wiring (Mar-24 afternoon)
date: 2026-03-24
aliases: [IO-centric watchdog wiring, watchdog wiring Mar-24 PM, freezing watchdog wiring]
source-count: 1
---

# I/O-centric watchdog wiring (Mar-24 afternoon)

**Date:** 2026-03-24 (recording header 01:46pm, 57m 55s; Russian). Recording base `IO-centric_Watchdog_wiring-20260324_094646`.
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Genadi Peari.

The afternoon follow-on to the [[wiki/meetings/2026-03-24-fp10-freezing-watchdog-discussion.md|morning watchdog session]], with Genadi Peari added. Two threads: (1) wiring the IO-board watchdog — Genadi confirmed the IO board's existing **P2 connector** already has input/output pins with a line buffer, so a single wire to the motherboard reset pin can pull it low; and (2) Genadi's sustained "this is unsystematic" challenge, pushing to capture kernel logs (serial console / a diagnostic box) and to consult external hardware expert **Evgeniy Alekseev** before committing effort. This produced the idea of turning the IO board into a diagnostic co-processor / built-in "black box," and Val's decision to brief Alekseev and meet him the next morning.

Substance lives on [[wiki/topics/egm-freezing-investigation.md]] (the "Mar-24 watchdog architecture" section). The later shipped plan — kernel 5.10/5.15 upgrade plus the watchdog, all fixes in one release — is on the Mar-26 [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|initiative-priority schedule]]. The morning session on the same day is [[wiki/meetings/2026-03-24-fp10-freezing-watchdog-discussion.md]].

## Sources

- [[raw/I_O-centric_Watchdog_wiring.md]] — Mar-24 afternoon IO-board watchdog wiring + systematic-approach debate (transcript).
