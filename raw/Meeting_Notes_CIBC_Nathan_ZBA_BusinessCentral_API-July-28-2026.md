# Meeting Summary — CIBC (Michael Hill) + Nathan Carver: ZBA account + Business Central API integration

**Date:** July 28, 2026, 4:01 PM Eastern · **Duration:** ~13 minutes (the meeting; unrelated personal/background audio after ~00:23 in the recording is ignored)
**Attendees:** Val Levitan, Michael Hill (CIBC), Nathan Carver (JVL, owns the API integration).
**Raw transcript:** [[Meeting_Transcript_CIBC_Nathan_ZBA_BusinessCentral_API-July-28-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Context:** the design confirmation for the JVL/CIBC ACH → Business Central automation (the ZBA sweep the memory records at acct [held in Corporate Registry] / ABA [held in Corporate Registry], Nathan owns the API).

## Summary

The architecture is now settled and confirmed on both sides:
- **Second (ZBA) account is open.** Third-party ACH deposits arrive in **batch format** (multiple transactions per batch) into the ZBA account, which **auto-sweeps to a separate account at end of day**.
- **Microsoft Dynamics/Business Central API connector confirmed available** (Michael verified with CIBC's Business Net Banking the prior week) — so BC can integrate with the bank.
- **Nathan clarified the API's role (resolving Michael's "fuzzy" area):** JVL does **not** initiate payments through it — the API only **verifies transaction history** so JVL's system can reconcile the ledger. After the automation deposits and the ZBA moves the money at end of day, JVL's system calls the API to verify each deposit and amount. "Wherever we can get the transaction history" — BC API if available, else Business Net Banking.
- Michael had the account paperwork **ready to send**, held only until this call clarified the need; he presses send after the call, and CIBC's implementation team contacts JVL within a couple of days.

## Decisions Made

- **ZBA + end-of-day sweep confirmed; BC API used read-only for reconciliation (verify, not initiate).** (all)
- **Account paperwork released; CIBC implementation team to follow up.** (Michael Hill)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael Hill (CIBC) | Send account paperwork; implementation team to contact JVL | Next couple of days | High | Held pending this call |
| 2 | Nathan Carver | Build the BC-side API call to verify deposits/amounts for reconciliation | TBD | High | Owns the integration |

## Dispatch Log

---
*Processed 2026-09-24 (backlog batch 6). Source: 07-28 Decision on Leviton Account Integration: Opting for Phased Rollout (Plaud)*
