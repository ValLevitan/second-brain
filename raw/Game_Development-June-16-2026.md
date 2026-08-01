# Meeting Summary — White Label Game Development

**Date:** June 16, 2026, 4:02 PM Eastern
**Duration:** ~41 minutes
**Attendees:** Val Levitan, Evgeny Kharetski, Pavel Frolov, Irina Shishko

## Summary

Val opened by framing the purpose: explore whether AI can help assemble games from structured designer input, using contracts and capabilities instead of per-game custom programming.

**Terminology standardization.** Val established the vocabulary the team must use going forward. "Contract" replaces "template" — it communicates constraints designers must work within. "Game mechanics" = the combination of math and visual layout that defines a game. "Capabilities" replaces "questionnaire" and "reskin" — designers express what they want through capabilities tied to requirements. "Artifact" = any final deliverable (code or graphic). "Manifest" is retired; data contracts and repos replace it.

**Architecture concept.** Each game = one project = one repository. Designers describe a game through capabilities. The repo gets filled with artifacts governed by data contracts. Common resources (buttons, arrows, fonts, frames) are reused across games. AI assembles games from pre-built components based on capability descriptions — like a website constructor. Programmers write new mechanics when needed; AI uses existing blocks for everything else. Quality control validates artifacts before they merge to main — visual comparison of what the designer committed against what the capability described.

Irina raised a concern about code duplication across repos (e.g., Calle Ocho 1 and Calle Ocho 2 sharing the same mechanic). Evgeny explained the game engine and mechanics layer would be separate from per-game graphics. Some code duplication across game repos is acceptable — it's more transparent than a shared-code monorepo with conditional theme loading.

**Sandbox experiment.** Val wants to prove this out quietly before involving the broader team. The plan: take the existing Calle Ocho game, reverse-engineer it into capabilities and requirements, then try to reassemble it from those descriptions. "Translate Russian to English, then English back to Russian, and see what survived." This stays confidential — Val doesn't want to cause alarm among the wider team until the approach is validated.

Val referenced a document from Boris Cherny about frontend/repo organization that he sent overnight. Evgeny hasn't read it yet but will.

**Roles and next steps.** Pavel Frolov quarterbacks the sandbox setup. Evgeny experiments with the reverse-engineering approach. Dmitri Kovalchuk (via Ivan) sets up the sandbox JIRA project with requirements and capabilities. Next check-in is June 25 at 8:00 AM Toronto time.

Evgeny asked for the transcript from the previous meeting he was patched into but wasn't formally invited to. Irina downloaded it and will send it to him. Val will also post the current meeting's transcript.

## Decisions Made

- **Use "contract," "capabilities," "game mechanics," and "artifact" as standard terminology** — drop "template," "reskin," "questionnaire," and "manifest." (Val)
- **Each game = one project = one repository** — code duplication across game repos is acceptable over a shared monorepo. (Evgeny, agreed by group)
- **Sandbox-first approach** — prove the concept with Calle Ocho before involving the broader team. (Val)
- **Keep the initiative confidential** — don't disclose to the wider team until validated. (Val)
- **Pavel Frolov leads coordination** — quarterbacks the sandbox setup and orchestration. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Read Boris Cherny's document about repo/frontend organization (sent by Val) | June 25, 2026 | High | Understanding alternative architecture patterns before next check-in |
| 2 | Evgeny Kharetski | Talk to Dmitri Kovalchuk to get sandbox JIRA project set up (requirements, capabilities, feature branches) | June 25, 2026 | High | Needed before experimentation can begin |
| 3 | Evgeny Kharetski | Begin reverse-engineering Calle Ocho game into capabilities/requirements, then attempt reassembly | June 25, 2026 | High | Core experiment to validate the white-label approach |
| 4 | Pavel Frolov | Quarterback the sandbox setup — coordinate all elements needed to get the experiment running | June 25, 2026 | High | Val assigned him as the orchestrator for this initiative |
| 5 | Irina Shishko | Send Evgeny the previous meeting transcript he couldn't access | June 17, 2026 | Normal | Evgeny needs context from the prior meeting |

## Open Questions

- Can AI reliably assemble a game from capability descriptions and pre-built components? (The sandbox experiment is designed to answer this.)
- What specific data contracts are needed for designer artifacts? (To be discovered during the Calle Ocho reverse-engineering exercise.)
- How should visual quality control work in the merge pipeline — compare committed graphics against capability descriptions, or against the designer's original artwork? (Raised but not fully resolved.)

---
*Processed from Teams transcript on June 16, 2026*
*Source meeting: White label game development*
