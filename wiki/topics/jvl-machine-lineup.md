---
type: topic
title: JVL machine and cabinet lineup
date: 2026-07-12
aliases: [Flex cabinets, Altera, Maple, Echo, Flex S, Flex C, cabinets, VLT, video lottery terminal, Flex SD27, V43, C10-VLOT-TERM-RU, Epic 950, FutureLogic, FlexPort, FlexPay, Nico, Miranda, Omni, Florida Ruta, CPU kit, coffin, iOBoard, Bally iview, Diamondlink, nano-optics, JCM, dual SAS, HAL]
source-count: 16
---

# JVL machine and cabinet lineup

A running glossary of the machine models, cabinet types, and product families that come up across JVL's planning, retrofit, and shipping discussions. Plain descriptions only; details are as stated in the transcripts.

## New / planned cabinets (2025 Jira roadmap)

- **Casino cabinets** — a planned initiative to build casino-type cabinets to match current market needs: dual-screen, vertical, and possibly a curved or "J-shape" monitor. Products noted include "FutureFLEX CD33" and "V49." [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex S ("Flex Upright Street")** — a simpler, more economy cabinet family; products under it include Flex S V43 and Flex S D27. Known internally as "Street," but likely just "S" to customers. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] JVL's goal is to keep Flex-S for street operation (it is currently also used for casino operation) and develop the stronger Flex-C for casinos. The FP7 CPU board is the hardware being evaluated for Flex-S. See [[wiki/topics/fp7-hardware-platform.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- **Flex C** — a planned stronger, more robust casino cabinet with a larger screen; big enough that JVL may treat signage/progressive as a separate element. Distinct from the earlier "Flex C43 Curve" game-design item below. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- **Flex Top** — a new countertop cabinet with a dual screen, roughly 24-inch; temporary plastic exists and one sample is assembled, but permanent tooling not yet ordered. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex Flat** (renamed from "Flex Pay") — a small flat 15-degree-angle 16-inch plastic top piece that sits on the Flex Pay pedestal. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Echo** — a countertop model being converted back to a gaming cabinet, fitted with HG6 games for conversion in Colombia. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]] Separately, an **ECHO consumer home device** (149 offline games, sold on Amazon) is the online team's go-to-market product — whether it is the same product line as this Echo cabinet is **unclear**. See [[wiki/topics/echo-home-gaming-device.md]]. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Flex C43 Curve** — a curved cabinet tied to game design work ("Georgia Co-op Jack Patrasche"). [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Payment / distribution products

- **Payment Platform** initiative: the payment **kiosk** itself; **Port**, the lighter version of the AFT; and **Pay Cloud**, what the kiosk will "morph into." Plus a **Payment Mobile Admin** application under discussion. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **Flex Mount** and a **CPU Kit** sit under accessories; the rest is online distribution. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- **FlexPort** — a payment device (a hardware **EFT / electronic-fund-transfer module installed on the machine**) that communicates with **FlexPay** and can push updates; on Jan 24 its beta was ~3 weeks out (~Feb 15 2025), to be tested with a Flex-S machine and a FlexPay kiosk assembled together. Ticket (TITO) validation is done by FlexPay: the machine reads the ticket code and passes it to FlexPay, which confirms it printed it. See [[wiki/meetings/2025-01-24-flexport-flexpay-beta.md]]. [[raw/flex_port_hardware_up-jan-24-2025.md]]
  - **FlexPort ↔ FlexPay integration (Feb 11):** the FlexPort module connects to the FlexPay kiosk over a **WebSocket** (handshake → device registration). Agreed logic: the machine **accepts no money or tickets until the device registers** with FlexPay; cash-out is only via FlexPay (the old RS-485/Mutagus path is fully disabled when FlexPort is installed); a bad ticket or 3 wrong PIN attempts sends the player to an administrator, with a ~15-minute ticket lockout to be added FlexPay-side. A test-utility showed a WebSocket 200 instead of the expected 101 upgrade — to be retested against a real FlexPay kiosk. Production shipment likely needs ~1 more week after FlexPay comes up. The payment processor **Incom** supplies the test server; a production contract was received and awaits Val's signature; [[wiki/people/felipe-miranda.md|Felipe]] ("Filippo") to host a multi-machine production test in his office. See [[wiki/meetings/2025-02-11-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]

## Printers

- **Transact Epic 950** — the #1 printer used in the South Dakota market; JVL decided to support it. See [[wiki/decisions/2025-01-22-support-epic-950-printer-for-south-dakota.md]]. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **FutureLogic** printers — JVL's software was written for the **Gen 2**; on the Gen 5 a "void after business day" ticket-printing issue appeared that is said to be already fixed and committed, to ship in the next ISO. The market's #2 printer family is referred to as "Paycheck" / FutureLogic. Operators can choose Epic 950 or FutureLogic in the machine menu. [[raw/sd_vlt_recap-jan-22-2025.md]]
- **Printer library taxonomy (Feb 19):** each printer is driven by a **hardware-abstraction-layer (HAL) library** on JVL's side (Pavel corrected Val: "firmware" sits on the printer, not on the machine). Two comms types: **Gen 2 / Gen 5** (made by **JCM**, "future logic") **and nano-optics** share one communication language; **Epic** (Transact) uses a different one — so two libraries. The **Epic 950** is JVL's first supported model; **Epic Edge** may follow. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## SAS ports and the "coffin" (Feb 19)

- The **CPU box** is called the **"coffin"** internally (Russian "гроб"/grob). Georgia machines have **dual SAS** (two DB9 serial connectors, primary + secondary; primary controlled by the Georgia Lottery). To drive a pay-kiosk printer, JVL adds a **third dedicated printer port** — a new DB9 connector (a **harness**, jumpered inside the coffin) with the printer HAL library. All three are interchangeable RS-232/DB9 serial ports logically, but the printer port is meant to always run as the printer so operators don't misassign SAS ports. See [[wiki/projects/georgia-market-rollout.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Bally iview** is the casino accounting/reporting system the Georgia machines report to; a Feb 19 finding: JVL sends correct data but Bally's final report doesn't match (cause unknown). The Georgia test/cert lab is **Eclipse**. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Cabinet monitor configs and the Florida Ruta CPU kits (Feb 19)

- **Echo vs Altera monitors:** the **Echo** cabinet is a **single-monitor** machine (selecting it disables the DSAP/progressive top display — no space to show it on the old software); **Altera** is a **dual-monitor** cabinet (pay table or progressive on the top screen). Selecting one monitor on an Altera works until a reboot, after which the progressive display is lost — an open single-monitor persistence bug to reproduce. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Florida Ruta CPU kits:** a JVL **CPU kit** installed inside a customer's own (often single-screen, minimal-button, touchscreen) cabinet for the Florida **amusement** market (max ~5 machines/location, similar to Georgia; ~80% of that market is single-screen). Termed **"Florida Ruta"** — needs **no GLI/lab approval** (Puerto Rico, using the same HitGames-6 software, does). Config differences by jurisdiction (denominations, "display most recent tilts," stacker-door check) live in per-locality XMLs; **show mode** and **stacker-door** default to unchecked for production. Machines are moving from an **SD card** to an **SSD drive** for faster boot. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **iOBoard (input/output board):** a Feb 18 embedded-group issue — the board is sometimes not detected on software **4.10** (and, less often, **4.09**), resembling a field symptom; cause not yet found. Some printers plug directly into the motherboard rather than through the i-board. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- **Progressive Controller:** an initial-setup screen picks the progressive controller available on the network; an **embedded progressive controller** runs inside a single machine (the approach used for the Florida "JPRE" market), so it works even where a location has one machine. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

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
  - **"Nico" cat game (Feb 6 review):** a game with a **"Nico" cat** character reviewed as still-image mockups (Lena presenting) — idle-with-meters, an attraction mode with promo text and character animation, and an on-machine view. Open feedback items for Juan: the topper **promotional text** (draft: "hold and re-spin feature with up to three bonuses") and the low-camera-angle, "huge and majestic" Nico-cat **topper** image. (Transcript otherwise blank.) [[raw/Game design meeting - February 6, 2025.md]]

## Screens, formats, and game-build terms

- **V-Deck** — a full-HD secondary screen on the machine; **Topper** — the top screen used for progressive signage. A typical layout runs videos across topper, main screen, and V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Game videos use the **VP8/VP9** format (chosen for alpha transparency). **Spine** objects are skeletal animations that run more efficiently than video; JVL balances spine animation against video to manage hardware load. **Miranda** is the tool/software product with an "animation controller" feature that can swap objects without programmers. [[raw/fp-7_performance_analysis_january_13_2025.md]] Miranda is a versioned JVL software product (versions "V8"/"Miranda 8", V9); its source is being migrated from SVN/Bitbucket into GitHub as part of the first migration batch (with Omni and FlexPay). See [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]] [[raw/github_explained-feb-3-2025.md]]

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
- [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- [[raw/github_explained-feb-3-2025.md]]
- [[raw/Game design meeting - February 6, 2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
