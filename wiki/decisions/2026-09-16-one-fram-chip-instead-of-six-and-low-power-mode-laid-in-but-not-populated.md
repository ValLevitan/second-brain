---
type: decision
title: Memory comes out of the street machine's board — one FRAM chip instead of six, the per-game statistics move out, and low-power mode is laid in but not populated
date: 2026-09-16
aliases: [one FRAM chip instead of six, 6 микросхем fram, под 256, одной 256, ferromagnetic memory six banks, фиромагнитик мемори 6 банков, statistics move to SD card or eMMC, last ten games and fifty free spins, low power mode, лоу пауэр мод, компоненты заложить но not populate, lay in but do not populate, light controller must go, not always correctly written]
source-count: 3
status: active
open-commitments: 1
open-questions: 2
---

# One FRAM chip instead of six, and low-power mode laid in but not populated

Worked out by [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]] and accepted by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept 16 2026 12:35 PM ET alignment call]] (held in **Russian**). This is where the money actually is in the [[wiki/topics/low-cost-street-machine.md|street machine]]'s electronics; the board layout it sits inside is [[wiki/decisions/2026-09-16-the-street-machine-carries-two-boards-and-a-new-io-board.md]].

Genadi named the target in one line: "**У нас сегодня … основное — это куча эф[-]рама, который стоит денег… [в]се остальное это ерунда**" — the pile of FRAM is what costs money; everything else is trivia [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## What the FRAM is for today, and how much of it there is

- **Six chips, each 256.** Pavel: "**у нас сейчас стоит … 6 микросхем f[ram]**"; Genadi: "**[п]од 256**"; Pavel: "**Да, под 256.**" Genadi described the same thing as "**фиро[м]агнитик мемори, котор[ой] … сегодня … 6 банков**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **What fills it: per-game history.** Pavel, twice and consistently: "**у нас есть, например, 6 игр[,] мы по каждой игре пишем последн[ие] … 10 сыгранных игр и … по каждой игре … последние там 50 фри спинов**" — for each of six games, the last **ten games played** and the last **fifty free spins**. That is "**основная часть памяти[,] куда уходит**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **The rest — live game state — is about a megabyte.** Genadi asked "**то, что у тебя там … 2 мегабайта — это что?**"; Pavel corrected him: "**не 2 мегабайта, сейчас оно меньше[,] один мегабайт где[-]то — это … всякие состояния игры[,] ивенты, [к]аунтеры и прочее**", kept so the machine can roll back "**когда питание вырубили посередине**" — when power is cut mid-game [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## The cut

**Drop the per-game statistics requirement and one 256 chip is enough.** Pavel: "**если нам это писать не надо, то мы одной микросхемой обойдёмся**", and specifically "**нам тогда хватит … одной 256**". Genadi floated "**ориентировочно один 128 килобайт**"; Pavel held at "**1 [×] 256**" and Genadi accepted — "**А 256. Да.**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**The statistics move off the FRAM — to an SD card or to the eMMC — and the team accepts they may not always be written correctly.** Pavel's own framing of the trade:

> "**Всю статистику оттуда вынести … вплоть до Того, что можно будет вставлять [SD-]карточку… если она умерла[,] с[-]д карточка[,] выкинули, вставили новую[,] потеряли статистику, ну и ладно.**"
> "**эту статистику вынести куда[-]то … за пределы эф[-]рама[,] держать её исключительно для себя, но рассчитывать, что она не всегда может быть корректно записана.**"
> [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

The alternative destination named was the processor board's own storage — "**мы это можем и на [eMMC]**", or an SD card "**вставлен[ная] … в р[-]к плату**". What stays on the single FRAM chip is "**критические данные**" and "**какие-то общие … счетчики[,] [к]аунтера**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Six games is the working assumption** for the sizing — Pavel: "**сколько нам игр надо поставить[?] 6… [п]редположим 6**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. That matches the six-game cap carried on [[wiki/topics/low-cost-street-machine.md]] from June 2026.

## The condition Pavel attached — and did not get an answer to

The whole cut rests on there being **no requirement** to keep the extended statistics, and Pavel said twice that he does not know whether there is one: "**опять[-]таки надо посмотреть по требованиям**", and "**это при условии, что мы можем отказаться от какой[-]то расширенной статистики, как это сейчас есть в класс[е] 3 … [и] в [Д]жорджии … тоже класс би**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

He also flagged which market the requirement would come from, and answered himself: "**Класс … [А] … или это … всё[-]таки не класс [А]… [э]то наверно то, что в [Д]жорджии, а мы сейчас говорим … всё[-]таки Техас и … стрит машины**" — the Class A question belongs to Georgia; this machine is Texas and street [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. Nobody in the room settled it. See [[wiki/topics/georgia-class-a-machines.md]] for why there is no Class A rulebook to check against.

## Low-power mode: Val argued himself out of his own position, and the compromise held

- **Genadi's opener:** "**Лоу пауэр мод для стрит машины, наверное, нам не нужен. Вообще в принципе**" — and his definition, "**когда мы мониторим при выключенном состоянии двери**", monitoring the doors while the machine is off [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **Nobody claimed it was the expensive part.** Val asked "**[н]еужели это действительно много денег?**" and the answer back was "**Это конкретно нет**" — not this specifically. Genadi's point was that the memory around it is [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **Val first agreed to kill it, emphatically:** "**Абсолютно[,] абсолютно. Абсолютно нам не нужно [мониторить] двери, и нам не нужно это абсолютно**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].
- **Then he reversed himself in the same breath**, and the reasoning is the interesting part — he argued the counterfactual against himself first: if the design did not exist and he were asking them to build it on a hunch, "**[в]ы бы сказали: нафиг нам это нужно … и тратить на это деньги? Я бы с вами согласился.**" But it does exist: "**[у] нас это уже есть, нам это дорого не стоит. И все рутин[ы] же написаны и протестированы, и время на это тратить не надо.**" On whether it will ever be used: "**Будем ли мы этим пользоваться? Хрен его знает.**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- **Genadi's compromise, accepted:** "**если можно компоненты заложить, но not [populate,] это окей**" — lay the components into the design, do not populate them [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

Pavel had set out what the feature actually costs in hardware terms — a battery on the board, plus the processor running at a low clock to read the door state and report it through the modem when power returns, so JVL knows "**что машина была открыта[,] в выключенном состоянии**" and "**кто[-]то лазил … в бил[-]акцептер**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. Val's aside — every machine now carries a modem, so "**можно сказать, что у нас есть пауэр проблема через мод[ем]**" — was not developed [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**One further component goes without argument:** Genadi, early — "**Лайт контроллер … должен уйти в любом случае**", the light controller must go in any case [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

## Oct 1 2026 — a first cut on the board already in production: two 256-Mbit FRAM chips not populated, $12 a board

On the [[wiki/meetings/2026-10-01-genadi-io-board-chips-flat-bom-pilot-and-street-cabinet-panel.md|Oct 1 4:59 PM call]] (Russian) Genadi: "Наш текущий [IO board] right away мы снимаем 2 чипа памяти, удешевляем его $12 на борт… [FRAM] чипы по 256 мегабит, каждый чип стоит $6. Мы их просто… not populate." His reason is the same one Pavel attached here as a condition: "у нас нету требований увеличить записи, количество транзакций и объём транзакций." This is a step on the *current* board, ahead of the one-chip street board above; whether the current board goes from six chips to four is not said. The fuller redesign (memory type, USB controller) is on [[wiki/decisions/2026-10-01-two-fram-chips-come-off-the-current-io-board-and-the-street-machine-board-grows-out-of-a-redesigned-io-board.md]] [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]. *(Pavel's open question below — is there a requirement for the extended statistics? — is still not answered by anyone; Genadi asserts there is none.)*

## Open commitments

- [ ] Pavel Frolov — confirm what must still be written to FRAM once the per-game statistics move out, and size the single chip against the actual requirements ("**надо посмотреть по требованиям**", "**решить, что мы туда пишем**") — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

## Open questions

- Is there a regulatory or product requirement anywhere that obliges JVL to keep the extended per-game statistics in protected memory? Raised twice by Pavel, answered by nobody. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- What follows operationally from statistics that "**не всегда может быть корректно записана**" — accepted as a trade, with no consequence traced. [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

**§15.8:** clear — component and memory-cost economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Transcript_IO_Board_Memory_Chip_Removal_and_Redesign-October-1-2026.md]]
