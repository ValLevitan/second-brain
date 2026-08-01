# Meeting Summary — JIRA Hierarchy Standard Review

**Date:** June 19, 2026, 11:01 AM Eastern
**Duration:** ~1h 26m
**Attendees:** Val Levitan, Dmitri Kovalchuk, Andrei Bosik, Pavel Frolov, Irina Shishko

## Summary

The team reviewed Dmitri's draft standard for JIRA hierarchy and terminology. The meeting was conducted in Russian. Five documents were shared ahead of time — two versions of the standard (Russian/English), one from Andrei, one from Irina, and an HTML linking releases to the hierarchy.

**Glossary.** The team walked through term definitions. "Capability" is a business-level system ability sized to fit within a release, living in its own JIRA project. "Requirement" describes what a capability must do (functional or non-functional). "Initiative" is a time-bound grouping of capabilities. Most definitions were accepted without objection. Val endorsed the glossary as useful and overdue.

**ADRs (Architecture Decision Records).** Significant debate about when ADRs are needed. Pavel argued they should be written even for straightforward new functionality. Dmitri said only when choosing between alternatives. Andrei read from a reference text confirming ADRs record decisions and reasoning for future teams — not needed for every feature. Val drew a clear line: ADRs are for architectural decisions, not tech stack choices, and not every feature warrants one. The team settled on ADRs being situational, not mandatory per feature.

**"Component" terminology.** Val challenged why "component" needs to exist as a concept given the agreed rule that one JIRA project = one GitHub repository. Dmitri explained it as a unifying term across contexts (library, service, platform). Pavel clarified components are useful as JIRA-internal categorization (e.g., marking tasks as "frontend" or "backend" within a project, auto-assigning component owners). Val accepted this as a JIRA-level convenience but pushed back on elevating it to a defined concept in the standard.

**"Platform" vs "Product."** Val corrected that Flex IQ is a product, not a platform. Dmitri agreed to drop "platform" and use "product," which aligns with having a product owner role.

**Feature-to-repository relationship.** Under the new model, one feature belongs to one project/repository. If work spans repos (e.g., frontend and backend), separate features are created in each. Andrei noted this differs from current practice where one feature could link branches across repos, but agreed it's cleaner. No artificial limit on the number of feature branches per feature.

**ADR location.** ADRs live in the repository they relate to. If the same decision applies to multiple repos, it gets duplicated into each — not stored centrally in an integration repo. Val: this is how both humans and AI naturally work, and duplication costs nothing. Integration repos can have their own ADRs (e.g., why a particular end-to-end testing tool was chosen), but those are about integration-level decisions, not component decisions.

**Requirements vs capabilities.** Requirements emerge from capabilities. Val framed it: requirements are to product owners what features are to developers — different language for different audiences. Dmitri agreed to clarify this relationship in the standard.

**Release model.** A release equals the sum of closed capabilities, though a release can contain just one capability. Component releases are auto-generated from tags; product releases compile a version matrix. The matrix template is known in advance (which components); only the versions are filled in at release time based on QA-approved tags. Release notes can be similarly auto-generated.

**Bugs and tests.** Not covered in this standard. Val directed the team to keep it that way — experiment first, standardize later.

**ADR traceability in JIRA.** No separate JIRA task needed to create ADRs — they ship with the feature. No JIRA-side tracking of which ADR maps to which requirement. The one-way link from ADR to requirement code in GitHub is sufficient.

## Decisions Made

- **Replace "platform" with "product" in the standard** — Flex IQ and similar assemblies are products, not platforms. Aligns with product owner role. (Val, Dmitri agreed)
- **ADRs are situational, not mandatory per feature** — Write an ADR only when an architectural or technical decision is made between alternatives, or when a fundamental choice needs to be recorded for future reference. (Consensus)
- **ADRs live in individual repositories, duplicated when applicable** — No central ADR storage in integration repos. Duplication across repos is acceptable and expected. (Val, Andrei, Dmitri agreed)
- **One feature = one JIRA project = one repository** — If work spans repos, create separate features in each. (Consensus)
- **No artificial limit on feature branches per feature** — The standard should not restrict this. (Andrei, Pavel, Val agreed)
- **No separate JIRA task for ADR creation** — ADRs are committed alongside the feature code. (Pavel, Val, Andrei agreed)
- **No JIRA-side ADR-to-requirement traceability needed** — One-way link from ADR to requirement in GitHub is sufficient. (Val, Andrei)
- **Bugs and tests excluded from this standard** — To be standardized later after experimentation. (Val)
- **Remove "semver" abbreviation from the standard** — Write out "version" in full; the abbreviation was unclear. (Val, Irina)

## Open Questions

- Where exactly does the boundary lie between an ADR and a tech stack choice? Val sees them as separate; Dmitri sees tech stack selection as an ADR function. Not fully resolved — the team moved on.
- How will cross-repository feature work be managed day-to-day when the new model requires separate features per repo? Andrei noted the old approach (one feature, multiple repo branches) was convenient. Practical workflow not yet tested.
- Component definition remains somewhat loose — useful as JIRA categorization but not rigorously defined in the standard. May need revisiting as the team gains experience.

---
*Processed from Teams transcript on June 19, 2026*
*Source meeting: Review JIRA Hierarchy Standard (Dmitri)*
