# Meeting Summary — JVL-Systems_GL_accounts
**Date:** August 3, 2026, 11:02 AM – 12:17 PM Eastern
**Duration:** ~1 hour 15 minutes
**Attendees:** Val Levitan, Igor Donis, Laura Escorcia, Cris Nacarino, Felipe Miranda Giorgi (translator, Spanish)
**Raw transcript:** [[Meeting_Transcript_GL_Accounts_Systems_Labs-August-3-2026]]

## Summary

This was a working session on the General Ledger (chart of accounts) for JVL Systems (US) and JVL Labs (Canada). Val ran it as a participation session and required Igor, Laura and Cris to answer questions rather than sit quietly. Felipe translated to Spanish throughout.

**Val's numbers on JVL Systems.** Val walked the team through statistics he pulled himself:
- Total GL rows: **803**.
- Accounts that have ever had a posting: **437**.
- Accounts actually used in the last 18 months: **143**.
- **50%** of all entries land in just **4** accounts; **95%** of all entries land in **40** accounts.

His point: JVL Systems runs successfully — sales, purchasing, manufacturing, payroll, multi-state taxes — on ~143 used accounts, so the other ~660 exist only because no one has cleaned them up. He argued JVL Labs, which no longer manufactures or purchases, should therefore need *fewer* accounts than Systems, not more.

**The account-count disagreement.** Val's understanding from earlier writing was that Igor wanted to *add* ~200 accounts to Labs (negotiated down from ~600). Igor clarified through Felipe that he was not inventing accounts — he wants to preserve Labs' accounting history from Navision: reuse **211** accounts from the historical Labs ledger plus **35** reusable from Systems, for **246** total. Val said he and Claude read Igor's written proposal as "add 200 on top," possibly a writing/translation miscommunication, and chose not to relitigate it — he wants to move forward on the count logic he presented (build from what is actually used).

**Navision → MSBC migration for Labs.** Background: Val issued a memo in November 2025 to stop using Navision, freeze it at December 31, 2025, and run JVL Labs on a new MSBC (Business Central) production instance from January 1, 2026. That did not happen cleanly — Navision is still in use and Labs' books are still there.
- Laura and Cris argued the priority is **not** reversing transactions but first building a clean chart of accounts, then logging all 2026 Labs entries month-by-month from Navision into BC and reconciling BC to Navision each month. Reversing first would mean doing the work twice.
- Laura noted Navision reversals are technically painful (older system; applied payments must be un-applied before they can be reversed, and the system stalls).
- Cris pointed out that most Labs *purchases* were done in BC (by Michael), but most Labs *payments* — to contractors/vendors, paid from the Canadian bank — were recorded in Navision. So there is more sitting in Navision than Val assumed.
- Val had believed Labs had only a few Navision transactions; he accepted he may be underestimating the volume and said he would look again.

**Where it landed.** Everyone agreed the number-one priority is grooming the GL for both companies, and that the two companies' ledgers must be automatically consolidatable on a monthly basis. Val will have Claude generate a first proposed chart of accounts for both Labs and Systems (he will not pre-review it — just generate and send), the team will mark it up, and a second Claude-generated version will follow. Only after that will they revisit how to stop using Navision. In the interim, the team must keep using Navision for Labs to preserve traceability of bank payments — Val agreed to this reluctantly, calling the situation "a disaster… but I have no choice."

## Decisions Made

- **Clean, groomed GL is the #1 priority for both JVL Systems and JVL Labs.** — Excess/unused accounts are to be cut; Systems uses only ~143 of 803. (Agreed by all)
- **The two companies' ledgers must be automatically consolidatable monthly.** — Requires a coherent, aligned account set across both. (Val; agreed)
- **Val will circulate a Claude-generated first-draft chart of accounts for both companies; team marks it up; a second version follows.** — Iterative build rather than manual account-by-account work. (Val)
- **Continue using Navision for JVL Labs in the interim** — until the clean GL exists in BC, to preserve traceability of bank payments. (Agreed reluctantly by all)
- **Do not chase blame** for how the situation arose — focus only on fixing it going forward. (Val, standing position)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Generate (via Claude) and circulate a first-draft proposed chart of accounts for both JVL Labs and JVL Systems to Igor, Laura and Cris | TBD (next step) | High | Kicks off the GL cleanup; Val will not pre-review, just send |
| 2 | Igor, Laura, Cris | Review the proposed chart of accounts and record/write remarks (or agree) so a second version can be produced | TBD (after #1) | Normal | Everyone to participate; leads to second Claude-generated version |
| 3 | Val | Re-examine how much JVL Labs activity actually sits in Navision for 2026 (esp. contractor/vendor payments from the Canadian bank) to reassess migration effort | TBD | Normal | Val suspected few transactions; Cris indicated payments volume is larger |
| 4 | Igor / Laura / Cris | Keep recording JVL Labs payments in Navision in the interim to preserve bank-payment traceability until the clean GL is live in BC | Ongoing | Normal | Interim measure Val accepted reluctantly |
| 5 | Val | Reconvene the group to discuss stopping Navision and the migration plan, after the second-generation chart of accounts | TBD | Normal | Explicitly deferred to a follow-up session |

## Open Questions

- Final account count for JVL Labs — Igor's 246 (211 historical + 35 from Systems) vs. Val's lean "only what's used" logic. Unresolved; to be settled by the Claude-generated proposal and team review.
- Actual transaction/payment volume in Navision for Labs 2026 — Val to verify; drives how hard the migration is.
- Migration cutover date — mid-2026 vs. January 2027 vs. later. Val noted that if cleanup drags into November with little progress, they may defer the fresh start to 2027 (or 2028).

## Dispatch Log

---
*Processed from Teams transcript on August 3, 2026 (scheduled meeting-watcher run).*
*Source meeting: JVL-Systems_GL_accounts*