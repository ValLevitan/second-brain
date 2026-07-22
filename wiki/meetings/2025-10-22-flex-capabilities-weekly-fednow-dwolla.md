---
type: meeting
title: Flex capabilities weekly — FedNow needs an FI, Dwolla onto the dev path anyway, InComm 24h-gap ask, features split (Oct 22 2025)
date: 2025-10-22
aliases: [flex capabilities weekly Oct 22, FedNow financial institution, Wells Fargo FedNow, Dwolla $0.75 transaction, InComm 24 hour gap, ACH adapter 8 features, reconciliation module 15 features, BEP 2656, BEP 2657]
source-count: 1
open-commitments: 3
open-questions: 1
---

# Flex capabilities weekly — FedNow needs an FI, Dwolla onto the dev path, features split (Oct 22 2025)

**Date:** 2025-10-22 (recording header 8:03 AM / displayed 12:03 PM) · **Attendees:** [[wiki/people/nathan-carver.md|Nathan Carver]] (host), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/juan-martinez.md|Juan Martinez]]. English.

> **Filename/header discrepancy (§11):** the staged file is named `Flex-POS_ACH_API_integration-october-21-2025.md`, but its recording header reads **"Flex Capabilities Weekly Update-20251022_080343"** dated **October 22 2025** — the header wins, so this stub is dated **2025-10-22**. It continues the recurring Flex-capabilities / payment-hub weekly cadence ([[wiki/meetings/2025-10-01-payment-hub-ach-vendor-weekly.md|Oct-1]] · [[wiki/meetings/2025-10-08-flex-capabilities-ach-vendors-fednow.md|Oct-8]]).

Substance lives on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Oct-22 section). **§15.8:** vendor/company economics only (Dwolla/FedNow fees) — no named-person compensation.

Durable points (single source):

- **The two payment-hub modules are defined.** Nathan has the **ACH adapter module** (the swappable component, one per provider — supports changing providers or running more than one) and the **reconciliation module** (the business rules that run the daily transfer jobs for all locations) well-defined — **23 requirements** total, one last refinement, then into Jira this week. Development is built primarily against **Dwolla's API** ("Duala/Dwala") — its reference IDs, callback hooks for ACH completion, and transaction types. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **FedNow requires being a financial institution.** Nathan's research: you must **be a financial institution to use FedNow directly**, so JVL cannot — it must go through an FI or be designated as one. **Dwolla supports FedNow**, so JVL can reach it through Dwolla (still paying Dwolla as middleman). Per Cody, Dwolla charges a flat **~$0.70–$0.75 per transaction for FedNow and RTP** (their two immediate/real-time styles), on top of the Dwolla cost, unless negotiated down. A **$0.75 transaction = one once-a-day grouped transaction per location** (e.g. 20 debits grouped into one); at 10 locations reconciled daily that is **~$7.50/day**. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **Dwolla's flat fee was NOT negotiated away.** Juan confirmed the **$2,500 + $2,500/month = $5,000** plus a **one-time $1,500 setup fee** still stand — it is an **off-the-shelf quote**. Val does not want to negotiate with Dwolla until he has **exhausted the Wells Fargo opportunity**, because the **most ideal / effective core solution is Wells Fargo with FedNow** (use FedNow under a Wells Fargo license, interfacing directly with ACH). [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **Wells Fargo meeting the same day.** A Wells Fargo / FedNow conversation was moved to **3:30**; Val will take it from his car with [[wiki/people/juan-martinez.md|Juan]], and wants to **zero in on FedNow** ("we need them for FedNow… if you can't provide it, go take a hike"), sending them a FedNow link if needed. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **InComm ACH-timing ask (Val's private negotiation).** InComm currently performs their ACH **every working day at 9:30**; Val has privately asked InComm to swipe JVL's account only **every second working day**, creating a **24-hour gap** between JVL receiving the money and InComm swiping it, plus 24 hours for JVL to swipe all its locations, run **full reconciliation, see which account is deficient in real time, and shut it off**. Today the team believes it has only **~30 minutes** between clients and ACH, so the window is "good news"; InComm hasn't refused. ("Elbow room.") [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **Decision: go with Dwolla now, don't wait for Wells Fargo.** Val's landing call — even if Wells Fargo comes on board, bureaucratic barriers mean no account before ~**March**, so use **Dwolla now** as the cost of market entry, and keep hoping for a positive Wells Fargo reply. Next objective: **negotiate Dwolla's price** and start the **technical setup**; Nathan to introduce Val to **Cody** (Dwolla's primary contact). Juan suggested converting the weekly calls to focus on the sandbox / API interaction. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **Timeline.** Location rollout ~**Jan 1** (realistically mid-January); beta test ~**Dec 1**; get the ball rolling with Dwolla ~**Nov 1**. Dwolla can allocate a team quickly, but that team then needs a **30-day window** to stand up its side; a **sandbox account** is available for initial testing. JVL is **closed Dec 22 → Jan 5**. Pavel estimated integration ~**1 month** — start **~Nov 15**, finish ~**Dec 15** — noting the same people carry other projects (Flex POS backend must finish first; magnetic-card auth and roll-printer receipt printing are **not MVP** this year). [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- **Feature/requirement breakdown settled.** ACH adapter module = **8 requirement groups / 93 granular line items**; reconciliation module = **15 groups / 160 items**. The **reconciliation module is the primary core for JVL**; the Dwolla-facing piece is only the 8-group ACH adapter. Val's vocabulary landed: a **"group" ≈ a feature**, a **"module" = a product** — so ACH adapter = **8 features**, reconciliation = **~15 features** (first group example: "transfer initiation"). Pavel may join or split some groups. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]

## Open commitments

- [ ] Pavel Frolov — split **BEP 2656** (ACH API adapter) into ~8 features and **BEP 2657** (reconciliation module) into ~15 features, lay them out as a schedule assigned to individuals for the next meeting; target inclusion in sprints ~**Nov 15** with tentative delivery ~mid-December — [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- [ ] Nathan Carver — introduce Val to **Cody** (Dwolla primary contact) so Val can start negotiating price, and start the Dwolla technical setup (~Nov 1) — [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
- [ ] Nathan Carver — send Val the requirements links and put the 23 refined requirements into Jira this week — [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]

## Open questions

- Does today's Wells Fargo meeting yield a path to FedNow under a Wells Fargo license (the ideal core solution) before ~March — or does JVL proceed on Dwolla alone? Val decided to build on Dwolla now regardless; the Wells Fargo outcome is still open. [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]

## Sources

- [[raw/Flex-POS_ACH_API_integration-october-21-2025.md]]
</content>
