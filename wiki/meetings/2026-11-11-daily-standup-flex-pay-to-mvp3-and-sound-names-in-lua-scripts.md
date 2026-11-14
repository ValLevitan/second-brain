---
type: meeting
title: Daily stand-up (short, 15 minutes) — Flex-Pay goes to MVP 3 on January 20 and the recycler probably too, but not for Georgia; Biratka extends the GCM bill-validator service to the recycler; sound files and their names live in the Lua scripts and the engine plays them by name; the emulator fetches firmware from dev or STG and does not emulate the cloud service; a factory-firmware board boots from the SD card only with an HDMI monitor, so the first firmware will be flashed by cable; Chudinov's machine-statistics export is released; Igor's scene tool is ported to the engine (Nov 11 2026, 6:17–6:33 AM)
date: 2026-11-11
aliases: [Daily Standup meeting Nov 11 2026, Daily Standup Flex Pay to MVP3 and Sound Names in Lua Scripts, Nov 11 stand-up, Flex-Pay to MVP 3 January 20, sound names in Lua scripts, factory firmware SD card needs HDMI, TIN-194, FIQ-83]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flex-Pay to MVP 3 and sound names in the Lua scripts (Nov 11 2026)

**Date/time:** Wednesday November 11 2026, **6:17 – 6:33 AM Eastern**, about 16 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** Kept to 15 minutes because another meeting followed ("нам 15 минут на это", Irina) [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. The previous stand-up is [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov 10]]; the next session that morning is [[wiki/meetings/2026-11-11-trial-game-review-aristocrat-mechanic-not-built-on-rage.md|the 6:37 AM trial-game review]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]].

**Purpose.** Round-the-table status ("быстренько пробегаемся", Pavel) [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-11 note) — Flex-Pay in MVP 3 on January 20; Wi-Fi on the port done (Tsymanov); Chudinov on MVP 2 bugs.
- [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]] (Nov-11 note) — Biratka's bill-validator service extended to the recycler and released; the recycler probably in MVP 3, not for Georgia.
- [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]] (Nov-11 note) — sound in the engine branch; sounds and names in the Lua scripts.
- [[wiki/decisions/2026-11-10-the-flex-iq-is-released-with-two-screens-connected-and-the-single-screen-install-fix-is-held.md]] (Nov-11 note) — the factory-firmware SD-card boot needs an HDMI monitor; a board hardware problem; cable flashing in future releases; a production flashing document.
- [[wiki/decisions/2026-10-29-machine-reports-come-as-a-role-limited-excel-export-from-the-legacy-cms-and-tableau-is-dropped.md]] (Nov-11 note) — the machine-statistics export closed and released; Val told it is ready.
- [[wiki/decisions/2026-11-06-rage-is-finished-nova-2-is-antons-rust-engine-with-lua-scripted-framework-and-games-lgs-stays-miranda-and-unity-are-not-needed-code-first-then-prose-no-browser-runtime-and-all-work-moves-to-corporate-repositories.md]] (Nov-11 note) — Igor's scene tool ported to the engine; custom shaders; merge and Anton's review.
- [[wiki/decisions/2026-11-05-the-modem-stays-always-on-with-no-operator-on-off-screen-and-is-disabled-only-through-a-deliberate-qr-scan-server-event-and-activation-code-routine.md]] (Nov-11 note) — Kharetski on the LTE task; Pavel looks at the Georgia modem tonight.
- [[wiki/topics/test-automation-strategy.md]] (Nov 11) — Khamin's TIN-93 closed and TIN-194; Seregin's FIQ-83 and the emulator ruling; Samusenko's tests 105, 111, 114 and machine 82.
- People: [[wiki/people/pavel.md]] (Nov 11) · [[wiki/people/alexander-biratka.md]] (Nov 11) · [[wiki/people/alexei-khamin.md]] (Nov 11) · [[wiki/people/anton-leshkevich.md]] (Nov 11) · [[wiki/people/anton-seregin.md]] (Nov 11) · [[wiki/people/daniil-stauskiy.md]] (Nov 11) · [[wiki/people/dmitri-kovalchuk.md]] (Nov 11) · [[wiki/people/dmitri-chudinov.md]] (Nov 11) · [[wiki/people/evgeny-kharetski.md]] (Nov 11) · [[wiki/people/igor-metelski.md]] (Nov 11) · [[wiki/people/irina-shishko.md]] (Nov 11) · [[wiki/people/ivan.md]] (Nov 11) · [[wiki/people/sergey-tsymanov.md]] (Nov 11) · [[wiki/people/vladimir-samusenko.md]] (Nov 11)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Flex_Pay_to_MVP3", "November 11, 2026" and "2026-11-11" found no page citing either file.
- **Notes vs transcript.** The notes' "January 20, 2027" is "начало следующего года, то есть там 20 января". The notes' "TIN-93" / "TIN-194" are "ти на 90 93" / "тин 194" (heard). "FIQ-83" is "фики 83"; Seregin's "Фики весь 12" — **unclear**. The notes' "RK3576" is "р к 35, 76" (heard); the closed task "р к 35 XX 61" — **unclear**. The notes' "the machine statistics export" is "Экспорт статистики по машинам war celine" (heard). The notes' "changes requested by Sergey for the other side" is "по лапу делал изменения… Это же Сергей просил запрос" — which Sergey asked and what "лапу" is are **unclear**. The notes' "fixed the overlay in autospins" is "оверлей в авто спинах калиочи" — Calle Ocho (heard "калиочи"). Ivan's "Я сам с дотой занимаюсь" (heard; possibly Dakota — **inference**).
- **§4 name calls.** "саша" = Biratka; "лёша" = Khamin; "Антон" (documentation, camera security) = Leshkevich; "Антон" (FIQ-83) = Seregin (he answers); "дима" (statistics export) = Chudinov (he answers); "Данил" = Daniil Stauskiy; "жжение" / "Женя" = Kharetski (he answers); "Сергей" = Tsymanov; "Владимир" = Samusenko; "Игорь" = Metelski; "Паша" = Pavel. "Андреем" (the MVP meeting, Biratka) — Klimovich by the MVP context (**inference**); "с Андреем… секьюрити с кэмерой" (Leshkevich) — which Andrei is **unclear**, left unresolved. "Майкла с ефимом" (Igor's Nebraska requests) = [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] and [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] by the game-design context. "Алексеев там специалист" (Khamin, on the SD card) — [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] by the board/hardware context (**inference**).
- **Garbles kept as heard.** "сайром" / "рисайтлера" = recycler; "билбалидатора" = bill validator; "аккумулятор" / "амулятор" = emulator; "со с т г" = STG; "касттон шейдерса" = custom shaders; "межликвесты" = merge requests; "lbay" = Flex-Pay (the notes' reading); "MP 2" = MVP 2; "лтая задачей" = the LTE task; "создате" — **unclear** (the printer problem).
- **Skipped as chatter.** The opening; the order of speakers; the goodbyes.
- **Not recorded:** none; no personal passage in either file.
- **§15.8:** clear. **§15 #9:** clear — the numbers are task, test and machine numbers.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
