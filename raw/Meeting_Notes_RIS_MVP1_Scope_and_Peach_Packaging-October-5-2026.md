# Meeting Summary — RIS changes review
**Date:** October 5, 2026, 11:00 AM – 12:07 PM Eastern
**Duration:** ~67 minutes
**Attendees:** Val Levitan, Pavel Frolov, Felipe Miranda Giorgi, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026]]

## Summary

Mostly English, some Russian between Pavel, Irina and Val. Val organized it. Goal: define **MVP1 of RIS (Remote Initial Setup) improvements** — at most three capabilities an operator will value, deliverable in about **two weeks**.

**Scope.** Pavel showed the RIS-improvement capabilities Sebastian wrote (under IP-90 and IP-747 Rage Gaming Platform). Val had the list ranked by priority, with items that cannot fit two weeks moved to the bottom. Pavel said the top items fit: CAP-252 (replace a part without Passport), 255, 246 (looks already implemented — to check), 250 (enable/disable printer during initial setup) and 254. Pavel grouped them into a "RIS improvement MVP1" release in Jira. Pavel said only Evgeny Kharetski is free now; Dima and Serge (server side) are not.

**Lottery lock (not MVP1).** Felipe raised machines that stay out of service after the lottery accounting system locks them. Val said it cannot be MVP1 and he will raise it in a separate meeting. Felipe will share his email thread.

**Non-functional requirements.** None for MVP1. Claude had suggested some; Pavel reviewed them and found them not applicable (one already exists as a functional requirement). Pavel said the last capability may need some investigation first.

**Critical error screen.** Felipe questioned the description: who at JVL gets the QR data, and why scan it. Answer (Val, Pavel): the screen will show the real cause in words (for example a loose Dallas chip, counter board on the wrong port, bad IO board) and the suggested fix, **and** keep the QR code. The QR data goes to a JVL database that is not real-time and not yet well processed; nobody is assigned to read it. In MVP1 the technician gets nothing from scanning. Real-time data for technicians is a later goal. The QR stays because Class 3 sites and many Georgia games will not have a modem. Val said if a description is unclear, the capability description itself must be rewritten; Sebastian (with Pavel) will review them. Felipe agreed the text needs a change.

**Release date and tests.** Val first said October 16; Pavel corrected it — the release date in Jira is **October 19**. Sebastian said the capabilities have acceptance criteria. Pavel said there are no test cases or test executions yet. Val asked who writes the tests and how; the answer is not clear in the transcript. Val said "add four days" to the test time.

**One 18-game pack vs separate Peach packs.** Felipe said putting Peach 1, 2 and 3 (18 games) on one USB stick would solve the problem of masters carrying different sticks, covering about 80% of installed machines. Pavel said one image for any set of games is already supported. Val said the earlier merges (Peach 1+2 into 12 games for Lucky Bucks) were his own undocumented decision ("tribal knowledge"); a placeholder capability was created in Jira to document it as done, but the code still needs to be combined. Felipe then raised a downside: in lottery reports a combined pack shows as one software number, so customers cannot compare Peach 1 vs 2 vs 3. Val pushed Felipe to give his own recommendation, not a question. **Felipe must decide by Sunday Oct 11: one release or three separate USB sticks.**

**Other.** Val confirmed with Irina that the timer, Linux and skill-stop redesign are already in Peach 1. No LTE modem in this release (Irina: adding it means switching to a new version with many changes).

**Next.** MVP2 planning in one week. Pavel needs to talk to server side (Dima, Serge) first.

## Decisions Made

- **RIS improvement MVP1 = CAP-252, 255, 246, 250, 254**, grouped as one Jira release. (Val, agreed by Pavel)
- **Lottery-lock auto-recovery is not in MVP1**; discussed separately. (Val)
- **No non-functional requirements for MVP1** — Claude's suggestions judged not applicable. (Pavel; Val accepted)
- **Critical error screen in MVP1 shows the cause and fix in words, plus the QR code**; QR data goes to JVL's database; technician real-time data is a later MVP. (Val, Pavel)
- **Release date October 19** (as set in Jira). (Pavel corrected; Val accepted)
- **No LTE modem in this release.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Decide and tell Val: one combined 18-game release or three separate Peach USB sticks (weigh lottery reporting) | 2026-10-11 | High | Val: "you take the ownership" |
| 2 | Felipe Miranda Giorgi | Set up RIS improvement MVP2 planning meeting, same time one week from now, all attendees; send invite | 2026-10-12 | Normal | |
| 3 | Felipe Miranda Giorgi | Share the email thread on lottery-locked machines with Val | TBD | Normal | For separate lottery meeting |
| 4 | Sebastian Cortes (with Pavel Frolov) | Review and fix capability descriptions, incl. critical-error QR text (technician gets nothing from scanning in MVP1) | TBD | Normal | |
| 5 | Pavel Frolov | Check whether CAP-246 is already implemented | TBD | Normal | |
| 6 | Pavel Frolov | Talk to server side (Dima, Serge) about MVP2 capabilities before estimating | 2026-10-12 | Normal | Before MVP2 meeting |
| 7 | [Needs Val's confirmation] | Write test cases and test executions for MVP1 acceptance criteria | Before 2026-10-19 | High | None exist yet; owner not clear in transcript |

## Open Questions

- Who at JVL will read the critical-error QR data — not assigned (Felipe).
- How lottery reports will tell Peach 1/2/3 apart if packed together (Felipe) — Felipe to recommend.
- Who writes the MVP1 tests and how (Val) — answer unclear.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-05 12:40 PM ET*
*Source meeting: RIS changes review*
