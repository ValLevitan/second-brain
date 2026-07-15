---
type: person
title: Andrey Bosik
date: 2026-07-13
aliases: [Andrey Bosik, Andrei Bosik, Andrei, Andrey, Andre]
disambiguation: "JVL DevOps manager. Distinct from Andrei Klimovich (online-games commercial lead) and from Andrew Khandov (C# Miranda developer). Owner-confirmed 2026-07-13. Canonical first name 'Andrey'."
source-count: 28
open-commitments: 5
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

## Open commitments

- [ ] Andrei — build a **generic base template** GitHub repo (from the Fortune Fupa template) that new game repos fork from — due unspecified — [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [ ] Andrei — create the 7 JVL-prefixed GitHub organizations and move current repos in (migrate Omni/Miranda/FlexPay first, ~1 hour), then inventory-map all remaining Bitbucket/SVN repos (old → new name → location) — due unspecified — [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [ ] Andrei — enable GitHub Copilot for the whole team, set up Lena on the tooling, and write a step-by-step VS Code / Git-LFS onboarding handout (draft with Andre, then test on Lena) — due unspecified — [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [ ] Andrei — create the two new **Game Concepts** and **Game Designs** GitHub organizations (mirroring the Jira concept/design/production stages) and grant Lena repo-creation rights — due unspecified — [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [ ] Andrei ("Andre") — get the Fortune Foo Paws `.github` **contact-sheet Action** working as a functional repo action (set up Git-access credentials, modify the YAML to use them) and demo it committing a Photoshop file — due by the Wednesday 9am meeting — [[raw/Git_progress_check_in_2025-02-28.md]]

- **Owner-ruled (2026-07-14):** the "Андрей" who co-designs the **one-button game-container deployment** with [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] is Bosik (see [[wiki/topics/rgs-architecture-and-integration.md]]). Owner also fixed his title wording: **DevOps engineer**. [[raw/Explain RGS.md]]

## Sources

- [[raw/GitHub repository structure.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]

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
