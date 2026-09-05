---
type: decision
title: Release Flex IQ in its current configuration and place 20–50 units to collect factual field data; replay and split are parked, not dismissed
date: 2026-08-21
aliases: [Flex IQ release as-is, park replay and split, place IQ units collect facts, IQ competes only with PAX, factual not hypothetical]
source-count: 3
status: active
open-commitments: 3
open-questions: 3
---

# Release Flex IQ in its current configuration and place 20–50 units to collect factual field data

At the [[wiki/meetings/2026-08-21-post-goam-show-recap.md|Aug 21 2026 post-GOAM recap]] (recording 1), [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] reported that essentially every operator at the Georgia GOAM show asked for two things Flex IQ does not do — **replay** (letting a player move from one machine to another) and **splitting a cash-out** (part onto a gift card, the rest as cash or lottery tickets) [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]. [[wiki/people/val-levitan.md|Val]] refused to change the product on that basis. Device substance lives on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## What was decided

- **Ship IQ as it is; do not change features on show feedback.** Val: "I would not focus right now on adding other features, changing features, I would focus on testing the existing routine… What we need to do is to keep on placing devices in the street. And start collecting factual information." Andrei restated the outcome: "this feedback… about the replay, about the split of the transaction, et cetera, they are being parked right now. So we are not putting them into the pipeline… Our strategy is we are releasing the device as it is right now" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **Parked, not dismissed.** Val cut in: "but we also not dismissing anything; we are at the stage of collecting." Andrei's condition: the requests must "not be lost," and once field data justifies a change the team must be able to prepare requirements and capabilities "in a matter of short time" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **The target is 20–50 placed units before conclusions.** Val: "I need to keep on increasing the number of locations to about 20, 30, 50 until I start getting true… remarks and data and factual complaints" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **The only competitor is PAX.** Val: "That's not our competition. Our competition is packs… people that have pucks, I'd like to replace pucks with this." He put roughly **5,000 Georgia locations** on PAX. Felipe accepted the framing: "we are toe to toe with packs, not with anything else" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **Add barcode reading so IQ can activate wrapped cards.** Val said a second front-facing reader is "not a big deal — we can install a second barcode reader"; the team will also test whether the existing reader can read a card inserted diagonally, with a **USB 2D barcode scanner** (Juan's suggestion) as a possible interim fix. Andrei's constraint: "we need to read a barcode, not to swipe and make stripe reader" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **Next steps for IQ:** initiate a new InComm test session for three more cards on a **new location ID without the invalid "N/A" character**, run it only after [[wiki/people/pavel.md|Pavel]]'s fix is released (implement ~Tuesday, release ~Wednesday), then install at the first real location "probably in one week" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]] [[raw/Meeting_Notes_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **Recycler is off the table for this session.** Val: "recycler, we're not ready for, the product is not ready… I don't want to make it a part of this conversation today because I know where it's going" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].

## Rationale — "hypothetical until IQ is in locations"

- Val's stated doctrine: "Everything that we're discussing here is hypothetical, unless… the final stage when IQ is in locations. When IQ is in locations, then the information we're getting is factual." And: "We will never find out until such a time that we have one, 5, 10, 50 units out. You just, you have to go through discovery. The market is new, the market doesn't know what they want" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- He treats every request as a valid hypothesis but not as a basis for action: "I believe that every hypothesis is valid. We just don't know the facts and go out and start changing things without really understanding how the market operates. It's silly" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- Val's own read on split demand: he does not believe the market needs it — "I don't think that you need a split and I think that the market is confused right now" — and on replay he called the demand cultural: "it's a cultural thing… that says, Peter has it, I want it as well." Juan noted the word "replay" itself "was drafted up by some attorney on behalf of the state" and that he had never heard it used in any other gaming jurisdiction [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].

## Dissent recorded

- **Juan Martinez and Andrei both argued split is needed to match PAX.** Juan: "I agree Val that that is a critical item if we want to be compared to packs is that we forego the security aspect and allow the manual entry or split of transactions," and separately asked for "an on and off option to allow partial gift card and other form of payment… to mirror what PAX allows" for the next release. Andrei noted split can be done **without** manual entry, keeping the transaction secure: "we will not allow you to edit a transaction… we still can add some security here, which PAX does not provide" [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].
- **The placement friction is real.** Felipe reported two AKS locations refused IQ because they could not split or manually enter (they make money selling lottery tickets), so AKS supplied a third location "where they don't have anything and they're willing to try whatever's out there"; Andrei and Felipe both expect friction selling IQ without replay or split [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]].

## Open commitments

- [ ] Andrei Klimovich — initiate a new InComm test session (request 3 more cards) and create a new location ID without the invalid "N/A" character — due ASAP; run the test only after Pavel's fix ships — [[raw/Meeting_Notes_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- [ ] Pavel Frolov — implement and release the fix for the invalid "N/A" character handling — due ~Tuesday implement / ~Wednesday release — [[raw/Meeting_Notes_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- [ ] Andrei Klimovich — after a clean test, register the first real IQ location and order its first pack of cards, then keep placing units toward 20–50 — due ~1 week for the first location — [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]

## History

- **Sept 2 2026 — the barcode-reading commitment is discharged.** On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept-2 pre-pilot call]] the answer landed as a hardware relocation rather than a second reader: [[wiki/people/genadi-peari.md|Genadi Peari]] had already ordered new boards, due "на следующей неделе", "которые позволят нам вывести сканер на переднюю панель" (Andrei); Val fixed the geometry — rotate 90 degrees, bring it forward, aim it downward not at the player's face — and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] confirmed he had already scanned JVL's test cards with a test application. The USB 2D scanner and diagonal-insert options were not taken up. Full ruling: [[wiki/decisions/2026-09-02-activate-incomm-cards-by-barcode-on-flex-iq.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
  - [x] Andrei Klimovich (with the engineers) — settle the barcode-reading solution (second reader / diagonal-insert test / USB 2D scanner) before the first install — **discharged Sept 2 2026** — [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open questions

- Does the market genuinely need replay and split, or is the demand cultural imitation? To be answered only by field data once units are placed — [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- Should locations be paid a small incentive per gift card issued to drive card usage? Juan floated "giving them five cents per card or some number that we can live with"; Val said he had thought about it too, and it was parked — [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- Do operators even want the reporting dashboard? Andrei said showing it "didn't ring any bells… no emotions at all," and wondered whether the people he showed it to work with numbers at all; Val: "could be a number of things" — [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
