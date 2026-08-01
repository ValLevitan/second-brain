---
type: meeting
title: JIRA Hierarchy — services, versions and where bugs live (June 11 2026)
date: 2026-06-11
aliases: [JIRA Hierarchy Services Versions and Bugs, Transaction Galaxy hierarchy, services versions bugs, where bugs live, virtual Aaron bug question]
source-count: 1
---

# JIRA Hierarchy — services, versions and where bugs live (June 11 2026)

**June 11, 2026, 7:31 AM ET · ~1h 7m.** Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/irina-shishko.md|Irina Shishko]]. Russian; speech-to-text rough and proper nouns garbled — worth a wording sanity check.

The Thursday working session set up on [[wiki/meetings/2026-06-08-jira-hierarchy-capabilities-and-sandbox-sync.md|June 8]], continuing the JIRA-hierarchy thread (June 1 planning → June 2 sandbox → June 5 IQ deployment → June 8 capabilities). The group worked out how to structure the hierarchy for **Transaction Galaxy**, and three questions dominated: whether to keep "services" in the hierarchy, how to handle product versions on the timeline, and where bugs belong. The main unresolved item — how to treat a production bug that traces to a requirement that was never written — was deferred to a "virtual Aaron" consult and a follow-up session on Monday, June 15.

Durable substance — drop the broken-out services (they are architecture, not business-facing hierarchy); no standalone authorization service; products = Flex IQ and Flex Recycler with version/timeline groupings; bugs spawn a new feature under the capability and the fix attaches to the already-shipped field version, not the in-progress one — lives on [[wiki/topics/github-release-management-pipeline.md]] (Jun-11, continuing the Jun-1/Jun-2/Jun-8 JIRA-hierarchy thread).

## Sources
- [[raw/Meeting_Notes_JIRA_Hierarchy_Services_Versions_and_Bugs-June-11-2026.md]]
