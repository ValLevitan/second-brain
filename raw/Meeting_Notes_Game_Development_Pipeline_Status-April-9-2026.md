# Meeting Summary — Game Development (Pipeline & Design Status)
**Date:** April 9, 2026, 6:08 PM Eastern
**Duration:** 15m 26s
**Segment:** 1 of 3
**Attendees:** Michael Gottlieb, Val Levitan, Lena Zhukova, Efim Podvoiski, Juan Martinez

## Summary

**Wolfpack slot addition.** Michael opened by telling the group he informed Lena that the company is sliding in an additional slot title called **Wolfpack** on the strength of excitement around Twin Bison. The abstract is complete, and Lena has started on comp art and game symbols. Lena reacted positively when Michael pitched her the idea. The project breakdown under **GC384** is: **GC386** (Wolfpack game concept art) consisting of **GC387** (main screen comp art) and **GC388** (game symbol). After Wolfpack, the art pipeline will move to **GC364 Lion's Riches update**, which consists only of **GC379** (updated screen comp art) because it's an already-released game being refreshed.

**IP 1029 Twin Bison design status.** Lena reported she has finished the art portion of Twin Bison design (IP 1029). A math feature is still in progress. Efim said he will finish the math "today or tomorrow" on design time, with play-testing to follow as a separate task.

**Rodeo Spins math tuning (mistakenly discussed under Twin Bison).** Michael launched into a detailed update on **GD 838 (Rodeo Spins)** — which he mid-stream realized he had been describing while the group thought he was talking about Twin Bison. For Rodeo Spins: he and Efim found the low-pay symbol on reel one was triggering too often, killing anticipation and feeling repetitive. They rebalanced the lowest three pays for greater variety, and Michael played the revised version and agreed it is a superior experience. They also tried wilds on reel one and rejected the change — it didn't work. Michael emphasized the short iteration cycle: Efim sends a file, Michael file-swaps into the build, and they can play-test in a very short period, no full builds required.

**Twin Bison volatility target.** Val asked what market the Twin Bison math targets and what volatility profile. Michael called it **medium volatility**, drawing from the Lions Riches win profile rather than duplicating it. He explained the design philosophy: other JVL games have "win profile bumps" and high multiples of bet way out on the tail, and those games underperform. Lions Riches brings the high pays into the middle of the profile, which resonates better with players. Efim confirmed medium: no huge wins, hit rate around 5 closer to 6, with room to adjust at this early stage. Michael framed the principle as **the $20 test** — a player needs enough "gasoline in the tank" to get across the desert with their $20, otherwise huge far-out wins are never seen. He cited **Liberty Spins** as a counter-example: nice crushing wins out on the tail, but the game isn't performing — the EV is hanging too high in the profile.

**Design-stage items moving to production.** Lena reported that **Lion's Riches** design is in backlog and will move to "in progress" once the concept is ready. **IP 1030** (Lions Riches for Georgia) and **IP 1031** (March 3 progressive bonus for Georgia release) have finished design and moved to production.

**Production status and South Dakota VLT 2 build review.** Lena reported production is focused on **IP 459**. Recently closed: **IP 988 La Rosa**, **IP 984 liquid glass home screen** — all liquid glass work for home screen is done. The only remaining liquid glass item is attraction videos for games, which can only be recorded once a proper ticker is implemented in all games. Michael reviewed the South Dakota VLT 2 build: making good progress, in the tuning/tweaking phase for **La Rosa**, **Wild Cole**, **Lion's Riches**. **Rodeo Spins** looking good. **Black Hills Kino** getting close, a few items remaining. **Cool Cat** just getting started. **Dragon Pace** still to do.

**Dragon Pace and Cool Cat implementation challenges.** **IP 997 Dragon Pace** has been restarted. Cool Cat keno progress is visible in the build but not properly playable yet — Anton has not inserted playing for free games. Efim explained Anton is struggling: the work is more than he anticipated. Anton is at the stage of inserting the selection scheme and hit a framework issue — he and Igor didn't initially realize the selection-bonus logic used across slot games cannot be reused for keno because it is tightly coupled to slot-game design in the existing framework. Anton effectively has to reinvent it. Michael added that **Black Hills Kino** was straightforward, but **Cool Cat** is complicated — the team is trying to be competitive against Squish, which means combinations, permutations, and complex sequencing of stacked free-games triggers and multipliers. Michael flagged Cool Cat will need substantial QA support.

**Peek-to-be-in bonus / major tax credit initiative.** Lena announced that in **Dragon Place** (the last slot game in South Dakota), they inserted a "peek-to-be-in bonus" interactive feature — an artificial interactive feature that now needs to be inserted in **all slot games** so that every title has an interaction feature in its bonus. The logic is based on the approach used previously in Hit Games products. The purpose is to qualify all games for "major tax credit" (CAVCO/interactive-content tax credit qualification implied but not named).

**IP 996 Clover Fortune free spins.** Michael noted Clover Fortune has seen a popularity increase. Juan said the report showed increased popularity in March vs February; Efim considered the increase only marginal. Michael confirmed **IP 996** Clover Fortune has free spins added for the next release. He played it heavily — the EV of the free spins is solid, the hit rate is solid, and the feature is kept traditional. The mechanic: when the star symbol hits, each adds additional free spins, sometimes accumulating to 25–27 or 30 free spins, plus an expanding wild. Michael's position: they are enhancing a popular game while being mindful that changing a beloved title can backfire. Lena noted Clover Fortune was the only game in the subtle-games lineup without free spins previously. Michael added a demographic aside — players from that era of game may be in their late 70s or 80s.

## Decisions Made

- **Wolfpack slot will be added to the pipeline** between Twin Bison and the Lion's Riches update. (Decided by Michael; endorsed by Lena's positive pitch reaction)
- **Twin Bison volatility profile is medium**, modeled on Lions Riches' win profile shape (EV concentrated in the middle, not on the high-pay tail). (Michael and Efim)
- **No wilds on reel one in Rodeo Spins** — tested and rejected. (Michael and Efim)
- **Rodeo Spins lowest three pays rebalanced for variety** — confirmed as a superior experience. (Michael and Efim)
- **Peek-to-be-in bonus feature will be inserted into all slot games** (based on the Dragon Place implementation and prior Hit Games logic) to qualify the catalog for major tax credit. (Lena)
- **IP 996 Clover Fortune will ship with free spins added for the next release.** (Michael)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim Podvoiski | Finish Twin Bison (IP 1029) math design work | April 10, 2026 (today or tomorrow) | High | Unblocks play-testing; Twin Bison is the lead title driving the Wolfpack decision |
| 2 | Lena Zhukova | Continue Wolfpack art: GC387 main screen comp art and GC388 game symbol under GC386 | TBD | Normal | Wolfpack was added to the pipeline on the strength of Twin Bison excitement |
| 3 | Lena Zhukova | Move Lion's Riches design (GC364/GC379) forward once Wolfpack comp art wraps | TBD | Normal | Lion's Riches is an already-released game being refreshed, smaller scope |
| 4 | Anton (external — flagged for clarification) | Implement keno selection-scheme logic for Cool Cat (must reinvent, cannot reuse slot framework) | TBD | High | Blocking Cool Cat playable build; framework coupling issue must be solved before QA can engage |
| 5 | QA team | Plan substantial QA coverage for Cool Cat (combinations, stacked free-games, multipliers) | TBD | High | Michael flagged this title as the most complex in the South Dakota VLT 2 build |
| 6 | Development team (unspecified owner) | Implement peek-to-be-in bonus interactive feature in all remaining slot games, following the Dragon Place pattern and Hit Games logic | TBD | High | Required for all-games qualification under major tax credit — catalog-wide scope |
| 7 | Development team (unspecified owner) | Implement proper ticker in all games so attraction videos for the liquid glass home screen can be recorded | TBD | Normal | Last remaining item for IP 984 liquid glass home screen |
| 8 | Juan Martinez | Continue monitoring Clover Fortune (IP 996) popularity data to verify March uplift is real | Ongoing | Normal | Disagreement between Juan (sees real uplift) and Efim (sees marginal change) — more data will resolve |

## Engineering Signals

### Confirmed Signals

- **Engineering Solution — Iterative math tuning via file-swap:** Michael confirmed the tight iteration workflow used by him and Efim — Efim sends a balance file, Michael swaps it into the build, plays, and gives feedback, all without a new build. This is the established development practice for math balancing.
- **CAP (Capability) — Peek-to-be-in interactive bonus as a cross-catalog capability:** Lena declared that the peek-to-be-in bonus feature "needs to be inserted now in all slot games to have interaction feature in all bonus." This is a capability requirement across the slot catalog, driven by tax-credit qualification.
- **ADR — Keno selection framework must be reinvented, not reused:** Efim stated that the selection-bonus logic for slot games "cannot be used in Kina because it's coupled with slot games design" and that Anton "has to reinvent it." This is an architectural decision arising from a discovered coupling violation in the existing framework — keno needs its own selection-scheme implementation.

### Suspected Signals

- **Possible ADR — Win profile shape as a design principle:** Michael articulated "the $20 test" and the principle that EV should be concentrated in the middle of the win profile rather than on the high-pay tail. This sounds like a design rule the team is consistently applying (with Liberty Spins as a failure case and Lions Riches as the positive reference).
- **Possible REQ — Tax credit qualification drives feature scope:** The "major tax credit" qualification is being used as a business driver for feature inclusion (peek-to-be-in bonus catalog-wide).

## Open Questions

- **Texas / Georgia market customization details for Rodeo Spins and related titles** — raised in passing ("Georgia belt buckle" precedent) but deferred to the deployment segment.
- **Who owns catalog-wide rollout of peek-to-be-in bonus** — Lena announced the requirement but did not assign an owner for the other games. (Michael Gottlieb)

---
*Processed from Teams transcript on April 13, 2026*
*Source meeting: Game Development — Segment 1 (April 9, 2026, 6:08 PM)*
