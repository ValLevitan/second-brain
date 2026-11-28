# Meeting Summary — Nova standup meeting
**Date:** November 24, 2026, 6:16 AM Eastern
**Duration:** 26 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Evgeny Kharetski, Anton Leshkevich, Igor Metelski, Daniil Stauskiy
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Nova_Standup_Bonus_Step_Templates_and_LGS_Statistics_Database-November-24-2026]]

## Summary

**Studio pipeline (Anton).** Anton built the pipeline step that builds the base game (reels, background and so on). Today he tests it and makes the changes from review. If he finishes, he moves to the installer and then thinks about auto-updates for the app.

**Bonus game step.** Alexander asked how the bonus step will work, since bonus games differ a lot. Anton: most likely a template that supports general features. He has not worked it out in detail. He does not want AI to generate all of it. Igor: they already built a bonus with a new mechanic. The brief holds the bonus screen and mechanic needs. The bonus is made on template scenes first and then the resources are converted by the contracts. The transition and the end message should be made in the same step. Alexander proposed more general steps ("create resource", "create scene" from a set of templates). Anton and Pavel: later. Now it would only slow the work. Pavel: 80/20, pick the low apples first.

**Engine and LGS (Daniil).** His pull request in the library is green; Anton told him to merge it himself. He and Alexander agreed how machine state will pass between the engine and LGS (task heard as LGS-1353). Texture format for the new engine: most likely WebP. Only WebP and PNG are supported now. Anton will check and write to Daniil. A speed comparison of formats waits until speed becomes a problem.

**Games (Igor).** Agents fixed games all day yesterday. He has four games (names as heard: Twin Bison, one unclear, Carnival, Sapphire Star). They come from different products with different progressives. His LGS cannot run them this way, so he waits for the LGS fixes.

**LGS (Evgeny).** LGS fixes are running; there are 300+ commits on top. He needs a repository for each of the four games, all following the same contract as the first one. Igor will ask for the repositories and upload the games. Evgeny also moves services to the new architecture. Yesterday the team decided the studio does not need LGS; games run on mocks. So he is making a container build where a real LGS runs in simulation mode, without bill validators, for testing new game logic.

**Firmware packages (Pavel).** Pavel is finishing the build so it gives ready firmware update packages that work on RK boards.

**Jira and LGS statistics (Alexander).** He renamed NOVA-2 to NOVA in Jira, about 300 edits, and fixed old "Omni" names. With Evgeny he discussed new LGS capabilities: collect statistics, keep them long term in a database on the machine, and send them to the hub. What to collect must still be discussed with Efim. LGS should move to a more modern base such as Spring; Evgeny will analyze it. Storage would become a fast buffer, with data written to the database in batches. Pavel raised two points: the design should allow an SSD, and it must not break GLI-11 rules on where history is kept. Idea: give GLI-11 and the code to Claude to check. For games removed from a machine, history could stay in an "archive" tab; screenshots could come from a cloud service.

**RK installer build.** It will be built in the same repository; the builder picks the platform. Evgeny says his side is about ready and he needs Pavel's go. If Igor delivers the game repositories first, Evgeny can already build a multigame for the current platform.

**Transcripts.** Evgeny noted that Claude with the Microsoft 365 connector reads Teams transcripts directly.

## Decisions Made

- **Bonus step: use templates and the step-by-step slot tool now. The more general "resource and scene" approach comes later.** — It would slow the work now. (Decided by Anton and Pavel)
- **Texture format speed analysis is done only if speed becomes a problem.** (Decided by Igor; no objection)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Test the base-game pipeline step and make the review changes | Nov 24, 2026 | High | Then installer, then auto-updates |
| 2 | Anton Leshkevich | Check the texture format for the new engine and write to Daniil | Nov 24, 2026 | Normal | After the meeting |
| 3 | Daniil Stauskiy | Merge his green pull request in the library | TBD | Normal | Anton: merge it yourself |
| 4 | Igor Metelski | Ask for repositories for all four games and upload them, same contract as the first game | TBD | High | Evgeny needs them for testing |
| 5 | Evgeny Kharetski | Finish the LGS fixes and the container build with LGS in simulation mode | TBD | High | |
| 6 | Evgeny Kharetski | Analyze moving LGS to Spring or similar | TBD | Normal | |
| 7 | Alexander Biratko | Create the requirements and capabilities for LGS statistics, the database and the history archive; discuss the statistics list with Efim | TBD | Normal | |
| 8 | [Unassigned — needs clarification] | Check the storage and history plan against GLI-11 with Claude | TBD | Normal | Evgeny offered; Alexander said "we will analyze" |
| 9 | Pavel Frolov | Tell Evgeny when everything is ready for the RK installer build | TBD | Normal | |
| 10 | Daniil Stauskiy | Take the demo mode menu task | TBD | Normal | Assigned by Alexander |

## Open Questions

- Does keeping history in a database on a replaceable disk fit GLI-11? (Pavel)
- Must history stay available after a game is removed from the machine? (Alexander)
- Game names and task numbers were heard unclearly in the transcript (one of Igor's four games; "LGS-1353"; platform names "F7 / 1000").

## Dispatch Log

---
*Processed from Teams transcript on November 24, 2026, ~6:25 PM Eastern*
*Source meeting: Nova standup meeting*
