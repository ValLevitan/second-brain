---
type: decision
title: Flex-IQ cannibalises MudaGoose — Val reverses his own "they will run in parallel" position, on business grounds, and says plainly that he misled the team
date: 2026-09-07
aliases: [cannibalise MudaGoose, no parallel operation, one topology IQ plus ports, we are obliged to cannibalise, I misled you, contract-level resistance, lay our own cable]
source-count: 2
status: active
open-commitments: 0
open-questions: 2
---

# Flex-IQ cannibalises MudaGoose — no parallel operation

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] in the first fifteen minutes of the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian), interrupting [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]'s walk-through of the show topology. It is the ruling the rest of the meeting is built on.

## The position being reversed

Minutes earlier on the same call, Val had described Flex-IQ and MudaGoose coexisting as the expected case: "Притом они… могут существовать, на скорее всего, будут существовать на одном и том же лакешине параллельно… Могут быть такие случаи, где они будут заменять друг друга, но, скорее всего, мы видим, что они параллельно работают" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## What was decided

- **JVL is obliged to cannibalise MudaGoose, for business reasons and not technical ones.** "По бизнес[-]причинам[,] другим причинам[,] не технологическим причинам мы должны… [cannibalise] [Муда]гус… То есть если мы заходим на лак[ейшн], устанавливаем своё оборудование, мы должны[,] мы обязаны [cannibalise] [Муда]гус. Поэтому решение, что они будут параллельно работать[,] это… неправильное решение" — and he dated the change: "Это мы пришли к этой реализации только чт[о,] вот совсем… Недавно" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **He said outright that he had misled the team.** "Схема топографии, где у нас параллельно остаётся жить [Муда]гус[,] невозможно… Я ошибочно ввёл вас в заблуждение, когда я думал, что… эта схема может жить параллельно… Это не технологическая вещь, это… бизнес[-]вещь" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. The derived notes record the same reversal, including that he "had misled the team on this" [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **There will be no combined installations at all.** Chudinov asked it as a yes/no — "у нас вообще будут установки flex [IQ и Муда]гус[?]" — Val: "Нет, не будет" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **Andrei set the frame that follows from it: one topology by the show.** "Вот мы сейчас обсуждаем условный октябрь 21[,] и к октябрю 21 мы уверены в том, что нам нужен только один тип с[е]тапа. Одна топология[ —] это IQ плюс порты. Никакого [Муда]гус[а]" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **If a location keeps MudaGoose, it keeps it as a separate system and JVL resists — probably at contract level.** Andrei: "если локация захочет оставить [Муда]гус у себя на локации, она его оставит как отдельное решение, но мы будем против этого." Pressed by [[wiki/people/irina-shishko.md|Irina Shishko]] — "Что значит[,] мы против[,] они захотят оставить[?]" — he answered: "Ну мы попробуем это на уровне контракта[:] если вы хотите с нами работать, то там никаких альтернативных ред[е]м flow не должно быть и отчётности," while adding he was not sure they should go that far: "я не уверен, что нам стоит туда лезть в эти дебри. Сейчас" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## The physical consequence Val named

Displacing the incumbent means displacing its wiring. "Это значит, что мы должны… класть свои провода… Или… устанавливать свою… систему… беспроводного… какой-то сети… [и] с машины мы в принципе выпихнем ихние [провода]… То есть наша задача [cannibalise] эту систему" *(the transcript garbles the word for the incumbent's wiring as "флэнджланг")* [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. That is the same in-premises link the [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md|9:08 Wi-Fi ruling]] settled an hour later, and the same exclusivity condition already ruled commercially on [[wiki/decisions/2026-08-31-transactional-equipment-only-with-location-exclusivity.md]].

## How this sits against the rest of the corpus

- It **hardens** the exclusivity condition of [[wiki/decisions/2026-08-31-transactional-equipment-only-with-location-exclusivity.md]] from a commercial term into a product constraint: there is now no build that can sit alongside MudaGoose, so the question no longer arises per-deal.
- It **closes** the direction Klimovich had floated on Sept 2 — that Flex-IQ might remain "решением только для мут[а гус]" (a MudaGoose-only product) — recorded on [[wiki/decisions/2026-09-02-priorities-iq-ports-flex-pay-recycler-texas-on-wallets.md]].
- It is the reason the "Lego bricks" upgrade path Andrei sold to a customer on Sept 1 — start simple "so it works with [MudaGoose]," add ports later — no longer describes JVL's own plan; see [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 1).

## Open questions

- **Whether to install on MudaGoose locations for a couple of months during the pilot, while the new version is finished.** Andrei asked it directly — "в рамках пилотного запуска… мы их тоже отменим или всё-таки туда мы установимся? Пока будет готова эта версия, почему бы нам не зайти на [Муда]гус хотя бы там пару месяцев посмотреть, как это всё работает?" — and Val did not rule: "Не знаю, не знаю, насколько сложно это всё. Мне кажется, что это мы только [создадим] какую-то путаницу." **Unresolved here, and raised again two hours later** at the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02 session]], where Val said "не думаю" and asked for a day or two; the live commitment is held once on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **How far JVL actually pushes contract-level resistance.** Andrei proposed it and immediately hedged; Irina's objection — that a location can simply choose to keep its incumbent — was never answered — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

**§15.8:** clear — product and commercial strategy only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
