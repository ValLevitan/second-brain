---
type: meeting
title: Schedule review — FlexPort-application handover + the Jira↔GitHub single-source-of-truth push (Mar 4 2026)
date: 2026-03-04
aliases: [Schedule review Mar 4 2026, schedule review March 4, IP 10-13 FlexPort application handover, Yavorski to Biratka handover, single source of truth Jira GitHub, feature branch discipline, sprints vs kanban Mar 4, FP 519 FlexPos software update, IP 902 FlexPos]
source-count: 1
---

# Schedule review — FlexPort-application handover + the Jira↔GitHub single-source-of-truth push (Mar 4 2026)

A ~1h56m JIRA schedule/release review (recording header **4 March 2026, 12:21pm**, 1h56m4s; §11 the header time wins over the `_072118` filename stamp) with [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — a Russian-language planning call walking the Minsk board (IP applications, features, sprints). Continues the Jira-workflow thread from the [[wiki/meetings/2026-02-27-nebraska-release-schedule.md|Feb-27 release-schedule call]] and the [[wiki/meetings/2026-02-20-jira-custom-fields-alignment.md|Feb-20 custom-fields alignment]].

**§4 resolution — "Irina."** The QA/testing Irina here (asks the purpose of the GitHub-branch field, how it links to a feature) is [[wiki/people/irina-shishko.md|Irina Shishko]] (Director of QA), not game-developer Irina Makarych, per the owner ruling 2026-07-18. The "Ирина макарович"/"исход" mention *inside* the call refers separately to [[wiki/people/irina-makarych.md|Iryna Makarych]] as an example of someone leaving — recorded as a role/status fact on the topic page.

One-line purpose: begin transferring [[wiki/people/eugine-yavorski.md|Yavorski]]'s FlexPort application (IP 10-13) to [[wiki/people/alexander-biratka.md|Sasha Biratka]], and push Minsk toward a single Jira↔GitHub source of truth with feature-branch discipline.

Substance is recorded where it belongs:

- **The IP 10-13 FlexPort-application handover** — the decision **not** to take Yavorski on permanently (his contract project ends ~March 24), moving the ownership/reporter role to [[wiki/people/alexander-biratka.md|Sasha Biratka]] (Val's/Pavel's pick over [[wiki/people/dmitri-chudinov.md|Dima Chudinov]], who is stretched across Flex-Q terminal + server-side work), and Val's "grow-the-performers / cut the stagnant" management rationale → [[wiki/people/eugine-yavorski.md]] (Mar-4) and [[wiki/people/alexander-biratka.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]
- **The single-source-of-truth workflow push** — the Jira-vs-GitHub "two sources of truth" problem, Val's "there is only one truth (the product/code); everything else is decoration on a Christmas tree" principle, the feature-branch discipline (a GitHub-branch field on every feature, populated when it flips to In Progress), the sprints→kanban board-reconfiguration question, the requirements-before-discussion "hygiene" argument, and the plan to run Claude to flag In-Progress features lacking a branch → [[wiki/topics/github-release-management-pipeline.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]
- **Marching orders** — Pavel to talk to [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]] about configuring the feature→GitHub-branch link (and the sprint→kanban board switch), and Val to run Claude against the transcript to enact the reporter change on IP 10-13 → noted on [[wiki/people/pavel.md]] (Mar-4). [[raw/Schedule_review-March-4-2026.md]]

**Unresolved mentions (queued, described inline, not force-matched).** The server-side "MP" tool that reads Jira custom fields (now trimmed to **14 fields**) that "Иран"/"ера" (garble; the Jira-tooling engineer cluster already queued Tier-B) promised to fix by end of week so it can be pointed at each task to flag missing data — kept as a garble, no page. "Андрейкин," which Val uses repeatedly, is a placeholder for an action-item to be captured in the transcript for Claude to action — **not** a person.

§15.8 — Val discussed raising the pay of team members who grow and cutting those who don't, but named **no salary/rate/bonus figures**; the specific compensation discussion is omitted per §15.8. Only role/status facts (Yavorski not made permanent; Makarych on the way out; Kharetski growing into more work) are recorded on the routed pages.

## Sources

- [[raw/Schedule_review-March-4-2026.md]]
