---
type: meeting
title: FlexPay / FlexPort / Flex-SMIB dev-progress standup (mid-June 2025, date inferred)
date: 2025-06-16
source-count: 1
---

# FlexPay / FlexPort / Flex-SMIB dev-progress standup (mid-June 2025, date inferred)

Weekly developer progress standup chaired by [[wiki/people/val-levitan.md|Val]] (Russian). Attendees: [[wiki/people/eugine-yavorski.md|Eugine Yavorski]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] ("Женя"), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] ("Dzmitry Chudzinau"), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/genadi-peari.md|Genadi Peari]].

**Date inferred (undated Russian transcript):** content postdates the [[wiki/meetings/2025-06-13-flex-tower-pos-architecture.md|June-13 ARM/Linux architecture meeting]] and the May-26 ARM-board decision — the Linux dev-kit is already ordered ("заказал этот дев кит… запустить линукс") — so it is placed at the mid-June weekly (Monday June-16 placeholder). Era (mid-June 2025) is certain; the exact day is not. QUEUE (Tier B) for owner confirmation.

Substance — the FlexPort/kiosk idle-screen timeout design (Chudinov's split minute: a 30-second confirm screen then a 30-second countdown before returning to the idle screen, "you still here?"), FlexPort logging to external memory (no filesystem, hand-written records, machine-readable-only, ~2,400-record circular "lifetime statistics" of bills accepted/rejected; a separate on-request statistics read for FlexPort connected to a kiosk; Alekseev to ship a USB dump utility), the just-ordered ARM-Linux dev-kit for the Tower/POS (next step = boot Linux and confirm it meets requirements), and Yavorski's certification warning — a lab told him passing is "unrealistic" because of a near-ban / sanctions on **Chinese microcontrollers** (a component flagged as sanctioned must be replaced or the UL/GLI certificate is void); Genadi to ask the lab, Val notes the motherboard chip is MEI or ARM ("ARM is a company, made in China doesn't matter") — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## Open questions

- Is there really a certification ban/sanction on Chinese microcontrollers that would block the ARM-Linux board, and does it apply to JVL's machines? — [[raw/Flex-Pay_Flex-Port_Flex-SMIB_progress_update.md]]

## Sources

- [[raw/Flex-Pay_Flex-Port_Flex-SMIB_progress_update.md]]
