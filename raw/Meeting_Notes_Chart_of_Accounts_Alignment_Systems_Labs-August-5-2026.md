# Meeting Summary — Chart of accounts alignment: JVL Systems and JVL Labs (before written markup)
**Date:** August 5, 2026, 11:00 AM–12:03 PM Eastern
**Duration:** ~63 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi (translating English↔Spanish), Cris Nacarino, Igor Donis, Laura Escorcia (AI CFO invited, did not speak)
**Raw transcript:** [[Meeting_Transcript_Chart_of_Accounts_Alignment_Systems_Labs-August-5-2026]]

## Summary

The AI CFO produced a definitive proposed general-ledger chart of accounts for JVL Systems and JVL Labs, delivered as an Excel with column J reserved for the team's comments. Val opened by setting ground rules: the meeting is not for justifying the past or assigning blame; the only valid comments are why a proposed account should be dropped or why a missing account should be added. He added that a change will only be accepted if all three of Cris, Igor and Laura back it and explain why it matters — one person arguing alone is not enough. Going forward, all remarks belong in column J of the Excel.

The team met the day before (Aug 4) to review the proposal but did not write comments in column J — they waited for this meeting to confirm its objective. Val confirmed that was correct: no line-by-line remarks were expected at this meeting, but from now on remarks go in the Excel.

The proposal reduces the chart to **146 posting accounts for JVL Systems and 96 posting accounts for JVL Labs**, down from roughly **800 accounts** in the current system.

Igor argued the non-posting accounts should be retained as titles / subtitles / totals so historical financial statements and backward analysis can still be produced, and raised concern about renaming vs. recreating account codes, preserving each account's history, and the complexity of re-linking (posting groups, dimensions, bank/module links). Laura reinforced this: building a company from scratch with ~148 accounts and re-linking everything the way it was originally configured (which took "Daniel" 8–10 months) would be a huge project; she prefers freezing and renaming existing accounts to preserve traceability, since "every dollar has a history."

Val disagreed on the accounting approach but deferred final judgment to the AI CFO (and, if needed, external auditor Sean). His concern is that the current system is heavily "contaminated," and he does not want to drag that contamination into the new structure. He leans toward freezing JVL Systems history as statements plus a trial balance / opening balances (frozen, not deleted, always revertable) and starting the going-forward ledger clean. He acknowledged he is not an expert accountant and welcomed being overruled if the approach is unsound.

On feasibility, Val's key point: what took Daniel ~8 months can now be done in about an hour with AI. He committed to experimenting immediately after the meeting — prompting AI to roll the ~800 accounts down to 147/148 and produce a many-to-one tracer table presented as a single Excel (800 on the left, 148 on the right), using his MCP connection to MSBC. JVL Labs is unaffected because it has no entries yet — its GL accounts can simply be erased and replaced with the new structure, which is why Val is pushing this now.

## Decisions Made

- **No line-by-line Excel comments were required for this meeting; from this meeting forward all remarks go in column J of the proposal Excel.** — Team had waited to confirm the objective; Val confirmed the process. (Decided by Val Levitan)
- **A proposed change is accepted only if all three (Cris, Igor, Laura) support it and justify it.** — Prevents single-person changes; gives the AI CFO a clear signal. (Decided by Val Levitan)
- **JVL Labs GL accounts will be erased and replaced with the new structure.** — Labs has no entries, so there is no history to preserve. (Decided by Val Levitan)
- **Direction (leaning, not final): freeze JVL Systems history as statements + trial balance/opening balances and start the going-forward ledger clean, rather than carry the current accounts forward.** — To avoid dragging system "contamination" into the new structure; to be validated by the AI CFO and, if needed, Sean. (Val Levitan — explicitly not locked)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Experiment with AI to roll the ~800 JVL Systems GL accounts down to 147/148 and build a many-to-one tracer table, presented as one Excel (800 → 148) via the MSBC MCP | Aug 5 (right after meeting) | High | Proof that the roll-down preserves history without an 8-month rebuild |
| 2 | Val | Consult Lev Rudky (or AI) on how to revise the currently usable JVL Systems GL / GL group into the new structure | TBD | Normal | Open technical question on migrating an in-use ledger |
| 3 | Cris | Show progress on the EDS reconciliation received from Sandra Carmona | TBD | Normal | Val wants visible movement on it |
| 4 | Laura | Credit out the fake sales and move the machines to trial warehouses so sales show clean | TBD | High | Clean-sales integrity |
| 5 | Cris, Igor, Laura | Keep working their Microsoft Planner cards — close out tasks that can be closed even if not yet due | Ongoing | Normal | Val asked them to move forward rather than wait |
| 6 | Cris, Igor, Laura | Put all future remarks on the proposed accounts in column J of the Excel | Ongoing | Normal | Process rule for the next markup round |

## Open Questions

- How to revise the existing, in-use JVL Systems GL group into the new GL without breaking usability — Val to consult Lev Rudky.
- Whether freezing history is the correct accounting choice vs. keeping title/total accounts for backward reporting — Val to let the AI CFO judge, may consult Sean (external auditor). (Raised by Igor / Laura)
- Whether to stand up a "JVL 2.0" company from scratch (possibly starting 2027) or produce a rolled-down version of the existing company — raised by Cris, unresolved.

## Dispatch Log

---
*Processed from Teams transcript on August 5, 2026 (scheduled meeting-watcher run)*
*Source meeting: Chart of accounts alignment: JVL Systems and JVL Labs (before written markup)*