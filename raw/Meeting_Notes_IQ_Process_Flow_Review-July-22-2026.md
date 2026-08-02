# Meeting Summary — IQ Process flow update
**Date:** July 22, 2026, 5:00–5:59 PM Eastern
**Duration:** ~58 minutes
**Attendees:** Val Levitan, Juan Martinez, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_IQ_Process_Flow_Review-July-22-2026]]

## Summary

Juan walked through the new Flex-IQ process flow (built from the morning call with Pavel, architected by Val) and raised his concerns point by point. The context is gift card payouts for Georgia COAM locations, where the Mother Goose (MG) system prints the payout ticket.

Points Juan accepted: MG always prints the ticket and IQ does not suppress or intercept it — the location keeps its existing paper process. If a card fails to validate, nothing happens; the failed transaction does not affect the location's normal workflow. The team confirmed "failed" (not "voided") is the term. Business Central posting is unaffected because Nathan's money flow only ever depended on successful transactions.

The main dispute: the current design records only successful (validated) transactions in the cloud and keeps no memory of anything else. Juan pushed back with real edge cases — a location that can't pay a large win on the spot and asks the player to return, an IQ unit dying with pending transactions on it (they exist only locally, so a replacement unit loses them), and partial redemptions where a $2,500 ticket is only partly paid before cards run out. His concerns: no way to pay the player later in the JVL ecosystem (manual entry is not allowed), theft risk on unresolved fractional balances, and locations demanding a PAX backup device, which costs JVL its $2 per-transaction fee. Juan proposed temporarily storing open transactions in the cloud (e.g., 3–5 days) and allowing manual entry under an administrator PIN controlled by the master. Andrei objected that manual entry destroys the "fully automated" advantage over PAX; Juan countered that masters can simply refuse to support the feature. Val explained his reasoning for eliminating memory: with IQ wedged as a guest into someone else's network, keeping partial data invites scenarios JVL can't resolve, while a memory-less design pushes operators toward JVL's future end-to-end network (free SMIBs replacing Mother Goose), where full memory and rich capabilities become possible. Val acknowledged he has swung "like a pendulum" between always-print/never-print and keep/don't-keep positions, said the prepaid MasterCard concept looks unrealistic on the street (players want cash; cards enable a gray market), and conceded there is no technical barrier to keeping data — the question is whether his no-memory assumption was wrong. Juan sees PAX as the true competitor and noted there is value in keeping cloud data at least until bugs are ironed out.

Other points: transactions under $7 are ignored, but the cashier needs a UI/UX notification telling her the ticket must be handled another way (same for over-$1,000). On wins over $1,000, splitting across multiple cards works until cards run out, leaving a fractional remainder — unresolved. Device commissioning: one IQ per location; when a new device is commissioned at a location, the old one is automatically decommissioned (no manual decommission step), with InComm notified automatically. Juan's technician-swap concern was resolved because commissioning always goes through InComm; a possible multi-device-per-location cap (3–5) was floated by Val for later thought.

No decisions were forced. Val was tired and asked to think it through overnight; the group scheduled a follow-up brainstorming session for tomorrow (July 23) at 8:30 AM, and Juan sent the invite during the call.

## Decisions Made

- **"Failed" is the term for unsuccessful transactions, not "voided"** — void was already abandoned. (Decided by Val, Andrei)
- **MG always prints the paper ticket; IQ does not suppress or intercept it** — keeps the location's existing process intact; card issuance is a separate cashier-initiated step. (Confirmed by Juan, Val)
- **Device decommissioning is automatic** — commissioning a new device at a location decommissions the old one (one-device-per-location rule); InComm gets notified automatically; no manual decommission process. (Agreed by Val, Juan)
- **Sub-$7 intercepts are ignored, but a cashier notification is required** — UI/UX must alert the cashier that the ticket must be processed another way. (Agreed by Juan, Andrei)
- **Defer the core dispute overnight** — whether to store pending transactions in the cloud and whether to allow manual ticket entry; reconvene tomorrow 8:30 AM. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Think through overnight whether to keep pending-transaction memory in the cloud and whether manual ticket entry should be allowed; bring a position to the 8:30 AM session | July 23, 2026 | High | Val: "I just want to think it through overnight and let's try it again tomorrow" |
| 2 | Juan | Send calendar invite for the follow-up brainstorming session at 8:30 AM tomorrow | July 22, 2026 | Normal | Done during the call ("Invite just sent") |
| 3 | Juan | Think further about the manual-entry / delayed-payout edge case | July 23, 2026 | Normal | "I'm gonna think about it a little bit more" |
| 4 | Juan | Share this meeting's transcript with Andrei when it is ready | July 23, 2026 | Low | Andrei asked for it at the end of the call |
| 5 | Val | Drill down with the team into the original concerns about temporarily storing transactions in the cloud | TBD | Normal | Juan asked; Val agreed ("Sure") |

## Open Questions

- Should pending (unfinished) transactions be stored temporarily in the cloud (e.g., 3–5 days), so they survive a dead IQ unit? (Raised by Juan; Val reconsidering)
- Should manual ticket entry be allowed under an administrator PIN held by the master? (Raised by Juan; Andrei opposed; undecided)
- How to handle wins over $1,000 — card splitting leaves fractional remainders when cards run out; partial redemption has theft risk. (Raised by Juan)
- Always print vs. never print the ticket — is the always-print position (least footprint in the location's network) the right one? (Val questioning his own switch)
- What were the original three-to-five scenarios that led Val to eliminate the memory component? (To be revisited with the team)

## Dispatch Log

## Notes

- "income"/"Incon" in the transcript refers to InComm; "packs" refers to PAX; "Mutagus"/"MG Oil" refer to Mother Goose.

---
*Processed from Teams transcript on July 22, 2026, 6:05 PM Eastern (scheduled watcher run)*
*Source meeting: IQ Process flow update*
