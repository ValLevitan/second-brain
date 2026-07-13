---
type: meeting
title: Embedded group — FlexPort ↔ FlexPay integration standup
date: 2025-02-11
aliases: [Embedded group alignment, FlexPort FlexPay standup]
source-count: 1
---

# Embedded group — FlexPort ↔ FlexPay integration standup

~21-min embedded/hardware engineering standup (Polish + Russian) on wiring the **FlexPort** machine module to the **FlexPay** kiosk. Recurring group; substance folded into [[wiki/topics/jvl-machine-lineup.md]] (FlexPort/FlexPay) and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]].

- Attendees: Val, [[wiki/people/genadi-peari.md|Gennady]] ("Gena"), a "Dima" (identity unclear — see Owner Decisions), "Andrei", and engineers "Evgeny"/"Eugenia" (transcribed). [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- Durable points: get FlexPay running in the engineers' environment, then connect the test program over **WebSocket** (a handshake returning 200 vs. the expected 101 upgrade suggests the test-utility, not necessarily JVL's low-level code, is the limit — must retest with a real FlexPay kiosk). Logic agreed: the machine **accepts no money/tickets until the device registers with FlexPay**; cash-out only via FlexPay; PIN/ticket errors and a bad-PIN lockout (block a ticket ~15 min after too many PIN attempts, handled FlexPay-side later). Blocked on chips arriving. Production shipment likely needs ~1 more week after FlexPay comes up. [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- **Incom** — the payment processor whose **test server** JVL currently uses; a production **contract** was received (Fri) and Val must read/sign it before going to production. [[wiki/people/felipe-miranda.md|Felipe]] ("Filippo") to host a multi-machine FlexPay+kiosk production test in his office. (Incom and the Felipe/Filippo identity flagged in Owner Decisions.) [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
