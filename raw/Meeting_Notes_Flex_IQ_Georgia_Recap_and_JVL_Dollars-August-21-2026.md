# Meeting Summary — Post_GOAM_show_recap (Flex IQ Georgia Recap & JVL Dollars)
**Date:** August 21, 2026, 4:01–5:45 PM Eastern
**Duration:** ~1 hour 44 minutes
**Segment:** Recording 1 — Flex transactional products. The meeting continued after a break on the slot machines with Felipe; that portion was recorded separately and is now captured as [[Meeting_Notes_Georgia_Machine_Sales_Strategy_Post_GOAM-August-21-2026]] (recording 2).
**Attendees:** Val Levitan, Andrei Klimovich, Juan Martinez, Felipe Miranda Giorgi
**Raw transcript:** [[Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026]]

## Summary

Andrei Klimovich and Felipe reported back from the Georgia GOAM trade show on the Flex transactional products — mainly Flex IQ (the small gift-card device), the Flex recycler, Flex ports, and the dispenser. Andrei left partway through; Felipe stayed for the later (separately recorded) slot-machine discussion.

**Flex IQ — market reaction.** Operators liked the design and build quality of Flex IQ, and understood the value of automatic (non-manual) transactions. But almost everyone asked for two things IQ does not do today: "replay" (letting a player move from one machine to another) and the ability to split a cash-out (part onto a gift card, the rest as cash or lottery tickets). Operators also said the current gift cards from InComm must ship **wrapped** whenever they are handled at a cashier desk (only kiosk-fed cards can be loose), and IQ cannot read a wrapped card today — its reader expects a swipe/stripe.

**Val's direction — place units, collect facts.** Val was firm and repeated it several times: he does not want to change features based on show chatter, which he called hypothetical. The job right now is to get Flex IQ into real locations (target 20–30–50 units) and collect factual complaints and data. IQ competes head-to-head with PAX (~5,000 PAX locations in Georgia) and nothing else. Feature requests (replay, split, multiple gift-card brands) are **parked** — recorded and not dismissed, but not being built yet; the team must be ready to move fast once real field data justifies a change.

**PAX and the 1.5-cards-a-day puzzle.** Val said InComm reports an average of only ~1.5 card validations per day across ~5,000 PAX locations (~7,500 cards/day). The team could not explain where the rest of the cash-out money goes — the strong suspicion is cash paid out off the books, which GLC does not enforce. Val believes InComm's PAX application (not the PAX hardware) works poorly and is used mainly because it lets locations cheat cheaply; InComm's own economics (~$450/year per device against fraud and clearing headaches) look unsustainable to him.

**Legislation note.** Reloadable gift cards became allowed for Class B machines as of July 1 (per a lottery slide Andrei and Felipe saw). InComm's current product does not support reload; this is a product limit, not a legal one.

**Barcode reader.** Because wrapped cards carry a visible barcode, Flex IQ needs to read barcodes. Val said adding a second, front-facing barcode reader is easy ("not a big deal"); the team will also test whether the existing reader can read a card inserted at an angle, and may use a USB 2D scanner as an interim fix.

**E-wallet / QR concept.** Long discussion on how to give players "replay" without Tito (paper) or the dangerous practice of sending credits back to a machine. The shared idea: convert a cash-out into a QR-code / barcode e-wallet the player carries between machines that have Flex ports installed. Val's preferred flow is to keep a bill acceptor on the machine, play, and issue the e-wallet on cash-out; Andrei and Felipe favored issuing the wallet at the cashier so the location keeps the valuable face-to-face contact with the player (upsell cigarettes, gas, etc.). No single flow was locked; all agreed the direction is ports in every machine plus a QR/e-wallet.

**Recycler.** Deferred — Val said the product is not ready and he did not want to discuss details this session. The show unit was a "make-do" build but created strong interest (Andrei: the Gamora board of directors had "dollar signs in their eyes"). Operators want to see thicker/heavier metal for security. Val said he already knows how to make it work and will.

**JVL Dollars.** Felipe found the "JVL dollars" pitch confusing at the show and suggested repackaging it or calling it a credit line. Val rejected that and defended the model in detail: physical, serialized cards with a barcode and a 12-month expiry, redeemable against any JVL product — deliberately NOT booked as an account credit, because a credit is a balance-sheet liability and the printed dollars are not. He framed it as a marketing and relationship tool (a tangible package that gets a salesperson in front of a CFO / decision-maker, not just a technician), modeled on a Miami restaurant chain's gift-dollar program. Andrei ended up agreeing with the reasoning.

**Tone note.** Val sharply rebuked Andrei for repeating (as a criticism) that the show unit's cover was 3D-printed rather than molded — Val had said several times that the production molds are ready and 3D printing was only used because there was not enough time before the show.

## Decisions Made

- **Release Flex IQ in its current configuration (no split, no replay) and focus on placing units to collect factual field data.** Feature requests are parked, not dismissed. (Decided by Val; Andrei/Juan/Felipe agreed.)
- **Next IQ steps: run one more InComm production test on a new location ID that has no invalid "N/A" character, after Pavel's fix is released, then install at the first real location (~1 week out).** (Decided by Val, Andrei, Juan)
- **Add a barcode-reading capability to Flex IQ** (second front-facing reader and/or interim USB 2D scanner) so it can activate wrapped InComm cards. (Decided by Val)
- **Keep the "JVL Dollars" model and name as designed** — physical serialized barcode cards with a 12-month expiry, redeemable against any JVL product, tracked in a simple verification database, deliberately not booked as an account credit. (Decided by Val, over Felipe's repackaging suggestion.)
- **Recycler is deferred** — not ready, not to be detailed now. (Decided by Val)
- **Texas test site secured** — 20 machines with Flex IQ, Flex Ports, and Flex Dispenser, first week of October (parked for a later conversation). (Stated by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Initiate a new InComm test session (request 3 more cards) and set up a new location ID without the invalid "N/A" character | ASAP (request now) | High | Run the actual test only after Pavel's fix is released |
| 2 | Pavel Frolov | Implement/release the fix removing the invalid "N/A" character handling | ~Tue implement, ~Wed release | High | Dependency for the IQ retest; Pavel not on this call |
| 3 | Andrei Klimovich | After a clean test, register the first real IQ location and order its first pack of cards; keep placing more units | ~1 week for first location | High | Goal is 20–50 units to get factual data |
| 4 | Andrei Klimovich + Felipe Miranda | Visit a nearby location today to observe how PAX handles wrapped gift cards (does the attendant unwrap them?) | Today, after work | Normal | Feeds the barcode-reader decision |
| 5 | Andrei Klimovich (with engineers) | Settle the barcode-reading solution (second reader / angle test / USB 2D scanner) before the first install | Before first location | Normal | Val to check with engineers on reading a card diagonally under the existing reader |
| 6 | Andrei Klimovich + Felipe Miranda | Establish a direct relationship and collect banking info with pilot locations for factual feedback | Ongoing | Normal | Felipe to introduce them to locations |
| 7 | Juan Martinez / Andrei Klimovich | Push Nathan Carver for details on the InComm invoice for the 3 test transactions (source of data, whether invoice received) | TBD | Normal | Neither has seen the invoice |
| 8 | Val Levitan | Build the JVL Dollars scheme — printed serialized barcode cards plus a simple verification database | TBD | Normal | Val's own item |

## Open Questions

- Why does card validation average only ~1.5 cards/day per PAX location, and where is the rest of the cash-out money going? (Raised by Val and Juan — unresolved; suspected off-book cash.)
- Does the market genuinely need "replay" and split, or is the demand cultural imitation? (To be answered by factual field data once units are placed.)
- Should locations be incentivized per gift card issued (e.g., a few cents each) to drive card usage? (Juan's idea — parked.)
- Exact e-wallet flow (issue at the machine on cash-out vs. at the cashier) — direction agreed, specific flow not locked.

## Dispatch Log

---
*Processed from Teams transcript on August 21, 2026 (scheduled meeting-watcher, capture-only).*
*Source meeting: Post_GOAM_show_recap — August 21, 2026*
*Capture note: This recording covers the Flex transactional-products portion only. The meeting continued after a break on the slot machines with Felipe; that was a separate recording whose transcript had only just begun processing (status "initial") at capture time and is not recoverable by the watcher's lookback. Logged in the Error Journal.*
