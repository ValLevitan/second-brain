---
type: meeting
title: Embedded group — FlexPort/FlexPay debug
date: 2025-03-25
aliases: [embedded group March 25, FlexPort FlexPay March 25]
source-count: 1
---

# Embedded group — FlexPort/FlexPay debug (Mar 25 2025)

**Attendees:** [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (Zhenya, now full-time), [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], the backend "Dima" ([[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — transcript names "Чудинов"), and [[wiki/people/genadi-peari.md|Genadi Peari]] (joined late). Opened in Polish/Russian.

**Purpose:** status on the FlexPort↔FlexPay integration bring-up and Val's push to work it live.

Substance lives on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]:
- Cash-out now works **only once** per ticket (money removed from the gaming machine but not re-credited to the ticket on repeat attempts).
- FlexPort still **hangs**; suspected cause is **simultaneous ping/pong message collision** in the async loop; fix idea = queue/pool outgoing messages.
- Val wants **live daily/weekly working meetings** before the April expo instead of async chat; Yavorski (full-time) and Chudinov to pair on logs.
- Genadi raised a **QR-scanner motion-detection** quirk (only scans when it detects movement).

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
