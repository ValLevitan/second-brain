---
type: person
title: Mikhail Perelman
date: 2026-07-13
aliases: [Mikhail Perelman, Misha, Миша, Mikhail, Michael]
disambiguation: "Procurement Manager (parts/vendors/shipments; the retrofit-lead "Misha"). Misha/Michael cluster (2, owner-ruled): [[wiki/people/michael-gottlieb.md|Michael Gottlieb]]=Senior VP Game Design / [[wiki/people/mikhail-perelman.md|Mikhail Perelman]]=Procurement Manager (the "retrofit Misha"). Resolve by context; queue if none."
source-count: 7
---

# Mikhail Perelman

Mikhail Perelman ("Misha") is JVL's **Procurement Manager** (owner-confirmed 2026-07-13). On the used-machine retrofit he owns the parts side — deciding what to order and sourcing it. Owner ruling: the "Misha" who leads the retrofit is this person (the retrofit-lead mentions are attributed to him), and he is **distinct** from [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] (Senior VP of Game Design); resolve by context — procurement/parts → Perelman, game design → Gottlieb.

## Role

- Worked through the retrofit plan with Val — what parts to order and how to rebuild each machine type. [[raw/retrofit_january_7_2025.md]]
- Tracks practical parts-sourcing problems, e.g. 30-inch monitors for the Maple cabinets and whether they can be bought reliably from China/Alibaba. [[raw/retrofit_january_7_2025.md]]
- Reported that a former supplier ("Angus"/"Akira") can no longer supply those large monitors. [[raw/retrofit_january_7_2025.md]]

The transcript is in Russian; his name appears as "Миша."

## Apr 28 2025 — purchasing bill-of-material; HS tracking

On the BC status call ([[wiki/meetings/2025-04-28-business-central-labs-tariffs-status.md]]) Val wants **Michael (Perelman) focused only on purchasing bill-of-material** items (with [[wiki/people/mary.md|Mary]] handling non-BOM POs like GLI). Lev believed **Michael had been tracking HS numbers / country-of-origin** for imports — now the pressing task to formalize on the vendor card. See [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/business_central_update-apr-28-2025.md]]

## June 24–26 2025 — procurement lead on the manufacturing move to Georgia

On the manufacturing-relocation sessions ([[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]) Perelman ("Misha"/"Michael") owns the procurement/logistics side of moving assembly from Canada to the new Louisville, Georgia warehouse. His tasks: find **subcontractors** for the warehouse electrical + pneumatic wiring; source an **electric pump truck**; travel to Georgia with [[wiki/people/genadi-peari.md|Genadi Peari]] (~2–3 weeks) to examine the warehouse and meet an electrician, a pneumatic company, a **metal fabricator**, and a couple of operator locations; push all supplier **quotations to DDP (Delivered Duty Paid) into the US** and begin placing destination-Atlanta orders (~30 days out); and obtain competitive quotes from **American manufacturers**. He needs **Business Central** access for JVL Systems (with Gennady) and confirmed there are ~**100 sets of Flex** whose components ship to Georgia. He agreed a trip "makes sense." [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]

## July 3 2025 — relocation execution status (vendors + Georgia warehouse layout)

On the July-3 alignment review ([[wiki/meetings/2025-07-03-procurement-relocation-georgia.md]]; Russian) Perelman reported progress a week after the June-24/26 decision, with Val pressing that "nothing has moved." His sourcing status: he had a **list of four US metal fabricators** to contact Monday (using Gena's drawings); monitor quotes from the California distributor **bySearch** (~7-year supplier — no clean quote yet) and **Alpha** (21.5"/27" — showing ~$70/monitor tariff, ~70–90% of the ~$95–100 unit cost, under DDP), with the **43"** still unquoted; upcoming meetings with **StarTech** (a Chinese LCD manufacturer with an England facility, Jul 10) and **General Touch** (touch screens, Jul 7); **power supplies** bought through a US distributor (MeanWell/Sagir); **PC/CPU boards** stocked through September with two China sources (**Nika** + a cheaper newer one). On the warehouse he mapped racking options (11 racks along the slanted wall / ~44 skids vs a perpendicular ~21-rack layout, 15-ft height, 12-ft forklift aisles). Val's direction: get a **used-racking company** to lay it out from a drawing, and — the recurring frustration — **copy Val and Genadi on all vendor correspondence** and send **everyone a DDP-quotation request**. See [[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]] and [[wiki/topics/tariffs-and-customs-compliance.md]]. [[raw/procurement_production_relocation-july-3-2025.md]]

## May 11 2026 — material-requirements report to be delivered via the BC MCP

On a [[wiki/people/val-levitan.md|Val]] / Perelman / [[wiki/people/lev-rudky.md|Lev Rudky]] call ([[wiki/meetings/2026-05-11-bc-material-requirements-mcp.md]]) Misha, as procurement manager, spelled out the material-requirements (MRP) report he wants — the one-click Navision report Anatoly built him, which the standard Business Central report does not reproduce. His model: input a part/subassembly/machine with a target quantity; get a **consolidated shortage list** (one row per unique part, netting stock + on-order + in-transit) enriched with **vendor + last price + minimum order quantity**, grouped by vendor for POs, plus a per-subassembly side-list for cross-checking. Today he builds the consolidation himself in an **Excel pivot table** on top of the BC export. Val proposed delivering it not by modifying BC but through the **BC MCP layer** (Claude doing the consolidation/enrichment in one step), and made Misha the canonical **"procurement manager" persona** for the requirements Val will draft from the transcript + Misha's example Excel. Misha to send the Excel sample immediately. Substance on [[wiki/topics/business-central-erp-implementation.md]] (May-11). §15.8 clear. [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]] [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]

## Sources

- [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/retrofit_january_7_2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/procurement_relocation-june-24-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [[raw/procurement_production_relocation-july-3-2025.md]]
