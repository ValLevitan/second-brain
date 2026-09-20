---
type: decision
title: Fifteen Flex-Ports is the MVP 1 number per location and the system is designed for 99 — what happens above the limit stays open until load testing answers it
date: 2026-09-16
aliases: [requirement 1432, number of FlexPorts, ports per location, design for 99, fifteen for MVP1, nine is a bad number, maximum 9 gaming machines, load testing, subnetworks, на свой страх и риск, дизайн на 99]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# Fifteen Flex-Ports for MVP 1, a system designed for 99

Requirement **1432** — how many Flex-Ports a single location must support — was on [[wiki/people/irina-shishko.md|Irina Shishko]]'s open-question list at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian). The capability it hangs off was not established on the call: Irina asked whether it sat under the same capability as the preceding requirement and got no answer [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The number in the requirement was a placeholder

[[wiki/people/dmitri-chudinov.md|Chudinov]] said plainly where it came from: "это требование мы создавали с Паша[,] надо было заполнить число[,] и брали с запасом… потому что система должна работать… с небольшим запасом" — he and [[wiki/people/pavel.md|Pavel Frolov]] wrote it, a number had to go in the field, and they took one with a margin [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. *(The figure [[wiki/people/andrei-klimovich.md|Klimovich]] read off the screen is rendered "20 лектов" in the transcript and is **not recoverable with confidence**; it is recorded here as a placeholder of unstated value rather than asserted as 20.)* [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

Klimovich's first instinct was that the requirement did not belong in MVP 1 at all, because the market it is written for does not need it: "в джорджии всё просто[:] одна локация, максимум 9 машин игровых" — in Georgia it is simple, one location, a maximum of nine gaming machines — and the headroom is "точно не на джорджию, но на… условный Техас" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. That connects the requirement to [[wiki/projects/texas-used-machine-distribution.md]] rather than to [[wiki/projects/georgia-market-rollout.md]].

## Val's ruling: two numbers, not one

[[wiki/people/val-levitan.md|Val]] rejected the margin as too small — "я думаю, что запас маленький[,] нам нужно дизайн[ить] систему под 100" — and then separated the release number from the design number [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **нужн[о] дизайн[ить] где[-]то на… я бы на 9 не дизайн[ил,] это плохое число. Ну где[-]то на 15 я [бы] дизайне[рил]… Это одно[,] это MVP. Ну в общем[-]то систем[е] нужен дизайн на 99.**
>
> *(You need to design for around… I would not design for 9, that is a bad number. Somewhere around 15 I would design. That is one thing, that is the MVP. But in general the system needs to be designed for 99.)*

Pavel had proposed 10 and then accepted the correction on the spot: "ну давайте поправим на 15" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The limit is per location** — Irina checked it ("это в одном локэйшен, да") and Val confirmed it. Pavel added the engineering qualifier: strictly it is per *network* — "это в одной сети, скажем так, потому что если мы разделяем лакейшн на саб[-]нетворк[и], то там эта проблема снимется" — splitting a location into subnetworks would remove the constraint, except that a location still needs one centralised terminal, so the qualifier does not actually buy an escape [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## What happens above the limit was deliberately left open

Two answers were on the table and neither was chosen. Pavel: "продолжать работать[,] просто… без гарантий" — let the extra ports keep working, without guarantees. Chudinov put the same fork sharply: "что делать, если 99 подключились и подключается 100[:] его отпинывать либо подключать? Но уже на свой страх и риск" — kick the hundredth away, or admit it at your own risk [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Klimovich ruled that the question is not answerable by argument, only by measurement — "только на [на]грузочном тестировании мы это узнаем. Если мы увидим, что и после… 99 и 120 поддерживаются, вот и ответ… Но если мы увидим, что 100 умирает… больше 99 мы не поддерживаем" — and asked that the open item stay in the requirement as a reminder, since its presence does not block anyone now. Irina agreed and noted the one practical cost: the open item will have to be marked up somehow so the AI assistant does not keep tripping over it ("его нужно будет как[-]то обозначить для Клода") [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

This is the one open question the meeting **chose** to leave open rather than clear, which makes it the exception to the whole purpose of the call.

## Open commitments

- [ ] Team — load-test the Flex-Port count per location to establish the real limit, and answer what happens to a port above it (reject, or admit without guarantees) — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open questions

- **What happens above the Flex-Port limit** — reject the extra device, or accept it without guarantees. Deliberately left in requirement 1432 as a reminder; answerable only by load testing — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

**§15.8:** clear — capacity design and market sizing only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
