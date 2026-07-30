# Meeting Summary — Flex_Recycler Requirements Working Session
**Date:** May 4, 2026, 1:01 PM Eastern (transcribed wrap-up segment)
**Duration:** ~8 minutes (transcribed portion only; full meeting ran longer, transcription was started mid-session)
**Attendees:** Val Levitan, Juan Martinez, Andrei Klimovich, Alexander Biratko (Sasha), Irina Shishko

## Summary

Val used the recorded wrap-up to lock in the workflow and JIRA-hierarchy decisions the team had just discussed off-record, and to assign parallel work tracks for the rest of the week.

**Capability migration and JIRA hierarchy change.** Val set as Priority #1 the grooming of the current capabilities into a dedicated CAP (capability) JIRA project type. Andrei is responsible for migrating and merging the 24 existing capabilities with the 8 capabilities that have already been built up in the new model. Val also stated they are "contemplating removing the Initiative level" in JIRA and replacing it with a **Product** project type, then wedging the new **Capability** level between Product and Feature. Net hierarchy: Product, then Capability, then Feature, then optional Story, then Subtask. The Initiative level would cease to exist.

**Capabilities already done do not get retroactive paperwork.** Val explicitly said the team will not "go through a circle of fictitious development" for already-completed capabilities; they will simply be marked done. Capabilities do not require acceptance criteria at this stage; only requirements do.

**Parallel catch-up tracks.** Andrei is catching up on the capability, requirement, and use-case side. Alexander (Sasha) is catching up on features and stories. Juan asked whether Alexander could create features without requirements first; Val clarified that requirements and use cases exist primarily to help Alexander when a capability is not self-evident. If Alexander already understands a capability from prior discussion, he can move directly to features. Many capabilities have been discussed already, so the two tracks can run concurrently rather than sequentially.

**Alexander starts feature development tomorrow (May 5).** Val noted Minsk had just ended its workday. When Minsk comes back online, Alexander begins developing features in earnest.

**Goal for the week.** By end of week, the team should have:
- On one side: a full set of capabilities and requirements, with acceptance criteria on the requirements.
- On the other side: capabilities and features, which may or may not be broken down further into stories and subtasks.

**Engineering standards Val stated on record (because this portion was being recorded):**
- Each Feature corresponds to a **GitHub feature branch**.
- A JVL feature branch is expected to last approximately **one calendar week**.
- Multiple pull requests per feature branch.
- Pull request size: approximately **200 to 400 lines of code** (Val's rough guidance).
- Multiple commits per feature branch per working day; Val's rough orientation is approximately 10 commits per feature branch per working day.
- A **Claude Pull Request Reviewer** is wedged into the feature-branch flow and serves as the team's basic reliance for integration testing at the PR level.
- Acceptance criteria live with the PR review process.

**Testing must run in parallel with development; this is non-negotiable.** Val gave Irina a direct charge: build a set of **end-to-end test cases** that test **capabilities** (not features individually), and engage them as Alexander delivers feature branches. Because features land at different times, the E2E test suite has to be catered to incremental delivery. Val stated forcefully: *"I will never accept sequential testing. It's going to be a fight forever. Tests must be done in parallel."*

**Next checkpoint scheduled.** Val originally proposed Friday May 8. Andrei said he would be away Friday, so Val moved the checkpoint to **Thursday May 7 at 8:00 AM**. Val said he does not like far-out meetings. Val committed to booking the meeting and circulating the undertakings and notes himself.

## Decisions Made

- **JIRA hierarchy will be restructured: Initiative removed; Product becomes the new top level; Capability is wedged between Product and Feature.** (Decided/proposed by Val; not contested in the recorded segment.)
- **Capability migration is Priority #1; Andrei owns it.** Merge the 24 existing capabilities with the 8 already in the new model. (Val)
- **Already-completed capabilities are marked done with no retroactive ceremony.** (Val)
- **Capabilities do not require acceptance criteria yet; only requirements do.** (Val)
- **Each feature equals one GitHub feature branch, approximately one calendar week duration, approximately 200 to 400 LOC per PR, approximately 10 commits per day rough average, Claude PR Reviewer attached.** (Val, stated on record.)
- **Testing runs parallel to development. No sequential testing. Irina builds capability-level E2E tests engaged incrementally as Sasha delivers feature branches.** (Val, non-negotiable.)
- **Next checkpoint: Thursday May 7, 8:00 AM Eastern.** (Val, accommodating Andrei's Friday absence.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Groom current capabilities and migrate/merge the 24 existing capabilities with the 8 capabilities in the new CAP project type; produce capabilities and requirements with acceptance criteria on the requirements | End of week (by Thu May 7 checkpoint) | High | Priority #1 per Val; unblocks Alexander's feature development and Irina's E2E test design |
| 2 | Alexander Biratko (Sasha) | Begin developing features tomorrow (May 5) when Minsk reopens; produce capabilities and features with optional stories and subtasks | End of week (by Thu May 7 checkpoint) | High | Parallel track to Andrei; relies on requirements and use cases for capabilities not already understood |
| 3 | Irina Shishko | Develop a set of end-to-end test cases that test capabilities, engaged incrementally as Sasha lands feature branches | End of week (by Thu May 7 checkpoint) | High | Val's hard rule: tests run parallel, never sequential. Tied to PR-level acceptance criteria and the Claude PR Reviewer flow |
| 4 | Val Levitan | Book the May 7 8:00 AM checkpoint meeting and circulate undertakings and notes from this session | Today (May 4) / before May 7 | Normal | Val explicitly took this on |
| 5 | Juan Martinez | (Implicit) Product Owner role on capability and feature definition; no specific task assigned in the recorded segment | TBD | TBD | Juan was active in clarifying questions but no explicit deliverable was assigned to him on tape |

## Engineering Signals

### Confirmed Signals

- **ADR — JIRA hierarchy restructure:** Remove Initiative level; introduce Product as new top level; wedge a new Capability level between Product and Feature. New stack: Product, Capability, Feature, optional Story, Subtask. Raised and decided by Val.
- **ADR — Capability project type (CAP) in JIRA:** Capabilities live in a dedicated CAP project type, distinct from Feature/Story workflow. Andrei executing.
- **ADR — Feature branch model:** Each Feature equals one GitHub feature branch, approximately one calendar week duration, multiple commits per day (approximately 10 rough), PRs sized at approximately 200 to 400 LOC, Claude PR Reviewer wedged into the flow as the integration-testing first line.
- **ADR — Parallel testing mandate:** End-to-end tests run parallel to feature development, never sequentially. E2E tests are written at the Capability level (not per-feature) and engaged incrementally as feature branches land.
- **CAP — Capabilities do not require acceptance criteria; requirements do.** Establishes the formal contract between layers in the new hierarchy.

### Suspected Signals

- **Possible ADR — Claude PR Reviewer as integration testing substitute:** Val said the Claude PR Reviewer is "your basic reliance on the integration testing." This is a meaningful architectural call about where integration testing happens (PR level vs. dedicated CI stage) and what tool owns it. Worth a formal ADR on the testing pyramid.
- **Possible REQ — "Tests must run in parallel with development" as a process requirement:** Val stated this as a hard rule. Worth capturing as a non-functional/process requirement on the Flex_Recycler product so it does not get re-litigated.
- **Possible CAP — End-to-end testing capability tied to capability-level coverage:** Irina's E2E suite is described as testing capabilities, not features. That is a coverage-model decision worth tracking.

## Open Questions

- **Juan's role/deliverable for the week.** Juan asked clarifying questions (notably whether Alexander needs requirements before creating features) but no explicit deliverable was assigned to him in the recorded segment. May have been covered before transcription started.
- **The Initiative-removal decision** is described as "contemplating" by Val; this is a decision direction but not stamped "Locked." Worth confirming at the May 7 checkpoint.
- **"Pavel"** Juan greeted "Hi, Pavel" mid-meeting, suggesting another attendee joined briefly. Not in the speaker labels for this segment. Not in JVL team table.
- **The first ~50+ minutes of the working session were not transcribed.** The substantive grooming discussion happened off-tape; only the wrap-up was captured. Worth flagging if anyone wants the underlying rationale beyond what Val recapped on record.

---
*Processed from Teams transcript on May 5, 2026*
*Source meeting: Flex_Recycler Requirements Working Session, May 4, 2026, 1:01 PM*
