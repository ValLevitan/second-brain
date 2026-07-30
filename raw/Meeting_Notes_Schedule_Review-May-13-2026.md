# Meeting Summary — Schedule Review
**Date:** May 13, 2026, 12:03pm – 2:46pm ET
**Duration:** 2h 43m
**Segment:** 1 of 2
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko

## Summary

Reshuffled the JIRA portfolio across four tracks.

- **Coamazen II / Liquid Glass:** Anton's FRAM 11-97 + 11-99 dropped as duplicates of Game Production work (IP 89 / IP 446 / IP 966). New Story added under FRAM 11-82 to anchor Igor's leftover multi-product work. Anton creates branch; Alyosha sets up builder.
- **Multi-Progressive:** Order swapped — 11-33 (June 2) before 11-34 (June 4). Match-3 bonus progressive lands ~June 11. Dima Kovalchuk pulled in May 18 to break BP 26-93 down.
- **Flex POS Alpha (Elizabeth, Georgia):** Release slid May 15 → May 20. Flow = SD install → QR passport register → Lease → Mutogus/printer/Income sandbox → Payment Hub logs.
- **Flex Recycler (IP 1059):** Capabilities still landing; ~20+ features unscheduled. Hardware ~1 month out. Schedule review booked for Tuesday May 19.
- **IP 1007 (Dispenser):** Tech changed from Pyramid printers → Flex Port + Telekt; description must be rewritten.
- **IP 527 (Player GUI):** Pushed to ~June 8.
- **Cleanup:** Flex Tower, Flex Tito Server, Flex Pay Cloud, Flex Port Wallet, Flex Pay Wallet — all archived/deleted. Flex Pay Software Platform → Backlog. ISO concept retired (Ivan needs briefing).

## Decisions Made
- Flex POS Alpha release date moved May 15 → May 20.
- Anton's FRAM 11-99 duplicate features deleted; work consolidated under Game Production.
- Multi-progressive sequencing: 11-33 (Jun 2) before 11-34 (Jun 4); Match-3 bonus progressive ~Jun 11.
- IP 1007 to be rewritten for Flex Port + Telekt printer technology.
- Stale features (Flex Tower, Tito Server, Pay Cloud, both Wallets) archived; Flex Pay Software Platform → Backlog.
- Architecture review with Dima Kovalchuk required before he starts Flex Pay rework.

## Undertakings

| # | Who | What | By When |
|---|-----|------|---------|
| 1 | Pavel | Order ~5 sandbox INCOM cards via Sergey Perestoevsky, ship to Elizabeth | Before May 20 |
| 2 | Pavel | Write Elizabeth's Alpha-release walkthrough | May 20 |
| 3 | Pavel | Add Story under FRAM 11-82 for Igor's leftover work | This week |
| 4 | Pavel | Plan Flex Recycler resourcing with Sasha (borrow Zhenya/Sergey T?) | Before May 19 |
| 5 | Pavel | Hand LGS 11-38 to Sergey Tsumanov if Zhenya needs runway | This week |
| 6 | Pavel | Pull in Dima Kovalchuk to decompose BP 26-93 | May 18 |
| 7 | Irina | Settle product structure for 3 game packages with Dima + Zhenya | This week |
| 8 | Irina | Brief Ivan that ISO (Wallet) tabs no longer apply on GitHub | Soon |
| 9 | Val | Book Flex Recycler schedule review (Pavel + Andrei) | Tue May 19 |
| 10 | Val | Architecture review with Dima before Flex Pay rework | Before Dima starts |

## Engineering Signals

**Confirmed**
- **ADR — Printer tech migration:** Pyramid printer + library replaced by Flex Port + Telekt printers. Affects IP 1007 and all dispenser/recycler ticket printing.
- **ADR — ISO model retired:** Flex Port Wallet / Flex Pay Wallet concept (ISO-based) no longer applicable on the GitHub workflow.
- **ADR — Service consolidation:** Flex Pay Cloud → Payment Hub.
- **ADR — Flex Tower / Flex Tito Server retired.**
- **REQ — Flex POS Alpha acceptance:** Elizabeth must complete SD install → QR passport registration → Lease creation → Mutogus/printer/Income sandbox card flow → Payment Hub log visibility.
- **CAP — Match-3 bonus progressive:** Different ceiling values than existing progressives; help-screen plumbing needs to surface correct ceiling per product.

**Suspected**
- **Possible ADR — Per-feature scheduling for Flex Recycler:** Capability-driven features need individual schedules with task-level rollup before the overall epic can show a date.

## Open Questions
- Routing for INCOM sandbox cards from Toronto — Pavel direct or via Sergey Perestoevsky?
- Does Sasha need a Spike ticket for "feature grooming" time, or stay informal? Val resisted creating a JIRA to-do-list pattern.

---
*Processed from Teams transcript on 2026-05-13*
*Source meeting: all_schedule_review-May-13-2026 (12:03pm segment)*
