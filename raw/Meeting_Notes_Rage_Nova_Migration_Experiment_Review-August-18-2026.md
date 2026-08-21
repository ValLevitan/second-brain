# Meeting Summary — RAGE-NOVA_migration — review
**Date:** August 18, 2026, 11:00 AM ET
**Duration:** ~45 minutes (11:08–11:53 AM ET)
**Attendees:** Val Levitan, Igor Metelski, Pavel Frolov, Irina Shishko, Efim Podvoiski, Evgeny Kharetski
**Raw transcript:** [[Meeting_Transcript_Rage_Nova_Migration_Experiment_Review-August-18-2026]]

## Summary

The meeting reviewed the experiment to migrate a RAGE game to the new NOVA (Omni/LGS) platform using Claude.

Igor spent about a day and a half using Claude to convert a horizontal RAGE "Salta Cota" (South Dakota) machine into a horizontal NOVA configuration with three screens. Before this, NOVA only had a vertical Omni build; Claude correctly built the new horizontal layout and moved the scenes and sprite resources of one game — Dragon Pays — across. Val stressed several times that this visual conversion would have been essentially impossible by hand in that time (it would have needed designers to rebuild the scenes from scratch), so doing it in a day and a half is a major result.

The experiment is not finished. The game logic does not run yet because the math for Dragon Pays is missing from the remote math server — only one game's math was set up there. Igor needs that math to complete the test. Efim, who owns the math, agreed to provide it. He would not promise same-day but expects roughly a day's work, with Thursday–Friday as the safe outside date. Igor will continue this week, and the group will meet next Monday to see Dragon Pays actually playing on NOVA.

A side discussion covered how math should be packaged now that it runs as a service in a Docker container. The team weighed one container per market versus per game, a giant container holding every game, and a container that configures itself from whatever games are installed. They converged on building the math container from a game list passed in during the integration build step, so each package gets a container built for its specific set of games. Efim resisted the "everything in one container" and fully self-configuring options as premature; he called the game-list approach a sound compromise to refine in practice. Certification is expected to verify per-game checksums.

Wider NOVA progress was better than expected. Efim has already partly ported the RAGE math to Rust, and Anton Lishkevich has rewritten the printer service and build validator in Rust and tested the printer. Evgeny cautioned there is still significant LGS-side work: SAS has not yet run on NOVA, multiprogressive needs porting, and the NOVA platform-service repo has diverged from the old RAGE center repo over roughly six months of RAGE development.

Val laid out the plan. RAGE releases do not change. He then framed a NOVA timeline: use September to polish the NOVA MVP capability list, begin intensive NOVA development on October 1, and deliver the first NOVA platform version (targeted at Salta Cota) to GLI by November 1. He noted only 12 calendar days remain before September 1. Val also flagged confusion from an earlier meeting where Lena had said the next South Dakota release is expected to be vertical; he directed the team to keep the experiment horizontal-to-horizontal and not touch the vertical machine.

## Decisions Made

- **Efim will supply the Dragon Pays math to the remote math server for Igor.** The experiment is blocked without it. (Decided by Efim Podvoiski, Val Levitan)
- **Igor will finish inserting the math, test the game logic, and demo Dragon Pays running on NOVA (horizontal Salta Cota) at Monday's meeting.** (Decided by Val Levitan, Igor Metelski)
- **Math packaging: build the math container from a game list passed in at the integration-build step, one container per game set / market.** Rejected alternatives: one giant all-games container, and a fully self-configuring container (both judged premature). (Decided by Efim Podvoiski, Pavel Frolov, Evgeny Kharetski)
- **RAGE release calendar is unchanged.** (Decided by Val Levitan)
- **Target NOVA timeline (Val's plan): September polish the MVP capability list; October 1 start intensive NOVA development; November 1 deliver the first NOVA version to GLI.** Stated as the plan, not yet a hardened schedule. (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Efim Podvoiski | Provide the Dragon Pays math on the remote math server to Igor | Aug 19–21 (today/tomorrow, Fri Aug 21 at latest) | High | Blocks the migration experiment |
| 2 | Igor Metelski | Insert the math, test the game logic, and demo Dragon Pays running on NOVA (horizontal Salta Cota) | Mon Aug 24 (next meeting) | High | Continues this week |
| 3 | Pavel Frolov | Send Val the Rust services Anton Lishkevich built (printer service, build validator) | TBD | Normal | Val asked to see them |
| 4 | Val Levitan (team) | Polish and finalize the NOVA MVP capability list during September | By Oct 1 | Normal | Precondition to starting NOVA development Oct 1 |

## Open Questions

- Exact build mechanics for assembling the per-package math container from the game list were left to be worked out in practice (Efim, Pavel, Evgeny).
- Whether NOVA can hit the Oct 1 → Nov 1 development window depends on unproven LGS-side work (SAS on NOVA, multiprogressive port); Evgeny voiced this as a risk.

## Dispatch Log

---
*Processed from Teams transcript on August 18, 2026 (scheduled meeting-watcher, capture-only).*
*Source meeting: RAGE-NOVA_migration — review*
