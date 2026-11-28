# Meeting Summary — Nova standup meeting
**Date:** November 26, 2026, 6:28 AM Eastern
**Duration:** 19 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Igor Metelski, Irina Shishko, Evgeny Kharetski, Anton Leshkevich
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Nova_Standup_Faster_Game_Loading_and_Efim_Progressive_Parameters-November-26-2026]]

## Summary

**Faster game loading (Igor).** All games cannot stay in memory at once. Before, a game took 10–12 seconds on the loading screen after it was picked. Igor changed this: it now loads in about 2 seconds. Shared resources stay in memory all the time. He also added touch support. He wants to try several games on a machine with touch.

**Testing on a machine.** Evgeny has an ISO with 3 games ready. The current stand has no touch panel. Plan (Pavel): Evgeny installs it on the existing stand (about 22 minutes), then the same flash drive goes into another machine to check touch. Irina has two vertical machines behind her for such tests. Pavel also wants one more movable vertical machine, with a stand on wheels to be bought.

**Tests and Igor's workload.** Irina asked how much work Igor has before he can write the tests Alexander wants. Alexander: Igor first gets tasks from the requirements Alexander made; tests after. Irina: we will not reach tests soon; not enough people. Evgeny: the new integration repository is ready for integration tests, with the SAS tool connected, so SAS and LGS tests can be written. Alexander's student comes in mid-December. Pavel: even just creating test tasks for features helps. Irina asked to wait until Monday.

**Tagged autotests (Evgeny).** Evgeny will have Claude list what the integration repository and other repositories need for autotests. Idea: each pull request in any component gets a test tag, and the integration repository runs only the tagged tests, not all of them (a full run could take 2 hours). Alexander reviews it, then it becomes a task.

**Progressive parameters and Efim.** The question is how to pass progressive settings to the math of the games that need them. Before, a flag in the game made it ask for the settings and pass them on. Now LGS must pass them when it starts a game, but only where needed, and LGS does not know where. Evgeny proposed sending them to every game; Efim did it his own way. Evgeny built his ISO without that game for now. Igor: best to ask the math itself. Pavel: the math should answer "who are you, which version, which games, which parameter template". Evgeny has no access to the math code; Pavel has. Pavel ran a Claude query: the math gives very little information about itself; contracts exist. Evgeny and Alexander: Efim should extend the API; if he will not, the team adds it.

**Efim and match-3 math.** Irina: Efim told her he heard about the NOVA match-3 math for the first time. Evgeny and Alexander got the same answer. Igor: he asked Efim more than a week ago; Efim said it was not ready. Evgeny: Efim has now delivered it in the last build, but it needs his new approach, which the team does not agree with.

**Meeting with Efim.** A meeting of about 45 minutes, about an hour after the standup. Attendees: Alexander, Evgeny, Pavel, Anton, Igor; Irina optional. Topics: the math API, how to rebuild math quickly for one game for debugging (Pavel), and an MCP for the math (Anton).

**Studio and LFS (Anton).** Anton is adding a way to run a game straight from the studio; it is partly done. Some LFS files were never pushed (they stayed on Igor's and Anton's computers), so Alexander could not check out the engine and framework. Anton uploaded them from his laptop and added guards that check the files are present. Goal for the end of the week: run a game from the brief.

## Decisions Made

- **Test Evgeny's 3-game ISO on the existing stand now, then move the flash drive to a touch machine.** — Fastest way to check, no hardware rebuild. (Pavel)
- **Hold a meeting with Efim today on progressive parameters and the math API.** — The team disagrees with Efim's approach; LGS cannot know which games need the settings. (Alexander, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Install the 3-game ISO on the stand, then test the same drive on a touch machine | Nov 26, 2026 | High | |
| 2 | Pavel Frolov | Set up the meeting with Efim (about 45 min, about an hour after the standup) | Nov 26, 2026 | High | Alexander asked Pavel to create it |
| 3 | Alexander Biratko | Discuss progressive parameters and the math API with Efim | Nov 26, 2026 | High | |
| 4 | Pavel Frolov | Build another movable vertical test machine (buy a stand on wheels) | TBD | Low | |
| 5 | Evgeny Kharetski | Have Claude list what repositories need for tagged autotests; give it to Alexander to review; make a task | TBD | Normal | |
| 6 | Anton Leshkevich | Run a game from the brief in the studio | Nov 27, 2026 | Normal | "End of the week" |
| 7 | Irina Shishko | Plan test tasks | Nov 30, 2026 | Low | "After Monday" |

## Open Questions

- How LGS will know which games need progressive parameters. To settle with Efim.
- Whether the team adds the math info API itself if Efim declines.
- Terms heard unclearly: "вы 1000" (machine to test on), "твинбайзен" (game name), "на компьютер Андрея не забудь" (Evgeny to Pavel, context unclear).

## Dispatch Log

---
*Processed from Teams transcript on November 26, 2026, ~10:00 AM Eastern*
*Source meeting: Nova standup meeting*
