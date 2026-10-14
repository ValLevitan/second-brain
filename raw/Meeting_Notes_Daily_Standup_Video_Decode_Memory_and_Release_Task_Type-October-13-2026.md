# Meeting Summary — Daily Standup meeting
**Date:** October 13, 2026, 5:05 AM – 5:29 AM Eastern
**Duration:** ~24 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Ivan Shpak, Igor Metelski, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026]]

## Summary

Tuesday standup run by Pavel. Held in Russian. Some task numbers are garbled in the transcript.

**PM agent questions.** Kovalchuk asked if the team should discuss the questions the PM agent posted this morning. They are not features, more like questions. Pavel: ask the PM agent to merge yesterday's questions with today's; the team discusses them tomorrow.

**Video decoding on the 8-game board (Daniil).** Daniil left a report in feature 343. The board is not a good fit for 8 games: RAM need is about 10 GB. Bonus and free-spin videos are almost 2 GB each. If decoded video is not freed, each game adds about 3 GB. If it is freed, the first entry into a feature has a small freeze. It is not decided if decoding is hardware or CPU. He also ran a game overnight and found memory leaks; he already knows where. Alexander: play must stay smooth; a small delay when entering a game is acceptable, slowdowns inside the game are not. Igor: on Rage they create decoders before an animation starts and destroy them after (a micro-freeze, then smooth play). Daniil: this works the same now, but memory is not freed after the feature ends. His idea: decode one game's videos when it is chosen on the select screen, free all on return. Pavel: Daniil works on the leak now; a separate investigation task may be needed on freeing and loading.

**Barcode scanner in the dark (Dzmitry).** This morning a terminal's barcode scanner seemed to go to sleep. Pavel: it is probably the dark — the scanner detects a change in the picture and does not turn on its backlight. Maybe the backlight should stay on all the time; something must be done. Dzmitry will check again tomorrow morning.

**Release work with no branches (Kovalchuk).** Dzmitry Chudzinau does release features (for example deploys) that have no code branches, so the report will flag "no branches". Kovalchuk suggested a new issue type, or a Task moved up in the hierarchy so it links to a capability. Pavel liked a separate issue type handled its own way. Sergey asked why not make a release branch; Dzmitry: no commits would land, they do not cut branches yet. Kovalchuk: such a type may also serve tasks the PM agent creates, but it may become clutter. Pavel: think about it. Not settled.

**Round-robin:**
- Alexander: finished capability 117 (card issuing through Payment Hub, works on STG; field fixes may follow). Finishing capability 134 (card dispenser error cases; task 1287).
- Alexey: narrowed the tests that run on each PR (checks took over 30 minutes); must watch it. Working on simulator tests passing in every PR, and hardware tests passing on a manual GitHub action run.
- Anton: closed 150 and 151. Firmware test: card creation failed, maybe hardware. Boot from flash drive: the drive is seen but the boot order seems to reset on reboot. Opened a story for Pavel (number garbled). Pavel will look.
- Dzmitry: date format made the same on all wallet screens (Spanish locale issue fixed). Payment Hub online-report fixes. Web services deployed to STG, DEV and PROD. Records tab was slow (front end recalculated dates per row) — fixed. The emulator smoke test takes 17 minutes per PR; he will speed it up.
- Evgeny: preparing MVP1 tests; setup done for 54 and 344; closing 1241. Will test while Ivan is busy, so fewer bugs reach Ivan. Pavel: while the feature is open, open stories under it for each test.
- Irina: asked if Evgeny should wait on yesterday's evening topic, since it may change things. Pavel: separate meeting after lunch. Testing items 53 (Pavel listed several numbers); will move others forward if not touched today. Updated requirements for Andrei after Vladimir's notes. Removed two unneeded features, FIX-163 and FIX-165.
- Ivan: TIN-17 done but not merged — an error in main. Waiting on TIN-26; sent Pavel at least 4 questions (link in Teams) and needs answers. Starting task 89.
- Igor: added Sapphire to 2 with new math and scenes; making vertical scenes. Sergey has not sent him the video; Pavel: Igor must write to him.
- Sergey: finished SMS/lease tasks and about 5 port telemetry tasks. Took the task discussed last evening; it needs a separate meeting. He does not see why RIS is involved. Pavel: the release was named RIS, that is the only reason. Pavel leaves now; talk after lunch.
- Vladimir: still on unblocked tasks, fixing Irina's changes and adding tests. Asked why GUI port tasks (122, 52) are on him. Irina: she assigned stories to the feature owner last night; if wrong, reassign (for example to Dima). Nobody must fix what is not theirs.
- Kovalchuk: watch your dates.

## Decisions Made

- **PM agent questions from yesterday and today are merged and discussed tomorrow.** — keep them from getting lost. (Decided by Pavel Frolov)
- **Yesterday evening's topic is discussed in a separate meeting after lunch, not at standup.** — Pavel leaves now. (Pavel Frolov, Irina Shishko)
- **Daniil works on the memory leak first; video decoding is discussed separately.** (Pavel Frolov)
- **While a feature is open, Evgeny opens stories under it for each test.** (Pavel Frolov)
- **Stories assigned to the wrong feature owner are reassigned, not fixed by force.** (Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | [Unassigned — needs clarification] | Ask the PM agent to merge yesterday's and today's questions | Oct 14 | Normal | Discussed at standup Oct 14 |
| 2 | Pavel Frolov, Sergey Tsimanov, Irina Shishko, Dzmitry Chudzinau | Separate meeting on yesterday evening's task | Oct 13 (after lunch) | High | Sergey brings questions as a list |
| 3 | Alexander Biratko | Finish capability 134 (card dispenser errors) | TBD | Normal | Task 1287 |
| 4 | Alexey Khamin | Watch the narrowed PR test run; simulator tests pass in each PR; hardware tests on manual GitHub action | TBD | Normal | |
| 5 | Pavel Frolov | Look at Anton's flash-boot story | TBD | Normal | Number garbled in transcript |
| 6 | Daniil Stauskiy | Fix the memory leaks found in the overnight run | TBD | Normal | Feature 343 |
| 7 | [Unassigned — needs clarification] | Investigation task: how to free and load decoded game video | TBD | Normal | Pavel: "possibly" |
| 8 | Dzmitry Chudzinau | Speed up the emulator smoke test (17 min per PR) | TBD | Normal | |
| 9 | Dzmitry Chudzinau | Check the barcode scanner again in the dark | Oct 14 (morning) | Normal | Backlight idea from Pavel |
| 10 | Evgeny Kharetski | Close 1241; test MVP1 and open stories under the feature | TBD | Normal | |
| 11 | Irina Shishko | Test items 53; move others forward if not touched today | Oct 13 | Normal | |
| 12 | Pavel Frolov | Answer Ivan's questions on TIN-26 (at least 4) | TBD | High | Link in Teams |
| 13 | Ivan Shpak | Start task 89 | TBD | Normal | |
| 14 | Igor Metelski | Write to Sergey about the video | TBD | Normal | Pavel asked |
| 15 | Irina Shishko, Vladimir Samusenko | Check GUI port tasks 122 / 52 and reassign if wrong | TBD | Normal | |
| 16 | Pavel Frolov, Dmitri Kovalchuk | Think about an issue type for release work with no branches | TBD | Normal | |

## Open Questions

- Video decoding on the 8-game board: hardware or CPU? Free decoded video after each feature (small freeze) or keep it (about +3 GB per game)? (Daniil Stauskiy)
- How to keep the barcode scanner working in the dark — backlight always on? (Pavel Frolov)
- Which issue type for release work with no code branches, and will PM-agent tasks become clutter? (Dmitri Kovalchuk)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: Daily Standup meeting*
