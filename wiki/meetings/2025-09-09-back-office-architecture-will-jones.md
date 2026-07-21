---
type: meeting
title: Back-office / transactional architecture — executive-developer alignment with Will Jones (Sept 9 2025)
date: 2025-09-09
aliases: [back office architecture Will Jones, transactional back-office Sept 9, executive developer alignment, Will Jones back office]
source-count: 1
---

# Back-office / transactional architecture — executive-developer alignment with Will Jones (Sept 9 2025)

**Date:** 2025-09-09 (12:20 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/will-jones.md|Will Jones]]. English.

A one-on-one where Val worked through *how to align the executive branch with the developers* on the transactional back-office (POS / payment) architecture. This is a distinct session from the same-day 2:41 PM [[wiki/meetings/2025-09-09-top-level-backend-architecture.md|Val↔Pavel top-level back-end]] session and the 3:18 PM [[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md|POS spatial/hardware]] session — same architecture push, different partner and framing. It continues the [[wiki/topics/persona-driven-design-and-orchestration-platform.md|orchestration-platform / requirements-first arc]] and the InComm/back-office thread; substance and the dated arc entry live there.

In brief (durable points):
- **Val's alignment method:** name the **initiative** → split into **products** → for each product define a set of **capabilities** → for each capability a set of **features** tied to use cases; then the group can agree which capability to build first and which features (e.g. "features 17 and 9") enable it. Val's worked example: initiative = transactional operations, product = **POS**, date = **January 1**, capability = converting player winnings onto a card. He is seeking **transparency/alignment**, not dictating engineering solutions ("what it's going to do, not how").
- **Will's role (as Val frames it):** an **executive** who helps define the requirements and capabilities for the whole system (Will prefers **user stories** over use cases — "more personality," closer to the user), and acts as a **two-way conduit** between the executive level and the developers (facilitator/mentor to Pavel, translated to Russian for the Minsk team).
- **The ACH / fund-encumbrance risk (durable):** when a player cashes winnings onto a card validated through InComm, JVL immediately **owes InComm** (encumbers the amount) but does **not yet hold the cash** — the location owner holds the physical cash overnight and JVL must ACH-pull it (Val's "end of day" = 3–4 AM). Val recounts Nathan's ~week-earlier discovery that **specialized fintech/ACH companies** (not banks) move these funds efficiently — "this must be part of our solution." Requires day-one **reconciliation reporting** to flag which operators didn't settle by ~3–4 AM. (Same thread as the Sept-3 [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Dwolla/Plaid ACH-provider]] discussion.)
- **Architecture stance (Will):** the **B2B connection to InComm hosted in Azure** (cloud) is priority-one and the one definitively-new piece; the team hasn't stood up cloud/DevOps before, so it's a real learning curve. Don't uproot the legacy CMS all at once — migrate **piece by piece**, solving the biggest business problem first, keeping a vision of the future architecture as a guide without detailing it fully now.

## Sources

- [[raw/back-office_architecture-will_jones-september-9-2025.md]]
