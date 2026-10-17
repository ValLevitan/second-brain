# Meeting Summary — WiFi_update-October-15-2026
**Date:** October 15, 2026, 11:04 AM – 12:31 PM Eastern
**Duration:** ~87 minutes
**Attendees:** Val Levitan, Pavel Frolov, Andrei Bosik, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026]]

## Summary

Held in Russian.

**Wi-Fi at the location: router or Flex IQ as access point.** Earlier meetings chose a separate Wi-Fi router at each location. Val questioned this: a router costs money, needs install, permission, power cables and a good spot on the ceiling. Pavel: Flex IQ can act as the access point itself; its Wi-Fi chip is soldered on the ready-made Chinese RK board and is not industrial grade. Options: an external USB Wi-Fi module or a new interface board with its own module, plus an antenna. Val: the antenna can go inside the plastic cover that replaced the second screen. Andrei: Flex IQ in access-point mode needs router functions (DHCP, NAT, DNS) in the OS and the app (Pavel: DNS is not needed). Pavel: not hard; a spike of about one week. Pavel did not want to drop either option, so **Flex IQ gets a switch: own access point or external router.** The terminals still reach the cloud through their own LTE modem, not through the router; the router only gives local Wi-Fi.

**Power loss and battery.** Val: the system must recover on its own after a power cut, with zero downtime and no reconfiguration. He wants a small battery so a terminal can report "power lost" and, if power does not return in a few minutes, a service call is raised. Flex IQ already reports link-down events to the logs; power loss is not handled today. Agreed idea: a battery in the payment terminals (Flex IQ, Flex Pay, recycler, dispenser), with a BMS board the main processor can read (charge level). The battery must be easy to swap (about 3-year life), with diagnostics on when it was replaced. Portable units get a small custom pack; kiosks with a stand can take a standard 12 V UPS battery. Pavel: Genadi is needed for this hardware work.

**Disconnects and reporting.** Val: on any lost link, retry for a few seconds first, then alert; log every event with a timestamp; report devices that drop often so they can be replaced. Pavel: FlexPorts already show red "out of service" within about 2 seconds of losing the host and recover by themselves.

**Diagnostics go to the cloud.** Val: service and diagnostic data must be in the cloud, not on the local screen. Today events go to Grafana dashboards for staff only; customers do not see them. Access must be role-based (RBAC); Andrei: Sergey Tsimanov already built part of it and it went to prod two days ago. Pavel: MVP3 idea is SSH access to any terminal from the firmware-management tool.

**Installer setup by phone.** Pavel's plan: on the location page in the dashboard, generate a QR code; the installer scans it on each FlexPort. This binds the ports to that location's Flex IQ and sets the Wi-Fi name and password, so foreign ports cannot join. Val liked it: everyone who installs ports must be registered with JVL, then a test walk-through with the phone, then a record of the first setup with date and time. Pavel suggested calling it a "location map". Pavel: this fits best when Flex IQ is the access point; an external router needs a more skilled installer.

**Separate Wi-Fi unit (raised, not adopted).** Val asked about a JVL unit with its own Wi-Fi, LTE modem and battery, leaving the on-board chips as they are. Andrei: this raises the customer's cost; a Wi-Fi module in the existing terminal is much cheaper. Pavel: first test the current module; it may be good enough. Andrei would not plan a separate device now. Pavel: keep a router as a backup option for hard locations.

**MVP1 status.** Irina: end-to-end autotests on acceptance criteria for Flex IQ, FlexPort, machine and card issue finish tomorrow; bugs found so far are fixed. **The only gap is the USB-stick update for FlexPorts.** Evgeny Alekseev's branch for the new memory chips is not merged to main and its build is red; Lyosha tried to merge it from fresh main and failed (the branch is very old). Evgeny must merge main into his branch, fix conflicts, check that USB-stick update still works and stays active after an update, and make it build on GitHub Actions. Then prose and contracts are updated, and the capability is synced with requirements and tested by hand with a real stick. Val expects 3 to 5 days.

**MVP2 scope (Val's view).** No Flex Pay. Flex IQ, Wi-Fi configuration, remote update (FlexPorts and Flex IQ), diagnostics, and GALAXY transactional brought to reporting and dashboards. Plus the location's bank shortfall: if the location account has too little money, charge a credit card; the operator is the guarantor if that fails, backed by accounting reports. Pavel: the location can pay on its own dashboard page with a card (for example Stripe) and notify Nathan's module for the invoices; reports tie to MSBC. Val and Andrei [which Andrei — confirm] are still polishing the MVP2 list. Val wants each MVP to take 2 to 3 weeks, best 2, with testing running in parallel with development.

**Resources.** Dima Chudinov and Vladimir Samusenko are on vacation for at least 2 weeks. Lyosha must work on the RIS re-issue. Irina said she will be alone. Irina: requirements and capabilities must come first; Val: Andrei [which Andrei — confirm] writes only functional requirements, the rest must come from engineers. Andrei Bosik: most Wi-Fi requirements are already written and need review.

Val's outlook: demand will grow fast from January. Competitors' installs take 2 people about 3 hours on site plus travel.

## Decisions Made

- **Flex IQ gets a switch between its own access point and an external router. MVP2 starts with the switch and an external router; the router moves inside JVL hardware in MVP3 or later.** — Gives a working path now and a planned step later. Pavel also suggested building the own-access-point mode in parallel in MVP2; not confirmed. (Decided by Val, agreed by Pavel)
- **Payment terminals get a backup battery and power-loss alerts.** — So JVL knows power is gone and can call service if it does not return. Battery must be swappable with a BMS the processor reads. (Val, Andrei Bosik, Pavel)
- **Service and diagnostic data go to the cloud, with role-based access.** — Nobody will use a local screen. (Decided by Val)
- **Installer setup by phone with a QR code from the location dashboard**, binding FlexPorts to the location and setting Wi-Fi; installers are registered with JVL; the first setup is recorded with a timestamp ("location map"). (Proposed by Pavel, approved by Val)
- **MVP1 lacks only the FlexPort USB-stick update; remote update for FlexPorts moves to MVP2.** (Val, Pavel, Irina)
- **Flex Pay leaves MVP2 and is relabelled MVP3**, subject to the final MVP2 list from Val and Andrei. (Val's view; Pavel will retag)
- **Each MVP cycle is 2 to 3 weeks, best 2; testing runs in parallel with development.** (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Alekseev | Merge main into his FlexPort memory-chip branch, fix conflicts, check USB-stick update works and stays active, make it build on GitHub Actions | ~Oct 18–20 (3–5 days) | High | Blocks MVP1; not present — Pavel and Val to push |
| 2 | Pavel Frolov / Lyosha | Check Evgeny's ready-to-merge work tomorrow morning | Oct 16 | High | |
| 3 | Lyosha | Sync the FlexPort capability with requirements (USB-stick flashing still works after the chip change) and test by hand with a real stick | After #1 | High | Manual test; no emulation |
| 4 | Pavel Frolov | Update prose and contracts for Evgeny's code | After #1 | Normal | |
| 5 | Pavel Frolov / Irina Shishko | Tell Andrei [which Andrei — confirm] the MVP1 release date | Oct 16 | Normal | Val did not know what to answer |
| 6 | Pavel Frolov | Review MVP1/MVP2 items; move Flex Pay from MVP2 to MVP3 | Oct 16 | Normal | |
| 7 | Andrei Bosik | Spike: attach an antenna to the current Wi-Fi module, run it as access point with several FlexPorts and phones, measure range and signal | ~1 week | Normal | Pavel's estimate |
| 8 | Val Levitan + Andrei [which Andrei — confirm] | Finish the MVP2 scope; then Andrei starts work with the team | TBD | High | |
| 9 | Andrei Bosik | Review and update the existing Wi-Fi requirements for MVP2 [implied — confirm] | TBD | Normal | |
| 10 | [Unassigned — needs clarification] | Bring Genadi in on the battery and BMS hardware | TBD | Normal | Pavel: "we need Genadi" |

## Open Questions

- Own access point in Flex IQ versus external router in the long run — Pavel is not sure the built-in option is better.
- Val's separate JVL Wi-Fi unit (Wi-Fi, LTE modem, battery) — Andrei and Pavel prefer testing the on-board module first.
- How to set Wi-Fi name and password on a third-party router without a skilled installer (Pavel).
- What JVL does when a power-loss alert arrives (call the location?) — Andrei.
- Whether Wi-Fi is an option or always included (Andrei asked; Pavel: probably included).
- Whether customers should see diagnostic dashboards (Andrei).
- Fewer people for the next 2 weeks (vacations, Lyosha on RIS re-issue) — Pavel and Irina to plan tasks.

## Dispatch Log

---
*Processed from Teams transcript on October 15, 2026, 2:45 PM Eastern*
*Source meeting: WiFi_update-October-15-2026*
