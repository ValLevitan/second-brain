---
type: meeting
title: Testing Framework E2E — working-group meeting #2 (May 27 2026)
date: 2026-05-27
aliases: [testing framework E2E, testing framework evolution for E2E tests, choking meeting 2, transactional E2E working group meeting 2, when is a CICD product done, one-sided contracts, Standard 5.1 release]
source-count: 1
---

# Testing Framework E2E — working-group meeting #2 (May 27 2026)

**Date:** 27 May 2026, 10:05 AM Eastern (§11 recording-header time); ~1h 43m; Russian (notes summarised in English).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/alexander-biratka.md|Alexander Biratko]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/sergey-tsymanov.md|Sergey Tsimanov]], [[wiki/people/ivan.md|Ivan Shpak]], [[wiki/people/alexei-khamin.md|Alexey Khamin]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]].

**Meeting #2 of the "choking-cycle" E2E working group** — the full group convening (much longer than the origin session) to work the question of how to know when a CICD-built product is actually "done", i.e. how to validate the transaction system end-to-end across many self-contained repositories, with the transaction product (closest to **Standard 5.1**) as the testbed. It continues the thread from the [[wiki/meetings/2026-05-22-transactional-e2e-testing-framework.md|May-22 origin session]] and the [[wiki/meetings/2026-05-25-e2e-testing-framework-evolution.md|May-25 evolution meeting #1]].

The substance — Pavel's over-repository integration-repo proposal vs the "build a test platform first" camp vs Andrei Bosik's already-existing integration repo; Val pushing back hard on building any upfront framework (the Karpathy propose-correct-accumulate stance) and forcing a real production release next week to surface the actual problems; the one-sided (zero-trust) contract clarification; the official company-wide release of Standard 5.1; and the CLAUDE.md-scale-limit / per-repo-knowledge-base discussion — lives on [[wiki/topics/github-release-management-pipeline.md]] (May-27 2026 section, continuing the transactional E2E thread) and [[wiki/topics/ai-assisted-development.md]] (May-27 2026 — the no-framework / let-the-AI-figure-it-out stance and the CLAUDE.md-as-wiki scaling note). §15.8: framework/testing/tooling and meeting-method content only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_Testing_Framework_E2E-May-27-2026.md]]
