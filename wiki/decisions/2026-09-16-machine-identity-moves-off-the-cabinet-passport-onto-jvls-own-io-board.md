---
type: decision
title: Machine identity moves off the cabinet-bound passport component and onto JVL's own I/O board
date: 2026-09-16
aliases: [passport component removed, убрать эту конструкцию, идентифицировать по I/O борту, cabinet ID, ID кабинета, identify by the processor board, RK3576 board identifier, our own board is more reliable, board change procedure, процедура смены борта, machine identity street machine]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Machine identity moves off the cabinet passport onto JVL's own I/O board

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept 16 2026 12:35 PM ET alignment call]] (held in **Russian**), after [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/genadi-peari.md|Genadi Peari]] had already worked the question out between themselves. It applies to the [[wiki/topics/low-cost-street-machine.md|street machine]].

## What the passport is, in Genadi's own description

> "**Паспорт у нас заложен как [piece] в памяти такой … [к]риптод, который притащит[ся] кабинету. Котор[ый] нельзя … по определению [оторвать]. И по нему мы определяем … ID кабинета.**"
> — an encrypted piece of memory bound to the cabinet, which by definition cannot be detached from it, and by which the cabinet's ID is determined.
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

Pavel put the same point as a design constraint: "**Предыдущее решение с паспортом подразумевало, что этот паспорт неразрывно связан с кабинетом, его невозможно оттуда оторвать**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## The ruling

Genadi put the question to Val plainly — "**Мы хотим [поддерживать] в таком виде это или убрать[?]**" — and Val answered:

> "**Нет. Вы можете убрать эту конструкцию и привязывать только всё в [I/O] борту.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

Genadi confirmed the target and added what happens to the contents: "**Либо к нашему i[-]борту, скорее всего, лучше даже… и всё, что в паспорте хранишь[,] на своем … кусочк[е] мемори[и] у себя, и всё**" — the passport's contents stay, on a slice of the I/O board's own memory [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**This removes a dedicated cabinet-bound component, not the passport itself.** It therefore does **not** overturn [[wiki/decisions/2026-09-11-the-passport-is-preserved-and-jvl-is-using-the-bindings-wrongly-in-this-market.md|the Sept 11 ruling that the passport must be preserved]] — that ruling is about the binding *feature* on the installed fleet, and neither source mentions the other. Recorded side by side, not merged.

## Why the I/O board and not the processor board

Pavel's first proposal was the processor board: "**идентификатор платы мы можем брать на RK 35 76, идентифицировать её именно … процессорной платой, а не кабинетом**", and "**отдельную микросхему можем не ставить[;] … лучше отказоустойчивость даже будет**" — no extra chip, and better fault tolerance [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Genadi's counter won the argument and it is a supply-chain argument, not a technical one:

> Genadi: "**А почему мы не идентифицируем нашим [MC]? На е[ё] борте.**"
> Pavel: "**Мы тоже можем … на [I/O board,] мы тоже можем.**"
> Genadi: "**Потому что это наша … более надежная [шт]ука[;] поменяешь завтра ещё что[-]то … [д]ругого производителя. Нашу — нет.**"
> Pavel: "**Ну а наш[у] мы не меняем.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

JVL does not change its own board; it might change processor-board suppliers. Pavel then closed it himself: "**давайте тогда зафиксируемся и будем идентифицировать [по I/O борту]**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Genadi's opening instinct — reuse a sector of the existing ferromagnetic memory rather than add a part, "**зачем нам … [э]кстра компоненты[?]**" — pointed the same way [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. And Val's own starting position, before the discussion, had been the opposite of where he landed: "**нам нужно паспорт опять**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## How this was actually decided — worth recording

The engineering choice was made **while Val was off the call on a phone call** (he stepped away at 00:45:21 with "**мне нужно общаться на звонок, продолжайте**" and returned at 00:54:42). Pavel and Genadi settled it between themselves in that window; Genadi then re-put it to Val from the top when he came back, and Val ruled at 00:57:37. The record is a two-stage one, not a single moment [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. See the §12 note on [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md]] for Val's absences on this call.

## Open questions

- **What happens when the I/O board is replaced?** Genadi asked for the board-change procedure — "**А как? … [п]роцедура смены борта**" — Pavel offered a comparison the transcript renders "**[к]ак на этих самых на альтерах**" (not interpretable; left as transcribed) and named "**[и]дентификатор**"; Genadi answered "**Я не знаю. Я не, я не знаю.**" **Nobody answered it, and the machine's identity now depends on it.** [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**§15.8:** clear — product identity design only; no named-person compensation. **§15.9:** no identifier values appear here — this page records *how* a machine ID is anchored, never an actual ID.

## Sources

- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
