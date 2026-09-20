# Meeting Notes — Billy Liu (PlayPay): Georgia Payment Ecosystem and Float Economics

**Date:** September 15, 2026, 7:08 PM – 9:33 PM Eastern
**Source meeting:** continuation of Val_Billy Liu (Outlook, 5:00–7:00 PM ET, organizer Val Levitan) — this session ran on past the scheduled end
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Raw transcript:** [[Meeting_Transcript_Billy_Liu_PlayPay_Georgia_Payment_Ecosystem_and_Float_Economics-September-15-2026]]
**Present:** Val Levitan (JVL), Bill "Billy" Ming Liu (PlayPay / SurfNote), one further participant
**Companion session:** [[Meeting_Notes_Billy_Liu_PlayPay_Mutual_NDA_Renegotiation-September-15-2026]] (segment 1 of the same evening)

> This is the second Plaud session of the same evening, starting minutes after the NDA session ended. With the NDA settled, the conversation turned commercial. Teams recorded none of it.

## What happened

A long working session on how a JVL–PlayPay payment tie-up would actually function in Georgia: who fronts the cash, who carries the regulatory risk, and where the margin comes from. No agreement was reached. This is groundwork.

## Billy's business, in his own account

- **SurfNote** is his company, 100% his. It has been licensed with the Georgia Lottery since 2014.
- **PlayPayments / PlayPay** is separate and newer, built afterwards, with his brother involved.
- Georgia opened with about 18,000 connected machines. SurfNote boards were in roughly half of them; he sold 8,000–10,000.
- He tells the Intralot-won-the-bid story from the 2014 launch party, where the lottery director told him "Billy, can you wait till the end."

## The commercial problem they worked through

**Pre-funding is the whole risk.** Billy pays players out of his own float and only later collects from the store. He must keep money pre-funded at Visa to be able to pay out at all — he cited a $10,000 pre-fund and noted Visa will not simply raise it on demand.

**The weekend gap is the worst of it.** ACH is same-day at best and does not run weekends. Friday through Monday means four days of payouts with nothing coming back. On his arithmetic: a location doing $100 per machine per day implies roughly $900/day/machine in payouts; across six machines over four days that is about **$24,000 of exposure at a single location over one weekend**.

**Margin.** Visa's interchange share is about **1%**, of which Billy keeps half — **0.5%** — under his Visa agreement. Val pushed on this twice, asking why it is half and why InComm appears to get more. The float itself is the other revenue: money sitting between payout and collection, which Billy said Visa shares with him and he would in turn share with JVL.

**Leverage over a non-paying location.** Billy cannot legally switch a machine off — the Lottery forbids it. What he can do is shut off his own AFT, kiosk and POS, and his contracts name him sole provider. For the roughly **10,000 legacy machines with no secondary SAS**, he wires his AFT through the bill acceptor, so killing the AFT kills money in and money out while leaving the machine running. Val's point in reply: JVL is connected to the machine and fully digital, so in a shared deal the control question changes.

**Hardware cost.** Today a master pays about $500 per unit per machine — six machines is $3,000 before any point-of-sale terminals. JVL's pitch removes that purchase, which prompted Billy's question of how you then control manipulation without a hardware anchor.

## The compliance disagreement — the important part

Billy's app lets a player move funds off the Visa card to a bank account or PayPal. He treats the Georgia Lottery's letter on this dismissively (he calls it "a stupid letter") and has offered to turn the feature off.

**Val disagreed with the whole posture.** His position: if Visa learns the law is being broken they will stop clearing the transactions, and the Lottery need only phone Visa to make that happen. Better to go to the regulator openly, show how the system works, and get clearance first.

This is a real difference in approach between the two parties and it is unresolved.

## Decisions

None. Val's stance from the earlier session held — leave it open, no pressure.

## Undertakings

| Who | What | By when |
|---|---|---|
| — | No undertakings were given by either side in this session | — |

Open questions left on the table: what Visa's actual interchange share is (Billy says it is a secret document), why InComm's economics appear better, and whether the Lottery would accept a self-checkout style dispenser model.

## Notes on the transcript

All four items below were put to Val on 2026-09-16 and settled:

- **InComm — 23 occurrences corrected.** The recording rendered the company as "income" / "Income" throughout: *"funded by income, and then income goes and gets money from the store"*, *"income is the master guy. Income has the sub accounts"*, *"I hated that Income Only charges two dollars to load"*, *"How does income do it?"*. **Val ruled InComm everywhere on 2026-09-16** and all 23 were corrected under the standing scoped-fix rule. Word-boundary matching only — the 3 occurrences of "information" in this transcript were left untouched.
- **Intralot** — rendered "Intellicom" and "Interloch" in the launch-party passage, where the correct spelling also appears. **Confirmed by Val 2026-09-16 and corrected** (2 occurrences).
- **"Every" (3)** → checked; used as the ordinary word here, not Everi. No action.
- **SMIBs** — rendered "snips" ("we started selling these boards, these snips"). **Confirmed by Val 2026-09-16 and corrected.** Applied as a scoped fix, not a blind rule: "snips" is also an ordinary English word and the 2024 Jira transcripts use it that way ("little image snips"), which were left untouched.

`Tito` → `TITO` was corrected once under the standing glossary rule.
