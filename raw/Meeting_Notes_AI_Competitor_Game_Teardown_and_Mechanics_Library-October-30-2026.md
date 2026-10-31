# Meeting Summary — Review – AI teardown of a competitor game (hypothesis test)
**Date:** October 30, 2026, 8:03 AM – 8:49 AM Eastern
**Duration:** ~46 minutes
**Attendees:** Val Levitan, Evgeny Kharetski, Pavel Frolov, Igor Metelski, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_AI_Competitor_Game_Teardown_and_Mechanics_Library-October-30-2026]]

## Summary

Held in Russian. Audio is poor in places. Unclear words are marked "heard".

**What Evgeny tested.** Evgeny asked Claude to break down competitor games from free YouTube videos: Aristocrat games (a penguin game, a wolf game, Timber Wolf three times), plus IGT and Blueberry (heard). About 234 minutes of video across 4 games. Claude can pull out the mechanics: how bonuses work, the grids, the symbols, the animations (for example the penguin that walks in from the screen edge and breaks ice on the reels). The math it can only guess roughly; Claude wrote its own model that runs each bonus about 20,000 times. The artifact was shared in the meeting chat. For long videos Claude cut frames every few seconds and studied closely the parts where the player balance changed.

**Capture list.** Evgeny made a first version of a document that says what to film on a competitor machine with the video-capture box: for example 10 seconds of the attract screen, then 5 seconds of each help/rules page. Val added that he can also play for money and then walk through the demo/show mode to record every bonus.

**Mechanics, not math.** Irina explained our math tests run 4 million games twice (up to 2 × 400 million when there are doubts). Pavel said playing a game for a long time is more useful than walking through every bonus. **Val: we need the mechanics, not the math.** Evgeny: with about 1,000 games of video the bonuses will show up; show mode can trigger them on purpose.

**Why do this.** Pavel: to find things in competitor games that we do not have, such as interactive characters that change nothing but give the game a feel. Val: Aristocrat, Light & Wonder and IGT lead new mechanics; JVL does not have their market reach and never will. JVL must pick up new mechanics faster, name them correctly, and turn them into capabilities and acceptance criteria for game designers. Not copying machines — understanding what the industry needs and doing it our way.

**Describing a new mechanic.** Val asked if Claude can describe a new mechanic in our own words and templates. Evgeny: yes, easily. Igor: from a written mechanic we could build a working bonus with placeholder scenes, define the code contracts, and learn what we need from math.

**Modular framework.** Igor: the new framework is planned as separate pluggable modules — engine, framework, games, bonuses — each following contracts set by the framework. A new bonus can then be added without changing the framework. Pavel asked where bonus resources and transitions live; Irina said in the game, Pavel said then the bonus is not independent. Igor: details to be worked out later. Pavel noted Aristocrat's bonus buy also carries its own math.

**Val's plan.** Val will get a market report and decide which games matter, only for JVL's markets (not Australia, Macau or Las Vegas). He takes on finding where to film them; the capture file will come from him. Steps: find the new mechanics (maybe two) → add them to our mechanics database, glossary and taxonomy → bring the framework to where it can build games with them → find all profitable titles with that mechanic in our markets → film them and confirm the mechanic → split out the themes and replace them with themes our players already know (wolves, etc.).

**Validation test first.** Evgeny will pick one of our games, break it down from video with a Claude session that knows nothing about our code, and in parallel build the wiki for the same game from our code. If the two match, the method works. Irina: use the GA-COAM machine with three different products installed and take one game from each, to get different mechanics. Val: remember those games use finite math, not random math. Target: next Friday, November 6.

**Engine requirements.** Val first asked for a proposed architecture from this and the previous transcript. Pavel said the architecture is still raw; the requirements list is further along. Val agreed: a requirements list, not architecture. Val also asked that our newer games' mechanics be written up (wiki first), covering at least two mechanics, not one game.

## Decisions Made

- **Focus on mechanics, not math.** — The goal is to learn new mechanics, not reproduce competitor math. (Val)
- **Validate the method on our own games first** — blind video breakdown compared with a code-based wiki, one game from each of the three products on the GA-COAM machine. (Evgeny proposed; Irina, Val agreed)
- **Only games that matter in JVL's markets** — Val picks them from a market report; Australia, Macau and Las Vegas are out. (Val)
- **Framework is modular** — engine, framework, games and bonuses as separate pluggable modules with contracts. (Igor; Val agreed)
- **Considered and superseded:** a proposed engine architecture — replaced by adding to the engine requirements list. (Val, after Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Get a market report, choose the competitor games that matter in JVL's markets, find where to film them, and issue the capture file | TBD | Normal | Val took this on |
| 2 | Evgeny Kharetski | Run the validation test: video breakdown of our games (one per product on GA-COAM) vs the code-based wiki, and compare | Nov 6, 2026 | High | Proves the method before filming competitors |
| 3 | Igor Metelski | Add to the new engine requirements list, using this and the previous meeting's transcript | TBD | Normal | Requirements, not architecture |
| 4 | Igor Metelski / Evgeny Kharetski [Needs Val's confirmation] | Write up the mechanics of our newer games (wiki first), covering at least two mechanics | TBD | Normal | Val named Igor, then Evgeny proposed doing it with the test |

## Open Questions

- Where bonus resources and transitions live — in the game or in the bonus module. (Pavel, Irina; Igor: later)
- How long a game must be played to describe it with confidence (Pavel suggested measuring this on our own games).

## Dispatch Log

---
*Processed from Teams transcript on October 30, 2026*
*Source meeting: Review – AI teardown of a competitor game (hypothesis test)*
