---
type: person
title: Dmitri Kovalchuk
date: 2026-07-13
aliases: [Dmitri Kovalchuk, Dmitry Kovalchuk, Dima Kovalchuk, Dima]
disambiguation: "IT (GitHub-admin, infrastructure, secrets/Azure, AI-tool accounts) — the IT-context "Dima". Dima/Dmitry cluster (3, owner-ruled): [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]=IT / [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]=Senior 3D designer / [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]=back-end. Resolve by context; queue if none."
source-count: 70
open-commitments: 16
open-questions: 3
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

## Sept 25 2026 (4:57 AM stand-up) — the discipline emails go out

At the [[wiki/meetings/2026-09-25-daily-standup-engineering-menu-and-jira-discipline.md|Sept-25 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]:

- **The emails are live.** The first went out that morning, only to people with problems, and they will come "Каждое утро". He showed HFM-671 (end date September 5), and named the other checks: over 14 days In Progress, a child open under a closed parent, a To-Do task with no dates. Fixes take "5, 10 минут через клод". See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-25 update).
- **A second message.** Chudinov got a "hierarchy exceptions, Friday 25" message; Kovalchuk said it is a different one and he will come and look at it.

## Sept 25 2026 (7:33 AM) — tasks straight to Claude, a shared knowledge base, and homework

At the [[wiki/meetings/2026-09-25-ai-project-manager-for-jira.md|Sept-25 "JIRA management AI" call]] (Russian) [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]:

- **Two problems, not one.** He split Val's problem into "не на кого назначить" and "нечего назначить" (tasks are not created).
- **Assign tasks to Claude.** He proposed assigning some Jira tasks directly to Claude, which would open a pull request; JVL once tried to connect this and it stalled. Not adopted; Val wants it studied.
- **A shared knowledge base.** Topics cross between meetings, so he suggested a server with one large knowledge base, like a second brain in Obsidian. He warned the data would be large and expensive, and that a pull request alone does not tell the AI to act.
- **Homework.** He proposed that each person design their own version of the AI project manager before the next meeting; Val agreed. See [[wiki/decisions/2026-09-25-one-company-second-brain-feeds-an-ai-project-manager-for-jira.md]].

## Open commitments (Sept 25 2026)

- [ ] Dmitri Kovalchuk — look at the "Jira hierarchy exceptions" message Chudinov received — due unspecified ("я к тебе подойду") — [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [x] Dmitri Kovalchuk (with the others on the call) — think through how he would build the AI project manager — due Tuesday Sept 29 2026, 7:00 — [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]] — **discharged Sept 29 2026:** the design meeting was held; see below — [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

## Sept 25 2026 (9:02 AM) — project equals repository, and repositories come first

At the [[wiki/meetings/2026-09-25-games-conversion-repos-jira-capabilities.md|Sept-25 9:02 AM games-conversion session]] (Russian) [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]:

- **Initiative vs project.** When Val said he mixes them up, he answered "Проект равно репозиторию" and read the standard: an initiative is a long direction with several releases that "будет объединять несколько проектов"; capabilities gather features, and features "лежат в проектах".
- **Order.** "Сначала репозитории создаем. Потом проект", because Jira project names match repository names.
- **His job.** Val: he opens the two Jira projects for the conversion work. Detail on [[wiki/decisions/2026-09-25-the-conversion-experiment-closes-and-the-converter-gets-its-own-project-and-repository.md]].

## Open commitments (Sept 25 2026, 9:02 AM)

- [ ] Dmitri Kovalchuk — open the two Jira projects for the games-conversion work, named to match the repositories — due after the repositories exist — [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]

## Sept 28 2026 — two daily Jira reports, and "name the CAP and the feature"

At the end of the [[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]] (Russian) he said two reports now arrive — Jira hierarchy (tied to MVP 1) and Jira discipline (statuses and dates) — and asked people not to break statuses. Because the meetings may later be read by AI, he proposed that everyone name the exact CAP and feature they work on; Pavel agreed. See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-28 update) [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].

## Sept 29 2026 (4:49 AM) — "есть динамика", and access for Vladimir

At the end of the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian): "Владимиру я доступа дал уже на репетитории тинты" (the TINT test repositories, by context), and on the reports: "ребята молодцы… [з]акрывают, следят да, по крайней мере есть динамика". See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-29 update) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

## Sept 29 2026 (6:02 AM) — at the AI PM design call: a task type at the top, who is responsible, and the absent code owner

At the [[wiki/meetings/2026-09-29-ai-pm-architecture-and-second-brain-plan.md|Sept-29 "Design_AI-PM" call]] (Russian) [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]; the project is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]]:

- **Against "drafts get lost".** "можно создать какойто тип задачи, определённый… проект, который будет… автоматически отображаться тебе в плане… на самом верху".
- **"Как определить ответственного."** His dilemma; Val's answer was no human responsible — the AI PM is an autonomous role.
- **The absent code owner.** If a code owner is not at the meeting, "PM создаст кучу задач, он придёт к паше условному либо к Ирине и спросит" — Bosik and Pavel called it the rare case.
- **References.** Keeping the transcripts means the AI "сможет сослаться куда то вот здесь тогда то принято такоето решение".
- He asked Val whether he could describe the character he wants for the AI PM.

## Sept 30 2026 — "watch your dates and statuses", and tasks go in the repository you work in

At the end of the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian): "Работать особо нечего сказать. Смотрите за датами статусами… Задачи создавайте в тех репозиториях, в которых работаете. Имя репозитории соответствует имени [проекта]" (last word garbled). Pavel: "есть такое тоже надо на свои посмотреть". See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Sept-30 update) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

## Oct 1 2026 — "dates slipped", Request Review was Lena's team's status, and he adds the Completed → To Do transition

At the end of the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]: "даты у некоторых задачах посъезжали. Это просрочен." In the status argument his discipline email started: "Теперь открывать, мне кажется, тоже не самый правильный вариант"; "Реквист ревью вроде только для ковапелити обсуждали"; the Capability Amendment "это если бак какой то был найден в полях… а [capability] типа уже закрыт"; "**Вообще этот рекластью был только для лениных**… для лены создавался у них там есть такая штука, когда Майкл проверял. То, что нарисовали и переводил дальше, то есть у нас для разработчиков такое не использовалось" ([[wiki/people/lena.md|Lena]]'s team; Michael read as Michael Gottlieb — inference); and the change: "он закончил свою работу, да он перевёл в комплект" — Irina: "Только из комплект в туду" — "**Хорошо, я добавлю.**… Давайте и Добавим." See [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]] and [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Oct-1 update).

## Open commitments (Oct 1 2026)

- [ ] Dmitri Kovalchuk — add the Completed → To Do transition to the feature workflow in Jira — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: not mentioned* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

## Oct 2 2026 (4:50 AM) — "не забивать на счет жира дисциплин", ask Claude to move dates, today's date in red, and a due date fixed live

At the end of the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]: "хотел попросить не забивать на счет жира дисциплин и и просить клоды. Тогда есть ли там нужно подвинуть сроки? Он замечательно подвиннет там попросить его подвинуть сроки на завтра и на такое число есть ручками. Это тяжело делать." To Chudinov's "Жира подсвечивает красным сегодняшнее же число": "Я б я внесу изменения… просто джира сама подсвечивает, то есть у тебя [репорт] подсвечивает, исходя из Того, что джира тоже подсвечивает сегодняшнее число. То есть в самой джире я этого брать не могу. Я могу это убрать из репорта… Давайте попробуем почитать, может быть, может быть, это и можно." Earlier he fixed a due date (on Kharetski's items by position in the round — inference) at Pavel's word ("Я поставлю какую дату поставить" — "поставь неделю назад"), and on Val's repository message: "Да, это [Вал] всем написал." See [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Oct-2 update) and [[wiki/topics/ai-assisted-development.md]] (Oct 2).

## Oct 2 2026 (7:32 AM) — "14 ноль ноль по идее по нашему"

On the [[wiki/meetings/2026-10-02-ai-pm-status-listener-core-and-318-transcripts.md|"Design_AI-PM - status" call]] (Russian) he spoke once, converting Val's "07:00" for the Tuesday status: "14 ноль ноль по идее по нашему" [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]. Bosik told Pavel the agent's knowledge base includes "вот эти отчёты" (the derived notes read them as Kovalchuk's Jira-discipline reports — a reading; see [[wiki/projects/ai-project-manager-and-company-second-brain.md]], Oct 2).

## Open commitments (Oct 2 2026)

- [x] Dmitri Kovalchuk — take the red highlight on today's date out of his report, and read whether Jira itself can stop highlighting the current day — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: done in the report ("убрал сегодняшнюю дату"); Jira itself not mentioned* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 5 2026 (4:54 AM) — today's date out of the report, four weekend automations, and the reopen cascade to build

At the end of the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]: "Я и [из отчёта] убрал сегодняшнюю дату, чтобы вас не мучило что? То задачи сегодня стекают. А на выходных ещё написал 4 автоматизации, которые должны. Немножко помогать с очередями, то есть если все дочерние фичи в статусе. Комплект то [капабилити] должна будет автоматически перевестись [в] реквист ревью. Вот так что если кого то что то не будет работать, пожалуйста, сообщайте." Working out Chudinov's request: "получается, [story] в туду стоит, и ты хочешь, чтобы фичи переводилась из комплитов в [In Progress]"; "Получается [фичу] из комплитов в [To Do] переводим… Из [Request Review] туда." Earlier, on Chudinov's camera: "Дима скрытой." Ruling: [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]]; see also [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Oct-5 update).

### Open commitments (Oct 5 2026)

- [ ] Dmitri Kovalchuk — automate the reopen: a story created under a Completed feature moves the feature Completed → To Do and its capability Request Review → To Do — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

### Open questions (Oct 5 2026)

- What the other three of his four weekend automations do — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Oct 6 2026 — the warning triangle and the status flow stay

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]: he asked everyone to watch their due dates, and raised Jira's warning triangle and the Proposed / Accepted / To Do flow. Both stay as they are — see [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]]. He offered to search Jira and remove MudaGoose tasks; Pavel said Jira is not the problem.

## Oct 7 2026 — overdue dates, the AI pilot reads the stand-ups, and the Jira Hierarchy report

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian; speaker label) [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]:

- "не забывайте про сроки просроченных сдач" — Biratka has "порядка 17".
- "митинги уже будут уже пилот обрабатываются искусственным интеллектом и должны будут создаваться задачи… Желательно с номерами" — [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Oct 7).
- On Irina's 44 regulations: the hierarchy report is Andrei's ("Андрея спрашивать"); the comments say the regulations are "активная, но они не опубликованы" — [[wiki/decisions/2026-09-17-planning-comes-off-pavel-and-goes-to-an-application-administrator.md]] (Oct-7 update).

## Oct 8 2026 — watch your dates; a glossary of Jira codes for the PM agent

At the close of the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]: "все молодцы, что следите за сроками", keep watching them. For the PM agent, a glossary of the Russian pronunciation of Jira project codes is needed, "Потому что, скорее всего, он их не поймет" — [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Oct 8). No owner was named.


## Oct 8 2026 (8:31 AM) — working on the second brain; the AI Draft window

- At the [[wiki/meetings/2026-10-08-ai-pm-listener-scope-draft-lifetime-and-october-12-go-live.md|Oct-8 AI-PM review]] Bosik reported that Kovalchuk ("Дима") has started work on the company second brain [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].
- He showed the feature the agent created from the Oct 6 meeting, linked to capability 259 [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].
- On the "AI Draft" lifetime he argued one day is too short: a meeting at 19:00 Minsk time will not be seen by morning, so the agent would delete what nobody has looked at. He also suggested a rule that people must review the created items within a set time. The window was not ruled — see [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## Open commitments (Oct 8 2026)

- [ ] Dmitri Kovalchuk — continue building the company second brain — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

## Oct 9 2026 — the PM agent "Dasha" in test mode; production Monday

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]]: "её будут звать пока что даша, возможно потом переименуем"; tasks may appear in the test project; production planned for Monday "если мы все успеем"; tasks come as drafts to accept or reject — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-9 update) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Oct 12 2026 — the Claude bot balance; the Jira "In Progress" automation; the AI PM starts

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 stand-up]]: the Claude bot has almost 300 Canadian dollars; some top-ups are refused, likely by the bank's security; he will not use another card without approval — [[wiki/topics/test-automation-strategy.md]] (Oct 12). He explained the automation that opens a task on any branch, commit or pull-request mention and proposed turning it off (not confirmed) — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-12 update). He told the team the AI PM starts today and that "AI Draft" tasks are rejected with a resolution — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-12 update) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Oct 13 2026 — the PM agent's questions; an issue type for release work with no branches; "watch your dates"

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 stand-up]]: he asked whether to discuss the PM agent's morning questions — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-13 update); he raised release work that has no code branches and asked for a new issue type or a Task raised in the hierarchy — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-13 update); and he reminded everyone: "не забывайте про сроки" [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

## Oct 14 2026 — walks the team through the AI digest; asks Andrei about the missing meeting

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 stand-up]] he shared the AI agent's daily digest (merged Oct-13 and Oct-14 items; same-name mix-ups; very cautious about Jira) and will ask Andrei why the two-hour Oct-13 meeting is not in it — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-14 update). He said he and "Дима" agree Tsymanov was right about a release branch — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]] (Oct-14 update). Pavel asked that he add the AI-created leak task to the team dashboard — [[wiki/topics/nova-platform-architecture.md]] (Oct 14) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

## Oct 14 2026 (10:03 AM) — at the AI PM update; "Дима… на финальной стадии"

On the [[wiki/meetings/2026-10-14-ai-pm-keep-the-0-80-threshold-and-meeting-rigor.md|Oct-14 AI PM update]] (Russian) with Val and Bosik; the notes confirm both names but do not mark who is Speaker 2, 3 or 4 [[raw/Meeting_Notes_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]. Val addressed him at the end: "Дима, у вас что-то было? Вы хотели что-то сказать, и я вас перебил" [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]. Speaker 2 said "Дима… трудится уже где-то на финальной стадии", with a launch maybe on Friday (Oct 16) — what it is is not said; his second brain work (Oct 8) is a possible reading (**inference**) [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]. Val kept the AI PM's 0.80 threshold and asked for more concrete meetings — [[wiki/decisions/2026-10-14-the-ai-pm-keeps-its-0-80-confidence-threshold-and-meetings-get-more-concrete-instead.md]].

## Oct 15 2026 — "address the agent directly"; "Dasha" is a bad name; the digest

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]: he told Khamin the agent creates something only when asked directly and ignores items below its threshold; the team found "Dasha" a bad name; he read the previous day's digest (MVP 1 to the 8th–9th of November as a comment on AIP-744) and explained that decisions go in as comments, not tasks — [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Oct 15). He is already adding the board filters so Daniil's task shows — [[wiki/topics/nova-platform-architecture.md]] (Oct 15).

## Oct 16 2026 — AI Draft lasts 24 hours; AI Draft on the dashboard; LGS 1226 / 1228; closed parents with open children

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] he told the team an AI Draft task must be moved to To Do or Reject within 24 hours or it disappears, agreed to show AI Draft in the dashboard's To Do column, reported the agent's three tasks and its LGS 1226 / 1228 links for checking, and raised closed parents with children in Backlog — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-16 update).

## Oct 19 2026 — about 11 tasks under a closed parent

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] he asked Pavel to review about 11 tasks whose parent is closed and suggested creating something to hang such stories on so they do not drop down the plan; he reminded Biratka that an AI Draft disappears after a day — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-19 update).

## Oct 19 2026 (in absentia) — to open the Jira projects for the first three hardware repositories

At the [[wiki/meetings/2026-10-19-github-msbc-repositories-per-project-mery-purchasing-endpoints-and-ai-coo.md|Oct 19 5:02 PM "GitHub-MSBC" meeting]] (English) Val: "Dima at the same time opens projects. You have to have projects in order to have a repository," and later "ask Dmitri Kovalchuk… To create 3 projects" — matching the harness, display and sheet-metal repositories; Nathan makes the request [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]. Record: [[wiki/decisions/2026-10-19-hardware-repositories-start-with-harness-display-and-sheet-metal-and-the-agent-generates-data-contracts-from-vetted-data-sheets.md]].

At the [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct-20 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]] he explained that the AI PM gets the recording about an hour later, assigns by keywords, and cannot yet act on "change this, add that" instructions; on naming it, "не Даша" — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-20 update). He relayed from Andrei that the self-hosted runners show no problems in monitoring — [[wiki/topics/test-automation-strategy.md]] (Oct 20). Per the notes he is to give Daniil access to the Clover Fortune repository — [[wiki/topics/nova-platform-architecture.md]] (Oct 20).

## Oct 21 2026 — the agent's comparison task and Pavel's AI Draft

At the [[wiki/meetings/2026-10-21-daily-standup-flex-port-mode-switch-and-sas-crc-fix.md|Oct-21 stand-up]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]] he told Pavel he should have an AI Draft, and asked Biratka about the Flex IQ / Flex-Port comparison the agent could not place in a project; Biratka said the work was done with 8–10 tasks — [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-21 update).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Status_Listener_Core_and_318_Transcripts-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Architecture_and_Second_Brain_Plan-September-29-2026.md]]

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
- [[raw/Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026.md]]
- [[raw/Meeting_Transcript_AI_Project_Manager_for_Jira-September-25-2026.md]]
- [[raw/Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Keep_080_Threshold_and_Meeting_Rigor-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_IO_Board_Firmware_via_GitHub_and_VP9_Video_Decode-October-20-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026.md]]
