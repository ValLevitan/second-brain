# Meeting Summary — RIS Persona Clarity
**Date:** July 8, 2026, 2:45 PM ET
**Duration:** ~16 minutes
**Attendees:** Val Levitan, Juan Martinez

## Summary

Val and Juan worked through the five "personas" that surfaced when the RIS code was reverse-engineered into human-readable requirements. The goal was to clarify what each persona means today and what it should become as the system is redesigned.

Juan corrected an earlier misunderstanding: he had asked for proper generic role names (like "system administrator"), not surnames of real people. Val agreed and they went persona by persona.

Val flagged a structural problem: the reverse-engineering produced only 22 requirements, which are too coarse because the code ties whole pages to one person. He thinks each should be split into five or more finer requirements. The plan is to first document how the system works today, then use that gap analysis to design new personas, requirements, features, and code.

They also discussed that access today is granted informally to people Val trusts (Juan, Elizabeth, Felipe on CMS/RIS) because the proper role structure does not exist yet. The redesign should introduce real granularity of access.

**Persona mapping agreed:**
- **P1 – System Administrator:** Juan and Elizabeth today (enter basic setup info within preset thresholds). Future → internal (JVL) technician.
- **P2 – Service Technician:** JVL field technician today (e.g., Sebastian before moving to product). Future → external/customer technician; drop the "JVL" qualifier.
- **P3 – CMS Core:** Machine-generated name for the central system that pulls configurations over the transit interface. Not a human — should be reclassified as a system architecture element, not a persona.
- **P4 – Performance Analyst:** Juan's role today (and Felipe) — sets RTP, max bets, jurisdiction parameters with the customer. Future → Product Manager.
- **P5 – Senior System Administrator:** Engineering-level admin who sets the thresholds/safety nets (Irina and Pavel today). Future → engineering architect, with authority split across product ownership (VP of Products) and engineering (Director/Vice Director of Engineering).

A key design intent: keep RIS (it makes installation fast) but allow the configuration to be tweaked in the field after install, which cannot be done today.

## Decisions Made

- **Reclassify P3 "CMS Core" from a persona to a system architecture element** — it is a machine interface, not a person. (Val to make the correction; Juan agreed.)
- **P5 threshold-setting is not just legislative** — it also covers system rules like button counts per class/jurisdiction; redesign should give this authority two inputs (product ownership + engineering). (Val, endorsed by Juan)
- **Future roles split P1/P2 into two distinct roles** — internal technician (P1) vs. external technician (P2), rather than one combined internal/external role. (Val, agreed by Juan)
- **RIS stays but becomes field-editable** — do not remove RIS; allow post-install tweaking. (Juan, endorsed by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Correct persona list so P3 "CMS Core" is a system architecture element, not a persona | TBD | Normal | Agreed it is a machine interface, not a human |
| 2 | Val | Save this transcript to notes and circulate it to Juan, then post to chat | TBD | Normal | Basis for continuing the persona/requirements rework |
| 3 | Val | Split the 22 coarse requirements into finer, singular requirements (~5+ each) | TBD | Normal | Current requirements bundle too much per page |

## Open Questions

- How exactly to model "CMS Core" as a system architecture element (non-human machine interface) in the new design.
- Final naming and authority structure for P5 (engineering architect vs. combined product/engineering authority).

---
*Processed from Teams transcript on July 8, 2026*
*Source meeting: RIS_persona_clarity-July-8-2026*
