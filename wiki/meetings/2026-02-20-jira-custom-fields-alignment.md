---
type: meeting
title: IT custom-fields alignment — the round-1 deletion plan (Feb 20 2026)
date: 2026-02-20
aliases: [IT custom fields alignment, JIRA custom fields cleanup Feb 20 2026, Jira custom fields action list, 165 custom fields, Linksee plugin, Jira Product Discovery cleanup, round 1 field deletion]
source-count: 2
---

# IT custom-fields alignment — the round-1 deletion plan (Feb 20 2026)

A screen-shared working call in which [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (IT, driving the JIRA administration screen) walked [[wiki/people/val-levitan.md|Val]] through JVL's custom-field inventory and agreed a first round of deletions (recording header **20 February 2026, 02:33pm**, 36m20s; §11 header time governs). [[raw/IT_custom_fields_alignment-February-20-2026.md]]

One-line purpose: shrink JVL's JIRA custom-field sprawl to a minimal working set so the Claude/MCP integration is simpler and cleaner, deleting only what is provably unused and keeping every deletion reversible.

**§12 — derived-document family (one meeting, two artifacts).** The transcript [[raw/IT_custom_fields_alignment-February-20-2026.md]] and the derived **Jira Custom Fields Cleanup — Action List** [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]] are the same Feb-20 meeting; both are cited here and no separate page is made for the action list (source-count 2).

This continues the custom-field-cleanup thread: it follows the [[wiki/meetings/2026-02-16-val-aaron-jira-acceptance-criteria-migration.md|Feb-16 Aaron acceptance-criteria migration method]], supplies the origin of the **"~70 custom fields removed"** remark in the [[wiki/meetings/2026-02-26-jira-planning-flex-dispenser.md|Feb-26 JIRA-planning call]], and precedes the [[wiki/meetings/2026-02-27-jira-custom-fields-review.md|Feb-27 deletion-matrix review]] that later produced the final 13-field keep list.

Substance → [[wiki/topics/ai-assisted-development.md]] (Feb-20):

- **The inventory.** JVL's JIRA instance holds **165 custom fields**, of which **94 are system-protected** and cannot be deleted; Dmitri's investigation sorted the remainder into a **~55-field round-1 delete list** plus **26 "active" fields** (used at least once in the last 12 months) held back for a case-by-case audit. [[raw/IT_custom_fields_alignment-February-20-2026.md]] [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]]
- **Round-1 deletions (~55).** Cancel the **Linksee ("Linx Fields") plugin** ($40/month; its 5 fields confirmed unused by field owners) and delete its **5 fields**; delete the two **Jira Product Discovery** projects (a trial Atlassian product JVL never adopted), which auto-removes their **~35 duplicated fields**; delete **12 zero-usage fields**; and delete **3 of 16 Jira Service Management fields** (#12/#14/#15, legacy "Assets" references), leaving 13 JSM fields. [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]] [[raw/IT_custom_fields_alignment-February-20-2026.md]]
- **The MCP rationale + the Acceptance-Criteria field.** Because the team now interacts with JIRA through the Claude/MCP integration, Val ruled data should live in standard, widely-visible fields; he directed migrating the **Acceptance Criteria** custom field's content into the standard **Description** field (an `.md`-template format) and then retiring it — the concrete instance of the Feb-16 method. [[raw/IT_custom_fields_alignment-February-20-2026.md]] [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]]
- **Safety net + schedule.** Deleted fields sit in a **60-day recycle bin** with values preserved; Dmitri took a **sandbox snapshot** of the day's state and keeps a backup, and will not rush the deletions (accuracy over speed given the irreversible 60-day cutoff), doing them the following week after preparing a work schedule for Val. [[raw/IT_custom_fields_alignment-February-20-2026.md]] [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]]
- **Val's AI-usage coaching.** Val taught Dmitri to prompt Claude collaboratively — open with uncertainty ("I'm not sure, let's think together what happens if…") rather than a direct command — after Dmitri's day-before experience where Claude moved straight to deleting a field when simply asked what deletion would do. [[raw/IT_custom_fields_alignment-February-20-2026.md]]

§15.8 clear — JIRA field counts, plugin cost, and tooling only; no named-person compensation.

## Sources

- [[raw/IT_custom_fields_alignment-February-20-2026.md]]
- [[raw/Jira_Custom_Fields_Action_List_2026-02-20.md]]
