---
type: person
title: Nathan Carver
date: 2025-06-09
aliases: [Nathan, Nathan Carver, Code Carver]
source-count: 20
disambiguation: "Nathan Carver (Code Carver LLC) — the JVL contractor-roster 'Nathan' (see [[wiki/topics/jvl-contractor-roster.md]]); the June-9 2025 onboarding meeting confirms this 'Nathan' is him. Not to be confused with any other Nathan."
---

# Nathan Carver

Nathan Carver is a **software engineer / engineering-leadership contractor** brought onto JVL in **June 2025** to help clarify product capabilities and close scope gaps on the Georgia payment products under a hard deadline. His firm is **Code Carver LLC** (from the [[wiki/topics/jvl-contractor-roster.md|contractor roster]]); the June-9 initial meeting with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/juan-martinez.md|Juan Martinez]] is his first recorded appearance. [[raw/nathan_juan-initial_meeting-june-9-2025.md]]

## Background (self-described, June 9 2025)

- **~20 years as a software engineer** building full-stack applications across many technologies — **JavaScript, Java, C#, mobile, embedded systems, mainframe, and web**. [[raw/nathan_juan-initial_meeting-june-9-2025.md]]
- The **last five years** were mostly **leadership on large, complex projects** — including in **medical software** — taking a new domain, breaking the work down for the team, keeping the product well-defined, scoping features, and making sure engineers stay aligned with the rest of the organization (here, the market). He describes himself as "dynamic in the software workflow": can write code but also help a team expand and prioritize its workflow. [[raw/nathan_juan-initial_meeting-june-9-2025.md]]

## Why JVL brought him on (June 9 2025)

- Val framed the meeting's two objectives: introduce Nathan to Juan, and give Nathan the immediate product picture. JVL expects "**significant clearance or clarity on the product**" and **immediate help ensuring that the features being negotiated against various capabilities are exactly what the market wants — with no scope gaps or things falling through the cracks.** [[raw/nathan_juan-initial_meeting-june-9-2025.md]]
- Val walked him through the **Georgia** market: a "skill slot machine" market where cash payout is prohibited today; a 2024 law lets wins convert to a **prepaid MasterCard**, becoming **mandatory June 1 2026**; validation runs through JVL's partnership with **[[wiki/organizations/incom.md|INCOMM]]** (JVL = hardware supplier, INCOMM = clearing house). Two business models: **temporary e-wallet** (near beta) and **TITO** (~75% to beta). Rollout target: begin TITO in the field the **first week of September**, ~**50–100 units across ~10–20 locations (more likely 20)** with multiple operators, through **December**; **deals start closing January**. [[raw/nathan_juan-initial_meeting-june-9-2025.md]] (Market context: [[wiki/projects/georgia-market-rollout.md]], [[wiki/topics/flexpay-business-architecture-payout-devices.md]].)
- [[wiki/people/juan-martinez.md|Juan]] would separately take Nathan through the e-wallet and TITO business models. [[raw/nathan_juan-initial_meeting-june-9-2025.md]]

## June 11 2025 — POS / Mother Goose onboarding

- On the [[wiki/meetings/2025-06-11-pos-mother-goose-manual-model.md|June-11 POS meeting]] Nathan was being brought up to speed on the new manual **POS** compliance model for Mother-Goose-only operators; Juan noted "there's a lot here for Nathan to digest… understanding FlexPay, understanding FlexPort," and the deep-dive was pushed to the Friday 6 a.m. session. [[raw/POS_mutha_goose_architecture-june-11-2025.md]]

## June 18–19 2025 — driving the FlexPOS use cases

- On the [[wiki/meetings/2025-06-18-gcoam-ticket-redemption-workflow.md|June-18 ticket-redemption session]] Nathan ran the workflow whiteboarding on **Confluence**, mapping the Tito redemption use case; he confirmed engineers still track in **Jira** (empty FlexTower/FlexPOS GitHub repos exist) and took the direction to build a JIRA requirements ticket for the "scan & validate" work. Val **redirected him from FlexTower to FlexPOS** (now priority #1) and to a meeting with [[wiki/people/aaron.md|Aaron]] to organize Jira. [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]
- On the [[wiki/meetings/2025-06-19-flex-pos-use-case-design.md|June-19 Flex POS session]] Nathan wrote the initial **"Manual Ticket Redemption for FlexPOS"** use case with [[wiki/people/pavel.md|Pavel]] for the Sept-1 beta — the Incom three-call API, the $2-fee flow, and the personas. (Full substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].) [[raw/flex_POS-use_case_architecture_requirements-june-19-2025.md]] [[raw/flex-POS_design-june-19-2025.md]]

## Jul 2025 — the transactional-architecture deep-dive arc

At the end of July Nathan led the two-session **transactional-architecture** arc (full substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]).

- **Jul 10** ([[wiki/meetings/2025-07-10-defining-product-capabilities.md]]): on the product-capabilities working session Nathan relayed InComm's **cloud-processing** recommendation (Incom disables by account not site-ID, so JVL's cloud should do the activation as a pass-through) — a "dramatic change" in architecture — and took the undertaking to **speak to John about the processing module** and start the **block-diagram system architecture** with Pavel for Val's review; the meeting split **Flex Tower from the Flex Redemption Center** and resolved to **outsource the transaction-processing module** to a specialist. [[raw/Defining Product Capabilities.md]]
- **Jul 29** ([[wiki/meetings/2025-07-29-transactional-architecture-ewallet-deep-dive.md]]): whiteboarded the **e-wallet architecture** with the **redemption kiosk as location hub** (wallet created only at the kiosk, PIN bound to the printed ticket barcode, kiosk syncs to the JVL cloud), then ran fraud/failure risk scenarios and raised the processing-application + database-cluster **redundancy** requirement. [[raw/Transactional-Architecture-Discussion-2025-07-29.md]]
- **Jul 31** ([[wiki/meetings/2025-07-31-transactional-architecture-continuation.md]]): had added summary docs to GitHub + a Confluence diagram; reframed data-sync from clustering to **event-driven message-queue replication** (with a Claude-generated trade-off matrix); took the undertaking to add an **operator mobile app to all schematics**. [[raw/transactional_architecture-july-31-2025.md]]

## Aug 2025 — Flex-POS capabilities dashboard + backend-architecture kickoff

- **Aug 6 mid-iteration sync** ([[wiki/meetings/2025-08-06-flex-pos-mid-iteration-sync.md]]): Nathan presented his GitHub **"flex-requirement" (FR) capability dashboard** — 9 capabilities in two maturity states, GitHub as the single source of truth with JIRA links circling back, counts updated manually (with Claude), and the team's Claude instructions/agents committed to source control for consistency. He agreed to split the ticket data structures into separate Mother-Goose/Tito/e-wallet folders and to build requirements by stepping through use cases (next: cashier authentication). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]]
- **Aug 14 backend-architecture kickoff** ([[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md]]): Nathan probed how (and whether) the CMS must integrate with the transactional system, and — with Aaron's Fujitsu/Verifone POS pattern as a model — endorsed taking the provisioning/encryption ideas and trading them off against JVL's timeline for the single POS + dispenser. In the phased plan he owns the **Phase-1 transactional-products MVP** (with Juan). See [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md]]. [[raw/backend_architecture-august-14-2025.md]] [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- **Aug 20 CMS/PayFlex block-diagram review** ([[wiki/meetings/2025-08-20-cms-payflex-block-diagram.md]], session 1 of 3): Nathan attended as JVL's technical product manager, being brought current on the PayFlex ecosystem and CMS; he proposed building an **adapter between the legacy and new CMS** and "slowly moving the source of truth to the cloud" (new data-persistence in the cloud). See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/CMS- Block Diagram_Arch.md]]

## Sept 3 2025 — ACH provider + dispute-resolution use case

On the [[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md|Sept-3 Flex Capabilities weekly]] Nathan (surveying providers with Claude) recommended an ACH-focused API house — transcribed "Diwala/Duwalla," **almost certainly Dwolla** (inference) — now integrated with **Plaid** for instant balance verification before a transaction (0.5%/transaction, $5 cap, $0.05 min). He also presented the Flex-POS **dispute-resolution use case** (cashier swipes the card, the device shows the fee/confirmation the player accepted, escalation to InComm's printed number), driven by his own audit trail card↔Mother-Goose-ticket. See [[wiki/organizations/incom.md]] (Sept-3). [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]

## Sept 16 2025 — payment-hub blueprint review

On the [[wiki/meetings/2025-09-16-backend-blueprint-payment-hub-review.md|Sept-16 blueprint review]] (1:03 PM, with Val + Pavel + Aaron) Nathan set the payment-hub tech stack with Pavel — a **Java** API service in a cloud container, horizontal scaling as low-hanging fruit, ACH vendors all **REST over OAuth 2** (switchable adapters). He owns **sourcing the third-party ACH provider**: gathering API docs from his **3 focused vendors** and reaching out for sales/technical consulting to feed Pavel's team. Booked to meet Val **Wed the 24th** to drive payment-hub API requirements from use cases (ticket redemption, location-owner reconciliation, JVL auditing) then device provisioning. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-16). [[raw/back-end_architecture_blueprint_review.md]]

## Sept 22 2025 — assigned the Flex POS specification

On the [[wiki/meetings/2025-09-22-specification-standards-review-aaron.md|Sept-22 specification-standards review]], when Val ruled that JVL spec **Omni first**, he assigned the **Flex POS specification to Nathan** in parallel because Flex POS is isolated ("we can put Nathan on that job and he can probably do a decent job"). Aaron and Val also agreed Nathan is **not** the Omni product owner. [[raw/specification_standards_review-september-22-2025.md]]

## Oct 8 2025 — ACH vendor-readiness table + FedNow research

On the [[wiki/meetings/2025-10-08-flex-capabilities-ach-vendors-fednow.md|Oct-8 Flex capabilities weekly]] (12:05 PM, with Val + [[wiki/people/pavel.md|Pavel]]) Nathan presented a **seven-provider ACH vendor-readiness table** (Dwolla, Modern Treasury, Stripe, Tabapay, Moov, Phoenix, Sila) with pricing and use-case fit — recommending **Dwolla** as ready-to-go with the fewest unknowns; **Modern Treasury** as a SaaS layer over JVL's Bank of America; **Stripe** (ACH pull, ~1.5%) pending its answer; **Tabapay** parked for high volume; **Moov** having asked for JVL's EIN. He took the undertakings to **schedule the Dwolla integration in Jira with Pavel** and to **dig into FedNow** (the near-real-time Fed rail Val surfaced — connection via a regulated institution or a Fedline third party) plus the NSF failure-mode use case. He'll put the Dwolla API on the development path (BEP 2656 / Nov-12). See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct-8). [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]

## Nov 5 2025 — Dwolla onboarding kickoff

On the [[wiki/meetings/2025-11-05-jvl-dwolla-onboarding-kickoff.md|Nov-5 Dwolla kickoff]] Nathan is on JVL's side as the ACH technical lead; Dwolla's Cody worked to get him invited to the onboarding project portal that morning (he hit a technical sign-in issue). The session is the first working call directly with Dwolla — the vendor Nathan had recommended and put on the dev path in October. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-5). [[raw/JVL_Dwolla-november-5-2025.md]]

## Nov 5–10 2025 — ACH-module spec review (state diagrams, Dwolla flow, retries)

Across the three ~7 AM ACH-module spec-review sessions Nathan is JVL's ACH technical advisor: he supplied the initial invoice/ACH-transaction **state-diagram** concepts (created → in-process → pending → completed/failed) the engineers build from, explained the Dwolla **verified/unverified customer** model, **drop-in UI components vs API integration**, and Plaid-based account verification, and raised the Dwolla balance/wallet-vs-direct-transfer question (Nov-6) and retry/escalation logic tied to error codes (Nov-10). Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov 5–10 ACH-spec arc). [[raw/Payment HUB_ACH module specification_05.11.25 .md]] [[raw/Payment HUB_ACH module specification_06.11.25.md]] [[raw/Payment HUB_ACH module specification_10.11.25.md]]

## Sources
- [[raw/JVL_Dwolla-november-5-2025.md]]
- [[raw/Payment HUB_ACH module specification_05.11.25 .md]]
- [[raw/Payment HUB_ACH module specification_06.11.25.md]]
- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
- [[raw/specification_standards_review-september-22-2025.md]]
- [[raw/back-end_architecture_blueprint_review.md]]
- [[raw/Flex_capabilities_weekly_update-october-8-2025.md]]
- [[raw/CMS- Block Diagram_Arch.md]]

- [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]]
- [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]
- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/backend_architecture_meeting_undertakings_august_14_2025.md]]
- [[raw/Defining Product Capabilities.md]]
- [[raw/Transactional-Architecture-Discussion-2025-07-29.md]]
- [[raw/transactional_architecture-july-31-2025.md]]
- [[raw/nathan_juan-initial_meeting-june-9-2025.md]]
- [[raw/POS_mutha_goose_architecture-june-11-2025.md]]
- [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]
- [[raw/flex-POS_design-june-19-2025.md]]
- [[raw/flex_POS-use_case_architecture_requirements-june-19-2025.md]]
