# Meeting Summary — FLEX-IQ Complete MVP: Cashier & Player Flow Demo
**Date:** May 26, 2026 — 3:02 PM (recording start)
**Duration:** ~1h 9m
**Attendees:** Andrei Klimovich, Pavel Frolov, Irina Shishko, Val Levitan
*(Alexey "Lesha" Khamin and Ivan "Vanya" Shpak assisted on-site in Minsk with the hardware and test cards.)*

## Summary

Pavel and Irina walked Andrei and Val through the full FLEX-IQ MVP, end to end: install a device, set up a customer and location, fund it, and run a cashier payout. The demo had two halves — the software flow on screen, then a live look at the physical hardware assembled in Minsk. The meeting was held in Russian.

**Device install.** Andrei played the JVL technician. He logged in under his own JVL account, scanned the device QR code and the barcode sticker, and the FLEX-IQ device registered. FLEX-POS came up registered.

**Customer and location setup.** Andrei opened the registration link Pavel had shared. He entered an email, received an activation code, verified the email, and validated a phone number, then filled in the location details. Two Georgia license types are supported: operate under your own license, or operate under someone else's as a "Master License Holder" (that option reveals an extra field). Roles are not built yet — right now everyone at JVL has full access to this site, and roles are required before real operation. The flow expects a JVL person (Juan, Andrei, or whoever covers the Georgia market) to check and approve the license-holder data the customer enters — i.e., confirm the customer actually holds a license.

**InComm.** Once the location is approved, its data is sent to InComm (today by separate email). InComm approves, then JVL approves and enters the InComm fields back in. InComm generates these fields per location, per customer, and right now they must be copied and pasted by hand each time. The values used today were sandbox test cards. The InComm workflow (email vs. an alternative they might offer) still needs to be defined.

**Funding and go-live.** A license expiry date was set (how long the device may operate). A funding source was attached through Payment Hub using sandbox values, and the location flipped to "operational." The terminal then showed idle time.

**Cashier and player flow.** The cashier enters a PIN; the keypad layout shuffles every time on purpose so no one can watch which keys get pressed. Last tickets printed by the Mutha Goose were listed, and any ticket can be redeemed or voided. On a redeem, the player screen shows the withdrawal plus a fee and asks to confirm. Andrei flagged the wording as unclear — it doesn't show the final amount the player actually receives. "Accept terms" can be pressed without scrolling to the bottom. The flow then offers a receipt by email or print, and the cashier swipes the player's magnetic card. The card did not issue — the InComm side failed and a machine/voucher number field is wrong. Pending transactions have no expiry; they stay in IQ indefinitely.

**Password / auth.** Both Andrei and Pavel were locked out of their accounts — Keycloak (the shared auth service) had no working password recovery. Pavel said recovery work needs to be scheduled soon.

**Hardware / Mutha Goose.** Lesha showed the assembled unit on camera. FLEX-POS splices in-line on a single cable: the Mutha Goose normally runs a DB9 cable to the printer (DB25 at the printer end). FLEX-POS has two DB9 ports and sits in the break between the Mutha Goose and the printer. A separate green RS-485 line daisy-chains the machines to the Mutha Goose. Andrei raised a constraint nobody had considered: in real shops the Mutha Goose usually sits well behind the counter, but FLEX-IQ is meant to sit on the counter facing the customer — so the connecting cable may have to run across a walkway where staff move constantly. Today's cable is about 1.6 m and can be made longer. Options floated: a longer off-the-shelf RS-232 extender (tested for reliability), or — per Val — possibly wireless later. Val called it a good point they hadn't thought about.

**Legal.** The terms-and-conditions PDF in the flow is a placeholder and must be replaced with the real JVL legal document before going live. Juan is drafting it; Andrei will sync with him.

Andrei's overall read: he is satisfied the system is ready for MVP, subject to a short fix list. He has not yet seen the hardware integrated on a real location.

## Decisions Made

- **Proceed to MVP.** Andrei is satisfied the system is ready to enter MVP, subject to a fix list. (Endorsed by Andrei and Val)
- **No abbreviations anywhere — make it house style.** Triggered by confusion over the "DBA" field. Spell things out on all screens and in all correspondence, always. (Decided by Val)
- **Defer UX nice-to-haves to a later release.** E.g., showing the three receipt options at once. Val: we can do whatever we need, just not in this release. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Log all demo comments into Jira as tasks or stories (no "improvement" type exists) | Right after meeting | Normal | Captures the fix list below |
| 2 | Pavel Frolov / dev | Find why the player card is not issuing — InComm side failed; voucher/machine number field wrong | TBD | High | Main blocker to a working payout |
| 3 | Dev team | Make the cashout display clearer — show withdrawal, fee, and final amount the player receives | July 5, 2026 | Normal | Andrei says it's a small change |
| 4 | Dev team | Switch the on-screen keypad to a standard QWERTY layout | July 5, 2026 (OK to slip) | Low | Current layout confuses users; minor |
| 5 | Pavel Frolov / dev | Schedule password-recovery work in Keycloak | TBD | High | Andrei and Pavel both locked out, no recovery |
| 6 | Juan Martinez | Draft the real JVL terms-and-conditions PDF to replace the placeholder | Before go-live | High | Required before operating |
| 7 | Andrei Klimovich | Sync with Juan on T&C progress | TBD | Normal | Asked ~a week ago; status unclear |
| 8 | Dev team | Fix the missing/incorrect machine (voucher) number on the printed ticket | TBD | Normal | Field shows wrong on the ticket |
| 9 | Dev team | Fix the Help screen to show the correct phone number and email | TBD | Low | Marked as an improvement |
| 10 | Pavel Frolov / dev | Test a longer cable (off-the-shelf RS-232 extender) for reliability to handle counter-to-Mutha-Goose distance | TBD | Normal | Cable may have to cross a staff walkway on real sites |

## Open Questions

- Why is the player card not issuing? Possibly wrong InComm fields or a server error — to be investigated.
- How to handle the physical cable run when the Mutha Goose sits far behind the counter (longer cable vs. wireless)? Not decided.
- The exact InComm workflow — email-based, or an alternative InComm may offer? Undefined.
- How does customer registration into InComm actually happen? Andrei said he doesn't fully understand it yet.
- Real-world hardware integration with the Mutha Goose — Andrei hasn't seen it on a live location.

---
*Processed from Teams transcript on June 9, 2026*
*Source meeting: [FLEX-IQ] Complete MVP Cashier, Player flow DEMO — May 26, 2026*
