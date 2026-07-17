---
type: decision
title: Secrets-management platform evaluation (Azure candidate → superseded by Delinea trial); manage secrets as assets
date: 2025-04-16
aliases: [Azure Key Vault secret server, secrets as assets, Microsoft secret server, secrets management platform choice]
source-count: 4
status: superseded
---

# Adopt a Microsoft/Azure secret server and manage secrets as assets

In the Apr-16 IT meeting ([[wiki/meetings/2025-04-16-it-assets-secrets-server.md]]) the IT team proposed a secrets-management platform and Val endorsed implementing it — advancing the Mar-19 InfoSec thread ([[wiki/topics/infosec-and-server-infrastructure.md]]), which had left the product choice open.

## What was decided

- **Use a Microsoft secret server in Microsoft Azure (Azure Key Vault).** The IT team researched the topic and proposes it because JVL's servers and devices already have internet access to reach the Azure portal for secrets. Val: "I need this implemented. That's our next thing," and asked the team to read the secrets-server whitepaper. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- **Manage secrets as assets, not the secret values.** Secrets (e.g. AWS credentials, domain-admin rights) are tracked as asset objects linked to the servers/services that use them; access is requested through the help desk, an admin approves/declines, and **Atlassian Automation** calls the Azure vault to grant that user rights to that secret for a set period — removing the human from the granting step and closing the audit loop. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- **Assets foundation first:** [[wiki/people/dmitri-kovalchuk.md|Dmitri]] has automated pulling computers from Atlassian Discovery into Jira; the next step is linking the **user record** (source of truth = **Microsoft Entra**, which lacks hardware/software data) to machines via a last-logged-in-user automation, so every ticket can show whose computer/software it is. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

## Rationale & context

- Aaron's security logic (from Mar-19 and restated): cutting a user's secret access neutralizes them even if their account exists. Val's own example — manage a **domain-administrator** credential as a secret while being a plain local admin on his own machine. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- Blocker noted: an old **Windows 2008** box can't export its info (WMI issues) and will be upgraded after a **Proxmox node** is installed. [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]

## Status

**Superseded 2025-05-28** (platform element). As of 2025-04-16 this was a leading direction; Apr-30 and May-7 kept the product uncommitted; **May-28 the scoring picked Delinea to trial and ruled Azure "not a secret server"** — see the May-28 section below and [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md]]. The "secrets-as-assets" control model and assets foundation are not superseded.

## Apr 30 2025 — still exploratory; define the "why" and build a backlog

Two weeks on ([[wiki/meetings/2025-04-30-secrets-management-strategy.md]]) the choice is not yet committed to a specific product. Andrei Bosik was "reading information" comparing **Microsoft, AWS and Delinea** (as transcribed "Delenia") secret managers and had registered with Microsoft to try it. Aaron reframed the task: define the "why" and requirements, self-score maturity, then build an implementation backlog starting with **GitHub CI/CD actions and AWS/Jenkins deployment keys** — rather than pick a platform blind. Current state remains **KeePass + AWS Secrets Manager**. Detail on [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/secrets_server-apr-30-2025.md]]

## May 7 2025 — still uncommitted; formal weighted-matrix evaluation

Three weeks on ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]) the product is still not committed. Aaron coached the IT team through a **weighted scoring matrix** (requirement weight 1–5 × product score 1–5) driven from a written information-security policy and risk register, with candidates **Azure Key Vault, AWS Secrets Manager, HashiCorp Vault and Delinea** (transcribed "Delinear/Delenia"); Kubernetes Secrets ruled out. A user-facing **web UI for self-managed secrets** (role-based, Entra-integrated) surfaced as a key requirement. Current state stays **GitHub secret store (CI/CD only) + AWS Secrets Manager**. The Apr-16 "Azure Key Vault" framing is therefore best read as a leading candidate, not a locked choice — the team is to research/score before trialing a winner. Detail on [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/it_department_maturity-may-7-2025.md]]

## May 28 2025 — superseded: Delinea chosen, Azure is "not a secret server"

The evaluation concluded on May 28 ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]): after scoring products against the written policy, the team picked **Delinea** to trial (CyberArk second, "very expensive"), and clarified that **Microsoft Azure is "just vault storage, just passwords" — not a true secret server**. So the Apr-16 "Azure Key Vault" *platform pick* is **superseded** by [[wiki/decisions/2025-05-28-trial-delinea-secrets-management.md]]. What survives from this decision is the **"manage secrets as assets" control model** (secrets as asset objects, help-desk-approved time-boxed access via Atlassian Automation) and the **assets-foundation work** (Discovery→Jira, Entra as user source of truth), which remain the intended design regardless of the chosen vault. [[raw/it_maturity_update-may-28-2025.md]]

## Sources

- [[raw/it_automation_schemas_secrets_server-apr-16-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/it_maturity_update-may-28-2025.md]]
