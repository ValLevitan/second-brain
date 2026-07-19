---
type: meeting
title: Flex POS implementation planning — September-1 beta roadmap (June 27 2025)
date: 2025-06-27
source-count: 1
---

# Flex POS implementation planning — September-1 beta roadmap (June 27 2025)

Roadmap meeting led by [[wiki/people/nathan-carver.md|Nathan Carver]] with [[wiki/people/juan-martinez.md|Juan Martinez]] (VP Product Owner for FlexPort/related products), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/val-levitan.md|Val]]. Purpose: agree the release roadmap, set a cadence, and pick the first requirements to drive implementation.

Substance — the **September-1 non-market beta** definition (a live Incom test site in JVL's Georgia showroom with three machines — Flex S + IGT + a vanilla machine — all fitted with Mother Goose hardware and a counter printer; play games, trigger a payout, manually pair the printed ticket value to a prepaid MasterCard via the Incom cycle; 3D-printed plastics acceptable), the ARM board just received (a week to validate; Eugeny installs out-of-box software then Minsk integrates Linux boot + Java + browser; Pavel/Dima + GUI from Ihar Hrybko & Anton, ~1 week after PCB), the release cadence (Sept-1 non-market → Sept-15/30 continuous integration → **Nov-1 critical market release** with ~10 installs worst-case → Jan-1 full TITO validation + admin/housekeeping; June-1-2026 regulator cliff drives a last-moment market rush), the card-reader max-config debate (swipe reader always installed for issuing plastic cards, + optional full-insert operator/privilege card, + possible future Incom contactless reader — up to three readers; provision the housing now, PIN vs lanyard-card lock/unlock), and the product-team cadence (Mon/Wed/Fri under 45 min; Belarus holiday shortens the July-4 week; Hrybko presents first UX Wednesday July-2) — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Fifth (latest) in the June Tito/Mother-Goose arc.

## Sources

- [[raw/Flex-POS Implementation Planning.md]]
