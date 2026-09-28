# Meeting Summary — Pyramid Technologies: printer integration intro call

**Date:** January 8, 2026, 9:01 AM Eastern
**Duration:** approximately 16 minutes
**Attendees:** Val Levitan, Pavel Frolov (JVL engineering, Minsk), Genadi Peari (introduced during the call), and from Pyramid Technologies (Mesa, Arizona) Jonathan Durst and Kerrie ("Kerry") Nollette. Plaud labels speakers by number; Jonathan, Kerry, Pavel and Gennady are all named in the transcript.
**Raw transcript:** [[Meeting_Transcript_Pyramid_Technologies_Printer_Integration_Intro-January-8-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "RE: Questions Regarding Pyramid Printer Integration and Ticket QR Payload", 9:00–10:00 AM ET, organiser Val, attendees Jonathan Durst, Pavel Frolov, Genadi Peari, Kerrie Nollette. Confirmed on both keys.

## Summary

First working call between JVL and Pyramid Technologies on integrating Pyramid printers into JVL machines for the Texas market. Val opened with introductions: JVL is a 42-year-old company that moved from amusement into gaming devices; he founded CashCode, sold to Crane in 2006; Pavel directs engineering from the Minsk subsidiary (owned 28 years); JVL is departing Canada, headquarters splitting between Miami and an Atlanta suburb in Georgia. Val positioned JVL's expanding transactional equipment line as a direct competitor to Banilla.

**Why Pyramid.** Pyramid printers are widely used in Texas kiosks. JVL's initial use case is servicing/repairing machines in that market, with its own transactional line to follow later in the year. Pyramid keeps mechanical, electrical and software under one roof in Mesa, Arizona.

**Technical ground covered (Pavel's questions).**
- Connecting a Pyramid printer over serial (DB9 or RJ-45 recommended) using printer commands: per the ESC/POS documentation, the QR code on the ticket is generated automatically from the payload sent to the printer — JVL only needs to send the payload; no separate QR generation.
- Ticket types: some tickets (duplicates and similar) may not need to be printed as full tickets; Pyramid noted the configurations are industry standard and must be set up before deployment.
- To start, JVL can use Pyramid's kit and mobile/browser application to confirm tickets and exercise the payment/rebate flow; print configurations from Jonathan's earlier printer work (about two years back) still apply.

**Asks agreed on the call.**
- Val will ask JVL's Texas connection to clarify exactly which ticket types must be supported, and revert to Pavel.
- Kerry confirmed Pyramid can release a mechanical CAD file for hardware integration, to be sent to Gennady (director of the electromechanical department, Toronto — Val joked he is bribing him to move to Georgia).

Val closed thanking Jonathan for the introduction to Kerry and looking forward to the project.

## Decisions Made

- **JVL proceeds with Pyramid printer integration for Texas**, starting from Pyramid's kit/application and the ESC/POS serial path. (both sides)
- **Pyramid will release the mechanical CAD file** rather than JVL hand-measuring the unit. (Kerrie Nollette)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Ask the Texas connection which ticket types JVL must support; revert to Pavel | TBD | High | Blocks ticket-generation scope |
| 2 | Kerrie Nollette (Pyramid) | Send the mechanical CAD file to Genadi Peari | TBD | High | For hardware integration into the JVL machine |
| 3 | Pavel Frolov | Start against Pyramid's kit and application (ticket confirm, payment, rebate flow) | TBD | Normal | Kit was already shipped for this purpose |

## Open Questions

- Which ticket types the Texas market actually requires (pending Val's contact).

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- "tickets captured by Exxon" (00:04:04 area, spoken by Pavel) — "Exxon" is almost certainly a mis-hearing of a kiosk/system name (Axxess?).
- "spend a little over 13 years on carry space" (00:01:58) — garbled introduction of Kerrie's tenure.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 1)*
*Source recording: 01-08 Weekly Meeting: Pyramid Printer Hardware Integration and Ticket Generation (Plaud)*
