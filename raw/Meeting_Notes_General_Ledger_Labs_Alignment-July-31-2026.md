# Meeting Summary — GL_Systems_Labs
**Date:** July 31, 2026, 10:00 AM Eastern
**Duration:** approximately 55 minutes
**Attendees:** Val Levitan, Igor Donis, Cris Nacarino, Laura Escorcia, Felipe Miranda Giorgi (translator)
**Raw transcript:** [[Meeting_Transcript_General_Ledger_Labs_Alignment-July-31-2026]]

## Summary

Val called this as an alignment meeting on the general ledger, not a question-and-answer session and not a critique. He asked Laura and Cris to attend so they would learn the subject; Igor carries first-hand responsibility for the general ledger.

Background Val laid out. In November 2025 he issued a memo to stop using Navision and move all entries to MSBC (Microsoft Business Central), with no entries into Navision as of January 1, 2026. A second memo created a new MSBC production instance for JVL Labs (the Canadian company) as of January 1, 2026. JVL Systems (the US company) had already been running on MSBC through all of 2025. When the Labs production instance was created, Val's instruction was to use an exact copy of the JVL Systems general ledger accounts.

The problem Val discovered in July 2026. Navision was never frozen; entries kept going into it for JVL Labs. JVL Labs did not assume all the charges out of Navision. And the JVL Labs general ledger is not identical to JVL Systems; it was not a clean copy. When Val asked to move the Navision transactions into JVL Labs in MSBC, he was told the MSBC accounts for JVL Labs are not set up, and Igor proposed a very large number of additional accounts (Val referenced a rate of about 600) to set them up. That alarmed Val.

Val's reasoning against expanding the account list. JVL Systems runs successfully on 437 accounts, of which about 8 are dead and should be deleted and about 100 are badly named, leaving roughly 430 working accounts that already cover sales, purchasing, manufacturing, payroll and multi-state taxes. By Igor's own account he added only four or five accounts over the past 18 months, which Val takes as proof the list is stable. Val also views JVL Labs as shrinking its day-to-day manufacturing and purchasing role, so its account set should be contracting, not expanding.

Val chose not to assign blame for how this happened and said he would not spend time finding a guilty party. He asked the team to do the same and focus on where things stand now.

Val will circulate this transcript and told the team to run it through Claude for a Spanish summary and to send any questions in writing afterward. He said this was a statement and an order, not a discussion, and that he expects aggressive daily action, tasks broken down and closed daily, and written daily reporting.

## Decisions Made

- **Stop using Navision immediately and freeze it at December 31, 2025.** Navision applies only to JVL Labs; JVL Systems has been on MSBC since 2025 and is not affected. (Val)
- **JVL Labs general ledger should mirror JVL Systems, not expand by hundreds of accounts.** The stable ~430-account Systems list is the model. (Val)
- **Target state is monthly, consolidated, automated statements between JVL Labs and JVL Systems**, which depends on one well-groomed, coherent set of general ledger accounts across both companies. (Val)
- **No blame exercise.** The team is to focus on the current state and the fix, not fault. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Donis (with Laura, Cris) | Stop all use of Navision; reverse all transactions out of Navision | Immediate | High | Navision relates only to JVL Labs |
| 2 | Igor Donis (with Laura, Cris) | Preserve Navision as of December 31, 2025 and reconcile it exactly to the accounting firm's statement (the closing balance) | TBD | High | This closing balance seeds the opening balance |
| 3 | Igor Donis (with Laura, Cris) | Create an opening balance in JVL Labs MSBC equal to the Navision December 31, 2025 closing balance | TBD | High | |
| 4 | Igor Donis (with Laura, Cris) | Re-enter all 2026 transactions into MSBC | TBD | High | Rather than expand the Labs account list |
| 5 | Igor, Laura, Cris | Break the work into realistic daily tasks, close them daily, and report progress to Val in writing every day | Daily | High | Val's stated expectation |
| 6 | Laura Escorcia, Cris Nacarino | Study the transcript (Spanish summary via Claude) to absorb the general ledger subject; send any questions to Val in writing | After transcript circulated | Normal | |

## Open Questions

- The exact number of additional accounts Igor proposed for JVL Labs is not settled; Val referenced a rate of about 600 and rejects that scale, but the reconciled account list is still to be produced.

## Dispatch Log

---
*Processed from Teams transcript on July 31, 2026 (back-captured after tenant transcript access was restored).*
*Source meeting: GL_Systems_Labs*
