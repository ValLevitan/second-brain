---
type: topic
title: Build pipeline and ISO parameterization
date: 2026-07-12
aliases: [build pipeline, ISO parameterization, Jenkins debate, devops pipeline, DTP-53, DTP 53]
source-count: 8
open-commitments: 2
open-questions: 1
---

# Build pipeline and ISO parameterization

An ongoing JVL engineering debate about how to build the game "ISO image" in a flexible way — letting a user pick which games, library versions, LGS/Math versions, etc. go into a build. It is the recurring sticking point (item "2.3") carried over from a December 20 2024 meeting into the Jan 13 2025 call.

> The Jan 21 2025 continuous-delivery call took this further into a full pipeline architecture — the three-layer "everything as code" model (product / environment / platform repos plus an integrator) and the "Hello World first" MVP step. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]] and [[wiki/decisions/2025-01-21-build-git-native-hello-world-environment-first.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## The core problem

- JVL wants to flexibly build an ISO image by choosing versions of its parts (games, progressives, LGS, Math, etc.) before the build starts. [[raw/development_pipeline_january_13_2025.md]]
- Neither Bitbucket pipelines nor GitHub Actions can present that choice cleanly *before* a build: the parts are stored in the repo, but you have to launch the build to list them — a "closed loop." [[raw/development_pipeline_january_13_2025.md]]
- Aaron noted GitHub Actions is a little more flexible than Bitbucket but still short of what JVL wants. [[raw/development_pipeline_january_13_2025.md]]

## The two competing approaches

- **Use Jenkins** (the Minsk team's comfort zone): use a Jenkins UI as a parameter-management tool to configure the build, then hand it to Bitbucket to assemble the final ISO. Sasha and Andrei favored a variant: a Jenkins-style UI generates a JSON config, pushes it to the repo, and that push triggers the Bitbucket pipeline. [[raw/development_pipeline_january_13_2025.md]]
- **Stay Git-native** (Aaron's push): avoid a separate Jenkins system; keep the build coupled to the code in Git so that everything is portable, automatable, clean, and traceable. Aaron's stated goals: pipeline portability (move between Bitbucket / GitHub / GitLab), automation of all options (Jira or even an AI could kick off a build), disposable/rebuildable clean build environments, and fully traceable changes (no one reaching behind the build server to change things). [[raw/development_pipeline_january_13_2025.md]]

## Aaron's deeper point

- He challenged whether the complexity is real or inherited: is the parameterization need driven by ~20 years of legacy architecture, or a genuine requirement? [[raw/development_pipeline_january_13_2025.md]]
- He wants QA embedded with the build system — QA should branch a copy (e.g. a big YAML file of parameters), configure and test against it, then close the branch — rather than being handed a Jenkins "control panel" that limits them. He argued QA engineers should be able to run basic Git commands. [[raw/development_pipeline_january_13_2025.md]]
- He tied it to AI: a Git-native pipeline lets AI tools drive builds naturally, whereas Jenkins forces screen-scraping a web page. See [[wiki/topics/ai-assisted-development.md]]. [[raw/development_pipeline_january_13_2025.md]]

## Resolution (Jan 15 decision meeting)

The Jan 15 decision meeting settled the debate in favour of the Git-native approach and simplification. Three decisions came out of it: [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

- **Move off Jenkins to a Git-native, serverless build system** — modules built separately, ISO reuses binary artifacts, config file stored in Git. See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]]. [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- **Standardise on GitHub over Bitbucket** and migrate repositories (phased; LFS support to re-verify; ~8 seats to buy). See [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Reduce the many build parameters to ~four archetypes** and move instrumentation to a post-build step. See [[wiki/decisions/2025-01-15-reduce-build-variants-with-post-build-instrumentation.md]]. [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]

A key insight from the meeting: JVL's sprawling Jenkins build parameters had effectively become an ad-hoc **test panel** — QA was using build-parameter toggles to test the software. Simplifying builds is meant to push that work into proper automated tests. See [[wiki/topics/test-automation-strategy.md]]. [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]

The work is to be tracked as JIRA features on the engineering board (under "IP-767 production services" / the DTP DevOps project), treated as a high-ranking backlog item in a two-week sprint rather than an ad-hoc side project. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## DTP-53 feature (the Git-native pipeline as a JIRA feature)

The build-system work is now tracked as JIRA feature **DTP-53** (under "DevOps tools and processes"), the follow-through on the Jan 15 commitment to break the work into features. Two planning sessions, Aaron coaching Pavel: [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]] [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]

- **Jan 16 (planning):** DTP-53's business value is to switch from Jenkins to a Git-native pipeline — improving build reliability, reducing overhead, enabling better test automation, and reducing build complexity. Pavel's first insight was that there are **several separate pipelines** (each model gets its own simple pipeline with minor parameters); Aaron, playing "Scrum Master," treated "several pipelines" as the first stories and had Pavel list them on a Miro board. [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]]
- **Jan 17 (feature definition):** Aaron pushed Pavel to write **features from the customer's perspective**, not user stories from his own — a feature must describe capabilities, customer, purpose and business value so another engineer can build it. Named pipeline modules: an **installer pipeline** (top layer, builds installable USB/ISO images from OS + application + config), **long-term artifact storage** (secure storage with metadata, access control, retention/purge, and integration — treated as an architectural design, not just a JIRA issue), and **GitHub configuration**. Aaron demoed using Claude with "explanatory" and "intellectual dissector" prompt styles to draft and critique the feature, but warned against over-reliance on AI ("regular old brains" first). Guidance: keep features **traceable and documented in Git** (markdown docs in the repo, JIRA reference in commits) so they evolve with the feature over years. [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]

## Open commitments

- [ ] Aaron (with Pavel) — break the build-system work out into JIRA features on the board and rank it in the sprint backlog — due unspecified — [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]] (in progress: now tracked as JIRA feature DTP-53 [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]])
- [ ] Pavel — rewrite the DTP-53 pipeline modules as proper feature descriptions (reverse-engineer the existing user stories back into features), documented Git-natively — due Wednesday (~Jan 22), reviewed at a team meeting Aaron will set for 9am — [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]

(Two more build commitments from this meeting are tracked on their owners' pages: Sasha's build-config file [[wiki/people/alexander-biratka.md]] and Pavel's module image files [[wiki/people/pavel.md]].)

## Open questions

- The final set of build archetypes and which legacy build directives to keep vs. retire is not yet settled. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Status

- Jan 13: unresolved; the team was "still stuck on 2.3." Homework assigned: Sasha (with the QA team) to define which parameters QA actually needs; Aaron to research GitHub capabilities matching Jenkins. A decision meeting was set for Jan 15 at 8am Eastern. [[raw/development_pipeline_january_13_2025.md]]
- Jan 15: **resolved** — Git-native + GitHub + archetype builds chosen (see Resolution above). [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Sources

- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_2_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_3_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]]
- [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
