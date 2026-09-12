---
type: decision
title: Flex-Port keeps its screen — Val rejects Pavel's "patch up the SMIB and do it without a little screen" variant, because demand is expected to be wild and there is no time to redesign
date: 2026-09-04
aliases: [Flex-Port keeps its screen, no-screen SMIB variant rejected, why do we need Flex-Port, demand will be wild, нам нужен экраны]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Flex-Port keeps its screen

A short exchange at the top of the SAS segment of the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept 4 2026 midday call]], reported second-hand and ruled on immediately.

## What was raised

[[wiki/people/genadi-peari.md|Genadi Peari]] brought forward what [[wiki/people/pavel.md|Pavel Frolov]] had said to him earlier that day: that SAS integration into the port was not being worked on at all, and that the port itself might not be needed — "он говорит, а мы же не занимаемся [с]ас интеграции в[о] порт… И он говорит, а вообще зачем нам flexport? Давайте на этом сми[бе] там чутьчуть подправим и будем делать без экранчика. Надо… на эту тему с ним поговорить?" — patch up the SMIB a little and build it without the little screen [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## What was decided

[[wiki/people/val-levitan.md|Val]] cut it off before Genadi finished the sentence: "Нет. Нет, нам нужен экраны, у нас нету времени заниматься этим с [SMIB]" — the screens are needed, and there is no time to go down that road [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. The derived notes record the same ruling: "Flex-Port keeps its screen. The no-screen variant Pavel floated is rejected — no time to redesign, and demand is expected to be high" [[raw/Meeting_Notes_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

His reason is commercial, not technical: "Потому что я рассчитываю, что у нас… если я правильно читаю рынок… [с]прос должен быть бешеный. Потому что мы все отдаем за бесплатно" — if he is reading the market right, demand will be wild, because everything is being given away free [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]. The giveaway he means is the bundle on [[wiki/decisions/2026-09-02-free-ports-and-pos-with-every-machine-bought.md]], itemised the same day on [[wiki/topics/jvl-machine-pricing-strategy.md]] (Sept 4, midday).

## How this sits against the Sept-2 ruling two days earlier

It **narrows** [[wiki/decisions/2026-09-02-flex-port-sas-universal-with-scanner-touch-vs-non-touch.md]] rather than contradicting it. On Sept 2 the family was set to split at **touch vs non-touch**, with Andrei Klimovich's matrix showing that a *simple non-touch screen* would close all the tasks, and a no-screen diode-only variant explicitly judged "откат в прошлое" — a step backwards — by Andrei himself. Pavel's Sept-4 proposal goes further than the Sept-2 floor: not a cheaper screen, but **no screen at all**, on the SMIB board. That is what Val refuses. **Non-touch remains alive; screenless does not** [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

Genadi's follow-on was that the port of SAS onto Flex-Port needs to be talked through with Pavel urgently — "Надо проговорить[ся] с Павлом срочно. Вот эт[у] порт[ацию] сас[а] на flexport" — which is what the rest of the meeting does: [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]] [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Open questions

- Pavel's underlying objection — whether the Flex-Port is the right vehicle at all, versus a lightly modified SMIB — was answered by Val on commercial grounds and **never argued on its merits with Pavel present**. Pavel joined the call later, from his car, and the SAS discussion with him went a different way (the debug-environment proposal on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]); nothing in the source revisits the screen — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]

**§15.8:** clear — product direction only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
