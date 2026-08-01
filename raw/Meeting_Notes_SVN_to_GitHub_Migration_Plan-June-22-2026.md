# Meeting Summary — SVN to GitHub Migration Plan
**Date:** June 22, 2026, 11:18 AM Eastern
**Duration:** ~27 minutes
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Andrei Bosik, Irina Shishko, Pavel Frolov, Evgeny Kharetski

## Summary

Val asked whether to move RAGE Studio (the old game framework) from SVN to GitHub. His initial instinct was to leave it in SVN, but most of the codebase has already migrated to GitHub (including the CMS backend).

The team unanimously favored migrating. Evgeny said it would eliminate duplicate dependencies and dual-repo maintenance — libraries like Progressive and Progressive Controller currently exist in both SVN and GitHub because CMS uses them.

**What to migrate and when:**

*LGS framework* — top priority. Evgeny estimated 1–1.5 weeks for the code transfer, plus separate work on the builder (Pavel and Lyosha's domain). The team agreed LGS should move to GitHub so all future game development uses it from there. Timeline: starting July 20 (after Evgeny and Lyosha return from vacation on July 16), target completion by August 2.

*Games* — current games being released before August 15 (GCam v2, Pyzno, Wolves, Dual Glass Display, LT Modems) will release from SVN as planned. After release, they can be migrated. New games will start directly in GitHub. Each game gets its own repository per the existing Jira standard — not a monorepo.

*Hybrid approach* — the builder will be modified to pull LGS and Progressive from GitHub while still pulling games from SVN during the transition. This lets the team work without waiting for all games to migrate.

*Math libraries* — Efim (currently on vacation) handles the math. Some math is already in GitHub (Andrei built actions for it), but it's built for the Omni platform, not old RAGE Studio. Efim needs to be asked how to provide math for old games from GitHub. Key principle: don't commit binary artifacts to repos — build via GitHub Actions and pull as artifacts. Val gave this ~2 weeks, running in parallel.

*Game asset handling* — old games have assets committed directly into the repo. Andrei noted that AI can analyze the repo structure and generate a .gitattributes file that routes large files to Git LFS. No raw source assets exist for old games — only exported assets.

*Igor Mitseiskiy* was assigned to start the game migration work. Anton to help. Pavel to handle or supervise the builder modifications.

Val asked for a timeline/schedule to be created.

## Decisions Made

- **LGS framework migrates to GitHub first** — the foundation everything else depends on. (Decided by group consensus)
- **Games stay in SVN until after their next release, then migrate** — don't disrupt active releases. (Decided by Val, supported by Irina)
- **Each game gets its own GitHub repository** — following existing standards, not a monorepo. (Decided by Val)
- **Hybrid builder during transition** — pulls framework from GitHub, games from SVN. (Decided by Pavel, agreed by group)
- **No binary artifacts committed to GitHub repos** — math and other compiled outputs build via Actions and are pulled as artifacts. (Decided by Andrei, confirmed by Evgeny)
- **Igor assigned to game migration, Anton to South Dakota** — (Decided by Pavel and Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Create a timeline/schedule for the full SVN-to-GitHub migration (LGS, games, math, builder) | June 24, 2026 | High | Val wants smaller chunks with clear dates; Pavel said he needs a couple of days |
| 2 | Evgeny Kharetski | Migrate LGS framework code from SVN to GitHub | Aug 2, 2026 | High | Starting July 20 after vacation; ~1.5 weeks estimated |
| 3 | Pavel Frolov / Lyosha | Modify the builder to support GitHub-based LGS and Progressive builds | Aug 2, 2026 | High | Without this, migrated code can't be built; runs in parallel with code migration |
| 4 | Andrei Bosik | Contact Efim about migrating math libraries to GitHub — ask how he proposes to do it, for which games, and how long it will take | TBD | Normal | Efim is on vacation but can answer via message; ~2 weeks estimated for the work itself |
| 5 | Igor [Mitseiskiy] | Start migrating game repositories to GitHub with separate repos per game, beginning with a framework + sample game to prove the new build structure | TBD | Normal | First step toward full game migration; GCam v3 games suggested as initial candidates |
| 6 | Val Levitan | Schedule a CI/CD standard progress review meeting for Friday June 26 at 9:00 AM with Pavel, Irina, and Andrei | June 22, 2026 | High | Review progress on the release pipeline standard and the migration schedule |

## Open Questions

- **How will the builder handle multi-repo game assembly?** Old games were built from a single monorepo with framework + all games. The new structure (separate repos per game + framework) requires a new build orchestration approach. Needs experimentation by Igor.
- **What to do with math libraries for old games?** Efim's math currently builds for Omni platform. Can the same source code produce artifacts for old RAGE Studio games? Needs Efim's input.

---
*Processed from Teams transcript on June 22, 2026*
*Source meeting: Review: Release Pipeline Standard (Andrei) — Segment 2*