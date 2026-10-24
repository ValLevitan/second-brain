---
type: person
title: Evgeniy Alekseev
date: 2025-03-11
aliases: [Evgeniy Alekseev, Evgeny Alekseev, Zhenya Alekseev, Женя Алексеев, Alekseev]
disambiguation: "Owner of the main embedded code branch, this page. Evgeny/Zhenya cluster — EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name): [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] = FlexPort/FlexPay integration software (alias Egorsky); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] = LGS/Omni backend (payroll "Kharetski Yauheni"; garble-aliases Koretski/Khorvatsky). Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. NO fourth Zhenya exists — a mention fitting none clearly is a mis-heard non-Zhenya (cf. Ethan/Efim), so treat as garble/mishearing and queue; NEVER create a new Zhenya."
source-count: 60
open-commitments: 11
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

## Mar 25 2026 — external-specialist consult on the Georgia machine freeze

On the [[wiki/meetings/2026-03-25-freezing-investigation-alekseev-followup.md|Mar-25 freezing follow-up call]] (11:03am; Val, Pavel Frolov, Genadi Peari, Alexander Biratko) Val brought Alekseev in as an **outside voice** on the Georgia EGM freezing problem, having sent him a problem document the day before. Alekseev offered three hypotheses: **memory management** issues (leaks / out-of-bounds / stack overflow — he rated ~90% likely); **printer-driver synchronous communication** (should use a separate thread with a command queue); and **chip/GPU errata** (obtain the vendor errata sheet for the exact processor). A technical debate followed — Alekseev held that memory corruption can hard-freeze even Linux, Pavel countered that x86 Linux memory protection makes an app segfault without taking the kernel down — and when Pavel opened the actual printer HAL code (`l_printer`) it **already had mutex locks throughout**, contradicting Alekseev's assumption that the printer code lacked thread safety (Pavel: the code Alekseev wrote for the Pyramid printer, simplified from a mutex-using template, is where the gap was). Alekseev was skeptical of Claude Code from his own trial; Val judged it likely misconfigured. See [[wiki/topics/egm-freezing-investigation.md]] (Mar-25). [[raw/transcript_Freezing_investigation-March-25-2026.md]]

## Apr 28 2026 — considered for the Flex-Recycler integration, then ruled out

At the [[wiki/meetings/2026-04-28-recycler-architecture-planning.md|Recycler Architecture Planning]] session (Val, Pavel Frolov, Alexander Biratko, Genadi Peari, Irina Shishko) Val opened intending to give Alekseev the Flex-Recycler integration contract — on the assumption he knows the recycler's byte-level protocol "inside and out" because he had implemented (but never tested) the same MEI protocol for FlexPay. Mid-meeting the team discovered the vendor ships a ready-made 2025 Java library (confirmed live on the vendor's GitHub), so no byte-level protocol work is needed. Val concluded **Alekseev is no longer needed for this work** — nothing against him, but the remaining integration is in-house Java/UI work driven with Claude Code. Val also said he did not want Alekseev on the future FP7 IO-board firmware-language change, preferring a younger AI-routing engineer. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Apr-28). §15.8 clear (staffing decision + component economics; no compensation). [[raw/Meeting_Transcript_recycler_architecture_planning-April-28-2026.md]] [[raw/Meeting_Notes_recycler_architecture_planning-April-28-2026.md]]

## Aug 12 2026 (in absentia) — the engineer who opens the hardware pull request

On the [[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug-12 Val–Genadi hardware-standard session]], "Alexey" / "Alexeyev" is the engineer whose PCB work goes into Genadi's GitHub repos — resolved to Alekseev by context (Genadi's hardware projects; the contractor whose PCB exports Genadi was moving into GitHub on Jul-29). Genadi said he uploads the release files himself because it is convenient; Val said the engineer should put them there and must not also merge. In the agent's worked example, "Alexeyev opens the pull request" and the reviewer merges and tags. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Sept 2 2026 — cutting board flash with Genadi, and the memory-threshold question referred to him

Reported on the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 Flex-IQ pre-pilot call]] (Russian; Alekseev **not present**). [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

- **He and [[wiki/people/genadi-peari.md|Genadi Peari]] are swapping one memory chip for another with four times less flash, to cut board cost.** [[wiki/people/pavel.md|Pavel]]: "Геннадий сейчас там занимается с алексеевым тем, чтобы заменить одну микросхему на другую[,] Там в 4 раза меньше памяти[,] она значительн[о]… экономит деньги." Embedded/hardware-adjacent context on Genadi's board work resolves this "Евгений Алексеев" to him per the §4 cluster rule [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- **The remote-firmware memory threshold was referred to him and Genadi.** Pavel: "это мы можем переадресовать этот вопрос геннадию и Евгению алексееву" — at what flash size does remote update become possible, and can that be set as a requirement? See [[wiki/decisions/2026-09-02-flex-port-sas-universal-with-scanner-touch-vs-non-touch.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open commitments (Sept 2 2026)

- [ ] With [[wiki/people/genadi-peari.md|Genadi Peari]] — answer at what flash size remote firmware update becomes possible on the cheap SAS SMIB board, and whether that can be set as a requirement — due unspecified — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Sept 4 2026 — he owns the SAS module, and he sets the method: merge it, don't polish it

At the [[wiki/meetings/2026-09-04-flex-slim-first-ten-and-flex-port-sas.md|Sept-4 midday production call]] Alekseev is the authority on where SAS actually lives. Asked whether SAS is implemented on Flex-Port, he corrected the premise: "Нет, на[ ]смиб сделан" — the basic SAS functionality is on **SMIB**, agreed with the WSS protocol side, and "просто надо взять этот софт[вер] модуль из СМИ[Б], перевести во флэкспорт." Val's "работа на полчаса" he put at "пару тройку дней," adding that [[wiki/people/eugine-yavorski.md|Yavorsky]] is needed [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

- **He set the method and Val took it.** Against Val's instinct to polish the trade-show demo: "не отполировать, скорее взять этот сас и добавить в основной этот мейн[-]бранч… соединить" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **And he set the scope discipline.** Against Yavorsky's request to narrow the task: "не сузить… есть документ, который делал… Дмитрий… И просто нужно, если этого недостаточно[,] просто чтоб дописали, какие ещё команды необходимо реализовать" — everything in [[wiki/people/dmitri-chudinov.md|Chudinov]]'s document is already implemented; if more is needed the document gets extended [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **He asked for the estimate to be deferred** until he has tried to insert and test it — "Может он… уже работает в достаточном объёме" — and he is the one who remembered the Jira ticket: "и джиру бы надо создать" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].
- **He accepted the cancelled weekend without argument** ("я то не против") while naming the real cost: "это ж опять надо всё вспомнить… мне тоже надо опять всё собирать" — the working environment has to be rebuilt from scratch [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

Ruling: [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]].

## Open commitments (Sept 4 2026)

- [ ] Restore his working environment and merge the trade-show SAS work into the Flex-Port main branch, connecting it up and checking what he can — due the weekend of Sept 5–7 2026 — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [ ] Create the Jira ticket for the SAS-on-Flex-Port work — due unspecified — [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]

## Sept 7 2026 — he specifies the Wi-Fi module, loses the antenna argument to certification, and takes remote update off Yavorsky

In both Monday meetings ([[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08]] and [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02]], Russian) Alekseev is the hardware voice.

- **He answered Val's opening question in three words** — "Конечно, есть вай фай" — and specified the answer: a module soldered onto the Flex-Port board, "намного дешевле и проще," at "4 $5 за борт," running the module's standard firmware over a UART so the existing WebSocket channel is simply duplicated, "может даже клод справиться" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He wanted a module with its own antenna and lost**, but on his own ground: the constraint he then supplied — "мы должны применять сертифицированную антенну, если мы хотим сертифика[цию]… все модули сертифицируются с определёнными видами антенн" — is what the ruling rests on. His evidence for onboard antennas was four devices he has built, one inside "полностью закрытого [железного] ящика" — [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He raised the three-interfaces-one-firmware problem** that Val could not answer and Pavel then solved [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He is on vacation that week** — "эту неделю я в отпуске не могу" — and has the Wi-Fi work, which is why Pavel took the larger part of SAS [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He put Flex-Port error handling at about 80 %** and was certain only of the heartbeat; Chudinov's "реализовано, но не проверялось" is the correction that stuck — [[wiki/decisions/2026-09-07-error-recovery-and-non-functional-requirements-come-first.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He volunteered for the remote firmware update** after the Wi-Fi work, when Val took it off [[wiki/people/eugine-yavorski.md|Eugine Yavorsky]]. His last test of it was "ещё год назад," against a simple simulator he wrote himself rather than over USB [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He explained the flash cut and its cause:** two 16 MB blocks instead of two 64 MB, ~10 MB used, "процентов 60," because "последний прайс на этот чип, который у нас заложен — $148. Я там вообще охренел просто" — [[wiki/decisions/2026-09-07-flex-port-flash-cut-to-two-sixteen-megabyte-blocks.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **He tried the shortcut and was refused.** Suggesting they simply amend the existing Jira ticket to say a module should be added, Val said no five times: "Давайте пусть больше будет ответственн[ости]" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **His standing request finally landed.** The emulators/virtual test system he says he has asked for since Flex-Port began — "я всё время просил сделать какие-то эмуляторы" — became [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]]. He can write the machine emulator himself; it is the Flex-Pay side he needs from someone else [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **Access, not willingness, is his blocker on prose:** "мне надо туда подключиться — для начала, чтоб кто-то меня подключил, ввёл [в] курс дела." Bosik undertook to set him up on Claude Code that day [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Open commitments (Sept 7 2026)

- [ ] Produce the new Flex-Port board configuration with the Wi-Fi module and tell [[wiki/people/genadi-peari.md|Genadi Peari]] what to add — due before the large board order — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Implement the Wi-Fi link on Flex-Port using the module's standard firmware, duplicating the WebSocket channel — due ~2 weeks max; no boards yet — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Implement and verify the remote firmware update on Flex-Port, after the Wi-Fi work — due after Wi-Fi, high — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] Do Wi-Fi first; SAS only at weekends this week — due this week — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Sept 9 2026 — booked for at least a week, offered the remote-log work, and floated for full time

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]]:

- **His current load:** "у Алексеева пока есть актуальные задачи по вайфаю. Это раз[;] во[-]2[,] доделать обновление прошивок… этих задач хватит? Ну на неделю точно" — the Wi-Fi tasks plus finishing the firmware-update work of [[wiki/decisions/2026-09-07-remote-firmware-update-mandatory-and-taken-off-yavorsky.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **Why the SAS work went to Pavel instead of him:** distance from the hardware. [[wiki/people/pavel.md|Pavel]]: "у Алексеева этого не будет ничего… он будет всё равно нас дёргать[,] но с задержкой в сутки[ —] дайте мне правильный софт, а поправьте мне в софте там что[-]то… суточная задержка всегда почти на любой запрос." Val reframed it rather than accepting it as a cost: "вот я ему дал работу, я пошёл спать, а он работает." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **What Pavel wants to give him:** the remote log-transfer work — "какой[-]нибудь вот… lo[g]s transferring это можно Алексееву, если он сможет это взять и вести… [е]сли он не только в выходные будет работать" — the feature specified on [[wiki/decisions/2026-09-09-three-more-flex-port-features-onto-capability-165.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **Val raised changing his employment basis:** "я могу, например, Алексееву попросить взять [эту работу] на своей работе или взять его на фултайм работу." Not resolved. Pavel's read of working with him: "долго его убеждаешь в том, что надо другим путём идти, но в целом он адекватный." **§15.8: recorded as a capacity/assignment question only — no terms or compensation appear in the source.** [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 14 2026 — his working method is named as the gap the code standard closes, and Bosik is sent to explain it

Half of the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|Sept-14 7:37 AM code-standards call]] (Russian) is about him. **He was not on it** — "**На этом митинге его нету… Он не сидит на месте**" — so everything below is reported by others [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. He was one of the two addressees of the code-standards email, with [[wiki/people/pavel.md|Pavel Frolov]].

**§15.8 — what is withheld.** The same passages contain repeated personal and performance assessments of him by [[wiki/people/val-levitan.md|Val Levitan]]. Those judgements are **deliberately not recorded on this page**, as are any engagement or compensation terms (none appear in the source). What follows is the **engineering working method and the process instruction** only.

- **How he lands code.** "**Кладёт код… большими порциями. Там огромное количество строчек, потому что он работает у себя на локальном компьютере, всё делает, а потом…**" — large portions, a huge number of lines, because the work is done on his own local machine first [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **He works as a single developer with no branching off his branch.** Val, in the same call: "**Алексеев он в принципе делает он сингл девелопер. У нас нету там ответлённых бранчей, и он берёт бранч… потом у него втягивает мень[н]**" — he takes a branch, completes it, and it is pulled into main [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Val ties the behaviour to the missing documentation, not to the man:** "**он держит весь код… должен быть в курсе всех дел, потому что нету ни прозы, ни описания, ни релиз[-ноутз]… ничего нету этого**" — no prose, no description, no release notes, so he has to stay across everything by hand [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. This matters directly to his own commitments above, which repeatedly turn on rebuilding a working environment that only he holds.
- **The rule he applies to other people's hands:** "**хорошо, если есть ошибк[а], ты её нашел. Так скажи мне, я это сделаю, я это внедрю. Но не лезь сам своими руками туда**" — tell me and I will implement it; do not go in there yourself. Pavel confirmed the characterisation: "**Это было примерно так**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. It is the exact opposite of paragraph 2's "the code belongs to the project" — see [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]].
- **What is being done about it:** [[wiki/people/andrey-bosik.md|Andrey Bosik]] books a meeting with him for the next morning and takes him through JVL's standards and practices, explaining the reasons, the dependency and the sequence rather than issuing the instruction — [[wiki/decisions/2026-09-14-alekseev-is-walked-through-the-standards-by-bosik-not-ordered.md]]. Bosik had already written to him about setting up his environment and running a short training, and was waiting for a reply — the continuation of the Sept-7 Claude Code setup undertaking [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **His availability window is stated for the first time:** "**в 07:00 он может взять митинг[;] в 8 он уже бежит на работу к себе**" — he can take a meeting at 07:00 and by 08:00 leaves for his own job [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. That is the explicit version of the weekend-only pattern already recorded here for Sept 7 and Sept 9.
- **The resourcing contingency, recorded as a resourcing fact:** if Bosik judges after the meeting that the way of working will not be adopted, JVL looks for another developer; Val's stated preference is to resolve the situation rather than break it. **The associated judgement about him is excluded** — [[wiki/decisions/2026-09-14-alekseev-is-walked-through-the-standards-by-bosik-not-ordered.md]] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Sept 14 2026 (12:04 PM, in absentia) — possibly needed on the firmware-distribution protocol

Separately from the 7:37 AM call above, [[wiki/people/pavel.md|Pavel Frolov]] named him at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|12:04 PM hardware call]] as possibly needed on the Flex IQ ↔ Flex-Port firmware-distribution work: "**возможно, как раз по этой задаче нам понадобится Алексеев, ну по[-]моему там на него тоже задача висит**" — and he thinks a task is already assigned. **Hedged on both counts and unconfirmed anywhere in the source.** The lead on it is [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(§4: "Алексеев" resolves to this page by context — embedded / hardware-adjacent work on [[wiki/people/genadi-peari.md|Genadi Peari]]'s projects, which is exactly what a Flex IQ-to-Flex-Port firmware protocol is.)*

**§15.8:** clear — task assignment only; no compensation or performance judgement is taken from this source.

## Sept 17 2026 (in absentia) — he is the one who prices the FlexPort board at quantity

[[wiki/people/genadi-peari.md|Genadi Peari]], putting the landed-cost problem to Val on the [[wiki/meetings/2026-09-17-flexpay-slim-lid-critique-and-flexport-landed-cost.md|Sept-17 1:54 PM segment]], named him as the person he checks board prices with: "**он стоит сегодня[ — ]я проверил на квонти[ти] с алексеевым**". The board is the FlexPort electronic board; the component price and the ordered price are **$46 and $60**. He was not on the call. See [[wiki/decisions/2026-09-17-import-duty-gets-its-own-tax-category-in-business-central.md]]. [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

This is the same working pair the corpus records on the flash-chip reduction (Sept 2 2026) and on the Aug-24 Flex-Port-Mini costing — Alekseev supplies the board numbers, Genadi carries them to Val. [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]

*(§4: "алексеевым" resolves to this page by context — board pricing on a Genadi Peari hardware project. **§15.8:** component pricing only, no compensation content.)*

## Sept 22 2026 (in absentia) — named as a user of the FlexPay emulator

On the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]], Pavel said the FlexPay emulator Anton is building is needed by QA "и Евгению Алексееву ещё кому-то, кто будет проводить тесты" — the Flex-Pay side Alekseev asked for on Sept 7 ([[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]], Sept-22 update). The bare "женя" Pavel offered as a test writer in the same passage is **probably** him (**inference**, not asserted) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].


## Sept 23 2026 (in absentia) — the intended user of the kiosk emulator for Flex-Port firmware

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]], Pavel named Flex-Port firmware updates as the emulator's most critical use, "Для Того, чтобы это можно было отдать там… Евгению алексееву". The emulator does not yet support the Flex-Port. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-23 update). [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

## Sept 25 2026 (in absentia) — Khamin is told to request a meeting with him

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]], [[wiki/people/alexei-khamin.md|Khamin]] asked whether they would meet "с алексеевым". Pavel asked what was needed from him "по прошивкам"; Khamin: "У меня мой пиар так и висит." Pavel: "Запроси митингу Алексеева." Irina: include Pavel. (Surname only; firmware fits this page's role.)

## Sept 26 2026 — WebSocket "later", the GUI page for himself, and new boards to test

At the [[wiki/meetings/2026-09-26-flex-port-telnet-console-and-gui-harness.md|Sept-26 Flex-Port development sync]] (Russian) [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]:

- **WebSocket.** He asked whether WebSocket had been tried on the Wi-Fi link; Pavel had not tried the one built into the module firmware. He began to ask whether Wi-Fi should be built into the WebSocket, then: "Ну ладно это потом." See [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] (Sept-26 update).
- **The GUI page.** "Мне бы хотелось бы" — Pavel showed him how to run the GUI harness. He asked which UART the console uses (the three-pin one).
- **New boards.** "Платы пришли" (count garbled) and "поиспитываем" — we'll test them.

## Open commitments (Sept 26 2026)

- [ ] Evgeniy Alekseev (speaker; "поиспитываем" = "we'll test", who exactly is not stated) — test the newly arrived boards — due unspecified — [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]

## Sept 28 2026 (8:02 AM, in absentia) — PORT-13 stays with him; the Wi-Fi software is taken off him

On the [[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]] (Russian; he was not present) [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]:

- **Firmware delivery.** Pavel: part of the remote-update tasks "[с]тояла на алексееве, но поскольку он работает только в выходные", and offered to take the story "порт 13 по доставке новой прошивке на flexport" himself. Val: "Я бы оставил бы это алексееву." So PORT-13 stays his, now inside MVP 1. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-28 update).
- **Wi-Fi.** Pavel: "вай фай я у него забрал он он только железо сделал" — Pavel's team does the Wi-Fi software. See [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]] (Sept-28 update).

## Open commitments (Sept 28 2026)

- [ ] Evgeniy Alekseev — deliver the firmware-delivery story PORT-13 for the Flex-Port, now in MVP 1 — due unspecified (the MVP 1 date is October 15) — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]

## Sept 29 2026 (8:06 AM, in absentia) — a working bootloader version handed over; "Monday" as reported

On the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian; he was not present) [[wiki/people/alexei-khamin.md|Khamin]] said: "вчера Алексеев тебе дал рабочую же версию, которая ставится [на] нормальное устройство[,] бут лодер… Говорил в понедельник буду готова, но если нет, значит… через костыли устанавли[ваем]… и обновляем" — a working bootloader version was handed to Pavel the day before, Alekseev had said it would be ready "в понедельник" (which Monday is not said), and the fallback is to install by workaround. Pavel: "у Алексеева спросим готовность прошивок… загрузчик". Surname only; firmware fits this page's role [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]. See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-29 update).

## Open commitments (Sept 29 2026, 8:06 AM — reported, not spoken by him)

- [ ] Evgeniy Alekseev (as reported by Khamin) — have the Flex-Port bootloader firmware ready for installing on a normal device — due "в понедельник" (which Monday is unclear) — [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

## Sept 30 2026 (in absentia) — the port side of firmware delivery stays with him

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; he was not present) Pavel, on Flex-Port firmware delivery: "нам надо придумать способ… [п]ередачи файла на флекспорт. А дальше мы эту работу оставляем на Алексеева, чтоб он дальше на порте сделал" — the Flex IQ side designs the delivery; what happens on the port is his (consistent with PORT-13 staying with him on Sept 28). Surname only; firmware fits this page's role. See [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-30 update) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]. The bootloader question of Sept 29 was not mentioned.

## Oct 8 2026 (in absentia) — cheaper memory, and the boards he orders online

On the [[wiki/meetings/2026-10-08-genadi-bom-standard-flex-slim-metal-mikhail-hand-over-and-data-contracts.md|Oct 8 3:59 PM alignment call]] Genadi said of "Алексеев" (this page by context — boards and Genadi's projects, §4) [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]:

- **Memory.** "Алексеев сделал очень сильное с этой памятью оно сильно удешевилось" — the memory became much cheaper.
- **Board ordering.** He orders boards online, in small quantities, which Genadi calls "намного удобнее намного дешевле"; but "Миша, ему должен сказать, Алексеев сам ничего не заказывает." Genadi's understanding is that Alekseev places the order and [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] pays — "По моему, если не ошибаюсь"; how that works without a PO he does not know.
- **What he ordered.** A small scanner interface board ("То ли там $4 стоит интерфейсный") a couple of times, and two boards for IQ.

The supplier name is garbled ("lcs carver") and is not resolved.

## Oct 9 2026 (in absentia, inference) — the bootloader on the new boards

On the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Oct-9 Transactional MVP 1 call]] Pavel said the last firmware changes for different memory sizes were made "алексеевым" — Alekseev by context (**inference**). Khamin: on the new boards nothing works, and the fix is not in the repository — "Он пишет, что у него работает… это всё у него локально." Pavel will write to him — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-9 update) [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].

## Oct 14 2026 (in absentia) — a Flex-Port USB-update build promised for that evening

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] Pavel said he had caught "Евгения Алексеева" two days before and reminded him that for the release on the 15th the Flex-Port software update must work at least by USB stick; Alekseev "обещал выкатиться версию сегодня вечером" — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-14 update) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 15 2026 (in absentia) — his FlexPort branch with the new memory chips does not build on GitHub

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: Khamin said Alekseev told the team to build and test his branch themselves; it was cut long ago and does not build on GitHub. Irina: he sent it on the night of the 15th and said "проверяйте". Pavel: branch from fresh main and pull in his memory-chip changes — [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 15); [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-15 update).

## Oct 15 2026 (11:04 AM, in absentia) — merge main into his branch; the USB-stick update is MVP 1's only gap

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]: Pavel named "Евгения Алексеев, Евгений яворский" as the authors of the Flex-Port software; the new-chip changes are not checked. His PR's branch is red, and Lyosha's attempt from fresh main failed. He must merge main into his branch, fix conflicts, check that the USB-stick update works and stays active, and make it build on GitHub Actions; Val: 3 to 5 days, Pavel: the weekend should do — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-15 11:04 AM update). Val also said he has laid out Wi-Fi on the port boards, not yet tested — [[wiki/decisions/2026-10-15-flex-iq-gets-a-switch-between-its-own-access-point-and-an-external-router-and-mvp2-starts-on-the-router.md]].

## Oct 16 2026 (in absentia) — a feature for his branch

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] Khamin said a FlexPort feature for "Алексеева ветка", for the new memory chips ("хип оф памяти" as heard), is created with the right parent and its capability is in progress [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. Whether he merged main into his branch, as asked on Oct 15, is not said — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-16 update).

## Oct 20 2026 (in absentia) — the USB-stick update still gates MVP 1; a 2:00 PM meeting with him

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] Pavel said a "Дима" made a firmware-transfer API about five months ago that does not work now, and Alekseev must sort it out because he is changing the bootloader; Khamin said Alekseev knows he must provide a build made by GitHub Actions; Pavel said he was written to before the weekend that the firmware must flash by USB; a meeting with him was set for 2:00 PM that day; capability 146 on him is marked MVP 2 — [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-20 update).

## Oct 20 2026 (7:01 AM) — his release build works in his branch; Val wants the build documented so JVL does not depend on him; he writes the STM32 / FreeRTOS rules

At the [[wiki/meetings/2026-10-20-flex-port-mvp1-usb-update-and-build-standards.md|Oct-20 7:01 AM Flex-Port firmware meeting]] (Russian) [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]: he said nobody had ever made the release configuration, and he fixed the build parameters over the weekend; his work is in branch HFM-663, version 0.0.84, not in main. Pavel disputed that no release had been built before. He held that only a developer can set up an automatic build correctly, and that documenting the system so others can build it "может занять больше времени, чем разработка проекта"; Val disagreed — he does not want the company to depend on one developer. With a Claude report he said many later changes break multithreading rules (for example the double beep); he agreed to write these rules as a development standard for STM32 projects on FreeRTOS, for Claude review. After Val left: his application hard-faults in the main loop; he will fix it and move the beeper to its own thread in the same branch, and asked for a Jira ticket first. Pavel gives him access to the Flex IQ (Flex POS) emulator — [[wiki/decisions/2026-10-20-flex-port-mvp1-needs-only-an-easy-release-build-and-the-usb-update-and-alekseev-writes-stm32-freertos-rules-for-claude-review.md]] [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]. This is most likely the "2:00 PM meeting" named at that morning's stand-up (**inference**).

## Oct 20 2026 (8:31 AM, in absentia) — a story to make his build production-ready

At the [[wiki/meetings/2026-10-20-third-party-egm-bv-emulation-mode-and-sas-data.md|Oct-20 8:31 AM third-party EGM call]] Val said MVP 1 needs only production-ready release software from him; Khamin writes the story; Pavel: good if he does it over the coming weekend; release on a Wednesday — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]].

## Oct 22 2026 (in absentia) — his Flex-Port work is checked before merge

At the [[wiki/meetings/2026-10-22-daily-standup-flex-port-cashout-screens-and-native-engine.md|Oct-22 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]] Khamin said he checks Alekseev's Flex-Port work that day and will tell him whether he can merge; Irina wants Elizabeth's build to wait for it — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Oct-22 update).

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]

- [[raw/Meeting_Transcript_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- [[raw/Meeting_Notes_FlexPort_Board_Landed_Cost_and_Import_Duty-September-17-2026.md]]
- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_recycler_architecture_planning-April-28-2026.md]]
- [[raw/Meeting_Notes_recycler_architecture_planning-April-28-2026.md]]
- [[raw/transcript_Freezing_investigation-March-25-2026.md]]
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
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Alignment_BOM_Ordering_and_Data_Contracts-October-8-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [[raw/Meeting_Notes_Flex-Port_MVP1_USB_Update_and_Build_Standards-October-20-2026.md]]
- [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Cashout_Screens_and_Native_Engine-October-22-2026.md]]
