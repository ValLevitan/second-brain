---
type: meeting
title: FP10 freezing watchdog discussion (Mar-24 morning)
date: 2026-03-24
aliases: [FP10 watchdog discussion, watchdog discussion Mar-24 AM, freezing watchdog design]
source-count: 1
---

# FP10 freezing watchdog discussion (Mar-24 morning)

**Date:** 2026-03-24 (recording header 09:19am, 31m 9s; Russian). Recording base `FP10_Freezing_Issue_Watchdog_Discussion-20260324_051935`.
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko (Sasha / "Biratka").

The morning working session that turned the manufacturer's freezing advice into a concrete engineering plan: confirm the **Linux kernel 5.15 upgrade** (BIOS untouched — the manufacturer says it is a kernel problem, not a BIOS one), weigh the three watchdog options (CPU-internal / SuperIO-BIOS / a new IO-board-centric one), and land on Alexander Biratko's **IO-board watchdog** design as the preferred permanent solution. Task split: Biratko leads the IO-board firmware, Pavel supports and does the kernel upgrade; Genadi to identify the reset pins.

Substance lives on [[wiki/topics/egm-freezing-investigation.md]] (the "Mar-24 watchdog architecture" section). Board-level context: [[wiki/topics/omni-core-advancement-and-game-templating.md]] (the IO-board watchdog is designed to carry forward to the future Omni platform). The afternoon follow-on with Genadi is [[wiki/meetings/2026-03-24-io-centric-watchdog-wiring.md]].

## Sources

- [[raw/FP10_Freezing_Issue_Watchdog_Discussion.md]] — Mar-24 morning watchdog-design call (transcript).
