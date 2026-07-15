---
type: person
title: Genadi Peari
date: 2026-07-12
aliases: [Genadi Peari, Genadi, Gennady, Gennady Perry, Perry, Gena]
source-count: 20
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

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
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
