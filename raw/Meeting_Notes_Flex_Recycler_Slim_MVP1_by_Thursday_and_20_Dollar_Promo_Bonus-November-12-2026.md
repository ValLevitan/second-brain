# Meeting Summary — Flex-Recycler Slim: short meeting (rollout date and Jira)
**Date:** November 12, 2026, 6:53 AM – 7:24 AM Eastern
**Duration:** ~31 minutes
**Attendees:** Val Levitan (organizer), Pavel Frolov, Alexander Biratko, Irina Shishko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026]]

## Summary

**Status.** Pavel: Alexander brought up the recycler this week and likes it a lot. He needs about two more days to finish the hardware bring-up. The Flex-Pay Recycler Slim capabilities were written by Andrei months ago, and Alexander made features for them, but the requirements have no acceptance criteria and must be reworked. Most features are almost ready because the project is built on the Flex-Pay code base; much is already tested on Flex-Pay.

**Val's plan.** Andrei (product owner) should meet the team, groom what goes into the recycler, pick the MVP 1 capabilities, set a release date and present it. Rewriting requirements is easy with Claude. Val insists MVP 1 is done by Thursday and put on the production server, so Andrei can take it from there and test it. Even an incomplete MVP 1 is useful, because it exercises the full CI/CD path. Anything that does not fit goes to MVP 2, dated one Thursday later. Cut scope, do not move dates. Pavel will make the releases right after the meeting; Val expects to see them within a couple of hours.

**Servers.** Val does not allow taking files from DEV or STG; only the ISO image from production. Pavel: then the bottleneck is that a production artifact must pass at least a basic set of autotests. Val agreed this runs as its own track; keep MVP 1 very limited. Alexander must build CI/CD for the recycler; server services already shared with Flex IQ also work for it.

**Target: Texas, e-wallet only, no TITO.** Typical location: two or more JVL vertical 43-inch machines (refitted T27 horizontal cabinets from Pennsylvania in the Georgia warehouse, with vertical TVs and Igor's converted Rage games), each with a Flex-Port, no printer and no bill acceptor, and one Flex-Pay Recycler Slim between two machines.

**$20 promo bonus (AFT).** Val first said: each $20 put in gives $2 promotional credit; only $20, nothing for $5 or $10. Pavel and Alexander showed that at 92% RTP the bonus gives about 102% return, which a skilled player could exploit. Val changed it: **machines at 90% and $1 per $20.** Alexander noted the recycler screen must show the offer clearly. Val asked that Andrei work out the text and visual. Andrei should review all Flex-Pay screens; for next Thursday only current screens are refined.

**Rage games to GitHub.** Val wants Igor Metelski's horizontal-to-vertical Rage conversion for the Texas V43 line to run in GitHub: Igor builds the environment and actions, and a CI/CD pipeline is set up. Val named Andrei Bosik for CI/CD; Pavel suggested Alexey Khamin may fit better, since it is old server scripts to move into the game repos plus an integration repo. Val did not decide that. Val also said he is not insisting on staying with Rage.

**Ownership.** Val told Pavel to take this in hand: plan, schedule and create releases right after meetings, even if not all capabilities are attached.

## Decisions Made

- **Recycler MVP 1 is done by Thursday and placed on the production server; what does not fit moves to MVP 2, one Thursday later. Cut scope, never move dates.** (Val)
- **Only the ISO image from production may be taken; no files from DEV or STG.** (Val)
- **First market is Texas, e-wallet only, no TITO tickets.** (Pavel asked, Val confirmed)
- **Promo bonus: $1 per $20 put in, only for $20, with machines at 90% RTP.** Considered and superseded: $2 per $20 at 92% (would pay about 102%). (Val, after Pavel and Alexander's point)
- **The recycler screen must show the $20 bonus offer; Andrei works out text and visual.** (Val)
- **Igor's Rage conversion for the Texas V43 games moves to GitHub with CI/CD.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Create the recycler MVP 1 and MVP 2 releases and plan them in Jira | Nov 12, 2026 | High | "Within a couple of hours" |
| 2 | Alexander Biratko | Finish recycler hardware bring-up | ~Nov 14, 2026 | High | "About 2 days" |
| 3 | Alexander Biratko | Build CI/CD for the recycler | Before MVP 1 Thursday | High | |
| 4 | Andrei Klimovich | Groom recycler capabilities, pick MVP 1 scope, set the date | TBD | High | Not present; Val's plan |
| 5 | Andrei Klimovich | Write text and visual for the $20 bonus on the recycler screen | TBD | Normal | Not present |
| 6 | Andrei Klimovich | Review all Flex-Pay screens and comment on each | TBD | Normal | Alexander's request |
| 7 | Igor Metelski | Set up the build environment and actions in GitHub for the Rage V43 conversion | TBD | Normal | Not present; Val says about 2 days |
| 8 | [Unassigned — needs clarification] | CI/CD pipeline for the Texas V43 games | TBD | Normal | Val named Andrei Bosik; Pavel suggested Alexey Khamin |
| 9 | [Unassigned — needs clarification] | Add the $20 promo bonus (AFT) to the capabilities | TBD | Normal | Alexander: not in capabilities yet |

## Open Questions

- Exact calendar dates: Val said MVP 1 "by Thursday" and MVP 2 "a Thursday one week later", and at the end "MVP 2 next Thursday". The later MVP 2 meeting used November 19 for the recycler.
- Who writes the Texas V43 CI/CD: Andrei Bosik or Alexey Khamin?
- Are the recycler devices for the demo already assembled? (Alexander asked; Val did not know)

## Dispatch Log

---
*Processed from Teams transcript on November 12, 2026 (scheduled meeting-watcher)*
*Source meeting: Flex-Recycler Slim: short meeting (rollout date and Jira)*
