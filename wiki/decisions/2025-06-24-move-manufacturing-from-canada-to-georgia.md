---
type: decision
title: Move JVL manufacturing/assembly from Canada to Georgia (Atlanta/Louisville)
date: 2025-06-24
aliases: [manufacturing relocation, Atlanta manufacturing, Georgia assembly, Louisville warehouse, DDP quotes, metal fabricator, Canadian manufacturing wind-down]
status: active
open-commitments: 4
---

# Move JVL manufacturing/assembly from Canada to Georgia (Atlanta/Louisville)

JVL will **stop manufacturing/assembling machines in Canada and move it to Georgia** (the Atlanta area). Recorded as a firm direction across two June-2025 sessions — a Jun-24 dictation of undertakings by [[wiki/people/val-levitan.md|Val]] and a Jun-26 alignment meeting where Val stated "we see **absolutely no way of manufacturing in Canada**" and confirmed the plan with [[wiki/people/mikhail-perelman.md|Mikhail Perelman]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/lev-rudky.md|Lev Rudky]]. This **resolves the previously-open "where does manufacturing land, Canada vs Georgia" question** that had held the [[wiki/topics/business-central-erp-implementation.md|Business Central]] Labs rollout on ice since April. [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## Why (Jun 26)

- **Tariff / financial risk.** Val: manufacturing in Canada "leaves us open to a lot of financial risks and uncertainties" — **tariff-related**. JVL already has a US company and is already expanding in the US market. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **Nothing ties JVL to Canada.** From a marketing perspective "there is nothing holding us to Canada whatsoever," and the **SR&ED / media tax credit** has "absolutely zero influence" from where manufacturing physically sits. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **Keep the Canadian entity alive for tax losses.** Val's caveat (Jun 24): check with the accountant to keep **JVL Canada in working order** so the accumulated **tax losses** there can still be written off. [[raw/procurement_relocation-june-24-2025.md]]

## What was decided

- **People.** [[wiki/people/elizabeth.md|Elizabeth]] heads manufacturing in Georgia (warehousing, inventory control, work scheduling) — confirmed with [[wiki/people/felipe-miranda.md|Felipe]] as "the right person," an engineer, "a different level" than [[wiki/people/arkady-batson.md|Arkadi]]. [[wiki/people/anibal.md|Anibal]] moves from Peru to Georgia (via [[wiki/people/mary.md|Mary]]) to be the **dedicated Echo/amusement-countertop assembler** (Val's "Porsche one-team" model — a dedicated line, not mass production). **Logistics (incoming + outgoing) stays with Mary.** [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]] [[raw/procurement_relocation-june-24-2025.md]]
- **The move sequence.** First move all **Echo/amusement** to Georgia; before that, prepare a stock of ~**50 machines in Toronto** to buy time while Georgia production is set up, then truck the rest. A container of parts already inbound, **plus additional parts for ~100 Flex sets**, ships to Georgia as a second stage (~**30 days** to load and ship Flex + Echo components). [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **Toronto keeps the refurbishing.** The Toronto shelving stays; **Maple and Altera** units are loaded there for **refurbishing**, then shipped to **Texas or Nebraska** (see [[wiki/projects/used-machine-retrofit-and-inventory-clearout.md]]). [[raw/procurement_relocation-june-24-2025.md]]
- **The Georgia site.** JVL moved from a ~**3,000 sq ft** unit in **Norcross** to a **10,500 sq ft freestanding building in Louisville** (as transcribed; a suburb of Atlanta — "like Richmond Hill and the market"). The lease **can be converted into a purchase** (Val checked with the lawyers). Echo + Flex stock moves from **Scarborough** to Louisville. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **Warehouse fit-out.** [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] + [[wiki/people/genadi-peari.md|Genadi Peari]] travel to Georgia to examine the warehouse and meet an **electrician**, a **pneumatic/air-distribution** contractor, and a **metal fabricator**; drop air + electrical lines from the ceiling, install shelving along the structural walls, and source an **electric pump truck** (not a forklift). [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **Procurement → DDP + US suppliers.** All supplier quotations move to **DDP (Delivered Duty Paid)** into the US (raises bill-of-material cost but removes immediate tariff uncertainty); step two is obtaining **competitive quotes from American manufacturers** to bring the BOM back under control. A first-priority task: **find a metal fabricator in America**. [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **ERP (Business Central) consequence.** Manufacturing runs on the existing **[[wiki/organizations/jvl-systems.md|JVL Systems]] Business Central** with **no manufacturing module** — assembly from **purchase-level components** (a podium that is a purchased item from Canada becomes an **assembled item** in Georgia). [[wiki/people/mikhail-perelman.md|Michael]] + [[wiki/people/genadi-peari.md|Gennady]] need BC access; the **Bill of Material moves from Navision ("the Vision") into Business Central**. [[wiki/people/lev-rudky.md|Lev]] estimated the config a **"medium"/~3-week–1-month** job (GL/chart of accounts first, then general posting setup); **JVL Labs stays on Navision/"the Vision"** for now (its BC conversion remains on ice). Detail on [[wiki/topics/business-central-erp-implementation.md]]. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## Dated timeline (§3 sequencer)

- **Jun 24 2025** — Val dictates the undertakings (Elizabeth heads manufacturing; Anibal → Atlanta for Echo; 50-machine Toronto buffer; DDP quotes; move BOM to BC; find a US metal fabricator; keep JVL Canada alive for tax losses). [[raw/procurement_relocation-june-24-2025.md]]
- **Jun 26 2025** — alignment meeting confirms it ("no way of manufacturing in Canada"), adds the Norcross→Louisville warehouse move, the lease-to-purchase option, the no-manufacturing-module BC path (Lev), and the Georgia trip agenda. [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## Open commitments

- [ ] Mikhail Perelman + Genadi Peari — travel to Georgia; examine the Louisville warehouse; meet an electrician, a pneumatic company, a metal fabricator, and visit a couple of operator locations — due ~2–3 weeks — [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [ ] Mikhail Perelman — push suppliers to quote **DDP into the US** and begin placing destination-Atlanta orders (~30 days out); find a US metal fabricator — due ~30 days — [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [ ] Lev Rudky — configure Business Central (JVL Systems) for Georgia assembly (no manufacturing module): redefine purchase items as assembly/BOM items, port the BOM from Navision, GL/chart of accounts then general posting setup — ~3 weeks/1 month — [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [ ] Val — confirm with the accountant that JVL Canada stays in working order to preserve the Canadian tax losses — due unspecified — [[raw/procurement_relocation-june-24-2025.md]]

## Sources

- [[raw/procurement_relocation-june-24-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
