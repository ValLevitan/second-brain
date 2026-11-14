---
type: meeting
title: NOVA-2 follow-up — code now in the company GitHub; Anton asks where game mechanics should live (compiled core, scripts or games) for certification, and Val leaves it open; Igor's scene flow is ported to the engine and the room agrees one tool, not two; the AI model is a replaceable setting; Kharetski's design agent opens a repository ticket; a Tuesday demo from brief toward a game with free spins; Val's no-designers picture and the metrics question for NOVA and Galaxy (Nov 11 2026, 7:31–8:32 AM)
date: 2026-11-11
aliases: [NOVA-2 follow-up - agile plan check, NOVA-2 Mechanics Placement One Studio Tool and Game Metrics, Nov 11 NOVA 2 meeting, Wednesday NOVA 2 follow-up, NOVA 2 at 7:30]
source-count: 2
open-commitments: 0
open-questions: 0
---

# NOVA-2 follow-up — mechanics placement, one studio tool, game metrics (Nov 11 2026, 7:31 AM)

**Date/time:** Wednesday November 11 2026, **7:31 – 8:32 AM Eastern**, about 61 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]] [[raw/Meeting_Notes_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]. Teams title: "NOVA-2 follow-up - agile plan check". **Language: Russian.** This is the "Wednesday morning" meeting set at the [[wiki/meetings/2026-11-06-nova2-studio-engine-demo-and-agile-merge-plan.md|Nov-6 merge meeting]], and the "7:30" NOVA 2 meeting Val named at the [[wiki/meetings/2026-11-11-trial-game-review-aristocrat-mechanic-not-built-on-rage.md|6:37 AM trial-game review]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (host), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]].

**Purpose:** each NOVA 2 owner reports since Nov 6 and the group agrees the next step [[raw/Meeting_Notes_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-11-nova-2-gets-one-tool-from-brief-to-game-igors-scene-flow-goes-into-the-studio-the-ai-model-is-a-replaceable-setting-a-tuesday-demo-and-where-mechanics-live-stays-open.md]] — the work status; one tool, not two; the replaceable model; the Tuesday demo; maths for the agent and the template repository; the mechanics-placement question left open with Val's view; agent standards; Val's no-designers picture and the metrics question; all commitments and questions.
- [[wiki/decisions/2026-11-06-rage-is-finished-nova-2-is-antons-rust-engine-with-lua-scripted-framework-and-games-lgs-stays-miranda-and-unity-are-not-needed-code-first-then-prose-no-browser-runtime-and-all-work-moves-to-corporate-repositories.md]] (Nov-11 7:31 AM note) — Nov-6 commitments discharged or carried.
- [[wiki/decisions/2026-11-10-the-online-creator-platform-is-not-pursued-and-jvl-aims-at-a-loop-from-player-data-on-the-machine-to-new-games-sent-straight-to-it.md]] (Nov-11 note) — Val gives the loop to the whole group; first metric ideas.
- Topics / projects: [[wiki/topics/nova-platform-architecture.md]] (Nov 11, 7:31 AM) · [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Nov 11)
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/efim-podvoiski.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] (all Nov 11, 7:31 AM)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Mechanics_Placement", "agile plan check" and "7:31" found no page citing either file. The same morning's 6:17 AM stand-up, 6:37 AM trial-game review and 8:31 AM MVP 1 release meeting are different sessions with their own stubs ([[wiki/meetings/2026-11-11-mvp1-release-procedure-release-notes-and-product-sign-off.md]]).
- **Notes vs transcript.** The notes' Tuesday "(Nov 17)" is "на вторник" on the transcript. The notes have Anton, Efim, Alexander and Andrei for one tool; the transcript also has Irina's "Еще должно быть 2 Тула", so the room was not unanimous at first. The notes' "Opus" is "опусом 5 и 5" (heard). The notes' "about $20+" is "от $20 и выше". The notes' "modem" is "модам" / "моду" (heard). The notes' metrics talk "after the meeting" is after Val's goodbye, with Efim and Pavel still on.
- **§4 name calls.** "Антон" = Leshkevich (he presents); "Игорь" = Metelski; "Ефим" / "ефима" = Podvoiski; "Саша" (Efim, to Biratka) = [[wiki/people/alexander-biratka.md|Alexander Biratka]]; "Андрей" with the service ticket and the repositories = Bosik; "Евгений" / "женя" / "жене агент" = [[wiki/people/evgeny-kharetski.md|Kharetski]] (he answers); "Паша" = Pavel; "Ирина" = Shishko. "Геннадий" inside Anton's example flow ("фрама Геннадий один" — heard) is **unclear**, not read as a person. "Игорь" in Efim's popularity example ("Сравнительная популярность Игорь") is a slip, **unclear**. "Алена" (Anton, one word) — **unclear**, chatter.
- **Garbles kept as heard.** "гитхад" / "гетхана" = GitHub; "расти" = Rust; "холденриспин" / "холден спин" = hold and spin; "ло" = Lua; "рейджа" / "редже" = Rage; "нового 2" / "нова 2" / "новадва" = NOVA 2; "жира" = Jira; "хайку" = Haiku; "опен раутер" / "ope" = OpenRouter; "д лельки" / "d lками" / "дрелки" = DLLs; "гкуам 3" = GA-COAM 3; "GVL" = JVL; "при спины" = free spins; "андретейнг" / "андрейкин" = undertaking; "сам чек" = checksum; "модам" / "моду" = modem (per the notes); "джорджи" = Georgia; "индудент интеллигент" = artificial intelligence (**inference**). **Unclear:** "g viltime", "в 1000", "д л к фай бонус", "agit tuse all therface протокол", "agentind tue", "фрама Геннадий один", "в реку".
- **Skipped as chatter.** The audio checks, Val dropping off and back, the goodbyes, "через жопу" and Kharetski's retort, Efim's question about the previous meeting's transcript.
- **Not recorded:** personal matters not recorded (one marker line in the transcript).
- **§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]
- [[raw/Meeting_Notes_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026.md]]
