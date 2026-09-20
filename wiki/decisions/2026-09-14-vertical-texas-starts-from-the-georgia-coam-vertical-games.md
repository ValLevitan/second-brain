---
type: decision
title: A vertical Texas product starts from the vertical Georgia COAM games, not from converting the horizontal Texas games
date: 2026-09-14
aliases: [Texas vertical conversion, days not weeks, измеряется в днях не в неделях, generate background video from description, two AI conversion experiments, склад код, graphic assets stretch will shrink, horizontal to vertical Texas, Georgia COAM as the Texas base, vertical Texas product, конвертация горизонтального Техаса в вертикальный, Rage-Nova_conversion]
source-count: 7
status: active
open-commitments: 2
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

- **Who assembles the background video?** Igor needs a person who can build it; after that he can fit it to element positions with Claude. No name was proposed. **Sept 16 update:** Pavel is testing whether the background video can be *generated* from a written description instead of assembled by a person — see the Sept-16 section above. The experiment is running; the question is not answered. **Sept 17 update:** the first such video exists and is running inside a playable vertical game — Anton Leshkevich generated it on Sept 16 and Igor built the scene from it on Sept 17 [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]. That answers *whether* it can be generated rather than assembled. It does **not** answer who does this as a standing job: no role or name was assigned, and the day's ruling points at a single "universal graphic designer" who has not been identified or hired. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **Which progressive does a vertical Texas product carry?** Set aside by Val, not answered; Igor's "mystery" read is an inference off a jackpot frame, not knowledge. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **How big is the maths rework?** Val directed that the maths be redone ("Математику другую"); nobody sized it. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- **What was cut out of the Georgia games, and what merely hidden?** Pavel: "мы выпиливали хенс, например, тогда… из Джорджия"; Irina: "Но мы его скрыли" — we cut *[hens/hands — garbled, not recoverable]* out of Georgia / no, we hid it. Recorded as spoken; not interpreted. [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]

## Sept 16 2026 — two experiments are running, and Val puts a unit on "fast"

Two days later, at the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept-16 12:35 PM ET alignment call]], Val asked [[wiki/people/pavel.md|Pavel Frolov]] for a short update "**просто чтобы Геннадий ориентировался лучше**" — so [[wiki/people/genadi-peari.md|Genadi]] could see where this stands. Pavel named **two experiments, both in progress** [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]:

1. **Generate the background video from a written description.** "**[В]зять горизонтальную игру[,] описать ее словесно[,] что там видео делает[.] И сейчас будем проверять, сможем ли мы генерировать фоновое видео по описанию. Скорее всего, что[-]то из этого получится.**" — take a horizontal game, describe in words what its video does, then test whether a background video can be generated from that description. **This goes directly at the open question below** — who assembles the background video — though nothing here answers it yet.
2. **Reuse a vertical layout for a different game, different maths, different market.** "**существующ[ую] … вертикальную игру с вертикальным [layout'ом] — для [Д]жорджия, например — взять и попытаться под этот [layout] сделать … другую игру с другой математикой и для другого рынка, например, для Техаса.**" — which is this decision's own scheme, now being tested rather than argued.

**If both work:** "**мы, наверное, довольно[-]таки быстро сможем конвертировать … разные игры … [под] вертикальный кабинет**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Val supplied the unit, unprompted:** "**Когда мы говорим очень быстро — это измеряется в днях[,] не в неделях**" — days, not weeks [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Pavel would not commit to it**, and the exchange is worth keeping whole because the two men end up agreeing on different things. Pavel: "**можно будет это утверждать, когда … первую игру … сделаем, закроем все баги**" — the claim can be made once the first game is finished and its bugs are closed. Val accepted that ("**Конечно, я понимаю[,] попробуй**") and narrowed his own claim to "**индикация на то, что похоже, что это получится**" — an indication, not a result [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**The one thing Pavel would state flatly** is the part of the pipeline that shrinks:

> "**[Т]о[,] что у нас из пайплайна уберётся довольно длительный период, который раньше занимал … разработка графических асса[тов] и их … причёсывание. Ну это сократится точно.**"
> — the long stretch that used to go on developing graphic assets and tidying them will definitely shrink.
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

*(**§4 / §9.131 — the tool.** Val credits "**склад код[ом]**" / "**склодам**" for this. The derived notes read it as **Claude Code**; the reading is supported inside this thread — the Sept-14 source has Igor Metelski naming "**Клод**" explicitly for the same work — but the Sept-16 string itself is a garble and the product name is recorded here as **an inference**, not as a fact. Val's verb in the same sentence, "**конденсировать игры**", is likewise a garble of *convert*, which is the word Pavel uses throughout.)* [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**Open commitment added Sept 16:**

- [ ] Pavel Frolov — finish the first AI-converted game, close its bugs, and then confirm how fast conversion actually is against Val's "days, not weeks" — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**§15.8:** clear on this page — game-engineering, art-production and product economics only; no named-person compensation appears in any of the sources. **§15.9:** no licence, registration, tax or account numbers appear.

## Sept 17 2026 — the scheme is running: a generated video is inside a playing vertical game

Three days later, at the [[wiki/meetings/2026-09-17-vertical-game-skeletons-and-the-art-pipeline.md|Sept-17 12:19 PM ET session]], [[wiki/people/igor-metelski.md|Igor Metelski]] screen-shared **a vertical game that plays**, built by dropping the video [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] had generated the day before into an existing game as its scene, with symbol positions computed from the video's proportions so each symbol lands in its own cell. Anton's video was itself produced in part by parsing an existing **vertical 3×3** game JVL already owns. [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]

**This is the first time in the corpus that both Sept-16 experiments appear as one working artifact** — a generated background video (experiment 1) carrying a different game on an existing vertical layout (experiment 2).

**What it does not do is close this decision's open questions.** The demo bypassed the pay-table mechanism the team had built, cutting the vertical pay table out of the horizontal one by hand; the untouched horizontal scene still breaks; and nobody was made the standing owner of background-video production. See the open-questions section above, where the "who assembles the background video?" item is updated rather than closed.

**Pavel's Sept-16 commitment is not discharged.** He undertook to confirm conversion speed only once the first game is finished and its bugs are closed; on Sept 17 the game runs but the bugs are not closed, and no speed claim was made. It stays open.

**A second ruling was taken at that session, recorded separately:** the reference layout for a conversion is another vertical game JVL already has, and each game format gets a fixed vertical skeleton — [[wiki/decisions/2026-09-17-hard-geometry-from-the-scene-files-and-a-vertical-skeleton-per-game-format.md]]. Nothing in it contradicts this decision; it is the working method underneath it.

**Val's own closing line is worth keeping for its correction.** He praised the result and added that they had managed without Anton — "**Классный результат … и обошлись без Антона**" — and was immediately put right by [[wiki/people/irina-shishko.md|Irina Shishko]] ("**а видео чьё?**") and [[wiki/people/pavel.md|Pavel Frolov]] ("**как это без Антона?**"); Val accepted it ("**опять Антон**"). The derived notes report that the video was Anton's work but **omit the claim Val actually made**, which is the part that shows how invisible the generation step was to him [[raw/Meeting_Notes_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]] [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]].

## Sept 17 2026 (12:45 PM) — the missing platform choice is supplied: Texas goes on NOVA

Two minutes after the 12:19 PM session above ended, on the [[wiki/meetings/2026-09-17-kleimenychev-hire-nova-direction-and-planning-handover.md|12:45 PM "General alignment" call]], [[wiki/people/val-levitan.md|Val]] ruled "**не делать никаких игр в речь**" and "**сразу переключиться на нового и Техас сделать на ново**" — build no games at all in RAGE, switch straight to NOVA, and **do Texas on NOVA**. [[wiki/people/pavel.md|Pavel Frolov]] had prompted it by noting that the running experiment produces RAGE output which would then need converting into NOVA anyway. [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

**This answers one of this page's own gaps.** The "What this decision does and does not settle" section above records that **no platform choice for the Texas vertical product is stated anywhere** in the Sept-14 sources. It is stated here, three days later: **NOVA**. That sentence stands as written about its own sources; this is the later source that supplies the answer. Full record on [[wiki/decisions/2026-09-17-no-more-games-on-rage-and-texas-is-built-on-nova.md]].

**The rest of that sentence still holds.** No product name, release date or market date for the Texas vertical product is given on the Sept-17 call either, and nothing there touches the standing positions that **RAGE is parked with no sunset date** and **NOVA→GLI is unscheduled** (see [[wiki/topics/nova-platform-architecture.md]]).

**This decision's own scheme is unaffected.** The *starting material* remains the vertical Georgia COAM game set; what Sept 17 adds is the platform that material lands on. **Its open questions are not answered** — who assembles the background video, which progressive a vertical Texas product carries, and how big the maths rework is are all untouched by the Sept-17 call.

**A new question comes with it:** what becomes of the RAGE horizontal→vertical conversion experiment already running — Val ruled on future games without saying whether the work in flight continues, is redirected or stops, and nobody asked. It is recorded on the Sept-17 decision page, not duplicated here.

## Sources

- [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Transcript_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [[raw/Meeting_Notes_Vertical_Game_Skeletons_and_Art_Pipeline-September-17-2026.md]]
- [[raw/Meeting_Notes_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Texas_Vertical_Conversion_and_Georgia_Game_Base-September-14-2026.md]]
- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
