---
type: meeting
title: Daily stand-up — which out-of-service screen shows when a lease expires or a terminal is unlinked; card-dispenser tests with no card dispensers in MVP 1; Flexport signal quality is MVP 2; QA stories must carry the versions used; one rules task stays open in To Do (Oct 8 2026, 4:58–5:28 AM)
date: 2026-10-08
aliases: [Daily Standup meeting Oct 8 2026, Daily Standup Lease Expiry Scenarios and Flex Signal Quality, Oct 8 stand-up, lease expired screen, out of service lease expired, аутов сервис лиз экспайрд, terminal unlinked from location, отвязать от локации, card dispensers not in MVP1, кордиспенсеров нет в MVP один, Flexport signal quality MVP2, port task 106, Flex IQ task 1328, versions on QA stories, firmware built by Claude shows zeros, TIN-61, TIN-13, TIN-16, TIN-19, F-52, FIQ-140, task 1239, task 1343, PM agent glossary, словарь глоссарий]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — lease-expiry screens and Flexport signal quality (Oct 8 2026)

**Date/time:** October 8 2026 (a Thursday), **4:58 – 5:28 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. Pavel: "Надо 15 числа осталось меньше недели" — less than a week to the 15th.

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"). Val was not present.

**Purpose.** Round-the-table status, plus two open product questions: which screen a terminal shows when its lease expires or it is unlinked from a location, and how card-dispenser tests can run when MVP 1 has no card dispensers.

## Where the substance lives

- [[wiki/decisions/2026-09-11-lease-blocking-reaches-the-flex-ports-and-is-never-automatic.md]] — Oct-8 update: the lease expired on the test terminals and all Flexports stopped; the out-of-service screens; two scenarios; review with Andrei.
- [[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]] — Oct-8 update: Khamin's card-dispenser tests; Irina: no card dispensers in MVP 1, raised two weeks ago and never discussed.
- [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] — Oct-8 update: Flexport does not send its own signal quality; Wi-Fi is MVP 2; tasks for MVP 2.
- [[wiki/decisions/2026-10-05-a-release-bakes-a-file-of-the-component-versions-it-contains-into-the-artifact.md]] — Oct-8 update: QA stories must say which versions were used; Claude-built firmware shows zeros.
- [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] — Oct-8 update: Khamin's rules task stays open, in To Do.
- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] — Oct-8 update: Kharetski's task 1239, and why the old release cannot move to Git.
- [[wiki/projects/ai-project-manager-and-company-second-brain.md]] — Oct-8: Kovalchuk asks for a glossary of Russian pronunciations of Jira project codes.
- [[wiki/topics/test-automation-strategy.md]] (Oct 8) and [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 8) — the rest of the round.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/andrei-klimovich.md]] (in absentia)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-8-2026", "2026-10-08", "1343" and "FIQ-140" found no page citing either file and no other stub for this session. The previous stand-up is [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct 7]]. The same day's [[wiki/meetings/2026-10-08-rage-nova-dragon-pays-vertical-port-and-symbol-distortion.md|7:04 AM Dragon Pays review]] is a different meeting.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" / "Лёша" = Khamin. "Антон" / "Антоха" = Seregin (he answers; Chudinov asks "Антоха" for edits). "Даниил" = Daniil Stauskiy. "Дима" called on after Daniil = Chudinov (he answers). "Женя" = Kharetski (he answers). "Ира" = Irina. "Иван" = Ivan. "Сергей" = Tsymanov. "Владимир" = Samusenko. The closing "Диме тогда слово" = Kovalchuk (he answers). "Дима" whose dates Biratka fixed = Kovalchuk by context (he speaks about dates — **inference**). "Андрей" with whom the lease scenarios must be reviewed — the one who wrote the requirements — = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] by context (he took the Flex-Port blocked-screen requirements on Sept 11 — **inference**). "Женя" who may hold the battery feature (Pavel to Ivan) — **unclear** which Zhenya; not resolved. "Андрей" whose reports Pavel reads with Dima's — **unclear**.
- **Garbled numbers.** The notes' readings are kept as readings: "спорт 106" = port task 106; "13, 28" = Flex IQ task 1328; "фик 67" = feature 67; "10 57" = 1057; "ф 52" = F-52; "12:39" = task 1239; "фи ай кью 140" = FIQ-140 [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].
- **Where the notes and the transcript differ.** The notes say Sergey took log-memory work "after the incident two days ago"; the transcript has "вчера по утру было. Позавчера" — he corrected himself to the day before yesterday. Kept as the day before yesterday.
- **§15.8:** clear. Nobody's pay or personal matters are recorded. **§15 #9:** clear. TIN, F, FIQ and task numbers are Jira keys.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
