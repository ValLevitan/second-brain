---
type: decision
title: Igor keeps the port autotests going and, in parallel, learns to convert Dragon Pays from horizontal to vertical and back (Oct 5 2026)
date: 2026-10-05
aliases: [horizontal to vertical in parallel, vertical Dragon Pays Oct 8, stretched symbols, символы растянулись, задание не достигнуто, no-distortion fit, горизонтальные в вертикальные, вертикальные в горизонтальные, Val's relative dependency, относительная зависимость, Pavel scale and stack, scale each screen and stack, Irina fit symbols into vertical cells, templates per format, 5x3 horizontal and vertical template, two resource sets in the game repository, pay table templates, million templates, transitions are themed, lantern transition, Secret Rodeo Spins transition]
source-count: 6
status: active
open-commitments: 0
open-questions: 2
---

# Igor keeps the port autotests going and, in parallel, learns to convert Dragon Pays from horizontal to vertical and back

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-05-rage-nova-port-autotests-and-horizontal-to-vertical-layout.md|Oct 5 2026, 7:01 AM review]] (Russian), after a long debate he started himself. It follows the same-format approval on [[wiki/decisions/2026-10-05-geometry-first-port-autotests-accepted-and-geometry-checks-named-graphic-contracts.md]] [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Val's belief

Horizontal-to-horizontal and vertical-to-vertical raise no questions for him. What stays with him is the relative dependency of elements between a horizontal and a vertical game: "то, что есть зависимость, у меня нет сомнения. Можем ли мы? Я не знаю." If an exact dependency exists, then "в теории" games could be converted either way. He does not ask to stretch two horizontal screens into one vertical screen; he asks to keep the proportions between elements [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## The positions

- **Pavel — scale and stack.** Scale each horizontal screen down by some factor ("в полтора раза… один и 6 или там один и 4", not fixed), keep the proportions, put the main field at the bottom of the vertical screen above the dashboard and the pay-table screen above it. About a third of the screen stays free (Igor: more than a third, "мы это считали"). Fit the reels edge to edge to give the player the most room [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Igor — tried, too small.** When they tried this before, the reels and symbols came out "очень маленькие", "чтото не очень красиво". He showed Spicy Fruits with two screens joined and a large empty area on top. He also gave a touch-screen example: a bonus with plates to pick, where a stretched layout would make the top plate hard to reach [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Irina — fit the symbols, not the field.** Keep 3×5 as 3×5 and fit each symbol from the horizontal game into the vertical cells. Pavel: that needs a template for the game [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **Igor — fixed templates per format.** "более правильный подход это просто иметь конкретный шаблоны": for example a 5×3 horizontal and a 5×3 vertical template, and a move from one template to the other. The game's repository would hold shared resources plus two sets, horizontal and vertical [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## Transitions do not fit strict maths

Igor: games differ by theme. Dragon Pays has a Chinese hanging lantern that drives its transition; another game would dissolve differently. Forcing all of it into strict mathematical frames would make every game look like a copy of one game. Irina: a transition lasts 4 seconds in every game; only the start of the dissolve differs. Igor: in Secret Rodeo Spins the transition is split across two scenes, and a bonus can be entered directly or through a pick feature, with two transitions of different timing [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

He added a technical point: free-spin reels start before the transition ends, and one free spin may wait for the transition-end event before the reels slow down; when that rule was once broken, bugs followed [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

His view: the team spends too much attention on element positions; designers "двигают не так активно совсем" [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].

## The pay-table templates (again)

Pavel: designers place the pay-table elements differently in each game. Igor: tell designers to work inside a template. Irina: as with 3×3 and 3×5 fields, pay tables can have templates by symbol count. Igor: "у нас будет миллион этих шаблонов". Irina: no, because the number of symbols is limited. Pavel asked whether a clone game gets the same template. Igor then said one template or two is "неважно" — the point is that designers stay inside a template [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]. This is the same pay-table question left open on [[wiki/decisions/2026-09-17-hard-geometry-from-the-scene-files-and-a-vertical-skeleton-per-game-format.md|Sept 17]].

## What Val decided

- **Do not stop the autotests.** "Я бы хотел бы закончить автотесты… Я не хочу вас останавливать в этом." [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- **Add a second task:** "Быстро научиться переводить горизонтальные игры в вертикальные или вертикальные в горизонтальные." [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- **On Dragon Pays.** Igor: "я могу использовать тот же самый драганпэйс дальше для экспериментов." Val agreed [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **A vertical template exists.** Val asked for a vertical template like the one Igor made; Igor: "У нас есть, мы его подготовили уже" in earlier months [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]].
- **In parallel.** At the close Val asked Igor to try to build "какуюто логическую зависимость" for moving horizontal views to vertical and back; Igor: "это можно сделать параллельно… независимой работы." Val: "Да." [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

## Relation to earlier rulings

- **Sept 20** set the order: standards into GitHub, then end-to-end tests, then a timed horizontal-Rage-to-vertical-NOVA conversion — [[wiki/decisions/2026-09-20-the-vertical-geometry-standard-glossary-and-adrs-go-to-github-outside-any-framework.md]]. Oct 5 runs horizontal↔vertical work **in parallel** with the tests, not after them. Evolution, not contradiction. Whether this replaces the timed conversion is not stated.
- **Sept 14** found that existing horizontal art cannot simply become vertical art — [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]]. Igor's "too small" answer to Pavel repeats that finding.

## Update, Oct 8 2026 — a working vertical Dragon Pays with stretched symbols; Val: the task is not reached

At the [[wiki/meetings/2026-10-08-rage-nova-dragon-pays-vertical-port-and-symbol-distortion.md|Oct 8 7:04 AM review]] (Russian) Igor showed the first result [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]:

- **What he built.** He measured the 5×3 game screen (five reels of three symbols), generated a vertical scene with the same geometry (reel frame, logo, accent video, pay table, dashboard, jackpot meters) and plugged it into his existing horizontal port. It is fully working: base game, messages, the transition into free spins and the free spins. The game holds both configurations at once; one parameter switches back to the horizontal version with its own resources.
- **The defect.** In horizontal Dragon Pays the symbols are wider than tall. With the geometry he chose, they came out slightly taller than wide — "Соответственно символы растянулись."
- **The second option.** Keep the symbols undistorted and fit the reel frame to them; then the rest of the screen must be filled. The reel frame stretches easily (plain lines, a plain background); he cut it from the existing video and had Claude fit it — "простейшая математика это линейное преобразование". To fill the gaps he extended the art (sky, a tree, matching lanterns) and generated the strip under the pay table.
- **His verdict.** Horizontal art in its current form "плохо, подходит под прямую конвертацию": the result looks like a game, but "вряд ли бы мы поставили… на машины и комуто… продали". Dragon Pays was a lucky case because its top-screen video helped.

**Val's challenge.** Everything else presented was a proposal for building games from the start, and he asked whether the team had drifted from the task. He agreed with the proposal (see [[wiki/decisions/2026-10-08-game-scenes-are-assembled-by-developers-with-claude-from-designer-resources-not-by-designers.md]]), but: "Да, если вернуться к этому заданию? То оно не достигнуто. Потому что у нас получается искажение, визуальное искажение при переводе символов." He asked whether a mathematical fit could avoid it — "это же математическая конвертация" [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

**The next try.** Igor: the symbol art has slack — the round shapes are really slightly flattened ovals — so Claude can be asked to "максимально заполнить площадь, при этом не допустив существенное искажение пропорций элементов". About half an hour for art only; longer with video. He would not promise a good-looking result. Val: "Давайте… попробуем." If it works, Val said, two comps are not needed and conversion can be done on the fly. Val then moved the AI-PM meeting and set a meeting with Igor "через 02:00" to see the result [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

**Kharetski — predictable and approved.** The pay-table descriptions "режет глаз" to him. Conversion must be predictable and approved by the people who own the games — "Майкл Лена" — or [[wiki/people/michael-gottlieb.md|Michael]] may later reject it. For existing games, a designer should draw a vertical comp from the existing horizontal art; for new games, universal resources and two comps. Pavel liked the variant Igor showed with the items in two rows ("в 2 ряда"; the notes read it as the meters). Val: the new style on vertical screens keeps the pay table to thin strips and gives more room to the main character. Igor: every game has a clean topper, a good source for main-character art [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

The notes record the same: the original task "is not yet achieved; Igor tries a no-distortion fit before the team decides more" [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

**On the open questions below.** Val still holds that a mathematical fit should work; Igor's no-distortion try tests it. At 7:04 AM the question stayed open. The follow-up session the same day (10:02 AM) is recorded below.


## Update, Oct 8 2026 (10:02 AM) — the retry works; Val accepts a 20% stretch and the Texas games follow

At the [[wiki/meetings/2026-10-08-dragon-pays-vertical-accepted-and-dutch-mill-port-plan.md|10:02 AM follow-up]] (Russian) Igor showed the retry. He did not remove the distortion; he matched it. The horizontal version already approved for production had symbols about 20% wider than tall, so he made the vertical symbols about 20% taller than wide (the 7:04 AM version was 40%). He first tried square symbols, but the reel frame came out too small. It took "ровно полтора часа", with 40 minutes of that for two generated videos. Pavel: "Выглядит значительно лучше." Val: "всё получилось." [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

The task this page set is therefore done for Dragon Pays, and the method now drives the Texas plan: [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]]. The notes record the same: "Igor's 20% vertical stretch is acceptable" [[raw/Meeting_Notes_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

The pay-table layout question stays open. The only new point: the gap between the logo and the pay table is kept for bonus descriptions, as in the new vertical games [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]].

## Open commitments

- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — experiment with converting Dragon Pays from horizontal to vertical and back, using the existing vertical template, in parallel with the autotests — due Thu Oct 8 2026 review (progress) — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] — **discharged Oct 8 2026:** he showed a working vertical Dragon Pays (with stretched symbols) at the review [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- [x] [[wiki/people/igor-metelski.md|Igor Metelski]] — ask Claude to fit Dragon Pays to vertical, filling the most area without significant symbol distortion (art first; video takes longer) — due Oct 8 2026 (follow-up "через 02:00") — [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]] — **discharged Oct 8 2026, 10:02 AM:** he showed a new vertical Dragon Pays with the symbols about 20% taller than wide (the same 20% the approved horizontal version has sideways, down from 40%); Pavel and Val accepted it [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]

## Open questions

- ~~Is there an exact mathematical dependency between the horizontal and vertical layouts? Val is sure there is one; Igor and Pavel doubt a simple transform works — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] (Oct 8: Val asked again for a mathematical fit; Igor's no-distortion try is the test — [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]])~~ **Answered in practice, Oct 8 2026 (10:02 AM):** a simple rule worked well enough — reel frame across the full screen width, frame height three symbols, symbols about 20% taller than wide — and Val and Pavel accepted the result. It is an accepted distortion, not a distortion-free transform [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- How many pay-table templates are needed, and does a clone game share its original's template? — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- How should the pay table be laid out in the vertical version? Kharetski finds the converted pay table wrong; Pavel likes the two-row variant — [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
- [[raw/Meeting_Notes_Dragon_Pays_Vertical_Accepted_and_Dutch_Mill_Port_Plan-October-8-2026.md]]
