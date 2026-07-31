# Meeting Summary — Testing Framework for Transactional Products (Part 2)

**Date:** May 22, 2026, 12:42 PM (Eastern)
**Duration:** ~9 minutes
**Segment:** Part 2 of 2 (continuation; Part 1 ended ~12:32)
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian (summarized in English)

> **Note:** Part 1 named a 4-person study group (Irina, Pavel, Biratko, Kharetski). Part 2 superseded that with a different, expanded list (see Decisions below). The **operative working group** that actually convened — confirmed visually by Val on May 25, 2026 — is 10 people: Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko, Alexey Khamin, Ivan Shpak, Evgeny Kharetski, Vladimir Samusenko, Sergey Tsimanov, Dzmitry Chudzinau. The kickoff Val proposed for Friday May 29 was **pulled forward to Monday May 25**.

## Summary

**Why the recording restarted.** Val explicitly turned the recording back on to capture the next thought — what steps are needed, the rough schedule, the commitment, the timeline. He invited Pavel to develop his idea further: "it's a sensible thought, I like it."

**Pavel's proposed working group (revising from Part 1).** Pavel pivoted away from the 4-person group Val named in Part 1 (Irina, Pavel, Biratko, Kharetski) and proposed a different mix:

- Alexey Khamin (Lesha) and Ivan Shpak (Vanya) from QA
- Sergey Tsimanov
- Alexander Biratko
- Vladimir Samusenko (newly-onboarded employee)
- (Pavel implicit as leader)

The task for them: come up with an approach to automatic testing that is **flexible**, **doesn't require constant maintenance**, and is written in language understandable to both humans and AI. Each contributes from their angle (QA, frontend, backend), and "if we find diamonds, we combine them into one pendant."

**Val's escalation: expand the group AND change the meeting style.** Val told Pavel his proposal was too narrow — extend the conversation to everyone currently in the office hall, take a break and just pull people in. Then Val pivoted to a much more important point: **how** the meeting itself must be run.

> *"Someone has to bring in the infection. One person who introduces the infection — that's what I call infection. It's stimulus that people maybe haven't thought about before."*

Val rejected the "say the idea and disperse to think about it" model. The right model is to sit in the room and **actively choke the idea on the spot**. Pavel takes everyone by the throat. The meeting attendee will make more mistakes than anyone — theories will be wrong in huge quantities — but you keep choking: *"but what if this way? but what if this way?"* In that pressure, real ideas surface. Someone will object "this doesn't work" and propose what does.

**The "choking meeting" methodology (Val's coined term).**
- Sit and don't let people relax mentally.
- If you see someone has mentally checked out, you press them back in.
- Like a boa constrictor — squeeze, don't release.
- Meetings must be **recorded**.
- When the room is squeezed dry and nothing more is coming, that's where you pause.
- Take the transcript, hand it to AI, let a new direction emerge.
- Then hold meeting 2. Then meeting 3.
- **Val committed to a 3-meeting budget for the cycle.**

**Val's breakthrough on data contracts (the technical pivot point).** During the discussion Val arrived at — and credited Pavel for triggering — a fundamental reframe:

- The repos *already* have **data contracts** between them.
- If repos know each other through data contracts, then we already know how each repo can be tested.
- Sum of repos + sum of data contracts → we can probably compose end-to-end **data-contract tests**.
- The catch: data contracts change every time code changes — they are **dynamic**, not static. They move with every commit.
- Therefore a **stable test framework cannot work** — you'd need a permanent team chasing the contracts as they shift.
- But this is exactly the kind of thing an **agent does in seconds**: read the data contracts and compose the tests from them. For a human this is impossible drudgery; for an agent it's routine.
- Conclusion: **don't build a framework. Build agentic dynamic test composition driven by the data contracts themselves.**

Val described this as Pavel "hammering through the wall with one blow" — they had backed themselves into a corner with "framework" thinking, and Pavel led them out. Val called it "a very, very elegant thought."

**Val's schedule commitment (since superseded).** In the meeting Val said he'd set up the kickoff for **Friday May 29, 2026 at 8:00 AM Eastern**, explicitly framed as the first of the 3 budgeted meetings. He then pulled this forward and convened the working group on **Monday May 25, 2026** instead.

**Pavel's framing of the kickoff agenda.** Pavel said the kickoff should open by voicing the problem to the room: "We don't have people who can constantly maintain a framework. It's dynamic. We don't want to maintain it. How do you see solving this problem?" Then let attendees respond.

**Val's closing reminder.** Don't let people leave the meeting — otherwise the thought escapes. *"If you let him leave after 1 meeting, that's a checkout."*

## Decisions Made

- **Working-group composition shifted** from Val's Part 1 proposal (Irina, Pavel, Biratko, Kharetski) to Pavel's expanded proposal in Part 2 (Khamin, Shpak, Tsimanov, Biratko, Samusenko, Pavel). Val endorsed and further expanded. The **final operative group** that actually convened on May 25: Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko, Alexey Khamin, Ivan Shpak, Evgeny Kharetski, Vladimir Samusenko, Sergey Tsimanov, Dzmitry Chudzinau. (Both Part 1 and intra-Part 2 lists are **superseded**.)
- **Test architecture pivots from "framework" to "agentic data-contract-driven composition."** Static testing frameworks are rejected because data contracts in JVL's 13-repo network are inherently dynamic. Tests will instead be composed at runtime by an agent reading the current data contracts. (Pavel proposed direction; Val locked it as the working hypothesis.)
- **Meeting methodology: "choking meetings."** The working group meets in person, recorded, with active pressure on participants throughout. No "go think about it" dispersal. Between meetings: feed the transcript to AI to surface the next direction. (Val mandated.)
- **3-meeting budget for the cycle.** (Val committed.)
- **Kickoff pulled forward from Friday May 29 to Monday May 25.** (Val executed.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Lead the working group as a "choking meeting": frame the problem (no maintenance budget for static framework; dynamic data contracts), pressure-test ideas live, don't let anyone disengage, record the session, hand the transcript to AI between sessions to derive direction for the next meeting. | First meeting: May 25 (held); cycle completes by ~mid-June 2026 | High | Val explicitly named Pavel as the meeting driver and the "infection carrier." |
| 2 | Working group (10 people, listed above) | Across 3 meetings, produce JVL's working theory for transactional E2E testing built on **dynamic agent-driven test composition from data contracts** — not a static framework. Output should be flexible, low-maintenance, and expressible in language readable by both humans and agents. | By end of 3-meeting cycle (~mid-June 2026) | High | Supersedes Undertaking #1 from Part 1. |

## Engineering Signals

### Confirmed Signals

- **ADR — Reject static testing framework for transactional in favor of agentic dynamic test composition from data contracts.** This is the central decision of the meeting. Captured here as a strong ADR candidate: "JVL will not build a maintained transactional E2E testing framework. Tests will be composed at runtime by an agent reading the current data contracts across the 13-repo network."
- **CAP — Agent capability: read all data contracts across the repo network and compose E2E tests from them.** Val explicitly framed this as the leverage point — drudgery for humans, routine seconds-to-minutes work for an agent.
- **REQ — Test approach must be flexible, low-maintenance, and expressed in language readable by both humans and AI.** Pavel's stated requirement; Val endorsed.
- **Methodology decision — "Choking meeting" format with 3-meeting budget per design cycle.** Val coined and mandated this as the JVL meeting style for architecture/design questions.

### Suspected Signals

- **Possible REQ — Data contracts must be machine-readable in a form an agent can ingest.** Implied by the agentic-test-composition direction but never explicitly stated as a requirement on the data-contract format itself. Worth surfacing in the kickoff.
- **Possible ADR — Data contracts become the canonical source of truth for both inter-repo integration *and* test coverage.** This widens the role of data contracts significantly; deserves explicit architectural acknowledgment.

## Open Questions

- Where do the data contracts currently live, and in what format? The agentic approach hinges on this being machine-readable.
- How does the agentic-composition approach interact with the NOVA platform's E2E work (Anton Liashkevich)? Not discussed in Part 2.
- Why was Dzmitry Chudzinau added to the operative group (he wasn't named in either segment of the May 22 transcript)? Likely a Val-level addition between May 22 and May 25.

---
*Processed from Teams transcript on 2026-05-25*
*Source meeting: Testing framework for transactional products — Part 2 — May 22, 2026*
*Working-group note updated 2026-05-25 from Val's confirmation of the 10-person operative group*
