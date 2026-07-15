---
type: decision
title: Build the self-serve dispensing tower first, magnetic-stripe-only, and rent it
date: 2025-04-16
aliases: [dispensing tower priority, payout tower decision, magnetic-stripe-only reader, dispensing tower rent model]
source-count: 1
status: active
---

# Build the self-serve dispensing tower first, magnetic-stripe-only, and rent it

In the Apr-16 one-on-one with [[wiki/people/genadi-peari.md|Genadi Peari]] ([[wiki/meetings/2025-04-16-flexpay-evolution-dispensing-tower.md]]), Val chose the next payout device to build and its hardware approach, evolving the device-catalog thinking on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## What was decided

- **Build the self-serve card-dispensing tower first, then follow up with the POS.** Time is short and JVL cannot do both at once — Val: "лучше сосредоточиться на dispensing, self-serve dispensing tower. Я вижу в этом больше применений. А потом дальше уже follow up with POS." He wants to capture the majority of the market "быстро и дешево … выпускать в больших количествах," ordering molds and dies for volume. [[raw/fkex_pay_evolution-apr-16-2025.md]]
- **Tower built on the FlexPort embedded base** — the next stage of work for [[wiki/people/evgeniy-alekseev.md|Evgeny Alekseev]] and [[wiki/people/eugine-yavorski.md|Evgeny Yavorski]]. Val's overall priority order: (1) finish the JVL business model; (2) switch to TITO architecture — build SMIB, bring FlexPort to condition, and build a **Local TITO Server**; (3) the Flex self-dispensing tower; (4) FlexPOS. [[raw/fkex_pay_evolution-apr-16-2025.md]]
- **Read magnetic stripe only — not barcode.** JVL cannot be sure cards will always carry barcodes and asked earlier to shorten the barcode without success, so the reader relies on the magnetic stripe "потому что это стандарт … Я боюсь рисковать." (The separate optical scanner for TITO tickets is resolved — the manufacturer supports the TITO barcode after a settings reprogram, and Pavel tested a black/white inversion.) [[raw/fkex_pay_evolution-apr-16-2025.md]]
- **Rent the tower, don't sell it.** The tower's cost of goods must be "очень дешевая" because the plan is to lease it, not charge for it — a recurring-revenue clearing-house model where JVL loads value onto cards and earns roughly a dollar per transaction. Val's illustrative math: "$36 million a year за тысячу установленных terminals" at $1/transaction × 100 transactions/day (recalling "Joseph's joke"). [[raw/fkex_pay_evolution-apr-16-2025.md]]
- **Deprioritize legacy non-FlexPort machines.** Machines that don't support FlexPort (a protocol issue on Alekseev's side) are not first- or second-priority: of ~35,000 machines in the market, ~17,000 have a single SAS port and perhaps ~1/5 of those (~3,000) are old and "do not fit"; with the industry moving toward TITO, Val judges these not worth chasing now. [[raw/fkex_pay_evolution-apr-16-2025.md]]

## Rationale & context

- Device targeted for **South Dakota, Nebraska and Puerto Rico**; JVL follows InComm as its technology partner (InComm is looking at Alabama and Texas), and no one loads winnings onto a MasterCard/Visa in North America without InComm. Val likes the model because it produces recurring revenue — but it demands "solid cash in the bank" to fund the clearing float. [[raw/fkex_pay_evolution-apr-16-2025.md]]
- Design intent for the tower: ~10–11 inches wide, height of a computer tower, ~500-card capacity in one width, a **7-inch screen** like the FlexPort's mounted at a slight angle in front, gray/milky plastic enclosure with no LED "choreography," loaded from the front (extractable mechanism as on FlexPay). Val rejected an LED-only signalling scheme once a controller is added, and preferred the small screen over both a bulb array and a large touchscreen. [[raw/fkex_pay_evolution-apr-16-2025.md]]

## Status

Active as of 2025-04-16 (a working direction, not yet a locked build spec). Deliverable set: [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] to draw the tower's industrial design (dimensions + standalone and between-machines views) by ~Wed/Thu; Val to prepare models for Igor by the next day; a follow-up meeting Monday. A "Sasha"/"Alex" 3D modeler who "gives little time" is referenced as doing modeling-but-not-integration — identity **unresolved / queued** (possibly distinct from the software-side [[wiki/people/alexander-biratka.md|Alexander Biratka]]; do not force the match).

## Sources

- [[raw/fkex_pay_evolution-apr-16-2025.md]]
