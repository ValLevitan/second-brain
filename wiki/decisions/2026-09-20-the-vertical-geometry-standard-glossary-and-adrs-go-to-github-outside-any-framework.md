---
type: decision
title: The vertical geometry standard, glossary and ADRs go into GitHub, outside any framework — then end-to-end tests, then a timed conversion
date: 2026-09-20
aliases: [geometry standard to GitHub, vertical geometry standard, ADR consolidation, glossary standards ADRs, experiment in a vacuum, эксперимент в вакууме, стандарты глоссари ADR, stopwatch experiment, секундомер, frameless integration, безрамочная интеграция, Pantone to Pantone, three stages GitHub then e2e then conversion]
source-count: 2
status: active
open-commitments: 8
open-questions: 4
---

# The vertical geometry standard, glossary and ADRs go into GitHub, outside any framework

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-20-vertical-geometry-standard-and-adr-consolidation.md|Sunday Sept 20 2026, 7:04 AM ET session]] (held in **Russian**), after [[wiki/people/igor-metelski.md|Igor Metelski]] showed the geometry standard he wrote for vertical game screens. [[wiki/people/pavel.md|Pavel Frolov]] proposed a different home for the work; Val overruled him. It follows the Sept-17 ruling that art must be turned into numbers — see [[wiki/decisions/2026-09-17-hard-geometry-from-the-scene-files-and-a-vertical-skeleton-per-game-format.md]]. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

*(Quotes are from an unpunctuated Russian speech-to-text transcript, kept word for word. Garbled words read differently here are in square brackets.)*

## What Igor brought

- **A written geometry standard for vertical screens.** He took the product rendered "**г к м 3**" / "**гэган 3**" as the base "**как самый свежий**" — its art is the newest. *(Read as the Georgia COAM 3 product by context — an inference; the derived notes write "GKM3".)* From its games he wrote "**требование к геометрическим параметрам игр**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- **The scene count, per Claude's review:** "**66 сцен, которые нужно сделать [в вертикальном формате] и ещё 60 сцен символов. Если мы хотим переделать символы**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- The standard, the zones, the bonus layouts and the transitions are described on [[wiki/topics/game-art-animation-production-pipeline.md]] (Sept 20).

## What Val ruled

**1. The work is an experiment "in a vacuum", and it goes into GitHub.** Igor had put the documents with the project: not yet committed in one product, copies in the "г к м 3" branch, and a local store of md files. [[wiki/people/irina-shishko.md|Irina Shishko]] added that "**пока вот эти все продукты, они только в [SVN,] нет ещё в гите**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

- **Igor's view:** general standards belong in GitHub, but a RAGE-only tool — "**рейч сын конвертер**" — should stay with RAGE.
- **Pavel's view:** this is experimental work; once a game is actually made for "**Рынка [Техас], [Небраска]**", "**мы заводим эту игру в новом репозитор[ии] в гетхабе**", and its documents live in that game's repository.
- **Val's ruling:** "**Нет, простите, я всётаки буду настаивать**". The work is "**под рамкой эксперимента**", "**абсолютно оторван от какогото принадлежания к любой … [фреймворку], он в вакууме находится**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

**His reason:** "**это в 1 раз в жизни … где мы правильно, ну с моей стороны правильно … определили подход к разработке игры … За все наши годы … Там 20 лет**" — and "**1 раз создаём правильное определение. Правильный глоссари**". He wants it gathered in one place and "**законсервировать его как начальную точку**" of a new development culture. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

**2. Glossary, standards and, above all, ADRs.** "**нужно создать [глоссари]. И записать стандарты и что самое главное записать все [ADR]s потому что [ADR] … Будут диктовать последующую архитектуру**". Later: "**[ADR]s, это самое важное, что существует здесь**", and "**Всё должно быть очень, очень жёстко описано**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

- **Igor did not know the term.** "**А вам один вопрос, что такое эдиарс?**" Val: "**Архитекчел рекордс**"; Val then explained it as "we decided to do it this way".
- **How to get them:** run Claude over all the meeting transcripts. "**Клод очень шикарно … Вытаскивает все [ADR]s с любого транскрипта … некоторые там будут липовые, их не нужно.**"
- **Where they live:** "**[ADR]ы должны быть частью вашего … Кода … В репозитории**". This matches the standing NOVA rule that ADRs live inside the repository they describe — see [[wiki/topics/nova-platform-architecture.md]].

**3. Two additions to the glossary** [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]:

- **A mathematical approach to colour.** "**я хотел бы, чтобы мы перестали говорить немножко синенький, немножко оранжевый**". Not every gradient needs a formula: "**мы идём с такой [пантоновой] гамой в эту [пантоновую] гамму. И мы туда доходим, например, за какоето определенное время или определённый [frames]**". Some things may stay descriptive — "**не всё нужно выражать в точных цифрах**".
- **The physics of materials and motion**, even if incomplete, because the next frontier of AI is "**описание материалов и физики движения**".

**Frameless integration as a named term.** Val asked for Igor's phrase to be recorded. [[wiki/people/pavel.md|Pavel]] supplied the Russian word, "**безрамочный**". Val extended it: "**фреймлес интеграция объектов, но также есть ещё [фреймлес] интеграция, бэкграундов и у них есть определённая физика**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

**4. The designers are kept out.** When Irina said the designers' source scenes could be found, Val said: "**я не хочу делиться с дизайнерами и никакими нашими подходами**". Pavel offered a route without them — "**попросите Андрея, достанька нам видео сырой**" (which Andrey is not said; left unresolved). Irina said the stored work can be found "**за спиной**". For new art, Val named "**Сергея [клименвича клименничева]**" — read as [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]] by context. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]] This matches Val's Nov-2025 instruction to keep the game-generation ambition away from Lena's team — see [[wiki/topics/game-art-animation-production-pipeline.md]] (Nov 11 2025).

**5. The order of work is fixed — three stages.** Val first asked for a timed test: give Claude "**горизонтальн[ую] [рейдж] игр[у]**" plus "**новые стандарты и [глоссари]**" and say "**Переведи это на [нова] вертикально**", with a stopwatch. Igor asked for the result to be defined — "**Результат, при этом рабочая новая игра**" — Val: "**Да**". Igor then said the auto-testing is unfinished and the full flow must exist first; Val agreed ("**Согласен … Вы правы**"). When Igor asked for a few days to finish testing first, Val said no — organise now "**пока у вас все свежее в голове**". The order he set [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]:

1. "**организуйте вот то, что уже [есть]**" — in GitHub.
2. "**Добейтесь … [энд-ту-энд] тестирование**".
3. "**3 этапом. Возьмите экспериментальную игру, переведите ее с горизонтального [рейдж] на вертикальный [омни]**" — then at once "**В нова**". *(He says "омни" and corrects to "нова"; NOVA is taken as meant.)*

**6. The standard goes into NOVA's skeleton.** To Pavel: "**В нова. Все эти новшества нужно … Перенести**", as part of the "**Юнифайд**" — Pavel: "**Скелетон**" — with a standard way for every game to call it, "**стандартно, безошибочно**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

**7. Deadline.** Igor asked for "**пару дней минимум**", ideally a week, so nothing un-reviewed is uploaded. Val: "**давайте в четверг**" — Thursday **Sept 24 2026** (date derived; the transcript says only "Thursday"). Val will set a one-hour meeting "**на 08:00 … [Eastern] time**". [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

## Technical rulings in the same session

- **Liquid-glass frames are drawn by the framework, not baked into video.** Igor's shader demo, and Pavel's verdict: "**это правильный подход, потому что очень легко поменять игру с трёх прогрессив левел на 2**". Detail on [[wiki/topics/game-art-animation-production-pipeline.md]] (Sept 20).
- **Few videos at run time, separate pieces before baking.** Igor: "**каждое видео это отдельные декодеры**", so a running game needs "**как можно меньшее количество видео**"; but when scenes are assembled, separate pieces keep the layout free to change.
- **The alpha channel is optional.** Where nothing happens it is left out, because it is "**дополнительный … фулл эйч ди ролик**" needing another decoder.

[[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

## Open commitments

- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — move and organise the geometry standard, glossary, standards and ADRs into GitHub, detached from any framework — due Thu Sept 24 2026 — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — add the glossary to the document, and an English version (it is in Russian today) — due Thu Sept 24 2026 — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — extract ADRs from the meeting transcripts with Claude, drop the false ones, and keep them in the repository with the code — due Thu Sept 24 2026 — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — add frameless integration (objects and backgrounds), the colour approach and materials/motion physics to the glossary — due unspecified — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — finish the end-to-end auto-testing so a full flow exists (stage 2) — due after the GitHub work — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — run the timed conversion: a horizontal RAGE game into a working vertical NOVA game, from the standards and glossary (stage 3) — due after stage 2 — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — carry the standard into the NOVA framework as part of the unified skeleton, with a standard call for every game — due unspecified — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — set the one-hour follow-up for Thursday at 8:00 AM Eastern — due Sept 20 2026 — [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

## Open questions

- **How far should the colour glossary go?** Val left it open: not every gradient needs a formula; decide as the work grows. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- **Can materials and motion physics be defined now, or only as a placeholder?** Val himself was unsure it is worth the time yet. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- **Can Claude re-cut a flat horizontal background by moving the horizon point?** Val thinks so; Igor said maybe, but not with the existing art of that product, and offered to try it in the background as cheap work. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- **Which "Andrey" fetches the raw video?** Pavel named only "Андрея". Not resolved. [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]

## Notes vs transcript

The derived notes were checked against the transcript. Where they differ, the transcript is followed [[raw/Meeting_Notes_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]:

- The notes name the new-art source "**Sergey Klimenchuk**". The transcript says "**клименвича клименничева**", read here as Sergey Kleimenychev. No "Klimenchuk" exists in the corpus.
- The notes say raw video is pulled "without involving" designers but drop **Pavel's "ask Andrey"** step.
- The notes name the second product "**NATO**" and a game "**Crest City Carnival**". The transcript's "нато" / "над" / "н а т" stays **unresolved**, as on the Sept-17 stubs; the game is **Crescent City Carnival** ("крестный сити карнавал"), an existing title.
- The notes say Igor "put the documents in the NATO project repository in SVN". The transcript says he had **not yet committed** them there; copies were committed to the "г к м 3" branch.

**§15.8:** Val's remarks on Igor's temperament and his view of how the designers would react are **not recorded** beyond the business rule (keep the designers out). No pay or compensation appears. **§15 #9:** no licence, registration, tax or account numbers appear.

## Sources

- [[raw/Meeting_Transcript_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
- [[raw/Meeting_Notes_Vertical_Geometry_Standard_and_ADR_Consolidation-September-20-2026.md]]
