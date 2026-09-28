---
type: person
title: Mikhail Perelman
date: 2026-07-13
aliases: [Mikhail Perelman, Misha, Миша, Mikhail, Michael]
disambiguation: "Procurement Manager (parts/vendors/shipments; the retrofit-lead "Misha"). Misha/Michael cluster (2, owner-ruled): [[wiki/people/michael-gottlieb.md|Michael Gottlieb]]=Senior VP Game Design / [[wiki/people/mikhail-perelman.md|Mikhail Perelman]]=Procurement Manager (the "retrofit Misha"). Resolve by context; queue if none."
source-count: 11
open-commitments: 1
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

## Aug 12 2026 (in absentia) — the purchasing lag, and where an agent would fit

On the [[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug-12 Val–Genadi hardware-standard session]], Genadi gave a live example: he had told Misha that a quotation for 43-inch touch screens for the next month had come in, a week had passed and the PO approval had not been sent — "it's between chairs and there's no one to remind them". Val's picture of the fix: a purchasing agent with access to Business Central prepares all the purchase orders and Misha gets approval rights to release them. Genadi also said he had raised a missing bezel with Misha because of an upcoming show. **§15.8:** Val's personal remarks about Misha in the same passage are withheld. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Sept 4 2026 — the China route for the Flex-Slim brackets, and the 100-Flex-Port order

Two procurement threads on the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept-4 midday production call]], both routed through "Миша" — resolved to Perelman by the procurement/parts/vendor context (§4) [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]:

- **The Flex-Slim brackets and harnesses go through him to China.** [[wiki/people/genadi-peari.md|Genadi]]: "что Миша может сделать… В Китае попросить за неделю сделать и прислать самолетом. Скажем, 10 [се]тов… ну в лучшем случае 2 недели." Val took China and told Genadi to ask for a rush through him: "Я бы хотел бы, чтобы вы попросили их… [через] Миша… Они всегда идут навстречу, им только нужно сказать." Ruling: [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]].
- **He is also the one to start ordering the harnesses for 100 Flex-Ports.** Genadi had spent time the previous day pushing him and [[wiki/people/elizabeth.md|Elizabeth Palomino]] to move that order — "чтобы она пошла, посчитала, чтобы он харнес[ы] начал заказывать" — and expected "Миша должен… маленькие какието заслать [orders]" for the Flex-Port SAS harnesses too.

## Sept 14 2026 — Val names him as the man who controls the RK3576 supply

At the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept-14 12:04 PM hardware call]] Val wanted the new compute boards moved: "**Значит, нам нужно срочно нажать на поставку RK 35 76 Минск. И это кто это контролирует? Это миша контролирует. Миша перельман**" — he asks who controls it and answers himself, **by full name**, which is unusual in this corpus and removes the normal §4 ambiguity [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

[[wiki/people/genadi-peari.md|Genadi]] did not know the order's status — "**я не знаю статус… Этот инвойс… вышел[?] я не знаю**" — then read the figures off his screen: supplier rendered "**тач, интеллигент**" (Touch Intelligent, name uncertain), about **$300 plus shipment**, "**3 секси чтото**" (three sixty something) all in, being **2 samples at $150** and about **$65 freight to Minsk**. Full record on [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**A second shipment on the same call, this one to Belarus.** Asked where the arrived validator/recycler had landed, Genadi's reply is mostly garbled but carries "**миша организовывает [ship]м[е]нт в Белоруссию**" — Misha organising the shipment to Belarus. Same procurement/shipment context, resolved to Perelman the same way (§4) [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**§15.8:** clear — freight and component cost only.

## Open commitments (Sept 14 2026)

- [ ] Mikhail Perelman — push the RK3576 delivery to Minsk (2 samples, ~$300 plus ~$65 freight) — due urgently. *(Val names him as the person who controls it; the transcript does not record the instruction being given to him or accepted, and the derived notes flag the same gap.)* — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Transcript_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/Meeting_Notes_bc_material_requirements_mcp-May-11-2026.md]]
- [[raw/retrofit_january_7_2025.md]]
- [[raw/business_central_update-apr-28-2025.md]]
- [[raw/procurement_relocation-june-24-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [[raw/procurement_production_relocation-july-3-2025.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
