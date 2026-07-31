# Meeting Summary — MRP Refinement
**Date:** June 1, 2026, ~3:30–4:11 PM ET (meeting) + June 2 follow-up chat with Nathan
**Duration:** ~40 minutes (meeting)
**Attendees:** Nathan Carver, Val Levitan, Lev Rudky, Mikhail Perelman

## Summary

The team reviewed the MRP (material requirements planning) tool Nathan is building. The tool pulls data from Microsoft Business Central through its API and produces a structured Excel workbook. Work on the Jira board is done up to task 860. Nathan is now on task 863 — generating the Excel workbook.

Nathan had emailed five setup questions. Lev gave the answers: the workbook is created once and then refreshed (not rebuilt each time), it stays user-owned, no new sheets will be added, and the metadata fields won't be used. The output file will have comment columns owned by the user. Mikhail asked for separate columns showing total on order and total on hand (quantity on hand) for the JVL Georgia location.

The team agreed to build in two phases. Phase 1 (task 863) covers forecast data, the bill of materials, open purchase orders, and lead times. Nathan will first make the tool generate the file, let Val and Mikhail check it looks right, then add automatic updating. Phase 2 covers the two items still marked red in DTP 847 — posted purchase invoice lines and vendor ledger entry — which Mikhail and Lev want so they can see whether each item was invoiced and paid.

Val confirmed every closed task is already linked to a requirement, and tasks 861, 857, 858, and 862 have theirs too. Only the two red items in 847 are missing requirements. Val coached Lev to write those as what he needs to see (amount due, amount invoiced, amount actually paid), not as instructions on which data source the engineer should use.

Nathan asked Mikhail to send a sample of the Excel file he uses today — the sheets and columns, with a few rows of data — so he can match the layout. Mikhail agreed; he uses two sheets (an "in" sheet and an "out" sheet) with parts list, descriptions, demand, total demand, and what is ordered.

Val raised two ideas for later: add a dashboard alongside or instead of Excel, and let the user issue purchase orders straight from the report — one at a time or all at once — to save time. Lev said they will think it through. Mikhail noted he prefers one combined purchase order per vendor (all items below reorder point, plus shipping), rather than a separate order each time a single item drops low.

Lev asked whether Nathan would be needed when Business Central is upgraded. Nathan said no — the tool uses the stable v1/v2 API; an upgrade would add a new version while keeping v2, so it should keep working unless an API is deprecated, which is unlikely.

On timing, Val noted Nathan is on schedule to finish by June 5.

### Follow-up — 1:1 chat with Nathan (June 2)

The day after the meeting, Nathan messaged Val and the plan shifted. He's still tracking to finish this week, but the Excel document is turning out much larger than expected. Based on the meeting, he questioned whether using Claude (the agent) is the best fit, and said the dashboard Val described is really a web-app with an agent for answering questions — he proposed combining the Business Central MCP/API with an application.

Val gave direction:
- Don't try to get Mikhail to change how he works — asking him to deviate isn't productive.
- Step 1 (now): build the dashboard with Claude-based inquiries.
- Step 2: add a trigger to flag the items and quantities to turn into a purchase order. This may remove the need for the Excel file; if Excel is still needed, tackle it then.
- Defer the Excel export until needed.
- Val's definition of the dashboard: a static report plus a Claude interface where Mikhail can give instructions.

Val described the target experience for direct PO placement: Mikhail reviews the report, spot-checks items, and checks the ones he wants to order (all or some, across all or some vendors). Before pressing a "GO" button, he can request a templated message draft to the vendor(s) asking for a shipping quote, a date the quantity will be ready, or other info (to be discussed with Mikhail). Pressing "GO" then generates all the POs in Business Central, combining parts by vendor.

Nathan's read: moderate effort. The hard part is getting the Business Central API calls right and verifying results. Agent-driven steps need verification gates — Mikhail confirming the order and reviewing the posted PO. He noted they may be using an agent where fixed procedural instructions (built into the MCP) would work better. He'll proceed with the dashboard and iterate. Asked for an estimate, he said he needs to break the bullet points into features first — roughly 8 hours. On June 2 he was fully on another project (an investor presentation June 3) and planned to get back into the MCP that night.

## Decisions Made

- **(June 2) Build the dashboard first; defer the Excel export.** The dashboard is a static report plus a Claude interface where Mikhail gives instructions. If Excel is still needed later, it becomes its own objective. (Val; Nathan to proceed and iterate)
- **(June 2) Don't ask Mikhail to change how he works.** Build around his current process. (Val)
- **(June 2) Direct PO placement is the step-2 goal** — select items → optional templated vendor message → "GO" generates POs in Business Central, combined by vendor. (Val; Nathan: moderate effort, needs verification gates)
- **Build in two phases (data scope).** Phase 1 = forecast data, BOM, open POs, lead times. Phase 2 = posted purchase invoice lines + vendor ledger entry. (Nathan, Val, Lev)
- **Output is created once, then refreshed** — user-owned, no new sheets added. (Lev — answers to Nathan's questions)
- **Generate first, automate later.** Nathan makes the tool produce the output, Val/Mikhail verify, then automatic updating is added. (Nathan, Val)
- **Requirements describe needs, not engineering.** Lev/Mikhail write what they need to see; Nathan decides how to pull it from the API. (Val)
- **Metadata fields not used.** (Lev)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Build the dashboard (static report + Claude interface for Mikhail) using Phase 1 data — forecast, BOM, open POs, lead times; defer the Excel export | This week (~June 5, 2026) | High | June 2 pivot; Excel doc grew larger than expected |
| 2 | Nathan Carver | Break the direct-PO-placement workflow into features and scope it (select items → templated vendor message → "GO" generates combined POs in Business Central) | TBD | Normal | Step 2; Nathan's rough estimate ~8 hrs after breakdown |
| 3 | Lev Rudky (with Mikhail Perelman) | Write the Jira requirements for the two red items in DTP 847 — posted purchase invoice lines and vendor ledger entry — stating what to show per item (amount due, invoiced, paid); attach to the feature | ~June 5, 2026 (before Phase 2) | High | Phase 2 can't start until these exist |
| 4 | Mikhail Perelman | Send Nathan a sample of the current MRP Excel file — sheets and columns, a few rows of data | TBD (soon) | Normal | Reference for data shape; still useful for the dashboard |

## Open Questions

- Is the Excel export needed at all, or does the dashboard + PO trigger replace it? (raised June 2)
- Exact form of the dashboard — Val: static report + Claude interface; Nathan leaning web-app + agent. To be refined as he builds.
- For PO placement: agent vs. fixed procedural instructions — Nathan thinks procedural (built into the MCP) may be better.
- What templated info Mikhail wants in the vendor message drafts (shipping quote, ready date, "other") — Val flagged "need to speak to Mikhail."
- Whether payment status can reflect actual bank payment (not just invoice issued/paid) — Lev noted tying in bank-payment data would be very difficult; tracking invoices is simpler.
- How many sheets the Excel file would have — depends on Mikhail's sample and the data shape (matters less if dashboard-first).

---
*Processed from Teams meeting transcript (June 1) + 1:1 Teams chat with Nathan Carver (June 2), on June 3, 2026*
*Source meeting: MRP - Refinement (June 1, 2026)*
