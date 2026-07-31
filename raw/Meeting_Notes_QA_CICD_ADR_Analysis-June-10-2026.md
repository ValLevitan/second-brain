# Meeting Summary — QA-Based CI/CD (ADR Analysis + Release Flow)
**Date:** June 10, 2026, 11:32 AM Eastern
**Duration:** ~1h 6m
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Alexey Khamin, Andrei Bosik

## Summary

**ADR / AI code-analysis experiment (Alexey).** Alexey reworked the existing GitHub action to run in one pass: first it analyzes the code with no ADR knowledge, then again with ADR awareness. It now produces two reports — the usual dependency/contract analysis, plus a new report showing what the ADRs changed. On a sample, the AI found 8 gaps without ADR context; with ADRs it fully understood and accepted 3, revised its view on 2, and left the rest open — roughly 62% of gaps clarified. The report also lists the most valuable ADRs, which ones didn't help (those not involved in cross-app interaction), and a recommendation: write an ADR whenever a system component is added.

Val pushed back hard on the report wording "moderately useful," arguing a result this strong should read as "needed," not lukewarm. Alexey clarified the AI wrote that label and it referred narrowly to the 3-of-8 fully-resolved subset (~33%), not overall ADR value.

**What an ADR is (Val).** Features are the output of architectural decisions; you record each decision as an Architecture Decision Record. The reverse also happens — a developer implementing a feature hits gaps or non-functional needs, goes back, makes more decisions, records them, then continues. Pavel noted ADRs now matter more because AI generates so much code that developers can't hold it all in their heads.

**ADR adoption.** The team agreed ADRs are necessary and should be applied to every feature, even small ones. ADRs live in each product repo under `docs/adr` (not in Jira), so the system stays ready even if they ever leave Jira. Irina raised that ADRs must be checked against requirements so a stale ADR isn't blindly trusted; Pavel and Val agreed to defer that requirement-vs-ADR cross-check for now rather than get bogged down.

**Release / CI-CD flow (second half).** Mostly an exploratory design walk-through using a worked example: adding modem support to a terminal. A PR into the platform SDK (RK3568) triggers a `.so` build; Claude reviews the PR, then unit/integration tests run and produce an artifact. RK publishes an updated contract to dependent products (Flex IQ, Recycler). They discussed GitHub pre-release vs release tagging: tag a pre-release after standalone tests pass, then run end-to-end tests against the services, then mark it a release. A passing E2E run feeds a version/compatibility matrix used to roll out only the changed artifacts. Deploy order matters but Andrei clarified wrong order only causes longer downtime (terminals wait and reconnect), not hard failure. They could not settle the flow verbally and decided to write it up and diagram it.

## Decisions Made

- **Adopt ADRs across all features, even small ones** — experiment showed ~62% of gaps clarified. (Pavel, endorsed by Val, Irina, Andrei)
- **ADRs are the developer/architect's responsibility**, written when a decision is made and reviewed by human eyes; stored in each repo under `docs/adr`, not Jira.
- **Defer ADR-vs-requirements (Jira) cross-validation** — add it later, don't stall the rollout now. (Pavel + Val)
- **Scale the AI ADR-impact report from 2 repos to all repos** of the transactional system; fix weak spots; add automatic contract generation to the action. (Andrei proposed, agreed)
- **Document the full release flow (commit → production)** via AI analysis plus a diagram, then review with the whole team. (Pavel + Andrei)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel + Andrei | Work out the full release/CI-CD flow (commit → production) in text, run AI analysis, produce a flow diagram | Thu Jun 11 (before noon) | High | Flow was too hard to follow verbally; needs visualizing before the all-hands |
| 2 | Val | Schedule + host the follow-up "Release" meeting to walk the team through the diagrammed flow (record it) | Fri Jun 12, 7:00 | High | Review the documented flow together |
| 3 | Pavel | Drive ADR adoption on every feature (already started with the team yesterday) | Ongoing | High | Experiment confirmed ADRs are needed; Val will enforce |
| 4 | Alexey | Expand the AI ADR-impact report from 2 repos to all transactional-system repos; flag missing ADRs/contracts | TBD | Normal | Scale the validated experiment; owner not crisply assigned — confirm |
| 5 | Dev team [owner TBD] | Add automatic contract generation to the GitHub action | TBD | Normal | So dependent products get updated contracts when a producer repo changes |

## Open Questions

- Do microservices need updating when a terminal-side capability (e.g., modem) is added? Pavel sees no immediate need, but it's open.
- Backward-compatibility / protocol-versioning approach for mixed-version fields.
- What counts as RK's "release artifact" — after standalone testing or after system-wide E2E? (Leaning: pre-release tag standalone, release tag after E2E.)
- Where to trigger final release/deploy — each product repo or centrally from the integration repo? (Leaning central, for single-point control + version tracking — per Alexey's read of what the AI would advise.)
- How deploy order/dependencies get captured and who owns it — release notes by the developer (Andrei) vs the architect (Val).

---
*Processed from Teams transcript on June 11, 2026*
*Source meeting: QA-based CI_CD — June 10, 2026 (Teams recording, transcription by Val Levitan)*
