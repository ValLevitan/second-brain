---
type: meeting
title: Transactional E2E Testing Framework (May 22 2026)
date: 2026-05-22
aliases: [transactional E2E testing framework, transactional E2E framework, E2E testing study group, choking meeting, agentic data-contract test composition, dynamic test composition, testing framework for transactional products]
source-count: 2
---

# Transactional E2E Testing Framework (May 22 2026)

**Date:** 22 May 2026, 12:02pm Eastern (§11 recording header time); one meeting in two recorded segments — segment 1 ~30m from 12:02pm, then Val turned the recording off and back on ~40m later for segment 2 ~9m from 12:42pm.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]].

A design conversation on how to build automated **end-to-end testing** for the **13 transactional-product repos**, set in the context of [[wiki/people/alexander-biratka.md|Alexander Biratko]]'s repo-organization standard v5.1 (structure repos so AI agents can work across them autonomously: a Product Owner writes the features/requirements, an agent decomposes them into the right repos). This is the direct continuation of the **new transactional E2E workstream** opened at the [[wiki/meetings/2026-05-21-ci-v5-1-two-week-operationalisation-review.md|May-21 CI v5.1 review]]. Segment 1: Pavel's view that the NOVA-style framework (what [[wiki/people/anton-leshkevich.md|Anton Liashkevich]] writes) does not port cleanly to transactional, Val's arguments for parallel (not sequential) dev-test and his "bugs are a scope gap, not planned work" framing, and Val's initial call for a four-person study group. Segment 2: the recording restarted to capture next steps — Pavel's expanded working group, the pivot from a static "framework" to **agentic data-contract-driven test composition**, Val's "choking meeting" methodology, and a three-meeting cycle budget.

Substance, the full working-group roster, the agentic-composition decision, the "choking meeting" method, and the undertakings live on [[wiki/topics/github-release-management-pipeline.md]] (May-22 2026 section, continuing the transactional E2E thread) and [[wiki/topics/ai-assisted-development.md]] (May-22 2026 — agents composing tests from data contracts). §15.8: repo/testing-framework/tooling and meeting-method content only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Transactional_E2E_Testing_Framework-May-22-2026.md]]
- [[raw/Meeting_Notes_Transactional_E2E_Testing_Framework-Part_2-May-22-2026.md]]
