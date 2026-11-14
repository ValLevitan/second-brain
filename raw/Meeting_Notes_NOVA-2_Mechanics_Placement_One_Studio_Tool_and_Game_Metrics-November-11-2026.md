# Meeting Summary — NOVA-2 follow-up - agile plan check
**Date:** November 11, 2026, 7:31 AM – 8:32 AM Eastern
**Duration:** ~61 minutes
**Attendees:** Val Levitan, Pavel Frolov, Anton Leshkevich, Igor Metelski, Efim Podvoiski, Irina Shishko, Evgeny Kharetski, Alexander Biratko, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA-2_Mechanics_Placement_One_Studio_Tool_and_Game_Metrics-November-11-2026]]

## Summary

**Anton: where game mechanics should live (certification).** Everything now lives in the company GitHub; Anton prepared the integration of Igor's tools into the Studio. Today the split is: a small compiled Rust core that rarely changes (certify once for a long time), and scripts (framework, games, assets) that implement the base mechanics. He listed three options:
1. Small core, mechanics in scripts — core is stable, but more content must be re-certified with each release.
2. Key mechanics move into the core — but each new game changes existing mechanics a little, so the core keeps being re-certified.
3. A flexible mechanics API in the core, designed with AI from a catalog of free online slot games. His scanner already has about 200 games (e.g. 24 "hold and spin" games). Games call parts of this API; new mechanics become possible through a bare API; every 1–1.5 years proven mechanics are promoted into a new core version. Not tried yet; needs an experiment.

Discussion: Efim said option 3 makes the first certification a "monster" full of mechanics with no games, and the lab will test each new game fully anyway. Igor suggested a test bench or checksums to prove a component is unchanged. Efim prefers a hybrid: a core plus a standard layer, and plugins/scripts that can be added without changing what already exists; interpreted scripts (Lua) cannot affect each other. Alexander: core plus basic mechanics only, everything else inside games, duplicates are fine; a fix in one game leaves the others certified; promote useful parts into the core over time. Pavel noted this matches Anton's yearly promotion idea. Val asked to leave the question open and discuss in small groups. Val's own view: he likes separate mechanics that grow over time; certify only the mechanics a package uses (e.g. 2 of 10), and when a mechanic changes, change only the mechanic, not the games.

**Anton: agent standards for the Studio.** He mentioned new agent-to-UI protocols. These standards change daily and their tools are in TypeScript and Python, so maybe the Studio should be written in a scripting language. He will study it and bring options.

**Igor: his art-and-scene tool vs the Studio.** He ported his Rage slot-art flow (Claude skills plus web tools for layer layout, paytable setup and an animation tuner) to the NOVA 2 engine; rendering now runs on the engine. He added custom shaders and better text support. His doubt: the Studio is a developer tool (game logic), while his tool takes a designer from creative brief to finished scenes. He asked for feedback from real users and whether designers even need it. Val said JVL will not have designers. Anton, Efim, Alexander and Andrei all prefer one tool for the whole flow (Anton described: a Jira task comes in, the agent builds scenes, the person approves or asks for fixes, then the agent animates, scripts and tests, then commit). Andrei added that one tool is easier to support.

**AI model in the Studio.** Igor said the Studio is wired to Haiku through OpenRouter (pay per token), while he works with Claude Code on Opus. Anton said he used a cheap model only for first tests. Val: do not save his money on this. Andrei: the model must be a replaceable setting; local models on the 16 GB GPUs may come later. Evgeny asked about local models.

**Demo plan.** Val asked what can be shown next. Agreed: a demo of one tool — even with a rough UI but sound logic — that loads the brief made by the game-design agent and goes as far as possible toward a finished game on the new flow, including free spins (Irina's idea). Val moved it from Monday to Tuesday (he travels Monday). Igor warned a full game will not fit in one 45-minute meeting.

**Evgeny: game-design agent.** Done: after the brief is approved, the agent asks whether to create a repository, collects references and the brief into a set structure, archives them, and opens a service ticket to Andrei to create the repo (the agent is not allowed to create GitHub repos). Not done yet: loading the game wiki (15 games from GA-COAM 3) and the math. Next: try to load the repo into the engine so Igor's flow starts from the brief. Igor said math data could be pulled from the Rage math DLLs through a small local server; Efim said he already has records of about 1,000–2,000 played games in a repository. Val asked to involve Efim directly.

**Andrei Bosik:** repositories created, code pushed, access given to everyone present. He raised who defines the contents of the template repository for new games; Evgeny said it is too early. Andrei agreed: finish the tool first, the template will follow from it.

**Val's closing picture (keep confidential).** Machines on location, e.g. 6 games each, send data through the modem showing what is popular. From that data a new game is made automatically, goes to the lab, comes back with checksums, is sent through the modem to the machine, checked, and played — in about a week. Question for Tuesday: what metrics must NOVA and Galaxy collect so game decisions can be made, assuming no designers. Pavel: track more than bet sizes and game counts, e.g. time in a game before the player switches. Efim: first metric is relative popularity under equal conditions (same games on 100 machines); retention is second, but JVL cannot know if the same player returns. After the meeting Efim and Pavel added: collect many metrics and let an AI look for correlations with popularity; Pavel mentioned a QR code shown on a big win (about $20+) that could link a player's phone. Efim doubted players would use it.

## Decisions Made

- **One tool, not two: Igor's art/scene flow is merged into the Studio.** — Agreed by Andrei, Anton, Efim, Alexander. (Decided by Val)
- **The AI model in the Studio is a replaceable setting; do not pick a cheaper model to save money.** (Val; Andrei agreed)
- **Next review is Tuesday (Nov 17): a demo of the single tool going from the design-agent brief toward a full game, including free spins.** (Val, with Andrei and Irina)
- **Where game mechanics live (core vs scripts vs games) stays open** for small-group talks and the next meeting. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Merge his scene/art tools into the repo with the engine | TBD | High | Anton asked; Igor agreed |
| 2 | Anton Leshkevich + Igor Metelski | Plan how to make one tool from two and show a demo from brief toward a full game, with free spins | Nov 17, 2026 | High | Tuesday meeting |
| 3 | Anton Leshkevich | Try Igor's scene flow himself | TBD | Normal | "I'll try it, I promise" |
| 4 | Anton Leshkevich | Study agent-to-UI standards and bring options, including writing the Studio in a scripting language | TBD | Normal | His own proposal |
| 5 | Evgeny Kharetski | Load the game wiki and math into the agent's second brain; try loading the new-game repo into the engine | Nov 17, 2026 | Normal | Val confirmed it as his undertaking for Tuesday |
| 6 | Evgeny Kharetski | Review the material Efim sent by email | Nov 17, 2026 | Normal | "By the next meeting" |
| 7 | Efim Podvoiski | Answer Evgeny's questions and show the recorded-games data | TBD | Normal | Val asked to involve Efim |
| 8 | All attendees | Think about which machine metrics NOVA and Galaxy must collect for game decisions | Nov 17, 2026 | Normal | Val's question for Tuesday |
| 9 | All attendees | Keep this work confidential inside the company | Ongoing | High | Val's request |

## Open Questions

- Where do game mechanics live — core, shared framework/scripts, or each game — and how does that affect GLI certification? (Raised by Anton; left open by Val)
- What metrics show why a game is popular, and how can return players be recognized? (Val, Efim, Pavel)
- What goes into the template repository for new games? (Andrei Bosik; deferred until the tool is done)

## Dispatch Log

---
*Processed from Teams transcript on November 11, 2026 (scheduled meeting-watcher)*
*Source meeting: NOVA-2 follow-up - agile plan check*
