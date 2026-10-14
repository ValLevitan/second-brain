---
type: decision
title: MVP 1 has no print queue — when the printer is busy, a Flex-Port ticket is created electronically and the cashier prints or reprints it from Records; Val asked Klimovich to pick one option and move the rest to MVP 2 or 3; self-service FlexPay printing is not MVP 1
date: 2026-10-05
aliases: [no print queue, без очереди, print queue MVP2, ticket still in the printer, тикет вставлен в принтере, get ticket from Flex-Port, print from Records, перепечатать из рекордс, pick one option, выберите один вариант, MVP 2 or 3, self-service printing not MVP1]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# MVP 1 has no print queue; tickets print from Records

Settled at the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 MVP 1 call]] (Russian, 8:01 AM). [[wiki/people/val-levitan.md|Val]] asked [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] to choose; Klimovich chose [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The question

[[wiki/people/alexei-khamin.md|Alexei Khamin]] found the case in autotests. A cashier prints a ticket and does not take it out. If the cashier tries to print again, the terminal says it cannot, the printer is busy ("нельзя кредитор занят" — "кредитор" read as the printer, inference) — fine. But if a Flex-Port asks for a ticket ("Get ticket") at that moment, the ticket is created in the system and does not print. Even after the first ticket is taken out, someone must ask the cashier to print the second. Khamin: "не нужно ли может быть лучше сделать там очередь?" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

- **[[wiki/people/dmitri-chudinov.md|Chudinov]]:** a queue gets complex fast — twenty Flex-Ports pressing "create ticket" at once, or a terminal reboot after which it "должен помнить вот этот напечатанный и не напечатанный" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].
- **[[wiki/people/pavel.md|Pavel]]:** with five players in line and five tickets, it is simpler to ask "на какой ты машине был" and print by machine number; "но опятьтаки это надо обсуждать" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The ruling

Val: "выберите один вариант любой вариант, который Андрей климович хочет имплементировать на MBP один… Всё остальное переместите на MVP 2 или 3." Klimovich: "Я вполне окей для MVP один без очереди двигаться. У нас все транзакции сохраняются в в рекорд из под рекордс их можно перепечатать или напечатать впервые." Chudinov: "Так и сделано." [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

Khamin then asked about FlexPay, where there is no cashier. Klimovich: on self-service kiosks nothing should print automatically. Val: "Это не MVP один" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

In one line: **no print queue in MVP 1; every transaction is in Records and the cashier prints or reprints it there; a queue, and FlexPay self-service printing, are later.** The derived notes record the same ruling [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## Where it sits

- It follows the Sept-21 rule that at the Flex-Port the wallet is created and the cashier prints it later ([[wiki/decisions/2026-09-21-at-the-counter-no-printer-no-wallet-at-the-port-the-wallet-goes-to-unclaimed.md]]) and the Sept-15 cashier flow with Records ([[wiki/decisions/2026-09-15-the-flex-iq-cashier-flow-login-redemption-receipts-and-records.md]]) — links are context, not citations.
- Val's "pick one, move the rest to MVP 2 or 3" is the same push as his hold on all other questions the same day — see [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] (Oct-5 update).

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
