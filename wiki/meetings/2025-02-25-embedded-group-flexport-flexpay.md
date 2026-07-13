---
type: meeting
title: Embedded group — FlexPort/FlexPay connection debugging & cash-out edge case
date: 2025-02-25
aliases: [embedded group Feb 25, FlexPay alignment Feb 25]
source-count: 1
---

# Embedded group — FlexPort/FlexPay (Feb 25 2025)

~23-min embedded-group standup (Russian). Attendees: [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]] ("Pasha"), [[wiki/people/eugine-yavorski.md|Evgeny]] ("Женя"), [[wiki/people/genadi-peari.md|Genadi]]; "Dima" (software, unattributed) referenced. Purpose: debug the dropped WebSocket connection and settle cash-out handling before shipping. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

Substance lives on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]] (FlexPort↔FlexPay integration) and [[wiki/topics/jvl-machine-lineup.md]]:
- Connection **drops despite a 1-second ping-pong** — cause not found; JVL side to investigate; pings not appearing in the logs.
- **Cash-out-and-walk-away** ruling (Val): cancel the ticket as "not claimed," pull credits off the machine, report to FlexPay; restore the money on paper via FlexPay during audit if the player returns and enters a PIN. Needs a new **informational protocol command** for abnormal states (device failure, not-claimed funds).
- **Logging is to be a requirement:** an enable-able detailed-log mode for the comms protocol (as with Bally/Konami AFT).
- **Config:** ~4 machines per FlexPay; ship 4 FlexPay + ~15 ports; FlexPort goes into JVL's own machines too (Val's uniformity requirement). Genadi's config + a working protocol targeted for **Thursday**; finish the hard-to-start machine then do a full firmware update.

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
