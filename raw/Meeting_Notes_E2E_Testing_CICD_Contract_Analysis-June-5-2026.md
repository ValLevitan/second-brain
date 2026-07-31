# Meeting Summary — E2E Testing in CI/CD (Follow-up, briefing Lesha)
**Date:** June 5, 2026, 11:59 AM Eastern
**Duration:** ~1h 42m
**Attendees:** Val Levitan, Alexey Khamin (Lesha), Pavel Frolov, Andrei Bosik, Irina Shishko

## Summary

Alexey ran the first experiment toward AI-driven testing in CI/CD. The rule for the experiment: he doesn't hand-write code — he drives Claude, following Pavel's approach. He pointed Claude at two product repos: **Flex IQ** (well documented, has data contracts) and the **SDK** repo (no docs, no contracts). Claude analyzed each repo, then compared how they fit together.

Main finding: where a repo has documentation and contracts, Claude works faster and digs deeper — it analyzes on its own and even questions things. Where there are no contracts (SDK), Claude had to generate them itself, which is shakier.

Pavel was clear this is **not yet a real end-to-end test**. It's AI-assisted analysis of the contracts and descriptions that say how repos connect — closer to a static integration check than a live test.

**Data contracts.** A contract describes what an app exposes to others (its inputs/outputs), not its internal logic. It belongs to one repo and stays the same as long as the external interface doesn't change — internal code can change without touching the contract. Example (Andrei): we consume Dwolla through their API; their internal changes don't change our contract. Our own apps talk the same way (e.g., Payment Hub reads Location Billing's contract to know how to call it).

**The signals.** Claude's report marks each check green (match — works), yellow (possible risk/mismatch to review), or red (one app expects something another doesn't provide). Val's working theory: if repos are built right per Standard 5.1 (independent, zero-trust, clean data contracts), the analysis goes green. Yellow means a repo is "dirty" — mixed concerns, missing description, or a hand-generated contract that may be wrong (as with the SDK).

**Source of truth — the key debate.** Contracts are generated from code, but Irina warned code can be wrong, so code alone can't be the truth. The group converged: a contract must be checked against **requirements** at the moment it's generated (an action inside the repo). After that, the test trusts the contract and only verifies the apps actually run and talk to each other per the contracts.

**The ADR breakthrough.** Most yellow signals aren't business requirements — they're technical decisions nobody wrote down. Pavel's example: two files do the same job (registering a scanner in the device list); writing that as a Jira requirement would flood Jira with millions of tiny entries. Val's conclusion: these belong in **ADRs** (Architecture Decision Records) — short technical-decision files that live in the repo, next to the code. Requirements are written by the business in business language; an ADR captures the architectural decision of *how*. Claude handles ADRs well, so the test should be pointed at them. Andrei agreed, and suggested acceptance criteria from Jira could be extra context later — Val was cautious that Jira criteria are too abstract for Claude, which wants concrete detail.

**Run history.** Alexey found that giving Claude a history of past runs makes it noticeably better — it revisits prior trouble spots, confirms what changed, and finds new issues each pass. Pavel: almost like learning from run history.

**Scope discipline.** Val pushed against covering everything at once. Build in small weekly steps — 50 small steps a year makes a strong system. The single "transactional platform" diagram that maps everything is "about everything and nothing"; each chunk (Flex IQ, Recycler, services) should get its own description of which repos it uses.

## Decisions Made

- **Continue the experiment as-is — don't change Alexey's direction or prompt approach.** The contract Claude generated is not being accepted as "truth" yet. (Val, agreed by Alexey)
- **Add one line to the prompt: also look at the ADRs** (alongside the data contracts). This is the only change for the next run. (Val, Pavel, Andrei)
- **ADRs live in the product repo they relate to** (next to the contracts); Alexey's test that runs the report lives in the integration repo. (Andrei, confirmed by Val)
- **Resolve the current yellow signals by writing the missing ADRs**, then re-run and compare the yellow count. Pavel expects ~70% of yellow remarks to clear — that would be the proof of concept. (Val, Pavel)
- **Contracts must be validated against requirements at generation time**, not just derived from code. (Pavel, Andrei, Irina)
- **Next meeting: Wednesday June 10, 8:00–9:00 AM Eastern.** Val will schedule it and attach this transcript. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexey Khamin | Re-run the Claude analysis on the same two repos (Flex IQ + SDK), adding one prompt line telling it to also read the ADRs; compare yellow-signal count vs. the current run | Wed June 10 | High | Core test of the theory that ADRs clear the yellow signals |
| 2 | Alexey + Pavel + Andrei | Write the missing ADRs explaining the decisions behind the current yellow signals; place each in the product repo it relates to | Wed June 10 | High | Pavel expects ~70% of yellow signals to clear once ADRs exist |
| 3 | Val | Schedule the Wed June 10, 8–9 AM ET follow-up; post this transcript to chat and include it in the invite description | Today | Normal | So the team has the record going in |
| 4 | Val | Set up a short follow-up with Pavel and Irina on the Flex IQ release sketch (~20 min out) | Today | Normal | Separate from the E2E topic |

## Open Questions

- Whether to also pull acceptance criteria from Jira as extra context, or rely on ADRs alone. Val cautious; Andrei wants ADRs first, Jira only if needed.
- Whether to move the ADR workflow to a draft→approval model (with a ship label). Deferred — try as-is first; some ADRs may need excluding from analysis (not yet implemented or abandoned).
- How automatic contract generation will be triggered and kept in sync once it's no longer run by hand.
- Longer term: expanding to running real artifacts/Docker images on a real environment. Flagged as a very large effort (ARM platform needs emulation); Pavel leans toward testing web services first.

---
*Processed from Teams transcript on June 5, 2026*
*Source meeting: E2E Testing in CI/CD — Follow-up (brief Lesha)*
