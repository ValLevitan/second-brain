# Meeting Summary — Transactional MVP1: CAPs, REQs, UI/UX

**Date:** September 17, 2026, 8:02 AM - 9:31 AM Eastern
**Duration:** approximately 1 hour 29 minutes
**Attendees heard:** Andrei Klimovich (organiser), Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Andrei Bosik
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026]]
**Source meeting:** Following: Transactional MVP1: CAPs, REQs, UI/UX — Microsoft Teams

## Summary

The daily MVP1 call. Val was invited but did not speak on this one. Two subjects filled the call: InComm's new SkillPay card, which forces a decision about supporting more than one card product, and Andrei Bosik's network and security list, which had to be split between MVP1 and MVP2.

**InComm launched SkillPay.** Klimovich gave the context: InComm officially put the SkillPay card on the market yesterday. It loads like PricePay and can be used for shopping and online, but unlike PricePay it can be put into any certified ATM and turned into cash. That is a large change in the market. Regulators have not reacted yet. Klimovich's reading is that players will strongly prefer SkillPay over PricePay, so JVL has to be able to issue it.

The two products are genuinely separate inside InComm, with their own settings. What is known already: activation fee is **$2 for PricePay and $3 for SkillPay**. Load min/max are the same today, $5 and $1,000, but there is no promise they stay the same. Daily cap and velocity may also differ.

**Decision: support multiple products, not two hard-coded ones.** Chudzinau proposed the shape and it was accepted. Today the location record holds a single UPC field; instead it becomes a collection of products. The cashier adds a product, names it, enters the UPC InComm gives, and sets that product's own limits and fees. The card's barcode already carries the UPC plus the card number, so the terminal knows which product it is scanning and can pull the correct fee from the server without the cashier saying anything. The location manager checks the scanned UPC against the products the location supports and declines with "product not available" if it is not enabled. Klimovich's closing words: for MVP1 we support **multi-product** from InComm, done at the payment-hub level. When a second payment provider appears later, another level will be added.

**The cashier UI flow was debated and deliberately parked.** The argument was about where the player picks the card. Pavel's position: do not add a button — after the amount screen, show the available products side by side with their fees and what each one can do, and the moment the cashier scans a card the flow continues on the right product. Chudzinau's position: the amount and the product have to be decided on the same screen, because the amount limits which product is possible, and bouncing back and forth between screens is bad service. His example — the player wants $1,500, one product caps at $1,000 and the other at $1,200; the screen should say straight away that this amount means two cards on one product and one card plus a leftover on the other. Bosik wanted the default to stay "maximum amount, best product pre-selected", comparing it to a fuel card that you just swipe. Klimovich agreed the current behaviour (pre-fill the redeemable balance, trimmed to the product's max cap, with a banner explaining the rest can be scanned again) becomes ambiguous with two different max caps. Fixed points everyone accepted: it is the player's money and the player always wants all of it; the screen should say immediately which cards can carry that amount. Klimovich parked the UI flow overnight and asked the team to come back to it tomorrow.

**InComm broker verification.** InComm needs screenshots and video of the full flow, per product, before it will verify JVL as a broker that issues its cards. They specifically want to see that the card is activated while it is still inside the sleeve — that the cashier does not open the sleeve or reach inside, and hands the player a fully sealed card. Klimovich confirmed the Moto Goose build sent two or three days ago has the player-confirmation step removed, so it now matches the real cashier-only flow, and he will record the screens from it today. He also opens a new email thread to InComm asking for SkillPay support, the documentation, and test cards.

**Andrei Bosik's network and security list (capability 144 and friends).** The devices look at the internet through their own LTE modem, with no router, no NAT and no firewall in front of them. So the operating system itself has to do the work a router normally does: firewall, NAT, and separate WAN and LAN profiles. Bosik's point that settled it: if the device answers pings from the internet, bots will ping it non-stop, and JVL pays per megabyte on those SIMs — the traffic bill alone justifies it. Klimovich's answer: **stays in MVP1**. Bosik will have Claude write it in Pavel's repository as a branch and a pull request, because he does not want to break the operating system; testing it was an open worry, with the idea floated of asking Claude to attack both versions, with and without the changes.

The rest of the list was split:

- **Signal quality / telemetry.** Bosik wants signal level shown both graphically (bars) and in decibels, because bars look perfect next to a jammer while the noise figures tell the truth. Flex IQ's admin settings already show decibels but not signal-to-noise. Agreement: for MVP1 what matters is that JVL can see it **remotely** — Chudzinau collects the metric periodically into the logs, sends automatically when there is internet, buffers to file and sends when the connection returns, the same way as all system and application logs. Grafana then carries a dashboard or alerts on top. Klimovich also wants the numbers on the operations portal; Bosik will own writing the requirement.
- **Capability 144 (remote FlexPort master: telemetry, firmware update, identification in the cloud)** had been moved into MVP1 by Pavel. After discussion it goes back out to MVP2. Irina's argument won: updating six FlexPorts from a USB stick is not a problem, JVL updates 3,000 machines from a stick. Klimovich noted the update is done by the machine owner's technicians, not by JVL, and accepted it for MVP1. Condition attached: logging in MVP1 must still be good enough to know a device is not working and that someone has to drive out with the stick.
- **Requirement 1410 (FlexPorts do not appear on the dashboard)** — Klimovich took it for the portal dashboard. Chudzinau noted the IQ terminal's setup screen (master mode, not cashier mode) will already list the FlexPorts on the network, and Sergei is finishing the function to re-attach a FlexPort. Stays in MVP1 under capability 144.
- **Requirement 1405 (route priority: LTE first, then LAN, then Wi-Fi)** — already works through the admin settings, where the connection can be prioritised by hand. Bosik asked why it is not automatic; Pavel's counter is that in some locations LTE does not work at all — a basement — and a hard-wired priority would leave nobody a way out. Agreed: make LTE the default, leave the manual override, revisit with Wi-Fi in MVP2.
- **Requirement 1418 (no device is a gateway for another)** — every device reaches the internet through its own modem. In MVP1 this is straightforward, there is a single gateway and it is the IQ. The DHCP-server and master question only arises with IQ plus one or more kiosks, so it moves to MVP2.
- **Requirements 1413, 1421, 1431, 1030** — orphans with no capability, or belonging to MVP2. Klimovich linked them to the MVP2 parking capability he created yesterday so nothing is lost. 1431 (PIN entry timeout) does not belong on Flex IQ at all — there are no PINs there — and has to be attached to FlexPay. 1030 is the watchdog requirement: Val's rule that every device must have a watchdog and reboot itself if it hangs. It is done on the gaming machines but the description is specific to FP10 and does not fit IQ, so the watchdog work for kiosks and IQ goes to MVP2.
- **Routers** must be models approved and sold in the United States; Bosik owns choosing one and will name it tomorrow so a couple can be bought from Amazon in time.
- **Capability 91** is already delivered; the fix version was missing, and Bosik set it during the call.

**Naming.** Bosik asked the team to stop saying "cloud" for the operations portal, because his Claude then misunderstands what is meant — anything but CRM. Agreed to call it the operations portal.

**Housekeeping.** Chudzinau closed all open questions on capability 122 and is still working on a few non-functional requirements for network behaviour; the logging and Grafana requirements are planned but not yet written. Irina and Pavel reworked the non-functional FlexPort requirements with Claude and will send Klimovich the list to review. Klimovich asked for every hardware-related text the cashier can see on the IQ screen so he can build the text collection; Chudzinau will supply the InComm error list and JVL's own messages ("no internet", "lease expired").

## Undertakings

| # | Who | What | Due | Priority | Context |
|---|-----|------|-----|----------|---------|
| 1 | Andrei Klimovich | Start a new email thread to InComm — JVL is ready to support SkillPay; ask for the documentation and test cards | Not set | High | Include Pavel, Chudzinau, Irina and Sergei |
| 2 | InComm request (via Klimovich) | Ask for **two** test cards of different products with different UPCs | Not set | High | Chudzinau's request, for the barcode work |
| 3 | Andrei Klimovich | Install the new Moto Goose build and record screenshots and video of the full activation flow for InComm's broker verification | Today | High | Player confirmation already removed from that build |
| 4 | Andrei Klimovich | Find a production SkillPay card with a barcode and swipe it on a Flex IQ so Chudzinau can read the logs and see what is on the magnetic stripe | Not set | High | His test card has no barcode |
| 5 | Andrei Klimovich | Write up the multi-product capability in Jira (product collection on the payment hub) | Not set | High | Decision taken on this call |
| 6 | Andrei Klimovich | Rethink the cashier UI flow for choosing the product and bring it back tomorrow | Tomorrow's call | High | Deliberately parked overnight |
| 7 | Andrei Klimovich | Link orphan requirements 1431, 1030, 1413, 1421 to the MVP2 parking capability; attach 1431 to FlexPay | Not set | Normal | So nothing is lost |
| 8 | Andrei Klimovich | Take requirement 1410 into the portal dashboard work (show FlexPorts and their serial numbers) | Not set | Normal | Stays in MVP1 |
| 9 | Andrei Klimovich | Collect the hardware-related on-screen texts for the IQ text collection | Not set | Normal | Printer tilts from Irina; error list from Chudzinau |
| 10 | Dzmitry Chudzinau | Send the InComm error list and JVL's own screen messages into the meeting chat | Not set | Normal | Agreed on the call |
| 11 | Dzmitry Chudzinau | Finish the logging work and write the Grafana / metrics requirements, including periodic signal metrics with offline buffering | Not set | High | Nothing written yet |
| 12 | Andrei Bosik | Contact KORE (the SIM provider) once Klimovich adds him to the communication chain; look at their site and API for anything useful | Not set | Normal | Possible direct channel to devices for debugging |
| 13 | Andrei Bosik | Own the requirement for remote visibility of signal quality (decibels, signal-to-noise) and add it if it does not exist | Not set | Normal | He raised it |
| 14 | Andrei Bosik | Choose the router model — approved and sold in the United States — and name it tomorrow | Tomorrow | High | So a couple can be ordered from Amazon in time |
| 15 | Andrei Bosik | Get the firewall / NAT / WAN-LAN profile work written via Claude as a branch and pull request in Pavel's repository | Not set | High | Confirmed as MVP1 |
| 16 | Andrei Bosik | Thin out capability 144 — remove the requirements that moved to MVP2 | Not set | Normal | Done partly during the call |
| 17 | Irina Shishko / Pavel Frolov | Finish reworking the non-functional FlexPort requirements and send the list to Klimovich to review | Not set | Normal | Reworked with Claude |
| 18 | Pavel Frolov | Find or create the capability covering logging to the cloud server — nothing was found in Jira | Not set | Normal | "Will have to ask Claude" |
| 19 | Sergei (via Pavel) | Take the SkillPay test-card task in parallel | Not set | Normal | Pavel's assignment |

## Decisions

- **JVL supports multiple InComm card products, not a fixed pair.** Implemented at the payment-hub level as a collection of products per location, each with its own UPC, fees and limits.
- The card's barcode carries the UPC, so the terminal identifies the product on scan and pulls the correct fee from the server. A UPC the location does not support is declined with "product not available".
- **PricePay $2 / SkillPay $3** activation fee. Load min/max are $5 / $1,000 for both today, but must be configurable per product.
- The cashier UI flow for choosing the product is **not decided** — parked overnight, back on tomorrow's call.
- **Capability 144 (remote FlexPort telemetry and firmware update) moves to MVP2.** Updating six FlexPorts from a USB stick is acceptable for MVP1; JVL updates 3,000 machines that way, and the owner's technicians do it.
- MVP1 logging must still be good enough to tell that a device is down and a technician has to drive out.
- **Firewall, NAT and WAN/LAN profiles on the device stay in MVP1.** Without them the devices answer pings from the open internet and JVL pays for the traffic.
- Signal quality for MVP1 means **remote** visibility — periodic metrics collected into the logs, buffered offline, sent when the connection returns, surfaced through Grafana.
- **LTE is the default route**, with manual priority kept in admin settings; Wi-Fi handling waits for MVP2.
- No JVL device is a gateway for another; each has its own modem. The DHCP/master question only arises with IQ plus kiosks, so it is MVP2.
- Watchdog on kiosks and IQ is MVP2; it exists on the gaming machines but the requirement is written for FP10.
- Capability 91 is delivered; fix version set during the call.
- The team calls it the **operations portal**, not "cloud" and not CRM.

## Open Questions

- **Where the cashier picks the card product** — Pavel wants the product screen after the amount with no extra button; Chudzinau wants amount and product on one screen because the amount decides which products are possible. Unresolved, back tomorrow.
- **What the amount field pre-fills** when two products have different max caps — the higher cap (which silently rules one product out), the lower one, or nothing at all.
- **Whether SkillPay uses the same InComm IP/endpoint** as PricePay, or a different one.
- **Whether the SkillPay card carries the UPC on its magnetic stripe** — needs a production card swiped and the logs read.
- **How the firewall changes get tested** without breaking the operating system. Ideas floated: have Claude attack it, and compare a build with and without the changes.
- **Regulator reaction to SkillPay.** It cashes out at any ATM; nobody knows yet how regulators respond, and Klimovich flagged the risk that the product is closed a week after JVL builds for it.
