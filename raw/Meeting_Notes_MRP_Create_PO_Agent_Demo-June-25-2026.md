# Meeting Summary — MRP - Create PO Demo
**Date:** June 25, 2026, 5:02 PM ET
**Duration:** ~43 minutes
**Attendees:** Val Levitan, Nathan Carver, Lev Rudky, Mikhail Perelman

## Summary

Nathan demoed the AI agent tool that creates purchase orders in Microsoft Business Central (BC). He walked through the workflow: enter a top-level assembly and quantity (e.g., 500 units), the agent explodes the BOM, calculates shortages net of on-hand stock and open POs, identifies vendors, and drafts POs directly in BC.

Of 32 component parts, 9 had vendor info configured in BC and could be processed immediately. 23 parts had no vendor item data — the main blocker. Where two vendors are eligible for the same part, the agent presents a cost comparison and lets the user choose.

Lev asked about the "requested receipt date" field on POs — it's not currently populated by the agent. Nathan agreed to add it as an interactive prompt. Mikhail confirmed some vendors operate in CAD, not just USD, so the agent needs to handle multi-currency by vendor.

Lev and Mikhail raised the idea of feeding the agent a file of multiple part numbers and quantities instead of entering them one at a time. Val pushed back firmly: the file-based approach recreates the old Excel workflow he's trying to eliminate. Val's position is that users should interact with the agent conversationally — same logic they'd apply in Excel (sort by vendor, add non-shorted parts) but spoken directly to the agent instead.

Val emphasized that BC must be the single source of truth. Mikhail's comfort with Excel comes from relying on personal memory and visual manipulation, but that information needs to live in vendor cards so the whole company can access it. Incomplete vendor data is the root problem to fix, not a reason to fall back to Excel.

Screen sharing from Nathan didn't work in Teams for Val (recurring issue). They briefly tried switching to Google Meet but it didn't work for Mikhail. Val asked Nathan to continue working and said he'd follow up in a separate meeting with Mikhail and Lev in Russian.

## Decisions Made

- **Agent will prompt interactively for requested receipt date** — needed on every PO. (Decided by Lev/Nathan)
- **No file-based batch input for now** — Val vetoed the Excel/text-file intermediate step; agent should handle multi-part orders conversationally. (Decided by Val)
- **BC is the single source of truth** — vendor card data must be complete; no Excel workarounds. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan | Load vendor item catalog spreadsheet into MSBC dev environment | TBD | High | Needed to hydrate the 23 parts missing vendor info so a full PO run can be tested |
| 2 | Nathan | Add "requested receipt date" as interactive prompt when the agent creates a PO | TBD | High | Required field on POs that the agent currently skips |
| 3 | Nathan | Handle multi-currency (CAD/USD) per vendor in the PO agent | TBD | Normal | Mikhail confirmed some parts are bought in Canadian dollars |
| 4 | Lev | Review PO output in MSBC dev environment and identify additional required fields | TBD | Normal | Nathan created two draft POs (including #303) for Lev to inspect |

## Open Questions

- What other PO fields beyond "requested receipt date" need to be populated by the agent? (Lev to determine after reviewing dev environment)
- How should the agent handle ordering parts that aren't in shortage but the user wants to add to a vendor PO anyway? (Raised by Mikhail, not resolved)
- What's the workflow for keeping vendor pricing updated in BC going forward — vendor sends price sheets, or checked online? (Nathan raised, deferred)

---
*Processed from Teams transcript on June 26, 2026*
*Source meeting: MRP - Create PO Demo*