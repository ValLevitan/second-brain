# Meeting Summary — Failed ACH payments: business needs and approach
**Date:** August 10, 2026, 8:30–9:32 AM Eastern
**Duration:** ~1 hour
**Attendees:** Nathan Carver, Val Levitan, Juan Martinez, Andrei Klimovich, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Failed_ACH_Payments_Flex_IQ_Beta-August-10-2026]]

## Summary

The team discussed how to handle a location's insufficient funds (an ACH "R01" / NSF code) on the Flex IQ payment beta, and settled the plan for the first single-unit pilot.

**How retries work.** JVL does not move money itself — Dwolla does. Dwolla treats every attempt as a brand-new transfer, so a true Nacha "re-initiation" is not possible. A resubmitted payment simply runs again as a new ACH transaction stamped with a retry code. Nathan confirmed this with Dwolla (Nancy).

**Proposed (post-MVP) flow.** On an NSF, Payment Hub would flag the customer as "verify balance," run a balance check before the next debit, and re-queue the transaction the next day. Because it is the next day, there would usually be a second invoice too, and Nacha requires each invoice to be matched and initiated separately. Balance checks exist but are currently switched off (deferred after alpha); the cost is negligible.

**Who is the customer / whose bank account.** Long discussion about master operator vs. location. AKS (the hottest prospect) wants JVL to deal directly with the location's bank account; masters generally do not want to be in the payment loop. Legal risk: if the contract is only with the master, JVL cannot pursue the location; to bill the location, JVL needs the location's agreement/consent. Andrei noted the current Payment Hub design lets only the master assign the Dwolla wallet per location, which may be wrong. Val's position: the agreement should be between the location and JVL (whoever's bank account is used), and this is mandated by Incomm ("it's not our thing — Incomm requires the location bank account").

**MVP discipline (Val, firmly and repeatedly).** Do not add new scope. For this beta: no retry automation, no balance check, and no blocking of any location. On an NSF the invoice simply stays unpaid in MSBC and is reconciled manually (credit card or check); Payment Hub will not know about out-of-band payments in the MVP, which is acceptable because nothing is blocked. Pavel's idea of a manual "try again" button is agreed as a next-version item.

**Single-unit go-ahead.** Place one Flex IQ unit in one beta location. Val does not need a signed customer agreement for this one unit and does not want to delay. Andrei needs the JVL–Dwolla contract signed to register a production location and assign a bank account; the Dwolla account is not active yet. Pavel already emailed Dwolla asking what is still needed — if no reply by end of tomorrow, they will use a manual workaround (fake bank-account assignment) for the single location.

**Technical readiness.** Andrei's last build had no crashes or errors. One minor issue remains: a "Mutagus / Mother Goose tilt" — if Mutagus powers on before IQ, IQ reports Mutagus as not detected (100% reproducible in Georgia, never in Minsk; tied to different EVO/motherboard versions and a comport-to-printer mirroring change). Fix workaround is to power-cycle Mutagus. The remaining software item is remote software update (Pavel, ~1–2 weeks); Val wants it flawless ("like a Swiss watch"). The cellular modem runs modem-only, is stable, on T-Mobile with good Georgia coverage.

**Invoicing.** Payment Hub does not email invoices; this will likely be set up in MSBC. Each location has a dedicated email. The customer invoice will show line-item fees (not a single service fee). Nathan will generate the current line-item version for review. Nathan is finishing QA items on the ledger/MSBC flip today.

**Agreement / timeline.** Juan's 10-page master agreement (JVL's own) needs re-review and shortening but is not required for the one beta location. Target: Dwolla signed ~Wednesday, install the IQ unit ~Thursday. The Georgia expo next week is only a ~6-hour fragment and is not worth a 2-week delay. Val asked Andrei to also start negotiating with another operator from the short list.

## Decisions Made

- **Beta MVP handles NSF manually, with no new automation** — no retry/re-initiation logic and no balance check added; NSF invoices stay unpaid in MSBC and are reconciled by credit card or check. (Decided by Val; agreed by Nathan.)
- **No location will be blocked for insufficient funds during the pilot.** (Confirmed by Pavel, Andrei, Juan.)
- **A manual "try again" / re-initiate button is deferred to the next version, not the MVP.** (Andrei, Pavel.)
- **Proceed with a single-unit beta** — one Flex IQ in one location; no signed customer agreement required for this one unit. (Val.)
- **Use the location's bank account** (as mandated by Incomm), not the master's. (Val.)
- **Customer invoices will show line-item fees.** (Val, Juan.)
- **Target schedule: Dwolla contract signed ~Wednesday, install the IQ unit ~Thursday; do not delay for the Georgia expo.** (Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda (lead), Andrei Klimovich | Get the AKS location agreement executed / push AKS to sign | This week (TBD) | High | Val: it's mainly on Felipe to secure the signed AKS location agreement |
| 2 | Pavel Frolov / Andrei Klimovich | Follow up with Dwolla on what is still needed to activate the account and register the location; if no reply, proceed with workaround | Aug 11 (by end of tomorrow) | High | Email already sent; Dwolla account not active yet |
| 3 | Pavel Frolov | Check the Dwolla dashboard for production access / setup status | Aug 10 (today) | High | Last checked Friday |
| 4 | Pavel Frolov | Finish remote software update; it must work flawlessly | ~Aug 24 (1–2 weeks) | High | Val: "like a Swiss watch," with all error checks |
| 5 | Pavel Frolov | Talk to Genadi about the Mutagus / Mother Goose "tilt" (not-detected) issue | Aug 10 (today) | Normal | 100% reproducible in Georgia, not in Minsk |
| 6 | Nathan Carver | Finish the QA items on the ledger / MSBC flip | Aug 10 (today) | Normal | Owed to QA |
| 7 | Nathan Carver | Generate the current line-item customer invoice and send it for review | TBD | Normal | Payment Hub doesn't email; likely set up in MSBC |
| 8 | Juan Martinez | Draft the location banking-information agreement; re-review and shorten the 10-page master agreement | TBD | Normal | 10-page master not needed for the one beta location |
| 9 | Andrei Klimovich | Begin negotiating with another operator from the short list, in parallel with AKS | TBD | Normal | Val's request; short list exists |

## Open Questions

- Does AKS want to use one (master) bank account across its locations, or require each location to assign its own account? (Andrei to clarify with AKS — different flow for JVL either way.)
- Is the JVL–Dwolla contract actually signed? Val believes it has been; Pavel/Andrei to confirm with Dwolla.
- Can AKS execute contracts this week? (Unknown — depends on Felipe.)

## Dispatch Log

---
*Processed from Teams transcript on August 10, 2026 (scheduled meeting-watcher sweep)*
*Source meeting: Failed ACH payments: business needs and approach*
