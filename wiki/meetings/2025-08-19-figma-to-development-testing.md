---
type: meeting
title: Figma-to-development / testing working session — Aug 19 2025 (12:02pm)
date: 2025-08-19
aliases: [figma to testing development, figma to development, Figma to executable, Maze, Joy UI]
source-count: 1
---

# Figma-to-development / testing working session — Aug 19 2025 (12:02pm)

**Date:** 2025-08-19 12:02pm · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/pavel.md|Pavel Frolov]] (Director of Engineering), QA lead [[wiki/people/irina-shishko.md|Irina Shishko]], UX/UI designer [[wiki/people/ihar-hrybko.md|Ihar Hrybko]], test-engineer [[wiki/people/anton-leshkevich.md|Anton Leshkevich]]. Mixed English/Russian (~90 min).

The **fuller group follow-up** to the [[wiki/meetings/2025-08-12-figma-to-testing-workflow.md|Aug-12 Aaron explainer]] — Val explicitly frames it as "the discovery for me was done last week in the meeting with Aaron … we left this week for Igor to dig more into it." Distinct, much larger session (§12 corpus-wide check cleared it against Aug-12; different attendees, a genuine debate rather than a monologue).

**Identity note:** the "Igor" repeatedly addressed here (the one building the Figma mock-ups / setup-screen UI) is **[[wiki/people/ihar-hrybko.md|Ihar Hrybko]]** — Pavel and Aaron say "Igor," and the answering speaker label is consistently *Ihar Hrybko* (registry: UX/UI, payroll "Igar Hrybko"). No separate/unresolved Igor in this meeting.

Substance and the dated place on the QA/testing arc: [[wiki/topics/test-automation-strategy.md]] (Aug-19 section). In one line: the group reached a **binary standoff** — Ihar (and Anton) hold that Figma cannot auto-generate integration tests or production-ready React for JVL's complex app (only usability testing, colour/design-token checks, or landing-page-grade code); Aaron reframes the real target as **defining what makes generated code "acceptable"** so a code-generation step (AI or deterministic) can produce both the React code **and** the parallel integration tests, collapsing the mock-up→code→test labour.

## Sources

- [[raw/figma_to_testing_development .md]]
