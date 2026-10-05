---
type: decision
title: Two FRAM chips come off the current IO board at once ($12 a board), the IO board is then redesigned to about half its cost with a new memory type and a modern USB controller, and the street-machine board grows out of that redesign
date: 2026-10-01
aliases: [two FRAM chips not populated, снимаем 2 чипа памяти, удешевляем его $12 на борт, 256 Mbit FRAM $6 each, not populate, IO board redesign half the cost, хотя бы в 2 раза, old USB controller hard to buy, динозавры, modern controller twice as cheap, street machine board from the IO board, аджастмент для борта на стрит машину, not enough interfaces on the Rockchip, USB hub printer card dispenser ports light support]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# Two FRAM chips come off the current IO board; the IO board is redesigned; the street-machine board grows out of it (Oct 1 2026)

Genadi Peari's plan, given when [[wiki/people/val-levitan.md|Val Levitan]] opened the [[wiki/meetings/2026-10-01-genadi-io-board-chips-flat-bom-pilot-and-street-cabinet-panel.md|Oct 1 2026 4:59 PM call]] (Russian) with "Говорим ещё раз, что нужно сделать?" — say again what is to be done. Val asked one question (what the chips are) and did not object; the segment ends on Genadi's "Всё" [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]. The derived notes record no formal decision and three undertakings in Genadi's name [[raw/Meeting_Notes_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]. It is recorded here as a decision because it is a concrete, costed plan stated to the owner at his request, with no objection, and because it changes the Sept-16 board plan (below).

## The three steps, in Genadi's words

1. **Now — two chips off the current board.** "Наш текущий [IO board] right away мы снимаем 2 чипа памяти, удешевляем его $12 на борт." Asked what they are: "[FRAM] чипы по 256 мегабит каждый чип стоит $6. Мы их просто… not populate." Why it is safe: "у нас нету требований увеличить записи, количество транзакций и объём транзакций" — there is no requirement to store more records or transactions [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].
2. **Next — review and redesign the existing IO board to cut its cost "хотя бы в 2 раза".** The redesign includes changing the type of memory ("заменой… типа памяти"), reviewing how the volatile memory is handled, and replacing the current USB controller, "который уже тяжело купить". "Сегодня надо современный контроллер" — much faster, much more capable, full functionality, "дешевле в 2 раза, потому что те уже очень старые динозавры" [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].
3. **Then — the street-machine board is an adjustment of that redesigned board.** "После этого на базе этого переделанного айо борта [мы] легко делаем [adjustment] для борта на стрит машину." It adds the interfaces the Rockchip platform lacks — "так как у нас не хватает интерфейсов на рокчип… поэтому борт мы договорились вынести" — a USB hub, ports for the printer and the card dispenser ("со спорты для принтера кардиспенсе"), light support, "и все необходимое, что для стрит машины нам будет не доставать" [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].

## How this sits against Sept 16 (evolution, not contradiction)

- **The street board is no longer a clean sheet.** On Sept 16 Genadi said the street machine's I/O board was "**под этот проект**" and "**чистый лист**" ([[wiki/decisions/2026-09-16-the-street-machine-carries-two-boards-and-a-new-io-board.md]]). On Oct 1 it is derived from the redesigned existing IO board. The later source is current; the Sept-16 interface list (USB hub, 2 SAS, printer port, bill-acceptor port, lighting) is not restated here — Oct 1 names a USB hub, printer and card-dispenser ports and lights. **"Card dispenser" is as spoken**; Sept 16 said bill acceptor, and no card dispenser has appeared in the street-machine thread before. Not reconciled on tape [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].
- **The memory cut now has a first step on the board in production.** Sept 16 planned one 256 FRAM instead of six on the *new* street board ([[wiki/decisions/2026-09-16-one-fram-chip-instead-of-six-and-low-power-mode-laid-in-but-not-populated.md]]). Oct 1 takes two 256-Mbit chips off the *current* board at once, $6 each. Whether the current board carries six chips (Pavel's Sept-16 count) and so goes to four is not said [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].
- **The old processor on the current board** was already called "древний" and "15 лет ему" on Sept 16; Oct 1 names the USB controller as the part that is hard to buy and to be replaced [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]].
- **Company economics only.** $12 a board, $6 a chip, a target of half the board cost — allowed under §15.8 (board economics). No named-person compensation.

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — stop populating the two 256-Mbit FRAM chips on the current IO board ($12 a board) — due unspecified ("right away") — [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — review and redesign the existing IO board to about half its cost: new memory type, volatile-memory handling reviewed, a modern USB controller in place of the hard-to-buy one — due unspecified — [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — derive the street-machine board from the redesigned IO board, adding a USB hub, printer and card-dispenser ports, light support and whatever else the street machine lacks on the Rockchip — due unspecified; follows the redesign — [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]

*(All three are stated as "we"; the notes assign them to Genadi as owner by implication. Recorded in his name.)* [[raw/Meeting_Notes_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]

## Open questions

- Does the street board carry a card-dispenser port (as spoken Oct 1) or a bill-acceptor port (Sept 16), or both? — [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
- Who does the redesign — Genadi himself, or [[wiki/people/evgeniy-alekseev.md|Alekseev]], who does the board work on Genadi's projects? Not said — [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]

**§15.8:** clear — board and chip economics only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
- [[raw/Meeting_Notes_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
