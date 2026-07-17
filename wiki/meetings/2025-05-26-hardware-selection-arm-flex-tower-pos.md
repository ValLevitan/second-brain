---
type: meeting
title: Hardware selection for Flex Tower / Flex POS — ARM-Linux board found (May 26 2025)
date: 2025-05-26
source-count: 1
---

# Hardware selection for Flex Tower / Flex POS — ARM-Linux board found (May 26 2025)

A Russian-language hardware call with [[wiki/people/val-levitan.md|Val]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]] ([[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] referenced, not present). The §3 continuation of the [[wiki/meetings/2025-05-21-tech-stack-flex-pos-tower-tito.md|May-21 tech-stack call]].

A weekend investigation turned up a **cheap ARM-based embedded-Linux board (Rockchip RK-series, ~$60)** that resolves the embedded-STM-vs-industrial-Linux dilemma left open on May 20/21 — Linux flexibility at nearly the STM price. Val ruled it the chosen direction for **Flex Tower, Flex POS and the standalone server**, pending Alekseev building the LVDS display interface and sample validation. The decision-grade content is on [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]]; the design-thread context is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## Sources

- [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
