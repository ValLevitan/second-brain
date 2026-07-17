---
type: decision
title: Trial Delinea as JVL's secrets-management platform (scored winner over CyberArk)
date: 2025-05-28
aliases: [Delinea, Delenia, secret server trial, secrets manager selection, DTP secret server MVP]
source-count: 1
status: active
open-commitments: 2
---

# Trial Delinea as JVL's secrets-management platform (scored winner over CyberArk)

On the May 28 2025 IT-maturity review ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]) [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/andrey-bosik.md|Andrei (Bosik)]] presented the completed product evaluation to [[wiki/people/val-levitan.md|Val]] and [[wiki/people/aaron.md|Aaron]]. This resolves the long-open "which secrets manager?" question and **supersedes the Apr-16 leading candidate (Microsoft/Azure)** — see [[wiki/decisions/2025-04-16-adopt-azure-microsoft-secret-server.md]]. [[raw/it_maturity_update-may-28-2025.md]]

## What was decided

- **Delinea (transcribed "Delenia"; also garbled "the linear" on the call) scored highest** against the requirement categories the team derived from their information-security policy, so JVL will **trial Delinea** (Delinea gave a trial/trial access the prior week). **CyberArk was the second-scoring product but was rejected as "very expensive."** [[raw/it_maturity_update-may-28-2025.md]]
- **Azure is not a true secret server** — the team clarified Microsoft Azure is "just vault storage, just passwords," so the Apr-16 "Azure secret server" pick is not the direction; Delinea is. [[raw/it_maturity_update-may-28-2025.md]]
- **Trial first, not commit.** Val asked directly whether they are adopting Delinea or trying it; the answer is **trying it first** — build a bounded evaluation so leadership can see how long it takes and know when "enough evaluation" is done. [[raw/it_maturity_update-may-28-2025.md]]
- **Where the work is tracked:** in the **DTP** Jira project (a "secret server / secrets platform" feature item populated with the evaluation stories), not the IT-support ticket project or the IP initiatives project. Andre to build the backlog of evaluation tasks. [[raw/it_maturity_update-may-28-2025.md]]
- **First evaluation steps named:** (1) **connect Azure OIDC authorization to Delinea**; (2) **transfer passwords from KeePass** ("key pass") into the Delinea secret database; then evaluate Delinea against the policy (e.g. the password-retention policy). [[raw/it_maturity_update-may-28-2025.md]]

## Rationale & context

- The evaluation followed Aaron's first-principles method (policy → risk register → requirements → weighted scoring → trial), so the choice is grounded in JVL's own written information-security policy rather than picking a product blind. Full method on [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/it_maturity_update-may-28-2025.md]]
- Aaron's coaching frame: define the backlog before starting so JVL can "call the shot" (his golf/pool analogy) — know the evaluation criteria and roughly how long, then stop when the checkboxes are covered. [[raw/it_maturity_update-may-28-2025.md]]

## Open commitments

- [ ] Andrei (Bosik) — build the DTP "secret server MVP" feature backlog (the evaluation tasks/stories, ordered), starting with Azure-OIDC→Delinea and KeePass→Delinea migration — due ~May 28–29 (Wednesday/Thursday) — [[raw/it_maturity_update-may-28-2025.md]]
- [ ] Dmitri Kovalchuk + Andrei (Bosik) — begin implementing/evaluating Delinea against the policy once the backlog exists (Dima can start first; Andre has GitHub-Actions-for-UEFIM work in front of it) — due ~next week — [[raw/it_maturity_update-may-28-2025.md]]

## Sources

- [[raw/it_maturity_update-may-28-2025.md]]
