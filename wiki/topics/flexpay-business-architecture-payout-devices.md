---
type: topic
title: FlexPay business architecture and the payout-device catalog
date: 2025-04-11
aliases: [FlexPay Evolution, payout tower, dispensing tower, cage POS, card-dispensing unit, temporary wallet, no-value wallet, FlexPay business model rethink]
source-count: 3
open-commitments: 4
open-questions: 3
---

# FlexPay business architecture and the payout-device catalog

In the week after the FlexSMIB architecture ruling ([[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]), Val opened a deliberate "FlexPay Evolution" strategy thread: he now believes the kiosk-centred business model may be rejected by the Georgia market, and wants JVL to **obsolete its own model before someone else does**, offering a catalog of cheaper payout devices instead of one kiosk. Sessions: Apr 8 strategy ([[wiki/meetings/2025-04-08-flexpay-evolution-strategy.md]]), Apr 8 GAMOA demo recap ([[wiki/meetings/2025-04-08-flexport-gamoa-demo-recap.md]]), Apr 11 "FlexPay Evolution 1" ([[wiki/meetings/2025-04-11-flexpay-evolution-1.md]]). The engineering/dev thread stays on [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]].

## Val's market math (Apr 8) — why the kiosk model may fail

- Georgia has "in access of 6,000 locations"; under the upcoming legislation each would need a payment kiosk "at $12,000 … it's an investment of close to $70 million," plus ~35,000 machines needing printer retrofits "at a cost of, I don't know, $500 per retrofit that's additional something like $17 million." [[raw/flex_pay_evolution-april-8-2025.md]] On Apr 11 Val rounds the market retrofit burden to "closer to a hundred million dollars" and calls a business architecture that forces a $12,000 kiosk on a five-machine location "flawed and possibly will fail." [[raw/evolution_flex_pay-april-11-2025.md]]
- Operators see no profit in complying — "they will try to do as little as possible to comply." Technically a cashier could pair a ticket number to a card manually with "a primitive application on a PC" using the Incom API — "a much, much, much … cheaper solution … and then our business model is completely ruined." [[raw/flex_pay_evolution-april-8-2025.md]]
- Constraint: the Incom agreement "puts the onus on the individual or the company who signed … to ensure that there is no fraud" — so tickets must be validated against a legitimate machine win (a mini TITO/SAS server), not typed in by hand. [[raw/flex_pay_evolution-april-8-2025.md]] For Mother-Goose-only operators, Val refuses to be the proxy signer: "I will not sign with them. I tell you one hundred percent now that I will not sign." [[raw/flex_pay_evolution-april-8-2025.md]]
- Strategic frame (Apr 11): the big competitors (Light and Wonder, IGT, Aristocrat) "are not making their own kiosks … we're not redesigning our machines"; Val wants JVL to capture the market as a technology leader with "three, four, five variations of the products, many levels of pricing" — "You cannot create a market with one style … A market is created by a catalog of products." Revenue thesis: "the bulk of our revenue will derive not from the sales of hardware, but from reoccurring revenue of processing transactions." [[raw/evolution_flex_pay-april-11-2025.md]] [[raw/flex_pay_evolution-april-8-2025.md]]

## The device variants on the table (Apr 8 + Apr 11)

1. **Cage POS (cheapest, half-automated):** attendant-facing touchscreen + scanner + magnetic card reader/loader in the cage, plus a customer-facing second display; ticket scanned, value moved to a card manually but validated against the mini SAS/TITO server. Rough component talk: "$250 altogether? Yes. Well, maybe even less" (Apr 8); Val's Apr-11 sizing: bill of material "probably … under $1,000 … a unit like this could be sold to the market at about $5,000." (The two figures describe different sketches of the same cage-POS idea — recorded as said, not reconciled.) [[raw/flex_pay_evolution-april-8-2025.md]] [[raw/evolution_flex_pay-april-11-2025.md]]
2. **Automated dispensing unit / "payout tower":** self-service card-dispensing unit next to the machines — scanner, small customer screen, large-capacity dispenser, mini TITO server inside; Val's Apr-8 cost vision "under 700 dollars, 600 dollars" (component talk: dispenser ~$350, FlexPort ~$100, enclosure ~$60 → "about 500 dollars"), vs FlexPay "considerably more." Marketing model: rent it "at a … dollar per day" on a three-year contract. On Apr 11 it becomes a slim **tower on a pedestal that fits between machines**; two towers per location give master/slave failover — "we already have this technology implemented in our embedded progressive" (Pavel). [[raw/flex_pay_evolution-april-8-2025.md]] [[raw/evolution_flex_pay-april-11-2025.md]]
3. **In-machine dispenser retrofit:** card dispenser inside each machine, routed through FlexPort — raised for completeness; Val: "Personally, I don't like it"; Juan adds many locations can't even open the master's machine door. [[raw/evolution_flex_pay-april-11-2025.md]]
4. **Cheap dual-dispenser kiosk:** Pavel's variant — strip bill acceptor and printer from the FlexPay kiosk and mount two large card dispensers ("that's how we planned the kiosk initially" — Val). [[raw/evolution_flex_pay-april-11-2025.md]]
- **Architecture dispute (open):** Val leaned on FlexPort as the embedded brain of the cheap devices ("it has all the input output … a dedicated team that could deliver the product in isolation"); Pavel dislikes the embedded route — "MBED is a difficult solution … not predictable in terms of development time" — preferring a cheap x86 platform with a 10-inch touchscreen at "the same money." Val: "whatever architectural solution … should really be dictated by you, not by me, Pavel." [[raw/flex_pay_evolution-april-8-2025.md]]
- **Direction picked (Apr 11, not a locked decision):** "I heard what Gennady said. Let's concentrate on the cheapest solution" (the cage POS), enabled by the TITO mini-server: "by the end of the month, we will have a Tito solution … The moment you have mini-server on a location, everything is open to you." New-device delivery talk: "we're talking about September of this year." Goal: "nail the business architecture by the end of this month," with a follow-up Wednesday 11 am ET and use cases written by everyone. [[raw/evolution_flex_pay-april-11-2025.md]]
- Applicability beyond Georgia (Juan/Val): the POS+TITO solution "is something we could also use in Puerto Rico … And in Nebraska? Yes … and I know for a fact that we could do it in Pennsylvania." [[raw/evolution_flex_pay-april-11-2025.md]]

## The GAMOA pulse-security objection (Apr 11)

- Juan relayed via Felipe: **Mike Patel** — rendered "the director of Gomorrah"/"Gomorrah's president" (the GAMOA operators' association; transcript garble) — "will not be buying our kiosk solution because if we offer pulse capture, it is not secure." [[raw/evolution_flex_pay-april-11-2025.md]]
- Rebuttal assembled on the call: Georgia's legacy **Mother Goose** payout system is itself pulse-based with no GLC mandate to remove it ("your regulator is saying pulses are OK"), and JVL's pulses "live only within a cabinet up to Flexport. We do not move the signal outside the cabinet" (Pavel) — arguably safer than the status quo. Juan to raise it with Patel on his Georgia trip the following week; Val: ask the masters directly "what is your dream solution here? 100%." [[raw/evolution_flex_pay-april-11-2025.md]]
- (On Apr 8 the engineering side — Pavel by adjacent context, inference — had also floated sniffing the Mother-Goose–era "Gaggle"/"yellow board" RS-485 protocol to validate printed wins on old locations; Val was skeptical — reverse-engineering a third-party protocol JVL doesn't control. Names as transcribed; unclear. [[raw/flex_pay_evolution-april-8-2025.md]])

## GAMOA demo configuration (Apr 8 recap)

- The event is "not a trade show. This is just a Gamoa meeting, two hour thing," maybe ~10 masters attending. Demo: **one JVL machine (Flex-S) with FlexPort and its bill acceptor kept**, connected via a separate router (Felipe's existing stock TP-Link, DHCP defaults) to one FlexPay; show **Diamond Link** software (Juan: "I need to push Diamond Link"); do **not** show a competitor machine, the scanner-only bracket, or TITO. [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]] The Apr-11 call adds: demonstration "next Thursday at 4 p.m." on "the 17th," showing "one V43 machine. With Diamond Link"; a device may need FedEx-ing for port reprogramming. [[raw/evolution_flex_pay-april-11-2025.md]]
- Hardware state: Felipe's current 3D-printed-plastic unit "needs to go into the garbage" (strip and keep reusable parts); he receives "two brand new units, production units, molded"; the design has capability for two bill-acceptor styles (back load and front load) though no cutouts were made. Ship plan on the call: units ship **Thursday**, arriving **Monday** (an evolution of Apr 7's "tomorrow we must ship"). [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]

## Temporary-wallet product rules (Apr 8 recap)

- The ticket is a **temporary e-wallet**, not a ticket — Val: "use it as a temporary wallet instead of a ticket. The ticket is just the wrong connotation." **No value is printed on the ticket** ("we do not print any value … It's hidden from the player") because the balance changes as the player moves between machines; the ticket carries **two counters** — playable credits and cashed/winnings value — and **only winnings can be redeemed to the prepaid MasterCard** ("by legislation, you can only convert credits won"). FlexPay shows both values; FlexPort shows only the machine-chargeable value. [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- **Scope gap found — the no-value wallet:** Felipe's use case — a player walks in with "his last and only $20," feeds the machine directly, wins, and has no wallet to carry the winnings. Fix direction: let FlexPay "print a no-value temporary wallet"; Pavel's variant: a "generate a new ticket" button at the machine with a PIN, printing at FlexPay. Open problems: blank-ticket spam at the kiosk, and collisions when the FlexPay is occupied. "That's a scope [gap] that we identified right now … implement it for the beta version testing," not for the show. [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- **Wallet validity period is unsettled:** Pavel mentioned tickets reusable "within 30 days"; Juan pushed back that a prior conversation had said as low as 24 hours (small operators' book-balancing; database size) — "we need feedback from the masters on that one." [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- Player-anonymity stance (Apr 8 strategy): most route players are anonymous and won't give a phone number, so a phone/e-wallet-registration model "I don't see it being a business model, at least from the start" (Val); the missing ingredient is a card usable for betting inside the machines, which "Incom promised" later this year (see [[wiki/organizations/incom.md]]). [[raw/flex_pay_evolution-april-8-2025.md]]

## Incom threads picked up in this series

- **Card-back-into-machine / Visa:** the Georgia COAM market complains that loading winnings on a prepaid MasterCard "takes all this winnings out of the immediate circulation of the gaming business"; Incom "is in talks with Visa" for a card the machine can validate, where Visa's ~3% fee could be made manageable if Incom runs the banking cycle internally — making JVL "a reoccurring partner." [[raw/evolution_flex_pay-april-11-2025.md]]
- **PCI-compliant optical scanner:** per the last Incom call, the optical card scanner must be PCI-compliant for a future Incom technology; Juan to re-read the notes so the hardware dimensions allow a swap-out. [[raw/evolution_flex_pay-april-11-2025.md]]
- "John from Income" reported masters want "the automated solution so that no clerk is involved" — one of the conflicting master-preference signals (locations reportedly want the human hustle). [[raw/evolution_flex_pay-april-11-2025.md]]

## Open commitments

- [ ] Juan Martinez — dig out the IGT-published TITO spec + the Bally handheld-scanner model, and confirm the TITO barcode encoding (a "code 205" name was spotted on-call, as transcribed) so a proper optical sensor can be chosen — due before the Wednesday follow-up — [[raw/evolution_flex_pay-april-11-2025.md]]
- [ ] Juan Martinez — on the Georgia trip, ask masters (and locations) their "dream solution," incl. raising the pulse-security rebuttal with Mike Patel — due trip week of ~Apr 14 — [[raw/evolution_flex_pay-april-11-2025.md]]
- [ ] Val — circulate the Wednesday 11 am ET FlexPay-Evolution e-vite with this recording, plus draft use cases — due ~Apr 14 — [[raw/evolution_flex_pay-april-11-2025.md]]
- [ ] All attendees — write down use cases / user experiences for the payout-device system before the Wednesday session — due ~Apr 16 — [[raw/evolution_flex_pay-april-11-2025.md]]

## Open questions

- Where does the redemption device belong — behind the cage or self-service on the floor? Val: "it's to be decided"; he doubts fully self-serve ("If this were possible, then Amazon self-checkout stores would prosper everywhere"). — [[raw/flex_pay_evolution-april-8-2025.md]]
- Wallet validity window: 30 days vs ~24 hours — needs master feedback. — [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- Can JVL's cage software run on a location's existing POS hardware? Complicated by mixed OSes and the player-PIN entry need — left open. — [[raw/evolution_flex_pay-april-11-2025.md]]

## Sources

- [[raw/flex_pay_evolution-april-8-2025.md]]
- [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- [[raw/evolution_flex_pay-april-11-2025.md]]
