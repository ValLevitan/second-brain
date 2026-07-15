---
type: topic
title: InfoSec, secrets management and server infrastructure
date: 2025-03-19
aliases: [secrets management, enterprise secrets manager, DevSecOps, Critical Insight, John Luke Peck, Minsk servers, cloud migration costing, Zabbix]
source-count: 2
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

## Open questions

- Which secrets-management product fits JVL's stack (Entra vs "Delenia"-type vs Password State-type) — **answered Apr-16** toward a Microsoft/Azure secret server (Azure Key Vault); see [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. — [[raw/info_security_server_infrastructure.md]] [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

## Sources

- [[raw/info_security_server_infrastructure.md]]
- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
