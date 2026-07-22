---
type: meeting
title: POS + FlexPort schedule review and ARM-board update-mechanism working session (Nov 11 2025)
date: 2025-11-11
aliases: [POS and PORT schedule review, FlexPort schedule review Nov 11, Flex Sport schedule review, Rockchip board reclamation Nov 11, POS_and_PORT-schedule_review]
source-count: 1
open-commitments: 3
---

# POS + FlexPort schedule review and ARM-board update-mechanism working session (Nov 11 2025)

**Date:** 2025-11-11 (12:01 PM recording header) · **Duration:** 2h 33m 56s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]], [[wiki/people/genadi-peari.md|Genadi Peari]]. Russian (English fragments mid-session). The single largest transcript in the backlog to date.

A long two-part working call on the Flex payout-device program: **Part 1** walked the Jira/sketch **schedule** task-by-task (statuses, acceptance criteria in Gherkin "given/when/then" form, module/feature owners, dates), and **Part 2** re-opened **how to update JVL software in the field on the Chinese Rockchip ARM board** and which board supplier to use — the continuation of the Nov-5 requirements call. The substance lives on the sequencer pages:

- Schedule, module ownership, the machine-startup blocker, and remote-update decision → [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Nov-11 section).
- The board supplier/update-mechanism debate (Rockchip vs STM/NXP/TI, dev-board vs finished board, application-only update, remote vs USB) → [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-11 section).

One-line takeaways: **Flex Sport all-in-one board ordered** and its basic FlexPay money-compatibility works; a two-week **machine-startup blocker** is holding Alekseev's testing, and [[wiki/people/pavel.md|Pavel]] is to own the root cause; the field-update model is settled as **update only the JVL application (not Linux), via a boot-time script, working the same for USB and remote**, built by [[wiki/people/evgeniy-alekseev.md|Alekseev]] rather than pulled from the FlexPos devs; a next-morning meeting was set to walk the firmware-update sequence.

## Open commitments

- [ ] Eugine Yavorski — send the letter describing the **protocol change** (a new command to mark the "stuck"/unclaimed money handed from Flex Sport to FlexPay) — due next day ("максимум завтра") — [[raw/POS_and_PORT-schedule_review.md]]
- [ ] Pavel Frolov — take charge of the **machine-startup blocker** (Alekseev has been unable to start the machines for ~2 weeks): organise the people and find *why* the mechanism does not start easily, not just make it run — due unspecified — [[raw/POS_and_PORT-schedule_review.md]]
- [ ] Pavel Frolov — draw a **block diagram** of the update procedure (partition structure, data layout, where downloaded/backup firmware versions live) for the firmware-update working meeting — due next day — [[raw/POS_and_PORT-schedule_review.md]]
- [x] Val Levitan — schedule the **next-morning meeting** with Alekseev to walk the firmware-update sequence, then continue the manufacturer-requirements discussion — **discharged**: held Nov-12 ([[wiki/meetings/2025-11-12-flexport-software-update-procedure-board-bringup.md]]) — [[raw/POS_and_PORT-schedule_review.md]]

**§15.8:** clear — only company/vendor economics appear (a ~$180 example board; the manufacturer's earlier ~$1,000 ask; ~$30 per field shipment; STM/NXP roughly 2× Rockchip cost). No named-person compensation.

**Same-name notes (§4).** "Евгений Алексеев / Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (embedded + board work on Genadi's project). "Евгений яворской / егорьевском" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (FlexPort/FlexPay integration software). "Дима пикулев" named again as a single-subcontractor JVL will *not* depend on ([[wiki/people/dima-pikulev.md|Dima Pikulev]]). Not resolved / queued: a Minsk night-shift **"Алексей"** who mechanically answers support questions (distinct from Alekseev); an **"Игнатий"/Ignat** Val spoke with about the Chinese reclamations; a garbled task-owner "Алексея батанова" on HFM-164 (the task is actually Alekseev's, per context) — all left unresolved.

## Sources

- [[raw/POS_and_PORT-schedule_review.md]]
