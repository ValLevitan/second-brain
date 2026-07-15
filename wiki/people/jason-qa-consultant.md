---
type: person
title: Jason (QA / test-automation consultant)
date: 2025-01-15
aliases: [Jason, Jason Welco, test automation consultant, QA consultant]
source-count: 4
open-commitments: 0
open-questions: 0
---

# Jason (QA / test-automation consultant)

An outside QA / test-automation consultant Val engaged to design a testing approach for JVL. He is distinct from Aaron — he says he worked on his proposal "in consultation with Aaron" and discussed it with Aaron the prior week. He appears to be US-based (his background looked "like Arizona" and he once described a cold trip to Toronto). [[raw/integration_and_testing_procedures_january_15_2025.md]]

His full name is recorded as **Jason Welco** on the Jan 21 continuous-delivery call transcript (earlier only "Mr. Jason" appeared; still worth confirming the spelling). [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Role

- Presenting a checkpoint of a test-automation proposal to Val, explicitly checking his "definition of done" against Val's business goals before going further. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Advocates shift-left testing: define test cases (BDD) at or before the time features/stories are built, and test individual components in isolation (simulating/mocking the APIs around them) rather than only "big-bang" full integration testing. [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Walked Val through the categories of test tooling: test-case management (X-Ray, which JVL already uses), API testing (no commercial tool yet), UI testing (e.g. Selenium as the open-source option), and adjacent quality tools such as static analysis and software composition analysis (named Synopsys / "Black Duck"). [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Frames the work as a journey done in phases, advising JVL to "start small," and warns that delaying builds up "technical debt." [[raw/integration_and_testing_procedures_january_15_2025.md]]
- Works with the JVL engineers — he was looking at API-testing tools together with Anton, and proposed the next step be a testing-architecture meeting with Pavel, Irina, Anton and Aaron. [[raw/integration_and_testing_procedures_january_15_2025.md]]

See [[wiki/topics/test-automation-strategy.md]].

## Continuous-delivery architecture call (Jan 21)

- Presented (with Aaron) the end-to-end continuous-delivery picture to Val, sharing a Miro diagram he had prepared; argued the pipeline can run in several places (Bitbucket, cloud, EGM) and that JVL will want more than one target over time. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Strongly advocated buying a real test tool (named **Tosca / SmartBear**, and a record-and-playback "WYSIWYG" wizard) so non-coding testers can author test steps, rather than relying on raw Cucumber/BDD; Val was reluctant to spend on tooling. He warned delaying testing builds up "technical debt." [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Referenced on the DevOps-container session (Mar 24 2025, date inferred)

- Val recounted telling Jason the next stage of the requirements work: "я когда разговаривал с Джейсоном, я сказал, на следующем этапе давайте мы возьмем самую advanced игру и reverse engineer эту игру в requirements" — take the most advanced game and reverse-engineer it into hard, "atomic binary" requirements to feed the asset-validation tool. Aaron also referenced the test-automation harness work "Jason has been talking about." See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/devops_container_approach_for_omni.md]] [[raw/devops_container_approach_for_omni_3.md]]

## Sources

- [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
