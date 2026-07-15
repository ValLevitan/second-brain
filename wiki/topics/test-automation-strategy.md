---
type: topic
title: Test-automation strategy and testing architecture
date: 2025-01-15
aliases: [test automation, testing architecture, QA automation, shift-left testing, proof of concept testing, Catalon Studio, end-to-end testing, standalone test tool, Tosca, Test 360, test 360 culture, unit-test coverage, TDD]
source-count: 4
open-commitments: 2
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

## Test types clarified (Jan 20 philosophy discussion)

Val questioned a JVL technical colleague (speaker identity unclear) to pin down what "automation testing" actually means. The distinctions drawn: [[raw/test_automation_philosophy-jan-20-2025.md]]

- **Unit tests** — test small pieces of code, written by developers, run automatically on each commit (CI/CD); isolated to one repository. No QA or GLI involvement. Merging two feature-branches within one repo (e.g. LGS) just runs both sets of unit tests — no integration build needed if you only work within LGS.
- **Integration / end-to-end tests** — test the whole assembled system; require an extra step: deploy the built system somewhere (server or local) and run tests against that deployment. This is what the colleague calls "GLI-type" testing. Hard to run per-commit because you must build and deploy the whole JVL/EGM architecture.
- Each repository (LGS, a game, RGS) has its own **trunk** (main branch); features are feature-branches merged into their own repo's trunk. [[raw/test_automation_philosophy-jan-20-2025.md]]

### GLI as the testing "customer"

- The colleague deliberately treats **GLI** as the client for the cleanest test system (higher bar than JVL's own QA). The plan: give GLI a set of tests (e.g. against the GLI-11 specification) that they run on each JVL change; if they pass, GLI can skip re-testing that area. Test harnesses / "test-enablers" would be built into the game/EGM and enabled only in debug builds (e.g. an `enable test harness` flag). [[raw/test_automation_philosophy-jan-20-2025.md]]
- GLI says most of their time goes to **checking the math**; they mainly take **screenshots** and verify with internal tools, and are not very forthcoming with details. JVL's idea: build a tool/harness that generates predefined outcomes per paytable and produces screenshots for GLI — GLI was lukewarm, wanting to keep part of the check on their own tools. Both Val and the colleague found it hard to pin down exactly what GLI wants. [[raw/test_automation_philosophy-jan-20-2025.md]]

### Low-code test tooling

- **Catalon Studio** — a low-code test-case IDE (evolved from the free "Test Project", now freemium) that lets non-programmers assemble test cases from readable steps while still allowing scripting. Test cases and reusable "building blocks" (e.g. imported LGS APIs like `setTilt`/`removeTilt`) are stored in Git. It integrates with Jira. Presented as one example among similar paid tools. [[raw/test_automation_philosophy-jan-20-2025.md]]
- A tool called **Tasker** was demoed to Jason and the colleague; the vendor said many manual (non-coding) testers use it. [[raw/test_automation_philosophy-jan-20-2025.md]]
- **Prior work reference:** Lyuba Volodko previously wrote tests using **Selenium** (a Java library) against a deployed CMS environment — the same kind of thing Catalon abstracts. (Single mention; no page yet — see Owner Decisions.) [[raw/test_automation_philosophy-jan-20-2025.md]]
- Aim over time: a **library of building blocks** from which non-programmer testers assemble test cases, with harder cases written directly in code. [[raw/test_automation_philosophy-jan-20-2025.md]]

## The standalone test tool (Jan 21)

On the Jan 21 continuous-delivery call, Val asked for the QA/GLI test tool to be treated as a separate effort from the CD pipeline. The MVP of the tool, as Anton described it, is three blocks: [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

- **Test management** — store and organise test cases.
- **Test authoring** — build test cases without scripting (or with it).
- **Test runner** — run the cases against a freshly deployed environment and produce results; later upload results back to X-Ray / Jira.

Val asked that the **math test** be the first test built, since GLI spends most of its time checking math (see [[wiki/topics/gli-certification-bottleneck.md]]). Jason argued for buying a real test tool (named **Tosca / SmartBear**, and a record-and-playback "WYSIWYG" wizard) so non-coding testers can author steps, warning that raw Cucumber/BDD "turns into goo"; Aaron reframed it as **"not a tool but a solution — a series of tools"** used in the right stages. The testing pyramid (unit → component → integration → end-to-end, with ITL/GLI on top) and where each layer runs is detailed on [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. Val stayed reluctant to spend on tooling. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Open commitments

- [ ] Val — set up a ~2-hour testing-architecture meeting with Pavel, Irina, Anton and Aaron — due next week (of Jan 15) — [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [ ] Val + the technical colleague — follow-up working session (~8:00–8:30am, to be confirmed) to figure out how to proceed on test automation; Val wants Aaron's help — due next morning (~Jan 21) — [[raw/test_automation_philosophy-jan-20-2025.md]]

## Open questions

- Whether JVL's game framework and engine actually expose internal APIs that warrant contract/API testing — the consultant says they do; Val says he is unaware of any. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## History

### The "Test 360" origin review (Fri Jul 5 2024 — date inferred; pre-dates the v1 window, Tier A-queued)

The earliest captured root of this effort — a Bitbucket-era progress review between Val, [[wiki/people/aaron.md|Aaron]] and [[wiki/people/anton-leshkevich.md|Anton]] (stub with the dating evidence: [[wiki/meetings/2024-07-05-test-360-progress-review.md]]). Val coined the name on this call: "I'm deliberately going to call it, I'm adopting the name **test 360 culture**, because I think it resonates now between the three of us." [[raw/test-360_progress_review_meeting.md]]

- **TDD teaching:** Aaron demonstrated test-driven development live — a **Gherkin** spec for fizzbuzz ("Gherkin is probably not a good thing, but…"), then a **JUnit** parameterized test, then ChatGPT-generated JavaScript that passes it — tests before code; example domain offered: **SAS**-protocol unit tests independent of implementation language. His claim: TDD has no real overhead because "I often write tests first… it helps you think through the issues." Anton confirmed: "We have successfully applied this approach in our **RGS** codebase" — new RGS code is expected to come covered with unit tests. [[raw/test-360_progress_review_meeting.md]]
- **State of the old code:** the P1000 platform has no tests ("it's just a historical artifact"); the online/Omni-predecessor code grew "super controllers"; Aaron: "**single responsibility** is probably the number one thing that I'm not seeing at JBL right now" (Val logged SOLID as a subject to study). Val's own inference: "this is probably subconsciously what I understood **when I fired my CTO** — … by accepting mediocrity of agreeing not covering something with unit tests." Monolith imagery settled on "spaghetti code." [[raw/test-360_progress_review_meeting.md]]
- **Anton's status then:** test environment set up and "approximately **9%**" of the Omni Engine code covered with unit tests, using the **Jest** framework (assertions and mocking), refactoring utility classes as he went (deleting never-executed code found via the coverage report); estimate to cover the existing code: "between **30 to 60 calendar days**." He wrote the first testing **requirements** (every merge triggers CI/CD; automated testing integrated into the pipeline; every code change linked to a ticket — Val's edit: say "ticket or work item," never codify Jira/Atlassian into a requirement) and emailed them plus Confluence docs to developers for votes/comments; he removed all old features from "test 360 for OmniFramework IP" ("**Initiative for product**") and created new unit-test/CI-CD ones. [[raw/test-360_progress_review_meeting.md]]
- **Rules added on the call:** Aaron — a feature branch must be **time-limited** ("if you let it hang out longer than the story… it should not be valid to bring back in… you are in jeopardy of damaging everybody else's efforts"); Val asked for a dashboard of branch ages (Bitbucket can show it). [[raw/test-360_progress_review_meeting.md]]
- **Plan around Alexander:** [[wiki/people/alexander-biratka.md|Alexander Biratka]] "won't be available until August" for Omni; Val's target — by mid-August, 100% of the existing Omni code covered at the 80% rate and reviewed/refactored by Anton **in collaboration with Alex Biratka** (Anton consults him before refactoring non-obvious code), so that when Alexander returns to advancing OmniFramework, Anton grooms alongside and starts writing the actual Test-360 modules. Aaron's poker-card estimate: real code coverage "will take **more than a year**." [[raw/test-360_progress_review_meeting.md]]
- **Measurement & scope questions Aaron posed:** define what "coverage" even means (function coverage of unit tests vs test coverage of requirements — or both), per-language tooling differences, and scope = **OmniFramework first** ("it should turn into the exemplary piece of code"); the old code base probably out of scope. Tooling: Aaron showed **SonarQube** (commercial code-introspection platform, "adopted by industry leaders"); Val wanted to "spec it as a tool of choice"; Aaron resisted premature adoption ("the organization isn't configured to even receive it yet" — same fate as his earlier OpenAPI suggestion). [[raw/test-360_progress_review_meeting.md]]
- **People risk:** Val worried [[wiki/people/irina-makarych.md|Irina]] must rule the process "with an iron fist"; his read — she will **adopt** what Alexander and Anton establish without opining, and nobody will challenge it "especially if we're going to get Yefim on site." Aaron's worry was understanding ("can we make sure that people understand why we do it this way"), not compliance. (Aaron's reading gift: **howtodeal.dev** — "12 types of underappreciated software developers.") [[raw/test-360_progress_review_meeting.md]]
- Next step then: Anton to draw the block architectural diagram of the flow (Bitbucket, IDEs, unit tests, plug-in modules like SonarQube) "today," review booked for the following Wednesday (the 10th) at 8 a.m. Eastern, one hour — Val: cap these reviews at ~an hour ("it's a little bit overwhelming for me to sit through these meetings for two hours"). (Outcomes of these 2024 commitments aren't visible in later sources; they are superseded by the Jan-2025 arc above, so recorded here rather than as open checkboxes.) [[raw/test-360_progress_review_meeting.md]]

## Sources

- [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [[raw/test_automation_philosophy-jan-20-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/test-360_progress_review_meeting.md]]
