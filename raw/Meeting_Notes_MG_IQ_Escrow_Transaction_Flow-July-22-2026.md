# Meeting Summary — MG<->IQ escrow?
**Date:** July 22, 2026, ~9:00–9:31 AM Eastern
**Duration:** ~31 minutes (recording appears to cut off mid-discussion)
**Attendees:** Val Levitan, Andrei Klimovich, Pavel Frolov, Dzmitry Chudzinau
**Raw transcript:** [[Meeting_Transcript_MG_IQ_Escrow_Transaction_Flow-July-22-2026]]

## Summary

Meeting held in Russian, organized by Andrei. Topic: how FlexIQ integrates into existing locations that run MutaGoose (MG), without breaking location operations and while minimizing JVL's liability. The trigger was a scenario Dzmitry raised in chat: if an IQ is pulled from a location, local MG transactions could remain on it.

**Escrow question — answered no.** Andrei asked whether MG could act as a kind of escrow: hold a cash-out transaction, pass IQ only the voucher number, machine number, and win amount; IQ shows it to the cashier and reports back on completion. Pavel's answer was an immediate no — MG has no such capability. Val said he expected that answer.

**Val's framing.** JVL competes with the manual PAX process, but is a "guest" in an established business that has run on MG for years. JVL cannot impose its own rules; all transaction processes must start from that reality.

**The agreed flow.** The MG ticket always prints (returning to how it originally worked). The transaction also appears in parallel on IQ. IQ validates the transaction through cloud services; only when validation fully passes does it issue a card. Completed card transactions are recorded in the cloud and become part of JVL's reporting. If a card cannot be issued, the customer still has the printed ticket and proceeds by the location's standard path — JVL is not involved. Do not print a second ticket when card issuance fails.

**Store nothing on IQ, know nothing beyond completed transactions.** IQ never stores transactions (transient memory of seconds/minutes at most). All transactions belong to the location and live in the cloud hub, keyed to the location's identifier, regardless of which IQ unit is installed. A broken IQ is simply replaced. JVL records only transactions that completed with an issued card; everything else JVL "doesn't know" — Val stressed this is deliberate liability protection ("we are in the banking business"). He warned the team not to be drawn into tracking anything more. Example report to a location: "You issued $100,000 in payouts; we made card transactions for $25,000; we have no idea about the rest."

**Commissioning.** There is no decommissioning process. An IQ is commissioned to exactly one location and can never move; if it ever connects from another location, it is no longer commissioned. Today commissioning is a manual dashboard procedure done on JVL's behalf (e.g., by Andrei or Filipp); it will likely be automated to some degree later. Pavel flagged that detecting a location change is unsolved post-MVP: GPS won't work indoors and the external IP address is unreliable.

**Dashboard visibility.** The master operator (business owner) sees only validated transactions with issued cards — no pending/live state. Val's strategy: when operators ask for more visibility, JVL offers free SMIB/port infrastructure, which enables extra capabilities on JVL's own network — "that's the hook." Pavel suggested pending transactions could still remain "under the hood" (not displayed) to allow seamless IQ replacement sync from the cloud; Andrei and Val held that a replacement IQ starts a new life and JVL knows nothing about what came before.

**MG reports and the printer.** With tickets always printing, JVL sits in parallel — signals pass through as if JVL doesn't exist. The printer prints all MG transactions and MG can reconcile its own tickets. Cashier-initiated MG reports are unaffected.

**Two MG + two IQ per location** (Dzmitry): theoretically possible (MG supports up to ~128 machines per spec) but no one sees a real use; one unit is cheaper.

**Max card cap ($1,000).** Agreed (consistent with the earlier chat with Juan): a payout above the cap splits into multiple cards — e.g., $2,500 becomes $1,000 + $1,000 + $500, recorded together against the single MG voucher (e.g., voucher #77). Partial failure is an open problem: if 2 of 3 cards issue and the third fails (cards run out, InComm service down), MG's printer still shows the full $2,500. Val: "an interesting problem, I don't know how to handle it yet." The recording cuts off mid-discussion of this case.

## Decisions Made

- **MG escrow mode is off the table** — MG cannot hold transactions in escrow. (Confirmed by Pavel)
- **Tickets always print; IQ runs in parallel** — IQ validates through the cloud and issues a card only after full validation; no second ticket is printed on card failure. (Decided by Val, agreed by Andrei and Pavel)
- **JVL stores only completed card-issued transactions, in the cloud, keyed to the location** — nothing is stored on IQ, and JVL keeps no knowledge of any other transactions, as deliberate liability protection. (Decided by Val)
- **No decommissioning process** — an IQ is commissioned to one location forever; if moved, it is simply no longer commissioned. (Decided by Val)
- **Master operator dashboard shows only validated card-issued transactions** — no pending state. (Decided by Val)
- **Payouts above the $1,000 card cap split into multiple cards** recorded together against the one MG voucher. (Agreed by Val and Andrei)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei (with Pavel/Dzmitry) | Pick the precise term for a transaction that ends without a card ("void" rejected — implies JVL acted; "cancel"/"abort" candidates) and be pedantic that the wording implies no JVL responsibility | TBD | Normal | "Подберем" — Andrei; Val: "будьте очень педанны к подбору этого слова" |

## Open Questions

- How to handle partial failure of a split payout (e.g., 2 of 3 cards issued on a $2,500 voucher while MG's printer shows the full amount) — Val: "I don't know how to handle it yet." Recording ended mid-discussion. (Raised by Andrei)
- How to detect that an IQ changed location post-MVP — GPS won't work indoors, external IP is unreliable. (Raised by Pavel)
- Whether pending transactions may quietly persist "under the hood" to support seamless IQ replacement sync, given the store-nothing stance. (Raised by Pavel and Dzmitry)

## Dispatch Log

---
*Processed from Teams transcript on July 22, 2026, 10:07 AM Eastern (scheduled watcher run)*
*Source meeting: MG<->IQ escrow?*
