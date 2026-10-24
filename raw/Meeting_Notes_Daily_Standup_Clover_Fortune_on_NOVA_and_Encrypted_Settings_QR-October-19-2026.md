# Meeting Summary — Daily Standup meeting
**Date:** October 19, 2026, 4:46 AM – 5:17 AM Eastern
**Duration:** ~31 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026]]

## Summary

Held in Russian. Pavel joined about 7 minutes late. Irina proposed moving the standup to 12:00; Pavel said "let's think". Not decided.

**Encrypted settings QR for Flex IQ and Flex-Ports (MVP2, Pavel).** The team must design how settings reach Flex IQ and Flex-Ports: Wi-Fi network name and password, network order (modem or LTE), Flex IQ parameters such as PIN codes, and binding. The QR code is generated on a server page for the location. The location owner or a technician bound to that location logs in and runs "export settings"; the page shows the QR. The QR is encrypted with a key personal to that location; the registered Flex IQ has the key, decrypts on scan, and applies the settings without showing them. Flex IQ can also get settings over the network, but if Wi-Fi is the only network, the QR is the only way. For Flex-Ports the QR is likely the only way. **A plain QR is not acceptable**: anyone could use "share network" on a phone, show the QR to the terminal, and break its real network. Only authorized staff may change settings. Start on the server side, collect the parameter list, and maybe run an architecture spike first on decryption on Flex-Ports. A task will be created for Anton Seregin. Alexey asked if terminals read a QR from a phone screen; Pavel: yes, at least a normal QR.

**Anton Leshkevich.** Finished porting Clover Fortune from Rage to NOVA; it plays in vertical and horizontal. Most game memory goes to textures and animations. WebP was likely chosen for online games (fast over the network). In AI-assisted tests he saved 1 to 1.5 GB of video memory on Clover Fortune with another texture format (format not named clearly). This matters for cheap hardware, where the GPU and the OS share one memory module. He did not yet check the Clover Fortune help screens and will recheck everything before the Wednesday deadline. Math for Clover Fortune is in a container (Efim made it). Irina: invite Anton to the Wednesday meeting where Igor shows Dutch Mill moved from Rage to NOVA, to compare both results. Whether Efim made math for all 6 games: ask Igor.

**Alexander Biratko.** Two tasks: IO board firmware update, and Terminal Hub connection checks, including attempts to spoof the hub (a terminal with a fake number). Andrei does part of the cloud hub changes. The repo README says the CI-built IO board firmware never ran on hardware. Pavel: the board in Alexander's Flex Pay already runs the CI build; it was not tested on gaming machines. Remaining step: build a version change, flash it and roll it back through the board service. Pavel: an AI Draft task (heard "SP 1360") is on Alexander; review it fast because it disappears after a day. Move it to To Do or reject it with a reason.

**Alexey Khamin.** Still adapting tests for CI, and reviewing.

**Anton Seregin.** Finished the printer scenarios. Closed a task from Vladimir (heard "FAKE 171"). Status of feature (heard "FAKE 67") is not clear in the transcript. Other devices sit in backlog (one heard as "fi 8 sei", LTE modem, LED strip light emulation, Wi-Fi QR). He tested a Wi-Fi QR on a normal bank scanner: it beeps but nothing is processed; this is not built at the kiosk. Pavel: it existed before, maybe broke, but was not encrypted, so it does not fit anyway.

**Daniil Stauskiy.** NOVA got dependency updates from the bot (Jest and others). The change touches mapping for contracts, so it needs its own feature; he will load all version bumps there. Found a small modifier display issue in the game bonus; will settle it with Sasha. Waiting for screens from Pavel to test on 2 large screens. Will try re-converting textures as Anton did. Asked Anton which format he used and asked for access to the second game. Pavel: yes. Anton will send the repo name in chat and a link to his Jira task with the image compression report (steps written by Claude).

**Evgeny Kharetski.** Fully closed one item (heard "NDP 1"). Ivan has battery questions; they will work through them. Starting the new project: the AI game designer agent. Pavel: a Jira project is needed for it; Evgeny: own repository, features, done properly. NOVA tasks remain (e.g. moving progressives). Evgeny works three directions at once: NOVA, Ivan's tests, and the AI agent.

**Irina Shishko.** Re-running tests rewritten in the new way and fixing gaps. Pavel: create tests for MVP2; review its capabilities and requirements. Irina: MVP2 still holds Pay, while the needed items sit in MVP3. Andrei owns capabilities, but waiting for him is too slow, so she will move Flex Pay to MVP3 herself and re-sort. Pavel agreed.

**Ivan Shpak.** Working with Evgeny on battery replacement; Evgeny answered his 14 questions yesterday.

**Sergey Tsimanov.** Finished the LISA implementation (soft-install handling discussed before) and deployed it on STG; it can be tested. Created a passport task from the earlier talk and works on it now. Passport and LISA are separate checks in one chain; testers can check LISA now if they do not change the passport. Claude set the passport due date to Oct 30; Sergey will change it himself (he expects it within about 3 days). Irina: max Oct 21–22.

**Jira (Dmitri).** About 11 tasks hang with a closed parent; Pavel must review them. Pavel: Claude linked the new stories to a feature that already closed. Dmitri suggested creating something to hang them on so they do not drop down the plan.

**Third-party machines (Pavel).** Flex-Port works incorrectly over AFT with the visiting Light & Wonder machines. On one machine money goes in by AFT but cash-out fails. On the second Light & Wonder machine commands go out but do not reach cash-in or cash-out. IGT does not answer the lock command (heard "72") and keeps reporting locked. Pavel asked Evgeny and Sasha for advice. Evgeny: look at what the port logs. The rest of the team was released; this topic continued as a new meeting, recorded separately.

## Decisions Made

- **Settings QR for Flex IQ / Flex-Ports must be encrypted per location and created only by authorized staff on a server page; a plain Wi-Fi QR is not acceptable.** — a plain QR lets anyone break the terminal network. (Decided by Pavel Frolov)
- **The team moves Flex Pay to MVP3 itself instead of waiting for Andrei.** — waiting is too slow. (Irina Shishko; Pavel Frolov agreed)
- **The passport task due date moves earlier than the Oct 30 that Claude set.** — Sergey expects ~3 days; Irina: Oct 21–22 at most. (Sergey Tsimanov, Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Create the server-side task for the encrypted settings QR (parameter list; maybe an architecture spike on decryption on Flex-Ports) for Anton Seregin | TBD | High | MVP2 |
| 2 | Anton Seregin | Work the encrypted settings QR task once created | TBD | Normal | |
| 3 | Anton Leshkevich | Recheck Clover Fortune, including help screens | Oct 21, 2026 | Normal | Wednesday deadline |
| 4 | Irina Shishko | Invite Anton Leshkevich to the Wednesday Dutch Mill review | Oct 21, 2026 | Normal | |
| 5 | [Unassigned — needs clarification] | Ask Igor whether Efim made math for all 6 games | TBD | Low | Irina and Pavel |
| 6 | Alexander Biratko | Review the AI Draft task on him: move to To Do or reject with a reason | Oct 20, 2026 | Normal | Disappears after a day |
| 7 | Alexander Biratko | Test IO board firmware update and rollback through the board service | TBD | Normal | |
| 8 | Anton Leshkevich | Send Daniil the repo name and the Jira link to the image compression report | TBD | Normal | |
| 9 | Pavel Frolov | Give Daniil access to the second game and the screens for the 2 large displays | TBD | Normal | |
| 10 | Daniil Stauskiy | Create a separate feature for dependency updates; fix the bonus modifier display with Sasha; test texture re-conversion | TBD | Normal | |
| 11 | [Unassigned — needs clarification] | Create a Jira project for the AI game designer agent | TBD | Normal | Pavel raised it |
| 12 | Irina Shishko | Move Flex Pay to MVP3, re-sort MVP2 capabilities, create MVP2 tests | TBD | Normal | |
| 13 | Sergey Tsimanov | Finish the passport task and change its due date | Oct 22, 2026 | Normal | |
| 14 | Pavel Frolov | Review ~11 tasks whose parent feature is closed | TBD | Normal | |
| 15 | Pavel Frolov, Evgeny Kharetski, Alexander Biratko | Review AFT cash-out problems on Light & Wonder and IGT, using port logs | TBD | High | Continued in a separate meeting |

## Open Questions

- Move the daily standup to 12:00? (Irina Shishko; Pavel: "let's think")
- Which texture format replaces WebP across games? (Daniil Stauskiy)
- Did Efim make math for all 6 games or only one? (Irina Shishko, Pavel Frolov)
- Where should stories linked to a closed feature hang so they do not drop off the plan? (Dmitri Kovalchuk)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-19*
*Source meeting: Daily Standup meeting*
