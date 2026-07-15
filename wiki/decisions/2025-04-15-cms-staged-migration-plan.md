---
type: decision
title: CMS moves in stages — 1.0 as-is (only if quick), 1.5 segmented on the same stack, 2.0 new platform
date: 2025-04-15
aliases: [CMS 1.5 plan, CMS staged migration, CMS 1.0 1.5 2.0, five-day rule]
status: active
source-count: 2
open-commitments: 3
---

# CMS moves in stages — CMS 1.0 / 1.5 / 2.0

Settled across the Apr 14–15 2025 pair of sessions ([[wiki/meetings/2025-04-14-cms-svn-github-product-repos.md]], [[wiki/meetings/2025-04-15-cms-migration-staged-decision.md]]) between Val, [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] and [[wiki/people/andrey-bosik.md|Andrey Bosik]].

## The decision

- **Do not split the legacy CMS monolith now.** The team's verdict ("по нашему вердикту лучше нам не разбивать на моторе, иначе мы просто создадим лишнюю работу") stood after two days of debate; Val accepted it — "последнее слово надо отдать разработчикам" (Bosik's framing). Scope: ~**15 SVN repositories** ("Их набралось аж 15 штук"), one big Core among them; the shared **monolithic database is not split** either (Chudinov: splitting it "чревато проблемами"). [[raw/cms_github_svn-apr-15-2025.md]] [[raw/cms_svn_github-april-14-2025.md]]
- **CMS 1.0 → GitHub only if it's quick — Val's five-day rule.** The as-is SVN→GitHub move (code carried over with no feature branches — "мы как бы делаем фиктивный такой перенос," Actions re-creating today's deploys) goes ahead **only if Chudinov/Tsymanov size it at ~5 working days (~2 calendar weeks)**; at "недели, 2-3 недели … Я советую это не делать" — three-week jobs always balloon. Chudinov's first estimate was "полтора спринта, реально два спринта" (≈ a month), which Val rejected as not worth it; Chudinov and Tsymanov to re-scope the real code volume and report. Until then development continues in SVN as today. [[raw/cms_github_svn-apr-15-2025.md]]
- **CMS 1.5 — the intermediate target Val named on the call:** same tech stack with **updated libraries** (updating libraries addresses the security concern; Chudinov confirmed they can be updated on today's stack), re-cut into **segmented products**, then moved to GitHub. "Мой путь с этой 1.5, он дольше, но он спокойнее и надежен." [[raw/cms_github_svn-apr-15-2025.md]]
- **CMS 2.0 — the new-technology platform** opened as its own initiative, laid out in Jira (products → features; each Jira feature branch maps to a GitHub branch), fed by the persona/requirements work. Product-splitting happens "в разговоре" (talk + Jira schematics) while the team keeps working in SVN. [[raw/cms_github_svn-apr-15-2025.md]]
- **Priority above all of it: the machine-software "manifests" product** — the server-side knowledge of an ISO release (game settings, progressives, number of bet buttons) now filled in by hand ("либо я, либо Паша, либо Ира" — error-prone) must become a product ("какой-то из GM Software Database Knowledge … Манифест довольно неплохое название"), needed because **Omni ships in ~1.5 months (June)** and the server must configure Omni machines. It is a separate product, "это уже пойдет не в монолит точно," and depends on LGS, Omni "и математику Ефима" ([[wiki/people/efim-podvoiski.md|Efim]]'s math). Chudinov to talk to Pasha and initiate a manifests meeting "со всеми заинтересованными" (incl. Pavel and Sasha Biratka). [[raw/cms_github_svn-apr-15-2025.md]]

## Why (the reasons collected on the calls)

The team's own reasons for eventually leaving the monolith: (1) **fault isolation** — "если один работает нестабильно на сервере … перестают работать все," while machine-licence issuance "должны продолжать работать всегда"; (2) **management visibility** — per-product development instead of one opaque monolith; (3) **tech-stack/security refresh** — outdated libraries; (4) resilience/отказоустойчивость. Val's counter-frame: library updates + partial stack changes solve security, so the real pain is monolith-vs-modules, best handled stepwise. [[raw/cms_github_svn-apr-15-2025.md]]

## Relation to earlier decisions

- **Evolves [[wiki/decisions/2025-03-23-migrate-legacy-cms-svn-to-github-by-features.md]]:** the Mar-23 intent (CMS to GitHub, organized by features, one repo) survives as direction, but the *initial* move is now explicitly **as-is with no feature-branch reorganization**, gated by the five-day rule; the by-features/product organization is deferred to the CMS 1.5/2.0 stages. [[raw/cms_github_svn-apr-15-2025.md]]
- Val's one-product-one-repository doctrine argued on Apr 14 (product = ISO image or production server, shipped by GitHub Actions) is recorded on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]]. [[raw/cms_svn_github-april-14-2025.md]]

## Open commitments

- [ ] Dmitri Chudinov + Sergey Tsymanov — size the real SVN→GitHub transfer volume against the five-day rule and report (email or the Thursday meeting) — due ~Apr 16–17 2025 — [[raw/cms_github_svn-apr-15-2025.md]]
- [ ] Dmitri Chudinov — talk to "Паша" and initiate the manifests-product meeting with all interested parties (LGS/Omni/math dependencies) — due ~Apr 2025 — [[raw/cms_github_svn-apr-15-2025.md]]
- [ ] Val — hold the follow-up on the transfer decision + manifests plan, set for Thursday Apr 17 2025, 10:30 — [[raw/cms_github_svn-apr-15-2025.md]]

## Sources

- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/cms_github_svn-apr-15-2025.md]]
