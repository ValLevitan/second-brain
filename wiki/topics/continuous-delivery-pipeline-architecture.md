---
type: topic
title: Continuous-delivery pipeline architecture (three-layer, Git-native)
date: 2025-01-21
aliases: [continuous delivery, continuous deployment, CD pipeline, CI/CD architecture, three-layer repos, product environment platform, Hello World pipeline, integrator repo]
source-count: 1
---

# Continuous-delivery pipeline architecture (three-layer, Git-native)

The architecture Aaron and the QA consultant Jason walked Val through on Jan 21 2025 for how JVL should build and deploy its software once it moves off Jenkins onto a Git-native pipeline. Val's stated aim for the meeting was to reach the simplest possible, MVP-first picture he (a non-engineer) could understand and give as an order. See the broader pipeline debate in [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Val's framing: two separate efforts

Val insisted the discussion split into two things that had been blurring together, so he could reason about each on its own: [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

1. **Continuous integration / delivery** — the pipeline that builds the product and deploys it.
2. **A standalone test tool** — a self-contained testing application JVL's QA (or GLI) could use. See [[wiki/topics/test-automation-strategy.md]].

Val asked for the standalone tool to be drawn and framed separately, saying he had assumed it was part of the pipeline until told otherwise. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## The three-layer "everything as code" model

Aaron's core point: everything — not just the product — is written as code in its own Git repository, so nothing is ever hand-built. He named four repository types: [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

- **Product** — the executable/compiled code (game, framework, RGS, math). What JVL has today.
- **Environment** — the set of system libraries, dependencies and OS configuration needed to *run* the product (e.g. Node, Java, DLLs). Aaron's example: cloning this repo and running one script configures a machine, instead of following a README by hand.
- **Platform** — the compute infrastructure the environment runs on: which OS, what virtual hardware, how the network is routed. Defined as code (Terraform / infrastructure-as-code). Aaron refused to fix it to Linux, wanting it kept "amorphous" (could be Linux, Windows, or serverless).
- **Integrator** — the script/system that packages everything together into an independent, runnable product (the installer is one piece of the integrator).

Aaron argued each of these layers has its *own* tests, so "at all times, all things are testable." Configuration-as-code and infrastructure-as-code were called out as distinct but blurry-bordered pieces. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Containers over disk images

Aaron pushed containers (Docker) over shipping OS disk/ISO images ("disk images deployed to an OS is so 2007"), including running containers *inside* the EGM, and said he had been shoving the dev team to consider it. Jason's near-term pragmatic take: for the EGM, which has only a small number of configurations, a Docker container with some deploy scripts and a manual build step may be enough to start. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## The testing pyramid

The testing layers, base to top: **unit → component → integration → end-to-end**, with JVL's **ITL/GLI-type** tests at the very top. Unit tests run inside the feature branch before it is merged back to main; integration and end-to-end tests need the built system deployed to an environment first, so they can't run per-commit as easily. Val's mental model (integration testing is a precondition of pulling a feature into main) was accepted at a high level. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## The standalone test tool — three essential blocks

Anton described the MVP of the standalone tool as three blocks: **test management** (store/organise test cases), **test authoring** (build test cases without writing scripts, or with them), and a **test runner** (run the cases against a freshly deployed environment and produce results). A later step would upload results back to X-Ray / Jira. Val asked that the very first test be the **math test**, since GLI told JVL math-checking is where GLI spends most of its time (see [[wiki/topics/gli-certification-bottleneck.md]]). [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

Jason argued a proper test tool (he named Tosca / SmartBear, and a record-and-playback "WYSIWYG" wizard) is needed so a non-coding tester can author test steps; he warned that letting anyone write raw Cucumber/BDD "turns into cucumber goo." Aaron's summary framing: **"it's not a tool, it's a solution — a series of tools"** executed in the right stages (his furniture analogy: no single tool builds a chair). Val remained reluctant to spend on tooling. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## MVP sequencing (what Val ordered)

Val drove the group to a first step (recorded as a decision — see [[wiki/decisions/2025-01-21-build-git-native-hello-world-environment-first.md]]): [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

- Build the three pipelines to deploy a trivial **"Hello World"** onto a development environment — estimated ~**1 week** to reach Hello World (the rest of the maturity is "the rest of the year").
- Start with the **Omni framework** plus **LGS** (local gaming server) as the first real product to port.
- Then incrementally move the existing "monolithic" Omni code into the product / environment / platform repositories (Aaron's "same bricks, different wall" — no rewrite of the code itself).

## Portability out of Minsk

Val was emphatic that the pipeline and test environment must **not** be physically entrenched in Minsk ("Minsk is as volatile as anything else… I'm pulling a lot of controls out of Minsk"). Aaron/Jason agreed it can run as cloud infrastructure (Bitbucket runners, AWS elastic compute, Azure), on the EGM, on a developer workstation, or via **GitHub Codespaces** (a fully virtualized dev environment in the browser — flagged as the big value proposition). JVL was confirmed to be moving toward GitHub, with Andrei doing the work. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Staffing the setup

- Use a **Russian-speaking DevOps engineer** — the one who previously set up Kubernetes and handed it to Andrei — to do the initial setup *first*, rather than Aaron's engineer **Nathan** (a capable DevOps engineer but non-Russian-speaking); Aaron's reason was change-management and communication, so the rest of the team can follow along. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- **Alexander (Sasha)** must define the environments for LGS / progressive controllers (only he can); **Anton** can do the Omni framework; **Igor Bitewski** for progressive; **Efim** for the math engine (deferred to last). See [[wiki/people/alexander-biratka.md]] and [[wiki/people/anton-leshkevich.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Aaron demoed that AI (Claude / Anthropic under the hood) can rapidly scaffold the Terraform, Docker file and even the tests for a Hello-World deployment — a way to reach the first result in about a day given system access. See [[wiki/topics/ai-assisted-development.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Sources

- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
