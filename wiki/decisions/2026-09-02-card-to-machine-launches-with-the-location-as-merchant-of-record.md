---
type: decision
title: InComm's card-to-machine product launches with the location as merchant of record — 5% capped at $50, paid by the player, no discounts
date: 2026-09-02
aliases: [card to machine, credits back into the machine, merchant of record, five percent capped at fifty, Van 19, Nuvei, fifty basis points, JVL as processor]
source-count: 2
status: active
open-commitments: 3
open-questions: 3
---

# Card-to-machine launches with the location as merchant of record

[[wiki/organizations/incom.md|InComm]]'s answer to the question the corpus has been circling since 2025 — how a player spends a prize card **back into a gaming machine** — arrived at the [[wiki/meetings/2026-09-02-incomm-machine-payments-and-recycler-standoff.md|Sept-2 2026 lunch]] as a product about to launch, with its commercial terms already fixed. It is InComm's decision, not JVL's, but it sets what JVL can build against. The Aug-26 promise of a deck on this topic, and of "a specific call to discuss that functionality" ([[wiki/organizations/incom.md]]), **rolls forward into this meeting**: the call happened here, and the deck commitment was re-made at the table. No source confirms the deck arrived, so it is carried below as open rather than discharged [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].

## The terms

- **5% fee, capped at $50 per transaction, paid by the player.** "We are looking at a **five percent fee and a fifty-dollar max** per [transaction]. **The player pays.**" Worked through: "they want a fifty-dollar ticket. It's going to debit fifty-five dollars or fifty-two off the card." Asked whether the 5% applies to each transaction: "At five percent. **No discounts.** No, I think we want to launch it at that" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].
- **The expected behaviour it is priced for:** "the vast majority of the purchase amounts are **between ten and twenty**… even if they have a **three hundred dollar** card, they purchase a series of ten [or] twenty dollar tickets." And on volume: "anywhere from **twenty percent to sixty percent of the gift card activations goes back into the game**" — from similar programmes, not this one [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].
- **The location is the merchant of record, and enrols with Nuvei.** "The location would **enroll with Nuvei as a merchant**, and they would use your hardware and your system to process the transaction. But Nuvei sends the transaction to Mastercard." And: "Currently, we've presented to Mastercard something that is **each location is the merchant of record for that transaction**… **That's just not how we're launching**" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]. *(The processor is spoken as "Nuvei" and once garbled to "New Base.")*
- **Status: not live anywhere.** "We're **finishing up internal testing** and hoping to go live in the market **by the end of this month**. But **it's not live anywhere**" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].
- **JVL's cut is unknown to the people in the room, with 50 basis points floated as a start.** Val: "What's the piece that goes for me?" — "I don't know." Val: "Well, you're introducing the card tomorrow, and you don't know." The eventual answer: "somewhere to start would be like **fifty basis points**." Val: "So out of five percent, **a half, half a percent**." Where the rest goes: "Some goes to [Nuvei], some goes to Mastercard… we're not getting the five percent by the time it gets to us" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].

## Why it works technically — the barcode keeps the machine out of PCI scope

- **The Van 19 string does the work.** "On the back of all of our cards, there's the **activation barcode**, which, in the API call, includes something called a **Van 19**, which is basically a long string of digits that is **meaningless to anyone outside of InComm**." InComm resolves it, runs a balance inquiry or pulls what a transaction needs, and passes that to a processor — "and **the kiosk or the game machine itself never has to touch any PCI data**, which keeps them out of the PCI compliance business, which is a bit of a nightmare, especially for a legacy hardware provider" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]. *(This is the same 19-digit **VAN** — Virtual Account Number — documented from the Mar-19 2025 card walkthrough on [[wiki/organizations/incom.md]]; the connection is an inference from the identical description, not stated in this source.)*
- **The problem it is built for is 50,000 legacy machines.** "Fifty thousand machines that are **not PCI compliant** that would like to be able to take credits back into the machine off of these cards **without having to upgrade fifty thousand individual machines** with a card reader and a processor — and we can do it with a **forty-dollar barcode scanner** as opposed to a **three-hundred-dollar** card reader" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].
- **It is not claimed to be the best deal for the player.** Val's objection — why pay 5% when the player can take the whole balance out of an ATM for $2.50 — was conceded rather than rebutted: "**Three dollars is more than two fifty**… what we see is this is probably not how you would behave." The fallback case is locations without a MoneyPass ATM, "a fairly frictionless way to continue gameplay." The speaker's own verdict: "**An imperfect solution overall, but it gets us most of the way**" [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].

## JVL's objection, and the path InComm conceded

**Val's objection is that the merchant-of-record design cannot survive contact with the Georgia market.** Two reasons, both stated bluntly [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]:

1. **Locations cannot enrol in anything.** "**Location is incapable of enrolling into anything**"; "Locations cannot register for themselves for many reasons because they need access to our equipment. We need to send the file to you. We need to receive something from you. We need to send something to the machine." The reply conceded the shape of it: "there's a whole operational workflow set up."
2. **The equipment moves and the contracts end.** "It's impossible because **today I'm in this location. Tomorrow I'm not**… Master lost the contract. He's not in the location anymore… **The contract finished. The machine is no longer there.**" The reply: "Yeah, I think that's accurate."

**Val's counter-proposal: JVL should be the processor.** "It's possible, but **I need to be processor**… if my equipment, if my setup arrives to location, whatever it is, and **I am the processor, I'm offering it with my equipment**, then it works." The answer was the nearest thing to an opening in the meeting: "**you're the second partner that's asked that question**… **I think there's a path there.**" Recorded as a conceded possibility, **not** as an agreement [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]].

## The settlement point Val disputed and then accepted

The longest single exchange of the meeting, and the one that changes JVL's obligations if it processes these transactions [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]:

- **Val's position:** once the win is on a card, the location no longer holds the money — "**The location has nothing. The cash is in your card**… Show me where the cash is."
- **InComm's position:** the location still owes the Lottery on the cash-in, so the loaded amount has to reach the location's account. "If they have a hundred dollars cash in and fifty dollars cash out. **They owe the lottery whatever the percentage is**… when your equipment processes our gift card cash in, **you send that money to the location because they need that money to settle with the lottery with their master license**."
- **The resolution as stated to Val:** "even if you have someone processing for you… if you're keeping the fee, that's fine. **But the fifty needs to make it into the location's account so that they're made whole.**" Val: "Gotcha."
- The **drop** stays where it always was — "The drop always stays with the location" — which was the part neither side disputed.

## The brokers offered instead, and Val's reaction

Two settlement brokers were offered as introductions if JVL does not want to handle settlement itself [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]:

- **Lunex Telecom** — "**Darren Lu** has operated Lunex for several years"; an existing InComm customer in "convenience and grocery store space" doing cell-phone top-up and other prepaid, which "about six years ago… moved into the COAM space to be the broker for the prize pay cards as well. They integrate with a lot of different kiosk vendors and **manage the settlement and the credit for the location**."
- **RWJ** — "a separate API and a pretty well-built **portal for the locations and master license holders** to log in. It manages the invoicing. They have a really full package solution."
- **Val's reaction to being a broker at all was negative, twice.** "I'm reconsidering… **It's a lot of very, very little money for a lot of risk**," and "A lot of risk for us… very no reward." That is the same arithmetic behind [[wiki/decisions/2026-08-31-transactional-equipment-only-with-location-exclusivity.md]].

Both brokers are already known to the corpus from the Jul-2025 and Jul-2026 InComm sessions on [[wiki/organizations/incom.md]]; **Darren Lu** is the first named principal for Lunex.

## Open commitments

- [ ] **InComm** — send the card-to-machine product deck to [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "**I'm gonna send the deck to [Andrei] now, so I don't forget**" *(the transcript renders the name "under"; the derived notes read it as Andrei)* — due immediately (Sept 2 2026) — [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]] [[raw/Meeting_Notes_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val]] / [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — pursue the "JVL as the processor" path InComm conceded might exist; it removes the location-enrolment problem entirely — due unspecified — [[raw/Meeting_Notes_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
- [ ] **InComm** — introduce Val to the two settlement brokers, Lunex Telecom (Darren Lu) and RWJ — due unspecified; Val is lukewarm on the broker role — [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]] [[raw/Meeting_Notes_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]

## Open questions

- **What is JVL's actual revenue share?** Nobody at the table knew; 50 basis points was offered as "somewhere to start," with the rest split between Nuvei and Mastercard. Val said he would ask **Camille** — [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
- **Can JVL enrol locations on their behalf, or become the processor, before launch?** Val asked "Can we do it for all the locations?" and got the launch design restated rather than an answer — [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
- **How does the remittance obligation work in practice** — if JVL processes, it must return the loaded amount to the location's account daily. Mechanism, timing and who carries the float are not addressed — [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]

**§15.8:** clear — card fees, basis-point splits, device prices and programme economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
- [[raw/Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026.md]]
