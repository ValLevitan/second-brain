# Meeting Summary — Testing Framework for Transactional Products

**Date:** May 22, 2026, 12:02 PM (Eastern)
**Duration:** ~30 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian (summarized in English)

> **See [Part 2](Meeting_Notes_Transactional_E2E_Testing_Framework-Part_2-May-22-2026.md)** — the 4-person study group named in this note (Irina, Pavel, Biratko, Kharetski) was **superseded** in Part 2 by a 10-person operative working group: Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko, Alexey Khamin, Ivan Shpak, Evgeny Kharetski, Vladimir Samusenko, Sergey Tsimanov, Dzmitry Chudzinau. Part 2 also pivoted the test architecture from "framework" to **agentic data-contract-driven test composition**. Treat Part 2 as the current direction.

## Summary

**Context (Val's opening recap).** Val recapped the broader initiative this meeting fits into. Biratko authored a standard (v5.1, ~3 weeks ago) defining how to structure repos so Claude or other AI can work across them autonomously. Concept: a Product Owner produces the bill of features and requirements; an AI agent decomposes those features into the correct repos; a properly structured repo network lets AI iterate on the product. They picked the **transactional product** as the pilot. 13 repos are now under monitoring; Biratko owns one, others are owned by different team members. Andrei Bosik has been monitoring the repos and it's working reasonably well — the theory holds for transactional.

**The question that triggered the meeting.** During that monitoring work, the question of testing surfaced: when feature branches merge into master, some end-to-end check should run that confirms the product still builds and behaves. **Who writes this? What kind of thing is it? How does it work?** Val was told it'd be similar to what Anton Liashkevich writes for the NOVA platform — but he's uncertain that reference holds for transactional.

**Pavel's response: NOVA-style framework doesn't port cleanly to transactional.** NOVA is a universal framework wrapping a set of reusable games. Transactional products / kiosks differ much more significantly from one to the next. A testing tool built for one repo will likely look very different from the next. *However* — if you build architecture for automatic terminal testing, you can identify common moments inherent to all kiosks: loading, displaying installation messages, registration, displaying general error states. That common functionality could be reused — including for tests. Irina agreed each kiosk is a self-contained product.

**Val's counter-argument on stability.** Speaking explicitly as a non-specialist: transactional feels *more stable* than gaming equipment, so it's hard to understand why gaming can be E2E-tested automatically but transactional can't. He doesn't accept the premise that transactional is too varied to automate.

**Val's argument on why automation matters (the real reason).** The push for automation isn't because human time is expensive — it's because **you can't hire enough testers to keep pace with developers**. If testing stays sequential (build, then test), that sequence becomes the bottleneck on release. Hiring 100 testers is theoretically possible but operationally a nightmare — load fluctuates, headcount can't. The only viable path: build the dev-test process **in parallel, not sequentially**. He doesn't have the answer for how, but the fact that other organizations do it means JVL can too — they just haven't learned how yet.

**Val's history-of-testing argument.** Years ago, the dogma was "QA writes tests." That quietly shifted: programmers write unit tests (always have). Then quietly: developers also write integration tests, despite earlier insistence that "integration tests are QA's job." His read: **E2E tests are now drifting toward developers too**, but the discussion is dishonest about it. Evgeny Kharetski told him that "anyone can write E2E tests" — Biratko, Mitsevsky, etc. Irina objected: Kharetski says that because he's a former QA. Val pushed back: no, Kharetski was naming people *outside* QA who could write them. Kharetski also said involving Mitsevsky in the topic would be interesting.

**Val's framing of bugs (key philosophical position).** Bugs aren't planned work — they're a **scope gap** or a **test gap**. If a bug is caught at integration test, that's the integration test doing its job. If a bug *isn't* caught there, the integration test itself has a gap. So you don't fix the bug — you fix the test that should have caught it.

**Pavel's pushback on the bug framing.** Pavel disagreed with "bugs are not planned work." You fix both the code and the test, and that work still has to be planned somewhere — just not within the original feature's scope. Irina reframed it: not within feature implementation scope, but as separately-planned remediation time. Val agreed he didn't mean bugs magically fix themselves — only that you don't budget "12% bugs" into a feature.

**Val's projection forward.** If AI is going to develop the code, focus must shift entirely to **scope definition** — what the market wants, what's specified for the programmer (or agent). Under that assumption, in theory there shouldn't *be* bugs. A bug only arises from a scope gap (what was asked vs. what was built) or from incorrect data contracts between repos. Code should come out clean at integration. As code grows, absolute bug count may rise — but in % terms it should fall, and if it doesn't, the failure is upstream in scope definition and product/dev alignment.

**Val's directive — form a 4-person study group.** Val's central ask: **Irina, Pavel, Biratko, and Kharetski should meet as a four-person group**, study how other organizations (he cited Microsoft, IBM as examples) handle this, read up, think, and **create JVL's own theory and philosophy** for E2E testing on transactional. JVL has no fundamental policy here. "We do it this way because we always did it this way" is unacceptable — that's the kind of anti-pattern (skrepa) Val won't engage with. A solid conversation starts from "here are three practical approaches we found at real companies, here's the theory, let's discuss." He acknowledged he's not an engineer and can't learn everything himself, but he's actively interested in the topic. The Liashkevich-for-NOVA model is a starting reference but he's uncertain Liashkevich can think deeply enough — fast but possibly shallow (he likened it to the young-bull/old-bull joke).

**Pavel's framing of the universality problem.** For games, JVL can build its own framework and reuse it. For other (transactional) projects, the team needs to go deeper into fundamentally different approaches — possibly very different from gaming — that are still universal enough that JVL doesn't have to hunt for a new specialist with every product launch. **Ideal:** the same actor who writes the code also develops the E2E test for it.

**The "same person or two agents" exchange.** Irina objected — same human can't do both code and E2E. Pavel: don't call it a human, call it an agent. Irina: then two different agents — but humans still manage agents. Pavel: in a year or two, no human manager. Irina (half-joking): right, in a year the agent will be telling *us* what to fetch.

**Val's closing philosophical point — labor shortage thesis.** Val pushed back on any pessimism. He recalled visiting Manhattan and learning the skyscrapers housed financial computing centers that had replaced cities of quants doing manual calculation. Now data centers are replacing those buildings — a building staffed by 5 people does the work. Yet **his personal workload has gone up, not down**, over the past 5 years. His prediction: global **worker shortage**, not surplus. Pavel agreed it's already underway. Val ended the recording there before going further into philosophy.

## Decisions Made

- **Form a 4-person E2E testing study group: Irina Shishko, Pavel Frolov, Alexander Biratko, Evgeny Kharetski.** They are to study external practical approaches (Val cited Microsoft and IBM as illustrative starting points), read, think, and produce JVL's own philosophy/theory for E2E testing on transactional products. (Directed by Val.)
- **Reject "we do it this way because we always did" reasoning.** Recommendations must be grounded in researched external practice. (Stated by Val; not contested.)
- **Bug-fix work must still be planned, even if not inside the feature's own scope.** Bugs arise from scope or integration-contract gaps, not from random feature-development overhead. (Pavel raised, Irina refined, Val agreed.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Irina Shishko, Pavel Frolov, Alexander Biratko, Evgeny Kharetski | Convene as a 4-person working group; research how Microsoft, IBM, and other organizations structure E2E testing for transactional / kiosk products; produce a written JVL philosophy and proposed framework for E2E testing on transactional, including what hooks the transactional platform itself needs to expose | TBD | High | Val explicitly named this as the core takeaway. JVL has no fundamental testing policy today and Val won't accept "we've always done it this way" as justification. Blocks any decision on who writes transactional E2E tests and how. |
| 2 | Pavel Frolov | Develop the architectural sketch for a transactional E2E framework that captures common kiosk capabilities (boot/load, installation-time messaging, registration, error-state display) as reusable building blocks across the 13 transactional repos | TBD | Normal | Pavel raised this in the meeting as the bridge between "every kiosk is unique" and "we need a universal framework." Feeds directly into Undertaking #1. |
| 3 | Val Levitan | Decide whether to bring Igor Mitsevsky into the testing conversation (Kharetski flagged this would be interesting to Mitsevsky) | TBD | Normal | Mitsevsky was named as a potential E2E test author. Kharetski volunteered the suggestion. No decision was made in the meeting. |

## Engineering Signals

### Confirmed Signals

- **REQ — E2E testing framework for transactional platform:** Val explicitly stated the need for "hooks to put into the transactional platform for correct E2E testing" and for a framework (or "something else for an E2E tester") that runs on every merge of feature branches into master. Triggered by, but distinct from, the existing repo-structure standard v5.1.
- **CAP — Common transactional kiosk capabilities:** Pavel identified a shared capability set across all transactional kiosks: boot/load, installation-time message display, registration, general error-state display. Proposed as a reuse layer for both functionality and tests.
- **ADR-candidate — Bug-as-scope-gap framing:** Val laid out a position that bugs reaching E2E indicate either a scope gap (what was specified vs. what was built) or a data-contract gap between repos, not feature-development sloppiness. Worth capturing as a guiding ADR if it survives the 4-person group's scrutiny.

### Suspected Signals

- **Possible ADR — Single-agent vs. dual-agent for code + E2E:** Pavel proposed the same code-writing agent also develops the E2E tests. Irina pushed back ("two different agents"). No decision reached.
- **Possible REQ — Inter-repo data-contract validation:** Val mentioned wrong data contracts between repos as a primary source of integration-time failures. Could become a formal requirement for tooling that validates contracts across the 13-repo network.
- **Possible Solution — Parallel dev-test process:** Val's stated principle that the dev/test pipeline must run in parallel rather than sequentially. Implementation path not yet defined.

## Open Questions

- Who specifically writes the E2E tests for transactional? Anton Liashkevich was named as the NOVA reference; no name was committed for transactional. The 4-person group is supposed to surface a recommendation.
- Is the deliverable a "framework" or "something else"? Val himself was uncertain about the right term.
- Does the answer end up being one universal transactional E2E tool, or per-repo tools sharing a common capability layer? Pavel leaned per-repo with shared layer; not resolved.
- Will Evgeny Kharetski and/or Igor Mitsevsky participate beyond just Kharetski being one of the four named? Val to decide.

---
*Processed from Teams transcript on 2026-05-25*
*Source meeting: Testing framework for transactional products — May 22, 2026*
