---
type: meeting
title: E2E Testing Framework Evolution (May 25 2026)
date: 2026-05-25
aliases: [E2E testing framework evolution, testing framework evolution for E2E tests, choking meeting 1, transactional E2E working group, AI-agent-driven testing, agent performs QA, who tests the tests]
source-count: 1
---

# E2E Testing Framework Evolution (May 25 2026)

**Date:** 25 May 2026, 10:02 AM Eastern (§11 recording-header time); ~1h 32m; Russian (notes summarised in English).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratko]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] (out sick — audio only), [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]], [[wiki/people/alexei-khamin.md|Alexey Khamin]], [[wiki/people/ivan.md|Ivan Shpak]], [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]].

**Meeting #1 of the 3-meeting "choking meeting" cycle** budgeted on [[wiki/meetings/2026-05-22-transactional-e2e-testing-framework.md|May-22 Part 2]] — the working group actually convening to evolve the transactional E2E-testing approach, picking up the [[wiki/meetings/2026-05-22-transactional-e2e-testing-framework.md|May-22]] pivot from a static framework to agentic data-contract-driven test composition. Pavel framed the goal as defining the direction of automated-test evolution over the next 6–12 months; the room debated whether a cross-product "framework" is even the right object, converged on AI agents that *perform* the QA job (grounded in Biratko's repo-standard v5.1 data contracts), and closed by assigning each attendee independent research ahead of a follow-up on **Wed May 27 6:00 PM ET** (Meeting #2 of the cycle).

Substance — Pavel's four status-quo problems, Alexander's "no universal framework" position, Val's reframe (an *approach*, not a framework; feed the AI the data contracts and let it compose tests) and his QA-is-historical-inertia thesis, the cross-repo CI-trigger problem, the platform-scope E2E view, test-session observability, and the decisions/research assignments — lives on [[wiki/topics/github-release-management-pipeline.md]] (May-25 2026 section, continuing the transactional E2E thread) and [[wiki/topics/ai-assisted-development.md]] (May-25 2026 — the agent-performs-QA thesis, hallucination-as-probability, agent personas/memory, the critic-agent idea). §15.8: framework/testing/tooling and meeting-method content only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_E2E_Testing_Framework_Evolution-May-25-2026.md]]
