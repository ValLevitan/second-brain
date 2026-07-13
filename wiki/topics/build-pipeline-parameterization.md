---
type: topic
title: Build pipeline and ISO parameterization
date: 2026-07-12
aliases: [build pipeline, ISO parameterization, Jenkins debate, devops pipeline]
source-count: 1
---

# Build pipeline and ISO parameterization

An ongoing JVL engineering debate about how to build the game "ISO image" in a flexible way — letting a user pick which games, library versions, LGS/Math versions, etc. go into a build. It is the recurring sticking point (item "2.3") carried over from a December 20 2024 meeting into the Jan 13 2025 call.

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

## Status

- Unresolved as of Jan 13; the team was "still stuck on 2.3." Homework assigned: Sasha (with the QA team, i.e. Irina's third-party team) to define which parameters QA actually needs; Aaron asked for research into GitHub capabilities that give Jenkins-equivalent flexibility. A decision meeting was set for Jan 15 at 8am Eastern. [[raw/development_pipeline_january_13_2025.md]]

## Sources

- [[raw/development_pipeline_january_13_2025.md]]
