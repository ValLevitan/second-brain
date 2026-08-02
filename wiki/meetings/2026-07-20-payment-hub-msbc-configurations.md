---
type: meeting
title: Payment Hub MSBC Configurations (July 20 2026)
date: 2026-07-20
aliases: [Payment Hub MSBC Configurations, Payment Hub Business Central config, G1 G2 dimension codes, COD payment terms Payment Hub]
source-count: 2
---

# Payment Hub MSBC Configurations (July 20 2026)

**Date:** July 20, 2026, 2:07–2:40 PM ET (~34 min)
**Attendees:** [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/sean-riley.md|Sean Riley]], [[wiki/people/lev-rudky.md|Lev Rudky]] ([[wiki/people/val-levitan.md|Val Levitan]] attended but did not speak).

The team reviewed how **Payment Hub** transactions should be configured in **Microsoft Business Central (MSBC)** before moving to production — the cash-flow **dimension codes** (G1 = 0107 "services rendered" on revenue lines; G2 intercompany = 0, since all Payment Hub business is with third parties), **AvaTax** with every line item non-taxable (COAM customers set tax exempt), **COD** payment terms (not Net 7), and confirmation that a posted invoice's GL entries match Igor's mapping. [[raw/Meeting_Notes_Payment_Hub_MSBC_Configurations-July-20-2026.md]] [[raw/Meeting_Transcript_Payment_Hub_MSBC_Configurations-July-20-2026.md]] Nathan will generate a full example cycle (invoice through posting) in the staging environment for the team to approve. This links back to the [[wiki/meetings/2026-05-12-payment-hub-gl-sales-tax.md|May-12 Payment Hub GL / sales-tax meeting]]. [[raw/Meeting_Notes_Payment_Hub_MSBC_Configurations-July-20-2026.md]]

Substance → [[wiki/topics/business-central-erp-implementation.md]] (July-20 section — BC config, dimension codes, GL mapping, COD terms) and [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (July-20 section — Payment Hub).

## Sources
- [[raw/Meeting_Notes_Payment_Hub_MSBC_Configurations-July-20-2026.md]]
- [[raw/Meeting_Transcript_Payment_Hub_MSBC_Configurations-July-20-2026.md]]
