# Meeting Summary — Review Payment Hub MSBC Configurations
**Date:** July 20, 2026, 2:07–2:40 PM Eastern
**Duration:** ~34 minutes
**Attendees:** Nathan Carver, Igor Donis, Sean Riley, Lev Rudky (Val Levitan attended but did not speak)
**Raw transcript:** [[Meeting_Transcript_Payment_Hub_MSBC_Configurations-July-20-2026]]

## Summary

The team reviewed how Payment Hub transactions should be configured in Microsoft Business Central (MSBC) before moving to production.

**Dimension codes.** Igor confirmed the cash flow dimension G1 must be 0107 ("services rendered") on all revenue lines. The G2 intercompany code must always be 0, because all Payment Hub operations are with third-party customers, not related companies. These codes are used only for the cash flow report. Sean noted that if the report depends on them, every transaction needs them filled in, and asked for a block that prevents posting an invoice without the G1 code. Nathan said the system can enforce that, and G2 can default to 0.

**Taxes.** Payment Hub will use AvaTax, but every line item is non-taxable — Juan Martinez previously confirmed zero taxes. COAM customers will be set as tax exempt on the customer card.

**Payment terms.** Nathan thought terms might need to be Net 7, but Sean explained COD is correct: the invoice and the draw on the customer's account happen the same day, and Net 7 would wrongly tell customers they have seven days before money is taken. Val had originally required that money close daily so there is never a credit risk. In MSBC, COD invoices post immediately (the invoice number switches from a CS/SO prefix to a PS prefix), which the group agreed is fine. The team confirmed a posted invoice's GL entries match Igor's mapping.

**Journal.** The customer payment journal the code writes to is named "Payment Hub" and lives under the Cash Receipts Journal batches. Confirmed correct.

**Access.** Igor does not have credentials for one AvaTax configuration item (related to the email points from Nathan). Lev can grant Igor full permissions in the test/sandbox environment but prefers not to change tax settings himself.

## Decisions Made

- **Keep COD payment terms for Payment Hub customers (not Net 7)** — the customer is charged the same day the invoice is issued, so Net 7 would set the wrong expectation. (Decided by Sean Riley, agreed by Nathan Carver)
- **G1 cash flow code = 0107 on revenue lines; G2 intercompany code = 0** — all Payment Hub business is with third parties. (Decided by Igor Donis, agreed by Nathan Carver and Sean Riley)
- **All Payment Hub line items non-taxable in AvaTax; COAM customers set as tax exempt** — Juan Martinez previously confirmed zero taxes apply. (Confirmed by Sean Riley and Nathan Carver)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Configure COAM customers in MSBC: COD payment terms, domestic, G1 code 0107, tax exempt | TBD | Normal | Customer card setup |
| 2 | Nathan Carver | Add a system rule that blocks posting an invoice unless the G1 cash flow code is filled in, and default G2 to 0 | TBD | Normal | Requested by Sean |
| 3 | Nathan Carver | Generate a full example cycle (invoice through posting) in the staging environment for the team to review and approve | TBD | Normal | Thumbs up/down review of configurations |
| 4 | Lev Rudky | Grant Igor full permissions in the MSBC test/sandbox environment | TBD | Normal | Igor lacks credentials for an AvaTax configuration item |

## Open Questions

None.

## Dispatch Log

[Empty — no dispatch yet.]

---
*Processed from Teams transcript on July 20, 2026, 4:05 PM Eastern (scheduled watcher run)*
*Source meeting: Review Payment Hub MSBC Configurations — July 20, 2026, 2:00 PM*
