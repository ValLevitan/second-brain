---
type: meeting
title: Daily stand-up — all web services go to production before the weekend; one machine's bad statistics block everyone again and a task is opened; tests to October 15 follow 80/20 with device tests first; a 12:45 meeting on testing with cloud services; DB9 or the 4-pin SAS connector; the old updater repo is archived; the AI PM "Dasha" starts Monday (Oct 9 2026, 4:46–5:22 AM)
date: 2026-10-09
aliases: [Daily Standup meeting Oct 9 2026, Daily Standup Weekend Service Rollout and Stats Blocking, Oct 9 stand-up, weekend web services rollout, statistics host blocked, 80 20 tests, cloud test meeting 12:45, DB9 vs 4-pin SAS connector, updater repo archived, Dasha PM agent, capability 133, capability 143, capability 117, emulator task 146, emulator task 147, bug 1057, feature 1343, task 1238, TIN-19, TIN-16, TIN-56, TIN-76, TIN-11, TIN-21, requirement 1813, test 769]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — weekend roll-out and the blocked statistics host (Oct 9 2026)

**Date/time:** October 9 2026 (a Friday), **4:46 – 5:22 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct 8]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not present.

**Purpose.** Round-the-table status on the Friday before the October-15 MVP 1 date, plus the weekend production roll-out and the statistics host that one machine keeps blocking.

## Where the substance lives

- [[wiki/decisions/2026-10-09-all-web-services-go-to-production-before-the-weekend-instead-of-waiting-for-georgia.md]] — roll out all web services now; Chudinov may test a terminal over the weekend.
- [[wiki/decisions/2026-10-09-one-machines-bad-statistics-must-stop-blocking-the-statistics-host-and-a-task-is-opened.md]] — a Minsk-office machine blocked the statistics host again; a task is needed.
- [[wiki/decisions/2026-10-09-tests-to-october-15-follow-80-20-and-port-machine-and-iq-tests-come-before-cloud-tests.md]] — 80/20, device tests first; Irina's "maybe 80%".
- [[wiki/decisions/2026-10-09-the-old-usb-updater-repository-is-archived-because-rauc-now-does-usb-updates.md]] — Biratka's old updater repo.
- [[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]] — Oct-9 update: Pavel sets the cloud-test meeting for 12:45.
- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] — Oct-9 update: Kharetski on 1238; Tsymanov's urgent lease-code task; the old RIS at factory reset is planned, not scheduled.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] — Oct-9 update: "Dasha" in test mode, production Monday.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 9, 4:46 AM) — Chudinov's Payment Hub answers, screen watchdog, SAS emulator, lease lost after reboot; the SAS connector; Tsymanov's fatal-error handling; Biratka's capabilities.
- [[wiki/topics/test-automation-strategy.md]] (Oct 9) — Khamin, Seregin, Irina, Ivan and Vladimir.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 9) — Daniil: no hardware VP8 decoder on the board; VP9 with alpha for the select screen.
- [[wiki/projects/georgia-market-rollout.md]] (Oct 9) — Ivan helped Elizabeth get SAS working; machines leave with modems.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/elizabeth.md]] (in absentia) · [[wiki/people/genadi-peari.md]] (in absentia) · [[wiki/people/sebastian.md]] (in absentia, inference)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-9-2026", "2026-10-09", "1238" and "Dasha" found no page citing either file and no other stub for this session. The same day's 8:01 AM [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Transactional MVP 1 call]] is a different meeting.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" = Khamin. "Антон" = Seregin (he answers). "Даниил" = Daniil Stauskiy. "Дима" called after Daniil = Chudinov (he answers); the closing "Дима" on the PM agent = Kovalchuk (he answers). "Женя" = Kharetski (he answers). "Ира" = Irina. "Иван" = Ivan. "Сергей" = Tsymanov. "Владимир" = Samusenko. "Андрей", who will archive the repo = [[wiki/people/andrey-bosik.md|Andrey Bosik]] by context (**inference**). "Геннадий" / "Гена" = [[wiki/people/genadi-peari.md|Genadi Peari]]. "Алексей", who with Genadi routed SAS to the 4-pin connectors, is **unclear** — the transcript gives no surname. "кортез", who wrote in the chat about the machines = [[wiki/people/sebastian.md|Sebastian]] (alias Sebastian Cortes) by name and field context — **inference**. "Элизабет" = Elizabeth.
- **Garbled numbers.** The notes' readings are kept as readings: "побилите 133" = capability 133; "143" = capability 143; "117 capobility" = capability 117; "фейк ю 146" / "феоке 147" = emulator tasks 146 / 147; "fram 1057" = bug 1057; "фрау 1343" = feature 1343; "12 38" = task 1238; "тин 76" = TIN-76; "стинг 56" = TIN-56; "18, 13" = requirement 1813; "7 69" = 769 [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Where the notes and the transcript differ.** The notes say Elizabeth "had to ship 10 machines today"; the transcript has "ей сегодня надо было в 10 машин отправлять на 5, из которых водем работали" — the count is garbled, so it is kept as "machines to ship". The notes' "4-pin" connector is right ("четырёхконтактные"); Pavel later says "девятиконтактный" for the one that needs a special cable — **unclear**. The notes give the cloud meeting "12:45"; no time zone is stated.
- **§15.8:** clear. Nobody's pay or personal matters are recorded. **§15 #9:** clear. TIN and task numbers are Jira keys.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
