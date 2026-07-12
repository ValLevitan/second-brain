---
type: topic
title: Build pipeline & ISO parameterization
date: 2025-01-13
aliases: [build pipeline, ISO parameterization, DevOps pipeline]
source-count: 1
---

# Build pipeline & ISO parameterization

The unresolved engineering question of how JVL builds its game ISO images flexibly, and the debate over the tools to do it.

## The problem

QA needs to build an ISO image by choosing versions of the parts that go into it (games, LGS, math, progressives). Neither Bitbucket pipelines nor GitHub Actions can present those choices before a build starts — you have to run the build to discover the available versions, which creates a chicken-and-egg loop [[raw/development_pipeline_january_13_2025.md]].

## Two camps

- **Jenkins as a parameter manager** — the engineers' comfortable option: use a Jenkins UI to gather parameters into a config file, then trigger the Bitbucket/GitHub build [[raw/development_pipeline_january_13_2025.md]].
- **Git-native, no Jenkins** — Aaron's push: keep the build coupled to the code in Git so it's portable, clean, traceable, automatable, and (crucially) ready for AI/natural-language tooling. He wants QA embedded in the Git workflow rather than driving a separate control panel [[raw/development_pipeline_january_13_2025.md]].

## Related progress

- Docker containerization of game modules is considered feasible (tested ~a year ago for math/RNG); LGS moved Java 8 → 17; Bitbucket pipeline for Omni games set up [[raw/development_pipeline_january_13_2025.md]].

## Status

- **Unresolved** as of 2025-01-13. Homework assigned; decision to be made at the follow-up on Wednesday 2025-01-15. QA (third-party team under Irina) to be consulted on which parameters they actually need [[raw/development_pipeline_january_13_2025.md]].

## Sources

- [[raw/development_pipeline_january_13_2025.md]]
