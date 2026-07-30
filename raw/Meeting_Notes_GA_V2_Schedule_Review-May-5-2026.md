# Meeting Summary — GA-V2 Schedule Review
**Date:** May 5, 2026, 3:00 PM – ~3:54 PM Eastern
**Duration:** ~54 minutes
**Attendees:** Val Levitan, Lena Zhukova, Juan Martinez, Michael Gottlieb

## Summary

The meeting was a Jira-driven walkthrough of the Georgia Vertical (Georgia Quan) V2 release plan under initiative IP-446. Lena drove the screen share; Val pressed for clarity on each feature, owner, and sequencing. Juan and Michael chimed in selectively, with Michael speaking up at the end on design compromises.

**Replan context:** Lena opened by explaining she had just come out of a separate planning meeting earlier in the day and had reshuffled assignments. All Anastasiya tasks tied to Bison were pushed out to *after* this product ships, so Anastasiya is now fully dedicated to GA-V2. Lena and Michael have agreed to several design shortcuts so all art assets can be completed by **first week of June**.

**Top-screen attraction (6702):** Anastasiya will produce attraction-screen presentation animations for **8 games**. Each game gets its own animation that will appear on the home screen.

**V-deck variants (6716):** The V-deck has different proportions/space than the top screen, so for each game Anastasiya must recompose the resources — sometimes converting a 2-line logo to 1-line, dropping the main character (e.g. on Laros they used the rose only, no girl). Lena said three deck variants are needed: Lines and Waves, Jetpot Rush, and Fire Eyes Link.

**Home-screen progressive display (6042):** Lena + Julia produce assets, Anton integrates. Three different progressive meters (Fire Eyes among them); each progressive needs its own meter, font effect for value display, and text object placement. Built using GVL tools and the phone tool in Rage Studio's Scene Editor; some assets created in After Effects and registered as animated video materials. Val pushed Lena to estimate how much faster this will be in Miranda with the new manifest-driven DMAS automation — Lena said ~**30%**, which surprised Val ("That little, huh?"). Lena replied "I think it's a lot."

**Liquid Glass win celebration (5998):** Assets are already done — the new celebration was already integrated in South Dakota. Anton just needs to integrate it into the vertical version. The redesign was driven by the new Liquid Glass dashboard (the old win celebration was tied to the dashboard); Michael fed in review comments on coin/gem counts.

**Anton's start-date dependency:** Val drilled into the integration sequence and concluded Anton's task **6002** cannot start May 14 as planned, because Igor must first finish **6106** and **6111** (Igor must build the game shell so Anton has something to integrate against). Lena agreed in principle but noted the timing in the integration stories is placeholder — Anton and Igor will set their own exact timing once they put time in tomorrow. Val explicitly framed this as a "timing warning, but you can ignore it. It doesn't matter."

**Attraction assembly (6682 / 6683):** Anastasiya supplies the assets (rooster animation, logo animation, background animation); Dima (Dmitriy Khandov) does the first assembly story (6683) creating a template, then Julia uses that template to assemble the other three games. Val initially assumed only Dima could do assembly; Lena clarified the split was carefully discussed with Dima.

**Dima workload check:** Val filtered Jira by Dmitriy Khandov and challenged whether he was busy through end of May — pushing back that Lena was conflating **calendar days vs work days** when defending his load. Lena maintained Dima is fully booked: he's also leading the home-screen build, where comments and rework are expected. After May 26 he's intentionally unscheduled to absorb fixes.

**Symbol/coin work for IP-1053 (6065 / 6799):** This is the match-3 progressive bonus coin — a 3D double-sided element that needs to be adjusted, exported, and integrated per game (different size for each of the four lines-and-waves games). **Arthur** is doing this work because he learned fast on similar South Dakota symbols. Reporting structure: Arthur officially reports to **Pavel** (and Yuri Villavicencio asked Lena to set it up that way) — needs a Belarus-based assigner due to past problems with **Irina Okarak**. Lena: "It's a little bit artificial." Val: "Got it."

**3D coin asset (6746):** Julia creates the coin asset. One neutral side is a dollar sign; opposite sides depict three jackpot levels. Integration happens later in **6053** (Jetpot bonus integration).

**Bonus transition + messages (6053, 6060):** 6053 is the bonus and transition/message scene — Julia builds, Igor integrates. Val noticed a 2-day gap between 6053 and 6060 and questioned it; Lena explained 6060 is a separate scene (digital topper) that Julia can run in parallel — they're not strictly sequential.

**Game-level integration (IP993 etc.):** For each game the team needs scene adaptation, messages adaptation, pay table, help screen, then full integration. Reels are moving up because of the Liquid Glass dashboard and getting wider because side badges are gone; pay tables change because of the Liquid Glass middle section that promotes the match-3 bonus. Arthur and Natalia split scene/message adaptations (e.g., Critical → Natalia, Rogers → Arthur). **Vitaliy** does all helps and pay tables for all games.

**Calle Ocho (969):** Math was inserted by **Irina Makaric**, who is no longer with the company. Work is sitting in Request-Review status because nobody has been playing the game. Carries over from pre-New-Year work when Georgia was originally a separate project.

**Fire Jewels and Ruby Power:** Pulled from this release to start at end of June — these will follow once the first two games are done. Val noted that headings like 1057 still say "Georgia Quan V2 lions reaches" and need correcting; Lena agreed.

**Live restructure during the meeting:** Val instructed Lena to split IP-446 into two top-level initiatives — **Georgia Quan V2 Games Production** and **Georgia Quan V3 Game Production** — and move V2-only items (including Dmitri's work) into V2. Lena did this on screen and Val asked her to save.

**Closing exchange:** Val asked the room "who wants to say this is a better way and that Val was right?" — half-joking. Michael acknowledged design compromises were made to hit the date ("nothing is magic here … we had to change the design in order to get it faster") with the V3 release as the place to revisit choreography and special effects. Val wrapped with an anecdote about his Leo father never admitting Val was right.

## Decisions Made

- **Split IP-446 into IP-Georgia-Quan-V2-Games-Production and IP-Georgia-Quan-V3-Game-Production.** Reorganize V2/V3 work into separate initiatives; move all Dmitri-related items with V2. Executed live in Jira during the meeting. (Val, Lena)
- **Anastasiya is fully dedicated to GA-V2; her Bison tasks deferred until after GA-V2 ships.** Frees capacity to hit first-week-of-June asset target. (Lena, Michael)
- **Match-3 progressive bonus design simplified to hit the date.** Choreography and special-effects work deferred to V3 release. (Lena, Michael)
- **Fire Jewels and Ruby Power deferred** out of the V2 cut; will follow the first two games starting end of June. (Lena)
- **Arthur reports to Pavel** for IP-1053 coin work (formal Belarus-based reporting line). Reason: past issues with Irina Okarak; Yuri Villavicencio requested this structure. (Lena, endorsed by Val)
- **Dima does first assembly story (6683); Julia reuses the template for the remaining three.** (Lena, vetted with Dima)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Lena | Split IP-446 into IP-Georgia-Quan-V2-Games-Production and IP-Georgia-Quan-V3-Game-Production initiatives in Jira; move V2 stories (including all Dmitri items) into V2 | Live in meeting / save immediately | High | Val asked her to save during the meeting; foundational restructure before the rest of the schedule is meaningful |
| 2 | Lena | Fix incorrect feature headings that still reference V3-only games (e.g., 1057 reads "Georgia Quan V2 lions reaches") so titles match the V2/V3 split | TBD (next planning pass) | Normal | Caught by Val while reviewing the schedule; clean labeling needed for the new initiative split |
| 3 | Anton + Igor | Self-time their integration stories (6002, etc.) once Igor's game-shell stories 6106 and 6111 are scoped — confirm whether 6002 truly slips from May 14 to following Monday | Tomorrow / next day per Lena | Normal | Val's timing warning: 6002 can't start May 14 because Anton needs Igor's first game assembled first. Lena said this is a placeholder and the two engineers will set real timing |
| 4 | Igor | Finish remaining South Dakota items, then begin GA-V2 work (6065 coin) on Monday | Monday May 11, 2026 | Normal | Lena confirmed Igor is not ready to start tomorrow; needs to clear South Dakota first |
| 5 | Lena (with Michael) | Land all GA-V2 art assets | First week of June 2026 | High | Hard target driving the whole schedule; assumes Anastasiya-shuffle and design shortcuts hold |
| 6 | Val | Sign off on the new V2/V3 initiative split once Lena saves it | After Lena saves | Normal | Val drove the split; should verify the Jira state matches what was discussed |

## Engineering Signals

### Confirmed Signals

- **ADR — Split GA Vertical scope into V2 and V3 release tracks:** Val explicitly directed the IP-446 initiative be split into two top-level initiatives (V2 Games Production, V3 Game Production). Rationale: V2 must hit first-week-of-June art-asset deadline; V3 absorbs deferred features (Fire Jewels, Ruby Power, choreography work).
- **ADR — Match-3 progressive bonus design simplified for V2; full choreography deferred to V3:** Michael stated explicitly: "We had to change the design in order to get it faster. We still have the vertical 3 to come back around with the additional games and we can continue to work on the choreography and the special effects with it."
- **CAP — Liquid Glass dashboard / win celebration / home screen:** Already shipped in South Dakota; being ported to GA-V2. Drives ripple changes (reels move up, reels widen, pay-table middle section promotes match-3 bonus, win celebration decoupled from old dashboard).
- **Solution — Belarus-based assigner workaround for Arthur:** Arthur's reporter set to Pavel (per Yuri Villavicencio's request) so task assignments come from Belarus. Workaround for past issues with Irina Okarak.

### Suspected Signals

- **Possible CAP — Manifest-driven DMAS automation in Miranda:** Lena cited ~30% production acceleration via "new DMAS achievements with manifest." Val seemed underwhelmed by 30%. Worth tracking as an explicit capability/tooling requirement?
- **Possible REQ — V-deck recomposition rules per game:** Lena described concrete patterns (1-line vs 2-line logos, drop main character, three deck families: Lines & Waves / Jetpot Rush / Fire Eyes Link). This sounded like an emergent requirement set, not currently formalized.

## Open Questions

- Will Anton actually slip from May 14 to following Monday, or can he start parallel work? Resolves once he and Igor put real timing on integration stories.
- Calle Ocho (969) sitting in Request-Review with no playtests — who picks up validation now that Irina Makaric is gone?
- Vitaliy's pay-table / help-screen workload across all games — implied owner but not drilled into.

---
*Processed from Teams transcript on 2026-05-05.*
*Source meeting: GA-V2_schedule-May-5-2026*
