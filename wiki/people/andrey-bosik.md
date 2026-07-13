---
type: person
title: Andrey Bosik
date: 2026-07-13
aliases: [Andrey Bosik, Andrei Bosik, Andrei, Andrey, Andre]
disambiguation: "JVL DevOps manager. Distinct from Andrei Klimovich (online-games commercial lead) and from Andrew Khandov (C# Miranda developer). Owner-confirmed 2026-07-13. Canonical first name 'Andrey'."
source-count: 16
open-commitments: 4
---

# Andrey Bosik

Andrey Bosik is JVL's **DevOps manager** (owner ruling 2026-07-13; canonical spelling "Andrey", was transcribed "Andrei"). He owns the Minsk build infrastructure, the GitHub migration, and the DevSecOps/DevOps function. Distinct from [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (online-games commercial) and [[wiki/people/andrew-khandov.md|Andrew Khandov]] (Miranda C# developer).

## History

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

## Open commitments

- [ ] Andrei — create the 7 JVL-prefixed GitHub organizations and move current repos in (migrate Omni/Miranda/FlexPay first, ~1 hour), then inventory-map all remaining Bitbucket/SVN repos (old → new name → location) — due unspecified — [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [ ] Andrei — enable GitHub Copilot for the whole team, set up Lena on the tooling, and write a step-by-step VS Code / Git-LFS onboarding handout (draft with Andre, then test on Lena) — due unspecified — [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [ ] Andrei — create the two new **Game Concepts** and **Game Designs** GitHub organizations (mirroring the Jira concept/design/production stages) and grant Lena repo-creation rights — due unspecified — [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [ ] Andrei ("Andre") — get the Fortune Foo Paws `.github` **contact-sheet Action** working as a functional repo action (set up Git-access credentials, modify the YAML to use them) and demo it committing a Photoshop file — due by the Wednesday 9am meeting — [[raw/Git_progress_check_in_2025-02-28.md]]

## Sources

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
