# Meeting Summary — Daily Standup meeting
**Date:** October 5, 2026, 4:54 AM – 5:40 AM Eastern
**Duration:** ~45 minutes
**Attendees:** Pavel Frolov, Alexey Khamin, Irina Shishko, Dzmitry Chudzinau, Sergey Tsimanov, Anton Seregin, Daniil Stauskiy, Evgeny Kharetski, Ivan Shpak, Vladimir Samusenko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026]]

## Summary

Monday standup run by Pavel. Alexander Biratko was absent. Held in Russian.

**Autotest stand debate.** Irina asked what stubs or emulators exist for card tests. Dzmitry: for Payment Hub autotests the team must decide between a real InComm (needs real cards and credentials, even in the sandbox) and a fake InComm (needs an emulator stand). He and Sergey run the full stand locally; it takes 15–20 GB of memory and someone has to manage and rebuild it. Pavel: this is about running autotests locally in the office with a real Flex Port and Flex IQ against a fake environment. His quick option: a Flex IQ build variant that fakes card issuance success or failure; enough for current tests. Irina: that covers today, but bigger checks are coming. Sergey: a separate stand like dev staging is needed. Dzmitry: properly this belongs in the cloud; Pavel disagreed, since local is needed to simulate third-party services; updates can be excluded from autotests. Pavel: this is not MVP1, or everyone will work only on the InComm stand. Agreed: a separate meeting with Andrei.

**Transactional.** Dzmitry closed all Transactional items; now on CAP-141 (enrollment). Part of Lyosha's bugs auto-closed. Pull requests wait on Pavel: FPORT-59 merged; FPORT-94 showed a merge conflict and no approve button until Pavel used the "Files changed" tab. SAS traffic from the machine looks noisy (polling, handpay 51); Pavel agrees it looks abnormal; Evgeny or Ivan to judge. Mockup review next. Dzmitry: a number of MVP1 Port tasks were assigned to Pavel and need triage; one with two SAS channels is not small. Pavel: meet right after the standup at 13:00 Minsk with Dzmitry, Sergey and Irina to go through them.

**Jira automation.** Kovalchuk removed the red highlight of today's date. He wrote four automations: when all child features are Complete, the capability moves to Request Review. Dzmitry: a story added to a completed feature should send the feature back to To Do and the capability to To Do as well; he found open stories hiding inside "done" trees. Irina agreed. Kovalchuk will implement.

**Device verification.** Anton closed FAQ-105 to 108 (reconciliation of printer work). The FlexPay-based task should probably be blocked; only a description exists, nothing to inherit. Printer scenarios (paper jam, printer disconnect) still need a real device; barcode scanner is simpler. He had to emulate location binding for the printer.

**LGS and ARM.** Daniil finished 1486. Pavel: open a branch in both repos (Rage converter and LGS) with the same description. Icons load first, then games; done. Next: run the game on the new ARM board with the select screen and game stubs to measure memory per game.

**Integration repo.** Evgeny integrates CC Talk and writes prose/contracts for the GT integration repo; a new separate IO board service was added; LGS-12-37 now, 12-3-24 next. Pavel's understanding: a manifest of component versions and sources, pulled at build time. Evgeny: later a GitHub Page where you pick release or snapshot versions. Both agree the release must bake a file listing the component versions into the artifact.

**Other.** Khamin fixed test rules, reviewed PRs for new rules, CI/CD at 3 of 5 steps; finishes tests today, one day on prose, tests from October 7. Irina will rework vague wallet-creation requirements. Ivan built a new release, will flash and test, then autotests. Sergey works on reprint at card issue and cut Flex IQ test time to 5 minutes. Vladimir: task 769, screen and text checks. Khamin asked how the terminal emulator stays in sync with main code; Anton: scripts in the repo, default from main, parametrized; Pavel's alternative of attaching an emulator artifact to every Flex IQ build was judged too heavy. "Kiosk" is to be renamed "terminal": fix in Jira and descriptions, leave commits.

## Decisions Made

- **The InComm/autotest stand is not MVP1; a separate meeting with Andrei will decide the design.** — Too big to settle in a standup; cloud vs local disputed. (Decided by Pavel Frolov, Dzmitry Chudzinau)
- **A story added to a Complete feature moves the feature and its capability back to To Do; Kovalchuk automates it.** — Open stories were hiding under done features. (Decided by Irina Shishko, Dzmitry Chudzinau)
- **Release artifacts include a file listing the component versions built in.** — Traceability of releases. (Decided by Evgeny Kharetski, Pavel Frolov)
- **"Kiosk" becomes "terminal" in Jira and descriptions only, not in commits.** — Name carried over from FlexPay. (Decided by Pavel Frolov)
- **Daniil opens a branch in both the Rage converter and LGS repos with one description.** (Decided by Pavel Frolov)
- Considered and superseded: attaching an emulator artifact to every Flex IQ build — dropped as too heavy; Khamin will use the repo scripts instead.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Arrange a separate meeting with Andrei on the autotest/InComm stand | TBD | High | Blocks Payment Hub autotests |
| 2 | Pavel Frolov, Dzmitry Chudzinau, Sergey Tsimanov, Irina Shishko | Meet after the standup (13:00 Minsk) to triage the MVP1 Port tasks assigned to Pavel | 2026-10-05 | High | Includes the two-SAS-channel task |
| 3 | Pavel Frolov | Review FPORT-94 pull request | 2026-10-05 | High | FPORT-59 already merged |
| 4 | Dzmitry Chudzinau | Check the FPORT-94 merge conflict | 2026-10-05 | Normal | |
| 5 | Evgeny Kharetski, Ivan Shpak | Judge whether the SAS polling/handpay 51 traffic is normal | TBD | Normal | Pavel thinks it is not |
| 6 | Dmitri Kovalchuk | Implement the reopen automation (story added → feature and capability to To Do) | TBD | Normal | On top of the four automations written |
| 7 | Alexey Khamin | Finish autotest rules today, one day on prose, start tests | 2026-10-07 | Normal | CI/CD at 3 of 5 steps |
| 8 | Anton Seregin | Verify printer and barcode scanner scenarios on a real device | TBD | Normal | Paper jam, disconnect |
| 9 | Daniil Stauskiy | Open branches in both repos; then run the game with select screen and stubs on the new ARM board | TBD | Normal | Memory measurement |
| 10 | Irina Shishko | Rework the wallet-creation requirements | TBD | Normal | Vague wording |
| 11 | Alexey Khamin | Look at the emulator build scripts and sync the emulator with the main code | TBD | Low | |
| 12 | Anton Seregin | Rename "kiosk" to "terminal" in Jira and descriptions | TBD | Low | |

## Open Questions

- Real vs emulated InComm for autotests, and where the stand lives (local vs cloud). Raised by Dzmitry Chudzinau, Irina Shishko.
- What the two-SAS-channel Port task actually requires. Raised by Dzmitry Chudzinau.
- Whether the FlexPay-based task should be blocked. Raised by Anton Seregin.

## Dispatch Log

---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: Daily Standup meeting*
