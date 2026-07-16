---
type: decision
title: Build a standalone "server in a box" (TITO + Incom API + JVL accounting host)
date: 2025-04-24
aliases: [server in a box, TITO server box, standalone server, Cisco-looking server, local server, JVL accounting host, Incom API server]
source-count: 1
status: active
---

# Build a standalone "server in a box" (TITO + Incom API + JVL accounting host)

Val's "final verdict" on the Apr-24 2025 FlexPay evolution call ([[wiki/meetings/2025-04-24-flexpay-server-dispenser-pos-evolution.md]]). Part of the FlexPay evolution arc — see [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## What was decided

- JVL will offer a **free-standing server as its own box** (not integrated into FlexPay), so a location can be handed a turnkey TITO/POS solution ("here's a little box, this is our TITO server… they will gravitate to our solution"). Val's rationale: attack the market hard for a "virtual monopoly." [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]
- Hardware: a **Linux-based industrial board** sourced by [[wiki/people/genadi-peari.md|Gennady]] — **3.5" × 5", fanless, ~$120–130**, ~10-year longevity; "like our v1000 board, just low performance." Mounted **outside** the machine like a router (its own desktop/router power supply), connected **over Ethernet** — "the server cannot be hardwired in any way to FlexPay." [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]
- The box runs **three server applications**: the **JVL accounting host**, the **Incom API**, and the **TITO server**. Enclosure styled to look like a **Cisco server** — deliberately oversized/"tough-looking," not showing off how small the board is. [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]
- **FlexPay stays on the machine CPU**; the server is a separate second physical product. In this configuration FlexPay just needs to support a **slave mode of operation** (Pavel's only, minor concern). [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]

## Execution

- Gennady to order server-board samples: **4 to JVL Toronto, 2 to JVL Minsk** (one each earmarked for [[wiki/people/evgeniy-alekseev.md|Alekseev]] and [[wiki/people/eugine-yavorski.md|Yavorski]], who are "very good with Linux"). [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]

## Status

Active as of 2025-04-24. The follow-up ran across **May 1–2** as tower/POS industrial-design reviews with Genadi (see [[wiki/topics/flexpay-business-architecture-payout-devices.md]]); the server-in-a-box verdict itself was not revisited there.

## Sources

- [[raw/evolution_flex-pay_pos_server-apr-24-2025.md]]
