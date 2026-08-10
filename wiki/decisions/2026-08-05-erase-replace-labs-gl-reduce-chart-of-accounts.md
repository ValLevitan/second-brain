---
type: decision
title: Erase & replace JVL Labs GL; reduce the chart of accounts (146 Systems / 96 Labs); freeze Systems history (leaning)
date: 2026-08-05
aliases: [erase and replace Labs GL, reduce chart of accounts, 146 Systems 96 Labs, freeze JVL Systems history]
source-count: 2
status: active
---

# Erase & replace JVL Labs GL; reduce the chart of accounts (146 Systems / 96 Labs); freeze Systems history (leaning)

On the [[wiki/meetings/2026-08-05-chart-of-accounts-alignment-systems-labs.md|Aug 5 2026 chart-of-accounts alignment]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/felipe-miranda.md|Felipe]] translating, [[wiki/people/cris-nacarino.md|Cris Nacarino]], [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/laura.md|Laura Escorcia]]) the AI CFO delivered a definitive proposed general-ledger chart of accounts as an Excel (column J reserved for the team's comments). [[raw/Meeting_Notes_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]

## What was decided (Val)

- **JVL Labs GL accounts will be erased and replaced with the new structure** — Labs has no entries yet, so there is no history to preserve; this is why Val is pushing the change now. [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]] [[raw/Meeting_Notes_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]
- **The proposal reduces the chart to 146 posting accounts for JVL Systems and 96 posting accounts for JVL Labs**, down from roughly **800 accounts** in the current system. [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]
- **Process rule: a proposed change is accepted only if all three of Cris, Igor and Laura back it and explain why it matters** — one person arguing alone is not enough. From this meeting forward all remarks go in **column J** of the proposal Excel (no line-by-line comments were required at this meeting; the team had waited to confirm the objective). [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]] [[raw/Meeting_Notes_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]
- **Direction (leaning, NOT locked): freeze JVL Systems history as statements + trial balance / opening balances (frozen, not deleted, always revertable) and start the going-forward ledger clean**, rather than carry the current heavily "contaminated" accounts forward. Val deferred final judgment to the AI CFO and, if needed, external chartered accountant [[wiki/people/sean-riley.md|Sean (Riley)]]; he acknowledged he is not an expert accountant and welcomed being overruled. [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]

## The accounting-approach tension (recorded, not resolved)

[[wiki/people/igor-donis.md|Igor]] and [[wiki/people/laura.md|Laura]] argued the non-posting accounts should be **retained as titles/subtitles/totals** so historical financial statements and backward analysis can still be produced, and that building a company from scratch and re-linking everything (posting groups, dimensions, bank/module links) the way it was originally configured — which took "Daniel" 8–10 months — would be a huge project; they prefer freezing and renaming existing accounts because "every dollar has a history." Val's counter: what took Daniel ~8 months can now be done in about **an hour** with AI. [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]

("Daniel" here is the person who originally built the ~800-account Navision/BC structure — distinct from [[wiki/people/daniel-eds.md|Daniel, the EDS family principal]]; kept as a plain-prose mention pending identity confirmation.)

## Undertaking

Val committed to experiment immediately after the meeting — prompting AI to roll the ~800 Systems accounts down to 147/148 and produce a many-to-one tracer table (800 on the left, 148 on the right) as a single Excel, using his MCP connection to MSBC — as proof the roll-down preserves history without an 8-month rebuild. [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]

Sits within the GL-grooming thread on [[wiki/topics/business-central-erp-implementation.md]].

## Sources
- [[raw/Meeting_Notes_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]
- [[raw/Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026.md]]
