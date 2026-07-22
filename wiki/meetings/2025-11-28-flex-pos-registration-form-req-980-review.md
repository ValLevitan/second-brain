---
type: meeting
title: Flex-POS registration form — requirement 980 walkthrough (customer/location onboarding) (Nov 28 2025)
date: 2025-11-28
aliases: [Flex-POS registration form, requirement 980 review, RAQ 980, Payment Hub Specification 980, LSA location service agreement, POS registration form Nov 28]
source-count: 1
open-commitments: 6
open-questions: 2
---

# Flex-POS registration form — requirement 980 walkthrough (customer/location onboarding) (Nov 28 2025)

**Date:** 2025-11-28 (recording header 03:01pm; base name `Flex-POS_registration_form-20251128_100122`) · **Duration:** 1h 10m 18s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]]. English. (Mery and "Igor" referenced but not speakers; Nathan Carver named as optional for a future Dwolla call.)

A line-by-line walkthrough of **JIRA requirement 980** ("Payment Hub Specification"), driven off Pavel's email + Juan's reply, defining the **customer/location registration web form** for the Georgia payment-hub product. Continues the POS-registration onboarding thread from the [[wiki/meetings/2025-11-06-payment-hub-ach-spec-review-registration-onboarding.md|Nov-6 "POS registration procedure" session]] and the ACH-spec arc; substance folds into [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-28 ACH-spec section).

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and grepped the whole wiki: `raw/Flex-POS_registration_form.md` is cited nowhere else. It is a **Nov-28 3:01 PM** Val/Juan/Pavel call reviewing requirement 980 — separate in date, attendees and content from the Nov-5/6/10 ~7 AM ACH-spec sessions (this one is specifically the registration *form* / field-by-field acceptance criteria + the location-service-agreement + money-flow discussion). Confirmed new.

Durable points (single source):

- **Registration is phased and each phase is shown to the customer.** Resolved to **phase 1 = customer account creation** (first/last name, email, password; verify email + cell), **phase 2 = location creation** (location fields entered), **phase 3 = location approval** (via InComm → Georgia Lottery, may take up to 3 business days). The status indicator prominently displays the stage; JVL messages the registered cell/email when the customer can proceed. Data is **saved server-side** (not browser-local) so the customer can resume, switch device/browser; Pavel proposed a "template" status for saved-but-unvalidated registrations. [[raw/Flex-POS_registration_form.md]]
- **Field decisions (acceptance criteria).** Abbreviations get decoded in parentheses — **LLH = Location License Holder** (name; alphanumeric), **MLH = Master License Holder** (number; numeric), **DBA** (doing-business-as, if applicable). Address fields grouped **under the LLH**. **Cell phone → multinational format** (an immediate Colombia requirement changed Val's mind from US-only). Email/cell verification accepts **code or link** (Pavel: likely both, since some mail providers cut links). Two fields to challenge with InComm: **"hours of business operation"** (JVL doesn't want it; on InComm's form) and the **MLH number** (only relevant if selling to a multi-location "United"-type owner) — both "if applicable," non-blocking, but Juan to verify with InComm. [[raw/Flex-POS_registration_form.md]]
- **"Master Service Agreement" renamed to "Location Service Agreement" (LSA).** Val disliked "master" (collides with master license). The **LSA is a contract, legally binding once both parties execute it**, and **no changes/redlines are allowed** — take-it-or-leave-it via **electronic signature** (if Georgia permits e-sig on these), because allowing any negotiation would stall JVL indefinitely and the agreement is tightly integrated with **InComm, Dwolla and Plaid**. E-signature apps provide a download after execution. [[raw/Flex-POS_registration_form.md]]
- **Persona = the location owner; one communication channel.** The person entering location fields is treated as the **location owner** (simplified for engineers, not "authorized representative"). **One email + one cell** = the single channel; even a multi-location owner gets all reports to one address (can be sorted by location). A future (non-MVP) **organizational-structure / secondary-email / two-way-transaction-authentication** feature is documented but parked. [[raw/Flex-POS_registration_form.md]]
- **No validation against a state location list; no data storage.** LLH location name is **free alphanumeric, no validation** — JVL will **not** validate against Georgia's approved/master list (manual, kills automation; Nebraska/Texas don't even publish such lists — Nebraska "not as sophisticated as Georgia," Texas "doesn't recognize this part of the business"). **Fraud protection = InComm** (if InComm gets GLC approval, that suffices). Val's rule: **store no location/state data at all — and advertise that JVL stores no data** (avoids liability, no benefit to storing). [[raw/Flex-POS_registration_form.md]]
- **InComm integration (for now, email).** On submit, JVL extracts the required fields and **emails them to InComm** from a **new JVL group email address** (so several people see it, not one). On InComm's validation reply, a JVL person **manually presses an "enable" button**, which auto-emails the customer to resume/add locations and flips the location status. InComm confirmed (via John) there is **no API/lookup** — they send a spreadsheet to GLC and wait 1–3 days for an email approve/deny; Val is separately asking John whether approval can be made instant (John to take it up with Allen Monday). [[raw/Flex-POS_registration_form.md]]
- **Bank-account linking parked for a Dwolla call.** Linking a location's bank account (Val: "link," not "assignment") via the **Dwolla + Plaid widget** was parked — Juan to set up a dedicated call with Dwolla (Val + Juan + Pavel; Nathan optional). Val's money-flow model (90% sure, to confirm with Dwolla): funds move **location → Dwolla's intermediary bank → (pause) → JVL bank** in one motion; the **JVL account is never cross-referenced to a location** (the location is cross-referenced to Dwolla's intermediary bank); **Plaid** only **verifies the account exists + balance-checks**, then an ACH relationship is established. Reconciliation consequence: swiping 10 accounts = **11 charges** (10 customer pulls + 1 Dwolla→JVL transfer), and the two reports must match minus the ACH fee. Pavel's read differs (one JVL Dwolla account accumulating all) — left to the Dwolla call. Juan's Venmo/Plaid anecdote: Plaid pops up, detects the bank, no Plaid account needed, all in-app. [[raw/Flex-POS_registration_form.md]]
- **Development posture.** Igor to **redo the Figma mockup** reflecting the part-1/part-2 split; QA to start reviewing the acceptance criteria and how to test them. Val told Pavel's team to **develop architecture, break work into features + acceptance criteria, and lay out Jira plans — but park actual coding** until the spec is clarified. Val will run the transcript through AI to summarise the blocking steps. [[raw/Flex-POS_registration_form.md]]

## Open commitments

- [ ] Juan Martinez — verify with InComm the necessity of the "hours of business operation" field, and the grounds for the MLH-number field — due ~next week — [[raw/Flex-POS_registration_form.md]]
- [ ] Juan Martinez — amend requirement 980: decode LLH/MLH/DBA in parentheses; rename Master Service Agreement → Location Service Agreement; state LSA = a legally-binding contract that cannot be modified — due unspecified — [[raw/Flex-POS_registration_form.md]]
- [ ] Juan Martinez — set up a dedicated call with Dwolla (Val + Juan + Pavel; Nathan optional) to settle bank-account linking / money-flow / reconciliation — due early next week — [[raw/Flex-POS_registration_form.md]]
- [ ] Val Levitan — relay John@InComm's reply (expected Monday) on whether location approval can be made instant rather than up to 3 days — due ~Monday — [[raw/Flex-POS_registration_form.md]]
- [ ] Igor (registration-form UI/Figma; identity unresolved — see §4 note) — redo the Figma mockup with the part-1 (customer) / part-2 (location) split — due unspecified — [[raw/Flex-POS_registration_form.md]]
- [ ] Pavel Frolov / team — develop the architecture and business flow, break into features + acceptance criteria, lay them into Jira plans, bring in QA — but do not code until the spec is clarified — due unspecified — [[raw/Flex-POS_registration_form.md]]

## Open questions

- Is the ACH flow a Dwolla wallet/balance path or a direct bank-to-bank transfer, and does JVL's account ever cross-reference the location? Val and Pavel model it differently; parked for the dedicated Dwolla call. [[raw/Flex-POS_registration_form.md]]
- Can InComm approve a location instantly rather than in 1–3 business days (no API today; spreadsheet → GLC → email reply)? Awaiting John/Allen. [[raw/Flex-POS_registration_form.md]]

**§15.8:** clear — product/registration-form and vendor (InComm/Dwolla/Plaid) process only; no per-person compensation. (The ~$10/gift-card and per-account pricing sketch are product economics, not compensation.)

**Same-name note (§4).** "Igor" here is the **front-end / UI designer** who built the initial registration web page and owns the Figma mockup — **not clearly resolvable** among the roster Igors (candidates: [[wiki/people/igor-nazarenka.md|Igor Nazarenka]] = mobile-app/UI, or Ihar Hrybko = UX/UI); left unresolved and queued rather than force-matched. "Mery" (asked to decode abbreviations in the requirement) is named only in passing. [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/nathan-carver.md|Nathan Carver]] as usual.

## Sources

- [[raw/Flex-POS_registration_form.md]]
