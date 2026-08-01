# Meeting Summary — White-Label Experiment Review (Calle Ocho)

**Date:** June 25, 2026, 2:37 PM (Eastern)
**Duration:** ~1 hour 2 minutes
**Attendees:** Val Levitan, Evgeny Kharetski (Zhenya), Irina Shishko, Pavel Frolov
*(Spoken in Russian; summarized in English. Referenced but not present: Michael Gottlieb, Efim, Lena Zhukova.)*

## Summary

Zhenya demoed the white-label experiment he built in the `ng-gameplay` template repository. The system uses Claude Code skills and hooks to automate new-game creation through a structured pipeline.

**The pipeline works in two stages:**

**Stage 1 — Designer interview.** A Claude Code skill runs a fixed 10-question interview with a game designer (Efim, Michael, or others). Questions cover game mechanics — spin types, bonus types, symbol types, progressives, free spins. If a question is skipped, Claude flags it at the end. Based on the answers, Claude auto-generates Capabilities and Requirements with acceptance criteria (3+ per Requirement, written to be testable). In the demo, one interview produced 10 Capabilities and 36 Requirements.

Before creating new Requirements, Claude searches JIRA by labels/tags for existing ones. Two-pass search: exact match first, then expanded semantic search via JQL if the first pass misses. If an existing Requirement fits, it proposes reuse. If similar but not exact, it recommends creating a new one. Everything stays in local memory during the interview — nothing is written to JIRA until the user validates.

**Stage 2 — Repository assembly.** A developer runs a second skill from the same `ng-gameplay` repo. Claude checks the module catalog (each module has an NPM manifest declaring which Requirements it implements), verifies all needed modules exist, and assembles a game repository. If a module is missing, it flags which Requirements are unsatisfied and that new code is needed (Features for developers). Placeholder graphics are generated to match the manifest contract — when designers later upload real art, contract validation rejects anything that doesn't match the expected sizes or format.

**Key discussion points:**

- **JIRA labels.** Val clarified his prior objection to labels was about human typos creating duplicates. Machine-generated labels are fine.
- **Capability tagging.** Val pushed to tag by project name/number rather than game name. Zhenya agreed — game = project = repository, so it's the same thing with a different label.
- **Features always needed?** Val wanted Features created even for reused code (for branch tracking). Zhenya explained: if all modules exist, the game is assembled automatically — no dev work, no Features needed. Features are only needed when modules are missing (dev side) or for new graphics (designer side). Val accepted.
- **"Artificial Michael."** Zhenya created a second Claude instance playing game designer Michael — trained on all prior meeting transcripts, Irina's JIRA scheme, and the Calle Ocho decomposition. Val got excited about the broader idea: an AI producer who knows all JVL games and could compare competitor games against JVL's catalog.
- **Omni only.** This approach works for Omni/NOVA (modular, one repo per game). Rage is out of scope — monolithic codebase, no modularity, nothing to assemble from.
- **Windows support.** Designers use Claude Desktop (Windows app), not CLI. Zhenya noted he needs to duplicate paths so skills work on Windows too.

## Decisions Made

- **Machine-generated JIRA labels are acceptable.** Val's prior objection was about human typos only, not the concept. (Val)
- **Capabilities tagged by project name/number**, not game name. Game = project = repository. (Val, Zhenya agreed)
- **Finish proof of concept on Omni/NOVA first.** Rage has no modularity — out of scope. (Zhenya, Pavel; Val accepted)
- **Proof of concept is close.** Team confirmed no major doubts remain. Next milestone: complete the full path to a working assembled game. (Val; all agreed)

## Undertakings

## Undertakings

None. The team agreed the next milestone is completing the full path to a working assembled game, but no specific actions, owners, or deadlines were assigned.
## Engineering Signals

- Token consumption is modest: ~40K tokens consumed during the 10-question interview (starting from ~60K base context).
- The `ng-gameplay` repository already existed but was unused; Zhenya repurposed it as the template home.
- Module manifests use standard NPM `package.json` to declare which Requirements each module implements.
- Acceptance criteria are baked into the skill rules — Claude generates 3+ testable criteria per Requirement automatically.
- Contract validation on graphics prevents designers from uploading assets that don't conform to the manifest (wrong size, format, etc.).

## Related

- Initiative: **Game Design Manifest** — `Initiatives/Game Design Manifest/`
- Prior meeting (same initiative): `Meeting_Notes_White_Label_Experiment-June-3-2026.md`
- Prior meeting (same initiative): `Meeting_Notes_Game_Manifest_Definition-June-3-2026.md`

---
*Processed from Teams transcript on June 25, 2026.*
*Raw transcript: `Initiatives/Game Design Manifest/evidence/transcript_white_label_review_june-25-2026.md`*
