---
type: person
title: Alexander Biratka
date: 2026-07-12
aliases: [Alexander Biratka, Alexander, Sasha, Sasha Biratka, Alexander Beratka, Sasha Beratka, Alex]
source-count: 8
open-commitments: 1
open-questions: 0
---

# Alexander Biratka

Alexander Biratka (called "Sasha") is a JVL engineer, part of the Minsk engineering team. He runs hardware/performance tests and works on the build pipeline.

## Role

- Ran the FP7 sample CPU board performance tests: fed simultaneous HD videos through the board and reduced the count until he found a "tolerable" threshold (about 20 FPS), landing on 7 simultaneous HD videos plus 2 half-screens on V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- He checked RAM and memory during the test and reported nothing was overloaded; he profiled the board only by visual control (watching it). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- On the build-pipeline call, Sasha explained the ISO-image parameterization problem: Bitbucket cannot build a flexible UI for choosing game/library versions before a build launches. He proposed generating a JSON config from a Jenkins-style UI, pushing it to the repo, then triggering the Bitbucket pipeline. [[raw/development_pipeline_january_13_2025.md]]
- He took the homework (with the QA team) to define which parameters QA needs when building the final ISO. [[raw/development_pipeline_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop as a participant; Aaron suggested Sasha try the AI tools on the Omni framework or LGS codebase. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- Sasha wrote a small script that generates a build-config file and creates an "envelope," demonstrating the Git-native approach. He agreed with the simplification ("I like any simple solutions") but asked not to hard-cap the number of build variants — add more only if needed. He also proposed the pragmatic fallback of re-attaching Jenkins on top to generate the config if all else fails. See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]]. [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## FP7 video testing and Pixi upgrade (Jan 16–17)

- On the Jan 16 game-design review, Sasha (with a colleague noted as "Emma") tried a new video format that improved FP7 performance slightly. [[raw/game_design_january_16_2025.md]]
- On the Jan 17 bottleneck testing, Sasha ran the video-stream tests, found VP9 best in Chromium and VP8 in Firefox, and reproduced the same limit on his own PC with a powerful Radeon 6650 XT — showing the bottleneck is the CPU, not the GPU. He proposed upgrading to the new Pixi engine version, and is to do that upgrade (~a week). See [[wiki/decisions/2025-01-17-upgrade-omni-to-pixi-8-6.md]]. The transcript credits "Beratka" with coining the term **"manifest"** for the asset-creation guideline. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## GitHub repo structure (Feb 11)

- On the Feb 11 org-structure session Sasha ("Alex") argued for shorter names in the URL and, for sorting/filtering, suggested the "JVL" tag belong at the **end** of org names (Aaron/Val kept it at the front). He asked to keep repo/org names readable and confirmed the naming standard. See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## Open commitments

- [ ] Sasha (Alexander Biratka) — write a real build-config file (game, framework, LGS, hardware abstraction layer), put it in Git, and set up a job that produces an image/archive (not a full ISO yet) — due by the next meeting (Monday) — [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

Note: the correct surname is **Biratka** (confirmed by Val). The transcripts spell it inconsistently — mostly "Beratka", once "Biratka" — so both forms are kept as aliases for search. The transcripts also use "Sasha" as a short form, and once the garble "Pasha" appears near his name; "Pasha" is treated as Pavel elsewhere. See [[wiki/people/pavel.md]].

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
