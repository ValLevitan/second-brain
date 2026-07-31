# Meeting Summary — White Label Experiment

**Date:** June 3, 2026, 3:34 PM (Eastern)
**Duration:** ~23 minutes
**Attendees:** Val Levitan, Irina Shishko, Pavel Frolov
*(Spoken in Russian; summarized in English. Referenced but not present: Evgeny Kharetski "Zhenya".)*

## Summary

This is the practical follow-on to the morning manifest meeting. Val wants to pull the common, non-creative parts of JVL's games out of the existing code and turn them into a reusable starting shell for new games. He calls these the "known" elements — buttons, dashboards, arrows, progressives — the parts that barely change from game to game.

His argument: designers spend time fussing over small details (button radius, a star here, a screen there) that don't move revenue. He's seen weaker-looking games at locations earn more, so these shared parts are already "good enough" and shouldn't be re-polished for every title. The dashboard, for example, takes only 10–12% at the bottom of a horizontal machine, with tiny margins.

The plan: extract these shared components from the code, describe them, and build an auto-populate command. A product owner picks options (theme, number of lines, number of bonuses, transitions) and the shared shell drops straight into the code already built. Val drew the same analogy as before — the repository felt impossibly complex until someone organized it on shelves, then it was simple.

Math and game mechanics are deliberately left out for now. They live in a separate project and are being decrypted and ported to Rust. Pavel pushed back that the mechanic is bound to the math and may not be extractable yet; the group agreed to set math/mechanics aside and handle only the known UI components first.

Pavel's framing is the one that landed: this is essentially a **white-label** code base — a shared environment copied for each new game. Val rejected calling it a "template/armada" because that implies a fixed design imposed on every game, which he doesn't want.

Irina said she already experimented after the morning meeting — she asked Claude to pull a manifest from Calle Ocho and it extracted everything (math, percentages, lines, layouts, symbols); the task now is to structure that so it's reusable. Val suggested she also have Claude build a product-owner questionnaire (the questions a PO answers when planning a new game) that can feed straight into code.

Concrete next step: hand Evgeny Kharetski ("Zhenya") a time-boxed experiment — take Calle Ocho, reverse-engineer it, pull out the common components, strip the creative/theme, and produce a reusable white-label environment for a vertical machine. He reports back in plain language on what's achievable. Deadline Monday, June 8; Val will book a review with him around 10:00 AM.

## Decisions Made

- **First pass covers common UI components only** (buttons, dashboards, arrows, progressives); math and mechanics are out of scope. Reason: math/mechanics are in a separate project, still being ported to Rust. (Val; agreed by Pavel and Irina)
- **Build a reusable "white-label" environment, not a rigid template.** Reason: Val won't impose a fixed "template/armada" design on every game — only the shared shell is reused. (Val; term coined by Pavel)
- **Reverse-engineer Calle Ocho as the source game.** Reason: continues the morning's manifest work; everything extractable comes out of it. (Irina, Val)
- **Defer Pavel's add-on ideas** (checkbox re-skin with new resources; auto-convert vertical→horizontal) to a later stage. (Val)
- **Time-box to Monday, June 8**, with a Val–Kharetski review ~10:00 AM. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski (Zhenya) | Reverse-engineer Calle Ocho: extract common components (buttons, dashboards, arrows, progressives), strip creative/theme, and build a reusable white-label environment for a vertical machine that copies per game. Report back in plain language on what's achievable. | Mon Jun 8, 2026 | High | Core experiment for the white-label/manifest approach. |
| 2 | Irina + Pavel | Brief Kharetski and hand him the experiment task. | Before Jun 8 | High | Kharetski wasn't in the meeting; Irina confirmed she'll give him the task. |
| 3 | Irina | Have Claude build a product-owner questionnaire — the questions a PO answers when planning a new game (theme, # lines, # bonuses, transitions) — so answers feed straight into code. | TBD | Normal | Val's suggestion; builds on her earlier Claude/manifest pull. |
| 4 | Val | Book the Val–Kharetski review for ~10:00 AM Mon Jun 8 (with Irina and Pavel); drop the transcript/recording into the chat. | Jun 8 | Normal | Val said he'd schedule it and post the transfer. |

## Open Questions

- Can the game mechanic actually be extracted, given it's bound to the math in a separate Rust project? Pavel is skeptical. Set aside for now — the experiment covers only the known UI components.

## Related

- Initiative: **Game Design Manifest** — `Initiatives/Game Design Manifest/`
- Sibling meeting (same day): `Meeting_Notes_Game_Manifest_Definition-June-3-2026.md`

---
*Processed from Teams transcript on June 3, 2026.*
*Source meeting: Call with Irina and 1 other-20260603_113434-Meeting Recording.*
