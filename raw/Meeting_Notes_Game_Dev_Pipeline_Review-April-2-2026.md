# Meeting Summary — Game Development Pipeline Review
**Date:** April 2, 2026, 6:03 PM Eastern
**Duration:** ~1 hour 33 minutes
**Segment:** Segment 1 of 2
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Juan Martinez, Efim Podvoiski

## Summary

The meeting was a comprehensive review of the game development pipeline across all active stages: game concept, game design, and game production. Val drove a significant portion of the meeting trying to understand the game design workflow, deliverables, and asset pipeline in detail.

**Game Concept Phase — Lion's Riches Update (GC364/IP531)**

The abstract for the Lion's Riches update has been completed by Michael. Lena has begun preliminary work on the concept art (GC379) but is prioritizing Twin Bison design work first. She estimated she would finish Twin Bison design on Monday and move to Lion's Riches concept art on Tuesday. Val questioned the 10-calendar-day estimate for producing the concept art. The scope includes a new main screen look, new background, new logo, new character look, new free spin screen, and new symbols — roughly 15-20 comp art assets. Critically, this is not from scratch: the same characters remain (an antelope stays an antelope, the African Savannah environment stays), but everything gets a new visual treatment inspired by the Twin Bison art direction that the team fell in love with. Lena confirmed the existing game provides the character and thematic reference, so the work is an evolution, not a blank-canvas creation.

**JIRA Status Management — Containers vs. Sub-tasks**

Val raised repeated questions about JIRA status consistency, specifically why an IP (Initiative) could show "In Progress" when some of its child tasks were still in "To Do." The team reached consensus that IPs function as containers: once any sub-task within an IP starts work, the IP moves to "In Progress," even if other sub-tasks remain in "To Do." This is semantically correct because the initiative has begun. Specific cleanups identified: IP882 (South Dakota VLT Game Concept) needs GC265 closed to complete the IP — Lena confirmed this was accidental. The team also discussed whether completed items should remain visible on the board. Val stated a 30-day visibility window for done items, though he expressed uncertainty about whether this was optimal. Val also flagged that reporter and assignee cannot be the same person in JIRA; Efim agreed to change his reporter to Michael on his tasks.

**Game Design Phase — Twin Bison (IP1029) and Pick 3 Bonus**

Twin Bison game design is actively in progress under IP1028 (Georgia Vertical 2 release). Lena and Michael are working on additional screens, messages, and animation stages for symbols. The math design (GD838) is nearly complete — Efim said he would finish it that day or the next, though play testing remains a separate future task. Michael reported that he and Efim rebalanced the low-pay symbol frequency on reel 1, which was appearing too often and killing anticipation. The lowest three pay symbols now have greater variety, which both Michael and Efim agreed was a superior play experience. They also tested adding wilds to reel 1 and rejected it — it didn't work.

The Pick 3 bonus (a new progressive replacing the Peach progressive for Georgia) is in progress for all object games in the next Georgia release.

**Deep Dive: Game Design Deliverables and the "Shopping Bag" Workflow**

Val spent a substantial portion of the meeting drilling into the game design workflow to understand exactly what deliverables are produced at each stage and how they flow downstream. The team arrived at a shared vocabulary:

- **Master File** (Val's "shopping bag," Efim's "collage"): A large Photoshop (PSD) file containing all composition art assets layered together. This is the central deliverable — it shows the holistic vision of the game screen with all elements (symbols, backgrounds, dashboards, logos, pay tables, reel frames, special effects). Multiple master files may exist per game depending on complexity (main screen, free spins, bonus screens). Lena called this the "master file" because all downstream artists reference it for proportions, positioning, and context.

- **Storyboard**: A visual description of transitions, messages, animation sequences, and game flow. Shows how the game moves from one state to another (e.g., main game to free spins). Storyboards are always required, even for game updates — you can copy-paste from a previous release and modify, but the full storyboard must exist.

- **Comp Art** (Composition Art): The assembled visual of what the entire game screen looks like. "Comp art" refers specifically to the rolled-up cumulative image of all assets, not individual elements. Individual items within comp art are called symbols, assets, or elements.

The pipeline flows: Concept stage (initial comp art, overall game look) → Design stage (animation descriptions/references, transitions, messages, storyboards, additional comp art) → Production stage (final asset creation, building, animation). The design stage's purpose is to answer as many questions as possible before production, where "the taxi meter is spinning." Lena and Michael calibrate the level of design specificity to each artist's capability — more creative latitude for skilled artists, more prescriptive direction for those with limited capabilities.

Downstream, game artists (Julia, Anton) work in parallel: Julia creates layouts and templates from the master file, Anton works on illustrations. They extract individual layers from the master file but need the whole file for context. The output is clean, final assets exported to developers.

Val expressed a vision for efficiency improvements: pre-building game shells before final art is ready so comp art can be dropped in and previewed in-game within minutes, and potentially automating animation generation (describe a coyote opening its mouth over 30 frames, and have it generated). Michael was enthusiastic about this. Efim noted this aligns with the math playtest automation direction. The team acknowledged this would require the Omni 2 architecture — it cannot be achieved within the current Rage Studio framework.

**Game Production — South Dakota VLT (IP459)**

Six games are currently working in the build: Black Hills Kino, La Rosa, Roger Spins, Glover Fortune, Lion Switches, and Wild Cold.

- **La Rosa**: One feature remaining in request review, waiting for the new build. Nearly complete.
- **Wild Cold**: New slot game assembled by Lena, "pretty good shape." Build just became ready; Lena and Michael will review after the meeting.
- **Dragon Pays**: Confirmed still going for South Dakota — it's consistently the #3 game in the market. Val initially confused it with a different dragon game from Georgia. Michael noted the updated version will look "much better, much cleaner, less cluttered."
- **Liquid Glass** home screen: Nearly finished. One feature still in progress — adapting the second screen's attraction mode background to match the new liquid glass home screen. Majority of work done; four features in request review to be reviewed with Michael after the meeting.
- **Black Hills Kino Deluxe**: In fine-tuning phase. Anton has not yet implemented the ticker behavior for South Dakota slot games — Lena characterized this as an inconvenience, not a blocker, since the overall product isn't done yet and Efim asked Anton to prioritize Pulkat Kino before his vacation. Michael noted it feels like "a progress meter stuck at 99%" and he will not approve certain items until the ticker is in place.

The target exit date for IP459 is April 29. Lena raised concern about QA timing — if production finishes by end of April and QA hasn't started testing, there could be a bottleneck. Val explained that in the current Rage Studio framework, QA will always be sequential to production. In Omni, QA would occur at branch integration with automated end-to-end tests that can be run repeatedly in stages. Michael specifically requested that QA begin testing Black Hills Kino now, as it's a new game type (keno) that the QA team (Ivan, Arena) hasn't tested before. Efim supported early smoke testing for novel games, with full testing reserved for finalized products.

## Decisions Made

- **IP status convention confirmed**: IPs function as containers — they move to "In Progress" when any child task starts, even if others remain in "To Do." (Agreed by Michael, Lena, Val, Juan)
- **Wilds on reel 1 rejected for Twin Bison**: Tested and didn't work. (Decided by Michael and Efim)
- **Low-pay symbol rebalancing approved for Twin Bison**: Greater variety across lowest 3 pay symbols on reel 1. (Decided by Michael and Efim)
- **Dragon Pays confirmed for South Dakota release**: Consistently #3 game, keeping it. (Confirmed by Juan, Michael)
- **Reporter ≠ Assignee in JIRA**: Efim to change reporter to Michael on his tasks. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Finish Twin Bison design, send to Michael for review | 2026-04-07 (Monday) | High | Blocks Lion's Riches concept art start |
| 2 | Lena Zhukova | Start Lion's Riches concept art (GC379) | 2026-04-08 (Tuesday) | High | Estimated 10 calendar days; new visual direction based on Twin Bison art style |
| 3 | Lena Zhukova | Close GC265 under IP882 | TBD | Normal | Accidentally left open; IP shows in-progress because of it |
| 4 | Efim Podvoiski | Finish Twin Bison math design (GD838) | 2026-04-03 | High | Play testing is a separate follow-up task |
| 5 | Efim Podvoiski | Change JIRA reporter to Michael on his tasks | TBD | Low | Reporter and assignee cannot be the same person |
| 6 | Lena & Michael | Review Wild Cold and La Rosa builds | 2026-04-02 (same day) | High | Build just became ready |
| 7 | Lena & Michael | Review liquid glass features (4 in request review) | 2026-04-02 (same day) | Normal | Attraction mode background still in progress |
| 8 | Val Levitan | Submit IT request for JIRA drag-and-drop ranking | TBD | Low | Unable to reorder items by dragging |
| 9 | Michael Gottlieb | Request QA begin testing Black Hills Kino Deluxe | TBD | High | New game type — QA team unfamiliar, needs early exposure |

## Engineering Signals

### Confirmed Signals

- **ADR: QA remains sequential to production in Rage Studio framework.** Val explicitly stated: "QA will always be sequential to production for as long as we stay with Rage Studio framework. I don't see how we can change it." In Omni, QA would shift to branch-integration-time testing with automated end-to-end tests.

- **REQ: Pre-build game shells for rapid comp art preview.** Val proposed that the game shell could be built before final art is ready, allowing designers to drop comp art into a running game and see it within minutes. Michael endorsed this. This can only be achieved in the Omni 2 architecture.

### Suspected Signals

- **Possible REQ: Automated animation generation from descriptions.** Val described a vision where you specify "30 frames, closed mouth to open mouth, evil look, specific dimensions" and the system generates the animation. Discussed aspirationally.

- **Possible ADR: Master file as the canonical design deliverable format.** The team established that the PSD master file (with storyboards) is the standard deliverable format from design to production. Current practice formally articulated.

## Open Questions

- Val expressed uncertainty about the 30-day visibility window for completed items on the JIRA board.
- Val said he still needs to work on understanding the JIRA stories structure.

---
*Processed from Teams transcript on April 11, 2026*
*Source meeting: Game Development (April 2, 2026, Segment 1)*
