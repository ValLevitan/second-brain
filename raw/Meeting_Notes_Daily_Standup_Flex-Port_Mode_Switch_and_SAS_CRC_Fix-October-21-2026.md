# Meeting Summary — Daily Standup meeting
**Date:** October 21, 2026, 4:46 AM – 5:15 AM Eastern
**Duration:** ~28 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Flex-Port_Mode_Switch_and_SAS_CRC_Fix-October-21-2026]]

## Summary

Held in Russian. Some names and ticket numbers are unclear in the transcript and are marked "heard".

**Flex-Port mode switch from the kiosk does not work (Alexander Biratko).** Alexander finished the Flex Pay vs Flex IQ communication analysis. He found many changes and created about 8–10 tasks under existing requirements (or requirements taken from Flex IQ). No new capabilities were needed. He starts implementing them. Today a Flex-Port cannot switch between SAS and bill validator mode on a kiosk command; someone must connect by telnet. Pavel: by design, a technician sets the mode per machine from the kiosk, because one kiosk can serve different machine types. The kiosk-to-port command is not built on the Flex-Port side. Pavel: "we will not wait" for Alekseev; it is about a 5-minute task on the port. Alexander has no port access yet but offered to do it. Sergey Tsimanov said it worked when he built it. Alexey Khamin: the switch exists on the terminal, but Flex-Port does not change its mode; he will re-check. Pavel: the mode is written to EEPROM and survives a restart.

**Flex Pay screen upside down.** Andrei's team assembled a Flex Pay with the screen upside down; their connector only fits one way. Alexander wanted to make a rotated build now. Pavel: wait — the team is at the trade show today and back tomorrow evening. First they must say whether touch works correctly, so we know if only the screen or also the touch must be rotated.

**Device registration and settings (Anton Seregin).** Anton worked on FP-1364 (heard "13 64"), got access to the location (manager), and covered terminal registration. He listed questions to agree on. He proposed reusing the Flex Pay Wi-Fi QR in a common part. Pavel: the Flex Pay QR is temporary — it is scanned only with the door open, by authorized staff in setup. It does not fit Flex IQ (setup by code; an unregistered device has no code and must show a QR to register). Flex-Port has no screen or service mode, so binding it to a location and giving it Wi-Fi details is the hard part. Pavel asked for a careful user flow and a system-wide architecture covering Flex-Port, Flex Pay and Flex IQ, then a joint review with Pavel, Alexander and Irina.

**SAS CRC bug fixed on Flex-Port (Pavel).** Some SAS commands are sent without a CRC, but our code sent a CRC after them. It worked on Aristocrat. IGT and Bally (heard "banila") rejected some requests because they answered before our CRC was sent. Fixed; now stable on all machine types. Cash-in/cash-out was not affected; statistics and meter commands were. Pavel also read statistics from a Bally machine: all games, money in and out, games played. These counters survive a factory reset. Irina: this is the kind of data being asked for. Not in the release; no capabilities or requirements yet (Andrei raised it as a possible market need for later MVPs). Pavel will attach a report on supported SAS commands to Jira.

**Other updates.**
- Alexey Khamin: moving tests to run on hardware through CI. Reviewed Evgeny's PR on the new integration repo. Tested the Flex-Port build from Alekseev's branch and replied to him.
- Evgeny Kharetski: the new integration repo lets only Alexey review, and Evgeny cannot approve his own PR; this slows work. He will ask Andrei to change the rules. Irina suggested moving review to Igor.
- Evgeny also works on AI agents and added tickets.
- Anton Leshkevich: Nebraska 2, and research on cutting RAM use; maybe a small result by the 8:00 meeting.
- Daniil Stauskiy: opening PRs for PNC-4 and NGCO-1 (heard). Two games (Fortune) run on his cabinet; next he loads them on the board to check memory for two games and memory release. Pavel asked to be called to see it today. Daniil moves NGCO-1 from backlog to To Do.
- Irina: rewriting the RIS requirements ("everything is very bad") — all capabilities in the release. Cleaning up port/machine tests, then bill validator connection tests.
- Ivan Shpak: continues on RIS, checking Evgeny's and Sergey's work. Sergey's part is not finished; Irina expects rework after yesterday's discussion.
- Sergey Tsimanov: finishing the passport task today (last scenarios on the stand, commit today), also roles for software updates, then closing the printer task (epic 950 issues confirmed).
- Dmitri Kovalchuk: Pavel should have a draft (heard "draft 1"). He asked Alexander about the Flex IQ / Flex-Port comparison the agent could not find; Alexander said the work is done (see above).
- No-SAS (bill validator) mode: Alexey asked about Jira documentation. Pavel: we want to fully test this mode, so it needs capabilities with proper requirements. Most of it was built a year ago without capabilities; requirements may exist but acceptance criteria are likely outdated. Some autotests will work; some must be written from scratch. Irina will check what Andrei created.

## Decisions Made

- **The Flex-Port mode (SAS or bill validator) is set by a technician from the kiosk, per machine; the missing kiosk-to-port command gets built now, without waiting for Alekseev.** (Pavel Frolov)
- **No rotated Flex Pay build until Andrei's team says whether touch also needs rotation.** (Pavel Frolov)
- **Device registration and settings need one architecture across Flex-Port, Flex Pay and Flex IQ, not a Flex Pay-only reuse of the Wi-Fi QR.** (Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Implement the Flex Pay tasks from the Flex IQ communication comparison | TBD | Normal | 8–10 tasks |
| 2 | [Unassigned — needs clarification] | Build the kiosk-to-Flex-Port command to set SAS / bill validator mode | TBD | High | Alexander offered; has no port access |
| 3 | Alexey Khamin | Re-check whether switching mode on the terminal changes the Flex-Port mode | Oct 21 | Normal | |
| 4 | Alexander Biratko | Make a rotated-screen Flex Pay build once Andrei's team answers about touch | After Oct 22 | Normal | Team at trade show |
| 5 | Evgeny Kharetski | Ask Andrei to change review rules on the new integration repo | Oct 21 | Normal | Blocks PRs |
| 6 | Anton Seregin | Prepare questions, user flow and a system-wide registration/settings architecture; review with Pavel, Alexander, Irina | TBD | Normal | FP-1364 (heard) |
| 7 | Daniil Stauskiy | Load two games on the board, check memory; call Pavel to see; move NGCO-1 (heard) to To Do | Oct 21 | Normal | |
| 8 | Anton Leshkevich | Share RAM-reduction findings | Oct 21, 8:00 AM meeting (maybe) | Normal | |
| 9 | Sergey Tsimanov | Finish and commit the passport task; finish software-update roles; close the printer task | Oct 21 | High | |
| 10 | Irina Shishko | Rewrite RIS requirements; check Jira for existing no-SAS capabilities | TBD | Normal | |
| 11 | Pavel Frolov | Close his in-progress task and attach the supported SAS commands report in Jira | Oct 21 | Normal | |
| 12 | Ivan Shpak | Keep checking Evgeny's and Sergey's RIS work | TBD | Normal | |

## Open Questions

- Who builds the kiosk-to-port mode command? (Alexander)
- Who reviews PRs on the new integration repo — Igor? (Irina)
- Must the Flex Pay touch be rotated with the screen? (Pavel)
- How does a Flex-Port (no screen) get bound to a location and get Wi-Fi details? (Pavel)
- Which no-SAS capabilities exist, and which autotests must be written new? (Alexey, Irina)
- Should third-party machine statistics become a capability? No requirements yet. (Pavel, Irina)

## Dispatch Log

---
*Processed from Teams transcript on October 21, 2026*
*Source meeting: Daily Standup meeting*
