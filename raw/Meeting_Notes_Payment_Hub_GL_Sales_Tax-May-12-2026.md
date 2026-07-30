# Meeting Summary — Payment Hub Report and GL Account Structure
**Date:** May 12, 2026, 6:01 PM ET
**Duration:** 53m 43s
**Attendees:** Nathan Carver, Igor Donis, Val Levitan, Sean Riley, Juan Martinez, Lev Rudky (late join)

## Summary

**Purpose.** Nathan opened by saying Alka had told him Igor held the GL account codes Payment Hub needs to integrate with Business Central. Goal of the meeting: get the codes, get them created in the new BC sandbox Lev had set up, and surface any other MSBC setup detail Nathan should know about so the testing/engineering team can point alpha testing at real codes.

**Scope of codes requested.** Nathan needs five GL codes total for the Payment Hub flow: two for the sales invoice (card amount and service fee), one for customer payments, and two for accounts-receivable dimensions (as those are referred to in MSPC). Igor confirmed he had a draft list in a spreadsheet (revenues + cost of sales accounts highlighted in bright yellow) but the codes had not yet been physically created in Business Central. Val pushed for Sean's review of the actual codes before creation. Sean approved the revenue and cost-of-sales accounts as shown.

**Sandbox/production parity.** Igor committed to creating the five new codes in Business Central in both the sandbox (Caja de Arena / the new one Lev built) and in production by end of day, then sending the final list to Nathan so Payment Hub could start posting against real codes.

**Sales tax — the dominant topic.** Sean repeatedly pressed on whether Georgia sales tax applied to these transactions and whether any GL account existed for sales tax collected. Igor confirmed a single consolidated sales-tax GL account already exists in the master chart of accounts (created originally; not new) and that Avalara — a Business Central add-on — captures sales tax at transaction time by ZIP code and produces state-by-state reports for filing. Currently every state's sales tax posts into that single GL account.

Sean's concern was reconciliation: if month-end Avalara says $10K is owed across multiple states and the GL says $8K, how do you sort the $2K variance back to a specific state without per-state GL accounts? His proposal had two paths: either (a) create one GL account per state JVL operates in, or (b) keep the single consolidated GL account but ensure the postings carry a sortable field code (state or ZIP) so the data can be cross-checked against the Avalara state report. Sean indicated (b) is acceptable if the capability exists; Igor agreed to try to apply that recommendation.

Val challenged whether reconciliation is actually happening today and stated his belief that the accounting department "really doesn't reconcile anything." Igor demonstrated an Avalara report that breaks sales and taxes out by state, which Sean acknowledged would support state-by-state filings — the missing step is the cross-check back to the GL.

**Georgia complications.** Juan flagged in chat that Georgia uses county-based sales tax, with rates ranging from 6% to 9% depending on where the machine is technically sold to — confirmed by JVL's Georgia office. This intensified the need for ZIP-level granularity. Juan also noted that some Georgia COAM customers are flagged as tax-exempt at the master level (not the location level); Felipe had mentioned this to him but he hadn't yet drilled into why.

**Architectural debate — where does taxability live?** Nathan initially asked whether Payment Hub itself should signal taxable vs non-taxable; he believed taxability was tied to the GL account code passed to MSBC, since the BC test invoice he showed had a "Tax Group Code" defaulting to NT (non-taxable). Igor confirmed the tax group code should reflect the Avalara taxable code instead.

Val rejected the framing that Payment Hub should make tax decisions. He labeled this a **scope gap in the original Payment Hub design** and stated the correct architecture: Payment Hub passes the address and asks the accounting host (Business Central + Avalara) for an invoice; the accounting host decides taxable vs non-taxable based on jurisdiction and rate tables. Payment Hub may explicitly override with a "this transaction is non-taxable" signal where the business rule requires it (e.g., the gambling win-payout leg, which Val and Juan both suspected is non-taxable), but the *default decision authority* sits with MSBC/Avalara.

Lev confirmed the implementation pattern: MSBC supports a default tax setting at the customer level, with the ability to change the value on the document line before posting. So each line item is independently taxable/non-taxable, customer template seeds the default, and the operator (or upstream system) can override.

**Two transaction types.** Val drew a distinction Juan agreed with: in the Payment Hub flow there are two transactions — (1) the customer/player getting paid out their winnings, which is likely non-taxable across jurisdictions, and (2) the service-fee transaction between JVL and Incom, which Val argued *should be* taxable wherever services are taxable. Juan said he'd never seen a tax on a service fee in his US experience; Val countered with "come live in Canada." Juan accepted the action item to verify with Incom whether the Payment Hub transactions are in fact taxable in each state JVL operates in (not just Georgia).

**Tax-exempt customers.** Nathan asked how MSBC handles tax-exempt customers. Initial proposal was two customer templates (taxable Georgia COAM / non-taxable Georgia COAM) with Payment Hub picking the right one at customer-creation time. Sean noted the conventional pattern: tax-exempt customers provide a tax-exempt ID at registration; absent that ID, the customer defaults to taxable. Nathan committed to exploring MSBC's API for customer onboarding to see how granular the tax-status control can be.

**Next meeting.** Reconvene in one week, same time. Nathan to send the invite and explicitly include Lev this time.

## Decisions Made

- **Five new GL codes (two sales invoice + one customer payment + two AR dimensions) approved as shown in Igor's spreadsheet.** (Decided by Sean Riley; Val concurred)
- **Igor creates the five codes in BC sandbox AND production by end of day today**, then shares the final list with Nathan. (Decided by Igor with Val's concurrence)
- **Sales tax GL account stays as a single consolidated account** — no per-state proliferation — *provided* postings carry a field code that allows sorting/reconciliation by state. (Decided by Sean; Igor agreed to implement)
- **Architectural decision: Payment Hub will NOT decide taxability.** Payment Hub requests an invoice from MSBC; MSBC + Avalara determine taxable status per transaction line based on customer default and jurisdiction rules. Payment Hub may pass an explicit non-taxable signal where business logic requires. (Decided by Val; endorsed by Lev's confirmation of MSBC's default + line-override pattern)
- **Each transaction supports a taxable/non-taxable setting** (customer default, line-level override). (Decided by Val and Lev)
- **Reconvene in one week, same time, with Lev invited.** (Decided by Val and Nathan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Donis | Create the five new GL codes (sales invoice card amount, service fee, customer payment, two AR dimensions) in BC sandbox AND production; send final list to Nathan | EOD May 12, 2026 | High | Nathan is blocked on alpha testing of Payment Hub against real codes |
| 2 | Igor Donis | Implement state-level sorting/field-code capability on the consolidated sales-tax GL account postings so month-end reconciliation against Avalara reports can be cross-checked state-by-state | May 19, 2026 (next meeting) | High | Today there is no mechanism to identify which state caused a GL-vs-Avalara variance — reconciliation gap |
| 3 | Juan Martinez | Verify with Incom whether the Payment Hub service-fee transactions are taxable per state (not just Georgia); clarify why certain Georgia COAM customers are flagged tax-exempt at the master level | May 19, 2026 (next meeting) | High | Architectural choice on customer-template design depends on the answer |
| 4 | Nathan Carver | Explore MSBC API: how Payment Hub passes tax-status to MSBC, customer-template options for taxable vs non-taxable, and whether tax-exempt status can be set during customer onboarding via API | May 19, 2026 (next meeting) | High | Required input for the architecture change in #5 |
| 5 | Nathan Carver | Rearchitect Payment Hub so it requests invoices from MSBC without making the taxability decision; allow each transaction to carry a taxable/non-taxable flag with customer-default + line-override semantics | TBD (after #3, #4) | High | Addresses the scope gap Val identified; system being designed for many jurisdictions |
| 6 | Nathan Carver | Schedule follow-up meeting for one week out, same time; add Lev Rudky to the invite | May 13, 2026 | Normal | Lev's presence was missed today; needed for MSBC-side architectural questions |

## Engineering Signals

### Confirmed Signals

- **ADR: Payment Hub does not decide taxability — accounting host (MSBC + Avalara) does.** Val: *"Payment Hub should not be making decisions whether it's taxable or not. It should be asking for an invoice. And then whatever the hosting, the accounting host is — the accounting host makes a decision whether it's taxable or not. That's probably the architectural decisions that your system should be."* Endorsed by Lev's confirmation that MSBC supports default tax setting at customer level with line-level override before posting.

- **REQ: Each Payment Hub transaction must carry a taxable/non-taxable setting (customer default + line-level override).** Val: *"As we design our system, I'm thinking that each transaction should have a setting, taxable or non-taxable, because we're designing the system for many jurisdictions."* Lev: *"There is a default value and it's changeable on document line before posting."*

- **CAP: Sales-tax GL postings must be sortable/groupable by state (field code or equivalent) to support state-level reconciliation against Avalara.** Sean: *"If you have a field code by state, you could sort by that field code and then easily cross-check against the Avalara report."* Igor: *"I try to apply this recommendation."*

- **Scope gap (defect/REQ):** Val explicitly named *"a scope gap"* in the original Payment Hub design regarding tax handling — Payment Hub was built assuming it would decide taxability, which conflicts with the multi-jurisdiction architecture.

### Suspected Signals

- **Possible REQ: Customer-template proliferation for tax-exempt cases.** Nathan proposed maintaining separate MSBC customer templates per tax profile (e.g., taxable Georgia COAM vs non-taxable Georgia COAM), with Payment Hub selecting at customer creation. Not yet validated — depends on what Nathan finds in the MSBC API.

- **Possible REQ: Tax-exempt ID capture at customer onboarding.** Sean described the conventional pattern (collect tax-exempt code at registration; default to taxable if absent). Not yet committed for Payment Hub.

- **Possible ADR: Whether Payment Hub or MSBC owns the "two transaction types" distinction** (player win-payout vs Incom service fee). Val asserted the win leg is non-taxable and the service-fee leg is taxable, but where that classification is set (Payment Hub vs Incom contract metadata vs MSBC line type) wasn't decided.

## Open Questions

- Are the Payment Hub service-fee transactions actually taxable in each state JVL operates in? (Juan to verify with Incom — #3)
- Why are certain Georgia COAM customers flagged tax-exempt at the master record level? (Juan — #3)
- Does the MSBC API expose enough fine-grained control for Payment Hub to set per-customer tax status at onboarding, or is the customer-template approach the only path? (Nathan — #4)
- Does the existing single sales-tax GL account already capture a state/ZIP field on each posting, or does that field need to be added? (Igor — #2)

---
*Processed from Teams transcript on 2026-05-12*
*Source meeting: Payment Hub Report and GL Account Structure*
