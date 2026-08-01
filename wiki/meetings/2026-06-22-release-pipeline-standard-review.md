---
type: meeting
title: Release Pipeline Standard Review (June 22 2026)
date: 2026-06-22
source-count: 1
---

# Release Pipeline Standard Review (June 22 2026)

**Date:** June 22, 2026, 10:01 AM ET (notes-only, ~1 h 16 min)
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]

Andrei walked the team through his **5-stage release-pipeline standard** — the path from commit to production deployment — the release/CI-CD companion to the JIRA-hierarchy standard locked on June 16. Feature branch → PR-to-main checks → pre-release/integration testing → release (version matrix) → deployment (integration-repo only).

Substance lives on [[wiki/topics/github-release-management-pipeline.md]] (Jun-22) — the five stages, the decisions (production deploys only from the integration repo; unit tests at PR stage not branch push; the version matrix stored as one file per release; all standards consolidated into the "knowledge" repository; ADR standard published as v0.5 and Dima's Jira standard at ~v2), and the unresolved cross-service integration-testing, Jira↔GitHub version-linking, and 3-vs-4-segment versioning questions.

## Sources

- [[raw/Meeting_Notes_Release_Pipeline_Standard_Review-June-22-2026.md]]
