# Meeting Summary — Nova Migration & Autonomous Coding Strategy
**Date:** 30 June 2026, 12:33 PM Eastern
**Duration:** ~1h 33m (transcript runs to 1:32)
**Attendees:** Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Alexander Biratko, Evgeny Kharetski, Dmitri Kovalchuk, Andrei Bosik, Irina Shishko

**Related initiatives:** [[Development and Release Processes and Procedures]] (absorbed the JIRA Hierarchy Standard) · [[NOVA Platform Architecture]]

## Summary

**Purpose.** Val called the team together to agree on how to move JVL toward autonomous coding (Claude Code), automated testing, and CI/CD — and how to roll out the new JIRA hierarchy and the NOVA platform without freezing product releases. He said many separate experiments have all come back positive, and he sees an exponential benefit in code quality, testing, and speed. His repeated question: *how* do we transition the whole company, and what do I push next?

**What's already done or in progress.**
- Pavel demonstrated a working end-to-end (E2E) test proof-of-concept an hour earlier; it ran reliably.
- Last week Evgeny showed generating Capabilities from existing code; Pavel reproduced it (code → prose → Capability) using feature HFM-577 with almost no prompting.
- Dmitri Kovalchuk finished the new JIRA hierarchy standard — it's in Kanban.
- Pavel wrote the repository-structure standard; Andrei is writing the new CI/CD standard.
- Dzmitry and Sergei already moved the Back Office (old CMS) code to GitHub.

**The proposed workflow.** Capabilities (product language) → Features (one feature branch per repo) → ADRs (architecture decisions captured inside the feature) → Claude implements. Val insisted JVL has no formal architect: a small group of colleagues who know the business sit together and create ADRs informally, in the same conversation where the feature is discussed. Dzmitry wanted a heavier "architect agent" step producing a detailed plan first; Val pushed back as too formal for JVL.

**Reverse-engineering requirements from code.** Val's stepwise plan: take today's Back Office and RAID Studio code → generate prose → Capabilities → Requirements with acceptance criteria → isolate Requirements for reuse. Code is the source of truth; don't jump straight from code to high-level Capabilities or precision is lost. Alexander Biratko was skeptical that reverse-engineered Requirements would be reusable (too code-specific); Evgeny questioned why Requirements must be universal at all and proposed tagging/marking Requirements and composing services from modules (each module's manifest noting which Requirement it implements). Dzmitry proposed a company-level agent that creates and reviews Requirements against a standard template, running as a loop service to flag non-compliant ones.

**Migration scope and timeline.** Dzmitry estimated a full backend move (AWS, transactional system, machine registration, RAS, manifests) could run to end of year — Val read that as 4–6, maybe 8 months. Conclusion: JVL cannot freeze releases for that long (transaction payouts on RK 35/68 must continue), so a full vacuum migration is rejected.

**RAID Studio / framework.** Moving the RAID game framework (C++) to Git is hard — huge repo volumes (a NOVA game ~500 GB; RAID ~5–40 GB) with heavily duplicated assets (libraries, sounds, video). Direction: keep RAID Studio for South Dakota (the only market tightly tied to Class III regulation); aim to move Georgia game releases to NOVA. Growth markets (Georgia, Nebraska, Texas) aren't regulator-bound, so easier to jump. Alexander argued they should just try migrating one game and building it to settle feasibility empirically.

**Reports / modems.** Pavel wants modems in the 2000-series machines for Georgia: collect play statistics, give operators reports (popular games, revenue), possibly sell report subscriptions and do remote installs without USB sticks. Dzmitry warned this risks rebuilding the old heavy CMS inside the new platform.

**Environment independence.** Evgeny: the system must not depend on any developer's individual Claude setup — each developer configures their own, and the build must still work. Andrei tied this to the single-source-of-truth model they're aiming for.

**Platform taxonomy (clarified by Val post-meeting).** NOVA = the new on-cabinet **gaming** platform. Galaxy = the new **online** platform, incorporating the Observatory and Orchestration modules (each itself containing many services). The CMS/Back Office migration target is Galaxy, not NOVA.

## Decisions Made

- **Do not freeze releases for a full migration.** A 4–6+ month vacuum rebuild is off the table; releases must continue. (Team consensus, endorsed by Val)
- **Go-ahead ("отмашка") on the new model:** every future feature taken into work must be tied to a Capability; if none exists, write one first. (Proposed by Pavel, endorsed by team)
- **Proceed to autonomous coding + automated testing + CI/CD.** Nobody opposed; everyone supports moving. (Consensus)
- **Stepwise reverse engineering:** code → prose → Capabilities → Requirements with acceptance criteria, then isolate for reuse. (Val)
- **Keep RAID Studio for South Dakota; target Georgia releases for NOVA.** (Intention, not locked)
- **System must be independent of individual dev environments.** (Evgeny, endorsed by Andrei)
- **New JIRA hierarchy standard is adopted** — done and in Kanban. (Dmitri Kovalchuk)

## Undertakings

| # | Who | What | When | Priority |
|---|-----|------|------|----------|
| 1 | Alexander Biratko | **Spike:** migrate a RAGE Studio–based game to the NOVA platform. Assess volume/duplication feasibility. | Jul 20 → end of July (~10 days) | High |
| 2 | Dzmitry Chudzinau | **Spike:** migrate the current CMS (Back Office) to the Galaxy Platform. | Jul 20 → end of July (~10 days) | High |
| 3 | Pavel Frolov | Move the Progressive Controller into Git and unify it, so Dzmitry/Sergei no longer work across two repos (SVN + Git). | After Evgeny returns from vacation | Normal |
| 4 | Andrei Bosik | Deliver the new CI/CD standard. | ~Jul 30 | High |
| 5 | Pavel Frolov | Schedule the #1 and #2 spikes in JIRA Plans — list tasks and durations for each. | ~Jul 6 | High |
| 6 | Team | Meet to assess the spike outcomes (#1 and #2). | End of July | High |

## Schedule

- **Mon Jul 6** — Pavel schedules Biratko (#1) and Dzima (#2) spikes in JIRA Plans (tasks + durations).
- **Mon Jul 20 → ~Fri Jul 31** — Biratko runs the RAGE-Studio-game → NOVA spike; Dzima runs the CMS → Galaxy spike (~10 days each).
- **~Jul 30** — Andrei's CI/CD standard ready.
- **End of July** — team assessment meeting on spike outcomes.

## Open Questions

- Must Requirements be universal/reusable, or are several similar ones acceptable? (Evgeny vs. Alexander — unresolved)
- How exactly to allocate people/projects for the transition (math, games, hardware libraries, etc.)? Val asked but it wasn't settled.
- Whether/how to move the RAID framework (not just code) to Git given the asset volumes.
- Do the game graphics need to be reworked for the new platform? (Raised at the end; transcript cuts off.)

---
*Processed from Teams transcript on 30 June 2026*
*Source meeting: NOVA New JIRA plans hierarchy, Claude Code autonomous game coding*
