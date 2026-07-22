---
type: meeting
title: Requirements for the ARM-board manufacturer — software-update procedure & deliverables (Nov 5 2025)
date: 2025-11-05
aliases: [ARM board requirements Nov 5, ARM board manufacturer requirements, Chinese ARM board deliverables, Flex software-update procedure, Rockchip board update, STM vs Rockchip Nov 5]
source-count: 1
open-commitments: 3
---

# Requirements for the ARM-board manufacturer — software-update procedure & deliverables (Nov 5 2025)

**Date:** 2025-11-05 (4:05 PM recording header) · **Duration:** 35m 29s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]]. Russian.

A working call to decide **how the JVL software on the Chinese ARM board gets updated in the field** and **what deliverables to demand from the board manufacturer**, and to revisit whether JVL should instead build its own board. Continues the ARM/Rockchip platform thread on [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md]] (see the Nov-5 section there) and the FlexPay payout-device arc [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

Durable points (single source):

- **The update problem.** The Chinese board's standard way to change the system is a full re-flash (over USB cable, needing a button-press at power-on with the box opened, or via an **SD card** — "декарт"). Both are inconvenient. What JVL actually needs is to leave **Linux untouched** and update **only the JVL software** (the Flex **backend + graphical user-interface** programs) — [[wiki/people/pavel.md|Pavel]]: update "backend и график юзер интерфейс программ для работы flex."
- **The agreed technical approach (Pavel).** Get the manufacturer's full sources → verify JVL can rebuild a working Linux image with all currently-installed programs → **rework the eMMC partition layout** so a dedicated partition holds the JVL application → add a **boot-time script** that checks for a firmware file on an inserted USB stick and, if present, writes it to the eMMC at a fixed offset. That gives a **partial software-update procedure** without touching Linux. [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] would do this work (Val confirmed at the close: "какие требования к алексееву?").
- **Chinese-vs-Alekseev split (Val's call).** Val's preference was to **not** run [[wiki/people/evgeniy-alekseev.md|Alekseev]] in parallel with the manufacturer — the Chinese asked for **$1,000** and Val would rather pay them more to deliver it, finding it "легче" to work with a company that "обеспечивают весь мир" than with a single subcontractor. [[wiki/people/genadi-peari.md|Genadi]] and Pavel pushed back that handing the partial-update work to the Chinese means more time lost in explanation; Pavel: "эту работу отдавать китайцам я против." Resolution leaned to Pavel's view — **Alekseev (or Pavel) builds the partial-update mechanism; the manufacturer only supplies the sources/deliverables.**
- **Why the manufacturer stays (no own board yet).** The team revisited building JVL's own board off an **STM** (STMicroelectronics — Val called it "британская", Genadi "Швейцарская") evaluation board vs the current **Rockchip** ("рок чип … китайская компания") ARM board. STM sells only an **evaluation board + schematics** (no ready-to-buy production board — you build your own on that base) with real **support** you can query; Rockchip-type boards ship "тысячами миллионами" for media boxes. A self-built single board (collapse the interface board onto one board) is a **~3-month project at best**, and only if STM has a chip supporting two screens (unknown). JVL cannot wait — it must **put a machine on a location** soon — so it **stays with the Chinese/Rockchip board for now**; an own-board evolution is deferred and, if ever done, "лучше делать через них." Val stressed proper **support** is worth overpaying for ("я бы переплатил бы деньги за правильный support").
- **SD-card route dropped for now.** Genadi's close: "**Не сесть декарт, а с usb. Но обновлять не всю не линокс, а только … вел софтвер**" — update over USB (not SD card), Linux untouched, JVL software only. Val agreed: "вот вот вот вариант я бы пошёл."

## Open commitments

- [ ] Genadi Peari — get from the Chinese manufacturer the **full deliverables**: complete documentation of the original delivery, the full **file structure / repository (sources)**, and a prepared **initial image** that already boots, supports **two monitors** correctly, and works from an SD card — everything except the USB upgrade — talking to them that night — [[raw/Requirements_ARM_board_manufacturer-november-5-2025.md]]
- [ ] Evgeniy Alekseev — once the sources arrive, do the three steps: verify a rebuildable working Linux with all programs; add needed utilities (Java, browser, other packages); rework the eMMC partitions + write the boot-time USB-update script — [[raw/Requirements_ARM_board_manufacturer-november-5-2025.md]]
- [ ] Val Levitan — have this transcript turned into a clean technical requirements document and send JVL's requirements to the Chinese manufacturer — [[raw/Requirements_ARM_board_manufacturer-november-5-2025.md]]

**§15.8:** no named-person compensation appears — only vendor economics (the manufacturer's ~$1,000 ask) and hardware/manufacturing requirements. Nothing held.

**Same-name note:** the "Евгений" throughout is [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (embedded/board work on Genadi's project; Val names "Алексеев" explicitly at the close), per the §4 registry. "Дима Пикулев" is named once as another reliable single-subcontractor — queued, not yet a page.

## Sources

- [[raw/Requirements_ARM_board_manufacturer-november-5-2025.md]]
</content>
</invoke>
