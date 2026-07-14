---
type: project
title: JVL 2025 strategic plan and Jira roadmap
date: 2026-07-12
aliases: [2025 plan, strategic plan 2025, Jira value stream, distribution infrastructure, DevSecOps grooming, ITSM, GitHub Jira alignment]
source-count: 9
open-commitments: 1
open-questions: 1
---

# JVL 2025 strategic plan and Jira roadmap

JVL's plan for 2025, both as a written executive strategy and as the Jira structure (value streams, initiatives, products) that Val and Aaron are grooming to drive it.

## The strategy

- Core idea: JVL is a small, nimble company competing against much larger gaming-technology firms, and wins on speed to market, lean operations, and rapid iteration rather than on scale. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- Four strategic pillars: (1) Games Development and Production, (2) Distribution Infrastructure, (3) Core Technology, (4) DevSecOps. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]

## What each pillar covers

- **Games** — rapid iteration and market-specific variants; the Fortune Fu Paws series as the model; expansion into Florida Market Games and HHR games. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- **Distribution Infrastructure** — multi-market deployment (Puerto Rico, Georgia); Flex-Pay and Flex-Port modular systems; a Mobile Administration App. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- **Core Technology** — the OMNI Platform integration; Binary Acceptance Criteria and Test-360 automated-testing architecture. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- **DevSecOps** — migration to Microsoft Business Central and GIT; Identity Management and a Secrets Server; on-premise infrastructure optimisation to cut technical debt. [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]

## The Jira structure being built (Jan 7)

- Val is organising the roadmap in Jira as a value stream ("Games / Distribution infrastructure / Coretec / DevOps") with initiatives and products underneath. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- New initiatives being created: casino cabinets, Flex S ("Flex Upright Street"), countertops, and a Payment Platform (kiosk, Port, Pay Cloud, mobile admin). See [[wiki/topics/jvl-machine-lineup.md]]. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val wants Aaron to help groom the plan and attach Jira links to the high-level initiatives, aiming for a team meeting the week of Jan 13 (Monday the 13th). Val is out on the 10th. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- Val was still unsure whether the Flex S cabinets belong at the "product" level in Jira and is rethinking it with Aaron. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Related market opportunity

- During the same Jan 7 planning call, Val discussed a South Dakota opportunity via MG Oil. See [[wiki/decisions/2025-01-07-pursue-mg-oil-south-dakota.md]]. [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]

## Executing the Core Technology and DevSecOps pillars (Jan 13–14)

- The Jan 13 development-pipeline meeting is the DevSecOps pillar in action: the debate over how to build the Omni-platform ISO image flexibly (Jenkins vs. a Git-native pipeline). See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]
- The Jan 14 AI-development workshop advances the same modernization: getting engineers onto Git-native, AI-assisted tooling, which Val ties directly to the pipeline goal and to scaling the company. See [[wiki/topics/ai-assisted-development.md]]. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## DevSecOps pillar execution (Jan 20)

Two Jan 20 sessions moved the DevSecOps pillar from strategy into concrete tool structure, with Val and Aaron coaching Andrei:

- **GitHub organization structure** — orgs mirror the value streams (Game Dev, Core Technology, Distribution, DevSecOps); Andrei owns DevSecOps and lets teams create their own repos. See [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]]. [[raw/github_organization-jan-20-2025.md]]
- **Miro ↔ Jira alignment + ITSM model** — the DevSecOps 2025-plan grooming session. Val and Aaron taught Andrei to structure the portfolio as **initiatives → products → features** in Jira, mirrored on a Miro board, and that every Miro card must map to a Jira issue. Key reframing: things like GitHub/Bitbucket/SVN are **products** (too big to be features) inside initiatives such as pipeline automation, infrastructure & network services, identity, ERP, AI/ML, data & analytics, etc. [[raw/meeting_various-jan-20-2025.md]]
  - **ITSM three pillars taught:** (1) **Jira Service Management** = customer requests (a Jira project type, not shown on the team's timeline); (2) **Jira issues / operations** = the change and task work; (3) **asset/CMDB database** (the "Assos" / Azure asset DB) = tracking objects. Nothing is created automatically from a request — someone decides what work (change/task) it becomes. [[raw/meeting_various-jan-20-2025.md]]
  - **Change management:** "if it works, don't touch it" — track every change; DevSecOps holds the authority to promote to production and must prove a change works before promoting it. Teams can do what they want in dev/staging. [[raw/meeting_various-jan-20-2025.md]]
  - **Products named:** RGS (runs on AWS; deployed via a Jenkins job that writes a manifest YAML to a Bitbucket repo, which Argo CD then deploys), LGS, the CMS website; plus containers/Docker and "cloud fabric" (Kubernetes), Hyper-V, EC2, Azure as infrastructure. A product's dependencies (platform, identity, containers) cross-cut all the initiatives. [[raw/meeting_various-jan-20-2025.md]]

## Minsk IT-structure follow-through (Jan 22)

- A short Jan 22 call turned the DevSecOps grooming into a work split: convert the Miro board into initiatives/products for the Jira plans view; **Andrei** takes the DevOps work (and will be educated on DevOps, which he agreed to), while **[[wiki/people/dmitri-kovalchuk.md|Dima]]** (JVL IT) takes application-support/install-and-configure work. Aaron acknowledged a reminder placed in the middle of the Miro board. See [[wiki/meetings/2025-01-22-minsk-it-structure.md]]. (The IT "Dima" is [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — owner-confirmed 2026-07-13.) [[raw/it_structure_minsk-jan-22-2025.md]]

## GitHub enterprise structure finalized (Feb 11)

- The Feb 11 repo-structure session locked the GitHub org naming convention and the **7-organization list** (Games Production; Math & Game Mechanics; Platform; Observability Platform; Core Technology; Systems Operations; Hardware & Firmware), with Pavel and Aaron agreeing to **restructure the Jira value streams to match** the orgs. Repo migration sequenced: Omni/Miranda/FlexPay → RGS → inventory-map the rest. See [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]

## GitHub-Jira level alignment debate (Mar 31)

A Russian-language Mar 31 meeting (Val with Irina, Andrey, Pavel and a "Yura" — see [[wiki/meetings/2025-03-31-github-jira-alignment.md]]) took up making the GitHub and Jira hierarchies match level-for-level ("уровни были одинаково распланированы и в гитте, и в Jira"): [[raw/github_jira_alignment-march-31-2025.md]]

- **What already matches:** features and the tasks under features sit at the same level in both GitHub and Jira ("фичер и таски уже под фичер, они на одном и том же уровне всегда"); feature branches correspond to features, features roll up into a **product**, and the product is then the **repository**. [[raw/github_jira_alignment-march-31-2025.md]]
- **The open question — what is the GitHub organization?** Val proposed the organization = the Jira **initiative** ("организация является инышарев" — the transcript garbles "initiative" as "инышарев" throughout). The counter-argument (speaker not attributable from the transcript): initiatives can end and close, JVL would get "very many organizations," and a GitHub organization name is globally **unique** — it is meant to be a very large abstract entity "usually including hundreds of repositories." That implies skipping the initiative level and rolling all products under **value streams** in Jira. [[raw/github_jira_alignment-march-31-2025.md]]
- **Proposed consequence:** reorganize Jira — possibly drop the top initiative level and go straight from value streams to products ("Тогда я предлагаю переорганизовать джиру... Сразу от value streams идти к продукту"). A participant declined to decide on the spot: "Я не готов принять сейчас такое решение. Надо подумать." [[raw/github_jira_alignment-march-31-2025.md]]
- **Homework, no decision:** study the topic that evening — talk to ChatGPT, read GitHub best practice, look for articles on how large companies solved this — and reconvene **Wednesday at 7 a.m.** [[raw/github_jira_alignment-march-31-2025.md]]

This debate revisits (but does not supersede) [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] and the Feb 11 org structure [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## Open questions

- Should the GitHub organization map to the Jira **initiative** or the **value stream** — and should Jira drop its initiative level and go value stream → product? (Homework set; follow-up Wednesday 7 a.m.) — [[raw/github_jira_alignment-march-31-2025.md]]

## Open commitments

- [ ] Andrei — rework the DevSecOps initiatives/products in Jira to align with the Miro board (rename initiatives + descriptions, create initiative and product cards, every Miro card = a Jira issue); demo a small slice at a Wednesday check-in — due Friday (with Wednesday check-in) — [[raw/meeting_various-jan-20-2025.md]]

## Sources

- [[raw/jvl_strategic_plan_and_vision_2025_2025-01-08.md]]
- [[raw/jira_value_stream_distribution_infrastructure_january_7_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/meeting_various-jan-20-2025.md]]
- [[raw/it_structure_minsk-jan-22-2025.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/github_jira_alignment-march-31-2025.md]]
