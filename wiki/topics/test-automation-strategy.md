---
type: topic
title: Test-automation strategy and testing architecture
date: 2025-01-15
aliases: [test automation, testing architecture, QA automation, shift-left testing, proof of concept testing]
source-count: 1
open-commitments: 1
open-questions: 1
---

# Test-automation strategy and testing architecture

JVL's effort to modernise how it tests its games — moving toward automated, component-level testing. Val engaged an outside QA/test-automation consultant ([[wiki/people/jason-qa-consultant.md|Jason]]) who is preparing a proposal; this page synthesises the Jan 15 2025 checkpoint conversation between Val and the consultant. It is closely tied to the build-pipeline changes decided the same day. See [[wiki/topics/build-pipeline-parameterization.md]].

## The two business goals (confirmed by Val)

Val confirmed these are the two goals / pain points the project must serve: [[raw/integration_and_testing_procedures_january_15_2025.md]]

1. **Increase speed to release a new game** from inception to production (and to GLI approval).
2. **Unambiguously define the acceptance criteria** for a product feature.

Val declined to add more goals or more wording, wanting the objective kept tight. The consultant noted a common third goal — being able to **scale QA/development sub-linearly with revenue** (grow R&D headcount slower than revenue) — but Val had not raised it, so it was left out. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Scope: a narrow proof of concept, not a broad quality program

- Val wants a **narrow-focus proof of concept** that testing speed can be improved "cradle to grave," not a broad quality project. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Focus is the EGM (the gaming machine), which has a fairly small, static set of cabinet/printer configurations to test — unlike general IT software deployed to many environments. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## The technical approach

- **Shift left:** define test cases (BDD) at or before the time features/stories are built, so the same requirement is interpreted the same way by developer and tester. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- **Test components in isolation, not only big-bang integration.** Today JVL tests all components smushed together; the consultant argues each component should be testable on its own by simulating (mocking) the APIs of the components around it, with full integration testing reserved for the whole feature on the cabinet. Val's mental model matched this at a high level (test at the point a story/feature is pulled into a branch), though Val disputed that JVL's framework and engine even have internal APIs to test. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- This connects to the build-pipeline decisions: the consultant observed that JVL's many Jenkins build parameters had effectively become an ad-hoc test panel, and moving to smaller, cleaner builds supports proper unit/component testing. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Tooling categories discussed

- **Test-case management:** X-Ray — already in place at JVL and usable for the proof of concept. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- **API testing:** JVL has no commercial tool for this yet; the consultant and Anton were evaluating options. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- **UI testing:** e.g. Selenium (open-source); used to drive the machine's configuration/meters web UI in test cases. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- **Adjacent quality tools:** static analysis (originated with "Lint") and software composition analysis (SCA) — named Synopsys, now "Black Duck" — flag risky code and vulnerable/licensing-problematic open-source dependencies. Noted as expensive (the consultant's former employer spent close to $1M/year on static analysis). [[raw/integration_and_testing_procedures_january_15_2025.md]]

## ROI framing

- Val gave the consultant a QA engineer's annual cost of **$36,000** as an input to the ROI analysis; the pitch is framed as slowing headcount growth (never as cutting headcount). [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Decisions and next step

- Val decided JVL will **not buy any testing tool this year**. See [[wiki/decisions/2025-01-15-defer-test-tool-purchases.md]]. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Val wants to "nail the architecture of testing" (both technical and process) first, via a dedicated ~2-hour meeting with Pavel, Irina, Anton and Aaron. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Open commitments

- [ ] Val — set up a ~2-hour testing-architecture meeting with Pavel, Irina, Anton and Aaron — due next week (of Jan 15) — [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Open questions

- Whether JVL's game framework and engine actually expose internal APIs that warrant contract/API testing — the consultant says they do; Val says he is unaware of any. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Sources

- [[raw/integration_and_testing_procedures_january_15_2025.md]]
