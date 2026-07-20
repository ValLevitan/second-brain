---
type: person
title: Aaron
date: 2026-07-12
aliases: [Aaron, Aron, Erin, Eric, Aaron Bockelie, aaronsb]
source-count: 69
open-commitments: 1
---

# Aaron

Aaron works with Val on JVL's product roadmap and Jira planning, and leads JVL's engineering-process modernization — the build pipeline and AI-assisted development.

## Role

- Val works with Aaron to organise JVL's products and initiatives in Jira, and to groom the 2025 plan before a team meeting. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val says he is "speaking to Aaron" about whether the Flex S cabinets should sit at the "product" level or be reorganised. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val asked Aaron to help groom the 2025 plan and attach Jira links to the high-level initiatives, aiming to be ready for a team meeting the week of the 13th. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Build-pipeline and DevOps push (Jan 13)

- On the development-pipeline call, Aaron pushed the Minsk team away from Jenkins toward a Git-native build pipeline — arguing for portability, automation, clean/disposable build environments, and full traceability, and for embedding QA in the build system rather than giving them a Jenkins control panel. [[raw/development_pipeline_january_13_2025.md]]
- He challenged whether the parameterization complexity was a real requirement or legacy baggage, and set homework to research GitHub capabilities equivalent to Jenkins. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]

## AI-assisted development lead (Jan 14)

- Aaron ran the hands-on AI-development workshop for the Minsk team, teaching VS Code + Cline + OpenRouter + MCP, the "maximizer" risk, the "70% problem," and `.clinerules`. He built a Bitbucket MCP server live. See [[wiki/topics/ai-assisted-development.md]]. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Val positioned Aaron as the current in-house expert on AI tooling but said he wants someone to eventually surpass him and lead JVL there. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- At the Jan 15 decision meeting Aaron drove the successful proposal to move JVL off Jenkins to a Git-native, "serverless" build system on GitHub, with a small set of build archetypes and post-build instrumentation. He wrote the English summary of the decisions in the meeting chat and coined "simplify and add lightness." See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]] and [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Val asked Aaron (with Pavel) to break the build-system work out into JIRA features on the board rather than run it as a side project. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Separately, the QA/test-automation consultant said his testing proposal was developed "in consultation with Aaron"; Aaron is to attend the planned testing-architecture meeting. See [[wiki/topics/test-automation-strategy.md]]. [[raw/integration_and_testing_procedures_january_15_2025.md]]

## Feature-coaching and DevSecOps grooming (Jan 16–20)

- **DTP-53 (Jan 16–17):** Aaron coached Pavel to turn the Git-native pipeline work (JIRA feature DTP-53) into proper stories and feature descriptions — playing "Scrum Master" on Jan 16, then on Jan 17 insisting features be written from the customer's perspective and documented Git-natively. He demoed prompt styles in Claude but warned against over-relying on AI. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]] [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- **FP7 bottleneck testing (Jan 17):** attended and helped drive the bottleneck questioning; Val repeatedly held Aaron up as the model of pushing him hard without worrying about his feelings. [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- **GitHub org structure + DevSecOps grooming (Jan 20):** co-coached Andrei with Val on GitHub organization structure and on aligning a Miro board with the Jira roadmap plus the ITSM operating model. See [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_organization-jan-20-2025.md]] [[raw/meeting_various-jan-20-2025.md]]

His surname is given as **Bockelie** on the Jan 21 continuous-delivery transcript. (First name may appear elsewhere transcribed as "Aron," "Erin," or "Eric.") [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]

## Continuous-delivery architecture and Minsk IT structure (Jan 21–22)

- **CD architecture (Jan 21):** with Jason, walked Val through the three-layer "everything as code" pipeline (product / environment / platform repos plus an integrator), the testing pyramid, and containers-over-disk-images; drove the group to the MVP "Hello World first" step. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]] and [[wiki/decisions/2025-01-21-build-git-native-hello-world-environment-first.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- **Minsk IT structure (Jan 22):** in a short planning call, agreed to convert the Miro board into Jira initiatives/products, shift application-support work to Dima and DevOps work to Andrei, and educate Andrei on DevOps (Andrei agreed). See [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/it_structure_minsk-jan-22-2025.md]]

## RGS integration and GitHub structure (Feb 11)

- **RGS API (Feb 11):** with Val, pushed [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] to make the RGS integrable by outsiders — a **Postman collection** and/or **OpenAPI** document, and moving the source off SVN to Git. Said JVL's API "could use a little love" before offering integration, and cited example RGS vendors (Comtrade Gaming etc.) that publish specs/examples. See [[wiki/topics/rgs-architecture-and-integration.md]]. [[raw/Aaron_Val_2025-02-11.md]]
- **GitHub repo structure (Feb 11):** co-drove the org-naming convention and migration plan — argued for human-readable, capitalised, JVL-prefixed **org** names (GitHub forms the slug) and short lowercase-hyphen **repo** names with no JVL prefix (citing the Home Assistant org and having set up **Ford**'s ~50,000 repos as his credibility). See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## GitHub access, meeting-tracking AI, and LFS onboarding (Feb 12–18)

- **GitHub access model (Feb 12):** introduced **Codespaces** (browser-hosted dev environment so code never lands locally) and the GitHub **audit log** / activity-based access-revocation pattern; argued **trust-but-verify** over trying to physically prevent copying; used **Ford**'s cloud-GitHub migration as the large-scale reference; and pushed Andrei to fix the Entra-ID/SSO admin-account issue and to use the "Well-Architected GitHub" guide + paid support. See [[wiki/topics/github-access-and-security-model.md]] and [[wiki/decisions/2025-02-12-github-repos-private-by-default.md]]. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **Meeting-tracking + cloud file architecture (Feb 17):** told Val that the source of truth for tracking a feature's progress must be GitHub (a Git repo) and demoed the GitHub **MCP** tool (branches, PRs, CI, permissions) alongside the Google Workspace tool. Then coached Val to think as a "DevOps engineer, not a user": treat your work as a product — "engineer Val" creates, "consumer Val" consumes — and **publish** distilled/consumable copies (PDF/web/Word) to OneDrive rather than syncing the original Git working repo there; GitHub stays the source of truth across devices. See [[wiki/topics/ai-assisted-development.md]]. [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]] [[raw/cloud_file_architecture_transcript_aaron-2025-02-17.md]]
- **Git-LFS / VS Code onboarding (Feb 18):** ran a hands-on session onboarding [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (and the graphics team) to VS Code + Git Graph + **Copilot** + committing via source control; quoted Copilot Business at ~$19/seat and said everyone should use it; deferred the spend decision to Val. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

## MCP automation, graphics migration, docs-as-code (Feb 21–26)

- **MCP automation ("replacing Pavel") (Feb 21):** in a short call Aaron explained that MCP servers can wrap raw API endpoints in higher-level "tools" carrying business logic (e.g. "deploy a machine to an environment"), and that the step-by-step flow a person like [[wiki/people/pavel.md|Pavel]] follows can be baked into an MCP so an AI orchestrates it — the same convention CI/CD build automation uses in GitHub. See [[wiki/topics/ai-assisted-development.md]]. [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]
- **Game/design repo split + docs-as-code (Feb 21):** in the LFS demo with [[wiki/people/lena.md|Lena]], Aaron proposed two repos per game (game + LFS design repo, joined by a git submodule; build doesn't need the comp art) and demoed docs-as-code — Markdown docs auto-rendered to a per-project website (Docusaurus/MkDocs/GitHub Docs) with Mermaid diagrams. He declared "the only source of truth is what's in git" and that his and Val's goal is to **retire Atlassian** (Confluence now, Jira in "a year or two") in favour of GitHub. He took on migrating Fortune Foo Paws' Confluence content into a GitHub docs site. See [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]] and [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Designer branching workflow (Feb 26):** coached the design team (Lena, Dima Khandov, Yulia, Anastasia) on feature/story branches, PR-only merges to `main`, and a branch-lifespan performance metric (3 days amazing → 10 days worst-acceptable) — applied to PSD files too; is building a Photoshop→contact-sheet GitHub Action; and set the plan to keep Juan/Michael out ~30 days until the core four are comfortable. See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Git progress check-in with the designers (Feb 28)

- Aaron ran a hands-on Git check-in with [[wiki/people/lena.md|Lena]], [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]] and [[wiki/people/andrey-bosik.md|Andre]] on the Fortune Foo Paws repo: put the repo-usage rules into the repo ("general instructions are better than no instructions"), **don't commit the GDD yet** ([[wiki/people/efim-podvoiski.md|Efim]]/Michael still writing it), and **clone this repo as the future game template**. He walked them through resolving a live **gitignore merge conflict** caused by direct commits to `main`, teaching that the repo owner merges PRs and that pending PRs must be ordered — and set Andre homework on the `.github` contact-sheet Action. He noted he should be used as a **consultant, not an employee**. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/Git_progress_check_in_2025-02-28.md]]

## Minsk persona / orchestration-platform workshop (Mar 10)

- Aaron co-led (with Val, in English, via a "Dima" translating) a long teaching session pushing the Minsk team toward **persona-driven, interview-based requirements** for JVL's planned new operations **orchestration platform** — reinforcing the "understand the customer, don't just re-build the software you have" theme and his earlier "you can't write monolithic software that way" point. He probed how the team gauges "feasibility medium / error cost low" tags on the reformatted persona. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/persona_development_journey_meeting_with_minsk-2025-03-10.md]]

## GitHub for graphic design check-in (Mar 12)

- Aaron handled the designers' **PSD-conflict** complaint (separate branches with separate files shouldn't truly conflict; the contact-sheet Action just runs twice on `main` — fix the script, don't debug it live with eight people) and pushed the rule that broken tooling goes into the **help-desk queue as a ticket**, connected to the PR/commit, not saved for meetings ("everybody is made the same"). He and Val told [[wiki/people/lena.md|Lena]] to **start the new-game repo now and "fake the review"** via a colleague, and to **fork from a generic template** (which [[wiki/people/andrey-bosik.md|Andrei]] must build). See [[wiki/topics/graphics-team-git-workflow.md]] and [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## SVN→Git migration of Efim's codebase (Mar 17)

- Aaron drove the plan to move [[wiki/people/efim-podvoiski.md|Efim]]'s codebase off **SVN** onto JVL's Git platform, then migrate the **Jenkins** builders to **GitHub Actions** in stages (black-box the scripts first, refine later). He framed it as understanding/documenting the code (static analysis) to improve commercial viability and cut the bus-factor risk that only Efim and [[wiki/people/igor-metelski.md|Igor Metelski]] can maintain it. See [[wiki/decisions/2025-03-17-migrate-rgs-codebase-svn-to-git.md]]. [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]

## Knowledge-base tooling and the funding arrangement (Mar 20–21)

- **Knowledge graph / tagging (Mar 20):** Aaron demoed a **3D force-directed graph** and D3 tree-map/chord/calendar views of a document set, critiqued Val's Cline/ChatGPT tagging pass as too simplistic, and proposed a **SQL database + Markov/Bayesian n-gram** classifier. As a **GitHub admin for JVL**, he had Val push ~171 tagged files to a new `text_analysis` repo and took on writing the classifier/visualizer. See [[wiki/topics/transcript-knowledge-base-tooling.md]]. [[raw/aaron_3d_force_directed_graph-March-20-2025.md]]
- **Building tools (Mar 21):** flagged OpenAI's new **GPT-4o Transcribe** models (shared by [[wiki/people/clayton-chancey.md|Clayton]]) to replace Whisper (diarization, longer files), noted Whisper's file-size limit and a possible splitter, and demoed running the Whisper MCP. He and Val agreed the arrangement where **Val funds guaranteed hours** for Aaron + Clayton to build bespoke AI tools that Aaron may then commercialise — part of Aaron's enterprise-AI-architecture consultancy (an alternative to **CPRIME**), tools to live in a "Foray" GitHub space. See [[wiki/decisions/2025-03-21-fund-aaron-clayton-bespoke-ai-tools.md]] and the transcription section of [[wiki/topics/ai-assisted-development.md]]. [[raw/aaron_building_tools-march-21-2025.md]]
- **Tagging science (Mar 21):** detailed the classification method (emergent no-hint AI tagging, term normalization, rare-tag "departures" as data-science signal, AI as a first-order thinking tool, an MCP pointed at the database, later vectorization) using his Chase bank-statement categorization project as the model; rejected an off-the-shelf docs-RAG MCP and is building his own. See [[wiki/topics/transcript-knowledge-base-tooling.md]]. [[raw/aaron_tagging_science-march-21-2025.md]]

## "Making use of knowledge" + Open WebUI install (Mar 26)

- Aaron drew out **why** Val wants his corpus mined (trends/direction over retrieval; the graph-database trade-off) and then screen-shared to **install Open WebUI** on Val's laptop from scratch — a GitHub gist → `git init` (teaching Val what a repo is) → a `docker-compose.yaml` pulling the **`open-webui:cuda`** image with a persistent volume and Watchtower → installing the **NVIDIA Container Toolkit / CUDA drivers** so the laptop GPU can do the RAG/vector-DB work. He suggested it might run better centrally (JVL's AWS/Azure, via "Andrea" — likely Andrei Bosik). See [[wiki/topics/ai-assisted-development.md]], [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/meetings/2025-03-26-aaron-knowledge-visualization-openwebui.md]]. [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]

## Open WebUI setup + MCP-design lesson (Mar 27)

- Aaron screen-shared to configure a self-hosted **Open WebUI** on Val's laptop end-to-end (settings, memory, models, web search via DuckDuckGo, image generation, connecting OpenAI's Whisper-1 and importing the **Anthropic** function so both Claude and GPT models are available in one UI), flagged that it could be deployed on **JVL's Active Directory** to replace individual ChatGPT accounts, and noted OpenAI had just adopted **MCP** across its products. He closed with a lesson on **good-vs-bad MCP-server design** (raw-endpoint vs consolidated-tool vs stateful/suggesting), and had cancelled a Minsk meeting to focus on it. See [[wiki/topics/ai-assisted-development.md]] and [[wiki/meetings/2025-03-27-openwebui-aaron-setup.md]]. [[raw/OpenWebUI_aaron_march-27-2025.md]]

## RGS Git session + vector-DB teaching day (Mar 31)

- **RGS migration session:** drove the plan to make the freshly-cloned RGS "whole on GitHub" — assigned [[wiki/people/igor-metelski.md|Igor Metelski]] the local-build task and a findings log, taught him git submodules, read the SVN `Checkout All` batch file into a repo map (MathEngine etc.), and challenged JVL's dev/prod "artificial wall" (agreeing to a one-on-one with [[wiki/people/efim-podvoiski.md|Efim]] on running the RGS in future). See [[wiki/decisions/2025-03-17-migrate-rgs-codebase-svn-to-git.md]] and [[wiki/meetings/2025-03-31-rgs-git-migration-working-session.md]]. [[raw/rgs_git_migration-march-31-2025.md]]
- **Vector-DB / Open Semantic Search session:** walked Val through where Open WebUI stores his vectorized transcripts, the internal-vs-Pinecone/Chroma trade-off, semantic search and diarization limits, and attempted an Open Semantic Search (Apache Solr) install via Cline — unfinished (Solr 503). See [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/meetings/2025-03-31-vector-db-second-brain-session.md]]. [[raw/vector_meeting_db-march-31-2025.md]]
- **Consulting-spend calculus:** showed Val his own AI usage — "I spent $1,300 over the last four months on my account"; "A lot of what you're paying me, I'm turning back into this to make sure that I can do things correctly and faster... I can do it real slow by myself, by hand, or we can do it really fast." He recommended JVL issue **separate API keys per developer** to measure adoption, and delivered the farmer/combine and dark-forest adoption arguments — see [[wiki/topics/ai-assisted-development.md]]. [[raw/vector_meeting_db-march-31-2025.md]]

## DevOps container approach for Omni (Mar 24–25, dates inferred)

- Led the two-day Miro design of the Omni-era repository/versioning/pipeline structure — the "printing press for games" model, the no-commits-to-main rule, the core-advancement manifest-of-tags concept, and (with Val) the frozen-capabilities golden rule; opened by demoing an AI that wrote and tested a small game for him in ~20 minutes ("It's the fact that I didn't code it… I'm not really a software developer"). He also disclosed he contributes to the **Open Web UI** open-source project — mostly by writing tests. See [[wiki/topics/omni-core-advancement-and-game-templating.md]] and [[wiki/decisions/2025-03-24-freeze-core-capabilities-before-game-production.md]]. [[raw/devops_container_approach_for_omni.md]] [[raw/devops_container_approach_for_omni_3.md]]

## InfoSec evening call (~Mar 19, date inferred)

- Coached Val on secrets-management platform selection and the DevSecOps framing ("DevOps is actually DevSecOps"), and offered his InfoSec network: **John Luke Peck**, Deputy CISO at **Critical Insight** (Aaron's former boss at a nuclear-engineering company) — Aaron pushed for an official Critical Insight engagement with himself staying as independent advisor. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/info_security_server_infrastructure.md]]

## Vector-DB tooling continued — N8N/Pinecone then Verba/Weaviate (Apr 15, Apr 23)

- **N8N + Pinecone (Apr 15):** screen-shared to build a RAG document-chatbot over Val's transcripts using the **N8N** automation platform + a **Pinecone** vector index + Google Drive + OpenAI embeddings/GPT-4o-mini; taught the embedding-model-must-match-the-index and input-sanitization lessons. See [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/meetings/2025-04-15-n8n-pinecone-rag-setup.md]]. [[raw/pinecone_n8n_transcript_setup-apr-15-2025.md]]
- **Verba/Weaviate + cloud hand-off (Apr 23):** demoed the open-source **Verba** RAG app on the **Weaviate** vector DB against ~384 of Val's transcript documents, walked Val's company-wide-knowledge-base thesis, and — when Val asked to scale it beyond his laptop — brought in [[wiki/people/andrey-bosik.md|Andrei Bosik]] to run it on JVL's AWS cloud in Docker; his **personal email aaronsb@gmail.com** was given for the doc-archive share. Also helped install the **Confluence MCP** on Val's laptop and reaffirmed the "run MCPs as Docker, not Node.js, so Watchtower keeps them current" rule. See [[wiki/topics/transcript-knowledge-base-tooling.md]] and [[wiki/meetings/2025-04-23-verba-weaviate-company-knowledge-base.md]]. [[raw/aaron_vector_knowledge_base-apr-23-2025.md]]

## Open commitments

- [ ] Aaron — introduce Val to John Luke Peck / Critical Insight and schedule the call — due unspecified — [[raw/info_security_server_infrastructure.md]]

## History — 2024 and earlier (sources staged 2025-03-29)

- **Test-360 progress review (Fri Jul 5 2024, date inferred; pre-window, queued):** taught Val and Anton TDD (Gherkin/JUnit fizzbuzz via ChatGPT), pushed branch time-limits, coverage-metric definitions, OmniFramework-first scope, and showed SonarQube while resisting premature tool adoption; estimated real code coverage "more than a year." The session where Val coined "test 360 culture." See [[wiki/topics/test-automation-strategy.md]] (History). [[raw/test-360_progress_review_meeting.md]]
- **JVL Insights (~2023–24):** Aaron's earliest recorded JVL engagement — named **"Aaron Bockelie (Atlassian Specialist) - Consultant"** in the JVL Insights knowledge-base proposal, scoped to integrate it with JIRA/Confluence, set up project-tracking/documentation workflows, and train the team on Atlassian tools. See [[wiki/projects/jvl-insights-knowledge-base.md]]. (Compensation figures in the source withheld, §15.8.) [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- **SQL/OLAP visualization architecture (~2024, likely Q4):** on the broader architecture session he proposed the low-hardware alternative to Pavel's SAS-host designs — commodity serial→Ethernet converters plus a **container host with virtual serial-adapter drivers**, cloud-deployable, "turn everything into casino as a service" — and pressed the team on SAS's acknowledgement/retry robustness. See [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/meetings/2024-sql-olap-visualization-architecture-2.md]]. [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]

## Apr 16 2025 — IT secrets/assets meeting + AI-tooling knowledge share

Two sessions Aaron led/hosted. (1) A short IT meeting on the **assets schema** (link user records via Microsoft Entra + Atlassian Discovery to machines with a last-logged-in-user automation) and a **secrets server** (adopt a Microsoft/Azure secret server; manage secrets as assets with Atlassian Automation granting time-boxed access) — see [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. Aaron bookable Friday 8–10 am ET. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]] (2) The bi-weekly AI-tooling knowledge share: his own **Jira MCP** (bi-directional, sprint management) replaces the buggy third-party Atlassian MCP; also demoed a memory-graph MCP and a Comfy UI MCP; recommended moving to the Docker version; homework = generate content with Comfy UI + an MCP, demo in two weeks. Detail on [[wiki/topics/ai-assisted-development.md]]. [[raw/mcp_experiences_tech-apr-16-2025.md]]

## GitHub↔Jira "capability" mapping (Apr 1–2 2025)

Across two sessions Aaron worked Val through how code actually relates to Jira, resolving the Mar-31 alignment homework. **Apr 1:** set the rule that a **repository is never a product** ("a product is an artifact in motion") and pushed to **flatten JVL's many GitHub orgs into one** with a naming convention (citing Block/Square, Home Assistant) — Val resisted. **Apr 2:** diagrammed monolithic-vs-multi-repo reality, showing **one Jira feature spans multiple GitHub branches**, which led Val to adopt a **Jira "capability"** level as the demonstrable executive unit. Val also credited Aaron with the **Jira/Atlassian MCP** that lets him interrogate features/capabilities in plain language. Full detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/git_jira_correlation-april-1-2025.md]] [[raw/gut_hub_jira_relationship-april-2-2025.md]]

## Apr 24 & 30 2025 — ECHO ITSM design; secrets-management framework

- **Apr 24:** Aaron designed the **"JVL Home" Jira Service Management + Confluence** ITSM setup for the legacy amusement base (polar-bear-themed portal, knowledge-base-first, funnel resolved cases back as "equity"). See [[wiki/topics/echo-home-gaming-device.md]]. [[raw/echo-home_jira-service-apr-24-2025.md]]
- **Apr 30:** on the secrets-management session ([[wiki/meetings/2025-04-30-secrets-management-strategy.md]]) Aaron pushed "define the why first," generated a **value-perspective doc + a maturity self-assessment framework** via an MCP "thinking"/sequential-reasoning server on his GitHub (published as a container), and coached starting with GitHub CI/CD and AWS/Jenkins keys, OAuth over static API keys. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/secrets_server-apr-30-2025.md]]

## May 1 2025 — Miranda organizing + the Unity question

- **Organizing Miranda ([[wiki/meetings/2025-05-01-organizing-miranda-github.md]]):** Aaron met Dmitriy Khandov (~Apr 29) and recapped to Val an action list to clean up the Miranda repo (`.gitignore`, purge logs/libraries, delete stale branches, a packaging/zip strategy) before opening a feature branch to fold the math emulator back in; the emulator may move to its own repo/product (undecided). He was candid that he wasn't sure Dima had fully understood. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/organizing_miranda_github-may-1-2025.md]]
- **Unity-instead-of-Miranda ([[wiki/meetings/2025-05-01-unity-instead-of-miranda.md]]):** with Val, Aaron probed Sasha on adopting Unity (now free of per-install fees) in place of Miranda; Aaron noted C# can be compiled on Linux with no OS-license cost. No decision. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/unity_instead_miranda-may-1-2025.md]]

## May 5–6 2025 — feature/capability granularity + Miranda follow-through

- **Feature granularity (May 5–6):** across three sessions ([[wiki/meetings/2025-05-05-feature-granularity-aaron.md]], [[wiki/meetings/2025-05-06-feature-jira-defining-and-reflection.md]]) Aaron deepened the capability model for Val — a **feature is temporary** (falls away when delivered) while the **capability is the permanent product description** whose legacy is its requirements + embedded tests; introduced **component** (a cluster of features) and the **double-diamond** (discover→define→develop→deliver); insisted features be **demonstrable in ~2 weeks** with a passing test as the minimum proof; and explained **Jira Product Discovery** (grown from Jira Align) as the home for the above-feature levels. Triggered by [[wiki/people/anton-leshkevich.md|Anton]]'s over-large LGS196 story and a board of ~100 open features. No ruling. Detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/feature_granularity_definition_aaron-may-5-2025.md]] [[raw/feature_defining_jira-may-6-2025.md]] [[raw/feature_reflection_jira-may-6-2025.md]]
- **Miranda GitHub follow-through (May 6):** reviewed the cleanup [[wiki/people/dmitriy-khandov.md|Dima]] had done and coached packaging (NuGet/MSI), a README "TLDR" structure, Unity-style capability docs, verbose PRs, branch deletion, and a rebase to purge the ~782k-line history; framed good docs as a "value multiplier." See [[wiki/topics/miranda-authoring-tool.md]] and [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/miranda_organization_github-may-6-2025.md]]
- **"The reason for Miranda" (May 6):** with Val probing whether free Unity makes Miranda unnecessary, Aaron "sold" Miranda as a Unity-nestled tool that mocks up JVL's slot games and connects them to the JVL backend. No ruling. See [[wiki/topics/miranda-authoring-tool.md]]. [[raw/the_reason_for_miranda-may-6-2025.md]]

## May 7 2025 — IT-maturity coaching + games-design tool adaptation

Two Aaron-led sessions this day. **IT maturity** ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]): he coaches [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrei]] to move IT from reactive to planned work, using the still-open secret-server choice to teach a first-principles chain (information-security policy → risk register → requirements → a weighted product-scoring matrix); homework to write risks/policy/requirements and score Azure Key Vault / AWS Secrets Manager / HashiCorp Vault / Delinea. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/it_department_maturity-may-7-2025.md]] **Games-design tools** ([[wiki/meetings/2025-05-07-games-design-ai-tools-adaptation.md]]): the bi-weekly practice session with Lena/Anastasia/Yulia/Dima Khandov on the Cline agent + his custom Confluence/Jira MCP and ComfyUI — he directed a switch to Docker-native MCP, explained Cline's coding bias (good at Git, poor at Confluence/Jira admin), and floated a separate authoring-vs-administrator Confluence MCP. See [[wiki/topics/ai-assisted-development.md]]. [[raw/tools_adaptation_games_design_department-may-7-2025.md]]

## May 8 2025 — capability/Compass + internal MCP servers

A three-segment Aaron↔Val strategy session ([[wiki/meetings/2025-05-08-capability-compass-mcp-aaron-session.md]]): Aaron introduced **Atlassian Compass** as the engineer-side "second diamond" that connects code feature-branches back to a project's components/capabilities (opposite Jira **Discovery**); worked the product→capability→feature philosophy on JVL core technology (see [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]); and pitched JVL **writing/maintaining its own MCP servers** as production tooling — MCP as a *specification* not a product, D-Bus/COM/AppleScript system-interface adapters, an in-stack Omni MCP class (naming [[wiki/people/alexander-biratka.md|Alex Baratka]] to write it), and AI-augmented QA via Gherkin. See [[wiki/topics/ai-assisted-development.md]]. [[raw/product_capability_feature-may-8-2025.md]] [[raw/discovery_tracking_capabilities_compass_jira-may-8-2025.md]] [[raw/mcp_servers_for_jvl-may-8-2025.md]]

## May 9 2025 — memory-graph MCP setup + the product taxonomy

Two same-day sessions. (1) **Memory-graph MCP setup** ([[wiki/meetings/2025-05-09-memory-graph-mcp-setup-aaron.md]]): Aaron screen-shared to install/configure his own **memory-graph MCP server** in VS Code + Cline for Val — single-file SQLite mode, backup-by-copying-the-`.db`, three storage modes; he wrote the tool himself. (2) **Product-capability-feature taxonomy** ([[wiki/meetings/2025-05-09-product-capability-feature-taxonomy-aaron.md]], ~162 min): Aaron pressed Val to define **portfolio** first while Val insisted on starting from **product** ("where do I make money?"); together they built the value-stream/product taxonomy and Aaron used his **directed-graph/visualizer tool in Claude Desktop (Claude Max subscription)** to synthesize a draft Jira-config document, then installed **Claude Desktop on Val's Linux** machine. Detail on [[wiki/topics/ai-assisted-development.md]], [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]] and [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/ai_aaron-may-9-2025.md]] [[raw/product_capability_feature_development-may-9-2025.md]]

## May 12 2025 — product-discovery coaching + the Miami product-manager hire

On the ~207-min product-discovery session ([[wiki/meetings/2025-05-12-product-discovery-double-diamond-aaron.md]]) Aaron taught Val the **double-diamond** discovery→capability→feature→story flow (Jira Product Discovery, effort-vs-impact scoring), worked a FlexPay capability example, and demoed a **Goose** multi-agent setup + explained **semantic ontology** (both on [[wiki/topics/ai-assisted-development.md]]). [[raw/theory_product_discovery_process-may-12-2025.md]]

- **The product-manager hire:** Aaron told Val he still needs a **human product manager** (agency is the missing AI piece — "in a year you might not"), had AI draft a **job description** (engineering mindset, covering all parts of a casino gaming system) and pull **reference executive profiles** (names surfaced: Noah Akers, Matt Wilson, Gerard Crosby, "Tashna," "Les" — people at Konami / Light & Wonder; Val thought them too senior). Aaron argued the PM should be a **real human physically located in Miami**, near Val. (These reference names are AI search results, not JVL people — no pages created.) [[raw/theory_product_discovery_process-may-12-2025.md]]

## May 15 2025 — the PDFX report-ingestion tool + SurfSense

On a short three-segment session ([[wiki/meetings/2025-05-15-ai-aaron-pdfx-surfsense.md]]) Aaron showed the **working PDFX tool** ("PDF access") he built to turn a sectioned PDF into a structured per-page index + extracted text for insertion into the memory-graph database (demoed on four by-state gaming-report PDFs), flagged the open-source local tool **SurfSense**, and walked Val through running `PDFX process <in> <out>` in a terminal. The working build of the May-14 dictated pipeline. Detail on [[wiki/topics/transcript-knowledge-base-tooling.md]]. [[raw/ai_aaron-may-15-2025.md]] [[raw/ai_aaron-may-15-2025 (1).md]] [[raw/ai_aaron-may-15-2025 (2).md]]

## May 28 2025 — IT-maturity review: Delinea selection

On the maturity review ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]) Aaron observed the IT team's progress (policy in Confluence, risk-mapping, product scoring) and validated **Delinea as the scored winner to trial** (see [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md]]). He coached them to build an executable DTP backlog with expected outcomes *before* starting ("call the par before you play the hole… you can say how long it'll take before you even begin"), pointed them at using AI grounded on their own policy to draft the stories, and framed the whole exercise as first-principles IT maturity — policy/plan first, infrastructure after. He gave the "before vs now" executive summary Val asked to have on record. [[raw/it_maturity_update-may-28-2025.md]]

## June 12 2025 — QA-engineering direction review

On the [[wiki/meetings/2025-06-12-qa-engineering-direction-aaron.md|QA-engineering show-and-tell]] Aaron course-checked JVL's in-house TypeScript test framework ([[wiki/people/anton-leshkevich.md|Anton]]'s Page-Object-Model + LGS-XML-abstraction framework; Irina's Jira↔X-Ray test linkage). His guidance: adding the abstraction layer is right but is "the beginning of retiring XML"; **when test-language ≠ component-language you're limited to integration tests** (decide by which language holds the majority of the app); and his headline doctrine — **chase "capability coverage," not code coverage** (measure mean-time-to-resolution and documented-capability coverage). He suggested GitHub PR templates/checklists as soft reminders and shared a 5W1H memo. See [[wiki/topics/test-automation-strategy.md]]. [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]

## Aug 12 2025 — Figma-to-testing workflow explainer

- On a short explainer ([[wiki/meetings/2025-08-12-figma-to-testing-workflow.md]]) Aaron laid out the **Figma → React → automated visual-regression testing** workflow: a Figma prototype is the design reference ("like CAD"), exported into React pages checked into source control as the real UI, then **TypeScript tests via a testing framework** acquire the running app's visual presentation and compare it to the Figma reference (mismatch = failing test), plus invoking each UI element to confirm it reacts correctly in React (Netflix as the worked example). See [[wiki/topics/test-automation-strategy.md]]. [[raw/figma_to_testing_transcript.md]]

## Aug 14 2025 — backend-architecture kickoff (advisory)

- On the [[wiki/meetings/2025-08-14-backend-architecture-cms-transactional-hhr.md|backend-architecture kickoff]] Aaron acted as the process advisor: he had **synthesized ~2 years of Val's recordings into a CMS knowledge-base repo** (the "CMSNG/NgCMS" architectural design doc + speculative GitHub issues); reframed the monolithic legacy CMS problem (MS SQL, single-thread locking, tribal knowledge); and pushed the group's method — **capabilities-driven, "don't create the solution while writing the spec," terminology discipline ("database vs data lake"), ETL-for-the-software-stack migration thinking, docs-in-repo (Mermaid), and IEEE-style architecture documentation "as a framework, not a mandate."** He warned "speculative feature development is very expensive," and recounted his Fujitsu/Verifone POS provisioning/encryption model as the hot-swap pattern. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] and [[wiki/decisions/2025-08-14-backend-architecture-block-diagram-first-mvp.md]]. [[raw/backend_architecture-august-14-2025.md]]

## Aug 15 2025 — Keeper: forcing-function governance

On the [[wiki/meetings/2025-08-15-keeper-install-authorization.md|Aug-15 session]], Aaron refused to relitigate the Keeper choice ("I don't want to make this a debate about Keeper… are you confident you're fulfilling the requirements defined for the company?") and gave [[wiki/people/andrey-bosik.md|Andrei]] the **"cover-your-own-back" forcing-function** framing: Keeper becomes the single password store, IT gains justification to delete/rotate any password not in it, and access is conditional — "there is no such thing as *do you want to use Keeper?* … I use Keeper. You will use it too, because that's the only way I'm going to give you my password." He set the governance homework: a plan for how Keeper is implemented, measured, sustained, governed, and adopted. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/keeper_security_implimentation_IT_maturity-august-15-2025.md]]

## Sources

- [[raw/figma_to_testing_transcript.md]]
- [[raw/backend_architecture-august-14-2025.md]]
- [[raw/qa_engineering_direction_review_aaron-june-12-2025.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/it_maturity_update-may-28-2025.md]]
- [[raw/git_jira_correlation-april-1-2025.md]]
- [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/integration_and_testing_procedures_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/dtp-53_feature_planning_meeting_january_16_2025.md]]
- [[raw/dtp-53_action_builder_pipeline_definition_of_features_january_17_2025.md]]
- [[raw/fr-7_identifying_bottlenecks_in_performance_during_testing_january_17_2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/meeting_various-jan-20-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/it_structure_minsk-jan-22-2025.md]]
- [[raw/Aaron_Val_2025-02-11.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Check_in_on_GitHub_2025-02-12.md]]
- [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]]
- [[raw/cloud_file_architecture_transcript_aaron-2025-02-17.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
- [[raw/persona_development_journey_meeting_with_minsk-2025-03-10.md]]
- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/reversing_distilling_from_ready_code_into_requir_2025-03-17.md]]
- [[raw/aaron_3d_force_directed_graph-March-20-2025.md]]
- [[raw/aaron_building_tools-march-21-2025.md]]
- [[raw/aaron_tagging_science-march-21-2025.md]]
- [[raw/OpenWebUI_aaron_march-27-2025.md]]
- [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]
- [[raw/rgs_git_migration-march-31-2025.md]]
- [[raw/vector_meeting_db-march-31-2025.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/devops_container_approach_for_omni_3.md]]
- [[raw/info_security_server_infrastructure.md]]
- [[raw/test-360_progress_review_meeting.md]]
- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- [[raw/mcp_experiences_tech-apr-16-2025.md]]
- [[raw/pinecone_n8n_transcript_setup-apr-15-2025.md]]
- [[raw/aaron_vector_knowledge_base-apr-23-2025.md]]
- [[raw/echo-home_jira-service-apr-24-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/organizing_miranda_github-may-1-2025.md]]
- [[raw/unity_instead_miranda-may-1-2025.md]]
- [[raw/feature_granularity_definition_aaron-may-5-2025.md]]
- [[raw/feature_defining_jira-may-6-2025.md]]
- [[raw/feature_reflection_jira-may-6-2025.md]]
- [[raw/miranda_organization_github-may-6-2025.md]]
- [[raw/the_reason_for_miranda-may-6-2025.md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/tools_adaptation_games_design_department-may-7-2025.md]]
- [[raw/product_capability_feature-may-8-2025.md]]
- [[raw/discovery_tracking_capabilities_compass_jira-may-8-2025.md]]
- [[raw/mcp_servers_for_jvl-may-8-2025.md]]
- [[raw/ai_aaron-may-9-2025.md]]
- [[raw/product_capability_feature_development-may-9-2025.md]]
- [[raw/theory_product_discovery_process-may-12-2025.md]]
- [[raw/ai_aaron-may-15-2025.md]]
- [[raw/ai_aaron-may-15-2025 (1).md]]
- [[raw/ai_aaron-may-15-2025 (2).md]]
- [[raw/keeper_security_implimentation_IT_maturity-august-15-2025.md]]
