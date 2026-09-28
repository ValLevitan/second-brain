---
type: meeting
title: Games conversion experiment — where the standards, ADRs, converter and scripts go, two projects under one initiative, and the experiment closes (Sept 25 2026, 9:02–9:43 AM)
date: 2026-09-25
aliases: [Games conversion experiment GitHub consolidation Jira project capabilities and requirements, Games Conversion Repos Jira Capabilities, Sept 25 9am games conversion call, converter repository call, experiment closes]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Games conversion experiment — repositories, Jira projects and retroactive capabilities (Sept 25 2026)

**Date/time:** September 25 2026, **9:02 – 9:43 AM Eastern** (about 41 minutes), from the `**Date:**` header line [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]. **Language: Russian.** It follows the [[wiki/meetings/2026-09-20-vertical-geometry-standard-and-adr-consolidation.md|Sept-20 geometry session]]: Igor opens with "На предыдущем митинге мы договорились…", and Bosik says the repositories Val asked for by email were not yet created because of open questions [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (chair), [[wiki/people/igor-metelski.md|Igor Metelski]] (presented the questions), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**Purpose.** Decide where the experiment's glossary, standards, ADRs, converter and helper scripts live; how the work maps to Jira; and when the experiment ends [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search found no page citing either file, and no stub for a Sept-24 or Sept-25 follow-up to the Sept-20 session. The same day's [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|8:05 AM MVP 1 call]] ended at 8:50 and has different content. It is a new meeting.

Substance lives on:

- [[wiki/decisions/2026-09-25-the-conversion-experiment-closes-and-the-converter-gets-its-own-project-and-repository.md]] — the rulings, the Jira structure, the undertakings
- [[wiki/decisions/2026-09-20-the-vertical-geometry-standard-glossary-and-adrs-go-to-github-outside-any-framework.md]] — Sept-25 update: where each piece actually goes; commitments re-dated
- [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]] — Sept-25 update: the geometry standard and glossary go to the same standards folder
- [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]] — Sept-25 update: initiative vs project, and repositories before Jira projects
- [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]] — Sept-25 update: the draft capabilities are still local
- People: [[wiki/people/igor-metelski.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/val-levitan.md]]

**§4 name calls** [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]:

- "Игорь метельский" / "Игорь мильский" / "Игорь цельский" (Val) = Metelski. "дима Ковальчук" / "дима, корольчука" = Kovalchuk. "Андрей" who will create the repositories ("Андрей тоже накрыть там творы позитория", garbled) = Bosik, **by context** (inference). "ира" = Irina. "Павел" = Pavel.
- "дима" in Igor's "инструкцию для димы" (what repository to create) = Kovalchuk, **inference** (he opens Jira projects).
- "нолочь" / "ноу ли че" / "нолыч бейс" = the `knowledge` repository (Bosik: "К ноу ли черепозиториям называется"). "рейдж" / "рэйд" = RAGE. "Нова" = NOVA. Igor twice says "омни" for the target platform ("конвертируем существующее рейдж игры в омни"); read as NOVA, since the omni repositories became nova on Sept 24 (**inference**). "drogonpays" / "dronpass" = the Dragon Pays game. "Галакси" = Galaxy.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]):

1. **The converter debate.** The notes give Igor's first proposal (keep it in each game's repository) and Val's ruling. They omit that Bosik first agreed with Igor ("Ну вот с этим я тоже согласен") and that Pavel first objected to a separate repository ("мне не нравится подход держать отдельные репозитории для Тула, который в зависимости от игры меняется") before Irina's question turned him.
2. **"Andrei creates the repositories."** The transcript line is garbled ("Андрей тоже накрыть там творы позитория"). Bosik as owner is an **inference**; the notes flag the same doubt.
3. **Target platform.** The notes write NOVA throughout; Igor said "омни" twice (see above).
4. **Omitted by the notes:** Kovalchuk's "Вчера инициативой мы назвали Галакси и no…"; Val's question whether Claude runs one agent or several for the scripts; Irina's six-games example of why the converter dies after use.

**§15.8:** two passages withheld — Val's teasing of Igor about smiling, and his remarks on Kovalchuk's memory — personal remarks about named people, not business substance. No pay or rate appears. **§15 #9:** no corporate identifier appears.

## Sources
- [[raw/Meeting_Notes_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
