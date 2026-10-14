---
type: meeting
title: Rage-to-Nova port review — two tool repositories done, geometry-first autotests on Dragon Pays accepted, the transition test that does not catch the defect, horizontal-to-vertical added in parallel, "graphic contracts", and no files left on a local computer (Oct 5 2026, 7:01–8:09 AM)
date: 2026-10-05
aliases: [Review Igor's Rage-to-Nova progress, Rage Nova Port Autotests and Horizontal to Vertical Layout, Oct 5 Rage to Nova review, repo standards ADR prose geometry and timing tests acceptance criteria, Dragon Pays port autotests, мутационное тестирование, графические контракты, graphic contracts, Nova scene generator, Rage to Nova scene converter, next review Thursday Oct 8 7:00]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Rage-to-Nova port review — autotests and horizontal-to-vertical (Oct 5 2026, 7:01 AM)

**Date/time:** October 5 2026, **7:01 – 8:09 AM Eastern** (about 68 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. Teams meeting. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (organizer), [[wiki/people/igor-metelski.md|Igor Metelski]] (presented), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. Irina left at about the 59-minute mark, at Val's request, to join another meeting [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

**Purpose:** follow-up to the last games-conversion meeting ([[wiki/meetings/2026-09-25-games-conversion-repos-jira-capabilities.md|Sept 25]]): the tool repositories, and the state of testing for the Rage-to-Nova port. Igor opened with "На прошлом митинге мы обсудили, что нам нужно вынести некоторые инструменты… в отдельные репозитории" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

**§12:** a corpus-wide search found no stub for this session. The same day's [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|4:54 AM stand-up]] is a different meeting (it ended at 5:40). The notes and the transcript share the title, date and time and link each other — one meeting. No stub exists for the Wed Sept 30 follow-up set on Sept 25; whether it was held is not shown.

Substance lives on:

- [[wiki/decisions/2026-10-05-geometry-first-port-autotests-accepted-and-geometry-checks-named-graphic-contracts.md]] — how the tests work, the transition defect they miss, mutation testing, Val's approval, "graphic contracts"
- [[wiki/decisions/2026-10-05-horizontal-to-vertical-conversion-runs-in-parallel-with-the-port-autotests.md]] — the horizontal↔vertical debate and Val's direction
- [[wiki/decisions/2026-10-05-conversion-tools-and-tests-leave-the-local-computer-now-and-claude-proposes-the-repository-layout.md]] — where tools and tests go, tests only from acceptance criteria, the next review
- Updates on [[wiki/decisions/2026-09-25-the-conversion-experiment-closes-and-the-converter-gets-its-own-project-and-repository.md]], [[wiki/decisions/2026-09-20-the-vertical-geometry-standard-glossary-and-adrs-go-to-github-outside-any-framework.md]], [[wiki/decisions/2026-09-17-hard-geometry-from-the-scene-files-and-a-vertical-skeleton-per-game-format.md]], [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]]
- Topics: [[wiki/topics/test-automation-strategy.md]] · [[wiki/topics/nova-platform-architecture.md]] · [[wiki/topics/game-art-animation-production-pipeline.md]]
- People: [[wiki/people/igor-metelski.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/val-levitan.md]]

**§4 name calls:** "рэйдж" / "рейдж" / "red shiggram" / "regesten" = Rage; "вомни" / "омниформат" / "ново" = the NOVA target (Igor also says "омни"); "драгон пейс" / "драганпейс" / "драганпэйс" = Dragon Pays; "саус дакоты" / "sust docota" / "сауздоклоты" = South Dakota; "тест 360" = Test 360; "мутейшн джиэс" = a mutation script, read as a `.js` file (**inference**); "Кристина одной и той же игры" — **unclear** (from context, "copies of one and the same game"); "спайси frots" = Spicy Fruits; "секрет родео спинс" = Secret Rodeo Spins (as spoken); "д 27" = D27 [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

**Notes vs transcript:** the notes [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] match the transcript on the rulings. They give the next review as "Thursday, October 8, 7:00 AM"; the transcript says "В четверг… на 07:00" without a date. They omit that Igor, after "у нас будет миллион этих шаблонов", later said the number of pay-table templates is "неважно".

**§15.8:** clear — no pay, rate or bonus appears. Val's remarks on reading load and on Igor's speaking pace are recorded only as working style. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
