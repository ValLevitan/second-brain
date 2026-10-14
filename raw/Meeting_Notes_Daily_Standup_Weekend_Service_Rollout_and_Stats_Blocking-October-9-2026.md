# Meeting Summary — Daily Standup meeting
**Date:** October 9, 2026, 4:46 AM – 5:22 AM Eastern
**Duration:** ~36 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Alexander Biratko, Sergey Tsimanov, Vladimir Samusenko, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026]]

## Summary

Friday standup run by Pavel. Held in Russian. Some task numbers and phrases are garbled in the transcript.

**Weekend rollout of web services.** Pavel said they must likely push Elizabeth today to install software on Flexport and Flex IQ. Dzmitry: with the weekend coming, roll out all web services now. Today everything runs only on dev stacks; do not wait for the last moment when Elizabeth starts bringing things up. Pavel agreed: "it is time." Dzmitry may bring up the terminal over the weekend and check it connects, maybe with a payout. Dzmitry asked that the bot not create a task for this.

**Statistics host blocked again.** Dzmitry: machines now ship to Georgia with modems and will send statistics. A machine from the Minsk office again spammed the host with data. This blocks statistics for everyone; someone must stop and clean it by hand. Causes vary: games not yet added on prod, or the installed software does not match the registration. Sergey: a mechanism already drops statistics from unregistered machines; how do we tell a test machine that is registered? He said a spot fix will not remove all problems. Pavel: if one machine's data in a packet stops processing for everyone, drop that packet rather than stop all processing. Some push message should also say which machine's data failed to parse. Sergey: the chain is not simple — on a server error the data is marked unsent and sent again. Dzmitry: they must think of a fix so nobody does this by hand. Pavel: a task is needed. No solution chosen. Dzmitry: the old accounting server will live about one more year, so it needs real work.

**Test plan to October 15.** Pavel: tests should mostly close by the 15th. Irina: maybe 80%. Vladimir: some tests are hard; TIN-56 needs the cloud (update delivery), maybe half can be done. Irina: that one is not MVP1 (it sits on capability 122), nothing cloud was built. Pavel: use 80/20 — close the main functions first, leave rare and complex ones to the last day. Dzmitry: favor tests tied to the port, machine and IQ, because servers can deploy at any time and devices are harder. Alexey: then there are no automatic runs, no emulators and no automatic environment setup.

**Cloud test meeting today.** Pavel set a meeting at 12:45 (time zone not stated) right after the standup. Topic: how to run automated tests that use cloud services, especially payment services. This likely needs an environment that can be controlled to emulate errors from the other side. Dzmitry asked to invite everyone interested.

**SAS connector.** Pavel, for information: Gennady and Alexey routed SAS on the Flexport board to small black 4-pin connectors. All ports now use DB9 for SAS. A release must fix one option. Pavel will talk to Gennady today. He prefers DB9 because it is standard and likely on all machines; the other needs a special cable.

**PM agent.** Dmitri Kovalchuk: the PM agent (called "Dasha" for now) runs in test mode; tasks may appear in the test project. Planned production start Monday, if all is ready. Pavel: daily email reports will list each person's tasks. Dmitri: tasks will have status "draft"; each must be accepted or rejected, likely with a link to the meeting where it was discussed.

**Other.**
- Alexander: finished capability 133 (validator). Finishing 143 (Wi-Fi), testing on the stand. Next: capability 117 (card checks on Payment Hub, card issue through the card dispenser); many card dispenser tasks still open. Writing prose for his repo. His old updater repo is not used in Flex IQ or Flex Pay. USB update still works through RAUC; he tested it on Flex Pay hardware. Full reinstall is by micro SD. Pavel: archive the repo; Alexander will ask Andrei.
- Alexey: CI on real hardware still cannot be set up so tests run. Working on TIN-76 (rules). Asked when it is decided how services come up for autotests.
- Anton: made emulator task 146 (set PIN codes and serials for technicians). Now on 147, so the emulator can run the terminal in emulator mode against real services (registration, card operations). Plans to close today.
- Daniil: bug 1057 almost fixed; commit and PR today. Feature 1343: the board has no hardware VP8 decoder; most game videos are VP8. The select screen has 11 videos with alpha; the processor decodes alpha at about 20 FPS. He will try re-encoding to VP9 with alpha for the select screen only. Pavel: try it; AI may help add alpha.
- Dzmitry: closed all old MVP1 features; added sounds and rolled them out. On real dev InComm, Payment Hub sometimes gives odd answers: no card issued, "suspect" status, answer only after ~30 minutes, and funds frozen on the wallet meanwhile. Possibly a partial product code match. He will investigate. A terminal stuck in a screen state it could not leave after 84 autotests (race when switching apps); he may add a watchdog to return to a valid screen. Suspects Irina's Flexport issue comes from the SAS emulator, which has many mismatches; will fix, today or tomorrow; working autotests may break. Machine does not keep the lease after reboot (Cortez reported); server side is correct; he will check what software the machine runs.
- Evgeny: on 1238 (lease work for the old software). Server side is Sergey's task (contract described). Pavel offered him next: option to use the old RIS saved on the hard disk at factory reset; it is planned but not scheduled. Evgeny does not load his plan far ahead because priorities change.
- Irina: one test blocked by TIN-19 (Dzmitry to check). TIN-16 she will split per the MVP2 talk, then close. Next maybe 17 and 18. Asked Vladimir why 769 is a blocker: the credit screen requirement (1813) — design has 33 screens, 32 seem needed.
- Ivan: found the machine they worked on; will create and send the installation. Closed one TIN yesterday; TIN-11 test in progress; looking at 1250; then the battery. Last night helped Elizabeth get SAS working with the SAS test tool (link up, pings). Pavel: she had to ship 10 machines today, so likely did nothing else; tell her no updates on Fords for now.
- Sergey: finished memory optimization; added a separate process for remaining-memory stats. Last task: on fatal cases (e.g. printer driver unpack fail, out of memory) show a clear critical error with a description in the stats, and go out of service. Pavel: also the lease tasks for Evgeny's project — allow a machine to apply the lease code even if the person did not scan all statistics. Urgent; done by middle of next week.
- Vladimir: closed autotests 42, 23 and 62; TIN-21 sent to Alexey for review. On 73: unsure if blocked (Payment Hub link during the operation); checking the current version. Needs a version stub in the emulator; may add it himself and send to Anton for review. Then TIN-30, 60 and 70.

## Decisions Made

- **Roll out all web services now, before the weekend, instead of waiting for Elizabeth.** — services run only on dev stacks today. (Proposed by Dzmitry Chudzinau, agreed by Pavel Frolov)
- **Archive Alexander's old updater repository.** — not used in Flex IQ or Flex Pay; USB update works through RAUC. (Decided by Pavel Frolov)
- **Test work to October 15 follows 80/20: close main functions first, leave rare and complex tests for last; favor port, machine and IQ tests over cloud.** — servers can deploy any time. (Pavel Frolov, Dzmitry Chudzinau)
- **Meeting at 12:45 today on how to test with cloud services; open to all interested.** (Decided by Pavel Frolov)
- **A task is needed so one machine's bad statistics no longer block everyone.** — fix method not chosen. (Pavel Frolov, Dzmitry Chudzinau)
- **Lease task (apply lease code without full statistics scan) is urgent, due middle of next week.** (Decided by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | [Unassigned — needs clarification] | Roll out all web services; push Elizabeth to install software on Flexport and Flex IQ | Oct 9, 2026 | High | Before weekend |
| 2 | Dzmitry Chudzinau | Bring up the terminal over the weekend and check it connects (maybe a payout) | Oct 11, 2026 | Normal | "May" — tentative |
| 3 | Pavel Frolov | Set the 12:45 meeting on cloud-service test environment; invite all interested | Oct 9, 2026 | High | |
| 4 | Pavel Frolov | Talk to Gennady about SAS connector (DB9 vs 4-pin) | Oct 9, 2026 | Normal | |
| 5 | Alexander Biratko | Ask Andrei to archive the old updater repo | TBD | Low | |
| 6 | Alexander Biratko | Finish capability 143; start 117; close open card dispenser tasks | TBD | Normal | |
| 7 | Anton Seregin | Finish emulator task 147 (terminal in emulator mode) | Oct 9, 2026 | Normal | |
| 8 | Daniil Stauskiy | Commit and open PR for bug 1057 | Oct 9, 2026 | Normal | |
| 9 | Daniil Stauskiy | Try VP9 with alpha for select-screen videos | TBD | Normal | Feature 1343 |
| 10 | Dzmitry Chudzinau | Investigate odd Payment Hub / InComm answers and wallet holds | TBD | Normal | |
| 11 | Dzmitry Chudzinau | Fix SAS emulator mismatches | Oct 9–10, 2026 | Normal | May break autotests |
| 12 | Dzmitry Chudzinau | Check what software the machine runs (lease lost after reboot) | TBD | Normal | Cortez report |
| 13 | Dzmitry Chudzinau | Look at TIN-19 blocker; maybe add screen watchdog | TBD | Normal | |
| 14 | [Unassigned — needs clarification] | Create task to stop bad machine statistics blocking the host | TBD | High | |
| 15 | Sergey Tsimanov | Lease task: allow lease code without full statistics scan | ~Oct 14, 2026 [Needs Val's confirmation] | High | "Middle of next week" |
| 16 | Sergey Tsimanov | Finish fatal-error handling (critical error, out of service) | TBD | Normal | |
| 17 | Irina Shishko | Split TIN-16 and close; check requirement 1813 / 769 (33 vs 32 screens) | TBD | Normal | |
| 18 | Ivan Shpak | Create and send the installation; continue TIN-11, 1250, then battery | TBD | Normal | |
| 19 | [Unassigned — needs clarification] | Tell Elizabeth: no updates on Fords for now | TBD | Normal | Pavel |
| 20 | Vladimir Samusenko | Add emulator version stub (review by Anton); then TIN-30, 60, 70 | Oct 9, 2026 | Normal | "By evening" — review or blockers |
| 21 | Dmitri Kovalchuk | Start PM agent "Dasha" in production | Oct 12, 2026 | Normal | If ready |

## Open Questions

- How will one machine's bad statistics stop blocking the host? How to identify a registered test machine? (Sergey Tsimanov, Dzmitry Chudzinau)
- Which SAS connector goes in the release: DB9 or the 4-pin connector? (Pavel Frolov)
- How to run automated tests that use cloud and payment services? For the 12:45 meeting. (Pavel Frolov, Alexey Khamin)
- Is requirement 1813 / test 769 a bug or a requirement error (33 vs 32 screens)? (Vladimir Samusenko, Irina Shishko)
- Why does Payment Hub on dev InComm sometimes not issue a card and answer late? (Dzmitry Chudzinau)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: Daily Standup meeting*
