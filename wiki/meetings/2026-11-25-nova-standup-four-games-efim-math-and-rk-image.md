---
type: meeting
title: NOVA stand-up — MVP 1 needs a game to prove the framework; Igor's four Georgia games run but are unchecked and wait on Efim's match-3 progressive maths (old maths not yet moved to his project); one game, one merge into the integration branch; the game icon moves into each game repository; all services build for ARM and Pavel wants an RK image with LGS only; Kharetski would put all current maths into the image, and labs are the question; the studio stays single-user with fixed steps (parallel templates later, before about Jan 15); the curve effect editor waits; the brief must describe the help screens because the GDD will be generated from it (Nov 25 2026, 6:19 AM)
date: 2026-11-25
aliases: [Nova standup meeting Nov 25 2026, Nova Standup Four Games Efim Math and RK Image, Nov 25 NOVA stand-up, NOVA standup Nov 25]
source-count: 2
open-commitments: 0
open-questions: 0
---

# NOVA stand-up — four games, Efim's maths and the RK image (Nov 25 2026, 6:19 AM)

**Date/time:** Wednesday November 25 2026, **6:19 AM Eastern**, 32 minutes 52 seconds, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Nova_Standup_Four_Games_Efim_Math_and_RK_Image-November-25-2026.md]] [[raw/Meeting_Notes_Nova_Standup_Four_Games_Efim_Math_and_RK_Image-November-25-2026.md]]. Teams title: "Nova standup meeting". **Language: Russian.** The day after the [[wiki/meetings/2026-11-24-nova-standup-bonus-step-templates-and-lgs-statistics-database.md|Nov-24 NOVA stand-up]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/anton-leshkevich.md|Anton Leshkevich]]. Val was not present.

**Purpose:** the NOVA team's daily status.

## Where the substance lives

- [[wiki/decisions/2026-11-25-one-game-one-merge-into-the-nova-integration-branch-the-studio-stays-single-user-with-fixed-steps-for-now-and-the-brief-must-describe-the-help-screens.md]] — MVP 1 and the game, Efim's maths, one game one merge, the select screen, the engine, RAGE into LGS, ARM and the RK image, the maths set, the studio, effects, help screens; all commitments and questions.
- Earlier rulings with Nov-25 notes: [[wiki/decisions/2026-11-24-the-studio-bonus-step-is-built-from-templates-now-general-resource-and-scene-steps-come-later-and-lgs-is-to-collect-statistics-into-a-database-on-the-machine-checked-against-gli-11.md]] · [[wiki/decisions/2026-11-23-nova-is-the-one-name-ip-481-is-the-root-initiative-owned-by-biratka-one-weekly-mvp-spans-hardware-system-and-studio-and-maths-and-sound-go-into-the-brief-agent.md]]
- Topics: [[wiki/topics/nova-platform-architecture.md]] (Nov 25)
- People (all Nov 25): [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/daniil-stauskiy.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/efim-podvoiski.md]] (in absentia) · [[wiki/people/andrey-bosik.md]] (in absentia)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Nova_Standup", "November-25-2026" and "2026-11-25" found no page citing either file; the same morning's 3:46 AM Minsk stand-up is a different recording ([[wiki/meetings/2026-11-25-daily-standup-bep-cleanup-and-port-update-requirements.md]]).
- **Speaker doubt.** The RAGE-into-LGS report (12:34–13:35) carries the label "Alexander Biratko", but it came right after Pavel called on "женя", whose audio failed, and it matches Kharetski's Nov-23 LGS catch-up; the notes also flag it. Kept under the label, marked **unclear**.
- **§4 name calls.** "Саша" = Biratka; "Игорь" = Metelski; "Женя" / "Джонни" = Kharetski; "Антон" = Leshkevich; "Даниил" / "Данила" = Daniil Stauskiy; "ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]; "ира" = Irina; "Андрей" who created the game repositories = [[wiki/people/andrey-bosik.md|Andrey Bosik]] (**inference**).
- **Garbles kept as heard.** "Обилите" / "копбилити" / "побилити" = capability; "fenbork" / "фолемгорте" = framework; "MB один" / "MBP один" / "VP один" = MVP 1; "джип прогрессии" / "фила прогрессива" — two progression types, **unclear**; "окрестности карнавала" / "к лесни карнавал" — a Carnival game (**inference**); "мачт 3 прогрессив" / "смач 3 прогрессивом" = match-3 progressive; "прицепам" / "присет" = preset; "дидпроект нарасти" — Efim's project, **unclear** (perhaps a Rust project); "масс сервер" / "мат сервис" = maths server; "пешком" — a package (**inference**); "новыми грейшен" = new integration (**inference**); "donpays" / "драгон пейс" = Dragon Pays; "день селекшн скрин" / "селек с кринтом" = game select screen; "ликвид глаз" / "levid глаз" = liquid glass; "Этап 228" — **unclear**; "в 00:04" — Daniil's closed feature number, **unclear**; "Долгая 1353" = item 1353 (notes); "дотацентра" = data centre; "сошкам" / "сошку" = ISO (**inference**); "гетхапейдж" = GitHub page; "подаром" / "arm" = ARM; "цитатап" = setup (notes); "вбилдер" = builder; "пейджер" = page; "калиоча" = Calle Ocho (**inference**); "спаян" / "спайнах" = Spine; "хелп стен" / "хлпа" / "хпа" = help screens; "г д" / "г д д" = GDD; "аллу как для лува" = Lua (**inference**); "Татьяна спрашивает" = "агент спрашивает" (**inference**).
- **Skipped as chatter.** Camera trouble, "Гинукс не рулит", "Собака", the joke about Efim, the goodbye.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Nova_Standup_Four_Games_Efim_Math_and_RK_Image-November-25-2026.md]]
- [[raw/Meeting_Notes_Nova_Standup_Four_Games_Efim_Math_and_RK_Image-November-25-2026.md]]
