# Meeting Summary — Game_Development
**Date:** September 25, 2026, 2:32 PM – 3:14 PM Eastern
**Duration:** About 42 minutes
**Attendees:** Val Levitan (organizer, chair), Michael Gottlieb, Efim Podvoiski, Lena Zhukova
**Raw transcript:** [[Meeting_Transcript_GA_Progressives_and_Class_A_Lions_Riches-September-25-2026]]

## Summary

Held in English. Some speech recognition errors (for example "RAS" for RIS, "Omni" for Nova, "Vivek"/"VDAC" for VDEC, "mass" for math).

**Georgia V2 RTP was wrong.** Michael said the Georgia V2 machines were deployed at **92% plus 4.5% for the progressive = 96.5%**. He said a player can feel the difference between 96.5% and 92%. Michael said it "should have never been there" and was a mistake. Val said at 96.5% JVL will never reach its net win and will "get kicked out". Val set **92% as good enough for now**. Val does not know how the machines got to 96.5%. Efim said a document from somewhere was used.

**Progressive top awards.** Michael gave the new values: **Match 3 = $2,400, Fiery Ice = $2,400, Jackpot Rush = $1,500**. He did field research. Progressives in the market are very different. Some competitors use $5,000 top awards. IGT uses separate progressives per game at about $300–$400. Fiery Ice and Jackpot Rush top awards are fixed and cannot go higher, so Match 3 was kept close to them. Match 3 is fed by all six games, so it should grow fast. Michael said several progressives in one cabinet matter: if one hits, the others keep running and the cabinet does not "go dead". Felipe said some locations ask to reset the progressive at $8,000 (not allowed; it goes to an overflow bucket). Felipe has had no complaints about current progressive levels. Efim agreed it is a middle position because there is no data. Val agreed with all points: not enough data, do no harm, multiple progressives are needed.

**Data is coming.** Val said that for the first time JVL will put out machines with "models" (as the transcript reads; possibly "modems" — speech recognition unclear). He called this a very big breakthrough. Michael agreed.

**RIS spot checks.** Val asked Efim to spot check the RIS actually installed on the machines. Michael said he told Felipe to communicate up front, and told Efim to "trust but verify" the data.

**Georgia V3 status.** Val said V3 **passed the interlock test**. The letter is expected **Monday (Sep 28)**. Delivery is **Monday to Wednesday (Sep 28–30)**. Val has not checked if all of Michael's changes are in this release. He asked Michael (and Efim) to call Felipe and verify on a running machine by video: VDEC, settings, RTP. Michael said he and Efim will do it.

**Class A product — Lions Riches as test bed.** Lena showed images. Reduced dual box, credits on the left, awards in the center, bet plus/minus in 25-cent steps from $0.25 to $5.00. A VDEC layout with plus/minus buttons is still needed. Lions Riches Georgia is a nudge game, so Efim must redo the math without nudge. Efim said the big challenges are the **$50 cap**, free spins, party time, and the number of math files. Efim said Nebraska software is basically Class 3 with a dual box added.

**Party time feature.** Michael said party time gives repeated $50 wins, like the competitor's "hot streak". He sees it as a substitute for progressives. The party time message stays on top while active. Efim suggested putting payouts above $50 into party time, maybe 10–20% of RTP. Michael said the party time wins they saw were at least $100. He expects a sweet spot of **$100–$250**. Val said he enjoyed party time and liked turbo. He said he has no opinion on the numbers.

**Flex-S cabinet (Val's spec).** Val said Class A will go into a new cabinet, "Flex-S" (sporty version, also called Street Machine):
- Basic machine without VDEC; a provision for a VDEC if the right narrow touch screen is sourced.
- Upright only, shallow deck, slanted about 10 degrees.
- Cup holder on one side, large slam button on the other side.
- 43-inch vertical screen (47 or 50 inch costs much more).
- Controls on the screen; Val asked how many buttons are needed, "probably 8".
- Val would also like the same Flex-S hardware in Texas.
Michael said they will orient it like Primero, where most of the interface is on the screen.

**Cash-out screens.** Lena showed the cash-out confirmation and the continue/print ticket dialog. Michael said the amount shown depends on the player's awards; a minimum cashable award is still to be set (maybe $5). Michael said the design is close to Primero and "when you're messing with people's money, don't be clever". Val is thinking about how to avoid a printer inside, for example AFT with the optical ticket scanner or rescanning the e-wallet. Val said to leave the icon as is for now. On meters, Val noted the logic is two pots (credits and awards). Michael said awards go to zero when the ticket prints. Val said to leave it like this for now.

**Felipe feedback.** Felipe praised the look of Twin Bison, the revised Lions Riches, and the parrots in Tropical Paradise.

**Schedule and tools.** Lena said Class A will be done in **Nova**. The team is working with Dima, Sasha Biratko and Igor on asset transfer and "liquid glass" in Nova. Full Class A production starts after Nebraska is in production. Efim said his Rust part is ready. In Jira (IP-1190), the **Lions Riches abstract targets October 9**. Lena said visual design is mostly done; storyboards are still needed. Production is not yet measured; it will not start until December/January, with R&D this month. Michael said the team is building everything for the first Nova products in Jira and Confluence. Val warned there may be a later migration (to GitHub) and some redundant work; he cannot say when and has no bandwidth for it now. Lena said Confluence documents can be moved to Markdown when needed.

## Decisions Made

- **Georgia RTP set at 92% for now** — 96.5% (92% + 4.5% progressive) was a mistake; JVL would never reach its net win. (Decided by Val Levitan; Michael Gottlieb agreed)
- **Progressive top awards: Match 3 $2,400, Fiery Ice $2,400, Jackpot Rush $1,500** — no data supports a bigger move; keep the three progressives close. (Proposed by Michael Gottlieb and Efim Podvoiski with Felipe; Val Levitan agreed)
- **Lions Riches is the test bed for the Class A product.** (Stated by Michael Gottlieb)
- **Flex-S cabinet spec: upright, shallow deck ~10°, 43-inch vertical screen, cup holder, large slam button, no VDEC in the basic version (provision kept), controls on screen.** (Decided by Val Levitan)
- **Class A is built in Nova; full production after Nebraska.** Lena stated this as already agreed; Michael also called it "Class A Nova". Val's words at that moment ("Sorry, no, no, no") are unclear in the recording. (Stated by Lena Zhukova)
- **Cash-out screen and meters stay as shown for now** — can be revised later. (Decided by Val Levitan)
- **Nova product docs continue in Jira and Confluence**; a later migration may cause some redundant work. (Val Levitan, Michael Gottlieb)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim Podvoiski | Spot check the RIS actually installed on the Georgia machines (ask for the RIS installed; check the RTP) | TBD | High | Val does not know how 96.5% happened |
| 2 | Michael Gottlieb, Efim Podvoiski | Call Felipe and verify on a running machine (video: VDEC, settings, RTP) that all of Michael's changes are in the Georgia V3 release | Before delivery, Sep 28–30, 2026 [Needs Val's confirmation] | High | V3 letter expected Sep 28 |
| 3 | Michael Gottlieb | Tell Val how many buttons the Flex-S button panel needs (Val: "probably 8") | TBD | Normal | [Needs Val's confirmation] on owner |
| 4 | Michael Gottlieb | Finish the Lions Riches Class A abstract (Jira IP-1190) | October 9, 2026 | Normal | "conceivably, we have to see" |
| 5 | Lena Zhukova | Close the graphical adaptation feature and create all Class A storyboards so the engineers understand the flow | TBD | Normal | |
| 6 | Michael Gottlieb | Work with Lena on the storyboard pieces and the time they will take | Week of September 28, 2026 | Normal | |
| 7 | Efim Podvoiski | Work out the Class A Lions Riches math without nudge ($50 cap, free spins, party time) | TBD | Normal | |

## Open Questions

- How did the Georgia V2 machines get to 96.5%? (Val Levitan)
- Should the RTP be 91%, 92% or 93%? Val said 92% is good enough for now. (Val Levitan)
- Party time win size: expected $100–$250; not final. (Michael Gottlieb, Efim Podvoiski)
- Minimum cashable award amount (maybe $5). (Michael Gottlieb)
- Can the cabinet avoid a printer (AFT with the optical scanner, or rescanning the e-wallet)? (Val Levitan)
- Flex-S hardware for Texas as well. (Val Levitan)
- VDEC layout with plus/minus bet buttons still to be designed. (Michael Gottlieb)
- Class A production effort not yet measured. (Val Levitan)
- Timing of any migration from Jira/Confluence. (Val Levitan)
- Val offered to cover other topics on Monday (Sep 28).

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: Game_Development*
