# Meeting Summary — Dwolla: reducing the reserve for the slowed GA-COAM rollout

**Date:** August 11, 2026, 8:15 PM Eastern
**Duration:** approximately 26 minutes
**Attendees:** Val Levitan, Marc Lee (Dwolla — sales & partnerships), Nancy Baccam (Dwolla — solutioning; has worked with JVL's tech teams and Nathan through integration). Nathan Carver referenced.
**Raw transcript:** [[Meeting_Transcript_Dwolla_Reserve_Reduction_Negotiation-August-11-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "JVL + Dwolla", 8:15 PM ET, organiser Marc Lee, attendees Val + Nancy Baccam. Confirmed. ("Qualls" in the raw transcript is a mis-transcription of Dwolla.)
**Context:** Dwolla is the ACH/payments rail for the GA-COAM prepaid-card cash-out. Ties to the Prize Redemption business-model work and Nathan's payment integration.

## Summary

Val asked Dwolla to **reduce the $36,000 reserve/deposit** in the signed order form, because he has dramatically slowed and shrunk the rollout since the aggressive plan was negotiated. New plan: **one test unit in one location now**, ~5 units in September, ~10 in October, then pause until a planned Q1-2027 rollout — a long debug period (could stretch to six months) before going wider. JVL is a private company funding this from its own pocket; Val argued the reduced volume means Dwolla is not at risk, so he should not have to tie up $36K for a trial. He was explicit that he is not disputing the fairness of $36K — he just does not want to part with it if he does not have to, and will be the first to come back and raise limits when volume grows.

The mechanics discussed:
- **Real transactions**, not $10 test amounts — Val needs a live cycle. Card issuer (InComm) caps **$1,000 per card**; realistic average ~$100/card, ~5–10 cards/day → ~$500–$1,000/day on one terminal, batched **daily**. Dwolla probed whether $10 or $100 per transaction would work; Val declined — he must match InComm's $1,000 limit because of location competition.
- Dwolla's production settings: **$5,000 per transaction / $25,000 weekly per terminal**; funds settle standard debit (3 days) into the JVL Dwolla balance, then 1-day credit to bank; JVL is approved for same-day ACH credit but does not need it during the trial.
- Dwolla's angle to lower the reserve: **disable same-day credit and reduce the client transaction limit** during the testing period (less risk with standard debits, business payees, no consumer chargebacks).
- Val is **cycle-focused, not terminal-focused** — he will not go forward unless the flow is fully automated (three providers/banks), no manual reconciliation on mismatches.

Dwolla will take the reduced-reserve ask to their risk/legal team and get back within a day or two. Val insisted: **agree the reserve first**, before re-circulating the order form (the order form's transaction-limit and reserve language would then be updated and sent to Monica to sign). Dwolla asked for updated financials; Val said they are unchanged (~$140K figure on file from ~a year ago) and he would be "regurgitating the same" numbers.

## Decisions Made
- Rollout slowed: 1 test unit now → ~5 in Sept → ~10 in Oct → pause → Q1-2027; extended debug (up to ~6 months). (Val)
- Reserve reduction to be decided by Dwolla risk **before** any order-form update. (Val's condition, Dwolla agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Marc Lee / Dwolla | Take reduced-reserve ask to risk/legal; propose disabling same-day credit + lowering transaction limit for the trial | 1–2 days | High | Val must move forward |
| 2 | Dwolla | After reserve agreed, update the order form (limits + reserve language) and send to Monica to sign | After (1) | Normal | Then production access |
| 3 | Val | Provide updated financials if available (else prior on-file figures stand) | — | Low | Dwolla asked; Val says unchanged |

## Open Questions
- Final reserve number Dwolla's risk team will accept for the trial (target: well below $36,000).

## Dispatch Log

---
*Processed from Plaud recording on September 25, 2026 (backlog batch 7). Source: 08-11 Risk-Calibrated Pilot JVL-Qualls Payments (Plaud).*
