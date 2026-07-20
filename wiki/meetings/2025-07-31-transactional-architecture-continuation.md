---
type: meeting
title: Transactional-architecture continuation — message-queue replication, Tito diagram, tech stack
date: 2025-07-31
aliases: [transactional architecture July 31, message queue replication, Tito diagram, tech stack selection]
source-count: 1
---

# Transactional-architecture continuation (Jul 31 2025)

The Thursday continuation of the [[wiki/meetings/2025-07-29-transactional-architecture-ewallet-deep-dive.md|Jul-29 deep-dive]] (Val had cancelled the Jul-30 mid-iteration sync to make room). [[wiki/people/nathan-carver.md|Nathan Carver]] had added summary docs to the GitHub repo + a Confluence diagram; the group resolved the data-sync approach (**event-driven message-queue replication** over database clustering), made **server-as-installable-software on every main device** a redundancy requirement, set **~7-day local data retention with hourly cloud dump**, butchered the e-wallet diagram into a **Tito diagram**, and named the **tech stack** (Linux / MySQL / Java / React). Attendees: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]].

Full substance on the arc sequencer [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-31 entry). Next: database design + hardware selection with the internal database team.

## Sources
- [[raw/transactional_architecture-july-31-2025.md]]
