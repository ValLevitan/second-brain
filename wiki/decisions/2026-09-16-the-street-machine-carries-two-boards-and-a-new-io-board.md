---
type: decision
title: The street machine carries two electronic boards — a new I/O board and a button/counter board — and the existing all-in-one board is scrapped
date: 2026-09-16
aliases: [two electronic boards, 2 борта электронных, ibort и батон борт, new I/O board street machine, button counter board, USB hub 2 SAS printer port bill acceptor, ID003 and ccTalk, pulse is not used in gaming, ай борт, батон борт, четыре канала сериал портов, street machine electronics spec, amplifier dropped use the TV's own, cell modem and WiFi mandatory, no electromechanical counters]
source-count: 2
status: active
open-commitments: 2
open-questions: 3
---

# The street machine carries two electronic boards — a new I/O board and a button/counter board

Settled at the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept 16 2026 12:35 PM ET alignment call]] (held in **Russian**) by [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]] working the cost problem together, with [[wiki/people/val-levitan.md|Val Levitan]] ruling on the items that were put to him. Genadi's closing count: "**будет 2 борта электронных**" — there will be two electronic boards. Pavel: "**Согласен**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

This is the electronics half of the [[wiki/topics/low-cost-street-machine.md|low-cost street machine]]. The cabinet half of the same call is on [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]].

## The two boards

- **An I/O board** — a **new** one, designed for this project. Asked whether it should be made "relatively universal" or "specifically for this project and it goes nowhere else", Genadi's answer was "**Мне кажется под этот проект**" — for this project [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **A button/counter board**, needed "**для поддержки кнопочек … там и подсветки какие[-]то базовые**" — to support the buttons and some basic lighting. Pavel had asked whether it was needed at all; Genadi's argument settled it: "**А как ты будешь 8 кнопочек тянуться с двери**" — how will you run eight buttons all the way from the door — "**8 линий**", eight lines. Pavel: "**всё правильно… Скорее всего, это всё-таки надо**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Pavel recorded the agreement: "**на 2 платы, значит, мы согласились — ibort и … батон борт**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## What the new I/O board carries

Genadi read the list back, twice, and it is the specification:

> "**usb house, 2 sassa. Один принтер, один билаксептер.**"
> "**нам надо 2 порта … [ID003] и [ccTalk]. Нам нужно порт для принтера, нам нужно 2 [SAS], usb house. И поддержку всех лайц, которые мы заложим. Вот это нужен такой новый iobord.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

So: a **USB hub**, **two SAS ports**, **one printer port**, **one bill-acceptor port**, and **support for whatever lighting is specified**. Pavel counted the serial side as **four serial-port channels** — "**туда 2 саса и опциональный принтер и опциональный билакцептор. То есть нам вот 4 канала сериал портов надо вынести туда**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Val had already set the two SAS ports himself earlier in the call: "**Естественно, должно стоять 2 саспорта**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**The bill acceptor is ID003 and ccTalk. Pulse is out, and it was ruled out without asking anyone.** The transcript renders the two protocols as "**ай дизеро зеленого 3**" and "**сиситок**" — ID003 and ccTalk by context. Genadi first said "**Не знаю насчет полсы**" (I don't know about pulse), Pavel offered to make it jumper-selectable — "**либо на [RS-]485 либо на [ccTalk]**" — and Genadi then closed it flatly: "**Палз, мы не можем использовать в гейминг**" and "**Не годится, не делаем, даже не спрашиваем**" — not suitable, we don't do it, we don't even ask. Val agreed: "**не можем, нет**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**The board sits at the front, with all connections reachable** — Genadi: "**Как вы говорите, дефронт со всеми подключениями**". Pavel's concern was port orientation: the ports "**на лицевую панель, наверное, должны смотреть**", or else the board turns 90 degrees, so long as "**не было вот этого сбоку втыкании**" — no more plugging in sideways. Genadi: "**Неважно, куда какая разница… Если перед лицом, то неважно. Если не на … карачках**" — it does not matter where, as long as it is in front of your face and not on all fours [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## What comes off

- **The audio amplifier is dropped; the TV's own is used.** Genadi: "**Амплифар мы можем выкинуть, использовать [built-in], который … [в TV] стоит. Требования … в машине, аудио нету больших**" — no serious audio requirement — and "**Никаких сабвуферов**". Val: "**Нету**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **No electromechanical counters.** Asked twice — by Pavel early ("**Нужно ли нам какие[-]то электромеханические счётчики в этом кабинете?**") and by Genadi directly to Val ("**Аккаунтеры нам нужны в машине электромеханикал**") — Val answered "**Нет. Нет**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **The existing all-in-one board does not carry over.** Pavel: "**тот вот борт, который делали такой комплексный, который объединяет в себе всё сразу. Он нам не подходит.**" Genadi went further — "**даже если он каким[-]то чуть[-]чуть подходит, мы же делаем новый кабинет. [Для] меня это чистый лист, если мы хотим сделать дёшево**" — a clean sheet, and the machine must be "**дешево[,] удобно и минималистически**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## What stays, mandatory

**A cell modem and WiFi, both.** Val, unprompted and flat: "**Нам нужно обязательно… нам обязательно нужно сел модом. Нам обязательно нужно вай фай**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. This is consistent with the fleet-wide position on [[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]] but was stated here on its own terms, for this cabinet.

## Why any of this matters — the price argument

Genadi's case for cutting was arithmetic, not taste:

> "**Стрит машина дешевая. [I/O] bort не может быть[,] с таким количеством памятью, которое он стоит там 60[-]$70. Когда он хочет машину за тысячу?**"
> "**Мы не можем иметь $60 [I/O] и машину за тысячу… никаких пропорций нет.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**On what a board costs today, the source contradicts itself inside three lines and is recorded that way.** Genadi said "**сегодня мы платим $600 за борт**" and then immediately corrected himself: "**Платили в прошлом году … в прошлом году. Сейчас наверно уже я даже не знаю сколько**" — that was last year's price; today he does not know. The derived notes carry only the first half ("they pay around $600 a board today"); the transcript's self-correction is the fuller record [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]] [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Val accepted the proportions — "**Я согласен**", twice — but entered one counter-point: memory will come back down. "**память вернётся к … прошлой цене обратно … через 2 года**", restated as "**через 2 года[,] 3 года**". He did not use it to overturn any cut [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

The **$1,000 build target** this is all measured against was set on [[wiki/decisions/2026-09-14-street-cabinet-main-screen-runs-on-lvds-not-a-controller.md|Sept 14]] and Val restated it here: asked "**вы хотите тысячу долларов в машину**", he answered "**Да да… Я хочу тысячу долларов машин[у], да**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## The board this all sits on — not re-settled here

The compute board was named twice and **not** re-decided. Val: the machine "**сможет работать на [rk 38 76]**" — the transcript string is "**рк 38 76**", which the derived notes render **RK3576**. Pavel later spoke of it as still open between two parts: "**если мы идём р к 35, 68 или р к там 35 76**" — if we go RK3568 or RK3576 — and once said **RK 35 76** on its own. The [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md|Sept 14 ruling]] (RK3576 with 8 GB, because the RK3568 renders badly vertical) **stands and is not contradicted by anything said here**; what this call shows is that the engineers were still speaking of both parts two days later. Recorded, not reconciled [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]] [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## About the board being replaced

Facts stated about the *current* I/O board, for the record: it is **four-layer** (Pavel: "**судя по всему, четырехслойная**"; Genadi confirmed "**Она четырехслойная**"); **Genadi laid it out himself** — "**как коннектора расставили? Это я делал[,] как компоненты[,] какие — это тоже я**"; and its processor is old — "**там уже процессор уже такой древний**", "**даже уже не 7 поколение**", "**15 лет ему**" (Pavel guessed "**6[-е?] 4[-е] поколение что ли?**" — the generation is not established). Genadi's conclusion: "**те умрут в любом случае[;] надо делать [I/O board]**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## Open commitments

- [ ] Genadi Peari — design the new I/O board to this specification (USB hub, 2 SAS, printer port, bill-acceptor port with ID003 + ccTalk, lighting support, front-mounted connections), plus the separate button/counter board — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Pavel Frolov — extend the development environment and build a new SDK for the new board. Val's instruction: "**Павел, вам нужно расширить [development environment]**"; Pavel's read-back: "**нам надо под новую плату делать свой SDK… который именно заточен под новую плату**" — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

## Open questions

- Where the I/O board and the motherboard physically sit relative to each other — left unresolved on this call. See [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]]. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- What the actual lighting scheme is — Pavel asked "**какие подсветки нам нужны? … классические, вот эти вот фонари сверху[?] … по периметру надо огни[?]**" and got no list back. The board must "support" lighting that has not been specified. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- What a board costs today — Genadi's $600 was corrected to last year's figure and no current price was given. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**§15.8:** clear — board, component and build-cost economics only; no named-person compensation. One comparative remark by Pavel about a named colleague's board work was **excluded** under §15.8; the non-evaluative fact it sat beside (that Genadi laid out the current board himself) is recorded above.

## Sources

- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
