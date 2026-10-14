---
type: meeting
title: Daily stand-up — MVP 1 extended to about November 8–9 with the MVP 2 tasks inside; no freeze inside a game; a library of about 5 South Dakota games on the RK3576; the Flex-Port update by USB stick for the 15th; remote RIS and boot-loop recovery; the AI digest (Oct 14 2026, 4:47–5:29 AM)
date: 2026-10-14
aliases: [Daily Standup meeting Oct 14 2026, Daily Standup MVP1 Extension and RK3576 Game Library, Oct 14 stand-up, MVP1 extension, RK3576 game library, capability 135, capability 116, FP 12 09, task 246, task 128, FlexPort 124 125 126, Pixi 8.22]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — MVP 1 extension and the RK3576 game library (Oct 14 2026)

**Date/time:** October 14 2026 (a Wednesday), **4:47 – 5:29 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct 13]] [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

**Purpose.** Wednesday round-the-table status, the day before the October-15 release. Anton Leshkevich had asked to join the stand-up, and Pavel added him [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]] — the MVP 1 date moves to about November 8 or 9, with the MVP 2-marked tasks; read as the RIS improvement MVP 1 (**inference**).
- [[wiki/decisions/2026-10-14-no-freeze-inside-a-game-so-a-games-videos-are-decoded-when-the-game-is-entered.md]] — a game's videos are decoded at game entry; about 5 games may fit in 8 GB.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 14) — Daniil's leak fix and Pixi 8.22, two Jira tasks, and the plan to convert South Dakota Rage games into NOVA vertical games for the RK3576.
- [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] — Oct-14 update: what the board is for.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Oct-14 update: the Flex-Port update by USB stick for the 15th.
- [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]] — Oct-14 note: the 15th still stands for the transactional release.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 14) — Biratka's capabilities 134, 135, 116; Chudinov's FlexPort tasks, the slow update on a production Flex IQ, and web services to the prose-and-contracts standard.
- [[wiki/topics/test-automation-strategy.md]] (Oct 14) — Khamin's real-hardware run, Seregin's installer, Ivan's task 128, Vladimir and the vague one-line requirements.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 14) — remote RIS needs the machine's software version; boot-loop recovery is not in MVP 1.
- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] and [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]] — Oct-14 updates.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] — Oct-14 update: the daily AI digest.
- [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] — Oct-14 update: a release branch is likely.
- [[wiki/projects/south-dakota-vlt-market.md]] (Oct 14) and [[wiki/topics/low-cost-street-machine.md]] (Oct 14) — the cheap street board and the South Dakota games.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia) · [[wiki/people/andrei-klimovich.md]] (in absentia) · [[wiki/people/igor-metelski.md]] (in absentia, inference)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-14-2026", "2026-10-14", "RK3576 game library", "8 или 9 ноября" and "Pixi" found no page citing either file and no other stub for this session.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей"/"Лёша" = Khamin. "Антон" called after the Flex-Port item = Seregin (he answers). "Даниил" = Daniil Stauskiy. "Дима" going on vacation = Chudinov (he answers). "Женя" = Kharetski (he answers). "Евгений Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (named in full; Flex-Port firmware fits his embedded role). "Андрей климович" is named in full. "Игорь", who has scripts to convert horizontal games, = [[wiki/people/igor-metelski.md|Igor Metelski]] by context — he ports Rage games to NOVA (**inference**). "Сергей" = Tsymanov (he answers).
- **Not resolved.** The "Антон" who is to pick a South Dakota game: Pavel had just briefed Leshkevich on the board, so Leshkevich is likely (**inference**); the notes ask Val to confirm which Anton. The "Антон" with a new Flex IQ for experiments is **not identified**. The "Андрей" whose web-service standards Chudinov followed is **not identified**. The "Андрей" who set up the daily AI digest is likely [[wiki/people/andrey-bosik.md|Andrey Bosik]], who owns the AI PM (**inference**) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- **Where the notes and the transcript differ.** The notes say the South Dakota games are "now on RAID"; the transcript reads "на реййд" and "Сауз дакоты рейдж" — the Rage platform by context. The notes' "Only FlexPay and RIS remain" reads "люкспей и ресатка" in the transcript (garbled). The notes name Evgeny Kharetski as the one to study boot-loop recovery; the transcript has Pavel address "Женя", and Kharetski answers [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- **Garbled numbers.** "ф п 12 09" (a start date Pavel asked Biratka to set) and Tsymanov's "бип 35 22" are kept as heard. The Jira project of the AI-created leak task is garbled ("ne… Анси один").
- **Skipped as chatter.** Greetings; Irina's VPN and sound.
- **§15.8:** clear. Nobody's pay. Chudinov's vacation from Oct 15 is an availability fact only. **§15 #9:** clear; the numbers are Jira keys and versions.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
