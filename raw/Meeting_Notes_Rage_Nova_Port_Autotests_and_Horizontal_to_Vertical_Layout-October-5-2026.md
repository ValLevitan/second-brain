# Meeting Summary — Review Igor’s Rage-to-Nova progress: repo standards, ADR/prose, geometry and timing tests, acceptance criteria
**Date:** October 5, 2026, 7:01 AM – 8:09 AM Eastern
**Duration:** ~68 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Rage_Nova_Port_Autotests_and_Horizontal_to_Vertical_Layout-October-5-2026]]

## Summary

Held in Russian. Follow-up to the last Rage-to-Nova meeting. Val organized it.

**Two tool repos are done.** Igor moved two experiment tools into their own repos, set up to the standard: a Nova scene generator (builds a vertical Rage-style scene from given geometry and resources) and a Rage-to-Nova scene converter. A new employee already used the converter to build a game selection screen for Nova, so the handover worked.

**Test approach for the Dragon Pays port.** The test game is Dragon Pays from the South Dakota product. It is horizontal, with four Full HD screens. Igor measured the geometry and timing of the original Rage game and wrote them up as MD files (for Claude) and HTML pages (for people). This covers the main screens in base game and free spins, overlays, win meter, balance meter, bet, buttons and the pay table screen. The topper is skipped because it is usually just a video. Timings cover transitions and reel spins, including anticipation and recognition animations. Igor shared Russian and English documents in the chat.

**How the tests work.** First, the tests check geometry: each element must sit in its expected screen area. Then they run game scenarios: add credit, spin, check buttons are disabled during the spin, then check balance, win, tickers and pay line highlights. This is different from the old Test 360 tool, which looked up elements by their internal scene names. The new tests check what a person sees on screen. Not covered yet: game-to-game transitions and sound.

**Transition test is not working yet.** By eye, Igor sees that the ported free-spins transition is wrong: the background fades faster than the lantern animation. The tests do not catch it. He started on this yesterday. He wants to use mutation testing: put known defects into code or data on purpose and check that the tests find them. Claude says it wrote a mutation script; Igor has not checked it yet and will ask an independent Claude session what the script does. One real port defect was caught: a big-win animation started at the same time as the bonus exit transition.

Val asked Igor to speak about 30% slower. He also said he cannot read long documents from everyone who works for him.

**Val approved the geometry approach.** For horizontal-to-horizontal and vertical-to-vertical ports, Val had no remarks and was very glad. He likes turning the artists' "by eye" layout into math.

**Horizontal to vertical — not settled.** Val believes there is a fixed relative dependency between the horizontal and vertical layouts, so games could be converted either way. Pavel suggested scaling each horizontal screen down proportionally and stacking them on the vertical screen. Igor said they tried that before and the reels came out too small. He prefers fixed templates for each format (for example 5x3 horizontal and 5x3 vertical) with two sets of resources in the game repo. Irina suggested fitting individual symbols into vertical cells, not the whole reel field. Igor warned that transitions are tied to each game's theme; forcing them into strict math would make all games look the same. Pay table templates were also debated: Irina said symbol counts are limited, so templates are few; Igor worried about many templates.

**Val's direction.** Igor continues the autotests. In parallel he adds a second task: learn to convert horizontal games to vertical and back quickly, using Dragon Pays. A vertical template already exists from earlier work.

**Where the tools and tests should live.** The rest of the conversion procedure (new math, logic transfer) and the test scripts exist only on Igor's computer. Igor splits them into universal scripts plus game-specific scenarios. Val said tests come only from acceptance criteria in requirements; to him the "universal scripts" sound like non-functional requirements that have no capabilities yet. Pavel agreed most of this is likely non-functional. Val sees the conversion work as a spike; at the last meeting they agreed it needs its own project. Evgeny: conversion tests belong to the conversion project, and game scenarios belong in the Nova integration repo, which has no structure yet. Pavel: about 80% of the tests will end up in the integration repo, and geometry must also be checked for new games. Evgeny called these "graphic contracts"; Val confirmed that will be the name. Pavel suggested referencing the scripts from the integration repo instead of copying them. Evgeny suggested giving this meeting and the standards to Claude for a proposal. Val liked the idea and said he does not want files kept locally: create the project soon and move things later if needed.

Irina left at about the 59-minute mark to join another meeting, at Val's request.

## Decisions Made

- **Geometry-first port tests are accepted for same-format ports** — elements are checked by screen position and size, then scenarios run. (Decided by Val Levitan)
- **Igor adds horizontal-to-vertical conversion work in parallel with the autotests**, on Dragon Pays. (Decided by Val Levitan)
- **Tools and tests must not stay on a local computer** — set up a project soon and put the remaining tools and tests in Igor's current repo for now; move them later if the place is wrong. (Decided by Val Levitan, Pavel Frolov)
- **Ask Claude for a repo-organization proposal** based on this meeting and JVL standards. (Proposed by Evgeny Kharetski, agreed by Val Levitan)
- **Next review Thursday, October 8, 7:00 AM.** Val first proposed Wednesday; Igor said it was too early. (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Continue the Dragon Pays port autotests, including a test that catches the wrong free-spins transition, and check the mutation script | Oct 8, 2026 | High | Progress review Thursday |
| 2 | Igor Metelski | Experiment with converting Dragon Pays from horizontal to vertical (and back), using the existing vertical template | Oct 8, 2026 | Normal | Runs in parallel with #1 |
| 3 | Igor Metelski | Move the local conversion tools and test scripts into his current repo | TBD | High | Val is against files kept locally |
| 4 | [Unassigned — needs clarification] | Create the Jira project for game conversion (Rage to Nova) | TBD | Normal | Pavel said "we need to make a project in Jira"; no owner named |
| 5 | [Needs Val's confirmation] | Give this meeting and the JVL standards to Claude and get a proposal for how to organize the conversion repos | TBD | Normal | Evgeny's idea; Val asked the group, Pavel said "OK" — owner not clear |
| 6 | Val Levitan | Send the invite for the Thursday 7:00 AM follow-up | Oct 8, 2026 | Normal | |

## Open Questions

- Is there an exact math dependency between horizontal and vertical layouts? Val is sure there is one; Igor and Pavel doubt a simple transform works. (Raised by Val Levitan)
- Do conversion tests live in a conversion repo, and game scenarios in the Nova integration repo? One repo or several for the conversion tools? (Raised by Igor Metelski, Evgeny Kharetski)
- How many pay table templates are needed? (Raised by Pavel Frolov)
- Does Claude's mutation script really work? (Raised by Val Levitan)

## Dispatch Log


---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: Review Igor’s Rage-to-Nova progress: repo standards, ADR/prose, geometry and timing tests, acceptance criteria*
