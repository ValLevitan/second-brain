# Meeting Summary — PROD test 2 with InComm kickoff
**Date:** November 20, 2026, ~10:02 AM – ~10:35 AM Eastern (recording)
**Duration:** ~33 minutes
**Attendees:** Andrei Klimovich (organizer), Val Levitan, Nathan Carver, Pavel Frolov, Igor Donis, Lev Rudky, Felipe Miranda Giorgi
**Language:** English (Igor partly in Spanish, Felipe translated)
**Raw transcript:** [[Meeting_Transcript_Andrei_PROD_Test_2_Billing_Runbook_and_Invoice_Terms-November-20-2026]]

## Summary

Andrei went through the open items for production test 2 and the first real location. Goal: go to the location next week (Wednesday or Thursday) with the back end ready — invoices issued and sent, wallet paid, money flowing location → JVL → InComm.

**Location billing.** Nathan has two runbooks: deployment and configuration check, and recovery of the stuck invoice from the first test (failed for technical reasons; Payment Hub sends a signal to reprocess it through Dwolla and MSBC). Since last month he was moved to other work; he needs feedback on the runbooks. Pavel: QA tested only up to the point where real money moves; the real-card flow through to Business Central cannot be tested in QA. Completing the recovery runbook works as a first integration test with Dwolla and MSBC; then another end-to-end test. Bank reconciliation with CIBC is still to be integrated (can go without it for a few). Nathan and Pavel's team (Dzmitry, Sergey) meet tomorrow (Saturday) at 9 AM; Pavel will have them read the runbook first. Nathan has an open question on terms "net 10 vs immediate".

**Location invoice terms.** Mock-up is ready; wording must be approved by Igor and Lev, then set up in MSBC. Payment is due on the invoice date. Igor (via Felipe): interest for late payment must be stated in the invoice or the customer contract; Igor needs Lev to change the terms in the system. Val: payment on the invoice date is not negotiable; interest starts later — 7 days, because ACH can take up to 5 days. Interest: 35% per year, simple daily, not compounded. No agreements are in place yet. Lev: the payment term is immediate to create; why not use the standard layout? Andrei: yes, standard layout; only the content must match the approved mock-up. Val: show the test invoice in one hour, no customization.

**Monthly connection fee invoice.** Not set up yet. Val: description "recurring monthly connection service"; recurring invoice on the 1st of each month; prorated by full days from the installation date (min 24 hours); the install date must be recorded in MSBC. This invoice goes to the operator (master): net 15, interest from day 31. Felipe asked if it is always the master; Val is 99% sure — if not, meet again. Andrei: Payment Hub requirements already describe this (master or location); keep it, simplify to master for now. Andrei's mock-up should be payer-type agnostic.

## Decisions Made

- **Location invoice: due on the invoice date; interest starts on day 7; 35% per year, simple daily, not compounded.** — ACH can take up to 5 days. (Val)
- **Use the standard MSBC invoice layout; only content must match the approved mock-up; no customization.** (Andrei, Lev, Val)
- **Monthly connection fee: recurring invoice on the 1st, prorated by full days from install date (min 24 hours), billed to the master; net 15, interest from day 31.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver, Pavel Frolov (with Dzmitry, Sergey) | Meet, go through the billing runbook and open items, then give expected dates | Nov 21, 9 AM | High | Pavel sent the invite |
| 2 | Pavel Frolov | Ask Dzmitry and Sergey to read the runbook before the meeting | Nov 21 | High | |
| 3 | Igor Donis, Lev Rudky | Set the payment term and produce a test location invoice for Andrei and Val to approve | Nov 20, ~11:35 AM | High | Val: "one hour" |
| 4 | Andrei Klimovich | Update the location invoice mock-up with interest from day 7 | TBD | Normal | |
| 5 | Andrei Klimovich | Tell Monica (contract) that the interest terms must be in the contract | TBD | Normal | |
| 6 | Andrei Klimovich | Make the content mock-up for the monthly connection fee invoice and share it | TBD | Normal | Net 15, interest from day 31 |
| 7 | Nathan Carver | Clarify the "net 10 vs immediate" terms question before any MSBC change | TBD | Normal | |

## Open Questions

- Is the monthly fee always billed to the master? Val 99% sure; Felipe doubts. (Felipe)
- When will CIBC bank reconciliation be integrated? Nathan says it was deprioritized. (Nathan)

## Dispatch Log

---
*Processed from Teams transcript on November 20, 2026, ~10:40 PM Eastern*
*Source meeting: PROD test 2 with InComm kickoff*
