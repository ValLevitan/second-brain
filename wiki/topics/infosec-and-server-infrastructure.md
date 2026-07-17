---
type: topic
title: InfoSec, secrets management and server infrastructure
date: 2025-03-19
aliases: [secrets management, enterprise secrets manager, DevSecOps, Critical Insight, John Luke Peck, Minsk servers, cloud migration costing, Zabbix]
source-count: 5
open-commitments: 2
open-questions: 1
---

# InfoSec, secrets management and server infrastructure

JVL's information-security thread — opened in an evening one-on-one between Val and [[wiki/people/aaron.md|Aaron]] (~Mar 19 2025, date inferred from the transcription stamp; Val called Aaron "after we met late this afternoon and I drove home"). Adjacent to the GitHub-side controls on [[wiki/topics/github-access-and-security-model.md]]. [[raw/info_security_server_infrastructure.md]]

## Secrets management platform — Val's first-priority instinct

- Val's takeaway from the afternoon session: he doesn't need much more before telling the team "go ahead, implement this secrets management platform… as a matter of first priority" — he is "scared of any consequences" of not having one. [[raw/info_security_server_infrastructure.md]]
- Aaron's deployment order: (1) pick the platform whose integrations best fit JVL's tool landscape; (2) weigh pricing/licensing (expensive ones carry unneeded features, free ones lack capacity); (3) weigh vendor support/reputation; (4) the IT services group must buy into managing *all* secrets this new way — service accounts, build systems, Active Directory restore passwords, even router/firewall passwords; then apply the strategy (where the secret server lives, networks assumed secure). [[raw/info_security_server_infrastructure.md]]
- Why it matters (Aaron): cutting someone's access to secrets neutralizes them even if their account still exists — "you're just a regular user at that point"; the only way around it is physical access to the machine. [[raw/info_security_server_infrastructure.md]]
- Vendor datapoints named on the call: Microsoft **Entra** (their renamed SSO-plus platform; Azure Key Vault for Azure apps); **Delenia** (transcript spelling) at "per user licensing of $54 a seat" (looks per-year — ~80 people ≈ $4,000-ish); a tool called **Password State** claiming "unlimited users for $6,000 a year." Aaron: "I think that's kind of the range for this." [[raw/info_security_server_infrastructure.md]]

## The Critical Insight engagement (pending introduction)

- Aaron lined up **John Luke Peck** — "Deputy CISO at Critical Insight" (an InfoSec company; Pacific Northwest), Aaron's former boss at a nuclear engineering company, "probably 41, 40" — to advise JVL. Aaron pushed for an **official engagement with Critical Insight** rather than a private job ("you would get a lot more leverage out of it"), with Aaron staying on as the independent advisory contractor. Val: "Understood… that could be a very healthy engagement and long-term." [[raw/info_security_server_infrastructure.md]]
- Val's framing of the consultant's role vs his own ops people: "not only help, but to have a supreme position over them" — a group that has "de facto done this before" and hands over the recipe. [[raw/info_security_server_infrastructure.md]]

## DevSecOps stance

- Aaron: "DevOps is actually DevSecOps" — security is inserted as *more tests* in the same harness ("Imagine those tests in a row… All you got to do is add more tests. Is this security check in here?…"), extending the Bitbucket-configuration/pull-request tests Anton had been writing. An average security posture, not "super futuristic high-tech bullshit." [[raw/info_security_server_infrastructure.md]]

## Minsk server inventory and cloud-migration costing

- Val, reading his server-infrastructure map: "I don't think there are too many services in Minsk" — entries include **DC App 01** ("Text your packer for building graphic resources for online games 1 through 4 batch" — transcript rendering), **RGS Master 01**, "Endev," "BERT," XP, terminals for access to **CAS servers**, and CAS-WA / CAS-APP / CAS-DB / CAS-OLAP running **Microsoft SQL** (an OLAP production server on "Microsoft SQL 2012 R2"). An **asset inventory in Jira** is being created, which will make this easier. [[raw/info_security_server_infrastructure.md]]
- Aaron's costing method for "what if I moved everything to cloud": pull one-month historical CPU/RAM/storage averages (e.g. from **Zabbix**, if they run it) per server, then price the equivalent rented VM (e.g. "an AWS medium-sized workload dedicated virtual machine host in the North America East region") — a known monthly amount; P2V the lift-and-shift cases. [[raw/info_security_server_infrastructure.md]]
- The abstraction step his ops thinkers miss (named as "Dimitri and… Andre" — the Minsk IT pair, by context [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]]): a production SQL server could be **rented as SQL services** (Azure SQL / AWS MS-SQL) with no OS/VM layers to maintain — higher per-transaction cost, fewer dependency layers. Aaron's car-buying analogy: cash purchase / 48-month loan / 96-month loan / lease each suit different financial standings — cloud services are the lease. [[raw/info_security_server_infrastructure.md]]
- Val's endpoint: stop being the person who worries where laptops and monitors go ("It's only $200. Don't go there") — find JVL people to drive and own this layer. [[raw/info_security_server_infrastructure.md]]

## Apr 16 2025 — assets schema and the secrets-server pick

The thread advanced in a short Apr-16 IT meeting Aaron led ([[wiki/meetings/2025-04-16-it-assets-secrets-server.md]]); the platform choice is now on [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

- **Assets progress:** the IT team creates/routes requests in Jira Service Management and is adopting **Atlassian Assets / Discovery**; [[wiki/people/dmitri-kovalchuk.md|Dmitri]] has automated pulling all computers from Discovery into Jira. **Microsoft Entra** is the source of truth for user records (username/mail) but holds no hardware/software data. Aaron's next step: link the user record to machines via a **last-logged-in-user** automation (copy once, don't churn shared machines), so every ticket can query whose computer it is, its software, and the person's ticket history. Blocker: an old **Windows 2008** box can't export (WMI); upgrade after a **Proxmox node**. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- **Secrets pick:** the team proposes a **Microsoft secret server in Azure (Azure Key Vault)**; Val: "I need this implemented. That's our next thing." The design manages **secrets as assets** (never the value) linked to servers/services, with **Atlassian Automation** granting time-boxed access on help-desk approval — closing the control loop Aaron described in March. Example: manage AWS credentials in the Microsoft vault; manage domain-admin rights as a secret. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- **Availability:** Val cancelled his own Friday session (in transit) but Aaron is bookable Friday **8–10 am ET** for the team's secrets-server questions; team to read the whitepaper. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

## Open commitments

- [ ] Aaron — make the introduction to John Luke Peck / Critical Insight and schedule a (West-coast-friendly, afternoon) call — due unspecified — [[raw/info_security_server_infrastructure.md]]
- [ ] Val — start learning the InfoSec process ("I think I have capacity to learn… listening and absorbing") — due unspecified — [[raw/info_security_server_infrastructure.md]]
- [x] Andrei Bosik + Dima Kovalchuk — read Aaron's secrets-management perspective doc, fill the self-assessment honestly, and produce a rough implementation backlog (start with GitHub CI/CD + AWS/Jenkins keys) — due next meeting Wed May 7 — carried into the May 7 maturity session (see below); Aaron re-set the homework to write risks/policy/requirements and score products — [[raw/secrets_server-apr-30-2025.md]] [[raw/it_department_maturity-may-7-2025.md]]

## Open questions

- Which secrets-management product fits JVL's stack (Entra vs "Delenia"-type vs Password State-type) — **answered Apr-16** toward a Microsoft/Azure secret server (Azure Key Vault); see [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. — [[raw/info_security_server_infrastructure.md]] [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

## Apr 30 2025 — secrets-management strategy session (define the "why" first)

A working session ([[wiki/meetings/2025-04-30-secrets-management-strategy.md]]) with [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] (IT) and [[wiki/people/aaron.md|Aaron]], continuing the Apr-16 secret-server pick ([[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]). [[raw/secrets_server-apr-30-2025.md]]

- **Current state:** JVL uses **KeePass** for passwords (master access held only by **Andrei Bosik and Dima Kovalchuk**) and **AWS Secrets Manager** for RGS on AWS; passwords are strong (≥12 chars). KeePass's single master password is a single point of failure — so, e.g., Pavel/Anton can't get one CI secret without access to everything. [[raw/secrets_server-apr-30-2025.md]]
- **Val's vision:** a central platform that **rotates credentials automatically via API** and integrates with GitHub CI secrets, AWS and Azure at once (rotate a key in all places simultaneously); a **check-out/check-in** model where a returned secret is immediately re-rotated; auth via **identity management (Microsoft Entra)** with user groups/roles. This lets more developers self-serve secrets responsibly instead of routing every request through IT. Example: put [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]'s **Unity license** into CI so Miranda can be built in GitHub Actions. [[raw/secrets_server-apr-30-2025.md]]
- **Approach Aaron pushed:** don't pick a product first — write down the **"why"** and requirements, self-score maturity against an assessment framework he generated (two PDFs, produced via an MCP "thinking"/sequential-reasoning server on his GitHub, published as a container), then build a **backlog** starting with the easiest wins: **GitHub CI/CD actions** and **AWS/Jenkins deployment keys** (Jenkins still deploys to AWS). MCP servers currently use static API keys and "probably should use OAuth." "The cloud is not available in our region" was noted (Claude access blocked on their network). [[raw/secrets_server-apr-30-2025.md]]
- **Homework (Andrei + Dmitry):** read the perspective doc, fill the self-assessment honestly, and produce a rough implementation backlog. Next meeting **Wednesday May 7, 8 am Eastern**. [[raw/secrets_server-apr-30-2025.md]]

## May 7 2025 — IT-maturity coaching: policy → risks → requirements → product

The follow-on session ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]), with [[wiki/people/aaron.md|Aaron]] coaching [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrei (Bosik)]], and [[wiki/people/val-levitan.md|Val]]. Aaron used the still-open secret-server choice to teach a first-principles method rather than let the team "pick any secret server" (a low-maturity reactive move). [[raw/it_department_maturity-may-7-2025.md]]

- **Where to track what:** Jira is for tracking the *work* (specific items you're doing); the *why* and the bigger-picture ideas/objectives belong somewhere else. The IT team had deleted their Confluence page and moved everything into Jira (JSM + an operations-system project); Aaron told them to restart a central place (Confluence) for ideas/objectives — Confluence chosen because it does diagrams and tables (Git only does text/mermaid diagrams). [[raw/it_department_maturity-may-7-2025.md]]
- **The chain:** information-security **policy** (written by the team, not downloaded) responds to a **risk register**; requirements flow from the policy; a secrets manager covers a fraction of those risks; the product that covers them best wins. Aaron framed it as "first-principles thinking" (why do we manage secrets at all → because stale credentials are the top compromise risk). [[raw/it_department_maturity-may-7-2025.md]]
- **Weighted scoring matrix:** the AI-generated evaluation table (moved to Excel) should weight each requirement **1–5** by importance, score each product **1–5** objectively (not "user-friendly," which is subjective — use "implementation complexity"), then multiply weight × score. Candidates named: **Azure Key Vault, AWS Secrets Manager, HashiCorp Vault, Delinea** (transcribed "Delinear/Delenia"), with **Kubernetes Secrets** ruled out and **Cloudflare** mentioned. Current state: **GitHub secret store** (a "secret store," good only for CI/CD) plus **AWS**; Dima works with AWS Secrets Manager, tried Azure Key Vault, used HashiCorp Vault 1–2 years ago. A key requirement Andre raised: a **web UI for users to self-manage their own secrets** (with role-based access), integrating with Microsoft Entra — AWS↔Entra integration is awkward. (Example user given: "Anton Mishkevich" = [[wiki/people/anton-leshkevich.md|Anton Leshkevich]].) [[raw/it_department_maturity-may-7-2025.md]]
- **Homework:** write the risks, a policy, and a list of **policy** (not product) requirements; research each product against the requirements (a day per product); score once and commit; then trial the winning platform before buying. Next meeting in two weeks. This continues, not contradicts, the Apr-16 "pick" and Apr-30 "define the why" — the product remains uncommitted; see [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. [[raw/it_department_maturity-may-7-2025.md]]
- **Val's operating stance** (recorded on [[wiki/topics/jvl-operating-principles.md]]): he does not want a chief-strategist layer for a 30-person shop, can get "80% success" himself, and is unworried about losing "$1,000 a month" on a slightly-wrong product — his fear is stalling ("Alabama mud … one tire spins, the other does nothing"). [[raw/it_department_maturity-may-7-2025.md]]

## May 12 2025 — the ActiveMQ / White Area Host botnet vulnerability

A distinct application-security thread (not secrets management): the **White Area Host** application (transcribed "освах"/"косвах" = **CASWH** / "CasinoLock" — the JVL server app machines talk to, still on SVN) runs an **old ActiveMQ** message broker with a known vulnerability. [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] with [[wiki/people/pavel.md|Pavel]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/val-levitan.md|Val]] worked the fix ([[wiki/meetings/2025-05-12-activemq-white-area-host-upgrade.md]]). [[raw/activeMQ_upgrade-may-12-2025.md]]

- **The exploit:** the vulnerability does **not** give an attacker filesystem or deeper system access (Dima had "cut off everything possible" previously) but lets them **load and execute a file in RAM** — enough to make JVL's machines part of a **botnet** generating "parasitic timing." It **can't be reproduced in the test environment**. Interim mitigations already in place: CASWH runs only ~**3 hours/day** and the exploited protocols were blocked (though an attacker can just change the port). [[raw/activeMQ_upgrade-may-12-2025.md]]
- **The fix (ruling):** upgrade ActiveMQ to a version that closes the vulnerability *and* still lets fielded machines connect (the machine/client side can't be changed), and **split ActiveMQ out of the Java app** into its own application; Docker-container-with-3-hour-restart is the fallback if no compatible fixed version exists. Full detail on [[wiki/decisions/2025-05-12-upgrade-activemq-split-from-white-area-host.md]]. [[raw/activeMQ_upgrade-may-12-2025.md]]

## Sources

- [[raw/info_security_server_infrastructure.md]]
- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/activeMQ_upgrade-may-12-2025.md]]
