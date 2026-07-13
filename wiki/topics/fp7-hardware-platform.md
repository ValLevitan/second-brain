---
type: topic
title: FP7 hardware platform
date: 2026-07-12
aliases: [FP7, FR7, FG7, FP-7]
source-count: 3
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

## Jan 16 check-in (game-design review)

- Lena reported the tests show FP7 "will work" for the Fortune Football games. [[raw/game_design_january_16_2025.md]]
- Sasha and a colleague ("Emma" — name unclear in transcript) tried a **new video format** that gave a little better performance. [[raw/game_design_january_16_2025.md]]
- Gennady's AMD 8000-series processor (same socket) is expected to add 20%+ performance; the regular China supplier will have the standard 8000-socket product in February. [[raw/game_design_january_16_2025.md]]
- Lena's idea to revert to a separate/**autonomous signage controller** (treat the machine as effectively three screens, and lighten the V-Deck) was liked by Val, Gennady and Pavel — both to cut power draw and because locations/gaming-control people prefer a separate controller. Not yet locked as architecture. [[raw/game_design_january_16_2025.md]]

## Jan 17 bottleneck testing (deeper investigation)

- Pavel and Alexander found **no useful under-the-hood metrics tool**, so they measured by increasing the number of simultaneous video streams until FPS dropped. **VP9** was more effective in Chromium, **VP8** in Firefox. With **8 Full HD videos** they held ~60 FPS; adding a 9th dropped FPS immediately. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- **The bottleneck is the CPU (video decoding), not the GPU.** The embedded GPU ran at ~50%; performance fell once the video count exceeded the CPU core count. Sasha reproduced the same behaviour on a PC with a powerful discrete Radeon 6650 XT, confirming the GPU is not the limit. Turning off hardware acceleration gave 0 FPS, so hardware decode is in use. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- A more powerful mobile CPU (Ryzen 9 vs Ryzen 7) would give only a modest gain (same L3 cache, higher clock); desktop CPUs are ruled out on power/heat. So the practical path is optimization, not a bigger CPU. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- Decode is done by a dedicated hardware decoder module (loosely tied to the iGPU in the AMD architecture) and Linux, not the CPU cores directly; VP8/VP9 remain the working codecs (chosen for alpha support). Optimization levers discussed: fewer/lower-res screens (3 HD, not 4K), lower bitrate/color depth, WebM/MP4 containers, using spine "sequences" for short animations to avoid decoding, and not rendering full-screen when unnecessary. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- **Outcome:** stay on FP7 and optimize (see [[wiki/decisions/2025-01-17-remain-on-fp7-hardware-ceiling.md]]); upgrade the engine to Pixi 8.6 (see [[wiki/decisions/2025-01-17-upgrade-omni-to-pixi-8-6.md]]); Dima Khandov to write an **asset "manifest"** (the word Beratka coined) telling designers how to build assets for FP7; Gennady to ship an 8000-processor FP7 board with four video outputs by ~March 1. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Conclusion and open items (Jan 13)

- Consensus: FP7 is workable for the Fortune Fu Paws game and the Flex-S / Omni platform, but only "with a lot of effort for optimization." See [[wiki/decisions/2025-01-13-adopt-fp7-for-flex-s-fortune-fu-paws.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Undertakings: Genadi Peari to ship 8000-processor samples (two to Minsk, ~two to Canada; ~30 days to Minsk); Pavel and Alexander to run further tests with a measurement tool to locate the true bottleneck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Aaron raised (but Val deferred) whether a Thunderbolt-connected external GPU could offload video rendering — Val called it the wrong question for now. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Plan B floated by Lena: if performance falls short once the game is built, move signage/progressive off this hardware onto a standalone controller. Val leans toward standalone progressive hardware but did not lock it as architecture. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
