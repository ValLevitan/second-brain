---
type: decision
title: Adopt GitHub over Bitbucket for JVL's repositories
date: 2025-01-15
aliases: [GitHub over Bitbucket, migrate to GitHub, Bitbucket to GitHub]
source-count: 1
status: active
open-commitments: 1
open-questions: 0
---

# Adopt GitHub over Bitbucket for JVL's repositories (2025-01-15)

**Decision:** Val decided JVL will standardise on GitHub (over Bitbucket) and eventually migrate all repositories from Bitbucket to GitHub. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

**Decided by:** Val ("I'm going to just make it a GitHub"), with the engineers' agreement. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Rationale and terms

- Bitbucket is "falling behind"; GitHub is recommended. GitHub also opens a path to eventually move project tracking off Jira (via GitHub Projects) and to add Copilot. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Cost:** Andrei flagged GitHub as more expensive than Bitbucket; the per-user figures cited in the meeting were inconsistent (GitHub quoted as $10 then $25/user/month, Bitbucket as $15 then $24). Val judged the difference immaterial ("we just spent at least that on this meeting") and used ~$21/user/month for the actual purchase. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Seats to buy:** the prior GitHub trial expired; Val is to purchase ~8 seats (Val, Sasha, the global admin account, [[wiki/people/dmitri-kovalchuk.md|Dima]] (JVL IT, added as GitHub admin — owner-confirmed 2026-07-13), plus Aaron, Anton, Andrei) at ~$21 each — roughly $170/month. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- **Migration is phased, not instant:** repositories not yet in production move quickly; production repos (with hard-coded paths, LFS usage) take longer to rewrite. A past attempt hit a **Git LFS problem** on GitHub, so LFS support must be re-verified — recorded as a required feature. [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
- Jira↔GitHub integration is considered easy (connect the repo in a project's settings). [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

## Open commitments

- [ ] Val — purchase ~8 GitHub seats (~$21/user, ~$170/month) so the team (incl. Sasha) can work on the new pipeline — due unspecified (imminent) — [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]

See [[wiki/decisions/2025-01-15-move-to-git-native-build-system.md]] and [[wiki/topics/build-pipeline-parameterization.md]].

## Sources

- [[raw/parameterization_in_the_development_pipeline_part_4_january_15_2025.md]]
