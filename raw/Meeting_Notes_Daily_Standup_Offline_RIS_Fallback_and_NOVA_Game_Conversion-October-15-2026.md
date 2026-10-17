# Meeting Summary — Daily Standup meeting
**Date:** October 15, 2026, 4:46 AM – 5:37 AM Eastern
**Duration:** ~51 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026]]

## Summary

Held in Russian. Dzmitry Chudzinau is on vacation.

**Offline RIS fallback (open).** Sergey works on task BB 3522 and will rewrite 3521 for the case where a machine boots with no RIS and asks the server for its RIS and bank configuration. If the machine's software does not match the last installation on the server, the server returns an error, as before. Evgeny's new machine-side plan: if there is no network, or the server refuses, the user may pick a previously saved RIS. Evgeny said there is no limit on how many are saved. Pavel thinks the last one is enough. Irina said this must be discussed again from the machine side, or conflicts will start. **Pavel moved it to a separate meeting after lunch.**

**NOVA game conversion.** Anton Leshkevich used Igor's tools to start converting Clover Fortune (from the 22 Megahit set; name confirmed by Val 2026-10-15). The horizontal layout already runs on the new platform. Efim added the game to the math server that GLI is looking at, so it runs on real data; some symbols are still simulated wrong. Vertical is next; he expects to finish by end of week. He commits the work but has no task yet. **Pavel: under capability 240 (NOVA migration) create one feature per game**, like the Dragon Pays conversion. Igor: Dragon Pays is universal — the cabinet type in the URL picks the resources. Dragon Pays vertical may not be merged to main yet.

**Designer tasks and NAD 2.** Designers are making many resources under tasks labelled NOVA. Igor thinks they are mixed up: they look like current NAD 2 games, not Dakota. Someone must sort this out with the designers. Igor reminded the team that the data center still needs NAD 2 product-code support (now still GKM2), and progressives for Nebraska (heard as Jackpot Rush, Safari Link, Machete, and a fourth "NA4" Nebraska) may need controller changes. **Pavel: tasks for the AI PM — one for NAD 2 product code in the data center, one for the Nebraska progressives.** Igor: NAD 2 is not a priority; it is needed closer to release, and most designer games are not ready (work runs to end of autumn). Evgeny can do it in parallel. Bet-button changes per game also need checking.

**Alexander.** Closed a task. Capability 135 is open only for the IO board update. Pavel: no rule forbids updating firmware on the fly for the payment terminal, so support IO board updates together with Flex Pay and Flex IQ firmware, if the boards allow it. Current board is the standard one (heard as "M08 40 08"). The requirement exists (task "135 Update") but Claude keeps asking which board and other questions. Pavel: the task exists; it needs refining and the questions answered. He continues capability 116 through the terminal hub (registration, re-registration, completion).

**Alexey.** Continues CI for tests on real hardware. A feature must be created under capability 242 to run scenario tests on hardware through the runner; he said this yesterday but the AI agent did not create it. Dmitri: to make the agent create something, address it directly; it ignores anything below the 0.80 confidence threshold, and calling it "Dasha" does not work. Evgeny Alekseev's FlexPort branch (new memory chips) does not build on GitHub. **Pavel: branch from fresh main and pull his changes in.** Irina was unhappy that Alekseev delivered on the night of the 15th and said "test it". Alexey built and installed the production FlexPort firmware: cash-out and credit both work; a few tests remain. Ivan checks that ports are closed.

**Ticket contact number.** Alexey: on the GALAXY pay site, location setup has contact numbers. Andrei or Elizabeth may have used their own mobiles, which would print on every e-wallet ticket. Sergey: the number comes from the customer location service; one number is optional; empty means nothing prints. Only the customer can change it after setup. Pavel: tell Andrei this field is the contact person who gets called when there is a problem.

**FlexPort test build.** Pavel put FlexPort 100, 120, 128, 130 and 117 in one experimental build. Irina: 117 passed, so it can be merged. Ivan and Vladimir are still running the rest. Ivan: Claude found no direct network access to the production firmware (checked about 65,000 ports); he will try himself. Pavel expects 128 to fail; extra debug was added to collect more data. Irina asked Ivan to move that test feature to Blocked.

**Anton Seregin.** Closed RUKA 3568-29 (USB stick loading) and split out the installer. A boot-order change sits in a PR, not applied: his board's SD card does not work, and Claude warned it might not boot. Scanner scenarios passed; printer scenarios in progress. Claude wrote a scenario where a ticket not taken within about 10 minutes becomes invalid. Nobody knows this rule; Irina: ask Claude where it came from. Printing a ticket then a receipt shows odd timeouts.

**Daniil.** Merged his branch; moved to the new Pixi version. Continues on performance and memory leaks. His "NE1" task does not show on the board; Dmitri is adding filters.

**Evgeny.** Checked the battery: works; new event added when the battery is replaced. He returned the plan to Ivan for a hands-on check. Next is LGS 1243 (heard as "LGS … isation"), front and back end.

**Irina.** Aims to bring autotests to 90% today; only 4 features are untouched. TIN 88 (date Oct 12) is not in MVP1 and should be removed.

**Vladimir.** TIN 32 closed. 71 and 72 out of Blocked with port fixes. 27 waits for review. 33 has questions on how the terminal and port reach the network; he will ask Pavel. Then 57, 63, 56. 56 is not MVP1 — at least remove the Oct 15 date.

**Test approach.** Anton Leshkevich asked if tests are scripts or agents. Pavel: scripts — Claude tests well, but results are not repeatable or kept. Alexey: Claude runs on every PR would cost too many tokens. Irina: keep committed tests and let Claude write them. Igor suggested a separate talk on Claude-run test scenarios.

**AI PM digest.** Dmitri read yesterday's decisions, now added as Jira comments: MVP1 moves to Nov 8–9 (comment on AIP-744); Ivan rebuilds FlexPort firmware with latest commits; Alexander sets a start date on FP 1209. The agent records decisions as comments, not tasks. Daniil: the decision for "NC1" may not fit — video decode settings are at browser/GStreamer level per board, not in that code.

## Decisions Made

- **Remote/offline RIS fallback (how many saved RIS on the machine) goes to a separate meeting after lunch.** — machine and server views differ. (Decided by Pavel Frolov, with Irina Shishko)
- **Support IO board firmware updates together with Flex Pay and Flex IQ firmware.** — no rule against on-the-fly updates for the payment terminal. (Decided by Pavel Frolov)
- **Alekseev's FlexPort memory-chip work: branch from fresh main and pull his changes in.** (Decided by Pavel Frolov)
- **FlexPort 117 passed and can be merged.** (Decided by Pavel Frolov, on Irina Shishko's test)
- **NOVA conversions: one feature per game under capability 240.** (Decided by Pavel Frolov)
- **NAD 2 data center support is not a priority now.** (Igor Metelski; Evgeny Kharetski agreed)
- **TIN 88 comes out of MVP1.** (Irina Shishko)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov, Irina Shishko, Sergey Tsimanov, Evgeny Kharetski | Meet on offline RIS fallback: how many saved RIS the machine keeps | Oct 15, 2026 (after lunch) | High | |
| 2 | Sergey Tsimanov | Rewrite BB 3521 for RIS/bank-config pull when no RIS is on the machine; adjust 3520 | TBD | Normal | |
| 3 | Alexander Biratko | Refine capability 135 IO board update task and answer Claude's questions | TBD | Normal | |
| 4 | Alexander Biratko | Continue capability 116 (terminal hub registration flows) | TBD | Normal | |
| 5 | [Unassigned — needs clarification] | Create a feature under capability 242 for hardware scenario tests through the runner | TBD | Normal | AI agent did not create it |
| 6 | Alexey Khamin | Branch from fresh main, pull in Alekseev's memory-chip changes, try to build FlexPort | TBD | High | |
| 7 | Alexey Khamin | Finish remaining tests on production FlexPort build | TBD | Normal | |
| 8 | Pavel Frolov | Tell Andrei the location contact number is the person called on ticket problems | TBD | Normal | Personal mobiles may print on tickets |
| 9 | Anton Leshkevich | Create a feature under capability 240 for his game conversion; finish vertical layout | End of week (Oct 16–17, 2026) | Normal | |
| 10 | [Unassigned — needs clarification] | Sort out with designers why NAD 2 resources are labelled NOVA | TBD | Low | |
| 11 | [Unassigned — AI PM] | Create tasks: NAD 2 product code in data center; Nebraska progressives | TBD | Low | Not priority |
| 12 | Ivan Shpak | Move the waiting test feature to Blocked; check Pavel's build after Vladimir; try production firmware network access | Oct 15, 2026 | Normal | |
| 13 | Anton Seregin | Finish printer scenarios; find the source of the "10-minute invalid ticket" rule | TBD | Normal | |
| 14 | Dmitri Kovalchuk | Add board filters so Daniil's NE1 task shows | TBD | Low | In progress |
| 15 | Evgeny Kharetski | Work on LGS 1243 front and back end | TBD | Normal | |
| 16 | Irina Shishko | Push autotests to 90%; remove TIN 88 from MVP1 | Oct 15, 2026 | Normal | |
| 17 | Vladimir Samusenko | Close TIN 71, 72, 27, 33 (ask Pavel on 33); then 57, 63, 56; remove Oct 15 date on 56 | Oct 15, 2026 | Normal | |

## Open Questions

- How many saved RIS should a machine keep — one or many? (Irina Shishko, Pavel Frolov)
- Where did Claude get the "ticket not taken in 10 minutes becomes invalid" rule? (Anton Seregin)
- Why do designer tasks for NAD 2 games carry the NOVA label? (Igor Metelski)
- Do the Nebraska progressives need controller changes? (Igor Metelski)
- Does the AI PM "NC1" decision fit Daniil's work, given video decode is set at browser level? (Daniil Stauskiy)
- Which board does the IO board update target (Claude sees a "42" board in the requirement)? (Alexander Biratko)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-15*
*Source meeting: Daily Standup meeting*
