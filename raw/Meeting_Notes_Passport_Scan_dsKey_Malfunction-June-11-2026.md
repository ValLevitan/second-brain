# Meeting Summary — Passport Scan / dsKey Malfunction
**Date:** June 11, 2026, ~10:49 AM Eastern
**Duration:** ~11 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Dzmitry Chudzinau (Minsk side; Felipe Miranda Giorgi and Elizabeth Palomino were not on this call)
**Language:** Russian

## Summary

Val read his own framing of the dispute back to the team to confirm he had it right: after the software upgrade, scanning the machine passport returns "dsKey not registered" and blocks the machine. Minsk believes the Dallas chip was replaced, so the block is correct; Felipe shows the Dallas was never replaced, so the upgrade is misbehaving. The team agreed that is the correct framing.

Val said he trusts Felipe's judgment and doubts a Dallas was actually reused, especially twice, since everyone knows reuse is not allowed and will not work; he suspects the fault is in the software update. Dzmitry pushed back: reusing old passports and Dallas chips does happen in the field, fairly often, though the reason is unknown. He pointed to an older thread Sergey raised about passport/database help, but admitted the team never got to the bottom of it before; it somehow started working and no conclusion was drawn. Dzmitry also said he has very little data and does not know which chips are involved. Val stayed skeptical that reuse is the cause.

Pavel proposed the way to settle it: read the actual Dallas number from the machine's logs and compare it against what the system's generated registration record says. If they do not match, the problem is on the software side. Val then gave Dzmitry direct feedback on communication: his answers are too clipped, with no direction and no guidance, leaving the field people like "deer in the headlights." Plain written English, an acknowledgment, and a clear next step are expected. Val closed on the point that this is not about who is right; machines down cost money, and the goal is to find the root cause and close it for good. He took ownership of writing the direction and posting it in the Teams chat.

## Decisions Made

- **Settle it with data, not argument:** compare the Dallas number encoded in the system-generated registration record against the actual Dallas number read from the machine's logs. (Decided by Val; method proposed by Pavel.)
- **Val writes and posts the English directional message** in the group Teams chat. (Val.)
- **Minsk decodes the registration record on their own side;** from the field they only need the logs. (Pavel, Irina.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Post the English directional message in the group Teams chat; set the compare-both-sides plan and ask the field for logs | June 11, 2026 | High | Unblocks the investigation; machines are down |
| 2 | Pavel / Minsk | Pull the registration record generated for the affected machines and decode the Dallas number encoded in it | TBD | High | One half of the comparison |
| 3 | Felipe / Elizabeth | Collect logs from machines 229918 and 230217 to read the actual Dallas number in each machine now; send to Minsk | TBD | High | Other half of the comparison (external, not on this call) |
| 4 | Dzmitry | Support the field in plain written English: acknowledge, give direction and a clear next step, not one-line answers | Ongoing | Normal | Val's explicit coaching; stop the "who's right" standoff |

## Open Questions

- Is there any real business reason the field would reuse or swap Dallas chips? Raised by Val; unresolved. Dzmitry says it happens but could not show why or with what data.
- What did the older Sergey passport/database thread actually conclude? Never resolved; may hold context.

---
*Processed from Teams transcript on June 11, 2026.*
*Source meeting: Passport_scan_mulfunction (June 11, 2026).*
