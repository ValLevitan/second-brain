# Meeting Summary — Val/Nate Re-align
**Date:** May 6, 2026, 6:35 PM ET
**Duration:** ~31 minutes
**Attendees:** Val Levitan, Nathan Carver

## Summary

This was a JIRA grooming and re-alignment session between Val and Nathan to clean up Nathan's open BEPs under **IP 436 (Orchestration Platform)** and **IP 1015 (Location, Billing and Payment Orchestration)** ahead of the July 1 target date.

**BEP 2657 — Job Orchestration:** Nathan's coding work is complete. Sergey Tsimanov has added integration tasks underneath it, which brings the entire feature into completion by **May 15**. The only thing remaining on Nathan's plate is one small story to call an API in the customer management service (for Sergey to integrate). Nathan and Val created this story live during the call: **"Activate customer"** under BEP 2657, assigned to Nathan with Sergey Tsimanov as reporter. It landed in backlog and Nathan owes a description and additional details inside the story.

**BEP 2670:** Nathan determined this is redundant — the work it covered (transfer orchestration / ACH transfers) has already been split up and completed under BEPs 2657, 2666, and 2668. Decision: abandon/close it as if it never happened. Val updated the status.

**BEP 2696:** Nathan created this originally as a general "risk management" placeholder for items that have been talked about but never properly defined or scoped. Not needed for July 1. Val moved it to **backlog**.

**MSBC Configuration Work (Payment Hub):** Nathan flagged one outstanding piece of configuration work — configuring **Microsoft Business Central (MSBC) Accounts Receivable** to allow posting of received payments and closing of invoices. This is configuration only, no code. Val and Nathan placed it as a new story under **BEP 2692 (Invoice Posting / Location Billing)** rather than under 2657. Story title: **"Configure MSBC for payment posting"**, assigned to Nathan, Pavel as reporter, starting **Monday May 11**, estimated **1 day of work**.

**Alpha POS / Accounting Hand-off:** Val pushed Nathan on the alpha POS testing readiness. Nathan confirmed his connectors for **Dwolla and MSBC** are in place and he has a working sandbox with MSBC that can be used for alpha testing. The host-side connection is **Dima and Sergey's** domain, not Nathan's — they are setting that up. However, before an official sandbox can be cut for testing, the **accounting team needs to decide how they want to configure the MSBC accounts**. Val emphasized urgency because **Alka is only available until June 1** and Val explicitly does not want to miss that window. Nathan agreed to schedule a meeting with the accounting team on **Monday** (their established cadence), send an engagement email, set a clear agenda ahead of time pulled from prior action items, and invite Val.

## Decisions Made

- **BEP 2670 abandoned/closed** — work is redundant; covered by BEPs 2657, 2666, 2668. (Val + Nathan)
- **BEP 2696 moved to backlog** — risk-management placeholder, not needed for July 1. (Val)
- **MSBC payment-posting configuration** to be tracked as a story under **BEP 2692**, not BEP 2657 — fits invoice-posting umbrella better. (Nathan + Val)
- **"Activate customer" story** created under BEP 2657, assigned Nathan, reporter Sergey Tsimanov. (Val + Nathan)
- **Accounting-team meeting** to be scheduled on Mondays going forward; must close before Alka leaves June 1. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Nathan | Schedule meeting with accounting team on Monday cadence to resolve MSBC account configuration; send engagement email, build agenda from last meeting's action items, and invite Val | Before June 1 (Alka availability) | High | Blocks creation of the official MSBC sandbox for alpha-POS testing; Alka leaves June 1 |
| 2 | Nathan | Fill in description and details on the new "Activate customer" story under BEP 2657 (also rename to "Reactivate customer account" if desired) | This week | Normal | Sergey Tsimanov is the reporter and needs the spec to integrate; part of BEP 2657 closeout by May 15 |
| 3 | Nathan | Configure MSBC Accounts Receivable for payment posting (new story under BEP 2692) | Starting Monday May 11, ~1 day work | Normal | Configuration-only work needed for payment-hub end-to-end |
| 4 | Sergey Tsimanov | Complete integration tasks under BEP 2657 to bring the feature to completion | May 15 | High | External — not on Nathan's plate, but gates BEP 2657 closeout |

## Engineering Signals

No engineering signals detected in this meeting. This was operational JIRA grooming (BEP cleanup, story creation, scheduling) with no architectural decisions, new requirements, or solution proposals beyond what is already tracked in JIRA.

## Open Questions

- Does the new BEP 2657 story stay named "Activate customer" or get renamed to "Reactivate customer account"? Nathan said he'd go in and change it; outcome not confirmed in-call.
- Final MSBC accounts-configuration approach awaits the accounting-team meeting with Alka.

---
*Processed from Teams transcript on 2026-05-07*
*Source meeting: Val/Nate Re-align — May 6, 2026*
