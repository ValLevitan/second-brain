# Meeting Summary — Daily Standup meeting
**Date:** November 16, 2026, 6:14 AM – 6:28 AM Eastern
**Duration:** ~14 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Morning_Standups_and_SMS_Fix_Release-November-16-2026]]

## Summary

**Standups move to the morning.** Anton Leshkevich is on a kind of leave: he keeps working but will not join the later meetings. Pavel said daily standups move to the morning, at least this week. Irina said this should have started today; Pavel forgot and will do it from tomorrow.

**SMS fix for Georgia.** Irina asked for a release so the problem found on Saturday (demo installs) can be checked in Georgia. It was first thought to be RIS (Dzmitry); Sergey said it is the SMS service. Sergey releases it today. Ivan checked on Saturday: not all cases, but the negative case worked.

**Status by person:**
- **Alexander:** took capability 372 (port with new screens). Also building features from the recycler capabilities Andrei wrote.
- **Alexey:** hardware autotests; now looking at tasks Val sent. Asked where the list of locations and products is; Irina: in Confluence.
- **Anton Seregin:** closed TINT-129; 125 and 130 in progress; plans to run on a real port next.
- **Daniil:** NewGin-26 PRs open, working with LGS 1340; NewGin-54 next.
- **Dzmitry:** NAD almost done. Wanted to pass paytables automatically but found conflicts in the files; waiting for Igor's fix. Modem work will be released today. With Andrei, reworking the build into full CI/CD for everyone.
- **Evgeny:** built the ISO file; will install it on a machine with LTE. LTE switch-off is done.
- **Irina:** autotests; sorted which capabilities and features go in which release. Pavel pointed out 3 standard tasks and the agent task on her (94, 95, 96).
- **Ivan:** checking the UI part of Evgeny's modem work; the server side is still with Dzmitry. Still has RIS questions. Will move the GT task date.
- **Sergey:** lottery tickets and fixing stories (redemption split).
- **Vladimir:** working on FIG-206 and FIZ-127 (test IDs); firmware service contracts about half done, 2–3 left. Irina asked when he starts autotests; she will set the ones Sergey already finished first for him.
- **Igor:** ported a game from GCMA 2; made a game-select screen for the vertical NAD he built; small fix for Evgeny; prepared files for Dzmitry. Still needs a small GLI fix for Dakota (from Ivan).
- **Dmitri K:** one draft for Alexander was missed. Pavel: Alexander checks if the bill recycler can pay out in a bundle or only one note at a time; moved to To Do. The agent can now move tasks; people should try it.

## Decisions Made

- **Daily standups move to the morning, at least this week.** Reason: Anton Leshkevich will not join later meetings. (Pavel)
- **Sergey, not Dzmitry, releases the SMS fix to prod.** It is an SMS issue, not RIS. (Dzmitry, Irina, Sergey)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Move the daily standup to the morning | Nov 17, 2026 | Normal | |
| 2 | Sergey Tsimanov | Release the SMS fix to prod for the Georgia demo-install problem | Nov 16, 2026 | High | Found Saturday |
| 3 | Dzmitry Chudzinau | Release the modem work | Nov 16, 2026 | Normal | |
| 4 | Igor Metelski | Fix the conflicts in the paytable files for Dzmitry | TBD | Normal | Igor promised |
| 5 | Evgeny Kharetski | Install the new ISO on a machine with LTE | TBD | Normal | |
| 6 | Irina Shishko | Set the finished autotest items first for Vladimir | Nov 16, 2026 | Normal | |
| 7 | Vladimir Samusenko | Start autotests after the firmware service contracts | TBD | Normal | |
| 8 | Ivan Shpak | Move the GT task due date | Nov 16, 2026 | Low | |
| 9 | Alexander Biratko | Check if the bill recycler pays out in a bundle or one by one | TBD | Normal | Moved to To Do |
| 10 | Igor Metelski | Make the small GLI fix for Dakota | TBD | Normal | Ivan's earlier request |
| 11 | Irina Shishko | Work the 3 standard tasks and the agent task (94, 95, 96) | TBD | Normal | Pavel pointed them out |

## Open Questions

None.

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
