---
type: decision
title: October 1 goes with one configuration — Flex IQ alone, the Flex-Port stays, FlexPay moves to MVP 2; MVP 1 runs on the linked network with one kiosk per location
date: 2026-09-11
aliases: [we finally decide we go with only one configuration, Flex IQ alone for October 1, FlexPay out of MVP 1, machine port IQ then machine port Pay, one kiosk per location either IQ or FlexPay, MVP 1 runs through the linked network, if there is no bottleneck we reconsider MVP 1, transactional MVP1 transactional MVP2 releases, October 2 end date, why ten more days, FlexPay initiative split, the kiosk is FlexPay]
source-count: 3
status: active
open-commitments: 4
open-questions: 3
---

# October 1 goes with Flex IQ alone — FlexPay drops to MVP 2, the Flex-Port stays in

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]], after [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] proposed it and [[wiki/people/irina-shishko.md|Irina Shishko]] asked for it to be said plainly.

## The two releases, as they now exist in the tool

[[wiki/people/pavel.md|Pavel Frolov]] opened by reporting that he had created them: "в спейсе продакт cap[a]bility создал 2 релиза[ —] транзакш[е]н MVP один и транзакш[е]н [M]VP 2[,] назначил им… [окто]ба 1 и [окто]ба 30" — two releases in the product-capability space, dated **October 1** and **October 30**, with capabilities already being linked to MVP 1 and features created underneath [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

*(The October 30 date is what Pavel put on the release object. The meeting's own title still reads "MVP2-Nov 1st", and the [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md|Sept-10 ruling]] said November 1 with a possible pull-forward to October 21 for the Georgia expo. Recorded as three renderings of the same second milestone; nobody in the room reconciled them.)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

Irina had the release renamed so "Transactional" comes first — "может мы сделаем вот это MVP один транзакшн[а]л… [п]оменяем местами" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The sorting criterion, corrected on the spot

Klimovich checked how Pavel had been assigning capabilities — by whether Pavel had read and understood them. Irina cut that off: "мвп один это то, что мы должны к 1 октября сделать, а не потому, что его понял или не понял Паша" — MVP 1 is what must be done by October 1, not what anyone did or did not understand [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. Pavel clarified that his uncertainty was only about the fragmented gateway capabilities: "то, что я не понял[,] это… что у нас г[е]т[в]е[й] раздроблено[на] разные [кейпа]билити… если мы сейчас принимаем решение, что они у нас остаются, я просто [пош]у их на MVP один" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## What MVP 1 is

- **It runs on the linked network, and a location gets one kiosk only.** Pavel: "MVP один работает через линкед[ ]этот самый нетворк… [и] на лакейш[н]е может стоять один киоск, либо IQ, либо flexpay[,] всё, а всё остальное идёт в M[V]P 2" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. This restates [[wiki/decisions/2026-09-09-one-transactional-unit-per-location-until-the-wi-fi-iteration.md]] two days later, unchanged.
- **Klimovich's focus argument:** polish one product rather than half-finish two — "из g[a]t[e]way[,] я бы фокусировался в первую очередь на IQ, то есть все [UI], всё полностью отполированную флоу. В первую очередь IQ. Если мы успеваем сделать ещё pay[,] … [Pay] может пойти на MVP 2" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **Irina's ordering, given before Val's ruling:** priority one is "машина[,] порт[,] айкью", priority two "машина[,] порт[,] [пэй]", both "до 1 октября", which Klimovich agreed to ("да[,] да") [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. **Val's later ruling narrows this** — see below.

## The ruling

Klimovich asked whether to pull FlexPay out of MVP 1 altogether — "и может быть вообще весь пока flex pay убрать[,] не знаю[;] что думаете[?]" Pavel answered that FlexPay is other people's work running in parallel ("flex pay делает другой человек… со стороны киоска[ —] саша биратка, а со стороны сервера… Сергей [Цы]манов"), which Val then separated out as a different question entirely [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]:

> **Val:** "[Н]ет, подождите[,] здесь мы запутали[сь в] 2 темах. Андрей говорит[:] давайте уберём с этой M[VP] один[,] значит перевести надо [в] M[V]P 2[ —] это правильное предложение. Павел говорит о том, что 2 работы делаются параллельно, но это отражается только на [скеджул]… Андрей прав абсолютно[:] зачем нам [это] оттуда[,] [из MVP] один[?]"

Irina then put it as a statement of record and Val confirmed it:

> **Irina:** "[Т]о есть к 1 октября, получается, мы окончательно решаем, что мы идём только с одной конфигурацией. С флекс[ ]а[й]кю."
> **Val:** "Мы окончательно это решаем, потому что мы хотим… [бо]тлнек, который вы нам говорите[,] у вас есть[;] если этого [ботлнека] нету, тогда мы пересмотрим M[V]P один. Но если этот [ботлнек] действительно существует, тогда да, мы соглашаемся с этим."

**Two things follow from Val's wording, and both matter:**
1. The narrowing is **conditional on the bottleneck the engineers reported**. If the bottleneck does not exist, MVP 1 gets reopened. The bottleneck in question is the Flex-Port readiness slip recorded on [[wiki/decisions/2026-09-09-flex-port-readiness-slips-to-september-25-and-stays-the-bottleneck.md]].
2. **The Flex-Port is not affected.** Klimovich checked immediately — "порт[,] порт же должен остаться" — and Pavel confirmed "стоп[,] стоп[,] да[,] всё верно" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## What this changes on the earlier decision

[[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]] recorded the October-1 target as **FlexPay** in self-service with bill acceptor, card dispenser and TITO printer. Two days later the same October-1 date now carries **Flex IQ** instead. The **date survives**; the **configuration does not**. Treated as **evolution, not contradiction** (§11): a later source updating an earlier state of affairs, with the earlier configuration moved to that page's history and its title annotated. FlexPay development itself is not stopped — it continues in parallel on Biratka and Tsymanov, it is simply not what ships on October 1.

## Who does what

- **[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] works Flex IQ first.** Pavel: "всё, что бы сейчас в первую очередь делать[,] дима[,] он будет делать [во] флекс айкью" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **[[wiki/people/alexander-biratka.md|Alexander Biratka]] takes the Flex-Port tasks and ports Chudinov's finished work across into FlexPay.** "все задачи, которые идут по флекс порту, это будет брать саша [Би]ратка[,] и он по факту по сделанны[м] работа[м] диминым… будет это переносить во флекспей" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **[[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] covers the FlexPay server side** — "со стороны сервера [до]бавляет поддержку Сергей [Цы]манов" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **Klimovich's own order is the IQ UX first, kiosks after** — "для меня приоритет… в первую очередь IQ отгрузить вам[,] потом уже заняться киосками" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Where the requirements stand

Klimovich still owes five capabilities and their requirements, then the UI/UX screen descriptions with the texts; the operations-dashboard update is last and can ship as-is — "[д]аже если мы будем релизиться с текущим [дашбордом,] нас это вполне устроит[;] мы можем его потом до[]выпускать". He was spending the whole day on it and expected to need about half of Monday, after which "будет весь пакет полностью всех требований… все экраны, все тексты" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. The capability count was put at "около 30" by [[wiki/people/andrey-bosik.md|Andrey Bosik]] [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**A follow-up call was set for Monday at 8:00 AM Eastern** to re-review the MVP 1 scope — "можем делать в понедельник снова звонок сделать на те же 08:00" — with Klimovich reserving the right to bring back capabilities that did not make MVP 1 rather than adding them alone: "[с]ам я их добавлять не буду… я бы хотел, чтоб мы так коллегиально делали". Val's answer: "это право у вас остается ежедневно" — the right to add stays open every day [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Update, Sept 22 2026 — the plan ends on October 2, Val wants other dates, and FlexPay gets its own initiative

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM call]], Pavel showed the MVP 1 schedule: "все, что [MVP] один сейчас… до 2 октября грубо стоит". The view mixed in MVP 2 items, so [[wiki/people/irina-shishko.md|Irina Shishko]] proposed two initiatives — one for Flex IQ (MVP 1), one for FlexPay (MVP 2). Val: "мне нравится, как [Ира] предлагает"; Pavel created it on the call. Val also ruled on the name: the kiosk is FlexPay, not "kiosk" — "Нам нужно быть [консистентны] к нашим стандартам" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**The date was challenged, not changed.** Val: "сделано большинство", so "почему нужно ещё 10 дней?" Pavel: "Потому что до этого было 2 года." [[wiki/people/dmitri-chudinov.md|Chudinov]]: built functionality still has clarifying requirements to meet, plus "абсолютно новые функционалы типа блокировки [Flex-Port]". Val asked twice for "почестнее". Pavel: "сейчас нет никого, кто хочет задержать сроки, скорее наоборот". Val agreed — "группа очень честная… ни у кого нету заинтересованности растягивать" — and closed: "вопрос оставлю открытым, хотел бы видеть другие сроки" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**Irina's release condition.** She said the team would release on time whether or not end-to-end tests exist, and that this is wrong for this release. Val: the only way to release "2 числа" is if developers help with the tests. See [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

*(The release object Pavel set up on Sept 11 is dated October 1; the Sept-22 schedule ends "roughly" October 2, and Val speaks of releasing "on the 2nd". This reads as the same target seen at day level, not a new date — **inference**.)*

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the remaining five capabilities and their requirements, then the UI/UX screen descriptions with texts; he expects to be done about half-way through Monday — due Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review by Monday which capabilities did not make MVP 1 and bring them to the group rather than adding them himself — due Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — finish linking capabilities to MVP 1 and MVP 2 and creating the features underneath — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — request edit rights for release names in the tool; she has none today ("я хотела сделать, а у меня нет прав"). Val's aside was to hand global renames to Claude instead: "я советую вам это отдать [К]лоду[,] чтоб он глобально это поменял" — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **Does MVP 1 keep its early-October end date?** Val left it open on Sept 22 and asked to see other dates; Pavel and Chudinov defended the plan — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- **Does the bottleneck the engineers report actually exist?** Val made the whole narrowing conditional on it and said MVP 1 would be reopened if it does not — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **Which date is the second milestone — October 21, October 30, or November 1?** The release object says October 30, the meeting title says November 1, the Sept-10 ruling said November 1 with a possible move to October 21. Not reconciled in any source — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — scope, sequencing and work assignment only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
