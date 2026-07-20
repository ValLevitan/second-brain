---
type: meeting
title: Flex-POS iteration review (Jul 25 2025) — transactional-architecture whiteboard
date: 2025-07-25
aliases: [Flex-POS_Iteration_Review-2025-07-25]
source-count: 1
---

# Flex-POS iteration review — July 25 2025

Friday session repurposed (per Jul 23) into a live architecture whiteboard, prepping for the Tuesday Jul-29 deep-dive. Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/juan-martinez.md|Juan Martinez]] (drawing in Visio), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]]. Purpose: draw the full set of transactional-device **topographies** (POS-only → +countertop dispenser → TITO → mini-ATM) so the engineering team can harden them.

Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Major rulings: the **"tower" concept is dead** — it split into a **countertop card-dispensing unit** and a **mini-ATM / Redemption Center**; **Flexport can fully act as a SMIB**; the **Flexpay kiosk has reached end of life** outside the e-wallet architecture. Distinct meeting from the undated ~Aug-1 weekly review.

## Sources

- [[raw/Flex-POS_Iteration_Review-2025-07-25.md]]
