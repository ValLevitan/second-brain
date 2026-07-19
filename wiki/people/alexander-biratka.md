---
type: person
title: Alexander Biratka
date: 2026-07-12
aliases: [Alexander Biratka, Alexander, Sasha, Sasha Biratka, Alexander Beratka, Sasha Beratka, Alex, Alex Beratko, Alexander Beratko, Sasha Piratko, Sasha Deratka, Alex Baratka, Alex Beratka, Alexander Berankov]
source-count: 25
open-commitments: 1
open-questions: 0
---

# Alexander Biratka

Alexander Biratka (called "Sasha") is a JVL engineer, part of the Minsk engineering team. He runs hardware/performance tests and works on the build pipeline.

## Role

- Ran the FP7 sample CPU board performance tests: fed simultaneous HD videos through the board and reduced the count until he found a "tolerable" threshold (about 20 FPS), landing on 7 simultaneous HD videos plus 2 half-screens on V-Deck. [[raw/fp-7_performance_analysis_january_13_2025.md]]
- He checked RAM and memory during the test and reported nothing was overloaded; he profiled the board only by visual control (watching it). [[raw/fp-7_performance_analysis_january_13_2025.md]]
- On the build-pipeline call, Sasha explained the ISO-image parameterization problem: Bitbucket cannot build a flexible UI for choosing game/library versions before a build launches. He proposed generating a JSON config from a Jenkins-style UI, pushing it to the repo, then triggering the Bitbucket pipeline. [[raw/development_pipeline_january_13_2025.md]]
- He took the homework (with the QA team) to define which parameters QA needs when building the final ISO. [[raw/development_pipeline_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop as a participant; Aaron suggested Sasha try the AI tools on the Omni framework or LGS codebase. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- Sasha wrote a small script that generates a build-config file and creates an "envelope," demonstrating the Git-native approach. He agreed with the simplification ("I like any simple solutions") but asked not to hard-cap the number of build variants — add more only if needed. He also proposed the pragmatic fallback of re-attaching Jenkins on top to generate the config if all else fails. See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]]. [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## FP7 video testing and Pixi upgrade (Jan 16–17)

- On the Jan 16 game-design review, Sasha (with a colleague noted as "Emma") tried a new video format that improved FP7 performance slightly. [[raw/game_design_january_16_2025.md]]
- On the Jan 17 bottleneck testing, Sasha ran the video-stream tests, found VP9 best in Chromium and VP8 in Firefox, and reproduced the same limit on his own PC with a powerful Radeon 6650 XT — showing the bottleneck is the CPU, not the GPU. He proposed upgrading to the new Pixi engine version, and is to do that upgrade (~a week). See [[wiki/decisions/2025-01-17-upgrade-omni-to-pixi-8-6.md]]. The transcript credits "Beratka" with coining the term **"manifest"** for the asset-creation guideline. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]

## GitHub structure homework and part-1 debate (Feb 7–10)

- **Feb 7 (Friday homework session):** among the homework group ("Sasha and Andre and Aaron"); Val asked him to put his diagram into GitHub as Andrei transferred the repository from Bitbucket. See [[wiki/meetings/2025-02-07-github-homework-and-bitbucket-transfer.md]]. [[raw/GitHub repository structure.md]]
- **Feb 10 (part 1):** Sasha presented the team's resolution — **one organization "or probably two"** (company-wide + a private one for the math sources), arguing **groups** are more flexible than organizations for rights and that mirroring Jira "didn't work out"; under Val's and Aaron's scaling challenge the meeting ended at **five organizations**. He named the shared codebases ("globally we have three projects. Lendbase, online, and server" with common libraries and people crossing projects) and dismissed the 100-directories management fear: "I'm not going to work with 100 directories all the time… we give them a group, that's it." He resisted splitting game production from platform ("If we divide the organizations, we create technical difficulties, but we do not solve the problem that you have voiced") but conceded on Lena: "This is how it will be. There are no problems" (Lena not working through him). (The "омни-платформа… по факту является игрой" example-game description in the same meeting has an unclear speaker — Pasha was asked to repeat it for Aaron — so it is not attributed to Sasha.) See [[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]] and [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/github _structure-pavel-aaron-andrei.md]]
- Val's meta-criticism in that meeting: Pavel gives up his questioning too easily when Alexander answers — "clearly, Alexander is a prominent, trusted senior engineer, and we love him," but disagreement between them is "a very good instrument to finding the truth." [[raw/github _structure-pavel-aaron-andrei.md]]

## GitHub repo structure (Feb 11)

- On the Feb 11 org-structure session Sasha ("Alex") argued for shorter names in the URL and, for sorting/filtering, suggested the "JVL" tag belong at the **end** of org names (Aaron/Val kept it at the front). He asked to keep repo/org names readable and confirmed the naming standard. See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## GitHub check-in (Feb 12)

- On the Feb 12 GitHub check-in Sasha was named a reviewer (with Val and Pasha) on Andrei's DevOps-repo pull requests, and his GitHub user account (rendered "Alexander Beratko" in the transcript) was used to demonstrate how an internal repo is visible to a non-member. See [[wiki/topics/github-access-and-security-model.md]]. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## DevOps container approach for Omni (Mar 24–25 2025, dates inferred)

- On the two-day Miro session (with Val, Aaron, Anton) he carried the framework-owner position: **no framework release artifact** — "there is no point in releasing the framework because we don't need it as a product"; a game is built from the framework's latest state; the framework is a set of assembly scripts, with templates possibly reduced to configuration files (the V1000 pattern: one framework that "умеет все" + per-game config). He questioned the many-red-templates model and converged with Anton on **few templates by delivery type** (online / land-based / genuinely different styles like bingo or roulette); prefers a **repository per game**. He disclosed a working **browser previewer** for exported scenes built on OmniFramework, already pushed to a repository. See [[wiki/topics/omni-core-advancement-and-game-templating.md]] and [[wiki/decisions/2025-03-24-freeze-core-capabilities-before-game-production.md]]. [[raw/devops_container_approach_for_omni.md]] [[raw/devops_container_approach_for_omni_3.md]]
- In Val's proposed core-technology team shape from the same sessions, Sasha is the **implementer** of what Dima Khandov (as requirements-driver) asks for ("Alexander doesn't do anything without any requirements"). [[raw/devops_container_approach_for_omni_3.md]]

## Open commitments

- [ ] Sasha (Alexander Biratka) — write a real build-config file (game, framework, LGS, hardware abstraction layer), put it in Git, and set up a job that produces an image/archive (not a full ISO yet) — due by the next meeting (Monday) — [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

Note: the correct surname is **Biratka** (confirmed by Val). The transcripts spell it inconsistently — mostly "Beratka", once "Biratka" — so both forms are kept as aliases for search. The transcripts also use "Sasha" as a short form, and once the garble "Pasha" appears near his name; "Pasha" is treated as Pavel elsewhere. See [[wiki/people/pavel.md]].

## History

- **Jul 2024 (date inferred; pre-window source):** on the Test-360 review, Anton recalled Alexander "won't be available until August" for the Omni project ("Alex Beratko"/"Alexandra Beratka" in that transcript); Val's plan was for Anton's unit-test coverage and refactoring to be done "in agreement and in collaboration with Alex Beratka" before Alexander returned to advancing OmniFramework in ~mid-August 2024. [[raw/test-360_progress_review_meeting.md]]

## Omni repo owner + the framework-repo lesson (Apr 14–15)

- On the Apr 15 Omni daily, Sasha had **renamed the products/repos** so one product = one repository (a game keeping two — code and assets); he kept designers' raw sources out of the game repo (hence the separate sandbox/asset-sources repo), owns renaming master→main on his repos after notifying users, and is to start working closely with Anton ([[wiki/people/anton-leshkevich.md|Leshkevich]]) on **integration tests** for the Kai-Ocho Omni port ([[wiki/decisions/2025-04-14-kai-ocho-first-omni-framework-game.md]]). [[raw/daily_omni_progress-apr-15-2025.md]]
- Val's Apr-14 retelling of the framework-repo lesson names him: when "Бератко" had to write Actions and assemble the framework product from two-three repositories, the team realized the product was described wrong — Val's standing example that repo structure exposes bad product definitions. Val also cites him (with Andrey and Pavel) as the crew whose GitHub bruises the CMS team should learn from. [[raw/cms_svn_github-april-14-2025.md]] [[raw/cms_github_svn-apr-15-2025.md]]

## GitHub–Jira product reshuffle (Apr 7)

Sasha raised the **git-submodule pain** that opened the Apr-7 reshuffle meeting ([[wiki/meetings/2025-04-07-github-jira-reshuffle-products.md]]): **Omni-Core** is a shared submodule inside **Omni-LandBase** / **Omni-Online**, so branching across submodules constantly produces merge conflicts and a manual submodule-reference commit. He leans toward dropping submodules; he refused to retroactively open feature branches over already-written code ("это обманный маневр"). The meeting landed on re-carving "Gaming Platform" into six product-repos, each product its own repository. See [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]]. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## Apr 16 2025 — Omni framework base classes, and "clone Sasha"

In the Omni daily Sasha (Biratka) was the framework owner: he writes the base classes the games trigger (bonus/base-game/free-spins), which each game then implements concretely. Most of the framework work rides on him — Val: "работает за трех человек" and joked "1 июня … мы Сашу клонируем." Sasha + Dima Khandov are to write the stories and descriptions for FRAM 19/478/476/459/653/FRAM 1 by the next day, and the master→main branch rename was restated as standard. His game repo/build was also used in the AI-tooling meeting (a designer built it via Cline; see [[wiki/topics/ai-assisted-development.md]]). [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] [[raw/mcp_experiences_tech-apr-16-2025.md]]

## Apr 22 2025 — Calle Ocho feature assignment

On the scheduling session ([[wiki/meetings/2025-04-22-calle-ocho-omni-feature-scheduling.md]]) Sasha took the **VDAC Panel (FRAM 476)**, **Game Interface Integration (FRAM 478, sound + matrix symbol sorting)**, **Game History (FRAM 459, LGS state save/restore)** and the **LGS-framework+game packaging (FRAM 653)** — the heaviest share (the playable base-game build lands only end of May). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]

## Apr 24 2025 — game↔framework↔LGS communication (setup-screens review)

On the setup-screens review ([[wiki/meetings/2025-04-24-omni-setup-screens-june-scope.md]]) "Sasha Biratko" (transcribed Beratko / Piratko / Deratka) owns the **game↔framework↔LGS communication** in his development plan; phoned mid-call, he confirmed that using the **legacy setup screens requires no changes in LGS** — the technical basis for shipping the June-1 release with legacy screens + new React initial-setup screens. See [[wiki/decisions/2025-04-24-omni-first-release-legacy-plus-remote-setup-screens.md]]. [[raw/set_up_screen_omni-apr-24-2025.md]]

## May 1 2025 — the "Unity instead of Miranda?" assessment

On the [[wiki/meetings/2025-05-01-unity-instead-of-miranda.md|Unity reconsideration call]] Val and Aaron asked Sasha whether JVL could adopt a licensed Unity ecosystem (with its casino engines) and drop Miranda. Sasha's read: good performance for **land-based** and native apps, historically poor for **browser** builds (like Pixi) though much improved; Unity's engine language is **C#** (new to JVL — his ~10 Unity people are designers building only the theme/view, no logic); refactoring Miranda's logic into Unity is unknown and depends on how much game logic is externalised to the remote gaming server/math. No decision. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/unity_instead_miranda-may-1-2025.md]]

## May 8 2025 — named as the Omni MCP-adapter author

On the [[wiki/meetings/2025-05-08-capability-compass-mcp-aaron-session.md|May-8 MCP session]] [[wiki/people/aaron.md|Aaron]] used **"Alex Baratka"** (this person, garble) as the example of who would need to write an **in-stack MCP server / JSON-RPC adapter inside the Omni framework** — exposing the running software's classes/methods to an AI agent (a debugger-like interface written with the code). See [[wiki/topics/ai-assisted-development.md]]. [[raw/mcp_servers_for_jvl-may-8-2025.md]]

## June 26 2025 — Omni grooming (bonus, sounds, service messages)

On the [[wiki/meetings/2025-06-26-omni-schedule-grooming.md|Omni schedule grooming]] Sasha picked up most of the reshuffled bonus-day tasks (partly shared with Anton Leshkevich), is finishing **Crazy Spins sound integration** (~done next week) and cache/service-message work, and helped shape the **topper-as-separate-application** direction (he'd earlier done the free-spins screenshot work; sees little difference in effort between embedding the topper vs a separate app, beyond a new repo/build). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI_schedule_grooming-june-26-2025.md]]

## Sources

- [[raw/OMNI_schedule_grooming-june-26-2025.md]]
- [[raw/fp-7_performance_analysis_january_13_2025.md]]
- [[raw/GitHub repository structure.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/game_design_january_16_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Check_in_on_GitHub_2025-02-12.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
- [[raw/test-360_progress_review_meeting.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/mcp_experiences_tech-apr-16-2025.md]]
- [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- [[raw/omni_calle_ocho_scheduling-apr-22-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/unity_instead_miranda-may-1-2025.md]]
- [[raw/mcp_servers_for_jvl-may-8-2025.md]]
