---
type: decision
title: GitHub repositories private by default; access granted per repository
date: 2025-02-12
aliases: [private by default, repo access control, least privilege GitHub, internal vs private repos]
source-count: 1
status: active
---

# GitHub repositories private by default; access granted per repository

**Decision (Feb 12 2025, Val + [[wiki/people/aaron.md|Aaron]] + [[wiki/people/andrey-bosik.md|Andrei]] ("Andrei Bosik") + [[wiki/people/pavel.md|Pavel]] + [[wiki/people/alexander-biratka.md|Alexander]]):** On the GitHub check-in meeting the group settled how repository access will work across JVL's GitHub enterprise. [[raw/Check_in_on_GitHub_2025-02-12.md]] Builds on [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]].

## What was decided

- **All repositories are created private by default.** Andrei's concern: a GitHub **internal** repository is visible to every member of the enterprise regardless of which organization they belong to; only **private** repositories are restricted. To keep one organization's repos from being seen by members of another, the default must be private. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- Andrei confirmed by demonstration (logged in as a normal user, Alexander's account) that an **internal** repo in an org the user is not a member of is still visible and cloneable; a ChatGPT/GitHub-manual check confirmed enterprise membership alone does **not** automatically grant cross-organization repo access when repos are private. Aaron: making a repo private "resolves 90% of our things." [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **New users get no repository access by default**; rights are granted per repository (least-privilege / "no blank check"). Val: adding a user to an organization should give **read** access at most, managed by the organization manager, and **no write rights for roughly the first three months** (a new hire has nothing useful to commit yet). [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **Documentation lives above the repos:** a company-wide, higher-level repository/front page describing JVL and its products, with links into repos a user can't yet access — so people can discover what exists and **request access** when they genuinely need it. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- **Homework:** Andrei to start the GitHub org setup over from scratch following the out-of-the-box private-by-default configuration, and remove the generic "IT" administrator identity (see the topic page). A follow-up check-in was set for the next morning. [[raw/Check_in_on_GitHub_2025-02-12.md]]

The supporting access model — Codespaces, the audit log, activity-based access revocation, and the Entra-ID/SSO admin-account problem — is captured on [[wiki/topics/github-access-and-security-model.md]].

## Sources

- [[raw/Check_in_on_GitHub_2025-02-12.md]]
