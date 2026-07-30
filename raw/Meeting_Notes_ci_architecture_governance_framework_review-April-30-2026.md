# Meeting Summary — CI Architecture Governance Framework Review (v5.1 Operationalisation)
**Date:** April 30, 2026, 12:03 PM Eastern
**Duration:** 26m 53s
**Attendees:** Aaron Bockelie, Val Levitan, Andrei Bosik, Alexander Biratko (Sasha), Evgeny Kharetski

## Summary

This was Aaron's working session with Val and Andrei (with Sasha and Evgeny on the line) to react to the v5.1 governance / CI-architecture documents that Andrei and Sasha had circulated, and to land a concrete two-week operationalisation plan. The conversation moved from Aaron's distilled four-principle reading of the standard, through a long metaphor pass to establish what "code ownership" actually means in JVL's environment, into an explicit short-horizon implementation plan with a hard checkpoint on **May 21, 2026**.

**Aaron's four-principle distillation of the v5.1 documents.** Aaron led with what he said he would personally take away as a developer-contributor at JVL — the four things he could hold in his head without re-reading 100 pages:

1. **Verification lives at boundaries, not at people.**
2. **Compliance data is for steering the standard, not steering people.**
3. **The standard has to be allowed to be wrong.**
4. **Ceremony is debt.**

He framed this as his personal takeaway, not a critique of the long-form documents — "I'm not discounting what you've written, I'm not saying throw it away."

**Val's counter-position on the documents.** Val pushed back on Aaron's instinct to compress. He acknowledged he usually agrees with Aaron, but argued Aaron was discounting the conditions JVL is coming from: the team has never practiced any of these ceremonies before. This is the first time the rules are being written. Even if individual contributors retain only 60-90% of the document and refer back rarely, the act of laying it out matters. Val's read as a non-engineer: he grasps ~75% directly, can ask Claude for the rest, and the specialists who will use it daily will read it and refer back. He concluded that the long-form document should be **saved as a ceremonial reference document**, while agreeing that "blind ceremony is death" — any ceremony has to remain subject to evolution. Aaron accepted that framing: "this is the reference architecture for what it's supposed to look like."

**Naming caution from Aaron.** Aaron flagged one stylistic concern: avoid naming too many roles with capital letters / formal role titles. It's fine to describe roles that way, but per principle #3 (must be allowed to be wrong), heavy formalisation locks in vocabulary that may need to be wrong later.

**Code ownership as the single most important change.** Aaron called out **CODEOWNERS** as probably the most important single thing the team can do — it grants explicit ownership of repository areas, ending the SVN-era nebulous state where "Pavel is responsible for the whole thing" by default. Val seconded this strongly as a *cultural* (not engineering) direction: he advised Andrei's team to actively emphasize that ownership is being assigned ("I'm giving you the ownership of this — maybe it's not all your code, but I'm making you the owner of it") and that ownership must come with **authority**.

**The Admiral & Fleet metaphor.** Aaron sketched the operating model:
- Val is the **Admiral** — sits in the office and watches the fleet go out to sea.
- Each code owner is the **skipper / captain** of their ship (repo). They own that ship.
- **DORA metrics** are how the Admiral evaluates the ships' missions.
- A well-run ship has its crew, missions, and routines. The Admiral can drop in unannounced — "is the brass polished, is everything ship-shape?" — and a healthy ship answers "yes, look, everything's running."
- An unhealthy ship is *obviously* messy when the Admiral visits. The system makes that visible.
- **Developer-health / "space" metrics** (developer friction, time-to-get-work-done) are the second key indicator beside DORA.
- The v5.1 documents are the **reference architecture** the ships return to port to consult — not something thought about constantly, but the source of truth when convening.

Aaron suggested that this can support **structured quarterly conversations** during quarterly planning — review each product's state against the operating principles, since "we've never had that before." This gives the team a chance to test how well the framework is working and whether production aligns with company goals.

**Sasha's example: ten repos as ten McDonald's franchises.** Aaron asked Sasha which project he'd be a code owner of. Sasha said "Lex dispenser" (singular). Andrei corrected: Sasha is actually code owner of **ten repos**. Aaron asked whether Sasha would have enough attention for ten; Andrei said yes. Aaron switched metaphors:
- Each repo is a **franchise** — a "book of business."
- The standard is a **franchise operating agreement** (McDonald's-style). You have to operate it a particular way to keep the franchise license.
- The code owner doesn't recite the operating model verbatim day-to-day; they internalise the *principles of governance* — measurement, data, cadence, "are we meeting too much or too little?"

Aaron deliberately paused here and told Sasha: think about what running ten repos this way will *feel like* day-to-day.

**Val's "we are at the juncture" framing.** Val summed up the meeting's posture: the team has finally arrived at a set of good decisions. They are not implemented yet, but the team believes in them. The exact practical run is unknown but the direction is right. He pivoted: *what's the next step? Who does what? Outline the next two weeks; come back in two weeks and measure.*

**Andrei's two-week proposal.** Andrei proposed applying the new standards to the **infrastructure payment repositories** first, since those are in very active development. The team can see what works and what doesn't, and modify the standards or reports based on real signals — "for example, reports cannot work correctly first some first days."

**Val's product-output instinct (and Aaron's pushback).** Val pushed for going further: he doubted that the team could draw conclusions on "what works" without actually trying to **produce a product** out of a repository under the new system. He drew an extended assembly-line analogy: a car factory can run a fake assembly to get just the frame at the end — no doors, no transmission, no windshield — and that still proves the line works end-to-end. From the frame, you incrementally add subassemblies. The question is "does the frame come out — can I get from Point A to Point X?"

Aaron declined to follow Val that far: **"I think you're talking in too much detail right now. We're making assumptions about what has to happen before it's happened yet."** Val accepted the pushback ("could be") and returned the question: how do we know in two weeks what's working and what isn't?

**Aaron's concrete two-week plan (typed manually, not via AI).** Aaron read out the numbered items he wrote during the call:

1. **Every repository has at least one code owner** (short-term, in the two-week window).
2. The **checks described in the previous document** run on every repo.
3. Use **GitHub Actions** triggered on every commit to main.
4. When a check fails three consecutive times, a **dashboard somewhere** flags it. The framing is American-baseball "three strikes" — three consecutive failures of the same kind means something nobody is catching or caring about. If Sasha owns 10 repos and 6 are throwing consecutive failures, that immediately surfaces that Sasha is overwhelmed and the ownership distribution is wrong.
5. **CRITICAL: these metrics cannot be tied to performance reviews or compensation.** If they are, "it will immediately turn into a gaming problem — not the JVL slots-games kind, but people will twist the numbers, consciously or not, to make themselves look good." The metric has to **stand on its own merit** — Aaron called it "valor" (a play on Val's name).

Andrei understood and agreed with all five points, asking for clarification on #5 specifically. Aaron's gaming-risk explanation landed.

**Implementation timing — Aaron's reality check on Andrei's "two days."** Andrei estimated two days to install the measurements. Aaron pushed for a more realistic week-by-week ramp:
- **Friday:** install on 1-2 repos and verify it works (CI actions trigger, dashboard flags correctly).
- **Monday:** deploy on the rest of the repos.
- **Tuesday:** verify they're all actually working.
- **Wednesday-Thursday:** accumulate a couple of days of signal data.
- **Friday (one week from start):** announce to all code owners — get thumbs-up.
- **Following Monday:** begin the actual two-week measurement period.

Critical constraint Aaron added: **measure only from the announce-point forward.** Andrei suggested using repository history to backfill; Aaron rejected this outright: *"the act of measuring it and assigning code owners changes the behavior of how the repositories work. That's bad data. The very fact that you're telling them things are being measured will change the way people think and react. That's what you want to measure."*

**Anchoring the next review to May 21.** That week-plus-two-weeks math lands the next checkpoint on **May 21, 2026**. Val took the undertaking to circulate the calendar invite.

**Broadening within the company.** Val asked Andrei and Aaron to use the internal weekly meeting (next week) to **bring the rest of the developers on board** — present the framework, walk them through what's about to happen, get them aligned. Andrei proposed a more concrete loop: on Friday of the following week, create a meeting with **Dima Chudzinau and Sergey Tsimanov** (CMS team) to show them the report and the framework and confirm/refine standards, since the act of building the reporting may force changes to the document.

Val closed the meeting at the 26-minute mark, declaring the discussion complete.

## Decisions Made

- **The v5.1 governance / CI-architecture documents are accepted as the reference architecture and saved as a ceremonial document.** Subject to evolution. (Val, with Aaron's concurrence.)
- **CODEOWNERS adoption is the highest-priority change.** Explicitly grants authority + responsibility per repo. (Aaron, Val concur.)
- **Pilot scope: the infrastructure payment repositories.** Andrei's proposal accepted as the two-week trial bed. (Andrei → Val.)
- **No tie between these CI / governance metrics and individual performance reviews or compensation, full stop.** Stand on own merit. (Aaron — Andrei agrees on the record.)
- **Measurement window starts only from the announce-point forward; repository history is not used as backfill.** (Aaron — Andrei agrees.)
- **Next checkpoint: May 21, 2026.** Val to circulate the invite. (Val undertaking.)
- **No formal role names in capital letters / over-formalisation of vocabulary in the standard.** (Aaron, accepted.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Circulate calendar invite for May 21, 2026 review meeting | Near-term | High | Anchors the two-week measurement cycle; without the invite, the cadence does not exist |
| 2 | Andrei Bosik | Install measurement actions on 1–2 infrastructure-payment repos (verify CI triggers + dashboard flagging works) | Friday May 1, 2026 | High | First step of Aaron's ramp; gates everything else |
| 3 | Andrei Bosik | Deploy measurement actions on remaining infrastructure-payment repos | Monday May 4, 2026 | High | Phase 2 of ramp; precedes verification |
| 4 | Andrei Bosik | Verify measurement is operating on all targeted repos | Tuesday May 5, 2026 | High | Confirm before signals can be trusted |
| 5 | Andrei Bosik | Accumulate initial signal data | Wed–Thu May 6–7, 2026 | Normal | Pre-announcement validation period |
| 6 | Andrei Bosik | Announce to all code owners that measurement is live; collect thumbs-up | Friday May 8, 2026 | High | Per Aaron: measurement officially "starts" at announce-point — the announcement itself is part of the experiment |
| 7 | Andrei Bosik | Begin formal two-week measurement window | Monday May 11, 2026 | High | Window runs through May 21 review |
| 8 | Andrei Bosik | Schedule and run internal Friday meeting with Dima Chudzinau and Sergey Tsimanov to walk them through the reporting + framework | Following week (~May 8, 2026) | Normal | Brings CMS team into the operationalisation loop early; report-building may force document edits |
| 9 | Aaron / Andrei / Val | Use next week's standing meeting to widen the framework knowledge across the rest of JVL developers | Next standing meeting | Normal | Per Val: "let's bring others into it" |
| 10 | Code owners (all) | Each repo must have at least one assigned code owner | Within the two-week window | High | Aaron's #1 short-term deliverable; precondition for ownership-based metrics to mean anything |

## Engineering Signals

### Confirmed Signals

- **ADR — Verification lives at boundaries, not at people.** (Principle #1.) Operationalises as: CI checks live on repository / commit boundaries; no manual sign-off process attached to individuals.
- **ADR — Compliance data steers the standard, not people.** (Principle #2.) Metrics must not be tied to performance reviews or compensation; if they are, the data is gamed and the standard cannot evolve from it.
- **ADR — The standard has to be allowed to be wrong.** (Principle #3.) Avoid over-formal vocabulary (capitalised role names) and other lock-ins that prevent course-correction.
- **ADR — Ceremony is debt.** (Principle #4.) Bias against process accumulation; every ceremony must justify itself by output.
- **ADR — CODEOWNERS is mandatory per repository.** Single most important short-term change; converts implicit "Pavel owns everything" into explicit per-repo ownership with authority.
- **CAP — DORA-style + developer-health metric stack on every repo.** Specifically: GitHub Actions on every commit-to-main; three-consecutive-failure threshold lights a dashboard alert.
- **ADR — Measurement window begins only at announce-point.** Repository history is *not* used to backfill metrics — using it produces bad data because the act of declaring measurement changes behaviour, and the behavioural change is precisely what's being measured.
- **CAP — Quarterly governance review.** Per Aaron: structured quarterly conversation during planning to review each product/repo against the operating standard.
- **Solution — "Franchise / Admiral & Fleet" framing for code-owner expectations.** Repo = franchise; standard = franchise operating agreement; Val = Admiral; code owners = skippers. Useful internal vocabulary for the cultural roll-out.

### Suspected Signals

- **Possible REQ — Dashboard system for surfacing three-consecutive-failure events across all repos.** Aaron referred to "a dashboard somewhere" without specifying the tooling. — *Val, is this a requirement against a specific tool (Grafana? GitHub-native? something Andrei builds?) or open-ended?*
- **Possible CAP — Internal-pilot-then-broaden rollout pattern as a JVL standard for engineering-process changes.** This meeting effectively established a model: implement on infrastructure-payment repos first → walk CMS team through it the following Friday → roll wider at next standing meeting. Worth tracking as a reusable governance-rollout capability.
- **Possible ADR — Val's "produce a product end-to-end" instinct as a validation principle for new process.** Aaron blocked it here as premature, but Val articulated a real principle: process is not validated until an end-to-end product attempt is made under it (the car-frame analogy). — *Val, does this warrant tracking as a future ADR for how JVL validates process changes? It was deferred, not rejected.*

## Open Questions

- **Tooling for the failure-detection dashboard.** Unresolved at the meeting — see Suspected Signals.
- **Should DORA + developer-health metrics be combined into one dashboard or two?** Aaron mentioned both ("DevOps metrics and essentially space metrics") without specifying integration.
- **How are code-owner overload signals (Sasha with 10 repos, 6 throwing failures) escalated and remediated?** The detection mechanism is clear; the rebalancing response is implicit.
- **What is the exact list of "infrastructure payment repositories" being pilot-scoped?** Andrei named the category but did not enumerate.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: CI Architecture — Governance Framework Review (v5.1 Operationalisation) (20260430_080353)*
