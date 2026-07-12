---
type: topic
title: FP7 (FR7) hardware platform
date: 2025-01-13
aliases: [FP7, FR7, FP7 board, FR7 board]
source-count: 1
---

# FP7 (FR7) hardware platform

The CPU/motherboard platform JVL is standardizing on for its machines, especially the Flex-S cabinet, running the Omni platform.

## What it is

- A CPU board sampled from China and tested in Minsk. The test unit used a **6800 APU (Ryzen 6000 series)**, chosen for price/performance [[raw/fp-7_performance_analysis_january_13_2025.md]].
- Main board supplier is referred to as "Batang" (name unclear in transcript) [[raw/fp-7_performance_analysis_january_13_2025.md]].

## Performance findings (January 2025)

- Runs Linux; videos in VP8/VP9 full HD (1920×1080); CPU (not dedicated GPU) doing the rendering [[raw/fp-7_performance_analysis_january_13_2025.md]].
- 13 simultaneous HD videos → ~5 FPS (choked). ~20 FPS ("tolerable") reached at **7 HD videos + 2 half-screens** [[raw/fp-7_performance_analysis_january_13_2025.md]].
- "Spine" animation objects run smoothly and can offload work from video [[raw/fp-7_performance_analysis_january_13_2025.md]].

## Upgrade path

- A **Ryzen 8000-series** board (~20% faster, small cost increase) is being developed, expected available end of February 2025 — held as an option [[raw/fp-7_performance_analysis_january_13_2025.md]].

Decision using this: [[wiki/decisions/2025-01-13-proceed-with-fp7-for-fortune-fu-paws.md]].

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
