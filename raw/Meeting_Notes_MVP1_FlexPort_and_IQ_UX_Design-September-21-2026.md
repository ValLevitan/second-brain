# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX
**Date:** September 21, 2026, 8:02 AM – 8:54 AM Eastern
**Duration:** about 52 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Andrei Bosik, Alexander Biratko
**Raw transcript:** [[Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026]]

## Summary

Andrei Klimovich walked the team through the finished UI/UX design for the FlexPort and IQ screens in MVP1. He said the functional side is fixed; only small design edits (text size, alignment) are left. Graphics stay as they are — no new visual language. The change is in the workflow (UX) and in the text.

**Cloud clean-up.** Irina created capability 229 to hold everything cloud-related so it does not block current development. Andrei was removing the remaining cloud mentions from capabilities and requirements while the call ran (capability 158 and requirements 1514, 1515, 1516, 1543 were named). Wallet work is local on the machine; only the card goes through the payment hub. Dzmitry asked everyone to mark this clearly in future reviews. Andrei said the clean-up would be finished about ten minutes after the call.

**FlexPort screen layout.** The layout is a grid of 4 horizontal swimlanes and 7 columns; every control has to fit that matrix. The language button moves to the top-left corner and stays there, which removes one step for the player — the ticket can be scanned straight away. A status zone sits on the right for technical icons. Screen resolution is 854 x 480, taken from Genadi.

**Status icons.** Andrei first wanted status icons only on the initialisation and idle screens. Pavel pushed back: roughly 70% of screens are error screens, and the icons carry useful information there. Andrei agreed to show them on error screens too. Andrei's view on player-facing logic stood: the player reacts to a clear message about his action, not to a pictogram.

**Printer tilts.** Andrei proposed permanent banners over every screen so a problem gets fixed fast. Pavel and Dzmitry objected — several banners at once would cover the whole screen, and a reporting screen does not need them. Andrei accepted he had over-engineered it.

**No paper in the printer.** This took the longest. Andrei's first idea was to create the wallet and let the cashier reprint later. Irina objected hard: the cashier has taken real money from the player and given nothing back, and the player will not come a second time. Dzmitry agreed the wallet should simply be invalid if nothing printed. The final rule splits by flow.

**IQ home and help screens.** The location name and address come from registration (the doing-business-as field plus the city). Help must show support contacts — the transcript names "Gell" and InComm — with phone number and working hours pulled from server configuration, so no rebuild is needed when a number changes. Competitors offer support roughly 6:00 to 23:00. Andrei said a separate support phone would be set up, answered by him or Felipe. Andrei Bosik suggested using an operator's virtual PBX number with call forwarding instead of a physical SIM; Andrei Klimovich accepted that.

**Wallet and card screens.** Reissue logic is guarded: the cashier can only issue a card against a wallet if he scans the physical media. Opening the wallet from transaction history without the media does not allow issuing. Amount entry shows only the dollar sign and inserts the decimal point automatically as digits are typed. "Create empty wallet" is a separate explicit button. After creating a funded wallet the screen repeats the balance and reminds the cashier to hand over the ticket and the receipt; the receipt is optional.

**Records and search.** Reprint is offered from the record details only while the wallet is still active, not after it expired. Card search gains a search on the last four digits of the barcode (card code, not card number) to settle disputes on the spot. Pavel and Dzmitry pointed out the four digits shown on the card front would confuse the cashier; Andrei agreed to add a clickable picture showing where to look under the barcode. The date picker control is still open — Dzmitry thinks the standard React one, to be confirmed with frontend.

**Machine identification.** With IQ moving into FlexPort, each port sits on one gaming machine, so a transaction needs a link to that machine. Today the port asks the machine for its serial number. Pavel noted Intralot assigns an asset number centrally, one per machine regardless of how many SAS ports are connected, and that this is probably the identifier that matters. Andrei did not want the identifier printed on the FlexPort screen where competitors visiting a location could read it.

**Texts.** Andrei built a text library: every interface element has an ID, and the library holds the English and Spanish text for that ID. Shared elements such as Cancel and Confirm exist once with a universal ID, reusable straight in implementation.

**Work split.** FlexPort screens go to Pavel's side, IQ screens to Dzmitry. Dzmitry will take the main flow because he can tie it to the business logic, and Vladimir will pick up the smaller pieces. Features cannot be created yet — Andrei has to load the capabilities and requirements into Jira first. There will be no feature lock today; possibly tomorrow. Andrei confirmed the team has enough work meanwhile.

## Decisions Made

- **Cloud scope is out of MVP1** — capability 229 holds it, and cloud mentions are being stripped from the MVP1 capabilities and requirements. Wallet lifecycle is local to the machine; only the card goes through the payment hub. (Decided by Andrei Klimovich, Irina Shishko, Dzmitry Chudzinau)
- **Cashier flow: check the printer before creating the wallet** — if the printer cannot print the carrier, the wallet is not created at all, so the cashier never takes money without giving something back. (Decided by Andrei Klimovich after Irina Shishko and Dzmitry Chudzinau objected to the reprint-later design)
- **FlexPort cash-out flow: create the wallet and send it to unclaimed** — the player at the machine cannot play any more, so the value must be preserved; the cashier prints it from the unclaimed screen. (Decided by Pavel Frolov, Dzmitry Chudzinau, Andrei Klimovich)
- **Tilts are not full-screen banners** — a red indicator at the top opens a list of current problems instead. (Decided by Andrei Klimovich, after Dzmitry Chudzinau and Pavel Frolov objected. Considered and superseded: Andrei's proposal to hang priority banners over every screen.)
- **Status icons also appear on error screens**, not only on initialisation and idle. (Decided by Andrei Klimovich after Pavel Frolov's objection)
- **Screen resolution is 854 x 480**, per Genadi's figures. (Confirmed by Andrei Klimovich to Pavel Frolov)
- **The machine performance report moves out of MVP1 into MVP2** — competitor reports rest on detailed per-machine data pulled through SAS, which needs its own work. (Decided by Andrei Klimovich, agreed by Pavel Frolov)
- **The engineering / technician menu moves to MVP2** — the QR-code screen showing asset number, serial number and IP address. (Decided by Pavel Frolov and Andrei Klimovich)
- **The protocol will carry the asset number as well as the serial number** from the machine to the port. (Decided by Andrei Klimovich and Dzmitry Chudzinau)
- **Card search uses the last four digits of the barcode (card code)**, with a picture showing the cashier where to look, because the digits printed on the card front are a different number. (Decided by Andrei Klimovich after Pavel Frolov and Dzmitry Chudzinau raised it)
- **Support phone number and working hours live in server configuration**, not in the build. (Decided by Andrei Klimovich)
- **Support calls go through a virtual number with forwarding**, not a separate physical phone and SIM. (Proposed by Andrei Bosik, accepted by Andrei Klimovich)
- **No feature lock today** — Andrei's capabilities and requirements are not in Jira yet; possibly tomorrow. (Decided by Andrei Klimovich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Finish removing cloud references from the MVP1 capabilities and requirements | September 21, 2026 | High | He said about ten minutes after the call |
| 2 | Andrei Klimovich | Add the remaining design edits (text sizes, alignment) to the FlexPort and IQ screens | September 21, 2026 | High | Functional side already fixed |
| 3 | Andrei Klimovich | Load the whole UI/UX design into Jira as capabilities and requirements | September 21, 2026 | High | Features cannot be created until this is done |
| 4 | Andrei Klimovich | Post the mockup / design project link in the team chat | September 21, 2026 | High | Pavel asked for the link |
| 5 | Andrei Klimovich | Change the wallet-creation requirement so the cashier flow checks the printer first | TBD | High | Follows from the no-paper decision |
| 6 | Andrei Klimovich | Write the requirement for the location name and address fields on the home screen | TBD | Normal | Doing-business-as field plus city, maybe street |
| 7 | Andrei Klimovich | Add the picture showing the cashier where the barcode digits are on the card | TBD | Normal | Prevents confusion with the number on the card front |
| 8 | Andrei Klimovich | Ask the operators in contact with JVL which identifier they use for a machine | TBD | Normal | Asset number versus serial number |
| 9 | Andrei Klimovich | Record a note to add the technician information screen in MVP2 | TBD | Low | Machine number / asset / serial on FlexPort |
| 10 | Dzmitry Chudzinau | Extend the FlexPort–machine protocol to also pass the asset number | TBD | Normal | Agreed with Andrei |
| 11 | Irina Shishko | Give Andrei the non-functional requirements list she and Pavel produced for FlexPort | TBD | Normal | She already cleaned the list |
| 12 | Andrei Klimovich | Review that non-functional requirements list and comment | TBD | Normal | After Irina hands it over |

## Open Questions

- Does MVP1 support multiple card products? Dzmitry Chudzinau asked; Andrei Klimovich said it was not settled and had to be decided that day. The implementation will be built for multi-product, but if screens cannot be finished in time only one product will be supported per location — probably SkillPay, if it stays on the market.
- Is the asset number guaranteed to be different on every machine, or is it driven by the serial number? Pavel Frolov raised it and suggested asking Intralot or the locations; he thought Felipe might know.
- Which control library gives the date picker for the IQ search screens? Dzmitry Chudzinau thinks the standard React one, but it needs confirming with frontend.
- Should the machine identifier be shown on the FlexPort screen at all? Andrei Klimovich worried competitors visiting a location could use it. Parked with the engineering menu in MVP2.

## Dispatch Log

---
*Processed from Teams transcript on September 22, 2026 (recovery capture — this meeting fell in a gap between watcher runs)*
*Source meeting: Transactional MVP1: CAPs, REQs, UI/UX*
