# Meeting Summary — Payment Hub Daily Service Fee Meeting
**Date:** July 24, 2026, 10:00 AM – 10:22 AM (Eastern)
**Duration:** ~13 minutes
**Attendees:** Val Levitan, Nathan Carver, Juan Martinez, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_Payment_Hub_Daily_Service_Fee-July-24-2026]]

## Summary

Val asked the group to explain the "daily fee" so he could close a knowledge gap. Nathan explained it is a configuration in Payment Hub assigned to a customer location; whatever fee is set flows onto the invoice when billing runs. Juan added it was envisioned as an upcharge for extra services (like enhanced performance or reporting). There is no live use of the fee today, but the group wants it ready: a fee set on a location's setup screen must carry all the way to a GL account in Business Central (MSBC) and be traceable — for example, a $5 daily fee showing up in the GL.

Juan flagged a naming problem: GL account 41421 is labeled "ACH service fee revenue," which is confusing, and other known fees (wallet fees, insufficient-funds fees, rejection/cancellation fees) are missing from the chart. Val's instruction: add codes for every fee already known, and reserve two extra fields with proper GL accounts in case something was missed — to avoid another redesign later.

Andrei asked whether to send an invoice on a day with zero transactions. Nathan initially proposed skipping invoices when there is nothing to charge, but Val, Juan, and Andrei agreed a consolidated daily invoice should go out by email for as long as an account is open, even if every line is zero — it reminds customers of potential fees and helps both sides reconcile. Nathan confirmed it would also push through MSBC as a zero invoice.

Andrei confirmed the daily fee field (41421) already exists in Payment Hub location settings. The group agreed it should default to zero for new locations and only be activated when a fee applies. Nathan will make sure Pavel's engineers design it that way.

Juan asked Val about the fee table in the final wallet ("Diwala") contract; Val asked Juan to request the fee table from the wallet provider instead, and recommended the same for "income" (as spoken in the transcript). Val also raised whether JVL's own bank fees belong in billing — his initial view is they are a cost of doing business, not a direct charge; he will think about it.

## Decisions Made

- **Add billing fee codes for all known fees, plus two reserved fields with GL accounts assigned** — to avoid future redesign when a missed fee appears. (Decided by Val, agreed by Nathan, Juan, Andrei)
- **Send a consolidated daily invoice by email as long as an account is open, even when all lines are zero** — transparency, fee awareness, and reconciliation for both sides; flows through MSBC. (Decided by Val, Juan, Andrei; Nathan agreed)
- **The daily fee field defaults to zero on new locations and is activated only if a fee applies** — the field already exists in Payment Hub location settings. (Agreed by Juan, Andrei, Nathan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Create billing fee codes for all known fees (wallet, insufficient funds, rejection/cancellation) plus two reserved fields, each mapped to a proper GL account | TBD | High | Blocks clean automated accounting design |
| 2 | Nathan Carver | Rename GL account 41421 to remove the "ACH" label | TBD | Normal | Requested by Juan; Nathan said it's easy |
| 3 | Nathan Carver | Make sure Pavel's engineers design the daily fee field to default to zero on new locations | TBD | Normal | |
| 4 | Juan Martinez | Dig through his notes and wallet exchanges to compile a list of banking-related fees (failed transfers, failed payments) and reconcile it with Nathan's codes | TBD | Normal | |
| 5 | Juan Martinez | Ask the wallet provider to send the contract fee table; do the same for "income" (as spoken) | TBD | Normal | Val redirected this from himself to Juan |
| 6 | Val Levitan | Consider whether JVL's own bank fees should appear in location billing | TBD | Low | Initial view: cost of doing business, not a direct charge |

## Open Questions

- Do JVL's own bank fees belong in location billing or Payment Hub, or are they purely an internal cost? (Raised by Val; Nathan unsure whether they'd go through location billing.)
- The full list of missing fee codes — pending Juan's compilation and the wallet provider's fee table.

## Dispatch Log

---
*Processed from Teams transcript on July 24, 2026, 12:01 PM (Eastern)*
*Source meeting: Payment Hub Daily Service Fee Meeting*
