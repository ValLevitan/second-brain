---
type: decision
title: Sign-off must be on final assembled machines, not open racks
date: 2025-03-07
aliases: [final sign-off, final product testing, open racks, test racks, Georgia office sign-off, assembled machine testing]
source-count: 1
status: active
open-commitments: 0
open-questions: 0
---

# Sign-off must be on final assembled machines, not open racks

On the March 7 2025 game-design meeting, [[wiki/people/val-levitan.md|Val]] ruled that games must be signed off on the **final, fully assembled and packaged machine** — the current product with current firmware — not on a PC or an open test rack. This came after a stutter / frame-freeze defect slipped through on the **Kai-Ocho** ("Kaiocho") game that neither the Minsk team's testing nor Michael's PC testing caught. [[raw/game_design_meeting_march_7_2025.md]]

## What was decided

- [[wiki/people/lena.md|Lena]], [[wiki/people/michael-game-producer.md|Michael]] and [[wiki/people/juan-martinez.md|Juan]] are the **final sign-off** on a game. Machines must be shipped to them from the **Georgia office assembly floor** (current product, current machines, current firmware); Lena may go to the office or have machines shipped to her home, but they must come off the assembly floor. Michael should ask to be put on a **video-conference call** to watch the machines being fully tested, assembled, packaged and shipped. [[raw/game_design_meeting_march_7_2025.md]]
- Rationale (Val): "you can do 99 things right… all you have to do is one thing wrong, and that is what the player notices"; the definition of quality is that every last detail — sound, vibration, touch, glare, the touchscreen — must be right, and those only show up on the final product in its enclosure. [[raw/game_design_meeting_march_7_2025.md]]

## Why the bug was missed (root-cause hypothesis)

- Val and Juan observed a **nanosecond stutter** on Kai-Ocho's main game screen and a **stutter / frame-freeze during the bonus**; it never happened on the Peach games or on Jackpot Rush. It only shows up under fast, sustained play (Juan played $400–$500 and caught it twice). [[raw/game_design_meeting_march_7_2025.md]]
- The hardware was ruled out as the cause: Michael said the same **16 GB of Kingston RAM** at the same clock speed is used across the board (relayed to him from the showroom/hardware side; the source of record does not name that person). [[raw/game_design_meeting_march_7_2025.md]]
- The leading hypothesis: **Minsk tests on open racks**, not final assembled cabinets, and racks "function differently" (they swap and substitute parts, and the thermal/enclosure environment differs — "weird shit happens when the thing heats up"). The Minsk team is to **analyse the logs on Monday** to find the real cause. [[raw/game_design_meeting_march_7_2025.md]]

## Sources

- [[raw/game_design_meeting_march_7_2025.md]]
