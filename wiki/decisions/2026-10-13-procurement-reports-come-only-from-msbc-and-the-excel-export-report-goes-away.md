---
type: decision
title: Procurement reports come only from MSBC — the Excel-export report must go; the MSBC consultant builds the reports and names the endpoints, Nathan links them through the API into MCP; Genadi works out the gaps with Lev this week so Mary gets concrete work
date: 2026-10-13
aliases: [reports only from MSBC, one source of truth for procurement, Misha's Excel report, pivot table report, freezing the facts, transport invoice, consultant builds the report, Nathan links endpoints into MCP, 1 2 3 4 gaps for Mery, 70 percent sure the report is needed]
source-count: 4
status: active
open-commitments: 5
open-questions: 2
---

# Procurement reports come only from MSBC; the Excel-export report goes (Oct 13 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-13-github-msbc-ai-bom-control-gate-and-msbc-only-reports.md|Oct 13 2026 4:32 PM "GitHub-MSBC" meeting]] (Russian) with [[wiki/people/genadi-peari.md|Genadi Peari]]. All quotations [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] unless marked.

## How it came up

Genadi: for procurement to work, "Нам нужен солид, репорт, чтобы он был всё время актуальный." Val answered with the source-of-truth rule.

## What was ruled

- **MSBC is the only source.** "Единственный [source of truth], который должен существовать… это MSBC" — prices, quantities, the physical count. "Все… эти репорты должны выходить только… Только из MSBC не из гетхаба. Ниоткуда." Without it, he said, counts, prices or the vendor will be entered wrong.
- **The Excel-export report must go.** At Mikhail Perelman's request, against Val's wish, [[wiki/people/lev-rudky.md|Lev]] made him a report in the style he used decades ago; the data is exported to Excel and worked in a pivot table. That freezes the facts at a point in time — "например, раз в месяц" — and errors are followed from memory instead of being entered in MSBC. Val: "репорт на который смотрит миша. Он должен исчезнуть… И его не может быть." Genadi: "Конечно, это неправильно."
- **Why now.** [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] is leaving ("миша в принципе уходит"); Val said this is probably better for the business because JVL will rely on "уан сорс оф [truth]". The hand-over is on [[wiki/decisions/2026-10-08-mary-takes-over-mikhail-perelmans-ordering-role-with-training-from-october-19.md]].
- **Who builds what.** Lev's MSBC consultants know how to build "академически правильно" reports; [[wiki/people/nathan-carver.md|Nathan]] knows the API and can pull any endpoint but must be told what to pull. So: "я бы сказал консалт[анту] сделай мне академически правильно. Все эти репорты и укажи мне эти энд поинт"; then "попросил бы нейтона линковать все эти эндс через API в MCP." Val then corrected himself: Nathan will not build the report inside MSBC — "это должен делать консультант" — Nathan builds the link through the MCP protocol.
- **Genadi's part this week: sit with Lev first.** Genadi offered to prepare a report template himself; Val: "вы не можете подготовить шаблоны репорта. Вы должны сесть с лёвой" — Lev knows what the report should be and what administrative data is missing. First discuss with Lev what is missing, "потом… обсудить с нейтаном, как это получить." Aim: prepare for Mary's return so she gets concrete work — "вот 1234 нам не хватает. Давайте наладим процесс."

## What is missing in MSBC (Val's example)

When a vendor ships, it should send a transport invoice, so JVL knows the goods have left and MSBC records how long transport takes. Vendors do not send it "потому что мы их не требуем", and the arrival date is taken roughly from Mikhail — "Поэтому мы не знаем, когда нужно заказать." Val said such a report is already in MSBC or easy to create, but it needs a discipline of administering purchase invoices. Genadi listed the fields a good report needs: revision, shipping date and transit duration.

## Why build a report in MSBC at all?

Genadi asked why, if Nathan pulls the data through MCP. Val: at first people must check that MCP and the agent understand the parameters; a person like [[wiki/people/elizabeth.md|Elizabeth]] may not pull the report right through MCP; accountants may need it. "На 70% уверен" the MSBC report will be needed.

## Microsoft, for context

Genadi mentioned an open-source ERP at "$30 в месяц". Val: that is per user, and "Microsoft нам стоит $100 на на юзерах". JVL may leave Microsoft, and maybe Jira, "через какието годы" — not now; first the agents must work reliably.

## How it sits against earlier sources

**Evolution.** On June 1 2026 the MRP tool was moved off the Excel export onto a BC-API dashboard (see [[wiki/topics/business-central-erp-implementation.md]], June 1); Oct 13 rules the remaining Excel report out. On Oct 8 Genadi asked "Нам нужен иметь репорт?" and Val tied the report to the BOM work ([[wiki/decisions/2026-10-08-msbc-stops-being-the-bom-source-and-the-week-of-october-12-goes-to-ordering-without-mikhail.md]]); Oct 13 separates the report from the BOM sync. The GitHub/MSBC split of data owners is on [[wiki/decisions/2026-09-30-engineers-never-change-msbc-and-administration-never-changes-github.md]].

## Oct 19 2026 update — "move away from building specialized reports"; Mary asks through MCP; endpoints from AI COO use cases

In segment 2 of the [[wiki/meetings/2026-10-19-github-msbc-repositories-per-project-mery-purchasing-endpoints-and-ai-coo.md|Oct 19 "GitHub-MSBC" meeting]] (English; Val, Genadi, Nathan) Val said: "We need to move away from building specialized reports. It has to be done through a multi-contextual protocol" — Mary writes in Spanish or English and gets an answer. Nathan is to add more MSBC endpoints for end-to-end inventory control, driven by AI COO use cases Val writes; Nathan agreed. Val also said the count "is more or less okay now" and the real gap is purchase invoices (prepayments, vendor shipping notices, lead time) [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]. Ruling: [[wiki/decisions/2026-10-19-mary-asks-business-central-through-mcp-not-special-reports-and-nathan-adds-msbc-endpoints-from-ai-coo-use-cases.md]]. **Evolution:** MSBC stays the only source and MCP the way in; the endpoint list now comes from the use cases. The consultant and Lev's report work were not mentioned on Oct 19, so those items stand as written. The notes record the same [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]].

## Open commitments

- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — work with Lev Rudky this week on what the procurement reports need and what administrative data is missing in MSBC; list the gaps so Mary gets concrete work — due week of Oct 13 2026 — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [ ] Genadi Peari — after Lev, discuss with Nathan Carver how to get the missing data (endpoints, MCP) — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] *(Oct 19: discussed with Nathan and Val — Nathan adds endpoints from Val's AI COO use cases; Genadi reviews the use cases. Whether the Lev step happened first is not said [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]])*
- [ ] Lev Rudky's MSBC consultant — build academically correct procurement reports in MSBC and name the endpoints — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [ ] [[wiki/people/nathan-carver.md|Nathan Carver]] — link the MSBC endpoints through the API into MCP, once named — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] *(Oct 19: now framed as adding more MSBC endpoints for end-to-end inventory control from Val's AI COO use cases — [[wiki/decisions/2026-10-19-mary-asks-business-central-through-mcp-not-special-reports-and-nathan-adds-msbc-endpoints-from-ai-coo-use-cases.md]] [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]])*
- [ ] [[wiki/people/mary.md|Mary]] — enter the missing information into MSBC as directed (e.g. vendor transport invoices) — due from the week of Oct 19 2026 (proposed by Val; the notes mark it "Needs Val's confirmation") — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]

## Open questions

- Will a report built inside MSBC be needed, or can everything come through MCP? Val is about 70% sure it will be needed. — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]] *Oct 19: Val — "We need to move away from building specialized reports"; Mary asks through MCP. Whether any report inside MSBC remains is not said; still open [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]*
- Who on the consultant side builds the reports? Val thinks Lev may know most of it himself. — [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]

**§15.8:** clear — no pay or rates; software prices per user only. Val's remarks judging named people's work are not recorded.

## Sources

- [[raw/Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
