# Meeting Summary — Recycler_state_of_ready_alignment
**Date:** July 31, 2026, 1:30 PM Eastern
**Duration:** ~15 minutes
**Attendees:** Val Levitan, Pavel Frolov, Genadi Peari

**Raw transcript:** [[Meeting_Transcript_Flex_Recycler_Georgia_Show_Readiness-July-31-2026]]

## Summary

Right after the expo-planning meeting, Val took the recycler readiness question to engineering (Pavel and Genadi). The meeting was in Russian.

**Use case for the Georgia show (Aug 18).** Val described the flow: a player inserts $20 and gets a QR code, plays across the Flex machines fitted with Flexports, finishes, goes to Flex IQ, is handed a fake card that emulates the future InComm "Skill Play" card, presents it to the recycler, and gets cash. The ideal flow would present the QR code directly at the recycler, which would issue the Skill Play card and then pay out cash.

**Pavel's read.** Both flows are technically possible but not very realistic on the timeline. He proposed a third scenario: before dispensing cash, show an extra screen indicating a digital card is being issued (not yet on the market) with a button to convert it to cash. It is not fully "honest" (properly it should be card first, then cash) but it is the only way to actually pay out what is on the e-wallet. The QR-ticket-to-cash flow already works in some form today. The architecture with Flex IQ and the Flex recycler as separate units would need new code on both sides to link them — realistic, but not on every timeline.

**Hardware state.** One recycler is lying in Georgia and a second is ordered there. Metal and parts are on hand; the teams have mandates and instructions to start assembling slim cabinets, and they want to build two — one for the show and one for the bank. They need to order a second dispenser (only one on hand). Nuance from Pavel: the Flex dispenser has not been touched in a while and needs to be powered up and checked; Genadi added that they have not even verified what is installed — there is no software on it.

**Denomination configuration problem.** Val wants the recycler set to "$5 and $20." Genadi reported that CPI's logic is different: the first drum must be fully filled with the minimum denomination, so a drum could be all $1, or a second drum split, with up to three denominations in the second drum — not a clean four-denomination setup. Pavel said this is not 100% settled; he spoke with Sasha today, who is studying whether any denomination can go in the first drum and has not ruled it out. Genadi said CPI's senior confirmed the minimum-first rule last week. On capacity, Genadi estimated one drum of $5s at ~$300, and splitting the second drum gives roughly $600 + $300 ≈ $1,200. Val was blunt that the minimum-denomination-first rule is bad design that no customer can use, and wants cassette 1 = $20 and cassette 2 = $5/$10. He told Genadi to open the conversation with CPI/JCM ("JC") on Monday and ask them to change their code.

**Direct cash and the cabinet.** Genadi asked whether cash can be dispensed from the recycler directly rather than only via a card. Val: for now, only via card — direct cash dispensing requires financing the dispenser and comes with new legislation, not now. The recycler must be placed into the slim cabinet and is better made slim; it can sit in front of the site.

## Decisions Made

- **Assemble two slim cabinets — one for the Georgia show, one for the bank.** (Val, Genadi)
- **For the show, use the QR-ticket-to-cash flow, with Pavel's extra "digital card issuance" screen before payout, rather than real card issuance.** (Val, Pavel)
- **Push CPI/JCM to change the denomination logic so cassette 1 = $20 and cassette 2 = $5/$10, rejecting the minimum-denomination-in-first-drum rule.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi | Open the conversation with CPI/JCM ("JC") and ask them to change the denomination logic so cassette 1 = $20 and cassette 2 = $5/$10 (not minimum-denomination-first) | Mon Aug 3 | High | Current CPI rule fills the first drum with the minimum denomination |
| 2 | Pavel | Work with Biratko to finish the recycler use case (QR cashout only, no card hand-out) to a tested, working state | Next week | High | Biratko is staying off vacation next week; needs the intermediate code |
| 3 | Pavel / Genadi | Power up and check the state of the Flex dispenser and get software to test the assembled station | TBD | High | No software currently installed; not verified |
| 4 | Genadi | Order a second dispenser and confirm the second recycler ordered for Georgia | TBD | Normal | Only one dispenser on hand |
| 5 | Genadi | Start assembling the slim cabinet(s) per the instructions received | Ongoing | Normal | Two cabinets — show and bank |

## Open Questions

- Whether CPI/JCM will change the first-drum minimum-denomination logic (Sasha is still studying whether any denomination can go in the first drum). (Genadi, Pavel)
- Direct cash dispensing from the recycler (versus only via card) awaits new legislation and dispenser financing. (Val)

## Dispatch Log

---
*Processed from Teams transcript on July 31, 2026, 2:00 PM Eastern*
*Source meeting: Recycler_state_of_ready_alignment*
