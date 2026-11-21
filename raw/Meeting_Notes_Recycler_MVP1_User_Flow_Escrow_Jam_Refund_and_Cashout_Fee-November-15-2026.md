# Meeting Summary — MVP-1 Recycler CAPs/REQs review
**Date:** November 15, 2026, 8:01 AM – 8:57 AM Eastern
**Duration:** ~56 minutes
**Attendees:** Andrei Klimovich (organizer), Val Levitan, Pavel Frolov, Alexander Biratko, Irina Shishko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Recycler_MVP1_User_Flow_Escrow_Jam_Refund_and_Cashout_Fee-November-15-2026]]

## Summary

**Scope for Thursday.** Andrei added all player screens and flows for the recycler to MVP 1 in Jira (the flow PDF is attached there next to the screens). Admin screens and flows follow tomorrow. Alexander: for Thursday the team only finishes the player flow and polishes the screens; reports take longer. Irina: MVP 1 is the piece done by Thursday; the first release to people comes later. Andrei summed up Thursday: take money, create wallet, pay out, update wallet, play with ports connected, so Andrei can install it and walk through it.

**Wrong recycler model in capability 341.** It refers to the RT model (2 drums). The unit JVL has is the RQ model with 4 drums (JCM makes both). Alexander owns the capability and will fix it.

**Bill in, escrow, cancel, timeout.** The recycler holds one bill in escrow. If no command is sent, it returns the bill after 30 seconds; repeated "hold" commands keep it. Val: all bills go to the drums. If the player presses Cancel, JVL returns the same money (for example 4 twenties). Three paths (Alexander, confirmed by Val): Cancel = return the money; Print = print the ticket; no action = wait for timeout, keep the money, no ticket, record it. Pavel asked not to use the word "unclaimed"; Val suggested "forfeit" or simply "refusal".

**$100 bills.** Val recommends refusing $100 bills. About 20 years ago Iran flooded the US with fake $100s, and accepting them invites counterfeiters. It is a setting and can be changed at any time.

**Printer problems.** No paper: block money insertion before it starts (Alexander: already done in Flex-Pay). Print fails or ticket jams: Val said the wallet exists only after the ticket prints. Andrei first proposed going back to a "try again" screen so an attendant could clear the jam and reprint. Val rejected this as too complex: cancel the transaction, return the money, put the product out of service, call the attendant to fix and test it. Andrei agreed and will simplify the flow.

**Texas: no playable/redeemable split.** Texas has no handpay rule like Georgia, so the ticket and wallet show one balance. Val reminded the team: any promo credits in Georgia COAM must respect the handpay law; promo credits must be played through before cash-out. Pavel: with $21 credited for $20, all $21 is playable but only $20 redeemable. Andrei asked if promo credits go in MVP 1; Alexander said move them to MVP 2 if not ready. Not settled.

**Cash-out fee.** Val wants 3 fee categories in setup (name, percent, who pays); not used yet. Example: in Nebraska, banks charge about $65 a month to service dispensers, and some operators want to pass this to the player. Alexander suggested taking the fee when money goes in; Andrei refused. Agreed for MVP 1: a fee option on the redemption screen, set per location. At 0 the line is hidden. Otherwise the player sees the fee before agreeing. Amounts below the smallest note stay on the wallet (for example $9 with $5 notes: player gets $5, $4 stays to play).

**RIS and Passport.** Val does not want to drop RIS (Remote Installation Setup) and Passport (birth certificate of the device, serials in the Dallas chip). Pavel: the recycler and Flex-Pay boards have a Dallas chip. Not in MVP 1, but needed before the first live recycler install (Andrei asked, Irina and Val agreed). The IQ install next week goes ahead without it (Val).

**Payout wait.** Andrei suggested 30 seconds to take a dispensed note; Val said at least 90 seconds. If not taken, the note is pulled back and the amount returns to the wallet. Pavel asked if this is per note.

**Power loss.** Bills in, then power off: Val said there is a GLI requirement (he thinks GLI-11) to restore to the same stage; a reference is needed. Alexander: the bill validator spits out the escrow note on start-up. Agreed: on restore return to the previous screen, give back the accepted bills, and do not credit the last note. Alexander: "restore to the same state" should be written as its own requirement. During payout: money must be frozen on the wallet as "in payout" before dispensing (Alexander, Andrei, Pavel). Once a note is out, it is not returned to the wallet. Andrei proposed booting into idle after a power loss; Irina said this may break the "return to the same state" rule. Not settled.

**One note or a bundle?** Unknown if the RQ dispenses one note at a time or a bundle. Andrei recalls Gennady's emails with JCM: the RQ cannot make bundles; a pricier model can. Val thinks JCM may have a bundle module. Alexander will check tomorrow in the office. Val: document the questions, send them to the JCM designers, and use Gennady with this transcript. Alexander wants own tests first.

## Decisions Made

- **Capability 341 must refer to the 4-drum RQ recycler model, not the 2-drum RT.** The unit JVL has is the RQ. (Andrei, Alexander)
- **Bill-in flow: Cancel returns the money; Print issues the ticket; no action until timeout = keep the money, no ticket, record it.** (Alexander, confirmed by Val)
- **Ticket jam or print failure: cancel the transaction, return the money, put the product out of service, attendant fixes and tests. The wallet counts only after a ticket prints.** Considered and superseded: return to a "try again" screen so the attendant can reprint (Andrei). (Val; Andrei agreed)
- **Texas ticket and wallet show one balance, no playable/redeemable split.** Texas has no handpay rule. (Andrei proposed, Val agreed)
- **MVP 1 cash-out fee: location setting shown on the redemption screen, hidden when 0.** Considered and superseded: fee when money goes in (Alexander). (Andrei; Alexander agreed)
- **RIS and Passport are not in MVP 1, but must be in place before the first live recycler install.** (Val, Irina, Andrei)
- **Power loss with bills in: restore to the previous screen, return the accepted bills, do not credit the last escrow note.** (Val, Alexander)
- **Payout funds are frozen on the wallet before dispensing.** (Alexander, Andrei, Pavel)
- **For Thursday, MVP 1 = the player flow only (money in, wallet, payout, play with ports).** Admin flows and reports come later. (Alexander, Irina, Andrei)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Finish admin screens and flows for the recycler in Jira | Nov 16, 2026 | Normal | "By tomorrow" |
| 2 | Alexander Biratko | Fix capability 341 to the 4-drum RQ model | TBD | Normal | He owns it |
| 3 | Alexander Biratko | Check in the office if the RQ dispenses one note at a time or a bundle; report to Andrei | Nov 16, 2026 | High | Affects the payout flow |
| 4 | Andrei Klimovich | Update screens and flows: jam = cancel and refund; one balance for Texas; adjust after Alexander's answer | Before Nov 19, 2026 | High | |
| 5 | Alexander Biratko | Polish the player screens for MVP 1 | Nov 19, 2026 | High | Thursday target |
| 6 | Andrei Klimovich | Write the power-loss requirement: restore to the same state, freeze payout funds | TBD | Normal | "We will write it"; Val wants the GLI reference |
| 7 | [Unassigned — needs clarification] | Send the open recycler questions to JCM designers, with Gennady, using this transcript | TBD | Normal | Val's advice; Alexander wants own tests first |

## Open Questions

- Does the RQ dispense one note at a time or a bundle? (Pavel, Andrei; Alexander to check)
- After a power loss during payout: resume payout or boot to idle? (Andrei proposed idle; Irina objected)
- Payout wait time: at least 90 seconds (Val), per note or for the whole payout? (Pavel)
- Promo credits in the first release or MVP 2? (Andrei asked; Alexander: MVP 2 if not ready)
- Which GLI requirement covers power loss? (Val thinks GLI-11; Pavel thinks kiosks use another GLI document)
- Who pays the fee categories and how much? (Val: not known yet)

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026 (scheduled meeting-watcher)*
*Source meeting: MVP-1 Recycler CAPs/REQs review*
