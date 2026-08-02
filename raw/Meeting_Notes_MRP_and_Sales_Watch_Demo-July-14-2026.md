# Meeting Summary — MRP and Sales Watch Demo
**Date:** July 14, 2026, 1:03 PM Eastern
**Duration:** 1 hour 5 minutes
**Attendees:** Val Levitan, Nathan Carver, Lev Rudky, Mikhail Perelman
**Raw transcript:** [[Meeting_Transcript_MRP_and_Sales_Watch_Demo-July-14-2026]]

## Summary

Nathan demoed two tools built on Business Central: Sales Watch and MRP (manufacturing requirements planning). He had moved the calculations into code so the agent only orchestrates rather than computing — responses are faster and, from his own checking, the totals are accurate. His remaining accuracy concern is whether the tool reads MSBC configurations correctly. Val cut the sales portion short and asked to focus on MRP, saying he would review sales separately.

**The shortage list looked wrong, then didn't.** Lev thought the output was too short — only 5 items. The cause was that his change to the input journal had not been picked up. After he set demand to 500 units on a line and refreshed, the list grew to 179 parts and he said it looked much better. He still wants to dig deeper to confirm there is no underlying inconsistency. Separately he wants all lines pulled regardless of shortage, because that makes problems visible; Mikhail agreed he needs the full parts list, not only shortages.

**Column definitions took up much of the meeting.** The stale PO column displayed "false", which Val called not descriptive. Lev explained stale means aged POs, potentially redundant. Mikhail noted their longest delivery is four months, so 120 days; Val countered that 120 days can be legitimate but 180 days is genuinely stale, and settled on a yes/no indicator over 180 days. Mikhail flagged that deliberately split orders spread over months would also trip the flag.

Mikhail did not understand "on order" versus "order quantity". Nathan explained on order is the sum of outstanding quantities across open purchase orders, and order quantity is the derived recommendation — demand less stock less what is already on order. Val intervened to set a rule: any column that comes from MSBC must keep the MSBC name, because names must not diverge between the two systems. Nathan confirmed those two particular columns are not direct MSBC fields, so renaming them would not conflict, but the team left them as they are.

**Saving work in progress is a hard requirement.** Lev said a real run is around 400 lines for a single assembly and closer to double for a whole device, so reviewing and adjusting quantities will span days. He needs to save and resume, on both purchase orders and items. Nathan confirmed it is doable.

**Adjusted quantity.** A new column lets the purchaser override the suggested quantity. Lev had originally specified it should default to the net demand value so only exceptions need editing, then reconsidered. Mikhail made the call: it should be empty.

Mikhail raised the harder follow-on: if Business Central changes overnight — parts received moving from on order to on hand, or stock consumed by a shipment — how does he refresh his working file without losing his adjustments? Lev pointed out that yesterday's adjusted values may simply no longer be correct. Nathan said it is doable but the mechanism was not settled.

**Other points.** Mikhail identified parts in the output they never purchase (I-5120, 515508, line 140); Lev said that is a bill of materials cleanup on their side, not Nathan's problem. Nathan will add guardrails on how deep the bill of materials is traversed — currently four levels — to protect against loops and excessive depth; Lev said several hundred lines is normal and anything beyond a couple of thousand should warn or stop. Consolidation is already one line per item with no duplicates. PO and payment handling is explicitly phase two, once this piece is stable.

Val closed by pressing the bank account and API setup. It moves them from alpha test, which begins July 15 and runs about a week, into beta test. He was clear it is not mission critical but wants it soon, because banks are slow between receiving instructions and implementing them — so the instructions need to go out early if that routine is to be exercised during beta.

## Decisions Made

- **Stale PO becomes a yes/no indicator based on over 180 days** — 120 days can be legitimate given a four-month maximum delivery; 180 is genuinely stale. (Decided by Val Levitan, with Lev Rudky and Mikhail Perelman)
- **Columns sourced from MSBC keep their MSBC names** — names must not differ between MSBC and this tool. Derived columns (on order, order quantity) are not MSBC fields and are being left as-is anyway. (Decided by Val Levitan)
- **Adjusted quantity defaults to empty**, overriding Lev's original spec of defaulting to net demand. (Decided by Mikhail Perelman)
- **The output must list all parts, not only shortages** (Decided by Lev Rudky, Mikhail Perelman)
- **Purchase order and payment functionality is phase two** — stabilise the planning output first. (Decided by Lev Rudky)
- **Bill of materials traversal gets depth and volume guardrails** — several hundred lines is normal; beyond a couple of thousand should warn or stop. (Decided by Nathan Carver, Lev Rudky)
- **Bank account and API setup is prioritised** to enable the beta test, though not mission critical. (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Implement the column changes from Lev's email — line numbers, unit of measure, unit cost, top-level part number | Week of July 14 | High | Nathan expected this to be quick |
| 2 | Nathan Carver | Add save and resume of work in progress, for both purchase orders and items | TBD | High | Reviews span days at ~400 lines per assembly |
| 3 | Nathan Carver | Add the adjusted quantity column, defaulting to empty | TBD | High | Purchaser overrides the suggested quantity |
| 4 | Nathan Carver | Provide a way to refresh a saved file against changed Business Central data while preserving adjustments | TBD | High | Mechanism not settled; Lev flagged that stale adjustments may be wrong |
| 5 | Nathan Carver | Output all lines regardless of shortage, not only shortages | TBD | High | Both Lev and Mikhail asked for the full list |
| 6 | Nathan Carver | Change the stale PO column to a yes/no indicator on the over-180-days rule | TBD | Normal | Currently displays "false" |
| 7 | Nathan Carver | Add guardrails on bill of materials traversal depth and line volume | TBD | Normal | Guard against loops; warn or stop beyond ~2,000 lines |
| 8 | Nathan Carver | Lay out the tasks in Jira based on this meeting's undertakings | TBD | Normal | Val asked directly |
| 9 | Nathan Carver | Send the bank the account and API setup instructions | As soon as possible | High | Gates the move from alpha to beta test; banks are slow to implement |
| 10 | Nathan Carver | Schedule a follow-up meeting the same week to review the iteration | Week of July 14 | Normal | Agreed so they can iterate quickly |
| 11 | Mikhail Perelman | Read Lev's email specifying the required columns and their order | TBD | Normal | He confirmed he had not read it during the call |
| 12 | Lev Rudky, Mikhail Perelman | Remove the parts they never purchase (I-5120, 515508, line 140) from the bill of materials | TBD | Normal | Lev confirmed this is their cleanup, not Nathan's |

## Open Questions

- How to refresh a saved working file against changed Business Central data without invalidating quantities the purchaser already adjusted. Raised by Mikhail Perelman; Lev Rudky flagged the correctness risk; Nathan Carver said it is doable but no mechanism was agreed.
- Whether the short shortage list was entirely explained by the journal not refreshing, or whether an underlying inconsistency remains. Raised by Lev Rudky, who said he needs to dig deeper.
- How assemblies used and their quantities will be shown in the output. Raised by Mikhail Perelman; Lev Rudky said the top-level item is not in there yet.

## Dispatch Log

---
*Processed from the saved raw transcript on July 28, 2026 — backfill of a capture that saved the transcript but never produced a summary.*
*Source meeting: MRP and Sales Watch Demo*
