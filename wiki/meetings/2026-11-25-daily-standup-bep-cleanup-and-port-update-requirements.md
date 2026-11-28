---
type: meeting
title: Daily stand-up — nothing new goes into the BEP Jira project (each repository has its own prefix; BEP to be deleted; Ivan moves his stories to CMS); old-project changes get a new capability; power loss during a Flex-Port update is not reported now — Pavel calls it a separate MVP and Seregin comments on Klimovich's requirement; Seregin's loader fix; Khamin's manual Flex-Port round and broken-firmware test; Bosik opens a capability for Chudinov's dead code before deleting GitHub variables; Emma's duplicate features; Claude limits and Samusenko's "standards" plugin; Pavel thinks MVP 2.1 goes on all devices (Nov 25 2026, 3:46 AM)
date: 2026-11-25
aliases: [Daily Standup meeting Nov 25 2026, Daily Standup BEP Cleanup and Port Update Requirements, Nov 25 stand-up, BEP clean-up stand-up]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — BEP clean-up and the port-update requirement (Nov 25 2026, 3:46 AM)

**Date/time:** Wednesday November 25 2026, **3:46 AM Eastern**, 41 minutes 32 seconds, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]] [[raw/Meeting_Notes_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The previous Minsk stand-up in the wiki is [[wiki/meetings/2026-11-24-daily-standup-requirements-sprawl-and-claude-review-merge-gate.md|Nov 24]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not present.

**Purpose.** Round-the-table status; Jira project hygiene; the Flex-Port update requirement.

## Where the substance lives

- [[wiki/decisions/2026-11-25-nothing-new-goes-into-the-bep-jira-project-each-repository-uses-its-own-prefix-old-project-changes-get-a-new-capability-and-the-power-loss-during-update-report-is-proposed-out-of-the-requirement.md]] — the BEP ruling, the new-capability rule, the power-loss case, the Flex-Port status, Bosik's GitHub and cluster notices, Emma, Claude limits and the plugin, MVP 2.1; all commitments and questions.
- Earlier rulings with Nov-25 notes: [[wiki/decisions/2026-11-24-a-pull-request-may-not-merge-while-a-claude-review-red-mark-stands-developers-lose-operating-system-access-to-the-production-accounting-host-and-the-requirements-sprawl-goes-to-a-separate-meeting-before-val.md]] · [[wiki/decisions/2026-11-20-a-failed-flex-port-firmware-update-is-not-shown-on-the-port-screen-and-hardware-only-autotest-scenarios-are-marked-manual-in-a-separate-feature.md]] · [[wiki/decisions/2026-11-18-claude-grooms-jira-under-a-written-standard-unlinked-work-untouched-three-months-is-archived-no-not-to-forget-tasks-backlog-at-most-a-month-everything-under-a-value-stream.md]]
- Topics / projects: [[wiki/topics/github-release-management-pipeline.md]] · [[wiki/topics/test-automation-strategy.md]] · [[wiki/topics/ai-assisted-development.md]] · [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (all Nov 25)
- People (all Nov 25): [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/ivan.md]] · [[wiki/people/andrei-klimovich.md]] (in absentia) · [[wiki/people/evgeny-kharetski.md]] (in absentia)

## Smaller status items, kept here only

- **Chudinov** finished some MVP 2 items and is studying a capability heard as "Билли 365"; his part of MVP 2.1 is closed [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]].
- **Samusenko**: tickets 116 and 107 are in review; he took 108 [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]].
- **Irina** finishes the autotests for 2.1 [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]].
- **Kovalchuk:** reminder on dates — Seregin has the most overdue items [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share date, time and title and link each other. A corpus-wide search for both filenames, "November-25-2026" and "2026-11-25" found no page citing either file.
- **§4 name calls.** "Дима" in the round = Chudinov (he answers; Biratka: "дима там будет чудинов"); "Дима" on the Claude account = Kovalchuk (speaker label); "Саша" = Biratka; "Антон" = Seregin; "Андрей" whose requirement it is = Klimovich ("Климовичем"); "Андрей" who answered the counters = Klimovich (**inference**); "женя" who talked with Val yesterday = Kharetski (**inference** — the Nov-24 design-guide call); "женя" with the RIS fixes, the modem questions and the RK3576 installer = Kharetski (**inference**); "Филиппа" = [[wiki/people/felipe-miranda.md|Felipe Miranda]] (**inference**); "Даниилу… Игорю… жение" = Daniil Stauskiy, Igor Metelski, Kharetski (NOVA team — **inference**).
- **Garbles kept as heard.** "Влик спорт флег хайкью" = Flex Port / Flex IQ (notes); "IP ему" / "мма" / "эмму" = Emma (notes); "холпов" / "хупов" — a studio phase, **unclear**; "полиса клиру" — **unclear**; "в и п" / "бепах" / "б е п" / "бип" = BEP; "цэсце" / "смеси" / "самэсте" / "цэмэске" = CMS (notes); "рейд" / "рейдж" / "рейч" = RAGE (**inference**); "лего с" / "легосе" = legacy; "сяйка" / "сийка" = CI; "githlication" / "Гетхаб апли кейшн" = GitHub application; "клод деспе" = Claude Desktop; "Стандартс" = the "standards" plugin; "м випи 21 под по флексей кью" = MVP 2.1 for Flex IQ; "р к 35 76" = RK3576; "инстаграм" = installer (**inference**); "2 модему" — which modem is **unclear**; "Билли 365" — capability number **unclear**; "с т г" = STG (**inference**).
- **Skipped as chatter.** Joining, "Без 15", swearing, the "Поругаем её" joke about Emma, the goodbye.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** clear — item and capability numbers only.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_BEP_Cleanup_and_Port_Update_Requirements-November-25-2026.md]]
