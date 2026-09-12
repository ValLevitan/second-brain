---
type: decision
title: Work around ARC's kiosk lock-in by swapping the PC board and stripping the per-machine printers — and route the proposal through CEO David Sloan, never directly to the kiosk vendor
date: 2026-08-31
aliases: [ARC kiosk conversion, kiosk PC board swap, throw away the board, route through David Sloan, do not approach Bill, barcode readers instead of printers]
source-count: 4
status: active
open-commitments: 1
open-questions: 2
---

# Convert ARC's kiosks rather than replace them — and go through the CEO, not the vendor

Two linked calls taken at the [[wiki/meetings/2026-08-31-arc-gaming-transactional-demo-class-a.md|Aug 31 2026 ARC Gaming demo]]: **what** JVL proposes to [[wiki/organizations/arc-gaming.md|ARC]], and — more consequentially — **who it must be proposed to**. [[raw/Meeting_Notes_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

## The constraint being worked around

ARC is locked into a ~20-year kiosk agreement a previous ARC CEO signed with his own other company, which ARC cannot exit. [[wiki/people/georgios-zazanis.md|Zazanis]]: "**One thing that will never happen is that we will never get out of what we have currently today.** That is the key. So whatever we do, **we have to build on top of it**." Full account on [[wiki/organizations/arc-gaming.md]]. [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

## What was decided — the technical shape

[[wiki/people/val-levitan.md|Val]]'s proposal, stated twice in the meeting:

- **Keep the kiosk shell, replace its brain.** "I have a better idea. **Keep your kiosk the way it is. I'll throw away the board inside and put my own board.** You throw away your printers. You don't need any. We'll give you those sensors, and you're in business. I'll process everything online." And again, itemising what the shell already has: "your kiosk has a bill acceptor. It has a card dispenser. It has a touch screen. It has a screen and printer. Does it? **It's driven by a PC board. We'll take the PC board and throw it in the garbage. We'll put a new PC board and convert it to the system.**" [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- **Strip the per-machine TITO printers; add one printer to the kiosk.** "We are taking the printer. We're installing **barcode readers**… Generates the ticket, but there's no printer. **We can add a printer into your kiosk.** Your kiosk has a barcode reader and it has a card dispenser, but it doesn't have a printer. **We removed six printers, so who cares?** We can take one printer and put it in here." The commercial sweetener: "You can sell printers. There's a market for it." [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- **One printer per location is the design goal**, articulated by the JVL voice presenting the device flow (**Speaker 3**; unnamed in both sources, read as [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] from role — an inference): "**Only one printer in the location, no jamming anywhere.** Now we can move to another machine through the same port." The ticket carries the wallet rather than the cash: "the ticket itself is a **carrier of an electronic wallet**. Money is on the electronic wallet of the player." Redemption stays flexible — "you can use either keyless or a card" — and can be self-service: "it can also be self-service, so the cashier has no burden." Device architecture on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- **The alternative — an API integration with the incumbent — was raised and is second-best.** Speaker 3: "**if the kiosk developers are open to give us access to the API**, all we do is integrate ports into game machines and make sure that our protocol creates tickets that work with a kiosk." Val's board-swap answer ("I have a better idea") is explicitly the version that does **not** need the vendor's cooperation: "**We don't need your developers.**" [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

## What was decided — the routing, and why it matters more

Val offered to call the kiosk vendor himself: "maybe **Bill** says he's willing to cooperate. I can talk to Bill. I know him very well. I can call Bill and say, 'Bill, I know that you sold. You have your monopoly on Arc. Why don't we work a deal together?'" [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

Zazanis blocked it, and gave the reason:

> "I'm afraid that if he [sees] the idea, he will say no and go and do it. He will… he cannot use it the moment somebody understands it and sees the value. **He's gonna do it**… He would say no to you, and the next thing I [hear from] David… **Has to come from David. David has to tell Bill. Bill, you need to work with[them] on this solution. Guys, figure it out together and see how you can use their system.**" [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

So the decision as the notes record it: "JVL to propose converting ARC's kiosks (JVL PC board) and eliminating per-machine printers — **route the proposal through CEO David Sloan, never directly to Bill**." [[raw/Meeting_Notes_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

Two facts make the routing non-optional rather than merely polite: **David Sloan is a long-standing friend of Bill's** (Val: "The Sloan… Is friends with Bill. For years"), and Zazanis reports Bill never refuses him outright but does not deliver either — "he never says no to me. Another two are still trying to fix our [card system]." [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

## The angle Zazanis suggested JVL lead with

Not the hardware — the data. "The kiosk keeps… all the transactions [that] go in the kiosk. He has a database [of] all of the financial activities. **Tell him we can process them online.**" [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]

## Sept 8 2026 — the route opens: Zazanis makes the introduction and steps aside

Eight days later, at the [[wiki/meetings/2026-09-08-arc-gaming-bundle-sanity-check-and-david-sloan-intro.md|Sept-8 ARC call]], the channel this ruling depends on was actually opened. Zazanis: "**I said to David, you know, Val wants to talk to you. He will reach out to you**… So **reach out to him. He's expecting you**," and — the change from Aug 31 — "**I didn't want to be in the middle of your discussions.**" Ruling: [[wiki/decisions/2026-09-08-val-approaches-david-sloan-directly-with-the-bundle-offer.md]]; the man himself on [[wiki/people/david-sloan.md]]. [[raw/Meeting_Transcript_ARC_Gaming_Vertical_Screen_Bundle_Offer_and_David_Intro-September-8-2026.md]]

**This does not discharge the commitment below.** What Val asked about taking to Sloan on Sept 8 was the **Georgia bundle offer**, not the kiosk board-swap; **the board-swap, the printers and the vendor are not mentioned anywhere in the Sept-8 sources**. So the route is now live and the proposal it was built for still has not travelled it. Both open questions below are untouched. [[raw/Meeting_Transcript_ARC_Gaming_Vertical_Screen_Bundle_Offer_and_David_Intro-September-8-2026.md]]

## Sept 9 2026 — Val met Sloan and did not raise it

The route was used the next day ([[wiki/meetings/2026-09-09-arc-gaming-backend-displacement-negotiation.md|Sept-9 4:35 PM]]) and **the kiosk board-swap was not put to him.** What travelled instead was the Georgia bundle and the [[wiki/decisions/2026-09-09-val-discloses-the-incomm-displacement-intent-to-arcs-ceo.md|InComm displacement disclosure]]; **the board, the printers and the barcode readers are not mentioned anywhere in either Sept-9 source.** [[raw/Meeting_Transcript_ARC_Gaming_Backend_Displacement_Negotiation-September-9-2026.md]]

**What the meeting did add is the vendor's own side of the relationship, from the CEO rather than the COO** — and it makes the second open question below sharper rather than answering it. Sloan and [[wiki/people/bill.md|Bill]] "**have been partners**"; Bill "**[is] running a kiosk company**"; and on service, "**I can [pick up] the phone to get anything changed on the kiosk.**" A satisfied customer with a personal line to his vendor is a harder sell for a board swap than a locked-in one. [[raw/Meeting_Transcript_ARC_Gaming_Backend_Displacement_Negotiation-September-9-2026.md]]

**And a new fact that may overtake this ruling entirely:** asked whether Bill is working on anything of the same nature as JVL's back-end intent, Sloan said "**That he's looking at different things because I've asked**" and "**I think he is working on a solution.**" Val's response was to offer to withdraw from ARC altogether — "if Bill is on it and you're friends with Bill, then I shouldn't be here" — which would moot this decision. **Nothing was settled.** See [[wiki/people/bill.md]] and [[wiki/decisions/2026-09-09-arc-account-exclusivity-sought-and-not-obtained.md]]. [[raw/Meeting_Transcript_ARC_Gaming_Backend_Displacement_Negotiation-September-9-2026.md]]

## Open commitments

- [ ] [[wiki/people/val-levitan.md|Val]] / [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — put the kiosk-conversion proposal together and route it via CEO David Sloan — due unspecified. *(Sept 8 2026: the introduction to Sloan has been made and Val is to initiate contact — but the kiosk-conversion proposal itself is not mentioned in that source. **Sept 9 2026: Val met Sloan and did not raise it.** Still open.)* — [[raw/Meeting_Notes_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]] [[raw/Meeting_Transcript_ARC_Gaming_Vertical_Screen_Bundle_Offer_and_David_Intro-September-8-2026.md]]

## Open questions

- **Does the kiosk hardware actually support what the swap assumes?** Zazanis corrected Val's inventory once already — the kiosks "[do not] accept money. [They] only issue vouchers… accept the vouchers and dispense the card" — so the bill acceptor Val listed may not be there. Not resolved in the meeting. [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- **Will David Sloan carry it to Bill at all?** The friendship that makes him the only viable route is also the reason the request may not be made. Zazanis on his own past attempts: "if I say this sucks, the other guy says George. It is what it is. Find the solution." **Sept 9 2026 leaves it untested — Val sat with Sloan for the whole meeting and never asked.** [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]] [[raw/Meeting_Transcript_ARC_Gaming_Backend_Displacement_Negotiation-September-9-2026.md]]

**§15.8:** clear — equipment, vendor and per-machine economics only; no named-person compensation.

## Sources

- [[raw/Meeting_Notes_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- [[raw/Meeting_Transcript_ARC_Gaming_Backend_Displacement_Negotiation-September-9-2026.md]]
- [[raw/Meeting_Transcript_ARC_Gaming_Transactional_Demo_and_Class_A-August-31-2026.md]]
- [[raw/Meeting_Transcript_ARC_Gaming_Vertical_Screen_Bundle_Offer_and_David_Intro-September-8-2026.md]]
