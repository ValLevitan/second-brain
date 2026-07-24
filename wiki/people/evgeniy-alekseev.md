---
type: person
title: Evgeniy Alekseev
date: 2025-03-11
aliases: [Evgeniy Alekseev, Evgeny Alekseev, Zhenya Alekseev, Женя Алексеев, Alekseev]
disambiguation: "Owner of the main embedded code branch, this page. Evgeny/Zhenya cluster — EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name): [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] = FlexPort/FlexPay integration software (alias Egorsky); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] = LGS/Omni backend (payroll "Kharetski Yauheni"; garble-aliases Koretski/Khorvatsky). Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. NO fourth Zhenya exists — a mention fitting none clearly is a mis-heard non-Zhenya (cf. Ethan/Efim), so treat as garble/mishearing and queue; NEVER create a new Zhenya."
source-count: 22
open-commitments: 1
---

# Evgeniy Alekseev

Evgeniy Alekseev (name confirmed by Val; "Zhenya Alekseev" / "Женя Алексеев" in the transcript) is a JVL developer who owns the **main code branch** of the FlexPort↔FlexPay embedded software. On the March 11 2025 embedded standup, the integration engineer ([[wiki/people/eugine-yavorski.md|Eugine Yavorski]]) said the main branch is "with Zhenya Alekseev" and that he would merge his own branch into Alekseev's to create the common project. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

**Owner-confirmed (2026-07-13):** Evgeniy Alekseev and [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] are **two different people**, both colloquially "Женя"/"Zhenya." Past "Zhenya"/"Женя" facts on Yavorski's page belong to the integration engineer; this page is only the main-branch owner.

On the Mar 17 standup, [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] again said he needs to **cooperate with "Женя Алексеев"** to finish the **cash-out** work — reinforcing that Alekseev owns the code the integration must land in. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Flex-port-update-March-17-2025.md]] [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]

On the Mar 25 standup, Alekseev is again the one who **can see behaviour the others cannot** on the FlexPay/machine side (Val: "то, чего мы сейчас не видим, а Евгений Алексеев видит"), so the cash-out debugging depends on him and Yavorski working together. (The transcript also renders a "Женя Львовский"/Zhenya Lvovsky, likely a mis-transcription of Yavorski — flagged, see Owner Decisions.) [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]

On the Mar 27 2025 scope-gap meeting, Val named the pair for the "make-do" local primitive SAS mini-server: "**Evgeniy Alexeev plus Evgeniy Yavorsky. Nobody else.**" — over Pavel's objection that they don't know the FlexPay operating system. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## The SAS implementation (Apr 1)

On the Apr 1 standup ([[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]) Alekseev took the **low-level SAS communication** build for the TITO/SMIB work — "создание проекта и написание исходного кода" plus hardware prep (machine, printer, validator, cable). He had studied the SAS protocol from "эти документы, которые Дмитрий приготовил" and sized it at "недели три займет" (~3 weeks; "Я-то затягивать не буду. Будет быстрее, иначе будет быстрее" when pushed); hardware needed only from the following week ("Эту неделю просто буду писать код"). Technical points he engaged: the **8-bit + 1 wakeup-bit** SAS serial quirk ("я там не вижу каких-то хитростей" — only when to send the bit was unclear), a constant address "1" per machine (one SAS-host connection each), the **IGT "SAS-тест" utility** as a test host, and that USB-to-RS232 adapters suffice. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Open commitments

- [ ] Evgeniy Alekseev — build the low-level SAS project (code this week, hardware assembled by next week), targeting ~3 weeks or faster — due ~late Apr 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Apr 16 2025 — dispensing tower is the next embedded stage

On the Genadi hardware call, Val placed the **Flex self-dispensing tower** (on the FlexPort base) as the next stage of work for Alekseev and Yavorski, after the TITO-architecture pieces (SMIB, FlexPort, Local TITO Server). He deprioritized the legacy machines that don't support FlexPort (a protocol issue on Alekseev's side) — ~3,000 of ~35,000 machines, "не первый, не второй приоритет." [[raw/fkex_pay_evolution-apr-16-2025.md]] See [[wiki/decisions/2025-04-16-dispensing-tower-first-magnetic-stripe.md]].

## SMIB/SAS bring-up (Apr 15, Apr 22)

- **Apr 15:** on the SMIB weekly ([[wiki/meetings/2025-04-15-embedded-group-smib-sas-printer.md]]) Alekseev reported **getting the SMIB↔machine SAS exchange working** after connecting Pavel's **AGT emulator** on COM1 and tracing the packets — the key discovery that the machine won't respond until it receives an **"81" packet** (a SAS PING carrying the machine address). He is building the SMIB on the **existing FlexPort board** for now (to be cannibalised into a cheap dedicated board later), with a basic Minsk-debug variant promised for the following week. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- **Apr 22:** on the follow-up ([[wiki/meetings/2025-04-22-flexport-tito-machine-setup-debug.md]]) his coding was done but **debugging was blocked** — his test machine wouldn't run in TITO mode and a Factory Reset alone didn't enable it; the group worked out the printer-connect → Factory-Reset → passport-scan → RIS → Enable-SAS procedure, and he needs Yavorski to enable TITO on his machine too. [[raw/flex_port_update-apr-22-2025.md]]

## May 7 2025 — SAS→WSS side of the TITO integration

On the FlexPort hardware call ([[wiki/meetings/2025-05-07-flexport-two-machines-tito-milestones.md]]) Alekseev owns the part that transforms **SAS → WSS** for TITO, which [[wiki/people/eugine-yavorski.md|Yavorski]] (who finished the WSS side) must dovetail with. Two slot machines had been prepared in the Toronto shop for Alekseev to test but wouldn't run until [[wiki/people/sergei-novitsky.md|Novitsky]] revived them (Alekseev had spent a Saturday on them with [[wiki/people/dmitri-chudinov.md|Dima Chudinov]]). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_port_hardware_update-may-7-2025.md]]

## May 8 2025 — his SAS ticket commands exercised

On the [[wiki/meetings/2025-05-08-flexport-flexpay-tito-standup.md|May-8 TITO standup]], [[wiki/people/eugine-yavorski.md|Yavorski]] ran **Alekseev's implemented SAS commands** for ticket-out / ticket-print on the FlexPort↔machine side and successfully printed/read a ticket; the integration continues merging against Alekseev's main branch / SAS→WSS work. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_hardware_update-may-8-2025.md]] [[raw/flex_pay_port_hardware_update-may-8-2025.md]]

## May 10 2025 — holds the weekend office access

On [[wiki/people/eugine-yavorski.md|Yavorski]]'s short weekend debug update ([[wiki/meetings/2025-05-10-flexport-flexpay-debug-update.md]]), Alekseev is named as the one who has the **office key and door code for weekend access** — Yavorski planned to take them from him to work the office over the weekend. [[raw/flex-port_flex-pay_update-may-10-2025.md]]

## May 15 2025 — SMIB board ordered; USB + firmware update assigned

On the May-15 FlexPay/FlexPort progress meeting ([[wiki/meetings/2025-05-15-flexpay-flexport-progress.md]]) the **SMIB board** Alekseev laid out is to be ordered Fri May 16 (delivery ~May 27). To that window he owns implementing **USB update handling + firmware-update capability** (target Tue May 20). Detail on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-pay_flex-port_update-may-15-2025.md]]

## May 20 2025 — partial USB done; utility + LED table

On the [[wiki/meetings/2025-05-20-flexport-flexpay-smib-action-review.md|May-20 SMIB action review]] Alekseev reported **partial USB done** (detects the stick, reads/decodes the file) with the remaining PC encode → flash → decode → memory-write → verify → switch-version utility targeted ~**May 25/26** (evolving his May-15 "USB update handling, target May 20" item). **MEI bill-acceptor compatibility** on FlexPort is on the backlog. He owns the **Red/Green LED state table** and created the JVL **SMIB GitHub repo** in-meeting. He also attended the same-day [[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md|test-plan meeting]] ("Лёша"). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]] [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]

## May 29 2025 — SMIB boards received; cheaper-processor firmware port

On the e-Wallet/TITO review ([[wiki/meetings/2025-05-29-ewallet-tito-flexpay-implementation.md]]) Alekseev confirmed **USB implementation done+tested (positive+negative)**, SAS command-packet prep (≤60 byte for WSS) done, and the LED-status doc on GitHub (21st); **MEI bill-acceptor compatibility testing → backlog**. He received **10 SMIB boards** (delivered May 26); weekend job = bring them up and **port the SMIB firmware from the expensive 176-pin "mock-up" processor to a cheaper fewer-pin permanent processor** (a firmware/pin-config project; the board layout is already done). He supplies Yavorski the internal command queue for real logging. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]

## Sept 22 2025 — universal interface board + 33 Jira tasks

On the Val↔[[wiki/people/genadi-peari.md|Genadi]] electro-mechanical alignment ([[wiki/meetings/2025-09-22-electro-mechanical-alignment-genadi.md]]), Genadi reported Alekseev is busy in Jira and will **open 33 tasks**: he is building the **monitor interface board** first, then a single **main interface board** universal to any ARM platform later dropped in — carrying a **USB hub/multiplier** ("no processor, no firmware, purely electronic"), communicating over one wire. He is also the **"Evgeny" who will adjust the FlexPort board file** to whatever Genadi's finalized mechanical form dictates (mount/size/perimeter-lighting/scanner reach) — hardware-adjacent board work on Genadi's project, per the updated §4 ruling (no fourth "Zhenya"). See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-22). [[raw/alignment_elctro-mechanical-september-22-2025.md]]

## Nov 11 2025 — Flex Sport board, the machine-startup blocker, and the field-update mechanism

On the Nov-11 POS + FlexPort schedule review ([[wiki/meetings/2025-11-11-pos-flexport-schedule-review-board-update.md]], 2h33m, Russian; Val, [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]], [[wiki/people/genadi-peari.md|Genadi Peari]]): [[raw/POS_and_PORT-schedule_review.md]]

- Alekseev closed the **binary-file preparation utility** and the **Flex Sport** (the new all-in-one board) **production-release** task; the board is ordered. He took the **USB blob-file decode** program (a computer/tablet app that parses the block file read from Flex Sport off a USB stick).
- **Blocked ~2 weeks on machine startup.** He has been unable to start the Flex machines — a stalled back-and-forth with Minsk — so his testing of HFM-164 (lockout / database / statistics-file logging) is stuck. Val ruled that [[wiki/people/pavel.md|Pavel]] must take over the root-cause hunt (why it won't start "with a light movement"), suspecting an architecture problem; Alekseev had jumped to the next task to avoid idling.
- **Owns the board field-update mechanism.** Per Part 2, Alekseev builds the two update procedures for the Rockchip board — prepare a writable JVL-application image, and a boot-time script that flashes an update off a USB stick (with backup/rollback), working the same for USB and remote. Details on [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-11). Genadi's argument: once he builds this once (~a week), JVL becomes hardware-supplier-agnostic.

## Nov 12 2025 — tasked with the Rockchip board build path

On the Nov-12 firmware-update working session ([[wiki/meetings/2025-11-12-flexport-software-update-procedure-board-bringup.md]]; Val, [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]]) Alekseev is given the concrete board bring-up task: take a repo, build a standard Linux image with **Buildroot** or **Yocto** (or a single-script GitHub-repo build), and boot it on the **RK3568** board to prove the build path, then work toward the Minsk-style **build infrastructure / custom board-support package** on GitHub (build itself ~a couple of days; the full infrastructure sized at ~4 weeks). His read: peripheral addressing is essentially identical across these Rockchip boards, so the work is learning the build, not the chip. He left the meeting at ~8am; the tail discussion (formalising the source questions to the Chinese) continued without him. Details on [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-12). [[raw/Flex-Port_software_update_procedure_review.md]]

## Nov 28 2025 — Linux image sources found; Linux-variant task handed to Aaron

On the [[wiki/meetings/2025-11-28-flexport-smib-sync-jira-review.md|Nov-28 FlexPort/SMIB sync]] Alekseev reported finding **5 usable SD-bootable Linux image sources** (Ubuntu/Debian/Buildroot) that work single-screen but need two-screen + touchscreen config (HFM-304 → ICM-327). His broader **Linux-variant task was removed** — Aaron now owns the board Linux image — and Val questioned two people being on it; Alekseev conceded he'll still have to dig into the device tree. His near-term focus is board tasks **274/275** (274 critical for Minsk, due this weekend) and diagnosing the eco test-machine that won't run (ICF-258 on hold — Val's point that JVL's anti-tamper machine design makes the home "eco" test rigs the wrong approach). He also owes Val a **link to where the design specs live** and raised the missing bill-validator diagnostics that became CPI-477 (on Dima Chudinov). Needs 10 "POS" boards from Minsk. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] and [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-28). [[raw/Flex-Port_Smib_alignment-November-28-2025.md]]

## Feb 12 2026 — Genadi to consult him on the ECHO acceptor and Flex-Port memory

On the second Feb-12 [[wiki/people/genadi-peari.md|Genadi]] call ([[wiki/meetings/2026-02-12-genadi-echo-printer-freeze-flexport-bom.md]]) Genadi named Alekseev as the person he needs for two hardware items: (1) the **ECHO gaming-cabinet printer** — a barcode-ticket bill acceptor over an unsupported serial protocol + a **24 V power adapter** (see [[wiki/topics/echo-home-gaming-device.md]] Feb-12); and (2) whether the **Flex-Port flash-memory amount can be reduced** (flash is ~half the board BOM) and pricing **EPROM** as the alternative. Val asked Genadi to raise it but cautioned that "given Alekseev's character" he might resist the memory-reduction ask — Val said he isn't sure it's his character, just doesn't want to "catch him at a bad moment." See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb-12). [[raw/Call_Genadi_Peari-February-12-2026-2.md]]

## Sources

- [[raw/Call_Genadi_Peari-February-12-2026-2.md]]
- [[raw/Flex-Port_Smib_alignment-November-28-2025.md]]
- [[raw/Flex-Port_software_update_procedure_review.md]]
- [[raw/POS_and_PORT-schedule_review.md]]
- [[raw/alignment_elctro-mechanical-september-22-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/e-wallet_tito_flex-pay_flex-port_implementation_update-may-29-2025.md]]
- [[raw/Flex-port-update-March-17-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/flex_port_update-apr-22-2025.md]]
- [[raw/flex_port_hardware_update-may-7-2025.md]]
- [[raw/flex_pay_hardware_update-may-8-2025.md]]
- [[raw/flex_pay_port_hardware_update-may-8-2025.md]]
- [[raw/flex-port_flex-pay_update-may-10-2025.md]]
- [[raw/flex-pay_flex-port_update-may-15-2025.md]]
- [[raw/flex-port_flex-pay_smib_update-may-20-2025.md]]
- [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
