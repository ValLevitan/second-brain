# Meeting Summary — Game Design
**Date:** Saturday, March 28, 2026, 9:32 PM Eastern
**Duration:** ~1 hour 28 minutes
**Attendees:** Val Levitan, Michael Gottlieb, Juan Martinez

## Summary

### Wolfpack — Twin Bison Clone Strategy

The central discussion was Val's push to create a thematic clone of Twin Bison to run in parallel production, testing whether the team can produce game variants with negligible schedule impact. The conversation began with the idea of a stallion theme, but Michael raised a critical artistic constraint: horses viewed front-on look awkward — their eyes are on the sides of their heads, their teeth look odd, and a stallion staring you down doesn't produce the same visceral impact that Twin Bison's wide-faced, direct stare achieves. A horse requires a 30-45 degree isometric view, making it fundamentally different from the Twin Bison template.

Val pivoted to a wolf, noting wolves have a similar broad facial structure to bison — shorter neck, stockier build, and capable of a compelling front-facing stare. Michael agreed this was a stronger fit. The name "Wolfpack" was adopted, with Michael noting it works thematically: during free spins, when symbols lock, more than two wolves locking constitutes a pack. Juan confirmed IGT doesn't own "Wolfpack" (their titles are Wolf Run and Coyote Moon). The team also briefly considered bear (too tall standing up, looks stuffed) and giraffe/horse together for a different game format.

Michael shared a cautionary lesson from Bally: when they produced math clones (Havana Cubana and Tahitian Queen), salespeople picked one and pushed it exclusively — one sold 300-400 units, the other sold zero. He solved this later with Wonder Woman Wild and Wonder Woman Gold — same theme but slightly different math, forcing salespeople to buy both, which accelerated to 3,000 total sales. His concern is that having three animal-themed lines-and-ways games in one game pack would make players think they're all the same game, regardless of whether one is 3x3 and another is 3x5.

The agreed sequence: (1) Let Lena finish Twin Bison game design (currently in progress, scheduled through ~April 6). (2) Have Lena produce a Twin Bison production schedule without knowing Wolfpack is coming. (3) Michael uses the intervening time to develop the Wolfpack abstract — story, environment, character design, symbol hierarchy, color priority. (4) Once the production schedule is locked, Michael introduces Wolfpack to Lena, expedites it through concept and design ("replace this with that"), and adds it to the production schedule in parallel. Val believes this parallel addition will be "negligibly" visible on the schedule. Juan will write the game concept offline and enter it into the system only after Michael has spoken to Lena.

Juan raised a strategic point: submitting both games to Eclipse simultaneously cuts testing costs in half — they only need to prove one math set and barely look at the second game. However, Wolfpack should NOT be in the same Georgia release as Twin Bison (too many similar animal games). It's more deployable in South Dakota and Nebraska, which are more receptive to game changes. Michael emphasized that any clone still needs a holistic creative vision — it's not just swapping symbols; there's geometric symbol hierarchy, color priority, environmental storytelling, and character behavioral characteristics that need to be thought through.

Val's stallion theme was preserved as a future concept for horizontal dual-screen machines, where the side-view perspective that horses require would work naturally.

### Lion's Riches Redesign

Michael is applying the Twin Bison visual approach (large animal face in the vertical space, staring down the player) to Lion's Riches, which is currently JVL's top-performing game (#1 in South Dakota). Val expressed concern that a lion requires different treatment — "a lion is a king," fundamentally different from the bison/wolf category. Juan anchored the discussion: Lion's Riches holds a continuous #1 position in South Dakota, and the original exercise was to improve an existing winner, not transform it. Any change toward the Bison visual approach would be a completely secondary project. Michael confirmed he's already working on bringing the vertical stare-down look to Lion's Riches and that it will replace the current digital glass pay table on the upper screen.

### Floating Pay Table and Screen Configurations

Val praised the floating pay table concept for dual-screen machines. It frees the entire second screen for character effects and animation, with only a small banner at the bottom for the pay table — "phenomenal" and "will rejuvenate the dual screen." Juan noted this was inspired by Bad Dog's approach. Juan also flagged a side-mounted pay table layout for single-screen configurations worth revisiting. Michael said he'd talk to Lena on Monday about designing for single-screen configurations.

### Production Efficiency and Automation Vision

Val laid out his broader vision for manufacturing efficiency at JVL. His core argument: JVL currently operates one game at a time ("crafting a Swiss watch"), but needs to run production like a conveyor belt — concept, design, and production as distinct, parallelized stages with binary (not analog) handoffs.

Specific automation milestones Val cited as already achieved or in progress:
- **Meeting-to-Jira automation:** Lena has tested going from meeting recording to populated Jira tasks with pictures, with no manual labor.
- **Comp art generation:** The team can verbalize game concepts in a meeting and receive 3 comp art variations within minutes.
- **Math generation:** Game math can be produced within one hour.
- **AI-powered PR checks:** Already implemented on pull requests — full AI review before approval, running at $250/month.
- **Bug turnaround:** Texas bug was fixed in one day/night, though Val considers this still too slow and believes bugs should be fixed automatically through data collection, automated analysis, and immediate fix deployment.

Val's target architecture: short feature branches (200-400 lines of code), merged into main (which serves as QA), with the ability to release directly from main at any time. This contrasts with the current industry norm where games sit in internal QA for 60 days and then another 60 days at GLI/Eclipse.

Val disclosed that JVL currently uses 55 different programming languages across their codebase — a legacy situation he called "criminal." Michael agreed it's "a house of cards, garbage layered on garbage" with no one remaining who understands the original decisions. Val is converting to languages that support full automation, specifically moving away from C, which doesn't work well with automated tooling. This platform consolidation is a prerequisite for entering the HHR (Historical Horse Racing) market.

Michael referenced his Bally experience with Unity, where artists could put art directly into games without any programmer involvement, with daily builds and art integration by early afternoon. He'd love to reach that state at JVL. Val clarified his vision goes further: not just artist-in-the-loop emulation, but continuous release capability — something he says no company in the industry does today.

### Eclipse Lab Partition Strategy

Val revealed a cost and compliance optimization: Eclipse has been signing all partitions on JVL's submissions, but the law only requires signing the SAS partition. This created an artificial re-approval obligation — whenever any signed partition's checksum changed (even non-regulated ones), Eclipse required re-certification. Val challenged this practice. The Omni system now has 7-8 separated partitions so that most jurisdictions only need the legally required partitions signed, dramatically reducing re-approval frequency and cost. Juan added that Eclipse charges an extra hour for each partition signed.

### Business Context and Market Status

Current sales are effectively zero — existing orders are on hold pending peripheral delivery, which Val says is being resolved. In South Dakota rankings, JVL slipped from a higher position to #4. Juan attributed this to a blizzard — players who braved the weather went to games they already love (the #1 game is an Ainsworth title from their 20-game multi-game suite), and JVL isn't established enough yet to be a destination. The Lion's Riches freezing bug fix is coming.

Val expressed urgency about the competitive landscape: IGT is laying off employees in the thousands, and large companies will survive on their worldwide license portfolios, not their content. JVL doesn't have that protection and has "zero chance of surviving unless we change the game" — meaning the business model, not just the products. Free/open markets require a different operational approach.

Rich Winley was mentioned as a Texas contact who casually claimed he could move thousands of units. Val advised taking this with a grain of salt.

The team acknowledged an artist recently quit and Lena was told to backfill, which surprised Michael. Val explained he needs the momentum now but eventually won't need as many people once automation is in place.

### Ticker Issue

Michael raised that a ticker feature has been waiting for months. Val challenged him to show the Jira task — Michael said he doesn't have access to the engineering schedule. Val directed him to ask Lena to point to the task, asserting there is "absolutely zero chance" there's a bottleneck with the engineers. Michael suggested Igor's military service deployment may have delayed it; Val disagreed, saying Igor being out hasn't affected the schedule.

## Decisions Made

- **Wolfpack is the next Twin Bison variant** — wolf theme, not stallion. Wolves have the right facial proportions for the front-facing stare-down look. (Val, Michael, Juan aligned)
- **Wolfpack will NOT ship in the same Georgia release as Twin Bison** — target South Dakota and Nebraska markets instead. Three animal stare-down games in one pack would look identical to players. (Michael raised, Juan and Val agreed)
- **Stallion theme reserved for dual/horizontal screen** — horse proportions suit isometric/side view, which works for wide-format displays. (Val proposed, Michael agreed)
- **Lion's Riches stays a separate project** — apply the vertical stare-down approach but don't clone it from Twin Bison. It's the #1 game and shouldn't be destabilized. (Juan anchored, all agreed)
- **Submit Wolfpack and Twin Bison to Eclipse simultaneously** — halves certification cost since only one math set needs proving. (Juan proposed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael Gottlieb | Develop the Wolfpack abstract/concept — story, environment, character design, symbol hierarchy, color palette, behavioral characteristics | April 6, 2026 | High | Must be ready before Twin Bison exits game design so Wolfpack can be fast-tracked through concept/design |
| 2 | Michael Gottlieb | Do NOT mention Wolfpack to Lena until Twin Bison production schedule is established | Ongoing | High | Val's parallel production experiment depends on Lena not being overwhelmed by the scope |
| 3 | Michael Gottlieb | Talk to Lena on Monday about designing for single-screen configurations (side pay table layout) | March 30, 2026 | Normal | Exploring single-screen product option |
| 4 | Michael Gottlieb | Ask Lena to point Val to the ticker task in Jira | March 30, 2026 | Normal | Ticker has been waiting months; Val wants to see where it sits in the engineering schedule |
| 5 | Juan Martinez | Write the Wolfpack game concept offline; enter it into the system only after Michael has spoken to Lena | After Michael confirms | High | Keeps Wolfpack hidden from Lena until the right moment |
| 6 | Juan Martinez | Write the REQ for Wolfpack with market-specific parameters (Georgia skill element, dual box skill, different market configurations) | TBD | Normal | Michael needs rough market parameters to start percolating on game variants |
| 7 | Val Levitan | Review Twin Bison production schedule once Lena provides it | After April 6, 2026 | High | Gate for introducing Wolfpack into production |
| 8 | Val Levitan | Push Twin Bison game design to "Done" status — currently shows "In Progress" with schedule extended to April 6 (was March 30) | ASAP | High | Schedule discrepancy — the game design review was completed on Friday but status wasn't updated |

## Engineering Signals

No engineering signals requiring action from this meeting.

## Open Questions

- **Wolfpack market timing:** If Georgia is too complex for the wolf game release, and South Dakota/Nebraska are the targets, what's the submission timeline for those markets?
- **Ticker task status:** Where does the ticker feature actually sit in the engineering pipeline? No Jira task was identified during the meeting.

---
*Processed from Teams transcript on March 28, 2026*
*Source meeting: Game Design*
