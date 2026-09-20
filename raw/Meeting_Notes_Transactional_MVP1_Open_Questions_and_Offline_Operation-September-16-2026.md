# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX

**Date:** September 16, 2026, 8:01 AM - 9:37 AM Eastern
**Duration:** approximately 1 hour 35 minutes
**Attendees:** Andrei Klimovich (organiser), Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko, Andrei Bosik
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026]]
**Source meeting:** Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams

## Summary

The daily MVP1 call. Irina drove it from a list she had built: about half of the MVP1 requirements still carry open questions, and open questions block the team from working with them. The meeting went through her list requirement by requirement and either answered the question, moved the requirement to MVP2, or deleted it. The big subject that came out of it was offline operation — what a location may keep doing when the internet is down.

**Klimovich's opening update.** He cleaned up the capabilities and requirements he authors and put them all into current statuses; he did not touch items authored by others and asked each author to do the same for their own. He also applied the small changes agreed on yesterday's call, including the reissue→reprint logic. He is continuing on the UI and the dashboard.

**Why the meeting happened.** Irina reported that roughly half of the requirements have open questions inside them, and as soon as Claude is asked to work with one, the open question comes straight back. The requirements have to be cleaned — either answer the question or remove it if it is no longer relevant — otherwise the work goes nowhere. Klimovich noted that some of the open questions are engineering questions he deliberately flagged as "how", not product or business decisions. Pavel suggested a filter showing the live requirements from all four authors so the team can walk one shared list; the meeting used Irina's list for today and will build the shared filter next.

**Offline operation — the main debate.** The trigger was requirement 1383: does the terminal need constant connectivity for the lease to validate? Chudzinau explained the current behaviour: Flex IQ and FlexPay pull a fresh lease date at start-up, then keep monitoring the last lease they hold; if the lease expires the device blocks itself even while disconnected, and unblocks when the connection returns with a fresh date. His position was firm — for Flex IQ there was a hard requirement that without internet and a server connection there is no point in it running at all, because JVL must be able to block a location at any moment, and an operator who can simply unplug the cable and keep trading defeats that requirement.

Val rejected that outright. A location will keep operating when the internet is down; they want players playing and putting money in, and JVL cannot be the reason the machines stop. His words: you cannot allow a location not to work. He also said the endpoint is cash, not tickets — the business prints money, and the plan must not block that.

The settlement, which Val called the right direction:

- Without internet the location keeps working. Wallets are created locally, money is loaded, players move machine to machine and play.
- The **one** thing that cannot happen offline is card issuance / redemption — that needs InComm, so the button is disabled with a clear "no connection" message and the player is told to come back.
- The player's eWallet stays in their hands, so nothing is lost.
- No internet at boot no longer prevents the device from starting, as long as the lease is still valid — the device already knows its own expiry date.
- Lease expiry blocking and internet-loss blocking are two different things and were being confused; only lease expiry blocks.
- **A device may run without server contact for 24 hours** — set as a working figure, not a final one. Val explicitly invited anyone with a critical view to say so; the alternatives floated were 6, 12 or 24 hours.

Val also floated printing some kind of validation ticket, or pre-generating a batch of about 100 validation IDs, so that something could still be issued offline. Chudzinau and Biratko both called that a bad engineering case. Biratko then asked the useful question — why move the eWallet to the cloud at all? The answer given was central validation of all tickets, the ability to consolidate and give bonuses, and kiosk replacement at a location. Once it was confirmed there is **no** goal of cashing the same eWallet at a different location, Biratko said the problem is much smaller than he first thought: all that is needed is a synchronisation point, since nothing else will try to update the ticket in the cloud. Val closed the topic by pointing out the cloud eWallet is a 2027–2028 release, not October 1, and the team should not spend two hours on it.

**MVP1 versus MVP2 — be honest.** Capability 116 assumes cloud behaviour that will not exist on October 1. Val's instruction was blunt: remove it, be honest with yourselves, what we cannot do by October 1 comes out. Anything mentioning the cloud moves to the MVP2 capability Klimovich created yesterday. The same rule was then applied through the rest of the list.

**Requirement-by-requirement outcomes.**

- **1378 (kiosk de-enrolment)** — a kiosk can be de-enrolled from a location but never from the cloud database. Nothing is deleted; it sits in an online or warehouse status. Wording corrected on the spot.
- **1379 (single cloud channel)** — moved out of capability 116 to the MVP2 cloud capability (177).
- **1382 (card issue end states)** — Chudzinau confirmed there is no cash on FlexPay in any form, so the "cash returned" state is dropped. Klimovich will check it against the other requirements covering card issuance on IQ and, if it duplicates, move it to MVP2 where FlexPay dispenser cases (card activated by InComm but stuck in the dispenser, or dropped to the trash box after a power cut) have their own logic.
- **1431 (PIN)** — was wrongly linked to a Flex IQ capability; there are no PIN codes on Flex IQ at all. Goes to FlexPay in MVP2.
- **1432 (number of FlexPorts)** — the figure was a placeholder. Georgia is simple: one location, maximum 9 gaming machines. Val wants the system **designed for 99**, with **15 as the MVP1 number**. What happens above the limit — reject or accept at your own risk — stays an open item to be answered by load testing.
- **1441 (physical/electronic cash return)** — not applicable to Flex IQ, where the cashier simply does not take money from the player if the ticket fails. Option removed.
- **1444, 1450, 1483, 1485** — FlexPay / Slim Recycler / self-service items still sitting in MVP1 by mistake. All moved to MVP2.
- **1447 (receipt)** — Klimovich's own note to design the receipt fields. Wording corrected so that not every top-up creates a receipt; yesterday's cashier prompt gate applies.
- **1454 (error catalogue)** — the full catalogue of errors still has to be created; status dropped from Published back to Draft.
- **1435 (response time)** — 200 ms between screens under load confirmed as the standard; the open-question wording removed.
- **1436 (data retention)** — retention is indefinite while the device is local; a factory reset / full re-image from SD card wipes everything, but software updates are expected over the air with data preserved.
- **1437 / 1438 (activation timeout)** — **30 seconds** agreed as the wait for a response before telling the player to retry. Errors that come back explicitly are shown immediately. A request sent with no answer at all leaves the transaction in a pending state until InComm confirms what happened. The second, unclear half of 1437 was deleted as over-engineered by Claude.
- **1533 (InComm daily cap and velocity)** — Chudzinau checked the InComm documentation: there is no daily-cap error returned, so JVL cannot detect it. The requirement is removed. Practical consequence accepted: the cashier will call JVL first, JVL reads the logs, and only then sends them to InComm. Klimovich wants a web interface showing the day's running total so support can spot a likely cap.
- **1469 (FlexPort collect timeout)** — **30 seconds** for the player to scan a ticket or create a new wallet on the FlexPort screen. Universal, not a per-location parameter, and will be revisited from observation.
- **1486 (email receipt)** — kept for self-service, to save paper.
- **1490 (cancel handling)** — lives in the transaction protocol; comment deleted. The **wallet identifier** is the reliable key — every transaction tied to a wallet must be retrievable from it.
- **852 (SAS ports)** — machine-side question; JVL's own machines support two ports, other manufacturers' vary.
- **1552 (what counts as withdrawable)** — already covered by the existing MVP1 capability on wallet splitting; Claude was asking for the logic to be spelled out. In Georgia it is straightforward — everything is hand-paid.
- **1451 (expired wallet display)** — a UI question; kept open until the UI is added.

**Ticket printing on FlexPort — MVP2 direction.** Pavel raised what happens if a player presses generate ticket on a FlexPort while another player is standing at the FlexPay. Klimovich said this is already thought through for MVP2: nothing prints at the self-service kiosk directly. The player creates a one-time redemption PIN (four digits), walks to the service kiosk, enters the PIN in a separate part of the interface, and the ticket is generated there; the same PIN can serve as the wallet access code where the location has PIN access enabled. Pavel suggested a QR code instead; Klimovich rejected it — a large share of players will not photograph anything and many do not have smartphones.

**Capability 122** was skipped entirely at Chudzinau's request — he is reworking its criteria himself off the back of his work with Klimovich.

**Val's close.** He thanked the team, said the discussion was productive, and repeated the focus instruction: the engineers keep working on the one functional requirement set and nothing else gets programmed.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | All requirement authors (Klimovich, Chudzinau, Frolov, Shishko) | Review and update the status of every capability and requirement they authored | Not set | High | Klimovich did his own; asked each author to do the same |
| 2 | Andrei Klimovich | Check requirement 1382 against the other requirements covering card issuance on Flex IQ; if duplicated, move it to MVP2 and rework it for FlexPay | Not set | Normal | Dispenser failure cases need their own logic |
| 3 | Andrei Klimovich | Add to the boot requirement that the device continues working with no internet at start-up, up to the agreed window | Not set | High | Follows from today's offline decision |
| 4 | Andrei Klimovich | Create the full catalogue of errors; requirement 1454 stays Draft until it exists | Not set | Normal | Status moved back from Published |
| 5 | Andrei Klimovich | Design the receipt field by field — which fields are printed | Not set | Normal | His own note in requirement 1447 |
| 6 | Andrei Klimovich | Check requirement 1430 (unconfirmed money) and attach it to the capability created for it | Not set | Normal | Raised by Chudzinau at the end of the call |
| 7 | Andrei Klimovich | Remove the open-question placeholder from requirement 1451 once the UI wording is added | After UI is added | Low | Kept open deliberately |
| 8 | Dzmitry Chudzinau | Rework the acceptance criteria for capability 122 himself | Not set | Normal | He asked for it to be skipped today |
| 9 | Dzmitry Chudzinau | Find a capability for requirement 1431 (PIN) on the FlexPay side | Not set | Low | Unlinked from Flex IQ, not yet re-linked |
| 10 | Pavel Frolov | Build the shared filter showing the live requirements from all authors, so the team walks one list | Not set | Normal | His proposal; today used Irina's list instead |
| 11 | Team | Load-test to establish the real FlexPort limit per location and answer what happens above it | Not set | Medium | 15 for MVP1, design for 99; the open item stays as a reminder |

## Decisions

- **A location keeps operating without internet.** Wallets are created locally, money is loaded, players play. Only card issuance and redemption are blocked, with a clear "no connection" message.
- **Working figure: 24 hours** a device may run without server contact before the location is considered blocked. Not final — 6, 12 and 24 were all on the table and Val invited objections.
- Lease expiry and internet loss are separate matters. Only lease expiry blocks the device. No internet at boot no longer prevents start-up while the lease is valid.
- **Anything depending on the cloud comes out of MVP1** and moves to the MVP2 cloud capability (177). Val: be honest with yourselves — what cannot be done by October 1 gets removed.
- A kiosk can be de-enrolled from a location but **never** from the cloud database — it moves to an online or warehouse status, nothing is deleted.
- There is **no cash on FlexPay** in any form; the cash-return end state is dropped from card issuance.
- **Design for 99 FlexPorts** per location; **15** is the MVP1 number. Georgia in practice is one location, maximum 9 machines.
- **30 seconds** is the wait for an activation response before telling the player to retry. A request with no answer at all becomes a pending transaction until InComm confirms.
- **30 seconds** is the FlexPort collect timeout for the player to scan a ticket or create a wallet. Universal, not per-location.
- **200 ms** between screens under load is the response-time standard.
- InComm returns no daily-cap error, so JVL cannot detect it — the requirement is removed and support will read the logs when a location calls.
- Data retention is indefinite locally; a full re-image wipes everything, but updates are expected over the air with data preserved.
- The **wallet identifier** is the key for retrieving all transactions tied to a wallet.
- Self-service ticket printing (MVP2) goes through a four-digit one-time redemption PIN entered at the service kiosk — not a QR code, and nothing prints at the self-service kiosk.
- The cloud eWallet is a 2027–2028 release and will not be designed in detail now.

## Open Questions

- **Is 24 hours the right offline window?** Set as a working number; 6 and 12 were alternatives and Val asked for critical views.
- **What happens above the FlexPort limit** — reject the extra device or accept it without guarantees. Answerable only by load testing.
- **Whether requirement 1382 duplicates existing Flex IQ card-issuance logic.** Klimovich to check.
- **Which capability requirement 1431 (PIN) belongs to** on the FlexPay side.
- **Whether a running daily total should be shown in the operator menu.** Pavel wants it for the cashier; Klimovich is against showing an unofficial InComm number, but wants it in JVL's own support web interface.
- **The logic for what counts as withdrawable** still needs spelling out beyond the Georgia hand-pay case (requirement 1552).
- **Capability 122** — Chudzinau is reworking it and it was not reviewed.
