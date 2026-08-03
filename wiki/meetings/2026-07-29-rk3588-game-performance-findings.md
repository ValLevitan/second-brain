---
type: meeting
title: RK3588 game-performance findings (Nova/Caliente on Rockchip)
date: 2026-07-29
aliases: [Findings from RK3588, RK3588 findings, Nova game on RK3588]
source-count: 2
---

# RK3588 game-performance findings (Nova/Caliente on Rockchip)

**July 29, 2026, 7:00 AM ET** (recording header 7:03–7:19 AM). Present: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratko]], [[wiki/people/irina-shishko.md|Irina Shishko]].

Pavel reported the results of testing a NOVA-platform game (**Caliente**) on the Rockchip **RK3588** board — the ARM-platform performance check assigned to the student developer Daniil on Jul-17. The base game runs smoothly at ~60 FPS; the only stutter is on bonus/free-spin transitions and is a memory shortage on the 4 GB test board. The team resolved to order a **16 GB RK3588** board with uniform HDMI outputs.

Substance recorded on:
- [[wiki/topics/nova-platform-architecture.md]] — the Nova game runs well on the RK3588 (ARM/Rockchip); confirms the browser-based platform carries the games (discharges the Jul-17 Daniil ARM-check commitment).
- [[wiki/topics/low-cost-street-machine.md]] — the measured answer to the compute-platform memory-sizing question (16 GB for 8 games; 4 GB causes bonus-game stutter; RK3588 confirmed as the top board over RK3568/RK3576/RK3399).

Builds on the [[wiki/decisions/2025-05-26-arm-linux-platform-flex-devices.md|May-26 2025 ARM/Linux platform decision]].

## Sources
- [[raw/Meeting_Notes_RK3588_Game_Performance_Findings-July-29-2026.md]]
- [[raw/Meeting_Transcript_RK3588_Game_Performance_Findings-July-29-2026.md]]
