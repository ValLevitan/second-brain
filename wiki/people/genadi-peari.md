---
type: person
title: Genadi Peari
date: 2026-07-12
aliases: [Genadi Peari, Genadi, Gennady, Gennady Perry, Perry, Gena]
source-count: 7
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

- **Embedded group (Feb 18):** Genadi ("Gennady") reported a **iOBoard (input/output board) detection issue** — the board sometimes isn't detected on software 4.10 and, less often, on 4.09 (resembling a field symptom); cause not yet found. His printer plugs directly into the motherboard, not through the i-board. He is to mail card dispensers to [[wiki/people/evgeny.md|Evgeny]]. See [[wiki/meetings/2025-02-18-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- **Alignment (Feb 19):** Genadi is replicating a **SAS harness** from manufacturer schematics (to replace the lottery-supplied SAS adapter) and is the contact for the **Epic Edge printer sample** ("I assume Gennady has sent it") and the **SSD drive** component for the Florida CPU kits. See [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Embedded group — FlexPay ship prep (Feb 25)

- On the Feb 25 embedded standup Genadi ("Геннадий") is the one preparing the hardware **configuration** to ship (~4 machines per FlexPay; 4 FlexPay + ~15 ports); Val pressed him to have it ready by **Thursday**. After the FlexPay+second-machine test ships, Genadi is to finish the hard-to-start machine and do a **full firmware update**. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## Flex V42/C design review (Feb 27)

- On the Feb 27 cabinet review Genadi ("Gennady") is the hardware/mechanical side: he flags that the **player-tracking bracket has predefined dimensions**, so the group agreed to keep three physical pieces made to look like one continuous piece rather than redesign the bracket ("less work for Gennady"), and he works through where the wiring/speaker channels and the credit-card reader go. See [[wiki/decisions/2025-02-27-flex-street-cabinet-design-direction.md]]. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
- Note: here "Gennady" is doing cabinet **hardware/brackets**, while a separate **[[wiki/people/igor-designer.md|Igor]]** does the industrial-design renderings — the two are distinct on this call. [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]

Name confirmed by Val as **Genadi Peari**; the transcripts render it "Gennady Perry" / "Gena", kept as aliases for search.

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Flex_V42_C_design_evolution_review_2025-02-27.md]]
