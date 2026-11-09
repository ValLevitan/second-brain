---
type: decision
title: Miranda development stops — Val sees no future in it, and the team (with Sasha, as reported by Irina) agrees it has outlived itself; earlier the same morning Miranda was ruled out as the basis for the new engine, being "only a converter" (Val, Oct 29 2026)
date: 2026-10-29
aliases: [stop Miranda development, Miranda development stopped, девелопмент Миранда, я не вижу будущего в миранде, Miranda has outlived itself, это себя изжило, Miranda is only a converter, Миранда нужна чисто для конвертации, Miranda not the basis for the engine, я бы миранду не брал за основу]
source-count: 10
status: active
open-commitments: 1
open-questions: 1
---

# Miranda development stops; Miranda is not the basis for the new engine

Two steps on one day, both in Russian, both with [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]] [[raw/Meeting_Notes_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]. The tool itself: [[wiki/topics/miranda-authoring-tool.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Step 1 — not the basis for the new engine (Oct 29, about 8:12 AM)

At the [[wiki/meetings/2026-10-29-ai-game-design-assistant-review-one-knowledge-base-and-a-full-cycle-test.md|Oct-29 game design agent review]] (6:59 AM), the talk turned to what the new engine must do [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]:

- **Val's starting point.** There are two groups of use cases: what the designers need and what the machine needs. "Дизайнеры для себя сделали как бы оболочку, которая называется Миранда" — so "мы знаем, что дизайнерам нужно от движка" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Kharetski.** "Ну я бы миранду не брал за основу, если честно." A normal engine — Unity, for example — shows the scene, lets you move elements as you like and start a working game from a button; "я думаю, что наша конечная цель такая." Then: "Такмиранда нужна чисто для конвертации игр… это конвертер", and later "Совершенно не нужно" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Bosik.** Miranda was perhaps a good solution at the time, but not the best one today; it is a converter, "возможно, это лишнее звено"; he agrees with Kharetski "полностью на 100%" [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].
- **Val.** "Хорошо выбросили много." [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]] The notes record it as a decision: Miranda is not the basis for the new engine; it is only a converter (Kharetski, Bosik; Val accepted) [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]].

## Step 2 — development stops (Oct 29, about 10:03 AM)

At the [[wiki/meetings/2026-10-29-engine-meeting-postponed-and-miranda-development-stopped.md|short 10:01 AM call]], after the engine meeting was put off, Val asked one more question [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]:

- **Val.** "Девелопмент Миранда я не вижу будущего в миранде, поэтому продолжать девелопмент я никакой не вижу смысла в этом правильно." [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]
- **The team.** Kharetski: "Похоже, что так." Irina: "в общемто мы на этом ещё на прошлом митинге остановились" (which earlier meeting is not named; the 7:00 AM review the same day fits — **inference**). Val asked whether he is supported; Kharetski: "Да" [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]].
- **Sasha.** Igor asked whether to ask Sasha too. Irina: "саша тоже мы уже сегодня спрашивали после этого митинга и Саша также на это смотрел. Что это себя изжило?" — the notes read this as Sasha agreeing that Miranda has outlived itself [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]] [[raw/Meeting_Notes_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]. Sasha is read as [[wiki/people/alexander-biratka.md|Alexander Biratka]], the Omni/Pixi framework engineer who writes the new-engine requirements — **inference** by role; the transcript gives only "Саша".
- **Val.** "Окей, договорились." [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]] The notes: "Stop Miranda development" — decided by Val, supported by Kharetski and Irina [[raw/Meeting_Notes_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]].

## Step 3 — Miranda is to be preserved properly (Oct 29, about 11:03 AM)

At the end of a [[wiki/meetings/2026-10-29-minsk-team-reorganization-and-staffing-review.md|10:32 AM call with Pavel and Irina]] Val said: "Обратите внимание, что миранду нужно правильно законсервировать" — to preserve it there must be correct prose, data contracts, and a correct repository. He had already sent that message to "Андрею и диме" and repeated it to Pavel and Irina "Чтоб не потерять это" [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]. Andrei and Dima here are [[wiki/people/andrew-khandov.md|Andrew Khandov]] and [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]], named by surname earlier in the same passage [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]] [[raw/Meeting_Notes_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]].

## Note, Oct 29 2026 (11:59 AM) — version 1 of the new engine still reads the Miranda assets

At the [[wiki/meetings/2026-10-29-new-game-engine-requirements-and-spikes.md|noon engine meeting]], asked by Val how designers will work with the new engine, Leshkevich: "Для 1 версии мы решили, что мы будем поддерживать его существующие асыты из миранды, то есть их варфлоу не изменится"; an editor comes later [[raw/Meeting_Transcript_New_Game_Engine_Requirements_and_Spikes-October-29-2026.md]] [[raw/Meeting_Notes_New_Game_Engine_Requirements_and_Spikes-October-29-2026.md]]. This fits the Oct-28 note on formats (below): development stops, but the Miranda assets stay usable — [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]].

## How it sits against earlier rulings

- **May 2025.** Val and Aaron asked whether Unity could replace Miranda; no ruling then — [[wiki/topics/miranda-authoring-tool.md]] (May 1 and May 6 2025).
- **Oct 21 2026.** When NOVA dropped the browser, Val said "мы все равно хотим отказаться от миранты" and called Unity-Miranda "утопия" — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]]. Oct 29 turns that wish into a stop.
- **Oct 28 2026.** The designers agreed the current formats from Miranda will do for now in the new engine — same page (Oct-28 note). Nothing on Oct 29 says the Miranda export formats are dropped; only development stops and Miranda is not the engine's basis (**inference** — the two are not linked in the meeting).

## Open commitments

- [ ] Andrew Khandov and Dmitriy Khandov — preserve Miranda properly: correct prose, data contracts, correct repositories (Val says he sent them this message) — due unspecified — [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]] [[raw/Meeting_Notes_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]

## Open questions

- What happens to the Miranda developers' current work and to the Miranda repository? Not discussed — [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]] — *Oct 29 2026 (10:32 AM): the repository part is answered — Miranda is to be preserved with correct prose, data contracts and repositories (Step 3)* — [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Note, Nov 6 2026 (10:33 AM) — "нам Миранда не нужна"; the Miranda-exported scene format stays as the working contract, simplified; the engine reads Miranda assets only because they were at hand

At the [[wiki/meetings/2026-11-06-nova2-studio-engine-demo-and-agile-merge-plan.md|Nov-6 10:33 AM NOVA-2 merge meeting]] (Russian) Val: "то, что я понимаю нам Миранда не нужна" — Biratka: "Нет"; Irina: "Мне нужна" (heard; **unclear** whether in earnest); Efim: "Насчёт Миранда я не знаю" and later "мы очень хотим уйти от миранды. Почему мы хотим от неё?"; Igor: "если ишка может собирать сцены, зачем нам нужно собирать их мирандой?"; Val: "Да и от миранды мы уходим" [[raw/Meeting_Transcript_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]]. Anton's engine "поддерживает асыты, которые были выпущены мирантой" because "это то, что у меня было"; Biratka: keep the Miranda/Pixi-era scene data contract as the working format, simplified, build scenes with AI, "нам юнити сам не нужен уже"; Anton: staying on Rage would mean its scene contracts and "3 d max" for designers — [[wiki/decisions/2026-11-06-rage-is-finished-nova-2-is-antons-rust-engine-with-lua-scripted-framework-and-games-lgs-stays-miranda-and-unity-are-not-needed-code-first-then-prose-no-browser-runtime-and-all-work-moves-to-corporate-repositories.md]] [[raw/Meeting_Transcript_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]] [[raw/Meeting_Notes_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]]. This confirms the Oct-28/Oct-29 reading above: development stopped, the export format survives; the Khandovs' preservation commitment is not mentioned [[raw/Meeting_Transcript_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]].

## Sources

- [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]
- [[raw/Meeting_Notes_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]
- [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- [[raw/Meeting_Transcript_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]
- [[raw/Meeting_Notes_Minsk_Team_Reorganization_and_Staffing_Review-October-29-2026.md]]
- [[raw/Meeting_Transcript_New_Game_Engine_Requirements_and_Spikes-October-29-2026.md]]
- [[raw/Meeting_Notes_New_Game_Engine_Requirements_and_Spikes-October-29-2026.md]]
- [[raw/Meeting_Transcript_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]]
- [[raw/Meeting_Notes_NOVA2_Studio_Engine_Demo_and_Agile_Merge_Plan-November-6-2026.md]]
