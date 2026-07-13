---
type: decision
title: Move JVL's build system off Jenkins to a Git-native pipeline
date: 2025-01-15
aliases: [Git-native build, serverless build, drop Jenkins]
source-count: 4
status: active
open-commitments: 0
open-questions: 0
---

# Move JVL's build system off Jenkins to a Git-native pipeline (2025-01-15)

**Decision:** JVL will move away from a Jenkins master-build menu system and rebuild its game-build pipeline on a Git-native, "serverless" platform (GitHub Actions / pipelines), with a small collection of official builds. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

**Decided by:** Val, after explicitly asking each engineer (Pavel, Sasha, Anton, Andrei) to agree with gravity; all agreed. Aaron drove the proposal. [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## What was decided

- Each module (game, framework, engine, LGS, hardware abstraction layer) is built **separately**; the final ISO image mostly **reuses binary artifacts**, with the option to build a module from source. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- The **build config file lives in Git**, so any build can be rebuilt later exactly as it was, with new parameters if needed (e.g. rebuild a shipped production build as a debug build to investigate). This is Pavel's key requirement and is easier under the new approach than in Jenkins. [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- Rationale for dropping Jenkins: Jenkins is always a server instance bound to a named host; a Git-native pipeline is portable across Git platforms, lightweight, and "risk-resistant." A cloud-hosted Jenkins would still be server-instance-based, so it does not solve the problem. [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- Compatibility between modules (e.g. which game runs with which LGS/framework version) is to be described via **manifests** declaring minimum supported dependent versions and product family (e.g. DLK games cannot run with HIT games); validated ideally by input validation and/or a test on the built ISO, not by an exhaustive version matrix (builds take ~40 minutes). [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- Fallback if the Git-native approach fails: Jenkins can still be re-attached on top to generate the config (raised half-jokingly by Sasha). [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]

## Trade-off accepted

- The new approach favours simplicity over infinite flexibility: rare, unusual build-parameter combinations will require a programmer instead of a checkbox. The team agreed such cases are rare and that simplicity is worth it. See [[wiki/decisions/2025-01-15-reduce-build-variants-with-post-build-instrumentation.md]]. [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]

This resolves the debate left open on Jan 13. See [[wiki/topics/build-pipeline-parameterization.md]]. Related platform choice: [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]].

## Sources

- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
