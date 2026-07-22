---
type: meeting
title: JVL + Dwolla — ACH onboarding kickoff (Nov 5 2025)
date: 2025-11-05
aliases: [JVL Dwolla Nov 5, Dwolla onboarding kickoff, Dwolla enrollment, Dwolla sandbox]
source-count: 1
---

# JVL + Dwolla — ACH onboarding kickoff (Nov 5 2025)

**Date:** 2025-11-05 (3:19 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], and from **Dwolla** (the selected ACH vendor) **Cody Van Wyk** and **Nancy Baccam** (external — no pages). [[wiki/people/nathan-carver.md|Nathan Carver]], Monica, Juan and other JVL team members are referenced as portal participants. English.

The first working session directly with Dwolla — the ACH provider JVL put on the development path in October ([[wiki/meetings/2025-10-08-flex-capabilities-ach-vendors-fednow.md|Oct-8]] / [[wiki/meetings/2025-10-22-flex-capabilities-weekly-fednow-dwolla.md|Oct-22]]) — to understand how to enroll the engineers and how the platform is structured. Substance on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-5 Dwolla section).

Durable points (single source):
- **Customer/funding-source model for JVL.** JVL uses the **unverified customer** object (a retail/convenience-store location in Georgia), created **via API** — the dashboard creates only "receive-only users." The **bank funding source must be verified**; the customer stays unverified. JVL's funds flow is the **receive flow** (receiving funds in from customers), which Dwolla configures on its end.
- **Onboarding sequence (Rocket Lane portal, onboarding.dwolla.com).** Order of operations: register the production account → Dwolla **risk-team review** of the financial position / bank statements → the (integration) **contract signed first is the precursor** to kicking off the review. Cody still owes Val the contract; approval is ~a week out once financials are provided. Weekly / twice-weekly meetings with Dwolla's dev-relations team (Spencer, Shreya) going forward.
- **Legal deliverables.** The main legal documents Dwolla needs are **terms of service and privacy policy** (a link suffices if JVL has them on its site). Val asked to work with Nancy to get the precise list so JVL's legal team can move faster.
- **Account registration = Monica's task.** Monica is to register the **production account** (distinct from the sandbox "play" environment): KYC on JVL Inc — state of incorporation (Florida/Delaware), beneficial ownership, and an **EIN letter**. Cody had emailed her the guide; she hadn't yet created the account.
- **Sandbox cleanup.** The team had set up **5 separate sandbox accounts** (Pavel, Nathan, Dmitri, Serge, +1), each with isolated data; Nancy will configure each to match production and recommended consolidating onto one admin (Pavel) with invited team members sharing one API key (a separate staging account is fine).

**§15.8:** no compensation material — vendor-onboarding process only.

## Sources

- [[raw/JVL_Dwolla-november-5-2025.md]]
