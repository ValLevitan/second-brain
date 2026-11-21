# Meeting Summary — Daily Standup meeting
**Date:** November 13, 2026, 6:16 AM – 6:44 AM Eastern
**Duration:** ~27 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Vertical_Rage_Games_for_Texas_and_Agent_Date_Moves-November-13-2026]]

## Summary

**Vertical Rage games for Texas.** Pavel said Val asked yesterday about turning horizontal machines into vertical ones. Some horizontal machines came in; a vertical machine is more useful for Texas. The idea: convert the machine fast, load the right software, and have a ready product for Texas. Igor already converted 6 games (the Texas games, NAD 1) from horizontal to vertical, as a first version, on his branch 1.27. The art was made with an AI tool and nobody approved it. He thought it was an experiment. To go further he needs creative briefs, for example how to use the top half of the screen for games that never had a vertical version. Irina said the work must also move to GitHub, and nothing goes to anyone yet. Pavel: plan tasks to move the needed parts to GitHub; the next step is CI/CD, an integration repo that builds Rage games into an ISO. Igor and Pavel will talk after the meeting.

**Sound in the new engine.** Daniil opened a pull request for NewGin-26 and checked it with a non-local LGS; sound plays well, and the Studio is fixed too. The old sound handling should come out of LGS. Alexander: LGS can and should be changed, in a separate task from the engine. Dmitri K: each repo has its own Jira project (table in the knowledge base).

**Autotests.** Anton Seregin finished the emulator part of test 129. Claude suggested splitting checks into a real-device part and an emulator part (for CI and fast PR checks), marked in the acceptance criteria. Pavel agreed it makes sense. A separate profile for the real Flex-Port is the next task. Anton also created 2 test accounts on STG for test 129. They are hard-coded; if the database is cleaned, tests fail, and nobody owns restoring them. Pavel: discuss separately with Irina, Ivan and Alexey.

**Due dates and the PM agent.** Dmitri K said due dates are much better. The agent's reminders had a bug (a task was reminded only once); now it reminds about all problem tasks. He proposed that the agent move due dates when asked in chat. Pavel: useful, if people read what the agent says. Dzmitry asked for a warning a day before. Dmitri K will turn on date changes today (if Microsoft works), test it one week, then maybe add early reminders; he may do it only for Dzmitry's own tasks.

**Status by person:**
- **Alexander:** adding the drum-management screen; tasks are in review and will close as a group. Pavel asked him to set end dates on in-progress tasks; he agreed.
- **Anton Leshkevich:** building an automatic builder; good progress; details in a meeting after the standup.
- **Dzmitry:** reviewed MVP 2 capabilities, waiting for Andrei. NAD 2 data received; will check if paytables change, if not migrate automatically. Starts the migration work today with Andrei (accounting host, prod). May switch off unneeded senders to make the database smaller. Repo rename from RK3568 to RK35xx not done yet. Pavel: run Claude over the projects (Flex IQ etc.) so actions use 35XX, not 3568. Dzmitry warned the Lotto Amazon key is tied to 3568; the parameter must not be erased at build time. LTE on the machine is still on him.
- **Evgeny:** LTE on/off. Will clear his Jira backlog, maybe on the weekend.
- **Igor:** GLI games now run on Windows. Cannot load the emails GLI sent; asked Ivan to copy them. Helped designers with branches; Nebraska; small fixes in NOVA 2 tools; symbol creation.
- **Irina:** autotests; reworking features because requirements changed.
- **Ivan:** RIS performance on the prod build. Pavel: update the date on the manual test task.
- **Sergey:** changes for installs; QR Wi-Fi in parallel.
- **Vladimir:** his tests are blocked, waiting for features, Wi-Fi or cloud. Helping Evgeny with contracts for hardware services in the NOVA integration repo.
- **Pavel:** closed the printer problem. Today: raise the Wi-Fi module speed (baud rate) and check reliability; MVP 2 tasks; MVP 1 for the recycler.

## Decisions Made

- **LGS and engine sound changes are separate tasks; sound handling is removed from LGS.** (Alexander, Pavel)
- **Autotests are split into a real-device part and an emulator/CI part, marked clearly in acceptance criteria.** (Anton Seregin proposed; Pavel agreed)
- **Vertical Rage work: plan moving the needed parts to GitHub, then build CI/CD (integration repo that builds the ISO).** Nothing is given out yet. (Pavel, Irina)
- **The PM agent may move due dates on a chat command; one-week trial.** (Dmitri K; Pavel agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Daniil Stauskiy | Open separate tasks for removing sound from LGS and for the engine | TBD | Normal | |
| 2 | Alexander Biratko | Set end dates on in-progress tasks | Nov 13, 2026 | Normal | Pavel's request |
| 3 | Anton Leshkevich | Explain the automatic builder progress in a meeting after the standup | Nov 13, 2026 | Normal | |
| 4 | Anton Seregin | Next task: separate test profile for the real Flex-Port | TBD | Normal | |
| 5 | Pavel Frolov, Irina Shishko, Ivan Shpak, Alexey Khamin | Decide who restores autotest accounts on STG if the database is cleaned | TBD | Normal | Raised by Anton Seregin |
| 6 | Dzmitry Chudzinau | Start NAD 2 migration work with Andrei | Nov 13, 2026 | Normal | |
| 7 | Pavel Frolov, Dzmitry Chudzinau | Run Claude over projects so actions use RK35XX, not 3568 (keep the Lotto key parameter) | TBD | Normal | Tasks already on Pavel, Dzmitry and others |
| 8 | Evgeny Kharetski | Clear Jira backlog | Nov 15, 2026 | Low | "maybe on the weekend" |
| 9 | Ivan Shpak | Copy GLI's emails to Igor | TBD | Normal | Igor's request |
| 10 | Igor Metelski, Pavel Frolov | Plan tasks to move Rage parts to GitHub, then CI/CD; talk after the meeting | Nov 13, 2026 | Normal | |
| 11 | Ivan Shpak | Update the date on the manual test task | Nov 13, 2026 | Normal | Pavel's request |
| 12 | Pavel Frolov | Raise Wi-Fi module baud rate and check reliability | Nov 13, 2026 | Normal | |
| 13 | Dmitri Kovalchuk | Turn on agent date changes; run a one-week trial | Nov 13, 2026 | Normal | |
| 14 | Dmitri Kovalchuk | Maybe add day-before reminders for Dzmitry's own tasks | TBD | Low | |

## Open Questions

- Creative briefs for the vertical games: how should the top half of the screen look for games that never had a vertical version? (Igor)
- Is the AI-made art acceptable? Someone must review it. (Igor)

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
