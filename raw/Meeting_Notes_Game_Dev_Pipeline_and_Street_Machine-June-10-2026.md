# Meeting Summary — Game Development
**Date:** June 10, 2026, 8:02 PM Eastern
**Duration:** ~1h 6m
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Juan Martinez, Efim Podvoiski

## Summary

**Jira hierarchy / "where do the game lists live."** Val pushed hard on one rule: if it's not in Jira, it doesn't exist in his world — no side lists in Confluence or in Michael's personal notes. Michael keeps a top-level list of games per release; Val wants that to live inside the Jira hierarchy instead. They landed on a working rule: approved-but-not-yet-started product can sit in **backlog inside the concept phase**, so everyone sees what's coming. Everything must pass through the concept phase — no skipping, even for near-identical reworks, because the team needs a documented "known good and approved" version of each game (especially with all the liquid-glass conversions and variations).

Val also walked through his target taxonomy out loud (capability → feature → deliverable, with features as GitHub artifacts) but said he was "philosophizing," not directing. The team debated GC vs GD labels and IP-per-game vs IP-per-market. Lena prefers a separate IP per game because it matches how production works. Val told Juan **not** to build a "liquid glass" capability yet — the capability-in-hierarchy idea is still being tested.

**Release pipeline** (Michael posted the schedule to chat):
- **Georgia Vertical 2** — almost done; liquid glass + match-3 progressive; 8 games. Submitting to Eclipse around June 15, possibly slipping to the 17th–19th. Guys were pulled off South Dakota D2702 to finish this.
- **South Dakota D2702** — almost done; 8 games including 2 Kinos (Cool Cat Kino, Black Hills Kino Deluxe) + 6 conventional. Upgrading the 60+ install base. QA moves to it after Georgia V2; lots of bugs, especially Kovalchuk. Still needs Keno-player feedback.
- **Georgia Vertical 3** — ~October. Cleanup of V2 plus more games: new Bison, updated Lions Riches and Queen of Luxor graphics (Lions & Waves); +2 in Jackpot Rush (Ruby Power, Fiery Jewels); +3 in Fiery Ice Link (La Rosa, Crescent City Carnival, Tropical Paradise). Extra games available in background, not all enabled.
- **Nebraska D2702** — was slated for January, which Val called "not good." Reordered to start right after Georgia V3, ahead of South Dakota Vertical 1. Games: Lions Riches Wild Colt, Clover Fortune, Dragon Pays, the two top performers from Nebraska D2701, plus Cayocho, Rodeo Queen, Sapphire Star, Sparkle 7.
- **South Dakota Vertical 1** — 3 vertical Kinos (Black Hills Kino Deluxe, Cool Cat Kino, Solar Kino) + 6 Lions & Waves games (Lion Riches, Wild Colt, Dragon Pays, Midnight Money + 2 new: Aaron's Pub, Dakota Bison, replacing 2 underperformers). Needs a cabinet submitted to the regulator, so it carries an external delay.

**Texas.** Val is no longer opposed to a dedicated Texas-themed game (Lone Star — a Golden Husk re-skin that's mostly already built). Texas will follow the Nebraska skill but on its own timeline, since Texas needs no regulatory approval and can carry software changes Nebraska can't. Val stressed he's giving no creative direction here.

**Street machine (single-screen vertical "street" cabinet).** Val laid out the design direction: single vertical screen, Rockchip platform (in testing now), max 6 games but WiFi + cellular to download games, external progressive controller to drive a full bank as a "video wall." Hardware: 8-button deck (1 slam, 5 bet, 2 service), drink-holder space, dashboard (player tracking, validator, printer) relocated below the vertical panel to kill the big insert, screen lowered ~4–5" with a slight "iPhone-ish" tilt, one clean line from M-deck to screen. Dropping the dedicated amp and subwoofer; mid-range speakers mounted below firing upward. Target: September. Michael is firmly on board ("just because you can doesn't mean you should"; cited Clover Fortune as proof simple games perform).

## Decisions Made

- **Approved backlog product may sit in the concept phase (in backlog)** even when not actively worked on, so the team sees what's coming. (Val, endorsed by Michael)
- **Everything passes through the concept phase — no skipping steps.** Reason: documentation of the "known good and approved" version of each variant. (Michael, agreed by Efim and Val)
- **No standalone game lists outside Jira.** Everything lives in the hierarchy with a path to a GitHub artifact. (Val)
- **Do not create a "liquid glass" capability yet** — capability-in-hierarchy still being tested. (Val → Juan)
- **Reorder pipeline: Nebraska D2702 moves ahead of South Dakota Vertical 1**, starting right after Georgia V3. (Val + Michael)
- **A dedicated Texas-branded game (Lone Star) is acceptable**; Texas follows Nebraska on a separate timeline. (Val, Juan)
- **Lena's reprioritization approved:** Queen of Luxor V3 graphics → Nebraska D27 → South Dakota vertical. (Michael)
- **Street machine direction set** (single vertical screen, Rockchip, 6 games, WiFi/cellular, video-wall progressive, relocated dashboard, no amp/subwoofer). Target September. (Val, supported by Michael)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena Zhukova | Send Val a reviewable build/ISO of Georgia V2 with all multi-games assembled | ~Mon June 15 | High | Needed before Eclipse submission; Windows build currently painful |
| 2 | Juan + engineers | Submit Georgia Vertical 2 to Eclipse | June 15, slip to 17–19 | High | Depends on engineers finishing fixes; status checked hourly |
| 3 | Lena Zhukova | Work in order: Queen of Luxor V3 graphics → Nebraska D27 → South Dakota vertical | TBD | High | Reprioritization approved by Michael; V3 graphics urgent |
| 4 | Michael Gottlieb | Put Nebraska Skill D2702 game list into concept-phase backlog, with Georgia and other approved product | TBD | Normal | Satisfies Val's "everything in Jira" rule |
| 5 | Juan Martinez | Reconcile IPs 1071 & 1072 into the agreed game-concept (GC) structure | TBD | Normal | Juan created them as IPs; aligning on GC for concept stage |
| 6 | Juan Martinez | Get Keno-player feedback on South Dakota D2702 | ~June 11 | Normal | One reviewer came in today; Denis flies back Friday |
| 7 | Juan Martinez | Continue Lonnie / Light & Wonder talk re: in-office self-testing of the SD vertical cabinet | TBD | Normal | Could work out bugs before sending prototype to regulator |
| 8 | Juan / Michael | Build out the South Dakota Vertical 1 cabinet schedule in Jira Plans | TBD | Normal | Val wants the regulatory submission path visible, not speculative |
| 9 | Juan Martinez | Create a Texas Skill game concept for the vertical project | TBD | Low | Mirrors Nebraska; separate timeline |
| 10 | Val Levitan | Action Michael's proposed reschedule of game-dev meetings | TBD | Normal | Michael on vacation the next couple of weeks |

## Open Questions

- **Jira taxonomy unsettled:** GC vs GD stage labels, IP-per-game vs IP-per-market, and whether to keep stages at all. Val suggested consulting more knowledgeable people; Lena prefers IP-per-game.
- **Street machine button deck:** mechanical buttons vs. keeping haptic feedback / a V-deck — undecided ("not 1,000,000% yet"); Val remains a "big advocate of feedback."
- **Street machine lighting:** perimeter lights vs. halo lighting — Val asked for a "vote," unresolved.
- **Lone Star scope:** just a Golden Husk re-skin, or a fully separate Texas progressive? Leaning re-skin since assets are mostly done.
- **South Dakota D2702 release date:** not firmly set; pending QA (after Georgia V2) and Keno-player feedback.

---
*Processed from Teams transcript on June 11, 2026*
*Source meeting: Game Development — June 10, 2026*
