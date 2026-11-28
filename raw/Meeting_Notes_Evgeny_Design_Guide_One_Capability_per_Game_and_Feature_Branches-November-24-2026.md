# Meeting Summary — Design Guide to Capabilities list
**Date:** November 24, 2026, 8:01 AM Eastern
**Duration:** 28 minutes
**Attendees:** Val Levitan, Evgeny Kharetski
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Evgeny_Design_Guide_One_Capability_per_Game_and_Feature_Branches-November-24-2026]]

## Summary

**Val's goal.** When all questions in the design guide (design brief) are answered, the result should be created in Jira by itself, under an initiative. Designers then work in feature branches. They put the required artifacts there, by hand or automatically. A pull request closes the feature branch. When everything is closed, the game design is done. This covers only the design stage (what Anton does in the design studio). Production comes after and is a different stage.

**How to link the studio and Jira.** Evgeny gave two ways:
1. The agent asks support (Andrei) to create a repository for the game. After approval the agent creates the feature branches. The studio knows which piece of work goes to which branch.
2. Build Jira into the studio.

Val chose way 1. He does not want the studio tied hard to Jira. He said he would like to move away from Jira and work straight in GitHub one day.

**One capability per game.** Evgeny asked why one game should be split into many capabilities. He proposed one capability per game. After discussion Val agreed. The capability is "make me a game" (a set of assets). Under it sit features, one per asset: each symbol, each transition, each sound. Each feature has a feature branch. When the artifact is merged, the feature closes. When all features close, the capability closes. Evgeny agreed that features are needed, because the studio makes the game elements one by one over several days. The feature set will be the same for every game.

**New mechanics are a different topic.** A new mechanic first means growing the studio itself (new layers, timing, instructions). That needs its own capabilities for the studio. Both agreed this is separate from making one game.

**Repository and project number.** Val: when an initiative for a game is taken, the project number and the repository must be created together, by JVL standards. An artist must not be able to open an initiative without them. The agent can ask Andrei, or Andrei can build his own automation. Approval may come from Val.

**Val's view of the next cycle.** Today the studio copies existing games. Later, new mechanics should be described by physics, geometry and timing diagrams. For now the cheapest way: record popular games on video, find which layers, physics, geometry and timing are missing, add the code, and discuss only the design brief.

## Decisions Made

- **Use way 1: the agent creates the feature branches in the game repository. No Jira integration inside the studio.** — Enough automation and control, and Jira may be replaced later. (Decided by Val)
- **One capability per game, with one feature per asset under it. Each feature has a feature branch and closes when its artifact is merged.** — Evgeny's proposal, changed by Val to keep features. (Decided by Val and Evgeny)
- **Project number and repository are created together when a game initiative is taken, following JVL standards.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Add to the brief agent: create one capability and its features for each game | TBD | Normal | Evgeny: "we can do this" |
| 2 | Val | Send Evgeny the transcript of this meeting | Nov 24, 2026 | Normal | Source for the agent update tasks |
| 3 | Evgeny Kharetski | Discuss with Alexander (Sasha) how to link this with the studio | TBD | Normal | |

## Open Questions

- Jira numbers were heard as IP-1197, IP-556 and "531". Not confirmed.
- Who creates the game repository: the agent through Andrei, or Andrei's own automation. Val said either is fine.
- How to describe new mechanics (physics, geometry, timing). Val does not want to work on this now.

## Dispatch Log

---
*Processed from Teams transcript on November 24, 2026, ~6:25 PM Eastern*
*Source meeting: Design Guide to Capabilities list*
