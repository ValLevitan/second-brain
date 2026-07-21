---
type: meeting
title: Top-level back-end architecture — how to build the whole back-end without slowing POS (Sept 9 2025)
date: 2025-09-09
aliases: [top level architecture back-end, top-level backend architecture, backend architecture Sept 9, InComm payment hub priority one]
source-count: 1
---

# Top-level back-end architecture — how to build the whole back-end without slowing POS (Sept 9 2025)

**Date:** 2025-09-09 (2:41 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]]. Russian.

Val's framing question: how to approach building the **architecture of the whole back-end** — sequenced so JVL ships the **POS first**, then additional **transactional-channel products**, then sweeps up the technical debt on the legacy CMS, then releases **HHR** — without spreading thin, yet with a systemic view of where the architecture is heading, and **without slowing the POS release**. This directly follows the Aug-14 [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md|block-diagram-first ruling]] and the Aug-27 payment-hub-first plan on the [[wiki/topics/persona-driven-design-and-orchestration-platform.md|orchestration-platform arc]].

Substance and the dated arc entry: [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-9 section). In brief:
- **Pavel's phasing for the next ~6 months:** priority #1 is a **cloud InComm payment hub** (a small, near-independent server doing the InComm transactions); JVL cannot quickly rebuild the legacy CMS, so **extend the existing legacy Flexpay/Flex-POS dashboard** to register Flex-POS devices and reuse the current CMS's interfaces to hit **January 1** (a POS with Mother-Goose-scheme software that talks to the payment hub, configures itself, gets RIS, and registers via the existing CMS/back-end). The payment hub is deliberately independent so it survives the later migration.
- **The method Val extracts (by asking "how is this done?"):** high-level **business requirements** first → draw the **top-level block diagram** → **decompose** each block (its requirements, constraints, non-functional requirements, tech stack) → descend level by level; at some level the legacy CMS ("7MS", transcribed variously) gets parked/renamed and folded into the orchestration/observability platform. Val explicitly does **not** want the whole system detailed top-to-bottom now ("we'd get stuck in the swamp") — just the top one or two levels to create alignment.
- **Top-level requirements sketched:** an observability/orchestration platform that supports **all cabinet types** — split into **transactional-hall cabinets** and **gaming cabinets** (monitoring + orchestration, any software class); geographically-independent/scalable; plus administration and system-access (non-functional, top-level).
- **Next steps:** Pavel to first stand up a **repository** as the home for the accumulating architecture info (a couple of days), then produce a **top-level block diagram** (~a couple of days) tying today's CMS to the future plan. **Follow-up meeting booked Tuesday ~4 PM** to review the top-level requirements, use cases and 1–2 architecture levels.

NOTE: other Sept-9 back-end/architecture sessions exist in the source set (a Will-Jones back-office session, a finance recurring meeting, a git-structure review) but are **not** in this batch and had not been ingested at time of writing — cross-link when stubbed. The 3:18 PM [[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md|POS spatial/hardware]] session is a separate meeting.

## Sources

- [[raw/top_level_architecture_back-end-september-9-2025.md]]
