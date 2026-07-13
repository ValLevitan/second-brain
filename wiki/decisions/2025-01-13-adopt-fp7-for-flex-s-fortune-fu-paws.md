---
type: decision
title: Adopt FP7 hardware for Flex-S / Fortune Fu Paws on the Omni platform
date: 2025-01-13
aliases: [adopt FP7, FP7 decision]
source-count: 1
status: active
---

# Adopt FP7 hardware for Flex-S / Fortune Fu Paws on the Omni platform

## What was decided

JVL will move forward with the FP7 CPU board, especially for the Flex-S cabinet, and implement the Omni platform on it. The Fortune Fu Paws game will be developed on this hardware. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Who and when

- Decided by [[wiki/people/val-levitan.md|Val]] at the Jan 13 2025 FP7 performance review, with agreement from the design side ([[wiki/people/lena.md|Lena]], [[wiki/people/dmitriy-khandov.md|Dmitry Khandov]]) and hardware ([[wiki/people/genadi-peari.md|Genadi Peari]]). [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Rationale

- Testing showed FP7 is workable for Fortune Fu Paws "but with a lot of effort for optimization" — combining spine animation with video to stay under the video-count performance threshold. Both Lena and Dima judged it doable. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Conditioned on resolving the build-pipeline / Omni issues discussed the same morning, which Val expected to resolve one way or another. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/fp-7_performance_analysis_january_13_2025.md]]

## Guidance and undertakings attached

- Lena's team develops Fortune Fu Paws under the current performance limits (staying under the established video-count threshold). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Genadi Peari to ship 8000-processor board samples (two to Minsk, ~two to Canada) as a performance upgrade path (~20% more power). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- Pavel and Alexander to run further tests with a measurement tool to locate the bottleneck; follow-up hardware meeting set for that Friday. [[raw/fp-7_performance_analysis_january_13_2025.md]]

See [[wiki/topics/fp7-hardware-platform.md]].

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
