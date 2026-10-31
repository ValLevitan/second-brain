---
type: meeting
title: Daily stand-up — the default CI build must build with default parameters; Yavorski blocked from merging into Flex-Port main (pull requests still allowed, no fork) while Alekseev keeps access; no Wi-Fi work into main before the port release; Leshkevich's engine spike has no Jira task ("no task, no work"); no free full replacement for FMOD; new capabilities marked MVP-2 Transactional (Oct 30 2026, 4:45–5:31 AM)
date: 2026-10-30
aliases: [Daily Standup meeting Oct 30 2026, Daily Standup Default CI Builds and Flex-Port Merge Lock, Oct 30 stand-up, Flex-Port merge lock, нету задачи нету работы]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — default CI builds and the Flex-Port merge lock (Oct 30 2026)

**Date/time:** October 30 2026 (a Friday), **4:45 – 5:31 AM Eastern**, about 45 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian**; the sound is poor in places. The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-29-daily-standup-cash-out-progress-screen-and-pulse-mode-installs.md|Oct 29]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]. Val was not present.

**Purpose.** Round-the-table status [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-30-the-default-ci-build-action-builds-with-default-parameters-for-its-target-environment-and-a-many-parameter-action-is-kept-for-claude-and-special-cases.md]] — Khamin's failed Flex IQ build; Pavel's default-build rule; the version conflict; a CI/CD task for Chudinov.
- [[wiki/people/eugine-yavorski.md]] (Oct 30) — he keeps messaging Khamin; Pavel asks Kovalchuk to block his merges into Flex-Port main; Alekseev keeps access; no fork; Pavel to ask Val whether work with him is over.
- [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Oct-30 note) — Leshkevich's modularity spike half done, no Jira task; the engine requirements into Jira that day; Daniil's FMOD sound-library problem.
- [[wiki/people/anton-seregin.md]] (Oct 30) — capabilities brought to standard; mark them MVP-2 Transactional; the Wi-Fi settings page and QR code next.
- [[wiki/people/alexei-khamin.md]] (Oct 30) — the port-to-idle recheck after a machine reboot.
- [[wiki/people/dmitri-chudinov.md]] (Oct 30) — the report-with-Excel-export capabilities; reviewing Andrei's edited requirements.
- [[wiki/people/dmitri-kovalchuk.md]] (Oct 30) · [[wiki/people/evgeniy-alekseev.md]] (Oct 30, in absentia) · [[wiki/people/anton-leshkevich.md]] (Oct 30) · [[wiki/people/evgeny-kharetski.md]] (Oct 30, 4:45 AM)
- Other people: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · in absentia: [[wiki/people/andrei-klimovich.md]]

## Other round-the-table items (kept here because they are short)

- **Pavel.** Two screens now work on the custom Linux kernel for the RK3576 SDK board ("Рк 35 68 43 р к 35 68 41… с д к 35 76", heard); next sound, the graphics accelerator and peripherals. Also the Wi-Fi access-point mode on Flex IQ and its setup screens, from tasks Anton Seregin created [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]. He also said a new integration task waits for a package that has not arrived in about a month; he will ask again, and it may go to Biratka — what device it is is **unclear** in the transcript [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Biratka.** One Flex-Port task left on BV mode (port 188, heard); Irina will pass him tasks from Andrei's updated requirements; on Flex Pay, capability 165 — SAS logging to Grafana [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Kharetski.** He finished the regulation ("регламент") discussed earlier and two feature requirements, not sure he committed them; he is preparing for a meeting that day (the notes: the competitor teardown — [[wiki/meetings/2026-10-30-ai-competitor-game-teardown-and-mechanics-library.md]]) [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Irina.** She is going through the requirements Andrei sent; she sent 22 (heard) to Biratka; the tests must then be adapted [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Ivan.** "джела" (Gela, heard) says the bill validator and printer do not show; Ivan had installed show mode without devices; he will most likely do a new install. CMS/RIS work goes on [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Tsymanov.** The port firmware changes are done for all projects and being tested (feature 189, heard); he will split the feature into capabilities per repository [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Samusenko.** He closed 3507 and LGS-44 as duplicates; a task "фрейк 3" (heard; an audit screen) is unclear and he is checking it with Biratka; he is reading the capabilities in Git ("полнова", read as on NOVA — **inference**) [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Default_CI_Builds", "October-30-2026" and "2026-10-30" found no page citing either file; the other Oct-30 sessions (8:03 AM teardown, 9:03 AM NOVA remote update) are different meetings.
- **§4 name calls.** "егорский" / "егорской" / "егорскому" and "яворского" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (Pavel says "яворского" directly; "Egorsky" is a registered alias). "Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. "евгениям" (Val approved Jira access for "the Evgenys") = Yavorski and Alekseev by context (**inference**). "Дима" asked to block merges = Kovalchuk (he answers); "Дима" on CI/CD and on Andrei's requirements = Chudinov (he answers). "Андрей" whose requirements were updated and whose port-107 item came up = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], as on Oct 29 (**inference**). "Влад" on sound — see the engine decision note. "Пиамогент" = the PM agent.
- **Garbles kept as heard.** "калиочио дачмил" — the notes read Dutch Mill; whether "калиочио" is Calle Ocho is **unclear**; "Анима анима" (the project Anton named) — **unclear**; "н ф л один" = NFL1 (heard); "мод ивинт" / "f mod" / "f mot" = FMOD; "ф с б" = FSB; "Корвии" — **unclear**; "ноланбэйс" — **unclear**; "флекс сми" — **unclear**; "ADR 503" (heard).
- **Skipped as logistics or chatter.** Pavel's proposal to move the stand-up 1.5 hours later from next week (a scheduling item; the notes leave it unconfirmed); jokes; the Halloween goodbye.
- **§15.8:** clear. **§15 #9:** clear; the numbers are task, port, feature and board numbers.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
