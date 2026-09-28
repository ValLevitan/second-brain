# Meeting Summary — Pyramid Technologies (Tomislav Jeras): NDA scope and QR prior-art disclosure

**Date:** January 22, 2026, 11:30 AM Eastern
**Duration:** approximately 16 minutes
**Attendees:** Val Levitan and Tomislav Jeras (Pyramid Technologies; named by Plaud's speaker detection). Jonathan Durst referenced as the mutual contact and "witness".
**Raw transcript:** [[Meeting_Transcript_Pyramid_Tomislav_Jeras_NDA_Scope_and_QR_Prior_Art-January-22-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "RE: [Pyramid Technologies] Re: Re: Emulator for the printer", 11:30 AM–12:00 PM ET, organiser Val. "Pyramid" and Jonathan appear in the transcript; confirmed on both keys.

## Summary

A first call between Val and Tomislav Jeras of Pyramid, following the January 8 engineering intro, to settle the NDA before JVL embeds Pyramid's QR decoding into its kiosk.

**The use case, in Val's words.** A Texas customer runs machines with Pyramid printers. JVL wants to sell that customer its kiosk — housing a Fujitsu cash dispenser — where a winning ticket's QR code, printed by the Pyramid printer, is presented to the kiosk and converted to a cash value. Val assumes Pyramid controls the QR-to-value conversion (a handshake, likely decoded with a private key — Tomislav: "You've summarized it fairly") and wants that decoding embedded in the JVL kiosk. JVL does not operate locations; it sells the kiosk to a local operator as a complete solution — the end customer is not expected to self-integrate.

**Val's concern about the NDA.** He is happy to sign, but wants it narrow enough to protect Pyramid's specific decode application without touching technologies that are common knowledge or that JVL already owns. His stated credentials: 42 years in the business, owned CashCode for 16 years until selling to Crane, sat on the GSA board of directors for five years, and JVL holds a number of transactional technologies based on TITO and QR codes. He does not want to spend money on litigation over prior art at "the sunset of my career", and wants no enemies in the industry.

**Pyramid's position.** Tomislav explained the NDA/terms exist to stop reverse-engineering, time-sharing their technology through a cloud server, or nefarious use — and to shield Pyramid from liability claims once JVL implements the decryption ("this thing did something we didn't intend and my customer lost 500 bucks"). He offered to go back to legal and narrow the language.

**The prior-art disclosure — the heart of the call.** Val put on record, deliberately and in advance, that JVL already has a very similar technology, shown at trade shows: a screen device that sits inside the machine in front of the player and generates QR codes (no printer involved); the QR can also be printed on a regular TITO printer as barcode or QR; a player can generate an initial QR at the kiosk and use it as a temporary e-wallet, walking machine to machine. His point: "I'm not going to copy you — I'm telling you I already have it," so Pyramid can never later claim JVL derived it from the disclosure. Tomislav asked for a brochure or marketing material to timestamp in Pyramid's vault; Val's counter: only under an NDA — which Tomislav took on board. Val also disclaimed any plan to manufacture printers or enter the bill-acceptor business again.

**Tone and close.** Tomislav said Pyramid does not litigate in these matters (only a handful of cases in 25 years) and that he is "good with this conversation — I'll document it accordingly and we move forward." He was to speak with his colleague at 3 PM his time and with John (Jonathan) about truncating/simplifying the NDA, aiming to have something for a follow-up discussion the next day.

## Decisions Made

- **JVL will sign Pyramid's NDA, narrowed to the QR decoding pathway actually being disclosed.** (Val Levitan, accepted by Tomislav Jeras)
- **Val's prior art is now formally disclosed and to be documented by Pyramid** — the on-screen QR generator shown at trade shows, TITO-printed QR tickets, and the kiosk e-wallet flow. (both)
- **JVL sells the kiosk as a complete solution to operators; no end-customer self-integration.** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Tomislav Jeras | Talk to Pyramid legal about narrowing/simplifying the NDA; work next steps with Jonathan | Same afternoon (3 PM his time) | High | Follow-up call promised for the next day |
| 2 | Tomislav Jeras | Document Val's prior-art disclosure internally | Immediately | High | "I'll document it accordingly" |
| 3 | Val Levitan | Provide brochure/marketing material of the JVL QR solution — only once an NDA is in place | After NDA | Normal | Val declined to hand it over unprotected |

## Open Questions

- Final NDA language — how narrow Pyramid legal will actually make it.
- Whether the follow-up call the next day happened and what came of it.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 1)*
*Source recording: 01-22 Business Discussion on Technology Integration and NDA Terms Between JVL and Pyramid (Plaud)*
