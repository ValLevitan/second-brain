---
type: decision
title: Flex V42/C street-machine cabinet design direction
date: 2025-02-27
aliases: [Flex V42, Flex V42/C, carbon fiber panel, floating monitor, street machine cabinet, credit card reader requirement]
source-count: 3
status: active
---

# Flex V42/C street-machine cabinet design direction

Design direction Val gave the industrial designer ([[wiki/people/igor-starovoytov.md|Igor Starovoytov]]) and hardware lead ([[wiki/people/genadi-peari.md|Gennady]]) on the Feb 27 2025 Flex V42/C review for the evolved **street-machine** cabinet (with a curved monitor). Treated as a decision because Val closed with "you've collected our comments now" and set the team to continue on this direction; several points are firm directives, one is a formal requirement. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]

## The direction

- **Remove the chrome.** Val's core complaint: the segmented chrome trim (around the player-tracking area and the bill acceptor/printer) "ages the machine" and looks like 1980s design; replacing it makes the machine "look younger." Chrome to be replaced with black chrome / brushed / darker finish, or a translucent material that lets the bill-acceptor and printer light bleed through. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **One continuous upper surface with a carbon-fiber weave.** The fragmented upper panel (currently three visible pieces — player-tracking plus left/right speakers) becomes a single continuous surface in the **carbon-fiber "weave" texture** already used on the machine; the decorative "dots" are dropped as an aging factor. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **Hidden speakers.** Speakers are relocated under the bottom edge of the monitor (down-firing, bouncing off the deck); the front left/right speakers become redundant. They may be hidden behind the continuous carbon-fiber surface with small non-visible sound exits. Rationale: [[wiki/people/felipe-miranda.md|Felipe]] confirmed operators are **disconnecting the speakers**, and in Georgia / South Dakota (convenience stores, bars, restaurants) locations don't want the machine loud, so in-your-face sound isn't necessary for a street machine. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **Keep the player-tracking bracket dimensions.** The bracket has predefined dimensions; rather than redesign it to a wider single opening, keep the three physical pieces (center + left + right) but make them **look like one continuous piece** — less work for Gennady and no new player-tracking documentation. A Flexport/tracking system is still needed even in Georgia (which has no AFT). [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **Floating curved monitor off the bottom edge**, supported by a triangular piece; the supporting/back piece should be **aluminum / stainless / brushed** (not black), so the curve stays visible and doesn't read like a flat home monitor. Light effects from the variable-thickness treatment to be added. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- **Add a full-insert credit-card reader (formal requirement).** Val: "please put on a full insert credit card reader" and confirmed "put it as a requirement." Location: **inside the door** for now. It is a **USB device**; [[wiki/people/pavel.md|Pavel]] already has a sample; it needs a **software** upgrade (not firmware) to drive it. Readers must be ordered. The four machines already prepared to ship can go **without** the reader for now. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]

## Scope note

This is an **evolutionary** change to the street machine (Flex S) that comes with the curved monitor — not a redesign of how the panels sit on the machine, and mainstream/existing configurations are left as they are. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]

**Later evolution (Mar 27):** Val broadened the approach — before detailing the curve machine, do a **preliminary industrial design across all three Flex machines as one family**, with monitor-angle and light-fixture changes and an amplifier box mounted on the base unit. See [[wiki/decisions/2025-03-27-preliminary-industrial-design-all-three-flex-cabinets.md]]. [[raw/Flex-S-design-March-27-2025.md]]

## Jun 8 2026 — the low-cost "street" machine: build the whole device under $2,000

A ~30-minute (mostly Russian) call ([[wiki/meetings/2026-06-08-low-cost-street-machine-design.md|Low-Cost Street Machine Design]], 9:48pm ET; [[wiki/people/val-levitan.md|Val]], [[wiki/people/genadi-peari.md|Genadi Peari]]) opened a **new, cost-driven** street-machine direction — distinct from the Flex V42/C aesthetic evolution above — because street prices have dropped a lot. This starts the June street-machine hardware thread (June-9 / June-16 follow-ups). The sell-cheap-plus-recurring-fee business model and device economics are also carried on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jun-8). [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]

- **The target: a whole device for under $2,000, including the bill acceptor.** Val counts the bill acceptor at ~$800, so the machine itself must come in around **$1,200**. (Decision.) [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- **Strip the cabinet.** **One door only** (bill acceptor + cassette), a **single 43-inch monitor** (either a bare touchscreen on the monitor, or a plain 43" monitor plus a small ~15" VDEC touchscreen — Genadi thinks the small-screen option, ~$45, is cheaper), no stand, no open/close light fixtures — flat and simple, "as cheap as an iPhone." Cut cost in many small places because "it adds up." (Decision.) [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- **Move the main board to a Rockchip platform and drop boards.** Genadi's rough costing: starting from the current **Flex** machine, moving to **Rockchip** and dropping the amplifier, light board, light controller, counters board and VDEC saves roughly **$500–600 in parts** before the cabinet. The metal cabinet itself is only ~$300, so little to save there; parts prices are rising (Rockchip doubled, memory up 4×). (Genadi's costing, endorsed by Val.) [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- **Self-built bill-path "nose"/bezel with an integrated QR-code reader** — Val's main new idea, replacing the $35 plastic nose *and* the complex player-tracking port and its screen, with either a small info screen or lit tactile buttons. Genadi liked the QR-in-the-nose idea ("brilliant") but is cautious about fitting it into other makers' cabinets where the bill acceptor sometimes sits too low; he'll work it out and check. (Val's direction; Genadi to develop.) [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
- **Open items (not resolved):** whether to include a ticket printer; a compliance catch — cutting the non-volatile memory down to "records only" (dropping game-state storage) saves money but runs into **jurisdictional compliance**, flagged not resolved; whether modern projected-capacitive touchscreens hide the ITO grid line (decides if a bare touchscreen looks clean); and whether the integrated nose fits other makers' cabinets. Next step: Val meets **Piratka** (a nickname) and Pavel (likely [[wiki/people/pavel.md|Pavel Frolov]]) the next morning (June 9, 8:00) to get their read on feasibility. §15.8: device/program cost economics only (the sub-$2,000 build target is product economics); no named-person compensation. [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]

## Sources

- [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- [[raw/Flex-S-design-March-27-2025.md]]
- [[raw/Meeting_Notes_Low_Cost_Street_Machine_Design-June-8-2026.md]]
