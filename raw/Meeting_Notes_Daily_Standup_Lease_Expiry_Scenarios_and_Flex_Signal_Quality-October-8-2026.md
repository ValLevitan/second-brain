# Meeting Summary — Daily Standup meeting
**Date:** October 8, 2026, 4:58 AM – 5:28 AM Eastern
**Duration:** ~28 minutes
**Attendees:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Alexander Biratko, Sergey Tsimanov, Vladimir Samusenko, Ivan Shpak
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026]]

## Summary

Thursday standup run by Pavel. Held in Russian. Some task numbers are garbled in the transcript. Pavel: the October 15 deadline is less than a week away.

**Lease expiry screens.** Irina asked when the "out of service — lease expired" screen shows. Dzmitry: today the server only works with the lease date; there is no way yet to switch off a location. This morning the lease expired on the test terminals and all Flexports stopped. Vladimir: the regulation says an expired lease shows out of service with the reason; a revoked lease shows out of service with no reason; Claude says the code does this. Alexey asked what happens if a terminal is unlinked from its location. Dzmitry: it should be handled but must be checked; Pavel: it shows a different screen. Vladimir sees two scenarios: lease expired (any cause) and terminal unlinked. Dzmitry: he sent the full scenario lists; they must be reviewed with Andrei. Not settled.

**Card dispenser tests.** Alexey's remaining tests involve card dispensers (InComm card issuing). Irina: there are no card dispensers in MVP1; she raised this about 14 days ago and it was never discussed — something must be done or work will stall. Dzmitry: run tests on real hardware, or bring up all transaction services in Docker as one local stand. Pavel: this can be a GitHub action on the internal self-hosted runner. Dzmitry: add a setting to use real InComm or an emulated one. Irina asked Alexey to raise any blocker at once — it is critical.

**Flexport signal quality.** Alexander asked whether Flexport sends its network signal quality to the kiosk. Dzmitry: no. Pavel: Wi-Fi is MVP2; Flexport and Flex IQ need MVP2 tasks to capture and send this data. Alexander named an existing port task (106) and Flex IQ task 1328.

**Version info on QA stories.** Dzmitry asked QA to add the versions used (Flex IQ, port OS, firmware) to every story they open for findings. Pavel: firmware built by the GitHub action has a real version; firmware built by Claude shows zeros. Dzmitry: build through the action.

**Other.**
- Alexander: groomed his tasks (6 in progress) and fixed dates as Dima asked. Works on Wi-Fi and Flexport; moving the port tiles screen.
- Alexey: TIN-61 stays open until the CI run on real hardware can be started by hand. Wanted to close his rules task (76) and open a new one; Irina said no — move it to To Do and add rules as needed.
- Anton: closed the rest of one feature (67); 3 stories need a real terminal, done today if he gets one. Prose and contracts generated, PRs in review; same for Flex Pay; Flex IQ prose and contracts finished yesterday. Set dates on closed items so reports match.
- Daniil: feature 1343 — game installed on the board, low FPS from the processor, investigating. Bugs filed on him are already fixed. On 1057 he wants someone to check visually that the result is right.
- Dzmitry: refactored card activation (fewer hops, faster). Found why a transaction to a machine failed; the machine emulator's SAS needs fixes. Current task F-52 (screens); no gaps found vs. mockups; asked Anton for a couple of edits. Will review traffic logs. Pavel suggested reviewing port firmware; Dzmitry: not before the 15th, maybe next week; Irina: not MVP1.
- Evgeny: working on 1239 (new lease for the old GA COAM). Server-side questions settled yesterday. Could not move the release to Git — the old version depends on Nexus. Fixed a bug where a tab did not show and re-released.
- Irina: autotests TIN-16 and TIN-19 still unwritten; will run tests and fix autotests after rewriting requirements from Dima, herself and Vladimir.
- Ivan: rebuilding the version a third time, hopes it is the last, done today. Then autotest TIN-13. Then the battery: will come for equipment this afternoon. Pavel: the feature may be with Evgeny; a story for the experiment is needed.
- Sergey: printer status task (ticket printing through the port, with a record if not possible). Took log memory optimization after the incident two days ago. Now on the Flex memory leak, FIQ-140.
- Vladimir: on task 62 (a requirement contradiction he raised). Blocked tasks and 42 in progress; others had requirement issues partly resolved yesterday.
- Kovalchuk: watch your dates. For the PM agent: add a glossary of Russian pronunciations of Jira project codes, or the AI will not understand them.

## Decisions Made

- **Alexey's rules task stays open in To Do; rules are added to it as needed, no new tasks for the same work.** (Decided by Irina Shishko)
- **Port firmware review is not MVP1.** (Irina Shishko, Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | [Unassigned — needs clarification] | Create MVP2 tasks for Flexport and Flex IQ to capture and send signal quality | TBD | Normal | Pavel asked; port task 106, Flex IQ 1328 |
| 2 | Alexey Khamin | Make CI run on real hardware start by hand; raise blockers to Irina at once | Oct 15 | High | TIN-61 |
| 3 | Alexey Khamin | Move rules task 76 to To Do | TBD | Low | |
| 4 | Anton Seregin | Run the 3 remaining stories on a real terminal | Oct 8 | Normal | If a terminal is free |
| 5 | Anton Seregin | Make a couple of edits for Dzmitry's screen task F-52 | TBD | Normal | |
| 6 | Daniil Stauskiy | Fix low FPS on the board for feature 1343 | TBD | Normal | |
| 7 | Dzmitry Chudzinau | Fix the machine emulator SAS; review traffic logs | TBD | Normal | |
| 8 | Dzmitry Chudzinau, Andrei | Review lease and location scenarios against requirements | TBD | Normal | |
| 9 | QA team | Add Flex IQ, port OS and firmware versions to every finding story | Ongoing | Normal | |
| 10 | Irina Shishko | Run tests; fix autotests after requirement rewrite | TBD | Normal | TIN-16, TIN-19 |
| 11 | Ivan Shpak | Finish the rebuild; then TIN-13; then battery work | Oct 8 | Normal | |
| 12 | Sergey Tsimanov | Fix the Flex memory leak | TBD | Normal | FIQ-140 |
| 13 | Vladimir Samusenko | Clear task 62 and the blocked tasks as requirements are fixed | TBD | Normal | |
| 14 | [Unassigned — needs clarification] | Add a glossary of Russian pronunciations of Jira project codes for the PM agent | TBD | Normal | Kovalchuk |

## Open Questions

- How should MVP1 tests that touch card dispensers / InComm run, when MVP1 has no card dispensers? Raised ~14 days ago, still not discussed. (Irina Shishko, Alexey Khamin)
- Which out-of-service screens show for lease expired, lease revoked, and terminal unlinked from its location? (Irina Shishko, Alexey Khamin)

## Dispatch Log

---
*Processed from Teams transcript on October 8, 2026*
*Source meeting: Daily Standup meeting*
