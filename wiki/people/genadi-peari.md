---
type: person
title: Genadi Peari
date: 2026-07-12
aliases: [Genadi Peari, Genadi, Gennady, Gennady Perry, Perry, Gena]
source-count: 43
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

## Sources

- [[raw/flex_dispenser-review.md]]
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
