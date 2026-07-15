---
type: topic
title: Puerto Rico product configuration
date: 2026-07-14
aliases: [Puerto Rico product line, PR product matrix, product configuration matrix, ARC-2000, V43, D27]
source-count: 3
open-questions: 1
---

# Puerto Rico product configuration

Which JVL hardware/software combinations ship into the Puerto Rico route market, worked out on a Mar 21 2025 call ([[wiki/people/val-levitan.md|Val]], **Irina**, [[wiki/people/pavel.md|Pavel]], [[wiki/people/genadi-peari.md|Genadi Peari]]) that summarized an earlier, more confused discussion — that earlier discussion is the ≈Mar 19 touch-fix/product-line meeting ([[wiki/meetings/2025-03-19-puerto-rico-touch-fix-and-product-line.md]]), where the config-table action and the Friday 10:30 "Product line for Puerto Rico" follow-up were set. A follow-up requirements document (AI-generated from the call) captures the same decisions formally. This is the product/hardware detail under the broader [[wiki/projects/puerto-rico-expansion.md]] project. [[raw/products_puerto_rico_touch_fix.md]] [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

("Irina" who led the table is not clearly resolved — possibly [[wiki/people/irina-makarych.md]], possibly another Irina; flagged in Owner Decisions.)

## Val's Puerto Rico pricing/marketing philosophy (≈Mar 19 2025)

The commercial logic behind the three product families — "три прослойки цен" (three price layers), stated by Val on the pre-meeting: [[raw/products_puerto_rico_touch_fix.md]]

1. **New Flex machines (D27 / V43) at ~$11,500** — the $15,000 list is "очень дорого" (too expensive) for Puerto Rico; with discounts buyers can get near **$10,500**. The trick: **remove the VDEC and fit 8 mechanical buttons** — buttons and VDEC "стоят более-менее одинаково" (cost about the same), so it's a **marketing device** that makes the machine *look* cheaper while carrying the newest games (Megahit-era) operated via buttons. No topper for Puerto Rico. [[raw/products_puerto_rico_touch_fix.md]]
2. **Refurbished machines at ~$5,000** — used machines pulled from the market, fully reconditioned ("вылизали и отполировали") with a company warranty, running their native software. [[raw/products_puerto_rico_touch_fix.md]]
3. **CPU kits at ~$3,500–4,000** — for the customer who wants to build his own: **HG6 games** (deliberately a step below the new machines — "Я не хочу чтобы они сказали, что CPU kit это вот как новая машина"), a natural electronics step-down, button-only (no VDEC support). Kit games are frozen — "Эти игры развиваться не будут"; buyers wanting evolving games must buy the VDEC product. [[raw/products_puerto_rico_touch_fix.md]]

Regulatory frame per Val: Puerto Rico is a "loose jurisdiction … очень слабо описано" but requires **SAS**, GLI-style compliance, and a bill acceptor; JVL ships **no printer** in these machines. The 8-button decision was settled here ("мы Apple, Altera V и Altera Retrofit, мы идем на 8 кнопочную" — one button layout across kits, retrofit and Flex-PR), retrofits keep all old electronics except a new counter board (supporting up to 8 buttons), and vertical HG6 titles (e.g. "Los Cuatro Grandes," transcribed "Loss Quattro Krantos") go to Altera V — needing per-product rework since cabinet support lived only in the HitGames branch (old SVN). The action to build the cabinet/software/game correspondence table ("пару дней" — with "Ира") produced the Mar-21 matrix above. [[raw/products_puerto_rico_touch_fix.md]]

**ioboard firmware for submissions (same call):** versions **4.10** and **4.11** both fix the "ioboard not found" tilt; 4.10 is the USB-protocol-compliant fix, 4.11 the simplified always-enabled variant recommended by [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] after Pavel found one motherboard where 4.10's detection failed ("Дима" rebuilt and retested the version — which Dima is unresolved, queued). Decision: verify update-over-4.11 works, run it on a couple more machines, then release 4.11 and include it in the new submissions. [[raw/products_puerto_rico_touch_fix.md]]

## The three product families

- **HG6 CPU kits** — get *new* electronics: new board and new counter board. [[raw/product_matrix_puerto_rico-march21-2025.md]]
- **HG6 retrofit machines** — keep the *old* board and old counter board; only the cabinet is changed. [[raw/product_matrix_puerto_rico-march21-2025.md]]
- **Flex-S machines** — run the **V1000** platform board, with **Megahit** software; split into two cabinet models: **V43** (vertical) and **D27** (horizontal). [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

Val's earlier clarification that had caused confusion: for Flex in Puerto Rico, JVL installs a **full V1000 board (not a cabinet kit)** with Megahit, so the product can grow. The five Puerto Rico machines already on production are to have their cabinet removed, a V1000 installed, and then wait for news. [[raw/product_matrix_puerto_rico-march21-2025.md]]

## Key technical points

- **One software, two button panels (the main resolution):** rather than maintaining separate builds, JVL will rework the **HG6** software so a single **XML configuration** file maps the key codes of *both* the legacy (old counter-board) panel and the new panel, so one software supports retrofit and kit machines without manual selection (which Val feared would cause errors). Genadi offered to make the wiring/mapping identical instead, but that would mean firmware changes; the software/XML route was preferred. See [[wiki/decisions/2025-03-21-hg6-support-legacy-and-new-button-panels.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]
- **Megahit on Flex with physical buttons is unproven:** it worked on Georgia but may need framework rework to handle all key codes; Megahit cannot fit an HG6 cabinet (more screens than it supports) but could run in a **two-monitor** configuration with rework. On Flex, machines register with a passport, so Megahit must recognise fewer monitors / reduced touchscreens per Puerto Rico's regulatory registration. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]
- **CPU boards:** retrofit machines and kits use the **cabinet board**; Flex-S uses the **V1000** platform. All machines use an **IMG file** (transcribed "EMG"), not an ISO. [[raw/product_matrix_puerto_rico-march21-2025.md]]
- **ARC-2000 (cheaper board) — deferred:** Genadi raised a lower-cost alternative — the **V1000 board on an ARC-2000** low-power mobile platform, ~**$130**, fully compatible but weaker — and asked whether it could go everywhere. Val deferred the question as non-critical, asking only that the board be named correctly for the record. See [[wiki/topics/jvl-machine-lineup.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## Approvals and certification

- **[[wiki/people/juan-martinez.md|Juan Martinez]] holds final approval** on the button-panel design (for the Altera V and Maple cabinets), the game selection, and the game-setup limitations for the Puerto Rico market. At the time of the call Juan was in Puerto Rico walking locations to look at exactly these things; expected back that day or Saturday. Harness may need to be ordered (a lead-time item once the machines start arriving). [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]
- **GLI certification** is required for every product/hardware-software combination before deployment in Puerto Rico. Val expects to get it but calls the requirement vague. See [[wiki/organizations/gli.md]]. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## The product matrix (as specified on the call)

The team agreed a table with columns **CPU kits / HG6 retrofit machines / Flex-S machines** (Flex-S split into V43 and D27), and rows for: panel-or-VDEC configuration, CPU board, software package (HG6 / Megahit), and which games run on vertical vs horizontal screens. Val had the requirements document generated by AI from the transcript rather than filled in by hand. [[raw/product_matrix_puerto_rico-march21-2025.md]] [[raw/requirements_puerto_rico-march-21-2025.md]]

## Open questions

- Whether Megahit on Flex will run correctly with physical buttons (and reduced monitors) without significant framework rework — unresolved on the call. [[raw/product_matrix_puerto_rico-march21-2025.md]]

## Sources

- [[raw/product_matrix_puerto_rico-march21-2025.md]]
- [[raw/requirements_puerto_rico-march-21-2025.md]]
- [[raw/products_puerto_rico_touch_fix.md]]
