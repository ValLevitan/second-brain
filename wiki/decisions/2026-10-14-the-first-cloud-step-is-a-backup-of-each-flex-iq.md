---
type: decision
title: The first cloud step is a backup of each Flex IQ to the cloud (about two days kept), because today a location's whole transaction history lives only in its unit — the full dashboard is likely MVP 3
date: 2026-10-14
aliases: [cloud backup of each unit, два дня бэкап на каждый юнит, per-unit backup, Flex IQ burns and the location is zeroed, transactions live only in the IQ, piece of mind backup, first cloud step, primitive dashboard, dashboard MVP 3, fifty units in three months]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# The first cloud step is a backup of each Flex IQ

Agreed at the [[wiki/meetings/2026-10-14-transactional-mvp1-launch-plan-brackets-daily-caps-and-mvp2-scope.md|Oct-14 3:49 PM launch-plan meeting]] (Russian): proposed by [[wiki/people/val-levitan.md|Val]], accepted by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## The worry

Klimovich: even from ten locations, all transactions "хранятся только внутри IQ. Не дай бог, он сгорает. У нас вся локация обнуляется." JVL can put in a new unit within an hour, but "Это все, что было до этого, оно исчезло." Moving it all to the cloud is painstaking work; "У нас уже все практически готово", then "Все готово, хотя я сомневаюсь в этом" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## The answer

- Val: a cloud does not work until every piece is ready — "Это nature of a cloud". So, instead: "Два дня бэкап на каждый юнит, который у нас есть", for some peace of mind. "Вас бы устроил такой подход?" [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- Klimovich: "У меня есть решение" — make a backup with some logic and frequency, and fetch it the same way [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].
- Val: there will be about fifty units in three months, "так что там это не страшно"; it lets JVL say some cloud is working, and reports and more can be joined to it later. Klimovich: "Хорошо." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- The derived notes: "First cloud step: per-unit backup to the cloud. (Val Levitan; Andrei agreed)" [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

## The dashboard

Klimovich: the dashboard is "очень примитивный" — a list of connected ports with a live-or-not status. A real one that uses what SAS 2 can give "пока нет. Это, наверное, ИВП-3" (read as MVP 3) [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]].

## Where it sits

- MVP 1 was kept local on Sept 14 and anything cloud-dependent left it on Sept 16 — [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]] (Oct-14 update), [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]].
- Which MVP the backup belongs to was not said. *(Inference: it was raised under the MVP 2 talk.)*

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
