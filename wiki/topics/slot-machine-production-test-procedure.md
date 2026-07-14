---
type: topic
title: Slot-machine production test procedure (SAS/TITO functional check)
date: 2025-03-29
aliases: [production test procedure, functional check, тестирование слот-машины, SAS host emulator test]
source-count: 1
open-questions: 1
---

# Slot-machine production test procedure (SAS/TITO functional check)

An internal JVL **written test instruction** (in Russian; author and date not stated — the file carries the Mar 29 2025 staging date) for verifying a slot machine's basic functionality after installing new software and connecting all devices ("Проверить базовую функциональность слот-машины после установки нового программного обеспечения"). It documents, step by step, how a production/test machine is brought up and exercised end-to-end, including the money-in/money-out loop. Related: [[wiki/topics/test-automation-strategy.md]] (the effort to automate this kind of testing) and the SAS/TITO glossary on [[wiki/topics/jvl-machine-lineup.md]]. [[raw/test_production_product_2025-03-29.md]]

## Required equipment

- A USB flash drive with the software image, a **SAS host**, and the machine with all devices connected — **4 monitors including the topper**, printer, bill validator, and others. [[raw/test_production_product_2025-03-29.md]]

## The procedure

1. **Setup:** connect the SAS host to the machine's port and attach all devices. [[raw/test_production_product_2025-03-29.md]]
2. **Software install:** insert the flash drive, power on, wait for the install, reboot and remove the drive. [[raw/test_production_product_2025-03-29.md]]
3. **Registration:** register the machine / update its **passport**, create the needed **RIS** and an **installation** for it, apply the installation (over the network or by flash), and "raise the machine into games" ("поднять машину в игры"). [[raw/test_production_product_2025-03-29.md]]
4. **SAS configuration:** open the slot door → Setup → Network/SAS → SAS; set **Asset# = 777, SAS Address = 1**. In Tito Configuration set **Validation Mode = Secure Enhanced** — at that moment the machine drops into a tilt: "**Validation ID not configured**." [[raw/test_production_product_2025-03-29.md]]
5. **SAS host emulator:** on the Misc tab **disable "Echoing Enabled"** and **enable "Use Echo Index"**; on the Validation tab press **Initialize Enhanced Validation**; on AFT-Registration/Lock press **Register Gaming Machine**. [[raw/test_production_product_2025-03-29.md]]
6. **Functional checks:** power-cycle; verify OS and interface load, physical buttons and touch screen work, **all 4 monitors show game resources**, and the monitors' **LED backlighting** is connected and working. [[raw/test_production_product_2025-03-29.md]]
7. **Money in / money out:** in the emulator's AFT-Transfer Funds tab enter **1000** in Cashable Amount, enable Auto Inc TID, do the AFT transaction and confirm **$10** lands on the machine (i.e. amounts are entered in cents — inference). Also feed money in via the **bill validator**; make several spins in any game; press **Collect** and confirm all money pays out as a printed **ticket**; insert that ticket back into the bill validator and confirm the money credits back onto the machine. [[raw/test_production_product_2025-03-29.md]]

## Open questions

- Which product/market this instruction belongs to, who wrote it, and when — none is stated in the document. [[raw/test_production_product_2025-03-29.md]]

## Sources

- [[raw/test_production_product_2025-03-29.md]]
