---
type: meeting
title: E2E Testing in CI/CD — Lesha's first contract-analysis experiment (June 5 2026)
date: 2026-06-05
aliases: [E2E Testing CICD Contract Analysis June 5, Lesha contract analysis experiment, AI contract analysis Flex IQ SDK, ADR breakthrough June 5]
source-count: 1
---

# E2E Testing in CI/CD — Lesha's first contract-analysis experiment (June 5 2026)

**June 5, 2026, 11:59 AM ET · ~1h 42m.** Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/alexei-khamin.md|Alexey Khamin]] ("Lesha"), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]].

The **Friday follow-up** the [[wiki/meetings/2026-06-01-e2e-testing-cicd-architecture.md|Jun-1 strategy session]] scheduled to add Lesha: he ran the **first experiment** toward AI-driven testing in CI/CD — driving Claude (not hand-writing code, per Pavel's approach) to analyze the data contracts of two product repos and compare how they fit together. Continues the "choking-cycle" E2E thread ([[wiki/meetings/2026-05-22-transactional-e2e-testing-framework.md|May-22]] → [[wiki/meetings/2026-05-25-e2e-testing-framework-evolution.md|May-25]] → [[wiki/meetings/2026-05-27-testing-framework-e2e.md|May-27]] → [[wiki/meetings/2026-05-29-ai-testing-and-build-architecture.md|May-29]] → [[wiki/meetings/2026-06-01-e2e-testing-cicd-architecture.md|Jun-1]]).

Durable substance — the experiment result (contracts + docs make Claude faster and deeper; a repo with no contracts is shakier), the green/yellow/red signal model, the "contracts validated against requirements at generation time" ruling, the **ADR breakthrough** (undocumented technical decisions, not business requirements, are what turn signals yellow → point the test at ADRs in the repo), the run-history benefit, and the decisions/undertakings — lives on [[wiki/topics/github-release-management-pipeline.md]] (Jun-5) and [[wiki/topics/ai-assisted-development.md]] (Jun-5).

## Sources
- [[raw/Meeting_Notes_E2E_Testing_CICD_Contract_Analysis-June-5-2026.md]]
