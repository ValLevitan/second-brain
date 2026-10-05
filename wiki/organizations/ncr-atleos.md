---
type: organization
title: NCR Atleos (ReadyCode cardless ATM network)
date: 2026-09-22
aliases: [NCR Atleos, NCR, NCRA, ReadyCode, Ready Code, Redigo, ReadyGo, ReadyCo, NCR Outlets, National Cash Register, Cardtronics, Waypoint, pre-staged transaction, PlayStation transaction, mini network, surcharge-free network, all point surcharge free]
source-count: 4
open-commitments: 5
open-questions: 5
disambiguation: "NCR Atleos = the ATM-network company (ReadyCode cardless cash in / cash out). An earlier transcript's 'NCR/Cruz' was a garble for NTS / Ryan Cruz (see wiki/organizations/nts-nebraska-technical-services.md) — not this company. The NCR 'dispenser' price on wiki/topics/flexpay-business-architecture-payout-devices.md refers to NCR as a maker of cash dispensers, not to this network deal."
---

# NCR Atleos (ReadyCode cardless ATM network)

NCR Atleos is an ATM company. It sells **ReadyCode**, a cardless way for a partner's customers to take cash out of, or put cash into, its ATMs. [[wiki/people/val-levitan.md|Val]] met it on **Sept 22 2026** as a possible way to pay Georgia amusement players that does not depend on [[wiki/organizations/incom.md|InComm]] ([[wiki/meetings/2026-09-22-ncr-atleos-readycode-cardless-atm-payout.md]]). It was a first call. No deal and no price were agreed. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## Who they are (as told on Sept 22 2026)

- **Company history, in the rep's words.** "about eight years ago, they bought out **Cardtronics**. NCR, obviously **National Cash Register**, they've been around for 140 years." The combination later split ("Wall Street didn't eventually find that very attractive… eventually, that split"). [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Being bought by Brinks.** "now we've been, you know, bought out by **Brinks**, and that transaction is in flight… everything's been approved, and we expect… in the new year… maybe some logo changes at some point, but **name changes for sure**." So the name on this page may change. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Business lines.** The ATM side, with a fintech side and a banking / commercial-banking side. Val confirmed this is the NCR "that manufactures cash related equipment". [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

### People met (external contacts, no individual pages)

- **Carlos** — commercial rep for ReadyCode; runs the fintech portfolio for surcharge-free partners (transcribed "all point surcharge free customers"); "a little bit over four years" with the company. Surname **Kalinchuk** comes only from the calendar invite quoted in the derived notes; it is not spoken in the transcript. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]] [[raw/Meeting_Notes_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Sean** (surname not stated) — product manager for the partner cash-out solution, transcribed as "**Waypoint**" (name not verified). Not [[wiki/people/sean-fellows.md|Sean Fellows]] or [[wiki/people/sean-riley.md|Sean Riley]] — resolved by context (NCR Atleos product role). [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## How ReadyCode works

- **No card.** The partner's own app creates the code. Sean's walk-through: the player picks the ReadyCode button in the app, enters an amount (his example: $60 of a $200 balance), and "your app will actually generate an **eight-digit code**". [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **At the ATM.** The player enters "an account number or a phone number", then the code. The ATM checks with the partner's API: "with this phone number and this code, what is the value?" The player then presses confirm; "they cannot modify" the amount. Carlos called it "two-point authentication… via your phone number, and then via the code". [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Pre-staged.** "it's a **pre-staged transaction**." The code "is valid for as long as you can make it for until it's redeemed, or you can give it a time window of like 24 hours". Amounts mentioned: "from twenty dollars all the way to… four hundred dollars", with higher or lower possible. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Cash in works the same way,** with its own code. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Back end only, under the partner's brand.** "They put their own brand. We're agnostic… we do that for you know, DoorDash or Uber or whoever." ReadyCode has **no app of its own**: "We don't have an app." To use it, JVL's app would integrate with their API. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **They hold no player data.** "We don't have the customer's information. We hold no information. They're simply redeeming the code on our network." [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## The network

- **~30,000 ATMs for cash out** ("When I first started, there was like seventeen thousand. Now there's almost thirty thousand"), and "around **thirty eight hundred** machines that have cash in capability". [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Georgia: "about a thousand thirty-two machines"** (Sean). [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Traffic is concentrated.** "eighty percent of our traffic for our network happens in those little areas" — the cash-in cities on Carlos's map (Seattle, Los Angeles, Miami, Houston, Dallas, New York). Of Atlanta: "we do a lot of business in Atlanta." [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Locator API.** Finds the nearest machine by address, latitude/longitude or zip code. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Only their own machines.** Asked if JVL could add "two thousand ATM machines of my own" in Georgia, Carlos said "It has to be our machines, just because it's a regulated transaction through the FDIC." They do take on "mini networks" on their carded surcharge-free product, but not yet on ReadyCode. He will find out. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **How old ReadyCode is — unclear.** Carlos said "This product's only been around for five years commercially. It's been around for about three years" in one breath, and earlier "what we also developed here in the last five years". The derived notes say three years. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## Money movement

- **Two FBO ("for benefit of") accounts** set up by the partner — one for cash in, one for cash out. The code's amount is pulled from the cash-out account and held. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Daily settlement.** "we have to settle daily… by one thirty every day we settle". Sean: for cash in, "the next business day we will transfer funds to your bank account… We will do an ACH transfer"; for cash out, "we would then pull funds from your bank". [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## Price (a ballpark only, given under pressure)

Carlos first refused — "We haven't dived into the commercials" — then gave numbers when Val asked for a ballpark: [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

- **Withdrawal: "about two seventy five"** ($2.75).
- **Deposit: a range, stated twice and not the same way.** First: "as low as a you know a dollar ten or eighty five cents, or it can be as high as you know three dollars". Then: "between a dollar twenty-five to you know four dollars". Priced as "transaction cost plus… interchange"; it rises with the maximum amount accepted, because "the more money they put in… the more times we have to send trucks to go pick up the cash". *(The derived notes merge these into "$0.85 to $4.00".)*
- **Cash handling is inside the price.** Val pressed on whether filling and emptying the ATMs costs extra. Carlos: "That's included in that dollar amount… 275… all of that is included." And: "There's not a monthly fee that's set. It's based off of transaction."
- **No fee at the machine.** It is a surcharge-free network. The partner chooses: absorb the cost, give one free transaction a month and charge after, or charge every time. The player never sees the fee at the ATM; it is added to the pre-staged amount — with a $5 fee, "that sixty dollars… would be a pre-staged sixty-five dollar transaction". *(The $5 was Val's own placeholder — "let's call it five dollars for combined cost" — not a quoted price.)*
- **Their comparison:** a Green Dot cash-in costs "like five dollars and fifty cents" on average, with a mixed customer experience.
- **No per-location data.** Val asked many times what a typical ATM or location transacts. Carlos: "We don't even have that information", "we don't do it by location. We just do it by customer", and such data would never be shared. He asked instead for JVL's projections at "12 months… 24 months and 36 months". Val: his Georgia volume is "Zero… It's a new legislation." Val: "I disagree with you, but I mean, it's your business."

## Relationship with InComm

- **InComm already uses them.** "They do business with us… They have our surcharge-free platform today… They transact on our ATMs surcharge-free today." Carlos called this public knowledge. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Confidential, and no talks with InComm about JVL.** Val asked if the call would reach InComm; Carlos: "No, we sign an NDA." And: "we've had no discussions with with them in relation to your business whatsoever." [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- How InComm's card-to-ATM payout works, as Val explained it to them, is on [[wiki/organizations/incom.md]] (Sept 22).

## Where JVL stands with them

- **Val needs a card.** When Carlos began selling the cardless benefit: "I need a card… The law says you must have a card." Asked later, he softened it: "I cannot say it with hundred percent reliance", only that InComm, with "maybe more than two thirds of the market", issues cards. So whether cardless is even legal in Georgia is open, and Sean offered to ask his compliance department. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Carlos's pitch:** ReadyCode as one "menu option" in a future JVL app, next to the card, not a replacement. [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **JVL's route to the player** is the AFT insert and a JVL app — see [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 22). [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- **Next step:** a commercial call. Carlos: "I'll meet with with our internal teams… That's the next discussion. It's a commercial discussion." [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## Sept 30 2026 — named by Val as an InComm competitor "being purchased right now by Brinks" (as said, not checked)

On the [[wiki/meetings/2026-09-30-larry-sharon-single-entity-jv-and-100-machine-pilot.md|Sept-30 8:42 AM call]] with [[wiki/people/larry-sharon.md|Larry Sharon]], when Larry proposed asking InComm to finance the JV, Val named NCR as one of InComm's competitors: "another one is you will know that company for sure called NCR. Okay. NCR is being purchased right now by Brinks. Okay. Because they shifted more more aligned with my business that I'm building now. Okay. They have actually a product that we might even bring on board afterwards. I spoke." Whether "NCR" here means NCR Atleos (this page) or another NCR company is not said; the Brinks purchase is recorded as Val's statement, not verified. The "product" is by context ReadyCode (see above) — **inference**. See [[wiki/organizations/incom.md]] (Sept 30) [[raw/Meeting_Transcript_Larry_Sharon_Single_Entity_JV_and_100_Machine_Pilot-September-30-2026.md]].

## History

- **Jul 1 2025 — InComm's own NCR deal.** At the Toronto product-strategy meeting, InComm's John described a cash-pickup code printed on the game receipt and collected at an ATM, with a deal "signed last week with NCR" (see [[wiki/organizations/incom.md]], July 1–2 2025). The Sept 22 2026 call does not mention this deal. [[raw/incomm_product_discussion-july-1-2025-4.md]]

## Open commitments

- [ ] Carlos (NCR Atleos) — send Val the ReadyCode deck — due unspecified — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [ ] Carlos (NCR Atleos) — take JVL's case to the internal team and come back with a commercial proposal for Georgia — due next call — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [ ] Carlos (NCR Atleos) — give a more specific deposit price ("let me take back what you shared and give you more of a specific dollar amount") — due next call — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [ ] Carlos (NCR Atleos) — find out whether JVL's own ATMs could run as a mini network on ReadyCode — due next call — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [ ] Sean (NCR Atleos) — ask his compliance department whether Georgia requires a card or allows cardless — due unspecified — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

## Open questions

- Does Georgia law require a physical card, or is a cardless payout allowed? Val first said a card is required, then said he could not say it with full certainty — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- What will ReadyCode actually cost JVL? Only a $2.75 withdrawal ballpark and two different deposit ranges exist — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- Could JVL put its own machines on the network as a mini network? — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- Where will JVL get per-location volume figures to build the projections NCR Atleos asked for? Carlos will not supply them — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- How old is ReadyCode commercially — three years or five? Carlos said both — [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]

**§15.8:** clear — product, network and price terms only. **§15 #9:** clear — no account, phone or registration numbers recorded; the rep's email in the notes is not copied.

## Sources

- [[raw/Meeting_Notes_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [[raw/Meeting_Transcript_NCR_Atleos_ReadyCode_Cardless_ATM_Payout_Architecture-September-22-2026.md]]
- [[raw/incomm_product_discussion-july-1-2025-4.md]]
- [[raw/Meeting_Transcript_Larry_Sharon_Single_Entity_JV_and_100_Machine_Pilot-September-30-2026.md]]
