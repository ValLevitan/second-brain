# Meeting Summary — Daily Standup meeting
**Date:** October 7, 2026, 4:52 AM – 5:13 AM Eastern
**Duration:** ~21 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Alexander Biratko, Sergey Tsimanov, Vladimir Samusenko, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026]]

## Summary

Wednesday standup run by Pavel. Held in Russian. Some task numbers are garbled in the transcript.

**Test coverage first.** Alexey finished the repo rules; prose is at 90%+. The CI work is at the report stage. He asked if the next steps (runs on real hardware by IP address, and hooking the test system into product repos) should start now. Pavel: not now, first cover the code with tests. Irina: the team is behind on test count because Alexey was on this work. Alexey will finish manual runs and then move to writing tests.

**AI now reads meetings.** Kovalchuk: meetings are in a pilot where AI processes them and will create Jira tasks. Say what you work on, with task numbers, so the AI can assign and create tasks correctly. Pavel: if a need comes up, say it in the meeting; the assistant may propose future tasks. Kovalchuk also asked everyone to watch overdue dates; Alexander has about 17 overdue.

**Bugs vs stories.** Alexander has 14 tasks in progress, partly because Claude opens bugs while he builds a feature. Pavel: bugs are for problems from outside; issues found during development are stories. Alexander will have Claude open stories instead.

**Flexport idle timer.** Irina asked if the 30-second timer restarts when the screen is touched. Pavel: yes, by common sense. Irina: the requirement does not say so clearly, so Claude raises questions.

**MVP1 stories.** Irina wants stories pulled up so they do not block features. Pavel: anything needed for MVP1 goes straight to To Do, even with no due date.

**Jira Hierarchy report.** Irina gets a report naming 44 regulations she must act on; they are active and assigned to no one (reporter Bosik). Kovalchuk: the report flags regulations that are active but not published. Pavel: take it to Andrei Bosik. Irina said Andrei will come and explain. Dzmitry had a similar case on the TINT branch. Pavel asked Alexey to check TINT-5 and TINT-6; if nothing useful, Pavel deletes them.

**Other.**
- Anton: cleaned his Jira and closed one item and its story. Moved one item that checks Sergey's work (key problem). Took 3 repos for prose and contracts; most done. Works on emulator fixes in parallel; a story from Alexey (and maybe Vladimir) still to do.
- Daniil: wrote prose for Novaport; contracts for the SDK sound repo; rewrote framework contracts and added a contract check when a PR opens. Pavel will give him a new board to test performance.
- Dzmitry: closed PORT-82 (two SAS connections). Deploying Mutagus removal to dev/stage; closes it if tests pass. Created a couple of stories. Pavel saw his PRs, no remarks; Claude review done and fixed.
- Evgeny: Claude advised starting with error handling; mostly done. Next task removes the QR and statistics. Release went out yesterday; Ivan's SAS question to be handled later.
- Alexander: Wi-Fi capability CAP-143 (tasks 1328, 1331); many tasks close today.
- Irina: tests today TIN-19, then TIN-16. Pavel asked to name tests by number or capability for the record.
- Ivan: checks yesterday's South Dakota issue (not sure it is a bug), then hands over South Dakota. Next priority: battery. Pavel may ignore Wi-Fi items in his story, since Wi-Fi is still in development.
- Sergey: found memory problems on Flex and created a capability and features. Today finishes printer statuses, then the new work.
- Vladimir: rechecked tasks 40 and 41 after blockers cleared. Installed Flexport this morning; reruns and logs defects if confirmed.

## Decisions Made

- **Cover code with tests first; CI hardware runs and product-repo hookup wait.** — Team is behind on tests. (Decided by Pavel Frolov, Irina Shishko)
- **Problems found during development are logged as stories, not bugs.** — Bugs are for problems from outside. (Decided by Pavel Frolov)
- **Items needed for MVP1 go straight to To Do, even with no due date.** (Decided by Pavel Frolov)
- **Flexport 30-second idle timer restarts on a screen touch.** — Requirement text is unclear. (Pavel Frolov)
- **Jira Hierarchy report question goes to Andrei Bosik.** (Decided by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | Finish manual test runs, then move to writing tests | TBD | High | Test coverage first |
| 2 | Alexey Khamin | Check TINT-5 and TINT-6 for anything useful | TBD | Low | Pavel deletes if not |
| 3 | Pavel Frolov | Give Daniil a new board to measure performance | TBD | Normal | |
| 4 | Dzmitry Chudzinau | Finish Mutagus removal on dev/stage; close if tests pass | TBD | Normal | |
| 5 | Alexander Biratko | Close finished Wi-Fi tasks; have Claude open stories, not bugs | Oct 7 | Normal | ~17 overdue |
| 6 | Irina Shishko | Run tests TIN-19, then TIN-16 | Oct 7 | Normal | |
| 7 | Ivan Shpak | Check yesterday's South Dakota issue, hand over; then battery work | TBD | Normal | |
| 8 | Sergey Tsimanov | Finish printer statuses, then the Flex memory features | Oct 7 | Normal | |
| 9 | Vladimir Samusenko | Rerun tasks 40 and 41 on Flexport; log defects if confirmed | TBD | Normal | |
| 10 | Irina Shishko | Ask Andrei Bosik about the 44 regulations in the Jira Hierarchy report | TBD | Normal | |
| 11 | All | State task numbers in meetings; watch overdue dates | Ongoing | Normal | AI pilot |

## Open Questions

- Should the Flexport timer rule be written into the requirement? (Irina Shishko)
- Why the Jira Hierarchy report sends 44 unassigned regulations to Irina (Irina Shishko).
- When to start CI hardware runs and product-repo hookup (Alexey Khamin).

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-07*
*Source meeting: Daily Standup meeting*
