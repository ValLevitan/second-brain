---
type: decision
title: Class-3 metering is the "constitution"; Georgia QAM gets separate parallel logic
date: 2025-05-28
aliases: [class 3 constitution, Georgia QAM legislation, jackpot limit, key-to-credit, parallel jackpot logic, SAS 6.03]
source-count: 1
status: active
open-commitments: 1
---

# Class-3 metering is the "constitution"; Georgia QAM gets separate parallel logic

On the May 28 2025 jackpot-treatment call ([[wiki/meetings/2025-05-28-jp-jackpot-class3-georgia-coam.md]]) — the reconvene from the May-21 Class-3-vs-COAM meter meeting — [[wiki/people/val-levitan.md|Val]] ruled on how JVL should structure jackpot/meter logic for Class 3 versus the Georgia Co-op (QAM/COAM) market. Continuation of the metering thread on [[wiki/projects/georgia-market-rollout.md]]. [[raw/jp_treatment-may-28-2025.md]]

## What was decided

- **Class-3 metering must be implemented in full, purely, exactly to spec** — "adhere with purity and clarity and full compliance to class three." Val's framing: **Class-3 meters are the "constitution"**; jurisdiction-specific rules like Georgia QAM are **"legislation"** that must be layered *onto* the constitution, never by altering the underlying Class-3 metering. [[raw/jp_treatment-may-28-2025.md]]
- **The current Georgia QAM implementation is wrong** because JVL "made it fit" — it adjusted the Class-3 meter behaviour to satisfy Georgia QAM rules instead of running two parallel logics. Right now it isn't manifesting (the jackpot-limit condition is never set in Georgia), but if an operator lawfully set it, JVL "would immediately fall out of compliance" and risk having all equipment disconnected. [[raw/jp_treatment-may-28-2025.md]]
- **The fix (sequenced):** (1) first verify the Class-3 logic and meters are flawless (extensive, triple-checked testing); (2) implement Class-3-type meters + Class-3 logic natively; (3) implement a **separate parallel logic** for Georgia QAM's **hands validation for jackpot payouts** — so a jackpot condition evaluates the hand count and allows a partial payout of only the amount the hands qualify, leaving the remainder in a hand-pay condition. Correct submissions get rolled out one-by-one; over a couple of years the wrongly-fitted logic ages out into archives. [[raw/jp_treatment-may-28-2025.md]]
- **Do not touch the meters themselves.** The SAS meter set "has been working for decades… like rewriting fundamental constitution" — new legislation (e.g. new SAS versions) is adopted separately, not by rewriting the meter constitution. [[raw/jp_treatment-may-28-2025.md]]

## Supporting technical points (from the call)

- **Jackpot/key-to-credit definitions:** with no jackpot limit set there is no jackpot, so all wins post to total coin-out; a jackpot limit (typical US **$1,200**, the IRS value) makes any win ≥ the limit a hand-pay. There is a separate **key-to-credit limit** setting; it must be **less than the jackpot limit**, and it needs a value (can't be enabled empty). A win above the jackpot limit goes **entirely to hand-pay** regardless of the key-to-credit value. Whether meters posted to the correct places (jackpot vs total-out) in JVL's Seminole testing is still being verified against the iView/Bally logs. [[raw/jp_treatment-may-28-2025.md]]
- **Georgia has no jackpots today** (amusement machines, not casino; the IRS $1,200 limit doesn't apply per Felipe), and JVL's jackpot limit doesn't work on the GQL/Class-II products because "it's not C3 yet" — the hand-count logic isn't there. If needed for the test lab (Eclipse), JVL could ship an RIS that unlocks a small jackpot limit for lab demonstration only, with production always no-limit. [[raw/jp_treatment-may-28-2025.md]]
- **SAS 6.03** was raised (it has ~10 changes — non-SAS progressive heat reporting, a "jackpot hand-pay hit-off to machine-pay exception") but is **not** being adopted for meters. [[raw/jp_treatment-may-28-2025.md]]

## Open commitments

- [ ] Juan Martinez — draft the requirements for the parallel Class-3 / Georgia-QAM jackpot logic discussed; team to think it over (Irina and Pavel to meet) and reconvene to make a final decision in ~10 days — due ~10 days after May 28 — [[raw/jp_treatment-may-28-2025.md]]

## Sources

- [[raw/jp_treatment-may-28-2025.md]]
