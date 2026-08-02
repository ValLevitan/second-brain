# Meeting Summary — virtual_walk_through_alpha_test-Flex-IQ
**Date:** July 15, 2026, 3:15 PM – 3:35 PM Eastern
**Duration:** ~15 minutes
**Attendees:** Andrei Klimovich, Val Levitan
**Raw transcript:** [[Meeting_Transcript_FlexIQ_Alpha_Test_Walkthrough-July-15-2026]]

## Summary

Andrei gave Val a virtual walkthrough of the Flex-IQ alpha test setup at the GA office showroom. The demo rig sits on one small table: printer, Mutha Goose, and the Flex-IQ unit. The stage runs on a test environment (sandbox); a production location will be added after Income validates them, to test invoicing end to end.

The demo covered the full cashout flow. Cashier logs in with a PIN and sees a pending-transactions desktop. Andrei played a game machine ($64 balance), cashed out $15, and the transaction appeared on the cashier side with timestamp, voucher number, machine number, and correct amount. From pending, the cashier can redeem to a card (player gets $13 of $15; $2 fee) or void. The redeem-to-card demo could not finish because the single test card was already used — cards must be cleared through an online app Dmitry Chudinov is still setting up. Andrei will clear the card and send Val a video of the full redeem flow.

Val asked for two product changes: print a confirmation ticket on the printer when a cashier settles a transaction (currently nothing prints), and rename the harsh "Void" status to something like "Ticket." Andrei agreed on the flow: settle as ticket → print confirmation. Andrei also plans to redo the on-screen cashout wording so the $15 / $13 / $2 fee split is clearer.

For demos to prospects, they agreed on a new layout: printer next to the Flex-IQ on its own, with the Mutha Goose tucked away on a separate table (it is still required — it intercepts the machine-to-printer signal — but the point is to show the location owner a clean setup).

Timeline: per the agreement, Andrei's team has 2 weeks (to ~July 29) to stand up the production server, verify remote software updates over modem (blocked — modems haven't arrived; Andrei asked Mikhail for a tracking link and got no reply yet), and find a location owner willing to be the first beta tester. Beta test at a real location targets August 1, with a contract signed. A draft location contract exists (worked up with Juan); Andrei will send it to Val and Monica in the coming days.

Trial terms discussed: device and setup free for the trial (Val suggested 90 days); the operator still pays all cashout money including the $2 per-transaction fees. Val wants the commercial terms worked out during the next 2 weeks and needs to consult before finalizing.

Val reminded Andrei — firmly, repeatedly — that he must be copied on all communications between Andrei and anyone else: use channels or email, no individual chats without Val.

## Decisions Made

- **Cashier settlement will print a confirmation ticket, and the status label will change from "Void" to something like "Ticket"** — the player needs physical proof the money was processed. (Decided by Val, agreed by Andrei)
- **Demo layout: Flex-IQ + printer standalone; Mutha Goose hidden on a separate table** — show prospects a clean setup while keeping the required signal interception working. (Decided by Val and Andrei)
- **Beta test at a real location targets August 1; production server ready within 2 weeks** — per the existing agreement. (Decided by Val)
- **Trial offer: device and setup free (~90 days proposed); operator pays all cashouts and $2 fees** — exact commercial terms to be finalized within the 2 weeks. (Decided by Val)
- **All of Andrei's communications must include Val** — channels or email instead of individual chats. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Clear the test card and send Val a video of the full redeem-to-card flow | TBD | Normal | Blocked on Dmitry Chudinov finishing the online card-clearing app; Andrei calling him today |
| 2 | Andrei Klimovich | Implement printed confirmation ticket on cashier settlement and change "Void" status wording to "Ticket" | TBD | High | Val: "needs to be done right now" |
| 3 | Andrei Klimovich | Send the draft location contract to Val and Monica | ~July 17, 2026 | High | "In the coming days"; draft prepared with Juan |
| 4 | Andrei Klimovich | Stand up and verify the production server | July 29, 2026 | High | 2 weeks per the agreement |
| 5 | Andrei Klimovich | Verify software updates can be pushed remotely over modem | July 29, 2026 | High | Blocked: modems not arrived; tracking requested from Mikhail |
| 6 | Andrei Klimovich | Find a location owner willing to be the first beta tester, with contract agreed | August 1, 2026 | High | Beta test on location starts Aug 1 |
| 7 | Mikhail | Send Andrei the tracking link for the modems | TBD | Normal | Andrei requested it; no reply yet |
| 8 | Val Levitan | Finalize trial commercial terms (length, pricing after trial) after consulting | July 29, 2026 | Normal | Val wants terms settled within the 2 weeks |

## Open Questions

- Final trial commercial terms — trial length (90 days suggested) and what the operator pays after the trial. Raised by Andrei; Val deferred pending consultation.
- Exact wording for the new settlement status ("Ticket," "Card," or other). Raised by Andrei.

## Dispatch Log

---
*Processed from Teams transcript on July 15, 2026, 6:56 PM Eastern (scheduled watcher run)*
*Source meeting: virtual_walk_through_alpha_test-Flex-IQ (July 15, 2026)*
