# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX

**Date:** September 15, 2026, 8:03 AM - 9:44 AM Eastern
**Duration:** approximately 1 hour 41 minutes
**Attendees:** Andrei Klimovich (organiser), Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko, Andrei Bosik
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026]]
**Source meeting:** Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams

## Summary

The daily MVP1 call, this time built on the UI/UX screens Klimovich promised the day before. It settled how balances are named, walked the FlexPort and Flex IQ screen flows, and ended with Val stopping the meeting to demand the non-functional requirements in writing and fixing the plan for the rest of the week.

**JIRA linking and planning dates.** Bosik opened with questions about the report he sends. Two rules were confirmed. First, dates are always set on the lowest level of work that exists, so the roll-up never breaks: plan the capability while nothing sits under it, and the moment features appear, take the date off the capability and plan the features; when stories appear under a feature, take the date off the feature and plan the stories. Second, the link direction between capability and requirement was wrong in the tooling. Klimovich had been using "requirement implements capability"; Irina said that is backwards — a feature is implemented, and it is based on requirements. The agreed form is **capability requires requirement** (requirement *is required by* capability), and Klimovich will go through and unify every link. Bosik will correct his report the same day rather than tomorrow, after Val pressed him on the delay. Klimovich has also created the capability covering the dual-wallet logic for the MVP1 release, and requirement 1538 moves out to the new MVP2 capability as agreed the previous day.

**The balance naming decision — recorded as an ADR.** Biratko raised the confusion that has been costing the team time: redeemable money is also playable, so a screen showing "playable" and "redeemable" invites the player to add them together, which is wrong. He hit this himself building FlexPay. Klimovich first proposed splitting the problem — internal engineering terms versus what the player sees — and both Val and Biratko refused: it has to be the same everywhere, because the split is exactly what causes the confusion. The answer settled on three lines:

- **Total** — everything on the ticket, and the amount the machine loads.
- **Playable only** — the part that cannot yet be withdrawn.
- **Redeemable** — the part that can be taken out.

Playable-only plus redeemable equals total, so the arithmetic is visible and correct. Biratko noted "playable only" is the same term the SAS specification uses. For the player screen, Pavel's proposal was accepted: total in large type, the two components small underneath. Internally the two balances stay as separate counters — Chudzinau made the case that the engine must know where money came from in order to return it there when a transfer fails, and priority on withdrawal is playable first, then redeemable. Val stated on the record that this is an **architecture decision (ADR)** and must live in the repository, asking explicitly that the transcript capture it.

Klimovich worked the arithmetic through out loud and everyone confirmed it: load $20 → total 20 / playable-only 20 / redeemable 0; win $150 → total 150 / playable-only 0 / redeemable 150; cashier adds $50 → total 200 / playable-only 50 / redeemable 150; the machine always shows total.

**Promotional money — parked.** Biratko and Pavel raised promo balances, which behave differently again and move machine to machine without becoming redeemable. Val said flatly that promo will become a live topic in Georgia very soon, because hands are going away and JVL intends to push promotional specifics through FlexPort as AFT — it is in the business plan. Irina drew the line: promo is not needed by October 1, so it goes to MVP2 or MVP3. Klimovich parked it and Val agreed.

**FlexPort screens.** The idle screen changes: the optical scanner stays on permanently, the screen simply says scan your ticket or insert money, and the language choice moves to a service button in the top right that switches on the fly from any screen. Chudzinau and Bosik confirmed a permanently-live scanner is not a hardware problem — JVL's own units have run a year, and supermarket price checkers work the same way, with motion detection driving the illumination that is the part that wears. Pavel's design note was accepted: the mock-ups must be drawn at FlexPort's real screen resolution, because a finger-sized button will take a quarter of that screen.

Error and blocked states become one unified screen with different texts. Val required two distinct signals rather than one: **maintenance** (under control, JVL is working on it) and **lockout** (the location is blocked). Pavel then raised the harder case — a block coming from the Georgia Lottery, which locks the machine but not JVL's system. Val's first position was that this is not JVL's problem; Klimovich and Pavel pushed back — JVL owns the eWallet, and a player who loads money and then cannot play or get it back is JVL's problem — and Val conceded ("you are more humanitarian people than I am"). The rule is that FlexPort synchronises with the machine state as closely as possible: machine blocked, door open, cannot accept money. Pavel already has this working in the version handed to Klimovich yesterday, but has not tested it with two SAS ports connected; Biratko will help build the test cases, since machine-side tilt transmission has to be enabled.

**Spanish.** Support for Spanish is needed — some operators have locations that are effectively entirely Spanish-speaking — but not necessarily by October 1. Biratko suggested showing both languages at once; Klimovich rejected it, on the argument that the player must be walked through a new experience with the least possible friction, and two languages on screen adds analysis. Game machines themselves are not being translated.

**Timeout on collect, and unclaimed money.** Klimovich had tested current FlexPort behaviour and reported that when the timeout expires the money evaporates. Val cut in: a player can never lose their money, full stop. The agreed handling is that a timeout sends the funds to **unclaimed money**, which Val wants treated as a real regulated item — each state has its own banking regulations for when unclaimed funds can be expropriated, and some states tax them. The implementation shape agreed with Biratko is to create an eWallet, transfer the money to it, mark it unclaimed and simply not print a carrier — the same transaction that already exists, minus the print. Chudzinau would rather it were a separate entity than a wallet, because the cloud wallet arriving in the next MVP makes wallets harder to handle. Val stopped the debate: this is all long since solved outside JVL, so start with **Juan Martinez**, and if he cannot cover it, Pavel books a meeting with GLI, who will charge a consulting fee. The specification to work from is **AFT**, which covers these transactions, plus the individual states' unclaimed-money legislation. Klimovich asked whether the release can ship without this in MVP1 — Val said yes without hesitation, but it must be done soon, MVP2 or MVP3, and it is definitely not part of MVP1.

**Flex IQ — cashier flows.** Login stays a PIN, and Klimovich wants the Cancel button removed so a correct PIN logs the cashier straight in. Pavel asked about moving to six digits; both Val and Klimovich said no — the device sits behind the counter, usually behind glass, and the PIN exists to separate cashier A from cashier B for accountability, not as real access control. Val's own requirement, recorded for Chudzinau: the login method must be **selectable — PIN or magnetic stripe card** — because a magstripe is stronger access control than a PIN. He would set it up on the device itself first and move it to a phone later. Pavel raised the risk that Genadi might drop the magnetic stripe reader from Flex IQ; Val confirmed it stays, only the second screen is being covered over, and asked Pavel to remind him. The cards will arrive pre-encoded — the reader reads but does not write.

The home screen gives the cashier three routes: create wallet, view records, and reports. Scanning a player's carrier from there opens that wallet directly, showing the live balance and what can be done with it, with load and redeem as options. On redemption, the redeemable amount is now pre-filled by default as the maximum, removing an extra action.

**Receipts.** On card activation the receipt always prints, no intermediate question — it carries the claim information, the fee deducted, the amount taken off the balance, and is the player's only sight of what is left on the wallet. For a balance top-up or a wallet created at the counter, Pavel argued the receipt should be optional with the cashier asking, and Klimovich accepted: a confirmation screen, to save paper.

**Reissue versus reprint — closed.** Yesterday's parked question was settled against Klimovich. Chudzinau's argument carried: two wallets with identical barcodes is not what reissue prevents, since a ticket can be photographed either way, and reissue only complicates the transaction history when investigating what happened. Pavel and Biratko agreed. Klimovich has already changed it to **reprint** and will re-check why he originally wanted reissue. Separately, Chudzinau raised when the amount gets frozen during redemption, to stop an accomplice loading the same money onto a machine while the cashier is redeeming it. The answer: at the point the cashier enters the amount and presses continue, the system re-queries the wallet, confirms the balance is still there, and freezes it — effectively debits it — until the activation completes.

**Records and reporting.** The cashier needs to see every transaction at the location: wallet creation on both IQ and FlexPort, balance updates, money out of a machine, redemptions, and money moved from a wallet onto a machine. Bosik asked for a date/period filter and Chudzinau for a direction filter (money to the machine versus money from it); both accepted. Scanning a carrier filters the list to that wallet. Bosik also asked whether X and Z reports (standard retail cash-movement reports) apply — Klimovich did not know the term and asked him to write it up.

The one MVP1 report stays the Georgia Lottery one, which Klimovich finishes today or tomorrow. He floated an MVP2 idea: tracking the stock of blank cards at the location — the cashier enters how many arrived, the system counts issuance down, and raises a signal when stock is low so the location reorders. Chudzinau pinned the MVP1 cloud scope down to two things only: device/operator online status, and a dashboard of issued cards. Everything else, including wider statistics collected from machines over SAS, goes to MVP2/3 — though Val called that machine statistics work "our showpiece" and Klimovich agreed it is one of the sweetest pieces, to be added in stages and sold as a premium tier on the web service, while the location itself sees only a minimal operating view. Val pushed Klimovich on the operations dashboard: he cannot say abstractly that something is in MVP1 without specifying which reports. Klimovich accepted and said he will close IQ and port capabilities today, then produce the MVP1 dashboard specification within a couple of days.

**LTE modem in every device.** Bosik asked whether the location router could serve as the shared LTE modem. Val's answer was no: every device — each IQ, each kiosk, each machine — carries its own LTE modem and SIM and is self-sufficient, while still seeing the others over WiFi, because SIM cards and data are cheap. He then asked the team to think about using the multiple modems for resilience — devices that find each other over WiFi could agree a map so that if one link fails another carries the traffic. Pavel noted a machine already has two channels, FlexPort and modem, so it can still reach the server if WiFi fails.

**Val's close — non-functional requirements, in writing.** Val's last block was the sharpest part of the meeting. He listed the non-functional areas that worry him: timers, handshaking, encryption, hung states, communications and pings between devices that do not arrive, the WiFi being introduced, and unit identification numbers. His Sonos analogy made the point — devices you believe are connected quietly drop off, and JVL cannot allow that: how does a device reconnect, how does JVL find out, how is the alarm raised. Chudzinau answered that Grafana is in place and alerting could be configured in future; Val stopped him:

> If it is not written, it does not exist.

He said he is tired of hearing "we know this, we discussed it, but it is not written down" and wants it to end — especially now, when any conversation can be transcribed and turned into written requirements through Claude in very little time. Without written non-functional requirements there is no ideology, no plan, and no way to write the automated tests, so the product cannot ship. There must be an engineering ideology set from above — an architecture ideologist who dictates it — and the prose in the repository must match the capabilities and have tests against it.

**The week's plan, fixed.** Tomorrow's 8:00 AM meeting does not go to Klimovich's capabilities — it goes to the **non-functional requirements**, owned by the five named people: Dzmitry Chudzinau, Andrei Bosik, Irina Shishko, Alexander Biratko and Pavel Frolov. Wednesday, Thursday and Friday are for finishing them; Val cannot attend Thursday but will be there Friday. Klimovich uses the same time to finish and clean his capabilities and requirements. **Monday, September 21 is the deadline** — a grooming meeting that assembles the whole MVP1, functional and non-functional, running quickly through every capability with its functional and non-functional requirements already attached. All present agreed.

Klimovich also proposed making the daily call a standing practice, which was accepted.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau, Andrei Bosik, Irina Shishko, Alexander Biratko, Pavel Frolov | Write the non-functional requirements — timers, handshaking, encryption, hung states, device pings, WiFi, unit identification numbers | September 21, 2026 | Critical | Val's closing demand; without them there are no automated tests and no release |
| 2 | Andrei Klimovich | Unify every capability↔requirement link to "capability requires requirement" | Today | High | Direction was reversed; Irina corrected it |
| 3 | Andrei Klimovich | Finish and clean all capabilities and requirements for Flex IQ and FlexPort, including the transaction set | Today | High | Stated as his own commitment for the day |
| 4 | Andrei Klimovich | Produce the MVP1 operations dashboard specification — which reports it actually contains | Within a couple of days | High | Val refused an abstract "it will be in MVP1" |
| 5 | Andrei Klimovich | Finish the Georgia Lottery report | Today or tomorrow | High | The one report that must make MVP1 |
| 6 | Andrei Klimovich | Speak to Juan Martinez about unclaimed money — where the entity lives and who owns the balance | Today | High | Val named Juan as the first source of knowledge |
| 7 | Andrei Klimovich | Redraw the UI mock-ups at FlexPort's real screen resolution | Before the next review | Normal | Pavel's point that finger-sized buttons change the whole layout |
| 8 | Andrei Klimovich | Re-check why reissue was originally chosen; reprint is now the design | Not set | Normal | Already switched to reprint |
| 9 | Andrei Klimovich | Record the balance naming decision (Total / Playable only / Redeemable) as an ADR in the repository | Not set | High | Val explicitly called it an architecture decision |
| 10 | Andrei Bosik | Correct the report field interpretation and planning-date logic, and push an updated report today rather than tomorrow | Today | Normal | Val refused to wait for the daily cycle |
| 11 | Andrei Bosik | Write up what X and Z reports are and whether they apply to Flex IQ | Not set | Low | Klimovich did not know the term |
| 12 | Pavel Frolov | Test that a block arriving over one SAS port is seen, with two ports connected | Not set | Medium | Raised with Irina the same morning; untested |
| 13 | Pavel Frolov | Remind Genadi that the magnetic stripe reader stays in Flex IQ | Next conversation with Genadi | Normal | Val's request, as a precaution |
| 14 | Pavel Frolov | Book a meeting with GLI on unclaimed money if Juan cannot cover it | After Klimovich speaks to Juan | Medium | Val accepted a consulting fee would apply |
| 15 | Alexander Biratko | Help build the test cases for machine tilt and block handling over SAS | Not set | Medium | Pavel said his field experience is needed to anticipate the cases |
| 16 | Alexander Biratko | Add the missing screen showing tilts and how to resolve them on Flex IQ | Not set | Normal | He raised it himself; Val agreed |
| 17 | Dzmitry Chudzinau | Prepare the first version of Flex IQ with wallet mode for Klimovich to review | Today | Normal | So Klimovich can see which screens already exist |

## Decisions

- Balance is presented as three lines everywhere — **Total**, **Playable only**, **Redeemable** — with playable-only plus redeemable equalling total. No separate internal and player-facing vocabulary. Recorded as an ADR.
- Player screen shows total in large type, the two components small beneath it.
- Internally two balances remain, with withdrawal priority playable first, then redeemable, so failed transfers return to the right side.
- Promotional money is out of MVP1 — MVP2 or MVP3.
- FlexPort's scanner stays permanently active; the idle screen asks the player to scan or insert money; language moves to a top-right service toggle that switches on the fly.
- Error and block states share one unified screen with different texts; **maintenance** and **lockout** are two distinct signals.
- FlexPort synchronises with the machine state — machine blocked, door open, cannot accept money — because JVL owns the eWallet and the player's money.
- Timeout money goes to **unclaimed money**: create the wallet, transfer the funds, mark unclaimed, do not print a carrier. A player can never lose their money.
- Unclaimed-money handling is not required for MVP1 but must follow soon, built from the AFT specification and state legislation, starting with Juan Martinez.
- Cashier login stays a 4-digit PIN, and must become **selectable between PIN and magnetic stripe card**. The magnetic stripe reader stays in the Flex IQ hardware.
- Cancel is removed from the PIN screen — a correct PIN logs the cashier straight in.
- Redemption pre-fills the maximum redeemable amount by default.
- Card activation always prints a receipt; a balance top-up or counter-created wallet asks first.
- **Reprint, not reissue**, for a carrier that failed to print.
- The redemption amount is frozen when the cashier confirms the amount and presses continue, after a fresh balance check.
- Records show all transaction types with date/period and direction filters; scanning a carrier filters to that wallet.
- MVP1 cloud scope is exactly two things: device online status, and a dashboard of issued cards.
- Every device carries its own LTE modem and SIM — no shared router modem.
- Tomorrow's 8:00 AM meeting covers non-functional requirements, not capabilities. **Monday, September 21 is the deadline** for the full MVP1 grooming pass.
- The daily call becomes standing practice.

## Open Questions

- **Whether X and Z reports apply to Flex IQ.** Bosik to write up what they are.
- **Where the unclaimed-money entity lives and who owns the balance** — operator, GLC, location or the tax authority. Val did not know; Juan Martinez, then GLI.
- **Whether unclaimed money should be a wallet or a separate entity.** Chudzinau prefers a separate entity because the cloud wallet arrives next MVP; Biratko's wallet-without-printing is the simpler route.
- **Whether a block arriving over one SAS port is visible when two ports are connected.** Untested.
- **Which reports the MVP1 operations dashboard actually contains.** Klimovich owes the specification.
- **Whether machine statistics over SAS become a premium paid tier**, and in which MVP each block lands.
- **How WiFi resilience across multiple device modems would work** — Val asked the team to think about whether the technology allows a failover map.
- **Administrative screens** (operator mode, cashier accounts, PIN changes, WiFi setup, diagnostics, connected FlexPort list) are likely MVP2, on the assumption remote update lands.
