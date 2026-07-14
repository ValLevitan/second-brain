---
type: organization
title: Incom (payment processor)
date: 2025-02-27
aliases: [Incom, InComm, Incomm, Income, Incom Payments]
source-count: 4
open-commitments: 2
open-questions: 2
---

# Incom (payment processor)

Incom is the third-party **payment processor** JVL is integrating with to activate and read the Georgia **COAM prize-redemption cards** through JVL's pay-kiosk. It supplies the card-activation/balance-check API and the test/production credentials; JVL's FlexPay/FlexPort kiosk is the client. Spelling appears as "Incom" in the meeting body (and "income" for the card VIN) and "incomm" in the source filename; kept both plus "InComm" as aliases pending confirmation (see Owner Decisions). [[raw/incomm_commissioning_plan_february-27-2025.md]]

Earlier appearances: on the Feb 11 and Feb 18 embedded standups Incom was named as the payment processor supplying the **test server**, with a **production contract awaiting Val's signature** and card-provider fields to fill in the FlexPay activation sequence. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]] and [[wiki/topics/jvl-machine-lineup.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]

## Feb 27 commissioning-plan call

The onboarding kickoff between JVL and Incom. [[raw/incomm_commissioning_plan_february-27-2025.md]]

### Incom-side people (roster — external contacts, no individual pages)
- **Alan** — technical/API contact; provides the test PAN numbers and the UPC needed for the balance-check test, and can reset test cards. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Paul** — attended; took questions on card usage. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **John** — facilitated/introduced the call. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Adam** — Atlanta-based; holds the compliance detail — the standard consumer-facing **language/terms** the kiosk must display — and will review JVL's consumer-experience demo (in person at JVL's shop or by video). [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Billy** — receives the merchant setup form from JVL and works with Incom's contract admin to assign JVL a unique merchant ID. [[raw/incomm_commissioning_plan_february-27-2025.md]]

### Test vs production environments
- JVL's current credential is a **development credential** that works **only in the test environment**; testing uses a **"flight" test card**. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- Path to production: JVL submits Incom's **merchant setup form** → Billy + contract admin (said to take "a couple of weeks") → Incom assigns a **unique merchant ID for JVL** (transcribed "JBL") → Incom issues a production **user ID and secret** that work only in production, using a different endpoint → JVL configures its machines with the production credential and activates a **production Georgia Core card** (not the flight test card). [[raw/incomm_commissioning_plan_february-27-2025.md]]
- Incom wants to work with JVL **in the shop** on the first machine to confirm it is configured with the production credential and can activate a production card; after that, per-install testing can be streamlined, but the technician should still send a **test transaction from the location** so Incom can verify the machine is configured correctly. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- Why per-location verification matters: Incom described a kiosk operator who shipped machines misconfigured with the wrong location's store ID, so all activations came in under the wrong location and the billing was wrong — Incom only knows the store ID it is told. [[raw/incomm_commissioning_plan_february-27-2025.md]]

### Balance-check API
- Balance check is currently **out of scope** for JVL's kiosk because it can't swipe cards yet, but Incom and JVL agreed to **test and certify the balance-check API now** by feeding a **PAN number** (Incom supplies test PANs) rather than a physical swipe; the test card already carries PAN data on track one plus the Incom VIN. A number "549345" was referenced for the test. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- A standard **MAG card reader** (not EMV) is sufficient for the card. Test cards can be reset with a **reversal** or a **deactivation** transaction so the same test card is reusable. [[raw/incomm_commissioning_plan_february-27-2025.md]]

### The COAM / debit-card legal state (per Incom)
- The industry read Incom gave: using a **credit card** is prohibited, using a **debit card** is unknown, and using a **debit card issued as a prize redemption** is allowed — "the state of the market today." At least two operators are already doing this; one restricts to **COAM cards** only, the other may accept any debit card. Whether a regulator (the "GLC" — Georgia Lottery Corporation) would treat a Walgreens open-loop gift card the same is unclear. [[raw/incomm_commissioning_plan_february-27-2025.md]]

## Status (Mar 27 2025)

- Val reported: **all contractual agreements with Incom are signed**; the additional information Incom requested was supplied by **Monika** (see [[wiki/people/monica.md]]); "any day they will approve us as a vendor and will open the connection for testing." The planned beta (3–5 free-of-charge operator locations) runs connected to Incom in both regimes (QR-code/FlexPort and TITO). See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## Open commitments

- [ ] Incom (Alan) — send JVL the blank **location onboarding / merchant setup form** and (Adam) the standard consumer-facing language/terms — due "after this call" (Feb 27) — [[raw/incomm_commissioning_plan_february-27-2025.md]]
- [ ] JVL (Val/Juan) — complete Incom's merchant setup form and arrange the in-shop first-machine production test; produce the consumer-experience demo for Adam's review — due unspecified — [[raw/incomm_commissioning_plan_february-27-2025.md]]

## Open questions

- Can a customer use **any** debit card at the kiosk, or only a prize-redemption/COAM card? The industry treats prize-redemption debit as allowed, plain debit as unknown, credit as prohibited. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- Would the regulator (GLC) treat an open-loop retail gift card (e.g. from Walgreens) the same as a COAM prize-redemption card? Unresolved. [[raw/incomm_commissioning_plan_february-27-2025.md]]

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/incomm_commissioning_plan_february-27-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
