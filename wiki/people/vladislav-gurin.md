---
type: person
title: Vladislav Gurin
date: 2025-05-28
aliases: [Vladislav Gurin, Vlad, Влад]
source-count: 3
open-commitments: 1
open-questions: 1
---

# Vladislav Gurin

Vladislav Gurin ("Vlad") is a JVL Minsk-side engineer/QA who is the team's authority on **SAS jackpot and meter behaviour** — on the May 28 2025 jackpot-treatment call he explained exactly how the machine posts wins to the total-out, total-jackpot and attendant-paid meters and how the key-to-credit feature behaves. [[raw/jp_treatment-may-28-2025.md]]

## Role

- On the May-28 call ([[wiki/meetings/2025-05-28-jp-jackpot-class3-georgia-coam.md]]) Vlad walked [[wiki/people/juan-martinez.md|Juan]] and [[wiki/people/val-levitan.md|Val]] through jackpot processing: with **no jackpot limit set, all wins go to the total coin-out meter**; with a limit (e.g. $1,200), a win at/above it posts to the total-jackpot meter; the **key-to-credit limit must be less than the jackpot limit**, and a win above the jackpot limit goes entirely to hand-pay regardless of the key-to-credit setting. [[raw/jp_treatment-may-28-2025.md]]
- He said he would be **out for about a week** starting ~May 29, so the meter-behaviour work pauses until his return. [[raw/jp_treatment-may-28-2025.md]]
- **June 10 2025 — the reconvene ([[wiki/meetings/2025-06-10-jackpot-meter-sas-scope-gaps.md]]).** Vlad ("Vlad") is the JVL-lab tester through whom the group tries to reproduce the key-to-meter jackpot scenarios. He explained the limits of JVL's testing rig: JVL has only a **~20-year-old IGT "SAS Tool" emulator (a SAS Tool, not a full SAS host)** with "circumcised" functionality — it can initiate an audit-key rotation manually via SAS long-poll, but has no player-tracking screen to press, so many host-side jackpot flows can't be exercised. He confirmed JVL currently has **no test for turning a mechanical key to send a >jackpot-limit win to the credit meter** — the scope gap the meeting uncovered. Meter substance on [[wiki/projects/georgia-market-rollout.md]]. [[raw/meter_sas_function-june-10-2025.md]]

## June 12 2025 — presented the jackpot/key-to-meter flowchart

On the [[wiki/meetings/2025-06-12-jackpot-meter-flowchart-review.md|June-12 flowchart review]] Vlad ("Vlad") walked Val, [[wiki/people/juan-martinez.md|Juan]] and an "Irina" through the **future-state flowchart** of Class-3 jackpot / key-to-meter behaviour he had built as the June-10 undertaking — the no-limit / limit-equals-jackpot / $25k-key-to-meter / hard-$30k-win variants, reusing the existing hand-pay dialogue, and the win-calculation double-posting concern. He was then given the next undertaking: **produce a block diagram of every JVL meter** (maximum set, proper names) for a Tuesday-11am follow-up (~June 17), which the team decided it "cannot move forward without." Meter substance on [[wiki/projects/georgia-market-rollout.md]]. [[raw/jp_meters-june-12-2025.md]]

## Open questions

- Vladislav Gurin is very likely the recurring **"Vlad" (Minsk QA)** flagged across earlier certification calls (e.g. the May-21 Class-3 meter retest, where "Vlad" was to run the GLI-approved MH1 software in parallel at JVL and report meter findings — see [[wiki/projects/georgia-market-rollout.md]]); the timing fits (that Vlad was "unavailable from ~May 29 for about a week," which Gurin confirms here). Treated as the same person by context but **owner confirmation queued** (Tier A). [[raw/jp_treatment-may-28-2025.md]]

## Open commitments

- [ ] Vlad — produce a **block diagram of every JVL meter** (proper names, used or not) for the Tuesday-11am follow-up (~June 17) — due ~June 17 — [[raw/jp_meters-june-12-2025.md]]

## Sources

- [[raw/jp_treatment-may-28-2025.md]]
- [[raw/meter_sas_function-june-10-2025.md]]
- [[raw/jp_meters-june-12-2025.md]]
