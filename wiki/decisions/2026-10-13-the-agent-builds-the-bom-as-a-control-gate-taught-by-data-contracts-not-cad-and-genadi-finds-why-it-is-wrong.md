---
type: decision
title: The AI agent builds the BOM as a "control gate" for whether it understands JVL products — taught by data contracts (.md files), not CAD exports — and Genadi finds why it is wrong instead of fixing it; reports, vendor data, BOM and agent logic run as separate parallel workstreams
date: 2026-10-13
aliases: [BOM control gate, control BOM template, 70 percent right, data contracts not CAD, no SolidWorks export, what each part gives out, find the error not fix it, four parallel workstreams, report now BOM in three months]
source-count: 3
status: active
open-commitments: 1
open-questions: 1
---

# The agent builds the BOM as a control gate, taught by data contracts, not CAD (Oct 13 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-13-github-msbc-ai-bom-control-gate-and-msbc-only-reports.md|Oct 13 2026 4:32 PM "GitHub-MSBC" meeting]] (Russian) with [[wiki/people/genadi-peari.md|Genadi Peari]], who agreed on the points below. It is the next step on the thread sequenced at [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]], after [[wiki/decisions/2026-10-09-the-georgia-flex-pay-slim-bom-is-built-forward-from-genadis-github-source-by-agent-and-script-with-human-approval-by-end-of-october.md]]. All quotations [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] unless marked.

## Genadi's concern, as he put it

- He backs the agent itself: it should take reports and files from GitHub, send them to manufacturing, get quotations and place orders — "все это абсолютно коррект."
- His one point: every report and operation needs a **locked**, exact bill of materials for every configuration of every product — "на 10 конфигураций флексов или там 30" — with the exact count of each component. Differences can be very small, but "если мы солс дакоты не пошлем кабель… Вы понимаете, что будут?" The BOMs "могут быть и в гитхабе тоже", but they must be locked.
- He does not lock a BOM alone: "это обсуждение perchesing продакшн и все вместе решают как его лок."

## What was ruled

- **The goal is not saving time — it is teaching the AI the product.** Val: "я не воюю за то, чтобы сэкономить полчаса. Я воюю за то, чтобы научить… [AI] понимать, как у нас построен продукт", because then "мы найдём массу массу других [efficiencies]". Building a BOM by hand may take half an hour or "гдето 04:00" — "неважно".
- **The BOM is the black-and-white test.** If the AI cannot build the BOM, it is also making errors elsewhere that are harder to find; the BOM "для меня чёрнобелый… Контроллы гейт". Genadi builds a control BOM as the template; the AI then builds its own, maybe "На 70% правильно на 30% неправильно", and the gap shows what is still missing in the setup.
- **Genadi checks, he does not correct.** "Я хочу использовать в этот майлстоун изготовление билов матевер, чтобы он вышел от [агента]. А вы проверили правильно он сделал или нет и не поправили за него. Не поправили, а нашли ошибку. Почему он неправильно это сделал?"
- **Data contracts, not CAD files.** Genadi proposed exporting designs from SolidWorks or another CAD tool so the AI sees the structure (Flex has two layers of sub-assemblies, the Slim three). Val: "я бы не пытался скормить ему" that; instead "ДЕЙТА [contracts]" — say in a plain .md text file what each electromechanical part "отдаёт наружу". With that the AI should "Собрать весь продукт неважно, сколько лейерс", in theory. Later — "через год" — it could take a picture and the parts and build a preview in CAD itself. Genadi agreed ("Я, я полностью согласен").
- **The AI must also be told business choices.** Genadi: if JVL decides to order a monitor assembly in China as a separate sub-assembly, "Ему это надо сказать, иначе же он соберет по своему." Val did not dispute it.
- **Four separate streams, in parallel.** Genadi: the AI BOM "через 3 месяца" is fine, "но репорт нужно сейчас." Val: "Репорт нужно параллельно. Репорт это одно. С вендером это другое Билла материл это совершенно другое… Логика… этих агентов это абсолютно другое." And: the GitHub–MSBC BOM sync has "ничего общего" with the report Lev and the consultant must build — "Это 2 разные вещи." Genadi: "Да, абсолютно." The report stream is on [[wiki/decisions/2026-10-13-procurement-reports-come-only-from-msbc-and-the-excel-export-report-goes-away.md]].
- **Handed to Genadi and Nathan.** Val wants to hand this architecture to Genadi and [[wiki/people/nathan-carver.md|Nathan]] — "между вами и нэйтаном. Это будет сделано" — because he has no time to do it by hand; [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] is to come off this work from next week ("со следующей недели, надо убирать с этой сцены").

## Why Val is confident

He is "почти уверен, что я прав" but wanted to find any mistake early. He pointed to software, where JVL's developers now program and write tests autonomously with Claude Code, and is "гдето на 90%" sure the same will work in electromechanics. His other example: the AI project manager in Minsk that sits in meetings and creates Jira tasks, built by [[wiki/people/andrey-bosik.md|Andrey Bosik]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] ("AI прочих менеджер сегодня делает Андрей босик и дима Ковальчук"). He also said AI tools have not made anyone work less, only faster and better.

## The agent Val wants (his vision, not a plan with dates)

Reading the sales forecast in BC, the agent would see that 50 machines are due this month, notice that a BOM revision pulled from GitHub is out of date, ask for new vendor quotes and enter them in MSBC, and warn that a new order is due "через 28 дней"; it would ask a person such as Elizabeth to recount a part ("У меня показывает в системе 38 штук иди и пересчитай"). Genadi added that it could compare drawings and prices — Val: "такое же количество отверстий такое же количество изгибов? Почему эта детально $30 дороже?"

## How it sits against earlier sources

**Evolution, not contradiction.** Oct 5 set data contracts as the repo model ([[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]]); Oct 13 rules out CAD exports as the teaching input and names the BOM as the test. On Oct 9 Genadi said an agent BOM "will be 90% correct" and a hand reference must stay; Oct 13 turns that reference into Val's "control BOM" template. Genadi's Oct-9 point that building a BOM "is not a time-consuming part" ([[wiki/decisions/2026-10-09-the-georgia-flex-pay-slim-bom-is-built-forward-from-genadis-github-source-by-agent-and-script-with-human-approval-by-end-of-october.md]]) is met by Val's "not about time" point.

## Oct 19 2026 note — the agent writes the contracts; errors show at assembly

On [[wiki/meetings/2026-10-19-github-msbc-repositories-per-project-mery-purchasing-endpoints-and-ai-coo.md|Oct 19]] (English) Val and Nathan agreed the data contracts are generated by the agent from the data sheets and drawings, not written by hand, and Val said he intends "to catch these mistakes during the final assembly, because it should not assemble with improper data contracts" — the fix is made "at the source". Same idea as the control gate here, now applied to the contracts themselves [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]. Detail: [[wiki/decisions/2026-10-19-hardware-repositories-start-with-harness-display-and-sheet-metal-and-the-agent-generates-data-contracts-from-vetted-data-sheets.md]]. No control BOM was mentioned.

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — build a control BOM as the template the agent's BOM is checked against (Val: "я могу [Генадия] попросить построить") — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] *(stated as a method; no date or product named)*

## Open questions

- Who locks a BOM? Genadi says purchasing and production decide the lock together; Val answered "забудьте про это… вы сами будете лок этот" and moved on. Not settled on tape. — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
