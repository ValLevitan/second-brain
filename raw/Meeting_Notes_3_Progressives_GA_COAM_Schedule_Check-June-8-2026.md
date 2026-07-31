# Meeting Summary — 3-Progressives GA-COAM Release Schedule Check
**Date:** June 8, 2026, 3:02 PM Eastern
**Duration:** ~14 minutes
**Attendees:** Val Levitan, Pavel Frolov, Igor Metelski, Lena Zhukova, Anton Liashkevich, Irina Shishko, Evgeny Kharetski

## Summary

Weekly schedule check on the 3-Progressives release for the Georgia COAM market. The team walked the Jira board to see what is on track against the June 16 target.

**Match 3 bonus (Igor).** The main flow is done — it enters the bonus, plays it, reports progressive wins, and shows the wins. Igor is now wiring in the animations for the designers (background, table, coin, and the final-draw animation) plus the sounds Vlad sent. He expects to finish today or tomorrow morning. A build the designers and Vlad can review for animations and sounds should be ready tomorrow.

**Progressive Jackpot bonus transition (Anton).** The task had the wrong assignee; it belongs to Anton and will be reassigned. Anton didn't get to it Friday. He'll insert the transitions today, but first he has to finish the Fill_G branch.

**Transition crash (Anton + Lena).** The Queen game crashes on the transition even though it was tested before and nothing was meant to change. Anton thinks the cause is small changes he made to how the bonus is selected, just before he updated the math; those likely need to be rolled back. He'll fix and re-verify — about 15–20 minutes. He also fixed crashes in the Fairies bonus on Friday.

**QA and bugs (Irina).** Irina asked Anton to go through all the logged bugs; some may need artist input. She updated the test schedule against the test plans. She currently sees 22 tasks in testing and 1 in development, with 3 more moving into development today or tomorrow, plus a number of bugs. The Match 3 test plan (task 1200) is set for 16:00. Match 3 testing sits with Ivan Shpak (Vanya).

**Board hygiene.** Val flagged tasks that, by schedule, should already be done. A few to-do items (1295/1296/1297) were due Friday and slipped to Monday because Anton couldn't start them; they can be moved given dependencies. Val and Irina reconciled several statuses live (in-progress vs to-do; one item Irina had set to "blocked" but hadn't saved).

Val noted that, on schedule, not everything is in the team's hands and June 16 readiness is a hope, not a certainty. Next check is Wednesday at the same time. Val asked Irina to stay on for a one-on-one.

## Decisions Made

- **Reassign the Progressive Jackpot bonus transition task to Anton** — it had the wrong assignee. (Pavel, Anton)
- **Anton finishes Fill_G first, then the transition integration** — sequencing his work for today. (Pavel, Anton)
- **Move the slipped Friday to-do tasks to Monday** — they have dependencies and it's now Monday. (Val, Pavel)
- **Next schedule check: Wednesday, same time.** (Val, Pavel, Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Finish Match 3 bonus (animations + Vlad's sounds) and produce a build the designers and Vlad can review | June 9 (tomorrow AM) | High | Release-gating; designers and Vlad are waiting |
| 2 | Anton Liashkevich | Finish Fill_G, then fix the Queen transition crash by rolling back the pre-math bonus-selection changes, and re-verify | June 8 (today) | High | Crash blocks the transition work; ~15–20 min |
| 3 | Anton Liashkevich | Insert the transitions for the Progressive Jackpot bonus (reassigned task) | June 8 (today) | High | Was due Friday, slipped |
| 4 | Anton Liashkevich | Go through all logged bugs; flag any needing artist input | TBD | Normal | Irina's request; some partially fixed |
| 5 | Pavel Frolov | Reassign the Progressive Jackpot transition task to Anton; reschedule the slipped to-do items (1295/1296) | June 8 (today) | Normal | Board hygiene |
| 6 | Irina Shishko | Run the Match 3 test plan (task 1200) and keep board statuses current against the test plans | June 8, 16:00 | High | QA gate; target readiness June 16 |
| 7 | Val Levitan | One-on-one with Irina after this call | June 8 | Normal | Val asked her to stay on |

## Open Questions

- Why does the Queen game crash on the transition when it was already tested and unchanged? Anton's theory is the pre-math bonus-selection changes — to be confirmed once rolled back.
- Will June 16 hold? Val flagged that not everything is in the team's control.

---
*Processed from Teams transcript on June 9, 2026*
*Source meeting: 3-Progressives release GA-COAM schedule check*
