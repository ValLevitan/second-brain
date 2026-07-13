---
type: decision
title: Remain on FP7 hardware; optimize rather than upgrade (2025-01-17)
date: 2025-01-17
aliases: [FP7 it is, FP7 hardware ceiling, stay on FP7]
source-count: 1
status: active
open-commitments: 3
open-questions: 1
---

# Remain on FP7 hardware; optimize rather than upgrade (2025-01-17)

**Decision:** After the deeper bottleneck testing, Val ruled that JVL will not move to any hardware beyond FP7 for its low/mid-grade products — "the verdict is we're not going to move to anything else. FP7 it is." The team will optimize (video formats, reduce to 3 HD screens, shift load to spine animation) rather than chase a more powerful platform, which mobile power/heat limits rule out anyway. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

**Decided by:** Val, with Pavel, Alexander, Gennady, Dima Khandov and Aaron. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Rationale

- Testing showed the bottleneck is the **CPU** (video decoding), not the GPU: the embedded GPU ran at ~50% while performance dropped as soon as the number of simultaneous videos exceeded the number of CPU cores. Sasha saw the same behaviour on a PC with a powerful discrete Radeon (6650 XT) card, confirming the GPU is not the limit. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- A more powerful mobile CPU (e.g. Ryzen 9 vs Ryzen 7) would give only a modest gain (similar cache, higher clock), and desktop CPUs are off-limits (~100W power/heat). So there is little room to grow by swapping the CPU. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- The real product needs only ~3 HD (1920×1080) screens, not 4K; dropping from 4 to 3 screens plus normal game-time optimization makes FP7 "still doable." The current test hit 8 videos at ~60 FPS — twice Lena's minimum. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## What still moves forward

- Gennady will ship an FP7 board with the **8000-series processor and four video outputs** by ~March 1 (samples promised after Chinese New Year). This confirms/extends [[wiki/decisions/2025-01-13-adopt-fp7-for-flex-s-fortune-fu-paws.md]]. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- A written **asset "manifest"** (how graphic designers must build video/spine assets for FP7) will be produced by Dima Khandov. See [[wiki/topics/fp7-hardware-platform.md]]. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Open commitments

- [ ] Dima Khandov — write a complete asset-creation manifest (video, spine, etc.) for the FP7 platform, tested with Sasha — due Feb 15 2025 — [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [ ] Gennady Perry — ship an FP7 board with the 8000 processor and four video outputs — due ~March 1 2025 — [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [ ] Pavel Frolov — check whether a better Linux driver can optimize the FP7 platform; with Sasha, revisit the Omni architecture to define which components (e.g. Pixi) need continuous updates and how they pass through GLI — due by the next meeting (Jan 31) — [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Open questions

- The exact cause of the CPU limit (video-decode scheduling / memory bandwidth) is understood well enough to proceed, but a rigorous measurement method ("company philosophy on how to properly measure things") is still lacking — Val wants more science, less "finger in the wind." [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## Sources

- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
