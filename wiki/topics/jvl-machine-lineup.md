---
type: topic
title: JVL machine and cabinet lineup
date: 2026-07-12
aliases: [Flex cabinets, Altera, Maple, Echo, Flex S, Flex C, cabinets, VLT, video lottery terminal]
source-count: 5
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

## Older machines being retrofitted (the used fleet)

- **Altera** and **Altera HH** — Altera HH carries a 30-inch monitor on top. JVL updates these to the HG6 platform (new platform, new buttons/panel, touchscreens where needed). About 88 machines. Likely destined for Puerto Rico. [[raw/retrofit_january_7_2025.md]]
- **Altera V** — has its own games; also likely bound for Puerto Rico, and expected to move quickly. [[raw/retrofit_january_7_2025.md]]
- **Maple** — the largest and most awkward group (~230 machines); comes in "Maple HH" and "Maple RT" variants. Uses the same 30-inch "Hammerhead" top monitor as Altera HH. Likely to be sent to Georgia and then on to a grey market (possibly Texas), or to Puerto Rico. [[raw/retrofit_january_7_2025.md]]
- **HG6 / HH G6** games with a bill acceptor are fitted during retrofit; standard JVL printer is used. [[raw/retrofit_january_7_2025.md]]

## Games and game families (2025 plan)

- **Fortune Fu Paws** series (also "Fortune full pause"/"future full pause"/"FuPos" in the audio transcripts) — a modular game series used to spawn market-specific variants quickly. Targeted for Class 3 Florida market, on the Omni platform, to be in the lab by June and market by September. It has heavy simultaneous on-screen action (objects, "cats," sparkles), which is what stresses the hardware. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]] [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] [[raw/fp-7_performance_analysis_january_13_2025.md]]
- HHR games, Florida Market Games, and a "Peach1234" release are named in the 2025 roadmap. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]] [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Screens, formats, and game-build terms

- **V-Deck** — a full-HD secondary screen on the machine; **Topper** — the top screen used for progressive signage. A typical layout runs videos across topper, main screen, and V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Game videos use the **VP8/VP9** format (chosen for alpha transparency). **Spine** objects are skeletal animations that run more efficiently than video; JVL balances spine animation against video to manage hardware load. **Miranda** is the tool with an "animation controller" feature that can swap objects without programmers. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## How customers see the products

- To customers and financiers, all JVL machines are described broadly as **video lottery terminals**; price and description vary only by hardware configuration (e.g. one vs. two screens) and software (number of games, features). Example naming: "video lottery terminal, Flex D27." [[raw/james_reble_elevate_january_14_2025.md]]

## Sources

- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/retrofit_january_7_2025.md]]
- [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/james_reble_elevate_january_14_2025.md]]
