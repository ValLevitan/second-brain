---
type: person
title: Genadi Peari
date: 2026-07-12
aliases: [Genadi Peari, Genadi, Gennady, Gennady Perry, Perry, Gena]
source-count: 56
---

# Genadi Peari

Genadi Peari is JVL's hardware lead. He develops the CPU boards and advises on processor choices.

## Role

- Explained the FP7 test used the "sweet spot" 6800 APU from AMD's 6000-series Ryzen (best price-to-performance, not the most powerful). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Recommended moving to the 8000-series Ryzen on the same socket for roughly 20% more performance at a modest extra cost (an estimated $20–$50 more), and said he is developing the board — available around the end of February. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Val's undertaking to Genadi: ship samples with the 8000 processor — two to Minsk and about two to Canada — noting it takes ~30 days to reach Minsk. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Named "Batang" as JVL's main hardware supplier for these boards. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## FP7 bottleneck meeting (Jan 17)

- Reported the supplier will provide the 8000-processor sample only after Chinese New Year — for now he can get a board with three video outputs; a board with four outputs (the 8000 processor) is committed for ~March 1. This updates his earlier Jan 13 "ship 8000 samples" undertaking. Tracked on [[wiki/decisions/2025-01-17-remain-on-fp7-hardware-ceiling.md]]. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- Gave the engineering view that Ryzen 9 vs Ryzen 7 offers a higher clock but the same L3 cache, so a CPU swap yields only a modest gain — reinforcing the "optimize, don't upgrade" conclusion. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Embedded group — FlexPort/FlexPay (Feb 11)

- On the Feb 11 embedded standup Genadi ("Gena") supplied the tool the engineers used to check the board, and the group was waiting on him and on chips to arrive before proceeding. See [[wiki/meetings/2025-02-11-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]

## Embedded group and market hardware (Feb 18–19)

- **Embedded group (Feb 18):** Genadi ("Gennady") reported a **iOBoard (input/output board) detection issue** — the board sometimes isn't detected on software 4.10 and, less often, on 4.09 (resembling a field symptom); cause not yet found. His printer plugs directly into the motherboard, not through the i-board. He is to mail card dispensers to [[wiki/people/eugine-yavorski.md|Evgeny]]. See [[wiki/meetings/2025-02-18-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- **Alignment (Feb 19):** Genadi is replicating a **SAS harness** from manufacturer schematics (to replace the lottery-supplied SAS adapter) and is the contact for the **Epic Edge printer sample** ("I assume Gennady has sent it") and the **SSD drive** component for the Florida CPU kits. See [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Embedded group — FlexPay ship prep (Feb 25)

- On the Feb 25 embedded standup Genadi ("Геннадий") is the one preparing the hardware **configuration** to ship (~4 machines per FlexPay; 4 FlexPay + ~15 ports); Val pressed him to have it ready by **Thursday**. After the FlexPay+second-machine test ships, Genadi is to finish the hard-to-start machine and do a **full firmware update**. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## Flex V42/C design review (Feb 27)

- On the Feb 27 cabinet review Genadi ("Gennady") is the hardware/mechanical side: he flags that the **player-tracking bracket has predefined dimensions**, so the group agreed to keep three physical pieces made to look like one continuous piece rather than redesign the bracket ("less work for Gennady"), and he works through where the wiring/speaker channels and the credit-card reader go. See [[wiki/decisions/2025-02-27-flex-street-cabinet-design-direction.md]]. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- Note: here "Gennady" is doing cabinet **hardware/brackets**, while a separate **[[wiki/people/igor-starovoytov.md|Igor Starovoytov]]** (contractor industrial designer) does the industrial-design renderings — the two are distinct on this call. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]

## Embedded group — FlexPort cabling (Mar 4, Mar 11)

- **Mar 4:** Genadi ("Гена") is the hardware side of the FlexPort test. He sent the **bill acceptor** (used in-line on the wire to credit the machine, while FlexPort reads the counters back off the machine), and flagged **cable errors** to fix — an **RX/TX swap** and a **jumper between pins 1 and 6** to wire the first counter — plus the electromagnetic **counter** wiring (two outputs on the large white connector). He was to send the schematics. [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- **Mar 11:** He is to supply the **pinout** so [[wiki/people/eugine-yavorski.md|Evgeny]] can re-solder a cable for JVL's own bill acceptors (**GCM** / "High Vision"), which use different connectors than the standard; one standard **UBA** was still en route. He also raised making the bill acceptor **non-mandatory** via a stub/emulation, and adding a protocol command to pull/ship the **log file**. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

Name confirmed by Val as **Genadi Peari**; the transcripts render it "Gennady Perry" / "Gena", kept as aliases for search.

## Puerto Rico product line (Mar 21)

- On the Mar 21 Puerto Rico product-matrix call, Genadi advised on the button panels: he offered to make the wiring/key mapping **identical** across old and new counter boards, but the team chose the software/XML route instead (his approach would need firmware changes). He also raised a cheaper board option — the **V1000 on an ARC-2000** low-power mobile platform (~**$130**, compatible but weaker) — which Val deferred. See [[wiki/topics/puerto-rico-product-configuration.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## Cabinet design, sound/power and refurbishing (Mar 27)

On a four-segment Mar 27 call with Val ([[wiki/meetings/2025-03-27-genadi-hardware-design-production-call.md]]), Genadi covered:
- **Cabinet industrial design:** he described JVL's two-pass process (general industrial design, then detailing) and agreed to have the industrial designer [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] do a **preliminary design across all three machines as one family** before detailing the curve machine; he praised mounting the **amplifier box on top of the base unit** and will prepare three variants with a per-model removable front cover. See [[wiki/decisions/2025-03-27-preliminary-industrial-design-all-three-flex-cabinets.md]]. Here Genadi owns the board/electronics; Starovoytov owns the visual/industrial design (the two are distinct). [[raw/Flex-S-design-March-27-2025.md]]
- **Sound + power redesign:** he laid out redesigning the **power distributor** (cheaper by ~40–50%, new regulators, filtration, new 5V/12V converters for higher current) and the **audio** (uprate the amplifier, reroute power, adjust gain, high-fidelity speakers, an audio engineer to run an initial test). Val approved a ~$200 component budget. Genadi is trying to free up an engineer (prefers not the "Arsenievs"; may try **Buyanov**, names unconfirmed). See [[wiki/decisions/2025-03-27-invest-in-flex-sound-and-power-redesign.md]]. [[raw/Hardware_redesign-march-27-2025.md]]
- **FlexPay kiosk production:** he argued **tooling won't fix the real constraint** (CNC throughput, painting, and screw-together assembly are the bottleneck, not shipping), that the plastics are done with little metal, and that moving parts to plastic would skip painting; he proposed buying ready-made device assemblies. See [[wiki/topics/flexpay-kiosk-production-and-tooling.md]]. [[raw/flex_pay_production-march-27-2025.md]]
- **Refurbishing:** he took the used-machine rebuild plan (Altera/Altera V plates + buttons to order, Maple mostly scrap) and undertook to write a **summary for Val and "Arkady"** and to prepare a button **layout** and order **grid** and give the programmers the key mapping. See [[wiki/projects/used-machine-retrofit-and-inventory-clearout.md]]. [[raw/refurbishing_genadi_planning-march-27-2025.md]]

## TITO/SMIB hardware support (Apr 1–7)

- **Apr 1:** the standup's "Гена/Геннадий" (hardware/office context — inference) is the supply point for [[wiki/people/eugine-yavorski.md|Yavorski]]'s SAS test rig — a printer and a replacement bill validator — and was in the office for the same-day handover/visit. [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- **Apr 2:** the SMIB meeting's action list has the **SMIB power-supply options** question directed to "Gennady" (external supply vs built-in). [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]
- **Apr 7:** "Gennady moved the barcode [scanner] on top of the bracket" for the next FlexPort hardware revision (focus distance); he has the **Flex S-adaptable FlexPort brackets** already manufactured for the Georgia demo, and is one of the people loading/shipping the Georgia terminals. [[raw/flex_pay_tito_smib_port-april7-2025.md]]

## FlexPay Evolution sessions (Apr 8–11, "Gennady" by hardware context — inference)

- In the payout-device strategy sessions ([[wiki/topics/flexpay-business-architecture-payout-devices.md]]) "Gennady" is the hardware/dispenser voice: proposed the minimal cage flow (attendant just hands the card — "хорошо, что аттендант выдал карту … больше ничего не должен делать"), was asked to research **card-dispensing unit sizes** for the tower concept (possibly smaller capacity than FlexPay's 200–300-card minimum since a cashier can refill through a back panel), and backed concentrating on the cheapest POS version. Attribution to Genadi Peari is by context (hardware lead researching dispensers), labeled inference. [[raw/flex_pay_evolution-april-8-2025.md]] [[raw/evolution_flex_pay-april-11-2025.md]]

## Apr 16 2025 — dispensing tower / POS design one-on-one

Val worked the payout-device design directly with Genadi (a Wednesday one-on-one; "I wish to have Pavel and Juan Martinez here, but … they're busy"). They scoped two devices — a cage **POS** and a self-serve **card-dispensing tower** — and Val decided to build the tower first, magnetic-stripe-only, on the FlexPort base (see [[wiki/decisions/2025-04-16-dispensing-tower-first-magnetic-stripe.md]]). Genadi is to prepare models for Igor Starovoytov's industrial-design sketch by the next day; Val floated (with unease) handing the whole tower project to others to free Genadi for the Flex-S machines. [[raw/fkex_pay_evolution-apr-16-2025.md]]

## Apr 15 & 23 2025 — SMIB weekly + the barcode-distance dispute

- **Apr 15 SMIB weekly:** Gennady is the hardware support for the embedded team — he supplies the programmer to Felipe and stands by (with Pavel/Yavorski/Alekseev) for the pre-exhibition FlexPort firmware update. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- **Apr 23 architecture meeting:** Gennady held the practical side of the **barcode-readability dispute** — he measured only **~10–12 cm** of scanner-to-ticket distance available in the cabinet bracket (10 cm suffices in his view), against Pavel's theoretical **15–20 cm** for the long central barcode; his undertaking is to verify readability on **FlexPay** after Pavel sends the reader's QR settings. He also confirmed the industrial-board preference (reject the cheap Chinese amusement board; a fanless **Tatang** board) for the standalone TITO server. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/evolution_flex_port-apr-23-2025.md]]

## May 1–2 2025 — dispensing-tower / POS design with Val

Two design calls ([[wiki/meetings/2025-05-01-flex-tower-spatial-design-review.md]], [[wiki/meetings/2025-05-02-flex-tower-pos-form-fit-design.md]]) working [[wiki/people/igor-starovoytov.md|Igor Starovoytov]]'s tower proposal. Genadi carried the hardware/mechanical side (tower width, the removable-head connector/mounting problem, dispenser sizing) and warned that a detachable-head-that-becomes-a-POS would force redesigning three Flex-S machines + the tower + a separate POS ("only come out by the end of next year"); Val resolved it by dropping the detachable head for a separate two-hood POS on unified FlexPort electronics. Genadi also handled the shop-floor logistics (preparing Evgeny [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s working station, via [[wiki/people/arkady-batson.md|Arkady]] / [[wiki/people/irina-shishko.md|Irina Shishko]]). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_tower_spacial_design_review-may-1-2025.md]] [[raw/flex_tower_pos_form_fit_design-may-2-2025.md]]

## May 6 2025 — tower hardware "make it a product"

On a hardware working call with Val ([[wiki/meetings/2025-05-06-flex-tower-hardware-design.md]]) Genadi is selecting components (power supply, filter, card reader not yet received) and the Flex speakers/acoustics, and takes the job to turn the tower into a manufacturable product (needs ~4 days). Calls: metal body/back with a plastic front door, a removable electronics head that slides in under the door, a fully symmetric shape dropping the reverse-angle undercut, backlit card slot (RGB provision added to FlexPort by [[wiki/people/evgeniy-alekseev.md|Alekseev]]), a simple pedestal + footing plate, front service, mass-production readiness. Dispensers ordered (2 Minsk / 3 Toronto, the cheaper ~450-card unit, via [[wiki/people/mikhail-perelman.md|Misha]]); Flex Curve paused; "Sasha" to help. "Speed over polish." Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_port_hardware_design_evolution-may-6-2025.md]]

## May 7 2025 — FlexPort two-machine bench + spare-unit shortage

On the FlexPort hardware call ([[wiki/meetings/2025-05-07-flexport-two-machines-tito-milestones.md]]) Genadi confirmed the floor state (four FlexPay units assembled, three in use; two slot machines checked on Georgia 1.14) and flagged that JVL has **only one spare FlexPort and needs another**; he is to arrange **temporary power** for the FlexPorts (a blank/simulation "iO board"). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_port_hardware_update-may-7-2025.md]]

## May 10 2025 — copied to protect Yavorski's workshop machines

On [[wiki/people/eugine-yavorski.md|Yavorski]]'s weekend debug update ([[wiki/meetings/2025-05-10-flexport-flexpay-debug-update.md]]) Val told Yavorski to email **[[wiki/people/arkady-batson.md|Arkady]] and Genadi (copy Val)** before going into the office over the weekend, so the machines set up for him in the workshop aren't moved or cleaned off his bench. [[raw/flex-port_flex-pay_update-may-10-2025.md]]

## May 15 2025 — tower electromechanical detailing

On a Val review of [[wiki/people/igor-starovoytov.md|Igor Starovoytov]]'s tower design ([[wiki/meetings/2025-05-15-flex-tower-hardware-design-review.md]]) Genadi took the dispensing tower into **electromechanical detailing**: surface finishes, the clear-plastic scanner-lit handle, three new sensors (door / dispenser-position / card-level), a China-sourced U-shape metal enclosure straight to molds, and a new universal FlexPort main board for [[wiki/people/evgeniy-alekseev.md|Alekseev]]. He is to hand plastics to "Sasha" and switch to **Flex Curve acoustics** (speakers + rapid model), and to design an enclosure for the **3.5-inch industrial board** (4 units to Pavel). He also owes a **red/green LED state table** for the screenless SMIB by Monday. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Flex_tower_hardware_design_review-may-15-2025.md]] [[raw/flex-pay_flex-port_update-may-15-2025.md]]

## May 20 2025 — industrial-design review; hardware items handled in absentia

- **Industrial-design call** ([[wiki/meetings/2025-05-20-flex-tower-industrial-design.md]]): the primary Val interlocutor on the FlexPort dashboard bracket and the FlexTower ([[wiki/people/igor-starovoytov.md|Igor Starovoytov]] does the CAD). Val leaned ~90% to a **Linux industrial board Genadi found** for the tower, directed dropping the credit-card swipe from the FlexPort dashboard (it moves to the tower), and set the priority order (Tower → POS → amplifier → TITO server → Flex-S → dashboard plastics). Sasha helped Genadi with the tower plastics; Genadi expects a near-orderable variant next week (awaiting samples). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/industrial_design_update-may-20-2025.md]]
- **SMIB action review (absent):** Genadi missed the same-day [[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md|SMIB action review]], but his hardware items were worked in absentia — SMIB boards (Alekseev confirmed ordered/shipped), the **20-FlexPort deployment kits** (Genadi to circulate the Bill of Material + part number), and the **iVision harness** (~May 23). [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]

## May 29 2025 — future hardware platform deferred

On the e-Wallet/TITO review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]; "Геннадий Перий") Genadi had nothing outstanding on the action list and said he is **waiting for [[wiki/people/evgeniy-alekseev.md|Alekseev]] to free up** so they can seriously discuss the next hardware platform — the **FlexTower and POS** (and whether to make updates to the massive FlexPort platform) — which Val pushed ~2 weeks out, untouched for now. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## June 18 2025 — GA-COAM redemption hardware direction

- On the [[wiki/meetings/2025-06-18-gcoam-ticket-redemption-workflow.md|June-18 ticket-redemption session]] ("Gennady") Genadi drove the hardware direction: the move from **SMTP to a cheap ARM board** (Linux + HAL), a price-sensitive **~8-inch ~3×4 monitor** for the POS (samples shipping Monday), first industrial design ~2 weeks, and simple two-shell plastics with ~30-day tooling. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]

## June 24–26 2025 — Georgia manufacturing trip + FP-7 board supply

- **Manufacturing move (Jun 24–26).** On the [[wiki/meetings/2025-06-26-procurement-manufacturing-transfer-alignment.md|manufacturing-transfer alignment]] Genadi ("Janati"/"Gennady") travels to Georgia with [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] (~2–3 weeks) to examine the new Louisville warehouse and meet an electrician, a pneumatic company and a metal fabricator, plus a couple of operator locations ("Gennady has very vague idea of what the locations are"). He (with Michael) needs **Business Central** access for JVL Systems. See [[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]. [[raw/procurement_relocation-june-24-2025.md]] [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- **FP-7 board supply for Omni (Jun 26).** On the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni grooming call]] Pavel is to talk to Genadi about **preparing new FP-7 boards** (possibly as a complete **CPU box** so nothing has to be swapped) for the Omni-on-FP-7 migration — same I/O/count boards otherwise; Val floated ordering ~10 boards for Minsk (~1-month lead). Genadi had earlier said a **new board "Dima Pikulev" worked on** is built for an "account-top board" and is **missing some interfaces** for full machine work (detail unclear, flagged). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## July 3 2025 — Georgia warehouse layout + vendor DDP quotes

On the July-3 relocation alignment ([[wiki/meetings/2025-07-03-procurement-relocation-georgia.md]]; Russian) Genadi is in the loop on both the **vendor DDP-quotation** push (Val's instruction: copy Genadi and Val on all vendor correspondence) and the **Georgia warehouse racking layout** — he provided fabricator drawings and worked through the rack count with [[wiki/people/mikhail-perelman.md|Perelman]] (11 racks along the slanted wall vs a ~21-rack perpendicular layout; 15-ft rack height, 12-ft forklift aisles). See [[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]. [[raw/procurement_production_relocation-july-3-2025.md]]

## Jul 29–31 2025 — transactional-architecture arc

In the two-session architecture deep-dive (with Val, Nathan, Juan, Pavel), Genadi worked the **redemption-center hardware** — the simplified-vs-robust Flexport debate (settled toward one Flexport because PIN entry needs a GUI/touchscreen) and the **~8-inch, front-serviced, floor-bolted / weighted-pedestal** redemption device (between-machines vs standalone; a recycler-inside-Flexpay standalone variant). Full substance: [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Transactional-Architecture-Discussion-2025-07-29.md]] [[raw/transactional_architecture-july-31-2025.md]]

## Aug 6 2025 — Flex-POS sync + Prize-Card thread

On the [[wiki/meetings/2025-08-06-flex-pos-mid-iteration-sync.md|mid-iteration sync]] Genadi backed keeping hardware requirements in GitHub (Val's preference) and moved from the review-meeting cadence into the weekly **Wednesday** review only (out of the daily working meetings). He was a participant in the same-day Prize-Card thread, confirming John's barcode point ("correct!"). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]] [[raw/Flex-Port-use_case-August-6-2025.md]]

## Aug 19 2025 — dual-screen dispenser + single-board Flex-Port design review

On a Val↔Genadi hardware one-on-one ([[wiki/meetings/2025-08-19-flex-dispenser-review.md]]; 4:46pm) Genadi proposed folding Flex-POS into **one dual-screen dispenser product** (cashier + player screens, one motherboard) instead of stacking a Point-XL on the dispenser (which needs two motherboards / two internet feeds); worked the symmetric hidden-cabling base and screen sizing (~8 inch); and reported [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s **single-board Flex-Port** (~3.5 inch, replacing the three-board assembly, ~30% cheaper), to be verified via a **~3-sample minimum run** then finalized. Genadi to take exact monitor dimensions and hand the mock-up to [[wiki/people/igor-starovoytov.md|Igor Starovoytov]]; follow-up booked Thursday. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_dispenser-review.md]]

## Sept 2025 — POS double-screen design + the one-board-vs-interface-board debate

- **Sept 3** ([[wiki/meetings/2025-09-03-flex-capabilities-weekly-ach-dispute-pos-design.md]]): presented the near-final POS industrial design — **8-inch cashier screen**, 7.5-inch device width, ~7-inch customer screen, centred dual-side scanner, top sunk magnetic-stripe reader, dispenser as a separate freestanding "dummy" product, optional floating third screen for the player. More mods promised the following Monday. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-3). [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]
- **Sept 9** ([[wiki/meetings/2025-09-09-pos-spatial-hardware-board-planning.md]], 3:18 PM, with Pavel): defended the **two-board split** (ready-made Chinese Rockchip main board + a cheap 2-layer interface board) against Val's push to consolidate onto one board — a custom processor board wouldn't be cheaper and would risk the January target. Agreed to keep the existing scheme and only ask the supplier to **swap the second monitor's HDMI-micro connector** for an industrial one. [[raw/POS_spatial_planning-september-9-2025.md]]

## Sept 22 2025 — electro-mechanical alignment one-on-one

On a Val↔Genadi one-on-one ([[wiki/meetings/2025-09-22-electro-mechanical-alignment-genadi.md]], 4:28 PM, Russian) Genadi covered the January-POS embedded hardware and warehouse logistics:
- **POS RockChip board** can't be flashed via a simple USB image (vendor needs proprietary PC softload, no source files); paths = get vendor source, find a better-supported ARM board, or engage [[wiki/people/dima-pikulev.md|Dima Pikulev]] to rebuild the Linux. Genadi backs an ARM industrial platform as the right embedded direction.
- **Core-control firmware** (Flex/Flex Top; one board replacing three) still unfinished — a bigger flash chip was added, so [[wiki/people/pavel.md|Pavel]] must re-solder one.
- Wants the **FlexPort mechanical form locked first** because "Evgeny" adjusts the board file to it ([[wiki/people/evgeniy-alekseev.md|Alekseev]] — hardware-adjacent board work on Genadi's projects, per the updated §4 ruling).
- Prepped **5 topics** for the [[wiki/people/denis-desmarais.md|Denis]] meeting; gathered old **Flex-E casino developments** (Carnival, Fortune, matrices, prototypes) for a rental-type amusement offering, reusing prior contractors/tooling — ~**5 "claims," purely electro-mechanical** (meaning of "claims" unclear in source, kept verbatim).
- **Warehouse consolidation:** add a cheap overflow warehouse near Atlanta, order proper new packaging so JVL units don't mix with Felipe's American returns; clear Canada + Georgia first and reuse freed shelving/lift; undecided on keeping the ~$7.40/sq-ft warehouse vs a taller ~$13/sq-ft one; discard anything untouched 2 years.
Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-22). [[raw/alignment_elctro-mechanical-september-22-2025.md]]

## Nov 3 2025 — machine QC checklist / release-form gap (Georgia)

On the [[wiki/meetings/2025-11-03-machine-qc-checklist-release-form.md|Nov-3 QC meeting]] (with Val + [[wiki/people/irina-shishko.md|Irina Shishko]]) Genadi diagnosed the gap behind the loose-speaker defect on the Georgia-shipped machines: sub-assembly build instructions all exist on the server, but there is **no final whole-machine checkup instruction** — and no diagnostic/loopback tool for the new **4-port (2 SAS + printer + extra)** set. He proposed reviving a **per-machine QC checklist / release form** that travels with each machine (each item signed), and undertook to (with Irina) compile the list of missing steps/documents/tools by process stage and to **travel to Georgia ~2 weeks** (late Nov / early Dec, after the ~Dec-20 release tuning) to work hands-on with [[wiki/people/elizabeth.md|Elizabeth]] on the problem sub-assemblies — crossing the border as a tourist (no laptop/tools). Substance on [[wiki/topics/slot-machine-production-test-procedure.md]] (Nov-3). [[raw/Machine Quality Control Checklist and a Release form.md]]

## Nov 11 2025 — Flex Sport tooling; worn down by the board suppliers

On the Nov-11 POS + FlexPort schedule review ([[wiki/meetings/2025-11-11-pos-flexport-schedule-review-board-update.md]]) Genadi reported **plastic ordered and tooling in progress** for the Flex Sport board, all on plan, and **metal brackets** (all cabinets) expected around **Dec 1**. In Part 2 he was visibly worn down chasing ~50 Alibaba board suppliers who won't support JVL's screens/Ubuntu/Debian (or push Android), and offered to forward Pavel all the Chinese email threads — but he backed the supplier-agnostic **application-only update** approach (build it once, adopt any Rockchip board in a couple of hours) as the way for JVL to stay "flexible." Substance on [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-11) and [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov-11). [[raw/POS_and_PORT-schedule_review.md]]

## Nov 19 2025 — digital-amplifier standalone device + POS audio design requirements

On a brief Val↔Genadi one-on-one ([[wiki/meetings/2025-11-19-genadi-audio-amplifier-standalone-pos-design-requirements.md]]; two recording segments 8:40 PM + 8:44 PM, ~7½ min total, Russian) Genadi restated that the **digital audio amplifier** must be broken out of the framework into a **standalone, hot-pluggable USB device**: today it is wired into the framework, so if it disconnects "the whole game falls" — as a standalone device the system must not crash, must return a defined error, and must re-attach on the fly. A serious cabinet needs a digital amplifier for adequate sound; ties to the move to the **Flex model's new speaker design** (3-way, no old grille). [[raw/Call_Genadi-November-19-2025-1.md]] For the POS/dispenser devices Val listed the audio components to fold into the requirements (speaker, an audio hub that can transmit, a monitor switch) and explained his design philosophy — **specify the building blocks and hand the graphics/UX to the professionals** rather than dictate it (the one constraint he imposes: place the speaker so nothing can be spilled on it). Genadi to add the feature to the design; Val recording and forwarding it. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Call_Genadi-November-19-2025-2.md]]

## Feb 12 2026 — two calls: Flex station for Texas + tooling onboarding; then ECHO printer, the Georgia freeze, Flex-Port BOM

Two same-day Val↔Genadi calls ([[wiki/meetings/2026-02-12-genadi-flex-station-flexbill-texas.md]], 4:36pm; and the callback [[wiki/meetings/2026-02-12-genadi-echo-printer-freeze-flexport-bom.md]], 5:21pm).

**Call 1 — Flex station / Texas:**
- Finished the Fujitsu-dispenser **Flex station for Texas** and is preparing drawings; the cabinet is built around a removable in-door **insert** so the same massive cabinet takes different bill devices (Fujitsu now, "belt bill"/FlexBill later). [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- Proposed assembling the **5 prototype sets in Georgia** rather than Toronto — Toronto has few components on hand, Canada-made units pay **duty**, and building in the US starts a US-fabricator relationship ("give the 5 sets to the one you'll later give 100"). Val agreed Georgia (or Florida) is the place to assemble, document and train on-site. [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- **Onboarded to the tooling with [[wiki/people/andrey-bosik.md|Andrei]]** — a GitHub repository created, **Claude Code + Claude Desktop** set up on his computer (Genadi "in shock" at the progress) — and Val pushed him to write his **JIRA tasks with [[wiki/people/pavel.md|Pavel]]** via the recorded-conversation → AI-drafts-the-tasks method. [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- Val's **FlexBill-for-Texas economics** (Texas machines today carry a printer + Fujitsu dispenser at heavy service cost; a Flex-S with scanner + one printer + FlexBill should replace it) → detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-1.md]]

**Call 2 — ECHO printer, freeze, BOM:**
- Raised **ECHO gaming with a printer**: it needs a bill acceptor that reads **barcode tickets** — Pyramid's "Platinum" acceptor does, but only over a **serial protocol JVL's gaming software doesn't support** — plus a **24 V power adapter** for the printer. Needs [[wiki/people/evgeniy-alekseev.md|Alekseev]]; Val non-committal, doubting the volume. See [[wiki/topics/echo-home-gaming-device.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Reported the **Georgia office 3-machine freeze** cleared after swapping SD cards, changing software, and on one machine removing the **PCIe SD-card adapter** (a Sapphire card runs without an adapter) — driving Val's **"never use a memory adapter" design hedge** (mount the SD as SATA). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12); implementation routed to [[wiki/people/pavel.md|Pavel]]. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- **Flex-Port BOM**: the main board is **~$45 per 100** (he'd recorded $50), of which **flash memory ≈ $15 (~half)** — flash tripled in price; to ask [[wiki/people/evgeniy-alekseev.md|Alekseev]] whether the memory amount can be cut and to price **EPROM** as the alternative (Val: EPROM's write endurance is plenty; JVL doesn't need flash speed). Left for Genadi to verify. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Flagged a **Flex-Port lighting/scanner** cosmetic defect (black spot / flickering backlight); Val wants it done properly, Genadi to experiment and dim the intensity meanwhile. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Val: before the **dispenser**, pick up the **statics** work, and **[[wiki/people/igor-starovoytov.md|Igor]] needs to be started first** ("the old wheel needs spinning up"). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]

## Feb 25 2026 — packaging in production, China shipment, POS to tooling; flagged as lagging

On a garbled Russian one-on-one with Val ([[wiki/meetings/2026-02-25-genadi-packaging-texas-flexport-market-strategy.md]], 11:01pm) Genadi reported hardware progress and was pressed to catch up with Pavel:

- **Packaging prototype now in production.** Genadi built the machine's **shipping-box packaging** (foam inserts holding the packed machine on all sides; monitors kept vertical, not screen-down; a shock absorber added because plain foam doesn't cushion) and it is "находится в продакшн." A sample was already made and brought to the office. He had rejected an alternative packaging from an industrial engineer Val calls "Andrei"; Val delegates packaging to Genadi but urges him to **work closely with Andrei** rather than override him. (Andrei — described by Val as an industrial engineer — is distinct from Genadi's usual industrial designer [[wiki/people/igor-starovoytov.md|Igor Starovoytov]] and from the registered Andrei/Andrey/Andrew people; no page, identity unresolved.) [[raw/Call_Genadi_Peari-February-25-2026.md]]
- **Fujitsu dispenser drawings → China.** He wired up the Fujitsu cash dispenser in the office and passed **updated drawings with the corrected bezel** to [[wiki/people/mikhail-perelman.md|Misha (Mikhail Perelman)]], but Misha stalled ~2 weeks finding a US fabricator; the call's resolution was to **ship the parts to China (Hangzhou) for reference pricing and air-freight them back** — **23 sets** went out that day. [[raw/Call_Genadi_Peari-February-25-2026.md]]
- **Flex Sport panel + POS.** Sent the **Flex Sport** panel back to be fully textured and to fix several wrong-sized bosses, after which the proof lighting reads even. Switched to finishing the **POS** drawings (transcribed "пёс"/"PES") to hand to **press-mold tooling**; reported that [[wiki/people/pavel.md|Pavel]]'s POS unit powered up with **both monitors working** (GUI/touchscreen still to do). [[raw/Call_Genadi_Peari-February-25-2026.md]]
- **Flagged as the one lagging.** Val told Genadi he is "the only one who's behind our plans" (Val had left him alone, "a vacuum," to work) and will book a meeting with Pavel so the two work the **two joint projects — POS and FlexPay — actively together**; Genadi noted the cash dispenser and POS are already in Jira with Pavel, and FlexPay-for-Texas needs a bit more work. Substance and Val's Texas market strategy on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-25). [[raw/Call_Genadi_Peari-February-25-2026.md]]

## Feb 26 2026 — Flex-dispenser hardware planning (two calls with Val + Pavel)

On the two same-day planning calls ([[wiki/meetings/2026-02-26-tasks-planning-alignment.md]] 2:35pm, [[wiki/meetings/2026-02-26-jira-planning-flex-dispenser.md]] 3:18pm) Genadi carried the hardware side of carving the Fujitsu-dispenser Flex device into JIRA:

- Walked his backlog status — **Flex Sport (IP 578)** sent for 2 more manufacturer iterations (samples ~2 weeks, effectively done); **IP 1014 Flex Cash Dispenser** BOM/Fujitsu-design closed with hardware development + [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s prototype in progress; will order an initial **15-unit "run"** (harness first). [[raw/tasks_planning_alignment-February-26-2026.md]]
- Opened the 3:18pm call with the core problem — **"Fujitsu doesn't accept cash, we need bill acceptors"** — and worked through adding a **bill acceptor + recycler** to FlexPay, warning it makes the unit roughly FlexPay's own width; agreed to Val's plan to **narrow the vertical FlexPay from ~2 ft to ~1 ft** in two stages (drop the recycler into the existing enclosure first, proper industrial design — vertical monitor, added height — second). He needs **two new tasks** (mechanical **redesign** + **BOM**) for the Fujitsu form, plus prototypes, harness and detailed BOM material (may copy tasks 371/372 or build fresh). Substance and the open commitment on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-26). [[raw/JIRA_Planning-February-26-2026.md]]

## Mar 11 2026 — the "Flex Recycler Slim" between-machines kiosk

On a garbled Russian one-on-one with Val ([[wiki/meetings/2026-03-11-flex-recycler-slim.md]], 08:31pm) Genadi worked the design of a new **slim payout kiosk (the "Flex Recycler Slim")** meant to stand between machines:

- He confirmed the current **black-and-white plastic prototypes** (one white, two black) assembled well and are strong enough — though he had to correct/improve a lot — and that a **properly-textured** plastic will look markedly better than the visibly built-up texture on the samples; new tooling forms take realistically **~7–8 weeks**. He has started the drawings, will finish laying everything out and **send to a pricing vendor** (transcribed "Quaternion"), and expects a first batch of ~**10 units**. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- On the design he proposed **~11 inches** wide, agreed the head must be no wider than the pedestal, and defended his stabiliser **foot** (needed so a standalone unit doesn't tip) while accepting Val's demand to keep it narrow enough to fit between machines. He noted JVL's **perimeter lighting** (one running-LED line, single driver, as on FlexPay) already exists and can be reused, and that electronics can hide inside with a serviceable door. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- **Board debate:** Genadi wanted to **reuse JVL's own board** (it has all the functionality + lighting) rather than start a new design with [[wiki/people/evgeniy-alekseev.md|Alekseev]], arguing its cost is mostly **memory** this product doesn't need (roughly halving the price); Val pushed for something **simpler/cheaper** and left it to a features discussion. He noted an **ARM + cheap-chip** path costs less than the FlexPort memory alone. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- **Undertakings:** finish the current tooling release (~1–2 days) then push the recycler slim; add a **scanner**; and **send Val the render** so Val can compose the feature list. Full device substance and Val's cheap-BOM/recurring-revenue economics on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Mar-11). §15.8 clear. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]

## Sources

- [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- [[raw/tasks_planning_alignment-February-26-2026.md]]
- [[raw/JIRA_Planning-February-26-2026.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- [[raw/Call_Genadi_Peari-February-25-2026.md]]
- [[raw/Call_Genadi-November-19-2025-1.md]]
- [[raw/Call_Genadi-November-19-2025-2.md]]
- [[raw/POS_and_PORT-schedule_review.md]]
- [[raw/Machine Quality Control Checklist and a Release form.md]]
- [[raw/alignment_elctro-mechanical-september-22-2025.md]]
- [[raw/flex_dispenser-review.md]]
- [[raw/Flex Capabilities Weekly Update-september-3-2025.md]]
- [[raw/POS_spatial_planning-september-9-2025.md]]
- [[raw/2025-08-06_Flex-POS-Mid-Iteration-Sync.md]]
- [[raw/Flex-Port-use_case-August-6-2025.md]]
- [[raw/Transactional-Architecture-Discussion-2025-07-29.md]]
- [[raw/transactional_architecture-july-31-2025.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/procurement_relocation-june-24-2025.md]]
- [[raw/Alignment_procurement_manufacturing_transfer-june-26-2025.md]]
- [[raw/procurement_production_relocation-july-3-2025.md]]
- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/product_matrix_puerto_rico-march21-2025.md]]
- [[raw/requirements_puerto_rico-march-21-2025.md]]
- [[raw/Flex-S-design-March-27-2025.md]]
- [[raw/Hardware_redesign-march-27-2025.md]]
- [[raw/flex_pay_production-march-27-2025.md]]
- [[raw/refurbishing_genadi_planning-march-27-2025.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]
- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [[raw/flex_pay_evolution-april-8-2025.md]]
- [[raw/evolution_flex_pay-april-11-2025.md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/evolution_flex_port-apr-23-2025.md]]
- [[raw/flex_tower_spacial_design_review-may-1-2025.md]]
- [[raw/flex_tower_pos_form_fit_design-may-2-2025.md]]
- [[raw/flex_port_hardware_design_evolution-may-6-2025.md]]
- [[raw/flex_port_hardware_update-may-7-2025.md]]
- [[raw/flex-port_flex-pay_update-may-10-2025.md]]
- [[raw/Flex_tower_hardware_design_review-may-15-2025.md]]
- [[raw/flex-pay_flex-port_update-may-15-2025.md]]
- [[raw/industrial_design_update-may-20-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
- [[raw/about_tickets_redemption-gcoam-june-18–2025.md]]
