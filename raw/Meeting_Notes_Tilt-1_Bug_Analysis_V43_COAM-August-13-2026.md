# Meeting Summary — Tilt-1_analysis
**Date:** August 13, 2026, 9:05–9:25 AM Eastern
**Duration:** ~20 minutes
**Attendees:** Val Levitan, Juan Martinez, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_Tilt-1_Bug_Analysis_V43_COAM-August-13-2026]]

## Summary

Val called this to understand the bugs found while testing the ten V.43 (version two) machines for Georgia COAM. The team first thought there was a single "tilt one" bug. When Irina's QA team in Minsk tried to reproduce it, they found three separate bugs instead.

Val stressed a caveat up front: until they read the logs pulled from the actual field machines, no one can be sure the three bugs Irina reproduced in QA are the same "tilt one" seen on the machine in Georgia. It could be something else. Juan asked whether the failure — seen on 2 of the 10 machines so far — will eventually hit the rest; that stayed open.

The three bugs:

1. **Tilt one when all games in a group are switched off.** Irina explained that "tilt one" is a broad, catch-all name the team uses for any unknown bug, so it is not descriptive. She reproduced it by blocking a machine the way the field does it — sending a separate command to disable each game one by one (Irina said this is how it is done in South Dakota / Light & Wonder), rather than one command to block the whole machine. Because the product has three game groups and the system cannot show a group with no games, disabling all the games in a group throws tilt one.

2. **Out-of-service workaround un-blocks a machine.** A machine blocked by Interlock (the regulator) can be returned to operational by a technician simply going into setup, setting it out of service, exiting, coming back, and setting it to operation. The regulator's block can be circumvented — that should not be possible.

3. **Blocked game comes back after a power cycle.** When a game is disabled and the machine is powered off and back on, the blocked game reappears and can be played on boot, even though it should stay disabled. As Juan put it, the power-on overrides the disable command possibly sent by the regulator.

On the display side, Pavel raised that each group currently needs at least one game enabled for the game-select screen, and asked how blocking/enabling should look to the player — a placeholder, a question mark, or something else. Juan suggested the game icon be grayed out to show it is unavailable; Pavel noted Inna sent a picture of the South Dakota implementation, which shows a blank card in place of the game card.

Val stopped the implementation discussion: nothing should be built yet. The team should first investigate the machine now in Felipe's Georgia office — Felipe connects it to the internet, Pavel accesses it remotely and pulls logs — and then have this conversation again. Val called the office-machine investigation the most acute priority.

Val also asked, for the record, that in NOVA the tilt should be narrowly focused per function rather than a broad catch-all — noting it so the point migrates into the NOVA discussion.

## Decisions Made

- **Do not implement any UI or blocking change yet** — first investigate the machine now in the Georgia office and pull its logs, then revisit the design. (Decided by Val — supersedes the in-meeting suggestions to gray out the game icon / show a blank card, which Val explicitly paused.)
- **The Georgia office-machine investigation is the top priority** — the most acute item right now. (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Access the field machine now connected in Felipe's Georgia office via remote access, pull logs, and investigate the tilt-one / game-blocking bugs | TBD (treated as most acute) | High | Already started remote access yesterday with Andrei Klimovich; needs to locate the machine on the business network |
| 2 | Pavel Frolov | Report findings from the machine back to Val and Juan | TBD | High | Val: "keep us posted on what your findings will be" |

## Open Questions

- Is the tilt one Irina reproduced in QA (Minsk) the same tilt one seen on the field machine in Georgia? Unresolved until the machine logs are assessed. (Raised by Val.)
- Will the failure spread to the remaining machines beyond the 2 of 10 seen so far? (Raised by Juan.)
- How should a blocked/unavailable game appear on the game-select screen — grayed-out icon, blank card, or placeholder? Deferred until after the investigation. (Raised by Pavel.)

## Dispatch Log

---
*Processed from Teams transcript on August 13, 2026, 10:01 AM Eastern (scheduled meeting-watcher run)*
*Source meeting: Tilt-1_analysis (August 13, 2026)*
