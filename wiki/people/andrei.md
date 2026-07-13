---
type: person
title: Andrei
date: 2026-07-12
aliases: [Andrei, Andrey]
source-count: 4
---

# Andrei

Andrei (also spelled "Andrey") is a JVL engineer on the Minsk team who works on build infrastructure and deployment.

## Role

- On the build-pipeline call, Andrei had checked that GitHub Actions is about the same as Bitbucket pipelines — a little more flexible, but still lacking the parameterization capabilities JVL wants. He suggested a Jenkins-style approach to fill in parameters and create a project file for another job. [[raw/development_pipeline_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop. He had distributed the OpenRouter API keys to Anton, Sasha, Pasha and himself, and Aaron noted Andrei may have build scripts / pipeline work pushing things out to Kubernetes. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- Andrei agreed with the Git-native direction ("I agree with Pavel"). He is the cost-conscious voice on the platform choice: he flagged GitHub as more expensive than Bitbucket and gave the (internally inconsistent) per-user price figures. He also raised that Jenkins runs as a self-hosted service (deployable to cloud/Kubernetes/Docker but not a ready-made SaaS). See [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]]. [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

His last name is not stated.

## Sources

- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
