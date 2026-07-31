# Meeting Summary — This and That (QA Strategy in the AI Development Cycle)
**Date:** May 28, 2026, 2:31 PM Eastern
**Duration:** ~1h 7m
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian (summarized in English)

## Summary

An open discussion about how QA and testing should fit into JVL's new AI-driven development cycle (GitHub feature branches, Claude Code agents, CI/CD). No firm process was settled. Val opened by saying he is spending real time studying how leading companies handle this, and he wants to know how the Minsk team's thinking is moving. He warned that if the team isn't pushing hard on it, it becomes a problem soon, because the right approach takes time to mature and cannot be rushed.

**Current state (Irina).** The team is still using its old testing approach and is still working out how the GitHub repositories and the new process fit together. Irina has been reading the platform documentation to understand how it is built before deciding where testing fits.

**What changed (Pavel).** During development, the AI (Claude Code) already runs many tests on real machines and records what it did in the pull-request and code-review notes — which machines, which steps. The weakness: those runs are not saved as a repeatable test plan, so they happen "invisibly" from QA's point of view.

**Val's idea — capture AI tests into a standard.** Give the agent an instruction (a Claude Code "skill") so every test it runs during feature-branch integration is written down in an agreed format. Let the AI study how tests are written today, propose a standard format Val approves, then convert its own runs into reusable test cases in that format. The team noted they don't yet have such a skill.

**The "bricks" idea (Pavel, credited to Andrei).** At pull-request time, ask the AI to write small, reusable regression ("retrospective") tests — positive and negative — into a dedicated test repository. Over time the AI picks the right bricks to assemble full end-to-end tests and checks them for conflicts and dependencies. These guard against the AI breaking something elsewhere, which the team says happens often.

**Scale and control (Val).** Val pushed back on the team's instinct to build a structure or database of all tests to "lean on" and manage by hand. His view: don't try to read or cover everything. If tests run in minutes on always-on environments (he cited ~500 running day and night), let them run constantly — tests that find errors are useful, and tests that find none are equally useful. Human-run testing is slow and costly; AI-run testing is cheap (just electricity). He cited an Elon Musk interview: soon AI will be too capable for humans to supervise its output directly, so designing a heavy human management layer is the wrong bet.

**Data contracts as the QA anchor (Val's firmest point).** Each integration is kept to roughly 200–400 lines of code and produces a versioned change to the repository's data contract plus its associated actions. Because the data contract is the one dynamic, deterministic record of change, QA should tie to data-contract changes and actions. Pavel agreed the data contract is the easy-to-grasp deterministic part, but cautioned that some behavior (timing, randomness, human input) is not captured by data contracts.

**Triggering tests on the pull request.** Pavel proposed that a PR action should build, deploy to the right environment, run integration tests, and — if the data contract changed — verify the contracts, before merge to main. All agreed on the sequence: if the integration test fails there is nothing more to check; if it passes, run end-to-end; if that passes, merge the feature branch to main (by hand for now, by AI later). Irina argued contract compatibility between paired systems (server vs. client, handled by different developers — she named Chudzinau as one) needs checking earlier, so one side isn't left waiting; Pavel argued the contract only needs checking when two modules actually integrate.

**Why this matters for JVL (Val's close).** Val believes a small company's advantage is that it can raise output with the same people, while big companies (he named Microsoft) carry heavy management layers and cannot adopt AI as cheaply. He wants to capitalize on that, and asked Pavel to keep iterating on the approach.

## Decisions Made

- **Tie QA to data-contract changes and their associated actions.** Reason: the data contract is the only dynamic, deterministic record of what changed per integration step. (Endorsed by Val; agreed by Pavel at the single-step / single-repository scale.)
- **Run tests on the pull request, in sequence, before merge to main** (integration → end-to-end → merge). Reason: no point running end-to-end if integration tests fail. (Agreed by Val and Pavel.)
- **Do not build a large human-managed test database to "control" AI test output.** Reason: the volume will grow beyond human tracking; let tests run continuously instead. (Val's position; not fully reconciled with the team.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Run a brainstorm / triage on how QA fits the AI development cycle; iterate over a couple of think-and-step-away rounds before settling an approach | TBD | High | Val's main ask; the approach is unsettled and Val wants it to mature properly |
| 2 | Pavel Frolov | Discuss the AI-driven development approach (the one Biratko described in repo standard 5.1) with Andrei Bosik and Evgeny Kharetski — not Biratko for now | TBD | Normal | Val finds Biratko's position hard to read; Andrei has a clear point of view |

## Open Questions

- How to wrap "real world" steps (real phone, real email for customer registration) into virtual / automated tests — e.g., using virtual phone/SMS services. Raised by Pavel.
- When should regression ("retrospective") tests run — at release, or on demand via the AI? No single answer; a rule to be worked out during development.
- Where does QA's scope start and end for an end-to-end flow on the Flex platform? Raised by Irina; unresolved.
- At what point must paired data contracts (server vs. client) be checked — early, to avoid one side waiting (Irina), or only at module integration (Pavel)? Unresolved.
- Whether to emulate all devices, and how to do it in practice. Raised by Irina.

---
*Processed from Teams transcript on May 29, 2026.*
*Source meeting: This and That — 20260528_103152-Meeting Recording (recorded May 28, 2026)*
