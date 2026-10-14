---
type: meeting
title: Daily stand-up — the 8-game board and video memory; a memory leak first; the barcode scanner in the dark; an issue type for release work with no branches; PM-agent questions merged for tomorrow (Oct 13 2026, 5:05–5:29 AM)
date: 2026-10-13
aliases: [Daily Standup meeting Oct 13 2026, Daily Standup Video Decode Memory and Release Task Type, Oct 13 stand-up, 8-game board memory, video decoding memory leak, barcode scanner backlight, release work with no branches, capability 134, task 1287, FIX-163, FIX-165, TIN-17, TIN-26, task 89, GUI port tasks 122 and 52]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — video memory on the 8-game board, and an issue type for release work (Oct 13 2026)

**Date/time:** October 13 2026 (a Tuesday), **5:05 – 5:29 AM Eastern**, from the `**Date:**` header line. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel. The previous stand-up is [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct 12]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present.

**Purpose.** Tuesday round-the-table status. Pavel left early; the topic from the evening before went to a separate meeting after lunch [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Where the substance lives

- [[wiki/topics/nova-platform-architecture.md]] (Oct 13) — Daniil's report on the 8-game board: about 10 GB of memory, bonus and free-spin videos near 2 GB each, free or keep decoded video, a memory leak found overnight; Igor's Rage decoder approach.
- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 13, 5:05 AM) — Biratka's capabilities 117 and 134; Chudinov's wallet date format, Payment Hub reports, web services on STG/DEV/PROD, the Records tab; the barcode scanner in the dark.
- [[wiki/topics/test-automation-strategy.md]] (Oct 13) — Khamin's narrowed pull-request tests; Seregin's firmware and flash-boot trouble; Chudinov's 17-minute emulator smoke test; Kharetski's MVP 1 tests; Ivan's TIN-17 and TIN-26; Irina and Vladimir.
- [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] — Oct-13 update: Kovalchuk asks for an issue type for release work that has no code branches; not settled.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] — Oct-13 update: the PM agent's questions from two days are merged and discussed on Oct 14.
- [[wiki/decisions/2026-10-06-the-ris-mvp1-changes-are-built-for-georgia-only-on-the-1-14-svn-line-with-nothing-else-added.md]] — Oct-13 update: Kharetski closing "1241"; Tsymanov's question on why "RIS" is in the release name.
- People: [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/ivan.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-13-2026", "2026-10-13", "8 игр", "barcode scanner" and "release features with no branches" found no page citing either file and no other stub for this session.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" = Khamin. "Антон" = Seregin (he answers). "Даниил" = Daniil Stauskiy. "Дима" called after Daniil = Chudinov (he answers); Kovalchuk names him in full: "у димы чудинова". "дима тебе слово" at the end = Kovalchuk (he answers). "Женя" = Kharetski (he answers). "Ира" = Irina. "Ваня" = Ivan. "Игорь" = Metelski (he answers). "Сергей" = Tsymanov (he answers). The "Сергей" who was to send Igor a video is **not identified** — the transcript gives no surname. "Андрей", for whom Irina updated requirements, is **not identified** either.
- **Garbled numbers.** The notes' readings are kept: "каполить 117" = capability 117; "tasko 12 87" = task 1287; "франтыч 343" = feature 343 in the notes. On Oct 9 and Oct 12 Daniil worked on feature **1343**; this is probably the same feature (**inference**). "12 41" = task 1241. Anton's story number ("аркад 35 60. 68. Чис 29") is **garbled**; the notes say so too [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].
- **Where the notes and the transcript differ.** The notes write "MVP1 tests"; the transcript reads "Мг пи один ра" (MVP 1 by context). The notes say Igor "added Sapphire to 2"; the transcript reads "Добавил сапфир старого на 2" — what "на 2" means is **unclear** [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].
- **§15.8:** clear. Nobody's pay or personal matters. **§15 #9:** clear; task, story and TIN numbers are Jira keys.

## Sources

- [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
