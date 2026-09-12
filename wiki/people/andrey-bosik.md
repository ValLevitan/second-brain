---
type: person
title: Andrey Bosik
date: 2026-07-13
aliases: [Andrey Bosik, Andrei Bosik, Andrei, Andrey, Andre, Andre Bostic]
disambiguation: "DevOps engineer (Minsk build/GitHub/DevSecOps). Andrei/Andrey/Andrew cluster (3, owner-ruled): [[wiki/people/andrey-bosik.md|Andrey Bosik]]=DevOps engineer / [[wiki/people/andrew-khandov.md|Andrew Khandov]]=C# Miranda dev (Dmitriy Khandov's father) / [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]=online-games commercial. Resolve by context; queue if none."
source-count: 83
open-commitments: 20
---

# Andrey Bosik

Andrey Bosik is JVL's **DevOps manager** (owner ruling 2026-07-13; canonical spelling "Andrey", was transcribed "Andrei"). He owns the Minsk build infrastructure, the GitHub migration, and the DevSecOps/DevOps function. Distinct from [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (online-games commercial) and [[wiki/people/andrew-khandov.md|Andrew Khandov]] (Miranda C# developer).

## History

- **JVL Insights (~2023–24):** named **"Andrei Bosik (Sr. Amazon Cloud Specialist) - Consultant"** in the JVL Insights knowledge-base proposal — AWS infrastructure setup/management, scalability/reliability, cloud security. His earliest recorded JVL role. Compensation figures withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- **SQL/OLAP architecture (~2024, likely Q4):** the "Андрей" who explained JVL's directory layout — local AD (2 servers × 3 sites, replicated) vs the separate Azure AD used for mail/Teams ("он в облаках, он настроил") — in part 1, and whom Val introduces in part 2 as "Andrej is designing DevOps." See [[wiki/topics/olap-power-bi-architecture.md]] and the two meeting stubs. [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]] [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- Through Jan–Feb 2025 he was framed as an engineer **being groomed** to own DevSecOps (Val/Aaron coaching him from "engineer" toward running it). As of the owner ruling (2026-07-13) his standing role is **DevOps manager** — the earlier "being groomed" framing is superseded. The build-up is captured in the coaching sections below. [[raw/it_structure_minsk-jan-22-2025.md]]

## Role

- On the build-pipeline call, Andrei had checked that GitHub Actions is about the same as Bitbucket pipelines — a little more flexible, but still lacking the parameterization capabilities JVL wants. He suggested a Jenkins-style approach to fill in parameters and create a project file for another job. [[raw/development_pipeline_january_13_2025.md]]
- Attended the Jan 14 AI-assisted-development workshop. He had distributed the OpenRouter API keys to Anton, Sasha, Pasha and himself, and Aaron noted Andrei may have build scripts / pipeline work pushing things out to Kubernetes. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Build-pipeline decision meeting (Jan 15)

- Andrei agreed with the Git-native direction ("I agree with Pavel"). He is the cost-conscious voice on the platform choice: he flagged GitHub as more expensive than Bitbucket and gave the (internally inconsistent) per-user price figures. He also raised that Jenkins runs as a self-hosted service (deployable to cloud/Kubernetes/Docker but not a ready-made SaaS). See [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]]. [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]] [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Becoming the DevSecOps owner (Jan 20)

- Two Jan 20 coaching sessions with Val and Aaron aimed to move Andrei from "engineer" to running **DevSecOps**. On GitHub structure, Val told him to own the DevSecOps organization, be its GitHub "champion," and let teams create their own repos rather than being the central bottleneck. Val pushed back hard on Andrei's instinct to write a rigid rulebook, wanting an agreed taxonomy through conversation instead. See [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]]. [[raw/github_organization-jan-20-2025.md]]
- In the DevSecOps 2025-plan grooming session, Andrei (with Dima) was coached on aligning a Miro board with the Jira roadmap (initiatives → products → features) and on the ITSM model. His homework: rework the DevSecOps Jira structure to match the Miro board. See [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/meeting_various-jan-20-2025.md]]
- He described how RGS is deployed today: a Jenkins job writes a manifest YAML to a Bitbucket repo, and Argo CD in the cloud deploys the new container. [[raw/meeting_various-jan-20-2025.md]]

## CD setup and taking on DevOps (Jan 21–22)

- On the Jan 21 continuous-delivery call, Andrei was named as one of the people (with Anton and a Russian-speaking DevOps engineer) who would help stand up the "Hello World" pipeline; Aaron noted Andrei can currently run the Kubernetes setup he inherited but needs to grow into being able to build/vary it himself ("master baker"). See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- On the Jan 22 Minsk IT-structure call, Aaron/Val decided to route the DevOps work to Andrei (and application-support work to Dima) and to educate Andrei on DevOps; **Andrei agreed** to take that path. See [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/it_structure_minsk-jan-22-2025.md]]

## JFrog and GitHub migration (Feb 6–11)

- **JFrog Artifactory call (Feb 6):** attended as JVL's DevOps voice ("Andre, walk me through how you do DevOps") — described JVL's USB-stick lab-compliance deployment and probed the artifact/binary-management fit. He is keen on the artifactory build-caching angle. See [[wiki/topics/jfrog-artifactory-artifact-management.md]]. [[raw/JFrog transcript - February-6-2025.md]]
- **Bitbucket→GitHub transfer, live (Feb 7):** on the Friday homework session Val leaned on him — "Andre, I'm working the entire weekend on learning git… I need access to github… can you do it right now?" — and Andrei **transferred the repository from Bitbucket to GitHub during the call** ("take me two minutes I transfer the repository") and was sending the invites as it ended. See [[wiki/meetings/2025-02-07-github-homework-and-bitbucket-transfer.md]]. [[raw/GitHub repository structure.md]]
- **GitHub repo structure part 1 (Feb 10):** presented the team's one-org-leaning resolution, explained the submodule mechanics — the team uses **GitHub Apps** rather than deploy keys, though "these GitHub applications work only in one organization" (his cross-org access solution followed on Feb 11) — and took the homework to **collapse his DevOps-documentation feature branches into main via a pull request** with Sasha and Pasha as approvers. Val, in Russian, called him "красивый парень, которого я доверяю" (a good guy he trusts) while insisting the structure must not depend on trusted individuals. See [[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]]. [[raw/github _structure-pavel-aaron-andrei.md]]
- **GitHub repo structure (Feb 11):** drove the session — built the Mermaid org-structure diagram, created the JVL-prefixed organizations, and agreed to move current repos in. He argued (with Sasha) for shorter URL names and GitHub-doc lowercase conventions, but conceded to Val/Aaron's human-readable, capitalised, JVL-prefixed org names. See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## GitHub access model and AI-tools rollout (Feb 12, Feb 18)

- **GitHub check-in (Feb 12):** the WEBVTT speaker labels give his name as **Andrei Bosik**. He drove the repository-access session — demonstrating that GitHub **internal** repos are visible enterprise-wide and that **private** repos solve JVL's isolation need — and defended the private-by-default approach. Val insisted the generic "IT" admin identity (auto-created by Entra ID/SSO) be replaced by Andrei's own identity. His homework: rebuild the org setup from scratch, private by default, and merge his DevOps-architecture feature branches back to main via reviewed pull requests. See [[wiki/decisions/2025-02-12-github-repos-private-by-default.md]] and [[wiki/topics/github-access-and-security-model.md]]. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **Git-LFS / VS Code onboarding (Feb 18):** Andrei worked to enable **Copilot** for the enterprise (asking Aaron about the version/cost tiers) and said he already uses Cline + OpenRouter in his own work and can teach the graphics team; he noted OpenRouter shows only aggregate (not per-user) activity and that one shared account is fine. Homework: enable Copilot for everyone, set up [[wiki/people/lena.md|Lena]], and write the onboarding handout. See [[wiki/topics/ai-assisted-development.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- **Embedded group (Feb 18):** attended the FlexPort/FlexPay standup. See [[wiki/meetings/2025-02-18-embedded-group-flexport-flexpay.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Graphics-team GitHub migration (Feb 21, Feb 26)

- **LFS demo (Feb 21):** attended the game-repo/design-repo session; when Aaron proposed the split, Aaron asked Andrei to check with [[wiki/people/alexander-biratka.md|Sasha]] whether building the full game requires the composition art — Andrei relayed the "no" that confirmed the split. Val also asked Andrei to look at Windows-Explorer Git-status plugins and think about the artists' user experience. See [[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Designer migration (Feb 26):** coached the design team on the branching workflow; agreed to **create two new GitHub organizations — Game Concepts and Game Designs** — mirroring the Jira concept/design/production stages, and to give Lena rights to create repositories under them. He pruned stale already-merged branches to demonstrate. See [[wiki/decisions/2025-02-26-designer-branching-workflow.md]] and [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

His surname is given as **Bosik** on the Feb 12 GitHub check-in (WEBVTT). (Distinct from [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], who runs the online-games commercial business — see Owner Decisions. Also distinct from [[wiki/people/andrew-khandov.md|Andrey Khandov]], the Miranda developer coached Feb 3 — Andrei is a named escalation contact there, not the coachee.)

## Git progress check-in (Feb 28)

- On the Feb 28 designer Git check-in, Andrei ("Andre") is the repo administrator: Aaron asked whether he had **disabled auto-resolve of conflicts** in the repo settings (he'd check), and Andrei said he had already **fixed the GitHub Actions** in the repo. His homework: understand the `.github` **contact-sheet automation** (Photoshop→thumbnail), create Git-access **credentials** for it and modify its **YAML** so it can commit, for a Wednesday-9am demo. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/Git_progress_check_in_2025-02-28.md]]

## GitHub for graphic design (Mar 12)

- Andrei diagnosed the designers' **PSD-commit conflicts**: the auto-generated contact-sheet `index.md` carries a changing **"generated on" date/time line** — he proposed deleting it. He walked the group through the **assets deploy pipeline** he built: artists commit to the **production source game assets** repo → a GitHub **Action auto-archives and deploys** to the game repo (a "complete assets bundle artifact") → a next step meant to trigger the **game-mechanic repo** Action, which **didn't work yet**. His support team is the destination for **help-desk CI tickets** (dispatching to Anton/Sasha/Pavel). See [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- He had **disabled fork-from-template "for security reasons"**; Val overrode this and Andrei **enabled forking from template repos for all repos** on the call, and is to build a **generic base template** that new game repos fork from. See [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## CMS persona-requirements call (Mar 23)

- Val invited "Andre" (Bosik) to the CMS-persona meeting to help and to **translate**, and asked him to **rename the Git repo** from "understandings"/"понятия CMS" to **"CMS"** — which he actioned. See [[wiki/decisions/2025-03-23-migrate-legacy-cms-svn-to-github-by-features.md]]. [[raw/cms_persona_requirements-march-23-2025.md]]

## CMS requirements-review follow-up (~Mar 25, date inferred)

- The "Andrei" on the CMS review-workflow session (see [[wiki/meetings/2025-03-25-cms-requirements-review-workflow.md]]; GitHub-org context → Bosik, inference): Val asked him specifically to review the AI-written requirements ("Если я могу попросить вас, Андрей, пожалуйста"); he asked whether the **"Observability Platform"** org should be renamed to "Orchestration" (Val: two systems in future, leave it for now — it holds live projects, transcribed "PortoServer, PortoHost") and whether he should create a "JVL Legacy CMS" org; he tried to raise the **RGS→GitHub** move "discussed last week" and Val took it offline to keep the meeting single-subject. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]

## GitHub commits — template demo (Mar 26)

- Andrei **demoed the working template repository** (one-button instancing; predefined Actions for contact sheets, sprites, and PR migration/update). Val pushed him and the team to build a **pull-request-back-to-template** loop (fork the template → incorporate a project's improvements → PR back) so templates don't go stale, and — with [[wiki/people/lena.md|Lena]] — flagged future **per-game-type templates** (Georgia/Omnia, Persistence, classical). This continues his generic-template commitment below. See [[wiki/topics/graphics-team-git-workflow.md]]. [[raw/github_commits-march-26-2025.md]]

## Mar 31 — GitHub-Jira alignment and the RGS migration

- **GitHub-Jira alignment (Mar 31):** an "Андрей" attended the Russian-language meeting on making GitHub and Jira hierarchy levels match (with Val, Irina, Pavel, and an unresolved "Yura") — resolved to Bosik by context (GitHub/Jira structure is his domain; inference). No decision; homework and a Wednesday-7 a.m. follow-up. See [[wiki/meetings/2025-03-31-github-jira-alignment.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_jira_alignment-march-31-2025.md]]
- **RGS migration (Mar 31):** Aaron assigned [[wiki/people/igor-metelski.md|Igor Metelski]] to "work with Andre and Afim to get the remaining... SPN [SVN] repos mapped over to git"; Efim confirmed "we" (his side with Andrei) can easily migrate the parts visible in the RGS checkout batch file for a Windows local build. See [[wiki/decisions/2025-03-17-migrate-rgs-codebase-svn-to-git.md]]. [[raw/rgs_git_migration-march-31-2025.md]]
- **OpenRouter usage:** in the same-day spend audit, "Andre is using it a little bit" (resolved to Bosik by context — he is the established Cline/OpenRouter user among the Minsk engineers; inference). [[raw/vector_meeting_db-march-31-2025.md]]

## Apr 23 2025 — the company knowledge-base cloud build

On the Verba/Weaviate session ([[wiki/meetings/2025-04-23-verba-weaviate-company-knowledge-base.md]]) Val brought Andrei in to own the **cloud implementation** of the transcript knowledge base: run the **Verba** app in a **Docker container on JVL's AWS cloud**, behind authentication (an **AutoProxy** he'd already installed), browser-accessible from any device. He agreed to write the **business requirements** and set up a **Friday 7 a.m.** session with Val. On the same call he confirmed the **Jira and Confluence MCP** servers function (he and "Dimitri" had test-queried them), agreeing to the run-them-as-Docker-not-Node.js rule so Watchtower auto-updates them. (The RAG bot itself flagged the same-name confusion Val's registry tracks — "wrong Andre… **Andre Bostic**," a mis-spelling of Bosik.) See [[wiki/topics/transcript-knowledge-base-tooling.md]]. [[raw/aaron_vector_knowledge_base-apr-23-2025.md]]

## Open commitments

- [ ] Andrei — build a **generic base template** GitHub repo (from the Fortune Fupa template) that new game repos fork from — due unspecified — [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [ ] Andrei — create the 7 JVL-prefixed GitHub organizations and move current repos in (migrate Omni/Miranda/FlexPay first, ~1 hour), then inventory-map all remaining Bitbucket/SVN repos (old → new name → location) — due unspecified — [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [ ] Andrei — enable GitHub Copilot for the whole team, set up Lena on the tooling, and write a step-by-step VS Code / Git-LFS onboarding handout (draft with Andre, then test on Lena) — due unspecified — [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [ ] Andrei — create the two new **Game Concepts** and **Game Designs** GitHub organizations (mirroring the Jira concept/design/production stages) and grant Lena repo-creation rights — due unspecified — [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [ ] Andrei ("Andre") — get the Fortune Foo Paws `.github` **contact-sheet Action** working as a functional repo action (set up Git-access credentials, modify the YAML to use them) and demo it committing a Photoshop file — due by the Wednesday 9am meeting — [[raw/Git_progress_check_in_2025-02-28.md]]
- [ ] Andrey — work out how to correctly create and name the **game-concept-stage GitHub repositories** (review the agreed naming table, propose naming + access model) for the next-day meeting — due Oct 8 2025 — [[raw/objectives_workflow_meeting-october-7-2025.md]]
- [ ] Andrei Bosik (with [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]) — produce a **cloud-cost estimate** for lift-and-shift of the as-is CMS/CASS architecture, two scenarios (keep MS SQL vs migrate to PostgreSQL), plus the current structural schema — due next Monday (~Mar 30 2026) — [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

- **Owner-ruled (2026-07-14):** the "Андрей" who co-designs the **one-button game-container deployment** with [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] is Bosik (see [[wiki/topics/rgs-architecture-and-integration.md]]). Owner also fixed his title wording: **DevOps engineer**. [[raw/Explain RGS.md]]

## GitHub–Jira product reshuffle (Apr 7)

On the Apr-7 reshuffle meeting ([[wiki/meetings/2025-04-07-github-jira-reshuffle-products.md]]) Andrei was tasked to make the **GitHub repositories a mirror image** of the six re-carved products and to **link the architecture diagrams** under the correct project in Confluence and Jira (Val also wanting the diagram referenced in the repo READMEs). See [[wiki/decisions/2025-04-07-recarve-gaming-platform-into-six-product-repos.md]]. [[raw/github_jira_reshuffling_products-april-7-2025.md]]

## CMS pair + Omni daily (Apr 14–15, "Andrei" by GitHub-context inference)

- In the Apr 14–15 CMS sessions he is the GitHub-mechanics voice (production deploys via GitHub Actions; Jira feature ↔ GitHub branch flow) and received Chudinov's list of the ~15 SVN repositories to move; his stated position on the split-vs-move dispute: "последнее слово надо отдать разработчикам, чтобы им с этим работать и нести за это ответственность." [[raw/cms_svn_github-april-14-2025.md]] [[raw/cms_github_svn-apr-15-2025.md]]
- On the Apr 15 Omni daily he walked the group through the designer asset flow (sandbox sources repo → GitHub-Action export into the game repo's assets directory → pull request) and is Val's preferred help channel — "я предпочитаю, чтобы все вопросы были адресованы к Андрею, а не к Паше." [[raw/daily_omni_progress-apr-15-2025.md]]

## Apr 16 2025 — repo naming/master→main, feature branches, MCP installs

In the Omni daily Andrei confirmed the GitHub repo-naming changes (renamed the asset repo to "asset src"), is the point of contact for feature-branch creation, and was tasked to rename `master`→`main` as the standard main branch across repos (safest done by whoever works the repo). He is installing Aaron's Jira MCP for himself and Yuri Zakharenko. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]] In the IT meeting Val had him install the Jira MCP + VS Code (Russian) on Yuri's machine [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]; in the AI-tooling meeting Aaron pushed him (DevOps) to capture the designers' local-build learnings back into CI. [[raw/mcp_experiences_tech-apr-16-2025.md]]

## Apr 24–30 2025 — QA env help, ECHO ITSM build, secrets-management lead

- **Apr 24:** on the Omni integration-tests onboarding ([[wiki/meetings/2025-04-24-omni-integration-tests-qa-onboarding.md]]) and setup-screens review, Andrei Bosik is the go-to for setting up each QA engineer's test **environment** and opening **GitHub branches**. [[raw/integration_tests-apr-24-2025.md]] [[raw/set_up_screen_omni-apr-24-2025.md]]
- **Apr 24:** Val tasked Andrei Bosik with building the **"JVL Home" Jira Service Management + Confluence** support ecosystem for the legacy amusement machines (working with "Andre K"). See [[wiki/topics/echo-home-gaming-device.md]]. [[raw/echo-home_jira-service-apr-24-2025.md]]
- **Apr 30:** Andrei Bosik is the **lead on the secrets-management project** — exploring Microsoft/AWS/Delinea secret managers, and co-holder (with [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]]) of the KeePass master. Homework with Dmitry: self-assess maturity and build an implementation backlog. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/secrets_server-apr-30-2025.md]]

## May 7 2025 — secrets-management maturity coaching

On the IT-maturity session ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]) Andrei (transcribed "Andre") is the second IT person [[wiki/people/aaron.md|Aaron]] coaches on the secret-server evaluation; he raised the requirement for a user-facing **web UI for self-managed, role-based secrets** integrating with Microsoft Entra. Belarus-based IT/DevOps context → this Andrei per the owner registry. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/it_department_maturity-may-7-2025.md]]

## May 12 2025 — ActiveMQ / White Area Host upgrade

On the ActiveMQ security-upgrade call ([[wiki/meetings/2025-05-12-activemq-white-area-host-upgrade.md]]) Andrei Bosik (DevOps) is present, checks Jira permissions during the live product-hierarchy cleanup, and is named to provide **OS-layer help** on separating/upgrading ActiveMQ (the hands-on work assigned to an engineer transcribed "Sergei Sandriev"). See [[wiki/decisions/2025-05-12-upgrade-activemq-split-from-white-area-host.md]]. [[raw/activeMQ_upgrade-may-12-2025.md]]

## May 28 2025 — Delinea selection; owns the evaluation backlog

On the maturity review ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]) Andre (with Dima) presented the completed policy + risk-mapping + product scoring; **Delinea** won (CyberArk second, "very expensive"). Andre's homework: build the **DTP** Jira feature backlog for the Delinea trial (Azure-OIDC→Delinea, KeePass→Delinea migration, evaluate against policy), and draw the **visual policy diagram** Val demanded (base-policy → derived-policy map). He has GitHub-Actions-for-UEFIM work ahead of implementation. See [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md]]. [[raw/it_maturity_update-may-28-2025.md]]

## Aug 15 2025 — Keeper purchase authorized; owns the rollout

On the short [[wiki/meetings/2025-08-15-keeper-install-authorization.md|Aug-15 session]] with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/aaron.md|Aaron]], Andrei reported that IT had asked users whether they'd use Keeper and got noncommittal answers — which Val rejected as absurd for a qualified IT department. Val ruled adoption mandatory and said "install Keeper, let's start using it"; Andrei confirmed "we can buy this product." Andrei owns the rollout: stand Keeper up as the production system, then move passwords from **KeePass step-by-step and manually** (Val's explicit rule — **no bulk import**, since KeePass holds many stale passwords), using the two use cases Andrei named (self-service password retrieval; time-boxed server access). Aaron's homework for him: a plan for implementing, measuring, sustaining, governing, and driving adoption of Keeper. This continues his secrets-management lead role from the [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md|Delinea→Keeper]] thread. [[raw/keeper_security_implimentation_IT_maturity-august-15-2025.md]]

## Aug 18 2025 — GitHub org consolidation (would own the admin model)

On the [[wiki/meetings/2025-08-18-github-org-consolidation.md|Aug-18 4:30pm meeting]] with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]], Andrei worked Val's push to **collapse JVL's several GitHub organizations into one (or few)**. He flagged the migration cost — **many Actions (incl. cross-referencing ones) must be rewritten** — and urged waiting **~1–2 weeks** for people to return from holiday. Under a single-org model **he alone would issue rights/permissions** (owners: Andrei, Dima, Val, Aaron). Andrei + Pavel to meet the next day to define org naming and the migration map. Reverses the multi-org structure he helped build; see [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]]. [[raw/Git_organization_management.md]]

## Oct 7 2025 — game-concept-stage workflow + repo prep

On a 3:02 PM prep call ([[wiki/meetings/2025-10-07-game-concept-workflow-prep.md]]) Val briefed Andrey ahead of the next day's game-concept-stage meeting: mapping the Jira→GitHub handoff (feature = branch, product = repository; "Done" = the PR merged, driven from GitHub), keeping a **universal Backlog/To-Do/In-Progress/Done workflow** across value streams (Andrey argued the shared action names must not change between streams even where game production adds wider stages — Val agreed), and replacing **Confluence with Obsidian** for writing game abstracts in MDX inside the repo (Andrey flagged the Python scripts that process this would need templating per repo). Andrey's homework: work out how to correctly create/name the game-concept-stage repositories. Continues his GitHub/DevOps ownership and the [[wiki/topics/docs-as-code-and-atlassian-exit.md|Atlassian-exit]] thread; ties to [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/objectives_workflow_meeting-october-7-2025.md]]

## Feb 2 2026 — handed the knowledge-graph tool with Dima

On the two-segment [[wiki/meetings/2026-02-02-knowledge-graph-tool-introduction.md|Knowledge Graph Tool introduction]], Andrei (with [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]) is one of the two people [[wiki/people/aaron.md|Aaron]] handed his built **knowledge-graph platform** to. He was the most active questioner — probing the data store (Aaron: **Postgres + Apache Age**), CPU-vs-GPU, RBAC/multi-user isolation, Docker install, OAuth providers (Entra/Google/Okta — planned), and internet exposure/security (Aaron: keep it off the open internet, use a VPN). This continues his standing ownership of the earlier **Verba/Weaviate** company-knowledge-base cloud build (Apr-23-2025) — the same lineage. Val charged him and Dima to "take possession of this tool" and lead the company from "noise" to "binary facts." Substance on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Feb-2). [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]] [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]

## Feb 3 2026 — Claude Code workshop (support + the persistent-rules `.claude` doc)

On the [[wiki/meetings/2026-02-03-claude-code-integration-continued.md|Feb-3 Claude Code workshop]] Andrei was present in a support role — helping [[wiki/people/ihar-hrybko.md|Igor]] navigate WSL/terminal paths during the live LGS-monorepo run, and noting Val's fixes to the machine's tooling failures. He shared the practical habit of having Claude Code keep a **`./claude` folder doc of recurring rules/mistakes** that you periodically ask it to re-analyse and update so the same errors aren't repeated. (He is also the co-recipient, with Dmitri Kovalchuk, of Aaron's Feb-2 knowledge-graph tool that Val cited here as the large-context future.) See [[wiki/topics/ai-assisted-development.md]] (Feb-3). [[raw/Claude Code integration - continued.md]]

## Feb 6 2026 — GitHub admin on the LGS/Claude-Code session

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6 UI/Claude-Code session]] Aaron's Claude analysis placed Andrei as the **GitHub admin** — one of the repo's admins, who **created and set up the repo** and manages access policies, pipelines and security-threat identification, with low code commits ("only touches gitignore"). Two concrete items (detail on [[wiki/topics/github-access-and-security-model.md]] Feb 6): he had set the GitHub auth timeout to **8 hours** (Aaron flagged frequent re-auth breaks agent tools), and he attributed the **"unnamed" leftover contributor** to the **Bitbucket→GitHub migration**, cautioning historical names may not be fully removable — against Val's clean-out and JVL-credentials-only directives. He agreed with Aaron that JVL should now write **rules for how it works with GitHub**. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Feb 11 2026 — manual Waze-repo sync (fork blocker)

On the [[wiki/meetings/2026-02-11-github-front-end-waze-setup.md|Feb-11 front-end Waze session]] (Andrei **not present**), Pavel explained that JVL **cannot fork** Aaron's Waze repo, so **Andrei copied-and-pasted it into JVL's internal** and makes updates manually when he sees changes on Aaron's side. [[wiki/people/aaron.md|Aaron]]'s directive: JVL must **configure its GitHub Enterprise environment to allow forking of public repositories** so each engineer forks and syncs the (daily-updated) Waze themselves rather than depending on Andrei's manual copy — the same "don't passively receive it from the IT team" point. See [[wiki/topics/ai-assisted-development.md]] (Feb-11). [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]]

## Feb 12 2026 — onboards Genadi Peari to Claude Code + a GitHub repo

On the first of the two same-day [[wiki/people/genadi-peari.md|Genadi Peari]] calls ([[wiki/meetings/2026-02-12-genadi-flex-station-flexbill-texas.md]]), Genadi reported that "**Andrei**" had set up a **GitHub repository** for his hardware work and installed **Claude Code and Claude Desktop** on Genadi's computer, and that they would continue that day (Genadi: "I'm in shock at how we've progressed"). By DevOps / Claude-Code-onboarding context this is Bosik (the Feb-2026 onboarding thread is his) — labeled a strong inference. [[raw/Call_Genadi_Peari-February-12-2026-1.md]]

## Mar 6 2026 — on the Jira-MCP briefing; named to grow the GitHub-dashboard tool

- On the [[wiki/meetings/2026-03-06-mcp-jira-new-release.md|Mar-6 3:29pm Claude↔Jira MCP briefing]] (with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/aaron.md|Aaron Bockelie]]) Andrei ("Andrei Bosik") is present as JVL IT while Aaron explains the refactored Jira plugin's custom-field-description requirement; his only recorded line is "All clear." See [[wiki/topics/ai-assisted-development.md]] (Mar-6). [[raw/MCP_JIRA_new_release_March-6-2026.md]]
- On the same-day [[wiki/meetings/2026-03-06-github-dashboard.md|GitHub-dashboard demo]] (Aaron ↔ Val; Andrei not present) Aaron named **Andrei** as the one who "needs to get into the mindset of growing the tool" — the homegrown GitHub Enterprise-management CLI — and noted Andrei already uses the GitHub CLI (`gh`). Consistent with his DevOps/GitHub-admin role and the Feb-9 "intelligence center" push. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-6). [[raw/GitHub_dashboard-March-6-2026.md]]

## Mar 9 2026 — designs the Jira↔GitHub enforcement loops

On a short 3:58pm call ([[wiki/meetings/2026-03-09-it-github-jira-infrastructure.md]], ~3m8s, Russian; file "Call with Andrei Bosik") Andrei walked [[wiki/people/val-levitan.md|Val]] through the two automated Jira↔GitHub "loops" IT wants to build: **(1)** any Jira task in-progress must have a GitHub branch — run **nightly at 21:00 Toronto time**, emailing the task's assignee; **(2)** a Jira start-date/timeline check (if a start date has passed but the story or its parent isn't In-Progress, notify the assignee) paired with a reverse check for a **GitHub branch with no matching Jira issue** (Val's "ghost branches"). Andrei's plan: run the loops in a **Docker container on JVL's own Docker machines in the Toronto office data centre**, not on Amazon — "why pay for it?". This is the design [[wiki/people/aaron.md|Aaron]] critiqued the same evening (7:14pm), arguing for a per-repo GitHub Action instead of a container. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-9). [[raw/IT_GitHub_JIRA_infrastructure-March-9-2026.md]]

## Mar 10 2026 — the transparency call (problem vs. mechanism)

On the [[wiki/meetings/2026-03-10-jira-github-transparency.md|Mar-10 ~50-min Russian call]] with [[wiki/people/val-levitan.md|Val]], Andrei is the engineering counterpart in Val's "you propose the *how*, I own the *what*" split. He reported that he and "Dima" (IT/Jira context → [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]; inference) had tested a **JIRA workflow validator** in the sandbox (blocks moving a Story to In-Progress while its parent Feature is still To-Do), argued that developers should only commit tested/working code (raising "repository cleanliness" — Val overrode this), diagnosed the 464-open-tasks dashboard as a **bottleneck**, and conceded he could **not** produce equivalent analytics from GitHub. He confirmed JVL can **block a pull request to `main`** when a branch has no linked JIRA issue, and asked Val to pin down the report metric (Stories with no commit — per day, per week, or both). Val said he would send Andrei this recording so Andrei could extract the problem, combine it with [[wiki/people/aaron.md|Aaron]]'s proposal (without over-complicating it), and return an engineering spec for the three to agree before implementing. Substance on [[wiki/topics/github-release-management-pipeline.md]] (Mar-10). [[raw/Transparency_alignment_JIRA_GitHub-March-10-2026.md]] [[raw/JIRA_GitHub_transparency-Draft-March-10-2026.md]]

## Mar 17 2026 — named to own JVL's Ways; the GitHub integration plan

On the final segment of the [[wiki/meetings/2026-03-17-jvl-ways-on-github-setup.md|Mar-17 Aaron↔Val Ways session]] (recording header 1:12pm) [[wiki/people/val-levitan.md|Val]] called Andrei in and [[wiki/people/aaron.md|Aaron]] prepped him for a next-day working meeting — earlier in the session Val had named Andrei as the person who should **own JVL's ways** ("trying to employ Andrei on this, but he's not ready yet… he needs more time," while ruling out [[wiki/people/pavel.md|Pavel]] for it). Andrei confirmed the two mechanics behind JVL's Ways adoption: (1) JVL runs a **daily script that auto-updates Aaron's Claude Code config + Claude Code** across its employees' environments; (2) JVL uses Aaron's Claude config **as-is, unmodified**. Aaron set the integration plan: create a **JVL branch inside the Claude Code config repo Andrei maintains** carrying proprietary JVL ways, so cloners get the integrated branch — a **hybrid of Aaron's ongoing ways + JVL's own**, since **GitHub Enterprise blocks a true fork** (Andrei's own point), with the JVL branch updated from JVL's main (which tracks Aaron's repo) and JVL ways never merging back to Aaron. Substance on [[wiki/topics/ai-assisted-development.md]] (Mar-17). §15.8 clear. [[raw/setting_JVL_Ways_in_GitHub-March-16-2026.md]]

## Mar 18–19 2026 — building the JVL Ways GitHub pipeline (and the clean-environment lesson)

The two next-day working sessions with [[wiki/people/aaron.md|Aaron]] and [[wiki/people/val-levitan.md|Val]] where Andrei — named to own JVL's ways — starts operationalizing them. **Mar-18** ([[wiki/meetings/2026-03-18-setting-up-jvl-ways-on-github.md]], 12:10pm): Andrei walks through Aaron's whiteboard branch/promotion pipeline (he will run the merge/stage/prod release process and "push the release button"), and attempts the live first Way-generation in Claude Code — open the `.cloud` git repo on main, let Claude create the branch, paste Aaron's "Senior Developer Architect" prompt then Val's source doc as one input — but it is **blocked by an Anthropic API outage** across regions; parked, with Andrei to save the prompt as text and circulate the Confluence link. **Mar-19** ([[wiki/meetings/2026-03-19-ways-github-integration.md]], 12:14pm): the integration run surfaces the **"clean environment" lesson** — Andrei's own **specialized personal tooling** (a personal Jira-MCP setup + GitHub CLI usage others don't have) **tainted** the ways generation, so Aaron ruled ways must be authored on the **minimum standard config every JVL machine gets**; Andrei agreed to **build a separate clean VM** with only the minimal shared software and replay the prompts. Substance on [[wiki/topics/ai-assisted-development.md]] (Mar-18 / Mar-19). §15.8 clear. [[raw/Setting up JVL ways on GitHub-March-18-2026.md]] [[raw/Ways_GitHub_integration.md]]

## Mar 23 2026 — data-access strategy; co-owns the cloud-cost estimate

On the data-access-strategy / CMS-cloud-migration call ([[wiki/meetings/2026-03-23-data-access-strategy-cms-cloud-migration.md]], 1:34pm, Russian; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/dmitri-chudinov.md|Chudinov]], [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]) Andrei is the DevOps/cost voice: he floated a **VPN tunnel** between a cloud cube and the on-prem database as a possible transitional pattern, argued data volumes aren't huge (the cube incremental-loads, doesn't rebuild every 30 min), proposed that engineers could use **pre-defined scripts** (any language) holding the DB connection as a Claude-invokable alternative to MCP, and — his headline point — made **sizing the cloud bill the critical first step** ("could be $100, could be $10,000/month; nobody knows"). He noted MS SQL cloud licensing is very expensive and endorsed evaluating **PostgreSQL** (self-hosted or managed). Val assigned him (with [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]) the **cloud-cost estimate** plus the current structural schema. Substance on [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/topics/ai-assisted-development.md]] (Mar-23). [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## Mar 26 2026 — mirrors the Linux kernel sources to GitHub

On the [[wiki/meetings/2026-03-26-initiative-priority-schedule.md|Initiative Priority Schedule]] meeting (discussed, not clearly present) Pavel named **Andrei Bosik** for the kernel-5.15 work's supporting task: **mirror the Linux kernel sources to GitHub** (so JVL's build pulls them from its own GitHub) — a background job Pavel expects to run ~a day on its own, freeing Pavel to do the kernel build itself. Consistent with his DevOps/GitHub-mirroring role. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-26). [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]] [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]

## Mar 27 2026 — Review of Engineering Guides: transcript storage, folder structure, workflow-example request

On the [[wiki/meetings/2026-03-27-review-of-engineering-guides.md|Review of Engineering Guides]] Andrei argued that transcripts should be stored **tied to their project** (not one undifferentiated repo) so they aren't disconnected from context, clarified that only **text transcripts** (not audio) go to GitHub, and questioned why the proposed directory structure separates "Architecture" and "ADRs." He requested that the Engineering Guides document include a **concrete step-by-step workflow example** (meeting → transcript → AI processing → ADR extraction → repository storage), fact-based with question marks where details are unknown rather than AI speculation. He co-owns (with [[wiki/people/dmitri-kovalchuk.md|Dima]]) preparing the repository structure for the incoming Clayton/Elena transcript pipeline (~April 10). Substance on [[wiki/topics/transcript-knowledge-base-tooling.md]] + [[wiki/topics/ai-assisted-development.md]] (Mar-27). [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]

## Mar 30 2026 — presents the automated reporting site + Claude Code Review expansion

On the [[wiki/meetings/2026-03-30-it-follow-up-reports-code-review.md|Mar-30 IT follow-up call]] with Val (~39m) Andrei demoed the new consolidated **GitHub reporting site** he built — all previously-manual reports auto-generated as web pages, split into a **daily compliance report** (commits-to-main, PR-vs-direct-push, 400-line PR-size threshold, days-since-activity, reviewed-by-other) and a **weekly Monday branch-audit report** (three improper-branch categories + sanctioned/active branches + per-user summary). He accepted Val's reformatting (rename "garbage"→"improper"; red non-sanctioned block on top, green sanctioned below; consider multi-week dynamics) and the enforcement workflow (send weekly, chase non-reactors after a week). On **Claude Code Review** he supplied the ~$50/PR cost data and took the direction to expand it beyond the current 3 repos (Flex POS / Flex Dispenser / Miranda) to all active repos, starting with Flex Sport POS. Substance on [[wiki/topics/github-release-management-pipeline.md]] and [[wiki/topics/ai-assisted-development.md]] (Mar-30). [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]] [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]

## Apr 13 2026 — the AgentWays cutover: his deployment watcher has been silently idle

Two connected threads this day. In the morning [[wiki/meetings/2026-04-13-aaron-claude-advancements-review.md|Aaron Claude Advancements Review]] (Andrei not present) Aaron flagged that he forked `cloud-code-config` into a new **AgentWays** repo (Rust-binary-first), so **Andrei's auto-deployment watcher — still pointed at the frozen `cloud-code-config` — has silently updated nothing for weeks.** Andrei must repoint his deployment tooling at AgentWays and work out how to compile/distribute the Rust binaries (cross-compilable per platform). In the afternoon [[wiki/meetings/2026-04-13-flex-pos-repo-architecture-review.md|Flex-POS Repo Architecture Review]] (Andrei present, with Val and [[wiki/people/alexander-biratka.md|Biratka]]) he asked whether Biratka's v2 repo document should therefore be discarded; Val said no — refine it to v3 at the 14 Apr joint Aaron session, where Andrei's AgentWays cutover and deployment-shape decision would also be worked out. Substance on [[wiki/topics/ai-assisted-development.md]] and [[wiki/topics/github-release-management-pipeline.md]] (Apr 13 2026). [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]] [[raw/Meeting_Notes_Flex-POS_Repo_Architecture_Review-April-13-2026.md]] [[raw/Meeting_Transcript_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]

## Open commitments (Apr 13 2026)

- [ ] Andrei Bosik — stop watching `cloud-code-config`; clone the new **AgentWays** repo and repoint the auto-deployment tooling at it; work out Rust-binary compilation/distribution — due before/at the 14 Apr Aaron session — [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]]
- [ ] Andrei Bosik — decide the AgentWays deployment shape (build-from-source / pre-built releases / container image) and bring the proposal (plus his deployment-side open questions) to the 14 Apr Aaron session — due 14 Apr 2026 — [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]] [[raw/Meeting_Notes_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]

## Open commitments (Mar 30 2026)

- [ ] Andrei Bosik — reformat + regenerate the weekly branch-audit report (improper rename, red/green split, per-user block into red) and send Val the link for review before wider distribution — due unspecified — [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- [ ] Andrei Bosik — expand Claude Code Review to all active repositories, starting with Flex Sport POS — due unspecified — [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- [ ] Andrei Bosik — create a main-project Jira ticket for release-process documentation (moved from Service Management) and start the conversation with Ivan Shpak and Aaron — due unspecified — [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]

## Apr 15 2026 — legacy CMS documentation progress check: owns the "documents readiness" report

On the [[wiki/meetings/2026-04-15-legacy-cms-documentation-progress-check.md|Legacy CMS Documentation Progress Check]] (with Val, [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]]) Andrei presented his 6-metric **"documents readiness"** dashboard tracking README/CLAUDE.md/docstring coverage across the legacy-CMS repos. Val coached him to *guide* a reader through a report rather than hand it over cold. Andrei argued the docs pass is also a **bus-factor** safeguard (the legacy CMS lives on a while regardless of future architecture) and undertook to deepen from repo-organization into **deployment infrastructure** by Apr 28. Substance on [[wiki/topics/docs-as-code-and-atlassian-exit.md]] + [[wiki/topics/ai-assisted-development.md]] (Apr-15). [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]

## Aug 24 2026 (reported) — he and Val ran the first prose-from-code experiment, and it failed

On the [[wiki/meetings/2026-08-24-nova-lgs-prose-standard-checkpoint.md|Aug-24 prose checkpoint]] (Russian; Bosik **not present**) [[wiki/people/val-levitan.md|Val]] described an **earlier, undated** experiment he had run with Bosik — "Андрей босик и я лично" — writing prose from code. His verdict: "Вот такой метод не сработал… просто выходила слабая очень" — the method did not work, the output came out very weak. What did work well was linking the code to the product's overall architecture: "когда вы связывали код с общей архитектурой, когда вы ему объясняли общую архитектуру продукта." [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

- [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] disagreed on the necessity of that step, arguing Claude already picks the architecture up from the project context. See [[wiki/topics/ai-assisted-development.md]] (Aug-24). [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- **Name note:** the derived meeting note for this session renders Val's collaborator as "Andrei Bockelie," conflating **Andrei Bosik** with [[wiki/people/aaron.md|Aaron Bockelie]]. The transcript says "Андрей босик" — Bosik. [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- Separately, Evgeny Kharetski was left to work out the no-prose-no-PR repository rule with an unnamed "Andrei," and Irina and Pavel credited an "Andrei" as the initiator of the `docs/prose` folder idea. **Neither mention identifies a surname**, so neither is attributed to Bosik here — left unresolved per §4. [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]

## Sept 3 2026 (referenced) — the "Andrei" who grants `knowledge` access, creates the integration repository, and holds the Claude Code configuration

At the [[wiki/meetings/2026-09-03-nova-prose-standard-skills-and-module-contracts.md|Sept-3 prose/contracts follow-up]] (Russian; Bosik **not present**) an unnamed "Андрей" is given three repository-administration jobs. **No surname is spoken on the call**, so the attribution below is an **inference from role context** (repository creation, access grants and shared tool configuration are the DevOps/GitHub-admin remit this page holds) — not a stated fact, and not force-matched. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

- **Company-wide access to the `knowledge` repository.** Pavel took the action: "надо Андрею написать письмо, что дать компани вайт акцесс всем. В репозиторию [knowledge]." See [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **Creating the NOVA machine-side integration repository.** Evgeny: "создаёт Андрей[,] наполняем… мы," adding that setting up a repository with the right structure "у Андрея, мне кажется[,] уже на потоку" — routine for him by now. See [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]]. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- **Moving the prose skills into the Claude Code configuration.** Vladimir: "разговаривал по этому поводу с Андреем[.] Вчера пришли к тому, что когда мы закончим… вынесем в конфи[г] кода так, чтобы все разработчики пользовались одной и той же версией скилла." [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- A **fourth, separate** "Андрей" mention on the same call is *not* attributable here: Irina said an "Андрей" had written the Recycler capabilities and broken them down very finely. Left unresolved per §4. [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]

## Sept 7 2026 — named driver of the Wi-Fi work, and the router-brand adviser

At the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08 Wi-Fi meeting]] (Russian) Val put the Wi-Fi write-up on Bosik specifically to take load off [[wiki/people/pavel.md|Pavel Frolov]]: "Андрей Босик, вы на себя можете это взять?" — "Да да, я, давайте конечно." Val's instruction: start today, take it under his control, talk directly to the people in that meeting, set the pace — "вы драйвер… вы задаете темп" — and, because "мне нужно это завтра, то вы вчера должны были начать." Bosik: "Все понятно, вопросов нету." Val's closing image was a tank that has to drive through walls. See [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]] [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

His other contributions:
- **He talked Val out of the jamming worry** — such devices exist and "забивают вот этот канал там 2 и 4 герца полностью по всем частотам," but the attacker must be inside the premises, and "кто это будет делать? Зачем кому это вообще делать?" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He argued for making a JVL device the access point** ("мне 2 вариант, лично больше нравится") and lost to Alekseev and Genadi on reliability grounds, taking it gracefully: "не[,] как скажете, я же только идеи подкидываю" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He answered the machine-count question:** with a third-party router, "там ограничения это только сам роутер" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He is the router-brand knowledge on the call:** Cisco as the American answer, and "Линксис это и есть циска[,] это суббренд циска," home/small-office against Cisco's mid- and large-business line; Nokia Finnish; MikroTik Lithuanian. He also raised the router QR sticker and was honest that he did not know which manufacturers ship one: "Не уверен, честно скажу" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **He confirmed the non-functional requirements already exist for Ethernet** — "для [Ethernet], наверное, это то же самое, что делали" — which is why Val's instruction was to have Claude find them rather than write them again [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- **Val named him as the person who understands the prose/data-contract standard**: "Андрей глубоко в этом разбирается, он был частью всей этой гимнастики" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Open commitments (Sept 7 2026)

- [ ] Write the Wi-Fi capabilities, break them into features in Jira, own the pace and coordinate the group — due start Sept 7 2026, high — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Ask Claude to find the existing non-functional requirements in the WebSocket protocol (handshake, heartbeat, reconnect, self-diagnostics) and attach them to the capabilities with single-line acceptance criteria — due unspecified, high — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] Call [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] today and set him up on Claude Code — due Sept 7 2026 — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Sept 9 2026 — the Sept-7 assignment produces output, and Val widens his role to planning

Two days after being made driver of the Wi-Fi work ([[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]]), Bosik's results were on [[wiki/people/val-levitan.md|Val]]'s screen during the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]]: "[я] смотрю сейчас на email от [Б]осика. Он создал огромное количество [рекваймент]." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

- **What he built:** capabilities first, then requirements under them — [[wiki/people/pavel.md|Pavel]]: "он не просто создавал реклай[мент]с[,] он создал [капа]билити под них, потом создал реклайментс" — across both Flex-IQ and FlexPay; the derived notes call it "the large batch of capabilities and requirements Andrei Bosik had just created off meeting transcripts." The Wi-Fi capabilities attributed to him on the call were **145, 143, 142 and 140**. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]] [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **Scope was deliberately narrow.** Val: "мы его просили только на вай[-]фай, потому что он концентрировался только на Алексее[ве,] чтоб Алексееву раздать работу." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **How he produced them:** from the recorded meeting, using his own engineering judgement — Val: "он присутствовал на митинге с Алексеевым… [с]делали запись этого транскрипта… но он же сам тоже инженер. Он понимает, что нужно делать." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **Val's expansion of the role:** Bosik and [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] should take the planning off Pavel entirely, in daily sessions — "[я] вижу, что [Б]осик и Ковальчук потянут планирование под вашей командой, где вам руками не надо дотрагиваться до этого." See [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- **The check Pavel put in front of it:** Irina and Khamin grade the coverage first; Pavel expects "на 5% в лучшем случае" of kiosk behaviour, and worried Bosik would generate too many capabilities on Flex-Port if left unbounded. Val's answer was to bound him explicitly — "если поставить ему задачу, что должно быть не больше… какого[-]то энного количества [капабилитис]… он это сделает." [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 10 2026 — he argues for the MVP split first, and is overruled twice

At the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]], the first source showing him in the room the morning after planning was delegated to him and [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] ([[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]). [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **His proposed order of work:** decide MVP 1 and MVP 2 contents first, then work out how to automate the testing of those features — "нам надо в принципе… 1 определить, что ходит в MV[P] один[,] в MVP 2, а затем… подумать, как мы можем автоматизировать тестирование этих фич." [[wiki/people/pavel.md|Pavel]] put requirements ahead of it. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He argued transactional scope is wider than the three named products**, and said he had personally linked the Flex-Recycler in because it has a Wi-Fi module too — "там оно шире[,] Паша… я лично привязывал, потому что там же тоже вай[-]фай модуль есть." Pavel ruled the Recycler out of both MVPs. See [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He proposed the disagreement channel that the group adopted** — just write it in the chat: "[д]айте в чате пока просто писать[,] да[,] и всё." See [[wiki/decisions/2026-09-10-capability-review-feedback-goes-into-the-meeting-chat.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He questioned whether the work is being certified at all** — "а это тоже сертифицируется?… [г]оворишь, вроде не будут сертифицировать это?" — leaving [[wiki/people/irina-shishko.md|Irina Shishko]]'s certification schedule on an unconfirmed premise. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He is assigned, with Dmitri, to study the last seven days of capabilities** before the Klimovich walkthrough, so the rest of the team is not pulled off its work. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Open commitments (Sept 10 2026)

- [ ] Andrey Bosik and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — study the capabilities created in the last seven days and flag disagreements, gaps and missing requirement links, before the meeting with Andrei Klimovich — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — he wins the Wi-Fi capability argument, asks two things "for the transcript", and loses the router one

At the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] Bosik raised more of the meeting's structural questions than anyone. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- **He owned up to three identical per-product Wi-Fi capabilities** — "у меня 3 одинаковых [кейпа]билити по вайфаю есть под каждый продукт" — and noted he had proposed the single form first and been talked out of it. Irina's acceptance-criteria ruling settled it his way. See [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He made the shared-components case for the whole device family** — the Flex devices share the RK board, Wi-Fi/LTE, screens, the QR scanner and remote update, so changing one thing should not mean editing every repository. Klimovich fully supported it and Val pointed at [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]. Bosik's own correction: his point is about the **product build**, not screens — "ты в одном месте поменял[,] и все продукты эти изменения за собой подтянули." Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 11). [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He pushed the Flex-Port master device into MVP 1**, splitting remote firmware update into master selection then distribution. See [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He asked explicitly "for the transcript" that Flex-Port firmware go into the same Amazon S3 store as the kiosk firmware** and be distributed from there, "чтобы у нас единое место хранения было." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He described how staging actually works today** when Val asked: a GitHub Action creates an artefact that lands on Amazon, and a web interface to the transactional terminal-management system picks which version goes to which device. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He challenged the plan to put an LTE modem in every device**, arguing for one bought LTE router per location — "[с]имку вставил, и он уже… раздаёт интернет". Val disagreed on cost and **the exchange was cut off without a decision**; it stands as an open question on [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He also put the Wi-Fi coverage question to Klimovich before the meeting proper** — how far Wi-Fi must reach across a Georgia location — and got the petrol-station description recorded on [[wiki/projects/georgia-market-rollout.md]] (Sept 11). [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He had Kovalchuk add [[wiki/people/alexei-khamin.md|Alexei Khamin]] and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] to the capability project during the call** — "[г]отово, проверяй." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He volunteered for weekend work** if Chudinov needs supporting: "конечно… если дима мне что[-]то будет присылать… то я это всё [сделаю]." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 11 2026 (10:33, in absentia) — the transcript-to-capabilities role is now named as a standing function

He was not on the [[wiki/meetings/2026-09-11-technician-complaints-and-new-capabilities-workshop.md|10:33 AM technician-complaints workshop]], but Val designed the whole Passport/RIS exercise around him and said so by name: talk the subject out for an hour on Monday, "[в]зять его транскрип… и перевести его на… [кейпа]билоти, можем отдать это… Андрею посику, который поможет нам из этого сделать [кейпа]билоте" — take the transcript, turn it into capabilities, hand it to Andrei Bosik, who will help make the capabilities out of it [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]].

**This is the third subject in five days routed through him this way** — Wi-Fi on Sept 7, planning generally on Sept 9, and now the Passport/RIS regulations. What began as one assignment is being used as a standing conversion service. See [[wiki/decisions/2026-09-11-new-regulations-for-the-passport-and-ris-talked-out-monday-and-converted-from-the-transcript.md]], [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]] and [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]].

## Open commitments (Sept 11 2026)

- [ ] Andrey Bosik — help convert the Monday Sept-14 Passport/RIS working-meeting transcript into capabilities — due after Sept 14 2026; **assigned in his absence** — [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
- [ ] Andrey Bosik — reformat the three identical per-product Wi-Fi capabilities into one — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Andrey Bosik — check whether the router already requested carries an LTE modem, and write up the router / network-topology view as a capability tied to a recognised standard — due immediately, flagged urgent — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Andrey Bosik — have the Flex-Port firmware placed by the workflow into the same Amazon S3 store as the kiosk firmware; he believes a capability for it already exists and should be found — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Nova_Prose_Standard_Skills_Module_Contracts-September-3-2026.md]]
- [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]
- [[raw/Meeting_Notes_Aaron_Claude_Advancements_Review-April-13-2026.md]]
- [[raw/Meeting_Transcript_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]
- [[raw/Meeting_Notes_Flex-POS_Repo_Architecture_Review-April-13-2026.md]]
- [[raw/Meeting_Transcript_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- [[raw/Meeting_Notes_IT_Follow_Up_Reports_and_Code_Review-March-30-2026.md]]
- [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Transcript_initiative_priority_schedule-2-March-26-2026.md]]
- [[raw/Meeting_Notes_initiative_priority_schedule-March-26-2026.md]]
- [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [[raw/setting_JVL_Ways_in_GitHub-March-16-2026.md]]
- [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]
- [[raw/Ways_GitHub_integration.md]]
- [[raw/Transparency_alignment_JIRA_GitHub-March-10-2026.md]]
- [[raw/JIRA_GitHub_transparency-Draft-March-10-2026.md]]
- [[raw/IT_GitHub_JIRA_infrastructure-March-9-2026.md]]

- [[raw/MCP_JIRA_new_release_March-6-2026.md]]
- [[raw/GitHub_dashboard-March-6-2026.md]]
- [[raw/Call_Genadi_Peari-February-12-2026-1.md]]
- [[raw/Claude_set-up_GitHub_Front_End-February-11-2026-part-2.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- [[raw/Claude Code integration - continued.md]]

- [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]]
- [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]
- [[raw/GitHub repository structure.md]]
- [[raw/objectives_workflow_meeting-october-7-2025.md]]
- [[raw/it_maturity_update-may-28-2025.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/Git_organization_management.md]]

- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]
- [[raw/architecture_sql_olap_visualization_2_2025-03-29.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_1_january_15_2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/meeting_various-jan-20-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/it_structure_minsk-jan-22-2025.md]]
- [[raw/JFrog transcript - February-6-2025.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Check_in_on_GitHub_2025-02-12.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/cms_persona_requirements-march-23-2025.md]]
- [[raw/github_commits-march-26-2025.md]]
- [[raw/github_jira_alignment-march-31-2025.md]]
- [[raw/rgs_git_migration-march-31-2025.md]]
- [[raw/vector_meeting_db-march-31-2025.md]]
- [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [[raw/Explain RGS.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- [[raw/mcp_experiences_tech-apr-16-2025.md]]
- [[raw/github_jira_reshuffling_products-april-7-2025.md]]
- [[raw/aaron_vector_knowledge_base-apr-23-2025.md]]
- [[raw/integration_tests-apr-24-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/echo-home_jira-service-apr-24-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/activeMQ_upgrade-may-12-2025.md]]
- [[raw/keeper_security_implimentation_IT_maturity-august-15-2025.md]]
- [[raw/Meeting_Notes_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Technician_Complaints_and_New_Capabilities_Workshop-September-11-2026.md]]
