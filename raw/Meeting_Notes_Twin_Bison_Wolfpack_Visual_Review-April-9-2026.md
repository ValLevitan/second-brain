# Meeting Summary — Game Development (Twin Bison & Wolfpack Visual Review)
**Date:** April 9, 2026, 6:24 PM Eastern
**Duration:** 6m 52s
**Segment:** 2 of 3
**Attendees:** Michael Gottlieb, Val Levitan, Lena Zhukova, Efim Podvoiski, Juan Martinez

## Summary

**Twin Bison free spins flow walkthrough.** Lena shared her screen and Michael narrated the Twin Bison free-spins flow from a presentation mockup. Sequence: the player lands three free-spin symbols; the free-spin symbol swells up; the transition plays with a **white running bison**; the player enters the free spins feature. The feature offers **10 free spins with locking bison**. A critical qualifier: **bisons unlock when participating in a line win**. Michael explained the reasoning — normally a locking wild stays locked for the duration of free spins, but because the bison is a high-pay symbol occupying a 3×3 block, keeping it fully locked would be game-breaking. The qualifier is an explicit player-facing message so the behavior is clear. Michael noted he debated this internally before bringing it to Efim and Juan.

**Free-spins exit transition.** After the free spins award their credits and a message displays the credits won, the player returns to the main game. Lena's design shows a snow/blizzard effect on the way back out. Michael agreed: on entry, entertain the player; on exit, it's about the money — no need to extend entertainment.

**Val's feedback on the exit transition (not adopted, debated).** Val liked the inbound transition (brown/summer theme → white/frost theme, snow effect). On the outbound transition, however, he argued the effect should be **a sun / melting / defrosting effect**, not snow, because the player is moving from frost back to the warmer main-game theme. Lena pushed back: the main game itself already uses snow and a frozen effect on the frozen vial, so the main game is not a summer scene. Val clarified he did not mean "summer" literally — he meant the visual opposite of frost, i.e., a defrosting effect. He framed his input as "$0.05, do whatever you want with it." Michael accepted the feedback as noted ("fair enough, thank you") without committing to a change. Val explicitly disclaimed wanting to become the game's producer.

**Locked bison look.** Efim asked to see the locked bison in the presentation. Lena showed it in the transition. Val praised the frozen bison symbol and called the "frozen symbol" concept a great one he has not seen used before.

**Wolfpack parallels and differences.** Val asked whether wolves in the upcoming Wolfpack title would also freeze the same way. Michael and Lena clarified: **wolves will lock but not freeze**. Lena's intended visual approach for Wolfpack's locked wolf is a different effect — she wants to use a **moon and howling wolf** motif rather than frost. She is open to adding a frosted treatment around the moon/wolf if the team prefers, so she flagged this for discussion. Michael added that wolves will **howl on line wins** when locked ("you can't have wolves that don't howl"). Val's suggestion: if Lena does add frost to the wolf, reusing the same in/out transition from Twin Bison would be efficient.

**Coyote vs. wolf clarification.** Val asked whether the "dog-looking thing" on screen was a wolf or a coyote. Michael confirmed **coyote**. Brief tangent about coyotes in both Michael's and Lena's backyards / parks and their predatory behavior toward pets.

## Decisions Made

- **Twin Bison free spins: 10 free spins with locking bison; bison unlock when participating in a line win** — player-facing qualifier will be shown for clarity. (Michael, with Efim and Juan agreeing)
- **Exit transition from Twin Bison free spins stays snow/blizzard back to main game** — Val's "defrost/sun" suggestion was noted but not adopted; Lena's rationale (main game is also frost-themed) prevailed. (Lena, with Michael agreeing)
- **Wolfpack locked wolf will not use a frozen effect** — Lena's direction is a moon-and-howl motif instead. (Lena; final direction deferred for internal discussion)
- **Wolves will howl on line wins when locked in Wolfpack free spins.** (Michael)
- **The "dog-looking thing" in the art is a coyote, not a wolf.** (Michael, confirming existing art intent)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Finalize Wolfpack locked-wolf visual treatment — decide between moon/howl-only vs. moon/howl with frosted treatment around it | TBD | Normal | Visual direction affects whether the Twin Bison in/out transition can be efficiently reused |
| 2 | Lena Zhukova | Include locked-bison visual in future presentations so reviewers can see it in context | Next presentation | Low | Efim requested; improves review efficiency |

## Engineering Signals

### Confirmed Signals

- **CAP (Capability) — Conditional unlocking wilds in free spins:** The "bison unlocks when participating in a line win" mechanic is an explicit capability the slot framework must support — locking-wild behavior that is contingent on line-win participation, not permanent for the feature duration. This capability is specifically designed to accommodate high-pay symbols occupying multi-cell blocks.

### Suspected Signals

- **Possible CAP — Transition-reuse / asset-library pattern:** Val's suggestion that Lena reuse the Twin Bison in/out transition for Wolfpack if she adds frost is an implicit argument for shared transition assets across themed titles.

## Open Questions

- **Final Wolfpack locked-wolf visual direction** — Lena and the team have not committed. (Lena Zhukova to resolve)
- **Whether Val's defrost-effect feedback will be revisited** — Michael said "fair enough" but did not confirm a change or a closed-out "no". (Michael Gottlieb)

---
*Processed from Teams transcript on April 13, 2026*
*Source meeting: Game Development — Segment 2 (April 9, 2026, 6:24 PM)*
