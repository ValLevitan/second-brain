---
type: meeting
title: QA Strategy in the AI Development Cycle (May 28 2026)
date: 2026-05-28
aliases: [QA strategy AI development cycle, this and that QA strategy, QA in the AI dev cycle, data contracts as QA anchor, capture AI tests into a standard, bricks regression tests, choking meeting QA]
source-count: 1
---

# QA Strategy in the AI Development Cycle (May 28 2026)

**Date:** 28 May 2026, 2:31 PM Eastern (§11 recording-header time); ~1h 7m; Russian (notes summarised in English).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]].

An open discussion on how **QA and testing** should fit JVL's new AI-driven development cycle (GitHub feature branches, Claude Code agents, CI/CD). **No firm process was settled.** This continues the E2E/testing-framework "choking-cycle" thread — the [[wiki/meetings/2026-05-22-transactional-e2e-testing-framework.md|May-22 origin session]] → [[wiki/meetings/2026-05-25-e2e-testing-framework-evolution.md|May-25 evolution meeting #1]] → [[wiki/meetings/2026-05-27-testing-framework-e2e.md|May-27 E2E meeting #2]] — narrowing from the cross-repo E2E problem to where the QA function itself lives when the AI already runs the tests.

The substance — Val's "capture the AI's own test runs into an agreed standard (a Claude Code skill)" idea, Pavel's "AI already tests invisibly" observation, the "bricks" reusable-regression-test idea (credited to Andrei), Val's push against a large human-managed test database and toward continuously-running always-on tests, the decision to **tie QA to data-contract changes and their associated actions**, and the PR-triggered integration → end-to-end → merge sequence — lives on [[wiki/topics/github-release-management-pipeline.md]] (May-28 2026 section, continuing the transactional E2E thread) and [[wiki/topics/ai-assisted-development.md]] (May-28 2026 — the AI-tests-itself/capture-into-a-skill stance and the don't-over-manage-the-AI argument). §15.8: QA/testing/tooling and meeting-method content only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_QA_Strategy_AI_Development_Cycle-May-28-2026.md]]
