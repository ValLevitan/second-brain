# Meeting Summary — Daily Standup meeting
**Date:** November 20, 2026, ~3:44 AM – ~4:34 AM Eastern (recording)
**Duration:** ~50 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Andrei Bosik, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko, Emma (AI-PM bot)
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026]]

## Summary

**Flex-Port firmware update failure.** Andrei Bosik asked whether Flex-Port should show an error on its own screen when a firmware update fails. Pavel: the port has two boot slots; it writes the new firmware to the second slot and switches only after the check passes. Alexey: if something goes wrong it silently stays on the old version. Sergey and Andrei had heard there is not enough space to roll back; Pavel asked to confirm with Evgeny (the board also has a button that may switch the slot; nobody has tested it). Irina: if the port is back on a working version, there is no place to show the player an error. Agreed: no error on the Flex-Port screen; the error stays in the terminal log and the operations dashboard. Pavel: acceptance criteria were written without knowing the real implementation and must be reviewed.

**Autotests that cannot be automated.** Vladimir: about 10 of ~23 scenarios on his Wi-Fi capability need real hardware (QR scanner, USB modem). Flex-Port has a command that simulates a scan, and some tests already use it. Agreed: mark such acceptance criteria as manual only, create a separate feature with the list to check by hand, and keep these tests in the repository so one filter finds them (Alexey; Irina says manual tests also go into Jira as test type).

**Wi-Fi test machines.** Machine 84 has no working Wi-Fi module; 82 is a demo machine. A spare board exists (83 is with Anton); swapping it into 84 gives two full IQ units with Wi-Fi. Irina will sort it out.

**Capability housekeeping.** Pavel moved all of Anton's MVP 1 requirements to request review and assigned them to Irina; she should delete inadequate or duplicate ones. Andrei Bosik will delete capabilities that are no longer relevant (tests already moved) — Irina: delete, not archive. Sergey's new item "ot-10" (for Anton's question) should not sit in 2.1 without a capability; Irina will move it. Andrei's MVP 3 Wi-Fi screen question was parked — focus now is 2.1 and 2.2 only.

**Release notes on the operations dashboard.** Andrei Bosik: production artifacts (terminal and Flex-Port firmware) should carry release notes (.md) that can be viewed or downloaded. Pavel asked Emma to create a capability for this; not for this release.

**Docker dev images.** Andrei Bosik asked everyone who builds Docker dev images in GitHub Actions to add a clean-up step so old images do not pile up (keep the last 1–3).

**Status by person:**
- **Alexander:** working through Andrei K's new recycler screen requirements (REQ-84 to REQ-107); MVP 1 not closed — the closing meeting did not happen because Andrei K has no recycler to test on.
- **Alexey:** hardware tests; Val's task to automate turning laws into requirements — repo and Jira project exist; will create a task.
- **Anton S:** items on 20; checking SAS updates; can work Saturday, half day (Irina has work for him; Vladimir is overloaded).
- **Daniil:** machine-state messages; sound library to the new engine; needs a task for the machine-state work.
- **Dzmitry:** closed two screen stories; SIM card task works on terminal 80, finishing the unregistered-terminal case; reviewing 2.1 and 2.2. Pavel: sort the MVP 2 capabilities first.
- **Evgeny:** game ISO builds ready to try; the shared build machine is full (.claude folder ~30 GB plus ~90 GB of other files) — asked Pavel to clean it.
- **Igor M:** set up CI for games (x86 first, ARM later); Nebraska.
- **Irina:** RIS review, then autotests and 2.1 capabilities. Reminder to all: do not rely only on Claude — read features, requirements and acceptance criteria yourself.
- **Ivan:** RIS battery issue found by Felipe; will write stories for Evgeny and Sergey (about ten RIS comments, urgent).
- **Sergey:** reviewing 2.1; next task: port–terminal statistics (feature 224).
- **Vladimir:** split cloud tests into new TINT items; 117 merging (asked Anton to review); blocked on Wi-Fi tests.

**Standup length.** Igor M said the standup runs almost an hour. Irina: the standup should be about what will be done next, not reports of what was done.

**Emma's voice.** Andrei Bosik: Emma uses a text-to-speech service with a Bulgarian voice model, the only one that speaks both Russian and English.

## Decisions Made

- **Failed firmware update is not shown on the Flex-Port screen; it stays in the terminal log and operations dashboard.** — The port falls back to the working version, so there is nowhere useful to show it. (Andrei Bosik, Irina)
- **Hardware-only test scenarios: mark acceptance criteria as manual, put them in a separate manual-check feature, keep them in the repository.** — About 10 of 23 Wi-Fi scenarios cannot be automated. (Pavel, Irina, Alexey)
- **Obsolete capabilities are deleted, not archived.** (Irina)
- **Release-notes viewing on the operations dashboard becomes a capability (not this release).** (Pavel, via Emma)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Clean the shared build machine disk (.claude folder and other files) | TBD | High | Blocks Evgeny's ISO tests |
| 2 | "Evgeny" (likely Evgeniy Alekseev, Flex-Port firmware — [Needs Val's confirmation]) | Confirm how Flex-Port firmware rollback really works (slots, space, board button) | TBD | Normal | Pavel asked to check with Evgeny; not in the call |
| 3 | Andrei Bosik | Remove the on-screen update error from the requirement | TBD | Normal | |
| 4 | Andrei Bosik | Delete obsolete capabilities | TBD | Low | Tests already moved |
| 5 | Irina Shishko | Move Sergey's "ot-10" item out of 2.1 | Nov 20 | Normal | |
| 6 | Irina Shishko | Sort out a Wi-Fi-capable IQ for tests (swap spare board into 84) | TBD | High | Vladimir blocked |
| 7 | Irina Shishko | Review Anton's requirements in request review; delete bad or duplicate ones | TBD | Normal | |
| 8 | Vladimir Samusenko | Mark non-automatable scenarios as manual and list them in a separate feature | TBD | Normal | |
| 9 | Dzmitry Chudzinau | Sort MVP 2 capabilities; find items that belong to him | TBD | Normal | |
| 10 | Daniil Stauskiy | Create a task for the machine-state work | TBD | Low | |
| 11 | Alexey Khamin | Create a Jira task for the laws-to-requirements automation | TBD | Low | |
| 12 | Ivan Shpak | Write RIS stories for Evgeny and Sergey | TBD | High | Irina: urgent |
| 13 | Anton Seregin | Work Saturday (half day) on tasks from Irina | Nov 21 | Normal | |
| 14 | All who build Docker dev images | Add an image clean-up step to GitHub Actions | TBD | Low | |

## Open Questions

- Does Flex-Port really have room to roll back, and what does the board button do? (Pavel)
- Andrei Bosik's MVP 3 question: do terminals need on-screen Wi-Fi network selection? Parked for a separate meeting. (Irina, Pavel)

## Dispatch Log

---
*Processed from Teams transcript on November 20, 2026, ~10:40 PM Eastern*
*Source meeting: Daily Standup meeting*
