# Meeting Summary — MG>Printer bypassing IQ if IQ is down
**Date:** July 17, 2026, 9:00 AM Eastern
**Duration:** ~62 minutes (transcript runs 00:00:03–01:02:02; recording cuts off mid-discussion)
**Attendees:** Andrei Klimovich, Pavel Frolov, Irina Shishko, Val Levitan (joined ~23 min in)
**Raw transcript:** [[Meeting_Transcript_IQ_Down_Printer_Bypass-July-17-2026]]
**Superseded by:** [[Meeting_Notes_IQ_Down_Printer_Bypass_Complete-July-17-2026]] — the meeting actually ran 2h13m; this note covers only the first ~62 minutes (captured while the meeting was still in progress)

## Summary

*Meeting held in Russian. Setup under discussion: the Flex IQ device sits between the Mutha Goose game controller and the ticket printer at a location.*

**The problem.** Andrei framed the goal: define what happens at a location if Flex IQ goes down for any reason. The location must keep working — every player cashout must at least get confirmation of the withdrawn money. If IQ is down, the printer gets no ticket-print signals. Mutha Goose holds only the last 25 tickets in memory (Irina and Pavel corrected Andrei's "20"), so an outage longer than 25 cashouts starts losing transactions outright.

**Cashier fallback for a dead IQ.** The cashier unplugs IQ and connects Mutha Goose directly to the printer; tickets print again. Once IQ (or a replacement) is back, the cashier presses the reprint button and the last 25 transactions flow into the device. Wires left at the location could get colored tags so the cashier doesn't have to think. Irina flagged the loophole: tickets printed and paid out directly, then the same 25 transactions re-transmitted to IQ, means double payout — noted for separate handling. Side note from Andrei: locations may no longer pay out in merchandise since July 1; lottery tickets and gift cards are still allowed.

**Making the failure visible.** The cashier's main job is selling gas and goods; nobody stares at the IQ screen. Mutha Goose beeps if IQ is unplugged or its Linux is down, but if the IQ program is loaded with the port open and fails internally, there may be no beep. The current "out of service" tilt display is too quiet — agreement to make it red and blinking/pulsing. A silent hardware edge case (torn data wire or burnt port: no beep, no tilt) was judged too narrow to solve now; behavior should be tested later. For remote awareness, Dima and Sergei are already extending terminal statuses beyond online/offline; Pavel believes a Mutha Goose-disconnected state will appear on the dashboard and will confirm.

**Failure scenarios enumerated (Andrei).** 1) IQ fully powered off. 2) IQ running but offline (no internet). 3) IQ running and receiving transactions from Mutha Goose, but redemption fails — INCOMM server unreachable, INCOMM returns an activation error, the location ran out of cards, or the operator is blocked (machines are not blocked in that case; Pavel thinks the "issue card" button disappears on the terminal but is not 100% sure — Andrei will test with an expired license). INCOMM is only contacted when a transaction is attempted, so errors surface at the card-issuance step.

**Deferred redemption proposal (Andrei/Pavel).** When a card cannot be issued right now, give the cashier one button with two exits: (a) void — player takes lottery tickets on the spot; the transaction is marked void in Payment Hub, never goes to INCOMM, and is considered settled between cashier and player; or (b) deferred redemption — the printer prints a stripped bearer ticket (date, time, amount, voucher number only — no confirmation code), the player returns later, the cashier finds the pending transaction by that ID and retries card activation. The ticket must be physically collected at redemption so it can't be claimed twice. Pavel's barcode-on-ticket idea (scan with the built-in reader instead of searching) was liked but shelved: with roughly two weeks to launch, printing is feasible, scanning is not. Economics: lottery-ticket payout gives the player the full sum, card issuance carries an activation fee — so deferred redemption is more profitable for JVL than voiding, and better than pulling IQ out of the chain. Every transaction that reaches IQ must end in one of two exits — sent to INCOMM for card activation, or paid out another way — and hangs in pending until then.

**Val's challenge.** Val joined about 23 minutes in and pressed for the reasoning behind each claim. His position: "either us or Mutha Goose" — a hard boundary. If our service cannot complete a transaction, IQ should simply report "transaction failed" and hand back to the old primitive system, like the current PAX flow: retry validation up to about 3 times, then just print the ticket and let the location settle it; nothing should be held or complicated. Pavel objected that exactly this fallback creates the double-payout case (tickets paid in lottery tickets, then IQ reconnected and reprint pressed). Val also stressed that today JVL is wedging into someone else's working system (Mutha Goose installations); once locations are fully JVL-owned (own machines, wiring, IQ, servers), an IQ failure becomes a service call and other channels (web, mobile apps) could take over payouts.

**Requirements dispute (unresolved).** Andrei: Georgia lottery regulations explicitly let the player claim winnings by debit card or lottery tickets, and the void flow was designed for the player-declines-card scenario. Val: he was present when the requirements were written — there was no choice; all winnings went to lottery tickets, and "void" just means cancel. He allowed it might be a gap ("пробел") worth discussing, though he doesn't see it. Irina suggested the choice may have grown from sub-$5 amounts that cannot be put on a card. The recording ends there, mid-discussion, with no resolution or wrap-up.

## Decisions Made
- **Cashier fallback procedure for a dead IQ stands: switch Mutha Goose directly to the printer, reprint the last transactions, settle with the player, reconnect after repair** — keeps the location running within the 25-ticket memory window. (Decided by Andrei Klimovich, Pavel Frolov, Irina Shishko; ~00:21:43–00:22:47)
- **Barcode/e-ticket scanning idea postponed; only ticket printing fits the ~2-week launch window, and the printed bearer ticket must be collected from the player at redemption** — no time to build scanning; collecting the ticket prevents repeat claims. (Decided by Andrei Klimovich; ~00:12:53–00:13:12)
- **The silent broken-wire/burnt-port failure case is deferred — not solved now, behavior to be tested later** — judged too narrow to dig into before launch. (Decided by Andrei Klimovich with Pavel Frolov; ~00:17:57–00:18:27)
- **The tilt/out-of-service screen must be made attention-grabbing: red, blinking/pulsing** — cashiers busy at the register don't notice the current quiet message. (Decided by Andrei Klimovich and Pavel Frolov; ~00:19:21–00:19:45)

Note: the deferred-redemption proposal itself was NOT decided — Val Levitan challenged it and the meeting cut off unresolved.

## Undertakings
| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Test terminal behavior with an expired license via location settings — verify whether the "issue card" button disappears when the operator is blocked | TBD | Normal | Pavel was not 100% sure the button disappears (~00:13:34–00:14:14) |
| 2 | Andrei Klimovich | Redesign the IQ tilt/out-of-service screen — red, blinking/pulsing, impossible to miss | TBD | Normal | Cashier must notice IQ failure immediately to switch the wiring (~00:19:21–00:19:45) |
| 3 | Pavel Frolov | Confirm with Dima and Sergei that the extended terminal statuses will surface tilt / Mutha Goose-disconnected states on the dashboard | TBD | Normal | JVL must see location failures remotely, ideally before staff calls (~00:19:47–00:20:31) |
| 4 | Andrei Klimovich | Re-check the written requirements and Georgia lottery regulations: is the player's choice between debit card and lottery tickets actually mandated? | TBD | High | Core dispute with Val left unresolved; Andrei said it can be reviewed (~01:00:16–01:01:45) |
| 5 | [Unassigned — needs clarification] | Add an interface button to print a deferred-redemption / receipt-copy ticket (date, time, amount, voucher number) | ~July 31, 2026 ("2 weeks" from meeting; Aug 1 launch on Mutha Goose mentioned) | High | Required for the deferred-redemption flow — but the flow itself is contested by Val and undecided (~00:14:15–00:14:37, 00:10:22–00:11:22) |
| 6 | [Unassigned — needs clarification] | Test IQ/Mutha Goose behavior when a data (TX) wire is torn or a port burns out — silent failure with no beep and possibly no tilt | TBD (explicitly "in the future") | Low | Deferred edge case; Pavel unsure whether a tilt appears (~00:16:45–00:18:27) |

## Open Questions
- How does reconciliation work when more than 25 transactions accumulate while IQ is down? The excess cannot be recovered from Mutha Goose memory. (Raised by Andrei Klimovich, ~00:22:48–00:23:03)
- Double-payout loophole: tickets printed and paid out directly via Mutha Goose, then the same transactions re-sent to IQ on reconnect/reprint. Flagged for separate discussion, never resolved. (Raised by Irina Shishko ~00:02:56; re-raised by Pavel Frolov ~00:33:28)
- Does the deferred-redemption proposal proceed at all? Val's position is "transaction failed → revert to the old system," Andrei/Pavel defend deferred redemption; the recording ends mid-argument. (~00:31:05–01:02:02)
- Should a location stay operational at all when Flex IQ is down, or should the machines be shut off? Andrei says it must keep working; not settled with Val. (Raised by Pavel Frolov, ~00:25:59–00:26:30)
- Was there ever a requirement giving the player a card-vs-lottery-tickets choice, or is it a gap in the requirements? (Dispute between Val Levitan and Andrei Klimovich, ~00:59:33–01:01:45; Irina's $5 hypothesis at ~01:01:48)

## Dispatch Log

---
*Processed from Teams transcript on July 17, 2026, 10:08 AM Eastern (automated meeting-watcher run)*
*Source meeting: MG>Printer bypassing IQ if IQ is down*