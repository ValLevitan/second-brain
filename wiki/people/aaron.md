---
type: person
title: Aaron
date: 2026-07-12
aliases: [Aaron, Aron, Erin, Eric, Aaron Bockelie]
source-count: 23
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
- **Git-LFS / VS Code onboarding (Feb 18):** ran a hands-on session onboarding [[wiki/people/dmitry-khandov.md|Dmitriy Khandov]] (and the graphics team) to VS Code + Git Graph + **Copilot** + committing via source control; quoted Copilot Business at ~$19/seat and said everyone should use it; deferred the spend decision to Val. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

## MCP automation, graphics migration, docs-as-code (Feb 21–26)

- **MCP automation ("replacing Pavel") (Feb 21):** in a short call Aaron explained that MCP servers can wrap raw API endpoints in higher-level "tools" carrying business logic (e.g. "deploy a machine to an environment"), and that the step-by-step flow a person like [[wiki/people/pavel.md|Pavel]] follows can be baked into an MCP so an AI orchestrates it — the same convention CI/CD build automation uses in GitHub. See [[wiki/topics/ai-assisted-development.md]]. [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]
- **Game/design repo split + docs-as-code (Feb 21):** in the LFS demo with [[wiki/people/lena.md|Lena]], Aaron proposed two repos per game (game + LFS design repo, joined by a git submodule; build doesn't need the comp art) and demoed docs-as-code — Markdown docs auto-rendered to a per-project website (Docusaurus/MkDocs/GitHub Docs) with Mermaid diagrams. He declared "the only source of truth is what's in git" and that his and Val's goal is to **retire Atlassian** (Confluence now, Jira in "a year or two") in favour of GitHub. He took on migrating Fortune Foo Paws' Confluence content into a GitHub docs site. See [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]] and [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Designer branching workflow (Feb 26):** coached the design team (Lena, Dima Khandov, Yulia, Anastasia) on feature/story branches, PR-only merges to `main`, and a branch-lifespan performance metric (3 days amazing → 10 days worst-acceptable) — applied to PSD files too; is building a Photoshop→contact-sheet GitHub Action; and set the plan to keep Juan/Michael out ~30 days until the core four are comfortable. See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## Git progress check-in with the designers (Feb 28)

- Aaron ran a hands-on Git check-in with [[wiki/people/lena.md|Lena]], [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]] and [[wiki/people/andrei.md|Andre]] on the Fortune Foo Paws repo: put the repo-usage rules into the repo ("general instructions are better than no instructions"), **don't commit the GDD yet** ([[wiki/people/efim-podvoiski.md|Efim]]/Michael still writing it), and **clone this repo as the future game template**. He walked them through resolving a live **gitignore merge conflict** caused by direct commits to `main`, teaching that the repo owner merges PRs and that pending PRs must be ordered — and set Andre homework on the `.github` contact-sheet Action. He noted he should be used as a **consultant, not an employee**. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/Git_progress_check_in_2025-02-28.md]]

## Minsk persona / orchestration-platform workshop (Mar 10)

- Aaron co-led (with Val, in English, via a "Dima" translating) a long teaching session pushing the Minsk team toward **persona-driven, interview-based requirements** for JVL's planned new operations **orchestration platform** — reinforcing the "understand the customer, don't just re-build the software you have" theme and his earlier "you can't write monolithic software that way" point. He probed how the team gauges "feasibility medium / error cost low" tags on the reformatted persona. See [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/persona_development_journey_meeting_with_minsk-2025-03-10.md]]

## Sources

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
