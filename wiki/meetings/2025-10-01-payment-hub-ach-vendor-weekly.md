---
type: meeting
title: Payment-hub / ACH-vendor weekly (Dwolla vs Stripe pricing; reconciliation-engine design) (Oct 1 2025)
date: 2025-10-01
aliases: [payment hub weekly Oct 1, ACH vendor pricing, Dwolla Stripe Tabapay, reconciliation engine, flex capabilities weekly Oct 1, BEP 2656, BEP 2657]
source-count: 1
open-commitments: 3
open-questions: 1
---

# Payment-hub / ACH-vendor weekly (Oct 1 2025)

**Date:** 2025-10-01 (12:01 PM) · **Attendees:** [[wiki/people/nathan-carver.md|Nathan Carver]] (host), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]]. English.

The next Wednesday session in the recurring Flex / payment-hub weekly cadence — continues the [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Sept-3 flex-capabilities weekly]] and the payment-hub thread of [[wiki/meetings/2025-09-15-flex-pos-alignment-scheduling.md|Sept-15]] / [[wiki/meetings/2025-09-16-backend-blueprint-payment-hub-review.md|Sept-16]] / [[wiki/meetings/2025-09-26-payment-hub-technical-architecture-deep-dive.md|Sept-26]]. What advanced: the ACH-vendor evaluation produced concrete pricing (Dwolla demo + Stripe quote) and Nathan began the reconciliation-engine architecture. Substance lives on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct-1 section) and ties to the Jira/GitHub split on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. §15.8: only vendor/company economics recorded — no named-person compensation.

- **ACH-vendor pricing compared (Dwolla vs Stripe vs Tabapay).** Nathan/Pablo/Juan took the **Dwolla** ("Duwalla") demo Monday (sandbox + API keys); its pricing is a **$2,500 platform fee + $2,500 monthly minimum-usage fee = $5,000/month flat**, plus a **$1,500 one-time integration fee**, ~**$0.18 per transaction (standard T+3)** rising to ~**$0.48 same-day (T+0)** up to 1,000 transactions (total transactions across all locations, not per-bank), plus **$0.07 per balance check**. **Stripe** has no flat rate — **8% of the transaction up to a $5 cap** on ACH direct transfers — cheaper at low volume, and possibly able to do **batch processing** (hand Stripe one batch job rather than initiating thousands of debits). **Tabapay** effectively declined / doesn't publish. Val's read: charge locations ~**$50/account/month + ~1% transaction fee**; Juan to build a side-by-side pricing spreadsheet. [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- **Same-day ACH is not immediate.** T+0 still clears only through fixed daily processing windows (a ~10 AM ET cutoff for same-day; clearing only by a later window) and excludes weekends, so JVL must reconcile the **day before**, missing the 2–10 PM play that is the bulk of gaming — a real risk on a "street business" where card validation happens before the money is collected. Design so the ACH provider is a **swappable adapter** (even a fallback second provider) to avoid slowing initial development. [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- **Reconciliation-engine architecture started.** Nathan created a **reconciliation-engine module** under the system architecture (batch-processing orchestration, e.g. a 7 AM settlement job that computes each location's amount due and initiates per-location transfers), using Spring-batch concepts and possibly Azure worker queues; he asked how long architecture takes and what follows. Pavel: the **tech stack is Java + Spring Boot + PostgreSQL on AWS + Kubernetes**, chosen because it is **"most familiar"** (Val flagged that familiarity should not be the justification); **~80% of the architecture** should be finalized within ~2 weeks (by ~Oct 15). [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- **Jira/GitHub + schedule.** ACH development is scheduled to start **~November 1**; the payment-hub features are **BEP 2656 (ACH API adapter)** and **BEP 2657 (ACH API adapter + reconciliation module)**, with the ACH API adapter finishing **~November 12**. Nothing sits under those features because — per the Aaron agreement — **stories go in GitHub, not Jira** (Jira will "show nothing under these features for a while"). [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- **Distribution model open.** Val leaned toward engaging an **operator** rather than going direct to locations, and tied the pricing/use-case questions to that unresolved choice. [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]

## Open commitments

- [ ] Nathan Carver — get Stripe's full pricing sheet; verify with InComm/PAX whether their partners (John, Tom) charge monthly/transactional **ACH fees** on the handheld ("PAX"/"Apoxia") devices — [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- [ ] Juan Martinez — obtain a copy of an actual signed **PAX/location ACH contract** (via Felipe or a location) to read the real fee schedule; build the vendor **pricing-comparison spreadsheet** — [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
- [ ] Nathan Carver + Pavel Frolov — finalize **~80% of the payment-hub / ACH architecture** within ~2 weeks (by ~Oct 15) — [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]

## Open questions

- Will JVL price ACH as a monthly fee + per-transaction fee (Val's ~$50/account/month + ~1% sketch), and will it distribute through an operator or direct to locations? Left preliminary. [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]

## Sources

- [[raw/Flex-HUB_capabilities_weekly-october-1-2025.md]]
