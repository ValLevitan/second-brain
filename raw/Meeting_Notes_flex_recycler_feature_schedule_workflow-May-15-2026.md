# Meeting Summary — Flex-Recycler Requirements Working Session: Feature Scheduling Workflow
**Date:** May 15, 2026, 12:01 PM Eastern
**Duration:** 49m 55s
**Attendees:** Val Levitan, Andrei Klimovich, Juan Martinez, Alexander (Sasha) Biratko, Irina Shishko

> **Sequence note:** This is the May 15 Friday session anchored in the May 5 Klimovich call (see `Flex-POS Recycler Web Interface Planning-May-5-2026/`). The agenda continues the GA-COAM v2 / Flex-Recycler workflow established in the May 8 sessions.

## Summary

Mixed-language working session covering the **Flex-Recycler requirements maturity check**, a **process-level dispute on requirement language quality** (Sasha challenged Andrei's heavy-text-with-cross-links style), and the **definition of the next milestone: feature-level schedule for the Flex-Recycler initiative** to be reviewed at a follow-up meeting on **May 20**.

**Pre-meeting clearing — Gamoa update deferred.** Juan offered an update from the previous night's Gamoa meeting (gift cards usable in ATMs as a path toward real cash-out, currently on hold pending mid-term elections). Val deferred this to a separate call.

**Andrei Klimovich's progress on Flex-Recycler capabilities → requirements.** Andrei reported:
- Player-facing capabilities are being prioritised first; the entire player flow is being covered.
- Only **3 minor capabilities remain**, all related to edge cases. The rest have been described with full requirements and use cases.
- One major requirement under review needs the team's feedback: the **PIN generation flow** for FlexPay cash-out.

**PIN generation: auto-generated vs player-input.** Andrei had designed the flow to **auto-generate** the PIN and display it to the player, optimising for minimal friction. Juan challenged immediately: the player must remember the PIN to come back later and cash out at FlexPay. *"I remember my birthday, I remember my wife's birthday — that's usually the pins I use. If you've given me a pin and I had two beers, I might forget that pin, then what?"* Andrei accepted the pushback: **player will be asked to input a PIN and confirm.** Standard pattern; no auto-generation.

**Val's structural focus when he joined: the capability-to-features-to-repo chain.** Val (after a Teams reconnection) refocused the conversation:

> *"I want to make sure that based on the capabilities already generated, Sasha can generate features. And that these features can be traced — set of features → capability → set of requirements → use cases. Laser precision. Give me one capability, multiple features, one repo, Claude Code programming. That's the chain I want to see."*

Sasha began an answer in Russian (heavily garbled by the transcription) — the substance was that he can generate features from Andrei's capabilities, but is encountering quality issues in how the requirements are written. Val turned this into a structural point:

**Andrei's domain knowledge gap.** Val: *"Andrei may create capabilities knowing the subject well, or imagining the subject well. There is a difference between knowing and imagining."* Val wants all of Andrei's capabilities **run by Juan** (who knows the subject) before they're treated as final. Juan supported with a clarifying point: **at the capability level (the simplest level — "the Flex-Recycler must accept money," "must have a bill acceptor"), it is very hard to be wrong**. Drift starts at the **requirements** level. Andrei agreed. Val: "exactly — that's why we use requirements + use cases to narrow capabilities into an exact interpretation."

**Capability close-out rules (reinforced — same as May 8).** Val restated and the team affirmed:
- **Acceptance criteria live on requirements and features, NOT on capabilities.**
- A capability closes when (a) the full set of features for that capability has been merged, **AND** (b) Andrei tests and confirms the capability, **AND** (c) Irina runs end-to-end testing with no failure.
- **Requirements do not go away** — they remain reusable and testable.
- Val will **push for end-to-end testing in automated regime** — not necessarily from day one, but the direction is firmly automated E2E.

**Andrei + Juan capability-grooming session: Monday May 18.** Juan said he's available all next week except Tuesday [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]. Andrei: *"let's do that on Monday — I'll be back in fields today, and then Monday."* Andrei is also partially required for Texas Expo prep next week but the role is minor, so capacity is there. Juan can pre-read the capabilities already shared in the common chat to surface comments before the live Monday session.

**MVP / Release-version prioritisation — when does it happen?** Andrei asked when product-side MVP / version-one / version-two prioritisation gets pinned. Val: **at the point of scheduling.** Process:

1. Sasha lays out all of the features with acceptance criteria.
2. Irina writes test cases for the features and groups them into test suites.
3. Pavel evaluates resource constraints (Sasha's attention is needed elsewhere, etc.).
4. Val sets the overall priority — Val is the sole authority for setting overall priority across initiatives.
5. Internal negotiation → schedule emerges.
6. When the schedule is presented, Andrei can scrub: *"I need it by such-and-such date, then capabilities 1, 5, 7 are MVP; everything else moves out."*

Val emphasised this is **symbiotic** — Andrei wants his project to succeed; other projects want to succeed; the company is not made of idiots — Andrei's MVP definition will stimulate reprioritisation across initiatives, not just down-scope his own.

**Should Andrei review the features Sasha writes?** Andrei asked. Val: *"I don't believe it's a practical thing for you to do. I'm open to exposing you to it, but from experience it's not practical."* Andrei accepted. Path forward: open communication line between Andrei and Sasha — if Sasha is unsure about a requirement's intent, he asks Andrei twice before making it a feature. *"My job is to introduce people, make a comfortable work environment, and have people communicating directly."*

**Val's MCP-MR success story as a model.** Val shared (referring back to his May 11 BC Material Requirements MCP work — see `BC Material Requirements MCP-May-11-2026/`) that he had just gone through a very productive Claude experience: a tight user profile (procurement manager) + careful attention to every verb and adjective in requirements → smooth Claude-driven feature delivery. The takeaway: requirements + capabilities quality directly drives feature delivery quality. Val told Andrei: *"I think you're making Alex's job very, very easy."* Sasha confirmed when asked: *"if requirements good, feature is good."*

**Sasha's process critique of Andrei's requirements style.** Sasha raised (in Russian) two specific concerns about Andrei's requirements text:

1. **Language is too academic / complex.** Sasha said he tells Claude to *"write in more accessible language, without specialised terms, without long links — and then it writes much better."* Andrei's hand-written requirements are dense enough that *"you have to spend a long time figuring it out — either dig through it or run it back through Claude."*
2. **Over-use of cross-links.** Claude (when used to draft Andrei's requirements) creates lots of cross-references to other requirement records. To understand a requirement you have to click through several links, when **two or three words of inline description would suffice**.

**Val's response: simple language is a 1,000% rule for JVL.** Val embraced Sasha's critique aggressively. *"Communicate to me like I'm an idiot. I want it to be a rule through the company. Just say it simply. I don't need PowerPoint presentations. I don't need fancy wording. Just get to the point within first three sentences."* Andrei tried to argue it's a balance; Val: *"there is nothing to balance. Trust me on this. Add a prompt to your Claude flow that all communication must be in very simple wording."* Andrei accepted: he'll rerun a couple of completed requirements through this filter and see how the results change.

**Andrei's defence of cross-links: single source of truth.** Andrei explained his reasoning: cross-links prevent drift — if a referenced requirement changes, you only need to update it in one place. Inline-text-with-links means you'd have to update both spots, and that creates noise. *"You won't have a point of truth."*

**Compromise reached — inline name display via Jira auto-linking.** Sasha agreed cross-links are fine **as a fallback** ("if the inline description isn't enough"), but argued that for most cases the *requirement name in 2-3 words* is sufficient — no click-through needed. Irina suggested a better solution: Jira can auto-populate the referenced requirement name when you insert a link — so the name shows inline AND stays in sync if it changes. Andrei: *"agreed, excellent — let's do that."* The combined pattern (auto-displayed name + clickable link to source) satisfies both single-source-of-truth and readability concerns.

**Jira labels vs components — Val's policy.** Juan mentioned filtering capabilities by the `flex_recycler` label. Val pushed back: *"labels is not a good thing in Jira. I'm trying to avoid using labels as much as possible. The better way is probably use of component."* Val will check with IT to make **`recycler` a component in Jira**, not a label. Juan also showed that he has been using **"transactional"** as a sector/category filter under gaming sector — Val asked whether that's tagged as a label or a component (current state was unclear in the screen-share). The action is to migrate sector/product categorisation off labels and onto components.

**Val's milestone definition — the feature schedule.** In the long English-Russian closing section (heavily code-switched), Val articulated the next milestone in detail. The structure he wants in Jira:

- **Open the Flex-Recycler initiative IP-1259** (per Val's reference).
- **Schedule the features** that are known.
- **Irina + Sasha jointly:** Irina at the **story** level (1–2 days each), Sasha at the **task** or **stories-under-feature** level — feature length **2–5 days each, maximum 10–20 hours of work**.
- **Feature branches:** clustered commits per day; **Saturday merges**.
- **If Sasha splits a feature into stories, the story length is 1–2 days max — anything longer should be a feature.**
- **Once features have assigned dates, they move from "Backlog" → "To Do" status in Jira.** "To Do" specifically means **scheduled + stock-ranked.** This terminology is now a JVL convention.
- **Feature schedule will visually appear as a calendar bar** (Val described a "barbed wire image") that stretches as stories are extended.

**Andrei's parallel-vs-sequential question.** Andrei said: I'll finish requirements next week, then Sasha can convert to features after that. Val: **No — done in parallel, not in tandem.** Sasha + Pavel + Irina start scheduling the **already-known** features now (don't wait for Andrei's remaining requirements to finish).

**Next checkpoint: Wednesday May 20, 8 AM Eastern.** Val will circulate the invite. Agenda: review the **schedule of the features that are known**. Andrei continues his capabilities + requirements work in parallel. Meeting closed; Andrei had to leave for another appointment at 10. Val, Andrei, and Juan then planned to meet with Felipe in a follow-on session.

## Decisions Made

- **PIN generation: player-input + confirm.** Auto-generated PIN abandoned. (Juan's feedback, accepted by Andrei.)
- **All Andrei's capabilities must be jointly groomed with Juan before they're treated as final.** Domain-knowledge reconciliation. (Val.)
- **Capability close-out criteria (re-confirmed):** all features merged AND Andrei tests positively AND Irina runs E2E automated test with no failure. (All.)
- **Direction: end-to-end testing in automated regime** — not from day one, but Val will push for it. (Val.)
- **MVP / release-version prioritisation happens at the scheduling step**, not during capabilities authoring. Val sets the overall priority; team negotiates resources; Andrei scrubs which capabilities make MVP for which date. (Val.)
- **Andrei does not review Sasha's features.** Communication channel between Andrei and Sasha kept open; Sasha asks Andrei twice when unsure. (Val.)
- **Simple language as a JVL-wide communication rule.** Andrei's requirement-writing process adds a Claude prompt enforcing simple, three-sentence-or-less framing without fancy wording. (Val, with Sasha's strong endorsement.)
- **Jira cross-link practice: inline name display + clickable source link.** Both single-source-of-truth and readability preserved. (Irina's compromise, accepted by Andrei + Sasha.)
- **Jira components, not labels, for categorisation.** "Recycler" becomes a component (Val to coordinate with IT). Sector/product categories (e.g., "transactional") to be migrated off labels onto components. (Val.)
- **Feature size: 2–5 days, max 10–20 hours. Story size: 1–2 days max.** Stories optional under features. (Val.)
- **Feature branches: clustered commits per day, Saturday merges into main.** (Val.)
- **"To Do" status in Jira ⇒ scheduled + stock-ranked.** "Backlog" → "To Do" transition is the scheduling moment. (Val.)
- **Capabilities + requirements work and feature scheduling run in parallel, not in tandem.** (Val.)
- **Next checkpoint: Wednesday May 20, 8 AM Eastern — feature-schedule review meeting.** (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Redesign PIN generation flow as player-input + confirm | This week | High | Replaces auto-generated PIN |
| 2 | Andrei Klimovich | Complete remaining 3 edge-case capabilities + finalize requirements + use cases | Through next week | High | Player-facing capabilities are the priority |
| 3 | Andrei Klimovich | Run completed requirements through a "simple language" Claude pass to reduce density and academic phrasing | This week | High | Per Sasha's critique + Val's enforcement |
| 4 | Andrei Klimovich | Adopt inline-name + clickable-link pattern for Jira cross-references | Going forward | High | Replaces link-only references |
| 5 | Andrei Klimovich + Juan Martinez | Joint capability grooming session Monday May 18 | Monday May 18, 2026 | High | Tuesday is out for Juan [Personal passage removed — owner ruling 2026-09-28: the JVL brain holds JVL matters only. Original kept in the source vault.]; Monday is the slot |
| 6 | Juan Martinez | Pre-read capabilities shared in common chat; raise comments to Andrei before the Monday session | Before Monday May 18 | Normal | Andrei pointed at the cross-links + question sections |
| 7 | Juan Martinez | Pay attention to the "Open Questions" sections in Andrei's requirements — these are sources for new requirements / changes | Ongoing | High | Andrei specifically flagged these as important |
| 8 | Alexander Biratko + Pavel + Irina | Begin scheduling the known features for the Flex-Recycler in parallel with Andrei's ongoing work | Starting now | High | Don't wait for Andrei's full set |
| 9 | Alexander Biratko | Convert known capabilities into features (2–5 days each, max 10–20 hours) | Ongoing | High | Per Val's sizing rules |
| 10 | Irina Shishko | Author test cases at the story level (1–2 days each) for the features Sasha drafts | In parallel with Sasha's feature work | High | Test cases group into test suites that align with Sasha's development priority |
| 11 | Val Levitan | Coordinate with IT to make `recycler` a Jira component (not a label) | This week | Normal | Part of broader migration off labels |
| 12 | Val Levitan | Circulate Wednesday May 20, 8 AM Eastern invite for feature-schedule review | This week | High | Next milestone gate |
| 13 | Andrei Klimovich | Maintain "send Alex updates when each capability set is ready" cadence | Ongoing | Normal | Juan endorsed; already in flight |

## Engineering Signals

### Confirmed Signals

- **ADR — Capability close-out requires three conditions:** (1) all features merged, (2) Andrei confirms via tests, (3) Irina passes E2E (eventually automated). All three together close the capability.
- **ADR — Acceptance criteria live on requirements and features, not on capabilities.** (Re-confirmed from May 8.)
- **ADR — Capability is one-shot/closes; requirement is durable/reusable.** (Re-confirmed.)
- **ADR — Simple language requirement across all JVL communication.** Enforced by prompt in requirement-drafting Claude flows. *"Like I'm an idiot. Three sentences max. No fancy wording. No PowerPoint."*
- **ADR — Jira cross-references use inline name + clickable link, not link-only.** Resolves single-source-of-truth and readability simultaneously.
- **ADR — Jira components, not labels, for categorisation.** Recycler becomes a component; transactional/sector classifications migrate to components.
- **ADR — Feature size: 2–5 days, max 10–20 hours. Story size: 1–2 days max.** Stories optional under features.
- **ADR — Feature branches: per-day commits clustered; Saturday merges into main.**
- **ADR — Jira "Backlog" → "To Do" transition = scheduling moment.** "To Do" ⇒ scheduled + stock-ranked. Codified JVL terminology.
- **ADR — Capabilities-requirements authoring and feature scheduling run in PARALLEL, not in tandem.** Sasha starts scheduling known features while Andrei finishes the remaining capabilities.
- **CAP — Player-input PIN at FlexPay cash-out** (replacing auto-generated). Player friction trade-off accepted; recall reliability prioritised.
- **CAP — MVP definition via capability scrubbing at scheduling time.** Val sets overall priority; team negotiates; Andrei scrubs which capabilities make MVP.
- **Engineering Solution — User-profile-first requirement authoring.** Val cited his BC MCP / MR success story: tight user profile + verb/adjective discipline → smooth Claude feature delivery. Pattern recommended company-wide.

### Suspected Signals

- **Possible CAP — End-to-end automated testing for Flex-Recycler.** Val flagged this as a direction; Irina committed. Worth tracking as a tracked capability with its own owners and milestones. — *Val, does this warrant its own capability record on the Flex-Recycler initiative?*
- **Possible ADR — Andrei's "Open Questions" section as a structured deliverable in every requirement document.** Juan was specifically directed to consult these. Worth formalising as a JVL requirement-document standard section.

## Open Questions

- **Final Jira component model.** Val pending IT coordination to convert `recycler` and other categorisations from labels to components. Until done, Juan continues filtering by current mixed-state tags.
- **Exact list of features to schedule first.** Sasha to derive from the capabilities Andrei has already marked complete.
- **E2E automation tooling and adoption window.** Irina to write the first test suites; automation timeline unclear.
- **How does the parallel feature-scheduling track integrate with Andrei's still-evolving capabilities?** Risk: if Andrei rewrites capabilities for simpler language after Sasha has already drafted features against the older text, features may need touch-ups. Mitigation not explicitly planned.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Flex_Recycler Requirements Working Session (20260515_080123)*
