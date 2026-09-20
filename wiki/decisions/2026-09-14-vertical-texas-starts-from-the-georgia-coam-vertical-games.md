---
type: decision
title: A vertical Texas product starts from the vertical Georgia COAM games, not from converting the horizontal Texas games
date: 2026-09-14
aliases: [Texas vertical conversion, horizontal to vertical Texas, Georgia COAM as the Texas base, vertical Texas product, конвертация горизонтального Техаса в вертикальный, Rage-Nova_conversion]
source-count: 2
status: active
open-commitments: 1
open-questions: 4
---

# A vertical Texas product starts from the vertical Georgia COAM games

Taken by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-14-texas-vertical-conversion-and-georgia-game-base.md|Sept 14 2026 6:38 AM ET working session]] (held in **Russian**), after [[wiki/people/igor-metelski.md|Igor Metelski]] demonstrated that the direct route — turning JVL's existing **horizontal** Texas games into vertical ones — breaks on the art. [[wiki/people/pavel.md|Pavel Frolov]] proposed the alternative, Val adopted it, Igor agreed it is the more workable scheme. [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## What was tried, and why it failed

Igor screen-shared real converted scenes in the tool the transcript renders as "сценезитер" (a scene editor). His framing of the geometry [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]:

- A **horizontal machine's main scene is two Full HD monitors** — "основная сцена это 2 фул эйч ди монитора", each "1920 на тысячу 80, то есть ширина 1920, высота 1080".
- A **vertical machine is one Full HD monitor in portrait** — "один фулл эйч ди монитор просто в портретной ориентации", same aspect ratio, "но он перевёрнут в портретную ориентацию".
- To build a vertical scene from horizontal material you must stack two scenes — for a base game the main scene with the reels and the pay-table scene: "нам нужно составить как бы 2 сцены, как бы одну на другой… для базовой игры это, например, мейн сцена, содержащая релы с символами и пэй тэйбл сцена".
- Because both source monitors are the same resolution, stacking them without distorting anything leaves "здоровенный кусок пространства, которые фактически ничем не заполнен" — a huge block of empty space.
- **The size of that block:** Igor first eyeballed it — "нижние 2… по высоте они по 1080 обе. А вот верхняя это 1200 пикселей там где-то так" — then read his own worked figure: "с 1080 1080 это сверху еще **1253**", the amount needed so the three-area composition has the same aspect ratio as the portrait monitor. (He rendered the portrait resolution as "1900 20080" — a garble of 1920 × 1080.) Pavel's aside that the three areas are not equal, "Ну не 3. 3 чуть больше", is in the same exchange.

**Three experiments, all shown live** [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]:

1. **Spicy Fruits** (transcript "спайси фрут" / "спасти фрутс" / "спайси фронт") — fill the empty top with some background. "Получилось плохо" — the logo was stretched and distorted ("растянуло и исказило… вот этот вот логотип"), and the reel area on the lower monitor "будет очень маленькая".
2. **Midnight Money** (transcript "мид нейтмани" / "миднайтмане") — stretch each horizontal monitor to half the vertical screen and join them. "При этом мы получаем искажение пропорций": the abstract background hides it somewhat, but the reel frame is stretched and the symbols must be distorted to fit it — "вся сцена и каждый символ они примерно на **57%** выше, чем… если мы ничего не искажаем".
3. **Dutch Mill** (transcript "дачмил" / "уточ мила" / "сдача милым"), one of the **3×3** games in the Texas product — "у нас в Техасе… в продукте есть игры 3 на 3". In theory the distortion should have mattered less; in practice the art itself breaks, because "нижний экран это какая-то улица, какие-то домики, а верхний экран это какие-то каналы, какие-то домики. Вот и вот на точке стык это всё как бы плавно не свозится" — the two halves do not blend at the join.

**A fourth, "exotic" option Igor raised and rejected himself:** leave the bottom monitor undistorted at Full HD and stretch the top one into the remaining space — "тогда верхний будет искажён по вертикали… больше, чем в 2 раза получается… не очень хороший вариант". [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**His conclusion — the engineering works, the art does not.** Building the scene is not the hard part: "сам процесс создания сцены он… вполне себе возможен и не очень сложный, просто занимает какое-то время" (find the videos, download them — rendered "даунстелить" — and join them), and it is a full scene that runs animations. "Но проблемы тут скорее именно с композицией элементов и в арте", and "с существующим артом эта задача не решим[а]" — with the existing art this task is not solvable. AI does not rescue it either: "тут мы с помощью ии даже уже ничего, наверное, не сделаем… Только экзотические варианты попросить [ИИ] генерировать нам арт… как будто бы такое себе" — i.e. asking AI to generate new art, which he called doubtful. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## The route that was adopted

**Pavel proposed it**, crediting a conversation with Igor the previous day: "Вчера ещё вот мы с Игорем общались, говорили о том, что может быть нам логичнее взять вертикальную игру для джорджии и её конвертировать в вертикальную игру для Техаса. Что это возможно, будет гораздо дешевле." — take a **vertical Georgia game** and convert it into a **vertical Texas game**; it will probably be much cheaper. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**Igor accepted it with one catch.** "Это могло бы быть выходом" — but every Georgia game carries a **symbol-driven progressive**, and the frames for those symbols are baked into the background video: "у нас там во всех играх символ прогрессивы. И рамки под эти символ прогресс[ив] запекли [в] фоновое видео… мне всё равно нужно проводить какие-то операции над фоновым видео." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**And he supplied the fix in the same breath.** The designers still hold the **unbaked scenes** — "у дизайнеров это же не запечённые видео… сцена [в] автосэмакс[е] ("3ds Max" by context — labelled an inference), они могут выключить видимость вот этих вот штуковин. Вот и запечь на новое видео, где их не будет." His verdict: "Типа, это вполне себе рабочий вариант." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**Val's ruling closed the progressive argument rather than answering it.** First, bluntly: "Ну какая разница, причём здесь прогресс[ив], [к]акая разница?" Then the direction itself: "А нет, не обращайте внимания на это, если мы пойдём с играми эт[от] Джорджия коа[м], то мы всё будем адаптировать. Мы не будем стараться подгонять, мы просто возьмём игрушк[у], мы переделаем" — do not pay attention to the progressive; if we go with the Georgia COAM games we will adapt everything, we will not try to make things fit, we will take the game and redo it. Pavel completed the thought with the maths — "Математику другую" — and Irina agreed ("Да"). [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**Igor's acceptance, verbatim:** "Да хорошо, ну то есть это я думаю можно… это более рабочая схема, по крайней мере чем пытаться… угадать, как нам здесь распределить элементы, чтобы было красиво" — a more workable scheme than guessing at how to distribute the elements so it looks good. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## What this decision does and does not settle

- **Settled:** the *starting material* for a vertical Texas product is the vertical Georgia COAM game set, not the horizontal Texas one; the direct algorithmic horizontal→vertical conversion is off the table with the current art; everything in the reused games — **including the maths** — is redone rather than fitted.
- **Not settled:** which progressive a vertical Texas product carries. Val set the question aside; he did not answer it. Irina asked directly "А у нас Техас мистери сейчас?" (is Texas mystery at the moment?) and Igor would only infer from a jackpot frame on screen — "судя по всему, он мистер[и]… я над ним не работал, я ранее не запускал его локально, но судя по вот этой вот рамке" — explicitly not knowledge. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **Not settled:** the size of the maths rework, or who assembles the new background video (below).
- **No product, release date, market date or platform choice for the Texas vertical product is stated anywhere in either source.** In particular nothing here schedules the product, and nothing here touches the standing positions that **RAGE is parked with no sunset date** and **NOVA→GLI is unscheduled** (see [[wiki/topics/nova-platform-architecture.md]]).

## Irina's alternative layout, not adopted

[[wiki/people/irina-shishko.md|Irina Shishko]] argued for a different arrangement rather than a different source game: leave the top screen at its current size, enlarge the main game field, keep the pay table as it is. "Нам нужно main экран увеличивать, а не верхний. То есть этого достаточно информации, и он не нужен больше"; and "Посмотреть поле, а оставить этот pay table таким как есть, потому что он достаточн[ой] высоты [и] ширины и потом посмотреть, сколько остаётся вверху, это то, что под лого идёт." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

Igor's answer is the durable engineering point: **replacing the background means replacing the whole scene**, because the reel frame and the logo are baked into it — "Замена фона это фактически замена все[й] сцены… потому что, например, рамка [р]елов она тоже запечена в фон. Вот [и] лого запечено [в] фон." He can place the reels and style the symbols freely — "мы со своей стороны можем как угодно раскидать позиц[ии]… [р]елов, сделать им какой угодно ст[а]йл для символов" — what he cannot do is produce the background video: "нам нужен человек, который… может собрать фоновое видео… А я уже смогу с помощью Клода подстроиться [под] это фоновое видео по позициям [э]лементов." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

Irina also made the cost argument for reuse generally — "переделать фон или… одну игру доработать, это всё-таки меньше, чем с нуля сделать там все игры" — and Igor confirmed this is normal practice: "Часто так делаем, когда мы берём существующие игры с… ста[рым] ар[том] и [меняем] арт на более современ[ный]" (the passage is heavily garbled; read as *old art swapped for more modern art*, labelled an inference). Pavel's own AI idea — let AI stretch the top background and place the auxiliary blocks itself — he rejected in the same sentence: "всё равно оно будет слишком разрежено и слишком много занимать места именно вспомогательная информация, а не рилы." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## Why this is different from the earlier RAGE→NOVA work

Val asked whether the team had not already done a horizontal→vertical conversion. Igor said no, and described the earlier work exactly as the corpus records it: "у нас была горизонтальная игра из продукта [sausd data nor pays] … и мы делали из неё горизонтальную же игру для продукта нов[а]" — a **horizontal** game from an existing product became a **horizontal** game for NOVA. The difficulty there was the framework, not the art: NOVA until then had only the vertical **Calle Ocho** ("у нас [в] нов[е] до этого была только вертикальная калиочи, нам пришлось… расширить… имеющиеся нов[а] [ф]ре[й]мв[о]р[к] для поддержки вот этих горизонтальных рас[кладок]"), while "арт там весь был и так горизонтальный. Соответственно, там никаких вопросов с искажениями… соотношения сторон экранов." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

*(The product name is rendered "sausd data nor pays" and the derived notes call it "an existing product name, not recoverable from the audio" [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]. **Inference, not assertion:** by cross-reference it matches the documented Aug-18/Aug-28 port of the horizontal game **Dragon Pays** out of the **South Dakota** product onto NOVA — see [[wiki/topics/nova-platform-architecture.md]] — which is the only horizontal-to-horizontal RAGE→NOVA conversion in the corpus. Left as a reading, not a fact; queued for the owner.)*

Igor added the design intent behind NOVA's layouts: the platform was meant to take one and the same game as either vertical or horizontal via configured layouts — "одну и ту же игру она может взять как вертикальную, так [и] горизонтальную… за счёт настроенных лояутов" — but even then "для вертикальной и для горизонтальной раскладки это были разные видео… а не одно и то же": different background videos per layout. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — call [[wiki/people/pavel.md|Pavel Frolov]] back on the "Юрий Валентинович" / finding-a-group-of-people topic, in a separate conversation — due same day (Sept 14 2026): "давайте мы отдельно поговорим над этим… На эту тему вам перезвоню тогда" — [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

No other firm commitment was made. Igor's offer to try further layouts was conditional and the meeting moved away from it: "если мы хотим этим заниматься, можно попробовать разные варианты… просто… сделать это… без изменений у нас не получится." [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## Open questions

- **Who assembles the background video?** Igor needs a person who can build it; after that he can fit it to element positions with Claude. No name was proposed. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **Which progressive does a vertical Texas product carry?** Set aside by Val, not answered; Igor's "mystery" read is an inference off a jackpot frame, not knowledge. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **How big is the maths rework?** Val directed that the maths be redone ("Математику другую"); nobody sized it. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **What was cut out of the Georgia games, and what merely hidden?** Pavel: "мы выпиливали хенс, например, тогда… из Джорджия"; Irina: "Но мы его скрыли" — we cut *[hens/hands — garbled, not recoverable]* out of Georgia / no, we hid it. Recorded as spoken; not interpreted. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

**§15.8:** clear on this page — game-engineering, art-production and product economics only; no named-person compensation appears in either source. **§15.9:** no licence, registration, tax or account numbers appear in either source.

## Sources

- [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
