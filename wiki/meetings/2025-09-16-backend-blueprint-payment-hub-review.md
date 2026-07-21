---
type: meeting
title: Back-end architecture blueprint review — the InComm payment hub as a cloud service (Sept 16 2025)
date: 2025-09-16
aliases: [back-end architecture blueprint review, payment hub cloud service, backend blueprint Sept 16, payment hub tech stack, specification of specifications]
source-count: 1
---

# Back-end architecture blueprint review — the InComm payment hub as a cloud service (Sept 16 2025)

**Date:** 2025-09-16 (1:03 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/aaron.md|Aaron Bockelie]]. English.

Pavel walked a blueprint of the CMS/Flex-POS back-end and the group settled how to build the **cloud "payment hub"** (the priority-#1 piece from the Sept-9 phasing) — its tech stack, the ACH-provider sequencing, a reconciliation MVP, and what a JVL "specification" should be. This is a **new, distinct session** from the Sept-9 [[wiki/meetings/2025-09-09-top-level-backend-architecture.md|top-level architecture]] (Val↔Pavel only, Russian) and the [[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md|Aug-14 kickoff]] (larger group) — it advances the payment-hub blueprint into concrete tech-stack and delivery decisions.

Substance and the dated arc entry: [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-16 section). In brief:

- **The Jan-1 bottleneck.** Val's opening frame: JVL has a **January 1** deadline for a big beta with **~10 operators** (hardware in temporary-mode format), and the most pressing bottleneck is **ACH processing** through a third party that sweeps money from operators' accounts onto JVL's bank account.
- **Pavel's architecture change.** Extend the existing legacy **Flexpay Manager** GUI to also set up **Flex-POS** terminals (same interface, minor changes); remove the direct terminal→InComm communication and move it to a **cloud "payment hub"** (a product name for the cloud service) that handles accounting, reporting, InComm communication and a **third-party ACH** integration. Future evolution: settings bind to the **location**, not the terminal, so hot-swappable devices pull their config from the control server.
- **Tech stack.** Nathan and Pavel agreed the payment hub is a **Java** API service deployed in a **cloud container**, with **Postgres** persistence — build with what the team already knows (Java/JavaScript) for near-instant output; horizontal scaling is "low-hanging fruit." ACH vendors are all **REST APIs over OAuth 2**, so an adapter can switch between vendors — the ACH-provider choice is **not** a blocking dependency for the tech stack.
- **Val's priority sequencing.** Have the back-end team build the cloud payment-hub service in **parallel** while **Nathan sources the third-party ACH provider** and onboards its API into the minimal architecture. Build a **reconciliation/accounting MVP early** (expected-vs-factual money — what JVL is owed vs what physically arrived in its account; reports across payment-hub↔location↔operator↔InComm).
- **Component-size rule.** Nathan's fault-isolation argument (specialized small modules limit blast radius) led Val to make it a work-order rule: **no component larger than a set size** — the payment hub is itself made of 3 components.
- **Specification standards.** Aaron surfaced formal frameworks — **TOGAF** (The Open Group), **ArchiMate**, **PlantUML**, **ISO** requirement/spec standards — but judged them **not a fit** for JVL's size and a January deadline ("you'll be spinning months"). Val wants only an **internal "specification of specifications"** — a lightweight agreed definition of what JVL considers a spec; he has a recording on it to circulate and align with Pavel.
- **Next steps / undertakings.** **Nathan:** gather API docs from his **3 focused ACH vendors** + reach out for sales/technical consulting; feed it to Pavel's team. **Pavel:** produce the deeper payment-hub architecture description (with Dima — [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] by context), then the API between Flex-POS/Flex-Pay↔payment hub and payment hub↔control server. **Meetings booked:** Nathan **Wed the 24th** (use cases driving payment-hub API requirements — ticket redemption, location-owner reconciliation, JVL auditing; then device provisioning); Pavel a **Monday** session on the specification.

## Sources

- [[raw/back-end_architecture_blueprint_review.md]]
