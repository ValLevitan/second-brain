---
type: topic
title: Slot-machine production test procedure (SAS/TITO functional check)
date: 2025-03-29
aliases: [production test procedure, functional check, тестирование слот-машины, SAS host emulator test]
source-count: 2
open-questions: 1
open-commitments: 2
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

## Nov 3 2025 — the final-machine QC checklist / release-form gap

The Mar-29 procedure above is the **software bring-up / functional check**. A Nov-3 2025 meeting ([[wiki/meetings/2025-11-03-machine-qc-checklist-release-form.md]]; [[wiki/people/val-levitan.md|Val]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/irina-shishko.md|Irina Shishko]], Russian) surfaced the **missing companion step** — a final whole-machine QC inspection and a per-machine **release form** — now that manufacturing has moved from Toronto to Georgia ([[wiki/decisions/2025-06-24-move-manufacturing-from-canada-to-georgia.md]]). It operationalizes the earlier [[wiki/decisions/2025-03-07-final-signoff-on-assembled-machines.md|final-assembled-sign-off]] ruling. [[raw/Machine Quality Control Checklist and a Release form.md]]

- **The trigger.** When tariffs on Canada loomed, JVL **mass-shipped 335 machines to Georgia** in varying states of readiness. On arrival, loudspeakers were found **not screwed into the cabinet** — the sub-assemblies were correct on the bench, but nothing verified them at the final machine. [[wiki/people/elizabeth.md|Elizabeth]] had personally checked the ~10 machines sent to one location (lights, screen, video) but the speakers sit hidden behind the front panel. [[raw/Machine Quality Control Checklist and a Release form.md]]
- **The gap (Genadi).** All **sub-assembly build instructions exist** on the server (Elizabeth works to them); what is missing is a **final full-machine checkup instruction** — power up, verify sound / speakers don't rattle, touchscreen, all monitors, boot, serial ports. "This is a hole we need to fill." [[raw/Machine Quality Control Checklist and a Release form.md]]
- **Port-testing tooling gap.** JVL used to test ~21–22 ports; the new machines expose only **4 ports (2 SAS, printer, one extra)** and JVL has **no diagnostic/loopback tool** for them, so a dead second SAS could ship unnoticed. [[raw/Machine Quality Control Checklist and a Release form.md]]
- **The release form (Genadi's proposal, revived).** A printed QC checklist that **travels with each released machine**, each item inspected and signed (touchscreens, speakers screwed, etc.) — JVL "used to do this." Val agreed it belongs in the final tech inspection and should ship with every machine, while noting even it might have missed this particular speaker case. [[raw/Machine Quality Control Checklist and a Release form.md]]
- **Root cause — lost tribal knowledge.** The late **Oleg (Hmyrov)** used to hand-check every machine; assemblers he trained kept doing so, but no one trained [[wiki/people/arkady-batson.md|Arkady]], who "never checks anything himself." Elizabeth — a degreed engineer who treats it as a career — is now preparing to **assemble 100 machines**, and Genadi will go work with her hands-on. [[raw/Machine Quality Control Checklist and a Release form.md]]

## Open commitments

- [ ] Genadi Peari & Irina Shishko — build a circulating document listing every missing step / document / instrument for reliable QC & reporting, laid out by process stage (assembly / post-assembly / troubleshooting), each stage naming who does it and what tool is needed — due unspecified — [[raw/Machine Quality Control Checklist and a Release form.md]]
- [ ] Genadi Peari — travel to Georgia (~2 weeks, late Nov / early Dec after the ~Dec-20 release tuning) to work hands-on with Elizabeth on the problem sub-assemblies; a work station to be prepared (Sergei sets up a computer); cross the border as a tourist (no laptop/tools) — due late Nov / early Dec 2025 — [[raw/Machine Quality Control Checklist and a Release form.md]]

## Open questions

- Which product/market this instruction belongs to, who wrote it, and when — none is stated in the document. [[raw/test_production_product_2025-03-29.md]]

## Sources

- [[raw/test_production_product_2025-03-29.md]]
- [[raw/Machine Quality Control Checklist and a Release form.md]]
