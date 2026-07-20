---
type: decision
title: Secrets-management platform trial — Delinea (May 28) → Keeper (Jul 23 pivot)
date: 2025-05-28
aliases: [Delinea, Delenia, Keeper, secret server trial, secrets manager selection, DTP secret server MVP]
source-count: 2
status: active
open-commitments: 2
---

# Secrets-management platform trial — Delinea (May 28) → Keeper (Jul 23 pivot)

**Status note (Jul 23 2025):** the titular **Delinea** trial is being displaced — after using it the IT team recommends **Keeper** instead (cheaper, unlimited servers, Docker gateway, more user-friendly, Entra SSO). The core decision (adopt a scored, policy-driven secret server) stands; the *product* is pivoting. Not yet formally locked by Val ("assuming Keeper is it"). See the Jul-23 section below.

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

## Jul 23 2025 — pivot toward Keeper

On the Jul-23 IT-maturity session ([[wiki/meetings/2025-07-23-it-capability-maturity.md]]), Andrei Bosik and Dmitri Kovalchuk reported that working with the Delinea trial surfaced restrictions/issues, and recommended **Keeper** as the replacement. Their comparison (corporate/vendor economics, allowed): **Delinea ≈ $22,000 and priced per connected server**; **Keeper ≈ $5,000–$7,000 with unlimited servers**, a **Docker-container gateway** (vs Delinea's Windows-server-only), **Entra ID SSO**, session recording, and time-boxed connection/credential sharing. Aaron did not object but pushed to prove the full use-case set (developers, GitHub Actions, NPM tokens, SSH) before purchase. Val treated the secret server as the **last stumbling block** of the IT transformation and was comfortable proceeding — but did not issue a formal lock. Full detail on [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/IT_capability_maturity-july-23-2025.md]]

## Sources

- [[raw/it_maturity_update-may-28-2025.md]]
- [[raw/IT_capability_maturity-july-23-2025.md]]
