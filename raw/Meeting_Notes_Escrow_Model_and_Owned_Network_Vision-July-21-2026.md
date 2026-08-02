# Meeting Summary — Call with Andrei Klimovich (Escrow Model and Owned-Network Vision)
**Date:** July 21, 2026, 7:05 PM Eastern
**Duration:** ~43 minutes
**Attendees:** Val Levitan, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_Escrow_Model_and_Owned_Network_Vision-July-21-2026]]

## Summary

The call was in Russian and continued the earlier discussion. Andrei reframed the narrow case Dmitry had raised: what to do with local transactions stored on a machine when a device is unbound. A transaction is created on the machine when received from MuthaGoose (pending), then moves to a terminal state — ticket printed, or card activated. Andrei recalled Val questioning whether to create the transaction on IQ at all.

**The escrow principle.** Val said his position is stronger than Andrei had put it: not "maybe we don't need to," but "we should not, and it is wrong to." His reasoning: JVL does not own the local network. When JVL taps into someone else's network to bind a machine to its IQ, the purpose is to emit PAX (JVL's competitor). Because JVL does not own the whole network, it cannot take responsibility for storing information; it can only push a transaction away or process it. While processing, it holds the transaction in escrow — if processing succeeds, accept it (transaction passed); if not, reject it. If JVL owned its own network, the logic would be radically different.

Val detailed the flow: pull MuthaGoose data only to display on the IQ screen (machine number, cashout amount) — do not create the transaction in Payment Hub yet. Only when moving to card issuance does JVL's protocol engage, create the transaction in Payment Hub as finalized, and tell MuthaGoose the transaction is processed. IQ is just a "pocket," not the brain — cloud services (Payment Hub) talk to INCOM directly, bypassing IQ. If MuthaGoose has no escrow capability, the fallback is: always print a ticket, then validate that ticket separately, and never pass the same ticket number twice — the same escrow effect without a handshake. Val stressed he is guessing about MuthaGoose's protocol; Pavel can confirm in one sentence.

Andrei worried this substantially changes how the product was conceived over ~2 years. Val disagreed that it is a full change: the base product mostly works as-is, and connection and business flow stay roughly the same. He said even if Pavel or Dmitry need up to 3 months, they will still put the test on a location, because nobody fully understands today where things are stored or how the flow runs; a new program can follow later. On the August 1 target, Val said it is fine.

**Owned-network product vision.** Andrei asked Val's vision of a system fully controlled by JVL on IQ, without MuthaGoose. Val described:
- **SMIB/SMI** — a module inserted into the machine, connected to the 2nd SAS port, communicating over WSS (as FlexPay and FlexPort do today), or ideally hardwired. He warned WiFi can be jammed cheaply (~$300 device), so run wires. SMIB transmits everything through the SAS port — all account and service info, plus bill-acceptor statistics (for example flagging a bill acceptor rejecting 20% of $20 bills) — captured to the cloud hub and turned into desktop/HTML reports.
- **Machine fit** — one SAS port is taken by Intralot; the 2nd port can carry SMIB. About 30% of Georgia machines are single-SAS and aging out.
- **FlexPort** — Val would use FlexPort instead of SMIB. It enables player mobility between machines rather than forcing a cashout each time.
- **Location types** — small locations (~5-6 machines) put a recycler within arm's reach; a few very high-volume "punching bag" locations (~10 machines) might keep bill acceptors and printers in the machines and skip a kiosk. Val guessed those are ~3% of the market (~100 of ~3000 machines) — a gut feel, not data. He expects most to move to recycler + secure arcade ticket + FlexPort/FlexIQ on JVL's own network, no MuthaGoose.
- **Config** — FlexPort hardwired to SAS-2 → FlexIQ → Flex Recycler; no bill acceptors or printers in machines where a recycler stands. Val was firm that bill acceptors cannot sit in machines if a recycler is present. IQ is still kept alongside a recycler for a full modular set and redundancy (either can pick up cloud-hub connectivity), at low incremental cost, and lets the location run consoles directly on IQ.
- **Player / skill-pay flow** — player loads money at the recycler, scans a QR at the machine via the FlexPort optical reader, and credits load. On cashout, once INCOM launches skill-pay-card conversion in the fall: money → gift card → buys skill card → skill card cashed out → site dispenses cash. If not cashing out, the same happens at IQ: player scans the ticket at IQ, cashier sees the transaction and can manually activate a skill-pay card from a stack and hand it over.
- **Skill-pay card** — can be read at the recycler and converted to game credits, or act like an ATM. It can work cross-location (issued at one operator, used at another with a GL system) — Val thinks the GL system may not even be needed if the location validates by its own principle.
- **Constraint** — this does not let the recycler accept ordinary credit cards; that is a separate track (Visa/Mastercard need verification). Skill-pay works precisely because JVL does not take credit cards. On registration, Val is unsure what type JVL needs; on the INCOM call it was raised that such terminals must be registered as ITM, but Val doubts it fully applies since JVL's terminals do not take credit cards (unlike TEM/ITM terminals that do).
- **Business-plan emphasis** — (1) IQ, (2) put in JVL's own network. Once JVL captures ~30% of the market via IQ, immediately try to move all locations onto JVL's own network, offering services impossible via MuthaGoose.

They agreed to bring in Pavel and Dmitry tomorrow to answer whether MuthaGoose supports the escrow mode. Andrei will send Val the two call recordings and share excerpts with Pavel and Dmitry to pre-load context. Andrei asked why the original design blocked the transaction from going straight to the printer; Val said that when they designed it they lacked the full requirements and facts (they did not know about PAX then), and now, with all the facts, they can change their minds.

## Decisions Made

- **Adopt an escrow model for other-network transactions** — IQ pulls MuthaGoose data only to display on-screen and does not create the transaction in Payment Hub until card issuance; if MuthaGoose has no escrow, fall back to print-ticket-then-validate. (Val's direction; Andrei agreed conceptually, pending validation with Pavel/Dmitry.)
- **Call with Pavel and Dmitry set for July 22 at 9:30 AM Eastern** to confirm whether MuthaGoose can operate in escrow mode. (Both; time chosen around Pavel's 7:00–9:00 commitments, and workable for Minsk.)
- **No bill acceptors in machines where a recycler is present.** (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Schedule and initiate the call with Pavel and Dmitry for July 22, 9:30 AM Eastern re: MuthaGoose escrow | July 22, 2026 | High | Val: 9:30 works around Pavel's earlier calls |
| 2 | Andrei Klimovich | Send Val the two July 21 call recordings and share excerpts with Pavel and Dmitry to pre-load context | July 22, 2026 | High | Val believes the recordings belong to the call originator (Andrei's side) |
| 3 | Val Levitan | Join the Pavel/Dmitry call to make decisions live | July 22, 2026 | Normal | |
| 4 | Pavel, Dmitry | Answer whether MuthaGoose can operate in an escrow (hold-then-validate) mode | July 22, 2026 | High | They best know how MuthaGoose works |

## Open Questions

- Does MuthaGoose support an escrow hold, or must JVL fall back to print-ticket-then-validate? To be answered by Pavel and Dmitry on July 22.
- What registration type must JVL obtain for these terminals — is ITM registration required given JVL does not take credit cards? (Raised by Val; flagged on the INCOM call.)

## Dispatch Log

---
*Processed from a provided .docx transcript on July 21, 2026.*
*Source meeting: Call with Andrei Klimovich (recording 20260721_150517)*
