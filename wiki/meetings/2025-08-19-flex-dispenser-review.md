---
type: meeting
title: Flex dispenser design review — Val & Genadi (Aug 19 2025, 4:46pm)
date: 2025-08-19
aliases: [Flex dispenser review, Flex-POS dual-screen dispenser, Flex-Port single board, dual-screen dispenser]
source-count: 1
---

# Flex dispenser design review — Val & Genadi (Aug 19 2025, 4:46pm)

**Date:** 2025-08-19 4:46pm · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]] (hardware). Russian. A hardware design one-on-one on the [[wiki/topics/flexpay-business-architecture-payout-devices.md|FlexPay payout-device]] arc — continuing the Flex-POS / Flex-Port thread. Own stub (§12 cleared: distinct Aug-19 hardware session, not the same as the 12:02pm figma meeting).

Substance and the dated place on the arc: [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Aug-19 section). In brief:
- **Flex-POS dispenser → a single dual-screen product.** Rather than stacking the existing Point-of-Sale (Point XL) on top of the dispenser (which would need **two motherboards and two internet feeds**), Genadi proposes one dispenser cabinet with **two screens** — a ~7-inch screen each for cashier and player, one motherboard driving both, a scanner at each. Val prefers this over two separate products; they iterate the screen angles, a symmetric "samovar/teapot-on-a-saddle" base that hides all interconnects, cabling routed through a central channel with four 90° exits. Screen sizing settled toward **~8 inch** ("give it room to breathe," ~17 cm width); 5-inch judged too small.
- **Flex-Port on one board.** [[wiki/people/evgeniy-alekseev.md|Alekseev]] laid out **Flex-Port on a single PCB** (enlarged ~3.5 inch) instead of the three-board assembly. Plan: Alekseev orders a **minimum sample run (~3, up to 10)** to verify, then finalize; a minimal plastic **insert/base plate** for mounting; Minsk doesn't need units (functionality unchanged). Economics discussed on the topic page (company/vendor figures only).
- Genadi to give the Flex-POS mock-up to industrial designer [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] after taking exact monitor dimensions; a follow-up booked for **Thursday**.

## Sources

- [[raw/flex_dispenser-review.md]]
