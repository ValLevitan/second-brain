# Meeting Summary — MRP Dashboard Demo
**Date:** June 10, 2026, ~10:03 AM ET
**Duration:** ~31 minutes
**Attendees:** Val Levitan (Owner), Nathan Carver (Business Central tooling, Detroit Devops), Lev Rudky (Manager of MIS), Mikhail Perelman / "Michael" (Manager of Procurement)

## Summary

Nathan demoed a new purchasing-planning tool he built. It connects to Microsoft Business Central (MSBC) and takes plain-language commands: you give it an item number and a quantity, it reads MSBC, sees what's on hand, works out the shortage, and recommends a purchase-order quantity. It is close to being able to create the purchase order directly in MSBC.

Background: Michael originally asked for the old Excel tool he was used to. Val's view is that Excel isn't the right answer — a dashboard you talk to in plain language, tied directly into Business Central, beats pulling data out to Excel and pushing it back. Val directed Nathan to build the dashboard first; Excel would only ever be a later "phase two" export, and the dashboard had to come first regardless.

Two gaps showed up in the demo:

1. **Missing vendor and price data.** Planning 10,000 units of a test item, the tool found the shortage but had no vendor name or unit price, so it couldn't recommend who to buy from or at what cost. Val was firm: MSBC is the only source of truth, and vendor names, unit prices, and all vendor detail must live there. Lev clarified the vendors *are* in MSBC but the pricing is not. Michael noted some items were ordered through the old "Vision" system and never in BC, so their data may be missing. Everyone agreed the pricing needs catching up in MSBC — not a big job.

2. **Multi-level assemblies don't fully explode.** Val tested a 5-level sub-assembly. The list came back too short (Lev caught it). The tool stopped at an intermediate sub-assembly (it treated "buttons and counters" as a finished part) instead of drilling all the way down. Lev's rule: keep exploding every bill of material down to the purchasable items, even when an intermediate level shows stock on hand. Nathan will set the tool to go up to 20 levels deep; Lev confirmed nothing goes near that (~5 max) and will send Nathan the correct exploded list as a benchmark.

Because the tool is an MCP server with no data store of its own, everything stays in MSBC — exactly the single-source-of-truth setup Val wants. Once real purchase orders are placed, their prices become history the tool can use to estimate future costs.

Michael's case for Excel: he likes filtering by vendor, sorting, and printing by clicking. His real need is to see, per vendor, how many items he's ordering — e.g., if a vendor supplies 5 items and 3 are already on the order, add the other 2 while the shipment is going out. Val and Nathan showed this is all doable in plain language. Trade-off: Excel is faster for pure sorting and filtering, but it creates a sync problem with MSBC. Compromise reached: keep MSBC as the source of truth and add a cheap **export-only** Excel view for quick viewing — all actual changes go through the tool.

## Decisions Made
- **MSBC is the single source of truth** for vendors, prices, inventory, and purchase orders — no Excel as a master file. (Val, firm; confirmed by Nathan)
- **Proceed with the plain-language dashboard, not the Excel tool.** Excel is at most a later view-only export. (Val)
- **Catch up vendor pricing in MSBC** — vendors are loaded, pricing is missing. (All agreed)
- **Fix the tool to fully explode multi-level BOMs** down to purchasable items, up to a 20-level cap, instead of stopping at intermediate stock. (Val, Nathan, Lev)
- **Nathan to log a Jira task** for the multi-level explosion fix and **schedule a follow-up for Friday afternoon (June 12)**. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Create a Jira task for the multi-level BOM explosion fix (full explode, ~20-level cap, keep going past intermediate on-hand stock) | June 11 | High | Tool currently returns an incomplete shortage list |
| 2 | Nathan Carver | Implement the multi-level explosion in the tool; start after the location-billing work clears | Target Fri June 12 | High | Main blocker before the tool can plan full assemblies |
| 3 | Nathan Carver | Schedule the follow-up meeting for Friday afternoon (June 12) with Val, Michael, Lev | June 11 | Normal | Review the multi-level fix |
| 4 | Lev Rudky | Send Nathan the correct fully-exploded BOM list for the test sub-assembly as a benchmark | Before Fri June 12 | High | Nathan needs it to validate the fix |
| 5 | Mikhail Perelman (Procurement) | Enter vendor unit pricing into MSBC (vendors already loaded) | TBD | High | Tool can't recommend a vendor or cost without it; not formally assigned in the meeting |

## Open Questions
- Can MSBC hold a live vendor price list, or will prices come from purchase-order history? Nathan wasn't sure, and noted a stored list would go stale.
- Printing — Michael asked whether/how he would print from the dashboard. Not resolved.
- Who exactly owns the vendor-pricing entry into MSBC, and by when? Procurement is the natural owner; not firmly assigned in the meeting.

---
*Processed from Teams transcript on June 11, 2026*
*Source meeting: MRP Dashboard Demo (June 10, 2026)*
