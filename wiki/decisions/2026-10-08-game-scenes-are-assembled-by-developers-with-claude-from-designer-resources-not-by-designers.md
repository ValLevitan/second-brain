---
type: decision
title: Game scenes are assembled by developers with Claude from the designers' resources and comp art, not by the designers in 3ds Max — Val insists, the room agrees; Igor's one-resource-set-for-both-layouts spec (a 1920×2160 master video) is the proposal behind it (Oct 8 2026)
date: 2026-10-08
aliases: [developers assemble scenes with Claude, сцены собирали разработчики, scenes built by Claude, Claude-built scenes, Val insists, я даже настаиваю, designers deliver resources not scenes, one resource set for both layouts, universal resources, универсальный набор ресурсов, master video 1920x2160, мастер видео 1920 на 2160, two Full HD screens stacked, cut a strip and scale to 1080x1920, progressive meters pyramid, two-row meters, pay table one line or top screen, 2 weeks to final comp, 3 months of production, Claude does it in hours]
source-count: 2
status: active
open-commitments: 0
open-questions: 2
---

# Game scenes are assembled by developers with Claude, not by designers

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-08-rage-nova-dragon-pays-vertical-port-and-symbol-distortion.md|Oct 8 2026, 7:04 AM Rage-to-Nova review]] (Russian), on a proposal by [[wiki/people/igor-metelski.md|Igor Metelski]]. [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] and [[wiki/people/pavel.md|Pavel Frolov]] agreed [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Igor's proposal — one resource set for both layouts

Igor described a game screen as separable parts: background, an accent video on the background, the reel frame, the logo, the dashboard and the pay table. These can be delivered separately and combined into one scene. If the team wants one set of resources for both horizontal and vertical games, the resources need firm requirements [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]:

- **Background video.** A master video at "1920 на 2 160, то есть это 2 фулл эйч ди монитора, которые уложены друг над другом". Horizontal: cut it in half for the bottom screen (reels and dashboard) and the top screen (progressives and accent video). Vertical: cut a strip and scale it down to 1080×1920, a portrait Full HD monitor.
- **Transitions.** The same master size. A transition is an accent plus an alpha channel that fades; the designers' only extra rule is that the accent must fit inside the vertical strip, so it can be cut out without distortion.
- **Reel frame and dashboard.** A fixed set of layouts with a set reel-frame position for each format. The dashboard is already more or less standard.
- **Pay table.** Below some number of symbols, one line above the reels; above it, the whole top screen (or the top half of a vertical screen).
- **Progressive meters.** One to three levels: a strip at the top. Four levels: a two-row "пирамидка", as already done in some games ("в фил игр… в играх с фалислинг прогрессиум" — which games is **unclear**). More than four: a column on the top screen (or top half), the accent video is removed and the logo moves up — as in the "джекпотраш" games (as spoken; title not verified).
- **Messages, help and win animations** simply cover the reel frame.

"мы всегда работаем с одним набором ресурсов… только по разному их распределяем по экрану" [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

**Where the master lives.** Pavel: so the video is cut at build time and the vertical build stores the cut resource. Igor: the source materials should also sit in the game's repository, so a new monitor layout never needs anyone else. Pavel: cropping a video is not serious work, even with a script (for example trimming 100 or 200 pixels from each side). Igor: Claude scripts whatever can be scripted [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

**Who assembles scenes.** Igor: today designers make the resources and then assemble the finished scenes — in 3ds Max, setting layers, cameras, then rendering. "возможно было бы удобнее, если бы сцены собирали разработчики"; Claude's scripts seem faster. The scene contract would then follow from the code, with no loop of finding defects in a delivered scene, telling the designers and waiting for a new export. Pavel: designers will ask how they can hand over resources without seeing the whole scene. Igor: through the comp art, which designers always make first; the converter places every element where the comp shows it [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

## Val's ruling

Val said he fully agrees and goes further: "я даже настаиваю, чтобы так было сделано, потому что… Скорость Клода превысит любого дизайнера с любой… автоматикой." His reasoning: designers take "может быть 2 недели" from the first discussion to a final comp, and then "3 месяца" to break the game down and do production; Claude, as he understands it, does it "за часы". He said he exaggerates on purpose to show the scale, and that Claude will only get faster. "Поэтому я просто не только поддерживаю это направление, но я настаиваю на этом." [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]

The condition, as Val put it: designers supply resources "в том формате, как вы сделали спецификацию". Igor: "Я думаю да", from his experience with several experiments; video work takes longer [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

Val asked the room. Kharetski: "Да, конечно." Pavel: "Да." Irina: "даже если это пускай будут не часы, а дни это всё равно несоизмеримо." Val also said working with designers is "очень, очень тяжело", which is why anything that can be converted automatically is preferred [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

The notes record the same decision and the same four names [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

## What is saved — Val's challenge

Later Val asked what is actually saved if designers still draw every symbol and resource. Kharetski: the scene assembly step — "сборку сцены с помощью дизайнеров они не будут сцены собирать", which Igor called one of the longest stages. For a new game, universal resources and two comps (one horizontal, one vertical) give two games from one pack of resources. For converting existing games, Kharetski said the saving is "очевидно". Val said scene assembly is a small part of the three months ("Это небольшой"); the question was not settled further [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]].

## What a comp is, as stated in the room

Kharetski: a comp is "просто расстановка элементов на экране" — a static picture that Lena shows Michael, who may ask for elements to be moved; once approved, the scene is built from it. Pavel: "компарт Лена рисует уже исходя из целевой целевого разрешения экранов." After the comp, designers produce symbols, animations and videos (After Effects named by Igor) [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]. This matches the comp-art vocabulary of Apr 2 2026 on [[wiki/topics/game-art-animation-production-pipeline.md]].

## Where it sits

- Sept 14 found that a developer cannot produce a background video; the reel frame and logo are baked into it — [[wiki/topics/game-art-animation-production-pipeline.md]] (Sept 14). Igor's spec keeps those parts separate so they can be placed by code. Evolution, not contradiction.
- Sept 20 already moved toward keeping pieces separate before baking, and liquid glass drawn by code — [[wiki/decisions/2026-09-20-the-vertical-geometry-standard-glossary-and-adrs-go-to-github-outside-any-framework.md]].
- The horizontal-to-vertical work it grew from is [[wiki/decisions/2026-10-05-horizontal-to-vertical-conversion-runs-in-parallel-with-the-port-autotests.md]] (Oct-8 update). Val said the discussion had drifted from that task.

## Open questions

- Who draws and approves a vertical comp for an existing game (Kharetski named Michael and Lena), and must it use only the existing horizontal art? — [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]] [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- How much of the three months does scene assembly really take — Val: "Это небольшой"; Igor and Kharetski: one of the longest stages — [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]

**§15.8:** clear — production method only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Dragon_Pays_Vertical_Port_and_Symbol_Distortion-October-8-2026.md]]
