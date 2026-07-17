---
type: decision
title: Adopt a cheap ARM-based embedded-Linux board (Rockchip RK) for Flex Tower / Flex POS / TITO server
date: 2025-05-26
aliases: [ARM board, Rockchip, RK3568, RK board, ARM Linux platform, embedded Linux board, industrial ARM board, LVDS adapter]
source-count: 2
status: active
---

# Adopt a cheap ARM-based embedded-Linux board (Rockchip RK) for Flex Tower / Flex POS / TITO server

On the May 26 2025 hardware-selection call ([[wiki/meetings/2025-05-26-hardware-selection-arm-flex-tower-pos.md]]), [[wiki/people/val-levitan.md|Val]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]] resolved the tech-stack question that had been left open on May 20/21 ([[wiki/meetings/2025-05-21-tech-stack-flex-pos-tower-tito.md]]) — **embedded STM32 vs industrial-PC Linux** for the Flex payout devices. Part of the FlexPay evolution arc — see [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## The dilemma this resolves

The May-20/21 choice was between a cheap embedded **STM32** "sandwich" (~$30, but needing scarce low-level C programmers and hard to develop) and an **industrial-PC Linux board** (flexible/browser-friendly but "**в три раза дороже**" ≈ 3× the price, ~$130). [[raw/selection_tech_stack_hardware-flex-pos_flex-tower_flex-tito-may-21-2025.md]] A weekend investigation found a **third path** that gives Linux flexibility at nearly the STM price: Val — "**направление, мне кажется, для нас, по-моему, это то, что мы искали**" ("this is the direction we were looking for") and "**Очень хороший вариант. Очень. Я даже не думал в эту сторону**" (very good option, I hadn't even thought this way). [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]

## What was decided

- **Platform: an ARM-based, fully embedded Linux board** (a **Rockchip RK-series** SoC — the "**линейка RK … 30, 31, 28, 33, 28, 35**"; a quad-core "**68-й, четырёхъядерный**" [≈ RK3568] cited), described as **~10× more powerful than STM** and a long-lived, widely-used product line (media players / TV-boxes / POS). It is **off-the-shelf**; samples available immediately. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **Everything is onboard/embedded:** built-in **2 GB RAM + 16 GB storage (eMMC/flash)**, watchdog timer, battery, several USB, **two full RS-232 serial ports** (a dispenser can connect directly), **two I2C interfaces** (already provisioned for touchscreens / can drive two screens), Ethernet/network, **12 V** power, plus **4 GPIO** signals (and ~3 ADC pins) and extra **UARTs** reconfigurable to GPIO. **~$60 ±$1** — only "**чуть-чуть дороже**" than the ~$30 STM. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **Software: Linux (Ubuntu) or Android**, programmable in any normal-computer language — **C, Java or JavaScript** — so **any JVL programmer** can work on it (not just low-level C specialists); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] and the other Linux developers can be harnessed, shipping the products faster. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **One board for all three devices** — **Flex Tower, Flex POS, and the standalone (TITO) server** (the server would keep its logs on a cheap **swappable external SD card**, ~$6–8, so a dying card can just be replaced). [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **Firm sub-ruling — no extra I/O boards.** JVL will **not** add any additional I/O devices/boards (no "IO-борт"); the 2–3 sensors a POS/Tower needs (door sensor, dispenser sensor) are wired straight to the board's **GPIO pins or UART**. Val: this must be "**точно решить**" (definitely decided). [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]

## The one piece of work that makes it cheap

- The cheap industrial touchscreens use an **LVDS** interface, so JVL builds a **simple adapter board** (like the one already in FlexPort) to connect the screen, and [[wiki/people/evgeniy-alekseev.md|Alekseev]] writes the **LVDS video interface** for Linux (a "довольно-таки небольшая работа," ~2 days). If that interface is **not** built, a controller adds **~$20**. JVL will also make providing the display driver a **condition of sale** with the board vendor (their software engineers can supply it). Net device penalty vs STM is therefore only **~$20 "all together,"** far below the May-21 industrial-Linux delta of ~$100–200. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]

## Execution / open items before final sign-off

- **Talk to [[wiki/people/evgeniy-alekseev.md|Alekseev]] first**, then **order samples** (they "cost pennies"); order the matching **LCD + touchscreen with the correct LVDS interface**. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **[[wiki/people/pavel.md|Pavel]] to size memory** — 16 GB storage is already enough; check whether **2 GB or 4 GB RAM** is needed by reading current memory utilisation on the FlexBay device (custom 64 GB / 4 GB variants are available, e.g. on AliExpress, at ~the same price). [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- **Power** still to be worked out (Tower needs 24 V for the dispenser + 12 V for the board; POS just 12 V). [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]

## Status

Active as of 2025-05-26. This is the chosen direction (resolving the May-20/21 deferral); Val wanted to **close it at a 7 am meeting the next day** once Alekseev confirms the LVDS interface and the samples are validated ("надо проверить, запустить, посмотреть, как она надёжно работает"). Recorded as ruled with that validation contingency, not re-deferred. [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]

## Sources

- [[raw/hardware_selection_flex-tower_flex-pos-may-26-2025.md]]
- [[raw/selection_tech_stack_hardware-flex-pos_flex-tower_flex-tito-may-21-2025.md]]
