---
type: decision
title: Proceed with the FP7 hardware for Flex-S / Fortune Fu Paws on Omni
date: 2025-01-13
aliases: [FP7 decision, FR7 decision]
source-count: 1
status: active
---

# Proceed with the FP7 hardware for Flex-S / Fortune Fu Paws on Omni

## What was decided

After reviewing performance tests of the FP7 (FR7) CPU board, JVL decided the board is good enough to move forward with — especially for the Flex-S cabinet — running the Omni platform, provided the games stay within the measured video limits [[raw/fp-7_performance_analysis_january_13_2025.md]].

## Key points

- **Measured limit:** at a "tolerable" ~20 FPS the board runs 7 simultaneous HD videos plus 2 half-screens (VDec). 13 videos choked it to ~5 FPS [[raw/fp-7_performance_analysis_january_13_2025.md]].
- **Lena's team** continues developing **Fortune Fu Paws** under those video thresholds, using "spine" animation objects to offload work from video where possible [[raw/fp-7_performance_analysis_january_13_2025.md]].
- **Gennady Perry** to ship two samples of the higher Ryzen **8000-series** board (~20% faster) to Minsk and two to Canada; kept as an option, not a dependency [[raw/fp-7_performance_analysis_january_13_2025.md]].
- **Pavel + Alexander** to run further tests to find the bottleneck; follow-up meeting set for Friday [[raw/fp-7_performance_analysis_january_13_2025.md]].
- **Plan B (not yet decided):** move progressive signage onto standalone/isolated hardware, especially for the larger Flex-C [[raw/fp-7_performance_analysis_january_13_2025.md]].

## Dependency

- Depends on resolving the build-pipeline issues discussed the same morning — see [[wiki/topics/build-pipeline-parameterization.md]].

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
