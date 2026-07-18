---
type: project
title: JVL 2025 strategic plan and Jira roadmap
date: 2026-07-12
aliases: [2025 plan, strategic plan 2025, Jira value stream, distribution infrastructure, DevSecOps grooming, ITSM, GitHub Jira alignment]
source-count: 16
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

## Jira components cleanup (~Mar 19 2025, date inferred)

Housekeeping rulings from a short components-objectives fragment (Val, [[wiki/people/pavel.md|Pavel]] and an unlabeled facilitator — stub: [[wiki/meetings/2025-03-19-jira-components-cleanup.md]]): [[raw/components_objectives_for_a_follow_up_meeting.md]]

- **Archive first:** "RUDA is not a component… a good candidate to move into an archived Jira development project" once its features/stories are closed — "we're not ever going to revisit that stuff again. Not in this iteration… Maybe we'll go back to RUDA again under Omni." [[raw/components_objectives_for_a_follow_up_meeting.md]]
- **Component naming:** review conventions (e.g. **TRDC** "might be split into something else"); remove obscure designations — an **empty component field beats a bad one**; only define components that fit the shared understanding. Real component examples named: **SAS, Neighbor, Passport**. [[raw/components_objectives_for_a_follow_up_meeting.md]]
- **RIS → Slot Links:** "remote initial setup" is not a component but an "incorrect or incomplete initiative name" — a many-featured element of **Slot Links**, "a large initiative that we should entertain," under which RIS will be redistributed; Slot Links itself is also not a component. [[raw/components_objectives_for_a_follow_up_meeting.md]]

## GitHub-Jira level alignment debate (Mar 31)

A Russian-language Mar 31 meeting (Val with Irina, Andrey, Pavel and a "Yura" — see [[wiki/meetings/2025-03-31-github-jira-alignment.md]]) took up making the GitHub and Jira hierarchies match level-for-level ("уровни были одинаково распланированы и в гитте, и в Jira"): [[raw/github_jira_alignment-march-31-2025.md]]

- **What already matches:** features and the tasks under features sit at the same level in both GitHub and Jira ("фичер и таски уже под фичер, они на одном и том же уровне всегда"); feature branches correspond to features, features roll up into a **product**, and the product is then the **repository**. [[raw/github_jira_alignment-march-31-2025.md]]
- **The open question — what is the GitHub organization?** Val proposed the organization = the Jira **initiative** ("организация является инышарев" — the transcript garbles "initiative" as "инышарев" throughout). The counter-argument (speaker not attributable from the transcript): initiatives can end and close, JVL would get "very many organizations," and a GitHub organization name is globally **unique** — it is meant to be a very large abstract entity "usually including hundreds of repositories." That implies skipping the initiative level and rolling all products under **value streams** in Jira. [[raw/github_jira_alignment-march-31-2025.md]]
- **Proposed consequence:** reorganize Jira — possibly drop the top initiative level and go straight from value streams to products ("Тогда я предлагаю переорганизовать джиру... Сразу от value streams идти к продукту"). A participant declined to decide on the spot: "Я не готов принять сейчас такое решение. Надо подумать." [[raw/github_jira_alignment-march-31-2025.md]]
- **Homework, no decision:** study the topic that evening — talk to ChatGPT, read GitHub best practice, look for articles on how large companies solved this — and reconvene **Wednesday at 7 a.m.** [[raw/github_jira_alignment-march-31-2025.md]]

This debate revisits (but does not supersede) [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]] and the Feb 11 org structure [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## The Apr 1–3 arc — the "capability" resolution (three consecutive sessions)

The Mar 31 homework played out over three days with [[wiki/people/aaron.md|Aaron]], ending in a durable structural ruling — full detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]:

- **Apr 1** ([[wiki/meetings/2025-04-01-github-jira-correlation.md]]) — Aaron set the ground rule that a **repository is never a product** ("a product is an artifact in motion") and pushed to **flatten JVL's many GitHub orgs into one** with a naming convention; Val resisted, wanting a structure he can control, but conceded there are "too many orgs" today and that engineers are already committing into an unvetted "wild west" org. [[raw/git_jira_correlation-april-1-2025.md]]
- **Apr 2** ([[wiki/meetings/2025-04-02-github-jira-capability-diagram.md]]) — Aaron diagrammed monolithic-vs-multi-repo reality, showing **one Jira feature spans multiple GitHub branches** (app + shared library), so the feature↔feature-branch mapping is not one-to-one. Val's breakthrough: connect GitHub feature branches to a **Jira "capability"** (a bundle of features) as the executive-demonstrable unit. [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- **Apr 3** ([[wiki/meetings/2025-04-03-github-jira-structure-lecture.md]]) — Val lectured the Minsk team on the resolved structure: insert a **capabilities** level between feature and product; **feature branches ≤ 1 week**; **lengthen sprints to ~3–4 weeks** delivering 2–4 features; **"no test, no pull"** (QA wedges an automated test into the merge); **repository = product** (FlexPay is a repository); SVN→GitHub is **locked**; and AI/MCP tooling (Jira MCP + sequential-thinking, with Sonnet/ChatGPT) bridges the executive↔engineering gap. [[raw/github_jira_setup-april-3-2025.md]]

The Mar 31 **initiative-vs-value-stream / flatten-vs-many-orgs** question was **not** settled by this arc — it stays open (see below).

**May 5–6 refinement (decision-in-motion).** Three further Aaron sessions ([[wiki/meetings/2025-05-05-feature-granularity-aaron.md]], [[wiki/meetings/2025-05-06-feature-jira-defining-and-reflection.md]]) reframed a **feature as temporary** and a **capability as the permanent product description**, added the ideas of a **component** (cluster of features) and the **double-diamond** flow, and floated moving the top levels (value stream / initiative / product) into **Jira Product Discovery** projects — with **capability** replacing the product-line level and **initiative becoming the product**. No ruling; a graph + Jira-refactor plan was deferred. Full detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]].

## May 9 2025 — Val's product taxonomy and canonical product list

On the ~162-min May-9 taxonomy session with [[wiki/people/aaron.md|Aaron]] ([[wiki/meetings/2025-05-09-product-capability-feature-taxonomy-aaron.md]]; internally duplicated — facts once) Val defined the top of the hierarchy and enumerated JVL's products, using Aaron's directed-graph tool to visualize it. Definitions/tree and the "rename Feature→Capability" direction are on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/product_capability_feature_development-may-9-2025.md]]

- **Value streams (Val's list):** **games, cabinets, core software, core hardware, payment systems** (he began the session with "where do we make money?" = slot games, amusement games, payment systems; the AI proposed adding "platform & infrastructure" and "hardware & cabinets" streams). [[raw/product_capability_feature_development-may-9-2025.md]]
- **Products (Val's canonical list):** **Echo, FlexS, FlexC, FlexPay, FlexPort, FlexSMIB, FlexTower, FlexPOS, FlexServer** (product definitions on [[wiki/topics/jvl-machine-lineup.md]]). Legislative markets (Florida, South Dakota, California, North Dakota…) and architecture classes (Class 2, Class 3, HHR) are **requirements**, not products. [[raw/product_capability_feature_development-may-9-2025.md]]
- **Pavel-created placeholder initiatives** ("Operating Systems," "Hardware Abstraction Layer" in firmware) were judged not real initiatives — a "giant to-do list" — and cleaned up. Val's caution against disrupting the game-software team by mixing machine hardware with game production ([[wiki/people/genadi-peari.md|Gennady]] would "be lost"). [[raw/product_capability_feature_development-may-9-2025.md]]

## May 12 2025 — the product-discovery process (double diamond)

On the ~207-min May-12 session ([[wiki/meetings/2025-05-12-product-discovery-double-diamond-aaron.md]]; internally duplicated — facts once) Aaron taught Val the **discovery → capability → use-case → requirement → feature → story** flow and the **double-diamond** (discover/define/develop/deliver), using **Jira Product Discovery** (impact/effort scoring; the successor to the old epic-hypothesis Confluence templates). **No adoption ruling** — conceptual coaching; Val's specific unsolved gap is turning capabilities into short testable features with tiny capacity. Detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]; the FlexPay worked example on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/theory_product_discovery_process-may-12-2025.md]]

## May 29 2025 — Jira Plans maturity: drop Task/Initiative, use GitHub Issues for engineering

On the [[wiki/meetings/2025-05-29-jira-plans-maturity.md|May-29 Jira-plans maturity session]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], [[wiki/people/irina-makarych.md|Irina]]) the capability arc moved toward a cleaner two-tool split — full detail on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. [[raw/jira_plans_maturity-mat-29-2025.md]]

- **Jira = product domain.** Hierarchy trimmed to **Product → Capability → Feature → Story**; Val wants to **remove the Task and Initiative layers** ("больше заданий в JIRA — готово"; "я хочу избавиться от инициативы"), keeping Initiative only where a market like Florida genuinely warrants one. This advances the May-5–9 "capability replaces the product-line level / initiative becomes the product" direction (still not a locked Jira-config refactor). [[raw/jira_plans_maturity-mat-29-2025.md]]
- **GitHub = engineering domain.** Enable per-repo **GitHub Issues** for technical/code-health discussion (branch cleanup, "stale branch" issues) so those conversations leave Jira; Jira holds only capability/feature/user-story. Demonstrated live by enabling Issues on the "Omni LAN-based framework" repo and filing a stale-branch issue for **FRAME-476**. [[raw/jira_plans_maturity-mat-29-2025.md]]
- **Test linkage.** **X-Ray test cases in Jira** are referenced from **test code in GitHub**; GitHub **Actions** run the tests and report results back to X-Ray (manual test procedures feed the same results). QA team is learning TypeScript to write these. Val booked a **June 5, 9 am** demo. [[raw/jira_plans_maturity-mat-29-2025.md]] See [[wiki/topics/test-automation-strategy.md]]. [[raw/jira_plans_maturity-mat-29-2025.md]]

## Open questions

- Should the GitHub organization map to the Jira **initiative** or the **value stream**, be **flattened into one org**, and should Jira drop its initiative level? (Mar 31 homework; Apr 1–3 arc introduced the capability level but left the org-structure question open — Aaron for flatten, Val against.) — [[raw/github_jira_alignment-march-31-2025.md]] [[raw/git_jira_correlation-april-1-2025.md]]

## Open commitments

- [ ] Andrei — rework the DevSecOps initiatives/products in Jira to align with the Miro board (rename initiatives + descriptions, create initiative and product cards, every Miro card = a Jira issue); demo a small slice at a Wednesday check-in — due Friday (with Wednesday check-in) — [[raw/meeting_various-jan-20-2025.md]]

See also the [[wiki/topics/casino-gaming-systems-product-management.md|casino/gaming-systems product-management]] framing (the Miami-PM-hire job profile).

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
- [[raw/components_objectives_for_a_follow_up_meeting.md]]
- [[raw/git_jira_correlation-april-1-2025.md]]
- [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- [[raw/github_jira_setup-april-3-2025.md]]
- [[raw/product_capability_feature_development-may-9-2025.md]]
- [[raw/theory_product_discovery_process-may-12-2025.md]]
- [[raw/jira_plans_maturity-mat-29-2025.md]]
