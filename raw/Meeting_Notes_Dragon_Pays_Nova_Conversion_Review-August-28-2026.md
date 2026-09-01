# Meeting Summary — RAGE_NOVA_conversion_update (Dragon Pays Nova Conversion Review)
**Date:** August 28, 2026, 9:02 AM – 9:39 AM Eastern
**Duration:** ~37 minutes
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski

**Raw transcript:** [[Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026]]

## Summary

Igor Metelski showed the result of porting the Dragon Pays game from the old Rage platform (the South Dakota / "Cota" horizontal-screen product) to the new Nova / Omni platform. The task was to move the game logic and math and the resources, so that a Dragon Pays machine on the new platform looks and behaves the same as the old one.

Igor reported the port is largely working. Efim supplied the real Dragon Pays math, and the game now runs on it. Igor ported the main scenes — base game and free spins — on both the main and the extended (second horizontal) screen, plus the messages and transitions, the dashboard, the help pages, and the resources and text. On screen the reels spin, payouts are credited to the balance, the money-format toggle works on both the dashboard and the meter, tickers and line highlights work, the celebration animation plays, the transition into free spins works, the locked-wilds feature works, and the progressive is drawn and credited to the balance — all checked against the real math responses.

Effort: about two weeks since the last meeting, but as background work, not full-time — Igor kept other LGS tasks going at the same time. Some of that time was one-time work (the Rage-to-Omni converter scripts, which are reusable). At one point Claude deleted a week of local changes: Igor had asked it not to push to the Omni submodule, and Claude over-applied that rule and wiped the framework and game changes too; Igor rebuilt the state from his records in about half a day. Igor also spent time modifying LGS for mystery progressive, but is unsure those test changes should be merged and thinks the LGS team should add that support properly (Val set this aside for today).

Completeness estimates differed: Pavel ~85%, Irina 95%, Igor cautioned there is still a fair gap versus the Rage games. Still outstanding: the risk feature; the game-select / "day selection" multi-game screen (never tried on Omni — needs a second horizontal Omni game to test with); some graphics nuances (wild/scatter label formatting, reel spin timing carried over from a different implementation); the jackpot-winner scene, which is reused from the Omni build rather than ported from Rage; slightly incorrect restore into free spins; and sound, which is placeholder (audio is driven by a separate LGS server and can be swapped later). On Windows it runs smoothly at ~60 fps, with some lag on a big win with many coins; the heavy full-screen celebration video is resource-heavy, the same as on Rage. The team wants to build it and test on a real machine.

The larger discussion was QA. Val's view: the Rage-to-Nova transition is the ideal moment to write requirements and acceptance criteria and keep the prose in the repository next to the code, so that Claude can generate and run the tests itself against acceptance criteria. Val called QA/CI the bottleneck — if it is solved, the migration can move very fast; if not, the speed gained on the port is worth nothing. Since the code and prose already exist, he wants to reverse-engineer the requirements and acceptance criteria from the prose, the code and the KPIs, working back through the overall architecture. Pavel's concern: animation dynamics cannot be specified pixel-by-pixel or frame-by-frame in prose — video playback is non-deterministic (frames get dropped under load) — so he proposed running the original game on a real machine, giving Claude access, and comparing event-by-event (not frame-by-frame) against the new platform. Pavel added that behavioral / functional tests (something happens, there is a response, status checks) can be covered 100%. Val cut the theory short and asked to move to practice: let Igor try it and report what works and what does not.

## Decisions Made

- **Proceed with migrating games from Rage to Nova.** Move forward as decided rather than keep debating. (Decided by Val)
- **Igor runs a QA-automation experiment on the ported Dragon Pays game** — reverse-engineer requirements + acceptance criteria from the prose and code, then try to automate testing ("no-hands" QA) against them and report what works and what doesn't. Timeline: one week, two weeks maximum. (Decided by Val)
- **Port a second game to Nova in parallel, assigned to Anton Lishkevich** (a line game), building on Igor's work — both to enable multi-game / game-select testing later and to spread the knowledge across the team (Kharetski, Metelski, Lishkevich). (Decided by Val and Pavel)
- **Any standards that emerge must be added to the company standards repository.** (Decided by Val — standing rule)
- **Follow-up review meeting set for Friday, September 4, 2026** (one week out); Val will schedule it. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Run the QA experiment: reverse-engineer requirements + acceptance criteria from the ported Dragon Pays prose and code, then try to automate testing against them and report what works and what doesn't | Sept 4, 2026 (max 2 weeks) | High | Val's core theory — QA is the bottleneck for scaling the Rage→Nova migration |
| 2 | Anton Lishkevich | Port a second game (a line game) from Rage/South Dakota to Nova in parallel, building on Igor's work, to enable multi-game/game-select testing and spread knowledge | TBD (parallel) | Normal | Pavel to assign and hand off Igor's work; Anton is not fully loaded |
| 3 | Igor Metelski / team | Add any standards that come out of this work to the company standards repository | Ongoing | Normal | Val's standing rule — distinguish a developer learning from JVL learning |
| 4 | Val Levitan | Schedule the follow-up review meeting for Friday, September 4 | Aug 28, 2026 | Normal | Val: "I'll schedule the meeting" |

## Open Questions

- How to test animation dynamics that cannot be written pixel- or frame-accurate in acceptance criteria — Pavel proposed event-by-event comparison against the original game running on a real machine; to be validated by Igor's experiment.
- Real-machine performance (big-win lag, resource-heavy celebration video) — needs a hardware build and test.
- Whether Igor's LGS mystery-progressive modifications should be merged, or the LGS team should implement that support properly (raised by Igor, deferred by Val).

## Dispatch Log

- 2026-08-28 — Scheduled the Sept 4 review meeting (undertaking #4). Teams meeting created Fri Sept 4, 9:00–10:00 AM ET, inviting Igor Metelski, Pavel Frolov, Irina Shishko, Evgeny Kharetski; objectives + undertakings #1–#3 placed in the meeting description. No emails or other reminders created (per Val).

---
*Processed from Teams transcript on August 28, 2026 (scheduled watcher, capture-only)*
*Source meeting: RAGE_NOVA_conversion_update-August-28-2026*
