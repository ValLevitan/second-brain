---
type: meeting
title: Flex POS use-case review — redeem & authentication workflows (June 20 2025)
date: 2025-06-20
source-count: 1
---

# Flex POS use-case review — redeem & authentication workflows (June 20 2025)

Working session led by [[wiki/people/nathan-carver.md|Nathan Carver]] with [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]]. Explicitly the **next-day continuation** of the [[wiki/meetings/2025-06-19-flex-pos-use-case-design.md|June-19 Flex POS use-case design]] session ("the use cases that we just started discussing yesterday") — a distinct meeting, not a re-transcription.

Substance — the redeem-ticket workflow diagram (four actors, session tied to an auditable ticket-redemption record; Incom pre-authorise → "activate" the gift card as a two-step in-sync operation with a bounding-box retry), the user-authentication use case (September-1: single-stage PIN or magnetic-card; defer 2FA; three role levels admin/manager/cashier, each PIN tied to a user, cloud-controlled), Val's failure-mode questions (POS as a critical single point of failure; two POS in parallel; recovery/lock-up; ask Incom John since JVL is on the hook for fund collection), the JVL-cloud-as-gateway-to-Incom vs POS-direct-to-Incom debate (Pavel prefers direct so it works if cloud is down, cloud = lease/rights server), the full-insert attendant/privilege card provision (make the housing opening now even if plugged for MVP; lanyard-inserted card auto-locks on removal), and the big capability↔feature↔story alignment doctrine (wedge a "capability" level between product and feature in Jira; features close weekly via a GitHub feature branch → main; free Pavel from acting as developer administrator) — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. September-1 non-market priority order: setup → authenticate → redeem gift card → reports → lease termination. Undertaking: Nathan/Pavel complete electro-mechanical (functional/use-case) requirements as first priority and hold an Incom discovery call with John on Monday. Fourth in the June Tito/Mother-Goose arc.

## Sources

- [[raw/review_flex-POS_use_cases.md]]
