# Meeting Summary — Receivables Settings: Aging Data Cleanup
**Date:** April 10, 2026, 7:44 PM Eastern
**Duration:** ~46 minutes
**Segment:** Segment 2 of 3
**Attendees:** Val Levitan, Lev Rudky, Felipe Miranda Giorgi, Laura Escorcia

## Summary

Val framed the core problem: the existing accounts receivable aging data is "contaminated." Before proper payment terms and credit limits were entered on a per-customer basis, the system had default or incorrect terms. The records from this period have incorrect aging calculations because the due dates were set based on wrong or missing terms. Val wants to clean up these records so the AR aging report is accurate for collections purposes.

Val initially considered whether to treat all contaminated records uniformly (ignoring the parts vs. machines distinction for historical data) and just age everything at one pace. He questioned whether the effort of retroactively fixing these records would be too excessive compared to the benefit.

Lev demonstrated the fix process by sharing his screen. He navigated to the Customer Ledger Entries table in Business Central, using Black Horse Entertainment as an example customer. The process is: open the customer record, view the open invoices in Customer Ledger Entries, switch to edit mode, and manually change the due date on each entry. The aged receivables report is driven by these due dates — if the due dates are wrong, the aging buckets are wrong.

While examining Black Horse Entertainment's records, the team discovered that several invoices actually showed correct aging. Val initially expected the data to be universally broken but found that for Black Horse, all displayed invoices were indeed expired and the amounts matched expectations ($2,250 per installment period for the invoice in question). This led to a realization: invoices issued after the installment payments add-on was properly configured would have correct due dates. Felipe confirmed that Elizabeth had been trained on setting terms and that installment payments had been in use "for a few months."

The team identified a specific problem with invoice 617 for Black Horse, which was created in October 2025 as "cash on delivery" (COD) — meaning it had no installment terms set at generation time. This is the type of contaminated record that needs correction.

Val established the cleanup rule: only invoices with non-zero remaining balances need due date corrections. Customers with zero outstanding balances can be ignored. The total scope is approximately 400+ line entries in the Customer Ledger Entries table, though many of these are installment splits of the same invoices.

A significant obstacle emerged: the Customer Ledger Entries table does not include a "payment terms" column, and adding one would require a customization. This means Laura cannot see the terms directly while reviewing the data. Val proposed a two-Excel approach: (1) Export the Customer Ledger Entries to Excel; (2) Use a separate Excel with customer names and their correct (current) terms from Felipe's master list; (3) Cross-reference the two to identify which due dates need correction.

The question of whether due dates could be bulk-updated via Excel upload was raised. Lev said he could potentially build an upload file and import process, but it would take effort and might not be more effective than manual entry depending on the number of records. Laura asked about this, and Lev acknowledged he'd need to build and validate such a tool.

Val and Lev clarified an important distinction late in the segment: the issue is not that terms are wrong — terms have been updated via Felipe's Excel. The issue is that due dates on historical invoices are wrong because they were calculated under old (incorrect) terms. Even though the customer now has correct terms, the already-posted invoices retain their original due dates. The fix is to compare each open invoice's due date against what it should be based on current terms, and correct the due date manually in Business Central.

Val raised another concern: terms that Elizabeth may have entered three months ago could have been overridden by the terms Felipe recently nominated. So the team cannot trust any historical term — they must compare everything against Felipe's latest Excel as the source of truth.

## Decisions Made

- **Only invoices with non-zero remaining balances need due date review** — zero-balance customers can be skipped. (Decided by Val and Lev)
- **Felipe's most recent Excel of customer terms is the single source of truth** for what the correct terms should be. Any previously entered terms (even Elizabeth's) are superseded. (Decided by Val)
- **Two-Excel cross-reference approach**: Export Customer Ledger Entries to one Excel; use Felipe's terms Excel as the second; Laura will create pivot tables and cross-reference to identify incorrect due dates. (Decided by Val)
- **Parts vs. machines differentiation is explicitly excluded from this cleanup** — the contaminated records will be aged uniformly without separating product types. (Decided by Val: "let's not separate parts from machines... let's just age it all at one pace")

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lev Rudky | Export the full Customer Ledger Entries table (all customers, open entries) to Excel and send it to Laura | ASAP | High | Laura needs this data to begin the due date review and pivot table analysis. This is the blocking first step. |
| 2 | Laura Escorcia | Create pivot tables from the Customer Ledger Entries export, cross-reference with Felipe's terms Excel, and identify invoices where due dates are incorrect based on current terms | TBD | High | This is the core cleanup work — approximately 400+ entries to review. Only non-zero balance invoices need correction. |
| 3 | Laura Escorcia | Manually correct due dates in Business Central for invoices identified as having wrong due dates | After undertaking #2 | High | Must be done in the Customer Ledger Entries table, one entry at a time, using the edit function Lev demonstrated. |
| 4 | Lev Rudky | Investigate whether an Excel upload/import process could be built to bulk-update due dates as an alternative to manual entry | TBD | Normal | Could significantly reduce Laura's manual work if the number of corrections is large. Lev needs to assess feasibility and effort vs. manual entry. |

## Engineering Signals

### Confirmed Signals

- **REQ: Payment terms column is not available in Customer Ledger Entries** — Lev confirmed that adding a terms column to this table would require a customization. The workaround is the two-Excel cross-reference.

### Suspected Signals

- **Possible REQ: Bulk due date update tool** — Laura asked about importing corrected dates via Excel. Lev said it's possible but needs development work. If the manual correction scope is large (400+ entries), this may become a formal requirement.

## Open Questions

- Exactly how many invoices have non-zero balances and incorrect due dates? The pivot table analysis will reveal this.
- Is Lev's potential Excel upload tool worth building, or is manual entry manageable given the actual number of corrections needed?
- Will the corrected due dates produce clean aging reports, or are there other data quality issues?

---
*Processed from Teams transcript on April 11, 2026*
*Source meeting: Receivables Settings — Call with Felipe and 2 others, April 10, 2026*