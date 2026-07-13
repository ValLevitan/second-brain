---
type: decision
title: Build the Git-native "Hello World" environment first (MVP step 1)
date: 2025-01-21
aliases: [Hello World first, CD MVP step 1, three-pipeline environment first]
source-count: 1
status: active
---

# Build the Git-native "Hello World" environment first (MVP step 1)

## What was decided

Val ruled — explicitly "treat it as an order" — that the first, MVP step of JVL's move to a Git-native continuous-delivery pipeline is to build the three "everything-as-code" pipelines (product, environment, platform repositories) and get a trivial **"Hello World"** deployed onto a development environment, before doing anything more elaborate. He kept the effort deliberately separate from the standalone QA/GLI test tool. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Scope of step 1

- Deliverable: the three pipelines produce a "Hello World" that runs on a deployed environment (a mock unit test asserting "Hello World"). Estimated ~**1 week** to reach this. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- First product to port afterward: the **Omni framework** + **LGS**; then move the existing monolithic Omni code into the product / environment / platform repos without rewriting the code itself. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Do **not** buy or design a large architecture up front; Val explicitly favoured MVP and "another revision" over over-design ("a large architecture will bury us"). [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Who and how

- Decided by [[wiki/people/val-levitan.md|Val]] with [[wiki/people/aaron.md|Aaron]], [[wiki/people/jason-qa-consultant.md|Jason]] and [[wiki/people/anton-leshkevich.md|Anton]] on the Jan 21 continuous-delivery architecture call. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Staffing: use the Russian-speaking DevOps engineer who set up Kubernetes (before Aaron's engineer Nathan), paired with Anton and Andrei, for the initial setup. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Why

- Val cannot act on a design he doesn't understand, and wanted the smallest thing that can be built on. Aaron: everything must be compiled from code (you can't hand-build a Jenkins/Git environment anymore); reproducibility, testability, scalability and geolocation-independence are the payoff. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Sources

- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
