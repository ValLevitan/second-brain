# Meeting Summary — GA-COAM_Fiery_Pay

**Date:** August 12, 2026, 3:31–4:02 PM (Eastern)
**Duration:** ~31 minutes
**Attendees:** Val Levitan, Juan Martinez, Felipe Miranda Giorgi (Andrei Klimovich was invited but was not in the office)
**Raw transcript:** [[Meeting_Transcript_Fiery_Pay_Competitive_Analysis-August-12-2026]]

## Summary

The team reviewed a competitor payment system called **Fiery Pay** (run by "Afshad," linked with Aristocrat) that is showing up in Georgia COAM locations, and talked through how JVL should answer it. Juan had posted a quick use case in the chat to prepare for a site visit.

**How Fiery Pay is understood to work.** It does not use a printer. It ties into the machine's bill acceptor (through a protocol like JCM or MEI), because the bill acceptor is what issues credits. Felipe described the full flow he saw at a location about two hours away (near Macon): the player puts cash into the bill acceptor and plays; on cash-out, the credits go onto a loyalty/e-wallet card that sits on the machine; the player then goes to a kiosk that converts player points to a gift card (a $2 fee) or a gift card back to player points. The gift card is a standard prize-pay / MasterCard-type card that can be spent anywhere (e.g., Walmart), but the player can also bring it back, scan the barcode, convert it back to player points, and load credits onto a machine. Partial amounts can be split between gift card and machine.

**Why the team sees it as a weak, risky design.** Val called the send-credits-back-to-a-machine approach a "legal-ish" gymnastics workaround — the operators seem to treat it as a "transfer" point rather than a redemption point. He and Juan both flagged heavy fraud exposure: money can be sent back to an unattended machine that someone else then sits down at, and there is no real systems check on the amounts. Val's larger point: after all the gymnastics, the player still walks away with a cash-spendable gift card, which defeats the whole purpose of keeping the money in play. Juan noted this space is essentially unregulated — GLC has said it does not control what these kiosks do.

**Open legal question.** Nobody could explain how a non-cash MasterCard gift card is legally converted into player points/cash. It appears to require a merchant ID / reseller status and looks like a "fake transaction" is being run to empty the card. It was unclear whether Fiery Pay or the location holds the merchant ID. Fiery Payments is a broader payments company (ATM and card processing across Visa, MasterCard, Amex, Discover, Union Pay, JCB), not just a COAM product.

**Market read.** Felipe hears appetite for this kind of system from several operators. The "Tito" hype is cooling; the solutions being talked about now are Batson (Light & Wonder), Easylinks (ticket printed in the back), Fiery Pay (Afshad / Aristocrat link — the most popular), and Access (with printer). One location Felipe recently serviced is pulling out its printers and kiosk to install the competitor system; Felipe saw the box and it was labeled "JVL kit for flex," which he found odd.

**JVL's answer.** JVL's "replay" feature is its version of the temporary wallet. To print the initial QR code, the location needs a **recycler** (not necessarily a FlexPay kiosk). Val's stated winning combination is a **recycler plus a flex port**, which also enables sophisticated reporting for operators; IQ is optional (Val: "you probably don't need it," though he expects operators will still take it). The recycler solution depends heavily on Income's price-play card. Val relayed a message received during the call from John Hasel at Income: the new card (the current one is Prize Play / Prize Pay; the new one is "Skill Pay") will be available from mid-September, which would let JVL implement the full solution around November.

Val confirmed he never spoke directly with Afshad because he refused to sign the NDA; the back-and-forth was on Felipe's side.

## Decisions Made

- **JVL's competitive package for these locations is a recycler plus a flex port, built around the "replay" temporary wallet and Income's price-play/Skill Pay card.** IQ is treated as optional, not required. (Direction affirmed by Val and not contradicted later; no formal sign-off.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Get from Andrei Klimovich a write-up of what he observed at the Macon-area location this weekend (gift-card ↔ player-points ↔ machine-credit flow) | TBD | Normal | Andrei visited Sat/Sun; nothing written up yet |
| 2 | Felipe Miranda Giorgi | Find and resend the video(s) he recorded of the competitor location flow (previously posted in Confluence) | TBD | Normal | Documents the full player flow he witnessed |
| 3 | Felipe Miranda Giorgi | Try to meet Mo Patel (possible Sunday breakfast) to see the Fiery Pay flow step-by-step at the new location | Sunday (tentative) | Low | Mo Patel is influential, ex-GOMOA president's relative |
| 4 | Felipe Miranda Giorgi | Keep passing any new information / "gossip" on competitor systems to Val and Juan as it comes up | Ongoing | Normal | Val's standing ask at close of call |

## Open Questions

- How is Fiery Pay legally converting a non-cash MasterCard gift card into player points (and effectively cash)? Who holds the merchant ID / reseller status — Fiery Pay or the location? (Raised by Juan and Val — unresolved.)
- What is actually inside the "JVL kit for flex" box the operator is installing, and is it genuinely a JVL kit? (Felipe saw the label — unexplained.)
- Does the recycler need IQ, or is recycler + flex port enough? (Val leaned toward not needing IQ but expects operators will still take it — left open.)

## Dispatch Log

---
*Processed from Teams transcript on August 12, 2026 (Scheduled Watcher Mode)*
*Source meeting: GA-COAM_Fiery_Pay*
