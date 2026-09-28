# Meeting Summary — CIBC (Sanjay, Michael Hill): ACH receiving-account architecture

**Date:** July 2, 2026, 11:07 AM Eastern · **Duration:** ~22 minutes
**Attendees:** Val Levitan; Sanjay Vishwanathan and Michael Hill (CIBC US).
**Raw transcript:** [[Meeting_Transcript_CIBC_ACH_Account_Architecture-July-2-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Context:** the design meeting behind the CIBC ACH → Business Central automation (the ZBA architecture later in production).

## Summary

Val specified his two-account design: a **receiving account that always sits at zero** — every incoming ACH gets an API reading ("how much is in this account now?"), then sweeps to a second **accumulation/transactional account**, preserving a clean stamped record per receipt with no intermingling. Michael translated it into banking terms (the zero-balance account records the deposit and the sweep) but pushed a simpler alternative: **one account integrated with Microsoft Business Central**, which reconciles receipts with amounts/timestamps directly — Val accepted the challenge to his architecture ("maybe there was an error in our architectural thinking") and chose to try the single-account path first. Mechanics: Monica already has Michael's directions and may have initiated the integration; the current open account can receive ACH and connect to Business Central. Sanjay's second-account paperwork explicitly deferred ("don't do it yet"). Escalation path: Val works with Monica + his tech; the heavy lifting is on the Business Central side, not the bank's; contact through Sanjay.

## Decisions Made

- **Try the single-account + Business Central integration before building the ZBA sweep pair.** (Val, adopting Michael's suggestion)
- **Second-account setup on hold.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val + Monica | Confirm/enable the account's BC integration settings | Urgent (Val's word) | High | Monica may have already initiated |
| 2 | Val's tech (Nathan's lane) | Drive the Business Central side of the integration | After #1 | High | "Most of the work occurs at Microsoft Business Central" |

## Dispatch Log

---
*Processed 2026-09-24 (backlog batch 5). Source: 07-02 Banking Architecture Pivot (Plaud)*
