---
type: meeting
title: AI Testing and Build Architecture (May 29 2026)
date: 2026-05-29
aliases: [AI testing and build architecture, testing with AI, how products get built, installer build-time integration gap, manifest approach, forward-only versioning, components renamed artifacts, testing pyramid, choking meeting build architecture]
source-count: 1
---

# AI Testing and Build Architecture (May 29 2026)

**Date:** 29 May 2026, 10:03 AM Eastern (§11 recording-header time); ~1h; Russian (notes summarised in English).
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]].
**Mentioned (not present):** [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]], Sergey Simonov, [[wiki/people/alexander-biratka.md|Alexander Biratko]] (Sasha), [[wiki/people/anton-leshkevich.md|Anton Liashkevich]], [[wiki/people/aaron.md|Aaron Bockelie]].

A working session on **how products are tested AND how they get built**. The team had agreed the prior Wednesday to **pause forward work until they settle direction**, so this was a smaller "think it through" meeting — a continuation of the same testing-framework/build thread from the [[wiki/meetings/2026-05-27-testing-framework-e2e.md|May-27 E2E meeting #2]] and the [[wiki/meetings/2026-05-28-qa-strategy-ai-development-cycle.md|May-28 QA-strategy discussion]].

The substance — dropping the deterministic-framework vision, the bounded/operator-controlled model for AI-run testing, the **build-ownership map** (who decides how each product is assembled: transactional vs gaming), the **installer build-time integration gap** and Andrei's data-contract-as-build-output fix, Evgeny's preferred **manifest-in-an-integration-repo** approach, **forward-only versioning** adopted as discipline, renaming "components" → "artifacts", accepting the **v5.1 repository standard** as ~80% working, and the **Monday June 1** session to drive it to a written standard — lives on [[wiki/topics/github-release-management-pipeline.md]] (May-29 2026 section, continuing the transactional E2E/build thread) and [[wiki/topics/ai-assisted-development.md]] (May-29 2026 — the bounded-AI-testing model and the test-taxonomy/testing-pyramid discussion). §15.8: build-architecture/testing/tooling and meeting-method content only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_AI_Testing_And_Build_Architecture-May-29-2026.md]]
