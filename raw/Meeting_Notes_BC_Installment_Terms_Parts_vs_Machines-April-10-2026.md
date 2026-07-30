# Meeting Summary — Receivables Settings: Installment Terms & Product Differentiation
**Date:** April 10, 2026, 7:26 PM Eastern
**Duration:** ~18 minutes
**Segment:** Segment 1 of 3
**Attendees:** Val Levitan, Lev Rudky, Felipe Miranda Giorgi, Laura Escorcia

## Summary

The meeting opened with a discussion about how Business Central handles aged receivables for Chile operations, specifically the aging buckets (30 days late, 60 days late, etc.). Val established a critical point: all JVL sales are installment-based without exception. There are no lump-sum payment terms — every sale is structured so that a fraction of the total amount is due every 30 days. For example, a 6-month term means 1/6 of the total is due every 30 days, 2/6 should be received by day 60, and so on. Lev confirmed that Business Central's installment payments add-on can handle this structure.

Val then raised a second, interrelated concern: JVL never sells a complete machine as a single line item — machines are sold in parts (components). This creates a product differentiation problem. Specifically, machines may carry multi-month installment terms (e.g., 6 months), but parts and services should never have terms longer than 30 days. Val needs the system to enforce different payment terms based on what is being sold — machines get extended installment terms, while parts and services get short terms (30 days or less).

Lev initially indicated this was a separate topic from aging, but Val pressed the point that both are connected because the terms determine how aging is calculated. Lev investigated and reported that payment terms in Business Central are assigned at the customer level — not at the product or line-item level. The customer record carries default payment terms, and those flow onto the invoice. Val pushed back, asking how to handle the scenario where customer ABC has 6-month terms for machines but 30-day terms for parts.

Felipe mentioned that he had seen Elizabeth working on an invoice where she selected "part or machine" — suggesting some differentiation mechanism may already exist. Val reinforced that product categorization is standard practice, noting that some countries even tax parts differently from finished goods, so there should always be a way to identify product type.

Lev explained a fundamental constraint: when a sales order is shipped, the invoice generated has a single due date for the entire invoice. The installment payments add-on splits the invoice into multiple sub-entries (each with its own due date and amount), but this operates at the invoice level, not at the line-item level. If one line item has a 6-month term and another has 30 days, the system cannot generate two different payment schedules from one invoice. Lev's conclusion: separate sales orders would be required — one for parts and one for finished goods — to achieve different terms.

Val was not satisfied with this answer, believing the system should be able to handle product-level term differentiation without requiring separate orders. Felipe relayed a suggestion from Laura (from the Colombia team) about creating duplicate customer records (e.g., "ABC Parts" and "ABC Machines"), which Val rejected as a workaround for software limitations that Business Central should not have.

The segment ended with Val asking Lev to check with the consultant and revisit the issue at the next conversation. Lev acknowledged he would investigate further but expressed skepticism that the system could support line-item-level terms without separate orders.

## Decisions Made

- **All JVL sales use installment payment terms with no exceptions** — this is a confirmed business rule. (Stated by Val)
- **Separate customer records (ABC Parts, ABC Machines) are not an acceptable solution** — Val explicitly rejected this approach. (Decided by Val)
- **The parts vs. machines terms issue is deferred to next conversation** — Lev will investigate further before then. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Investigate whether Business Central can apply different payment terms to different product categories (parts vs. finished goods) on a single sales order/invoice, and check with the consultant | Before next meeting (TBD) | High | Blocking the ability to enforce short terms on parts while allowing extended installment terms on machines. Val believes it should be possible; Lev is skeptical. |

## Engineering Signals

### Confirmed Signals

- **REQ: Product-category-based payment terms** — Val explicitly stated that parts and services must never have terms longer than 30 days, while machines can carry multi-month installment terms. This is a business rule that the system must enforce: "We have a stipulation that parts can never be longer than 30 days." The system currently cannot do this at the invoice level.

### Suspected Signals

- **Possible ADR: Separate sales orders vs. single-order line-item terms** — Lev's finding that Business Central requires separate sales orders to achieve different terms per product type represents an architectural constraint. If confirmed after further investigation, this would require a workflow decision: either accept separate orders or pursue a customization.

## Open Questions

- Can Business Central support different payment terms per line item on a single invoice, or is this an inherent platform limitation requiring separate orders?
- What is the current mechanism Elizabeth uses when selecting "part or machine" on invoices — is it cosmetic or does it affect terms?
- Should JVL pursue a customization to Business Central if the platform doesn't natively support product-level terms?

---
*Processed from Teams transcript on April 11, 2026*
*Source meeting: Receivables Settings — Call with Felipe and 2 others, April 10, 2026*