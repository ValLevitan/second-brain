---
type: meeting
title: Daily stand-up — MVP 2.2 work goes into a temporary "dev" branch off main, merged when 2.1 is released (an experiment, kept out of the reports); Flex-recycler support stays off production; Khamin finds the Flex-Port update erases the base application, so Pavel asks Alekseev before the requirement changes; the master capability is Accepted; up to four local Claude review rounds; SMS release only from main disputed; Jira tasks for non-code work not decided (Nov 26 2026, 3:45 AM)
date: 2026-11-26
aliases: [Daily Standup meeting Nov 26 2026, Daily Standup Jira Tasks for Non Code Work and MVP2 2 Dev Branch, Nov 26 stand-up, dev branch stand-up]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Jira tasks for non-code work and the MVP 2.2 dev branch (Nov 26 2026, 3:45 AM)

**Date/time:** Thursday November 26 2026, **3:45 AM Eastern**, 40 minutes 22 seconds, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Jira_Tasks_for_Non_Code_Work_and_MVP2_2_Dev_Branch-November-26-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Jira_Tasks_for_Non_Code_Work_and_MVP2_2_Dev_Branch-November-26-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The previous Minsk stand-up in the wiki is [[wiki/meetings/2026-11-25-daily-standup-bep-cleanup-and-port-update-requirements.md|Nov 25]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present.

**Purpose.** Round-the-table status; where MVP 2.2 code goes; the Flex-Port update requirement; Jira for non-code work.

## Where the substance lives

- [[wiki/decisions/2026-11-26-mvp-2-2-work-goes-into-a-temporary-dev-branch-off-main-flex-recycler-support-stays-off-production-and-alekseev-is-asked-before-the-flex-port-return-requirement-changes.md]] — the dev branch, the master capability, the recycler, the Flex-Port finding, review rounds, Jira for non-code work, the EBDS module, GitHub, SMS release, RIS; all commitments and questions.
- Earlier rulings with Nov-26 notes: [[wiki/decisions/2026-11-25-nothing-new-goes-into-the-bep-jira-project-each-repository-uses-its-own-prefix-old-project-changes-get-a-new-capability-and-the-power-loss-during-update-report-is-proposed-out-of-the-requirement.md]] · [[wiki/decisions/2026-11-25-mvp-2-1-closes-only-after-alekseev-confirms-the-wi-fi-module-update-and-the-autotests-finish-the-scope-stays-fixed-an-alpha-build-goes-to-andrei-on-saturday-and-minsk-gets-full-new-flex-ports.md]] · [[wiki/decisions/2026-11-20-a-failed-flex-port-firmware-update-is-not-shown-on-the-port-screen-and-hardware-only-autotest-scenarios-are-marked-manual-in-a-separate-feature.md]] · [[wiki/decisions/2026-11-20-mvp-2-1-is-set-for-wednesday-november-25-task-399-moves-into-2-1-no-central-rollback-fix-forward-and-mvp-2-2-is-the-master-role-and-reporting.md]] · [[wiki/decisions/2026-11-24-a-pull-request-may-not-merge-while-a-claude-review-red-mark-stands-developers-lose-operating-system-access-to-the-production-accounting-host-and-the-requirements-sprawl-goes-to-a-separate-meeting-before-val.md]] · [[wiki/decisions/2026-11-18-claude-grooms-jira-under-a-written-standard-unlinked-work-untouched-three-months-is-archived-no-not-to-forget-tasks-backlog-at-most-a-month-everything-under-a-value-stream.md]] · [[wiki/decisions/2026-11-12-the-recycler-gets-its-own-mvp-1-on-the-production-server-by-thursday-november-19-and-its-mvp-2-a-week-later-scope-is-cut-never-the-date.md]] · [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]]
- Topics / projects: [[wiki/topics/github-release-management-pipeline.md]] · [[wiki/topics/test-automation-strategy.md]] · [[wiki/topics/ai-assisted-development.md]] · [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (all Nov 26)
- People (all Nov 26): [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia) · [[wiki/people/andrei-klimovich.md]] (in absentia) · [[wiki/people/sebastian.md]] (in absentia)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share date, time and title and link each other. A corpus-wide search for both filenames, "November-26-2026" and "2026-11-26" found no page citing either file.
- **§4 name calls.** "Саша" = Biratka; "Лёша" = Khamin; "Дима" in the round = Chudinov (label); "Дима" on dates = Kovalchuk (label); "Андрей" who answers the MVP 2.2 questions = [[wiki/people/andrei-klimovich.md|Klimovich]] (**inference**); "Андрей климович" (Kovalchuk's alpha-build example) = Klimovich; "алексееву" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]; "женя" who asked about the bill-validator service = Kharetski (**inference**); "нэйтана" = [[wiki/people/nathan-carver.md|Nathan Carver]] (**inference**); "эмма" = Emma, the AI project manager; "вал" / "давал" = Val; "Володя" = Samusenko; "Ваня" = Ivan.
- **Garbles kept as heard.** "подвижку" = NOVA (notes); "капбилить" / "capoбилитил" / "кампобилити" = capability; "Олег рисайте ро" / "риса иклеру" = the RIS recycler (notes); "Сайпер" = the recycler (**inference**); "е б д с" = EBDS; "мии мии" / "мий мий" — perhaps MEI, **unclear**; "симовский" — **unclear**; "пор 13" / "спорт 3" — the closed item with the update requirements, **unclear**; "пофлекси и кюфлекс. Фей и рефлекс рисай кллера" = the Flex products and the Flex recycler (notes); "maney" / "Майне" = main; "мегенхаме" — **unclear**; "Дженни" — whom Ivan and Pavel address is **unclear**; "семьям ту 730" — a fix number, **unclear**; "146" — a front-end task, **unclear**; "аккаунтин хост" = accounting host; "с т г" / "стг" = STG; "в леге" = legacy (**inference**); "полюсе" = policy; "в о т" = OTA (**inference**); "MVVP" = MVP; "саузда корвен" / "солсакоте" = South Dakota (notes and §4 garble rule); "в масштане" — **unclear**; "ацепт" / "аксептот" = Accepted; "прополз" = Proposal; "не гашевич" = negotiation; "девку" / "деф" / "д ветку" = the dev branch.
- **Skipped as chatter.** Joining, the meeting-timer remark, the banter about the incoming student, the goodbye.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** clear — item numbers only.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Jira_Tasks_for_Non_Code_Work_and_MVP2_2_Dev_Branch-November-26-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Jira_Tasks_for_Non_Code_Work_and_MVP2_2_Dev_Branch-November-26-2026.md]]
