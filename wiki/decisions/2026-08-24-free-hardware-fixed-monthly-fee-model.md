---
type: decision
title: Give the operator all the transactional hardware free and charge a fixed ~$60–90 per month; hand the per-transaction dollar back to the operator
date: 2026-08-24
aliases: [free hardware monthly fee, $65 per month model, operator keeps the transaction dollar, profit centre not cost centre, Flex subscription model, 42000 machines 7400 locations]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# Free hardware, a fixed monthly fee, and the transaction dollar handed to the operator

At the [[wiki/meetings/2026-08-24-flex-port-mini-capabilities.md|Aug 24 2026 Flex-Port-Mini session]] (Russian), [[wiki/people/val-levitan.md|Val]] set the commercial model that the cheap [[wiki/decisions/2026-08-24-flex-port-mini-via-second-sas-only.md|Flex-Port-Mini]] exists to make possible. His opening constraint when [[wiki/people/genadi-peari.md|Genadi]] asked what the target was — "А цена?" — was one word: "Я хочу их отдавать во фри" (I want to give them away free) [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## What was decided

Val's closing formulation: "Юзкейс, для оператора мы даём ему всё оборудование за бесплатно. И берём с него какой то фикс масла и… Между 60 и… $90 в месяц. И даём оператору возможность… Получать деньги с инкома… Доллар за транзакцию. Вот такая бизнесмодель." — give the operator all the equipment free, charge a fixed monthly fee between $60 and $90, and let the operator collect the money from InComm, the dollar per transaction [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

- **Everything free: Flex IQ plus a Flex-Port-Mini on every machine with a second SAS port.** Val's pitch script: "Вот тебе я. Флекс IQ. Вот тебе бесплат. Флэгспорт meni. Который подключается ко 2 сассу… Всё, что ты делаешь, добавляешь вот эту панель. Тебе не нужен, как его муда груз. Тебе не нужно все твои титул? Ты можешь выкинуть всё это?" — you add this panel, you don't need Mutha Goose, you don't need your TITO, you can throw all of it out [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **The reference monthly figure Val used throughout is $65.** "Плати нам $65 в месяц. И вся система тебя бесплатна" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **JVL gives up the per-transaction dollar it takes today.** Val: "Ты получаешь процесс мфи, вот этот доллар, который Мы зарабатываем, мы теперь его отдаём… И все деньги твои, ты сам зарабатывай деньги. Всё тебе за бесплатно" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **Two months up front plus a security deposit.** Asked by Genadi why not charge $200 for the Flex IQ, Val said he would rather take "1 2 месяца сразу $130 секьюри депозит, то есть ещё $65 или там $100. Который возвращается потом" — one or two months up front, $130, plus a further $65 or $100 as a refundable security deposit [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## Market maths quoted in the session

- **Market shape:** "42000 машин на лакешне 7400 лакешнов. 5,9 машин на локешине в среднем. Значит 6 таких портов" — ~42,000 machines across ~7,400 locations, averaging 5.9 machines per location, so about 6 ports per location [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **Payback, first pass:** at a $20 port cost, 6 ports = $120, plus $200 for Flex IQ = **$320 per location**; at $65/month that is **5 months** to recover the hardware — "за 5 месяцев мы отбиваем" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **Payback, second pass:** with the ports at $30 each, Val recomputed "180 200 $380" = **$380 per location**, recovered in **6 месяцев** — six months, which he called normal [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **Revenue at scale:** "если я могу взять 7000 лакейшинов по $65, это $42000 в месяц. Это $420000 в месяц," corrected moments later to "**455000 в месяц**" — roughly **$455K/month** across ~7,000 locations at $65 [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **The operator's break-even.** Pavel: "если у тебя в месяц больше 65 кэшаутов, то ты уже вот отбиваешься" — above 65 cash-outs a month the operator is already ahead on the transaction dollar alone. Val: "Ты отбиваешься и получаешь всё за бесплатно, тебе ничего не стоит… Ты же за 30 дней даёшь как минимум 2 тикета выпускаешь" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## Rationale — reframe the fee as the operator's profit centre

- Genadi assumed the reason for a monthly fee was that per-transaction billing is impractical ("невозможно чарчивать эти транзакции по доллару"); Val corrected him: "Нет, потому что я не хочу с этим ******* — Потому что я хочу ему сказать, что на тебе это твой профитцентр. То, что ты думаешь ты мне платишь ты мне ничего не платишь, это твой профицентр." The point is to be able to tell the operator that what looks like a payment is in fact their own profit centre [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- Val's design constraint on cost follows directly from the model: "мне нужно цену довести до нуля. Ну, образно говоря. Чтоб я мог отдавать этому" — drive the price to (figuratively) zero so it can be given away — plus "довести флекса айкью до состояния, где это можно for free" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- Genadi expected free hardware to multiply uptake: "Было бы гораздо больше, если бы все бесплатно всё это забирать… Наверно было бы в 5 раз больше" — perhaps five times more [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

This is consistent with the ~$65–$100/month recurring-revenue figure Val reported pitching to Georgia operators three days earlier ("nobody even flinched") — see [[wiki/projects/georgia-market-rollout.md]] (Aug 21).

## Stage 2 — considered, not decided

- **Drop Flex IQ entirely and issue vouchers from any mobile device running a cashier app.** Val: "2 этапом мы уходим от флекс IQ. И даём им пользоваться любым… Мобильным девайсом, с какимто приложением?" and even wondered aloud whether it should come first ("А может быть, это даже стоит сделать в первую?"). Pavel liked it — "в плане железа упрощается" — but flagged the cost trap: "понадобится ставить модем в каждый… сми борт… чтоб каждый сми п независимо… На сервер передавал данные," which Val agreed would put the cost back where it started: "Ну тогда это получится то же самое. По цене." Left as a possible stage 2 [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## Open commitments

- [ ] Val Levitan — write up the player use-case and the operator / master-operator business case in plain writing against the ~$45 (Mini) / ~$250 (Flex-Port) budget assumptions, then have Claude produce the capabilities document, and reconvene — due unspecified — [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]

## Open questions

- The fee is a range ($60–90) with $65 as the working reference; the final figure is not fixed — [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- What kind of specialist is needed to build the stage-2 mobile cashier app? Val: "Я не знаю, что для этого требуется какого сорта специалист для этого тоже" — [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
