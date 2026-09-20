---
type: decision
title: Hard geometry comes out of the scene files, and every game format gets a fixed vertical skeleton
date: 2026-09-17
aliases: [vertical skeleton, жёсткий скелет, hard geometry and motion physics, жёсткая геометрия и физика, skeleton per game format, one universal graphic designer, reference layout is another vertical game, за эталон другую вертикальную игру, 3x3 3x5 4x5 skeletons, game scene is a folder]
source-count: 2
status: active
open-commitments: 4
open-questions: 3
---

# Hard geometry comes out of the scene files, and every game format gets a fixed vertical skeleton

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-17-vertical-game-skeletons-and-the-art-pipeline.md|Sept 17 2026 12:19 PM ET session]] (held in **Russian**), after [[wiki/people/igor-metelski.md|Igor Metelski]] demonstrated a playable vertical game built from a video [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] had generated the day before. It is the next move on the thread ruled on Sept 14 — see [[wiki/decisions/2026-09-14-vertical-texas-starts-from-the-georgia-coam-vertical-games.md]] — and it changes *what JVL asks of artists*, not which games are converted.

*(**A note on the quotes.** The source is an unpunctuated Russian speech-to-text transcript. Quotes below are reproduced word-for-word with punctuation and spacing added for readability; every word that is garbled in the source and read differently here is shown **in square brackets**, and anything not recoverable is said to be not recoverable rather than reconstructed. In particular, Val's word for artificial intelligence comes through as "артисты lentelgins", "lentallegent" and "артифицировал" and is bracketed as [AI]; "темплей" is bracketed as [темплейт]; "пэйбл" / "pettaible" as [пэйтейбл]; "релов" as [релы].)*

## What Val ruled

**Stop taking the artist's intent as the input; take the numbers the intent already turned into.** Val's own framing of the problem, in order [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]:

- He first described how he imagined it worked — "художники они же не программируют, они говорят, мне нужно вот это, например, посередине или в левом углу", and then the programmer places it and the artist says a little left, a little right. Igor corrected him: that is not how JVL works, the designer hands over a scene with the components already placed "по авторской задумке".
- Val's point survived the correction and sharpened: the author's intent has already become numbers by then, and the numbers are what he wants. "**Авторская задумка глазом видна, но потом это переходит в … геометрические параметры и в [жёсткую] математику … где находится вот жёсткая геометрия, где она находится.**"
- And flatly, once the game is already built: "**жесткую физику и геометрию артисты задумки до сегодняшний день, когда уже игра сделана, меня не волнует … меня интересует жёсткая геометрия и физика.**"
- His verdict on the hand-waving was blunt and coarse — he called the graphic designers' gesturing worthless, "**просто люди, которые не знают, как объяснить геометрию, механику, текстуру**", and asked only "**как точно ихняя [—] переводится в жёсткую математику**" (the elided word is obscene; the sentence is otherwise verbatim).

**Why he wants it:** with the hard maths in hand he can build a template from it and have AI vary the look — "**когда я знаю жёсткую математику, я могу взять по этой жесткой математике, сделать [темплейт] и потом попросить [AI] задавать разные тоны игры**" — after which the remaining work is routine and can be handed to "**одного нормального универсального график дизайнера одного**", one competent universal graphic designer, working with Anton's and Igor's help and the accumulated groundwork. He asked explicitly what milestone gets them there: "**Какие нужно майлстоун достичь, чтобы всё получилось правильно и потом уже шло … дальше рутина**". [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**Igor said this is not hard.** "**Да без проблем конечно, ну это это очень легко сделать**", and later "**техническим это без проблем сделаем**". The mechanism already exists: the geometry is written in a file inside the scene ("**в сцене написано в файле**"), and JVL's own tooling already contains parsers that read existing geometry out — "**у нас в рамках инструментов написаны парсеры, которые вот эту самую существующую [геометрию] разбирают**". [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**The direction is a reversal of the experiment that produced the demo.** Igor was careful to say the demo ran the other way round — art-first: "**суть эксперимента была в том, что мы отталкиваемся от арта … нам нарисовали, что вот здесь у нас будет рамка [релов] … здесь у нас будет pay table, и я искусственным интеллектом разбираю … арт и по … арту понимаю, что вот сюда мне нужно будет поставить символы.**" Pulling the numbers out of the existing scenes instead is the option he offered in the same breath. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

## The skeleton Val described

A fixed vertical skeleton per game format, plus a library of artifacts, plus geometry and motion physics already known from other games — with **only the screen-size parameters recomputed** [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]:

> "**Потом у нас будет набор разных артефактов. Геометрия вся будет известна, физика движения будет вся известна, потому что мы знаем, как это было сделано в других играх. Единственное, что … сам должен посчитать … параметры при … других размерах экрана.**"

(The words immediately before this — "**у нас этот скелет будет на доос крым скелет на вертикальные**" — are garbled; the intended contrast between two skeleton kinds is **not recoverable** and is not asserted here.)

Inside the skeleton the standard furniture is pinned and cannot move: "**здесь будет прогрессия, здесь будет dash bored, здесь будут кредиты … и они не могут сдвинуться никуда**" — progressive, dashboard, credits. The skeleton is selected by the game's matrix: "**если это 5 на 4, значит жёсткий скелет**". Val's intolerance for the alternative was explicit — a designer saying "**здесь будет немножко зелёненькая, здесь немножко красненько**" is, in his words, what he cannot listen to. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**Igor confirmed the skeleton is buildable:** "**мы можем создать скелет для любого исполнителя дизайнера, куда нам что нужно размещать**" — a skeleton that tells any designer, in-house or outside, where to put what. His only question back was what to measure it against. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

## The reference-layout ruling — this is the part that was actually settled

Igor's blocking question: the game he is converting has no vertical layout of its own — "**вертикальной раскладки для этой игры у нас не было … у нас пока что … нету вот этой вот папки со сценой вертикальной, что мы берём за эталон?**"

**Val's answer, verbatim:** "**Мы … берем за эталон раскладку на другую вертикальную игру.**" — the reference is the layout of **another vertical game JVL already has**, not the game's own horizontal layout. He added that the standard elements are already designed and therefore not worth arguing about — "**У нас есть стандартные элементы … где прогрессив, сколько прогрессив — это уже дизайны сделаны. Какая нам разница?**" [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

This is the same scheme the Sept-14 ruling adopted at product level, now stated as the working rule for an individual conversion.

**Val also named the fork that follows from it** [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]:

- **New game** → go to the artist with the skeleton's questions and demand the answers: "**новая игра, новый сюжет, всё новое. Художник, дай мне набор вот этих вот ответов, вот тебе вопросы, дай мне ответы.**"
- **Game already built** → go to the folders where the answers already sit: "**мы идём в папки, в которых это ответы все лежат … дайте мне ответы, которые у нас уже известны.**"
- **And a third step he wants next:** replace the artist in step one with AI — "**если у нас получается и 1 и 2, тогда я хочу идти на 3 сразу: 3 — я вместо художника говорю … график дизайна, дай мне вот это.**" *(Two words between "говорю" and "график дизайна" — "Эй. Сериал." — are garbled and are not read as anything; whether he named a tool there is not recoverable.)*

## The pushback, which was not resolved

**Pavel Frolov and Irina Shishko both said the pay table defeats a fixed skeleton.** Pavel: "**в каждой игре они просто размещают вот эти вот [пэйтейбл] … они посвоему его делают, оно необязательно от игры к игре повторяется. То есть вот это мы в скелет [засунуть] никак не сможем.**" Irina agreed twice — "**Оно не повторяется как раз.**" [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**Anton Leshkevich's counter-proposal:** a game template in which the animations are replaced by plain grey squares, plus tools that generate content on the fly — "**Игра [темплейт], где вместо анимации будут просто серенькие квадратики, да, и потом предоставить тулы, которые … генерируют на лету**". [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**Pavel's reply folds that back into the same idea and adds a method:** a grey-square template is comp art, and comp art *is* the skeleton — "**это все равно похоже на [компарт] … компарт это по сути то и есть вот этот вот скелет … с положением чего-то**". If the pay-table frames existed in advance and positioned, then "**мы бы … видео сгенерировали, потом на сгенерированное видео просим Клода или … какой-то ИИ наложить на каждый кадр вот эти вот рамки, перегенерировали видео с рамками**" — generate the video first, then ask **Claude** (or some AI) to lay the frames over every frame and regenerate the video with them. He hedged it himself: "**Ну так это работает, наверное.**" [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

Nothing was settled between these positions. Val did not rule on the pay table.

## What Igor committed to

**Vertical skeletons for about six horizontal games, by Monday.** "**… за 6 игр горизонтальных … это игры 3 на 3, там 3 на 5, 4 на 5 … и я просто под эти игры … разберу вот эти вот скелеты, то есть … вертикальная игра: здесь [релы], здесь элементы [пэйтейбла], здесь ещё что-то, что нужно.**" *(The verb is garbled in the source — "вот он осознает за 6 игр горизонтальных" — so the exact phrasing of the undertaking is not recoverable; the object, the count and the formats are.)* Asked how long: "**Пару дней, ну типа завтра, понедельник**" — a couple of days, so Friday Sept 18 or Monday Sept 21. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

*(The derived notes render this as "about six horizontal game **formats**"; the transcript says six horizontal **games**, of the formats 3×3, 3×5 and 4×5 [[raw/Meeting_Notes_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]. The line that follows — "**у нас на все игры для [надо] будут таких 20 лет**" — is garbled past reading and nothing is taken from it.)*

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — build the vertical skeletons for the roughly six horizontal games (3×3, 3×5, 4×5), using another existing vertical game's layout as the reference — due "a couple of days", i.e. Sept 18 or Mon Sept 21 2026 — [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — pull the hard geometry and motion physics out of the existing scene files with the parsers already written, so each artifact is described in numbers — due unspecified — [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — point AI at the game directories and produce the list of scenes across the games with the artifacts each one needs; he said this "**не займёт много времени**" — due unspecified — [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — write to Val on Friday Sept 18 with the day he prefers to meet (Saturday, Sunday or Monday) — due Sept 18 2026 — [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

*(A fifth item the derived notes list as an undertaking — writing the technical requirements for an outside designer, naming the video format, aspect ratio and required resources — is in the transcript only as something that **can** be formulated out of this work, "**можно сформулировать чисто технические требования к … внешнему дизайнеру**". It is recorded here as a possibility, not a commitment [[raw/Meeting_Notes_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]] [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]].)*

## Open questions

- **How does the pay table fit a fixed skeleton?** Pavel and Irina say its layout differs in every game; Anton's grey-square template and Pavel's overlay-the-frames-with-Claude method were both floated and neither was adopted. Val did not rule. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- **Which day do Val and Igor meet — Saturday, Sunday or Monday?** Val flies on Friday and offered Saturday; Igor would rather not work Saturday ("**суббота — день для семьи**"), offered Sunday or Monday, then said "**ну хорошо, давайте в субботу**" anyway; Val refused to choose for him — "**подумайте, напишите мне**" — and added he may be free from the airport on Friday if he gets there early with somewhere to sit. Unresolved at the end of the call. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- **Who fixes the old horizontal scene and the steal scene?** Igor showed that the untouched horizontal scene still breaks — picking something there drops into the steal scene — and said it is outside the question of his own scene. Nobody was assigned. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

## What this decision does not touch

No product, release date, market or cabinet is named for a vertical product anywhere in either source. The standing positions elsewhere in the corpus are untouched: **RAGE is parked with no sunset date**, **NOVA→GLI is unscheduled**, and the **South Dakota VLT-2** question is not raised here. The Sept-14 ruling's own open items — which progressive a vertical Texas product carries, and how big the maths rework is — were not discussed.

**§15.8:** clear — game-engineering, tooling and art-production economics only; no named-person compensation, rate or performance judgement appears in either source, and none is recorded. **§15.9:** no licence, registration, tax or account numbers appear.

## Sources

- [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [[raw/Meeting_Notes_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
