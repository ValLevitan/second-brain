# Meeting Summary — Discuss new IQ process flow- Part 2
**Date:** July 23, 2026, 8:38–10:00 AM Eastern
**Duration:** ~1 hour 22 minutes
**Attendees:** Val Levitan, Andrei Klimovich, Juan Martinez
**Raw transcript:** [[Meeting_Transcript_IQ_Process_Flow_Part_2-July-23-2026]]

## Summary

Continuation of the IQ process flow discussion (Part 1 was July 22). Three big topics: IQ memory, the "recorder" device idea, and hand pay for wins over $1,000.

**IQ keeps no memory.** Val's position, accepted by the group: IQ is a "dumb" pass-through terminal — a screen that automates card issuance, nothing more. It holds a transaction only during the validation cycle (about 30 seconds). A transaction ends in one of two states: validated or failed. Only card-issued transactions are recorded in the Payment Hub cloud, tied to the location. If an IQ dies, its replacement knows nothing about unfinished transactions — by design, for security (avoids duplicates when the location may have paid the player some other way). Mother Goose tickets always print; IQ never blocks that path.

**No manual entry.** Manual ticket entry stays banned — it is the fraud source that operators and InComm complain about in PAX. Andrei's idea of scanning ticket photos was rejected as unreliable (smudged print can misread amounts).

**The "recorder" — a new product idea.** Val proposed a small box (like a Flex Port board with no display) that sits between Mother Goose and the printer, needs only power and line in/out, and permanently records every transaction at the location. It never turns off and syncs to the cloud through IQ or another JVL device. After an IQ outage, it lets JVL hand the operator a report: "these transactions happened while we were out of service — you decide how to treat each one." It could be adapted from the existing Flex Port hardware, possibly delivered within ~30 days, and rented (Val floated 99 cents/day). Naming: the device is the "recorder" (a dumb recorder); a "CFO agent" reads from it. The August 1 pilot launch is NOT delayed for this — it gets added to the product roster.

**Changes to the current flow before/after August 1.** Andrei walked through today's behavior: pending transactions live only on the IQ, the Void button still exists, and card-issued or voided transactions get written to Payment Hub. Agreed changes: implement ticket pass-through; remove the Void button; the only path is issuing a card, with 2–3 automatic retries, after which the transaction is automatically marked failed (no button). Failed is a terminal state.

**Pending-transaction timeout.** How long does an untouched transaction stay on the IQ screen? Juan suggested about an hour. Val proposed (explicitly "shooting from the hip") 24 hours, plus 48 hours for the operator to resolve with escalating warnings, then erase and notify. Not settled. The screen should display the countdown and highlight dying transactions.

**Hand pay for wins over $1,000.** Val's proposal, which Juan endorsed from casino experience: any win over $1,000 becomes a "hand pay" and leaves the regular automation cycle. The transaction shows in a distinct color (e.g., yellow); the cashier is trained never to touch it and to call the person in charge. The Payment Hub (not IQ) sends an SMS to the master operator's decision maker with a one-time code — one code per jackpot, expiring, including amount, ticket number, and location. Entering the code unlocks only that jackpot for processing. The amount is split across multiple InComm cards ($1,000 max each, $2 fee per card); the split must ensure the last card is never below $7 (the $5 card minimum plus the $2 fee). InComm has no pre-approval process (Dmitri confirmed the day before) — cards either load or error. If a card in the sequence fails after retries, that remainder is failed (terminal); a recorder could enable re-automation later. A hand-pay report goes back to the approver when the cycle finishes. Juan noted the CFO can weigh the location's $5,000 daily InComm limit when approving, or ask InComm for a temporary increase. Val prefers SMS over email and said the market should be consulted on the approval mechanism.

## Decisions Made

- **IQ keeps no local transaction memory — only transitional memory during the ~30-second validation cycle; every transaction ends validated or failed.** — Keeps IQ simple and avoids duplicate-payment risk. (Decided by Val, agreed by Andrei and Juan)
- **No manual ticket entry and no photo/scanner entry.** — Both are fraud and error sources; PAX's manual entry is a known complaint. (Decided by Val)
- **Remove the Void button; the only action is issuing a card, with 2–3 automatic retries, then automatic "failed" — no button. Failed is terminal.** (Decided by Val, confirmed by Andrei)
- **Wins over $1,000 are handled as "hand pay": visually flagged, locked until a per-jackpot SMS code from the decision maker unlocks it, then split across cards with the last card never below $7.** — Mirrors the established casino hand-pay procedure. (Proposed by Val, endorsed by Juan and Andrei; market consultation still wanted)
- **Add the "recorder" device to the product roster; do not delay the August 1 pilot for it.** (Decided by Val)
- **Naming: the device is the "recorder"; the "CFO agent" is the software agent that reads from it.** — Avoids persona confusion Juan raised. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Write a high-level summary of the agreed process changes and send it to Val, Juan, and himself in the chat for review, including a basic mention of the recorder device | July 23, 2026 (today) | High | Only after the three agree does it get unwound into caps/reqs updates for the dev team |

## Open Questions

- How long a pending transaction stays on the IQ screen before auto-erase: Juan suggested ~1 hour; Val floated 24h + 48h operator window (~72h total) but said he was "shooting from the hip." Not settled.
- Exact hand-pay approval mechanics — Val wants the market consulted before finalizing the SMS-code approach.
- Recorder device details (hardware basis, pricing, delivery) — only sketched; Val estimated ~30 days and 99¢/day rental as rough ideas.

## Dispatch Log

## Related

- Part 1: [[Meeting_Notes_IQ_Process_Flow_Review-July-22-2026]]

---
*Processed from Teams transcript on July 23, 2026, 10:05 AM Eastern (automated meeting-watcher run)*
*Source meeting: Discuss new IQ process flow- Part 2*
