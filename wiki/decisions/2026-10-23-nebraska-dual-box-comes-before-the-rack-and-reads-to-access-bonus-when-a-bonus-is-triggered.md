---
type: decision
title: Nebraska dual box — on a win the dual box comes up first and the rack follows the choice; when a bonus is triggered the box reads "to access bonus"; the same approach goes to Class A (Oct 23 2026)
date: 2026-10-23
aliases: [dual box rule, rack after the dual box, move the skill to the outcome of the spin, to access bonus, to access win, dual box before racking, Nebraska dual box behaviour, dual box requirements]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Nebraska dual box: the box first, then the rack; "to access bonus" on a bonus trigger

Agreed by [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] and [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] at the [[wiki/meetings/2026-10-23-game-development-dual-box-rule-and-colombia-class-3.md|Oct 23 2026, 2:00 PM game-development meeting]] (English), with [[wiki/people/lena.md|Lena Zhukova]] and [[wiki/people/val-levitan.md|Val Levitan]] present [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]. The dual box is the "pick the larger coin" skill overlay; where it sits and which markets get it is on [[wiki/decisions/2026-10-08-dual-box-for-nebraska-class-a-and-georgia-five-reel-and-no-smaller-touch-area-for-the-wrong-coin.md]].

## Why a change now

- **The Nebraska build is up and playing.** Michael: "we have the Nebraska build up and playing, and Efim and I have been going back and forth, and there is a meaningful change we want to make in terms of how the skill, the dual box skill behaves" [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]].
- **Few machines in the field.** Asked how many machines JVL has in Nebraska, Val said "Ten." Michael: "if we change the mechanic and the behavior, it's not going to be terribly consequential." Val: "Not a factor." [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]
- **How it worked before.** In the old build (with the Golden Husk) the player went into the bonus, picked the coin, and the win was racked; the skill part came only at that point [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]].
- **Where the old way came from.** Michael: it was "A byproduct of… the skill meter", which was "percentage fractional win, and that kind of goofed everything up. And then we went to the dual box. We now have the freedom to do it on the front end." [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]

## The rule

- **Move the skill to the outcome of the spin.** Michael: "we're going to move the skill part to the outcome of the spin. That's how it behaves for line wins", and "I want to move the racking until after the dual box selection" [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]].
- **Line wins.** "the rule is on a regular line win, don't rack, dual box comes up, pick a choice, rack." To Lena: "we don't want to rack on the outcome of the spin. We only want to rack here." [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]
- **Bonus triggers.** On a win the box says "to access win". When the Match 3 progressive is triggered, the player is "choosing to access the Bonus", so the text must change. Efim widened it: "not just much 3 bonus, right, but any kind of bonus, but free Spins or bonus in fire eyes" (Fiery Ice — **inference**). Michael first noted that "some games have entry wins for free spins", then agreed with Efim that one rule is "more consistent": for the Match 3 progressive "or free spins, the text should read… to access bonus" [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]] [[raw/Meeting_Notes_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]].
- **Class A too.** Michael: "this basically is how we're going to be doing it for Class A as well when we move forward with the Class A stuff." [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]] See [[wiki/topics/georgia-class-a-machines.md]].

## Written requirements asked for

Lena: "Igor asked me if it's possible to write the requirements for the behavior of the box." Michael: "Yeah, yes." Efim: "Yeah, sure… We just want to decide first." [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]] Which Igor is not stated. By context he is a game developer on the Nebraska build; the §4 Igor cluster has five members, and the wiki does not pick one.

## Relation to earlier rulings

- **Oct 8 2026** set where the box sits (lower, above the button panel, for Class A; Nebraska keeps its panel) and refused a smaller touch area for the wrong coin. Oct 23 changes **when** the box appears, not where. This is a new rule beside that one, not a reversal — [[wiki/decisions/2026-10-08-dual-box-for-nebraska-class-a-and-georgia-five-reel-and-no-smaller-touch-area-for-the-wrong-coin.md]] (Oct-23 update).
- The Nebraska product is on [[wiki/projects/nebraska-skill-market.md]].

## Open commitments

- [ ] [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] / [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] — write the requirements for the dual box behaviour (asked by Igor via Lena), once the final rule is agreed — due unspecified — [[raw/Meeting_Notes_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]] [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — change the Nebraska build: rack only after the dual box choice, and show "to access bonus" for the Match 3 progressive and free spins — due unspecified — [[raw/Meeting_Notes_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]] [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]

## Open questions

- Which Igor asked for the dual box requirements? — [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]
- [[raw/Meeting_Notes_Game_Development_Dual_Box_Rule_and_Colombia_Class_3-October-23-2026.md]]
