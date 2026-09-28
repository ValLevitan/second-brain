---
type: person
title: Dmitri Kovalchuk
date: 2026-07-13
aliases: [Dmitri Kovalchuk, Dmitry Kovalchuk, Dima Kovalchuk, Dima]
disambiguation: "IT (GitHub-admin, infrastructure, secrets/Azure, AI-tool accounts) — the IT-context "Dima". Dima/Dmitry cluster (3, owner-ruled): [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]=IT / [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]=Senior 3D designer / [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]=back-end. Resolve by context; queue if none."
source-count: 38
open-commitments: 11
open-questions: 2
---

# Dmitri Kovalchuk

Dmitri Kovalchuk is **JVL's IT person** (owner ruling 2026-07-13) and the recurring **IT-context "Dima"** across the meetings — account administration, GitHub-admin, application-support, and internal-platform/observability work. (Owner correction is its own citation.)

## Role

- Administers the shared **AI-tooling accounts** (OpenRouter / ChatGPT workspace); in the Feb 18 onboarding he advised removing a subscription from the JVL workspace rather than recreating a free account per user, and rated "Grok." (Named via WEBVTT speaker labels.) [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

## The IT "Dima" appearances (owner-attributed)

Per the owner ruling, these IT-context "Dima" mentions — previously flagged unattributed or provisionally linked elsewhere — are **this person**:

- **GitHub admin seat:** "Dima" added as a GitHub administrator among the ~8 purchased seats. See [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]]. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Minsk IT-structure (Jan 22):** takes the **application-support / install-and-configure** work while Andrei takes DevOps. See [[wiki/meetings/2025-01-22-minsk-it-structure.md]]. [[raw/it_structure_minsk-jan-22-2025.md]]
- **DevSecOps/GitHub coaching (Jan 20):** attends the GitHub-org-structure and DevSecOps-grooming sessions with Andrei. [[raw/github_organization-jan-20-2025.md]] [[raw/meeting_various-jan-20-2025.md]]
- **IT observability / monitoring** as an operations function sits with IT (Kovalchuk). NOTE: the **"Observability Platform" GitHub org** named on Feb 11 (owner transcribed "Dima Chudinov") is **[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]**, the back-end architect who builds that CMS-replacement backend — a distinct person (owner ruling 2026-07-13, correcting the earlier fold of "Chudinov" into this page).

**Distinct people (do not merge), all sometimes "Dima":** [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (Senior 3D Graphic Designer), [[wiki/people/andrew-khandov.md|Andrey/Andrew Khandov]] (Miranda developer), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (back-end architect). A "Dima" who **delivers FlexPay builds** in the embedded group is a developer, not clearly IT — left **unresolved** per the ruling's "if a mention clearly isn't IT-related, leave it unresolved."

- **GitHub-commits template check-in (Mar 26):** present as "Dima Kovalchuk"; Val questioned whether the meeting was productive for him ("it seems like Dima Kovalchuk doesn't need to be here") — consistent with his IT (not game-dev) role. He is also among the team members using the VS Code / MCP tooling Aaron pushes. See [[wiki/topics/graphics-team-git-workflow.md]] and [[wiki/topics/ai-assisted-development.md]]. [[raw/github_commits-march-26-2025.md]]

## History

- **JVL Insights (~2023–24):** named **"Dmitri Kovalchuk (Sr. System Administrator, MS SQL Specialist) - Consultant"** in the JVL Insights knowledge-base proposal — to manage/optimize its MS SQL database, ensure data integrity/security, and build the data aggregation/categorization. Compensation figures withheld (§15.8). See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- **SQL/OLAP architecture, part 1 (~2024, likely Q4):** provisionally, the "Дима" called in (with Andrey) to explain how the local three-site Active Directory and the separate Azure AD (mail/Teams) work — an IT-infrastructure context that fits this page per the owner's Dima rule; **flagged, not certain**. See [[wiki/meetings/2024-sql-olap-visualization-architecture-1.md]]. [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]

## Apr 16 2025 — assets schema and secrets server

In an Aaron-led IT meeting, Dmitri showed progress on Atlassian **Assets/Discovery** — he has automated pulling all computers from Discovery into Jira, and creates/routes requests in Jira Service Management. Next step (Aaron): link the user record (source of truth = **Microsoft Entra**) to machines via a last-logged-in-user automation. He researched secrets management and proposed a **Microsoft secret server in Azure (Azure Key Vault)**, which Val endorsed. Blocker: an old **Windows 2008** box can't export (WMI); to be upgraded after a Proxmox node. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]] See [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]].

## Apr 30 2025 — secrets-management (KeePass co-owner)

On the secrets-management strategy session ([[wiki/meetings/2025-04-30-secrets-management-strategy.md]]) Dima Kovalchuk is named a **co-holder of the KeePass master** (with [[wiki/people/andrey-bosik.md|Andrei Bosik]]) and takes the homework — with Andrei — to read Aaron's perspective doc, self-score secrets maturity, and produce an implementation backlog (starting with GitHub CI/CD + AWS/Jenkins keys). See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/secrets_server-apr-30-2025.md]]

## May 7 2025 — secrets-management maturity coaching

On the IT-maturity session ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]) Dima (the IT "Dima") is one of the two IT people [[wiki/people/aaron.md|Aaron]] coaches through the weighted-matrix method for the secret-server choice; he reported working mainly with **AWS Secrets Manager**, having tried **Azure Key Vault** and used **HashiCorp Vault** 1–2 years ago, with the **GitHub secret store** used for CI/CD. See [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/it_department_maturity-may-7-2025.md]]

## May 28 2025 — Delinea selected; DTP backlog

On the maturity review ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]) Dima (with Andre) presented the completed secret-server evaluation to Aaron and Val: **Delinea** scored highest (CyberArk second, "very expensive"), Azure clarified as "just vault storage." Plan: trial Delinea via a **DTP** Jira backlog — first connect Azure OIDC to Delinea, then migrate passwords from **KeePass** to the Delinea secret database, evaluating against the written policy. Dima can start implementing first (Andre has GitHub-Actions-for-UEFIM work ahead). See [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md]]. [[raw/it_maturity_update-may-28-2025.md]]

## Sept 5 2025 — proposed owner of JVL's Microsoft/365 tenant

On a short call ([[wiki/meetings/2025-09-05-copilot-mcp-atlassian-microsoft-tenant.md]], 1:57 PM; [[wiki/people/val-levitan.md|Val]] present), [[wiki/people/aaron.md|Aaron]] proposed the directive **"Dmitri, you are responsible for our Microsoft tenant and our 365 tenant space"** and asked Dmitri to understand and help set up **Copilot Studio** for JVL plus **Copilot agents with MCP access to Atlassian**. (Recorded as Aaron's proposed assignment; fits the IT "Dima" context — infrastructure / AI-tool accounts.) See [[wiki/topics/ai-assisted-development.md]] (Sept-5). [[raw/copilot_mcp-september-5-2025.md]]

## Sept 15 2025 — SharePoint demo for the finance file architecture

On [[wiki/people/alka-sood.md|Alka Sood]]'s 4:01 PM file-architecture call ([[wiki/meetings/2025-09-15-onedrive-sharepoint-file-architecture.md]]) Dmitri (with [[wiki/people/andrey-bosik.md|Andrei Bosik]]) **live-demonstrated SharePoint** — explaining SharePoint (a site) vs OneDrive (storage), and creating a **private team site** (Microsoft-credential sign-in, members, owner/edit rights) — as JVL decided to move the weekly payment proposal and other finance files off email onto secured SharePoint sites. Fits his Sept-5 assignment as owner of JVL's Microsoft/365 tenant. See [[wiki/topics/jvl-finance-back-office.md]], [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/One-Drive _ Sharepoint_discussion.md]]

## Feb 2 2026 — handed the knowledge-graph tool with Andrei

On the two-segment [[wiki/meetings/2026-02-02-knowledge-graph-tool-introduction.md|Knowledge Graph Tool introduction]], Dmitri (with [[wiki/people/andrey-bosik.md|Andrei Bosik]]) is one of the two IT people [[wiki/people/aaron.md|Aaron]] handed his built **knowledge-graph platform** to, to deploy and run. In the first segment he asked how users **upload their own knowledge** into the graph (not just read it); in the Russian coda he was cautious ("we discussed one thing… let's just launch it and see"). Val charged him and Andrei to "take possession of this tool" and lead the company from conversational "noise" to "binary facts." Fits his IT/infrastructure role. Substance on [[wiki/topics/transcript-knowledge-base-tooling.md]] (Feb-2). [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]] [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]

## Feb 20 2026 — leads the JIRA custom-fields inventory + round-1 deletion plan

On the [[wiki/meetings/2026-02-20-jira-custom-fields-alignment.md|Feb-20 IT custom-fields alignment call]] (2:33pm; with Val), Dmitri ran the JIRA administration screen and presented his investigation of JVL's **165 custom fields** (94 system-protected): he identified a **~55-field round-1 delete list** — cancel the **Linksee plugin** ($40/month, 5 unused fields), delete two never-adopted **Jira Product Discovery** projects (~35 duplicated fields auto-removed), 12 zero-usage fields, and 3 of 16 Jira Service Management fields — plus **26 "active" fields** held for audit. He created a **sandbox snapshot** and relies on JIRA's 60-day recycle bin, and will do the deletions the following week without rushing. This is the round-1 execution behind the Feb-27 review's final 13-field keep list. Consistent with his IT/JIRA-administration role. See [[wiki/topics/ai-assisted-development.md]] (Feb-20). [[raw/IT_custom_fields_alignment-February-20-2026.md]]

## Feb 27 2026 — drives the JIRA custom-fields cleanup

On the [[wiki/meetings/2026-02-27-jira-custom-fields-review.md|Feb-27 JIRA custom-fields review]] (2:05pm; with Val + [[wiki/people/aaron.md|Aaron]], who deferred to Dmitri as the driver), Dmitri ran the screen-share and the JIRA field administration: he reported the field counts (25 used in the last six months, 17 system-managed), **exported the field list to Excel**, struck the delete rows red, kept the requirement-categorization/requirement-type and Jira-Service-Management reporter fields Aaron flagged, and produced a **final list of 13 custom fields to keep** — deleting the rest **on Monday** after practising on the sandbox instance. Consistent with his IT/JIRA-administration role. See [[wiki/topics/ai-assisted-development.md]] (Feb-27). [[raw/Review_custom_fields_JIRA-February-27-2026.md]]

## Mar 17 2026 — grooming the IP-89 dashboard (bulk-archive automation)

On a short Russian call ([[wiki/meetings/2026-03-17-ip-89-dashboard-grooming.md]], 3:54pm; with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/lena.md|Lena Zhukova]]) to groom the **IP-89** game-production Jira dashboard, Dmitri is the IT/Jira admin doing the work: he cautioned that **"bulk move doesn't always work well,"** agreed to **prototype an automation** that moves all children of a parent to archive while copying the parent's status and resolution down, and flagged that the **resolution list may not be editable** (he'll note it) during the status/resolution cleanup. Consistent with his IT/JIRA-administration role. See [[wiki/topics/github-release-management-pipeline.md]] (Mar-17). [[raw/Grooming Dashboard for IP-89-March-17-2026.md]]

## Mar 18 2026 — not a Ways trusted-stage-user candidate

On the [[wiki/meetings/2026-03-18-setting-up-jvl-ways-on-github.md|Mar-18 JVL-Ways-on-GitHub session]] (Aaron/Val/Andrei Bosik; Dmitri not present) Val floated **Dima** as a candidate **trusted stage user** for the Ways pipeline; [[wiki/people/aaron.md|Aaron]] **rejected him** because he "is not using cloud code for writing code on a daily basis," and Val agreed (adding that Dima "doesn't really want to learn things"). A role-fit datapoint: Dmitri is IT/admin, not a daily Claude-Code developer. See [[wiki/topics/ai-assisted-development.md]] (Mar-18). [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]

## Mar 23 2026 — data-access strategy call; owns the current-state architecture diagram

On the data-access-strategy / CMS-cloud-migration call ([[wiki/meetings/2026-03-23-data-access-strategy-cms-cloud-migration.md]], 1:34pm, Russian; with [[wiki/people/val-levitan.md|Val]], [[wiki/people/dmitri-chudinov.md|Chudinov]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], [[wiki/people/andrey-bosik.md|Andrei Bosik]]) Dmitri is the IT/infrastructure voice: he explained that **cloud/browser Excel cannot connect to an external on-prem cube** (only desktop Excel with hard-coded credentials), that a **regular OLAP cube can't role-slice data per user** (you'd need a separate cube per consumer), and that going cloud means moving the whole stack and shifting auth from **LDAP/AD to Microsoft Entra ID SSO**. He estimated standing up the cloud infra (a couple of servers + networking) via Claude Code at **~one week**, with software-side migration on top. Val assigned him the **current-state block diagram** of the CASS/cube/host infrastructure and (with Bosik) the **cloud-cost estimate**. Substance on [[wiki/topics/olap-power-bi-architecture.md]] and [[wiki/topics/ai-assisted-development.md]] (Mar-23). [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## Open commitments

- [ ] Dmitri Kovalchuk — produce a **current-state block diagram** of the as-is CASS/OLAP-cube/intermediate-host infrastructure (no optimization) — due next Monday (~Mar 30 2026) — [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [ ] Dmitri Kovalchuk + [[wiki/people/andrey-bosik.md|Andrei Bosik]] — produce a **cloud-cost estimate** for lift-and-shift of the as-is architecture, two scenarios (keep MS SQL vs migrate to PostgreSQL) — due next Monday (~Mar 30 2026) — [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

## Mar 27 2026 — Review of Engineering Guides: recording access, Jira restructure demo, archive workflow

On the [[wiki/meetings/2026-03-27-review-of-engineering-guides.md|Review of Engineering Guides]] Dmitri raised the prerequisite that the AI needs access to meeting recordings (in Teams only the owner has access) and demonstrated the proposed Jira hierarchy changes live in the sandbox — showing that **renaming** levels preserves relationships but **inserting** a Capability-Ticket level would break **~1,700 parent-child links**. He took the undertaking to prepare an **Excel comparison table** (current vs proposed hierarchy, with factual examples/screenshots) for Val, and to co-own (with [[wiki/people/andrey-bosik.md|Bosik]]) setting up the repository structure for the incoming transcript pipeline (~April 10). Substance on [[wiki/topics/ai-assisted-development.md]] + [[wiki/topics/transcript-knowledge-base-tooling.md]] (Mar-27). [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]] [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]

## Apr 15 2026 — legacy CMS docs check: clarified his cloud-cost estimate was lift-and-shift as-is

On the [[wiki/meetings/2026-04-15-legacy-cms-documentation-progress-check.md|Apr-15 legacy-CMS docs check]] Kovalchuk clarified that the cost figure he had presented earlier was the cost of lifting-and-shifting the legacy CMS infrastructure **as-is** into cloud with no rework — context for why refactoring it first onto cheaper infrastructure (which the documentation pass enables) is the cheaper path. Substance on [[wiki/topics/docs-as-code-and-atlassian-exit.md]] (Apr-15). [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]

## Sept 7 2026 — named as a candidate to take Jira write-up load off Pavel, then passed over

At the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|Sept 7 9:08 Wi-Fi meeting]] (Russian), [[wiki/people/val-levitan.md|Val]] asked whether the Wi-Fi capability write-up could be handed to "Диме Ковальчуку, Андрею Климовичу и Андрею Босику," saying "мне нужна помощь в этом" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

He was not on the call and the work went to [[wiki/people/andrey-bosik.md|Andrei Bosik]] — [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]]. No commitment attaches to Kovalchuk.

## Sept 9 2026 — credited with splitting Flex-Port out of the FP Jira project, and brought into the planning work

At the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] [[wiki/people/pavel.md|Pavel Frolov]] explained why Flex-Port now has its own Jira project and new issue numbering: "[д]о этого у нас флекспорт жил в проекте [ФП]. А сейчас у нас произошло разделение[ —] ну[,] Дима Ковальчук вот эти все… сделал, поэтому мы сейчас переходим на новое [нумерование]." The project name now matches the repository one-to-one. See [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] (Sept 9 2026). [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

[[wiki/people/val-levitan.md|Val]] then named him alongside [[wiki/people/andrey-bosik.md|Andrei Bosik]] as the pair who should take planning off Pavel — "[с] ним[,] Ирой[,] и я бы ещё привлёк Диму Ко[ва]льчука. Они бы вам разложили бы всю эту [работу] по полочкам" — in daily recorded sessions: [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]]. [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]

## Sept 10 2026 — he is the one who can create Jira components, and nobody else can

At the [[wiki/meetings/2026-09-10-capability-requirements-workflow-and-mvp-split.md|Sept-10 2026 5:31 AM transactional call]], the Jira-administration role this page describes shows up as a hard dependency: the group could not tag capabilities by product until he acted. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

- **He confirmed the components do not exist and must be created** in the capability project: "[и]х нету[,] [П]аш… [и]х надо создать[,] в проекте кап[…]" — after [[wiki/people/irina-shishko.md|Irina Shishko]] noted the rest of them cannot add components themselves: "это надо [Д]име тогда заводить компоненты, потому что мы по моему просто так не можем компоненты добавить." [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He asked for the list in writing so he could do it fast:** "[в]ы можете мне список скинуть, я посо[зд]аю быстро… [в] чатик напишите[,] я создам." See [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]]. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- **He was also assigned, with [[wiki/people/andrey-bosik.md|Bosik]], to study the last seven days of capabilities** ahead of the Klimovich walkthrough — the pair named in [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]], here pointed at review rather than planning. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- A small aside from the same call, on his kit rather than his work: he was on background noise without proper headphones, and [[wiki/people/alexander-biratka.md|Biratka]]'s explanation was that as the admin he cannot have them — "[а] он админ[,] у него… не может быть." Recorded as spoken; no equipment policy is asserted. [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Open commitments (Sept 10 2026)

- [ ] Dmitri Kovalchuk — create the FlexPay, Flex-IQ, FlexPort and Terminal Hub components in the capability project — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [ ] Dmitri Kovalchuk and [[wiki/people/andrey-bosik.md|Andrey Bosik]] — study the capabilities created in the last seven days before the Klimovich meeting — due September 10 2026 — [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]

## Sept 11 2026 — called into a meeting for one item, and offers to automate it

Kovalchuk joined the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept-11 8:04 AM call]] near the end, at Val's request, for the capability-workflow question alone — "давайте позовём диму Ковальчука, чтобы он поправил [воркфлоу]". [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

- **His first instinct was to delete the misleading green "Accepted" status; Val said no** and redefined its meaning instead. See [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]]. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He answered Irina's "who moves it to In Progress" with automation:** "[м]ы это можем [за]автоматизировать[:] любая фича, которая начинается [в ин прогресс,] тогда переводит любой [капа]билити из туду в ин[ ]прогр[есс] тоже." He would not do it on the fly — "[п]рям на лету не смогу" — because it needs testing. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **He is also the man Val named, in absentia earlier in the same call, as the person who knows the shared-component problem** and would likely propose solving it as a component. [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open commitments (Sept 11 2026)

- [ ] Dmitri Kovalchuk — automate the capability status transition from feature status (To Do → In Progress and back), after testing — due after Monday Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] Dmitri Kovalchuk — move all MVP 1 capabilities into To Do — due Monday Sept 14 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Sept 14 2026 (in absentia) — his workflow change is asked about, and two people disagree on whether it landed

He was not on the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept-14 8:01 AM call]], but [[wiki/people/val-levitan.md|Val]] opened his process block by asking about him directly: "[К]овальчук[,] поменял ли он [workflow] на… кей[по]б[и]л[и]т[и] [workflow?]" [[wiki/people/andrey-bosik.md|Andrey Bosik]] answered "насколько знаю, да, поменял"; [[wiki/people/pavel.md|Pavel Frolov]] said he still sees the old behaviour — "после [Proposed] Accept это он зелёненьким остался." Nobody resolved it, and Val proceeded on the assumption that it had landed [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

This sits against his two Sept-11 commitments below, one of which — moving all MVP 1 capabilities into To Do — fell due that very Monday. The whole Jira rule set Val then laid down is on [[wiki/decisions/2026-09-14-nothing-in-mvp1-may-still-be-proposed-and-bosik-writes-the-exception-report.md]].

## Open questions (Sept 14 2026)

- **Did the capability workflow change actually take effect?** Bosik says yes, Pavel sees evidence it did not — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## Sept 17 2026 (in absentia) — proposed as "application administrator" for engineering plans, and not yet asked

At the [[wiki/meetings/2026-09-17-kleimenychev-hire-nova-direction-and-planning-handover.md|Sept-17 12:45 PM "General alignment" call]] — which he did not attend — [[wiki/people/val-levitan.md|Val]] proposed taking plan administration off [[wiki/people/pavel.md|Pavel Frolov]] and giving it to him. Val named him ("**Зиму Ковальчука**", the transcript's garble of *Диму*; [[wiki/people/irina-shishko.md|Irina Shishko]] says the name clearly a moment later) and, when Irina asked in what capacity — "**Но дима Ковальчука чисто как?**" — answered "**Как администратора**", then specified the term: "**аппликейщен администратора**", an **application administrator**. [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

**The job as described:** Irina and Pavel sit with him, record the conversation, talk the plans through; he administers them, reports them back on a regular cadence, they correct, he carries on. Val's stated gains were an extra pair of hands, a good administrator, and "**полный трансперация**" — full transparency on plans. Full record on [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]].

**He has not been asked, let alone agreed.** Val handed the persuading to Pavel and Irina in the same breath as the name: "**Както нужно уговорить.**" … "**Это вам.**" Nothing in either source records him being approached. [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

**§4 note.** This mention is an **IT / administration** context — administering plans as a service to the engineering group — which fits the owner-ruled IT "Dima" of this page. It does not resurface the queued ambiguity about a "Dima Kovalchuk" appearing in software-architecture contexts; no architecture or development work is discussed here.

**§15.8:** clear on this entry — role and working method only; no compensation and no personal assessment of him appears in either source. (The same meeting contained assessment material about other named people; it was not ingested — see the meeting stub.)

## Open questions (Sept 17 2026)

- **Will he accept the application-administrator role?** Val instructed Pavel and Irina to persuade him; nothing is agreed and he was not on the call — [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]

## Sept 22 2026 (4:48 AM stand-up) — a status for testing, and a draft overdue-task report

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]:

- **Statuses.** He proposed a status "типа реквистест" for capabilities whose features are done but whose testing is not, and later two statuses. See [[wiki/topics/test-automation-strategy.md]] (Sept 22) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **The report.** He presented a draft personal mailing of overdue, due-today, over-14-day, orphaned and undated tasks, To Do only. See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-22 update) [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Access.** On Daniil's missing access to the knowledge repository: "должно всех доступен быть… По дефолту" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Open commitments (Sept 22 2026)

- [ ] Dmitri Kovalchuk — check why a story cannot move from Request Review to Complete in the "h fm" project settings — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [x] Dmitri Kovalchuk — finish the overdue-task report and send each person their list, after feedback — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]] — **discharged Sept 24 2026:** report finished; email alerts start Sept 25 morning — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]

## Sept 22 2026 (8:01 AM, in absentia) — the green Accepted colour comes back to him

On the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]], Pavel said a task on the Accepted colour had already gone to "диме ковальчуку", yet capability 180 still showed green, "наверное, к этому надо ещё раз подойти". No new task or date was set. See [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] (Sept-22, 8:01 AM update) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## Sept 24 2026 (4:46 AM stand-up) — Req Review, the grey Accept status, and the report goes out

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Statuses.** He added a Req Review status to capabilities and will build a rule moving a capability there from In Progress when all features and stories are green. He moved Accept Capability to grey To Do, because Claude read green as closed. See [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] (Sept-24 update).
- **Completed versus Closed.** His definition: Completed can be sent back; Closed is fully packed up. Same page.
- **The report.** Finished; email alerts start Sept 25 in the morning. To-Do tasks must carry an end date. See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-24 update). This discharges his Sept-22 report commitment above.
- **The Flex IQ emulator.** Pavel asked him to see its features created. See [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-24 update).
- **Access.** He will give [[wiki/people/ivan.md|Ivan]] write access once told where.

## Open commitments (Sept 24 2026)

- [ ] Dmitri Kovalchuk — build the In Progress → Req Review rule — due Sept 24 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [ ] Dmitri Kovalchuk — check the auto-rule so a parent never closes before its children — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [ ] Dmitri Kovalchuk — see that features for the Flex IQ emulator are created, with the Flex-Port firmware protocol as its own feature — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]

## Sept 24 2026 (10:00 AM) — projects match repositories, and the grooming job

At the [[wiki/meetings/2026-09-24-nova-galaxy-jira-hierarchy-cleanup.md|Sept-24 10:00 AM NOVA/Galaxy call]] (Russian) [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]:

- **Project = repository, done.** He had created all projects: "отношение один к одному все репозитории соответствуют проектам в жире". Older extra projects remain; Val: they will be closed.
- **LGS and RGS.** Their keys were already taken by old projects; he proposed keeping the key and renaming the project to match the repository. Val: "Окей класс класс отлично."
- **Filters.** A task already lives in its own project, so that is a grouping; one can filter by release and pick MVP 1. Jira now calls projects "spaces".
- **The grooming.** Val asked him to remove the product IP layer, attach features to existing or new capabilities with Claude, then create the releases as timeline lines. He: "Я могу попробовать"; he cannot yet see the size of the job and will report on Tuesday. Commitment on [[wiki/decisions/2026-09-24-capabilities-sit-in-one-flat-list-under-each-platform-and-releases-are-timeline-lines-not-initiatives.md]]. See also [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-24 10:00 update).

## Open commitments (Sept 24 2026, 10:00 AM)

- [ ] Dmitri Kovalchuk — rename the LGS and RGS Jira projects to match their repositories, keeping the keys (his proposal, which Val approved) — due unspecified — [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Notes_Kleimenich_Hire_Nova_Direction_and_Planning_Handover-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Legacy_CMS_Documentation_Progress_Check-April-15-2026.md]]
- [[raw/Meeting_Transcript_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Notes_Review_of_Engineering_Guides-March-27-2026.md]]
- [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [[raw/Grooming Dashboard for IP-89-March-17-2026.md]]
- [[raw/Setting up JVL ways on GitHub-March-18-2026.md]]
- [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
- [[raw/IT_custom_fields_alignment-February-20-2026.md]]
- [[raw/Introduction to Knowledge Graph Tool-part-1-February-2-2026.md]]
- [[raw/Introduction to Knowledge Graph Tool-part-2-February-2-2026.md]]
- [[raw/One-Drive _ Sharepoint_discussion.md]]
- [[raw/copilot_mcp-september-5-2025.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/it_maturity_update-may-28-2025.md]]
- [[raw/architecture_sql_olap_visualization_1_2025-03-29.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/github_commits-march-26-2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/it_structure_minsk-jan-22-2025.md]]
- [[raw/meeting_various-jan-20-2025.md]]
- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [[raw/Meeting_Notes_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Capability_Requirements_Workflow_and_MVP_Split-September-10-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_NOVA_GALAXY_Jira_Hierarchy_Cleanup-September-24-2026.md]]
