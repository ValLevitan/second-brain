---
type: meeting
title: Flex-POS iteration planning (Jul 14 2025) — spike to dump ticket data
date: 2025-07-14
aliases: [Flex-POS Iteration Planning 2025-07-14]
source-count: 1
---

# Flex-POS iteration planning — July 14 2025

Short planning call. Attendees: [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/juan-martinez.md|Juan Martinez]] (joined briefly, dropped on arriving at a casino). Purpose: fold Jim/[[wiki/organizations/rks.md|RKS]] feedback into the iteration and green-light [[wiki/people/pavel.md|Pavel]]'s **spike** to connect a real printer and dump all ticket data.

Substance on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Key points: Jim confirmed the confidence number is a **hash of the whole ticket data** and print signals are **all ASCII**; Pavel will connect the real printer and dump data (read-only, no reprint from POS at this stage); requirement docs (FR 1.1 intercept print data, F 1.2 store complete ticket metadata) move from Confluence to Jira, with **GitHub as the source of truth** per Val's push away from Atlassian.

## Sources

- [[raw/Flex-POS Iteration Planning 2025-07-14.md]]
