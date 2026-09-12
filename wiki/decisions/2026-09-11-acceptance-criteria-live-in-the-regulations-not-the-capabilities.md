---
type: decision
title: Capabilities carry no acceptance criteria — the criteria and requirements live in the regulations, which is why duplicate per-product capabilities can be merged and tagged by Component
date: 2026-09-11
aliases: [acceptance criteria only live in the regulations, a capability is just a general description, three identical Wi-Fi capabilities, one capability per product is wrong, tag by Component not by title prefix, the regulations stay and go on living, gateway capabilities stay separate, e-wallet operations initiative]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Acceptance criteria live in the regulations, not in the capabilities

Settled by [[wiki/people/irina-shishko.md|Irina Shishko]] at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]], in answer to a structural objection from [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] that had blocked a clean-up nobody disagreed with.

## What triggered it

[[wiki/people/andrey-bosik.md|Andrey Bosik]] volunteered that he has the same capability three times over, once per product: "у меня 3 одинаковых [кейпа]билити по вайфаю есть под каждый продукт" — and noted with some feeling that he had proposed the single-capability form originally and been talked out of it: "я сразу так предлагал… ты[,] дима[,] и мой дима[,] вы меня переубедили, тогда сказали[:] давай под каждый писать свою" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Chudinov's objection

He argued the merged form breaks down over time. Take "add a Wi-Fi modem", needed today in two products (Flex IQ and Pay) for scheduling reasons; if a third product needs the same modem a year later, "мы подымаем эту же старую к[а]п[а]билити или создаём новую[?] Мы будем в архивах копаться" — do you reopen the old capability or create a new one, and go digging through archives? And: "почему в одном случае одна, а в другом случае новая[?]" His real worry was stated next: "получается[,] мы… акцепт[анс] критери[и] на разные продукты в одном cap[a]билити" — acceptance criteria for different products piled into a single capability [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The ruling that dissolved it

> **Irina:** "[С]топ[,] стоп[:] акцепт[анс] критери[и] только в [регламента]х живут[;] cap[abi]l[i]t[y] это просто общее описание. Основное[ —] там требование[,] критерий и так далее[ —] они в [регламентах], которые никуда не деваются, остаются жить."
> **[[wiki/people/andrei-klimovich.md|Klimovich]], the same moment:** "[У ка]п[аб]или[ти] нету [ак]септ[анс] критерия." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

Chudinov accepted it immediately, and said plainly that he had not known: "а я не… знал о[б]… последних обновлениях, извините" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Why this matters beyond Wi-Fi.** If a capability carries no acceptance criteria, there is nothing product-specific inside it to protect, and the per-product duplication has no justification. It also explains the same morning's ruling that capability 163 (one carrier per wallet) becomes a **regulation** rather than a standalone capability — see [[wiki/decisions/2026-09-11-one-card-at-a-thousand-dollars-and-the-rest-stays-on-the-ticket.md]]. It sits directly on top of the workflow chain re-affirmed the day before on [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]] — capability → requirements (in the regulation) → features, acceptance criteria on the requirement.

## The mechanism: Component, not a title prefix

[[wiki/people/pavel.md|Pavel Frolov]] pointed back at the agreement already made: "мы же договорились[,] там дима Ковальчук… предлагал создать… [к]омпонент в проекте capo[bi]lit[ies][,] и мы просто промаркируем вот то, что везде сейчас прописано flexpay[,] да[,] префе[к]с[ —] мы добавим туда, что это флекспей" — tag it FlexPay in the Component field instead of prefixing the title [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. That is the mechanism decided on [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]], now being applied.

## The one place duplication was deliberately kept

The gateway capabilities went the other way. Pavel found "гетвей [и]волет креэйшн" and "гетвей [и]волет инфо[ ]дисплей" too fragmented — "как[-]то кажется, что это слишком раздроблено" — and proposed folding them into a single "[И]волет [о]перейшн" capability [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

Klimovich explained why they exist: he could not find historical capabilities covering the functionality, so he wrote new ones on a unified model — "появляется такой объект как гейтвей[;] гейтвей может быть киоск гейтвей[,] может быть IQ киоск… и есть общий [капабилити], который говорит, что каждый гейтвей должен уметь создавать [и]вол[ет,] читать [и]вол[ет] и так далее" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**They settled on keeping them separate**, because the features underneath will be test executions and autotests written with Claude against the regulations, and separate capabilities delineate those cleanly — Pavel: "тесты, которые пишутся с [Клодом] по тем [регламентам], которые ты там привязал… [т]огда можно даже… не объединять их[;] так будет… проще по разграничению… разных тестов" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. See [[wiki/topics/test-automation-strategy.md]].

## The initiative, and Val's objection to the bucket name

Pavel created an **initiative** for the e-wallet-operation capabilities so they need not be duplicated across FlexPort — "иначе нам бы пришлось во многих местах дублировать… для флекспорта… а у нас иерархия не давала бы этого сделать" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

Val pushed back on the name: "только мне не нравится флекспорт[,] как [нейм;] если вы уже берёте это… наверное[,] что[-]то надо переименовать", because "это всё очень брод[ер]" — FlexPort is too narrow a bucket for something that broad. Pavel agreed he can move everything out of Flex into E-wallet Operations, and said the same applies to the FlexPay capability: "я могу… вообще всё, что во флек[с,] перенести в этот [и]волет опер[ей]шн… [и] то же самое flexpay" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — reformat his three identical per-product Wi-Fi capabilities into one: "надо просто переформатировать будет мне[,] так точно[,] моё" — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — move the Flex and FlexPay capabilities into the E-wallet Operations initiative and rename the bucket off "FlexPort", which Val called too narrow — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **Does the "no acceptance criteria in a capability" rule hold when the same capability serves products with genuinely different criteria?** Chudinov's original worry was answered by pointing at the regulations, but nobody worked through a concrete two-product example in the room — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The derived notes summarise this as "Bosik has three identical WiFi capabilities, one per product, and agreed to reformat them into one" and "capabilities carry no acceptance criteria; the criteria and requirements live in the regulations, which stay" — consistent with the transcript.)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — process and tooling only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
