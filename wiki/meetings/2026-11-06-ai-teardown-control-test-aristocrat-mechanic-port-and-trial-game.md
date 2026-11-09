---
type: meeting
title: AI teardown review 2 — the control test on JVL's own GA-COAM games: a phone video of the help screens and bonus rounds is enough; Igor ported an Aristocrat bonus from Kharetski's YouTube breakdown into a Rage game in under a day; competitor maths is not needed, JVL fits its own with Efim; a JVL style template; Igor builds a trial game with an Aristocrat mechanic on the wolves, lions and bison graphics; interactivity ideas rejected; Leshkevich's NOVA 2 status email and a merge meeting (Nov 6 2026, 8:00–8:58 AM)
date: 2026-11-06
aliases: [AI teardown review 2, control test on our own GA-COAM V2 games, AI Teardown Control Test Aristocrat Mechanic Port and Trial Game, Nov 6 teardown review, competitor teardown review 2, пробная игра, trial game with an Aristocrat mechanic]
source-count: 2
open-commitments: 0
open-questions: 0
---

# AI teardown review 2 — the control test on JVL's own games (Nov 6 2026)

**Date/time:** Friday November 6 2026, **8:00 – 8:58 AM Eastern**, about 56 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]] [[raw/Meeting_Notes_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]]. Teams title: "AI teardown review 2, control test on our own GA-COAM V2 games" [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]]. **Language: Russian**, with a short garbled English stretch (about 00:40–00:44) while the group read Leshkevich's email. It is the Friday validation test promised on Oct 30 ("next Friday… the 6th") — [[wiki/meetings/2026-10-30-ai-competitor-game-teardown-and-mechanics-library.md|the Oct-30 teardown review]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (host), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]].

**Purpose:** a control test — film JVL's own GA-COAM games as if they were a competitor's machine, with no special access ("никаких доступов специальных… каких-то вики… просто вот видео. И все"), and see whether Claude pulls the mechanics out; then what Igor did with the Oct-30 YouTube breakdown [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]] [[raw/Meeting_Notes_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]]. Val opened: "похоже, что огромное количество работы сделано. Спасибо за клод ссылки" [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-06-phone-video-of-help-screens-and-bonuses-is-enough-for-a-teardown-the-mechanic-is-ported-onto-jvls-own-maths-and-igor-builds-a-trial-game-with-an-aristocrat-mechanic.md]] — the control test's result; Igor's Aristocrat bonus port and how long it took; the maths ruling; the style template; the trial-game assignment and the Wednesday review.
- [[wiki/decisions/2026-11-06-interactivity-features-are-rejected-because-players-play-only-to-win-and-the-machine-must-be-sharp-and-focused-on-the-player-who-wants-to-win.md]] — Bosik's camera-tracking character and modem announcements; Val's "50 years… Zynga" answer.
- [[wiki/decisions/2026-10-30-competitor-games-are-studied-for-new-mechanics-not-maths-only-in-jvls-markets-and-the-video-method-is-first-proved-on-jvls-own-games.md]] (Nov-6 update) — the Nov-6 validation commitment discharged; Val's capture file narrowed to a phone instruction.
- [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Nov-6 8:00 AM note) — Leshkevich's NOVA 2 status email read out: a designer studio integrated with Jira on his own engine, 12 capabilities and 60 requirements; how Igor's work would plug in; the merge meeting with Anton.
- [[wiki/decisions/2026-10-24-code-not-confluence-is-the-source-of-truth-and-claude-builds-a-wiki-per-old-game-from-the-svn-code.md]] (Nov-6 update) — Igor has templated 15 GCM3 games.
- Topics: [[wiki/topics/slot-game-design-principles.md]] (Nov 6) · [[wiki/topics/game-art-animation-production-pipeline.md]] (Nov 6)
- People: [[wiki/people/evgeny-kharetski.md]] (Nov 6, 8:00 AM) · [[wiki/people/igor-metelski.md]] (Nov 6, 8:00 AM) · [[wiki/people/val-levitan.md]] (Nov 6, 8:00 AM) · [[wiki/people/pavel.md]] (Nov 6, 8:00 AM) · [[wiki/people/irina-shishko.md]] (Nov 6, 8:00 AM) · [[wiki/people/andrey-bosik.md]] (Nov 6, 8:00 AM) · in absentia: [[wiki/people/anton-leshkevich.md]] · [[wiki/people/efim-podvoiski.md]] · [[wiki/people/lena.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "AI_Teardown_Control_Test", "November 6, 2026, 8:00" and "8:00 – 8:58" found no page citing either file. The same morning's 9:03 AM remote-update review and the 6:15 AM Minsk stand-up are different sessions with their own stubs; the stand-up's "3 артефакта к митингу" line is Kharetski's preview of this meeting.
- **Notes vs transcript.** The notes read "five to seven short videos"; the transcript has "57 видео по пару минут" (heard) — recorded as unclear. The notes name the mechanic "progressive persistence"; the transcript has "S pressift porscistens" and "просив presestands" (heard) — the wiki reads it as "perceived persistence", the Aristocrat idea Val embraced on Oct 30, as an **inference**. The notes give Nov 11 as the due date for Igor's two undertakings; the transcript says only "во вторник или среда… на среду… в 07:00" (Nov 11 2026 is that Wednesday). The notes read "(Juan)" for the lost product owner; that line is not on this transcript at all (it is on the 9:03 AM meeting).
- **§4 name calls.** "Женя" on the YouTube breakdown = [[wiki/people/evgeny-kharetski.md|Kharetski]] (he is in the room); "Ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]; "Лена" / "Майкла и Елены" = [[wiki/people/lena.md|Lena Zhukova]] and [[wiki/people/michael-gottlieb.md|Michael Gottlieb]]; "Антон" / "Антона ишкевича" on NOVA 2 and the studio = [[wiki/people/anton-leshkevich.md|Anton Leshkevich]]; "пиратка" (to be invited) = [[wiki/people/alexander-biratka.md|Alexander Biratka]]; "Дэвид" (Pavel: "Дэвид бы сказал, что… ему нравится играть") — which David is **unclear**, left unresolved.
- **Garbles kept as heard.** "Тимберль" / "тимберленд вульфе" = Aristocrat's Timber Wolf (as on Oct 30); "лайтен бондар" = Light & Wonder; "рейд" / "рейж" / "red shigra" = Rage; "г к вам 3" = GCM3; "над" (the coin-pick bonus product) — read as NAD (**inference**); "Джорджия кло" — **unclear** (the three latest Georgia games); "парашинс" / "паршиц" = par sheets; "наш татив" = штатив (tripod); "зинга" = Zynga; "каб 299" / "кап 299" — heard; "фреймворксон геймс лау" = "framework on games Lua" (the notes' reading); "230" (the merge meeting's time) — **unclear**, the transcript then says "Через полтора часа".
- **Transcript artifact.** From about 00:11 to 00:16 the "Evgeny Kharetski" label echoes Igor Metelski's sentences in garbled form (the same crosstalk artifact as on Oct 30). Those lines are read as Igor's words.
- **Skipped as chatter.** Greetings; Val's "как для пятиклассника" and the jokes about shocking Efim; the English fragments while reading the email; goodbyes.
- **Not recorded:** personal matters not recorded (one short passage of Bosik's reported to the parent; nothing recorded here).
- **§15.8:** clear — the dollar figures are market history and play examples. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]]
- [[raw/Meeting_Notes_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026.md]]
