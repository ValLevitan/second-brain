---
type: person
title: Anton Leshkevich
date: 2025-01-21
aliases: [Anton Leshkevich, Anton, Antoine, Anton Dmishkevich, Дмишкевич, Дмишкевичем]
disambiguation: "One of THREE distinct Antons. Anton Leshkevich = Minsk engineer (Omni/RGS, this page). Distinct from Anton Seregin (Minsk payroll, wiki/people/anton-seregin.md) and the SMM/Meta-ads contractor (wiki/people/anton-smm.md). Owner-confirmed 2026-07-13. Resolve 'Anton' by context; queue if unclear."
source-count: 11
open-commitments: 1
open-questions: 0
---

# Anton Leshkevich

Anton Leshkevich is a JVL Minsk engineer. He knows the Omni framework and RGS codebases well and acts as a bridge between the Russian-speaking Minsk team and the English-speaking advisers (Aaron, Jason). His surname is given on the Jan 21 continuous-delivery call. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

**Owner ruling (2026-07-13):** distinct from [[wiki/people/anton-seregin.md|Anton Seregin]] (Minsk payroll) — shared given name only — and from the [[wiki/people/anton-smm.md|SMM ad contractor "Anton"]]. (Earlier batches folded "Anton" into the AI-assisted-development topic without a person page; this page splits him out — see [[wiki/topics/ai-assisted-development.md]].)

## Role

- Participated in the Jan 14 AI-assisted-development workshop; his repo access worked throughout and he received an OpenRouter API key. Aaron suggested he try the AI tools on the **RGS** codebase. See [[wiki/topics/ai-assisted-development.md]]. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- On the Jan 21 continuous-delivery architecture call he advocated an MVP approach — start with a simple "Git triggers build" pipeline and trim everything unnecessary. He defined the standalone test tool's three essential blocks (test management, test authoring, test runner). See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- He said he can write the **environment** definition for the Omni framework himself (he used to work with that codebase); noted he recently could not set up the LGS environment because of missing dependencies and had to ask Alexander for help — used as evidence the reproducible-environment approach is worth doing. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- Val repeatedly used Anton as the check on whether an explanation had landed ("Anton, do you understand this?"), positioning him as the team member who must be able to re-tell the plan. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

- **Closest person to Efim's math (late Jan–early Feb):** on the docs-in-Git session Val named him the nearest thing to redundancy on the company's most guarded asset — "I think the closest person right now is Anton Leshkevich" (to [[wiki/people/efim-podvoiski.md|Efim]]'s math work); Aaron's takeaway: then at least one other person can review what Efim commits. See [[wiki/meetings/2025-02-01-docs-in-git-vs-confluence.md]]. [[raw/the_importance_of_storing_artifacts_in_git.md]]

## DevOps container approach for Omni (Mar 24–25 2025, dates inferred)

- On the two-day Miro session he presented the artist-files pipeline, translated between Aaron and Alexander, and supplied the key technical corrections: the framework is a Git repository used as a **submodule** — no release artifact — with **git tags** on master marking versions ("this is framework version 1.2.3"); breaking API changes flow dev-branch→master as the de-facto release. He recalled splitting Omni into repositories with submodules/branches/tags ("я поэтому в Omni пытался разбить на репозитории") and that Omni's current game work (he names "Dragon's Array") links everything into the game directly — no template exists yet. His one-button goal: an ISO image from a manifest of repos+tags, in small per-product iterations. He raised sound-asset validation and designers' Git-friction; took the action to name the pipelines/repos on the board. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/devops_container_approach_for_omni.md]] [[raw/devops_container_approach_for_omni_3.md]]

## Open commitments

- [ ] Anton — name the pipelines/repos on the Miro board ("these become repos that we can actually point our finger on") — due unspecified — [[raw/devops_container_approach_for_omni.md]]

## History

- **Test-360 progress review (Fri Jul 5 2024, date inferred; pre-window, queued):** owned the first unit-test push on the Omni framework — test environment set up, ~**9%** of the Omni Engine covered using **Jest**, light refactoring (deleting never-executed code found via coverage reports; consulting Alexander Biratka before non-obvious refactors); wrote the first testing requirements (CI/CD on every merge, automated testing in the pipeline, every change linked to a ticket) and emailed them plus Confluence docs to developers for votes; estimated 30–60 calendar days to cover the existing code. He confirmed the RGS codebase already ran the commit-triggered unit-test approach, and that P1000 has no tests ("a historical artifact"). Transcribed once as "Antoine." See [[wiki/topics/test-automation-strategy.md]] (History). [[raw/test-360_progress_review_meeting.md]]
- **JVL Insights (~2023–24):** named **"Anton Leshkevich (Sr. Programmer) - Consultant"** in the JVL Insights knowledge-base proposal — to develop/integrate AI algorithms in **Python**, build front-ends in **JavaScript**, and ensure compatibility with existing **Java** applications. (Note the draft labels him a consultant; 2025 sources treat him as a JVL Minsk engineer — both recorded.) Compensation figures withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

## Integration tests for the Kai-Ocho Omni port (Apr 15)

- Val on the Omni daily: "Вам в этот разговор еще нужно подтягивать Антона … Саша, вы с Антоном должны вплотную начинать работать, чтобы Антон делал интеграционные тесты" — Anton builds the integration tests for the first Omni game ([[wiki/decisions/2025-04-14-kai-ocho-first-omni-framework-game.md]]). Attribution to Leshkevich by Omni/test-automation context (consistent with his Mar-24 auto-testing role), labeled inference. [[raw/daily_omni_progress-apr-15-2025.md]]

## Apr 16 2025 — trains QA on integration tests (changed decision)

Val changed his earlier plan: rather than Anton writing the integration tests himself, Anton is to **train JVL's QA engineers** to write them ("Я не хочу, чтобы вы сами руками писали эти тесты … начинали учить наших QA-инженеров"). He is to prepare a presentation and run a kickoff meeting with Irina and Pavel — Val offered to attend Friday **6:30 am**. Anton had also been doing the game-history screenshot work on the Omni framework. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] See [[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md]].

## Apr 22 2025 — Calle Ocho feature assignment

On the scheduling session ([[wiki/meetings/2025-04-22-calle-ocho-omni-feature-scheduling.md]]) "Anton" was assigned the game-integration features — **Free Spins (FRAM 664)**, **Mass Engine (FRAM 2)**, **Bonus Game (FRAM 699)** and **Pick Your Fortune Dialog (FRAM 693)** — plus the matrix symbol-sorting under FRAM 478 (~2 days, done before on the online side), run at ~70% so he can also begin QA tests. See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

  - **Identity note — OWNER-CONFIRMED (2026-07-15):** the transcript surname "**Антоном Дмишкевичем / Anton Dmishkevich**" is a **transcription garble**, positively this Anton Leshkevich (not a distinct person). The garble variants are recorded in his aliases so future occurrences auto-resolve. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

## Apr 24 2025 — demos the first Omni integration test; trains QA engineers

On the Omni integration-tests onboarding ([[wiki/meetings/2025-04-24-omni-integration-tests-qa-onboarding.md]]) Anton demoed the **first Omni init-setup integration test** — **Selenium + TypeScript on Node.js** (chosen over Playwright, which was harder to fit into JVL's custom automation framework) — run against a local **LGS docker + LGS-UI** repo via `Yarn Start`. Tests live in the Git repo beside the code, each with a unique key (for future X-Ray integration). Consistent with the [[wiki/decisions/2025-04-16-replace-testers-with-test-engineers.md|Apr-16 decision]] that Anton **trains the QA engineers** to write integration tests rather than writing them himself; Val named him (with [[wiki/people/alexander-biratka.md|Alexander Biratko]]) as a TypeScript-learning source. Detail on [[wiki/topics/test-automation-strategy.md]]. [[raw/integration_tests-apr-24-2025.md]]

## Sources

- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/the_importance_of_storing_artifacts_in_git.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
- [[raw/test-360_progress_review_meeting.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
- [[raw/integration_tests-apr-24-2025.md]]
