---
type: meeting
title: GitHub repo-naming convention and validation tool (Sept 9 2025)
date: 2025-09-09
aliases: [git structure review Sept 9, repo naming kebab taxonomy, repo name validation tool]
source-count: 1
---

# GitHub repo-naming convention and validation tool (Sept 9 2025)

**Sept 9 2025, 1:23pm.** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/andrey-bosik.md|Andrei Bosik]].

Working session on the **repository-naming convention** — a strict kebab taxonomy (category / subcategory / component / variant), the rule that separators within a term use underscores while dashes join taxonomy levels, and the abbreviation policy (spell out JVL-specific ones like LGS; keep well-known API/GUI/OS). Aaron began turning the naming spreadsheet into a JSON-backed **validation tool** loaded into GitHub to flag wrong repo names, potentially wired to Jira support-requests and webhooks for auto-creation. [[wiki/people/andrey-bosik.md|Andrei]] floated a separate "Knowledge" organization; Aaron pushed back toward one org. This is session 1 of the Sept 9→16 git-repo-structure arc — substance and dated sequence live on [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## Sources

- [[raw/review_git_structure-september-9-2025.md]]
