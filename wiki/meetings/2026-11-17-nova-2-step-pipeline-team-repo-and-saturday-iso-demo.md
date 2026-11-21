---
type: meeting
title: NOVA-2 follow-up (Tuesday check) — Anton's one-agent builder made Lions Riches badly, so it becomes a step-by-step pipeline with a human check between steps; quality first, cost later; his converter moves to a new team repository and Igor and Kharetski join; Igor ran Twin Bison on NOVA 2 with a local LGS; the ISO installs with maths but no game, so the first ISO with a game is shown Saturday Nov 21; system messages get a standard library; requirements come from prose written from Rage; next an RK3576 build with services; a producer joins Jan 15 (Nov 17 2026, 8:04–9:33 AM)
date: 2026-11-17
aliases: [NOVA-2 follow-up - Tuesday check, NOVA-2 Step Pipeline Team Repo and Saturday ISO Demo, Nov 17 NOVA 2 meeting, Tuesday NOVA 2 follow-up]
source-count: 2
open-commitments: 0
open-questions: 0
---

# NOVA-2 follow-up — step pipeline, team repository and the Saturday ISO demo (Nov 17 2026, 8:04 AM)

**Date/time:** Tuesday November 17 2026, **8:04 – 9:33 AM Eastern**, about 88 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]] [[raw/Meeting_Notes_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]]. Teams title: "NOVA-2 follow-up - Tuesday check". **Language: Russian.** It follows the [[wiki/meetings/2026-11-13-nova-2-agent-converter-demo-and-first-iso-by-tuesday.md|Nov-13 7:01 AM Friday check]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (host), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]].

**Purpose:** the Tuesday check on NOVA 2 — what Anton learned, how to turn his tool into team work, and what the first ISO artifact is [[raw/Meeting_Notes_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-17-the-nova-builder-becomes-a-step-by-step-pipeline-with-human-review-in-a-team-repo-quality-before-cost-first-iso-shown-saturday-rk-build-next.md]] — what Anton learned; quality first; the step pipeline; AI review and style books; the team repository; Twin Bison and the ISO; system messages; languages and builds; requirements from Rage; dates; the plan to March; all commitments and questions.
- [[wiki/decisions/2026-11-13-nova-is-done-only-when-a-ci-built-image-from-the-production-server-runs-on-a-machine-the-first-iso-is-built-tuesday-texas-first-then-georgia-and-the-design-agent-waits.md]] (Nov-17 update) — the Tuesday ISO slips to Saturday; the machine portal.
- [[wiki/decisions/2026-11-11-nova-2-gets-one-tool-from-brief-to-game-igors-scene-flow-goes-into-the-studio-the-ai-model-is-a-replaceable-setting-a-tuesday-demo-and-where-mechanics-live-stays-open.md]] (Nov-17 note) — one tool, now without a central agent.
- Topics: [[wiki/topics/nova-platform-architecture.md]] (Nov 17) · [[wiki/topics/ai-assisted-development.md]] (Nov 17)
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/daniil-stauskiy.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/lena.md]] · [[wiki/people/efim-podvoiski.md]] (all Nov 17)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Step_Pipeline", "Tuesday check" and "Saturday ISO" found no page citing either file. The only other Nov-17 stub is the daily stand-up ([[wiki/meetings/2026-11-17-daily-standup-flex-port-error-codes-and-task-178-to-mvp3.md]]), a different meeting.
- **§4 name calls.** "Антон" = Leshkevich; "Игорь" / "метельский" = Metelski; "женя" / "Евгений" / "корецкий" = Kharetski (the brief agent, the build and services — "корецкий" is a listed garble of his name); "Саша" / "Сашка" / "бератко" = Biratka; "Андрей" (CI, portal) = Bosik; "Паша" = Pavel Frolov; "Ира" = Shishko; "Даниил" = [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]]; "диму чудинного" / "дима чудинов" = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]; "Лена" = [[wiki/people/lena.md|Lena]] (design team); "Ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] (maths); "серёгин" = [[wiki/people/anton-seregin.md|Anton Seregin]] (Val: "как 2 Антона нашего зовут… Он серёгин да"); "Владимир" = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] (inference by context). **Unresolved:** "ваню или лешу" (Bosik). "Жене" here means "Женя" by context.
- **Garbles kept as heard.** "лайф риджес" = Lions Riches; "фаббул" / "фейбл" = Fable (per the notes); "клодсон" = Claude Sonnet; "дипсик" = DeepSeek; "thind bys" / "твинбайс" = Twin Bison (per the notes); "вебсотит" / "вебсокет" = WebSocket; "сошка" / "исошка" / "песо" / "а с о имидж" = ISO; "лджис" / "элджс" / "лжес" = LGS; "фп севен" / "pseven" = FP7; "р к 35 76" = RK3576; "sio bord" = IO board; "malty arch doter contine" = multi-arch Docker container; "юлиции" = Unity; "пикси" = Pixi; "свинья" = SVN; "саксептон" = acceptance (criteria); "калиочи" / "колеочи" = Calle Ocho; "Нгс" — read as the NOVA LGS (inference); "пока из грела" — **unclear**; "москтракта" — **unclear**.
- **Notes vs transcript.** The notes date "Wednesday" as Nov 25 (inference from Val's "неделя 23 начинается до 27"). The notes omit Val's lines on GLI certificates and the legislative requirements in Git (Texas not added, Nebraska in). The notes call the producer "under contract"; the transcript's term is garbled. Irina's "С 6 до 7" next to Val's "с 10 до полудня" is her own clock and is not used.
- **Skipped as chatter.** The opening "лев / лёва" banter, the Lua jokes, Val's "young buffaloes and old men" banter, the money aside about Aristocrat, the farewells.
- **Not recorded:** personal matters not recorded.
- **§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]]
- [[raw/Meeting_Notes_NOVA-2_Step_Pipeline_Team_Repo_and_Saturday_ISO_Demo-November-17-2026.md]]
