---
type: meeting
title: Flex capabilities weekly — ACH vendor readiness table, Dwolla on the dev path, FedNow discovered (Oct 8 2025)
date: 2025-10-08
aliases: [flex capabilities weekly Oct 8, ACH vendor readiness table, FedNow, Dwolla Modern Treasury Stripe Tabapay Moov, payment hub Oct 8, BEP 2656]
source-count: 1
open-commitments: 2
open-questions: 1
---

# Flex capabilities weekly — ACH vendor readiness table, Dwolla on the dev path, FedNow discovered (Oct 8 2025)

**Date:** 2025-10-08 (12:05 PM) · **Attendees:** [[wiki/people/nathan-carver.md|Nathan Carver]] (host), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]]. English.

The next Wednesday session in the recurring Flex / payment-hub capabilities weekly — continues the [[wiki/meetings/2025-10-01-payment-hub-ach-vendor-weekly.md|Oct-1 payment-hub weekly]] and the [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Sept-3]] cadence. What advanced: Nathan presented a **vendor-readiness table** across seven ACH providers, JVL committed to putting the **Dwolla API on the development path**, and Val surfaced **FedNow** as a cheap real-time alternative to dig into. Substance also on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct-8 section); Jira/GitHub split per [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. §15.8: vendor/company economics only — no named-person compensation.

Durable points (single source):

- **Vendor-readiness table (7 ACH providers).** Nathan has reached out to all; connections made with all but the bottom two (**Phoenix**, **Sila**). The top four he spoke to salespeople directly: [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
  - **Dwolla** ("Duwalla") and **Modern Treasury** both support JVL's use case well. **Dwolla is ready to go** — full support (they move the money, set up accounts, JVL just initiates via their API); could stand up a team and get JVL live in the next few months; ~**$2,500 minimum monthly** transaction charge, ~**$5,000/month minimum at 10 locations**, rising to ~**$13,000/month at 2,000 locations**. Fewest unknowns.
  - **Modern Treasury** is a **SaaS layer over JVL's existing bank (Bank of America)** — not in the middle of the money flow; a **flat ~$6,000/month fee** *plus* whatever BofA charges for the ACH transactions, so JVL would have two negotiation points (BofA + Modern Treasury).
  - **Stripe** does **ACH pull** (initiate a pull of funds from the location), which matches JVL's product, but that's outside Stripe's normal product — under evaluation; a **flat 1.5% fee on ACH pulls** ("pretty high"), ~**$1,600/month at a 10-location pilot** (vs >$5,000 for Dwolla/Modern Treasury) but **unreasonable at scale unless they cap it**. Still awaiting Stripe's answer (~early next week).
  - **Tabapay** is a good potential vendor but needs **high volume (1,000–2,000 locations)** — revisit once JVL scales.
  - **Moov** ("Move") responded asking for **JVL's EIN** (their way of verifying JVL is a real entity); Val/Nathan unsure whether to share it.
  - Per-location cost framing: ~**$500/location/month at the 10-location pilot**, dropping to ~**$10** then ~**$7/location/month** at scale (the platform fee, Dwolla quote, calculated with Claude). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- **FedNow surfaced as the cheap real-time option.** Val flagged **FedNow** (Federal Reserve): interbank clearing/settlement, funds sender→receiver in **near real time, any time, any day of the year**, with a **fraud tool**. Pricing per the table Val shared: the **$25 fee has been waived (2025)** and it's only a **half-cent per transaction**; the service dates to 2023, this is a 2025 summary. Caveat — you must connect through a **regulated deposit institution / credit union** (or possibly build a "Fedline connection" via a certified third party); it may or may not be open to the private sector. Nathan to dig into it (and into going through the bank directly). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- **Decision: Dwolla onto the development path.** Val: "let's start putting Dwolla API on the development path" and reflect it in the Jira plans (his "only instrument of truth"). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- **Jira schedule.** The payment hub sits under **IP632** (~9 features), scheduled well into the **first week of December**; the **ACH API adapter (BEP 2656)** is where Dwolla fits, a ~**2-week integration finishing ~Nov 12** — Pavel noted the estimate is rough (they haven't read the Dwolla API docs yet). The **job scheduler** work Nathan is looking at is already covered by **Spring Boot** in the existing tech stack (Java+). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]

## Open commitments

- [ ] Nathan Carver + Pavel Frolov — schedule the **Dwolla integration** and reflect it in the Jira plans for the next meeting — [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- [ ] Nathan Carver — dig further into **FedNow** (how to connect: via a bank/regulated institution or a certified third-party Fedline connection) and define the NSF / insufficient-funds failure-mode use case (for Pavel) — [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]

## Open questions

- Which ACH rail does JVL build on — Dwolla (on the dev path now, fewest unknowns) or the cheaper-at-real-time FedNow (if the private-sector access hurdle can be cleared)? Left open pending Nathan's FedNow research and Stripe's answer. [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]

## Sources

- [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
