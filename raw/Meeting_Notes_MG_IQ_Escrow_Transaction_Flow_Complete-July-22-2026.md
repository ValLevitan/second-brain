# Meeting Summary — MG<->IQ escrow?
**Date:** July 22, 2026, 9:31–10:12 AM Eastern
**Duration:** ~41 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Pavel Frolov, Dzmitry Chudzinau
**Raw transcript:** [[Meeting_Transcript_MG_IQ_Escrow_Transaction_Flow_Complete-July-22-2026]]
**Supersedes:** [[Meeting_Notes_MG_IQ_Escrow_Transaction_Flow-July-22-2026]] — that note was captured mid-meeting and covers only the first ~31 minutes.

## Summary

Meeting held in Russian, organized by Andrei. Topic: how FlexIQ integrates into existing locations running MutaGoose (MG) without breaking location operations and while minimizing JVL's liability. The trigger was Dzmitry's chat scenario: if an IQ is pulled from a location, local MG transactions could remain on it.

**Escrow question — answered no.** Andrei asked whether MG could act as a kind of escrow: hold a cash-out transaction, pass IQ only the voucher number, machine number, and win amount; IQ shows it to the cashier and reports back on completion. Pavel's answer was an immediate no — MG has no such capability. Val said he expected that answer.

**Val's framing.** JVL competes with the manual PAX process but is a "guest" in an established business that has run on MG for years. JVL cannot impose its own rules; all transaction processes must start from that reality.

**The agreed flow.** The MG ticket always prints (returning to how it originally worked). The transaction also appears in parallel on IQ. IQ validates through cloud services; only when validation fully passes does it issue a card. Completed card transactions are recorded in the cloud and become part of JVL's reporting. If a card cannot be issued, the customer still has the printed ticket and proceeds by the location's standard path — JVL is not involved. Do not print a second ticket when card issuance fails.

**Store nothing on IQ, know nothing beyond completed transactions.** IQ never stores transactions (transient memory of seconds/minutes at most). All transactions belong to the location and live in the cloud hub, keyed to the location's identifier, regardless of which IQ unit is installed. A broken IQ is simply replaced; a replacement IQ "starts a new life" and JVL knows nothing about what came before — Pavel's suggestion of keeping pending transactions "under the hood" for seamless replacement sync was rejected. JVL records only transactions that completed with an issued card; everything else JVL deliberately "doesn't know" — liability protection ("we are in the banking business"). Example report to a location: "You issued $100,000 in payouts; we made card transactions for $25,000; we have no idea about the rest."

**Commissioning.** There is no decommissioning process. An IQ is commissioned to exactly one location and can never move; if it ever connects from another location, it is no longer commissioned. Today commissioning is a manual dashboard procedure done on JVL's behalf (e.g., by Andrei or Filipp); likely automated to some degree later. Pavel flagged that detecting a location change is unsolved post-MVP: GPS won't work indoors and the external IP address is unreliable.

**Dashboard visibility.** The master operator (business owner) sees only validated transactions with issued cards — no pending/live state. Val's strategy: when operators ask for more visibility, JVL offers free SMIB/port infrastructure, which enables extra capabilities on JVL's own network — "that's the hook."

**MG reports and the printer.** With tickets always printing, JVL sits in parallel — signals pass through as if JVL doesn't exist (technically IQ is inline, but process-wise and legally it is parallel). The printer prints all MG transactions, MG can reconcile its own tickets, and cashier-initiated MG reports are unaffected.

**Two MG + two IQ per location** (Dzmitry): theoretically possible (MG supports up to ~128 machines per spec) but no one sees a real use; one unit is cheaper.

**Above-limit cash-outs — resolved by not taking them.** The card cap is $1,000 (InComm limit). Splitting a payout into multiple cards (e.g., $2,500 = $1,000 + $1,000 + $500 against one MG voucher) was discussed, but partial failure kills it: if 2 of 3 cards issue and the third fails (cards run out, InComm down), MG's printer still shows the full $2,500. Resolution: a cash-out exceeding the one-card limit is not processed at all — IQ does not show it and does not light the card button. Dzmitry: better not to get entangled — it makes JVL dependent on InComm. Same for cash-outs below the card minimum (Andrei cited $5; Val said anything under $7): passed through, not shown on IQ. Andrei will consult Juan and press PAX's people (Alan and team, who have ignored the question so far) on how PAX handles above-limit payouts; the question stays open until today's PAX cycle is understood.

**Requirements are living.** Val fixed the agreement as of today's date (July 22, 2026): if JVL's competitive position advances, capabilities change or requirements are added. Requirements are "a living creature."

**SMIB status.** Development was stopped at some point and only needs a go-ahead to resume. Val hoped for delivery in about a month; Pavel estimates closer to 3 months. Val was enthusiastic about restarting it.

**August 1 launch — LTE only.** All IQs at all locations connect via LTE; no LAN cabling. SIMs: buy retail cards (prepaid is fine — avoids contract-approval steps); Val accepted after initially questioning why not a regular plan. On tariffs, Val shut down the optimization discussion: ~$50/month unlimited is immaterial at beta scale (~10 locations, then 20–50); engineering time costs more than the savings. No log/traffic optimization work now — revisit when there are ~1,000 locations.

**Capabilities rework.** Rather than reworking the capabilities created earlier, Dzmitry will create a new capability reflecting today's agreed flow for the current stage. Val cautioned against rushing into a mess: take a day, clean up, think it through.

**Val's standing instruction:** do not hold meetings of this kind without him — he wants to be present at every one.

## Decisions Made

- **MG escrow mode is off the table** — MG cannot hold transactions in escrow. (Confirmed by Pavel)
- **Tickets always print; IQ runs in parallel** — IQ validates through the cloud and issues a card only after full validation; no second ticket is printed on card failure. (Decided by Val, agreed by Andrei and Pavel)
- **JVL stores only completed card-issued transactions, in the cloud, keyed to the location** — nothing is stored on IQ; a replacement IQ starts a new life with no history; deliberate liability protection. (Decided by Val)
- **No decommissioning process** — an IQ is commissioned to one location forever; if moved, it is simply no longer commissioned. (Decided by Val)
- **Master operator dashboard shows only validated card-issued transactions** — no pending state. (Decided by Val)
- **Cash-outs above the one-card limit ($1,000) are not processed at all** — not shown on IQ, card button not lit; supersedes the split-into-multiple-cards idea discussed earlier in the meeting. Pending sanity-check with Juan and PAX practice. (Decided by Val, Andrei, Dzmitry)
- **Cash-outs below the card minimum ($5–7) are likewise not shown or processed on IQ.** (Agreed by Andrei and Val)
- **The agreed scope is fixed as of July 22, 2026** — requirements are living and will change if JVL's competitive position changes. (Decided by Val)
- **SMIB development gets the go-ahead to resume** — estimate ~3 months (Pavel; Val hoped ~1). (Endorsed by Val)
- **August 1 launch: all IQs on LTE** — retail SIMs, unlimited plan; no traffic/tariff optimization at beta scale. (Decided by Val and Andrei)
- **A new capability will be written for the current stage** instead of reworking the earlier ones. (Agreed by Andrei and Dzmitry)
- **No more meetings of this kind without Val present.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei (with Pavel/Dzmitry) | Pick the precise term for a transaction that ends without a card ("void" rejected — implies JVL acted; "cancel"/"abort" candidates) and be pedantic that the wording implies no JVL responsibility | TBD | Normal | "Подберем" — Andrei; Val: "будьте очень педанны к подбору этого слова" |
| 2 | Andrei | Consult Juan on the above-limit rule and persistently press Alan and team on how PAX handles payouts above the per-card limit — they have ignored the question so far | TBD | High | Val: "давайте настырно проработаем это"; the above-limit rule stays open until answered |
| 3 | Dzmitry | Create a new capability covering today's agreed transaction flow for the current stage (instead of reworking the earlier capabilities), taking a day to clean up and think it through | TBD | High | "Сделаю новую"; Val: "давайте мы возьмём день, почистим, задумаемся" |
| 4 | Pavel | Resume SMIB development now that the go-ahead was given; delivery estimate ~3 months | TBD | Normal | "Просто надо дать отмашку"; Val: "очень, очень классно" |

## Open Questions

- How PAX handles cash-outs above the per-card limit — Alan and team have not answered; the no-processing rule stays provisional until today's PAX cycle is understood. (Raised by Val and Andrei)
- How to detect that an IQ changed location post-MVP — GPS won't work indoors, external IP is unreliable. (Raised by Pavel)

## Dispatch Log

---
*Processed from Teams transcript on July 22, 2026, ~12:05 PM Eastern (scheduled watcher run — complete recapture; the 10:07 AM capture had used a mid-meeting transcript)*
*Source meeting: MG<->IQ escrow?*