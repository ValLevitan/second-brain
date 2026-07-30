---
type: meeting
title: CI Architecture v5.1 Operationalisation — Two-Week Review (May 21 2026)
date: 2026-05-21
aliases: [CI v5.1 two-week review, CI v5.1 operationalisation review, structure-compliance framework review, DORA metrics review, artifact-based test verification, transactional E2E framework, TS-360 vs transactional E2E]
source-count: 2
---

# CI Architecture v5.1 Operationalisation — Two-Week Review (May 21 2026)

**Date:** 21 May 2026, 11:58am ET (~1h 25m) (§11 recording header time; the `_075803` filename stamp is UTC, 4h behind — not the meeting time).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/alexander-biratka.md|Alexander Biratko]] ("Sasha"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]. [[wiki/people/aaron.md|Aaron Bockelie]] was absent (started a new job, unseen for weeks).

The first operational checkpoint of the v5.1 standard + structure-compliance framework (v0.1) Andrei wrote, ~10 days into real-world running — the two-week review anchored at the [[wiki/meetings/2026-04-30-ci-architecture-governance-framework-review.md|Apr-30 governance-framework review]]. The framework runs clean on the **13 transactional-equipment repos** (one FAIL over the window — an English→Russian docs regression, self-corrected); the live problem is the **REVIEW status** (checks the automated framework can't decide), which Val ruled cannot scale by human triage. The team landed an **artifact-based pattern**: each repo's CI emits a log artifact (test results + coverage), and the compliance framework reads it — tests run where they belong, the framework only verifies they ran. Also settled: the API contract is **generated from code** at build time, so the framework verifies its *presence*, not its content; **DORA metrics** run as a separate Layer-2 report on Google's published thresholds; no scope expansion beyond the 13 repos; and a **new, separate end-to-end test framework for the transactional payment products** (distinct from TS-360, which stays on the game side under NOVA) with [[wiki/people/alexei-khamin.md|Aleksey "Lyosha" Khamin]] proposed as architect/owner. Next checkpoint set for **June 11 2026, 8am ET** (three weeks, not two).

Substance, the DORA thresholds, the artifact/contract decisions, the E2E-framework design questions, and the full undertaking set live on [[wiki/topics/github-release-management-pipeline.md]] (May-21 2026 section). Continues the [[wiki/meetings/2026-04-17-ci-architecture-payment-platform.md|Apr-17]] → [[wiki/meetings/2026-04-24-ci-architecture-reconvene.md|Apr-24]] → [[wiki/meetings/2026-04-30-ci-architecture-governance-framework-review.md|Apr-30]] CI-architecture series. §15.8: CI/governance/DORA/tooling economics only; no named-person compensation (metrics explicitly must never tie to reviews or pay — the Apr-30 rule reaffirmed).

## Sources
- [[raw/Meeting_Transcript_ci_v5_1_two_week_operationalisation_review-May-21-2026.md]]
- [[raw/Meeting_Notes_ci_v5_1_two_week_operationalisation_review-May-21-2026.md]]
