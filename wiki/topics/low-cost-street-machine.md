---
type: topic
title: Low-cost street machine (sub-$2,000 street cabinet program)
date: 2026-06-09
aliases: [street machine, street cabinet, low-cost street machine, low-cost street cabinet, street slot machine, sub-$2000 street machine, RK3588 street machine, stripped street cabinet]
source-count: 3
---

# Low-cost street machine (sub-$2,000 street cabinet program)

A durable, multi-meeting JVL hardware program (June 2026) to build a stripped-down, very cheap "street" slot machine — a self-contained single-screen cabinet — aimed at **price-sensitive markets like Texas where JVL's Flex cabinet is too expensive to sell** and where street prices have dropped a lot. The guiding rule Val set is: **strip the cabinet, do not cheapen the games** — the machine loses hardware, not picture quality. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]] [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]

The thread runs across the [[wiki/meetings/2026-06-08-low-cost-street-machine-design.md|June-8 design opener]] (cost levers + business model), a [[wiki/meetings/2026-06-09-low-cost-street-cabinet-platform.md|June-9 cabinet-platform feasibility read]] (the compute board), and a [[wiki/meetings/2026-06-09-street-machine-industrial-design.md|June-9 industrial-design walkthrough]] (the cabinet itself); a June-16 design-direction session follows. The cabinet aesthetic/design direction is also carried on [[wiki/decisions/2025-02-27-flex-street-cabinet-design-direction.md]], and the sell-cheap-plus-recurring-fee business model on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## The build target and economics

- **Whole device under $2,000, including the bill acceptor.** Val counts the bill acceptor at ~$800, so the machine itself must land around **$1,200**. Cost is cut in many small places because "it adds up." [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- **Cut components, not visuals.** Savings come from removing hardware, not from downgrading the picture. Switching the bill acceptor saves about **$600**; dropping the amplifier, light board, light controller, counters board and VDEC off the current Flex saves roughly **$500–600 in parts**; the bare metal cabinet is only ~$300, so little is left to save there. Parts prices are rising (the compute board doubled, memory up ~4×). [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]] [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Not a low-quality product.** Games keep normal resolution and color; Val explicitly rejected dropping to the animation-only level of Biratko's online games. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Business model.** Sell the machine cheap (~$5–6k, rough) and earn a **recurring connection fee** (~$3/day, or ~10%); the recurring remote services are what make selling cheap machines a viable business (details on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]). [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]

## The compute platform (RK3568 → RK3588)

Because the topper and video board are dropped, the machine can move **off x86 to a cheaper ARM board** — NOVA already runs on ARM, so it is not tied to x86. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]

- **Step up from RK3568 to RK3588.** The team has Rockchip **RK3568** boards but only at **2 GB RAM**, which is too little. Pavel and Genadi favor the **RK3588** — about twice the cores, 4× video decode, handles 8K — for only **~$10 more**; the **RK3576** is an in-between option. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Memory sizing is the main open question.** Each game is ~**500–700 MB** and must load fully into RAM to switch quickly (that is why Flex uses 16 GB). Capping the machine at **~6 games** — which fits the planned subscription/ELT model — means **4 GB might work**, but 6–8 GB gives headroom, especially with progressives. Decision: **order 8 GB sample boards, measure real use, then size down** rather than guessing. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Order proper samples from China, standardize on one maker.** Val rejected buying an **Orange Pi 5** (RK3588, 16 GB) locally in Minsk; he wants **two sample boards ordered from a more reliable / cost-effective manufacturer in China**, and that manufacturer standardized on for support across all products. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Test path — port Calle Ocho.** Port **Calle Ocho** (the only game currently on NOVA) to the RK board, strip the topper and video-decoder components, run it, then load **5–6 copies at once** to measure memory use and performance. This can start now on the existing RK3568 boards while the RK3588 samples are ordered. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Rising board price.** The RK3568 supplier now wants **$100** (up from $50 in December), driven by memory cost. [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]

## The cabinet / industrial design

- **Single-screen, vertical 43" HD display** with a good black level; **no topper and no static top** — the whole design must be self-contained on the one screen. The **touchscreen covers the full screen** (not half), because skill features sit at the top and need to be touchable. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **Screen built into the cabinet** — a shallow panel, glass over a single metal cover/channel — not hung outside like Flex. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **Monolithic sheet-metal body** (cheapest), not split into a face plus extra parts; a cast/molded face would need a mold. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **A single door** with the bill acceptor and cassette (nightstand-style, no separate front access in the strip-to-the-bone framing). [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]] [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Placement in formations.** Machines set up in clean shapes — a straight line, back-to-back, triangle or square; backs need handles and wheels for moving; floors will not be level (these are not casinos) so the legs need a big adjustment range, levelable **from the top** without reaching underneath. Player seating is unresolved. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **Peripherals.** Leaning to a **TITO ticket printer** (cheapest), hidden in the door/bezel to keep the machine slim, with paper pre-sized for the US region; the bill validator must also support TITO/rating tickets (JCM has options, model TBD). Genadi proposed a **back-load payload bill validator** that drops down and opens together with the front-service door — Val agreed and said "make it a provision." **About 8 buttons**, one large spin button, with the panel flipping from the back for easy button swaps. (The June-9 platform meeting had pushed a harder strip of **≤2 buttons** as the extreme target; the industrial-design meeting settled the fuller cabinet on ~8.) [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]] [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- **Lights.** Val's lean is **one perimeter light line** — proven, industry-standard, not expensive, "won't cut $10 to make it worse"; Genadi pushed two vertical strips or reusing the Flex light assembly, and a halo light shows poorly in bright street locations. Not fully locked. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **Audio.** No amplifier and no subwoofer — use the Rockchip board's built-in **3 W/channel amp** with two small fixed front-facing speakers (~$20 saved). [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
- **Self-built bill-path "nose"/bezel with an integrated QR-code reader** (the June-8 idea) replaces the $35 plastic nose plus the complex player-tracking port and its screen. [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]

## Service and recurring revenue as the core

Val stressed repeatedly that **service is the core of the business**. Front service access is mandatory, and every peripheral — bill validator, printer, buttons, screen — must have **two-way feedback**, so operators can see status remotely (is the screen working, is a button dead), push software updates over the air, and pull service and accounting data. Without those recurring services, selling cheap machines alone is a hard business; the feedback hooks are what make the services sellable. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]

## Shared progressive

Because street machines stand close together in a bank, link them through a **cloud "progressive" control** into a shared jackpot/bonus displayed across the row of screens — half-screen, third-screen, or the whole row for a big bonus, like a scoreboard. Val considers this a strong feature. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]] [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]

## Scope note and next steps

The passive **Flex** machine keeps being built in parallel; the street machine is a **different principle**, not a replacement. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]] Next step: Val writes everything up as an **industrial-design brief** (framed as a design task, not a spec) and sends it to Genadi with the meeting recording; Genadi briefs the contractor industrial designer [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] in person for rough, radical hand-drawn concepts and a preliminary 3D model (~3 variants) — Igor is slow, so start now. Val will re-confirm the bill-validator choice with Juan and recover the lost candidate list. [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]

*§15.8: device/BOM/build-cost economics only (the sub-$2,000 build target is product economics); no named-person compensation recorded.*

## Sources

- [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Industrial_Design-June-9-2026.md]]
