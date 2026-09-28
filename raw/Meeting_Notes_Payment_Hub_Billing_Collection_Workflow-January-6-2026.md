# Meeting Summary — Payment Hub: Location Billing & Collection workflow

**Date:** January 6, 2026, 11:17 AM Eastern
**Duration:** approximately 42 minutes
**Attendees:** Val Levitan, Nathan Carver (walkthrough lead), Pavel Frolov, and per the Outlook invite Juan Martinez and Dzmitry Chudzinau. Plaud labels most speakers by number; Nathan and Pavel are addressed by name in the transcript, the others cannot be attributed line by line.
**Raw transcript:** [[Meeting_Transcript_Payment_Hub_Billing_Collection_Workflow-January-6-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Location_Billing_Collection", 11:00 AM–12:00 PM ET, organiser Val. Nathan and Pavel are both named in the transcript, so the pairing is confirmed on both keys.

## Summary

Nathan walked the team through the Payment Hub billing-and-collection workflow document — header and invoice-line creation against Business Central (MSBC), failure modes, alerting, retry behavior with the ACH provider (Dwolla), and the daily balance-check / payment-initiation cycle. The meeting was a requirements-shaping session: several rules were settled in the room, and open policy questions were parked for review.

**Division of labor between systems.** Val set the architectural boundary early: Business Central sends the actual invoice to the customer — not Payment Hub. "The Payment Hub should be exactly what the name is, it's a hub. It should not be really a brain of any sort, or a database of any sort." Business Central owns what is outstanding on an invoice ("that's what it does for a living"); Payment Hub decides which invoices to initiate payment on, because Business Central cannot juggle that logic.

**Daily cycle.** Payment Hub commits the final invoice posting overnight (around 1:00–1:30), then at 8:00 AM Central starts balance checks through the Dwolla endpoint before initiating ACH draws (Dwolla's cutoff is 9:00 AM Central; the start time must be configurable). Weekend and holiday payments are queued with Dwolla and settle the next business day; queued transactions can be cancelled if the account drains over the weekend. Whether to run balance checks on non-processing days was debated — there is a per-check fee, but Val noted it is only 17 cents, so it may be worth running anyway to compare against what is queued.

**The NACHA constraint on partial payment.** The room worked through what happens when the account cannot cover the full amount due across several invoices (the worked example: three invoices totalling $815, only $500 in the account). Val's ruling, tested by the group: a partial draw against a *single* invoice is possible but opens an easy customer dispute under NACHA, so JVL will not do it; a partial draw against the *total* is fine as long as each ACH transaction matches one invoice exactly.

**Which invoices to pay when cash is short.** Nathan proposed oldest-first as the simplest rule. Pavel countered that the system should choose the *combination* of invoices that brings in the most cash, and Val restated it — "combination of invoices that optimize the amount of cash brought into the company" — and adopted it ("That's a great point, Pavel"). Invoices that cannot be covered leave the location disabled.

**Insufficient funds handling.** On a failed balance check: mark the check failed, set the invoice status to insufficient funds, flag the location, disable the POS terminal(s) — all terminals if a location ever has more than one — and notify the operations team. Pavel added a requirement: the POS device must display a message when locked, whether the lock is manual or automatic. Reactivation needs a manual path (reactivate the location, resubmit invoices through Business Central); a manual balance check may be part of that flow, though Pavel warned that a mid-day balance check is a weak trigger for re-enabling, since funds can be gone again by the time the ACH window opens — left open.

**Balance-data regulation question.** Nathan flagged that balance checks return personal account information; JVL may not be allowed to *store* the actual balance without stepping into stricter regulation, though comparing against it is fine. Dwolla masks account numbers behind funding-source IDs, which may keep JVL clear. To be verified.

**Overdraft idea.** Val floated asking whether locations have overdraft protection on their account; the room suggested recommending overdraft in the Location Service Agreement rather than checking a flag. Val was unsure whether querying the account balance has practical value at all, but ruled to keep it in the requirement and option it out later if useless.

**Monthly statement.** The group liked having Business Central's monthly statement show the customer which invoices were paid and which are outstanding, to reduce disputes.

## Decisions Made

- **Business Central sends the invoice email; Payment Hub does not.** Payment Hub is a hub only — no brain, no database. (Val Levitan)
- **No partial payment of a single invoice** — each ACH transaction must match one invoice exactly, because a partial draw invites a NACHA dispute; partial coverage of the *total* across whole invoices is allowed. (Val Levitan)
- **When cash is short, initiate the combination of whole invoices that maximises cash collected**, superseding the oldest-first proposal; then disable the location for the uncovered remainder. (Pavel Frolov's point, adopted by Val)
- **Payment Hub decides which invoices to initiate; Business Central tracks what is owed.** (group)
- **The POS device must display a message when a location is locked**, manual or automatic. (Pavel Frolov)
- **Balance check stays in the requirements** even though its practical value is unproven — option it out later if useless. (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan Carver | Build more multi-invoice scenarios for the partial-coverage logic | TBD | High | He asked for at least two more worked scenarios |
| 2 | Nathan Carver | Verify regulations on storing account-balance data from balance checks | TBD | High | Dwolla's funding-source-ID masking may keep JVL clear |
| 3 | Nathan Carver | Learn how invoice emailing is triggered from Business Central | TBD | Normal | Prerequisite to finalising the delivery flow |
| 4 | Team | Review the failure-mode chart and set JVL's response policy per mode | TBD | High | Nathan: "something for our review when we actually make policy" |
| 5 | JVL | Consider recommending overdraft protection in the Location Service Agreement | TBD | Low | Raised as an alternative to querying an overdraft flag |
| 6 | Engineering | Define Dwolla retry strategy (rapid retries can look like an attack) | TBD | Normal | Dwolla publishes retry recommendations |

## Open Questions

- Whether a manual balance check should be able to re-enable a location, given funds can drain again before the ACH window (Pavel's objection) — explicitly left open.
- Whether JVL may store the actual balance figure, or only compare against it.
- Whether balance checks run on weekends/holidays (17 cents each) or only on processing days.
- The exact reactivation flow after an insufficient-funds lock.

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "DWALA" / "Douala" / "Duvalo" / "DWOLA" — almost certainly **Dwolla** (ACH provider), throughout (e.g. 00:11:43, 00:12:29, 00:18:22).
- "MSVC" (00:00:11), "MSNBC" (00:11:13), "MSPC" (00:14:16) — almost certainly **MSBC** (Business Central).
- "KLS" (00:24:01) — almost certainly **POS**.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 1)*
*Source recording: 01-06 Payment Hub Workflow and Business Rule Definition (Plaud)*
