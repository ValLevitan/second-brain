---
type: decision
title: Migrate the legacy CMS from SVN to GitHub, organized by feature
date: 2025-03-23
aliases: [CMS migration, CMS to GitHub, CMS SVN to Git, Protohost migration, understanding CMS repo]
status: active
source-count: 4
---

# Migrate the legacy CMS from SVN to GitHub, organized by feature

**Decision (Val, Mar 23 2025):** move JVL's **legacy CMS** (the ~20–30-year-old machine content-management system, today living in **SVN**) into **GitHub**, organizing the repositories so their branches represent **feature branches**, where every feature traces back to a **requirement**. The current sprint's concrete step: move the **Protohost** library (a CMS artifact) from SVN to GitHub. [[raw/cms_persona_requirements-march-23-2025.md]]

## The logic Val laid out

- The chain is **requirements → features → code**; "no one needs a feature if there is no requirement for it." A repo's branches should each be a feature; the repository itself is the product. [[raw/cms_persona_requirements-march-23-2025.md]]
- Val's blunt version: the only truth is **committed code**; between a requirement and code sits "the spending of money," and he wants to measure the time from requirement to code. [[raw/cms_persona_requirements-march-23-2025.md]]
- Deliberately a **"start from the end"** exercise on a legacy product: aim for ~**80% accuracy** (the 80/20 rule), don't chase perfection, **freeze/preserve** the current code, then move on to designing the new orchestration platform. [[raw/cms_persona_requirements-march-23-2025.md]]
- It doubles as a **training exercise** for [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] and the backend "Dima" ([[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] by context) before they tackle the new platform. [[raw/cms_persona_requirements-march-23-2025.md]]

## One repo vs. many — modular, not microservices

- Dima proposed a **microservices** architecture with a repository per microservice (~10 repos, since the CMS is ~10 modules). Val/Aaron pushed back: if disabling half the services breaks the system for a user, it is **not** microservices — it is a **modular** architecture. Aaron recommended **one repository** rather than ten (ten repos = ten times the rules/overhead). **Resolved: try to fit everything into one repository** (Dima accepted, pending understanding the structure). [[raw/cms_persona_requirements-march-23-2025.md]]

## Housekeeping

- The Git repo initially named "understandings" / "понятия CMS" is to be **renamed to "CMS"** (Andre — [[wiki/people/andrey-bosik.md|Andrey Bosik]] — actioned). Val had put an AI-written description of the current CMS (from Dima's whiteboard **CMS legacy block diagram**) into the repo as a starting "understanding" markdown file. [[raw/cms_persona_requirements-march-23-2025.md]]

Related requirements/persona critique on the same call: [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. Meeting stub: [[wiki/meetings/2025-03-23-cms-persona-requirements.md]].

## Follow-up (~Mar 25 2025, date inferred)

- Two days on, Val walked Chudinov/Tsymanov through the concrete review workflow for the AI-generated overview/use-cases/requirements now in the GitHub "Observability Platform" org (pull-requests-only corrections, ~80% good-enough bar, requirements→features→code→actions→deploy→**conserve**), ruled progressive/розыгрыш in scope and the org name unchanged, and held the line against Dima's adapt-don't-rebuild pushback. Details on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]; stub [[wiki/meetings/2025-03-25-cms-requirements-review-workflow.md]]. [[raw/cms_requirements_development-dzima-sergei-andrei.md]]

## Update — staged plan supersedes the initial by-features reorganization (Apr 14–15 2025)

- After two more sessions with Chudinov/Tsymanov/Bosik, the *initial* GitHub move was re-scoped to an **as-is transfer with no feature-branch reorganization** (and only if it fits Val's ~5-working-day rule); the by-features/product-repo organization is deferred to the staged **CMS 1.5 / CMS 2.0** plan. The direction of this decision stands; its method evolved — see [[wiki/decisions/2025-04-15-cms-staged-migration-plan.md]]. [[raw/cms_svn_github-april-14-2025.md]] [[raw/cms_github_svn-apr-15-2025.md]]

## Sources

- [[raw/cms_persona_requirements-march-23-2025.md]]
- [[raw/cms_requirements_development-dzima-sergei-andrei.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
