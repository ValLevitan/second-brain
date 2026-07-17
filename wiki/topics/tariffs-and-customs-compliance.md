---
type: topic
title: Tariffs and customs compliance (US–Canada tariffs, HS-code tracking, CBSA validation)
date: 2025-04-28
aliases: [tariffs, US-Canada tariffs, HS code, HS codes, harmonized system, country of origin, intercompany transfer pricing, BOM plus 30, CBSA, Canadian customs, CARM, trade compliance validation, international trade attorney, duty drawback, transitional export waiver, slot machine component subcategory]
source-count: 7
open-commitments: 6
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

## HS-code progress + the Canadian audit (May 1 2025 — Lev action-list review)

On the May-1 action-list review ([[wiki/meetings/2025-05-01-action-list-review-lev-rudky.md]]), Val and [[wiki/people/lev-rudky.md|Lev]] worked point #2 (HS tracking, the highest-priority item) to a near-complete state: [[raw/action_list_review_lev_rudky-may-1-2025.md]]

- **HS codes assigned, country-of-origin not yet.** In **Navision**, HS codes are now assigned to **every purchased component** (not just at the vendor level); **country of origin** is the one missing field. Lev called it "90% there" — for the current **Canadian Customs audit**, once country of origin is added JVL "can definitely print a complete report." The audit only wants what was imported under which HS code and whether tariffs due were paid. [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- **Deliverable:** an **Excel report by vendor, by part/item description, by HS code** for all imports from **China and Korea** (US excluded for now), with English HS descriptions — due **the evening of May 2**. Focus is "specifically on imports from China specifically to Canada." [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- **New China→Canada tariffs.** Both Val and Lev noted, as something newly discovered, that there are now tariffs on imports **from China to Canada** ("something new that I was not aware of"). For the current audit the Canadian side is "just to classify." [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- **The two-HS-number export point (restated):** imports enter Canada under one HS number; when JVL applies work and exports the finished product to the US it moves under a **different HS number** (transformation of origin) — a future **US Customs** question, not part of this Canadian audit. [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- **Standardise HS-per-component across all companies.** Val's rule: any future company (JVL Systems US, a Puerto-Rico/Peru/Mexico/Colombia entity) must set up purchasing so **every vendor+part carries an HS code from that country's table** — "a setup where a purchase could be made from the system that doesn't have HS code must not be implemented." [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- **Colombian firm as file-manager (final negotiation).** Val said he is in **final negotiation to hire the same Colombian firm that won JVL's earlier trade case** — international-trade/tariff specialists — as a proactive **"file manager"** to keep a fully-prepared, easily-defensible dossier, **not** for litigation (a licensed firm would be retained separately if litigation comes). This is the same firm as [[wiki/people/maria-sanchez.md|Maria Sanchez]]'s (the CBSA-matter advisor). [[raw/action_list_review_lev_rudky-may-1-2025.md]]

## Val's supply-chain / tariff exposition (May 1 2025 — game-design review)

Prompted by [[wiki/people/michael-gottlieb.md|Michael]] asking whether tariffs affect JVL, Val laid out the exposure on the [[wiki/meetings/2025-05-01-game-design-review.md|May-1 game-design review]] ("Huge"): [[raw/game_design_review-may-1-2025.md]]

- **Industry-universal.** "There is no such thing as an American-made slot machine for the most part" — **IGT's cabinets are made in Mexico**, parts come from China; **IGT was first to publish a tariff price increase**, so everyone follows. JVL's bill of material "will go up," and suppliers "are not ready," forcing larger orders and more inventory held. [[raw/game_design_review-may-1-2025.md]]
- **Canada's 100% surcharge on Chinese steel** — but the classification is unclear (rolls of steel vs prefabricated single-purpose cabinets); if it applies to all incoming metal it would be "a catastrophic event." [[raw/game_design_review-may-1-2025.md]]
- **China-vs-Canada sourcing math.** A Chinese order arrives **~90 days** door-to-door (incl. ocean + rail); an identical Canadian order runs **~120–180 days**, and no single Canadian supplier can make the ~50-part variety (would need ~5 vendors, which don't exist in Ontario). Canada also **cannot chrome-plate plastic** anywhere (nearest supplier Ohio) and **cannot apply textures** (DuPont/Dunlop closed their Canadian reps). JVL is moving away from chrome to **black + textures**. [[raw/game_design_review-may-1-2025.md]]
- **Ship-to-Georgia-for-assembly doesn't escape it:** shipping cabinets to Georgia to assemble there draws a **100–200% surcharge** — "that business is dead." JVL is considering **its own sheet-metal fabrication** (possibly split with a partner) or moving to **fiberglass forms** (rejected historically as costly/manual). A **CNC machine** today has a **~3-year waiting list**. [[raw/game_design_review-may-1-2025.md]]
- **Mitigation already in place:** JVL built a large buffer inventory (hundreds of machines) and — post the Colombian court case — every purchased item already carries its own HS code; open risk is whether the code gets "challenged or misinterpreted or reinterpreted." [[raw/game_design_review-may-1-2025.md]]
- **Belarus manufacturing idea (floated).** No tariff **China→Belarus** and no tariff **Belarus→US**, plus a **tax-free zone by the airport**; goods could be labelled "manufactured in Belarus" and shipped to the US tariff-free. China→Belarus transit ~1 month (landlocked, single rail branch, ~20 days). Contingent on geopolitics ("if Trump makes nice with Putin"). Recorded as Val's speculative option, not a plan. [[raw/game_design_review-may-1-2025.md]]

## Analyst research memo (May 2 2025)

A staged research/analysis document ("Dodging the tariff bullet") assembled for JVL. It is an **analyst memo, not a JVL primary source or an owner ruling** — its figures are external claims and some are illustrative; recorded here with that caveat. [[raw/tariff_effect_jvl_research-may-2-2025.md]]

- **Rates cited:** slot machines classified under **HS 9504.30**; Chinese components into Canada **0–6.5%** under MFN (Korea mostly duty-free under the Canada–Korea FTA); finished machines Canada→US **0% if USMCA-compliant, 25% if not** (since March 2025); Chinese goods reaching a **145% total tariff** by April 2025 (10% Feb → 20% March → 145% April). [[raw/tariff_effect_jvl_research-may-2-2025.md]]
- **USMCA qualification** to avoid the 25%: either a **tariff-shift** (non-originating materials change classification) or **Regional Value Content of 60% (Transaction Value) / 50% (Net Cost)**, hinging on whether Canadian manufacturing is a "substantial transformation"; a **10% de-minimis** allowance exists (up from NAFTA's 7%); records must be kept **5 years**. [[raw/tariff_effect_jvl_research-may-2-2025.md]]
- **Mitigation levers suggested:** US **Foreign Trade Zones**, **duty drawback** (reclaim up to 99% of duties on components when the finished product is exported), **binding rulings**, component diversification ("China+Many" — Taiwan/Malaysia/Vietnam), and tariff engineering (ship components separately as "kits"). The memo claims peers cut effective rates from 25% to under 8%. [[raw/tariff_effect_jvl_research-may-2-2025.md]]
- Note it also flags a **162% increase in CBP anti-circumvention determinations**, targeting exactly JVL's profile (Canadian assembly of Chinese components for US export) — relevant to the CBSA validation thread above. [[raw/tariff_effect_jvl_research-may-2-2025.md]]

## Commercial-side restatement (May 16 + 19 2025 — Klimovich updates)

Two [[wiki/people/andrei-klimovich.md|Klimovich]] updates restated the tariff picture from the ECHO/distributor angle (facts here; product-pricing detail on [[wiki/topics/echo-home-gaming-device.md]]):

- **Metal-parts tariff band + USMCA exemption.** Andrei's read: finished JVL products under the **9504** HS code (with a certificate of origin) should ride the **USMCA exemption** into the US, while **metal parts / metal cabinets imported from China into Canada** are the exposed input, carrying roughly **8–25%** (rumored to rise) — consistent with the Apr-28/May-1 two-HS-number transformation-of-origin mechanic above. Val: absorb a small tariff effect, pass on a significant one. [[raw/update_andrei_klimovich-may-19-2025.md]]
- **Home-version price move (contemplated, not announced):** distributor price possibly **$3,080 → $3,400**; Val's guidance to distributors — describe it as contemplation pending official guidance, honor current prices, reserve stock before any increase. [[raw/update_andrei_klimovich-may-19-2025.md]]
- **HS 95.04.30.0010** appears on JVL's certificate of origin — used to unstick Burger King's border-held return (see [[wiki/organizations/burger-king.md]]). [[raw/update_andrei_klimovich-may-19-2025.md]]

## CBSA matter — new customs advisors introduced (June 11 2025)

Val was introduced to a **customs / international-trade specialist, [[wiki/people/lucie.md|Lucie]]** ("Lucy"), by the lawyer [[wiki/people/alan.md|Alan]] (a ~40-year advisor of Val's who does not practice customs), for the same **CBSA China-import** problem. Whether Lucie/Alan's firm is the same engagement as [[wiki/people/maria-sanchez.md|Maria Sanchez]]'s Colombian advisory (Apr-30, also on the CBSA matter) is **unresolved — queued Tier A**. [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]

- **The exact classification dispute stated plainly.** JVL imports **formed, painted sheet-metal cabinet parts from China**. Border/customs are charging the **25% steel/aluminum tariff** on them; Val's argument is that a **bent, hole-punched, single-purpose slot-machine cabinet part cannot be repurposed** for anything else, so it belongs in the **slot-machine-component subcategory** (Val cites ~"9500-something") rather than the generic sheet-metal category. Classification hinges on **primary use** (general-use vs specific-use rules); the specific category should prevail if the part can't be used for anything else. Nobody has previously used the subcategory because **components were never a tariff subject for the past 20–30 years** — "we haven't had to." [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- **The end-to-end tariff logic Val relies on:** a **complete slot machine is tariff-exempt China→Canada and Canada→US** (Val: he could fabricate the whole machine in China and ship it through Canada tariff-free); it is only **importing components, assembling, and re-exporting** that draws the 25% on the metal. Val: preserve the current HS numbers as much as possible; the sheet metal enters under one number (he referenced **tariff 84**) and the finished machine exports under the slot-machine number (**~95 / "9400-something"**). [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- **The won-case precedent (Colombia).** Val recounted winning a case where the **government of Colombia** claimed he was merely a **transit center** (China→Colombia) not adding value — he proved value-add via the **change of tariff number** in vs out. (This is the same Colombian trade win handled by [[wiki/people/maria-sanchez.md|Maria Sanchez]]'s firm; here recorded as Val's own framing.) He wants to be careful changing tariff numbers so as not to disturb the value-add argument. [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- **Duty-drawback / transitional export waiver (Alan's angle).** Alan raised the old **duty-drawback licence** he'd seen at companies he sold — reclaim/avoid the tariff when goods are re-exported within a few years — and JVL's **freight forwarder** separately mentioned a **transitional licence / waiver** for goods that are **100% exported** and not consumed in Canada. They will look into whether it still exists (there are **new CBSA rules for release of goods before payment as of April 2025**). [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- **US vs Canada guidance.** Because **Canadian customs decisions are not public** (US ones are), Alan/Lucie's firm can look at how the **US treated a matter under the harmonized system** and reach out to a **US colleague** — relevant because Canada and the US share the harmonized HS system. [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- **Deadline:** JVL has a **CBSA reply due June 16**; Val will send Lucie the current HS classification number + product descriptions, and Alan will respond to CBSA's last email (cc Lucie). If needed, the reply is to say lawyers were retained and request an extension. [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]

## Open commitments

- [ ] Val — send [[wiki/people/lucie.md|Lucie]] the current HS classification number + product descriptions for the China-origin cabinet metal — due right away (before the June-16 CBSA reply) — [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- [ ] [[wiki/people/alan.md|Alan]] — respond to CBSA's last email (cc Lucie); reply or request an extension by June 16 — due by June 16 — [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- [ ] [[wiki/people/lucie.md|Lucie]] / Alan — study whether JVL qualifies for a duty-drawback / transitional export-waiver licence (and the specific-vs-general HS classification), given the new April-2025 CBSA release rules — due unspecified — [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
- [ ] JVL (Lev, priority #1) — add an HS-code field to the vendor card and start tracking HS code + country of origin per item in Navision — due unspecified (top priority) — [[raw/business_central_update-apr-28-2025.md]]
- [ ] Lev — deliver the Excel report (by vendor / part / HS code + English descriptions) for all China & Korea imports — due evening of May 2 — [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- [ ] Maria Sanchez's firm — run a conflict check and send Val an hourly-rate proposal for advising on the CBSA response — due Friday (~May 2) — [[raw/cbsa_maria_sanchez-april-30-2025.md]]

## Open questions

- Does a Canada–China free-trade agreement exist (bearing on the China-import tariff/origin treatment)? Being checked. [[raw/cbsa_maria_sanchez-april-30-2025.md]]
- What will CBSA actually request in its follow-up letter (origin, valuation, or routine input verification), and what is JVL's exposure? Unknown until the letter arrives. [[raw/cbsa_maria_sanchez-april-30-2025.md]]

## Sources

- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/cbsa_maria_sanchez-april-30-2025.md]]
- [[raw/action_list_review_lev_rudky-may-1-2025.md]]
- [[raw/game_design_review-may-1-2025.md]]
- [[raw/tariff_effect_jvl_research-may-2-2025.md]]
- [[raw/update_andrei_klimovich-may-19-2025.md]]
- [[raw/tariffs_lucie_alan_intro-june-11-2025.md]]
