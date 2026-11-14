# Meeting Summary — Daily Standup meeting
**Date:** November 9, 2026, 6:15 AM – 7:05 AM Eastern
**Duration:** ~50 minutes
**Attendees:** Pavel Frolov (host), Irina Shishko, Anton Leshkevich, Daniil Stauskiy, Alexander Biratko, Alexey Khamin, Anton Seregin, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko, Dmitri Kovalchuk
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Due_Date_Rule_in_Standard_and_Update_Dependency_Map-November-9-2026]]

## Summary

**Due dates in Jira (Dmitri Kovalchuk, long discussion at the end).** Friday's report missed about 30 tasks that have no due date; Dmitri sends a message on them tomorrow. He offered to block the move to To Do or In Progress when the due date is empty. Dzmitry proposed a default of one week instead. Pavel does not want a hard block: allow the move, send a notification the next day. Evgeny: he rarely uses To Do, his Claude moves backlog tasks straight to In Progress and most close within a day, so a due date adds nothing at today's speed; field work (GLI, Eclipse, field bugs) cannot be planned; he even has a daily job that pushes overdue due dates later. Dmitri disagreed: for real planning the field matters. Pavel explained the purpose: with a due date per task you see which list fits into a month before a release. Outcome: the rule goes into the standard so every Claude sets a due date when a task moves to To Do; whoever moves a task to To Do sets the date, not necessarily the person who does the work; the creator must not put a new task straight into To Do. Dmitri changes the standard today. Evgeny's Claude was trained on the standard from two weeks ago and does not set due dates; it does enforce "no work without a task" and branch naming.

**Sound (Daniil).** FRAM-1496 checked: the board plays loud sound, the problem was found and fixed. FMOD-5 (heard) goes In Progress and uploads tomorrow: a complete move to the Rust sound library with stereo and automatic sound distribution. Anton Leshkevich asked him to integrate the library with the engine Anton is writing; Anton has a task for it and will write to Daniil after the meeting. Alexander: LGS and the engine still need a link for volume control and test sounds. Pavel: the old need to stop sound in the framework for data-center tests goes away. Alexander: sound can now sync to the frame, and a game pause with sound pause becomes possible.

**Alexander Biratko.** Three projects: over the weekend he took the recycler repository and the Flex-Pay audit, and started bringing FPORT tasks up to date (FPORT-38 heard, not finished; merge will take time). Flex-Pay update work continues, tests are long. Irina sent him port bugs; he starts them tomorrow morning. The recycler moves to the Pay platform as the base; his experiment with the new recycler worked: it answers statuses and switches. The old recycler is not needed, as Val said; Alexander removes it from the project.

**Alexey Khamin.** Testing updates sent through the Flex-Port terminal; Sergey updated something and it should work now. Today he helps with the production install on the Flex IQ. Hardware autotests run in parallel. Irina sorted the current MVP 2 capabilities and requirements into features and assigned them to Alexey, Vladimir and herself: whenever he waits on something, he writes those tests, otherwise the team will not make it.

**Anton Leshkevich.** Ported casino games to make the framework support more game types, not only slots. Next: build the engine for the boards; he needs the boards and accounts from his email. Pavel: it may be simpler to buy locally with allocated money; Anton sent Mery the Amazon links and will settle it with her. Meanwhile he works on game templates in Rust and the studio that the agent rewrites to the game design. He sent Igor the links from Saturday's engine meeting; they will talk during the day.

**Anton Seregin.** Firmware emulation in progress: fake firmware, receiving it from the cloud to the terminal and on to the port. Pavel proposed that Anton also covers the autotests for firmware transfer to the Flex-Port, since he builds the emulator anyway. It is all one feature, FIQ-81 (heard), in the integration repository. Irina sets Claude to find all related tests and move them to Anton.

**Dzmitry Chudzinau.** With Andrei he continues reworking the account host. Asked about the CMS deploy status (letter sent Friday). Asked about BusyBox: Pavel recalls a 2009–2010 license letter from the rights holders during development, before any release; Claude sees no problem. Pavel: for every product we need to keep license files per component and a page listing every component in the image, perhaps reachable by QR code; then no problems. Dzmitry had been waiting since last Monday to commit to Flex IQ; Pavel and Irina: on Tuesday everyone was told they can commit again. Manifests for the update system: no math, no framework, no games exist yet. Pavel: the new engine and games are not ready; math is open now (Val gave the go-ahead), ask Andrei Bosik for the repository; Efim rewrote math in Rust. Dzmitry explained to Anton: the team builds a system of future updates of any component on the machine; a single element (game, LGS, framework, math) may be replaced and the server must know nothing breaks, so a dependency map by version is needed; he needs all repositories so Claude can see how they interact. Anton will send his repository links; Dzmitry asks Andrei for access.

**Evgeny Kharetski.** Saturday: the SAS tool agent and NOVA. RIS improvements: fixed the transfer bug Irina reported (new version looked for a ris_new file that old versions never create; now takes the last saved by number), added a warning that RTP cannot be checked so apply at your own risk. With Ivan he answered GLI questions. The SAS tool now checks a machine against the specification over SAS and shows what it supports (Dzmitry's idea); on our machine 96% coverage. Pavel: that was missing two weeks ago with foreign machines. A mode to run NOVA autotests through the SAS tool is close; he needs Pavel's pull request merged. Math is mocked until games exist; a math contract was added to LGS and he is testing contracts so new versions of the progressive controller stay compatible.

**Igor Metelski.** Took Anton's repositories; added custom shader support for objects on different views and on one view, in a local branch; wants a shared branch to commit to. NAD 2 FPS is unstable locally, he fixed a couple of places. Math DLLs lying in the Rage games can be wrapped in a small server that talks to LGS by the same protocol as Efim's math server, so development does not have to wait for Efim.

**Irina Shishko.** Started writing tests for MVP 2, created the features over the weekend, ran Alexander's port tests and listed what to fix.

**Ivan Shpak.** With Evgeny looked at the GLI answers; one item likely goes to Igor on the framework side. Built with Evgeny's RIS improvements changes; will check the delivered machine. Pavel: the tasks dated November 5–6 are on him.

**Sergey Tsimanov.** Wi-Fi: QR done on the IQ side; now network creation, then the protocol for the Flex-Ports.

**Vladimir Samusenko.** On TINT-115 (heard); TINT-111 Wi-Fi tests: the terminal as access point with internet from the SIM card is implemented on machine 84 but not yet in the firmware. Pavel: Sergey rebuilds the Flex IQ and it should work on the Flex-Ports; only two ports have Wi-Fi, one more will be made; all Flex IQ have the module, antennas must be checked. Irina wants one of her ports 156 or 159 fitted. TINT-101 and TINT-102 came back to Vladimir; Irina will check and close them. He finished a draft of capabilities for LGS and will enter them in Jira. Pavel moves all Wi-Fi ports to Sergey.

**Closing.** Irina asks Pavel about FIQ-8 (heard), in the backlog, one feature per capability needed now. Ivan reminds Pavel about Andrei and the Git deletion issue.

## Decisions Made

- **The standard gets a rule: a task moved to To Do must have a due date; Claude sets it automatically** — closes the missing-due-date problem for everyone. (Pavel, Dmitri Kovalchuk)
- **The creator must not put a new task straight into To Do; whoever moves it to To Do sets the date** — (Dzmitry, Irina, Pavel)
- **No hard block in Jira on empty due date; a next-day notification instead** — Pavel rejected Dmitri's block. (Pavel)
- **Due dates are needed at feature level; small features need not be split into stories** — (Pavel)
- **Anton Seregin also covers the autotests for firmware transfer to the Flex-Port, all under FIQ-81 (heard)** — he builds the emulator anyway. (Pavel, Irina)
- **The old recycler is removed from the project; the new recycler on the Pay platform stays** — per Val. (Alexander)
- **Math repository is open to Dzmitry for the dependency map; ask Andrei Bosik** — Val gave the go-ahead. (Pavel)
- **All Wi-Fi ports move to Sergey** — (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Update the standard today: due date required when moving to To Do, creator does not move to To Do | Nov 9, 2026 | High | Send to everyone |
| 2 | Dmitri Kovalchuk | Send the message on the ~30 tasks without due date | Nov 10, 2026 | Normal | |
| 3 | Daniil Stauskiy | Upload the finished Rust sound library (FMOD-5, heard) | Nov 10, 2026 | Normal | Stereo and auto distribution |
| 4 | Anton Leshkevich | Write to Daniil after the meeting about integrating the sound library into the engine | Nov 9, 2026 | Normal | |
| 5 | Anton Leshkevich | Settle the board purchase with Mery; talk to Igor about the engine | Nov 9, 2026 | Normal | Amazon links sent |
| 6 | Anton Leshkevich | Send Dzmitry the links to his repositories | TBD | Normal | For the dependency map |
| 7 | Dzmitry Chudzinau | Ask Andrei for access to Anton's repositories and the math repository | TBD | Normal | |
| 8 | Alexander Biratko | Start Irina's port bugs tomorrow morning; remove the old recycler from the project | Nov 10, 2026 | Normal | |
| 9 | Alexey Khamin | Write the MVP 2 tests Irina assigned whenever he waits on something | TBD | Normal | |
| 10 | Irina Shishko | Have Claude find all tests tied to firmware transfer and move them to Anton Seregin | TBD | Normal | |
| 11 | Irina Shishko | Check TINT-101 and TINT-102 and close them if not tests | TBD | Normal | Anton wrote them, Sergey commented |
| 12 | Evgeny Kharetski | Connect the NOVA autotest mode in the SAS tool once Pavel's pull request is merged | TBD | Normal | |
| 13 | Pavel Frolov | Merge the pull request Evgeny is waiting on | TBD | Normal | |
| 14 | Pavel Frolov | Move all Wi-Fi ports to Sergey; look into FIQ-8 (heard) in the backlog | TBD | Normal | |
| 15 | Ivan Shpak | Check the delivered machine with the new RIS improvements build; the tasks dated Nov 5–6 | TBD | Normal | |
| 16 | Vladimir Samusenko | Enter the LGS capabilities draft into Jira after a review | TBD | Low | Status to discuss next meeting |

## Open Questions

- BusyBox license: is there a problem or not? (Dzmitry, Pavel)
- Status of the CMS deploy Dzmitry asked about on Friday? (Dzmitry)
- Which Flex-Port numbers have the Wi-Fi module? (Vladimir)
- In what status and to whom does Vladimir enter the LGS capabilities? (Vladimir)

## Dispatch Log

---
*Processed from Teams transcript on November 10, 2026, 7:40 AM Eastern (scheduled meeting-watcher)*
*Source meeting: Daily Standup meeting*
