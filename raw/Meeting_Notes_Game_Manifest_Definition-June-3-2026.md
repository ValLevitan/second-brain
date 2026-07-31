# Meeting Summary — Game Manifest Definition

**Date:** June 3, 2026, ~10:28 AM (Eastern)
**Duration:** ~1h 55m
**Attendees:** Val Levitan, Dmitriy Khandov, Irina Shishko, Andrei Bosik, Pavel Frolov
*(Referenced, not present: Alexander Biratko, Lena Zhukova, Michael Gottlieb, Efim.)*

> Spoken in Russian; summarized in English. The game is **Calle Ocho** (Miami's SW 8th Street); the raw audio transcribed it phonetically.

## Summary

The team opened a serious, multi-meeting effort to demystify how a game is designed, centered on one artifact: **the manifest**. Val's first requirement was a shared definition, because "manifest" means different things to different people — and it already collides with the *platform release manifest* used in the testing strategy.

The working definition: a machine-maintained, human-readable file describing the **structure of one game scene** (objects, types, hierarchy, masks, matrix, animation type). It is structural not visual, points only to functional resources, is one-per-scene with inheritance, is a **data contract**, is **never hand-written**, and is **volatile** as the game is born.

Irina split it into a **technical manifest** (structure + placeholders, runnable, can hold math, ugly — nearly identical across games) and a **graphical manifest** (look, sizes, positions — different per game). ~90% is a shared standard base; the rest is per-game.

Val wants the **direction reversed**: today the programmer declares the expected structure and it is checked at output (programmer → designer); the target is design defining the structure up front (design → engineering), which removes the waterfall and enables parallel work. Goal: a wide-format game in ~1 month instead of ~8.

The team mapped the manifest onto the product chain — **Capability → Requirement (with acceptance criteria) → Features → Design Document (DD, replacing the GDD)** — and tied testing to it: validate the built scene against the contract by acceptance criteria, with continuous parallel E2E rather than end-of-line testing.

**Live experiment:** the Calle Ocho transition-bonus folder (images + JSON) was given to AI, which reconstructed the screen ~80% — correct portrait 1080×1920, spine animation, localized Spanish toggle, win spinner, `BonusComplete` vs `BonusAwarded` selected by win > 0, and real fire-over-diamond resources. It missed only the spinner's exact position, which comes from a special Biratko component not in the folder.

Val's plan to move forward: take Calle Ocho's **code + GDD**, reverse-engineer back to the starting point, enumerate every unknown normally settled in design conversations, define them in the manifest, and "see where we get stuck." Next case: the same game "buffed", with a bison theme.

## Decisions Made

- **A shared definition of "manifest" comes first**, before any tooling. (Val)
- **The manifest is a data contract, generated/maintained by code or AI — never hand-written.** (Val, agreed)
- **Structure splits into a technical manifest (shared, ~90%) and a graphical manifest (per-game).** (Irina, endorsed)
- **Reverse the manifest's direction** — define structure up front from design, not check it at output. (Val)
- **The manifest is stored in the game's own repo, written down as a standard** — not in Miranda, not ad hoc. (Val)
- **Move from GDD to DD (Design Document)** in the product chain. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Drop the transcript into the chat so Andrei can work on it with AI | Same day | Normal | Andrei's request |
| 2 | Val / team | Run the Calle Ocho reverse-engineering exercise: code + GDD → starting point → list of unknowns → define in manifest | TBD (next sessions) | High | The core proof for the initiative |
| 3 | Team | Decide one-file-vs-two for the technical/graphical manifest | TBD | Normal | Open structural question |
| 4 | Team | Find an external source of truth so manifest tests are not circular | TBD | High | Otherwise the test proves nothing |

## Open Questions

- **External source of truth** — how to avoid the circular "export the scene, test against the same scene" trap.
- **The non-deterministic ~20%** — bonuses, transitions, non-standard behaviour; how the manifest captures it.
- **One file or two** for technical vs graphical.
- **Where a transition lives** — inside the main scene or as its own object.
- **How "Requirement", JIRA "Story", and "DD vs GDD" reconcile** with the June 2 JIRA tree (Capability → Feature → Story).

## Engineering Signals

- Manifest-as-data-contract aligns with NOVA's "one repo, one data contract" principle and with the testing strategy's generated contracts.
- **Terminology risk:** "manifest" is overloaded across JVL — game-scene manifest, platform release manifest, and likely more. Always qualify the word; never use it bare.
- AI reconstruction at ~80% from manifest-style data alone suggests the deterministic bulk of a scene is already automatable; the value is in capturing the undocumented ~20%.
- Continuous parallel E2E (not end-of-line) is the assumed testing model, consistent with testing strategy v13 and the E2E framework work.

## Related

- Initiative: **Game Design Manifest** — `Initiatives/Game Design Manifest/statement_of_purpose.md` (canonical write-up).
- Reverse Requirements Engineering; NOVA Gaming Platform; Testing Strategy v13; JIRA Hierarchy (June 2).

---
*Processed from Teams transcript on June 3, 2026.*
*Source meeting: Manifest-20260603_062837-Meeting Recording.*
