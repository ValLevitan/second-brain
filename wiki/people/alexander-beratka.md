---
type: person
title: Alexander Beratka
date: 2026-07-12
aliases: [Alexander Beratka, Alexander, Sasha, Sasha Beratka]
source-count: 3
---

# Alexander Beratka

Alexander Beratka (called "Sasha") is a JVL engineer, part of the Minsk engineering team. He runs hardware/performance tests and works on the build pipeline.

## Role

- Ran the FP7 sample CPU board performance tests: fed simultaneous HD videos through the board and reduced the count until he found a "tolerable" threshold (about 20 FPS), landing on 7 simultaneous HD videos plus 2 half-screens on V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- He checked RAM and memory during the test and reported nothing was overloaded; he profiled the board only by visual control (watching it). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- On the build-pipeline call, Sasha explained the ISO-image parameterization problem: Bitbucket cannot build a flexible UI for choosing game/library versions before a build launches. He proposed generating a JSON config from a Jenkins-style UI, pushing it to the repo, then triggering the Bitbucket pipeline. [[raw/development_pipeline_january_13_2025.md]]
- He took the homework (with the QA team) to define which parameters QA needs when building the final ISO. [[raw/development_pipeline_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop as a participant; Aaron suggested Sasha try the AI tools on the Omni framework or LGS codebase. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

Note: the transcripts also use "Sasha" as a short form and once the garble "Pasha" appears near his name; "Pasha" is treated as Pavel elsewhere. See [[wiki/people/pavel.md]].

## Sources

- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
