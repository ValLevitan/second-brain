---
type: organization
title: Incom (payment processor)
date: 2025-02-27
aliases: [Incom, InComm, Incomm, Income, Incom Payments]
source-count: 13
open-commitments: 3
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
- **John** — facilitated/introduced the call; surname **Houseal** given on the Apr-3 COAM payment-options recording (the InComm lead who walks through the gift-card solutions). [[raw/incomm_commissioning_plan_february-27-2025.md]] [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **Allen Lee** — the InComm "Alan" (technical/API contact); started/hosted the Teams transcription on the Apr-3 payment-options call; likely = the "Alan" of the Feb-27 and Mar-19 calls (same first name, InComm technical role — inference). [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **Jared** — InComm-side; owns the security stance on the barcode balance-check (agreed to a PIN-based approach). [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **Adam** — Atlanta-based; holds the compliance detail — the standard consumer-facing **language/terms** the kiosk must display — and will review JVL's consumer-experience demo (in person at JVL's shop or by video). [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Billy** — receives the merchant setup form from JVL and works with Incom's contract admin to assign JVL a unique merchant ID. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- **Susanne** — handed Alan the sample card on the Mar 19 user-cases call (role not stated). [[raw/incomm_flex-pay_user_cases.md]]

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

## Mar 19 2025 — card dispensing/activation user-cases walkthrough (Alan)

Alan took the JVL team step-by-step through issuing a prepaid card from the kiosk ([[wiki/meetings/2025-03-19-incomm-flexpay-card-user-cases.md]]; a **Susanne** on the Incom side handed him the sample card): [[raw/incomm_flex-pay_user_cases.md]]

- **Card data:** the test cards carry identical data on the **magnetic stripe** and a **30-digit activation barcode** — first ~11 digits are the product **UPC**, the last 19 digits the **VAN (Virtual Account Number)** (track-one number beginning "605812"/"605823" — both cited on the call), printed under the barcode. Incom recommends a **barcode reader** so the card can be read **while still in the dispenser** (less mechanism, no need to dispense before reading); if magstripe-only, the UPC must be configured on the kiosk since it isn't on the stripe. The kiosk should support **UPC configuration per product** (Pavel asked to write the requirement; Alan framed it as supporting both MagStripe and barcode). [[raw/incomm_flex-pay_user_cases.md]]
- **Two-step activation:** first a **pre-authorization** (non-financial — verifies connectivity, kiosk setup, card number and loadable amount), then — after redeeming the winning ticket — an **Activate** call with near-identical fields but a new transaction ID. The card must **never be handed to the consumer before activation completes**; failed cards go to an internal **escrow bin/tray** for troubleshooting, never to the player. [[raw/incomm_flex-pay_user_cases.md]]
- **IDs and reconciliation:** requests carry access ID (test credential "ICT test," lowercase i), **merchant ID** (assigned by Incom), **store ID** (assigned by the Incom merchant so their activation reports reconcile — not invented by JVL), and **terminal ID** (JVL's own kiosk identifier); a **machine setup form** per deployment tells Incom/the merchant who and where (MLH/LLH names, address). All fields must be kiosk-configurable. [[raw/incomm_flex-pay_user_cases.md]]
- **Fees and limits:** consumer pays a **$2 fee** (e.g. redeem $22 to load $20 — only the load amount is sent to Incom); the fee is revenue-shared down the chain location→merchant→Incom (Alan's split figures were explicitly "a sample value"). Card max is **$1,000**; the minimum he needed to re-check with Adam ("either $10, $20 or $1"). [[raw/incomm_flex-pay_user_cases.md]]
- **Downstream use:** at merchant POS only the **magstripe/track-two** matters — "MasterCard does not know anything about" the VAN or barcode, which exist solely for activation between JVL and Incom; the mobile number/email capture is **optional**, only for sending Ts&Cs ("no validation code required to use the card"). A returning player's card **cannot be deducted** by the kiosk — "there is nothing you can do with that card" (whether the card could fund more play is a question Alan would take to John). Incom doesn't care how kiosks reach JVL's gateway — only the gateway talks to Incom. [[raw/incomm_flex-pay_user_cases.md]]
- The product's UPC context: the card discussed is the "**COEM card**" (as transcribed — consistent with the Georgia COAM redemption card this integration serves). [[raw/incomm_flex-pay_user_cases.md]]

## Status (Mar 27 2025)

- Val reported: **all contractual agreements with Incom are signed**; the additional information Incom requested was supplied by **Monika** (see [[wiki/people/monica.md]]); "any day they will approve us as a vendor and will open the connection for testing." The planned beta (3–5 free-of-charge operator locations) runs connected to Incom in both regimes (QR-code/FlexPort and TITO). See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## COAM gift-card solution meeting — "JVL Payment Options" (John Houseal)

The market/solution meeting Val committed to on the Apr 2 SMIB call — owner Val, "Timeline: Today, tomorrow, or Monday," purpose "Discuss market dynamics and understand operator strategies" [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]. The substance was first captured from a derived notes document (see [[wiki/meetings/2025-04-03-incomm-coam-gift-card-solutions.md]]); the **actual Teams recording** ("JVL Payment Options," ~36 min, **John Houseal** / **Allen Lee** InComm-side, with Val and Juan) is a fuller, speaker-labelled transcript of the same meeting and confirms every point below plus the detail in the next subsection. **Date discrepancy (see Open contradictions):** the recording header dates the meeting **April 3, 2025, 5:42 PM**, while the derived notes are headed **April 7** — recorded, not resolved. **John Houseal** (the Incom lead) and Val worked the merchant problem that **gift cards can't be used to play at COAM machines**, so merchants fear losing in-store spend (feedback "from multiple operators"; use case: a $100 win loaded onto a MasterCard can't fund further COAM play). [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]] [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]

- **Three solution options (John):** (1) player asks the **clerk to swipe the card for cash** (no system changes); (2) contract a **merchant acquirer** to put card readers on kiosks/machines — rejected as unattractive: **$50–$200/month maintenance + 3% transaction fee** (a $100 transfer nets the merchant $97); (3) **barcode on the card** processed **directly with Incom** — no merchant acquirer, no 3% fee, avoids **PCI compliance** ("the barcode is not considered payment card information"), only a modest **~$20–25/month** accounting/settlement fee. [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- **Barcode security:** protected by a **PIN set on first use** (first PIN entered becomes the card's PIN); changeable anytime via **IVR or the website**. [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- **Role model:** location houses the machines; machine owner manages them; **JVL supplies the machines/kiosks**; **Incom is the program manager and technology provider** (gift-card product + APIs, money movement, compliance) — Incom **does not build kiosks**; operators design their own kiosk configurations (card readers, digital wallets, etc.). [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- **Incom's expansion plans:** targeting **Texas, Florida, Pennsylvania, Nebraska and Iowa** "to improve the player experience and reduce dependence on cash," with per-market product adaptations — ATM-usable cards in Pennsylvania, large-win payouts in Nebraska — plus a **print-on-receipt** product for merchandise markets (player picks among gift-card providers). [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- **Follow-up:** Juan + Val to "regroup and think of a proper business model" for the discussed solution. The card-scanning prospect surfaced the same day in the FlexPort scanner ruling — see [[wiki/decisions/2025-04-07-flexsmib-modern-flexport-legacy.md]]. [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]

### Detail the recording adds

- **How the money actually moves:** funds sit on a gift card held in an account at **Sutton Bank** that InComm manages. When a player scans/authorises a purchase, InComm confirms the balance and the merchant gives the player play-credit *immediately*; InComm then **wires the merchant whole (~a day later)** — the merchant extends credit on the belief InComm will pay, because InComm holds the card balance. InComm must now process not just gift-card activations but **redemptions/spend**, routing money back to the **7,000 merchants** in "Co-In." [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **PIN mechanics:** the barcode balance-check can't be done today (Jared wants PIN-based for security, since the barcode is exposed and "roommates can take photos of it"); PIN is **set on first use** (whatever four digits are first entered), one PIN per barcode, changeable via IVR or website. **Cards are not reloadable** — a player gets a **new card each cash-out**; "those are the rules until 2026." Making cards rechargeable would require **KYC** on the player, "which I don't think anybody wants to do." [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **PCI:** option 2 (mag-stripe reader) is in PCI scope because it reads real card data (16-digit number, expiry, CVV) sent to MasterCard; option 3 (barcode) is **outside PCI scope** because the barcode "means nothing to MasterCard… only to InComm" — InComm makes it payment information only inside its own wall, insulating the industry. [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **The four participants (Val's framing):** the **location** (houses machines), the **master** (owns/routes the machines), **JVL** (supplies machines/kiosks), and **InComm** = "the **program manager** for the gift-card product and the **technology provider** for the APIs" and money movement (all regulated in the US) — InComm **does not build equipment** ("that will not happen"). Val questioned the point of a kiosk at all; John: most people want to limit clerk interaction and keep the gaming environment self-sufficient. [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **Operators design their own flow** — John's examples: **Excel** (owns **Bulldog Entertainment** in Georgia) puts a kiosk in every location, using TITO + a digital wallet; **Intermax at Kroger** wouldn't pay **~$15,000** per kiosk so they hung cards and put optical readers on the machines (ran into problems, now looking at kiosks); **United** (~1,300 locations) is deploying handheld devices to associates rather than $10–15k kiosks. [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- **Juan's opening framing (from the pre-recording audio):** kiosk-product rollout is slow — "maybe three to 400 with thousands to go" — and someone at the GAMOA meeting asked "how does anyone expect us to do this in one year's time"; masters/locations are "savvy… used to skating around the letter of the law," hence the gift cards; Juan's worry is that an automated kiosk lets a player walk away, whereas a window redemption keeps the location owner able to upsell. [[raw/incomm_meeting—april-3-2025-1.md]]
- **Fannin County detail:** **Pace-O-Matic** sued the sheriff's office in **Fannin County, Texas** and a judge ruled its machines were **skill machines, not gambling machines** — "the first time a court in the state of Texas has ever issued an opinion on these devices" — driving InComm's Texas interest. [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]

## Open commitments

- [ ] Val + Juan — regroup and define a proper business model for the COAM gift-card solution (barcode option) — due unspecified — [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- [ ] Incom (Alan) — send JVL the blank **location onboarding / merchant setup form** and (Adam) the standard consumer-facing language/terms — due "after this call" (Feb 27) — [[raw/incomm_commissioning_plan_february-27-2025.md]]
- [ ] JVL (Val/Juan) — complete Incom's merchant setup form and arrange the in-shop first-machine production test; produce the consumer-experience demo for Adam's review — due unspecified — [[raw/incomm_commissioning_plan_february-27-2025.md]]

## Visa / card-back-into-play talks and future scanner requirement (Apr 8–11 2025)

- **Card usable for betting:** Val told the FlexPay-Evolution group "later this year, Incom promised to have a card that you're able to use for betting inside the machines" — the missing ingredient for the temporary-wallet business model (today that possibility is "very expensive. Like $3 per transaction or something like this" elsewhere; "in Incom's case, it's much cheaper"). [[raw/flex_pay_evolution-april-8-2025.md]]
- **Visa route:** the Georgia COAM market complains the prepaid-MasterCard payout "takes all this winnings out of the immediate circulation of the gaming business"; Incom "now is in talks with Visa" for a card the machines can validate — Visa charges ~3% of value today, "but if income does the banking cycle internally, then they could keep the cost manageable," making JVL "a reoccurring partner with them." [[raw/evolution_flex_pay-april-11-2025.md]]
- **PCI-compliant optical scanner:** per JVL's last Incom call, the optical card scanner must be **PCI compliant** as a MasterCard requirement for a future Incom technology (optically scanning the card and treating it as a debit-type transaction, eliminating the ~3% fee); Juan to re-check the notes so the FlexPort/kiosk hardware dimensions allow a scanner swap-out. [[raw/evolution_flex_pay-april-11-2025.md]]
- **Fraud onus reminder (Val):** the signed Incom agreement "puts the onus on the individual or the company who signed … to ensure that there is no fraud" — the reason JVL's cheap payout devices must validate tickets against a mini TITO/SAS server, and why Val refuses to proxy-sign for Mother-Goose-only operators. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_pay_evolution-april-8-2025.md]]
- "John from Income" (the Apr-7 John, by context) reported masters want "the automated solution so that no clerk is involved." [[raw/evolution_flex_pay-april-11-2025.md]]

## Open questions

- Can a customer use **any** debit card at the kiosk, or only a prize-redemption/COAM card? The industry treats prize-redemption debit as allowed, plain debit as unknown, credit as prohibited. [[raw/incomm_commissioning_plan_february-27-2025.md]]
- Would the regulator (GLC) treat an open-loop retail gift card (e.g. from Walgreens) the same as a COAM prize-redemption card? Unresolved. [[raw/incomm_commissioning_plan_february-27-2025.md]]

## May 20 2025 — described as the GLC-sanctioned processing monopoly (BDC call)

On the [[wiki/meetings/2025-05-20-bdc-flexport-ga-coam-financing.md|BDC financing call]] Val characterised Incom (transcribed "**Income**") as a **monopoly sanctioned by the Georgia Lottery Corporation (GLC)** — "a six-billion-dollar U.S. company" doing the **last-mile conversion of fiat money to digital money and depositing it on a MasterCard**. JVL's equipment sits between the player and Incom, connected to three points (JVL's platform, the GLC/JLC platform, and Incom's platform), earning revenue from hardware sales and from **processing the fiat→digital conversion**. Consistent with the payment-processor role documented above. [[raw/bdc_intro_to_flex-port_ga-coam-may-20-2025.md]]

## Open contradictions
- ~~InComm COAM gift-card meeting date: Apr 3 vs Apr 7.~~ **RESOLVED BY OWNER (2026-07-15): it was a two-day meeting** — Apr 3 (first session, Teams recording) and Apr 7 (second session, derived notes) are BOTH genuine session dates of one meeting. Recorded on one stub [[wiki/meetings/2025-04-03-incomm-coam-gift-card-solutions.md]] (Apr-3 primary, Apr-7 second session; facts attributed per session where distinguishable). This **supersedes** the earlier §11 auto-resolution to Apr-3-only — a derived-notes date can also be a real second-session date.

## May 30 2025 — the live test cycle at Felipe's office ([[wiki/meetings/2025-05-30-qa-flexport-flexpay-plan.md]])

On the FlexPort/FlexPay QA-plan meeting Val described how Incom will support JVL's commissioning: as an **exception**, Incom will create a **fictitious test location** inside **Felipe's Georgia office** (assigned a real location number) so real money flows through Incom's **production** environment. The test is chiefly to prove the **positive money-transfer cycle** with Incom — play → Temporary Wallet → validate at FlexPay (full or partial) → money to Incom → Incom registers → card issued → Incom sends to **JVL Bank**, which takes a **commission** → Incom invoices JVL for the player winnings. **Juan** will receive the Incom reports by **email** (mailboxes created by **Andrei**). Val again characterised Incom as a **~$6-billion company** that moves slowly, so JVL must run thorough internal tests before each live test. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]

## Sources

- [[raw/qa_flex-port_flex-pay_plan-may-30-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-11.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/incomm_commissioning_plan_february-27-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/incomm_flex-pay_user_cases.md]]
- [[raw/2025-04-07-COAM_gift_card_solution_incomm_notes.md]]
- [[raw/SMIB_FlexPay_Action_Items_April_2_2025.md]]
- [[raw/flex_pay_evolution-april-8-2025.md]]
- [[raw/evolution_flex_pay-april-11-2025.md]]
- [[raw/incomm_transcript_gacoam_payment_options-april-4-2025.md]]
- [[raw/incomm_meeting—april-3-2025-1.md]]
- [[raw/bdc_intro_to_flex-port_ga-coam-may-20-2025.md]]
