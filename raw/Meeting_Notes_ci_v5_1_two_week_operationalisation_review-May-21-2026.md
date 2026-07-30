# Meeting Summary — CI Architecture v5.1 Operationalisation — Two-Week Review
**Date:** May 21, 2026, 11:58 AM Eastern
**Duration:** 1h 24m 57s
**Attendees:** Val Levitan, Andrei Bosik, Alexander (Sasha) Biratko, Evgeny Kharetski

> **Sequence note:** This is the **two-week checkpoint** anchored at the April 30 CI Architecture Governance Framework Review (see `CI Architecture Governance Framework Review-April-30-2026/`). Aaron Bockelie — who originally drove the v5.1 reading and the ramp plan — was absent for this review (new job, very busy; Andrei noted he hasn't been visible for weeks).

## Transcript Quality Note

Conducted in Russian. Summary in English. The conversation worked from two shared documents Andrei dropped into chat (Russian + English versions of the compliance report + framework) plus a live screen share of the compliance dashboard. The report files themselves carry granular per-repo / per-day data not reproducible here — the summary captures the verbal substance.

## Summary

The review served three purposes: (1) **first operational checkpoint** of the v5.1 standard + structure-compliance framework (v0.1) Andrei wrote, after ~10 days of real-world running; (2) **work-through of the framework's open questions** that emerged during operation; (3) **commitment to next steps**, including a new end-to-end test workstream for the transactional payment products and a next checkpoint on **June 11**.

**Aaron's absence acknowledged.** Andrei opened by asking whether Aaron would join; Val: unlikely — Aaron has started a new role and is heavily occupied. Andrei noted Aaron hasn't been seen in weeks. The team proceeded.

**Scope confirmation.** The 13 repositories under structure-compliance monitoring are all **transactional-equipment repositories** (Andrei's, Sasha's, Dima Chudinov's, and Sergey Tsimanov's repos). Andrei extended **CODEOWNERS to all GitHub repos** as a side effect (not just the 13) — he walked the org-level repository list, identified historical committers, and hand-curated the actual owners.

**Code-owner-count policy: minimum 2 per repo.** Andrei explained the rationale: vacation / illness / departure coverage. If a repo has only one owner and that person is out, pull requests stall. Val initially recalled the original policy as 1 owner per repo; Andrei corrected — they had agreed on a *minimum of 2* (and ≤3) precisely to avoid the single-point-of-coverage failure. Some repos still have only 1 owner where 2 isn't possible.

**Compliance statuses — 5 possible verdicts.** When the framework checks a repo against a standard item, it emits one of:
- **PASS** — clean.
- **FAIL** — systematic violation persisting more than 3 consecutive days. Single-day or short-duration deviations are not flagged as FAIL (people self-correct).
- **WARNING** — borderline.
- **REVIEW** — the framework cannot determine PASS/FAIL automatically; **human judgment required**.
- **N/A** — the standard item doesn't apply to this repo.

**Results so far: clean.** Over the ~10-day window:
- **Only one FAIL recorded** — documentation language regression: an English documentation file was rewritten into Russian (violating the standard that all docs are English), caught, then rewritten back to English. FAIL appeared while the regression was live; cleared on correction.
- **May 19** caught a separate transient error on one repository; resolved by today (May 21).
- **All previously-red items** from the start of the window have been remediated. Andrei showed the May 11 baseline (broadly red) versus today (broadly green).

**The "REVIEW" status is the bottleneck.** Many fields in the compliance dashboard end up in REVIEW status because the automated checker cannot deterministically verify the standard. Examples:
- **Section 22 of the standard** (API testing coverage): the script can find that the repo has some test code, but cannot verify that the tests actually exercise the contract correctly.
- **Contract correctness** generally: how do you confirm that the API actually returns what the contract says it should?

**Val's hard rule: REVIEW cannot scale via human triage.** *"Looking at the number of repos requiring human review, this will become a bottleneck. If we don't have the capacity to systematise the manual reviews, we'll bury the whole effort — and the rest of the automation we're building is rendered pointless if humans are still doing the review by hand."*

**Approach to closing out REVIEW items — Sasha's framing.** The team worked through several alternative paths:

1. **Mini-test action that calls each API and compares to the OpenAPI spec** (Evgeny's initial proposal). Andrei's pushback: this only works for one class of REVIEW item; many others (e.g., unit test coverage percentage, integration test coverage) need a different approach.

2. **Test framework as part of the structure-compliance framework itself** — Sasha pushed back: *"this puts the testing responsibility on the wrong tool. The compliance framework should verify standards conformance, not run the tests. Tests should live in the repository's own pipeline."*

3. **Artifact-based pattern (the landing decision):** Each repo's CI action **emits a log artifact** (or set of artifacts) at build time containing test-run results — pass/fail, coverage percentage, etc. The structure-compliance framework **reads those artifacts** to know if the standard is met. This separates "running the tests" (repo's CI does that) from "verifying that tests exist and pass" (compliance framework does that).

Val supported the artifact path. Sasha: *"this is the right division — tests run where they belong, the compliance framework just confirms they ran."*

**Contract handling clarification.** Andrei believed the **API contract file** was hand-authored as a separate artifact in each repo and that the framework should compare it to the API. Sasha corrected: **the contract is *generated* from the code at build time** (OpenAPI / Swagger style — derived from the project's source annotations). There is no separate hand-written contract file. Implication: the compliance framework should verify **the contract artifact's *presence* in the build output**, not validate it independently. Andrei accepted and will revise the framework's contract check accordingly.

**DORA metrics layer — Andrei's second reporting layer.** The structure-compliance report is **Layer 1**. The **DORA metrics report is Layer 2** — separate report, separate data source. Andrei adopted **Google's published DORA thresholds** as the initial baseline because JVL doesn't yet have its own historical distribution to set local thresholds from:

- **Elite:** ≥ 1 release per business day.
- **High:** ~weekly.
- **Medium:** ~monthly.
- **Low:** no releases in 6 months.

Val: these thresholds are configurable, JVL-customisable per company maturity, and revisable annually as the team's cadence shifts. The Google baselines are "quite strict" but JVL already shows up reasonably against them.

**What DORA actually measures — clarification.** Sasha asked whether DORA was counting commits or builds. Andrei: it tracks **CI/CD action executions** — the GitHub Action run events. If a commit doesn't trigger an action (e.g., a documentation-only commit), it doesn't move the DORA number. If a single commit triggers multiple actions (e.g., a dev action + a release action), that counts as 2.

**Sasha proposed splitting DORA into two reports** — one tracking *release* cadence, one tracking *general build/merge* cadence. Andrei: possible, just need to clarify how to distinguish the two action types. Deferred — the current numbers are informative enough to start.

**Should we extend monitoring to more repos?** Andrei asked. Val: **no — stay focused on the 13 transactional repos.** Extending the structure-compliance framework right now is premature; let it stabilise on the current scope. Continue monitoring; refine the report's accuracy per the discussion.

**New workstream: end-to-end (E2E) test framework for transactional payment products.** Long stretch toward the end of the meeting. Triggered by Val's observation that without automated E2E, the manual-review bottleneck never goes away.

- **NOT a part of TS-360 (Test-360).** TS-360 is the existing test framework for the **game side** (game framework + LGS testing) under NOVA. TS-360 was written historically by Sasha Korochkin and team; substantial code exists for game-flow testing.
- **NEW separate framework** for **transactional payment system** E2E testing. Sasha: *"this is a different system — it's not the game flow, it's transaction protocols, ticket creation, wallet operations, data passage between aplliances."* Lives in its own repo.
- **Anton Leshkevich is NOT the right owner** for the transactional E2E framework. He's busy on the NOVA-side TS-360 work. The transactional E2E framework needs a different owner.
- **Andrei Bosik proposed Aleksey "Lyosha" Khamin** as the architect/owner for the new transactional E2E framework. Reasons:
  - Khamin is already doing some automation work and tests on Cleo.
  - He had worked alongside Korochkin previously on TS-360.
  - Evgeny: Khamin is a strong programmer; technically capable.
  - Khamin "lit up" when he heard about the Rust migration — he wants to work on the new tooling, not stay on legacy C games.
- **Val: I see Khamin as a future Product Manager** — flagged as an aside, but his career arc may be product-side eventually. He'll consult Pavel on the Khamin assignment.

**Infrastructure questions for the new E2E framework:**
- **Where does the system under test run?** Evgeny: it should run isolated in Docker containers, locally or in a cloud-hosted private slice — not shared infrastructure. Andrei: launching ~10 containers in a GitHub Action runner is expensive and complex but feasible.
- **Should it test the staging environment** (the team's actual staging slice in Amazon), or a self-deployed isolated stack? Evgeny preferred isolated; Andrei argued staging is already there and proven, so use it. Compromise: hybrid; details TBD.
- **Hardware emulation:** for components like Flex-POS (which has its own hardware reader / dispenser), the E2E framework will need to emulate the hardware peripherals — same way TS-360 already emulates bill validator behaviour. *"The price of having automated tests is that you have to emulate the hardware."*
- **Database access from the test framework:** Sasha suggested either (a) direct query access to the test database deployed in Docker, or (b) adding a test-only API hook to each microservice that exposes a query interface. Option (b) is cleaner. Evgeny: "as one option, yes."

**Khamin's readiness assessment.** Andrei: *"he's probably not fully ready right now, but if he wants this, he can grow into it. He's an engineer. The biggest question is architecting the test framework cleanly — writing the tests themselves is a 10."*

**No expansion to NOVA repos yet.** Val confirmed: stick with the 13 transactional repos for both structure-compliance and DORA monitoring through the next checkpoint.

**Closing summary by Andrei — what changes get implemented before the next checkpoint:**

1. **Compliance framework reads CI action artifacts** (log file containing unit test results + coverage percentage) to remove the REVIEW status on test-related items.
2. **End-to-end testing for payment system** integrated similarly — once the E2E framework exists, its results flow through the same artifact pattern.
3. **Contract check changed from "validate" to "verify presence"** since the contract is generated from code at build time.
4. **Andrei asks Dima Chudinov and Sergey Tsimanov** to update their CI actions to emit the log artifact during the run. They've already been "looking sideways" at Andrei for asking process changes — they say "ask Pavel to plan this with us." Andrei will route through Pavel.
5. **3 weeks** to next checkpoint — better than 2 weeks because the changes Andrei is making + the dev work Chudinov/Tsimanov need to do takes some weeks to settle. Val initially proposed 4 weeks; Andrei pushed back to 3. **Next meeting: June 11, 2026, 8 AM Eastern.** Val to circulate.
6. **New undertaking:** find an architect for the new transactional E2E framework. Val to consult Pavel; team flagged Khamin as the primary candidate.

Val asked Andrei to send him the meeting transcript via Microsoft chat at the end.

## Decisions Made

- **Continue structure-compliance + DORA monitoring on the same 13 transactional-equipment repos.** No expansion to other repos / NOVA yet. (Val.)
- **Code-owners policy: minimum 2 per repo, max 3.** Vacation/leave coverage. (Re-confirmed — was originally agreed at the April 30 meeting.)
- **REVIEW status is the bottleneck and must not scale via human triage.** Automated alternatives must be found. (Val.)
- **Artifact-based test verification.** Repos' CI actions emit log artifacts containing test results + coverage; structure-compliance framework reads the artifacts. Tests run where they belong; compliance framework just verifies they ran. (Val + Sasha + Andrei.)
- **API contract is generated from code at build time** (OpenAPI-style) — not hand-written. Compliance framework verifies *presence* of the contract artifact, not its content. (Sasha → Andrei.)
- **DORA thresholds: start with Google's published baselines (Elite ≥1/day, High ~weekly, Medium ~monthly, Low ≥6 months no release).** Customisable as JVL collects its own distribution. (Andrei.)
- **DORA tracks CI/CD action runs**, not commits — documentation-only commits don't trigger actions and don't move DORA. Multiple actions per commit count separately. (Andrei.)
- **New separate E2E framework for transactional payment products** — distinct from TS-360 (which serves the game side under NOVA). Separate codebase, separate repo. (Sasha + Evgeny + Andrei.)
- **TS-360 stays on the game side / NOVA.** Anton Leshkevich is NOT the owner of the new transactional E2E framework. (Val + team.)
- **Aleksey Khamin proposed as the architect / owner of the new transactional E2E framework.** Val to consult Pavel before final assignment. Val also flagged Khamin as a future Product Manager candidate. (Andrei → Val.)
- **Next checkpoint: June 11, 2026, 8 AM Eastern.** Three weeks out (not four). (Val + Andrei.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Update structure-compliance framework to read CI action artifacts (log file with unit test results + coverage percentage) for REVIEW-status items | Before June 11 checkpoint | High | Removes the human-review bottleneck on test-related items |
| 2 | Andrei Bosik | Change contract check from validation to presence-verification | Before June 11 checkpoint | High | Contract is build-generated, not hand-authored |
| 3 | Andrei Bosik | Coordinate with Pavel to schedule the work Dima Chudinov and Sergey Tsimanov need to do — add log-artifact emission to their CI actions | Soon | High | Chudinov + Tsimanov pushed back on direct asks; route via Pavel |
| 4 | Dima Chudinov + Sergey Tsimanov | Add log-artifact emission to their CI actions on their repos | Before June 11 (Pavel-scheduled) | High | Required input for the compliance framework's artifact-reading update |
| 5 | Andrei Bosik | Continue monitoring the 13 transactional repos; refine status accuracy per discussion | Through June 11 | High | No scope expansion |
| 6 | Val Levitan | Circulate June 11, 2026, 8 AM Eastern invite for next CI v5.1 review checkpoint | This week | High | 3-week cadence |
| 7 | Val Levitan | Send Andrei the meeting transcript via Microsoft Teams chat | After this meeting | Normal | Andrei requested |
| 8 | Val Levitan | Consult Pavel on assigning Aleksey Khamin as the architect / owner of the new transactional E2E test framework | Before June 11 | High | Pavel's input gates the assignment |
| 9 | Val Levitan + Pavel | Decide on the architect for the new transactional E2E framework; if not Khamin, identify alternative | Before June 11 | High | Cannot proceed with E2E framework design without an architect |
| 10 | Andrei Bosik + future E2E architect | Define the new transactional E2E framework architecture: container-based isolated infrastructure; database access path (direct or via test-only hook); hardware emulation for Flex-POS peripherals | Through next iteration | High | Discussed verbally; design needs to land in writing |

## Engineering Signals

### Confirmed Signals

- **ADR — Structure compliance framework v0.1 stays in production scope of 13 transactional repos** through next checkpoint. No NOVA expansion yet.
- **ADR — Code-owners policy: 2 minimum, 3 maximum per repo.** Coverage rationale.
- **ADR — Test verification via artifact-reading.** Repos' CI emit log artifacts; compliance framework reads them. Decouples test execution from compliance verification.
- **ADR — Contract is generated from code at build time** (OpenAPI style). Compliance framework verifies *presence*, not content.
- **CAP — DORA metrics monitoring** layered separately from structure compliance. Two reports, two data sources.
- **ADR — DORA initial thresholds = Google baselines** (Elite ≥1/day, High ~weekly, Medium ~monthly, Low ≥6 months silent). Configurable for JVL maturity.
- **ADR — DORA tracks CI action runs, not commits.** Documentation-only commits do not appear.
- **CAP — Separate E2E test framework for transactional payment products.** Distinct from TS-360 (game side / NOVA). New repo, new owner.
- **CAP — Hardware emulation as a price-of-entry for transactional E2E.** Flex-POS readers, bill validators, dispensers must be emulated in the test framework — same pattern as TS-360 emulates game-side hardware.
- **CAP — Test-only API hook pattern.** Microservices may expose a test-only endpoint for the E2E framework to read internal state — cleaner than giving the framework direct DB access.
- **Engineering Solution — Pavel as the routing point for cross-team process changes.** When Andrei needs Chudinov/Tsimanov to do extra work, the path is through Pavel for scheduling — not direct asks.

### Suspected Signals

- **Possible REQ — Split DORA reporting into "release cadence" + "merge cadence" sub-reports.** Sasha proposed; Andrei accepted in principle. — *Should this be a tracked enhancement for the next iteration of the DORA report?*
- **Possible CAP — Cloud-isolated test environment for the new E2E framework.** Evgeny argued for it; Andrei pushed back on cost. — *Val, does this warrant a separate decision (use staging) vs (provision isolated cloud) for the new framework?*
- **Possible ADR — Khamin as Product Manager candidate.** Val flagged this as an aside; Khamin's actual product-manager development path is not currently tracked. — *Worth surfacing as a personnel development plan?*

## Open Questions

- **Who is the architect for the new transactional E2E framework?** Khamin is the leading candidate; Val to consult Pavel.
- **Does the new E2E framework deploy isolated infrastructure or use existing staging?** Architectural decision needed before any code is written.
- **How does Flex-POS hardware peripheral emulation get built?** Pattern is known (analogous to TS-360 bill validator emulation), but specific peripheral list and emulation depth need scoping.
- **How are Chudinov / Tsimanov's CI action changes prioritised against their existing work?** Pavel-mediated, but the actual scheduling not pinned.
- **What's the exact division between TS-360 (game side / NOVA) and the new transactional E2E framework?** Some overlap risk on protocol-testing — interactions between the game side and transactional side.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: CI Architecture v5.1 Operationalisation — Two-Week Review (20260521_075803)*
