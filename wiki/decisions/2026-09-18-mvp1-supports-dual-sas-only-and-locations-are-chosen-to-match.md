---
type: decision
title: MVP 1 supports dual SAS only — the bill-acceptor and counter-emulation environment is deferred, and MVP 1 locations will be picked so every machine is dual-SAS
date: 2026-09-18
aliases: [dual SAS only, only dual SAS in MVP1, MVP один только дуо сас, two environments or one, bill acceptor and counter emulation, эмуляция билакцептора и каунтеров, MudaGoose environment, MG environment, fully equipped with dual SAS machines, supporting both is almost double the testing, почти икс 2 тестирования, automate the tests so environment two is covered faster, capability 151 scope item four]
source-count: 3
status: active
open-commitments: 1
open-questions: 1
---

# MVP 1 runs on dual SAS only, and the MVP 1 locations are chosen so it can

Settled at the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept 18 2026 8:03 AM call]] (Russian). It is a **scope ruling for MVP 1**, taken by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] and supported on testing grounds by [[wiki/people/pavel.md|Pavel Frolov]] — and Klimovich said in the same breath that the underlying **business** question is still open.

## How it came up — out of capability 151

The team was cleaning **capability 151** ("Flex IQ must work in the port environment" — Klimovich: "**общая [капабилити], которая говорит о том, что флекса IQ должен работать в порт[ ]энвайменте**"). Two pieces of its text were struck: the cloud wording, and, on [[wiki/people/dmitri-chudinov.md|Chudinov]]'s instruction, "**убрать в скоб[е] 4 пункт про м г инваймент**" — the fourth scope item about the MG environment [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

Pavel picked the removal straight back up — "**раз мы уже как бы дошли до мут[а]гус[а] энваймента… который мы убираем**" — and asked the scope question it exposes. **The two renderings, Chudinov's "м г инваймент" and Pavel's "мутагуса энваймента", are the same scope item spoken seconds apart**; the corpus's canonical name for it is **MudaGoose**, the legacy payment mode ([[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]]). *(That identification is a reading from context, not a statement in the source.)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## The question, including the self-correction

Pavel asked it about the wrong device first and corrected himself inside the same turn [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**Оставляем ли мы сейчас… для MVP один[,] что флекс[а] айкью должен уметь работать с 2 типами[.] Точнее[,] нет. Наверное, флегспорт должен работать с 2 [энвайрон]ментами. Один из них подключаемый через сас. А 2[-й,] подключаемый через эмуляцию билакцептора и каунтеров.**"

So the two environments are: **connected over SAS**, and **connected by emulating the bill acceptor and the counters**. *(The derived notes put the question on the Flex-Port only and do not record that Pavel first asked it about Flex IQ.)* [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## The ruling

Klimovich, immediately: "**Я предлагаю для MVP один сфокусироваться только на дуо сас[ ]поддержке**" — and then the operational half that makes it work [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**давайте договоримся[:] [MVP] один — только д[у]о[ ]сас, и мы будем выбирать локации на MVP один те, которые полностью эквип[ированы] д[у]о[-]сас машинами.**"

**Pavel supported it for a reason worth keeping, and it is not a product reason:** "**поддерживать оба — это почти икс 2 тестирования**" — supporting both is close to double the testing [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The price of deferring was named and turned into work:** "**задача тогда обкатать возможность максимально автоматизировать какието тесты, чтобы уже 2[-е] покрыть гораздо быстрее**" — build the test automation during MVP 1 so the second environment can be covered much faster afterwards [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Klimovich flagged the business question as still open, in the same sentence

> "**мы[,] это нерешённый до конца ещё бизнес вопрос[:] у нас одни операторы говорят, что мне достаточно д[у]о сас[,] я все машины[;] другие говорят…**"

The sentence trails off unfinished on the recording [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]. **This ruling therefore settles MVP 1's engineering scope and settles nothing about the market.**

**It does not resolve the standing contradiction over how much of the Georgia fleet lacks a second SAS port**, which now runs to several incompatible estimates across Aug 24 – Sept 16 2026 — see the open contradiction on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and the Sept-7-versus-Sept-9 split on [[wiki/decisions/2026-09-09-jvl-supports-both-dual-sas-and-single-sas-and-not-mudagoose.md]]. **Nothing here is resolved either way.** What this adds is a dated data point of a different kind: whatever the market split turns out to be, the **first release** deliberately does not address the single-SAS half, and JVL will choose its pilot locations to avoid needing to.

## Oct 5 2026 — annotation: a Port task "где 2 сас канала" that nobody can yet approach

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) [[wiki/people/dmitri-chudinov.md|Chudinov]], on the MVP 1 Port tasks parked on Pavel: "там есть не мелкая. Я там одну задачу пропустил, даже не знаю как подходить там, где 2 сас канала." [[wiki/people/pavel.md|Pavel]]: "В [порте] нет смысла 2 [SAS] канала это ктото." Chudinov: "у него понятно один, но машина подключена к 2. У нас есть какието там требования или что мы чтото получаем оттуда я не понял… мне надо хотя бы общее представление." Pavel: a separate session after the stand-up to go through all those tasks, "кто создавал и так далее" [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. Recorded here because it is the first engineering task the wiki sees on the dual-SAS case this ruling scoped MVP 1 to; what the task asks for is not known. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 5, 4:54 AM).

## Open questions

- What does the MVP 1 Port task with "2 сас канала" (the machine connected to two SAS hosts, the port with one) actually require, and who created it? — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Open commitments

- [ ] The MVP 1 team — automate the tests during MVP 1 so the second environment (bill acceptor and counter emulation) can be covered quickly afterwards — due unspecified; proposed by Pavel Frolov as the condition of deferring, and not assigned to a named person on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — protocol scope and test effort only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
