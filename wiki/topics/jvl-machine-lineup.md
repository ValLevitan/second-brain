---
type: topic
title: JVL machine and cabinet lineup
date: 2026-07-12
aliases: [Flex cabinets, Altera, Maple, Echo, Flex S, Flex C, cabinets, VLT, video lottery terminal, Flex SD27, V43, C10-VLOT-TERM-RU, Epic 950, FutureLogic, FlexPort]
source-count: 9
---

# JVL machine and cabinet lineup

A running glossary of the machine models, cabinet types, and product families that come up across JVL's planning, retrofit, and shipping discussions. Plain descriptions only; details are as stated in the transcripts.

## New / planned cabinets (2025 Jira roadmap)

- **Casino cabinets** — a planned initiative to build casino-type cabinets to match current market needs: dual-screen, vertical, and possibly a curved or "J-shape" monitor. Products noted include "FutureFLEX CD33" and "V49." [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex S ("Flex Upright Street")** — a simpler, more economy cabinet family; products under it include Flex S V43 and Flex S D27. Known internally as "Street," but likely just "S" to customers. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] JVL's goal is to keep Flex-S for street operation (it is currently also used for casino operation) and develop the stronger Flex-C for casinos. The FP7 CPU board is the hardware being evaluated for Flex-S. See [[wiki/topics/fp7-hardware-platform.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- **Flex C** — a planned stronger, more robust casino cabinet with a larger screen; big enough that JVL may treat signage/progressive as a separate element. Distinct from the earlier "Flex C43 Curve" game-design item below. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- **Flex Top** — a new countertop cabinet with a dual screen, roughly 24-inch; temporary plastic exists and one sample is assembled, but permanent tooling not yet ordered. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex Flat** (renamed from "Flex Pay") — a small flat 15-degree-angle 16-inch plastic top piece that sits on the Flex Pay pedestal. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Echo** — a countertop model being converted back to a gaming cabinet, fitted with HG6 games for conversion in Colombia. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex C43 Curve** — a curved cabinet tied to game design work ("Georgia Co-op Jack Patrasche"). [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Payment / distribution products

- **Payment Platform** initiative: the payment **kiosk** itself; **Port**, the lighter version of the AFT; and **Pay Cloud**, what the kiosk will "morph into." Plus a **Payment Mobile Admin** application under discussion. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex Mount** and a **CPU Kit** sit under accessories; the rest is online distribution. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **FlexPort** — a payment device that communicates with **FlexPay** and can push updates; on Jan 24 its beta was ~3 weeks out (~Feb 15 2025), to be tested with a Flex-S machine and a FlexPay kiosk assembled together. Ticket (TITO) validation is done by FlexPay: the machine reads the ticket code and passes it to FlexPay, which confirms it printed it. See [[wiki/meetings/2025-01-24-flexport-flexpay-beta.md]]. [[raw/flex_port_hardware_up-jan-24-2025.md]]

## Printers

- **Transact Epic 950** — the #1 printer used in the South Dakota market; JVL decided to support it. See [[wiki/decisions/2025-01-22-support-epic-950-printer-for-south-dakota.md]]. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **FutureLogic** printers — JVL's software was written for the **Gen 2**; on the Gen 5 a "void after business day" ticket-printing issue appeared that is said to be already fixed and committed, to ship in the next ISO. The market's #2 printer family is referred to as "Paycheck" / FutureLogic. Operators can choose Epic 950 or FutureLogic in the machine menu. [[raw/sd_vlt_recap-jan-22-2025.md]]

## Older machines being retrofitted (the used fleet)

- **Altera** and **Altera HH** — Altera HH carries a 30-inch monitor on top. JVL updates these to the HG6 platform (new platform, new buttons/panel, touchscreens where needed). About 88 machines. Likely destined for Puerto Rico. [[raw/retrofit_january_7_2025.md]]
- **Altera V** — has its own games; also likely bound for Puerto Rico, and expected to move quickly. [[raw/retrofit_january_7_2025.md]]
- **Maple** — the largest and most awkward group (~230 machines); comes in "Maple HH" and "Maple RT" variants. Uses the same 30-inch "Hammerhead" top monitor as Altera HH. Likely to be sent to Georgia and then on to a grey market (possibly Texas), or to Puerto Rico. [[raw/retrofit_january_7_2025.md]]
- **HG6 / HH G6** games with a bill acceptor are fitted during retrofit; standard JVL printer is used. [[raw/retrofit_january_7_2025.md]]

## Games and game families (2025 plan)

- **Fortune Fu Paws** series (also "Fortune full pause"/"future full pause"/"FuPos" in the audio transcripts) — a modular game series used to spawn market-specific variants quickly. Targeted for Class 3 Florida market, on the Omni platform, to be in the lab by June and market by September. It has heavy simultaneous on-screen action (objects, "cats," sparkles), which is what stresses the hardware. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]] [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] [[raw/fp-7_performance_analysis_january_13_2025.md]]
- HHR games, Florida Market Games, and a "Peach1234" release are named in the 2025 roadmap. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]] [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Games in production (Jan 16 design review):** [[raw/game_design_january_16_2025.md]]
  - **Rodeo** ("Rodeo Clean") — a country-music-themed slot; the free-spins music was praised as an "earworm," with expanding wilds and a girl/flag/horseshoe animation. Composed with an outside music partner.
  - **Crescent City Carnival** — Val and Juan agreed to give the woman character "nondescript ethnicity" (Cuban/Puerto Rican/exotic) so games reflect the diverse Florida market.
  - **Roger Green** — a game looking "really good," reviewed alongside Crescent City Carnival.
  - **Fortune Football** — the next big game to move the whole team onto; needs a new dashboard, new system-framework messages, a gambling feature and a "local" (fractional-bet) feature; production being planned as a block diagram of milestones in the new Omni workflow.
  - **The "fat cat" / mannequin-cat persistence game** — a perceived-persistence game whose core hook is inflating a cat across ~10 states; the design must tune how much the cat inflates per hit (Goldilocks: noticeable but leaving runway) and the ratio of false hits to real hits (e.g. ~9 false to 1 real). Math is easy to change but animation states must not paint the design into a corner. **Progressive-in-game gambling** is wanted eventually in this framework but deferred to save time. [[raw/game_design_january_16_2025.md]]
  - **Coin Trio** — referenced as a competitor/reference game whose bonus-coin distribution JVL is interpolating from. [[raw/game_design_january_16_2025.md]]

## Screens, formats, and game-build terms

- **V-Deck** — a full-HD secondary screen on the machine; **Topper** — the top screen used for progressive signage. A typical layout runs videos across topper, main screen, and V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Game videos use the **VP8/VP9** format (chosen for alpha transparency). **Spine** objects are skeletal animations that run more efficiently than video; JVL balances spine animation against video to manage hardware load. **Miranda** is the tool with an "animation controller" feature that can swap objects without programmers. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## How customers see the products

- To customers and financiers, all JVL machines are described broadly as **video lottery terminals**; price and description vary only by hardware configuration (e.g. one vs. two screens) and software (number of games, features). Example naming: "video lottery terminal, Flex D27." [[raw/james_reble_elevate_january_14_2025.md]]
- **Item numbers / older quote:** A May 11, 2022 quote used item number **"C10-VLOT-TERM-RU"** — a video lottery terminal with **one monitor** and a different (simpler) software set. The current **Flex-S** machines have **two monitors** and more/more-complex games (hence higher price); **"Flex SD27" is itself the item number** for that model, and **V43** is another. Val confirmed C10-VLOT-TERM-RU is a *different* hardware+software combination, not the same as Flex-S. [[raw/elevate_convo_w_scott_rambeau_january_15_2025.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/retrofit_january_7_2025.md]]
- [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/james_reble_elevate_january_14_2025.md]]
- [[raw/elevate_convo_w_scott_rambeau_january_15_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/sd_vlt_recap-jan-22-2025.md]]
- [[raw/flex_port_hardware_up-jan-24-2025.md]]
