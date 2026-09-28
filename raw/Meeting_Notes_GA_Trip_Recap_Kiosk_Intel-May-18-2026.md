# Meeting Summary — GA trip recap: kiosk intel, the merchant doctrine, and the POS renaming

**Date:** May 18, 2026, ~11:30 AM Eastern (second segment of the 2h37m May 18 recording)
**Duration:** approximately 55 minutes
**Attendees:** Val Levitan, Andrei Klimovich (Speaker 8 — presenting the trip findings), Felipe Miranda Giorgi (Speaker 4), Juan Martinez. (Between the two meetings the recorder caught a few minutes of unrelated background audio — an entrepreneur interview — noted and ignored.)
**Raw transcript:** [[Meeting_Transcript_GA_Trip_Recap_Kiosk_Intel-May-18-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "GA Trip Recap", 11:30 AM–12:30 PM ET, organiser Andrei Klimovich. Confirmed.

## Summary

Val set the format — "free conversation… individual thoughts and experiences from the gut, no speeches" — and got exactly that, including disagreements he welcomed.

**Competitor kiosk landscape (Andrei's field observations).** ~Five manufacturers cover the Georgia market. Common traits: tall tower/slim form factors (screen at shoulder height, small floor footprint), ATM-grade metal ("feels much more protected than our current FlexPay"), all-in/out support — TITO, receipt printing, card swipe onto e-wallet/player card, and **gift-card refill**; some offer split redemption (part to gift card, part stays as TITO). Pricing intel: kiosks ~$10K average; the big POS units ~$7K. Kroger's flow has no kiosk at all: unprotected player cards hang by the machines; account creation, play, cash-out and gift-card conversion all happen at the machine.

**Andrei's challenge and Val's discipline ruling.** Andrei questioned whether a standalone kiosk is needed at all — RFID/phone e-wallet could do everything at the machine. Val's ruling, delivered firmly: the committed pipeline (FlexPay kiosk, POS, FlexPort, Recycler) is the focus — "we cannot switch on a dime… committing to another development is extremely expensive and will not expedite penetration of the current product." New ideas are welcome only as identified risks against the current product. Juan added history: InComm and the lottery danced around digital wallets last August ("the Georgia player isn't skilled enough for phones" — never "not permitted"), and July-1 reloadability may accelerate digital.

**FlexPay gaps conceded (Andrei's risk list):** no gift-card refill, no debit/credit acceptance, and a form factor "too massive" vs the slim towers. Val accepted the form-factor point — **Flex Slim** (the recycler chassis, optionally without the recycler) answers it.

**The merchant doctrine (the meeting's recurring lesson).** Val and Juan drilled the same point through every claim: taking money OUT of a prepaid Mastercard requires a **Mastercard merchant number in a business category — and "gaming" is federally untouchable** ("the biggest casinos have lobbied for years and cannot get it"; class-action fear — "a husband gambles his wages away and the wife sues"). Every observed "card acceptance" claim must therefore be dissected: buying a *product* (a $20 player's card — a physical thing) is a merchant transaction that works; cash-for-gambling does not. Debit vs credit matters (credit for gaming = federal violation). Andrei saw card readers on kiosks in locations and a warehouse but never personally swiped; **Felipe undertook to physically test buying a TITO ticket with his own debit card and film it.** Gift-card refill similarly is an **InComm/Mastercard API capability, not a kiosk feature** — when the service side (post-July-1 reloadability) turns it on, JVL supports it through the API (Juan: ~a week of engineering, the card swiper is provisioned).

**The gift-card → prize-card → ATM chain, disambiguated.** John Housel (InComm) piloted kiosk redemption where winnings → gift card → secondary card → ATM-cashable card (~$6.50 total fees; players already launder gift cards through Kroger money orders anyway — his justification). Mike Patel/GAMOA pointedly did NOT endorse it (spotlight fear: "we have a good thing going, let's not fuck it up"); nothing is certain until the midterm elections. Val cut off the amateur legal speculation twice: "stop dreaming up the legislation — none of you are any authority to me on legislation."

**Pax dissected (the competitive foil).** Weaknesses: manual amount entry (fat-finger and skim risk — Val's arithmetic: an extra $5 on every ticket, 10 tickets/day = $18K/year/location; Lucky Coin's operator shrugs it off as "allocations", CUB(?) cited tens of thousands per month), and reconciliation hell — lottery reports vs location reports vs Pax vs MudaGoose, InComm ACH-debits the operator next day right-or-wrong, "you let it go… that is exactly what you do." Val's conclusion: **"Pax is not a competitor if we do our job correctly"** — automatic meter-driven amounts plus single-source reconciliation is JVL's killer feature; the POS must be coupled with operator intelligence/reporting.

**The renaming decision.** Andrei's observation (echoed by Juan): "POS" makes operators think of full retail point-of-sale (goods libraries, gas-station integration — the location owner's problem, not theirs), while the actual product is a gift-card issuance/validation device. Decision: **rename the Flex POS** — everyone contributes candidates to the chat, Juan collates. (This is the meeting that set up the later "IQ" naming.)

**July 1 sentiment.** An operator told Felipe that an extension request to the Georgia Lottery (reportedly a year) was denied; market anxiety is real; Lucky Bucks at ~75% Pax coverage.

## Decisions Made

- **Pipeline focus reaffirmed: FlexPay, POS, FlexPort, Recycler — no new-architecture detours.** (Val)
- **Flex Slim adopted as the answer to the form-factor gap.** (Val, accepting Andrei's point)
- **Rename the Flex POS — candidates to be collected.** (all; Juan collates)
- **Gift-card refill and card acceptance are API/service capabilities to adopt when InComm/Mastercard enable them — not JVL build items now.** (Val/Juan)
- **All card-acceptance claims get physically verified before belief.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe | Physically test a debit-card TITO purchase at a live location, on video | ASAP | High | The claim that gates everything |
| 2 | Juan Martinez | Collect and post Flex-POS rename candidates | Days | High | "I'll come up with a couple of terms" |
| 3 | Andrei Klimovich | Share the kiosk photo set for the hardware discussion | Next session | Normal | Promised at the top |
| 4 | Juan Martinez | Retrieve the CUB(?) loss figures cited (tens of thousands/month) | TBD | Low | For the reconciliation pitch |

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "Kamau / Gomorrah" — **GAMOA**; "income" (throughout) — **InComm**; "John Hassel / Housel" — InComm's presenter, spelling unconfirmed; "Mims Amusement" (02:02:12) — operator name, unconfirmed; "CUB" (02:33:08) — unclear source of the loss figures; "Pax eighty / parks / packs / tax device" — **Pax (PAX A80?)** handheld; "Kruger" — **Kroger**; "LexPay / space kiosk" — **FlexPay**; "EOS" (01:40:10) — **POS**; "Muskoka" (01:59:31) — **Mastercard** (garble); "wizard for three days" (01:39:40) — "was there for three days"; "Marcus" (01:40:10) — **market**.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 4)*
*Source recording: 05-18 Cross-Border Tax Strategy and Georgia Gaming Market Analysis (Plaud), second segment*
