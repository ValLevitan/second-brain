---
type: decision
title: The Epic 950 is the priority printer for the terminal and the only one tested actively for now; other models, the Epic Edge included, stay supported; Pavel writes the supported-printer requirement
date: 2026-10-05
aliases: [Epic 950 priority, эпик 950, Epic Edge, эпик eдж, supported printer models, какие принтеры мы поддерживаем, printer requirement, Pavel writes the printer requirement, Павел должен сделать, printers differ, 5-second print timeout, тайминг 5 секунд, TransAct housed printer]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# The Epic 950 is tested first; all printer models stay supported

Settled at the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 MVP 1 call]] (Russian, 8:01 AM) by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/val-levitan.md|Val]] assigning the write-up [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The question

[[wiki/people/alexei-khamin.md|Alexei Khamin]]: the autotests found that the requirements do not say which printers the terminal supports. Emulators already exist, so the team needs to know what to aim at: "хорошо бы добавить модельки" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## What was said

- **Pavel — the Epic 950 first.** Genadi contacted the TransAct printer makers, who have a printer with a housing; "внутри, по сути, там будет стоять эпик 950. Скорее всего, это приоритет номер один." He first thought the Edge was the same printer, only with USB as well as RS-232 [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].
- **[[wiki/people/dmitri-chudinov.md|Chudinov]] — printers do differ.** The Rust print library was tested on a simple ticket. Then the richer Flex IQ ticket came (more fields, more text), and printing got slower. One printer printed fast, the other slower, and one failed with a print error. The print timeout was 5 seconds; it was enough before and not after, so it was raised: "Ну сейчас печатает всё хорошо" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].
- **[[wiki/people/irina-shishko.md|Irina]]:** on the machines, too, the printers "явно работали поразному" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The ruling

Pavel: "мы тогда можем остановиться эпик 950 эпик eдж проверяем и на том, и на том". Then, to [[wiki/people/ivan.md|Ivan]]'s question about support: "Я за то, чтобы все все поддерживать, но просто сейчас не активно не тестировать это." Khamin asked that someone put it in the requirements. Val: "Павел должен сделать рекламу" (the requirement — "рекламу" is a garble of "реквайремент", the notes' reading). Pavel: "Окей." [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

In one line, as the derived notes read it: **the Epic 950 is the priority and the only printer tested actively for now; all models stay supported, the Epic Edge included** [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]. *Ivan's lines on the Edge are garbled ("Только 950 эдже не будет"; "пока что эдж идет от 50, хорошо?"), so whether the Edge is tested now is not fully clear in the transcript.*

## Where it sits

- The TransAct housed unit with the Epic 950 inside is on [[wiki/decisions/2026-09-23-jvl-stops-building-its-own-tito-desktop-box-and-uses-jcm-or-transact-for-now.md]] (Sept 25).
- The same printer was chosen for South Dakota in 2025 — [[wiki/decisions/2025-01-22-support-epic-950-printer-for-south-dakota.md]] (context, not a citation).
- On Oct 1 a printer-library change made for the Epic 950 stopped the e-wallet ticket printing — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 1, 4:48 AM). That is context for why "printers differ".

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — write the requirement listing the supported printer models — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

**§15.8:** clear. **§15 #9:** none; "950" is a model number.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
