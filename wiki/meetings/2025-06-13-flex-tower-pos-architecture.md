---
type: meeting
title: FlexPay system architecture walkthrough — Flex Tower / Flex POS (June 13 2025)
date: 2025-06-13
source-count: 1
---

# FlexPay system architecture walkthrough — Flex Tower / Flex POS (June 13 2025)

Architecture review chaired by [[wiki/people/juan-martinez.md|Juan Martinez]], presented by [[wiki/people/pavel.md|Pavel Frolov]]. Attendees: [[wiki/people/val-levitan.md|Val]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]], [[wiki/people/ihar-hrybko.md|Ihar Hrybko]] ("Igor"). Purpose: agree the FlexPay component architecture and introduce Val's new "offline POS" (POS-non-SAS) idea for Mother-Goose street operators.

Substance — the Flex Tito server as the central brain (secure-WebSocket to every device; all API logic centralised so Tower/POS/SMIB stay "dumb"), the device catalog (Flex SMIB board, Flex Tower kiosk with card dispenser + QR scanner + 5–6" touch + swipe reader, Flex POS cashier terminal with 10" touch + optional 2nd screen), the ARM-Linux-vs-STM split (FlexPort stays STM/"done," Tower is an open choice, POS leans ARM-Linux on a compelling China board), the manual **offline "POS non-SAS"** for operators who keep Mother Goose (manual dollar entry, ~$1/day 3-year lease for exclusivity, printer serial-sniff via dual RS-232), Pavel's fraud concern (cashier could self-issue cards with no cross-check to Mother-Goose cash-out; Incom per-location throttling limits partly mitigate), and the 5"-screen legibility worry driving Hrybko's Figma prototype — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Undertaking: Hrybko to build an interactive player-side Flex Tower prototype for a combined June-19/20 (Friday 6am) sizing review; Juan/Felipe expedite persona use cases; Nathan bridges use-cases→capabilities→features into GitHub. Third in the June Tito/Mother-Goose arc (June-11 → **June-13** → June-19/20 → June-27).

## Sources

- [[raw/Flex-Tower _POS - Architecture.md]]
