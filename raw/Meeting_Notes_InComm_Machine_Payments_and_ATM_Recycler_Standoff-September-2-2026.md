# Meeting Summary — InComm lunch: card-to-machine payments, and InComm telling Val his cash recycler would end the partnership

**Date:** September 2, 2026, ~11:55 AM – 2:02 PM Eastern
**Duration:** ~2 hours 7 minutes (working lunch, Lebanese/West Indian restaurant)
**Attendees:** Val Levitan, Andrei Klimovich, one further JVL colleague; from InComm — a commercial lead (ex-United Gaming, ex-Home Depot asset protection), a product/regulatory lead, and a third colleague. Adam and John referenced but not present.
**Location:** Restaurant near Lawrenceville
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar match:** none found on val@jvl.ca — filed on content alone

**Raw transcript:** [[Meeting_Transcript_InComm_Machine_Payments_and_ATM_Recycler_Standoff-September-2-2026]]
**Related:** [[Meeting_Notes_Billy_Liu_PlayPay_Partnership_Deep_Dive-September-2-2026]] (same day) · [[Meeting_Notes_InComm_Skill_Pay_ATM_Guidance-August-26-2026]] · [[Meeting_Notes_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026]]

## Summary

The most consequential meeting in this batch. It has two halves: a product briefing that is genuinely useful to JVL, and a confrontation in which InComm told Val his cash-recycler ATM plan would end their partnership.

### The new product — card-to-machine payments

InComm is finishing internal testing on a product that lets a player load credits from a prize card **back into a game machine**, and hoped to go live by the end of September. The mechanism matters: the barcode on the back of the card carries a **Van 19** string, meaningless outside InComm, which InComm resolves and passes to a processor. **The kiosk and the game machine never touch PCI data** — solving the problem that ~50,000 legacy Georgia machines are not PCI compliant and would otherwise each need a card reader. A $40 barcode scanner replaces a $300 card reader.

- **Fee: 5%, capped at $50 per transaction, paid by the player.** No discounts at launch. Typical purchases are $10–$20 even from a $300 card; InComm sees 20–60% of gift-card activations going back into the game.
- **The location is the merchant of record** and must enrol with the processor. Val objected hard: locations are incapable of enrolling, and equipment moves — "Today I'm in this location. Tomorrow I'm not. The contract finished. The machine is no longer there." His counter-position: **JVL should be the processor**, offering it with its own equipment. The InComm lead conceded he was "the second partner that's asked that question" and "I think there's a path there."
- Val's revenue share was unknown to the people in the room; a starting point of **50 basis points** was floated.
- Two settlement brokers were offered as introductions: **Lunex Telecom** (Darren Lu — cell top-up and prepaid, moved into COAM about six years ago) and **RWJ** (separate API, portal for locations and master licence holders, handles invoicing). Val's reaction to becoming a broker himself was negative: *"It's a lot of very, very little money for a lot of risk."*
- **Settlement point Val initially disputed and then accepted:** when a card funds a machine, the loaded amount must still reach the location's account, because the location owes the Lottery on the cash-in. InComm walked him through it; Val's objection was that the location no longer physically holds the money, and the resolution is that JVL would have to remit to the location.

Background given: cards are issued through **Sutton Bank** (Ohio) on the **Mastercard** network with Pulse as backup debit; the black/blue card difference is a back-end funding-structure and regulatory distinction invisible to the consumer. Every product change needs approval up a triple chain — InComm to Sutton to Mastercard — which is why it takes so long, and they have had to educate Mastercard about the Georgia COAM market from scratch. ATM access uses **MoneyPass** ($2.50 transaction fee, up to $600, no surcharge on-network) chosen for its convenience-store footprint; **AllPoint** is the other large network but sits in CVS and Target.

### The confrontation — Val's cash recycler

Val laid out his ATM concept and, unusually, gave his credentials first: he founded **CashCode in 1990**, sold it to **CPI** (which then acquired MEI, formerly Mars Electronics), and sat on the board of the **Gaming Standards Association in Las Vegas for six years (2000–2006)** writing the system-to-peripheral protocol standards. CashCode's killer product was **bill-to-bill** — a bill hopper replacing the old coin hopper — so he understands bill dispensing intimately.

His proposal: the most expensive part of any ATM is the **refill cycle**. Build a device that takes bills in, sorts them into **recycling cassettes**, holds the float, and dispenses from it — so the operator never pays an armoured-car refill and pockets the ATM charges instead. He described the mechanism in detail (bills wound between two tapes like a reel-to-reel recorder rather than stacked, so worn bills work), and noted the drop cassette holds the bulk of the money separately from the recycling cassettes. He was emphatic about intent: *"This is not about politics, and this is not about beating the law. This is about me capitalizing on technology, and my goal is to sell technology."*

**InComm's answer was no.** Their reasoning, delivered candidly:

- Since Val's earlier conversations the regulatory climate has hardened. There has been significant interaction between InComm, the Lottery, the Governor's office and the Attorney General's office, and the battle lines have moved.
- At the trade show, **Joe Kim (the Lottery's counsel) noticed Val's product**, noticed Billy Liu's, and noticed other kiosk vendors advertising ATM functionality — and gave a speech that afternoon which InComm reads as saying two things: **you may not exchange the gift card for cash**, and **he does not want workflows that funnel redemption toward a cash destination**.
- Therefore InComm "would struggle to see our partnership" continue if JVL pushes ATM functionality closer to COAM. Even Val's fallback — dispense the card from a separate station ten steps from the ATM — was rejected: *"We don't believe that would be received very well in the current climate."*
- Their stated motive was risk, not competition: this programme is a small part of InComm's business and they will not risk the licence for it. *"I don't want you to work with my competitors. I'm just saying we can't do that in association with our products."*

**Val's grievance, stated plainly.** He pointed out that two years ago, in a one-on-one with John, InComm had validated the whole business model, told him it was a great product and pushed him to invest — and he now sits on that investment unable to capitalise on it. *"You made me spend a lot of money, a lot of money, on building something that you're now saying that it's not going to go."* The InComm lead apologised for the shift while attributing it to Georgia's regulatory evolution.

**The letter dispute.** InComm asked Val to write a note confirming he is not doing cash recycling in association with the Skill Pay card. Val refused to write it, and drew a careful distinction he repeated several times: InComm may ask whether the screens he submitted do what he says they do, and he will answer honestly — but they may not ask him to promise not to build something he never submitted. *"You should not ask me to guarantee something else."* He reminded them he has in-house counsel too. The compromise landed on InComm writing to confirm that the features seen on the show floor are not associated with this solution, which Val said was a fair question to ask.

Val closed conciliatory — *"I'm more of a lover than a fighter"* — arguing both sides should work toward the business rather than shutting it down, and adding that no Georgia regulator actually wants him to be loud and ugly.

### The other proposal — replace PAX

Late in the meeting Val made a commercial offer that InComm did not reject. InComm gives away **PAX A80 devices** (retail ~$200, ~5,000 given away since March) that do nothing but activate cards. Val's argument: PAX leaves MudaGoose in place, which means the location can bypass the whole mechanism and not pay InComm. **JVL's IQ point-of-sale can remove MudaGoose**, rewire the location, and give JVL the ability to shut the terminal off if the location does not pay — solving InComm's collection problem. His offer: *"Buy my device instead of PAX. You'll pay the same amount of money."* JVL would upsell the operator on machines and give the ports away.

InComm's reply was to decline buying the hardware but to offer support: they would help lower the location's investment and pay a bounty, **especially for net-new locations**, since they hold ~70% market share and the last 30% is hard for them to reach. Val's counter-argument was the throughput problem: in that 70% they are issuing only **one and a half cards a day**, and he pressed them on where the other $900 per machine per day goes if the Lottery paid out $5 billion. He also raised, unprompted, that JVL's ports behave like a Class III player-tracking system and could issue **promo credits** on the SAS 2 port — free play registering on a promo meter outside the counters, which he acknowledged might alarm the Lottery.

### Market intelligence gathered

- **United Gaming:** rumours of financial trouble. Their original ~$860M–$1B credit line (2023) from **MGG** (private equity) was used to acquire competitors and routes; MGG facilitated a refinance and **Fortress** came in, so lenders now hold more power. Purchasing has moved from informal decisions to a **quarterly capex budget set by the lenders**, executed by CFO **Jason Flurry** and COO **Marsha Hayward** (ex-Scientific Games). Bunty remains "the spine". The InComm lead's advice: get time with Flurry and Hayward, though Hayward is hard to reach and does not engage the market.
- **Georgia operator landscape:** beyond the association, the larger operations named were United, Ultra and others, with very different strategies.
- **Culture:** a tight community that makes decisions collectively over WhatsApp, with little analytical rigour — a view Val strongly shares. His own line: *"in our industry we say that operators make money in spite of themselves."* Both sides agreed products get branded good or bad without evidence, and that operators will not tune machines the way a casino floor does.
- **Val's own admission, worth noting:** JVL has service-level relationships but **no top-level relationships** in Georgia — "like none, zero" — and no senior management in place who can build them. He called it very problematic and very concerning.
- **Other markets discussed:** Nebraska and South Dakota (Class III VLT with a central system; every location has an ATM, ten machines per municipal address, operators buy corners with four entrances and put a bar in the middle). Florida is Seminole Class III — six or seven casinos, close to $3 billion, ~6% tax, machines supplied on participation, and they will never allow distributed gaming.

## Decisions Made

- **InComm will not support JVL's cash-recycler ATM** in association with their products, and said the partnership would struggle if JVL proceeds. Val accepted the constraint for now — "it leaves me with no choice but not to do it" — without conceding the point.
- **Val refused to write a letter** promising not to build cash recycling. Agreed instead that InComm may write asking him to confirm the show-floor features are not associated with this solution.
- **The card-to-machine product launches with the location as merchant of record**, 5% capped at $50, no discounts. Val's request to be the processor himself was acknowledged as a possible path, not agreed.
- **InComm declined to buy JVL's IQ device** in place of PAX, but offered a bounty and location-investment support, weighted to net-new locations.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | InComm | Send the product deck to Andrei | Immediately — "I'm gonna send the deck now, so I don't forget" | High | Card-to-machine product |
| 2 | InComm | Write to Val asking him to confirm the show-floor features are not associated with the Skill Pay solution | Open | High | The agreed alternative to Val writing a note |
| 3 | Val | Decide whether to answer that letter, having involved his own counsel | On receipt | Critical | Val: "consult your legal counsel because I have one in house too" |
| 4 | InComm | Introduce Val to the settlement brokers — Lunex Telecom (Darren Lu) and RWJ | Open | Medium | Val is lukewarm on being a broker |
| 5 | Val / Andrei | Pursue the "JVL as processor" path InComm conceded might exist | Open | High | Removes the location-enrolment problem entirely |
| 6 | Val | Get time with Jason Flurry (CFO) and Marsha Hayward (COO) at United | Open | High | Where machine purchasing decisions now sit |
| 7 | Val | Address JVL's absence of senior-level relationships in Georgia | Open | Critical | Val named it himself as very concerning |
| 8 | InComm / Val | Work out the bounty and net-new-location arrangement | Open | Medium | InComm's counter-offer to buying hardware |

## Key facts worth keeping

- **Card-to-machine:** 5% fee capped at $50, player pays; Van 19 barcode keeps machines out of PCI scope; $40 scanner vs $300 reader; ~50,000 non-PCI-compliant machines in Georgia; 20–60% of activations return to the game.
- **Issuer chain:** Sutton Bank (Ohio) → Mastercard, Pulse as backup. Every change needs InComm → Sutton → Mastercard approval.
- **ATM:** MoneyPass, $2.50, up to $600, no on-network surcharge; chosen for convenience-store footprint. AllPoint is CVS/Target.
- **PAX A80:** ~$200 retail, given away free since March, ~5,000 units; activates cards only, leaves MudaGoose in place.
- **InComm holds ~70% of the Georgia market**; issuing ~**1.5 cards per day** per location.
- **United Gaming:** MGG private equity, Fortress in on the refinance; capex now lender-set quarterly; CFO Jason Flurry, COO Marsha Hayward.
- **Val's history:** founded CashCode 1990, sold to CPI; GSA board Las Vegas 2000–2006, wrote the system/peripheral protocol standards.

## Flagged for Val — the strategic collision

Three positions taken this week are mutually inconsistent and need reconciling:
1. **InComm** says the partnership struggles if JVL puts ATM/cash functionality near COAM.
2. **Billy Liu (PlayPay)** wants exclusivity — no InComm, no physical card dispensing.
3. **Flex-IQ's multiple-clearinghouse capability** ([[Meeting_Notes_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026]]) was specified precisely so the operator could choose a provider other than InComm.

Separately: Val's grievance that InComm's John validated and pushed the investment two years ago is a concrete claim. If it is going to be used, the record of that conversation is worth locating now.
