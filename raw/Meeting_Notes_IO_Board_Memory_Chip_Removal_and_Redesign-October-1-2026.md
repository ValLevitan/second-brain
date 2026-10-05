# Meeting Summary — Various
**Date:** October 1, 2026, 4:59 PM – 5:01 PM Eastern
**Duration:** About 2 minutes
**Segment:** Segment 1 of 3
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026]]

Teams meeting organized by Val. Held in Russian. Val asked Genadi to repeat what needs to be done; Genadi gave the plan. Other segments: [[Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026]], [[Meeting_Notes_Street_Machine_Cabinet_Dashboard_and_Printer_Access-October-1-2026]].

## Summary

**Step 1 — remove two memory chips.** On the current IO board, do not populate the two FRAM chips (256 Mbit, $6 each). This saves $12 per board. There is no requirement to store more transactions, so the board stays as is otherwise.

**Step 2 — redesign the IO board.** Review and redesign the existing IO board to cut its cost, at least in half if possible. This includes changing the memory type, reviewing how volatile memory is handled, and replacing the current USB controller, which is now hard to buy. A modern controller is faster, more capable, and about half the price.

**Step 3 — street machine board.** Use the redesigned IO board as the base for the street machine board. Add the interfaces the Rockchip platform lacks: Genadi said it was agreed to move this to a separate board, with a USB hub and ports for the printer and card dispenser, light support, and anything else the street machine needs.

## Decisions Made

No formal decisions recorded. (Genadi referred to an earlier agreement to move the extra interfaces to a separate board.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Stop populating the two FRAM chips on the current IO board | TBD | Normal | Saves $12 per board; stated as "we" |
| 2 | Genadi Peari | Review and redesign the IO board: new memory type, modern USB controller, target about half the cost | TBD | Normal | Stated as "we"; owner implied |
| 3 | Genadi Peari | Base the street machine board on the redesigned IO board, adding USB hub, printer and card dispenser ports, and lights | TBD | Normal | Follows item 2 |

## Open Questions

None.

## Dispatch Log

---
*Processed from Teams transcript on October 1, 2026, 6:15 PM Eastern*
*Source meeting: Various*
