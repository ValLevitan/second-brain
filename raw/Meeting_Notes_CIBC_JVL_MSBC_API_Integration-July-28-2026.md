# Meeting Summary — CIBC/JVL ACH + Microsoft Dynamics API Integration
**Date:** July 28, 2026, 4:00 PM Eastern
**Duration:** ~13 minutes
**Attendees:** Michael Hill (CIBC), Val Levitan (JVL), Nathan Carver (JVL)
**Raw transcript:** [[Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026]]

## Summary

Call to confirm how the new CIBC account structure for JVL will work and what role an API needs to play.

**Account structure (settled).** The second account is already open and set up as a Zero Balance Account (ZBA). Deposits arrive into the ZBA from a third party in batch format — one batch holds multiple transactions. At the end of each day the ZBA automatically sweeps those funds out into a separate account. Michael confirmed his side of the setup is already built; he was only holding it until this call.

**What the API is actually for.** The group clarified that JVL's system sits at the end of the chain. It does not need to initiate any transactions — it only needs to read the daily transaction history to verify each deposit and its amount, so JVL can reconcile its own ledger. Whatever source gives the daily transactions (a Dynamics API, or another CIBC API returning balance/transactions) is acceptable.

**Microsoft Dynamics integration.** CIBC can integrate Microsoft Dynamics into its Business Net Banking; the connector is approved. Once integrated, Business Net Banking transactions feed into Dynamics, where JVL could see date, dollar amount, and sender. Michael's view: Dynamics would mostly duplicate the transaction data into its own ledger for faster reconciliation, and does not need to be central. Val's hunch (unproven): because CIBC is already integrated with Dynamics and JVL runs Dynamics Cloud on the latest version, the integration may already be more capable than assumed — possibly an easier path than building what they were calling an API.

**Batch detail.** Open point: whether a batch amount, once in Dynamics, still shows as the aggregated batch or as itemized transactions. Michael can set up a report in Business Banking that drills into a batch — e.g. a $30,000 payment clicked open to show the individual senders and amounts. Val asked that the detail be as complete as possible: timestamps and any banking/service/transactional charges, delivered as close to real time as possible.

**Decision on scope.** Proceed with the implementation as-is. Do not set up a transmission service for now — that would only be needed if JVL wanted to run its banking primarily through the Dynamics interface. Start with the current approach (ZBA sweep + Business Banking batch-detail report) and expand later if needed. Nathan will get Business Net Banking access to see the interface and detail report firsthand, then judge whether it meets the need or should be pressure-tested over a couple of months.

## Decisions Made

- **Proceed with the ZBA account structure as designed** — batch deposits land in the ZBA and sweep to a separate account at end of day; Michael's setup is ready. (Michael, Val)
- **API role is read-only verification** — JVL pulls daily transaction history to reconcile its ledger; it will not initiate transactions. (Val, Michael)
- **No transmission service for now** — revisit only if JVL decides to use the Dynamics interface as its primary banking front end. (Michael, Val)
- **Deliver batch detail via a Business Banking drill-down report** rather than relying on the Dynamics integration for it. (Michael)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael Hill (CIBC) | Submit ("press send") to move the implementation forward right after this call | July 28, 2026 | High | [External — manual follow-up needed] |
| 2 | Michael Hill / CIBC | Have someone contact JVL to advance the implementation before end of week | By July 31, 2026 | High | [External — manual follow-up needed] |
| 3 | Michael Hill (CIBC) | Arrange Business Net Banking access for Nathan to view the interface and batch-detail report | TBD (after setup) | Normal | [External — manual follow-up needed] |
| 4 | Nathan Carver | Once access is granted, review the interface/detail report and decide if it meets the need or run it a couple of months to pressure-test | TBD | Normal | Depends on #3 |

## Open Questions

- Whether a batch amount, once translated into Microsoft Dynamics, reads as the aggregated batch or as itemized transactions (Michael unsure).
- Whether the existing CIBC–Dynamics integration is already capable enough to be the easier path, versus building a separate API (Val's hunch, not yet proven).

## Dispatch Log

---
*Processed from a transcript Val provided on July 28, 2026*
*Source meeting: CIBC/JVL ACH + Microsoft Dynamics API Integration — July 28, 2026*
