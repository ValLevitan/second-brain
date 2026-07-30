# Meeting Summary — Game Development Schedule Review

**Date:** 14 May 2026, 7:33pm Eastern
**Duration:** ~24 minutes
**Segment:** 1 of 2 (Jira schedule walkthrough — preceded the lineup discussion)
**Attendees:** Val Levitan, Michael Gottlieb, Lena Zhukova, Juan Martinez, Efim Podvoiski

## Summary

Val drove a live walkthrough of the Jira game-development schedule with Lena, Michael, Juan, and Efim, working IP by IP to clean up statuses and confirm dates.

**Solar Keno (IP 882 / GC 263).** Michael is writing the abstract; Lena is starting comp art. Theme positioned as JVL's answer to the IGT Keno game "Da Vinci Diamonds," leaning on current public interest in Artemis/UFOs/aliens and the natural contrast of planets against starfields. This will be the first vertical Keno product for South Dakota.

**Georgia Vertical (IP 535).** Val asked whether this should move from "In Progress" to "Done/Released." Michael and Lena confirmed — V1, V2, and V3 for Church are finished. Val closed it on the board.

**Game Design pipeline.** Nothing currently in game design — the previous wave just wrapped. Next wave (South Dakota / Nebraska / Texas vertical) is what's spinning up. Game Concept currently holds only South Dakota VLT.

**South Dakota VLT — Game Production (IP 459).** Lena reported very good progress on the South Dakota titles (Black Inna through Clover Fortune Dawn). A fresh build was sent to Michael today with small changes from Vlad and timing tweaks from Anton — these are in final review. Michael publicly thanked the engineering team, calling out the work on Cool Cat Keno as especially difficult ground for the studio (first Keno product) and praising their execution.

Remaining work on Lena's side: minor items in Kovalchuk and assembly of the home-screen attraction mode (all game demo videos need to be added). Igor will integrate the attraction-mode videos into the home screen the week of May 18 — this is not a simple insertion task; he will spin it up as its own work in his space and start Monday.

**IP 1056 due date concern.** Michael flagged that IP 1056 showed "due tomorrow," which couldn't be right since the home-screen video integration won't be done by then. Lena clarified the *story scheduled* there (Julia assembling the scene from recorded videos) will be done tomorrow; the *integration into the home screen* sits on Igor's side and he'll create his own task for that work starting Monday.

**IP 1063 — Pick to Win universal interactive bonus.** Lena explained per Pavel/Irina this should not slip to July. It's a bonus that must be added to each game to qualify for the media tax credit. Igor will tackle it in mid-June after wrapping the Giorgi work; assets are ready, only programmer time is needed. That's why it currently sits in "To Do" with a later date.

**South Dakota VLT release date.** After confirming Lena's portion can be done effectively next week and Pick-to-Win sits to the side, Val pushed the South Dakota launch to **June 10** with Lonnie (compliance/test lab). Juan will set wheels in motion. Juan noted they may be able to do pre-testing in the office with Denis if Lonnie permits — he is working that angle.

**Cool Cat Keno — operator validation.** Michael asked Juan to get Black Hills and Cool Cat Keno in front of a real Keno player before launch. Michael said he is in final tuning (pacing, timing, three speed settings adjustable to player preference). He noted JVL's rack times are slightly longer than competitors' but is comfortable with that — high wins aren't frequent, and players can snap the meter by pressing play. He prefers rack timings closer to slot machines. Juan confirmed Lena had sent the software ISO; Denis already has it but is in Nebraska this week. The general manager at 77 Casino (a Keno expert per the weekly competitor report) has agreed to come to the office — Juan is targeting end of next week to install and get her feedback. Michael then asked Lena to issue a fresh ISO including the latest Cool Cat and Black Hills tweaks; Lena will ask Ivan, expected Monday (note Monday May 18 is Victoria Day — Canadian holiday).

**Giorgi V2 Game Production (IP 446).** In progress: liquid glass home screen, Match the Progressive bonus, Rodeo Spins game, Crazy Cold, Lions Riches game, Kovalchuk work. Lena's primary goal for next week is to hand Igor a workable (not final) home screen with game buttons and at least one game's assets from each of the three categories — Fiery Ice Link, Jackpot Rush, and Lines and Ways — so Igor can run a first build with all three categories.

**Queen of Luxor math.** Val asked Efim whether he had started; Efim had started but hadn't moved the ticket to In Progress. Val pushed him to update the status. Lena will move the parent IP to In Progress accordingly.

**IP 1053.** Val flagged it should be in To Do, not In Progress. (Lena initially said it was correctly in progress; appears to have been resolved in-call.)

**Match 3 Progressive Bonus Button (story 6746 / AA-6746).** Not scheduled because all work was done — Lena had simply forgotten to close it. They closed it together on-call (refreshing twice to clear the "review request" state); once closed the timeline dropped off the schedule view automatically.

**Sparkle Seven, Sapphire, Rodeo Queen.** Schedule confirmed correct. Val: "no holes" — nobody saw gaps.

**Clayton meeting cancellation / automation rollout.** Val asked why today's Clayton meeting was cancelled — Lena said back injury, can't sit. Val joked Clayton could work standing. The "piece of automation" Lena has been validating in sandbox is not yet live; Clayton cancelled two meetings, expected to recover and go live Tuesday next week. Lena likes how it works in sandbox but can't quantify time savings yet — she needs real usage for a couple of weeks. Val confirmed this will benefit the other girls on the team too, expecting cumulative time savings.

## Decisions Made

- **IP 535 (Georgia Vertical) closed as Done/Released** — V1/V2/V3 for Church are complete. (Val, with Michael and Lena's confirmation)
- **South Dakota VLT launch pushed to June 10 with Lonnie** — Lena's portion is effectively complete next week; Pick-to-Win bonus is parallel and won't block. (Val)
- **Story 6746 (Match 3 Progressive Bonus Button) closed** — all underlying work done. (Val/Lena, on-call)
- **Fresh ISO with latest Cool Cat Keno and Black Hills builds to be cut Monday May 18** — for operator validation by the 77 Casino GM. (Michael, executed via Lena → Ivan)
- **Igor begins home-screen attraction-mode integration Monday May 18** — handled in his own task space, not part of Julia's video assembly story. (Lena)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Michael | Continue writing Solar Keno (IP 882) abstract | Ongoing | Normal | First vertical Keno product for South Dakota |
| 2 | Lena | Start Solar Keno comp art | Ongoing | Normal | Parallel to Michael's abstract |
| 3 | Julia | Assemble attraction-mode scene from recorded game demo videos | May 15 2026 | Normal | Feeds Igor's home-screen integration |
| 4 | Igor | Integrate attraction-mode videos into home screen | Week of May 18 2026 | Normal | Creates own task in his space; not insertion-only work |
| 5 | Igor | Implement Pick-to-Win universal interactive bonus (IP 1063) across games | Mid-June 2026 | High | Required for media tax credit qualification; assets ready |
| 6 | Juan | Set wheels in motion to schedule South Dakota VLT testing with Lonnie | June 10 2026 | High | Locked launch date |
| 7 | Juan | Continue working with Lonnie on possible pre-testing with Denis at office | Before June 10 | Normal | Could save time if Lonnie agrees |
| 8 | Lena → Ivan | Cut fresh ISO with latest Cool Cat Keno + Black Hills builds | Monday May 18 2026 | High | Replaces ISO Denis already has; needed for operator validation |
| 9 | Juan | Tell Denis to hold off installing current ISO; install new one when delivered | May 18+ | Normal | Avoids wasted work |
| 10 | Juan | Coordinate with Denis to install ISO and invite 77 Casino GM to office for Cool Cat Keno feedback | End of week May 22 (target) | High | Keno expert validation before launch |
| 11 | Lena | Deliver workable (non-final) home screen to Igor with game buttons + sample assets from all 3 categories (Fiery Ice Link, Jackpot Rush, Lines and Ways) for Giorgi V2 | Week of May 18 2026 | High | Unblocks Igor's first build with all 3 categories |
| 12 | Efim | Move Queen of Luxor math to In Progress in Jira | Immediate | Normal | Already started, just untracked |
| 13 | Lena | Move parent IP for Queen of Luxor to In Progress | Immediate | Normal | Follows Efim's status update |
| 14 | Lena | Validate Clayton automation in real-use scenario | Tuesday May 19 2026 onwards | Normal | Go-live after Clayton recovers from back injury; quantify time savings over ~2 weeks |

---
*Processed from Teams transcript on 2026-05-14 — filed as historical data, no dispatch.*
*Source meeting: Game_Development-20260514_153314-Meeting Recording (segment 1 of 2)*
