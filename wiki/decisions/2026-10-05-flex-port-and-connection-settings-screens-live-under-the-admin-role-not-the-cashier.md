---
type: decision
title: The Flex-Port and connection screens of capability 141 have no mock-ups, so Chudinov designs them himself — and they live under the admin role, not the cashier, with the Recycler's port display as the model
date: 2026-10-05
aliases: [capability 141 screens, port screens under admin, под ролью админа, не у кассира, Recycler port display as reference, как это сейчас сделано в ресайклере, no mock-ups for setup screens, setup mode screens, machine to Flex IQ transaction screen, Flex-Port status screen]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# Port and connection screens go under the admin role

Settled at the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 MVP 1 call]] (Russian, 8:01 AM) by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], on a point raised by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The problem

Chudinov is on capability 141. It covers seeing which Flex-Ports are connected and their state, and the money moving between a machine and the terminal: "посмотреть, какие фликспорты подключены, их состояние" and "денежные транзакции от машины на терминал и в другие стороны". There are no mock-ups for the set-up screens: "для мастер варианта для сетапа нет никаких макапов… Эти экраны делаются на данный момент на наше усмотрение" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

- **The port screen** already exists and is being refined. It shows which machine is on which port, its status and the IP addresses [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].
- **The transaction screen** (money from the machine to the IQ and back) he builds that day: "Этот экран я буду делать сегодня". He expects to show it and maybe rework it [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## The ruling

Klimovich: "это не должно вас останавливать. И да, мы макапы не делали единственное пожелание, пускай оно живёт под ролью админа да не у кассира." For a model: "за референс можете взять, как это сейчас сделано в ресайкле" — the port display on the Recycler. Chudinov: "Он там делал Владимир, это там, скорее всего будет это по аналогии" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]. ("Владимир" = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], by context — inference.)

In one line: **the port and connection screens are built without mock-ups, sit under the admin role (the cashier does not see them), and follow the Recycler's port display.** The derived notes record the same ruling [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## Where it sits

- Because the cashier does not see these screens, the cashier had no place to see unclaimed money. That gap is closed in cashier Records — see [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] (Oct-5 update).
- The Recycler is out of both MVPs ([[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]]); here it is only the visual model.

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — build the machine-to-Flex IQ money transaction screen in set-up mode (admin role) — due Oct 5 2026 ("сегодня") — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

**§15.8:** clear. **§15 #9:** none; 141 is a capability number.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
