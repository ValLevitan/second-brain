# Meeting Summary — 3-Progressives for GA-COAM: Schedule Rejig
**Date:** May 22, 2026, 2:31 PM Eastern
**Duration:** 46m 51s
**Attendees:** Val Levitan, Pavel Frolov, Igor Metelski, Lena Zhukova, Anton Leshkevich, Irina Shishko, Evgeny Kharetski

> **Sequence note:** Tactical scheduling session for the GA-COAM v2 / 3-progressive release. Lives downstream of the May 8 capability decomposition and workflow definition (see `GA-COAM v2 Capability Decomposition-May-8-2026/` and `GA-COAM v2 Requirements Workflow and Personas-May-8-2026/`). Original schedule-review checkpoint date moved from Thursday May 14 to this session.

## Transcript Quality Note

Russian throughout; summary in English. The team worked from the live Jira board on screen — exact feature numbers are reproduced where the audio + Pavel's references caught them.

## Summary

This was a tactical scheduling rejig session. The team walked the active task list against the July 1 ship target and recognised that, under the current sequencing, **Igor's chain extends to ~June 10**, which is too late to leave room for testing and review before July 1. The session restructured the work into a parallel-track plan to compress the timeline.

**Stale framework feature deleted.** Pavel flagged feature **FRA-1005** ("framework master test") assigned to Anton from a long-ago session. Anton: *"I don't know — I need to talk to Efim about this; nobody ever followed up."* Val: *"if it's been sitting there and nobody's asking, it doesn't exist."* Pavel moves it to backlog. Anton accepts; he can re-add later if it turns out to be needed. **Val's broader rule reinforced: stale work items get killed, not preserved on hope.**

**Current schedule projection: too late.** Pavel pulled Igor's task chain — **finishes ~June 10**. Irina: that's a Friday, leaves only one weekend to test and hand off. Unrealistic. The longest item is feature **FRA-1196** (match-3 bonus logic), which Igor estimated at one week. Pavel flagged that Valentin historically took **~2 weeks** for similar bonus work. Igor acknowledged: the SVN commit history confirms 2 weeks was the historical floor for net-new bonus development, *but* this one might go faster because it resembles the Jackpot Rush bonus pattern.

**Match-3 bonus dependency map.** Igor walked the team through why match-3 cannot just be parallelised:

- **Match-3 progressive is tightly tied to a specific progressive controller and data centre configuration** at engine-initialisation time. The math engine for the bonus games requires progressive-parameter pre-population during init — those parameters flow through the data centre.
- **Current branch v0.24 (where multi-product work is happening)** does not accept the new match-3 mechanism — the data centre in v0.24 doesn't know about it.
- **Therefore:** developing match-3 bonus in v0.24 is blocked until v0.24 picks up multi-product + new-progressive support, which is the long path.

**Proposed workaround — separate experimental branch.** Igor and Pavel landed on the plan:

- Create a **separate experimental branch from GK base** (likely v0.117/v0.119 — clarified by Irina as v0.119, the standard GCAM branch).
- Add match-3 progressive support in the **Data Centre** and **Progressive Controller** in this experimental branch.
- Igor + Anton can then develop the match-3 bonus *in parallel* with the v0.24 multi-product work.
- This decouples the bonus from the multi-product critical path.

**Evgeny (Zhenya)'s current blocker — Windows Docker RIS.** Evgeny explained what he's been working on: getting the data centre + framework to launch under Windows Docker locally (so Anton can develop without the physical machine). Status:

- **RIS** (initialisation flow) is now passing — Evgeny populated the data centre with the 3 real games Igor provided (replacing the 3 dummy stubs).
- **But normal setup is failing post-RIS.** The framework restarts after RIS and the restart crashes.
- Pavel: how much more time? Evgeny estimates ~2 days (so ready by Tuesday May 26).

**Critically: Anton can develop the game-select screen NOW on the existing single-product launch path.** Anton confirmed he can launch the existing one-product mode from a different branch (not v0.24). Evgeny: *"yes, you can launch a different data centre — single-product, like the standard launch."* This is enough for Anton to start the game-select implementation **on Monday May 25** without waiting for the multi-product launcher to be fixed.

**Home screen development is blocked.** Anton's original Monday-onward plan was the home screen. Lena and Igor agreed: the home screen requires the multi-product mode running, since the home screen displays multiple games grouped by progressive type — which requires the multi-product launch path to work. Home screen waits.

**Resources status (Lena).** Lena confirmed:
- **Game-select resources** ready Monday in usable form — not final, but enough to develop against. Final video / texture replacements happen during the review cycle.
- **Match-3 bonus resources** available — Anton can work on the bonus when he picks it up.
- **Home screen resources** available.
- Lena specifically engineered the asset pipeline so that all three workstreams have something to work with starting Monday.

**Revised work plan, by person and week:**

- **Anton (week of May 25)**: Game-select screen implementation (in single-product mode; FRA-1182 area).
- **Anton (from ~June 1)**: Pick up match-3 bonus task **FRA-1196** in the new experimental branch — once Igor + Dima have the data centre + controller side ready for match-3 in that branch.
- **Igor (week of May 25)**: Continue multi-product work; coordinate with Dima Chudinov on adding match-3 progressive support to the experimental branch.
- **Igor (from ~June 1)**: Return to multi-product / 3-progressive coexistence (FRA-1204 / FRA-1205 tasks) once Anton has the match-3 bonus going.
- **Dima Chudinov**: Currently making presets for Miranda from the server side; also expected to add match-3 progressive support to the experimental branch in MBD progressive controller.
- **Evgeny**: Finish Windows Docker launch fix by Tuesday May 26.
- **Lena**: Final art assets through June 5 (Friday); final asset substitution week is June 1-5.
- **Goal**: Something **reviewable by June 5**, final review cycle June 8 onward, July 1 ship.

**Pavel's question — can match-3 bonus be developed on a separate experimental branch right now?** Iterated through the team:
- Igor: *"if we add match-3 progressive support to that branch, yes."*
- Pavel: *"can we add fake match-3 support?"*
- Igor: *"let's not do fake — better to add proper progressive support."*
- Anton: *"yes, we can pick any branch, add match-3 progressive there, develop the bonus there. Theoretically works."*
- Irina: *"switch to DC version v0.119; tell it about the new match-3 progressive product."*

**Translation to Jira:** Tasks FRA-1195, FRA-1201, FRA-1196 (match-3 chain) are now disconnected from the v0.24 branch and put on the experimental branch. Anton can start them from Monday May 25; expected to wrap by ~June 5.

**Builder under Windows.** Anton noted that once Evgeny's Windows Docker launch is working, Anton needs to update the local builder's launcher (replace the data-centre button-launch with container-based launch). A few hours of work. Pavel estimates this can be done by Tuesday at the latest. Lena pressed: *"realistically by June 1? We need to see things under Windows in the last development week."* Pavel: *"yes, not later than Tuesday May 26."*

**Next checkpoint — Tuesday May 26, 10 AM Eastern.** Pavel took the undertaking to schedule the next meeting at **10 AM Eastern (Toronto-friendly time) on Tuesday May 26**. Title: **"3-Progressives"**. Val to be added as an optional invitee.

Val closed: *"OK, invite is set for Tuesday. We won't move further today. Thanks all, have a good weekend."*

## Decisions Made

- **Stale framework feature FRA-1005 ("framework master test") moved to backlog / treated as non-existent.** Anton may re-add if needed later. (Val.)
- **Igor's chain ending ~June 10 is unacceptable** for July 1 ship — restructured. (Val + team.)
- **Match-3 bonus moved off the v0.24 critical path into a separate experimental branch** based on GK v0.119. (Igor + Pavel + Anton.)
- **Anton starts game-select screen implementation Monday May 25** on the existing single-product launch (does not wait for multi-product launcher). (Anton + Evgeny.)
- **Anton picks up match-3 bonus (FRA-1196) from ~June 1** in the experimental branch. (Pavel + Igor + Anton.)
- **Home screen development deferred** until multi-product launch path is working. (Anton + Lena.)
- **Lena's design assets available Monday May 25** for all three workstreams (game-select, match-3, home screen). (Lena.)
- **Final review-ready build by June 5; final assets/review cycle June 1-5; ship July 1.** (Lena + team.)
- **Windows Docker launch ready by Tuesday May 26.** (Evgeny.)
- **Anton's Windows builder launcher updated to container-based launch by Tuesday May 26.** (Anton, conditional on Evgeny finishing.)
- **Next checkpoint: Tuesday May 26, 10 AM Eastern.** Pavel sends invite. (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Move FRA-1005 ("framework master test") to backlog | This week | Normal | Stale feature; Anton may re-add later if needed |
| 2 | Pavel Frolov | Schedule the next 3-Progressives meeting for Tuesday May 26, 10 AM Eastern (Toronto-friendly time); add Val as optional | Today | High | Cadence checkpoint |
| 3 | Evgeny Kharetski | Finish Windows Docker launch fix (current blocker on framework restart after RIS) | Tuesday May 26 | High | Unblocks Anton's builder work and downstream development |
| 4 | Anton Leshkevich | Start game-select screen implementation in single-product launch mode | Monday May 25 | High | Doesn't wait for multi-product launcher |
| 5 | Anton Leshkevich | Update local Windows builder launcher to container-based launch (replace data-centre button launch) | After Evgeny finishes, by Tue May 26 | High | Few hours of work; enables Lena to review under Windows |
| 6 | Anton Leshkevich | Pick up match-3 bonus FRA-1196 implementation from ~June 1 in the experimental branch | From ~June 1 | High | After Igor + Dima have the data centre + controller side ready |
| 7 | Igor Metelski | Continue multi-product work week of May 25; coordinate with Dima Chudinov on adding match-3 progressive support to the experimental branch | Through next 1-2 weeks | High | Match-3 cannot be in v0.24; needs separate branch |
| 8 | Igor Metelski | Return to multi-product / 3-progressive coexistence tasks (FRA-1204, FRA-1205) from ~June 1 | From ~June 1 | High | Picks up after Anton has the bonus moving |
| 9 | Dima Chudinov | Add match-3 progressive support to the MBD progressive controller in the experimental branch | Week of May 25 | High | Required for Igor's parallel match-3 work |
| 10 | Dima Chudinov | Continue Miranda preset work on the server side (in-flight) | Ongoing | Normal | Separate, mentioned by Pavel as ongoing |
| 11 | Lena Zhukova | Deliver workable game-select / match-3 / home-screen design assets by Monday May 25 | Monday May 25 | High | Engineered the pipeline so all three workstreams have inputs Monday |
| 12 | Lena Zhukova | Final asset substitution week June 1-5; reviewable build by June 5 | June 5 | High | Anchors the design-review cycle |

## Engineering Signals

### Confirmed Signals

- **ADR — Stale features without owner-asks are deleted, not preserved.** General rule extracted from Val's handling of FRA-1005. Applies JVL-wide.
- **CAP — Three-progressive coexistence (multi-product / multi-progressive) is implemented in branch v0.24** for the main launch path. Match-3 progressive lives in a separate experimental branch on top of GK v0.119, joining the main path later.
- **Engineering Solution — Parallel-branch decoupling for blocked critical-path work.** When a feature requires both upstream services (Data Centre + Progressive Controller) and downstream consumers (game framework + bonus), and the upstream-services side blocks development on a particular branch — fork a new experimental branch where upstream is configured to support the new mechanism, develop the downstream in parallel, then merge later.
- **CAP — Single-product launch path remains operational** in branches outside v0.24, enabling Anton to develop the game-select screen without waiting for multi-product to stabilise.
- **REQ — Math engine for match-3 bonus requires progressive parameters injected at initialisation time.** Specifically: the math engine needs progressive configuration data flowing through the data centre during init — direct dependency, not a runtime lookup.
- **Engineering Solution — Tuesday-cadence sync meeting at 10 AM Eastern** during the next-week critical-path period. Toronto-friendly timing; weekly tactical sync.

### Suspected Signals

- **Possible CAP — Lock-in for "no fake progressive support."** Igor explicitly resisted Pavel's "add fake match-3 support" suggestion — better to add proper progressive support. Worth tracking as a working principle: when introducing new architectural primitives, add the real implementation rather than the stub. — *Val, is this a JVL-wide rule, or specific to this case?*
- **Possible REQ — Reviewable-by-June-5 milestone gating ship-readiness.** Lena's June 5 anchor is treated as fixed. If June 5 slips, July 1 ship is at risk. — *Should this be explicitly tracked as a gate-condition, not just a working aim?*

## Open Questions

- **Exact branch number** for the experimental match-3 branch. Discussion converged on v0.119 (GK base) but specific branch name not finalised on the call.
- **Dima Chudinov's bandwidth** to add match-3 progressive support to MBD controller alongside his existing Miranda preset work. Irina implied he's doing multiple tasks; Pavel implied she'd ask Evgeny / Pavel; not pinned.
- **Whether the homescreen blocking on multi-product is permanent** for this release or just for current developer assignment. The team accepted home-screen-defers but didn't address whether a different developer could attempt it in parallel.
- **What's needed to confirm match-3 progressive parameters flow correctly into math engine init** — specifically, what test gate confirms the experimental branch's data-centre-to-math-engine plumbing is working.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: 3-Progressives for GA-COAM - May-22-2026 (20260522_103154)*
