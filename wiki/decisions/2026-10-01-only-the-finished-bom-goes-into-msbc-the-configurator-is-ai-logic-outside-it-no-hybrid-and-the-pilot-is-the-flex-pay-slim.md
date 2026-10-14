---
type: decision
title: Only the finished bill of materials goes into MSBC; the "configurator" that builds it is AI logic outside MSBC, with the versions in GitHub; no hybrid; and the pilot is the Flex Pay Slim BOM, pulled flat by Claude Code in a two-hour session with Genadi
date: 2026-10-01
aliases: [AI configurator, конфигуратор, configurator as AI logic, туда нужно загнать только готовый билов материи, only the finished BOM into MSBC, no hybrid, я не хочу делать гибрид, flat BOM pilot, Flex Pay Slim pilot, two hours on one flat BOM, не займёт больше чем 02:00, Claude Code builds the structure, pull the part number flat with all suppliers, пойдём обратным путём, sources of truth lead time physical count forecast, MSBC is not built for this, SAP Salesforce offer nothing, supplier history leaves Genadi's head, quotations not in GitHub, item cards in GitHub]
source-count: 4
status: active
open-commitments: 1
open-questions: 2
---

# Only the finished BOM goes into MSBC; the configurator is AI logic outside it; no hybrid; the pilot is the Flex Pay Slim (Oct 1 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] on the second segment of the [[wiki/meetings/2026-10-01-genadi-io-board-chips-flat-bom-pilot-and-street-cabinet-panel.md|Oct 1 2026 call]] (5:02–5:39 PM, Russian) with [[wiki/people/genadi-peari.md|Genadi Peari]]. It is the day-after continuation of the [[wiki/meetings/2026-09-30-github-to-msbc-bom-flat-list-bridge.md|Sept 30 meeting]] (Val: "Я хочу вернуться к разговору") and the parked 12:04 PM follow-on; the whole thread is sequenced on [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]]. Quotations from [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]] unless marked.

## What was ruled

- **The objective is not an export.** "[The objective] заключается в том, чтобы не просто смотреть на это, как экспортировать [bill of material]… [и] держать… заказы и административную часть в [MSBC] — это неправильный подход к теме." Narrowing it that way "уничтожает, убивает процесс того, что… я хочу добиться."
- **The split.** Once the versioning is in GitHub, "нам нужно перейти на финансовый менеджмент… [per supplier], который находится [в] Business Central… Мы также называем [MSBC]. Я так говорю для транскрипта просто." There: "Административно-финансовая менеджмент. Туда там ничего не надо делать. **Туда нужно загнать только готовый [bill of material].**"
- **The configurator is AI logic, built outside MSBC.** "А конфигуратор, как вы называете его? Конфигуратор сам нужно создать вне, он должен быть логикой AI." Genadi's read-back: "в [GitHub] будет… структура просто дата, флэт. И будет какая-то логика, по которой будет создаваться продукт из [GitHub] посредством этого конфигуратора." Val: "это будет сделано некоторыми шагами" — in steps.
- **No hybrid.** Genadi, late in the call: a hybrid "абсолютно реально" — MSBC builds the multi-level BOM, the rest elsewhere — and "Какая вам разница, что будет [source of truth]? Почему не может MSBC… быть сорсом для количества деталей?" Val: "**Я не хочу делать гибрид**, я хочу делать так, чтобы [AI agent] мог следить за [bill of material], за продакшн, за заказами, за [shortages] сам. И на это особого ума не надо."
- **The sources of truth, as Val listed them.** "всё, что в [truth]… находится в принципе во флат [bill of material], которые разложили один раз в [GitHub]"; the next source "находится в фактах, типа как lead time… как минимум [ору] ещё что-то" (the second word is garbled; the derived notes read MOQ); "следующий… в самом физическом пересчете деталей"; "ещё один… в форкаст." Whatever can hold all of these together wins — "Для меня этот [substance] это AI."
- **MSBC as a BOM tool, in his words.** "[MSBC]… это больная форма того, что могли сделать за все это время. Пока не было ничего лучшего." Today "компании как… [accounting — garbled]… Salesforce… в принципе ничего не предлагают собой" (Genadi interjected "Сап" — SAP). He pointed Genadi at a recently released finance bot from Grok as the kind of thing now possible (details not verified here).
- **Prices stay out of GitHub.** When Genadi proposed putting vendor communications, "cotation какие-то spex" with the items in GitHub, Val: "в гетхабе это не нужно." Genadi: "Но вы сказали общение с вендором, ревизии, даташиты — не цены." So: revisions and datasheets yes, quotations and prices no — consistent with [[wiki/decisions/2026-09-30-engineers-never-change-msbc-and-administration-never-changes-github.md]].

## Why — Val's reasons, beyond the BOM

- **Supplier history must leave one head.** Only about 30% of parts come from SolidWorks (Genadi: "вначале я бы сказал 30%, а потом это всё поддержка… никакой связи с солидворксом"; Val agreed — "или 70% или 50%… проходит мимо [SolidWorks]"). The rest is continual work with suppliers, many still prospects, not yet "[finance suppliers]": drawings, technical data, samples, versions from each. "сейчас это все держится или в имейлах или в [chats], или где-то ещё, и об этом знаете только вы… у вас под это есть память хорошая… Мне от этого нужно уйти. Мне нужно сделать свою память, AI… и AI… логику." Genadi: "Так мы про это договорились?" Val: "Мы договорились, в какой-то степени… на это нет резистанции."
- **The old tooling is the wrong road.** Flat-BOM export "существовал в [SolidWorks] уже давно", and the SolidWorks marketplace has "трансляторы, которые сразу могут взять [bill of material] и положить их в Business Central напрямую" — Genadi: "Согласен" — "но это неправильно. Это было раньше. И такие движения не позволяют вклинить сюда AI процесс."
- **Headcount.** "я не хочу расти в количестве людей… найти хороших людей всегда было тяжело… мы работаем в разных местах." He does not want a C-level layer under him; the replacement he is building is AI executives (see [[wiki/topics/ai-assisted-development.md]], Oct 1).
- **The AI handles categories and reasons.** Parts are already grouped "в категориях… например… money device"; explain what a money device is (bill acceptor, printer, AFT) and its limits, and "AI разберется быстрее и более эффективно, чем любой [human]." Each change is a GitHub commit with its reason — "он на пожизненно это запомнил." Genadi agreed that every ECO "должны быть [stored в GitHub], проверяться каждый раз абсолютно."
- **It is like the autotests.** Val: a year or two ago writing autotests from acceptance criteria "было просто на уровне фантастики. Но сегодня Алексей Хамин и Ваня наш пишут эти тесты. И [Claude] тестируют." Genadi: "снимаю шляпу, как вы этот клод и вообще всё вот это изменили."

## Genadi's standing doubt, on the record

- "Как можно создать заранее конфигуратор на то, что ты не знаешь, как будет?" — and, repeatedly, he cannot see the one step: "Построение деревьев [bill of material в MSBC] посредством… флэт структуры в [GitHub] — вот эту трансформацию я просто не понимаю, как это можно сделать. Потому что есть факторы, которые мы меняем на ходу… [bill of material] должны быть разбиты [в] соответствие шагам в продакшн."
- His example: special screws added to a bill-acceptor connector kit after a one-off problem — "как можно сказать AI: тебе нужно пойти найти этот айтем, или его создать и добавить его туда?" Val: the same way Genadi reasons it himself — there is a category and a commit that says why.
- "любая ERP система… они все [pull] из [database]… если он может сделать такую [дубликат] в [GitHub], чтобы она не была флэта, чтоб можно было модули делать, их собирать — это было бы прекрасно." And: "Я не вижу логики… У меня нету даже идей." Val: "вы не поймете до тех пор, пока вы не начнете с этим работать." Genadi: "Дай бог."
- His own first step, offered twice: item cards in GitHub now for everything JVL buys today, taken from MSBC ("у нас сегодня есть эта вся в MSBC… все эти [items] взять, в [GitHub] сделать полностью этот лист"), with revisions and vendor changes. Val did not take it up; he moved to the pilot. Later Genadi offered "какой-то модуль, который можно пользоваться прямо в [GitHub]… замены построение [bill of material] в MSBC". Not answered.

## The pilot

- **Val's proposal.** "давайте мы с вами возьмём время… возьмём [flat bill of material], у нас не займёт больше, чем [02:00 — two hours, by context]. Я при вас поиграю с этим, и мне кажется быстро мы найдём кучу вещей, как это можно делать." If it works, the logic is handed to "какому-то AI агенту", which is corrected when it errs and then "руководит всей этой логикой."
- **Which BOM.** Val: "или Флекс IQ или [Flex Pay Slim], любой." Genadi: "давайте слим, и мы сейчас надо работать со слим уже. У нас слим будут конфигурации… для Техаса" (cut off).
- **What Genadi says is in it.** "этот номер, который я вам дал, это то, что я последний создал" — the latest BOM, built for Georgia; it lacks small items ("количество винтиков… мелкого нету") but has "все компоненты, всё, что мы покупаем… каста [part], который будет меняться в зависимости от [jurisdiction]… кит для [bill acceptor], для [card dispenser]… правильные [sub-assemblies]… вся структура", built the way the Flex is.
- **What Val will do.** "Напишите мне в чате, какой [part number] вы хотите взять… Дайте мне точный [part number]… Я возьму транскрипт… этот [part number]… я попрошу, чтобы [Claude Code] создал мне инфраструктуру… вытащить этот [part number], сделать его флат, и лист всех [suppliers] на все детали, которые входят… в этот [Flex Pay Slim]. И мы начнем оттуда, пойдём обратным путём." Then: "я сначала сделаю структуру в [GitHub]… Я практически уверен, что я сам это смогу сделать."
- **Nathan.** Genadi: "Я так понимаю, что нэйтан сделает какие-то эксперименты?" Val: "Да мне давно это нэйтане нужен, я сам могу это сделать" — **unclear** whether "I have long needed this from Nathan" (the notes' reading [[raw/Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]) or "I don't need Nathan for this"; the second half, "I can do it myself", is clear. Later Val allowed that there may be "куча вещей, которые нам или нейтану нужно будет подтянуть." Nathan's Sept-30 experiments are not withdrawn on tape.

The derived notes record the same two decisions ("Only the finished BOM goes into MSBC… no hybrid"; "Pilot on the Flex Pay Slim BOM") and three undertakings [[raw/Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]].

## How this sits against Sept 23–30 (evolution; the dispute is not closed)

Sept 23: GitHub is the BOM's source of truth, contested. Sept 24: the BOM is built in BC automatically from GitHub data. Sept 30: one flat list in GitHub agreed; the grouping into assemblies contested; Nathan to experiment items-first. **Oct 1 adds the name and place of the grouping step — a "configurator" that is AI logic, outside MSBC — rules out the hybrid Genadi proposed, and replaces the Sept-24 "fake BOM on the new Slim" idea with a dated pilot method (Claude Code pulls the Slim part number flat with suppliers; a two-hour session).** Genadi's objection is unchanged in substance ("I cannot comprehend" on Sept 30; "Я не вижу логики" on Oct 1), so the Sept-23 decision's "contested by Genadi" status stands. Evolution, not contradiction.

## Oct 5 2026 update — the pilot goes to Nathan

Four days later Val met Genadi again ([[wiki/meetings/2026-10-05-design-to-msbc-zero-trust-repos-and-data-contracts.md|Oct 5, 1:19 PM]]), explained the developer repo model, agreed Genadi "сами это не подтянете", and handed the Flex Pay Slim pilot to Nathan Carver, to be shown to Genadi when done [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]. At 1:58 PM Nathan took it as a reverse spike: flatten the MSBC BOM into GitHub, rebuild it through repos, data contracts and agents, push it back and compare [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]. The ruling here stands; the pilot's doer and form change — see [[wiki/decisions/2026-10-05-nathan-carver-runs-the-flex-pay-slim-bom-reverse-spike-and-flex-port-follows.md]]. The Val-builds-it-himself and two-hour-session items move to History below.

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — put the exact MSBC part number of the Flex Pay Slim BOM in the chat — due Oct 1 2026 ("Поставьте сюда в чат, пожалуйста"); Genadi said he had already given a number — [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]

## History

- [x] [[wiki/people/val-levitan.md|Val Levitan]] — take the transcript and the part number and have Claude Code build the GitHub structure: the Flex Pay Slim as a flat list with all suppliers for every part, then work backward — due unspecified — [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]] — **handed over Oct 5 2026, not done by Val:** the build goes to Nathan Carver as the Flex Pay Slim reverse spike [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]] [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
- [x] [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/genadi-peari.md|Genadi Peari]] — a working session of about two hours on the flat BOM, Val working it in front of Genadi — due unspecified — [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]] — **replaced Oct 5 2026:** Nathan demonstrates the spike and Genadi reviews it [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- *Answered Oct 5 2026:* "Is Nathan Carver's Sept-30 experiment still wanted?" — yes; the pilot itself goes to him [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]

## Open questions

- How are multi-level BOM trees and production-order sub-assemblies produced from a flat GitHub list, when parts and kits change on the fly? Genadi's question, unchanged since Sept 23; Val's answer is "you will not understand it until you work with it" and the pilot — [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]
- Genadi's offer of item cards in GitHub now for every bought item, and of a small module in GitHub replacing BOM-building in MSBC — neither answered — [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]

**§15.8:** Val's sharper remarks at Genadi, and an exchange about who is "smart" or "dumb", are held generically; the substance is recorded. Personal matters not recorded (a marked passage and the lines after it). **§15 #9:** none — the part number is not spoken.

## Sources
- [[raw/Meeting_Transcript_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]
- [[raw/Meeting_Notes_Flat_BOM_in_GitHub_and_AI_Configurator-October-1-2026.md]]
- [[raw/Meeting_Transcript_Design_to_MSBC_Zero_Trust_Repos_and_Data_Contracts-October-5-2026.md]]
- [[raw/Meeting_Transcript_Nathan_Carver_Flex_Pay_Slim_BOM_Reverse_Spike-October-5-2026.md]]
