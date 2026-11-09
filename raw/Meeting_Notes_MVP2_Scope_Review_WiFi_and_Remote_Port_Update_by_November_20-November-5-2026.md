# Meeting Summary — MVP2 - Scope review
**Date:** November 5, 2026, 8:01 AM – 8:55 AM Eastern
**Duration:** ~54 minutes
**Attendees:** Val Levitan, Andrei Klimovich (organizer), Pavel Frolov, Irina Shishko, Dzmitry Chudzinau, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_MVP2_Scope_Review_WiFi_and_Remote_Port_Update_by_November_20-November-5-2026]]

## Summary

**Pyramid bill acceptor test.** Pavel created the capability and assigned it to Alexey, but thinks it is faster to set up an Echo cabinet in Georgia and connect it remotely to our network. Val agreed: do it remotely and use as few subcontractor hands as possible; someone can insert a bill or ticket once a week.

**MVP1 release.** A new capability and requirements were added yesterday for delivering builds through the interface (Flex-Port build download); Sergey is working on it. Andrei is ready to release once it lands, early next week. There are no metal brackets yet; plastic ones for one location (4 machines) are printed and Andrei picks them up today. Val: plan Monday internally, tell the client Wednesday, so the client is never waiting on us. A release means the production services deployed, the Flex-IQ and Flex-Port firmware visible on the production server UI (AWS), and the Jira release done through the GitHub procedure.

**Purpose of design.** Val asked that every release scope carry a short plain-language statement of what the client gets and why (example: every machine has a modem; turning it off must be intentional), so engineers understand the intent. Andrei will add it as a custom "Purpose of design" field that lives across the release.

**MVP2 must be narrow and fast.** Andrei's draft put monitoring and data collection at the centre. Val cooled that: the gap between MVP1 and MVP2 must be short; Wi-Fi setup comes first because it is a huge installation cost; then remote updates, robust installation and diagnostics during install. Everything else goes to MVP3. Pavel: Wi-Fi removes the engineer pulling cables to a router; remote Flex-Port firmware update through the modem removes the USB stick. Andrei agreed these two are the backbone of MVP2. Val reminded that only 5 locations are being installed, Christmas is a dead zone, the team is tired and he promised not to disturb them from mid-December.

**Dates.** Val: MVP2 in two weeks. Jira already holds November 20 (Friday) as the preliminary date; Val expects around November 23 with normal delay, and MVP3 around January 20. At the end Val said November 20 cannot be missed.

**Wi-Fi.** Flex-IQ works both as the access point (preferred, no router at the location) and as a client of an external access point for large locations. New Flex-IQ units need Wi-Fi antennas ordered and a mounting place designed; Val: email Genadi Peari and assign the task; Andrei will, with Val in copy.

**Scope rulings.**
- Location block when money cannot be collected: Val — the existing manual block command is enough for MVP2; automatic block logic and the credit-card flow go to MVP3.
- Cloud backup as an intermediate step (snapshot of IQ wallets and transactions to restore on a replacement IQ): Dzmitry — same work as full cloud wallets, not doable in two weeks with testing; dropped. Full cloud wallet and transaction storage in MVP3.
- SIM-card binding and traffic balance: MVP2 (Pavel).
- Credit-card payment of location invoices as a secondary method: MVP3; Dwolla does not store cards, Sergey Tsimanov spiked Stripe, and Dwolla was sold to a larger player that has card payments.
- SAS link for bill validator and counters: MVP3.
- Split redemption: MVP2 adds a lottery-ticket category with its own operation type for reporting; custom per-location categories in MVP3.
- Basic money-in and money-out reports in the Payment Hub web: MVP2 (Val: "100%"). Inspector report stays in MVP2 on the Flex-IQ. Invoice collection cycle: MVP3.
- Smaller ticket barcode: Andrei cut the scanning height from 6 cm to 3 cm so it fits inside the Flex-Port height (needed for low mounts such as Light & Wonder cabinets); stays in MVP2, Andrei describes it in detail.
- Forfeited wallets (stuck money the cashier reloads): MVP3; watch real cases first. Cashier corrections move with it.
- Master vs location-owner roles in Payment Hub onboarding: MVP1 onboards location owners only; Andrei wants the role split done early in MVP2.
- Monitoring and notifications: Andrei decides what piece fits by November 20.

**MVP3 outlook.** Flex Pay Slim kiosk; locations with several gateways, IQs and a kiosk sharing tickets and wallets through the cloud. Pavel: syncing Wi-Fi access points across gateways has no good design yet. Andrei Bosik asked for an audit journal of server user actions (AAA); Dzmitry: much is already logged to Grafana, writing key events to the database is a business-process question; parked until the first installs run. Andrei Klimovich: every release gets its own audit capability describing what is logged and shown.

**Next steps.** Andrei cleans up MVP2 in Jira, reports, then writes the capabilities and requirements by Monday. Meeting Monday 8 AM Eastern on the MVP1 release and the MVP2 capabilities; invite Dzmitry, Sergey Tsimanov, Alexander Biratko, Irina and Pavel; Val will be on the road. Val wants every person to leave that meeting with a clear MVP2 definition and a resource plan.

## Decisions Made

- **Pyramid bill acceptor is tested remotely on an Echo cabinet in Georgia, with minimal subcontractor hands** — (Pavel, Val)
- **MVP1 release targeted internally for Monday November 9; the client is told Wednesday** — (Val)
- **MVP2 core is Wi-Fi (IQ as access point and as client), remote Flex-Port firmware update, robust installation and install diagnostics; scope kept narrow** — (Val, Andrei K, Pavel)
- **MVP2 release date November 20 (about November 23 with slack); MVP3 about January 20** — (Val)
- **Location block: manual command is enough for MVP2; automatic block and credit-card flow in MVP3** — (Val)
- **Cloud backup intermediate step dropped; full cloud wallet storage in MVP3** — (Dzmitry, Andrei K)
- **Moved to MVP3: SAS/bill validator link, credit-card invoice payment, invoice collection cycle, forfeited-wallet cashier action, cashier corrections** — (Andrei K, team)
- **Stays in MVP2: SIM binding and traffic balance, money-in/out reports in Payment Hub, inspector report on IQ, lottery-ticket split category, smaller barcode, master/location-owner role split, a piece of monitoring** — (Andrei K, Val, Pavel)
- **Every release scope gets a "Purpose of design" statement and its own audit capability** — (Andrei K, after Val's request)
- **Follow-up meeting Monday November 9, 8 AM Eastern on MVP1 release and MVP2 capabilities** — (Andrei K, all)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Clean up and update the MVP2 scope in Jira, then report | Nov 6, 2026 | High | Before writing capabilities |
| 2 | Andrei Klimovich | Write the MVP2 capabilities and requirements | Nov 9, 2026 | High | Reviewed Monday 8 AM ET |
| 3 | Andrei Klimovich | Write the "Purpose of design" statement for MVP2 as a custom field | Nov 9, 2026 | Normal | Val's request |
| 4 | Andrei Klimovich | Email Genadi Peari to order Wi-Fi antennas for new Flex-IQ units and design their mounting; assign the task, Val in copy | TBD | High | Val's instruction |
| 5 | Andrei Klimovich | Send the Monday 8 AM ET meeting invite (Dzmitry, Sergey, Alexander Biratko, Irina, Pavel, Val) | Nov 6, 2026 | Normal | |
| 6 | Andrei Klimovich | Describe the smaller-barcode requirement in detail | TBD | Normal | 3 cm scan height |
| 7 | Andrei Klimovich | Rewrite the location-block requirement as manual block only | TBD | Normal | Auto-block to MVP3 |
| 8 | Andrei Klimovich | Pick up the plastic brackets from printing | Nov 5, 2026 | Normal | One location, 4 machines |
| 9 | Sergey Tsimanov | Finish the Flex-Port build download capability | Early week of Nov 9 | High | Blocks the MVP1 release |
| 10 | Pavel Frolov | Set up an Echo cabinet in Georgia for remote Pyramid testing | TBD | Normal | Alexey assigned the capability |

## Open Questions

- How to configure Wi-Fi access points when one location has several gateways? (Pavel) — MVP3, no design yet.
- Which server user actions go into an audit journal in the database, not only Grafana? (Andrei Bosik, Dzmitry) — revisit after first installs.
- Which piece of monitoring and notifications fits by November 20? (Andrei K)

## Dispatch Log

---
*Processed from Teams transcript on November 5, 2026, 10:10 AM Eastern*
*Source meeting: MVP2 - Scope review*
