---
type: person
title: Aaron
date: 2026-07-12
aliases: [Aaron, Aron, Erin, Eric, Aaron Bockelie, aaronsb]
source-count: 118
open-commitments: 2
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

## Feb 9–10 2026 — per-engineer Claude Code onboarding (Chudinov, Yavorski)

- **Feb 9 — Chudinov onboarding** ([[wiki/meetings/2026-02-09-claude-code-onboarding-chudinov.md]], 1h46m, Pavel translating): Aaron coached back-end architect [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] on **language models as "the new compiler layer"** — write intentions/specs, build developer-experience guardrails (linters, static analysis, tests, doc strings) that carry the context, and codify conventions as Claude Code **"ways" (why) vs "skills" (how)** rather than reading every line by hand. He named **Python Vulture**, **cyclomatic complexity**, **Simian/SonarQube**, and a **`make`/lint** line-count pass; demoed his own **memory-graph acceleration** project (Rust cache over a Postgres graph DB, 5M-node L-system benchmark); pitched a command-line **ADR tool** as one-step, text-native architecture memory and the **Claude↔Gemini "cross-examination"** method; and generated a spring-coding-conventions doc into `docs/` (not `CLAUDE.md`, "too big"). Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-9). §15.8 clear (Aaron coaching "very expensive," vendor economics; no figure). [[raw/Claude_Code-Dzmitry.md]]
- **Feb 10 — Yavorski knowledge transfer** ([[wiki/meetings/2026-02-10-claude-code-yavorski-knowledge-transfer.md]], ~7m): [[wiki/people/eugine-yavorski.md|Yavorski]]'s Claude Code attempt built but did the wrong thing (logs to console) for lack of a **spec**; Aaron: "the JIRA issue became the specification." When Val reframed it as a **one-time knowledge transfer** from the contractor so JVL owns the project, Aaron proposed (and Val accepted) to **clone all of Yavorski's repos, set up the framework himself, and write pull requests for Yavorski to review** — starting from the JIRA issue. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-10). [[raw/Claude_Code-Yavorski.md]]

## Open commitments

- [ ] Aaron — introduce Val to John Luke Peck / Critical Insight and schedule the call — due unspecified — [[raw/info_security_server_infrastructure.md]]
- [ ] Aaron — clone all of Yavorski's FlexPort/FlexPay repos, set up the framework himself, and write pull requests for Yavorski to review (one-time knowledge transfer to JVL) — due unspecified — [[raw/Claude_Code-Yavorski.md]]

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

## Aug 18 2025 — git meta-analysis repository

On a short Val↔Aaron check-in ([[wiki/meetings/2025-08-18-git-meta-analysis-repo.md]], 2:04pm) Aaron reported a **meta-analysis repository** he configured — kept **local, deliberately not committed into JVL**, connecting **every JVL repo as a submodule** in an org with per-repo instructions, protected by a **git hook against accidental write-back** so analysis reports can be deleted and a **clean sub-agent parallel analysis** re-run. A prior "Flex"-focused run was "tainted" by context about an upcoming demonstration; he proposes re-running on a **fresh cloud instance with no prior context**. Val plans to rename the recurring meeting to "GitHub intelligence." [[raw/undertakings_git_intelligence-august-18-2025.md]]

## Aug 19 2025 — figma-to-development / testing debate

On the [[wiki/meetings/2025-08-19-figma-to-development-testing.md|Aug-19 working session]] (the fuller follow-up to his Aug-12 explainer) Aaron pressed the QA/UI team past the "Figma can't do it" standoff: define **what makes generated code acceptable** so a code-generation step (AI or deterministic) can produce the React code **and** the parallel integration tests in one flow — the real problem being QA capacity and the missing mock-up→code→test link. He argued JVL may be "using Figma in a way it wasn't designed to be used." See [[wiki/topics/test-automation-strategy.md]]. [[raw/figma_to_testing_development .md]]

## Aug 2025 (date inferred) — serverless SRE demo + the "two cultures" operating model

On an undated strategy 1:1 ([[wiki/meetings/2025-08-15-aaron-val-two-cultures-operating-model.md]]; month inferred ≈ Aug 2025, day a placeholder, QUEUED) Aaron and Val worked through how to structure JVL's engineering org and infrastructure. [[raw/Aaron + Val.md]]

- **Serverless "AI-as-SRE" demo.** Aaron showed a practice WordPress site (**graphattract.io**) running **serverless on Google Cloud Run** — deploy a Docker image, auto-scaling, a **$50 budget cap**, and a **coding agent configured with prompts/roles/GitHub access to act as the site-reliability engineer** — arguing this collapses a "3-month deploy" to a couple of days and directly supports the plan to move JVL's **IT infrastructure off Belarus**. His thesis: an SRE's traditional VM/OS-patch stack can be discarded ("we don't need a server anymore"); the barrier is people's 20-year thinking mold, not the technology. [[raw/Aaron + Val.md]]
- **The "two cultures / collective exceptionalism" model (Aaron's frame, Val's conclusion).** A structural place for both sides: a **North-American product/customer-facing engineering layer** (Aaron named "the Wills, the Nathans, the Aarons") that defines the WHY, the value proposition, monetization, deployment and governance; and the **Minsk/Belarus (and Aaron's Ukraine-Polish) "binary" execution teams** who "just live in" the intricate systems. Each admits its shortcomings; a **buffering layer** sits between "how we want things designed" and "their binary calculation." Aaron's read: Minsk "will never change / only slowly, forcefully, not naturally" and won't fully integrate — so the model is complementary specialization, not assimilation. [[raw/Aaron + Val.md]]
- **Software is ~20% of the problem.** Aaron: writing the code is "only 20%"; the other ~80% is why-we're-doing-it, monetization, deployment, orchestration, and governance — which is why product/customer-facing people are needed above the coders. [[raw/Aaron + Val.md]]
- **Repositioning Pavel to a feature-level lead.** Val floated "de-promoting" [[wiki/people/pavel.md|Pavel Frolov]]; Aaron reframed it as a **promotion in Pavel's own eyes** — narrow him to a tighter box (write his stream-of-consciousness notes **inside the GitHub projects / issues / code he's changing**, where an AI coding agent "vacuums it up" to stay on track), let him deliver **features off a feature branch** that [[wiki/people/nathan-carver.md|Nathan]] and [[wiki/people/will-jones.md|Will]] then hold to defined delivery expectations (docs, tests, integration), syncing the feature branch back to the **capability**. Pavel must adopt AI coding tools "like the farmer who won't use the tractor" — or that is eventually his exit. Val noted Pavel is already excited about **GitHub Actions** (an inventory of accumulated builders to be moved into Actions — a Pavel proposal). [[raw/Aaron + Val.md]]
- **Hiring rule (Val's takeaway, Aaron endorsed).** Don't put a "sweet-talking, good-writing" non-coder into a Will/Nathan product-engineering seat — hire a **"recovering engineer"** who found "the enlightenment of defining how to engineer" and **can still code** (could do the other side's job, if slowly). And, as a rule of thumb "for now," such leads should be **North American** (Canada/US/Mexico) — Val ruled out Europeans; South Korea "too rigid," Mexico "too different a culture," Brazil "starting to look like Europe" — "purple unicorns otherwise." [[raw/Aaron + Val.md]]

## Aug 26 2025 — the "drop user stories, spec from recorded conversation" session

On a late one-on-one ([[wiki/meetings/2025-08-26-jira-github-spec-drop-user-stories.md]], 7:32 PM) Aaron argued out the requirement-vs-business-case ordering with Val (his position: in scaled-agile the business use case is captured first, and you don't inject other parties' legislative requirements into your own tracking system) and wrote a top-to-bottom **meta-requirements ladder** (business use case → requirements → capabilities/epics → features → user stories → tasks). When Val concluded JVL **cannot produce user stories** and should replace them with **AI-interpreted specifications distilled from recorded developer conversations**, Aaron agreed to "eviscerate" the user-story layer — move items into **GitHub as issues**, stop allowing user stories in Jira — building the "JVL variant" of the Aug-22 Spec-Driven Development Process. Detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/Git_JIRA_spec.md]]

## Sept 5 2025 — Copilot Studio + MCP-to-Atlassian push

On a short call ([[wiki/meetings/2025-09-05-copilot-mcp-atlassian-microsoft-tenant.md]], 1:57 PM) Aaron — having "a lot of success" with **Microsoft Copilot** across his documents/emails/Teams — pushed to make **Copilot Studio** available for JVL so the team can build **Copilot agents with MCP access to Atlassian** (to interact with, and later verify the configuration of, JVL's Atlassian platform). He framed the enabling step as making [[wiki/people/dmitri-kovalchuk.md|Dmitri]] responsible for JVL's Microsoft/365 tenant. See [[wiki/topics/ai-assisted-development.md]] (Sept-5). [[raw/copilot_mcp-september-5-2025.md]]

## Sept 10 2025 — minimum-viable architecture for the January POS

On a coaching 1:1 ([[wiki/meetings/2025-09-10-minimum-architecture-pos-deployment.md]], 12:42 PM) Aaron helped Val decide how far to push a fast "old-fashioned" POS for January without derailing the transformation. His frame: every work unit is **curation → analysis → decision**, and **"variety"** (breadth of experience) means the analyst works narrower than the curator/decider — so a request must contain the recipient's experience, and **"productive doubt"** (code reviews, demos) is the friction that grows understanding ([[wiki/people/dmitri-chudinov.md|Dima Chudinov]], the principal back-end architect, should challenge *why* each requirement exists). His guidance: write **requirements** (a performance envelope — "50,000 players," ~100 concurrent transactions) not specs; call the 3–5-yr vision an **"architectural goal,"** not architecture; deliver a **"minimum viable architecture"** for POS (must not calcify); and **don't build a serverless/microservices payment system from scratch in ~4–5 months** — adopt a validated design pattern and iterate. As executive Val mandates the constraints (serverless, cloud-first, no monolithic SQL, understandable by others) with [[wiki/people/nathan-carver.md|Nathan]] shaping them; the **InComm validation service** is a static anchor. Iron triangle: fast/cheap/good, pick two. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-10). [[raw/Minimum_Architecture_POS_deployment_planning-september-10-2025.md]]

## Sept 16 2025 — payment-hub blueprint review: "specification of specifications"

On the [[wiki/meetings/2025-09-16-backend-blueprint-payment-hub-review.md|Sept-16 blueprint review]] (1:03 PM, with Val + Pavel + Nathan) Aaron played the process advisor on how JVL should write specs. He surfaced the formal frameworks — **TOGAF** (The Open Group), **ArchiMate**, **PlantUML**, **ISO** requirement/spec standards — but judged them **not a match** for JVL's size and the January deadline ("you'll be spinning months writing all the specs; it will not let you hit January 1st"). His steer: distil an **informal, smaller** interpretation — an internal agreement on "what we consider a specification," not ISO certification. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Sept-16). [[raw/back-end_architecture_blueprint_review.md]]

## Jan 29 2026 — Clayton's MCP-tools working session

On the [[wiki/meetings/2026-01-29-jvl-working-session-mcp-tools-demo.md|working session]] where his colleague [[wiki/people/clayton-chancey.md|Clayton Chancey]] demoed the custom JVL Atlassian MCP tools (with Val and [[wiki/people/lena.md|Lena]]), Aaron shared Clayton's "AI-augmented" framing: with enough high-quality context scaffolded intelligently, an LLM can judge which pieces to automate and how — judgment-informed augmentation, not blind automation. Substance on [[wiki/people/clayton-chancey.md]]. [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]

## Feb 2 2026 — the built knowledge-graph platform, handed to Andrei & Dima

On a two-segment session ([[wiki/meetings/2026-02-02-knowledge-graph-tool-introduction.md]]) Aaron demoed the **knowledge-graph platform** he had been building "for months and months" — a **"reasoning as a service"** system extracting concepts + typed edges out of documents into a graph (PostgreSQL + **Apache Age**, five Docker containers, a **KG command line**, an **MCP server**, a **Fuse** driver, a web workstation; inference via Anthropic/OpenAI APIs or local Ollama) — and handed it to [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] to deploy and run. He framed it as **not RAG** but "a persistent front brain" / "conceptual memory" for tools like Claude, positioned against Neo4j/Google/Microsoft/Meta systems that cost "hundreds of thousands a year." Still "barely alpha," single-developer, dev domain **kg.broccoli.house**. The direct descendant of his 2025 transcript-knowledge-base thread. **§15.8 clear:** "Val paid for this"; vendor/program economics only. Substance on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Feb-2). [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]] [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]

## Feb 3 2026 — Claude Code integration workshop (the "AI sandwich")

On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 working session]] (continuing a prior Claude Code onboarding not in the vault) Aaron coached the Minsk engineers on working with a coding agent — his **"AI sandwich"** (define → execute/generate → review-decide, human on both ends), **tests + developer-experience as engineered guardrails** ("sharpen your knives before you butcher the meat"), the **whiteboard→Claude→git decisions** capture flow, **JIRA-as-planning / GitHub-as-decision layer**, and **"think like a data scientist"** (the developer becomes a "data engineer for your AI teammate") — then ran a **live Claude Code exploration** of the LGS monorepo on [[wiki/people/ihar-hrybko.md|Ihar Hrybko]]'s machine (three 200k-token Explorer sub-agents auto-writing a `docs/` tree + test scaffolding; hampered by Windows/WSL problems). He generated his own slides live in Claude Desktop while teaching. §15.8 clear (vendor economics only). Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-3). [[raw/Claude Code integration - continued.md]]

## Feb 6 2026 — live LGS Claude-Code session + Claude Teams demo

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Aaron ran a live Claude Code session over the cloned LGS repo to turn the team's **implicit knowledge explicit** — collecting each engineer's self-description, then prompting Claude (with **multiple parallel instances / Explorer sub-agents**) to reconcile roles against git commit history and generate a **team-collaboration handbook** (roles/ownership, process handbook EN+RU, CODEOWNERS, PR/bug/feature templates, glossary, a Figma→React→back-end→CI→Docker→EGM pipeline doc), pushed as a **PR** the team voted to merge. He closed by demoing **Claude "Teams" (feature "released yesterday")** — autonomous agents that message each other via inboxes — tasking code-owner agents as **proxies of the team members** to mature the docs. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb 6) and [[wiki/topics/github-access-and-security-model.md]] (Feb 6). [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 11 2026 — GitHub front-end Waze setup (compiler-stack + ways system)

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 front-end session]] with [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], [[wiki/people/pavel.md|Pavel]] and Val, Aaron taught his **compiler-stack layer diagram** ("a language model is a machine that compiles natural language into source code") and his **Waze ("ways") system** — an overlay on Claude Code where **skills = how** and **ways = why** (documentation / pull-request / release ways; repo/project/user scopes), traceable back through a **regulatory → requirements → policy → way → context-injection** chain (SAS / SOC 2 examples). He argued GitHub is the shared decision space ("any decision spoken into the air disappears; any decision written in GitHub is available for capture"), then ran a **live Waze/ADR conversion** of Anton's infrastructure-orchestration-core front-end repo (chose ADR domains, wrote an inaugural ADR, created local build/front-end/micro-front-end ways, slimmed the CLAUDE.md) — the run stalled on the repo's auth/MFA/network problems and the PR never executed. He set himself up as "the senior engineer for AI" who approves the team's pull requests, told JVL it must enable **forking of public repos** so the team can sync his (daily-updated) Waze, and flagged that [[wiki/people/nathan-carver.md|Nathan Carver]] had committed a `.claude` directory into the Flex-POS monorepo. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-11). §15.8 clear (tooling/consulting economics; the "help the bank account" line is a joke). [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]] [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]

## Feb 16 2026 — JIRA acceptance-criteria custom-field migration method

- On a ~1m20s clip ([[wiki/meetings/2026-02-16-val-aaron-jira-acceptance-criteria-migration.md]], 1:12pm) Aaron gave Val a **lossless method to retire JIRA's "acceptance criteria" custom field**: have Claude write a script that **enumerates every issue with the field populated (including closed ones)** and downloads the data, **process it offline** to find the per-issue changes, then **transform in batches** by appending each issue's acceptance-criteria content to the **end of the main issue description**, **verify against a local checklist**, and only then **delete the custom field** ("this way you won't lose any data"). Antecedent to the Feb-27 2026 "Review custom fields JIRA" work. Substance on [[wiki/topics/ai-assisted-development.md]] (Feb-16). §15.8 clear. [[raw/Val—Aaron.md]]

## Feb 27 2026 — JIRA custom-fields cleanup (advisor) + the fail-fast/source-of-truth session

- **JIRA custom-fields review** ([[wiki/meetings/2026-02-27-jira-custom-fields-review.md]], 2:05pm; with Val + [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]). Aaron advised (deferring the decisions to Dmitri, "I'm the advisor here"): configure **by intention and use, not technical guesswork** ("this is like going into an electrical cabinet and flipping wires… not the right way"); build a **deletion matrix** working **backward from the dashboards and their filters**; **verify on the sandbox** and against populated issues before deleting. This is the "Review custom fields JIRA" work his Feb-16 acceptance-criteria method set up; the outcome was a **13-field keep list** for his MCP to address. See [[wiki/topics/ai-assisted-development.md]] (Feb-27). §15.8 clear. [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
- **Fail-fast / source-of-truth session** ([[wiki/meetings/2026-02-27-obsidian-settings-review.md]], 2:45pm; the source filename is **mislabeled** `Claude_Code_implementation_JVL_curriculum_development` — the recording is "Obsidian settings review" but the content is this AI-philosophy discussion, §11). Aaron's thesis: AI **amplifies intentions** (and incompetence) and compiles intent into tangible output; a wrong decision reached in half an hour of prompting cost nothing, so **stop being emotionally invested** and be ready to flip the script (even run the positive and negative paths in parallel), collapsing three-week deliberations into ~three-day correction cycles. He tied it to the prior session's git-repos-with-code-owners + **ADR** structure + inline code documentation, and to writing things down ("if it's not written down, you'll never get out of the correction cycles"). Val gave him a **free week to finish the MCP**. See [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/transcript-knowledge-base-tooling.md]] (Feb-27). §15.8 clear (Aaron's coaching "crazy money," no figure). [[raw/Claude_Code_implementation_JVL_curriculum_development-February-27-2026.md]]

## Mar 6 2026 — the refactored Jira MCP briefing + the GitHub-dashboard tool demo

- **Claude↔Jira MCP new release** ([[wiki/meetings/2026-03-06-mcp-jira-new-release.md]], two segments 3:29pm + 3:43pm; briefing Val, with [[wiki/people/andrey-bosik.md|Andrei Bosik]] on seg 1). Aaron laid down the rules for the **refactored Jira plugin for MCP**: it can use **any** custom field (caveats for complex ones like multi-dropdowns), but each field must carry a **terse, well-written description** — an empty description is **deliberately ignored**, and a poor one degrades MCP performance across everyone's chats; users must add their **Jira auth token**. He then coached attaching requirements **by domain, not project** (requirements are cross-project — "North Dakota, specifically math"), confirming each is accepted/discussed and routing the many un-accepted legacy requirements to whoever should decide. See [[wiki/topics/ai-assisted-development.md]] (Mar-6). §15.8 clear. [[raw/MCP_JIRA_new_release_March-6-2026.md]] [[raw/MCP_JIRA_new_release_March-6-2026 (1).md]]
- **GitHub dashboard demo** ([[wiki/meetings/2026-03-06-github-dashboard.md]], 8:53pm; with Val). Aaron demoed a **"GitHub Enterprise Management Operator"** CLI he wrote himself (not purchased), checked into the GitHub Enterprise's own repo and built on the **GitHub CLI (`gh`)** — invite/remove/audit/list users, Copilot + repo management — and drove it with **Claude** in plain language, having Claude **add a new capability and its tests live** during the recording. His framing: GitHub has **no out-of-the-box reporting** (why Claude had steered Val toward a Jira dashboard), so JVL builds and grows its own tools; he ran a **62-repo collaborator report** ("18 users have access to all 62 repos" + one outlier + a CSV), said this only became feasible for coding agents "the last year," and could make it an **MCP server**. Andrei Bosik named to grow the tool. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-6). §15.8 clear. [[raw/GitHub_dashboard-March-6-2026.md]]

## Mar 9 2026 — critiques the Jira↔GitHub enforcement design (GitHub Action, not a container)

On a ~10m evening call ([[wiki/meetings/2026-03-09-jira-github-enforcement-aaron.md]], 7:14pm) Aaron reviewed the Jira↔GitHub branch-enforcement design Val had worked out earlier the same day with [[wiki/people/andrey-bosik.md|Andrei Bosik]] and called it "unusually prescriptive" and over-complicated. His pushback: it needs **no Docker container and no cloud spend**, and a container holding rights to both the codebase and Jira is a **high security risk** — it should be a **GitHub Action** running in seconds, with GitHub holding the keys in escrow. The model: an Action **per repository** checks each opened branch (any branch other than reserved names like `main`/`published` must carry a **Jira issue ID** in its name), looks the issue up in Jira, confirms the **reciprocal GitHub link back**, and blocks the commit / deletes the illegal branch — or, less aggressively, **blocks the merge to `main`** without a valid linked issue. He rejected "one giant thing to solve it all" (his Tetris analogy) in favour of per-repo Actions even at hundreds of repos, and endorsed a **special central repo that queries every repo for the enforcement Action and flags noncompliant ones** on a trust-and-verify basis — never *preventing* people from editing Actions (git history shows who changed what). His scaling point: "there's only one Andrei and there's thirty other people." See [[wiki/topics/github-release-management-pipeline.md]] (Mar-9). §15.8 clear. [[raw/Aaron_Val-March-09-2026.md]]

## Mar 13 2026 — where capabilities, requirements and ADRs are stored (git repo = source of truth)

On a short evening call ([[wiki/meetings/2026-03-13-capabilities-requirements-adr-storage.md]], 9:33pm; with [[wiki/people/val-levitan.md|Val]]) Aaron settled JVL's storage/source-of-truth model. He rejected Val's "keep it unchangeable in Jira" (Jira is a deletable, cloud-hosted issue tracker with **no cryptographic integrity** — "I just don't trust it") and ruled the **git repo the source of truth**, with Jira holding a **shadow copy** on a reciprocal link (repo wins on divergence). **ADRs and capabilities are kept with the repo** — never in Jira or Confluence — while **requirements stay as informal text blobs in Jira "for now"** because JVL "lacks the maturity" for a dedicated requirements tool ([[wiki/people/juan-martinez.md|Juan]]'s data-set curing is the first step toward it). He corrected Val's "GitHub" to "**git repo**" (elemental-tool thinking) and gave the flow **requirements → capabilities → ADR → spec → code**, tests as contracts. This nails down the storage layer behind the Aaron-"Ways" ADR/Capabilities documents. See [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-13). §15.8 clear. [[raw/Capabilities_requirements_ADR-storage-March-13-2026.md]]

## Mar 13 2026 — brief cameo on the "Semantic Understanding" transcription session (2:00pm)

Earlier the same day, Aaron joined the last ~15 minutes of the [[wiki/meetings/2026-03-13-semantic-understanding-clayton-aaron.md|2:00pm "Semantic Understanding" session]] ([[wiki/people/clayton-chancey.md|Clayton]], [[wiki/people/lena.md|Lena]], [[wiki/people/val-levitan.md|Val]]). Clayton caught him up on the plan to build a custom Whisper transcription pipeline for JVL's Russian/slang meetings; Aaron confirmed there are good **fine-tuned Russian Whisper models**, agreed the Teams/Copilot Russian gap is real ("politics"), and endorsed running the flow on **N8N** as a hosted low-code service. He and Clayton — who had each built Whisper tools before — agreed to spend ~an hour together on it. He did **not** attend the Mar-19 follow-up. Detail on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-13). §15.8 clear. [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]

## Mar 16 2026 — release-procedure teardown + the documentation-flow feedback (two-segment call)

A single continuous Val↔Aaron call recorded in two segments ([[wiki/meetings/2026-03-16-release-procedure-and-eng-documentation-flow.md]], headers 12:07pm + 12:21pm), run as a dictation session Val turns into written guidance for [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]].

- **Release procedure (seg 1).** Aaron dictated how to tear down JVL's broken Jira **ISO** release-tracking project and move release versioning into **git tags** (git = source of truth): don't delete outright — first **export/dump the ISO issue types + properties** as a data source, work with [[wiki/people/ivan.md|Ivan]]/QA to pick the real "leading-edge" items, find which repos are **referenceable** in GitHub (ignore the un-migrated SVN ones — "leave that stuff to die"), **tag releases in git for the matching repos**, discard the rest, then delete the ISO issue type from Jira; don't over-invest in archaeology except for versions handed off for validation or to customers. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-16). §15.8 clear. [[raw/Aaron_Val-release_procedure_GitHub-March-16-2026.md]]
- **Documentation flow (seg 2) — reversed his own Mar-13 ruling.** Reviewing JVL's Administration + Engineering Documentation Guides, Aaron **pivoted on keeping capabilities in the git repo**: because a capability is a **"CAP"+number** code tied to a requirement ("a whole lot like a Jira issue") and a git markdown file can't enforce **referential integrity** to its requirement, capabilities (and requirements) belong in **Jira** (requirement↔capability **issue links** form the network), while **ADRs stay in the git repo** referencing the CAP/requirement codes; also keeps non-technical people like [[wiki/people/juan-martinez.md|Juan]] out of git. He defined **"AI-first" as collaborate-not-AI-only** — every PR/requirement/capability/ADR authored with AI must still be **read and accepted by a human** before moving on, hard as that is against AI's content volume. See [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-16). §15.8 clear. [[raw/Execeutive_Engineering_documentation_flow-March-16-2026.md]]

## Mar 17 2026 — decomposing Val's "company architect" into JVL Ways; the GitHub integration plan

The next morning's four-segment session ([[wiki/meetings/2026-03-17-jvl-ways-on-github-setup.md]], headers 12:12/12:22/12:33/1:12pm) — the **first real application of Aaron's Ways system inside JVL**. Aaron ran Val's draft "automated company architect" prompt through his own **ways-production Claude environment** and decomposed it: the document is "three things stapled together" (persona + workflow + checklist); a single `way.md` would be **~120 lines of injected context** — too costly to fire on every prompt — so it becomes a **progressive-disclosure tree** (parent senior-architect persona → pass-one / pass-two ways → GitHub-check ways, ADR sub-template kept once). He taught Val the **way (guidance/"why") vs skill (context+output-format/"how")** split against Val's own draft, flagged the tightly-scoped output sections for removal, and warned off the capability-statement template (JVL's Jira "user story" templates get mis-filled). With **[[wiki/people/andrey-bosik.md|Andrei Bosik]]** (seg 4) Aaron set the GitHub plan: a **JVL branch in the Claude Code config repo Andrei maintains** carrying proprietary JVL ways over Aaron's daily-updated public copy — a **hybrid**, since GitHub Enterprise blocks a true fork, with JVL ways **never merging back** into Aaron's copy ("I don't want the word JVL inside" it) and breaking changes shipped in **version notes**. Agreed to compose/commit the ways live the next day, then have Andrei try them. The requirements-vs-capabilities/INCOSE grounding (segs 1–2) is on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-17); the Ways/GitHub detail on [[wiki/topics/ai-assisted-development.md]] (Mar-17). §15.8 clear. [[raw/Requirements_Capabilities-March-16-2025.md]] [[raw/Reference_Guides-March-16-2026.md]] [[raw/Val_Ways_set-up-March-16-2026.md]] [[raw/setting_JVL_Ways_in_GitHub-March-16-2026.md]]

## Mar 18–19 2026 — the JVL Ways GitHub pipeline (architecture + integration)

Two next-day continuations of the Mar-17 session. **Mar-18** ([[wiki/meetings/2026-03-18-setting-up-jvl-ways-on-github.md]], 12:10pm, with [[wiki/people/andrey-bosik.md|Andrei Bosik]]): Aaron drew the full **JVL Ways branch/promotion architecture** on a Confluence whiteboard (main clone → /jvl ways branch → integrate-on-merge → test-QA auto-scoring → stage trusted-user gate → prod release-by-script), set the **trusted-stage-user** model (must use Claude Code for code daily — he **rejected [[wiki/people/dmitri-kovalchuk.md|Dima]]** as a candidate; Val named **[[wiki/people/evgeny-kharetski.md|Kharetski]]**), and explained why the gates exist (a mis-scored way shipped straight to prod "breaks the steering" on everyone's machine). The live Way-generation attempt was blocked by an **Anthropic API outage** and parked. **Mar-19** ([[wiki/meetings/2026-03-19-ways-github-integration.md]], 12:14pm): Aaron pitched a **translation-as-a-service** endpoint (a separate system Ways could call — LLM translation + an admin-curated terminology override table, modeled on the Whisper tool) and ran the integration live, teaching the **"clean environment" lesson** — Andrei's personal specialized tooling **tainted** the ways generation ("food coloring in the dough… you cannot unmix it"), so ways must be authored on the **minimum standard config every JVL machine gets**. Both sessions' substance, plus the folded **JVL GitHub Ways architecture guide**, on [[wiki/topics/ai-assisted-development.md]] (Mar-18 / Mar-19). §15.8 clear. [[raw/Setting up JVL ways on GitHub-March-18-2026.md]] [[raw/Ways_GitHub_integration.md]]

## Mar 27 2026 — absent from the automation review (pulled onto the same outage incident)

Aaron was **not present** at the [[wiki/meetings/2026-03-27-automation-progress-review.md|Mar-27 automation progress review]] despite the recording base naming him: [[wiki/people/clayton-chancey.md|Clayton]] explained Aaron "will not join because he is also part of this incident" — a same-day Anthropic/Claude-Code outage both were troubleshooting. The meeting reviewed the transcription **pipeline Aaron and Clayton had earlier devised**, now productized by Clayton into a hosted microservice. See [[wiki/topics/ai-assisted-development.md]] (Mar-27). [[raw/Meeting_Transcript_automation_progress_review-March-27-2026.md]]

## Mar 31 2026 — referenced (not present) at the transcripts MCP setup

Aaron was **not present** at the [[wiki/meetings/2026-03-31-transcripts-mcp-setup-lena.md|Mar-31 transcripts-MCP setup]] (Clayton + Lena + Val) but was referenced throughout: a ~19-hours-prior meeting of Aaron's had already been auto-ingested (proving the Power Automate trigger works); Aaron "can also do this" (help Lena set up the Mac); Aaron had been pushing the team toward Mac/Linux; and Val invoked Aaron's phrase **"useful bureaucracy."** Notably, [[wiki/people/clayton-chancey.md|Clayton]] said he and Aaron **strongly disagree** on hallucination — Clayton's view that hallucination is a user category, not a model property. See [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-31). §15.8 clear. [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]] [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]

## Apr 3 2026 — Ways multilingual + session traceability, and the code-to-prose methodology

A continuous [[wiki/people/val-levitan.md|Val]] sync in two segments ([[wiki/meetings/2026-04-03-val-aaron-sync-ways-multilingual-code-to-prose.md|one stub]], §11 header times 12:23pm / 1:06pm; §12). Aaron demoed his own [[wiki/topics/ai-assisted-development.md|Ways]] work and taught a code-analysis method. [[raw/Meeting_Transcript_Ways_Multilingual_and_Session_Traceability-April-3-2026.md]] [[raw/Meeting_Transcript_Code_to_Prose_Methodology-April-3-2026.md]]

- **Ways as a Rust binary with session traceability.** Aaron showed Ways now compiled into a single fast Rust binary with a **session-visualization view** (an "abtop"/Agent-B-top process monitor for Claude sessions, plus an animation of which Ways fired at each turn and predictions of the next), demonstrating that **every turn is traceable to the Way that triggered it** — an audit trail proving guidance was followed. [[raw/Meeting_Transcript_Ways_Multilingual_and_Session_Traceability-April-3-2026.md]]
- **Native multilingual Ways.** He built a **~120MB local multilingual embedding model** (runs on the CPU, not via an API, so a network failure can't hang a session) so a Russian-speaking developer typing Russian triggers the same Ways as English; he was generating translation stubs for Japanese/German/Spanish and others via parallel agents. He asked that [[wiki/people/andrey-bosik.md|Andrei]] verify the build once pushed, then Russian speakers tune the detection via PRs/notes. [[raw/Meeting_Transcript_Ways_Multilingual_and_Session_Traceability-April-3-2026.md]]
- **Ways origin + roadmap.** Aaron recounted the project's evolution (documents-folder text files → user-scope CLAUDE.md → hooks → structured Ways) and his philosophy — "prescriptive, not proscriptive guidance triggered by context but not requested by intent and then injected just in time before tools execute" — plus plans to rename the repo **"agent-ways"** and make it work with any hook-capable turn-based coding agent. He also showed a governance/"constitution" framework able to encode per-jurisdiction rules with rule→Way→code traceability. [[raw/Meeting_Transcript_Ways_Multilingual_and_Session_Traceability-April-3-2026.md]]
- **Code-to-prose methodology.** In segment 2 Aaron taught his method of translating code into plain-language prose as a "miniature specification" (the reverse-requirements direction), using the LLM as a "Tower of Babel" between code, math notation and human language, so two developers can reconcile incompatible code at the **intention** level rather than by parsing each other's code — "that's basically a specification." [[raw/Meeting_Transcript_Code_to_Prose_Methodology-April-3-2026.md]]

## Apr 13 2026 — Monitor + Attend + AgentWays: the agent peer-mesh

A long [[wiki/people/val-levitan.md|Val]] session ([[wiki/meetings/2026-04-13-aaron-claude-advancements-review.md|Aaron Claude Advancements Review]]; §12 six recording fragments) in which Aaron presented Anthropic's new **Monitor** tool (push-injected background watcher, Claude Code v21.98), his **Attend** ambient-sensing Rust framework (5 sensors — context/processes/get/disclosure/peers — injected into a session) and its **agent peer-mesh** (Claudes auto-discover each other with no server and coordinate unprompted — he demoed two idle Claudes negotiating their own UX fix and offering to file a GitHub issue), the **AgentWays** repo forked from `cloud-code-config` (Rust-binary-first — so [[wiki/people/andrey-bosik.md|Bosik]]'s watcher on the frozen `cloud-code-config` has been silently idle for weeks), multilingual Ways via a runtime cosine model (Russian + Traditional Chinese), a Bose QC Ultra 2 reverse-engineering example (packet capture + APK disassembly → C/Python/Rust libs), and his **"human mode"/trust-and-monitor** governance thesis (control shifts from steering to trust as attention budget is exceeded; Val made it a JVL operating principle). The Flex-POS takeaway: **one Claude per submodule** connected by the peer-mesh, no master Claude. Full detail on [[wiki/topics/ai-assisted-development.md]] (Apr 13 2026). §15.8 clear. [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]] [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-1-April-13-2026.md]]

## Apr 28 2026 — referenced (not present) in two sessions

- **IP MCP model regression** ([[wiki/meetings/2026-04-28-lena-ip-mcp-model-regression.md|Lena IP MCP Model Regression]], Clayton + Lena + Val): Clayton cited Aaron as a counter-data-point — Aaron reports **no problems with Opus 4.7** — but qualified that Aaron is doing coding work, where 4.7 is fine, unlike the multi-needle retrieval Lena's workflow needs. Lena also referred to **"Aaron's MCP add-on"** as the separate tool she currently uses for deleting/archiving JIRA issues. [[raw/Meeting_Transcript_lena_IP_MCP_model_regression-1-April-28-2026.md]]
- **CAS/CMS doc-readiness review** ([[wiki/meetings/2026-04-28-cas-cloud-migration-doc-readiness-review.md|CAS Cloud Migration Doc-Readiness Review]]): Dmitri Chudinov explained a "docstring" as "how Aaron described it" — a comment on every Java method stating what it does and its inputs/outputs. [[raw/Meeting_Transcript_cas_cloud_migration_doc_readiness_review-April-28-2026.md]]

## Sept 4 2026 — Pavel corrects the record on what Aaron actually built for the RK3568

Asked by Val whether the Flex-Port debug environment should be "типа, как сделал [Аарон] для rk 35 68," [[wiki/people/pavel.md|Pavel Frolov]] said no and drew the distinction: "**Аарон никакую среду не подымал**, он всего лишь собрал набор скриптов, которые позволяли собрать нужные модули[ ]и собрать корневую файловую систему для этого [RK] процессора" — a build toolchain, not a development environment; the environment work that followed was Pavel's own ("а потом вы уже делали" — Val; "Да" — Pavel). Recorded because it narrows what the corpus elsewhere attributes to Aaron on the RK3568. Context on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 4) [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

## Sources

- [[raw/Meeting_Transcript_lena_IP_MCP_model_regression-1-April-28-2026.md]]
- [[raw/Meeting_Transcript_cas_cloud_migration_doc_readiness_review-April-28-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-1-April-13-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-2-April-13-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-3-April-13-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-4-April-13-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-5-April-13-2026.md]]
- [[raw/Meeting_Transcript_Aaron_Claude_Advancements_Review-6-April-13-2026.md]]
- [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]]
- [[raw/Meeting_Transcript_Ways_Multilingual_and_Session_Traceability-April-3-2026.md]]
- [[raw/Meeting_Transcript_Code_to_Prose_Methodology-April-3-2026.md]]
- [[raw/Clayton-Aaron-JVL-semantic-understanding-March-13-2026.md]]
- [[raw/Aaron_Val-release_procedure_GitHub-March-16-2026.md]]
- [[raw/Execeutive_Engineering_documentation_flow-March-16-2026.md]]
- [[raw/Requirements_Capabilities-March-16-2025.md]]
- [[raw/Reference_Guides-March-16-2026.md]]
- [[raw/Val_Ways_set-up-March-16-2026.md]]
- [[raw/setting_JVL_Ways_in_GitHub-March-16-2026.md]]
- [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]
- [[raw/Ways_GitHub_integration.md]]

- [[raw/Capabilities_requirements_ADR-storage-March-13-2026.md]]
- [[raw/Aaron_Val-March-09-2026.md]]
- [[raw/MCP_JIRA_new_release_March-6-2026.md]]
- [[raw/MCP_JIRA_new_release_March-6-2026 (1).md]]
- [[raw/GitHub_dashboard-March-6-2026.md]]
- [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
- [[raw/Claude_Code_implementation_JVL_curriculum_development-February-27-2026.md]]
- [[raw/Val—Aaron.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-3.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-4.md]]
- [[raw/Claude_Code-Dzmitry.md]]
- [[raw/Claude_Code-Yavorski.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Claude Code integration - continued.md]]
- [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]]
- [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]
- [[raw/Clayton_jvl-working-session-2-summary-January-20-2026.md]]
- [[raw/back-end_architecture_blueprint_review.md]]
- [[raw/Minimum_Architecture_POS_deployment_planning-september-10-2025.md]]
- [[raw/Aaron + Val.md]]
- [[raw/copilot_mcp-september-5-2025.md]]
- [[raw/Git_JIRA_spec.md]]
- [[raw/undertakings_git_intelligence-august-18-2025.md]]
- [[raw/figma_to_testing_development .md]]
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
- [[raw/Meeting_Transcript_automation_progress_review-March-27-2026.md]]
- [[raw/Meeting_Transcript_Transcripts_MCP_setup_Lena-March-31-2026.md]]
- [[raw/Meeting_Notes_Transcripts_MCP_Setup_Lena-March-31-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
