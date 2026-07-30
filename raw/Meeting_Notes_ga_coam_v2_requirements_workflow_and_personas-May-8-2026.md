# Meeting Summary — V2 V43 GA-COAM v2 / 3-JP-Progressive: Requirements Workflow, Personas, and Feature-to-Capability Mapping
**Date:** May 8, 2026, 3:00 PM Eastern
**Duration:** 32m 48s
**Attendees:** Val Levitan, Juan Martinez, Efim Podvoiski, Igor Metelski, Irina Shishko

> **Sequence note:** This is the reconvened afternoon session following the May 8 morning meeting that decomposed Capability 9 into three capabilities (see `GA-COAM v2 Capability Decomposition-May-8-2026/`). Val's recess plan from that meeting was: he and Juan would pair on capabilities + requirements during the break, then bring the team back to walk requirements. This session is the result.

## Transcript Quality Note

Same bilingual code-switching dynamic as the morning session — frequent Russian-language stretches that the Teams engine garbled phonetically into English. The English-clear portions carry the structural decisions cleanly. Russian content has been translated where decipherable; ambiguous fragments are flagged inline.

## Summary

This session formalised the JIRA / capability / requirement / feature workflow for the GA-COAM v2 work, locked in a third persona (JVL Product Manager), and pinned the immediate sequence of work for Juan, Igor, and the controller / data-centre side. The structural rules established here are intended to be applied across JVL going forward, not just to this initiative.

**Where things stand at the top of the session.** Val opened by noting that capabilities have been broken out from the original Capability 9 split. Requirements should be viewed through **two personas** as initially scoped: an **operator (master operator)** and a **player**. Val had Claude draft 6 requirements and sent them around. Juan independently drafted his own set; he'll reconcile after reviewing Val's document, focus on the same two personas, and incorporate the important additional items.

**Rule: acceptance criteria belong in requirements, not in capabilities.** Val placed all acceptance criteria into the requirements rather than the capability records. His reasoning: capabilities don't have acceptance criteria by nature (capabilities are one-shot frames); acceptance criteria attach to specific, testable requirement statements. Juan: this aligns with how the team has historically treated acceptance criteria. Locked.

**Val's full briefing to Igor on the JIRA → GitHub feature workflow.** This is the single longest structural moment in the session — Val walked Igor through the end-to-end pattern:

- **Features are linked to capabilities, not to requirements.** A capability is closed/complete when all of its features have been pulled into `main`. Requirements remain in the system as durable, reusable items — they do not close out with the feature.
- **Each feature = one feature branch in GitHub.** A JIRA feature carries a direct link to the GitHub feature branch.
- **Feature size: approximately 5 workdays each.** Sized so a single feature is a tractable Claude-Code unit.
- **Features should be fully developed by Claude Code.** Repository standards have been circulated and discussed exhaustively. If something doesn't work in the standards, raise it — but the expectation is that features are Claude-implementable end-to-end.
- **Stories are optional under features.** Not required; include only if the developer judges them useful.
- **Maximum 2–3 concurrent feature branches per developer.** Val: "you can work on multiple branches at the same time, but not too many — multiple, I'm considering two, maximum three."
- **Each repository has a Claude Code reviewer "sitting on top of it."** Pull requests are reviewed by the Claude code reviewer and committed by the developer. After review, feature branches are pulled into `main`.

**Juan's clarifying question + Val's restatement.** Juan asked: "you said features attach to the capability, not the requirement?" Val confirmed and tightened the language: *"features are attached to capabilities, and a capability is done when the set of features is pulled into main. Capability gets done, closed, done. Requirements are reusable and remain in the system."* This is the canonical phrasing.

**Igor's confusion about the match-3 bonus game flow.** Igor flagged that he understands the game-board state but doesn't understand the game flow from the current requirements (in Russian). Efim said the right move is to link **Michael's game-flow design** (which Michael had been working on, sent to the group as a separate document) to the requirements. Val concurred — the game-flow concept exists already; it just needs to be attached to the requirement record so Igor can pull it into the feature design. Igor: "yes, that's right."

**Feature description quality — the Claude Code feedability test.** Igor pressed Val on what level of detail features need to carry: should the description contain technical implementation details, like specific class names? Val's answer (paraphrasing the garbled stretch): **a feature description must be specific enough to be fed to Claude Code as the implementation source of truth.** Product-manager view drives the *what*; the feature description itself has to be technical enough that Claude Code can pick it up and implement from it. Igor: understood.

**Third persona introduced: JVL Product Manager.** Initiated by Juan reflecting that the existing two-persona scope (operator + player) doesn't cover the case where the *product manager inside JVL* makes decisions about how the product should behave in the market that are neither operator-driven nor player-driven. Val formalised the persona name explicitly and corrected Efim on the terminology:

> "The third persona is **JVL's Product Manager**. That's an individual within JVL who tells everyone how he or she sees this particular product to be functioning in the market. That name is Product Manager. Not Operations Manager, not QA Director, not head of chief, not chief of heads — **Product Manager: manages product.**"

Juan accepted: he is informally already that role, gathering customer / operator data + comments to inform decisions — but final product-shape decisions live with him as Product Manager.

**First Product-Manager requirement: progressive settings cannot be changed on the fly.** Efim raised the technical question — "do we allow progressive settings to change on the fly?" Juan: "Correct, we do not." Val: that requirement still lives in requirements, but it now traces back to the **Product Manager** persona — *"Product Manager is telling us, do not let this be changed on a flight."* Juan: "I'll add that."

**Attract-mode display fix.** Efim raised that one of Juan's requirements appeared to state that **all three progressives should be shown on the display zone simultaneously** — which Efim believed wasn't feasible. Discussion clarified that the requirement was intended for **attract mode only**, not during active play. During play, only the progressive corresponding to the game being played should display. Juan accepted this was an under-specified statement on his part and committed to updating the requirement. Val noted his own Claude-drafted requirements actually break this down correctly — Efim admitted he had only glanced at Val's document and missed it. Juan's broader reflection: *"this is the balance where I'm not necessarily trying to tell engineering what to do. Why would you display all three progressives at the same time? That's utter player confusion."* Val: this kind of design intent must still be **explicitly written**, not implied — a design feature is not an engineering solution. Juan: agreed, will update.

**Juan's hold on Igor's feature drafting.** Juan asked Igor explicitly: *"don't start features right now."* Juan needs time to:
- Meet with Michael, design the match-3 game flow.
- Write/update the relevant requirements.
- Reconcile against Val's Claude-drafted requirements.

Juan committed to completing all of this **today (May 8)**. Igor agreed.

**Action chain for Igor.** Val laid out the sequence post-Juan's completion:
1. Once Juan has finished capabilities + requirements + personas (effective tomorrow / weekend, with Pavel back in office Monday May 11), Igor begins drafting features in Claude.
2. **Where a feature is confusing or unclear, Igor must call a meeting WITH JUAN as the business representative.** Val was explicit: *"You cannot call a meeting with Efim and ask him to clarify. You have to, you must clarify it with Juan. Must."*
3. After features are clarified and drafted, Igor's next undertaking is to **create a schedule** — so Val can review timeline productively.

**Controller + data-centre side coordination.** Igor (in Russian) raised that multi-progressive support also needs work on the **controller** and **data-centre** side. Val agreed: that work is owned on the data-centre side (Dima or similar — needs alignment with Pavel when he's back Monday). Igor: I'll add detailed descriptions to my features (technical level) so they can be fed to Claude Code. Val: business acceptance criteria live in *requirements*; technical acceptance criteria live in *features*. Igor: understood.

**Schedule-review meeting placement.** Val proposed Thursday review; Juan flagged he has a doctor appointment for pump removal at 10 AM Thursday. Val moved review to **Friday May 15** (schedule review meeting), then walked back: Wednesday is too early for Igor to have a schedule ready, but Friday May 15 is too far out. Final landing: **Thursday May 14, 9:30 AM Eastern**, without Juan as the required attendee — Juan added as optional, can dial in until his appointment.

**Val's closing message on design stages.** Val emphasised, specifically to Efim, that **the design stages will have written capabilities and requirements just like the development stages**. There is no special exemption. Val noted this seems like a mammoth undertaking but it is not — the actual design specs (screen layout, color, palette, line widths, etc.) **already exist**, written down. They have been discussed with **Dima Handoff and Lena**. The work is converting those existing specs from their current format into the capabilities + requirements format the team is now using.

## Decisions Made

- **Acceptance criteria live in requirements, not in capabilities.** (Val, Juan accepted.)
- **Features link to capabilities, not requirements.** (Val.)
- **A capability is done/closed when its set of features is pulled into `main`. Requirements are durable and reusable.** (Val.)
- **One JIRA feature = one GitHub feature branch.** (Val.)
- **Feature length target: ~5 workdays.** (Val.)
- **Max 2–3 concurrent feature branches per developer.** (Val.)
- **Stories under features are optional, not required.** (Val.)
- **Each repository has a Claude Code reviewer.** PRs reviewed via code reviewer, committed by developer, then merged to `main`. (Val.)
- **Feature description quality bar: detailed enough to be fed directly to Claude Code as the implementation source of truth.** (Val, Igor accepted.)
- **Technical acceptance criteria live in features; business acceptance criteria live in requirements.** (Val.)
- **Third persona: JVL Product Manager** (in addition to operator/master and player). Specifically: an individual inside JVL who articulates how the product should function in the market. Not operations manager, not QA director, not chief. (Val.)
- **First Product-Manager requirement: progressive settings cannot be changed on the fly.** (Juan + Efim, accepted by Val.)
- **Attract-mode display behaviour clarification:** all three progressives shown only in attract mode; during play, only the progressive for the game being played. (Juan, accepted.)
- **Igor does not start drafting features until Juan completes the capabilities + requirements + personas update.** (Juan, accepted by Igor.)
- **Igor must clarify ambiguous features with Juan (business representative), not with Efim.** (Val.)
- **Schedule-review meeting: Thursday May 14, 9:30 AM Eastern.** Juan optional. (Val.)
- **Design stages produce written capabilities and requirements just like development stages.** Specs already exist (screen, color, palette, line width) — they need to be converted from current format. (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Meet with Michael to design the match-3 game flow | Today (May 8, 2026) | High | Igor cannot start features until this is documented |
| 2 | Juan Martinez | Write/update the relevant requirements (including the corrected attract-mode-only display behaviour) | Today (May 8, 2026) | High | Same dependency |
| 3 | Juan Martinez | Reconcile his requirements against Val's Claude-drafted set of 6 | Today (May 8, 2026) | High | Avoid duplicate or contradictory requirements |
| 4 | Juan Martinez | Add the Product-Manager-persona requirement: "progressive settings cannot be changed on the fly" | Today (May 8, 2026) | High | Captures Efim's technical-constraint flag through the new PM persona lens |
| 5 | Efim Podvoiski | Link Michael's game-flow design document to the relevant requirement record | Soon | High | Required input for Igor's feature work |
| 6 | Igor Metelski | Wait for Juan to finish requirements / capabilities / personas before starting feature drafts | Through end of weekend | High | Avoid wasted Claude-Code feature work that would need to be redone after Juan's edits |
| 7 | Igor Metelski | Once unblocked, draft features in Claude with technical-level detail sufficient for Claude Code to implement from | Starting Monday May 11 | High | Use the new three-capability structure as the linking target |
| 8 | Igor Metelski | When a feature is unclear, call a meeting with Juan (business representative) — NOT with Efim — to clarify | As needed | High | Val was explicit on this routing |
| 9 | Igor Metelski | Add technical acceptance criteria to each feature; reflect business acceptance criteria back to requirements where missing | Concurrent with feature drafting | Normal | Reinforces the criteria-placement rule |
| 10 | Igor Metelski | After features are drafted, produce a schedule for Val to review | Before Thursday May 14, 9:30 AM Eastern review meeting | High | Anchors the schedule-review meeting; precondition for Val to assess timeline |
| 11 | Dima Kovalchuk (or controller / data-centre owner) | Coordinate with Pavel when he is back Monday May 11 on multi-progressive support for the controller and data centre | Week of May 11 | High | Parallel workstream to Igor's framework features; Pavel's return in office unblocks it |
| 12 | Val Levitan | Book Thursday May 14, 9:30 AM Eastern schedule-review meeting; Juan as optional attendee | This week | High | Cadence anchor; Juan flagged 10 AM doctor appointment |
| 13 | Team (design side) | Convert existing screen/layout/palette/line-width specs (already discussed with Dima Handoff and Lena) into capability + requirement format | Ongoing | Normal | Val's closing message to Efim: design stages are not exempt from the capability/requirement discipline |

## Engineering Signals

### Confirmed Signals

- **ADR — Acceptance criteria belong in requirements, not in capabilities.** Logical rationale: capabilities are one-shot frames; testable criteria attach to durable, singular requirement statements. (Val + Juan.)
- **ADR — Features link to capabilities, not to requirements.** A capability closes when all its features merge into `main`; requirements remain durable in the system. (Val.)
- **CAP — JIRA-to-GitHub workflow.** One JIRA feature = one GitHub feature branch; feature size target ~5 workdays; max 2–3 concurrent branches per developer; Claude Code reviewer per repo; PR-reviewed-then-merged. This is the canonical pattern for JVL feature delivery going forward.
- **CAP — Claude-Code-feedable feature description quality.** Features must be specified at a level of detail sufficient to hand directly to Claude Code as the implementation contract. Not abstract product description.
- **ADR — Technical vs business acceptance-criteria placement.** Business acceptance criteria go in requirements; technical acceptance criteria go in features. (Val.)
- **CAP — Third persona: JVL Product Manager.** Distinct from operator/master and player. Captures internal-to-JVL design intent for how the product behaves in the market. Goes alongside the existing personas in all future requirements work.
- **REQ — Progressive settings cannot be changed on the fly.** Sourced from the Product Manager persona. First explicit requirement tied to the new persona.
- **REQ — Attract-mode-only multi-progressive display.** During active play, display only the progressive of the game being played. All three progressives surface only in attract mode.
- **Engineering Solution — Routing escalation rule.** When a developer hits ambiguity in a feature, the resolution path is "meeting with Juan as business representative" — not "ask Efim." Reinforces the product-manager-as-source-of-truth pattern.
- **ADR — Design stages produce capabilities + requirements just like development stages.** No exemption. Existing screen-layout / palette / dimensional specs convert into the capability + requirement format.

### Suspected Signals

- **Possible CAP — Claude Code reviewer-per-repo as a JVL-wide engineering standard.** Mentioned here as a given, but worth tracking as a CAP if not already formalised — the existence of the reviewer is load-bearing for the entire "Claude Code implements features" workflow. — *Val, is this already documented as a standard capability, or just verbal?*
- **Possible REQ — Feature schedule artifact as a structural output of feature drafting.** Val expects every developer's feature set to land with an accompanying schedule. Worth tracking as a process requirement (not just an ad-hoc Igor ask).

## Open Questions

- **Where is Michael's game-flow design document currently stored**, and what's the link mechanism into the requirement records (Confluence link? JIRA attachment? Obsidian path?). Efim is to link it; the mechanism isn't pinned.
- **What is Pavel's specific Monday May 11 hand-off on the multi-progressive controller + data-centre side?** Igor mentioned coordination but didn't define deliverables.
- **Whose name owns the data-centre features?** Val mentioned Dima/Sergey/Kharetski generally; for *this* GA-COAM v2 work specifically, the owner needs to be named.
- **How is "the existing screen / layout / palette / line-width spec" stored today?** Val said "we know where it is, there are documents that already exist" — but didn't name the location. Required to actually do the convert-to-capability work.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Alignment_3-JP_CAP-REQ_Review (20260508_110042)*
