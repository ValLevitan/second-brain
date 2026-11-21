# Meeting Summary — Jira hygiene cadence
**Date:** November 18, 2026, 6:23 AM – 6:37 AM Eastern
**Duration:** ~14 minutes
**Attendees:** Val Levitan, Dmitri Kovalchuk
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Dmitri_Jira_Grooming_Rules_and_Short_Backlog-November-18-2026]]

## Summary

**Dmitri's starting idea.** Every repository is linked to its own Jira project. Some Jira projects have no repository and never will (portfolio projects). Dmitri wants to start grooming there. Tasks not updated for 6 months: close them, or send one message to the owners first. No answer → close as Rejected or move to To Do. He does not want to delete them; he wants to keep them as a trail.

**Val's rules.** Val said Dmitri is on the right track and added:
- A link between a Jira project and a repository is a good sign the work is real and active. No link → put it in a separate bucket; most of it can go.
- Lena's items that sit outside her main (old-architecture) projects are 99% not needed. Give her a short deadline to attach them to a serious project, or archive. Val grooms her projects with her every week and kills what is not current. She keeps her artifacts on her own computers.
- 6 months is too long. Use 3–4 months: no project link, no repository, nobody touched it for 3 months → archive.
- An initiative with no capabilities under it is not serious → archive. People use these as a to-do list "not to forget".
- "Not to forget" tasks are not allowed in Jira. Val gave an example from 15 minutes earlier: a Dzmitry Chudzinau task due Dec 18; Val asked to move it to Dec 11 because the company closes on Dec 18; it turned out to be a "not to forget" task.
- No long backlog. A real backlog is "not this week, next week" — at most next month.
- Everything must sit under a value stream or be removed. For Val, work in a value stream means money is flowing. He mentioned that the team now says Miranda and the RAGE studio are no longer needed, and asked how much money was burned on them.

**Write it as a standard.** Val asked Dmitri to write these rules as standards in the standards repository, then point Claude at Jira to groom on a schedule. Claude can email a task's owner that the task will be archived soon unless it follows the standard. Val expects a few people to be upset at first; the standard answers them. He reminded Dmitri of the standards contest ($50 prize).

**AI-PM reports.** Dmitri said an agent already sends daily due-date reminders; grooming notices can be added. Val said the AI-PM reports are hard to read. Facts only is right, but the style needs a guide: short simple sentences, plain English for second-language readers. Dmitri said the agent has a character description; he will extend it and ask Andrei if he already started.

**Close.** Dmitri already drafted a list that is almost a standard. Val will send him this transcript.

## Decisions Made

- **Jira grooming rules (Val's direction for the standard):** no project/repository link and untouched 3 months → archive; initiative with no capabilities → archive; "not to forget" tasks not allowed; no backlog longer than about a month; everything under a value stream or removed. — To clean Jira and stop spending on work outside value streams. (Decided by Val; Dmitri agreed)
- **Rules go into the standards repository and Claude does the grooming.** — So nobody grooms by hand. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Write the Jira grooming rules as a standard in the standards repository | TBD | High | He already has a draft list |
| 2 | Dmitri Kovalchuk | Extend the AI-PM character/style guide so reports use short, plain sentences; ask Andrei if he already works on it | TBD | Normal | Val finds AI-PM reports hard to read |
| 3 | Val Levitan | Send this transcript to Dmitri | Nov 18, 2026 | Normal | Input for the standard |

## Open Questions

- Deadline for Lena to attach her loose items — the transcript is garbled ("15:00"); exact time frame unclear.
- Notice period before a task is archived — garbled in the transcript ("14:00"); not settled.

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026*
*Source meeting: Jira hygiene cadence*
