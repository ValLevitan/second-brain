---
type: meeting
title: Daily stand-up — Flexport tests stay on real ports (no port emulator now); separate Flex IQ version numbers per environment wait until after MVP 1; location billing goes to production as it is; the Jira "In Progress" automation fires on any mention of a task key; the AI PM's "AI Draft" tasks are reviewed from tomorrow; the Claude bot balance; video alpha on the board (Oct 12 2026, 4:56–5:42 AM)
date: 2026-10-12
aliases: [Daily Standup meeting Oct 12 2026, Daily Standup FlexPort Emulator and Jira Auto Progress Rule, Oct 12 stand-up, Flexport emulator debate, STM32 emulator, self-hosted runner, Jira auto In Progress rule, port 118, TIN-30, AI Draft review, Claude bot balance, feature 1343, capability 117, PR 169, port 111, task 1241, tasks 118-122]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flexport tests on real ports, and the Jira auto-progress rule (Oct 12 2026)

**Date/time:** October 12 2026 (a Monday), **4:56 – 5:42 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct 9]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not present.

**Purpose.** Monday round-the-table status. This is the day the AI PM was set to go live (Oct-8 ruling); Kovalchuk told the team it starts today.

## Where the substance lives

- [[wiki/decisions/2026-10-12-flexport-ci-tests-run-on-real-ports-through-the-internal-runner-and-no-port-emulator-is-built-for-now.md]] — the port-emulator debate; STM32; real ports with hooks; a simulator study is not MVP 1 and likely not MVP 2.
- [[wiki/decisions/2026-10-12-separate-flex-iq-version-numbers-per-environment-are-not-an-mvp1-blocker-and-a-fix-comes-after-mvp1.md]] — each environment counts its own versions; a task after MVP 1.
- [[wiki/decisions/2026-10-09-all-web-services-go-to-production-before-the-weekend-instead-of-waiting-for-georgia.md]] — Oct-12 update: production prep with Andrei; location billing goes out as it is.
- [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] — Oct-12 update: the automation that moves a task to In Progress on any branch, commit or pull request mention; Kovalchuk's "turn it off" is not confirmed.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] — Oct-12 update: it starts today; "AI Draft" tasks are reviewed from tomorrow morning; Reject with a resolution.
- [[wiki/decisions/2026-10-07-cover-the-code-with-tests-first-and-the-ci-hardware-runs-and-product-repository-hookup-wait.md]] — Oct-12 update: Khamin is now bringing the tests up on pull requests and on real hardware.
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Oct-12 update: no Flexport emulator for now.
- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] — Oct-12 update: Kharetski near the end of "1241"; he tests it himself; "до 22".
- [[wiki/topics/test-automation-strategy.md]] (Oct 12) — Khamin, Seregin, Irina, Ivan and Vladimir; tasks 118–122.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 12) — Chudinov's round, Biratka's capability 117, Tsymanov, Pavel's PR 169.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 12) — Daniil's feature 1343: frame rate and how to do alpha.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/nathan-carver.md]] (in absentia) · [[wiki/people/igor-metelski.md]] (in absentia, inference) · [[wiki/people/andrey-bosik.md]] (in absentia, inference)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-12-2026", "2026-10-12", "STM32", "self-hosted" and "AI Draft" found no page citing either file and no other stub for this session. The same day's 11:29 AM [[wiki/meetings/2026-10-12-ris-mvp2-scope-and-release-timing.md|RIS MVP 2 call]] is a different meeting.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" / "лёша" = Khamin. "Антон" = Seregin (he answers). "Данил" = Daniil Stauskiy. "дима" called after Daniil = Chudinov (he answers); "Дима" on the Claude bot, the Jira rule and the AI Draft tasks = Kovalchuk (he answers). "Женя" = Kharetski (he answers). "Мира" / "Ира" = Irina. "Ваня" = Ivan. "Сергей" / "Серёга" = Tsymanov. "Владимир" = Samusenko. "Андрей", who wrote about the card and who prepares production with Chudinov = [[wiki/people/andrey-bosik.md|Andrey Bosik]] by context (**inference**). "нейтан" = [[wiki/people/nathan-carver.md|Nathan Carver]] (location billing). "Игорь", to be asked how alpha and blend modes were solved in the Rage games ("Ну игры же както решил эти вопросы"), = [[wiki/people/igor-metelski.md|Igor Metelski]] by context — he ports the Rage games to NOVA (Oct 8) — **inference**.
- **Garbled numbers.** The notes' readings are kept as readings: "capality 117" = capability 117; "app IQ 147" = task 147; "ITV 150 и 151" = tasks 150 and 151; "Франк 1343" = feature 1343; "в порт 118" = port task 118; "тинт 30" = TIN-30; "fort 111" = port 111; "Порция номер 169" = pull request 169; "12:41" = task 1241 (the notes add "number unclear") [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].
- **Where the notes and the transcript differ.** The notes say Daniil re-encoded the videos "to VP8"; the transcript's codec word is garbled ("на в пде ведь"), and his later line reads "я его по 9" (VP9 by context — **inference**). On Oct 9 he had said the board has no hardware VP8 decoder. The codec is kept as **unclear**. The notes' "Decisions Made" list the AI Draft review from "October 13"; the transcript says "с завтрашнего утра" (from tomorrow morning), which is Oct 13 by the calendar.
- **§15.8:** clear. The Claude bot top-up amounts are a tool's running cost, not anyone's pay. Nobody's pay or personal matters are recorded. **§15 #9:** clear; TIN, port and task numbers are Jira keys.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
