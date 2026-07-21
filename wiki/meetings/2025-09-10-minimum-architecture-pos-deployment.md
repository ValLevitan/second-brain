---
type: meeting
title: Minimum-architecture POS deployment planning with Aaron (Sept 10 2025)
date: 2025-09-10
aliases: [minimum architecture POS, minimum viable architecture, POS deployment planning Sept 10, sandwich curation analysis decision, variety productive doubt]
source-count: 1
---

# Minimum-architecture POS deployment planning with Aaron (Sept 10 2025)

**Date:** 2025-09-10 (12:42 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]]. English.

A coaching/strategy 1:1 where Val decided how far to push an "old-fashioned," get-it-done MVP for the **January POS** without derailing the engineering transformation. Continues the flexpay/transactional POS thread (Sept-3 [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Flex weekly]], Sept-9 [[wiki/meetings/2025-09-09-top-level-backend-architecture.md|top-level back-end]] / [[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md|POS hardware]]) and the [[wiki/topics/persona-driven-design-and-orchestration-platform.md|requirements-first / orchestration-platform arc]] (Sept-10 section there).

Durable points (single source):
- **Aaron's "sandwich" model.** Every unit of work has three phases — **curation → analysis → decision** (e.g. agile: backlog refinement → development → deployment). He introduced **"variety"** = the breadth of experience a party brings: the person doing the *analysis* always operates at narrower variety than the one curating/deciding, so a request must be framed to contain the recipient's experience set. Learning = increasing variety; **"productive doubt"** (code reviews, demonstrations) is the constructive friction that grows it — Dima shouldn't blindly accept requirements nor reject them, but challenge *why* each exists.
- **Requirements, not specifications, come first.** Define the **performance envelope** ("the POS shall track up to 50,000 players on release day"; a concurrency target of ~100 simultaneous transactions) — the *what*, not the tech platform (not "it's SQL"). A well-written requirement carries its own justification, pre-answering first-order doubt.
- **Naming discipline (Aaron).** Don't call the 3–5-year vision "architecture" — it's a **goal** ("architectural goal"). Val liked framing it as **scalability**, but Aaron insisted you must define the *dimensions* you're scaling into, not just say "scalable." The near-term deliverable is a **"minimum viable architecture"** for the POS deployment — with the caution it must not calcify into the true architecture.
- **Don't build from scratch under the clock.** Aaron's strong advice: a small team cannot build a serverless/microservices payment architecture from first principles in ~4–5 months; **adopt a validated, known design pattern** and iterate. As the executive, Val mandates the constraints — **serverless, cloud-first, no big monolithic SQL, understandable by others** — [[wiki/people/nathan-carver.md|Nathan]] helps shape them as business-technical advisor; then hand [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] (principal back-end architect) the requirements+goals to assess and iterate the "sandwich" review cycle several times. Warns of the **iron triangle** (fast/cheap/good — pick two).
- **Anchor points.** The **InComm validation service** will stay relatively static for years — a fixed "pin on the map" the architecture can build around. Reuse the legacy monolith's **purpose and tribal knowledge** (not its code): split it conceptually into services, extract a couple, and design a new cloud service to run the POS MVPs. Val: the 30-year-old Java monolith is understood to need chopping up — stop relitigating that.
- **Val's landed decision:** push the minimum-viable POS for January using **minimum structural changes** to the dev cycle (the "one big thing" = get **off SVN onto git**, finishing the repo-taxonomy Excel first), forgoing other transformation initiatives that would cause slowdown — while not screwing up the transformation.

## Sources

- [[raw/Minimum_Architecture_POS_deployment_planning-september-10-2025.md]]
