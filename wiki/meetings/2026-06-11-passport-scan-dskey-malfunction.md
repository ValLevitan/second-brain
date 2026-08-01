---
type: meeting
title: Passport scan / dsKey malfunction (June 11 2026)
date: 2026-06-11
aliases: [Passport Scan dsKey Malfunction, dsKey not registered, Dallas chip registration dispute, passport scan blocks machine]
source-count: 1
---

# Passport scan / dsKey malfunction (June 11 2026)

**June 11, 2026, ~10:49 AM ET · ~11 min.** Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dzmitry Chudzinau]] (Minsk side). The Georgia field parties [[wiki/people/felipe-miranda.md|Felipe Miranda]] and [[wiki/people/elizabeth.md|Elizabeth]] (surname Palomino, per this source) were referenced but not on this call. Russian.

A short call on a Georgia field incident: after a software upgrade, scanning a machine's passport returns **"dsKey not registered"** and blocks the machine. Val read his own framing of the dispute back to the team to confirm it — Minsk believes a Dallas chip was replaced so the block is correct, while Felipe shows the Dallas was never replaced so the upgrade is misbehaving — and the team agreed that framing is right. The agreed way to settle it: compare the Dallas number encoded in the system-generated registration record against the actual Dallas number read from the affected machines' logs.

Durable substance — the incident itself, the reuse-vs-software-bug dispute, and the resolution ownership (Val to write and post the English directional message; Minsk decodes the registration record; the field pulls logs from machines 229918 and 230217) — lives on [[wiki/projects/georgia-market-rollout.md]] (Jun-11). The device-registration mechanism it turns on — the Dallas number is encoded in the generated registration record and can be decoded and compared against the chip in the field — is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jun-11).

## Sources
- [[raw/Meeting_Notes_Passport_Scan_dsKey_Malfunction-June-11-2026.md]]
