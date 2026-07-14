---
type: decision
title: Structure GitHub organizations to mirror the Jira value streams (2025-01-20)
date: 2025-01-20
aliases: [GitHub org structure, GitHub organizations value streams, GitHub champions]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# Structure GitHub organizations to mirror the Jira value streams (2025-01-20)

**Decision:** JVL's GitHub organizations will mirror its Jira value streams / strategic pillars — Game Development, Core Technology, Distribution, and DevSecOps — with the GitHub Enterprise being JVL itself. Repositories live under organizations (not under "projects"), and teams create and name their own repositories rather than having Andrei create them centrally. Each organization has at least one designated GitHub "champion"/expert. [[raw/github_organization-jan-20-2025.md]]

**Decided by:** Val (with Aaron), coaching Andrei. [[raw/github_organization-jan-20-2025.md]]

## Rationale and terms

- In Bitbucket, the project name is not part of the repo path; in GitHub, the **organization** name is part of the repo path, so orgs (not projects) are the right home for repos. GitHub "Projects" are optional planning/filter views (they could eventually replace or complement Jira). [[raw/github_organization-jan-20-2025.md]]
- Andrei should own the **DevSecOps** organization and be its champion; he should operate GitHub, not be the bottleneck that creates every repo. Letting each team own repo creation (with `.gitignore`, 2FA, license, internal-visibility choices) prevents Andrei from being buried in administrative work — "I save money by not doing admin work; I make money doing productive work." [[raw/github_organization-jan-20-2025.md]]
- Val pushed back hard on Andrei's request for a rigid **rulebook** for repo naming: he wants a *conversation and agreed taxonomy*, not binary rules — "people who need binary rules may not be able to work for us." Recorded and captured knowledge (record the meeting, transcribe, feed to ChatGPT, build the taxonomy) is the method, not top-down rules. [[raw/github_organization-jan-20-2025.md]]
- Naming style: do **not** use all-capitals for repo/org names (called bad practice). [[raw/github_organization-jan-20-2025.md]]

Relates to [[wiki/decisions/2025-01-15-adopt-github-over-bitbucket.md]] and [[wiki/topics/ai-assisted-development.md]].

## Follow-up (Mar 31) — the org-level question reopened

On Mar 31 Val proposed mapping GitHub organizations to Jira **initiatives** instead; the counter-argument (org names are globally unique, orgs are very large entities, initiatives close) pointed back toward value streams and possibly dropping Jira's initiative level. No decision — homework set, follow-up Wednesday 7 a.m. This decision stays **active** until that is resolved. Details on [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]. [[raw/github_jira_alignment-march-31-2025.md]]

## Open questions

- Does the GitHub organization map to the Jira initiative or the value stream (Mar 31 debate, unresolved)? — [[raw/github_jira_alignment-march-31-2025.md]]

## Open commitments

- [ ] Andrei — create the DevSecOps GitHub organization and begin setting it up (repos + projects); read the leadership/modern-software-org material Aaron shared; grow into the DevSecOps (not just engineer) role — due unspecified — [[raw/github_organization-jan-20-2025.md]]

## Sources

- [[raw/github_organization-jan-20-2025.md]]
- [[raw/github_jira_alignment-march-31-2025.md]]
