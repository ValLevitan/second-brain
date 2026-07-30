# Meeting Summary — Receivables Settings: Category-Based Terms & Subscriptions
**Date:** April 10, 2026, 8:35 PM Eastern
**Duration:** ~10 minutes
**Segment:** Segment 3 of 3
**Attendees:** Val Levitan, Lev Rudky

## Summary

Val opened by formally assigning Lev the undertaking to figure out how to handle the differentiation between payment terms for parts versus complete machines in Business Central. He then proposed an alternative approach: instead of differentiating by product type, terms could apply only to purchases above a dollar threshold — specifically, $15,000. This would effectively exclude most parts and small items from extended terms while capturing machine sales.

Lev responded that he could generate separate reports for parts versus finished goods based on shipment data, but this would not be reflected on the aged receivables report — which is the report Val needs for collections. Val confirmed that aged receivables is the report that matters.

Val then expanded the product categorization beyond just parts and machines. He outlined at least five distinct product/service types that JVL sells or will sell, potentially on a single invoice: (1) machines (finished goods), (2) connection services, (3) transactional equipment, (4) parts, and (5) service. Each category should carry different financial offers — different payment terms based on the product type. Val stated this is normal business practice: "A category should have different financial offers based on the category of the product."

Lev reiterated the constraint: a single invoice can only have one set of payment terms. If a sales order contains a machine and a part, the invoice generated from that shipment cannot split into two different payment schedules. Val pushed back, saying the system should be able to handle multiple product types on one invoice with different terms applied per category.

The conversation shifted to subscription services. Val raised the scenario of selling transactional equipment (e.g., $1,000) that comes with a monthly connection service (e.g., $5/month). He asked how subscription billing would work. Lev mentioned a subscription module that is built into Business Central (not an add-on), though he noted it's primarily designed for the purchasing side and he has never worked with it. Val was interested in whether the subscription concept — which introduces a separate billing category — could be leveraged for other product types.

Lev clarified that the subscription module is not a product category mechanism — it's a separate billing module for managing recurring charges. It does not solve the problem of applying different terms to different product types on the same invoice.

Val closed by leaving Lev with the undertaking: figure out how to handle multi-month credit terms in a restricted form so that JVL doesn't end up financing small amounts (e.g., $1,000 of parts over 10 months at $100/month). Val emphasized this is becoming more urgent because JVL is introducing transactional products, which would need entirely different terms from machines.

## Decisions Made

- **Product categorization is broader than just parts vs. machines** — Val identified at least 5 categories (machines, connection services, transactional equipment, parts, service) that need distinct financial treatment. (Stated by Val)
- **The $15,000 threshold approach is on the table** as a possible workaround for product-level terms. (Proposed by Val, not yet decided)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Figure out how to handle product-category-based payment terms in Business Central, specifically: (a) how to restrict multi-month terms so small-value items (parts, services) don't get financed over many months, (b) whether the subscription module can help, (c) whether a dollar threshold approach ($15K+) is technically feasible on the aged receivables report | Before next meeting (TBD) | High | JVL is introducing transactional products with different financial structures. The current system cannot differentiate terms by product category on a single invoice. This is a strategic capability gap. |

## Engineering Signals

### Confirmed Signals

- **REQ: Category-based payment terms** — Val explicitly defined 5 product categories (machines, connection services, transactional equipment, parts, service) that require different payment terms. This is a confirmed business requirement: "Each type of product is a category and a category should have different financial benefits or financial offers."
- **REQ: Subscription/recurring billing for connection services** — Val described a scenario where transactional equipment is sold with a monthly connection service fee ($5/month). This requires a recurring billing mechanism in Business Central.

### Suspected Signals

- **Possible ADR: Dollar threshold vs. product category for terms differentiation** — Val proposed terms applying only to purchases over $15,000 as a pragmatic alternative to full product-category-based terms. If the category approach proves infeasible in Business Central, the threshold approach would be an architectural decision.

## Open Questions

- Can the Business Central subscription module be repurposed or extended to support JVL's connection service billing model?
- Is the $15,000 threshold approach technically feasible within the aged receivables framework?
- Will JVL need a Business Central customization to achieve product-level terms, or is there a configuration-based solution?

---
*Processed from Teams transcript on April 11, 2026*
*Source meeting: Receivables Settings — Call with Felipe and 2 others, April 10, 2026*