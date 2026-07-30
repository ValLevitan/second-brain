---
type: meeting
title: CI Architecture Reconvene — v5.1 Standard & Integration Repo Review (Apr 24 2026)
date: 2026-04-24
aliases: [CI Architecture Reconvene, repo standards v5.1, repository standards v3, invariants not tools, CODEOWNERS, sheriff and deputies, code owner per repo, DORA CALM, well-architected github, compliance checks draft, deprecation window 30 days, guiding framework undertaking]
source-count: 2
---

# CI Architecture Reconvene — v5.1 Standard & Integration Repo Review (Apr 24 2026)

**Date:** 24 April 2026, 12:15pm Eastern (§11 recording header); ~1h 43m.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/alexander-biratka.md|Alexander Biratko]] ("Sasha"), [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]].

The **Friday reconvene** promised at the end of the [[wiki/meetings/2026-04-17-ci-architecture-payment-platform.md|Apr-17 CI Architecture session]] — called to review Biratko/Bosik's draft repository-organization standard. Aaron arrived having already critiqued the draft (v4) as "extremely brittle" for prescribing specific tools instead of **invariants**, and having asked Claude for "regulatory prose" that "masquerades as formalism"; he then **rewrote the standard live during the call** into v5, then v5.1, plus two companion documents (a compliance-checks draft and a using-the-compliance-data draft). Val **accepted v5.1 as JVL's repository-standards framework** and pivoted the second half to enforcement — introducing `CODEOWNERS`, the **sheriff-and-deputies** governance metaphor (Andrei Bosik as sheriff of JVL's git infrastructure, one code owner minimum per repo), the DORA/CALM underpinning, and a social-pressure-plus-release-gating enforcement ladder. Andrei's undertaking: produce a **guiding management framework** for the next meeting (Thursday Apr 30), which the three Minsk engineers will then present in Minsk. The standards/governance substance and its dated sequence live on [[wiki/topics/github-release-management-pipeline.md]] (Apr 24 2026 section, which sequences the CI-architecture series); the Claude-in-the-loop authoring and "AI-tools-to-reach-compliance-cheaply" throughline is on [[wiki/topics/ai-assisted-development.md]] (Apr 24 2026 section). §15.8 clear — CI/repo-governance/tooling only; rewards were discussed abstractly as a game-theory lever, no named-person compensation ingested. [[raw/Meeting_Notes_CI_Architecture_Reconvene-April-24-2026.md]]

## Sources
- [[raw/Meeting_Transcript_CI_architecture_reconvene-April-24-2026.md]]
- [[raw/Meeting_Notes_CI_Architecture_Reconvene-April-24-2026.md]]
