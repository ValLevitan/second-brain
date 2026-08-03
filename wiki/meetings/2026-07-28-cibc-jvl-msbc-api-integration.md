---
type: meeting
title: CIBC / JVL MSBC API Integration (account structure settled, API role scoped)
date: 2026-07-28
aliases: [CIBC JVL MSBC API Integration, CIBC ACH Microsoft Dynamics API Integration]
source-count: 2
---

# CIBC / JVL MSBC API Integration (account structure settled, API role scoped)

**Date:** July 28, 2026, 4:00 PM ET (~13 min).
**Attendees:** Michael Hill (CIBC, external); [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]] (JVL).

A short call to confirm how the new **CIBC account structure** for JVL will work and what role an **API** needs to play (CIBC ↔ Microsoft Business Central). The account structure is now settled — a Zero Balance Account receives batched deposits and sweeps them to a separate account at end of day — and the group scoped the API down to read-only verification. This continues the CIBC banking-setup thread from the [[wiki/meetings/2026-07-02-cibc-business-central-integration.md|Jul-2]] and [[wiki/meetings/2026-07-06-cibc-banking-setup-review.md|Jul-6]] calls. [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]] [[raw/Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]

Substance lives on:
- [[wiki/organizations/cibc.md]] (Jul-28) — the settled ZBA-plus-sweep account structure, the batch-deposit drill-down report, and Michael's setup being ready. [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
- [[wiki/topics/business-central-erp-implementation.md]] (Jul-28) — the read-only API role, the Microsoft Dynamics / Business Net Banking integration, and Val's hunch that the existing CIBC–Dynamics integration may already be the easier path. [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]

## Sources

- [[raw/Meeting_Notes_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
- [[raw/Meeting_Transcript_CIBC_JVL_MSBC_API_Integration-July-28-2026.md]]
