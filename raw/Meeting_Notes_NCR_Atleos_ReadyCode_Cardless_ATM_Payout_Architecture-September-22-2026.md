# Meeting Summary — NCR Atleos / ReadyCode — cardless ATM payout for JVL's Georgia amusement business
**Date:** September 22, 2026, 1:01 PM – 2:17 PM Eastern
**Duration:** 1 hour 16 minutes
**Attendees:** Val Levitan (JVL); Carlos Kalinchuk (commercial rep, ReadyCode fintech portfolio, NCR Atleos); Sean (product manager)
**Raw transcript:** [[Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar:** paired with the Outlook event "NCRA + Jvl: ReadyCode Discussion" (1:00–1:45 PM ET, organizer Carlos.Kalinchuk@ncratleos.com). Val postponed his next meeting to let the call run long.

## Summary

A first call. JVL is looking for a way to pay Georgia amusement players that does not depend on InComm. NCR Atleos sells a cardless ATM cash-in / cash-out product called ReadyCode. Neither side knew the other's business at the start, so most of the call was each explaining their own.

**Who NCR Atleos is now.** NCR bought Cardtronics about eight years ago. Wall Street did not like the combination and the businesses split. **Brinks is now buying them** — the deal is approved and in flight, and Carlos expects name changes, possibly logo changes, in the new year. Carlos runs the surcharge-free fintech partnerships. Sean is product manager for the partner solution.

**How ReadyCode works.** No card. The partner's own app generates an **eight-digit code**; the player walks to any ATM on the network, enters a phone number (or account number) plus the code, and the ATM calls the partner's API to check the code and the amount. The player presses confirm and takes the cash — the amount cannot be changed at the machine. The same works in reverse for cash-in. It is a **pre-staged** transaction, and the code can be valid for as long as the partner wants. Two-factor: phone number plus code. ReadyCode is backend only — partners put their own brand on top, the way DoorDash and Uber do.

**The network.** About **30,000 ATMs** enabled for cash-out (17,000 when Carlos joined four years ago) and about **3,800** that can take cash in. Sean gave **1,032 machines in Georgia**. 80% of network traffic sits in a handful of metros; Atlanta is one of them. A geo-locator API returns the nearest machine by address, latitude/longitude or zip code.

**Money movement.** The partner sets up two **FBO ("for benefit of") accounts** — one for cash in, one for cash out. Settlement is daily, closing at 1:30. Cash a player puts in is ACH'd to JVL's bank the next business day; cash paid out is pulled from JVL's bank.

**Price.** Carlos did not want to discuss commercials but gave numbers when Val insisted: **about $2.75 per withdrawal**. Deposits are cost-plus-interchange and range roughly **$0.85 to $4.00** depending on volume and the maximum amount accepted — the more cash going in, the more often their trucks must collect it. Val pushed on whether cash servicing is extra. It is not: **the per-transaction price covers all cash handling, with no monthly fee and no separate servicing charge.**

**Who pays the fee.** The network is surcharge-free at the machine — the player never sees a fee on screen. The partner chooses: absorb it, allow one free transaction a month and charge after that, or charge every time. Whatever the partner charges is added to the pre-staged amount (a $60 withdrawal becomes a $65 pre-stage).

**Val explained the Georgia model in full.** 7,400 convenience-store locations, 47,000 licensed amusement machines, regulated by the Georgia Lottery Corporation. A player pays cash at the counter or a kiosk, gets a barcoded paper e-wallet the size of a dollar bill, plays, then brings it back. The cashier or kiosk scans it, calls InComm's API, and hands over a physical prepaid card the player redeems at any ATM. **KYC sits on the licensed location, not on the player** — InComm ships blank barcoded cards to registered locations and the card is married to an amount at the moment of issue. The KYC ceiling is **$1,000**. The card is effectively single-use: ATM redemption, cashback or partial redemption, **no reload**. Val said the technology to reload exists from several sources and he does not understand why InComm limits it; Carlos guessed a compliance reason.

**Val corrected Carlos twice on language.** Not gambling — Georgia law prohibits gambling, and the machine is approved through a testing laboratory as a **skill amusement device**. And when Carlos began explaining the advantages of going cardless, Val cut in: "I need a card. The law says you must have a card."

**Val was careful about InComm before saying anything.** He asked whether the call was being recorded on their side (no), whether the conversation would get back to InComm (no — an NDA is in place), and whether NCR Atleos has exclusivity with InComm. Carlos was open: InComm uses their surcharge-free carded platform today and that is public knowledge, but there have been no conversations with InComm about JVL.

**Where it stalled.** Val asked repeatedly what a typical location or machine transacts per week. Carlos said they do not hold that data, work by customer rather than by location, and would never share it. Val did not accept the answer and said so plainly, then made the practical point: his Georgia volume today is **zero** — the legislation is only now coming into effect — so he has nothing to project from and needs a price to move the discussion forward. Carlos's position held: he will take the case to his internal team and come back with a commercial proposal.

**Val's own direction.** JVL's hardware carries an **AFT (Automated Funds Transfer)** insert that reads the machine's virtual counters — cash, promo and about thirty others. That is JVL's route to the player. Val said a JVL app with a direct customer touch point is certain, and that JVL would equally be happy to ride on a partner's app. ReadyCode has no app of its own.

**One ask Carlos could not answer.** Val asked whether he could add **2,000 ATMs of his own** to the network in Georgia. Carlos said it has to be their machines because the transaction is FDIC-regulated, but that "mini networks" do exist on the carded side. Not on ReadyCode — the product is only about three years old commercially. He will find out.

## Decisions Made

No formal decisions recorded. This was an introductory call; both sides agreed the next one is the commercial discussion.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Carlos Kalinchuk | Send Val the ReadyCode deck | TBD | High | [External] Val asked twice; Carlos said he would send the file |
| 2 | Carlos Kalinchuk | Take JVL's case to the internal team and come back with a streamlined commercial proposal | Next call | High | [External] Georgia only, starting from zero volume |
| 3 | Carlos Kalinchuk | Give a specific deposit price rather than the $0.85–$4.00 range | Next call | High | [External] He said a simpler commercial scheme is possible |
| 4 | Carlos Kalinchuk | Find out whether JVL's own ATMs could run as a mini network on ReadyCode | Next call | Normal | [External] Never been asked before on the cardless product |
| 5 | Sean | Check with the NCR Atleos compliance department whether Georgia requires a physical card or allows cardless | TBD | High | [External] He offered this himself; it decides whether ReadyCode fits at all |
| 6 | Val Levitan | Work out JVL's volume projections for Georgia at 12, 24 and 36 months | TBD | High | Carlos will not price without them; Val says he has no basis yet |

## Open Questions

- **Does Georgia law actually require a physical card?** Val said it does, then walked it back — "I cannot say it with hundred percent reliance" — noting only that InComm holds more than two thirds of the market and that is what InComm does. He also said a fully digital competitor program exists but he knows little about it. Sean is checking with compliance. This decides whether ReadyCode is usable in Georgia at all.
- **Price.** No firm number. $2.75 per withdrawal is an estimate Carlos gave under pressure; deposits are an unresolved range.
- **Can JVL put its own ATMs on the network?** Open with Carlos's team.
- **How much does a location actually transact?** Carlos will not provide it and says the data does not exist in that form. Val does not accept this and will need another source to build his projections.
- **Why does InComm not allow reloading the card?** Val thinks it is not a technical limit. Carlos guessed regulation. Neither knows.

## Notes on the transcript

Plaud mis-transcriptions corrected under `Plaud_Transcript_Glossary.md`: **9 automatic** (7 `JBL`→JVL, 1 `JDL`→JVL, 1 `Income card`→InComm card) and **17 scoped** (`Income`/`income`/`Incom`→InComm, ruled by Val 2026-09-22; the 14 occurrences of "information" were left untouched by word-boundary matching).

Flagged after the first pass, then **confirmed by Val on 2026-09-22 and corrected** (added to the glossary fix table the same day):

- **JPL → JVL**, 2 here. A new variant; the glossary previously had JBL, JDL, GBL, Javel and JVO but not this. The rule carries a documented exception: in the media tax credit (OIDMTC) filing, JPL is the name of a game, listed beside JPS, HG5P, DLK, HG3 and HG6, and must never be rewritten there.
- **CashCode**, 3 here (a two-word form and a lowercase one-word form). The earlier rules matched neither spelling.
- **Prize Play → InComm's card**, 3 here. Val was unsure of the name himself on the call, so the uncertainty was real, not only a transcription error.

Still flagged and **not** corrected — not in the glossary, awaiting Val:

- **`NCR Outlets`** (1) → NCR Atleos.
- **`Redigo`** (2) / **`ReadyGo`** (1) / **`Ready Code`** (4) → ReadyCode.
- **`Waypoint`** (1) — Sean's product name as transcribed; not verified.
- **`PlayStation transaction`** (1) → pre-staged transaction.
- **`Paulo`** (1) → Val. Sean addresses him this way once.
- **`John`** (1) → Sean. Carlos thanks "John" when he means Sean.
- **`PPI`** (1) → PII.

Speaker labels are unreliable throughout — Plaud splits Val across Speaker 1 and Speaker 2 and puts both halves of an exchange inside one block. Read by content, not by label.

## Dispatch Log

---
*Processed from Plaud offline recording on September 22, 2026*
*Source meeting: 09-22 Exploration of a Cardless Cash Access Solution for JBL's Amusement Business in Georgia*
