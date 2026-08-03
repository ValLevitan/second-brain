# Meeting Summary — RE: JVL PROD Location Registration Questions
**Date:** July 27, 2026, 12:00 PM – 12:30 PM Eastern
**Duration:** ~27 minutes
**Attendees:** Jason Hall, Camille Kearns, Allen Lee, Billy Reach, Ida Myers, Adam Harlow (InComm); Juan Martinez, Andrei Klimovich, Pavel Frolov (JVL)
**Raw transcript:** [[Meeting_Transcript_InComm_PROD_Location_Registration-July-27-2026]]

## Summary

InComm walked the JVL team through the business models for gift card reselling in the Georgia COAM market, then answered JVL's open questions about production location registration.

**Reseller models.** There are two ways JVL kiosks can operate in a location. Either JVL acts as the gift card reseller itself (JVL already has a merchant ID with InComm, posted in the meeting chat), or the kiosk sits in a location that has an existing agreement with another reseller. The main resellers are RWJ, Yinlow, and Lunex. RWJ and Yinlow locations do NOT connect to InComm's RTG system — the kiosk must integrate with their own middleware (RWJ's is called Yugo Hub / PayAnyUp) using an encryption key from RWJ. Lunex locations use RTG but pass the Lunex merchant ID. Some large operators act as their own reseller — same setup as Lunex, using their merchant ID. Juan confirmed JVL wants to support both models.

**Credentials.** JVL uses its own RTG credentials (UAT credentials in UAT, production credentials in production) for every location it registers, regardless of which merchant ID applies. Allen noted JVL's RTG credentials are currently linked only to the JVL merchant ID — InComm must associate them with other merchant IDs (e.g., Lunex) as JVL engages those locations. Pavel confirmed JVL already has its credentials from a terminal test at the Georgia office last year.

**Production test request.** Andrei asked to register a temporary production location (a couple of weeks) at JVL's office to test the full cycle: onboard a location, issue real production cards, receive an invoice, and reconcile it — before going live. The blocker is that JVL has no master or location license number. This isn't InComm's standard process (test invoices can't be generated in the test environment), so Jason will review options internally — possibly a manually crafted sample invoice — and respond this week. Juan noted a similar $2 invoice was produced (and credited) during last year's office test.

**Test cards.** JVL's orange cards are legacy but Adam Harlow confirmed they work for the production test — same UPC and configuration, only different artwork. New black card inventory (or the upcoming Skill Pay card with ATM access, launching this year) is available if needed.

**Go-live process.** For each real location, JVL fills out a kiosk location sign-up form when a placement is confirmed, then on install day completes a live production test transaction and submits the go-live form with pictures of the location license and card. InComm cancels the test activation and verifies the kiosk on the back end.

Juan also flagged a sensitivity: masters own the location relationships, and JVL acting as a direct reseller could conflict with masters who buy JVL gaming equipment.

## Decisions Made

- **JVL will pursue both reseller models** — selling kiosks into locations with existing reseller agreements AND acting as the reseller itself. (Decided by Juan Martinez)
- **Orange legacy cards will be used for the production test** — same UPC and configuration as the black cards, so no new inventory is needed for testing. (Decided by Adam Harlow, agreed by Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Jason Hall | Review JVL's request for a temporary production location registration (full cycle incl. invoice and reconciliation) with Allen and Adam, and respond with a solution | July 31, 2026 | High | Blocks JVL's end-to-end test before live rollout; "this week... within a few days" |
| 2 | Jason Hall | Make introductions so JVL can integrate with Yugo Hub (RWJ's middleware) | TBD | Normal | Needed for locations with RWJ agreements |
| 3 | Jason Hall | Send the slide deck with the kiosk location sign-up and go-live test transaction form links | July 27, 2026 | Normal | "I'll send you this deck after the call" |
| 4 | Andrei Klimovich | Reply to the existing email thread if the test-card shipping address or contact person needs updating | TBD | Low | Only if the address on file has changed |
| 5 | Juan Martinez / Andrei Klimovich | Keep InComm advised on which resellers/merchants JVL engages per location, so credentials can be linked to the right merchant IDs | Ongoing | Normal | [External — manual follow-up needed] InComm must do back-end setup per relationship |

## Open Questions

- How the temporary production test will be structured (live billing vs. a manually crafted sample invoice) — raised by Andrei Klimovich; Jason Hall to respond this week.
- Whether JVL's initial target customers' locations already have RWJ/Yugo Hub or other reseller agreements — raised by Jason Hall; Juan Martinez was unsure.
- How JVL acting as a direct reseller squares with masters owning the location relationships — raised by Juan Martinez; InComm offered to advise as needed.

## Dispatch Log

## Notes

- All speakers except the JVL side are InComm staff (external).
- Val attended but did not speak (no lines in the transcript).

---
*Processed from Teams transcript on July 27, 2026, 2:05 PM Eastern (scheduled watcher run)*
*Source meeting: RE: JVL PROD Location Registration Questions*
