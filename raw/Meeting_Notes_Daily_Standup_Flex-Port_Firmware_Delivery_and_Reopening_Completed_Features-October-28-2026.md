# Meeting Summary — Daily Standup meeting
**Date:** October 28, 2026, 4:50 AM – 5:28 AM Eastern
**Duration:** ~37 minutes (standup itself ~23 minutes; it was moved to 12:00 Minsk and started at 00:14 into the recording)
**Attendees:** Pavel Frolov, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear names, numbers and words are marked "heard". Alexander Biratko was absent; Dima (heard as the person due back tomorrow) is also out today.

**Flex-Port firmware delivery.** Sergey handed the update work for production to Andrei; CI still needs an update on his side. Internal test: IQ firmware arrives and its signature is verified (dev). He is researching how to pass firmware on to the Flex-Port. The USB update path on the port already exists. Pavel: Sergey does the protocol change for firmware transfer to the Flex-Port; on the port side, put the firmware on flash, check the checksum, and if it matches switch boot from sector 1 to sector 2. Sergey said this mechanism is already there. Sergey worried that some people may see this as their area; Pavel: customers being satisfied matters more. Sergey will build and test it, and agree with Dima tomorrow.

**Completed feature gets a new story.** Dmitri asked what to do when a developer marks a feature complete and later a new story (like a bug) is created under it. Options he raised: reopen the feature automatically, link the story sideways instead of as a child, or add a new status such as "needs rework". Pavel: no extra status; do not reopen automatically. The person who creates the story should move the feature back to To Do / In Progress, or pick a different parent, because people and AI sometimes choose the wrong parent. A notice can go to the story's creator that the parent is closed.

**Jira projects.** Dmitri asked whether tasks may still be created in the Core Technology and BEP (heard) projects. Pavel: those are for tasks with no repository; since things have moved, try to move work to the new projects. Pavel's own draft task will be closed as a duplicate, since the work was done in another task.

**Video format for games.** Anton Leshkevich finished porting Sparkle Seven (heard) and fixed the requirements as agreed yesterday. Designers agreed the current formats from Miranda are fine for now. Pavel: VP9 is the right video format because ARM boards decode it in hardware; current game video is VP8, which is not supported. Igor will rebuild with the new Sparkle math.

**Bill validator mode tests.** Irina continues autotests for BV mode. Pavel asked to go through the list Andrei sent last evening and decide what to fix. Irina: the work stalled because Alexander did not finish yesterday's port work; she had told Andrei to report findings at once and to add MVP needs to the requirements right away. Pavel agreed findings should come at once, while the team is still on site.

**Multi cash-out on SAS.** Alexey asked if the multi cash-out change affects BV mode on SAS. Pavel: two cash-outs inside the timeout can happen; in SAS they should add up to one ticket, but he suspects it may not work now. Irina will check.

**Other updates.**
- Alexey: hardware tests continue. Unclear who sets up the cloud terminal hub / manager so services can be pulled from repositories; Irina: wait for Dima tomorrow, together with Andrei. Yavorsky (heard "Egorsky") again commented on HFM-692 (heard) after Andrei updated requirements; this touches MVP-1. Pavel: ask Dima to remove him from the reviewers of this project; Alexey already wrote to Andrei.
- Anton Seregin: drafts done for "cap bill" (heard), Flex, Flex Pay and Flex-Port. Next the features table is split by repository, then moved to Jira. Pavel: when ready, review with Irina and Sergey. He will close the old emulator / kiosk rename task, done long ago.
- Daniil: finished NC6 (heard), now NFL1 (heard). Asked about IP-1113 (heard), a board report; Pavel asked him to re-read it.
- Ivan: still on RIS. Pavel has not finished the installer that keeps old RIS data after reinstall or a software change; copying was slow. Ivan: the 224 server downloads in ~10 minutes; take the latest build 4353 (heard).
- Evgeny: no change — agents, RIS problems (heard).
- Igor: integrating new resources, fixed designer requests, working on crane design (heard).
- Vladimir: port fixes done; modem defects retested, green. No fresh backlog. Two IQ text tasks wait on a text library that does not exist yet (one really belongs to Kaimov, heard); old tasks 1–2 years old (LGS dispenser) need review.
- Alexander absent and did not finish yesterday's port work; Pavel will call him.

## Decisions Made

- **Sergey does the firmware transfer protocol change for the Flex-Port** — port side is simple: flash, checksum, switch boot sector. (Decided by Pavel)
- **No automatic reopening and no new status when a story is added under a completed feature** — the story creator moves the feature back or changes the parent, since parents are sometimes set wrong. (Decided by Pavel; Dmitri agreed)
- **Game video should be VP9, not VP8** — ARM boards decode VP9 in hardware. (Pavel)
- **Pavel's draft task is closed as a duplicate** — work done in another task. (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Call Alexander about the unfinished port work | Oct 28, 2026 | High | Blocks Irina's BV tests |
| 2 | Sergey Tsimanov | Build and test firmware transfer to the Flex-Port; agree with Dima | Oct 29, 2026 | High | Dima back tomorrow |
| 3 | Irina Shishko | Go through Andrei's list from last evening; decide what to fix; add MVP needs to requirements | Oct 28, 2026 | High | |
| 4 | Irina Shishko | Check multi cash-out in BV mode on SAS | Oct 28, 2026 | Normal | Alexey's question |
| 5 | Alexey Khamin, Irina Shishko | Settle cloud terminal hub setup with Dima and Andrei | Oct 29, 2026 | Low | "Not urgent" |
| 6 | Pavel Frolov | Ask Dima to remove Yavorsky (heard) from reviewers on HFM-692 (heard) | TBD | Normal | Alexey also asked Andrei |
| 7 | Pavel Frolov | Finish the installer that keeps old RIS data; use build 4353 (heard) from the 224 server | TBD | Normal | For Ivan |
| 8 | Pavel Frolov | Close his draft task as a duplicate | Oct 28, 2026 | Low | Dmitri's question |
| 9 | Anton Seregin | Finish drafts; review with Pavel, Irina and Sergey | TBD | Normal | Then split by repo and move to Jira |
| 10 | Anton Seregin | Close the emulator / kiosk rename task | Oct 28, 2026 | Low | Done long ago |
| 11 | Daniil Stauskiy | Re-read IP-1113 (heard), board report | TBD | Normal | |
| 12 | Igor Metelski | Rebuild Sparkle Seven with the new math | TBD | Normal | |
| 13 | Sergey Tsimanov | Update CI for the production update | TBD | Normal | |
| 14 | Vladimir Samusenko | Sort out the two IQ text tasks and review 1–2-year-old backlog tasks | TBD | Low | Text library missing |

## Open Questions

- Who sets up the cloud terminal hub so services can be pulled from repositories (Alexey).
- Does multi cash-out in BV mode add up to one ticket on SAS (Alexey, Pavel).
- What to do about Yavorsky's (heard) review comments on HFM-692 (heard) (Alexey).

## Dispatch Log

---
*Processed from Teams transcript on October 28, 2026*
*Source meeting: Daily Standup meeting*
