---
type: person
title: Genadi Peari
date: 2026-07-12
aliases: [Genadi Peari, Genadi, Gennady, Gennady Perry, Perry, Gena, Геннадий, Kenadi]
source-count: 98
open-commitments: 32
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

## Jan 8 2026 — introduced to Pyramid Technologies; the printer CAD file to go to him

On the [[wiki/meetings/2026-01-08-pyramid-technologies-printer-integration-intro.md|Jan-8 Pyramid intro call]] Val introduced "Gennady" to Pyramid as JVL's director of the electromechanical department, located in Toronto, and asked that Pyramid's mechanical CAD file of the printer be sent to him for hardware integration, so JVL need not hand-measure it. See [[wiki/organizations/pyramid-technologies.md]]. [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]] *(§15.8: a joking remark about his relocation is not recorded.)*

## Feb 12 2026 — two calls: Flex station for Texas + tooling onboarding; then ECHO printer, the Georgia freeze, Flex-Port BOM

Two same-day Val↔Genadi calls ([[wiki/meetings/2026-02-12-genadi-flex-station-flexbill-texas.md]], 4:36pm; and the callback [[wiki/meetings/2026-02-12-genadi-echo-printer-freeze-flexport-bom.md]], 5:21pm).

**Call 1 — Flex station / Texas:**
- Finished the Fujitsu-dispenser **Flex station for Texas** and is preparing drawings; the cabinet is built around a removable in-door **insert** so the same massive cabinet takes different bill devices (Fujitsu now, "belt bill"/FlexBill later). [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- Proposed assembling the **5 prototype sets in Georgia** rather than Toronto — Toronto has few components on hand, Canada-made units pay **duty**, and building in the US starts a US-fabricator relationship ("give the 5 sets to the one you'll later give 100"). Val agreed Georgia (or Florida) is the place to assemble, document and train on-site. [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- **Onboarded to the tooling with [[wiki/people/andrey-bosik.md|Andrei]]** — a GitHub repository created, **Claude Code + Claude Desktop** set up on his computer (Genadi "in shock" at the progress) — and Val pushed him to write his **JIRA tasks with [[wiki/people/pavel.md|Pavel]]** via the recorded-conversation → AI-drafts-the-tasks method. [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- Val's **FlexBill-for-Texas economics** (Texas machines today carry a printer + Fujitsu dispenser at heavy service cost; a Flex-S with scanner + one printer + FlexBill should replace it) → detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-1.md]]

**Call 2 — ECHO printer, freeze, BOM:**
- Raised **ECHO gaming with a printer**: it needs a bill acceptor that reads **barcode tickets** — Pyramid's "Platinum" acceptor does, but only over a **serial protocol JVL's gaming software doesn't support** — plus a **24 V power adapter** for the printer. Needs [[wiki/people/evgeniy-alekseev.md|Alekseev]]; Val non-committal, doubting the volume. See [[wiki/topics/echo-home-gaming-device.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Reported the **Georgia office 3-machine freeze** cleared after swapping SD cards, changing software, and on one machine removing the **PCIe SD-card adapter** (a Sapphire card runs without an adapter) — driving Val's **"never use a memory adapter" design hedge** (mount the SD as SATA). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12); implementation routed to [[wiki/people/pavel.md|Pavel]]. This is an early datapoint in the dedicated [[wiki/topics/egm-freezing-investigation.md]] (Genadi drove the Mar-9 meeting and the Mar-20 FP10-manufacturer email). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- **Flex-Port BOM**: the main board is **~$45 per 100** (he'd recorded $50), of which **flash memory ≈ $15 (~half)** — flash tripled in price; to ask [[wiki/people/evgeniy-alekseev.md|Alekseev]] whether the memory amount can be cut and to price **EPROM** as the alternative (Val: EPROM's write endurance is plenty; JVL doesn't need flash speed). Left for Genadi to verify. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Flagged a **Flex-Port lighting/scanner** cosmetic defect (black spot / flickering backlight); Val wants it done properly, Genadi to experiment and dim the intensity meanwhile. [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- Val: before the **dispenser**, pick up the **statics** work, and **[[wiki/people/igor-starovoytov.md|Igor]] needs to be started first** ("the old wheel needs spinning up"). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]

## Feb 23 2026 — the Crane CPI recycler consultation

Genadi joined Val and Juan on the [[wiki/meetings/2026-02-23-crane-cpi-bnr-vs-scr-recyclers.md|Feb-23 call]] with [[wiki/organizations/crane-cpi.md|Crane CPI]]. The transcript labels him only "Speaker 5"; he is identified by context (Val greets "Gennady"; Juan asks "the S C R Gennady right?"). [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]

- He asked how the BNR loader capacity and the recyclers fit together, what "not marketed for gaming" means for GLI, and how the SCR's four drums are configured. [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- His comparison: using two SCRs "is very similar to having one BNR… In terms of capacity" and price; the smaller unit is "exactly a width of the bill acceptor". He closed on the SCR: "We are more flexible and better reliability." [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- He asked for "the command list and every all the software package firmware" so JVL can integrate. Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-23). [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]

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

## Mar 4 2026 — FlexPort IP-578 Q&A (written)

A **written question→answer exchange** with [[wiki/people/val-levitan.md|Val]] (not a meeting or recorded call): Val sent prepared follow-up questions across the transactional-hardware backlog and Genadi answered each in writing. Genadi's answers: the **2nd-iteration Flex Sport/FlexPort samples (IP-578)** were requested but the manufacturer ("Hesheng", as written) had not returned from holidays, so no reply yet (no issues expected); the **FlexPOS tooling drawings (IP-955)** are not submitted, deferred until after the Texas Pay-Station prototype production (Cash Dispenser + Recycler) is released; the **Flex Cash Dispenser prototype order (IP-1014)** was placed, expected **March 20**; a **Hangzhou quotation** for the Vertical Pay Station came back, but reviewing **HFM-400 with Val and Pavel** forced a requirements change — **HFM-400** (Fujitsu variant) reworked wider to take a **bill acceptor + ticket printer**, and a new **HFM-401** created for a **Cash Recycler SCR from MEI**, with EM drawings for both due that week; [[wiki/people/mikhail-perelman.md|Misha]] is awaiting a **GA manufacturer** quote (none yet); the **HM-400 BOM** was **created in BC**; POS physical integration was discussed with [[wiki/people/pavel.md|Pavel]] (minor wiring left, no work needed from Genadi — Pavel has functional prototypes and owns the system/GUI finish); and Genadi asked for a short meeting with Val to scope the **vertical FlexPay** (phase-2) requirements. Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Mar-4). §15.8 clear (BOM/hardware only). [[raw/Genadi_Review_draft_questions_FlexPort_IP-578-March-4-2026.md]] [[raw/Genadi_reply_to_Val_questions_FlexPort_IP-578-March-4-2026.md]]

## Mar 11 2026 — the "Flex Recycler Slim" between-machines kiosk

On a garbled Russian one-on-one with Val ([[wiki/meetings/2026-03-11-flex-recycler-slim.md]], 08:31pm) Genadi worked the design of a new **slim payout kiosk (the "Flex Recycler Slim")** meant to stand between machines:

- He confirmed the current **black-and-white plastic prototypes** (one white, two black) assembled well and are strong enough — though he had to correct/improve a lot — and that a **properly-textured** plastic will look markedly better than the visibly built-up texture on the samples; new tooling forms take realistically **~7–8 weeks**. He has started the drawings, will finish laying everything out and **send to a pricing vendor** (transcribed "Quaternion"), and expects a first batch of ~**10 units**. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- On the design he proposed **~11 inches** wide, agreed the head must be no wider than the pedestal, and defended his stabiliser **foot** (needed so a standalone unit doesn't tip) while accepting Val's demand to keep it narrow enough to fit between machines. He noted JVL's **perimeter lighting** (one running-LED line, single driver, as on FlexPay) already exists and can be reused, and that electronics can hide inside with a serviceable door. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- **Board debate:** Genadi wanted to **reuse JVL's own board** (it has all the functionality + lighting) rather than start a new design with [[wiki/people/evgeniy-alekseev.md|Alekseev]], arguing its cost is mostly **memory** this product doesn't need (roughly halving the price); Val pushed for something **simpler/cheaper** and left it to a features discussion. He noted an **ARM + cheap-chip** path costs less than the FlexPort memory alone. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]
- **Undertakings:** finish the current tooling release (~1–2 days) then push the recycler slim; add a **scanner**; and **send Val the render** so Val can compose the feature list. Full device substance and Val's cheap-BOM/recurring-revenue economics on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Mar-11). §15.8 clear. [[raw/Flex-Recyler-Slim-Meeting-March-11-2026.md]]

## Mar 20 2026 — SR&ED project list (hardware R&D)

On the [[wiki/meetings/2026-03-20-sred-progress-review.md|Mar-20 SR&ED progress review]] (Russian; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/efim-podvoiski.md|Efim]], [[wiki/people/lena.md|Lena]]) Genadi represented the **hardware** R&D for JVL's 2025 SR&ED claim. He said he **already had his project list compiled** and did not need the maximum spread "because I don't have many people to attach" to it, and flagged a couple of thin-2025 items — a platform effort and some year-end **RockChip-chip** activity — as **better deferred to the 2026 claim** where the real work falls. *(Attribution of labour/hours to projects; no pay figures — §15.8 clear.)* See [[wiki/topics/sred-tax-credit.md]] (Mar-20). [[raw/SREDs_progress_review-March-20-2026.md]]

## Mar 30 2026 — OMNI board-to-board USB link (Full Speed on purpose)

On a very short (~1m24s), heavily garbled call with Val ([[wiki/meetings/2026-03-30-genadi-omni-board-communication.md]], header 9:51pm) Val asked about the board-to-board communication link [[wiki/people/dima-pikulev.md|Dima Pikulev]] built in the OMNI hardware stack. Genadi confirmed they **intentionally fitted a USB Full Speed chip rather than a USB High Speed one** for the iBoard-to-mainboard link, because the higher speed wasn't needed for the use case, and there is an **option to increase the bandwidth later** if required. (The transcript is too garbled to reliably reconstruct exact figures or the precise board/component names — Full Speed vs High Speed USB are the standard 12 Mbit/s vs ~480 Mbit/s tiers.) This is the hardware side of the **iBoard high-speed memory-chip / state-persistence** concern [[wiki/people/alexander-biratka.md|Biratka]] raised earlier the same day about a peripheral-abstraction protocol layer — see [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-30). §15.8 clear. [[raw/Meeting_Transcript_Genadi_OMNI_Board_Communication-March-30-2026.md]] [[raw/Meeting_Notes_OMNI_Board_Communication_Genadi-March-30-2026.md]]

## Apr 20 2026 — schedule review: HFM backlog + dispenser-vs-recycler strategy

On the [[wiki/meetings/2026-04-20-genadi-schedule-review-alignment.md|Apr-20 schedule review]] (1h 7m; with Val) Genadi ran the active hardware backlog — HFM 507 tooling (samples ≥4 weeks), HFM 514 Georgia critical parts, HFM 504 fifth-country BOM (to walk with [[wiki/people/mikhail-perelman.md|Mikhail Perelman]]), HFM 519 sample plan, the **FDM-not-SLA** decision for the HFM 511 Minsk rapid prototype, and the Flex PAY IP 1014 sample verification (Pavel took it on because [[wiki/people/evgeniy-alekseev.md|Alekseev]] can't). Midway it became a strategic debate — dispenser vs. recycler+FlexSport bundling, distributor pricing, the Pyramid-dongle integration constraint, and Val leaning toward dropping the cash dispenser. Genadi pushed back on the dispenser's effort-to-sales ratio and was tasked with producing short (~2-week) and long-term schedules for the slim recycler product **IP 1055**. Full substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Apr-20). §15.8 clear. [[raw/Meeting_Transcript_genadi_schedule_review_alignment-April-20-2026.md]] [[raw/Meeting_Notes_genadi_schedule_review_alignment-April-20-2026.md]]

## Apr 21 2026 — continue planning: the Flex Slim (IP 1055) Jira Gantt

On the [[wiki/meetings/2026-04-21-genadi-continue-planning.md|Apr-21 continuation]] (~1h 24m; with Val; transcript only) Genadi and Val sequenced the **Flex Slim (IP 1055)** schedule — HFM 529 design (to ~May 8) → tooling (pilot molds, ~1-month lead) → transition-to-production (prototypes, metal set, BOM story HFM 556), with IP 1055 wrapping ~end-June and a production run ~June 20. Genadi flagged he can't finish HFM 519 (complex plastic) by May 8 (needs ~a week more) and that a flash-mounted touchscreen sample must be ordered to the vandal standard (~14 days). He also raised the refreshed-cabinet line (IP 759 / "Flex S"), needing a market-requirements review with the product side ([[wiki/people/andrei-klimovich.md|Andrei Klimovich]]; Val also referenced [[wiki/people/juan-martinez.md|Juan Martinez]]), and discussed a planned Georgia trip to help the on-site person set up the warehouse/production layout. Full substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Apr-21). §15.8 clear. [[raw/Meeting_Transcript_genadi_continue_planning-April-21-2026.md]]

## May 22 2026 — general alignment: task load and the May 26–30 Georgia trip

On a short [[wiki/meetings/2026-05-22-genadi-general-alignment.md|May-22 general-alignment 1:1]] (~15m, 3:32pm ET; with Val) Genadi ran his current hardware task load and laid out his **Georgia trip: depart Tuesday May 26 morning (via Buffalo), arrive Tuesday afternoon, return Saturday May 30 morning** — booked to keep a full working day Friday May 29. He had a "whole list" of tasks from **Elizabeth and Filipp**: assemble the two Flex Cash Dispenser samples (one Dispenser, one Recycler), walk assembly steps through with the on-site team, review the **Maple** assembly/wiring, and study the **parts-finding / shop-organization gap** (Filipp flagged that Toronto's shop made parts easy to find but the Georgia team spends too long looking — Genadi wants to learn what Toronto did differently). He is finishing **INBC port numbers** so **Andrei (Andriy)** can test next week, still owes the **Slim** BOM + review harness, and booked a **Monday May 25 AM** session with [[wiki/people/mikhail-perelman.md|Misha]] to walk the **Prinzera** BOM and order 3 PCBs + components for the 10-unit build. The meeting ended when Val cut it short to send a Flex-POS release-schedule planning email (he'd noticed the schedule looked off when the Flex-POS release landed the same day). Device/sourcing substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (May-22). §15.8 clear (device/component/sourcing/logistics economics only). [[raw/Meeting_Notes_Genadi_General_Alignment-May-22-2026.md]]

## Aug 6 2026 — asked to build a hardware "CxO" AI; current build status

On the [[wiki/meetings/2026-08-06-ai-engineering-workflow-hardware-cxo.md|Aug-6 1:1 with Val]], Genadi said the builds are almost finished with only small fixes left and the units are close to production-ready; he works mainly with **Andrei and Elizabeth**, uses **Claude** for analysis (e.g. choosing a module/modem in minutes instead of ~2 weeks by hand) but not for compilation, and said his **SolidWorks PDM** already manages files well (he loses no time on file organization and has never lost a file or revision). He asked whether he needs a SolidWorks license or a daily-use file server (left unresolved — Val will read up). [[raw/Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]

Val asked him to **build a hardware "CxO" AI** (a hardware operational/product officer) with proper references, in the simple/low-bureaucracy form suited to a one-person department. Two component types — **BUY** (market parts with part numbers: power supplies, PLAs, monitors) and **MAKE**; engineering specs/artifacts in **GitHub** next to code/prose/ADR tied to the project repo, with the order reference/part number as a cross-reference in **Business Central**; the second brain (raw source data) built in **Obsidian**, wiki/documents in GitHub. Val offered to help set up the starting prompts and to build a second brain for the hardware CxO from Genadi's accumulated **Outlook quotations** so it can review prices/quantities and help automate sourcing. Genadi flagged 4–5 topics to firm up as next steps; Val will send him the meeting transcript as a base. Method context on [[wiki/topics/ai-assisted-development.md]] (Aug-6). [[raw/Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]] [[raw/Meeting_Transcript_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]

## Open commitments

- [ ] Genadi Peari — spend a couple of days in conversation with AI to assess where SolidWorks/AI integration stands and how organized files across Business Central + SolidWorks + GitHub would help a hardware CxO — due TBD — [[raw/Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]
- [ ] Genadi Peari — firm up the 4–5 next-step topics and structure the past year's accumulated quotations so a CxO can review prices/quantities for sourcing — due TBD — [[raw/Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]

## Aug 12 2026 — the hardware GitHub standard, the BC sync, a JCM recycler and a cheaper board

A ~2.5-hour 1:1 with Val ([[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug-12 3:00 PM ET]]; Genadi is the transcript's "Speaker 1"). [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

- **Sourcing.** He had contacted JCM about its four-drum recycler, received the full SDK and documentation and a link to its engineering sustaining team, and been quoted 1,850 for one unit (currency not spoken; the notes read it as dollars); he agreed to organise a sample to Minsk. He also argued for the **RK3576 with 8 GB** (sample ~$150, cheaper in production) over a ~$250–290 16 GB board, as "more than enough" for a street machine. See [[wiki/organizations/jcm.md]] and [[wiki/topics/low-cost-street-machine.md]] (Aug-12). [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **Purchasing gap he named.** A quotation for 43-inch touch screens for the next month had waited a week with no PO approval, "between chairs"; he wants something automatic to chase it, not him or Val. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **The repository question.** He raised it because Andrey had asked him how to prepare a repository. He described buy vs make components, said his electronics are already in product-organised GitHub repos, and pushed back on the draft in two places: why two separate repos (hardware-mechanical vs hardware-manufacturing) when only final versions go to GitHub — which led to the merge — and against new numbers for a finished product when its BOM changes (versions under the same number would be fine). He described a release as source + Gerber archive + pick-and-place + BOM + schematic PDF. Detail on [[wiki/topics/github-release-management-pipeline.md]] and [[wiki/topics/business-central-erp-implementation.md]] (Aug-12). [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **His review role.** Val told him he should not upload the files himself: the engineer opens the pull request and he, as reviewer, merges it. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Open commitments (Aug 12 2026)

- [ ] Genadi Peari — write the BOM-synchronization section into the draft hardware standard — due unspecified — [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [ ] Genadi Peari — read the draft hardware standard (knowledge-repository invitation) and approve the pull request if he agrees, raising any disagreement now — due unspecified — [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [ ] Genadi Peari — write a scope/task from this discussion so Nathan Carver can start the GitHub→BC sync capability — due unspecified — [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [ ] Genadi Peari — ask JCM for one recycler unit and organise delivery to Minsk — due unspecified — [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Aug 24 2026 — costs the Flex-Port-Mini down to ~$40–45, and picks up AI agents in a day

On the [[wiki/meetings/2026-08-24-flex-port-mini-capabilities.md|Aug-24 Flex-Port-Mini session]] (Russian, with Val and [[wiki/people/pavel.md|Pavel Frolov]]) Genadi acted as the cost authority on the new port. Product ruling: [[wiki/decisions/2026-08-24-flex-port-mini-via-second-sas-only.md]].

- **He held the line on the build cost against Val.** Val pushed low — "$20, да?" then "В $30 мы можем вложиться?" — and Genadi initially agreed to $30 (he had himself floated $25 earlier); once he costed the scanner and memory he reversed: "все равно мы вложимся в 40. Мы не вложимся в 30" — we will fit in 40, we will not fit in 30 — and settled on "40 плюс минус 5… я бы сказал что $40. 40 45, да," which Val accepted as a $45 working budget. His breakdown: the scanner engine costs **$11** today, plus an interface board JVL makes itself (he quoted around **$15** for it), and flash memory is the other driver — even 32 [MB] "будет стоить наверное, $10, если не больше." [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **He won the argument for a minimal screen.** Val wanted none; Genadi argued for "без тачскрина самый простой маленький экранчик" at around $5 "на случай, что нам надо какието месседжи выдавать всётаки может мы чтото не видим," and when Pavel identified the cash-out prompt as the concrete need, Genadi: "Вот это нужен экранчик для этого." [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **He supplied the reference costs for the existing devices:** today's full Flex-Port with scanner and screen sits "в районе 140 $150," its board alone had cost **$45** before memory prices rose, and the Flex IQ bill of materials came to about **$210** fully assembled with enclosures. He vouched for the current scanner's quality: "он очень качественный. На самом деле мы мы не взяли какойто крапий там китайский." [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **He argued for daisy-chain support so the operator does nothing.** "тогда оператору вообще ничего не надо делать, просто тот же провод. Из бута гус воткнул, изъяла борт, воткнул к нам" — unplug from Mutha Goose, plug into JVL — and rejected WiFi on installation grounds ("нам же надо будет в каждую машину пытаться, гдето пристроить антенну… может даже вай фай сложнее установить") and on cost ("это уже не будет $30"). He also flagged the residual risk: if an operator will not disconnect Mutha Goose, new cabling is needed anyway. [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **He expects free hardware to multiply uptake** — "Было бы гораздо больше, если бы все бесплатно всё это забирать… Наверно было бы в 5 раз больше" — and read the payback as fast: "это будет окупаться за 2 недели. Наверное, это почти фри." [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **AI-agent adoption (warm-up segment).** He reported being delighted the previous week: an "Andrei" (which Andrei is not stated) showed him "пару фокусов как как агентов настраивать"; he mastered it "буквально за день" and has used it for GitHub work and for asking how to structure "MSBC" (recorded as transcribed; not expanded in the source). This follows Val's Aug-6 push for him to build a hardware "CxO" — see [[wiki/topics/ai-assisted-development.md]] (Aug-24). [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Preamble-August-24-2026.md]]

## Aug 25 2026 — briefed on the 25-machine Texas install; argues cash box over cassettes

On an [[wiki/meetings/2026-08-25-texas-install-recycler-sourcing-cpi.md|Aug-25 call]] (~10:39 AM ET, English; Val greets him "Kenadi", the transcript labels him "Speaker 2") [[wiki/people/val-levitan.md|Val]] briefed him on a Texas conversion of 25 machines to one recycler plus 25 Flex-Ports, and on finding a larger recycler. Device substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Aug 25). [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]

- **He asked the scoping questions.** Dollar capacity ("how much we want to recycle"), denominations, "twenty five recyclers or… one recycler", and whether JVL cabinets are included (no — "an existing location that we are converting"). [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- **He argued the real limit is the cash box, not the cassettes.** "more cassettes, it doesn't help you because you fill up cassettes… you need a huge capacity the cash box". He put a standard cash box at "nine hundred" bills against Val's "twelve hundred". [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- **He rated JCM better on configurability** than the present unit, and called the "IT" vendor's cradle-port product flimsy: "looks like a toy". [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- **He saw the flaw in a shared floor printer at once** — "somebody else grab your ticket who is beside the printer" — and offered printing at the cashier through IQ as the alternative. [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- **He named a "Matthew Cherian"** when Val asked about contacts at CPI; the source does not make clear who he is. [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]

## Open commitments (Aug 25 2026)

- [ ] Genadi Peari — get in touch with Emmanuel to find out which bill acceptors the Texas location has — due unspecified — [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- [ ] Genadi Peari (by context — Val said "Let's connect with CPI" without naming who; the notes assign it to Genadi) — get CPI's stackable-recycler product information and SDK, and check its protocol against JVL's current integration — due soon ("there isn't too much time before… the go date") — [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]] [[raw/Meeting_Notes_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- [ ] Genadi Peari — send Val one-directional status updates on the Texas preparation ("I don't want to chase you") — ongoing — [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]

## Sept 2 2026 — the new boards that unblock the Flex-IQ pilot (reported; Genadi not present)

On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 Flex-IQ pre-pilot call]] (Russian; Genadi **not present**) two pieces of his work were reported as the hardware path for the pilot. [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

- **He solved the barcode-scanner placement and ordered the boards.** [[wiki/people/andrei-klimovich.md|Andrei]]: "Геннадий уже придумал. Мы ждём на следующей неделе новые борды, которые позволят нам вывести сканер на переднюю панель." The same boards are to carry the printer **switcher** that passes Mutha Goose's printer signal through Flex-IQ when IQ is active and disconnects when it is not — agreed between Andrei and Genadi, along with rolling the harness back to version 1. See [[wiki/decisions/2026-09-02-activate-incomm-cards-by-barcode-on-flex-iq.md]] and [[wiki/decisions/2026-09-02-implicit-consent-and-mandatory-printed-receipt.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **He is cutting board flash cost with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]].** [[wiki/people/pavel.md|Pavel]]: "Геннадий сейчас там занимается с алексеевым тем, чтобы заменить одну микросхему на другую[,] Там в 4 раза меньше памяти[,] она значительн[о]… экономит деньги" — the follow-through on the flash-reduction direction recorded on [[wiki/decisions/2026-08-24-flex-port-mini-via-second-sas-only.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **The memory-threshold question was referred to him.** Pavel, asked at what memory size remote firmware update becomes possible: "это мы можем переадресовать этот вопрос геннадию и Евгению алексееву… Я этим вопросом не занимался" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **Val wants him on the Monday follow-up.** Pavel: "Нам Геннадий не нужен на том митинге[?]"; Val: "Да нужен" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 2 2026)

- [ ] With [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — answer at what flash size remote firmware update becomes possible on the cheap SAS SMIB board, and whether that can be set as a requirement — due unspecified — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Sept 4 2026 — the parts inventory for the first ten Slims, and the two things he says out loud that nobody else does

Genadi is the load-bearing voice in both midday calls of Sept 4 2026.

**On the modem call** ([[wiki/meetings/2026-09-04-lte-modem-firmware-mismatch-and-kore-settings.md]]) he is the one who names the cause, and names it as a strategic error rather than a technical one: Minsk's 7455 came from AliExpress, Georgia's identical model number came from elsewhere with different firmware — "то, что они разные… это была ошибка номер один." He also supplied both remedies: two types of modem, five of each, already received with a second version going in, and the same modem in a North-America variant on Amazon at about **$16** where the firmware is likely right, finishable "дня 2." And he took the antenna position: put it into an opening, do not glue it to the body, "потому что все сигналы же уходят." Ruling: [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

**On the production call** ([[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md]]) he walked the entire Flex-Slim bill of materials from memory — two Slims in hand and eight in the ocean, twenty plastics landed in Georgia, ten card dispensers bought with four installed and six in stock at about $380 each, twelve monitors, the small interface board, set wires ordered, RK3568 as the standard board — and identified the brackets and harnesses as the only real gap. Ruling: [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]] [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

**Two things he raises that nobody else does:**

- **Received goods are invisible.** The twenty plastics "пришли 20 штук[,] в системе их нету… Кроме меня сейчас, наверное, никто не знает" — nobody but him knows they are there. Val: "я эту проблему налажу[,] я её понимаю и я знаю, как её наладить… Сразу её не нала[д]ишь." This is the same inventory-visibility gap that runs through [[wiki/topics/business-central-erp-implementation.md]] [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **He does not trust Yavorsky's estimate, and says so privately.** After the engineers left and Val called it "продуктивный разговор," Genadi shook his head: "[Е]горский, когда говорит 2 недели[,] это это 2 месяца минимум… Он тянет… в любом случае без Павла это не пройдёт." **Recorded as his judgement, not as fact** [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

He also reported spending time the previous day pushing [[wiki/people/elizabeth.md|Elizabeth Palomino]] and [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] to get an order of **100 Flex-Ports** moving — her to count, him to start ordering harnesses. His reaction to Val's giveaway arithmetic was "Ничего себе," and his first instinct was the operator's: "чтобы они могли ретрофит[нуть] весь лакейшен." He asked for time on the recycler at the end of the call and Val deferred it [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Open commitments (Sept 4 2026)

- [ ] Release the drawings for the three Flex-Slim brackets — due same day or next — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Get the brackets and two or three harnesses made in China through [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] on a rush, landed within a week — due about one week — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Place the metal order for 100 units at 14 gauge once the brackets are finalised — due after the brackets — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Establish where the eight in-transit Flex-Slims are and when they land — ongoing — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Order the North-America-variant modems (~$16 on Amazon) and ship them to Georgia — due within about two days — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [ ] Rework the antenna placement so it sits in an opening rather than glued to the metal enclosure — due unspecified — [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]

## Open commitments (Aug 24 2026)

- [ ] Source and spec a cheap non-touch information display for Flex-Port-Mini and confirm flash/memory sizing so the build lands near $40–45 — due unspecified — [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]

## Sept 7 2026 (8:00) — he challenges the ticket printer, and supplies the idea the group liked most

At the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|8:00 GACS show-setup call]] (Russian) — the first of the morning's three.

- **He asked the awkward hardware question twice and lost it on the merits.** "откуда пришло требование, что нам нужен именно ticket[-]принтер на лак[ейшне]? Почему обычный ролл[-]принтер, который уже стоит, не может быть и [для e-]вол[етов]?" His case: the roll printer is already there, the TITO unit is "немножко нестандартная вещь," it needs its own supply because "они **24 вольта**," everyone else prints QR codes on ordinary roll printers, and the tickets are awkward to carry — "вот эти тикеты в кошельке не очень удобно держать, они длинные." Pavel, Chudinov and Val defended the TITO printer on paper quality and ticket format; the ruling went against him — [[wiki/decisions/2026-09-07-one-tito-printer-and-one-paper-for-everything.md]] [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **And in the same meeting he supplied the improvement everyone approved.** Starting from "каким образом [и]гро[к] получает [и]волет, если нету на машине принтера?" he proposed that the Flex-Port send a command over SAS so the ticket prints at the cashier's IQ printer — his objection to the alternative being "**он оставляет машину с выигрышем**." Klimovich: "мне нравится. Идея хорошая" — [[wiki/decisions/2026-09-07-print-the-winnings-ticket-at-the-cashier-over-sas.md]] [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **He set the Pay Slim schedule under questioning.** The brackets and fittings for the dispenser and printer are done, but the drawings had **not** gone out — Val: "вы уже отправили чертежи?"; Genadi: "Нет ещё… В течение одного[-]2 дней. Сегодня[,] завтра" — and the Slim itself about two weeks. Val converted it into Wednesday drawings, factory Monday, air freight, "в течение 2 недель это будет в Джорджии" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

*(His three commitments from this meeting — the Pay Slim drawings, the first Pay Slim unit, and the 3D-printed TITO-printer enclosure — are held once on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/decisions/2026-09-07-one-tito-printer-and-one-paper-for-everything.md]], and deliberately not re-counted here.)*

## Sept 7 2026 (9:08) — he frees the board space for the Wi-Fi module and kills Val's cost-saving idea in one line

At the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08 Wi-Fi meeting]] (Russian).

- **He said the thing that settled the access-point question.** Against Bosik's proposal to make a JVL device the AP and Val's momentary agreement, Genadi: "Андрей, это не экономия, это надежно здесь. Ротор поставить, этого не ставить — это не экономия" — removing the router is not a saving. Val withdrew his own idea straight after [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He confirmed the module already carries FCC** when Pavel queried it: "Он уже он уже включен," and compared it to the module on the Rockchip board [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He freed the space.** First "Выкинь 2 банк[.] Флэш," then the better answer to Alekseev's question about two serial connectors — "Выглядит, что нам один нужен" — giving both board space and a UART: "нам 3 сериальных порта не нужно… на порте, то есть один можно убрать… [остаётся] 2 для вай фая." He noted the printer UART is spare in this variant and that he had already sent the SAS arrangement: "мы уже договорились, куда сас[,] я уже… послал уже" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He is the one who made the antenna solvable:** "у нас [порт] торчит наружу, и там огромный периметр, по всему периметру можно пустить [антенну]," and asked for an optional socket for a certified external antenna to be fitted regardless. Alekseev would not commit — see [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He set the hardware deadline:** the module goes into the board revision now under way, "перед заказом вот этого большого количества" — before the large order [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Open commitments (Sept 7 2026)

- [ ] Provide board space and an optional socket for a certified external antenna within the Flex-Port's plastic perimeter — due unspecified; not fully agreed with Alekseev — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Sept 9 2026 — mould first, then stands and harnesses; the brackets are away

At the [[wiki/meetings/2026-09-09-october-rollout-staging-and-unit-ramp.md|Sept-9 8:43 AM rollout meeting]] (English, Plaud recording) [[wiki/people/val-levitan.md|Val]] set his order of work: "[Genadi is] working right now on changing the mold. **Making another mold, removing the screen**… that's his **number one priority**. His other priority is to install the **stan[d]s. All of the internal… components, harnesses**, everything to ensure that we can accommodate for all the purposes." [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]

**The brackets from the Sept-4 critical path are reported done:** "[t]his is already done today and sent to the manufacturer… [h]ere is already done. It's past tense" — discharging the drawing-release commitment on [[wiki/decisions/2026-09-04-brackets-and-harnesses-from-china-and-a-metal-order-for-one-hundred.md]]. [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]

**A new bracket task points at him:** the drawings for other manufacturers' machines — Light & Wonder, IGT, Banilla and Aristocrat — are to be obtained and passed to him: "[j]ust get the drawings and give it to Gennady." No owner was named for fetching them. See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]]. [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]

Full hardware picture, including the stock position and the printer fallback: [[wiki/decisions/2026-09-09-the-mould-without-the-screen-comes-first-and-the-printer-has-a-fallback.md]]. [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]

**Open commitments (Sept 9 2026)**

- [ ] Make another mould with the screen removed — stated as his number one priority — due unspecified — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]] [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [ ] Install the stands and all internal components and harnesses — his second priority — due unspecified — [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]

## Sept 11 2026 — named to control the Georgia in-house rehearsal

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] Val asked how the team practises before installing anything on October 1. [[wiki/people/pavel.md|Pavel Frolov]]'s answer: the Georgia office already has assembled Flex IQ units, so it is a matter of installing the new software, connecting the TITO printer and moving the QR scanner — "эта задача, которую, наверное, Геннадий должен… проконтролировать", with Val agreeing [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Open commitments (Sept 11 2026)

- [ ] Genadi Peari — control the in-house Flex IQ rehearsal build in the Georgia office: new software, TITO printer connected, QR scanner moved — due before October 1 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 (12:04 PM) — he loses the work-order argument, wins the enclosure, and reads the board invoice off the screen

At the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept-14 12:04 PM hardware call]] (Russian; with Val and [[wiki/people/pavel.md|Pavel Frolov]]) Genadi is the one being sequenced, and he pushes back in three places. [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

- **The one he lost.** He asked to release a **standalone TITO printer and standalone card dispenser** as peripherals first; Val refused — the cabinet comes first — and Genadi took it without argument: "**А я думал надо быстро и пропустить окей?**" But he immediately converted the loss into the thing he actually needed: "**нам надо рядом с [IQ] иметь тито принтер, чтобы работал**" and "**хотя бы в[а]ринг надо заказать**", which is how the printer *enclosure* got pulled in front of the cabinet instead. See [[wiki/decisions/2026-09-14-tito-printer-cases-come-before-the-street-cabinet.md]].
- **The one he lost on materials.** Told to hand the box to "Sasha" as a plastic part, he objected that they had agreed not to do plastic and that metal is trivial — "**если просто согнуть из металла — это очень быстро, это один день… нечего отдавать**." Val overruled him on product grounds ("**Вы не можете поставить предмет из металла на стол… Это не модерн[ый] подход**"), and Genadi conceded on his own terms: the unknowns get resolved first, then Sasha can have it.
- **The one he won.** The enclosure spec is entirely his — external desktop power supply, **RS-232 in from outside** instead of AC inside the box, **connectors on a back panel** ("**индустриальная, это как нормальная**"), and no security because "**это всего лишь принтер[]**". Val's only addition was to size the back for **400 tickets** rather than 200.

**He gave the date and Val held him to it.** IQ, then Slim, then IQ again, then the printer, all that week; the cabinet starts **September 23** — "**23 можете приступить к кабинету?**" / "**Думаю да**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

**The rest of his list on this call:** the Flex IQ covers (Elizabeth has 10; boards already changed so ten can be done by hand; the screens cannot simply be removed, so a cover has to be ordered and a permanent change issued — **not done yet**, and he said so plainly: "**Нет**"); the **FlexPay Slim** full BOM and drawing set released that day so a ~50-unit request could go the next; **one recycler only**, in the **option-2** variant that keeps the card dispenser, with the dispenser fit unchecked — "**честно говоря, я не проверял**"; the **RK3576** as the target board; and the street cabinet, where he already has ideas written down for a cheaper one-piece body and simpler electronics. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 14, 12:04) and [[wiki/topics/low-cost-street-machine.md]] (Sept 14). [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**He also carries the modem diagnosis forward, and Pavel still will not take it.** Genadi: on Flex IQ "**мод[ем] заработал сразу без всяких проблем — это симка какая[-]то [incompatibility]**"; Pavel: "**Я бы так не говорил однозначно, Гена.**" Same shape as their Sept-4 exchange. See [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Sept-14 update). [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**§15.8:** clear — hardware, sequencing and component-cost content only.

## Open commitments (Sept 14 2026)

- [ ] Genadi Peari — order the Flex IQ cover and issue the permanent change for the rear-screen removal — due week of Sept 14 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Genadi Peari — release the full FlexPay Slim bill of materials and drawing set, new card-dispenser harnesses included — due Sept 14 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Genadi Peari — check whether the card dispenser fits alongside the recycler, and order the option-2 unit — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Genadi Peari — design the standalone TITO printer enclosure (back-panel connectors, external desktop power supply, RS-232 from outside, 400 tickets, no security) — due before Sept 23 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Genadi Peari — resolve the enclosure unknowns, then hand the plastic box design to "Sasha" (§4 unresolved) — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] Genadi Peari — finish IQ, Slim, IQ again and the printer this week, then start the street cabinet — due Sept 23 2026 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Sept 15 2026 (in absentia) — the magnetic stripe reader is confirmed to stay in Flex IQ

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] [[wiki/people/pavel.md|Pavel Frolov]] raised an alarm that Genadi was about to drop the magnetic stripe reader from the Flex IQ design — "нам сейчас надо главное остановить Геннадия, а то он сейчас магни[т]ик страйп ридер выбросит из флекс[ ай]к[ью]". Val had already spoken to him and said he is not dropping it: "**я разговаривал с ним, он это не выбрасывает[;] всё, что мы уничтожаем в этом дизайне[ — ]это 2 экран… мы просто крышку делаем сверху**" — the only thing removed is the second, player-facing screen, and it is covered rather than taken out. Val asked Pavel to remind him anyway, as a precaution, in case other conversations had gone differently [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

The reader matters because Val wants the cashier login method to become selectable between a PIN and a magnetic stripe card — see [[wiki/decisions/2026-09-15-the-flex-iq-cashier-flow-login-redemption-receipts-and-records.md]].

## Sept 16 2026 (12:35 PM) — he pushes back on being told how, then concedes on evidence, and wins the identity argument

At the [[wiki/meetings/2026-09-16-street-machine-board-spec-and-georgia-class-a-order.md|Sept-16 12:35 PM alignment call]] Genadi ran the street machine's electronics down to a specification with [[wiki/people/pavel.md|Pavel Frolov]]. Three things characterise how he argued it [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]:

- **He objected, on the record, to Val specifying method.** Mid-way through Val's list of how the cabinet should open and where the electronics should sit: "**вы сейчас очень много говорите, как делать? Я считаю, что это неправильно**". He raised two concrete engineering objections behind it — machines could not then stand side by side, and there would be no room for lighting around the monitor — and both were answered on the spot. See [[wiki/decisions/2026-09-16-street-machine-electronics-move-to-eye-level-and-the-monitor-opens-like-a-cupboard-door.md]].
- **He conceded the moment he heard the evidence, and said why the argument had gone badly.** On Val's recording of technicians refusing to buy JVL machines: "**Я верю[,] просто…**", "**во-первых, я это всё слышу 1 раз сейчас**", and then "**если бы начали с Того, что просят[,] … то я понял**" — if we had started from what they are asking for, I would have understood.
- **He won the machine-identity argument against Pavel** on a supply-chain point rather than a technical one: identity should bind to JVL's own I/O board, not the processor board, because "**это наша … более надежная [шт]ука[;] поменяешь завтра … [д]ругого производителя. Нашу — нет**". Val ruled his way. See [[wiki/decisions/2026-09-16-machine-identity-moves-off-the-cabinet-passport-onto-jvls-own-io-board.md]].

**His cost frame for the whole exercise**, which is the argument the rest of the call ran on: "**Стрит машина дешевая. [I/O] bort не может быть[,] с таким количеством памятью, которое он стоит там 60[-]$70. Когда он хочет машину за тысячу?**" — and "**много денег стоит фиро[м]агнитик мемори**". On the current board price he gave "**сегодня мы платим $600 за борт**" and then corrected himself inside two lines — that was last year, and he does not know today's figure [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**Two facts he stated about the board being replaced:** he laid out its connectors and chose its components himself — "**как коннектора расставили? Это я делал[,] как компоненты[,] какие — это тоже я**" — and it is four-layer, with a processor he called "**древний**" and "**15 лет ему**" [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]].

**His status round opened the call** and confirms the Sept-14 sequence is holding: releasing the Georgia plastics (quoting and ordering now); updating the monitor scanner, moving it to a different place, needing a quotation before release; the **TITO printer** "**послезавтра**"; and the **street machine** next week [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]. He also asked Val for a reference picture for the cabinet's visual design and was told there is no competitor product to point at — see [[wiki/topics/low-cost-street-machine.md]].

## Open commitments (Sept 16 2026, 12:35 PM call)

- [ ] Genadi Peari — release the IQ moulds and tooling. Val: "**Выпускаться? Да, да, выпускать**"; Genadi: "**Я сегодня[,] завтра же я это сделаю**" — due Sept 16–17 2026 — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Genadi Peari — get the quotation for the Georgia plastics and release them — due that week — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Genadi Peari — finish the monitor scanner update (scanner moved to a different position); needs a quotation before release — due that week — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Genadi Peari — design the new street-machine I/O board (USB hub, 2 SAS, printer port, bill-acceptor port with ID003 + ccTalk, lighting support, front-mounted connections) plus the separate button/counter board — due unspecified — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [ ] Genadi Peari — start the street machine's visual design the following week, without a reference picture — due week of Sept 21 2026 — [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]

## Sept 17 2026 (1:47 PM) — he is on the receiving end of a finish-and-fit list, and then raises the costing gap nobody else raises

A ten-minute Val↔Genadi call in two recorded segments ([[wiki/meetings/2026-09-17-flexpay-slim-lid-critique-and-flexport-landed-cost.md|Sept-17 1:47 PM call]], Russian), the first of the two with Val holding a built **FlexPay Slim** and reading out complaints.

**He argued the cover was unnecessary, and lost on aesthetics rather than on engineering.** His case was that the bay is already a service compartment — the monitor locks when shut and it is opened only for service — so tidying and shortening the wires is enough without adding another cover. Val did not take it and specified a flat **metal mesh on small legs or standoffs** instead, rejecting both a box and a solid plate: "**она бы стоила нам буквально копейки, но эстетику придала просто колоссальны**". Genadi echoed it back — "**Мэш металлический[,] мэш такой**" — and took it: "**Окей… Понял**". See [[wiki/decisions/2026-09-17-a-metal-mesh-on-standoffs-covers-the-flexpay-slim-service-bay-and-legs-replace-the-string.md]]. [[raw/Meeting_Transcript_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]

**He contributed the one piece of mechanism on the call.** Having asked Val to choose between a lid that does not slam and a lid that opens itself — and been told to decide it himself — he supplied the consequence: with a gas strut "**нам не нужно делать стоперы, потому что оно поднимется на высоту этого… газ[ ]лоудера**", no separate travel stoppers are needed because the strut sets the open height. Val: "**Да да, хорошо**". [[raw/Meeting_Transcript_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]

**He corrected Val on the state of the front wiring rather than letting it pass.** Val believed the front-side connections had already been rerouted to the back — "**Помоему, что это уже сделано**" — and Genadi said plainly they had not: "**Ну не сделано, но…**" Same shape as his Sept-14 "**Нет**" on the Flex IQ covers. [[raw/Meeting_Transcript_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]

**He closed the topic with a service reservation, not a design objection:** "**Я с проводами немножко тяжело[,] на ремонт[ ]ли[,] это надо**" — the wiring is awkward where servicing is concerned. He had also let slip "**А я думал[,] что это серьёзно?**", the same deflating reaction he gave on Sept 14 when sequenced. Neither line appears in the derived notes. [[raw/Meeting_Transcript_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]] [[raw/Meeting_Notes_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]

**And in the second segment he said the thing he is the only one in the corpus who says out loud: he does not know what a machine costs.** Having priced the FlexPort electronic board at quantity with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], he put the gap to Val — it "**будет обходиться не… в $46, как должно быть**" but "**в $60 изза этих таксов**" — and then gave the reason he was raising it at all: "**вы меня[,] когда спрашиваете[:] Геннадий, сколько стоит мне эта машина? Я, честно говоря, confus[ed], потому что я смотрю… а потом я смотрю туда[,] и в[о] студии freen[t] [words]**" — one figure, then another with freight in it. He warned Val off his own numbers — "**чтобы вы не были мистейкенс с нашими ценами, потому что это зависит и прайсинг**" — because the suppliers "**перепаковывают… делают хитрости**", and "**потом это в аэропорте**". Ruling: [[wiki/decisions/2026-09-17-import-duty-gets-its-own-tax-category-in-business-central.md]]. [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]] [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

This is the third time in a fortnight that Genadi is the one who names a *visibility* problem rather than a technical one — after the twenty plastics that were physically in Georgia but invisible in the system (Sept 4) and his own "$600 за борт" board price withdrawn as last year's number inside two lines (Sept 16).

*(His four commitments from the Sept-17 lid list — the mesh, the damped legs, the wire tidy-up and the front-to-back rerouting — are held once on [[wiki/decisions/2026-09-17-a-metal-mesh-on-standoffs-covers-the-flexpay-slim-service-bay-and-legs-replace-the-string.md]] and deliberately not re-counted here.)*

**§15.8:** clear — the call is a criticism of the unit, and only the engineering faults are recorded here, never a judgement of the person who built it. No compensation material appears in either Sept-17 file.

## Sept 21 2026 — the source of the Flex-Port screen size

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM call]], Klimovich said he took the screen sizes and pixel data from Genadi: "я все взял данные от Геннадия по размеру экранов", and gave the resolution as "854 на 480" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]].

## Sources

- [[raw/Meeting_Transcript_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]
- [[raw/Meeting_Notes_Flex_Pay_Slim_Lid_and_Wiring_Critique-September-17-2026.md]]
- [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Genadi_General_Alignment-May-22-2026.md]]
- [[raw/Meeting_Transcript_genadi_schedule_review_alignment-April-20-2026.md]]
- [[raw/Meeting_Notes_genadi_schedule_review_alignment-April-20-2026.md]]
- [[raw/Meeting_Transcript_genadi_continue_planning-April-21-2026.md]]
- [[raw/Meeting_Transcript_Genadi_OMNI_Board_Communication-March-30-2026.md]]
- [[raw/Meeting_Notes_OMNI_Board_Communication_Genadi-March-30-2026.md]]
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
- [[raw/SREDs_progress_review-March-20-2026.md]]
- [[raw/Genadi_Review_draft_questions_FlexPort_IP-578-March-4-2026.md]]
- [[raw/Genadi_reply_to_Val_questions_FlexPort_IP-578-March-4-2026.md]]
- [[raw/Meeting_Notes_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]
- [[raw/Meeting_Transcript_AI_Engineering_Workflow_and_Hardware_CxO-August-6-2026.md]]
- [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Preamble-August-24-2026.md]]
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Notes_October_Rollout_Staging_and_Unit_Ramp-September-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Notes_Street_Machine_Board_Spec_and_Georgia_Class_A_Order-September-16-2026.md]]
- [[raw/Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026.md]]
- [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- [[raw/Meeting_Notes_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
