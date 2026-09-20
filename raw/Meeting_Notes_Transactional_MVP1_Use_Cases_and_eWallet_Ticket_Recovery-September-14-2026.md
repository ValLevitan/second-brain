# Meeting Summary — Transactional MVP1: CAPs, REQs, planning

**Date:** September 14, 2026, 8:01 AM - 9:03 AM Eastern
**Duration:** approximately 1 hour 2 minutes
**Attendees:** Andrei Klimovich (organiser), Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Alexander Biratko, Andrei Bosik
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026]]
**Source meeting:** Transactional MVP1: CAPs, REQs, planning — Microsoft Teams

## Summary

Andrei Klimovich walked the team through the MVP1 use cases one by one, so everyone would leave with the same expectation of what the release does. He opened by saying MVP1 is fully formed at capability level and finalised into one version; the only thing still missing is the UI/UX screens and final texts, which he would add by the next morning. He had collected the use cases on a separate Confluence page — high level, but enough to see what MVP1 must be able to do. The second purpose was to settle how builds get delivered.

**Build delivery — Val cut the premise.** Klimovich asked for regular builds once anything is testable, with a short list of what went into each one; he has git access and can download and install himself. Val stopped that immediately: he does not want anyone downloading and installing. Bosik said the environment that does it automatically is almost ready. Pavel Frolov corrected him on scope — FlexPort cannot be updated remotely yet, so FlexPort still has to be downloaded and installed the old way. Val told Klimovich his task is to stop the team downloading, and set a 30-day target to finish it.

**What MVP1 is.** Flex IQ working in a FlexPort environment. No kiosks, no self-service. Four framing scenarios:

1. Money arrives on an eWallet through the counter — IQ must be able to create a loaded eWallet.
2. Money moves from the eWallet to the game machine through FlexPort.
3. If the location is blocked — by whatever mechanism — creating a loaded eWallet on IQ must not work.
4. If a transfer fails midway in either direction, the money must always be recoverable on one of the two original sides. No money is lost in transit.

**eWallet rules.** The eWallet holds the player's balance outside the machine, and one eWallet has exactly one carrier — the printed ticket — which exists in a single copy. Balance can be checked at the counter, and on FlexPort it happens automatically when the carrier is scanned. Klimovich was firm that the money must not move straight away: the player has to be shown the balance and confirm. Irina Shishko put it as a dialogue between the player and the port, and Klimovich agreed — confirmation is needed, and showing the current balance is part of that dialogue.

Expiry is handled by a TTL set when the eWallet is created. Val asked what "expired" actually means and what the period is. Klimovich proposed 30 days by default, configurable per location, minimum one day and maximum 365. Val questioned why an empty wallet should be held for 30 days rather than a few hours; Pavel answered that it is simpler to keep it than to build separate logic for empty tickets, and Val accepted that as a good answer.

Dzmitry Chudzinau asked whether the expiry is printed on the ticket, and what happens if a location later changes the default from 30 days to 45. Klimovich's design prints the validity period — "wallet valid for X days" — plus the creation date and time, deliberately showing the life span rather than only the creation date. Tickets already printed are not reprinted when a location changes its setting; the rule for that case is written up separately in the requirement, not in a use case.

**Balances are snapshots.** Klimovich stated it as a global requirement governing all eWallet handling: any balance held at a gateway is a snapshot, and every time anything is done with a balance the system must fetch the current state. Otherwise $20 recorded at creation may since have become $5 and the system keeps operating as if it were 20.

**Collect — the new fork.** This came out of the previous Monday's call and Klimovich called it an excellent requirement that solves a lot. When the player presses collect on the machine, FlexPort goes into a fork: scan your carrier now and the money moves onto that eWallet, or press "print new" — IQ then prints a ticket for a newly created eWallet on the printer attached to it, and the player walks to the cashier to collect it. What happens next is the player's business: back to the machines, or redemption.

Pavel confirmed the mechanics: if the player chooses "print me a new one", the transaction closes at once, nothing stays on the FlexPort, and the ticket is with the cashier.

**Current FlexPort behaviour, and the timeout.** Klimovich had tested how FlexPort works today: on collect, the machine balance is written down to zero immediately and the money sits pending on FlexPort; if nothing happens, the wait expires — the timeout is configurable but currently around 30 seconds — and the money disappears from view. He asked whether the money is genuinely gone from the machine at the moment collect is confirmed and cannot return there within that operation. Pavel said they are working on exactly this, do not yet know whether it can behave differently, tried and failed, and has passed the task to Evgeny Kharetski. Money not scanned in time lands in "unclaimed" on the terminal, where it can be found; what the cashier then does with it — reprint a ticket or something else — is the open part.

**Proving a ticket is yours.** Alexander Biratko asked how a player confirms a printed ticket is theirs, and what happens when two people from different machines both claim one. Klimovich: the machine is not on the ticket, but the IQ transaction shows which machine the transaction came from, and the ticket carries a transaction or eWallet identifier, so the cashier can take two tickets, look at the IQ screen and match each to the right person. Verbally it works exactly as it does today — "I was on machine 3."

**Redemption.** Klimovich called this the heart of the process. The InComm card is unchanged in this version. What is added is min/max logic, and it needs a different approach from the one used for Moutagouz. If the eWallet balance is below the card minimum plus the activation fee, nothing can be done with the transaction — MVP1 adds no lottery-ticket fallback. The cashier scans, IQ says plainly it cannot be loaded, and the ticket goes back to the player to play more or add money. At the other end, the maximum load on a card is $1,000: issue one card, the remainder stays on the eWallet, rescan the ticket, issue another card, and repeat until the whole balance is redeemed.

**Daily caps.** InComm holds a velocity and a daily cap per location to control fraud. JVL does not manage them and most likely does not even know the values. Klimovich's question to the engineers was whether a cap rejection comes back as an explicit InComm error that can be translated for the cashier — "your location has reached its daily cap, contact InComm" — or whether it is just a generic failure. Chudzinau said everything InComm documents is handled and interpreted; a bare "error" on screen means the response could not be recognised. Klimovich asked for the error library with the texts currently in use so he can review the wording. Pavel asked whether those interpretations are translated into Spanish when Spanish is selected — yes, from a hard-coded translation collection, not translated on the fly.

**Play-through.** Chudzinau flagged something that had not been said out loud: money put onto an eWallet still has to be played before it can be taken out. Klimovich confirmed the rule stands and that the dual balance stays — a deposited part and a playable part — and it must be reflected everywhere a balance is communicated, including what the cashier sees on IQ. He said he would add a capability for it so it does not get lost; Pavel suggested it may already exist as a requirement inside a capability, and Klimovich agreed to search first.

**Cloud versus local.** Chudzinau raised requirement 1538, attached to capability 158, which leans heavily on a cloud eWallet balance reachable from several terminals. MVP1 stays local — the terminal keeps its own wallet balances. His practical point was that Claude goes wrong closing a capability whose requirement demands a cloud balance, and starts creating features for it. Klimovich did not want to rewrite every capability down to "local, local, local", since he wrote them describing where JVL wants to arrive. The agreed answer was to move requirement 1538 to a new MVP2 capability describing the full cloud logic. Irina's framing was the reason it matters: when the release ships October 1, it must be clear what was closed and what comes next.

**Dashboard and reporting.** The MVP1 dashboard shows activated cards only — who, where, when, how much. All eWallet movement on a terminal stays local and is not exported; Chudzinau called that a separate group of work and said it is better done together with the move to cloud, which Klimovich accepted. Pavel identified it as reporting for the new capability Klimovich had just said he would create.

**Receipts and the printer.** On card activation, once the procedure is complete and the card is confirmed active, a receipt must print immediately showing how much was loaded, the fee and so on; Klimovich would add the field design the same day. Biratko asked whether a broken or empty printer blocks card issue — it does not. The printer does report back: general errors, head errors, jams, and low or absent paper. Klimovich wants IQ to show those, and also to warn before the paper runs out, and asked for the list of tilts JVL can handle. Irina offered the machine-side list and Biratko confirmed the printer is the same one.

Val added a requirement of his own: JVL must be able to measure, at any point in time, how much paper is left, how many cards are left, and how full the bill stacker is, and push that to the operator or administrator preventively rather than after the fact. Biratko and Klimovich said there is no capability for it yet, and Klimovich placed it in MVP2, where the kiosk arrives and it becomes unavoidable. Val accepted that it is noted.

**The painful scenario — a carrier that does not print.** Chudzinau explained that on FlexPay wallet creation sits inside the output transaction, so if the printer does not work the wallet is not created at all and the person is told why. That opened the argument about where the money then sits: Biratko pointed out that on the port the money has already left the machine, so it cannot simply stay there.

Klimovich said this exact block had been added the day before, and it is the worst case: the player chooses "create new" on FlexPort, the ticket does not print, he comes to the cashier and there is nothing. The agreed logic is that the eWallet is created the moment the player presses "create new" and the machine's game credit is loaded onto it, so the money is already saved. If the ticket then fails to print for any reason, the transaction must be visible to the cashier. A whole block of transaction capabilities covers this: the full history of created eWallets, issued cards and every operation, on the IQ screen, filterable. The player says he played machine 3, the cashier filters collect transactions, finds the one matching that machine and time, and has an option to produce the carrier.

Klimovich had specified that option as a reissue — close the eWallet just created, move its balance to a new eWallet, and print that one's ticket — to preserve one wallet, one carrier, and to block a fraud where a player holds a photocopy. Pavel and Biratko both pushed back: money can only be taken off a ticket once, so a copy is not the threat; and a plain reprint carries the same impersonation risk as a reissue. Biratko added that protecting against copying is effectively impossible without a PIN, and Chudzinau pointed out a PIN is out of the question when the cashier is doing the reprint. Chudzinau's alternative was that the wallet is created with a status and the print action moves it out of the "unclaimed" block, with no new number involved. Klimovich could not remember why he had settled on reissue, said he may have found something awkward at the time, and parked the question for re-reading on both sides. What is firm: the cashier must see the transaction, identify it, select it, and send a print-carrier command when auto-print failed. Identification stays verbal, as it is today with Moutagouz.

**Two cashiers.** Bosik asked whether the scenario assumes exactly one Flex IQ per location, and what happens with two cashiers and two IQs. Klimovich said not to think about it now — it cannot be supported and he cannot see why it would be needed; a location almost always has one cashier, and the next version of the ecosystem with IQ plus kiosk is where that gets solved. Irina thought two IQs at one location would be expensive and pointless.

**Finding transactions, and the one report.** A block covers how transactions are searched and sorted on IQ, including the small convenience that scanning a player's carrier filters the transaction list down to that eWallet. Klimovich accepted not all of it may be finished and gave the priority order: first showing the created transaction so a reprint is possible, then the history of issued cards, which feeds the report.

One report is needed in MVP1, and Klimovich thinks it has to make the release. The scenario: an inspection from the Georgia Lottery, which controls the market, arrives at the location and asks for a report of cards issued over a given period. The cashier presses one simple button and gets it. Klimovich has an example of such a report from one of JVL's competitors and intends to reproduce it; he would work the same day on what goes on it and how it fits the ticket printer.

**Top-up.** Irina pointed out the eWallet can also be topped up on IQ, the same way money moves on collect. Klimovich agreed there is no use case written for it but the capability exists — add or update balance on IQ has to be there just as create-on-IQ is. Irina noted that capabilities 148, 149 and 150 were previously treated as already implemented, needing only automated tests; Chudzinau said the business logic moved over from FlexPay and is implemented, but changes there mean changes here. Klimovich said the UI changes regardless: IQ never had this UI at all, and FlexPay's is self-service facing a player while IQ's faces a cashier, so the volume of information and the way you enter the screen are both different.

**Capability list.** Pavel said the use cases were all clear, and that a large part of the capability list looks almost done, or done but not covered by automated tests — mostly needing corrections and some added reports. Klimovich had run the whole list through Claude in both directions the day before — use cases against capabilities, then capabilities back to the experience they produce — and considers the list current. Pavel flagged two overlaps: capability 171, location block enforcement, looks like the same thing as 118, terminal lease and remote disable. Klimovich agreed they overlap strongly and said 171 exists to carry the more detailed requirements — how a block affects the port, IQ and the different kiosk types separately, what is shown on screen, what state things sit in. One rule he remembered writing: if an operation is mid-flight when a location block arrives, the operation must at minimum be allowed to complete.

**SAS and AFT.** Pavel suggested giving Klimovich the current port firmware so he can install it, connect to a machine over SAS and walk the new SAS workflow himself, seeing the screens and messages. That build now analyses error cases and reports them — SAS not connected, FlexPort not connected, AFT not configured. Biratko added that the same IFT transfer screens appear on third-party machines too, because it is the standard, which surprised Klimovich. Val stepped in to name the source: the standard is published by the Gaming Standards Association as SAS, it is public, and capabilities must be written against it rather than invented. On the version, Pavel and Biratko said the newest is 6.03; Val insisted on 6.02 because some machines have not been updated. Biratko thought AFT had not changed between them; Val's answer was that you cannot take the latest release and assume. Biratko will send the specification. Klimovich said it is a new area for him and he will learn it quickly.

**JIRA hygiene — Val's organisational block.** Val closed with process. He asked whether Kovalchuk had changed the capability workflow; Bosik believed so, but Pavel saw "Accepted" still showing green after "Proposed". Val's rules:

- Nothing in MVP1 can still be in "Proposed" today. That negotiation sits between Klimovich and Pavel. MVP1 items must be at least Accepted.
- Everything already in To Do must have features under it, and the features being worked on must be In Progress and carry a linked feature branch.
- Capabilities in progress cannot be unlinked from requirements, and requirements cannot be without acceptance criteria. Irina added that a capability should only be Accepted once it holds all its requirements, and that requirements themselves should change status when they are approved.
- Klimovich owns pushing capabilities out of Proposed — in Val's words, selling them to the developers. After that, features must be created against them and the features put into the schedule.

Val asked Andrei Bosik to write a routine that checks this logic and sends a short exception report — only what does not match the rule — to Val, Pavel and Klimovich. Bosik agreed and said he needs to think about how to implement it, and that such a thing may already exist.

**Close.** Next meeting tomorrow at the same time, to go through the UI/UX. Pavel's task before it: make sure everything In Progress is scheduled.

## Decisions Made

- **MVP1 is Flex IQ working in a FlexPort environment.** No kiosks, no self-service systems. (Andrei Klimovich)
- **No money may be lost in a transfer.** If funding fails midway in either direction, the money must be recoverable on one of the original sides. (Andrei Klimovich)
- **One eWallet has exactly one carrier** — the printed ticket, in a single copy. (Andrei Klimovich)
- **FlexPort must show the balance and get player confirmation before moving money**, not transfer automatically on scan. (Andrei Klimovich, framed by Irina Shishko as a player-to-port dialogue)
- **eWallet TTL default is 30 days**, configurable per location, minimum 1 day and maximum 365. (Andrei Klimovich, accepted by Val Levitan)
- **Empty eWallets are simply kept** rather than given separate cleanup logic — cheaper than building the special case. (Pavel Frolov, accepted by Val Levitan)
- **The ticket prints the validity period plus creation date and time**, and is not reprinted if a location later changes its default. (Andrei Klimovich)
- **Every balance operation must fetch the live balance.** Any stored balance is a snapshot. Global requirement. (Andrei Klimovich)
- **On collect, FlexPort offers a fork:** scan your existing carrier, or print a new ticket from the IQ printer. (Andrei Klimovich, from the previous Monday's call)
- **Collect money not claimed before the timeout goes to "unclaimed" on the terminal** for manual handling. (Pavel Frolov, accepted)
- **The eWallet is created the moment the player presses "create new"**, before printing, so the money is saved even if the ticket never prints. (Andrei Klimovich)
- **A printer fault does not block card issue.** (Andrei Klimovich, in answer to Alexander Biratko)
- **Redemption below the card minimum plus activation fee is refused** — no lottery-ticket fallback in MVP1; the ticket goes back to the player. (Andrei Klimovich)
- **Maximum $1,000 per card, with repeat issuance** against the same ticket until the balance is drained. (Andrei Klimovich)
- **Daily caps and velocity stay InComm's.** JVL does not manage them and only interprets the returned error for the cashier. (Andrei Klimovich, Dzmitry Chudzinau)
- **The play-through rule stays, and the dual balance must be visible** wherever a balance is shown, including to the cashier. (Andrei Klimovich, raised by Dzmitry Chudzinau)
- **MVP1 stays on local terminal storage.** Requirement 1538 moves off capability 158 to a new MVP2 cloud capability. (Andrei Klimovich, proposed by Dzmitry Chudzinau, agreed by Pavel Frolov)
- **The MVP1 dashboard shows activated cards only.** eWallet movement reporting is deferred and done together with the cloud move. (Dzmitry Chudzinau, accepted by Andrei Klimovich)
- **One report must make MVP1:** cards issued over a period, on one button, for a Georgia Lottery inspection. (Andrei Klimovich)
- **Two Flex IQs at one location is not supported in MVP1** and is deferred to the IQ-plus-kiosk version. (Andrei Klimovich)
- **Capabilities must be written against the published SAS standard, version 6.02, not 6.03** — because some machines have not been updated. (Val Levitan, over Alexander Biratko's view that AFT did not change between versions)
- **Nothing in MVP1 may remain in "Proposed".** MVP1 items must be at least Accepted; To Do items must have features; features in progress must have a linked feature branch; capabilities in progress must be linked to requirements with acceptance criteria. (Val Levitan, extended by Irina Shishko)
- **Target: stop manual downloading and installing within 30 days.** (Val Levitan)
- **Deferred, explicitly:** paper / card / bill-stacker telemetry and preventive alerts (MVP2, with the kiosk); reissue versus reprint for an unprinted carrier (parked for re-reading).

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Add the final UI/UX screens and texts for IQ and FlexPort to the MVP1 page | September 15, 2026 morning | High | The one thing he named as still missing; tomorrow's meeting is built on it |
| 2 | Andrei Klimovich | Add the receipt design — which fields are shown and the logic behind them | September 14, 2026 | High | Promised for the same day |
| 3 | Andrei Klimovich | Add a capability for the audit report (one button, cards issued over a period), modelled on a competitor's report he holds | Before MVP1 | High | Driven by Georgia Lottery inspections |
| 4 | Andrei Klimovich | Add the dual-balance (deposited versus playable) logic to the capabilities, or find where it is already written as a requirement | Not set | Medium | Pavel suggested searching first |
| 5 | Andrei Klimovich | Move requirement 1538 off capability 158 into a new MVP2 cloud capability | Not set | Medium | So Claude stops trying to build cloud features into MVP1 |
| 6 | Andrei Klimovich | Add preventive printer messaging to IQ — low paper as well as out of paper | Not set | Medium | Needs the tilt list first |
| 7 | Andrei Klimovich | Re-read the reissue-versus-reprint capability and settle which approach MVP1 takes | Not set | Medium | He could not recall why he chose reissue |
| 8 | Andrei Klimovich | Learn the SAS 6.02 AFT standard and write the capabilities against it | Not set | Medium | New area for him; he said he will pick it up quickly |
| 9 | Andrei Klimovich | Push every MVP1 capability out of "Proposed" status | Immediate | High | Val: nothing in MVP1 can still be Proposed today |
| 10 | Dzmitry Chudzinau | Send Klimovich the library of InComm errors with the texts currently used to interpret them | When he has time | Normal | For a wording review |
| 11 | Irina Shishko / Alexander Biratko | Send Klimovich the list of printer tilts handled on the machine | Not set | Normal | Same printer as FlexPort |
| 12 | Alexander Biratko | Send Klimovich the SAS specification (public; version per Val is 6.02) | Not set | Normal | Val offered to obtain it from the GSA if nobody sends it |
| 13 | Andrei Bosik | Build a routine that checks the JIRA status rules and sends a short exception report — only what does not match — to Val, Pavel and Klimovich | Not set | High | Bosik agreed and needs to work out how; he thinks something similar may exist |
| 14 | Pavel Frolov | Give Klimovich the current FlexPort firmware so he can install it, connect over SAS and walk the new workflow | Not set | Normal | So Klimovich sees the real screens and messages |
| 15 | Pavel Frolov | Make sure everything In Progress is scheduled | September 15, 2026 | Normal | Val's task ahead of tomorrow's meeting |
| 16 | Evgeny Kharetski (via Pavel Frolov) | Determine whether collect money can stay on the machine instead of moving to FlexPort immediately | Not set | Medium | Pavel tried and failed; task handed over |
| 17 | Andrei Bosik / Pavel Frolov | Finish remote update so nobody has to download and install builds, FlexPort included | Within 30 days (target set in the meeting) | High | Val's condition on the whole build-delivery discussion |

## Open Questions

- **Reissue versus reprint for a carrier that failed to print.** Klimovich parked it; Pavel, Biratko and Chudzinau each argued against reissue. Nobody disputes what the cashier must be able to do — only how it is implemented.
- **Whether collect money can be held on the machine** rather than moving to FlexPort the instant collect is confirmed. With Evgeny Kharetski.
- **What the cashier does with money sitting in "unclaimed"** — reprint a ticket, or something else. Pavel named it as the open part.
- **Whether capability 171 (location block enforce) and 118 (terminal lease and remote disable) should be merged.** Klimovich agreed they overlap strongly but kept 171 for the per-device detail.
- **What goes on the inspection report and how it fits the printer width.** Klimovich would work on it the same day.
- **Whether Kovalchuk actually changed the capability workflow.** Bosik believed yes; Pavel saw evidence it had not taken effect.
- **Ticket identification stays verbal.** No anti-copy mechanism is possible without a PIN, and a PIN does not work when the cashier is doing the reprint.
- **Preventive supply monitoring** (paper, cards, bill stacker) has no capability at all yet. Placed in MVP2.
- **Whether SAS 6.02 versus 6.03 actually matters for AFT.** Biratko believed AFT did not change; Val ruled on 6.02 anyway because of unpatched machines.

## Notes on the transcript

The meeting was held in Russian and the Teams transcription garbles almost every English product and technical term. Readings that are near-certain from context: "MVP один" / "VP один" / "BMWP один" / "мвпи один" / "IVP один" / "NBP" / "MUP один" = MVP1; "иволят" / "и волет" / "уволит" / "вольт" / "его лет" / "ivolete" / "и улице" = eWallet; "Кэрри" / "karier" / "Керри" = carrier (the printed ticket); "тикет" / "тито" / "стикет" / "cicket" / "secet" = ticket; "флекспорт" / "флегспорт" / "фекспорт" / "флекс порт" = FlexPort; "IQ" / "айкью" / "ай кью" / "ikeunter" = Flex IQ; "флекспей" / "flexpay" / "лексп" = FlexPay; "ИНКОМ" / "инкома" / "инкомовская" = InComm; "рекламент" / "реклармент" / "рекламу" / "ириквайменс" = requirement; "капбилити" / "кейпобилети" / "копеллити" / "побилити" / "кпбилити" / "беллиси" = capability; "юскейс" / "us кейс" / "дискейсов" / "yсам" = use case; "редемшн" / "рыденшн" / "рыбшн" / "redamtion" = redemption; "ресит" / "рисито" / "resit" = receipt; "репринт" / "репсинт" / "repsint" = reprint; "лиишью" / "лишь" / "Russia" / "регишь" = reissue; "анклейм" / "анкле" / "анкл то" = unclaimed; "тилт" / "телтов" / "тилтов" = tilt (printer/validator fault code); "дейли кап" / "дэй cap" / "кэпа" = daily cap; "велосиси" = velocity; "плейбл" / "плей был" = playable balance; "мутагуз" / "мутэнта" / "смыф" = Moutagouz (the existing product, spelling uncertain); "дашборт" / "даш борт" / "дажбо" / "даже борт" = dashboard; "клод" = Claude; "лакейшн блок инфорс" = location block enforce; "терминал лиз энд ремоут дизэйбл" = terminal lease and remote disable; "сас" / "с. А. С." / "sass" = SAS; "AFT" / "IFT" / "а с AFT" / "по FT" = AFT (SAS fund transfer); "j паблош stander" / "j li stendart" / "желает" / "чиллаи" / "часы gamy Stand red surgi" = the Gaming Standards Association and its published standard; "экобилети" / "эконобилети" = capability level; "пропост" / "прополз" / "пропуст" / "Полоз" = Proposed (JIRA status); "эксептенс" / "аксептон скрейтинг" / "экседед" = Accepted / acceptance criteria; "инпрогресс" / "инфограз" = In Progress; "фетрус" / "фьючерс" / "фичеры" / "печи бранч" = features / feature branch; "схедюл" / "скетживать" / "с кетжук" = schedule / scheduled; "жени харецкому" / "женихарецкому" = Evgeny Kharetski; "ковальчуку" = Kovalchuk; "тита" / "дизайн тито" = the ticket design.

Worth confirming with Val or Klimovich before being treated as fact: the numbers quoted for the requirement and capabilities (1538, 158, 171, 118, 115, 148/149/150) are audible but never spelled out; the name "Moutagouz" for the existing product is a guess from the audio; and the exact card maximum — Klimovich said "$1,000 maximum load", which should be checked against the InComm terms. The raw transcript is preserved unchanged, in Russian.

## Dispatch Log

*(empty — captured by the scheduled meeting-watcher sweep, no dispatch)*

---
*Processed from Teams transcript on September 14, 2026, 10:05 AM Eastern*
*Source meeting: Transactional MVP1: CAPs, REQs, planning*
