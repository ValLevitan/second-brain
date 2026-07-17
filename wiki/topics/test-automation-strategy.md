---
type: topic
title: Test-automation strategy and testing architecture
date: 2025-01-15
aliases: [test automation, testing architecture, QA automation, shift-left testing, proof of concept testing, Catalon Studio, end-to-end testing, standalone test tool, Tosca, Test 360, test 360 culture, unit-test coverage, TDD, FlexPay test plan, FP-262, Page Object Model, POM, Selenium, XPath]
source-count: 13
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

## Apr 24 2025 — QA-engineer onboarding kicks off (integration tests in practice)

The test-engineer transformation ([[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md]]) reached its first working session, alongside a conceptual explainer the same day.

- **Onboarding kickoff** ([[wiki/meetings/2025-04-24-omni-integration-tests-qa-onboarding.md]]): [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] demoed the first Omni init-setup integration test — **Selenium + TypeScript on Node.js**. He chose Selenium over **Playwright** because Playwright "подразумевает использование их целого багажа инструментов" and was harder to fit into JVL's custom automation framework. Tests live **in the Git repo beside the code**; each test gets a **unique key** "reserved for future use" (hoping to integrate with **X-Ray** or another test-management tool). Local run uses a **docker of the built LGS + the LGS-UI repo** (still in Bitbucket) via `Yarn Start`; [[wiki/people/andrey-bosik.md|Andrei Bosik]] helps set up each engineer's environment. [[raw/integration_tests-apr-24-2025.md]]
- **The agreed model:** a market requirement → a product **capability** (a demonstrable set of features/branches) → per-feature integration tests; a feature branch can only merge to `main` once its integration test passes — test-driven development with QA engineers writing tests in parallel with developers ("вы имеете такой же авторитет, как имеет девелопер"). Val stressed this is **not yet "automation"** — automated regression suites come later, once many keyed tests exist and can run on every submission. Init-setup being "95-97%" done, QA practices on it first. JIRA anchors: the product is **Omni Land-Based Framework (IP 416)**; QA test development sits under **Core Tools (IP 438) → IP 105**. TypeScript-learning sources named: [[wiki/people/alexander-biratka.md|Alexander Biratko]], Anton, and an AI assistant. [[raw/integration_tests-apr-24-2025.md]]
- **Conceptual explainer** ([[wiki/meetings/2025-04-24-ci-cd-qa-org-explainer.md]]): the classic "throw it over the wall to QA" model is superseded by DevOps, where **test engineers (not testers)** write unit tests with mock-ups (e.g. JUnit) beside the functional code, then integration tests against a **continuously-deployed** service (a game vs a torn-down/rebuilt RGS) — the "continuous integration" and "continuous delivery/deployment" halves of CI/CD. [[raw/ci_cd_qa_structure-apr-24-2025.md]]

## May 14 2025 — Omni test-status reality check

The second segment of the May-14 Omni review ([[wiki/meetings/2025-05-14-omni-schedule-and-test-review.md]]), continued by [[wiki/people/val-levitan.md|Val]] with [[wiki/people/irina-makarych.md|Irina Makarych]] (and Pasha) after the schedule crew left — a candid check on where Omni testing actually stands versus the Apr-24 QA-engineer onboarding above. [[raw/omni_test_status_review-may-14-2025.md]]

- **The intended model restated:** write test tasks per **feature**; a set of features forms a **test suite**; on a **pull request into main**, integration tests should fire "in theory." [[raw/omni_test_status_review-may-14-2025.md]]
- **The practice: nothing yet.** "На практике мы пока ничего не имеем, потому что нет никаких тестов" — there are no tests and, for now, no one to write them; everyone is still **learning JavaScript** well enough to understand what a test is. [[wiki/people/anton-leshkevich.md|Anton]] (the test-engineer who wrote the Apr-24 Selenium/TypeScript setup examples — resolved by that context, inference) has created a couple of examples and a **setup base**. A **Friday meeting with Anton** is booked to **write the first test together**, walking through a UI test step-by-step so people at least understand what is written. [[raw/omni_test_status_review-may-14-2025.md]]
- **Docker mismatch:** they configured Docker for tests but it turned out **Igor set it up for himself as a developer**, while QA needs something different — a misunderstanding to sort out. [[raw/omni_test_status_review-may-14-2025.md]]
- **Val wants to attend the Friday session** (proposed shifting it from 4 → 10 or 5 their time) specifically to **gauge people's reactions** — whether they ask questions or stare blankly — "приобрести какое-то чувство реальности" (acquire a sense of reality). Irina noted Anton would move the meeting and add Val. [[raw/omni_test_status_review-may-14-2025.md]]

## May 16 2025 — QA test-implementation kickoff (everyone writes tests, integration-first)

The Friday-before follow-through to the May-14 reality check: a working session ([[wiki/meetings/2025-05-16-qa-test-implementation-kickoff.md]]; Russian) getting the QA engineers actually writing tests against the live Omni init-setup work. [[raw/qa_test_implementation-may-16-2025.md]]

- **Three test areas restated:** UI, Backend, and games — UI is the most demonstrative/simplest and where [[wiki/people/anton-leshkevich.md|Anton]] just demoed; Backend is Vlad's area (a **v0.1** of a test framework with an **API for tilts** already implemented, more LGS APIs added as scenarios need them); games are "still dark," last. [[raw/qa_test_implementation-may-16-2025.md]]
- **Val's two organizational asks:** (1) **everyone present except Pavel should start writing code** now — even primitive/broken — as the best way to learn, with Anton helping on the harder bits; (2) each QA engineer **talks daily with a developer** and writes tests **in parallel with (even slightly ahead of) the feature** being built, so tests aren't written against a feature developed in a vacuum. Meetings every 2–3 days, ~1 hour. [[raw/qa_test_implementation-may-16-2025.md]]
- **Integration tests first:** because a feature is pulled into `main` once done, it must not merge **without an integration test** — ideally developer + tester work the feature together and the passing test gates the pull request. Concrete first target: the **multi-language init-setup** feature — a test that the language switches on all available tabs. [[raw/qa_test_implementation-may-16-2025.md]]
- **Where to run tests (unresolved):** everyone wanted tests to run on a **real machine**, not a fake pass/fail; the setup ("init setup") isn't stable on the machine yet (it can fall over on connect). Interim: write/run **locally** now against what's available (e.g. English-language check), then point the same test at a real machine later by changing the IP/entry point — "the test functionality should be preserved." [[raw/qa_test_implementation-may-16-2025.md]]
- **Language work cast:** the multi-language commits are done by **Igor** (rendered "Игорь Макаров" — by the localization context this is the LGS-630 init-setup localization owner, i.e. [[wiki/people/ihar-hrybko.md|Igor Hrybko]]; surname transcription uncertain, Tier B) together with **Anton**. Val urged using **dictation + AI** to draft use-cases/descriptions in plain language, and looking for documented examples (Atlassian, YouTube) rather than guessing — referencing that **Anton and [[wiki/people/jason-qa-consultant.md|Jason]]** had earlier surveyed testing applications. [[raw/qa_test_implementation-may-16-2025.md]]
- **Action-plan discipline:** one of the engineers (not Val) must voice the objectives + a numbered action plan for the Wednesday check-in — for **everyone**, regardless of whose feature is ready, so all get into the acceptance-criteria / use-case / write-the-code mindset. Cap meetings at 45 min, keep Monday + Wednesday cadence. [[raw/qa_test_implementation-may-16-2025.md]]

## May 19 2025 — the QA-into-main argument (no Dev branch)

On the May-19 branch-structure review ([[wiki/meetings/2025-05-19-github-branch-structure-debate.md]]; Russian) Val used the **git branch model as leverage for the QA transformation**. The branch mechanics are on [[wiki/topics/graphics-team-git-workflow.md]]; the QA-culture point: [[raw/github_branch_structure-may-19-2025.md]]

- Val's argument for **main-only (no Dev branch):** a Dev branch tells the QA engineers "you can't do it anyway, we're not counting on you." He would instead **apply pressure** — merge feature branches straight into `main`, require a test, and help them write it — because JVL's QA engineers (**Ivan, Vlad, Alexey**, mentored by [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], the one who can already write tests) have *accepted the challenge* to learn to program properly in **TypeScript** and become "fully qualified QA-engineers." A Dev branch **discourages** exactly that. [[raw/github_branch_structure-may-19-2025.md]]
- **Bug fixes as test changes, not bug tickets:** Val would rather a missed bug become a **task to fix the test** (the test should have caught it) than a standalone bug branch — a test made a bug possible because the test was incompletely specified. Pavel pushed back (bugs arise for many reasons — version incompatibility, scope-gaps). Left as an ongoing disagreement, not resolved. [[raw/github_branch_structure-may-19-2025.md]]

## May 20 2025 — FlexPay/FlexPort test-plan strategy ("one philosophy" argument)

A Russian test-strategy meeting ([[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md]]) between [[wiki/people/val-levitan.md|Val]], QA lead [[wiki/people/irina-makarych.md|Irina Makarych]] ("Ира"), [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/evgeniy-alekseev.md|Alekseev]] on how to test the FlexPay/FlexPort system. The transcript internally duplicates (§12, facts taken once); no decision was locked — Val chose to step back and reconsider, and to schedule a follow-up. [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]

- **Test the system, not the parts in isolation.** Irina and Pavel argued (and Val agreed) that FlexPay and FlexPort **don't work standalone** — testing must cover the whole chain (FlexPay + FlexPort + machine), with plans for a **test jig/bench** for FlexPort (a special tool plus a test program Val asked Alekseev to write). [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- **The Jira test-plan structure debate.** The existing **Flex Payments (FP) project Test Plan (FP-262)** described **both configurations — Temporary Wallet and TITO — in one plan.** Val pushed to **simplify**: split into **two separate test plans** (one per scheme), describing the two configurations only at the higher **initiative** level, because a plan spanning both huge architectures is unmanageable. Team agreed to split. [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- **Val's "company needs a philosophy" stance.** He escalated the disagreement into a management point: a company where "you can do it this way or that way, whatever you like" is **rudderless** — "a car racing at huge speed with no steering wheel." He'd "rather fight for my philosophy than run a company where anything goes," while acknowledging the irritation was **at himself** for not conveying it, and that he was only ~75% sure he was right and open to being shown otherwise. This is a recurring Val theme (see the same-week [[wiki/meetings/2025-05-19-github-branch-structure-debate.md|branch-structure debate]]). [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- **The architecture crux (fed the [[wiki/topics/flexpay-business-architecture-payout-devices.md|payout-device thread]]):** Val's core position is that **Temporary Wallet and TITO should not coexist on one location** and were never designed to; Irina had understood from prior direction that they *could* run together — a communication gap Val took responsibility for. The QA implication: keep **one FlexPay software** that supports both schemes (developers' convenience — "1% code difference," one flash drive) but **test each scheme separately**, never a test spanning both; consider a config toggle to disable one scheme per location. (Val's broader worry — that binding TITO to the FlexPay codebase risks a repeat of the amusement→slot base they later threw away, and that FlexServer may grow into "FlexCloud" — is recorded on the payout-device page.) [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]

## May 21 2025 — test-engineering progress: first QA-written tests, POM, LGS models

A Russian working session ([[wiki/meetings/2025-05-21-test-engineering-progress.md]]; transcript internally duplicates its first half — §12, facts taken once) where the QA engineers demoed their first Selenium/web tests, chaired by [[wiki/people/val-levitan.md|Val]] with test-engineer [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] and QA engineers [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]], [[wiki/people/alexei-khamin.md|Alexei Khamin]] ("Лёша"/"Алексей Хамер") and "Vlad". The §3 continuation of the May-14/16/19 QA-transformation thread. [[raw/test_engineering_progress_report-may-21-2025.md]]

- **Val's meeting-discipline lecture.** Every meeting should start from a **written summary** ("вот это мы решили") that everyone confirms, then walk the **prior action list** to closure, and only then discuss new items — "лучше не создавать новые action list, чем забыть пройтись по старым." He models it on **Jeff Bezos**, who "circulates written notes и заставляет всех читать written notes одновременно на митинге." He asked someone other than himself to chair when he's absent, and pressed the engineers to practise voicing the action list ("это не будет Антон"). Val also described his own **knowledge-base habit** (recording meetings → Whisper transcripts → trying to load them into a database with proper tagging and **map-graph structures** that auto-link files) — the practice this second brain itself grew from (see [[wiki/topics/transcript-knowledge-base-tooling.md]]). [[raw/test_engineering_progress_report-may-21-2025.md]]
- **The four QA-transformation principles (Val, confirmed by the team).** (1) Product Management breaks a product into **Capabilities** (user-perspective, easy to write a user story/UX for), not features-first; engineers then open **feature branches** toward milestones. (2) Connect **QA engineers** at the feature stage, sitting **shoulder-to-shoulder** with developers — "Вы должны перестать думать, что вы не тестировщики. Я должен вас поднять на **Engineering Level**." (3) **Create tests in parallel with, or ahead of, feature development.** (4) **Focus on integration tests first**, so a pull request is justified by a passing integration test — and "когда они не проходят, это настолько же хорошо, когда они проходят" (a failing test is as good as a passing one). The team agreed with the direction but flagged it "практически тяжело." [[raw/test_engineering_progress_report-may-21-2025.md]]
- **What the engineers demoed.** [[wiki/people/irina-shishko.md|Irina Shishko]] ("Это говорит Ирина Шишко") wrote two working tests on the **init-setup configuration page** — footer buttons present/enabled, and the **language** button launching a new page. [[wiki/people/ivan.md|Ivan]] and [[wiki/people/alexei-khamin.md|Alexei Khamin]] took the **multi-language** feature with Anto[n]. Ivan's tests work but he hit a big **wait/synchronization** problem — elements not found unless he hard-codes a timeout; **full XPath** selectors break when the UI shifts or an ID changes ("буквально в айдишнике одно буквы изменилось"), so he compares `getPresentText` against text he recorded by hand, and needs a genuinely **fresh front-end+back-end build** each run. Alexei's test won't run yet — an **import/web-browser conflict** (debugged live with Anton: a double `open URL`, a missing `()` on finalize). [[raw/test_engineering_progress_report-may-21-2025.md]]
- **The localization-dictionary gap.** The language tests need a **single source-of-truth dictionary** to compare against (not the code comparing to itself); the **Spanish** translations are missing/empty. The dictionary was prepared by **[[wiki/people/ihar-hrybko.md|Igor]]** (Hrybko, localization owner — surname transcription uncertain, Tier B) — the team must ask him in **what form** it exists so tests can pull from it. The backend+UI container the testers run was given by "**Женя**" (a Zhenya — which one unresolved, queued). [[raw/test_engineering_progress_report-may-21-2025.md]]
- **Anton's framework primitives (POM + LGS models).** [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] built new test-framework primitives that **abstract LGS access** into models (e.g. `enable-language`, set language, set language for games via **tap-set-languages** requests) instead of raw LGS calls, plus **Page Object Model (POM)** classes — e.g. an `InitSetup` object exposing language selection and a theme toggle, with a sample test that flips the theme and asserts new≠old. Everything is still on **mocks**; he posts informative **pull-requests** (examples + docs) to the channel and tracks the object-implementation plan in **Jira**. Next-week action list (for a **Mon May 26, 7am ET** meeting): Irina finishes the footer tests; Ivan resolves his wait/XPath issues; Ivan+Alexei align on the dictionary with Igor; Vlad picks an LGS feature (and tells Anton which model to add); Anton finishes the Initial-Setup pages and more LGS abstraction models. [[raw/test_engineering_progress_report-may-21-2025.md]]

## May 29 2025 — Jira/GitHub test linkage matured

On the [[wiki/meetings/2025-05-29-jira-plans-maturity.md|May-29 Jira-plans maturity session]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], QA lead [[wiki/people/irina-makarych.md|Irina]]) the test-to-code plumbing was made concrete inside the broader Jira/GitHub split (decision on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]). [[raw/jira_plans_maturity-mat-29-2025.md]]

- **Where tests live:** test **cases/suites** in **Jira via X-Ray**; test **code** in **GitHub** beside the product code, each test's ID referenced in the code. **GitHub Actions** run the automated tests and report results back to **X-Ray** (the "Test 360" testing project lives in GitHub); **manual** test procedures feed the same result store. A test must ship with the feature branch — "no test, no pull." [[raw/jira_plans_maturity-mat-29-2025.md]]
- **QA into TypeScript:** the QA team is moving off pure manual testing into writing code; **Anton** already built a primitive automated test (a multilanguage-button check) to extend. Val wants those visible in X-Ray. [[raw/jira_plans_maturity-mat-29-2025.md]]
- **GitHub Issues for engineering discussion:** enabled per repo so technical/code-health talk (stale branches, etc.) leaves Jira — a slot-machine setup-screen example (toggle a switch → setup field appears → Irina writes the test) illustrated the feature/test cadence. Val booked a **June 5, 9 am** demo of live tests in the repo and X-Ray. [[raw/jira_plans_maturity-mat-29-2025.md]]

## May 30 2025 — FlexPort/FlexPay QA-plan structure in X-Ray

On the [[wiki/meetings/2025-05-30-qa-flexport-flexpay-plan.md|May-30 QA/rollout meeting]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], QA lead **Irina** "Ира") Irina walked the concrete X-Ray test-plan structure that implements the [[wiki/meetings/2025-05-20-flexpay-flexport-test-plan.md|May-20 "split into separate plans"]] direction. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]

- **X-Ray now lives per project** (system changed): test cases live in the **FlexPayment (FP)** developer project they test (per Aaron's rule that tests live with the code); the **QRM (QA & Release Manager)** project holds test-documentation tasks and release items (e.g. **QRM-338** = test creation; **IP-884** = the FlexPort "Wallet" release ISO). [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- **Three test plans for the e-Wallet variant:** a **FlexPort** plan (~8 cases), a **FlexPay** plan (~27 cases, plus ~27 more + ~30 FlexPort), and a combining plan — all three must pass "green" to certify the e-Wallet configuration. Test **sets** within a plan (ticket creation, setup, reports, **card issuance**) can be moved to a future device's plan when a **Tito server / Tower** replaces FlexPay. Test cases are **>50% written**, needing more for **partial redemption**. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- **QA-lead identity note:** "Ира/Ирина" is routed to **Makarych** (consistent with the May-20 test-plan meeting); the transcribed-surname ambiguity with [[wiki/people/irina-shishko.md|Shishko]] stays queued Tier A. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]

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
- [[raw/integration_tests-apr-24-2025.md]]
- [[raw/ci_cd_qa_structure-apr-24-2025.md]]
- [[raw/omni_test_status_review-may-14-2025.md]]
- [[raw/qa_test_implementation-may-16-2025.md]]
- [[raw/github_branch_structure-may-19-2025.md]]
- [[raw/flex-port_flex-pay_test_plan-may-20-2025.md]]
- [[raw/test_engineering_progress_report-may-21-2025.md]]
- [[raw/jira_plans_maturity-mat-29-2025.md]]
- [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
