---
type: topic
title: FP7 hardware platform
date: 2026-07-12
aliases: [FP7, FR7, FG7, FP-7]
source-count: 1
---

# FP7 hardware platform

FP7 is a JVL CPU-board hardware platform being evaluated for the Flex-S cabinet, running the Omni platform. The Jan 13 2025 meeting tested whether it is powerful enough for the games JVL wants to ship. (The transcript spells it FP7, FR7 and FG7 interchangeably — treated as one platform.)

## What FP7 is

- A CPU-board platform built around an AMD Ryzen APU on a given socket. The first sample used the "sweet spot" 6800 APU from the 6000-series Ryzen (best price-to-performance, not the most powerful). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- JVL's main supplier for these boards is "Batang." The same socket also takes an 8000-series Ryzen for roughly 20% more performance at modest extra cost. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Intended mainly for the Flex-S cabinet (street operation); JVL's plan is to develop a stronger Flex-C for casino use later. See [[wiki/topics/jvl-machine-lineup.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## The performance test (Jan 13)

- A sample board was sent from China to Minsk. Dmitry Khandov built a test scene of 13 simultaneous HD (1920×1080) videos; Alexander Biratka fed them through the board, which nearly choked at about 5 FPS. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Reducing the video count found a "tolerable" threshold (about 20 FPS) at 7 simultaneous HD videos plus 2 half-screens on V-Deck. Val and Lena agree 20 FPS is not satisfactory but is the working ceiling for now. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Videos were in VP8/VP9 format (chosen because they support alpha transparency); OS was standard Linux with no special drivers; profiling was by visual observation only (no deep instrumentation). RAM and memory bandwidth were not the bottleneck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- "Spine" objects (skeletal animation) ran smoothly even when videos dropped frames — so shifting effects from video to spine animation reduces load, at the cost of extra design effort to synchronize the two. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Conclusion and open items

- Consensus: FP7 is workable for the Fortune Fu Paws game and the Flex-S / Omni platform, but only "with a lot of effort for optimization." See [[wiki/decisions/2025-01-13-adopt-fp7-for-flex-s-fortune-fu-paws.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Undertakings: Gennady Perry to ship 8000-processor samples (two to Minsk, ~two to Canada; ~30 days to Minsk); Pavel and Alexander to run further tests with a measurement tool to locate the true bottleneck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Aaron raised (but Val deferred) whether a Thunderbolt-connected external GPU could offload video rendering — Val called it the wrong question for now. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Plan B floated by Lena: if performance falls short once the game is built, move signage/progressive off this hardware onto a standalone controller. Val leans toward standalone progressive hardware but did not lock it as architecture. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
