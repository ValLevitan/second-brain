# Meeting Summary — MRP Dashboard: Purchasing Workflow & RFQ
**Date:** June 12, 2026, ~4:02 PM ET
**Duration:** ~1 hour 5 minutes
**Attendees:** Val Levitan (Owner), Nathan Carver (Business Central tooling, Detroit Devops), Lev Rudky (Manager of MIS), Mikhail Perelman / "Michael" (Manager of Procurement)

## Summary

Friday follow-up to the June 10 demo. The tool is Nathan's plain-language agent that reads Microsoft Business Central (MSBC) and plans purchasing. Two things got settled: the assembly-vs-purchase question from last time, and the shape of the full purchasing workflow Val wants built.

**Assembly vs purchase — resolved.** Last time the tool stopped exploding a sub-assembly. The cause is a flag in MSBC. If an item is marked "purchase," MSBC and the agent treat it as one bought part and don't explode it. If it's marked "assembly," the agent explodes it into all its sub-parts. So the flag works as intended — not a bug. Nathan's agent exploded the test component into ~120 purchasable parts, grouped by category (cabinet, sheet metal, plastics, electronics, power, display, audio). Lev confirmed the data is correct. The one odd item — an assembly flagged as a purchase — was a historical case Michael explained: because electronics had long lead times, JVL bought the components early, shipped them to the vendor at zero price, and received the finished board back. That item carries a BOM even though it's bought whole.

**Vendors still missing in MSBC.** The 120 parts came back with no vendors attached. Vendors and vendor-to-part links still need to be entered in MSBC before the agent can say who to buy from. Same gap as June 10, still open.

**The purchasing workflow Val wants.** Val laid out the full cycle and got agreement it's the right one:
1. Say how many machines/items to build.
2. Agent pulls the shortages (needed vs. on-hand and on-order).
3. An **editorial screen** where Michael reviews and applies his judgment — change quantities, pick vendors, drop or add items.
4. Agent sends an **RFQ (Request for Quotation)** to each vendor instead of going straight to a purchase order.
5. Vendor replies land in Outlook; the agent reads the emails and fills the editorial screen automatically. Val demoed this live with his own travel email (the agent pulled flight and hotel confirmations from Outlook on its own) to show the same works for vendor quotes.
6. Back-and-forth on the RFQ as needed; agreed price plus one line for DDP (Delivered Duty Paid — freight, duty, taxes).
7. On approval, the agent generates the purchase order; it goes for approval and gets emailed to the vendor.

Val's point throughout: Michael already does exactly this by hand (he calls his draft PO an RFQ); the steps are fixed and reproducible — **Shortages → RFQ → Reply → Purchase Order** — so they can be automated. Michael pushed back that too much data is missing today and that quantity decisions involve judgment (MOQ, price breaks at 15/20/100/300/500 pieces, parts shared across products, family molds, choosing among vendors). Val agreed Michael keeps the decisions, but they go through the editorial screen, not a separate manual process. Both agreed to build it step by step and test as they go.

Inventory accuracy underpins all of it — shortages are only as good as the on-hand count. JVL does a physical count in Georgia next week. Val told Nathan not to hold for it; keep building in parallel.

## Decisions Made
- **The MSBC purchase/assembly flag is correct and authoritative.** Purchase = single bought part, no explode; assembly = explode to sub-parts. (Lev confirmed; Val, Nathan)
- **Target workflow = Shortages → editorial review → RFQ → reply/negotiation → purchase order**, with an editorial screen where Procurement keeps the judgment calls. (Val laid out; Lev "satisfactory"; Nathan endorsed)
- **Vendor quotes auto-ingested from Outlook** by the agent via the MS365 connection, then shown on the editorial screen. (Val, demoed live)
- **DDP captured as a single line** (freight + duty + taxes) added after the vendor quote, not modeled per part. (Val)
- **Do not hold for the Georgia physical count.** Nathan keeps building async that week. (Val)
- **Break the workflow into Jira features with time estimates.** (Val directed Nathan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Build the exploded-view + RFQ flow: explode the BOM at several build quantities (e.g. 100/200/300), consolidate the same part across sub-assemblies, total by vendor, combine parts under a set dollar value into one order, then generate an RFQ per vendor showing last price, new quantity, and a DDP line | Async / ongoing | High | The workflow Val dictated on the recording; core deliverable |
| 2 | Nathan Carver | Break that workflow into Jira features and estimate time for each (decipher Val's recorded dictation into a task set) | Next | High | Val wants it in Jira before the build |
| 3 | Nathan Carver | Keep building async through the week of June 15 (Georgia physical-count week); do not hold | Week of June 15 | Normal | Val explicitly said don't hold |
| 4 | Mikhail Perelman (Procurement) | Enter vendors and vendor-to-part links (and pricing) into MSBC | TBD | High | Agent can't recommend a vendor or send an RFQ without it; carried from June 10, still not firmly assigned |

## Open Questions
- Vendor and pricing data in MSBC still not entered. Who owns it and by when? Procurement is natural owner; not firmly assigned. Blocks the vendor-consolidation and RFQ steps.
- What dollar threshold counts as a "low-value" part to combine into one order? Not specified.
- How much of Michael's quantity judgment (MOQ, price breaks, shared parts, family molds) gets encoded as rules vs. left to the editorial screen? Agreed in principle; specifics open.
- Michael remains skeptical full PO automation is feasible given missing data; agreed to build incrementally and adjust through testing.

---
*Processed from Teams transcript on June 15, 2026*
*Source meeting: MRP Dashboard Demo (June 12, 2026)*
