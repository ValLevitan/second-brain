---
type: person
title: Alexander Biratka
date: 2026-07-12
aliases: [Alexander Biratka, Alexander, Sasha, Sasha Biratka, Alexander Beratka, Sasha Beratka, Alex, Alex Beratko, Alexander Beratko, Sasha Piratko, Sasha Deratka, Alex Baratka, Alex Beratka, Alexander Berankov, Biratko, Alexander Biratko]
disambiguation: "Alexander cluster (provisional — owner ruling pending): distinct JVL people sharing the given name Alexander. [[wiki/people/alexander-biratka.md|Alexander Biratka]] = Omni/Pixi framework & build engineer (aka Sasha; garbles Beratko/Baratka); [[wiki/people/alexander-korochkin.md|Alexander Korochkin]] = LGS QA-automation engineer (GitHub Alexander_K@JVL, read-only; aka Alexander K); [[wiki/people/alexander-tumanov.md|Alexander Tumanov]] = Minsk QA / data-center knowledge-capture hire (surname unverified). Resolve by context: Omni framework / Pixi / build → Biratka; LGS QA automation / read-only build consumer → Korochkin; manual-tester onboarding / data-center interviews → Tumanov. A further name 'Alexander Derok' (back-end build-integration / Java, per Val on Feb-6-2026) is unconfirmed — queued, not a page. Not [[wiki/people/alexei-khamin.md|Alexei Khamin]] (different name). Queue anything fitting none; never force-match."
source-count: 76
open-commitments: 16
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
- [ ] Move Flex-Pay onto the RK3568 platform — due "the 15th" (September 15 inferred), set Sept 1 2026 — [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [ ] Write prose for the NOVA platform's common/shared part (the game's own prose deferred) — due September 2026 — [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]] [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]

Note: the correct surname is **Biratka** (confirmed by Val). The transcripts spell it inconsistently — mostly "Beratka", once "Biratka" — so both forms are kept as aliases for search. The transcripts also use "Sasha" as a short form, and once the garble "Pasha" appears near his name; "Pasha" is treated as Pavel elsewhere. See [[wiki/people/pavel.md]].

## History

- **Jul 2024 (date inferred; pre-window source):** on the Test-360 review, Anton recalled Alexander "won't be available until August" for the Omni project ("Alex Beratko"/"Alexandra Beratka" in that transcript); Val's plan was for Anton's unit-test coverage and refactoring to be done "in agreement and in collaboration with Alex Beratka" before Alexander returned to advancing OmniFramework in ~mid-August 2024. [[raw/test-360_progress_review_meeting.md]]

## Omni repo owner + the framework-repo lesson (Apr 14–15)

- On the Apr 15 Omni daily, Sasha had **renamed the products/repos** so one product = one repository (a game keeping two — code and assets); he kept designers' raw sources out of the game repo (hence the separate sandbox/asset-sources repo), owns renaming master→main on his repos after notifying users, and is to start working closely with Anton ([[wiki/people/anton-leshkevich.md|Leshkevich]]) on **integration tests** for the Calle Ocho Omni port ([[wiki/decisions/2025-04-14-calle-ocho-first-omni-framework-game.md]]). [[raw/daily_omni_progress-apr-15-2025.md]]
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

## ~July 14 2025 — OMNI schedule review

On the [[wiki/meetings/2025-07-14-omni-schedule-review.md|OMNI schedule-review]] Jira walkthrough (with Val + [[wiki/people/pavel.md|Pavel]]) Sasha reported: VDEC free-spins in but an **animation artifact** under investigation; the **bonus scene ~30% done** (was Anton's, who's on Nebraska) — handed to [[wiki/people/ihar-hrybko.md|Igor Hrybko]] since Sasha can't finish it in a week; the **progressive spinner ported C→TypeScript but its progressive mode untested**; screen-capture works; and he noted the new framework is easier to onboard than the old C/OS one. He's off to **Dagestan on holiday** ~the 21st (back ~28–29). See [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/OMNI schedule review.md]]

## Jul 31 2025 — to be pulled into the amusement-games-platform question

On the [[wiki/meetings/2025-07-31-amusement-games-revival-pavel.md|amusement-games revival session]], Pavel said he'd need to involve **"Sasha"** to see what he's missing on opening the game framework as a platform (the "white-label" idea) — the framework/Pixi context that maps to Biratka (by context; he is JVL's Pixi/framework engineer). See [[wiki/topics/amusement-games-revival.md]]. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Aug 28 2025 — explains Omni animation architecture (recorded for a spec)

On a call [[wiki/people/anton-leshkevich.md|Anton Leshkevich]] recorded to generate a technical specification ([[wiki/meetings/2025-08-28-omni-animation-architecture-biratka.md]]), Sasha (filename "Biratko") walked through Omni's animation system: the two live types (**Spine** + video) plus a slower Unity-native converter he expects to drop; the **Unity→JSON scene exporter** (a Unity script emits a JVL-format JSON the Pixi engine parses, with custom element types like a `spinner` declared on the Unity side and realised only in the JVL engine); a common start/stop/pause clip interface; and the **animation-controller state machine** (Unity-exported JSON of variables/states/transitions, fired transition events code can subscribe to) — which he judged "workable, not very elegant." Substance on [[wiki/topics/omni-core-advancement-and-game-templating.md]]. [[raw/Anton_Liashkevich_Alexander_Biratko_about_OMNI-august-28-2025.md]]

## Feb 3 2026 — Claude Code workshop (the "context collapses into one head" concern)

On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 Claude Code workshop]] "Sasha" attended as one of the engineers being onboarded. Aaron used his testing practice as an example (Sasha runs **unit + integration tests** to verify libraries do what they should). Sasha raised the session's main push-back: the whole context still ends up "in the head of the person writing the prompt," and a long Claude session eventually **forgets** earlier instructions — so the prompter must keep directing the agent's attention to the specific area. Val agreed but pointed at the large-context future (Aaron's [[wiki/meetings/2026-02-02-knowledge-graph-tool-introduction.md|Feb-2 knowledge-graph tool]]). See [[wiki/topics/ai-assisted-development.md]] (Feb-3). [[raw/Claude Code integration - continued.md]]

## Feb 6 2026 — named as a team member but absent (the "Alexander" confusion)

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] his GitHub handle came up as **"Alexander_B@JVL"**; Val confirmed **"Alexander B is definitely part of the team. He's just not on the meeting with us right now."** Aaron's Claude Code run mislabelled an "Alexander" as QA-automation and then as a heavy **back-end build-integration / Java** contributor; Val resolved that the tool had **confused two different Alexanders** — the back-end role belongs to a separate "Alexander Derok" (transcribed, unconfirmed — queued) and the QA role to [[wiki/people/alexander-korochkin.md|Alexander Korochkin]] — **not to Biratka**. Recorded to prevent future mis-linking; see the disambiguation block. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Mar 4 2026 — takes over Yavorski's FlexPort application (IP 10-13); the FP 519 root-repo anti-pattern

On the [[wiki/meetings/2026-03-04-schedule-review.md|Mar-4 schedule review]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]) [[wiki/people/pavel.md|Pavel]] picked Sasha — over [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] — to take over [[wiki/people/eugine-yavorski.md|Yavorski]]'s **FlexPort application (IP 10-13)**, becoming its reporter/owner once he finishes the current **cash-dispenser** task (~1–2 weeks). He is expected to absorb the code by monitoring Yavorski's commits and using Claude for code review. [[raw/Schedule_review-March-4-2026.md]]

- **FP 519 exposed the feature-branch anti-pattern.** Sasha's **FlexPos software-update** feature (FP 519) — a small Python auto-updater that sits in the **RK3568** root, watches for an update file, unpacks it, swaps the link and reboots — was built as a **standalone repo committed to root, not under a feature branch**, so nothing linked it back to Jira. It became Val's worked example for the feature-branch discipline he wants (each feature under **IP 902 = FlexPos** gets its own branch, surfaced via a GitHub-branch field). See [[wiki/topics/github-release-management-pipeline.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]

## Mar 26 2026 — reassigned off the external watchdog onto the FlexFare cash dispenser

On the [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Initiative Priority Schedule]] meeting Pavel noted Sasha ("Sasha Piratko") had external-hardware watchdog-timer tasks planned; with the team choosing the Linux kernel-panic auto-reboot (Option 4) over an external watchdog chip (Option 2), Pavel **pulled Sasha off the external-watchdog work** and reassigned him to the **bill/cash dispenser for FlexFare**. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-26). [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]] [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]

## Mar 30 2026 — OMNI 2 architecture call (language stack, containerization, peripheral abstraction)

On the [[wiki/meetings/2026-03-30-omni-architecture-biratka.md|Mar-30 OMNI Architecture call]] with Val, Sasha was the senior engineer Val brought the OMNI 2 plan to. He accepted the **three-language target (Rust, TypeScript, Java)**, arguing Java should stay for LGS (TypeScript can't drive native devices; a Rust rewrite of LGS is too large and Java is easier to maintain/debug and well-supported by AI tooling); he noted AI-assisted coding works especially well with Rust. He explained the **containerized-math origin** (a Julia container run directly on target), agreed games can be containerized for QA with "small" effort, and offered to check with [[wiki/people/pavel.md|Pasha]] on auto-mounting the game Docker as a filesystem directory for LGS. On Val's **peripheral-abstraction protocol** he raised the **iBoard latency** concern (a high-speed memory chip persisting bet state on Spin; ~10ms protocol overhead uncertain) while confirming all slow peripherals are unaffected. He is currently implementing the **cash dispenser** and can't fully validate it without physical hardware (documentation "half in Japanese, half in English"). Two undertakings, ~by Apr 4: (1) assess the peripheral-abstraction approach from a QA/business angle; (2) correct the outdated OMNI architecture MD doc Val will send and return it. Substance and the two open commitments on [[wiki/topics/omni-core-advancement-and-game-templating.md]] (Mar-30). [[raw/Meeting_Transcript_OMNI_Architecture_Biratko-March-30-2026.md]] [[raw/Meeting_Notes_OMNI_Architecture_Biratko-March-30-2026.md]]

## Apr 13 2026 — the repo-architecture v2→v3 debate

On the [[wiki/meetings/2026-04-13-flex-pos-repo-architecture-review.md|Flex-POS Repo Architecture Review]] (with Val and [[wiki/people/andrey-bosik.md|Bosik]]; transcribed "Biratko"/"Sasha") Sasha defended his **v2 repo standard**: a top-level `repo-[product-name]` repo holding cross-repo docs including **data contracts**, on the principle that "truth must live in one place." Val resisted the master concept (self-describing repos + Aaron's Attend peer-mesh instead), but at minute 21:38 Sasha independently described the peer-mesh pattern in his own words — "that is exactly what Aaron built," Val said. Outcome: v2 is **not discarded** but promoted to **v3** at the 14 Apr joint Aaron session. He also proposed a daily/weekly Claude drift-check on the standard. Substance on [[wiki/topics/github-release-management-pipeline.md]] (Apr 13 2026). [[raw/Meeting_Notes_Flex-POS_Repo_Architecture_Review-April-13-2026.md]] [[raw/Meeting_Transcript_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]

## May 12 2026 — appointed Chief Architect of NOVA

On the founding NOVA platform architecture session ([[wiki/meetings/2026-05-12-nova-platform-architecture-overview.md]]) [[wiki/people/val-levitan.md|Val]] formally appointed Biratka **Chief Architect of NOVA** on the record — "Alexander Vladimirovich Biratko is appointed Chief Architect of this project" — his full name confirmed for the transcript as **Александр Владимирович Биратко**. The role explicitly carries authority to make architectural decisions, which he exercised (e.g. ruling one repository per hard service over Anton's monorepo suggestion on release-ability grounds). He drove the as-is walkthrough (Segment 1) and the to-be design (Segment 2), and owns all NOVA ADRs (which live as files inside each repo). Full architecture on [[wiki/topics/nova-platform-architecture.md]]. His immediate undertakings: consult [[wiki/people/pavel.md|Pavel]] on the name and architecture; confirm the Arrange-vs-MathEngine repo split with [[wiki/people/efim-podvoiski.md|Efim]]; get MathEngine/Arrange access (math secrecy relaxed); and pick the first service to port to Rust. §15.8 clear — architecture/role only, no compensation. [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_2-May-12-2026.md]] [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_1-May-12-2026.md]] [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]

## Sept 1 2026 — back from vacation: Flex-Pay onto RK3568, and the prose split he proposed

He returned from vacation on Aug 31 2026 ("Вчера вчера вышел"; Irina: "2 день только") and was the subject of the [[wiki/meetings/2026-09-01-nova-prose-qa-automation-check.md|Sept-1 check-back]]. [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]

- **New assignment: move Flex-Pay onto the RK3568 platform, targeting the 15th.** Announced by Pavel; Sasha supplied the platform himself ("На ркплатформе"). See [[wiki/decisions/2026-09-01-flex-pay-onto-rk3568.md]]. Val characterised his area as "транзакшенал оборудование[м]" (transactional equipment) but said he had not worked out which Flex-Pay is meant. [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **He proposed the prose split that Val adopted.** Describing the shared platform repository alone loses the code that lives in the game and carries from game to game, so "мы можем как бы разделить эти прозы… Поэтому мы можем описать вначале касающиеся общей части," with the game's prose written later or when the next new game is written. Val: "Я сторонник, чтобы именно так сделать." This refines his [[wiki/topics/nova-platform-architecture.md|Aug-13 commitment]] to write prose for the framework and one base game. [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **He argued twice for not discarding the existing manual tests** — first that Claude could simply walk the existing test cases and add what is missing, then that bug-specific, location-specific and rare-settings tests "могут быть прям прям важными," proposing a one-time overlap analysis. Val heard him and did not adopt it. See [[wiki/decisions/2026-09-01-freeze-existing-manual-test-cases.md]]. [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **Pavel named him as the candidate for the games-side NOVA prose** ("саша был у нас претендентом на то, чтобы заняться этим"), and Val added him to the Friday QA-automation check-in with [[wiki/people/igor-metelski.md|Igor Metelski]]: "Я приглашу тогда сашу бератко сюда тоже." [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- **Sept 3 (referenced, not present).** Irina cited his existing game-assembly-and-run-on-a-machine work as a candidate integration base; Pavel pointed out it is the old approach with a hardware layer as a set of libraries, not the Rust-module integration Evgeny is describing. See [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 4 2026 — pushes the scene tool toward automatic visual validation, and defends the browser

At the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|Sept-4 morning meeting]] [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]:

- **He saw the designer use-case in Anton's scene-validation tool** — load a scene and see it in the new engine while developing a new game, and layer scenes to see the finished game — then pushed it further, to automatic validation by screenshot comparison: "разрешить искусственному интеллекту посмотреть старый вью… и новый вью, и чтоб он мог это сравнить и сказать, что да, действительно новый вью получился такой же… без нашего участия." Pavel accepted the reasoning, because isolating a scene removes the non-determinism that blocks pixel comparison inside a running game. Anton had built the tool as an evolution of one Sasha himself started "пару лет назад." See [[wiki/topics/test-automation-strategy.md]] (Sept-4). [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He floated rewriting JVL's own engine in Rust** — "возьмём наш старый движок и доработаем его, например, переведём его на раст" — and argued a house engine may be the cheaper investment: "платить какому нибудь [Unreal] явно будет намного больше, чем поддерживать свой движок." He also conceded Rust's limit for video buffers: "там всё равно требуется доступ… Прямой к памяти. Поэтому там сишка останется." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **But he defended the current browser stack** — JVL chose it because the product had to be online, no free engine as good has appeared, "браузер не умрет… в ближайшие 5 лет точно," and "в реальности на данный момент нам хватает возможности браузера." His one named risk: possibly having to rewrite a piece of Chromium to implement a feature. See [[wiki/decisions/2026-09-04-browser-pixi-stack-concern-closed.md]]. [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He reported the printer library is already being integrated into Flex-Pay** — "Библиотеку принтера уже интегрируем во флекспей" — one of the pieces of evidence Val used for "1 октября началось уже в сентябре или даже в августе." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- **He named the Val–Irina acceptance-criteria disagreement for what it is:** "что перв[ое,] яйцо или курица." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sept 7 2026 — named for the Flex-Pay emulator groundwork

At the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|Sept 7 9:08 Wi-Fi meeting]] (Russian), pressed by [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] for a virtual test system, [[wiki/people/pavel.md|Pavel Frolov]] said he would take it to Biratka and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]: "я поговорю с Сашей Бираткой, с Димой Чудиновым — что можно сделать относительно быстро" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

The route Pavel eventually chose is on [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]]. Biratka was not on the call and took on nothing himself.

## Sept 9 2026 — strict hours, and already on FlexPay

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] [[wiki/people/val-levitan.md|Val]] asked whether three named people could work more hours — "[с]колько люди сейчас работают[:] [Б]иратка, [К]орецкий, Хам[и]н[?] Их можно, чтоб они больше работали?" — and [[wiki/people/pavel.md|Pavel]] answered for him: "[н]у[,] Саша[,] если только с ним договариваться, на какую[-]нибудь там не знаю[,] субботу" — a specific Saturday would have to be agreed with him. Val's own characterisation, said approvingly: "Саша очень дисциплинированный, он вовремя приходит, вовремя уходит." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

Pavel also placed him on the current work: "флекспей сейчас занят Саша Биратка." **§15.8: hours and assignment only; no compensation appears in the source.** [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 10 2026 — the man who would not let "study the capabilities" stay vague

At the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]] he did the useful procedural work: he kept asking what the review was actually for until the group produced an answer, and he proposed the mechanism that became the filing scheme. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **He forced the review's output to be defined.** "[А] какой… результат изучения должен в итоге получиться?… [э]кзамен будет?", then "[н]у вот я нашёл к[апа]били[ти,] я с ним не согласен[ —] что я буду делать?… [к]акой от меня требуется действие?" The answer — say what you disagree with, what is missing, and where requirements are absent, in this meeting's chat — is on [[wiki/decisions/2026-09-10-capability-review-feedback-goes-into-the-meeting-chat.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He proposed using the component column**, which became the per-product components decision: "там колонка есть компонент[,] наверное[,] да?… может[,] отметить[,] но каждый ка[паб]илити[,] к чему это относится". See [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He counted the projects and was not satisfied by the answer** — three, then four once cloud service implementation was counted, with [[wiki/people/pavel.md|Pavel]] conceding "как минимум 4, а может даже пять[-]шесть" — and pressed that a filter alone will not pull the right items out: "[м]ы получаем просто список… элементов[,] и даже вот ты попытался фильтр какой[-]то настроить." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He was assigned the FlexPay capabilities discussed that morning.** [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Open commitments (Sept 10 2026)

- [ ] Alexander Biratka — review his own FlexPay capabilities, the ones discussed that morning — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — assigned the Flex-Port work and the FlexPay port, and absent that day

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] [[wiki/people/pavel.md|Pavel Frolov]] set the work split: Biratka takes the Flex-Port tasks and ports [[wiki/people/dmitri-chudinov.md|Chudinov]]'s finished Flex-IQ work across into FlexPay — "все задачи, которые идут по флекс порту, это будет брать саша [Би]ратка[,] и он… по сделанны[м] работа[м] диминым… будет это переносить во флекспей" — with [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] on the FlexPay server side [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**He was not working that day.** Pavel reported "саша… сейчас не работает" and that Sasha's tasks are FlexPay, which MVP 1 no longer needs after Val's narrowing; [[wiki/people/irina-shishko.md|Irina]] added that he simply cannot. Twenty minutes later, on the [[wiki/meetings/2026-09-11-nova-game-change-regulatory-procedure.md|9:30 call]], Pavel gave the reason — "[у] саши там какая[-]то трагедия в семье сегодня" — a family bereavement [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]] [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]. *(The two "Sasha" mentions are treated as the same person on context — the transactional call names Biratka in full — and this is flagged rather than asserted.)*

## Sept 14 2026 (8:01 AM) — back on the call, and the one who keeps asking what happens when it breaks

Three days after his absence he was present and active on the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|8:01 AM use-case call]], and every one of his contributions was a failure case.

- **How a player proves a printed ticket is his**, and what happens when two people from different machines both claim one: "если пришло… 2 человека там с разных машин[,] говорят[: ] я напечатал". Klimovich's answer — match the IQ transaction, which carries the machine, against the identifier on the ticket — is recorded on [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **Does a broken or empty printer block card issue?** "[Е]сли принтер недоступен, сломался или там нет бумаги[,] мы не блокируем же выпуск карточки[?]" Klimovich: "нет, не блокируем" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **The observation that broke the FlexPay analogy.** Where Chudinov said FlexPay simply does not create the wallet if the printer is dead, Biratka pointed out the port cannot do that, because "они же не остаются на машине, они переходят на порт" — the money has already left. He then sketched the recovery himself: "теоретически… транзакция может закончиться, но потом мы… можем перепечатать [ticket] на самом IQ."
- **The limit of any anti-copy protection:** "защититься от копирования тикета это практически нереально[,] если мы не используем пин[-]код" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **He supplied the SAS knowledge Klimovich lacked** — the specification is public, it says which AFT features are mandatory on a machine and which optional, and he volunteered to send it. He also held the minority view that AFT did not change between 6.02 and 6.03, which Val over-ruled on principle ([[wiki/decisions/2026-09-14-capabilities-are-written-against-the-published-sas-standard.md]]). His own dating of the standard: when he joined, 6.02 was current, and 6.03 came out recently.
- He confirmed the IQ printer is the same one as on the machine — "они точно такие же будут[,] и там принтер такой же" — and that JVL has no capability yet for measuring paper, cards or stacker fill: "у нас, наверное, нет таких к[а]пабилити пока что" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Open commitments (Sept 14 2026)

- [ ] Alexander Biratka — send Klimovich the SAS specification (public; the version Val ruled on is 6.02) — due unspecified; Val offered to obtain it himself if nobody sends it — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 15 2026 (8:03 AM) — he opens the meeting's central question from his own mistake, and brings the SAS wording that settles it

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] (Russian) he raised the balance-naming problem that became the meeting's title, and grounded it in something that had confused him personally while building FlexPay: "**вроде бы есть какойто плейбол и редибл и мне так хочется их сложить, но по факту нельзя их слаживать**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**He refused the split and supplied the word.** When Klimovich proposed separate internal and player vocabularies, Biratka refused alongside Val — "я тоже не согласен, надо чтоб одинаково было" — and it was his insistence on "**playable only**" rather than "playable" that made the arithmetic work, with the authority that the SAS specification already uses that term. He pressed for it in the internal database field too, and Val widened it to everyone. See [[wiki/decisions/2026-09-15-balance-is-total-playable-only-and-redeemable-everywhere.md]].

**He designed the unclaimed-money mechanism** as the smallest possible change: create an empty wallet, transfer the money, mark it unclaimed, and simply do not print a carrier — "по факту то же самое, только без печати тикета". Chudinov dissented in favour of a separate entity, and Val stopped the debate and routed it to Juan and GLI. See [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]].

**He kept asking what happens when it breaks.** He asked what happens when the timeout expires, which is what produced the ruling above; he asked whether the two-SAS-port block case had been tested, which it had not; and he asked for a Flex IQ screen showing tilts and how to resolve them, which does not exist — "я вот не увидел экрана, наверное, его стоит добавить". Val agreed [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**Two smaller ones:** he suggested showing both languages at once, and was overruled on friction grounds; and he confirmed the magnetic stripe reader does not write, so cards must arrive pre-encoded. He is one of the five named owners of the non-functional requirements ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## Open commitments (Sept 15 2026)

- [ ] Alexander Biratka — help [[wiki/people/pavel.md|Pavel Frolov]] build the test cases for machine tilt and block handling over SAS, using his field experience — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Alexander Biratka — add the missing Flex IQ screen showing tilts and how to resolve them — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] Alexander Biratka (with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/pavel.md|Pavel Frolov]]) — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Sept 16 2026 (8:01 AM) — he asks why the wallet is going to the cloud at all, and the problem shrinks

The third MVP 1 morning call ([[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]], Russian). He spoke little and changed the shape of one argument.

With the room deep in offline synchronisation, he stopped it to ask the first-principles question: "**для начала[,] почему мы хотим переместить [е]в[олет] в облако, для чего?… кто[-]нибудь может сказать[,] я просто не в курсе**" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The answers were [[wiki/people/val-levitan.md|Val]]'s — central validation of all tickets, consolidation, bonuses — and [[wiki/people/andrei-klimovich.md|Klimovich]]'s, kiosk replacement at a location [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

He then tested the hardest case himself — cashing the same e-wallet at a different kiosk — and, once Val confirmed there is no such goal, revised his own estimate of the difficulty downward on the spot [[[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]]:

> **[Т]огда проблема, наверное, не такая большая, как как я сразу подумал… нужна нам нужна точка синхронизации[;] если… больше никто не будет пытаться обновить наш тикет на облаке, тогда… немного возникнет сложностей.**

That framing — a synchronisation point rather than a distributed ledger — is what let Val close the topic as a 2027–2028 problem ([[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

He also joined Chudinov in refusing Val's pre-generated-validation-ID idea, in his own gentler register: "это решение очень не очень хорошее", and before that "это сложно" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Sept 18 2026 (8:03 AM) — he is back in the room, inherits the FlexPay half of MVP 1's cast-offs, and says almost nothing

The [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|fifth and final MVP 1 morning call]] before the Monday gate (Russian). He is **back after missing the Sept-17 session**, and speaks five times in sixty-eight minutes.

**Four capabilities moved to him and out of MVP 1 in the same motion.** [[wiki/people/irina-shishko.md|Irina Shishko]]'s reason each time is that the work is FlexPay and "**Саша занимается flexpay['ем]**": **117**, **79** and **80** went to MVP 2 as FlexPay items sitting in MVP 1 by mistake — "**её просто пропустили в прошлый раз, когда передвигали**" — and **116**, "**вообще… флекспей сплошной**", had its responsible person changed from [[wiki/people/dmitri-chudinov.md|Chudinov]] to him and went to MVP 2 too, "**потому что все фичи саши[ны]**". [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**Capability 156 is the one he waits on rather than owns.** [[wiki/people/pavel.md|Pavel]] set the sequence: "**как только дима сделает имплементацию, саша просто возьмёт и перенесёт её… это простое[,] по идее[,] копирование**", with Biratka's dates set only after Chudinov's. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**One capability was taken away from him on principle.** Capability 180 (Flex-Port session life — waiting mode, inactivity timeout) had been assigned to him, and both Pavel and Irina called that wrong — "**требования вешать [на] разработчика — это вообще странно**" — so it went to Pavel. Nobody blamed him; nobody knew who had done it. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**His one substantive question is about receipts**, and it is the question that produced the printing answer: "**а там такие же… будут ре[си]ты, да?**" Pavel: "**Да[,] одинаковые. Единственное[,] там логика печати… чуть[-]чуть разная**" — at the FlexPay the cashier chooses whether to print, in the self-service kiosk the player chooses whether he wants English. [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**⚠ He is one of the two of Val's five named non-functional-requirement owners who go unmentioned** in the Sept-18 status round — the other is [[wiki/people/andrey-bosik.md|Andrey Bosik]]. He was in the room and it never came up; his share is neither reported nor discharged ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]). [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Open commitments (Sept 18 2026)

- [ ] Alexander Biratka — port Chudinov's implementation of capability 156 across to FlexPay once it is done, and set his dates after Chudinov's — due after Chudinov delivers — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Sept 21 2026 (8:02 AM) — two words that settle one fact about the asset number

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM call]] (speaker label "Alexander Biratko") he spoke twice. Asked by Pavel whether the asset number is one per machine however many SAS ports, he said "Да, один", and added the condition: "Но если она работает с AFT и принтером, то да." The derived notes give this fact to Pavel [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]] [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 21).

## Sept 22 2026 (4:48 AM stand-up) — he owns capability 137, and lays out the game-select screen design

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]:

- **Done:** the touch-panel work and the move to the new monitor — "Всё заработало" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Capability 137 is his.** He asked whether the capability or only its features sit on him; Pavel: "ты будешь за неё отвечать". He is creating features to port the mechanism already built for Flex IQ (capability 122). The transcript names 137's subject as "softway. Антферба менеджмент" — read as software and firmware management (**inference**). See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-22 update) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **The game-select screen.** He explained his original design — a separate module loaded like a game — and proposed proving it with plain squares and two copies of one game. See [[wiki/topics/nova-platform-architecture.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **FlexPay overlay.** Pavel said he can move the overlay for FlexPay if Chudinov's expected build break comes [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Open commitments (Sept 22 2026)

- [ ] Alexander Biratka — build the capability 137 features by porting the Flex IQ mechanism from capability 122 — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [ ] Alexander Biratka — with Daniil, talk through and write down the game-select-screen architecture (separate repository or framework artefact) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]

## Sept 22 2026 (8:01 AM) — MVP 1 is clear to him, and only two reasons to update a library

On the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]:

- **MVP 1.** Asked by Val, he said the FlexPay capabilities are MVP 2 and he has screen questions for later; where Flex IQ and FlexPay coincide, "у меня вопросов нету".
- **Kept on features.** Pavel would not release him for test writing: "Я диму и сашу на это не отдам" ([[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]]).
- **Dependency updates.** Only for a vulnerability in a library JVL uses that shows up for JVL, or for functionality a newer library gives; "В других случаях я думаю, не нужно" ([[wiki/topics/github-release-management-pipeline.md]], Sept 22).

## Sept 23 2026 — three features under capability 137

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian; label "Alexander Biratko"), he said he created three features under 137. **FP-1249** (update work) is almost done and installed on the kiosk for checking; a separate logging bug is in progress; **FP-1250** and **FP-1251** are also update work. See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-23 update). He confirmed he works in the FlexPay platform repository. [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

## Sept 23 2026 (8:00 AM) — "we are the host", on what a lost SAS link means

On the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]] (Russian; label "Alexander Biratko"), on the device-disconnect requirements: the SAS standard "описывает работу машины, а не хаста, а мы в данном случае хостом работаем", and losing the machine over SAS is losing the main link — "мы дальше работать не можем". On router purchasing: test it by looking at the router bought. See [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Sept 24 2026 — 137 blocked on Amazon-side endpoints

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian; label "Alexander Biratko") [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]], he said he is closing feature 13-49 under capability 137. The next two, 12-50 and 12-51, are blocked until new endpoints are added on the Amazon services side, so the app can update. Then he will review the FlexPay capability. See [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] (Sept-24 update).

## Sept 24 2026 (8:01 AM) — a warning on cashier power over unclaimed money

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM MVP 1 call]] (Russian; label "Alexander Biratko"; joined late) he warned that if cashiers can redirect unclaimed money, one may "потом не придумал способ их воровать". Cashier handling went to MVP 2. See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]] [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

## Sept 24 2026 (10:00 AM) — features under the right capabilities, and "now is the time" to rename

At the [[wiki/meetings/2026-09-24-nova-galaxy-jira-hierarchy-cleanup.md|Sept-24 10:00 AM NOVA/Galaxy call]] (Russian; label "Alexander Biratko") [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]:

- **Given the job.** Val: "Александр, тогда я хочу на вас положить ответственность" — move all NOVA features under the right capabilities, creating capabilities and requirements where missing. He pointed out there are no requirements yet. Commitment on [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]].
- **The rename.** On renaming the "omni" repositories: there is "нет финальной сборки" yet, so now is the time; what breaks gets fixed.
- **The model.** Once only capabilities sit under the platform, he said, the two views (Chudinov's and the project view) are combined.

## Sept 25 2026 (8:05 AM) — warehouse or office, and "no stops" on the instruction

On the [[wiki/meetings/2026-09-25-transactional-mvp1-flexport-third-party-egm-compatibility-testing.md|Sept-25 8:05 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]: he asked whether a warehouse is better, since the owner's staff can help; Irina and Chudinov said Minsk needs network access, and Pavel offered a hybrid. On timing: "инструкцию можем стартовать… Никаких остановок у нас не должно быть" — Flex IQ is already "достаточно работоспособен, чтобы проверять много". See [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-25 update).

## Sept 28 2026 — card dispenser, bills, the NOVA pull requests, and MVP 2 questions

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]], Russian): capability 137 (updates) is mostly done, with long install checks running. Capability 134 (features 12 84, 12 85, 12 86) brings full card-dispenser support; Pavel asked that it try Syncotek first. Capability 133 (which bills to accept) needs a bill test on the kiosk to close. Next: moving the GSM-modem control code to the Flex-Port. Most of the Omni → NOVA pull requests are in his repositories. On Dragon Rain: "Абсолютно копия" of a game, with the same math [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]]): he called the PIN question "техническая задача… [н]е бизнес". He works only on MVP 2 and is blocked on FlexPay updates — the server has no update support for FlexPay yet. He asked for someone to work on MVP 2's business side, and will collect business questions (for example a dispensed card the player does not take) for these calls and one email thread [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

## Open commitments (Sept 28 2026)

- [ ] Alexander Biratka — make the card dispenser try Syncotek first; finish capability 134; test bill acceptance on the kiosk to close 133; put start and end dates on his tasks — due Sept 28 2026 (134) / unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [ ] Alexander Biratka — accept and merge the Omni → NOVA rename pull requests in his repositories — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [ ] Alexander Biratka — collect MVP 2 business questions, send them by email in one thread, and raise them on these calls — due ongoing — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]

## Sept 29 2026 — capability 134 waits on a real server, and the modem reconnects

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian; label "Alexander Biratko"; he appeared late): on capability 134 "[т]ам у меня 3 фичи… открыто", all possible update tasks are done, and "последним шагом будет проверка на реальном с реальным сервером, который пока не поддерживает flexpay" — so his Sept-28 commitment to finish 134 that day is not discharged. The "GS[M]" task is still not started. On the modem: the progressive reconnected and carried on — "просто это учитывать". See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 29, 4:49 AM) and [[wiki/decisions/2026-09-17-lte-is-the-default-route-and-the-manual-override-stays.md]] (Sept-29 update) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

## Sept 29 2026 (8:06 AM) — nothing urgent on MVP 2

On the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian; label "Alexander Biratko"), asked by Klimovich about MVP 2: "я буду, если что писать… письма… как договорились… пока у меня такого именно срочного ничего нет" — he will send the business questions by email as agreed on Sept 28 (that commitment stays open above); nothing urgent that day. In segment 1 he joined the small talk (not recorded) [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Pre_Meeting_Draniki_Chat-September-29-2026.md]].

## Sept 30 2026 — capability 247 (the modem for FlexPay) connects on a SIM, and the LED service instead of the HAL

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian; label "Alexander Biratko") [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **247.** "я вчера создал новую [capability], связанную с [модемом] для flexpay. Её не было это [capability] 247"; most features done, checks left; "сегодня с утра у тебя взял. Симкарту… всё уже подключилась, то есть сеть есть"; he expects to close it that day. The Sept-29 "GS[M] task not started" is now this capability.
- **LEDs.** His analysis: the HAL library already implements the LED strip but its APIs are not exposed; FlexPay still runs on the HAL; the LED service exists in two copies (Pavel's early one, and Anton's with a Java wrapper — "я его подключаю как джава библиотеку… это будет удобнее"); "я попробую наверно уже с сервисом работать уже [с HAL] не буду бороться". Next: "работа с ледами и с переключением на сервис". See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 30, 4:57 AM).
- His Sept-28 commitments (134, Syncotek, 133, dates) were not mentioned.

## Open commitments (Sept 30 2026)

- [ ] Alexander Biratka — finish the checks and close capability 247 (modem for FlexPay) — due Sept 30 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [ ] Alexander Biratka — the LEDs on FlexPay through the LED service (not the HAL) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Sept 30 2026 (8:03 AM) — print another Flex IQ, no FlexPay cases, a burned USB port, the modem question, and sounds already on FlexPay

On the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian; label "Alexander Biratko") [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]:

- **Devices.** "Можно еще один распечатать?" — a 3D-printed Flex IQ "чтобы он был более менее законченным устройством"; for FlexPay "с корпусами у нас вообще нету… может быть гена может там чтото похожее дать?"; big parts "можно склеивать… прям как Монолит"; but without the right panel "смысла нету". His board: "со сгоревшим [USB] одной". He proposed ordering "оригинальную панель хоть одну". See [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 30, 8:03 AM).
- **The recycler** belongs to the Flex Recycler project — "какой [MVP] у нас" — Pavel: 3. See [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]] (Sept-30 update).
- **Modems.** "GSM модемы у нас будут какого?… какой модели… 2 возможных подключённых или один всётаки. Никто не знает"; new modems "надо будет протестировать… это такая важная часть". See [[wiki/decisions/2026-09-04-north-america-modem-variant-and-ask-kore-for-the-apn.md]] (Sept-30 update).
- **Sounds.** Pavel: "Саша уже со стороны даже flex pay звуки поднял… звучки красивые играют". See [[wiki/decisions/2026-09-30-flex-iq-sound-feedback-and-the-flexpay-slim-led-language-go-to-mvp-2.md]].

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Pre_Meeting_Draniki_Chat-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_QA_Automation_Strategy-September-1-2026.md]]
- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Transcript_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_1-May-12-2026.md]]
- [[raw/Meeting_Notes_nova_platform_architecture_overview-Segment_2-May-12-2026.md]]
- [[raw/Meeting_Transcript_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]
- [[raw/Meeting_Notes_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]
- [[raw/Meeting_Transcript_OMNI_Architecture_Biratko-March-30-2026.md]]
- [[raw/Meeting_Notes_OMNI_Architecture_Biratko-March-30-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]]
- [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]
- [[raw/Schedule_review-March-4-2026.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Claude Code integration - continued.md]]

- [[raw/Anton_Liashkevich_Alexander_Biratko_about_OMNI-august-28-2025.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- [[raw/OMNI schedule review.md]]
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
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Game_Change_Regulatory_Procedure-September-11-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Notes_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_EGM_Compatibility_Testing-September-25-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
