# Meeting Summary — Call with Felipe Miranda Giorgi
**Date:** March 31, 2026, 3:37 PM Eastern
**Duration:** ~27 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi

## Summary

Felipe and Val discussed ACH collections, credit terms, retroactive customer approvals, and sales strategy across three main threads.

**ACH authorization mechanics for parts invoices.** Felipe opened the call asking whether JVL needs per-invoice customer authorization to draw ACH, or whether a blanket/recurring authorization model is feasible. He noted that QuickBooks supports an "invoice accepted" flow and suggested JVL's ACH customer agreement could contain language such as "JVL may debit invoices due under agreement" or "JVL may debit amounts owed" to avoid per-invoice paperwork for parts/service. Val responded that while templated per-invoice execution is possible, the real problem is that customers will not consistently execute per-invoice paperwork. Val's preferred model: spell out terms on every invoice and draw via ACH at term maturity — not limited to parts, but applicable to any purchase.

**Credit terms and approval methodology for parts.** Felipe described the current pain point: technician signs invoice in the field, JVL emails the customer, customer lets invoice age, then another part goes out, and another — aging accumulates. Felipe asked whether parts should be COD, 10 days, or 30 days. Val was firm: COD is impractical, and the correct answer is **net 30 days for any customer who has passed credit approval**. Val emphasized the need to separate "term approval methodology" from "normalized terms" — parts accounts should not stretch to 12-month payments on a $5,000 part. Val acknowledged JVL currently lacks a credit approval cycle and methodology; he intends to publish a set of documents covering approval process, templated documentation to circulate to customers, and collection process. Val estimated 2-3 months to implement. He also said the current downturn in demand creates advantage — there's time for retroactive approval cycles without pressing sales pressure.

**Retroactive approval leverage strategy.** Val walked through how Felipe can drive customers through retroactive approval: when a customer needs parts but has no credit application on file, use COD as the lever. Never blame the customer — instead attribute friction to "head office restructuring" or "finance department guardrails in our new system that prevent issuing an invoice without payment first." Then offer help: "let me help you get proper terms that you deserve — here's the credit application."

**Transparency and customer alignment.** Val stressed that regardless of invoice size, constant transparency and constant account grooming with the customer — sending statements, showing available credit — is the way of life. A $5 invoice past term matters because the customer needs to know.

**Automation and payment links.** Felipe asked why JVL can't offer customers a "click here to pay" link against their bank account for ACH. Val: we probably can eventually, but not at current data automation level. JVL is switching from Bank of America to a smaller, friendlier bank and is creating an API between that bank and Business Central. Val cautioned "we need to walk before we run" — basic credit application, basic approval, basic customer-approval tracking in the system don't exist yet.

**Fire prioritization posture.** Val described his triage: he attends to fires, not smoldering issues. Payment automation is smoldering; credit methodology is the current fire.

**Sales strategy — vertical cabinet rollout.** Felipe asked how JVL will sell a new game for the existing vertical cabinet without customers assuming it's just an upgrade on their existing (possibly underperforming) machine. Val reframed the market opportunity: JVL has ~2,100 machines in locations, at best 1 per location — which is ~30% of the addressable market. 70% (~4,000 locations) don't have JVL machines. At 30% cover of those 4,000, that's 1,200 machines — roughly two years of sales at 600/year (Felipe's best year). The vertical market ceiling is even higher since JVL has sold fewer vertical machines.

**Freezing/reset issue — reputation management.** Val: the win-per-day revenue issues were driven by machines being out of commission 30-50% of the time due to freezing/reset bugs. Those issues are fixed. Val plans to release a message: "we found the problem, this is what it was." He proposes a repetitive messaging posture: 50% downtime recovered → stellar performer; it's not a math problem or a game problem, it's a fix that has been delivered. Val will offer samples to loyal customers — new software on their existing machines, monitored via QR codes, demonstrating pre/post performance. If the math makes sense for the customer, they buy; if it doesn't, they don't.

**Nebraska and Texas skill markets.** Val reported that the first Texas machine (previous version of skill, aligned with Light & Wonder's initial-skill-feature methodology, less binding than the original Vanilla-inspired feature / "notch") made $280/day net win. Juan delivered the data that day. Val expects subsequent machines to perform considerably better. New Nebraska software was submitted to the enforcement commission (Nebraska has no gaming commission — it's handled by the alcohol/enforcement authority) about a week prior; approval typically takes up to two weeks. Operators are lined up, machines are in place, RIS has been issued to Dennis. Felipe has been trying to reach Ray at Inamax and spoke to Dennis. Val confirmed Felipe should install the new Nebraska software now at Inamax for in-house testing purposes, and confirmed Felipe is not restricted in where to sell — machines sold from Georgia can go to Inamax.

## Decisions Made

- **Normalized parts term is net 30 days for approved customers.** (Val) COD rejected as impractical; 12-month payments on small parts amounts rejected.
- **Credit approval methodology to be formalized.** Val will publish documents covering approval process, templated customer documentation, and collection process. Timeline cited: 2-3 months.
- **Retroactive approval strategy: COD-as-lever, guardrails framing.** (Val) Never blame customer; attribute friction to finance department / new system guardrails; offer help to get proper terms.
- **Preferred ACH draw model: terms on every invoice, automatic draw at maturity** — not per-invoice customer authorization. (Val)
- **Felipe to install new Nebraska software at Inamax for in-house testing.** (Val authorized)
- **No geographic restriction on Felipe's sales.** Georgia-sold machines can go to Inamax and other markets. (Val confirmed)
- **Freezing/reset issue will be addressed through repetitive external messaging + loyal-customer sample program.** (Val)

## Engineering Signals

### Confirmed Signals

- **CAP: ACH-terms-driven automatic draw.** Val articulated the capability direction: every invoice spells out its terms; ACH automatically draws at term maturity; no per-invoice customer authorization required. Applicable to all purchases, not parts only.
- **CAP: Bank-to-Business Central API integration.** Val cited in-flight work to create an API between the new bank (replacing Bank of America with a smaller, friendlier bank) and Business Central.
- **REQ: Credit approval cycle and methodology.** Val committed to publishing formal documentation of the approval process, templated customer-facing documents, and collection process — currently absent from JVL.
- **REQ: Customer-visible statement and credit transparency.** Constant statement delivery and visible available credit to customer is a stated requirement of the operating model.

### Suspected Signals

- **Possible CAP: Customer "pay-by-link" with bank account / ACH transfer.** Felipe asked for this; Val said "we probably can, but not at current data automation level." Tabled but directionally acknowledged. *Val, does this warrant tracking as a formal capability for the bank-API initiative?*
- **Possible REQ: Parts-invoice acceptance mechanism (QuickBooks-style "accept invoice" → debit authorization).** Felipe raised this as an alternative path; Val's preferred ACH-terms model supersedes it, but the underlying need (auditable customer assent per draw) may still apply. *Val, track or discard?*

## Open Questions

- Which bank is JVL moving to (replacing Bank of America)? Not named in the meeting.
- Exact scope and delivery date of Val's promised credit-methodology document set — Val cited "2-3 months" for full implementation but no interim milestone.
- Nebraska enforcement-commission approval status — pending; expected within ~1 week of the meeting date.

---
*Processed from Teams transcript on April 13, 2026*
*Source meeting: Call with Felipe Miranda Giorgi — March 31, 2026*
