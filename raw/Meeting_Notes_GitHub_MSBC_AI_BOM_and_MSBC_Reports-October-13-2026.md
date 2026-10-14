# Meeting Summary — GitHub-MSBC
**Date:** October 13, 2026, 4:32 PM – 5:24 PM Eastern
**Duration:** ~52 minutes
**Attendees:** Val Levitan, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_GitHub_MSBC_AI_BOM_and_MSBC_Reports-October-13-2026]]

Held in Russian.

## Summary

**Why Val wants this architecture.** Val opened by saying he wants to understand Genadi's doubts about the business architecture he is pushing. He is "almost sure" he is right but wants to find any mistake early. Genadi said he fully supports the AI agent pulling files from GitHub, sending them to manufacturing, getting quotes and placing orders. His one concern: all reports and operations need a locked, exact bill of materials (BOM) for every configuration of every product (for example 10 or 30 Flex configurations). Small differences matter; a missing cable to South Dakota is a real problem. BOMs can live in GitHub, but they must be locked. Genadi also said he does not lock BOMs alone; purchasing and production decide together.

**BOM as a test of AI understanding.** Val said the goal is not to save half an hour (or 4 hours) per BOM. The goal is to teach AI how JVL products are built. He expects AI to find many other efficiencies once it understands the product. The BOM is his black-and-white test and "control gate": Genadi builds a control BOM as the template; the AI then builds its own (maybe 70% right); the gap shows what is still missing in the setup. Val compared this to software, where JVL developers now program and test with Claude Code autonomously. He is about 90% sure the same will work in electromechanics.

**Data contracts, not CAD files.** Genadi suggested exporting designs from SolidWorks or other CAD so the AI can see the product structure (Flex has 2 layers of sub-assemblies, Slim has 3). Val disagreed: he would not feed it CAD files. He wants correct data contracts — plain-text .md files in the repositories that say what each electromechanical part gives out. With that, the AI should in theory assemble the whole product itself, at any number of layers. Later (maybe in a year) the AI could take a picture and the parts and build a preview in CAD itself. Genadi agreed, and added the AI must also be told business choices, for example ordering a monitor assembly in China as a separate sub-assembly. Val said AI tools have not made anyone work less, only faster and better.

**Vendor data.** Val needs administrative and financial data for each vendor (bank, contacts, admin) to come from the vendor itself into MSBC, in a format that can be loaded directly. Parts, semi-finished goods, products and services bought from the vendor come from GitHub. What does not work today is joining the admin/financial side and the technical side for the same vendor. Genadi said this is a format question to work out with Nathan. He also said he currently stores files in the repository by project, and Nathan should decide how to organize or tag them.

**Procurement reports must come only from MSBC.** Genadi said procurement needs a solid, always-current report. Val said the only source of truth is MSBC — prices, quantities, physical counts. Reports must come only from MSBC, not from GitHub or anywhere else. Misha, against Val's wish, got Lev to export MSBC data to Excel (a pivot-table report like he used decades ago). This freezes the facts, about once a month, and errors are tracked from memory. Val said that report must disappear. Misha is leaving; Val said this is probably better for the business because the company will rely on one source of truth.

**What is missing in MSBC.** Val's example: vendors do not send a transport invoice when goods ship, because JVL never asks for it. So MSBC does not know shipping time, and JVL does not know when to order. Lev knows what information is missing but does not push it. Val said the needed report may already exist in MSBC (or is easy to create), but it needs disciplined purchase-invoice administration.

**Who builds the reports.** Val: Lev's MSBC consultants know how to build academically correct reports; Nathan knows the API and can pull any endpoint, but needs to be told what to pull. Plan: the consultant builds correct reports and names the endpoints; Nathan links the endpoints through the API into MCP. Genadi summarized: make a template of the ideal report, check what MSBC has and lacks (revision, shipping date, transit duration), consultants add missing fields, Nathan pulls the data for the AI agent. Val then corrected himself: Nathan will not build a report inside MSBC; the consultant does that. Genadi asked why build a report in MSBC at all. Val: at first people need to check that MCP and the agent understand the parameters; a person like Elizabeth may not pull it right through MCP; accountants may need it. He is about 70% sure the MSBC report will be needed.

**Future AI agent vision.** Val described the agent asking a person (e.g. Elizabeth) to recount a part ("system shows 38, recount"), reading the sales forecast in BC, noticing a BOM revision in GitHub is out of date, asking for updated vendor quotes, and warning that a new order is due in 28 days. Genadi added the agent could compare part drawings and prices (same holes, same bends, why $30 more). Val mentioned the AI project manager in Minsk (Andrei Bosik and Dima Kovalchuk) that listens to meetings and creates Jira tasks.

**Three separate things.** Genadi proposed: BOM by AI in about 3 months is fine, but the report is needed now. Val: the report, the vendor data, the BOM, and the agent logic are separate things in parallel. GitHub–MSBC BOM sync has nothing to do with the Lev/consultant report. Val wants to hand the architecture to Genadi and Nathan to execute; he has no time to do it by hand. Misha should be off this work from next week.

**Microsoft.** Genadi mentioned an open-source ERP at about $30/month. Val: that is per user, and Microsoft costs about $100 per user. JVL may leave Microsoft (and maybe Jira) in some years, not now; first the agents must work reliably.

**Time off.** Genadi asked to take time off this week for work at home. Val agreed and told him to take full days. The recording ends as Val starts a point about visa regulations.

## Decisions Made

- **Procurement reports come only from MSBC; Misha's Excel-export report must go away** — MSBC is the single source of truth; Excel snapshots freeze facts and rely on memory. (Decided by Val Levitan)
- **The AI agent builds the BOM; Genadi checks it and finds why it is wrong, rather than fixing it for the agent** — the BOM is the control gate that shows whether AI understands the product. (Decided by Val Levitan; Genadi agreed)
- **Teach the AI through data contracts (.md files of what each part gives out), not by feeding SolidWorks/CAD exports.** (Decided by Val Levitan; Genadi agreed)
- **MSBC reports, vendor data, BOM sync, and agent logic are separate parallel workstreams.** (Decided by Val Levitan; Genadi agreed)
- **The MSBC consultant builds the MSBC reports and names the endpoints; Nathan links the endpoints into MCP.** (Decided by Val Levitan)
- **Genadi takes time off this week; Val approved full days.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Work with Lev on what the procurement reports need and what admin data is missing in MSBC; list the gaps ("1, 2, 3, 4") so Mery can get concrete work | This week (by Oct 16, 2026) [Needs Val's confirmation] | High | Prepare for Mery's return |
| 2 | Genadi Peari | After Lev, discuss with Nathan how to get the missing data (endpoints, MCP) | TBD | Normal | Val's order: Lev first, then Nathan |
| 3 | Genadi Peari, Nathan | Agree the format for vendor admin/financial data into MSBC, and how to organize or tag files in the repositories | TBD | Normal | Join admin and technical data per vendor |
| 4 | Lev's MSBC consultant | Build academically correct procurement reports in MSBC and name the endpoints | TBD | Normal | Val ~70% sure the report is needed |
| 5 | Nathan | Link the MSBC endpoints through the API into MCP | TBD | Normal | After the consultant names them |
| 6 | Mery | Enter the missing information into MSBC as directed (e.g. vendor transport invoices) | From week of Oct 19, 2026 [Needs Val's confirmation] | Normal | Proposed by Val; Mery back from vacation next week |

## Open Questions

- Will a report built inside MSBC be needed, or can everything come through MCP? Val is about 70% sure it will be needed. (Val Levitan)
- Who exactly on the consultant side builds the reports? Val thinks Lev may know most of it himself. (Val Levitan)
- Genadi's exact time-off days are not clear in the transcript. (Genadi Peari)
- Visa regulations point was cut off when the recording ended. (Val Levitan)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: GitHub-MSBC*
