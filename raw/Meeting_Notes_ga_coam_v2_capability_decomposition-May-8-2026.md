# Meeting Summary — V2 V43 GA-COAM v2 / 3-JP-Progressive: Capability Decomposition Review
**Date:** May 8, 2026, 1:11 PM Eastern
**Duration:** 44m 14s
**Attendees:** Val Levitan, Juan Martinez, Efim Podvoiski, Igor Metelski, Irina Shishko

## Transcript Quality Note

This meeting was conducted bilingually — Igor Metelski opened in English and explicitly asked permission to switch to Russian when needed; subsequent sections code-switched heavily, and Microsoft Teams' transcription engine garbled both languages in the middle stretches. The substance below is recovered from the English-clear sections plus translated Russian fragments. The structural decision-making (the three-way capability split, the requirements-vs-features distinction) lands clearly in the transcript even where individual exchanges are muddled.

## Summary

This was the second of Val's alignment meetings on the V2 V43 GA-COAM v2 / 3-JP-Progressive initiative, with the explicit purpose of pairing **capabilities** (market-facing description of what the product can do) with **features** (developer-facing implementation units). The meeting's most consequential outcome is structural: what was originally one bloated **Capability 9** is decomposed into **three distinct capabilities**, exposing a foundational capability that was implicit and therefore invisible.

**The starting state — Capability 9 as Juan wrote it.** Juan opened by sharing Capability 9: *"Deliver a new jackpot experience designed to replace the existing Georgia peach progressive bonus. It must support 3 levels of progressive, support the existing match-3 symbol concept (which we've done before), and be compatible with all legacy line-and-ways games within a multi-game software set."* Juan flagged the cabinet would support **three different progressive types**: Jackpot Rush, Fiery Ice Link, and the new match-three. The match-three would only apply to the legacy peach-style games.

**Igor's feature breakdown.** Igor walked through the features he had drafted against this requirement, attempting English. He listed five features tied to the multi-product + match-the-bonus requirement set:

1. **Multi-product packaged games** — combine games from different game products (Jackpot Rush, Fiery Ice Link, GCAM games) into one product, with each game using its own resources (progressive dialogues, messages, etc.). Different products with different common resources, mixed in a single deployment.
2. **Multi-progressive support** — one cabinet supports multiple progressive types concurrently.
3. **Progressive controller** — the orchestration component (referenced but not fully detailed in the English-clear sections).
4–5. Additional features (covered in the Russian-language portions but not cleanly captured by the transcription).

Igor noted these features connect to both the multi-product requirement *and* the match-the-bonus requirement.

**Val's structural challenge — what *is* the capability?** Val pressed: *"I'm struggling to visualize what capability is there. Is the capability to display a three-level progressive? Is it to mathematically calculate three-level progressive? Is it to increment meters?"* The question wasn't rhetorical — Val was probing whether Juan's single Capability 9 was actually one capability or several conflated.

Juan pushed back: *"By definition, progressive implies an increment rate. Why would I tell engineers something they don't know? Capability is growing into a requirement itself. The heavier it gets, why do I need a capability when I can detail all this in individual requirements?"*

**Val's articulated principle (used as the alignment rule for the rest of the meeting):**
> **Capability is something that gets executed once. Requirements live there for a long time and could be reusable. A requirement is singular; capability is all-encapsulating.**

This framing carried the discussion. Once the team accepted that capabilities are one-shot organisational units (the conceptual frame for a release), Juan's question became *which* one-shot frames are actually present in this work?

**The implicit foundational capability — Efim's intervention.** Val's reframing of "what are we actually trying to deliver" led Juan to articulate: *"three unique progressive systems within the one game — three unrelated progressives within the same package of games released for the Georgia market."* Val wanted to refine the word: *"non-symbiotic progressives — like, what's the word — three unrelated progressives, in one machine, or in the same display."* Juan agreed.

At this point Efim made the critical intervention: *"First of all, we are trying to combine games from three different products in one product. This is something that is important for developers. Then we have this one capability." It seems so obvious to Juan that he didn't even think it was worth mentioning, but it is the first capability."*

Juan accepted immediately: *"Right, so what you just described is completely unrelated to match-three. That should be a standalone capability."*

**The three capabilities — final decomposition.** The team agreed to split Capability 9 into three distinct capabilities:

1. **CAP: Support three different families of games in the same package** — specifically the families **Lines and Ways**, **JPRG-AAB / Jackpot Rush (Georgia)** (Efim suggested "GPRG-Georgia" to disambiguate from the standard JPRG product), and **FILG (Fiery Ice Link Georgia)**. The foundational capability — never done before in a single product.
2. **CAP: Provide three unrelated (non-symbiotic) progressives within the same package of games released for the Georgia market** — three in-game progressives coexisting on the same machine. Efim emphasised this is also a novel capability — *"never did something like this."*
3. **CAP: New match-three progressive (the existing match-three-symbol concept reapplied)** — replaces the existing Georgia peach progressive bonus on the legacy peach-style games. Initially Val asked whether this was a fourth progressive; Efim clarified it is *one of the three* (the third one, alongside Jackpot Rush and Fiery Ice Link).

Juan accepted the split: *"Correct. I'll create these right after we're done, and then I'll start on the requirements for the ones already done — I just need to work on the first two."* Efim noted requirements will be short and obvious in places because most of the problems are technical (i.e., live in features, not requirements).

**Igor's question — liquid glass / new screen interface as a separate capability?** Igor (in Russian) raised whether the new screen interface / liquid-glass display redesign should be its own capability — since framework developers will work on it as a distinct workstream. Discussion:
- Irina: liquid glass is just a *requirement* — that this package must include liquid glass + 2 [other elements].
- Igor pressed: but to which of the three new capabilities does the new interface belong?
- Efim: none of them — it doesn't belong to any of these three.
- Val: liquid glass is **its own capability, already existing.** Not a new one to create here.
- Irina: technically the capability doesn't yet *exist* as a formalised record — only requirements for it exist.
- Val acknowledged that JVL doesn't yet have enough product managers who can formalise the full set of capabilities — that's a gap to work through, but for this meeting it's not blocking. The liquid-glass piece lives separately from the three GA-COAM v2 capabilities being defined here.

**Igor's second push — progressive controller + data centre.** Igor noted that **progressive controller** and **data centre** components will be needed for the implementation. Val's response (translated): *"of course, but we can't describe these from a market perspective — from a market perspective these capabilities don't change."* These belong in **features**, not capabilities. Igor accepted the framing.

**Feature-writing ownership.** Val laid out the feature-writing assignment:
- **Framework-side features**: **Igor** writes them.
- **Data-centre-side features**: **Sergey or Dima or Kharetski** writes them.

Efim asked: should we bring Sergey/Dima/Kharetski into this meeting? Val rejected: bringing more people in would just multiply the noise — *"if each person says 3 sentences, that's 60 sentences."* Better to split: finish what Igor is on now, then bring others in separately when their domain is the focus.

**Meeting recess and reconvene plan.** Val proposed retiring this meeting and reconvening in **one hour**, during which:
- Val and Juan work together on the capabilities + requirements alignment (Juan to formalise the three capabilities and write requirements for the first two; the third already largely has requirements).
- The reconvened meeting would then walk through the requirements with the engineering team, with Val raising specific requirement-level questions where capability is now clear but requirements aren't.

Juan committed to creating the capabilities right after this call. The recess decision was the closing structural point of this meeting.

## Decisions Made

- **Original Capability 9 is decomposed into three separate capabilities** (foundational multi-product, three-coexisting-progressives, and match-three). (Val + Juan + Efim, consensus.)
- **Capability vs. requirement principle** (Val's articulation, accepted by team): a capability is one-shot / executed once; a requirement is durable / reusable. A capability is the all-encapsulating frame; requirements are the singular items inside it.
- **Capability 1 (foundational, multi-product)**: Support three different families of games in the same package — Lines & Ways + JPRG-AAB (or GPRG-Georgia, Efim's naming) + FILG (Fiery Ice Link Georgia).
- **Capability 2 (multi-progressive coexistence)**: Provide three unrelated (non-symbiotic) progressives within the same package of games released for the Georgia market.
- **Capability 3 (match-three progressive)**: New match-three progressive replacing the existing Georgia peach progressive bonus on legacy peach-style games.
- **Liquid glass / new screen interface stays in its own already-existing capability scope.** Not part of the three above. (Val.)
- **Progressive controller, data centre components, and similar engineering-internal artefacts are *features*, not capabilities.** Capabilities describe market view; features describe implementation. (Val, accepted by Igor.)
- **Feature ownership split**: Igor writes framework-side features; Sergey/Dima/Kharetski write data-centre features. (Val.)
- **Do not add more participants to this meeting line** — split sessions by domain to keep the conversation focused. (Val.)
- **Recess for one hour; reconvene to walk requirements against the three new capabilities.** (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan Martinez | Create the three new capabilities in JIRA (or wherever capabilities live) — split out from the original Capability 9 | Immediately after this meeting | High | Foundational for the requirements walk-through in the reconvened session |
| 2 | Juan Martinez | Write requirements for the first two new capabilities (multi-product family support + three coexisting progressives); refine existing requirements for the match-three capability | Within the next hour | High | Reconvened meeting will walk these |
| 3 | Val Levitan | Pair with Juan on capability + requirement alignment during the recess | Within the next hour | High | Val's offered direct collaboration |
| 4 | Igor Metelski | Continue drafting framework-side features against the new three-capability structure | Ongoing | High | Once capabilities are renamed/split, Igor's features need to be retagged to the correct capability |
| 5 | Sergey / Dima / Kharetski (data-centre side) | Draft data-centre features against the new capabilities | Future meeting (separate from Igor's) | Normal | Val deferred bringing them into this thread — they get a dedicated session |
| 6 | Team | Reconvene to walk through requirements per capability | One hour after the recess | High | Val's stated plan |

## Engineering Signals

### Confirmed Signals

- **ADR — Capability-vs-Requirement definitional principle.** Capability = one-shot, all-encapsulating frame for a release. Requirement = durable, singular, reusable. This is now a JVL-wide working definition coming out of this meeting. Applies beyond GA-COAM v2.
- **ADR — Capabilities describe market view; features describe implementation.** Implementation-internal artefacts (progressive controller, data-centre components, etc.) belong in features, not capabilities. (Val, accepted by Igor.)
- **CAP — Multi-product packaged games (three families in one product).** Foundational. Lines & Ways + JPRG-AAB (Georgia variant naming: GPRG-Georgia / JPRG-AAB per Juan/Efim) + FILG (Fiery Ice Link Georgia). Never done before in a single product.
- **CAP — Three unrelated (non-symbiotic) in-game progressives coexisting on the same machine.** Independent progressive systems, no cross-symbiosis. Novel.
- **CAP — Match-three progressive replacing the legacy Georgia peach progressive bonus.** Applies only to legacy peach-style line/ways games.
- **REQ — Latest Any-bit version of Jackpot Rush is required.** (Juan confirmed inline.)
- **REQ — Liquid glass / new screen interface must be part of the V2 V43 GA-COAM v2 package.** Lives under the pre-existing liquid-glass capability scope, not under the three new ones.
- **Engineering Solution — Feature-writing ownership is split by domain.** Igor owns framework-side feature drafting; Sergey/Dima/Kharetski own data-centre feature drafting.
- **Engineering Solution — Capability decomposition by "what would be executed once" test.** When a capability description gets too heavy (Juan's complaint that "capability is growing into a requirement itself"), the heuristic is: each one-shot frame becomes its own capability.

### Suspected Signals

- **Possible REQ — JVL needs more product-manager capacity to formalise capabilities.** Val acknowledged in passing that the team doesn't have enough product managers to formalise the full capability set (specifically the liquid-glass capability is undocumented as a capability even though it exists in practice). — *Val, does this warrant tracking as a formal organisational gap / hiring requirement?*
- **Possible CAP — Liquid-glass screen interface as a formalised capability.** Per Irina, it currently exists only as requirements, not as a capability. — *Worth promoting to a capability now that the V2 V43 GA-COAM v2 work depends on it?*

## Open Questions

- **Naming convention for Georgia-variant Jackpot Rush.** Juan said "JPRG-AAB"; Efim suggested "GPRG-Georgia" to avoid colliding with the standard JPRG product. Need a canonical decision.
- **Exact list of features under each new capability post-recess.** Igor had drafted 5 features against the old Capability 9; those features now need to be retagged across the three new capabilities. The mapping isn't yet locked.
- **Liquid-glass capability formalisation.** Whether to retroactively create the capability record now (so the V2 V43 GA-COAM v2 work can reference it cleanly) or leave it as implicit.
- **Will Sergey/Dima/Kharetski's data-centre feature session happen on a fixed date** or be opportunistic?
- **What were features 3, 4, and 5** in Igor's original list? The transcript garbled them in the Russian sections — they need to be re-extracted from Igor's actual feature document.

---
*Processed from Teams transcript on May 22, 2026*
*Source meeting: Alignment — V2 V43 GA-COAM v2 / 3-JP-Progressive REQ • CAP • Features Review (20260508_091149)*
