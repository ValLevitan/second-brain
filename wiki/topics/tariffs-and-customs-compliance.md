---
type: topic
title: Tariffs and customs compliance (US–Canada tariffs, HS-code tracking, CBSA validation)
date: 2025-04-28
aliases: [tariffs, US-Canada tariffs, HS code, HS codes, harmonized system, country of origin, intercompany transfer pricing, BOM plus 30, CBSA, Canadian customs, CARM, trade compliance validation, international trade attorney]
source-count: 2
open-commitments: 2
open-questions: 2
---

# Tariffs and customs compliance (US–Canada tariffs, HS-code tracking, CBSA validation)

How JVL is bracing for the 2025 US–Canada tariff environment and customs scrutiny of its cross-border component and machine flows. Two threads converge here: the tariff/HS-code strategy Val laid out on the Apr-28 Business Central call, and a Canadian-customs (CBSA) validation on China-origin imports raised on the Apr-30 call. Related: the Mexico [[wiki/meetings/2025-03-19-asimex-flex-importation.md|Asimex importation]] work and the 2023 Colombian ruling that JVL machines are Canadian-origin (see [[wiki/people/maria-sanchez.md]]).

## The tariff problem (Apr 28 2025)

- Every shipment to the US "is going to go through… but the cost is a toss-up" — the tariff amount and **who absorbs it** are outside JVL's control. Val is **squeezing importations to the minimum** to build runway, and **advising customers that pricing will eventually increase**. [[raw/business_central_update-apr-28-2025.md]]
- Val credited a pre-Christmas 2024 decision as buying breathing room: JVL "worked non-stop, no holidays… and shipped **330 machines to Georgia**" before the tariff situation tightened. [[raw/business_central_update-apr-28-2025.md]]

## Intercompany-transfer strategy to minimize tariffs

- Val's stated strategy: the Canadian company ([[wiki/organizations/jvl.md|JVL Labs]]) **sells to the US company (JVL Systems) at the cost of the bill of material + 30% markup**, so that is the value crossing the border. Tariff is then paid only on the **marginal** intercompany price (illustratively ~$4,000) rather than the full retail value (~$12,000). [[raw/business_central_update-apr-28-2025.md]]
- Consequence: tariffs "will virtually prohibit us from selling directly from Canada to anybody in the US" — direct Canada→US customer sales stop making sense, since the customer would pay tariff on the whole machine. [[raw/business_central_update-apr-28-2025.md]]

## HS-code / country-of-origin tracking (the most pressing action)

- JVL must track, per component: **country of origin** and **HS (Harmonized System) code / tariff classification**, verified with Customs ahead of import, and record it **inside the ERP** by adding an **HS-code field to the vendor card** for each purchased item. Val: out of all the action items, "tracking HS numbers is the most pressing one" — do it in **Navision now** (the system holding most purchasing), pending the BC migration. [[raw/business_central_update-apr-28-2025.md]]
- Mechanic Val and Lev worked through: HS numbers are fixed, but the **country of origin drives which HS number applies through transformation of origin**. Example given — metal-fabrication parts bought from **China** come in under one HS number; when JVL sells a **V-Deck** to a US customer it is a different part number under a **different HS number, sold as made-in-Canada**. JVL "was tracking it for Columbia" but "slacked off"; [[wiki/people/mikhail-perelman.md|Michael]] is believed to have been tracking it. [[raw/business_central_update-apr-28-2025.md]]
- Val is **hiring a qualified international-trade attorney** for incoming/steady customs work and **assigning [[wiki/people/mary.md|Mary]]** closely to the HS/tariff subject. [[raw/business_central_update-apr-28-2025.md]]

## CBSA China-import validation (Apr 30 2025)

- JVL received an **April 24** email from **CBSA (Canadian Customs)** — a **"Trade Compliance Validation"** on merchandise imported from **China into Canada**, obtained through the **CARM** system. It only asks JVL to confirm the **contact person (name, title, mailing address)** for customs documentation; CBSA will then send a letter about **past importations**. JVL uses a Canadian **broker** (paperwork only, no commercial negotiation). [[raw/cbsa_maria_sanchez-april-30-2025.md]]
- Val engaged the **Colombian firm of [[wiki/people/maria-sanchez.md|Maria Sanchez]]** as an advisory "quarterback" — explicitly **not as Canadian legal counsel** (they cannot give a reliance opinion on Canadian law), working hourly. They will run a conflict check and send a proposal Friday; Val will answer the initial CBSA email himself and set up a common document drive. A colleague ("Marina") is checking for a Canada–China free-trade agreement. [[raw/cbsa_maria_sanchez-april-30-2025.md]]

## Open commitments

- [ ] JVL (Lev, priority #1) — add an HS-code field to the vendor card and start tracking HS code + country of origin per item in Navision — due unspecified (top priority) — [[raw/business_central_update-apr-28-2025.md]]
- [ ] Maria Sanchez's firm — run a conflict check and send Val an hourly-rate proposal for advising on the CBSA response — due Friday (~May 2) — [[raw/cbsa_maria_sanchez-april-30-2025.md]]

## Open questions

- Does a Canada–China free-trade agreement exist (bearing on the China-import tariff/origin treatment)? Being checked. [[raw/cbsa_maria_sanchez-april-30-2025.md]]
- What will CBSA actually request in its follow-up letter (origin, valuation, or routine input verification), and what is JVL's exposure? Unknown until the letter arrives. [[raw/cbsa_maria_sanchez-april-30-2025.md]]

## Sources

- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/cbsa_maria_sanchez-april-30-2025.md]]
