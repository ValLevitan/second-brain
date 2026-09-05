---
type: decision
title: Freeze the existing hand-written test cases in their current warehouse; Claude-written tests go into a new one
date: 2026-09-01
aliases: [freeze the old test cases, two test warehouses, do not migrate manual test cases, old tests will die, new warehouse for AI tests]
source-count: 2
status: active
open-commitments: 0
open-questions: 2
---

# Freeze the existing hand-written test cases; new AI-written tests go into a new warehouse

Val's recommendation at the [[wiki/meetings/2026-09-01-nova-prose-qa-automation-check.md|Sept 1 2026 check-back]], after [[wiki/people/alexander-biratka.md|Alexander Biratko]] and [[wiki/people/irina-shishko.md|Irina Shishko]] argued for reusing parts of the existing manual test set. This is the QA-side companion to the [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md|Aug-28 QA-automation experiment]] [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].

## What was decided

- **Val's recommendation: do not touch the existing hand-written tests — freeze them where they are.** "тесты, которые у нас вот сейчас есть, написано руками, с которым мы живём сейчас. Я бы их не трогал бы, я их как бы заморозил бы. И положил бы… в этот werlaws" [warehouse] [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **New tests, written by Claude off the requirements' acceptance criteria, go into a new warehouse.** "а новые тесты, которые пишет клод на базе… вот этих вот эксептонс критериев, которые в рекументе я положил бы их в новый wargause" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **Then measure how often anyone actually goes back to the old set.** "Добавлял бы в этом новом wer house вот эти тесты и смотрел сколько… раз я буду обращаться к старым тестам? У меня такое ощущение, что в очи в очень короткое время" — his instinct being, very soon, never. Irina agreed on that point: "Уже никто туда не пойдёт" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **If coverage turns out to be missing, ask the AI for more tests rather than reaching backwards.** "если я понимаю, что мне не хватает какихто тестов, которые написал ai, я бы лучше обратился б ещё раз… сказал бы мне не хватает этих тестов. Давай допишем, чем возвращался бык старом. Потому что я не вижу связки между старым и то, что новое начинается" — he sees no linkage between the old set and what is starting now [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].

## Val's premise, and the objection to it

- **Val's premise: today's manual tests will die.** "Я не совсем положительно отношусь к… каст кейсом, которого нас написано сегодня. И я не думаю, что они будут сильно [applicable] в будущем"; asked by Irina whether he meant the automated tests written for the NOVA platform, he widened it — "Любые тесты, которые сегодня существуют у нас, которые руками были написаны… Мне кажется, что они… умрут" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **Alexander's counter, twice put.** First: just point Claude at the existing test cases and have it add what is missing — "можно как бы потом просто опять же тому же клоду сказать, пройдись по тест кейсам и добавь Того, что не хватает." Then, sharper: some tests are specific to particular bugs, particular locations, or rare settings cases and "некоторые могут быть прям прям важными" — some may be genuinely important [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **His concrete alternative — a one-time overlap analysis.** "мы можем сгенерировать новые тесты… на основе там прозы… Потом сделать просто один раз анализ… вот у нас есть старые тесты. Вот у нас эти и сравнить, посмотреть пересечение… и уточнить, а действительно ли эти тесты, вот которые не пересекаются, они нам нужны и выбросить? То есть это работа на один раз." He framed his motive not as coverage anxiety but as not losing important cases: "Стоит посмотреть на старые тесты, чтобы не потерять какието важные случаи" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].
- **Val heard it and did not adopt it**, saying they were nearly saying the same thing ("мы практически одно и тоже говорим") but restating his preference, and then closing the topic as hypothetical: "я думаю, что сейчас это просто трата времени. Этот разговор это гипотезы, разные о жизни подскажут, как правильно делать" — practice will settle it. His own softening: "Ну пока и хорошо" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]].

## The gap this leaves, acknowledged on the call

[[wiki/people/pavel.md|Pavel]] flagged that in the first phase the written capabilities and requirements-with-acceptance-criteria "не будут покрывать всё то, что на данный момент к ве держат в своей голове или там в своих тесткейсах" — will not cover everything QA holds in their heads or in their existing test cases. Val: "Конечно, но меня это не пугает" [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]. Pavel's working method for closing the gap is on [[wiki/topics/test-automation-strategy.md]] (Sept-1).

## Open questions

- Should the old hand-written tests be compared against the newly generated set at least once, to catch edge cases before they are lost? Alexander argued yes (a one-time overlap analysis); Val argued against reaching backwards. Left to practice rather than settled — [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]] [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- How much of QA's existing knowledge is lost in the first phase, given the acknowledged gap Pavel named and Val accepted — [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]

## Sources
- [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
