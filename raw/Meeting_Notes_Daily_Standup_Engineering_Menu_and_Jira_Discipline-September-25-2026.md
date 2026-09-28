# Meeting Summary — Daily Standup meeting
**Date:** September 25, 2026, 4:57 AM – 5:24 AM Eastern
**Duration:** About 27 minutes
**Attendees:** Pavel Frolov (chair), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Engineering_Menu_and_Jira_Discipline-September-25-2026]]

## Summary

Spoken in Russian. The speech recognition is poor in places, so some task numbers below are uncertain. Round-the-table status, then two longer topics: an engineering menu for technicians, and the new Jira discipline emails.

**Engineering menu idea.** Vladimir will soon run out of FlexPort screen work. Pavel proposed a page in TouchGFX for an **engineering menu**, for technical staff, not operators. It would open in a special way, for example by scanning a special QR code. It could have several pages: a network page (IP addresses, link state, Wi-Fi signal level), a page with the last transactions, and a page with recent errors (time, type, loss of connection, a device dropping off, failed transactions). Pavel said IP addresses matter most to him, because the production build will not show them. Vladimir will sketch something and then they discuss. Dzmitry suggested that, for now, Claude looks at Andrei's mockups and builds screens close to them; the differences get checked at the end.

**Jira discipline emails.** Dmitri Kovalchuk said emails went out today to people whose Jira tasks have problems. They will arrive **every morning**, only to people who have problems. Problems include: an end date already in the past (example: HFM-671, end date September 5), a task In Progress for more than 14 days, a child still in progress under a closed parent, and a To-Do task with no dates. Fixes can be made by hand, or by asking Claude, which takes 5–10 minutes (for example, move dates one day forward). Most problems are with Pavel and Irina; Andrei fixed all of his today. Dzmitry also got a message titled "Jira hierarchy exceptions, Friday 25"; Dmitri said that is a different message and will come and look at it. Pavel closed: **everyone watches their own dates.**

**Debug flags for tests.** Alexey wants tests to be able to set a cashier PIN and a lease directly on a terminal, for virtual terminals. Dzmitry does not like flags that make it feel like a separate build, and does not want business logic like "do not overwrite if flag is on". They agreed a test may set these values, and the server may overwrite them later. Dzmitry will think about it and may add a list.

**Individual status.**
- **Alexey Khamin** — mostly autotests; waiting for an API from Dzmitry.
- **Alexander Biratko** — software updates. Andrei created the needed keys in the repository; he is now generating certificates to upload.
- **Anton Seregin** — progressive work (task 12-60). His branch is old and has conflicts with main; he is resolving them. Then he will write instructions for IQ to move the emulator project. Pavel asked that the "prose" (the description of how it works) is also updated. Rule stated by Pavel: on every merge into main or a top-level branch, the prose must be updated to match the code.
- **Daniil Stauskiy** — committing the button move changes. Talked to Igor about a game to test; will likely copy one of our games and change its config for testing. Igor said the rest of the screen moves to next week.
- **Dzmitry Chudzinau** — CAP 152; closed a batch, about 3 items left. With Andrei, will review the GitHub variables for updates: which are common to all terminals and which are per terminal.
- **Evgeny Kharetski** — integration with a partner service; RIS work needs a lot. Waiting on a task he gave Anton. Moving commits across (task number not clear in the transcript). Next: CI/CD for the progressive controller, then the proto, then a regression repository, then a simple build that a non-technical person (for example an artist) can run, then autotests.
- **Irina Shishko** — sorting out differences and an email, then creating features for autotests.
- **Ivan Shpak** — the Eclipse test passed. He will create another installation for the next game package, then one more for the last games plus devices. Then autotests. His changes are in the port 9 branch. Task 14 is ready (PR ready) but not closed until Alexey commits his part.
- **Sergey Tsimanov** — took a Flex IQ task on receipt printing from Dima; doing their scopes together. Pavel mentioned a link quality / device state dashboard per device as later work.
- **Vladimir Samusenko** — FlexPort fixes after Andrei updated the description. All missing screens already have tasks under CAP 156. Collector screens need FlexPort tasks 14 and 15, and claim screens need port tasks 63 and 64 (backend first). Design task port 52; all commits go into the port 9 branch, so these tasks ship together. Will send Pavel the document that describes all this. Done in about 1–1.5 hours, then needs new work.

**Meeting with Alekseev.** Alexey's pull request is still waiting. Pavel told him to request a meeting with Alekseev. Irina said to include Pavel.

## Decisions Made

- **On every merge into main or a top-level branch, the prose (description) must be updated to match the code.** (Stated by Pavel Frolov)
- **Tests may set the cashier PIN and lease directly; the server may overwrite them.** No "do not overwrite" business logic. (Agreed by Dzmitry Chudzinau and Alexey Khamin)
- **Everyone watches their own Jira dates**, using the daily discipline emails. (Decided by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Seregin | Resolve conflicts with main, then write instructions for IQ to move the emulator project, with updated prose | TBD | Normal | |
| 2 | Vladimir Samusenko | Sketch an engineering menu (network, last transactions, recent errors) for discussion | TBD | Normal | Pavel's idea; IP addresses most important |
| 3 | Vladimir Samusenko | Send Pavel the document describing the missing screens and tasks | TBD | Normal | |
| 4 | Alexey Khamin | Request a meeting with Alekseev about his pending PR, include Pavel | TBD | Normal | |
| 5 | Dzmitry Chudzinau | Think about test flags for PIN and lease; add a list of needed items | TBD | Low | |
| 6 | Dzmitry Chudzinau | With Andrei, review GitHub update variables: common vs per terminal | TBD | Normal | |
| 7 | Dmitri Kovalchuk | Look at Dzmitry's "Jira hierarchy exceptions" message | Today (Sep 25, 2026) | Low | |
| 8 | Ivan Shpak | Create the next Eclipse installations (next game package, then last games + devices) | TBD | Normal | |
| 9 | All | Fix own Jira date and status problems from the daily emails | Ongoing | Normal | |

## Open Questions

- Which pages and data the engineering menu should hold (Pavel, Vladimir).
- Whether debug flags for tests should exist at all, and which ones (Dzmitry).

## Dispatch Log

---
*Processed from Teams transcript on September 25, 2026*
*Source meeting: Daily Standup meeting*
