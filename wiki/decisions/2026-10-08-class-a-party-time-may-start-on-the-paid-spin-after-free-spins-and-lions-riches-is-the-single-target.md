---
type: decision
title: Class A design — after free spins, the next paid base-game spin may trigger party time; Lions Riches is the one game that defines Class A behaviour before it spreads to the rest (Oct 8 2026)
date: 2026-10-08
aliases: [party time after free spins, subsequent base game spin may trigger party time, set a flag, Class A requirements, IP-1220, IP 1220, IP-1190, Lions Riches definitive target, one particular game definitive target, reverse engineered Primero, 50 bucks a pop, 50 50 and 25, ready by October 16, living breathing document, GD-979 storyboard, Class A kickoff in Russian]
source-count: 2
status: active
open-commitments: 3
open-questions: 2
---

# Class A — party time may start on the paid spin after free spins; Lions Riches is the single target

Set by [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] with [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], and presented to [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-08-game-design-class-a-party-time-and-dual-box.md|Oct 8 2026, 12:00 PM game-design meeting]] (English). Val asked questions and did not object [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]. Background: [[wiki/topics/georgia-class-a-machines.md]].

## Where the requirements come from

Val: "I don't know where to get legislative requirements for Class A. Did you manage to find anything at all?" Michael: "I could not identify anything. Basically, I have reverse engineered or deconstructed what Primero is doing. And that is what we are going to do with one variation." The work is the Class A requirements document (Jira **IP-1220**; Michael opened the item with **IP-1190**, and the notes write "IP-1190 / IP-1220"), "the complete overview of what is required for taking our games and making them compliant with Class A" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

## The one variation — party time after free spins

- **Why.** Party time is the chase: "the party time wins are 50 bucks a pop, and that's basically more powerful and more compelling and more important than anything else." Free spins are weak because "you can win no more than $50 in free Spins" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- **What.** "after the completion of free Spins, on the subsequent regular game base game spin, we may trigger party time." The player "will have to press the spin button, place an additional wager to be compliant, and then go into party time for as many Spins as we need them to go into party time." Michael: "We don't see anything in the regulations that precludes that" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- **Val's point on the $50.** "it does not have to be 50. It could be less than 50. It cannot be more than 50… if you have to pay out, let's say, 125… you could have 50, 50, and 25." Michael had seen only $50 wins ("every single time it was 50") but called it "a very valid point"; they will check in the maths whether paying less than $50 "achieves our goals" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- Primero's help screens are "incredibly vague" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

## Lions Riches is the single target

"IP 1193, Lions Riches is going to be the test bed for this." Once Class A Lions Riches plays, they study behaviour and timing, "refine it within Lions Riches and then take that and propagate it through all the remaining games… we need to have one particular game that's going to be the definitive target for how the thing is going to behave" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

## What the document and storyboards hold

- **New cabinet note.** Michael read from the document: the release "is currently scheduled to have a new cabinet design. This cabinet may have a reduced sized Vdeck"; then the V43 bet levels are not shown on it, and it shows bet up / bet down icons "like our competitors" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- **Content.** Bet levels, game flow, choosing the larger coin, the confirmation, how party time works [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- **Storyboards.** [[wiki/people/lena.md|Lena Zhukova]] is drawing a detailed storyboard of about 16 screens "with all like proper numbers and all like meters or values" for programmers (task GD-979, under IP-556 "Class A, V43 Nova design", IP-1198 Lions Riches and GD-945). One frame: "if you change your bet level, party times is disabled. If you change your bet level back to the previous bet level, party times enabled" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].
- **Kickoff.** At the Class A kickoff, "Efim is going to speak to them in Russian and make sure there is no confusion" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

**GD-945 is named two ways.** Michael first calls it "the Georgia coam Lions Riches adaptation", then "the Nova Lions Riches adaptation work"; the notes use Nova. Recorded both ways [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]] [[raw/Meeting_Notes_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

## Schedule

Val: "So Class A requirement that says ready by October 16th." Michael: "We'll see. Yeah, we'll see. This is… at the concept level." The money-in, credits, awards and cash-out framework will stay; "the math piece of it is the piece that we're going to have to continue to work on over time." It is "a living, breathing document" [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]].

## Relation to earlier pages

- Sept 25: party time was read as "a substitute for progressives", and Efim listed free spins and party time as open maths problems — [[wiki/meetings/2026-09-25-georgia-progressives-and-class-a-lions-riches.md]]. This ruling is the first answer on the free-spins side. Evolution.
- Platform: [[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]].

## Open commitments

- [ ] [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] / [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] — check in the maths whether party-time payouts below $50 (e.g. 50 + 50 + 25) meet the goals — due unspecified — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — finish the detailed Lions Riches Class A storyboard (GD-979) — due unspecified — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
- [ ] [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] — explain Class A behaviour to the developers in Russian at the Class A kickoff — due kickoff (date not set) — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]

## Open questions

- Will the Class A requirements really be ready by October 16? Michael: "We'll see" — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
- Should party-time payouts ever be less than $50? Val says they may be; Michael has only seen $50 — [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]

**§15.8:** clear — product and maths content only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
- [[raw/Meeting_Notes_Game_Design_Class_A_Party_Time_and_Dual_Box-October-8-2026.md]]
