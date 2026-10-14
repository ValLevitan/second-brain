---
type: decision
title: The conversion tools and test scripts leave Igor's computer now — into his current repository until a better place is set — and Claude is asked for a repository-layout proposal (Oct 5 2026)
date: 2026-10-05
aliases: [no files kept locally, я против чтобы они лежали локально, conversion tools into current repository, universal scripts and game scenarios, tests only from acceptance criteria, non-functional requirements, нон фанкшнал, spike not project, спайк, conversion tests vs game scenarios, Nova integration repository has no structure, 80 percent of tests to the integration repository, reference not copy, feed the meeting to Claude, Jira project for game conversion, next review Thursday 7:00]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
---

# The conversion tools and test scripts leave Igor's computer now, and Claude is asked for a repository-layout proposal

Set at the [[wiki/meetings/2026-10-05-rage-nova-port-autotests-and-horizontal-to-vertical-layout.md|Oct 5 2026, 7:01 AM review]] (Russian). [[wiki/people/val-levitan.md|Val Levitan]] made the call; [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] shaped it. It carries on from [[wiki/decisions/2026-09-25-the-conversion-experiment-closes-and-the-converter-gets-its-own-project-and-repository.md|Sept 25]] [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What is done, and what is still local

- **Two tool repositories are done.** Igor moved two experiment tools into their own repositories, set up to the standard with prose (and ADRs — read from the garble "Я д р в них", **inference**): a NOVA scene generator ("для создания вертикальной рейдж сцены и заданной геометрии ресурсов") and a Rage-to-NOVA scene converter. A new employee used the converter to build a game-select screen for NOVA, so the handover worked [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. *(The employee is not named. [[wiki/topics/nova-platform-architecture.md]] records Daniil converting the select screen from Sept 30 — that it is him is an **inference**.)*
- **The rest is only on his computer.** The rest of the conversion procedure (connecting the new maths, moving the logic from Rage to NOVA) and the test scripts "существует только локально до сих пор". It is unclear how to hand it to another developer [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **His split.** Universal scripts for any game, plus game-specific test scenarios. A scenario says what to do and which acceptance criteria it covers, and is fed to the universal scripts [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## Val: tests come only from acceptance criteria

- "Тесты пишутся после Того, что сделан написан эксцептом критериев рекларамент." The scripts were written apart from requirements and acceptance criteria [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- He read the "universal scripts" as **non-functional requirements** that are not written yet and have no capabilities. His explanation: functional requirements come from use cases set by the customer, and "заказчика это рынок"; non-functional requirements describe the technical product the engineers need, and are not set by the market. He said these are the standards adopted from the consultants, and asked to be corrected if wrong [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- Pavel: "большинство Того, что мы здесь обсуждаем, это и будет нон факшнал рекларамент." Irina saw the scripts more as "хуки" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- Igor said game scenarios are exactly what acceptance criteria describe — add money, press spin, wait, check — and each check has its own functional acceptance criterion [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## Project or spike, and where the tests live

- **Pavel:** the series of meetings describes a project to convert games from Rage to NOVA, with a Jira project and a Git repository. **Val:** "для меня это… Спайк." But they agreed at the last meeting that it needs its own project. Pavel: "Мы говорили, что нужен репозиторий… этот репозитории завели да?" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- **Evgeny:** autotests that check a conversion belong to the conversion project, not to NOVA. Game scenarios belong in the NOVA integration repository, which exists but "структура нет, ничего нет" yet; it will appear soon [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Pavel:** in the end "на 80% или на 100%" of the tests move to the integration repository, for building the game. They need not be copied: "на них можно сделать референс в интеграционном репозитории". Evgeny: "это тоже разберёмся" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Igor:** one repository or several for the tools? The converter and the tests both need the measurements of the original game. Evgeny: separate, independent structures are the norm. Pavel: the conversion repository looks like an integration repository too [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## What was decided

- **Ask Claude.** Evgeny: give this meeting and the standards to Claude, because the case "не выглядит какаято стандартная". Val liked it: ask Claude for a proposal "согласно нашим стандартам" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **For now, Igor's current repository.** Pavel: "пока что мы, наверное, принимаем решение, что нам надо сейчас сделать проект в giry"; Igor can put all his other tools and the tests in the repository he uses now. Evgeny: the game scenarios can go there too for now, "чтобы их не потерять" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Nothing stays local.** Val: "Я, я против, чтобы они лежали локально, поэтому чем скорее давайте заведём проект" — and if something lands in the wrong place, "мы потом переместим это" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Next review: Thursday at 7:00.** Val first said Wednesday; Igor thought it was too early. Val: "В четверг значит, на 07:00 я назначу" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. The notes give the date as Thursday Oct 8 [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — move the local conversion tools, test scripts and game scenarios into his current repository — due unspecified ("чем скорее") — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [ ] Owner not named — create the Jira project for game conversion (Rage to NOVA) — due unspecified — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [ ] Owner not named — give this meeting and the JVL standards to Claude and bring back a proposal for organizing the conversion repositories — due unspecified — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — send the invite for the Thursday 7:00 follow-up — due before Thu Oct 8 2026 — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

## Open questions

- Do conversion tests live in a conversion repository and game scenarios in the NOVA integration repository? One repository or several for the conversion tools? — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- Are the "universal scripts" non-functional requirements that need capabilities of their own? Val's reading; not settled — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
