---
type: meeting
title: Recycler Architecture Planning — Requirements, Scope, Acceptance (Apr 28 2026)
date: 2026-04-28
aliases: [Recycler Requirements Scope Acceptance, Flex-Recycler architecture planning, Flex Recycler REQ series, bill recycler integration, GVL API]
source-count: 2
---

# Recycler Architecture Planning — Requirements, Scope, Acceptance (Apr 28 2026)

**Date:** 28 April 2026, 1:04pm Eastern (§11 recording header time); ~1h 12m.
**Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratko]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/irina-shishko.md|Irina Shishko]].

The first of the Apr-28→30 Flex-Recycler REQ working sessions: how to architect, scope, and staff the bill-recycler product (on the Rockchip RK3568 platform) and how to write requirements/acceptance criteria for it. Val opened intending to hand an integration contract to [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], but a mid-meeting discovery — the recycler vendor supplies a ready-made 2025 Java library (confirmed live on the vendor's GitHub) — removed the byte-level protocol work and, with it, Alekseev's role. The team then aligned on a new Flex_Recycler repo (assembled from FlexPay/FlexDispenser parts, not forked), reuse of the depopulated gaming-machine IO board, a Java "GVL API" interface with a not-implemented stub, shipping one of the two paid-for recycler samples to Minsk, and CI/CD + acceptance tests from day one. Substance and citations live on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Apr 28 2026 section). §15.8: machine/component/logistics economics only (e.g. ~$30 IO-board saving from FRAM depopulation); no named-person compensation. [[raw/Meeting_Notes_recycler_architecture_planning-April-28-2026.md]]

## Sources
- [[raw/Meeting_Transcript_recycler_architecture_planning-April-28-2026.md]]
- [[raw/Meeting_Notes_recycler_architecture_planning-April-28-2026.md]]
