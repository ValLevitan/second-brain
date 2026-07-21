---
type: meeting
title: POS spatial/hardware planning — one-board vs interface-board debate (Sept 9 2025)
date: 2025-09-09
aliases: [POS spatial planning, POS spatial planning Sept 9, one-board vs interface-board, HDMI connector debate]
source-count: 1
---

# POS spatial/hardware planning — one-board vs interface-board debate (Sept 9 2025)

**Date:** 2025-09-09 (3:18 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]] (references [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] and a "Sergei"). Russian. Val leaves partway (another meeting); Genadi + Pavel continue.

A Flex-POS physical-layout and PCB-partitioning session continuing the [[wiki/meetings/2025-08-19-flex-dispenser-review.md|Aug-19 hardware review]] on the [[wiki/topics/flexpay-business-architecture-payout-devices.md|FlexPay payout-device arc]]. Genadi walked the initial block scheme of the whole product (from his talk with Alekseev): a **~800×608 cashier screen**, a smaller/lower-resolution customer screen, a centred scanner readable from both sides, a top magnetic-stripe reader, the motherboard mounted **vertically in the top section**, and a **main interface board** below multiplexing all external connections into one harness. **Val pushed for a single consolidated board** (as achieved on Flex-Port) so the unit assembles fast, mounts like a "sandwich" behind the screen, and keeps connectors up off the tabletop (spill/water/vibration failures are what cost JVL money — "our money is in assembly and development, not in buying the board"). **Genadi and Pavel defended the two-board split** (the ready-made cheap Chinese Rockchip main board + a cheaper 2-layer interface board), arguing a custom processor board wouldn't be cheaper, would delay the January target, and likely wouldn't work first try; a custom board is a **future** exercise, not now.

Substance and the dated arc entry: [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-9 section). In brief:
- **Decision: keep the existing (ready-board + interface-board) scheme** for the Jan-1 product; improve it later. Genadi to ask the China supplier only to **swap the second monitor's HDMI connector for a more industrial one** (a shielded/latching type; the current HDMI-micro connector is the one weak point). Touchscreens to connect via **USB** (standard, transparent to software).
- **Cabling** routed from underneath through a widened base for easy hand access; card-reader **status LED** to be driven from the interface board (lit only when awaiting a card); the reader's built-in beeper kept; a monochrome embossed **JVL** logo on the reader slot instead of a separate lit part.
- Pavel floated **LVDS daisy-chain / dual-mode** to drive both monitors off one connector (depends on the Rockchip supporting dual mode) — an Alekseev question. A **meeting with Alekseev booked for the next day**.

Two distinct Sept-9 sessions were held: this 3:18 PM hardware/spatial one and the 2:41 PM [[wiki/meetings/2025-09-09-top-level-backend-architecture.md|top-level back-end architecture]] session — separate stubs.

## Sources

- [[raw/POS_spatial_planning-september-9-2025.md]]
