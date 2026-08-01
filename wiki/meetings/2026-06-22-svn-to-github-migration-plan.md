---
type: meeting
title: SVN to GitHub Migration Plan (June 22 2026)
date: 2026-06-22
source-count: 1
---

# SVN to GitHub Migration Plan (June 22 2026)

**Date:** June 22, 2026, 11:18 AM ET (notes-only, ~27 min)
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]

Val asked whether to move **RAGE Studio** (the old game framework) from **SVN** to **GitHub**. His instinct was to leave it in SVN, but most of the codebase has already migrated, and the team unanimously favored finishing the move. Sequencing set: LGS framework first, games migrate after their next release, a hybrid builder during the transition, math libraries via GitHub Actions, and old-game assets routed to Git LFS.

Substance lives on [[wiki/topics/github-release-management-pipeline.md]] (Jun-22) — the LGS-first plan and timeline (start July 20, target Aug 2), the games-stay-in-SVN-until-after-next-release rule, one-repo-per-game, the hybrid builder, the no-binary-artifacts principle, and the math-libraries and builder open questions.

## Sources

- [[raw/Meeting_Notes_SVN_to_GitHub_Migration_Plan-June-22-2026.md]]
