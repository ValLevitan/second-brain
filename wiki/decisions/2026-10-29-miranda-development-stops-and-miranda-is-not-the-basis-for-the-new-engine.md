---
type: decision
title: Miranda development stops — Val sees no future in it, and the team (with Sasha, as reported by Irina) agrees it has outlived itself; earlier the same morning Miranda was ruled out as the basis for the new engine, being "only a converter" (Val, Oct 29 2026)
date: 2026-10-29
aliases: [stop Miranda development, Miranda development stopped, девелопмент Миранда, я не вижу будущего в миранде, Miranda has outlived itself, это себя изжило, Miranda is only a converter, Миранда нужна чисто для конвертации, Miranda not the basis for the engine, я бы миранду не брал за основу]
source-count: 4
status: active
open-commitments: 0
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

## How it sits against earlier rulings

- **May 2025.** Val and Aaron asked whether Unity could replace Miranda; no ruling then — [[wiki/topics/miranda-authoring-tool.md]] (May 1 and May 6 2025).
- **Oct 21 2026.** When NOVA dropped the browser, Val said "мы все равно хотим отказаться от миранты" and called Unity-Miranda "утопия" — [[wiki/decisions/2026-10-21-nova-drops-the-browser-for-a-native-engine-no-code-before-capabilities-and-mvp1-is-a-stable-nova-releasing-six-texas-games.md]]. Oct 29 turns that wish into a stop.
- **Oct 28 2026.** The designers agreed the current formats from Miranda will do for now in the new engine — same page (Oct-28 note). Nothing on Oct 29 says the Miranda export formats are dropped; only development stops and Miranda is not the engine's basis (**inference** — the two are not linked in the meeting).

## Open questions

- What happens to the Miranda developers' current work and to the Miranda repository? Not discussed — [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]
- [[raw/Meeting_Notes_Engine_Meeting_Postponed_and_Miranda_Development_Stopped-October-29-2026.md]]
- [[raw/Meeting_Transcript_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
- [[raw/Meeting_Notes_AI_Game_Design_Assistant_and_Second_Brain_Knowledge_Base-October-29-2026.md]]
