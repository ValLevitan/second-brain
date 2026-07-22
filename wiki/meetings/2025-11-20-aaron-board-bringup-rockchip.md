---
type: meeting
title: Aaron board bring-up working session — Rockchip Buildroot/U-Boot, own boot chain, pick the blue board (Nov 20 2025)
date: 2025-11-20
aliases: [Aaron Val Nov 20 board, Rockchip bring-up Nov 20, Buildroot U-Boot Aaron, blue board Genadi, SD-card EMMC flashing, Aaron + Val (1)]
source-count: 1
open-commitments: 3
---

# Aaron board bring-up working session — Rockchip Buildroot/U-Boot, own boot chain, pick the blue board (Nov 20 2025)

**Date:** 2025-11-20 (recording header 1:32 PM) · **Duration:** 31m 36s · **Attendees:** [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/val-levitan.md|Val Levitan]]. English.

A live screen-share where Aaron demonstrated bringing up the Chinese Rockchip ARM board himself — the next step in the board bring-up thread carried by [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (see its Nov-12 section) and [[wiki/meetings/2025-11-12-flexport-software-update-procedure-board-bringup.md]]. Part of the FlexPay/POS payout-device hardware arc ([[wiki/topics/flexpay-business-architecture-payout-devices.md]]). This is a **distinct session** from the August "Aaron + Val" two-cultures call ([[wiki/meetings/2025-08-15-aaron-val-two-cultures-operating-model.md]]) and the Feb-11 RGS-integration call — the "(1)" in the raw filename is Obsidian numbering, not the same recording. Corpus-wide `qmd update` + grep confirms the raw file is cited nowhere else.

Substance is on the ARM board decision (Nov-20 entry); durable points captured once here:

- **Aaron already has a working build + boot chain.** He is using **Buildroot** as the distro and building his own **U-Boot** from source so JVL controls the whole boot chain. He extracted and **decompiled the DTB** from the board he was given, binwalked and pulled the images out of it, and had soft-bricked one board (loaded the wrong U-Boot) then recovered it — so he now has a functional U-Boot builder for it. [[raw/Aaron + Val (1).md]]
- **Switched to the Rockchip 6.6 BSP kernel.** Mainline Linux (6.1/6.2) wasn't mapping the DTB to the network interface, so Aaron moved to Rockchip's official **6.6 BSP** kernel (pulled from Rockchip's official Linux source tree) to get Ethernet and the other services working. [[raw/Aaron + Val (1).md]]
- **Flashing flow demonstrated.** Write a bootable SD image, catch the board in U-Boot, switch it to boot off the SD card temporarily, then a script wipes the internal **eMMC** and copies everything onto it and sets the device boot script so it auto-starts next reboot. Aaron prefers always having a bootable eMMC image so a lost/failed SD card doesn't kill the board; Pavel would rather build a specially-organised SD image that boots fully from SD directly. [[raw/Aaron + Val (1).md]]
- **Reproducible builds via Docker + GitHub Actions.** Aaron builds inside an **Ubuntu 22.04 Docker container** (the same container GitHub uses), pulling his own user ID so files aren't owned by root — so the host OS doesn't matter. His repo has build targets (build kernel / U-Boot / Buildroot / SD image) and a **local-release vs release** split: local-release publishes images into the repo, release pushes them to GitHub with the runner's own credentials. A full build takes ~an hour or two. [[raw/Aaron + Val (1).md]]
- **The repo is structured to evaluate multiple boards.** Aaron built it so several candidate boards can share one build system (DTBs per board). Pavel confirmed JVL has the **original DTS/DTSI files** for the second ("blue") board — supplied by the vendor, not extracted — which should simplify that board. Pavel had also filed the official **SDK request to Rockchip** and expects them to provide the special files/documents. [[raw/Aaron + Val (1).md]]
- **Decision — converge on the blue board; goal is no Chinese dependency.** Genadi wants to finalise a single model so he can get quotations (price / harnesses). Because JVL has the original DTS/DTB for the **blue board**, that one is preferable / easier; Aaron will keep trying to get Ethernet + the pulled DTB working on the smaller board he's on now and, if the DTB problems persist, switch to the blue board (Pavel/Genadi to share those DTBs). Genadi's takeaway, confirmed by Aaron: eventually **no Chinese involvement** — JVL builds its own image from sources. Boot from USB was ruled a partial (not full) boot ("99%"); JVL will stay with the **TF/SD card** for full updates and a separate partition for the JVL application. [[raw/Aaron + Val (1).md]]

## Open commitments

- [ ] Genadi Peari — finalise which board model JVL goes with (cheaper / most convenient), order more boards of the final version, and prepare a set of harnesses and displays for Aaron — due unspecified — [[raw/Aaron + Val (1).md]]
- [ ] Pavel Frolov — share the blue board's original DTS/DTB files with Aaron (taken from Aaron's earlier e-mail; Genadi also has them) and take a firm grip of the board work in the chat Val set up — due next couple of days — [[raw/Aaron + Val (1).md]]
- [ ] Aaron Bockelie — get Ethernet + the extracted DTB working on the current board; if problems persist, switch to the blue board; keep an eye on the Teams chat for the next two days — due ~2 days — [[raw/Aaron + Val (1).md]]

**Meeting-logistics note (not durable substance):** Val "ping-ponged" Aaron between back-to-back meetings because of the Minsk time difference (a narrow window to catch employees) — he cut this call to move Aaron into the next one (the [[wiki/meetings/2025-11-20-github-for-graphic-design-team-git-lfs.md|2:05 PM GitHub-for-graphics session]]) and set up a Teams chat for Genadi and Pavel to coordinate.

**§15.8:** clear — only hardware/build content and vendor logistics; no named-person compensation.

**Same-name note (§4):** [[wiki/people/aaron.md|Aaron Bockelie]] (build-pipeline/engineering consultant), [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/genadi-peari.md|Genadi Peari]] (hardware) as usual; no ambiguous short-forms in this call.

## Sources

- [[raw/Aaron + Val (1).md]]
