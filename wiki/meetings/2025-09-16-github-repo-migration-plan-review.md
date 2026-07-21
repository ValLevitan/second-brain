---
type: meeting
title: GitHub repo migration plan review (Sept 16 2025)
date: 2025-09-16
aliases: [git repo structure Sept 16, migration plan review, one story per repo, secrets migration]
source-count: 1
---

# GitHub repo migration plan review (Sept 16 2025)

**Sept 16 2025, 12:03pm.** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/pavel.md|Pavel Frolov]].

Review of [[wiki/people/andrey-bosik.md|Andrei]]'s written change plan (placed in Confluence, RU + EN; Aaron noted it belongs in git). Worked out **how to track the migration**: model GitHub as a product/capability, the two target organizations as features, and **one Jira/GitHub story per repository** (Aaron: write stories for the end structure, each repo atomically movable) — consolidating ~11 organizations down to **2**. Covered secrets/variables/self-hosted-runner migration (recreate same-named secrets in the target org; a "GitHub Organization Secrets migrator" tool — never route secrets through an LLM/MCP, only names), and the change-management discipline (per-repo analysis, ordering, notifying repo owners). [[wiki/people/val-levitan.md|Val]] pressed for a firm schedule after only one of the prior undertakings was complete; set a Friday check-in against a ~2-week plan. Session 4 (final) of the Sept 9→16 arc — substance and dated sequence live on [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## Sources

- [[raw/git_repo_structure.md]]
