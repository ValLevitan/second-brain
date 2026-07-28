---
type: organization
title: Diamond Amusement
date: 2026-07-23
aliases: [Diamond Amusement, Diamond, Diamond Amuse, Diamond Games]
source-count: 4
open-commitments: 3
open-questions: 2
---

# Diamond Amusement

**Diamond Amusement** is a **Georgia coin-operated-amusement-machine (COAM) master/terminal operator** running distributed routes — a JVL customer in the Georgia land-based market and, as of Feb 2026, a prospective **data-sharing partner**. It is led by its CEO/owner [[wiki/people/sean-fellows.md|Sean Fellows]], who the team treats as the **sole decision-maker** for the account. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]] [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]

Longstanding relationship with JVL: Sean recalled buying early **JVL countertops** from **Bob Whitehead** years ago and operating **Cash Code** equipment. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]] Diamond first bought JVL Georgia slot product (the "Peach One" build) in 2025 to start testing — [[wiki/people/felipe-miranda.md|Felipe]] installed it and met Sean and his tech (May 29 2025). [[raw/felipe_georgia_market_update-may-29-2025.md]]

## Scale and JVL footprint

- Diamond operates a portfolio of ~**1,000–1,200 units** across its routes (the summary states 1,200; in the debrief Val worked from a ~1,000-machine figure). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]] [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]
- JVL has **41 units** deployed at Diamond — about **4%** of Diamond's floor — averaging **$167 win-per-unit-per-day** (Feb 2026), well above the Georgia state average. [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]] [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- Diamond currently runs **3 JVL machines at one of its office locations**, which Sean offered as a first data-collection site (~1.5 hours from Felipe). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]] [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]

## Sean's Georgia market read (Feb 9 2026)

The benchmarking below is **Diamond's own operational data**, presented by Sean at the partnership meeting. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]

- **Market softness + saturation.** Diamond's revenues were declining, attributed to the government shutdown and bad weather over the recent 90-day cycle (Sean said the dip was industry-wide per five-year seasonality). Structurally, Georgia now runs **over 41,000 machines** (up from 36,000–38,000 in the 2021 COVID period); despite the ~14% machine growth, the **state average win-per-unit fell from a COVID-era ~$137 to ~$108** (~21% decline). Sean expects ~18 months of adjustment, including store closures. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- **Competitive benchmark** (win-per-unit across Diamond's portfolio): JVL **$167** (41 units); IGT "Price is Right" package **$221** (109 units), full IGT portfolio **$176** (182 units); **Aristocrat $305** (65 units, all in top-tier locations, ~25% fewer units than IGT); **Novomatic $169** (30 units). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- **Tiering.** Sean frames the market as the "**big three**" (Aristocrat, IGT, Light & Wonder) trading the top spot by location, a next tier of **JVL, Novomatic, and Bad Dog's "Hollywood Game"**, then "filler"/legacy. Premium equipment goes to top-tier locations first; underperformers get cycled out for a proven top performer. **Konami** entered and already exited Georgia (blamed on its distributor Bravery Gaming). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- **RTP as a penetration tactic.** New entrants launch at **94–96% RTP** vs legacy low-90s (JVL's H3 runs **92%**), buying player time to win share, then trimming RTP in later releases. Sean stressed volatility profile matters as much as RTP, and that the Georgia distributed route runs **~3–5 years behind land-based casino trends** — an opening for a manufacturer with casino intelligence. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- **Gift-card regulation (July 1).** The Georgia gift-card requirement is **statutory and enforced from July 1**, but there is **no kiosk mandate** — many retailers add gift-card capability via POS APIs. **InComm** reported serving **4,500+ locations** monthly and ramping; **Mike Harum** (COF division) sends educational comms; details published at **gacoam.com**; the lottery + GMOA scheduled three regional seminars. [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]

## The Feb 9 2026 data-sharing partnership

At the partnership meeting ([[wiki/meetings/2026-02-09-diamond-amusement-partnership-meeting.md]]) JVL proposed a **collaborative data-sharing arrangement** to fix its Georgia information deficit: place JVL machines in **tier-one locations directly alongside IGT / Light & Wonder / Aristocrat**, and across all three tiers (low / mid / premium), in exchange for granular operational data. Sean responded positively — offering to pull data from the 3 office-location JVL machines, facilitate field visits, deploy across all tiers, and provide **historical baselines** (he cited **$80 / $140 / $500** win-per-unit example locations). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]

JVL's offered value exchange: **free trial machines, extended warranty, spare-parts kits, first access to new game releases** (Fiery Ice Link, Jackpot Rush), and negotiable additional terms. JVL also previewed its **transactional product suite** (TITO, e-wallet, kiosk, POS card-dispensing, its own merchant/processing) for the new Georgia regulatory environment, and its next-generation **"liquid glass"** game portfolio (Fiery Ice Link, Jackpot Rush series, revamped Peak games). [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]] See [[wiki/projects/georgia-market-rollout.md]].

The same evening JVL held an **internal debrief** ([[wiki/meetings/2026-02-09-diamond-amusement-exec-debrief.md]]) that surfaced a performance concern and a data-reliability problem (below).

## Open questions

- Why does JVL's **new "enhanced nudge" software perform ~50% below JVL's older software** at Diamond (roughly $80 vs a $167 average) — is it a genuine regression, a lower-tier placement of the upgraded machines, or a reporting artifact? Only ~10% of Diamond's JVL cabinets carry the new software, mostly ones that returned to the warehouse for TITO/printer retrofit before redeployment. Team could not resolve it without field data. [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]
- Are the **Intralot / GLC reports** JVL relies on even trustworthy? The debrief found garbage meters (impossible billions/trillions wagered, negative game profit) traced to an old **Mother Goose** misconfiguration whose bad pay-table-ID data is never cleaned up; the **Co-am ID intentionally obscures machine serial and location**, so JVL cannot tie a machine on the report to a place. Sean imports the same GLC reports into pivot tables. [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]

## Open commitments

- [ ] Sean Fellows (Diamond Amusement) — provide performance data for the deployed JVL machines, identify/prepare low-, mid- and premium-tier locations for JVL test deployments with historical baselines, and facilitate field visits — due unspecified — [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- [ ] JVL "Nico" (partnership follow-up owner named in the meeting summary; not matched to a known person — see note) — follow up with Sean on next steps, define multi-tier test parameters, data reporting formats/frequencies, and finalize Diamond's compensation package — due unspecified — [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- [ ] [[wiki/people/felipe-miranda.md|Felipe]] — get into Diamond's locations to collect factual win-per-unit numbers himself (Val's directive), and follow up on transactional-product technical specifications (with "Lisa," named in the summary) — due unspecified — [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]] [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]

*Note (inference): the meeting-summary auto-assigned two follow-up owners, **"Nico"** and **"Lisa,"** who do not match any known JVL person in this wiki (the only "Nico" here is a cat character on a game topper — clearly not this person). These names are recorded as they appear in the summary and left unresolved.*

## Operator briefing (2026)

A JVL operator briefing prepared for the 2026 meeting cycle profiles Diamond as a **mature, well-organized operator with over 30 years in the Georgia COAM market** and significant market influence. Leadership named in the briefing: CEO **Shawn Fellows** (the "Sean Fellows" of this page), COO **Terry Spivey**, and head warehouse technician **Terra Horton**. Shawn previously served **two terms as President of GAMOA** and remains active in industry advocacy through AMOA; Terry Spivey is also very active in Georgia industry matters, particularly through GAMOA initiatives. [[raw/georgia_operator_briefing_Diamond_Amusement.md]]

- **Scale (2026):** 1,002 decals assigned; ~200 estimated locations (briefing estimate at ~5 machines/location typical GA); a **large operator, approximately #6 statewide**. Diamond has grown through acquisitions of smaller routes, particularly **since 2024**, expanding its footprint and increasing the number of legacy JVL units under its control. [[raw/georgia_operator_briefing_Diamond_Amusement.md]]
- **Relationship:** friendly with Shawn, operational alignment with COO Terry Spivey, and active technical collaboration with head technician Terra Horton. Diamond has upgraded several cabinets to the **latest Dual SAS configuration**, and JVL worked closely with their technical team to accelerate field deployment and minimize downtime. JVL ran a **dedicated technician training session at Diamond's office on January 28, 2026** to improve field troubleshooting. [[raw/georgia_operator_briefing_Diamond_Amusement.md]]
- **Purchase history:** recent direct purchases of **18 Flex D27** and **6 Flex V43** cabinets, plus multiple **legacy JVL units controlled through route purchases** rather than direct sales. [[raw/georgia_operator_briefing_Diamond_Amusement.md]]
- **Technical / service notes:** experienced, responsive technical team; demonstrated willingness to adopt upgrades (Dual SAS conversion); good collaboration on deployment timelines; no major unresolved service escalations currently noted. Service history: an estimated **60–80 inbound service calls between 2025 and 2026** (constant call / FaceTime setup help and troubleshooting). [[raw/georgia_operator_briefing_Diamond_Amusement.md]]

The briefing reinforces the strategic read already on this page — Diamond's industry influence makes it a valuable **reference operator**, its growth via route acquisition increases JVL's indirect footprint, and continued technical engagement strengthens relationship stability. See [[wiki/projects/georgia-market-rollout.md]] and the related Georgia masters [[wiki/organizations/aks-amusement.md|AKS Amusement]] and [[wiki/organizations/inamax-ultra.md|Inamax / Ultra]]. [[raw/georgia_operator_briefing_Diamond_Amusement.md]]

*Note (reconciliation): the briefing's direct-purchase count (24 recent Flex cabinets) is distinct from — and complementary to — the ~41 total JVL units deployed at Diamond cited in the Feb-9-2026 interview/debrief, which include legacy route-acquired units.*

## Sources

- [[raw/Diamond_Shawn_Fellows_interview-February-9-2026.md]]
- [[raw/Exec_recap_Diamond_Amusement-February-9-2026.md]]
- [[raw/felipe_georgia_market_update-may-29-2025.md]]
- [[raw/georgia_operator_briefing_Diamond_Amusement.md]]
