---
type: meeting
title: Flex-Port software-update procedure + Rockchip board bring-up working session (Nov 12 2025)
date: 2025-11-12
aliases: [Flex-Port software update procedure review, Flex-Port hardware suppliers requirements, Rockchip board bring-up Nov 12, device tree Chinese supplier questions, firmware update sequence Nov 12]
source-count: 2
open-commitments: 2
---

# Flex-Port software-update procedure + Rockchip board bring-up working session (Nov 12 2025)

**Date:** 2025-11-12 · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]], and (first segment only) [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. Russian.

The **next-morning firmware-update-sequence meeting** set at the [[wiki/meetings/2025-11-11-pos-flexport-schedule-review-board-update.md|Nov-11 POS + FlexPort review]] — how to update JVL software in the field on the Chinese Rockchip ARM board, and how to get the board sources JVL needs from the manufacturer. Substance lives on the ARM/Rockchip sequencer decision: [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (Nov-12 section). Continues the FlexPay payout-device arc [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

**Two-segment meeting (§12 multi-segment).** This is **one meeting recorded in two consecutive files** under the same Teams recording base name `Flex-Port_software_update_procedure_review`: segment A `[[raw/Flex-Port_software_update_procedure_review.md]]` (07:01am, 1h 2m 13s, with Alekseev) and segment B `[[raw/Flex-Port_hardware_suppliers_requirements.md]]` (08:03am, 17m 5s, without Alekseev). Segment A ends with Val telling Alekseev he has to leave ("вам нужно уже идти. Евгений, да 08:00") and closing the call; segment B begins ~7 seconds later with the same three remaining people continuing the same thread (getting the device-tree/bootloader sources from the Chinese). It is a recording split, not a second meeting — facts recorded once, each cited to its segment.

Takeaways:

- **Two update procedures confirmed:** (1) a **partial in-field update** of only the JVL application + data that must change quickly (when there is no direct terminal access); (2) a **full terminal swap** — if a remote update is impossible or something broke, install a fresh preconfigured terminal, take the broken one back to base and fully re-image it via cable using the standard tool. [[raw/Flex-Port_software_update_procedure_review.md]]
- **Server-driven update with backup + rollback:** before flashing, back up the application/partition **and** the database; download the new firmware from the server over the **secure encrypted channel**; install and try to boot; on success it's done, on failure **roll back** to the prior state; worst case, replace the terminal. The update is run from the **main program on the server** (a continuously-connected, fully-controlled process; encryption keys prevent a fake/pirate firmware being pushed). [[raw/Flex-Port_software_update_procedure_review.md]]
- **Val's added step:** set a flag when an update starts; if the terminal does not reconnect within **15 minutes**, raise an automatic alert. Rollout should be **sequential and coordinated with location owners** (a scheduler: try 2 terminals overnight, then 5, then the rest) — not a silent bulk push to 500 terminals. [[raw/Flex-Port_software_update_procedure_review.md]]
- **USB + SD-card routes kept.** The USB application update stays (not going away) alongside SD-card boot; a boot-time script checks for a USB stick carrying a newer version and updates only the JVL-application partition. [[raw/Flex-Port_software_update_procedure_review.md]]
- **Board bring-up = the gating problem.** To customise the image (bootloader config, boot screen, device tree) JVL needs the manufacturer's **sources**; the Chinese suppliers hand over only binaries, not the **device tree** ("девайс три") source or the bootloader config. Board is Rockchip **RK3568**. Alekseev's read: the peripheral addressing is essentially the same across these Rockchip boards, so the work is learning **how to build the Linux image**, not the chip architecture. [[raw/Flex-Port_software_update_procedure_review.md]]
- **Build systems.** Two main image-build systems named — **Buildroot** and **Yocto** ("ёпта") — plus a simpler single-script GitHub-repo approach (one `build.sh` that pulls and builds everything). Task for [[wiki/people/evgeniy-alekseev.md|Alekseev]]: take a repo, build a standard image, flash it to the board, confirm it boots — the build itself is ~a couple of days; standing up the full Minsk-style **build infrastructure / custom board-support package** on GitHub was sized at ~**4 weeks** ("может занять и больше"). [[raw/Flex-Port_software_update_procedure_review.md]]
- **Device-tree comparison plan.** Pavel dumped the device tree from the board on his desk; the plan is to dump it from the **second board** (Genadi's Toronto board) and compare both against the **Rockchip reference eval board** — if the configs line up, JVL can reuse the reference-design sources changing only the device tree. Genadi to request the **full schematic** for the Toronto board. [[raw/Flex-Port_software_update_procedure_review.md]]
- **Questions to send the Chinese supplier (segment B).** Ask them: the **device-tree source**; the **bootloader (u-boot) revision + its config file**; and **which build system** they use (Buildroot / Yocto / proprietary). If proprietary → drop that supplier ("даже не трогал"); if they share the **GitHub repo** that builds the same binary they ship → that supplier is confirmed suitable. Genadi has already been asking for their repo and has **not received it**; Val's read is they will share once JVL is a real ordering customer. [[raw/Flex-Port_hardware_suppliers_requirements.md]]

## Open commitments

- [ ] Evgeniy Alekseev — build a standard Linux image (Buildroot or Yocto) from a repo and boot it on a Rockchip board to prove the build path, then work toward the Minsk-style build infrastructure / custom BSP — due ~4 weeks — [[raw/Flex-Port_software_update_procedure_review.md]]
- [ ] Genadi Peari — keep pressing the Chinese supplier for the device-tree source, bootloader revision + config, build-system answer, and the Toronto board's full schematic; Pavel to keep investigating or find a more responsive supplier — due unspecified — [[raw/Flex-Port_hardware_suppliers_requirements.md]]

**§15.8:** clear — only vendor economics appear (the Chinese offered to do the bootloader customisation for **~$2,000**). No named-person compensation. Nothing held.

**Same-name note (§4):** "Евгений / Евгений Алексеев" here is [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (embedded + board work on Genadi's project), per the registry — not [[wiki/people/eugine-yavorski.md|Yavorski]] or [[wiki/people/evgeny-kharetski.md|Kharetski]]. [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/genadi-peari.md|Genadi Peari]] as usual.

## Sources

- [[raw/Flex-Port_software_update_procedure_review.md]]
- [[raw/Flex-Port_hardware_suppliers_requirements.md]]
