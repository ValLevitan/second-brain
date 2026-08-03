# Meeting Summary — Spec_gaps
**Date:** July 30, 2026, 10:01–10:25 AM Eastern
**Duration:** ~23 minutes
**Attendees:** Andrei Klimovich, Val Levitan, Juan Martinez
**Raw transcript:** [[Meeting_Transcript_IQ_Unit_Location_Binding-July-30-2026]]

## Summary

Andrei raised a design gap in the IQ / Flex IQ rollout: the system cannot verify that a given IQ unit is physically at the location it is registered to. Today the unit is bound to a location manually in the payment hub. Nothing stops an operator from moving a unit from a registered location A to an unregistered location B; cards issued at B would still pass and be billed to A.

Andrei walked through how registration works: JVL sends a location's details (license number, address, contact) to Incom, Incom verifies and returns secret keys, and those keys plus location data are set up as a location profile in the payment hub. Each card-issue request sends those keys, and Incom returns a success pass if they match. The unit itself has no awareness of its physical location beyond that manual link.

Juan explained that Incom used to verify that a location was GLC-authorized (up to ~36 hours), but stopped — the burden of checking thousands of locations now falls on the master under lottery penalty. Juan's view: if the location is lawfully authorized and JVL still gets the card event and bills for it, the mismatch may not matter much.

Andrei framed two approaches: keep the manual binding (JVL must know each unit's destination), or push binding onto the operator (JVL just ships units and operators distribute them). Val preferred the operator-driven approach, noting it mirrors how operators already move JVL machines and reassign CoMIDs without telling JVL. Val added that an LTE modem's triangulation, combined with the Mother Goose serial number, would give a fairly reliable read on a unit's location — and that JVL should "quietly" listen to it rather than actively police it.

The group discussed a related legal/collections angle: registering credit against a company's title so units can't simply walk with a company sale, versus the friction that puts on operators. Also noted: an Incom decommissioning step exists but JVL only learns of decommissioning if told, or if a new device registers at the same location; otherwise a unit just shows zero revenue, which is a possible theft/abuse vector.

Val's overall direction: don't over-engineer a solution in a vacuum. For the 5-machine pilot the gap is not important (one location per operator, close communication). Get to a real pilot, gather real cases, and revisit. The topic was explicitly parked. Val also floated needing a minimum monthly charge per unit (~$10, figure TBD) so parked units still generate some revenue.

The main pilot blocker is the production environment Andrei is still trying to get from Incom; he is pushing them daily and won't release until it's tested on production.

## Decisions Made

- **Park the unit-to-location verification problem** — not important for the 5-machine pilot; revisit once real-world data exists. Avoid engineering a solution without exposure to the actual problem. (Decided by Val, agreed by Andrei and Juan)
- **Prefer operator-driven unit binding over JVL manual binding** for the longer-term model — mirrors how operators already handle JVL machines. (Val's stated preference; not finalized)
- **Focus effort on getting to a live pilot run** rather than on edge-case design. (Decided by Val, agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Keep pushing Incom daily to deliver the production environment; do not release until tested on production | Ongoing (daily) | High | Main pilot blocker |
| 2 | Andrei Klimovich | Test the rewired cable for the direct-connection solution devised the previous day and report back | TBD (right away) | Normal | "I'll test it right away. I'll let you know." |
| 3 | Val Levitan | Consider/define a minimum monthly charge per unit (~$10, figure open) so parked units still generate revenue | TBD | Low | Raised as something on Val's mind, not yet decided |

## Open Questions

- Should JVL move to operator-driven binding, and if so what binding procedure (semi- vs fully-automatic)? Raised by Andrei; direction leaning operator-driven but not finalized.
- Whether JVL should register credit/units against a company's title (as done conceptually with loans) to protect collections when locations/companies are sold. Raised by Val; unresolved due to operator-friction concern.
- What the minimum monthly charge should be ($10 vs $100 vs other). Raised by Val.
- How to handle Incom decommissioning notifications reliably. Raised by Juan; noted as low urgency.

## Dispatch Log

---
*Processed from Teams transcript on July 30, 2026, 10:38 AM Eastern (scheduled meeting-watcher, capture-only)*
*Source meeting: Spec_gaps (Teams, organized by Val Levitan)*
