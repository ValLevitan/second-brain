# Meeting Summary — REQ State of Readiness (Transactional)
**Date:** July 2, 2026, 9:19 PM Eastern
**Duration:** ~50 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Juan Martinez

## Summary

Val asked for a clear picture of where each transactional product stands on capabilities, requirements, use cases, and personas. The team went product by product.

**Recycler** — Best-covered product. Player experience fully covered. Root operator role ~80% (missing settlement and alerting). Technician / JVL master / JVL technician roles covered for use cases and capabilities, but no written requirements. The **Georgia version** (hidden card-to-card conversion, then cash) is not covered at all and needs high priority.

**Flex IQ** — Covered only at the player-experience level (basic MVP: issue gift/debit card, pull transaction from Mother Goose, print receipt). No operator or technician coverage. It's in release-candidate phase, expected to be delivered next week. It was built without properly collected written requirements — files exist but aren't groomed. (Formerly called Flex POS, which did have documentation.)

**Payment Hub / Operators Dashboard** — Andrei built an interactive HTML prototype with Claude covering operator, root operator, and JVL technician roles from the recycler view, including reports, financial reconciliation, and invoicing. Requirements exist from the recycler side. JVL role still needs adding (a day or two). Nathan has already done significant work here.

**Port, SMIB, Dispenser** — Port and SMIB are functional products with initial requirements; no personas/use cases. Dispenser has very little but can be spun up quickly. None are August-show priorities.

**August Georgia Expo** is the driving deadline. Val wants a beautifully polished Flex IQ with an operator interface (showing operators their machine intelligence/accounting) as the minimum, and the Georgia recycler added if capacity allows — that would make it a "killer show." Texas market (needs recycler/dispenser) is secondary to Georgia.

Core tension: the team can't write clean requirements for something built in a vacuum. Plan is to test the live IQ release candidate, do a gap analysis against a written MVP vision, and convert findings into requirements in parallel.

## Decisions Made

- **August Georgia Expo priorities are Flex IQ (polished, with operator interface) + Georgia-version Recycler.** Port, SMIB, and Dispenser are not show priorities. (Val, endorsed by Juan and Andrei)
- **Payment Hub added as a third product needing formal requirements**, alongside IQ and Recycler. (Val)
- **Two meetings Tuesday, July 7:** 9:00 AM for IQ (MVP vision + requirements, bringing engineers Pavel, Irina, Gennadi); afternoon (~4:00 PM) for Payment Hub operators dashboard requirements. (Val, Andrei)
- **Thursday, July 9:** meeting with engineers on task scheduling, after requirements are sent Tuesday night for them to absorb. (Val)
- **Andrei's Georgia trip approved** — budget is a "go," booking an apartment for two months, in the Georgia office Monday July 13. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Juan | Contact John at InCom (include Alan + team) to verify the second/rollover card conversion (ATM-to-instant-cash) for the Georgia recycler; report back whether to push for integration | Mon Jul 6 | High | Determines if Georgia recycler is feasible for the August show; Val trusts Alan's answers over John's |
| 2 | Juan | Compile all Flex POS requirements and notes he holds over the weekend; add to Monday call with Andrei to feed the Flex IQ requirements discussion | Mon Jul 6 | High | Flex POS docs are the basis for IQ requirements |
| 3 | Andrei | Talk to Juan Monday re the Payment Hub prototype; if aligned, convert the HTML operational dashboard into written operator-portal requirements | End of Tue Jul 7 | High | Feeds the Tuesday afternoon Payment Hub meeting |
| 4 | Andrei | Write a high-level MVP vision document (his vision, with clusters) and share with Val and Juan | Tue Jul 7 (for meetings) | High | Needed as the baseline to gap-analyze the live IQ |
| 5 | Andrei | Resolve a corporate card with a higher credit limit for the Georgia apartment booking (take up with Inna; Juan's card as backup) | Before Georgia trip | Normal | Current limit too low to book the apartment |
| 6 | Andrei | Travel to Georgia over the weekend; be in the office Monday Jul 13 to connect the IQ release candidate to Mother Goose + machines and test the full cycle for gaps/defects | Mon Jul 13 | Normal | First real hands-on test of the live product |
| 7 | Val | Schedule the two Tuesday meetings (9 AM IQ, ~4 PM Hub) and the Thursday engineers scheduling meeting | — | Normal | Val booked at least one during the call |

## Open Questions

- What exactly is the IQ MVP, and how close is the "under the hood" ecosystem (Payment Hub, MSBC integration) to release? Still a black box to the product team.
- Whether Flex Pay should also be shown, since Flex IQ currently talks only to Mother Goose (not Flex Port yet), and Flex Pay↔Flex Port already works — possibly an easier lift.
- Juan wants a separate short session with Val on caps and requirements for RIS (will send a sheet).

---
*Processed from transcript on July 3, 2026*
*Source meeting: REQ state of readiness- Transactional*
