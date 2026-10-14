---
type: decision
title: Igor keeps the port autotests going and, in parallel, learns to convert Dragon Pays from horizontal to vertical and back (Oct 5 2026)
date: 2026-10-05
aliases: [horizontal to vertical in parallel, горизонтальные в вертикальные, вертикальные в горизонтальные, Val's relative dependency, относительная зависимость, Pavel scale and stack, scale each screen and stack, Irina fit symbols into vertical cells, templates per format, 5x3 horizontal and vertical template, two resource sets in the game repository, pay table templates, million templates, transitions are themed, lantern transition, Secret Rodeo Spins transition]
source-count: 2
status: active
open-commitments: 1
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

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — experiment with converting Dragon Pays from horizontal to vertical and back, using the existing vertical template, in parallel with the autotests — due Thu Oct 8 2026 review (progress) — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

## Open questions

- Is there an exact mathematical dependency between the horizontal and vertical layouts? Val is sure there is one; Igor and Pavel doubt a simple transform works — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- How many pay-table templates are needed, and does a clone game share its original's template? — [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026.md]]
