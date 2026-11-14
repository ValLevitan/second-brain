---
type: person
title: Daniil Stauskiy
date: 2026-11-08
aliases: [Daniil Stauskiy, Daniil, Даниил, Daniil Stauski]
source-count: 16
open-commitments: 1
open-questions: 0
---

# Daniil Stauskiy

A developer on JVL's Minsk engineering team (speaker label "Daniil Stauskiy" in the daily stand-ups run by [[wiki/people/pavel.md|Pavel Frolov]]) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. In November 2026 his work is the game sound library for the new engine: he is rewriting the sound repository in Rust on PulseAudio after dropping the Kira library, with a converter that turns the existing FMOD sounds from FSB into FLAC with JSON descriptions — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]]. He appears by first name on earlier pages (the engine capabilities he drafted, his RK3576 board tests, a server-side player-video spike) — see [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]], [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] and [[wiki/people/anton-leshkevich.md]]; those mentions are cited there, not here. Page created Nov 8 2026 from the Nov 2–3 stand-ups, where he speaks for himself; the role wording above is the wiki's (**inference** from the work described, not a title given in a source).

## Nov 2 2026 — the sound spike: Kira dropped, PulseAudio, Rust, FSB → FLAC + JSON

At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] he asked how to write up the spike's outcome in the task's comments, then reported: "Сейчас мы переписываем в репозиторе звука на rast"; Kira dropped for now — it cannot send sound to the top and bottom speakers separately and has no event system, saving only about 200 lines; with PulseAudio there will be one ready library for the LGS that plays on Windows and ARM; a converter tool already exists; FSB becomes FLAC and the sound description a JSON file [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. Pavel and Biratka turned it into the rewrite in Rust inside the engine — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]], where his commitment is tracked.

## Nov 3 2026 — moving the library to Rust; dependency requests

At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]: "Делаю задачу ахмад 4" (heard — a task name, **unclear**), moving the sound library to Rust ("на раз"), and in parallel looking at dependency requests that came in ("во франки пришли", heard; the notes read Dependabot) — what to merge and what to decline [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].

## Nov 4 2026 — the Rust sound-repository pull request is open; NC-1 can be closed; no task for now

At the [[wiki/meetings/2026-11-04-daily-standup-release-build-handoff-and-nad2-product-code.md|Nov-4 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]: on the rewrite of the sound repository in Rust ("на раз") "я уже открыл пиар" after solving a few problems; he closed dependency requests in the repositories; "пока нечего делать… Нет никакой задачи"; he asked whether "н ц один" (heard; NC-1) can be closed, since all its child tasks are done — Pavel: "Думаю, что можно закрывать… новое вроде не планируется"; Pavel and Biratka will think of a task for him tomorrow [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-4 note). A short exchange about his day is personal matters, not recorded.

## Nov 5 2026 — on the sound board: left speaker and subwoofer work, the right channel is silent; no task created yet; a possible engine piece later

At the [[wiki/meetings/2026-11-05-daily-standup-new-engine-capabilities-and-georgia-handpay-tilts.md|Nov-5 stand-up]] (Russian): "я сейчас удачи не создал [heard; no task created], но сейчас буду ну работать со звуковой платой. Я уже проверил сейчас левая колонка из сабвуфе работает, а вот на правую колонку почемуто звук ещё пока не выводится. Ну будут смотреть, разбираться"; Pavel's goal: sound returns after a sound-card power loss without rebooting the machine — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-5 note), where the commitment is tracked. Biratka: once his tasks run out he could take a limited engine capability — [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Nov-5 note) [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]].

## Nov 6 2026 — sound on both speakers through the Rust library, but quiet; the amplifier works; PulseAudio can boost it, but should it; sound comes back after pulling the USB and the power from the sound board

At the [[wiki/meetings/2026-11-06-daily-standup-modem-off-confirmation-capability-and-cap-287-in-mvp2.md|Nov-6 stand-up]] (Russian; his report was repeated because Pavel's headphones were off) [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]: his task numbers are heard three ways ("Фрау, 1996, 97"; "1096, прям 1997"; "from 1496 fron 7") — not recorded; "уже проверил на 2 колонках работается… играет, почему то тихо причём… сам по себе усилитель точно работает"; the sound banks keep the loudness they had in the LGS; "Я по сути через пульс аудио могу его усилить… но я просто не знаю как бы так должно, либо усилитель сам по себе уже должен усиливать"; the old FMOD library also went through PulseAudio, "а я именно… на Ростовской [Rust] библиотеке проверял"; on the old LGS crash when another board was unplugged: "сейчас я и ю с б вытягивал и питание отключал именно с платы звуковой. Потом при подключении звук восстанавливается" — Pavel: "Отлично отлично то что надо" — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-6 note), where the Nov-5 commitment is discharged and the quiet-sound commitment and the two open questions are tracked.

## Nov 9 2026 — FRAM-1496 checked and fixed; FMOD-5 (heard) to upload tomorrow as the full move to the Rust library (stereo, automatic distribution); should a sound library still go into the LGS? Biratka: no longer needed

At the [[wiki/meetings/2026-11-09-daily-standup-due-date-rule-in-standard-and-update-dependency-map.md|Nov-9 stand-up]] (Russian; Pavel started with him) — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-9 note) [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]].

### Open commitments (Nov 9 2026)

- [x] [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]] — upload the finished Rust sound library (FMOD-5, heard) — due Nov 10 2026 — [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]] — *done Nov 10 2026 (heard): "закончил задачами вход, 4 вход 5"* — [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]

## Nov 10 2026 — FLAC streaming from disk, RAM about 400 MB to 35 MB; NENG-26 (heard) passed to him; the volume path; FRAM-1496 to be closed as rejected

At the [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov-10 stand-up]] (Russian; he went first) — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-10 note) [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

### Open commitments (Nov 10 2026)

- [ ] [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]] — close FRAM-1496 as rejected, with the reason (sound no longer goes through the LGS) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]

## Nov 11 2026 — sound plays in the engine branch, in time; the sounds and their names go into the Lua scripts

At the [[wiki/meetings/2026-11-11-daily-standup-flex-pay-to-mvp3-and-sound-names-in-lua-scripts.md|Nov-11 stand-up]] (Russian): in his branch the engine now calls the sound library directly, with sounds on spins and reels, "всё звучит хорошо… работает в тайминге"; parts of the engine are not finished; on where sound names should live so the engine is not rebuilt, Anton Leshkevich: in the Lua scripts, the engine plays by name; "Окей, так и буду делать тогда, ну завтра ещё там доделаю" — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-11 note; the commitment is tracked there) [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]].

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
