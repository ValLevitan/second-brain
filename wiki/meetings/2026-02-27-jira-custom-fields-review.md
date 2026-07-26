---
type: meeting
title: JIRA custom-fields cleanup review — the deletion matrix (Feb 27 2026)
date: 2026-02-27
aliases: [Review custom fields JIRA Feb 27 2026, JIRA custom fields cleanup, custom field deletion matrix, 13 fields kept, minimum custom fields]
source-count: 1
---

# JIRA custom-fields cleanup review — the deletion matrix (Feb 27 2026)

A working call reviewing JVL's **JIRA custom fields** to decide which to keep and which to delete (recording header **27 February 2026, 02:05pm**, 26m40s; §11 the header time wins over the `_090556` filename stamp). Attendees: [[wiki/people/val-levitan.md|Val]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (driving, at the screen), [[wiki/people/aaron.md|Aaron Bockelie]] (advising).

This is the actual **"Review custom fields JIRA"** work that the [[wiki/meetings/2026-02-16-val-aaron-jira-acceptance-criteria-migration.md|Feb-16 acceptance-criteria migration clip]] flagged as its "future batch" antecedent, and it continues the **~70-custom-fields-already-removed** thread from the [[wiki/meetings/2026-02-26-jira-planning-flex-dispenser.md|Feb-26 JIRA-planning call]].

One-line purpose: trim JVL's custom-field sprawl down to a minimal working set, driven by intended use rather than technical guesswork, and hand the surviving fields to Aaron's MCP.

Substance → [[wiki/topics/ai-assisted-development.md]] (Feb-27):

- **The method Aaron pushed** — don't "clip wires in an electrical cabinet"; decide by intention and use, working **backward from the three dashboards and their filters** (whatever a filter doesn't reference is a deletion candidate) to build an explicit **"deletion matrix"** of keep-vs-delete, then **verify in the sandbox instance** and against populated issues before deleting, so nothing breaks existing workflows or searches. He framed it inside a longer wind-down — a notional "JVL not on JIRA by 2028" horizon — asking which parts of JIRA are essential to keep. [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
- **Val's decision principle** — "less is more": consume ~20% of the features 80% of the time; a field used in the last six months isn't necessarily used *productively*; the requirement is used but not to its fullest, so focus on using the requirement fully rather than adding unused requirement facets; deleted fields stay recoverable for ~60 days if something can't live without them. [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
- **The mechanics** — [[wiki/people/dmitri-kovalchuk.md|Dmitri]] exported the field list to **Excel**, struck the delete rows red, kept the "requirements categorization label"/"requirement type" and the JIRA-Service-Management reporter fields Aaron flagged as risky, and produced a **final list of 13 custom fields to keep**; he will actually delete the rest **on Monday** after practising on the sandbox. Val asked Aaron's **MCP to address those 13 fields**. [[raw/Review_custom_fields_JIRA-February-27-2026.md]]

§15.8 clear — tooling/process only; no named-person compensation.

## Sources

- [[raw/Review_custom_fields_JIRA-February-27-2026.md]]
