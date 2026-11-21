---
type: decision
title: Genadi works only on the bill of materials with Nathan, not on procurement; drawings and data sheets for every part go into GitHub, and a missing data sheet is something the agent must report, not guess; what Genadi knows about purchasing goes into written standards, and he builds his own agent that checks all purchase orders once a day against them; MSBC gaps go to Nathan as use cases for his MCP (Val, with Genadi Peari, Nov 20 2026)
date: 2026-11-20
aliases: [Genadi only on the BOM, не работали с прокюрментом, работали только под нейтоном, PO check agent, daily PO agent, polit агент, посмотри на все POL, все ваши знания должны лечь в стандарт, data sheets in GitHub, дата шитс, Nathan not faking the assembly, нэйтан не фейкает эту сборку, $1500 air freight, packing list quotation, MCP use case loop, use case for Nathan, Nov 20 Genadi call]
source-count: 2
status: active
open-commitments: 5
open-questions: 2
---

# Genadi works only on the BOM with Nathan; his purchasing know-how goes into standards checked daily by his own PO agent (Nov 20 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] on an ad-hoc call with [[wiki/people/genadi-peari.md|Genadi Peari]] on Friday Nov 20 2026, about 3:09–3:25 PM Eastern, in Russian ([[wiki/meetings/2026-11-20-genadi-data-sheets-in-github-and-po-check-agent.md|stub]]) [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]. Genadi agreed. It follows the BOM thread of [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md|Nov 16]] and [[wiki/decisions/2026-11-18-the-next-bom-spike-is-a-self-learning-supplier-loop-the-agent-finds-the-supplier-asks-for-the-missing-data-updates-the-data-contracts-and-reassembles-with-no-human-answers.md|Nov 18]].

## Data sheets in GitHub

- **What Val wants to see.** "Все чертежи. И дата шитс. На каждой из. Элементов, которые мы покупаем или строим на машину" — for JVL's own design, export it from the CAD tool (heard "solegos"; the notes read SOLIDWORKS); for a purchased part, put in all its information. It looked to him as if "туда перестала поступать информация" — "Но может я неправильно на это смотрю?" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **Genadi's status.** "наши чертежи уже почти все там"; for data sheets he had not gone further. For "весь этот кабинет" he built the BOM and loaded "абсолютно все детовщицы"; "Для этой конкретной сборки все телевизоры загружены телевизоры, тощенные пауэрс и плай ну мейн сингс" (TVs, power supplies, main things); for the rest "я просто не входил ещё". Which cabinet is not named [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **Why it matters.** Val: "Без дельтащитц у нас не будет. Daita contracks" and without data contracts no bill of material ("пилот материю", heard). An export from MSBC of a BOM built by hand has no data sheets: for TVs "там будет сказана модель телевизора, но это всё". He wants to be sure "что нэйтан не фейкает эту сборку" — without data sheets he does not see how an agent can assemble a BOM [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **A gap is reported, not guessed.** Val: when something is missing, the agent "должен сказать, я не могу принять здесь решение. У меня не хватает"; then people supply it, rather than it being laid in blind. Genadi: "Абсолютно"; with a part number the agent finds the data sheet faster than he can — Val: "100% он найдёт быстрее" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].

## Only the BOM, not procurement

- Genadi had spent the day on procurement: "Вы мне просто сказали, что работой больше с прокюрментом, я целый день сегодня занимаюсь прокюрментом". Val: "Нет, нет… я не сказал, чтоб вы работали с протюрматом. Я был специфик, чтоб вы не работали с протюрматом, чтоб вы работали только под нейтоном… Прокюрман не надо делать." When Genadi said he meant organising procurement so it works, Val repeated: "не надо ничего этого делать… Фокусируйтесь только чтобы заработал… билов материал с нейтаном и всё" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]. ("протюрмат" / "прокюрман" = procurement; "нейтон" = [[wiki/people/nathan-carver.md|Nathan Carver]].)
- This keeps the Nov-16 split: procurement administration is Val's side; Genadi's is specs and data sheets — [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]].

## The procurement example Genadi raised

- JVL ordered modification parts — a cover to close the monitor ("крышечку для монитор закрыть"; the model words "base modifications preldo 21 модификэйт 2 новых" are **unclear**). Genadi asked the supplier for 50 sets ("50 цетов") because "нам надо сейчас IQ собирать". The supplier sent a packing list ("Fuller list", heard) and asked "$1500" for shipping; Genadi: "это не стоит… $1500 за посылка там 3 коробки" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- Procurement only wrote back "а почему так дорого?". Genadi: with the packing list's volume and weight, procurement could get its own quotation, and should see that the supplier added parts "которые не должны быть не надо. Нам их самолётом посылать?" (the notes read these as parts meant to come by ocean). What it should cost is said as "Хьюсти доллар" — the figure is **unclear**; the notes say only "far less". Who in procurement wrote is not named [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- "Упала между стульев" — no one caught it until he did today [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].

## The ruling — standards, plus an agent, not hands

- **Why not by hand.** Val: "то, что вы делаете это очень хорошо… Но это очень тяжело", and the chance of catching everything is small; "я боюсь, что вы у меня всего один. И я боюсь, чтоб вы не сгорели" doing mundane work; "мне… выгоднее переплатить на этом, чем вас замучать в этом" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **Val writes a standard from this call.** "Я сейчас возьму транскрипт и напишу стандарт." It goes into the knowledge base, "там есть репозитории, которые называются стандарты"; his AI-COO reads the standards before acting ("когда я открываю чат… я говорю акт CO… у него есть инструкция… посмотреть за стандарты"; "CO" / "сио" read as COO — **inference**). His example of a standard's output: the AI-COO may act itself or tell "меры гетми 3 котс" — read as "Mary, get me 3 quotes" (**inference**) [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]. Genadi: "Вы должны идентификай все частные случаи уан бай засунуть их туда, и тогда он будет работать" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **Genadi does the same.** "напишите стандарт… В гидхап"; "Все ваши знания должны лечь в стандарт" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **His own PO agent.** "сделайте себе эйджента. Которого вы открываете раз в день и говорите, посмотри на все POL… посмотри на стандарты и скажи мне, что не совпадает с стандартом" ("POL" / "пиоус" = POs). From that list he can tell each person what to fix — "скажи меры, скажи пете, скажи федя, скажи коле" (stock names, not a list of staff) — and stop "закрывать дырки" himself. Give it a persona: "ты мой, этот самый polit агент… Каждый раз ты открываешься, ты смотришь на стандарты". Genadi: "Good point… это надо сделать"; "это надо обязательно вау" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]].
- **The MCP loop.** Nathan already has an MCP for MSBC that Val uses with his AI executive ("для своего seo o"), but it covers only part — "30% 10% я не знаю". When Genadi's agent says it has no access, he asks it in the same chat to "напиши мне драфт. Us кейс. Фон нэйтан. Оф mcp", puts the use case in GitHub, Nathan adds it to the MCP, and "у вас получается луб" [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]. This is the same use-case route as [[wiki/decisions/2026-10-19-mary-asks-business-central-through-mcp-not-special-reports-and-nathan-adds-msbc-endpoints-from-ai-coo-use-cases.md]] (Nov-20 note there).

In one line: **Genadi's hours go to the BOM with Nathan; what he knows about buying is written down once as standards, and an agent, not Genadi, checks every PO against them each day.**

## How it sits against earlier rulings

- **Nov 16 split** — kept, and made sharper: no procurement work at all for Genadi — [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]] (Nov-20 note).
- **Nov 18 supplier loop** — the same rule that a missing data sheet is named by the agent, not filled by a person — [[wiki/decisions/2026-11-18-the-next-bom-spike-is-a-self-learning-supplier-loop-the-agent-finds-the-supplier-asks-for-the-missing-data-updates-the-data-contracts-and-reassembles-with-no-human-answers.md]] (Nov-20 note).
- **Standards repository** — [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] (Nov-20 note).
- **Who writes standards** — on Nov 16 Val told [[wiki/people/lev-rudky.md|Lev Rudky]] "я не буду писать за стандарты"; here he says he will write one himself from this transcript. Not a contradiction ruled on — see the open question on [[wiki/decisions/2026-11-16-lev-rudky-writes-the-standards-val-sends-him-short-bullet-points-instead-and-the-purchase-order-topic-becomes-a-po-standard.md]] (Nov-20 note).

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — write a standard from this call's transcript (the freight case Genadi described) and file it in the standards repository — due unspecified ("сейчас") — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — send Genadi the transcript ("Я вам отошлю транскрипт") — due unspecified — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — load drawings and data sheets for all parts into GitHub (done so far for one cabinet's main parts) — due unspecified — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — write his procurement knowledge as standards in GitHub — due unspecified — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — build his own agent that once a day checks all POs against the standards and lists what does not match; MCP gaps go to Nathan as drafted use cases — due unspecified — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]

## Open questions

- Is Nathan's agent BOM really built from data sheets? Val wants to be sure he "не фейкает эту сборку" — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- What should the 50-set monitor-cover shipment have cost, and which parts should not have gone by air? Genadi's figure ("Хьюсти доллар") is **unclear** — [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]

**§15.8:** clear — the $1,500 is a supplier freight quote, not anyone's pay. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
