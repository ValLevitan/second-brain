---
type: person
title: Eugine Yavorski
date: 2025-02-18
aliases: [Eugine Yavorski, Evgeny Yavorsky, Yavorski, Yavorsky, Яворский, Evgeny Egorsky, Egorsky, Егорский, Evgeny, Yevgeny, Zhenya, Женя, Евгений]
disambiguation: "One of TWO Zhenyas (owner-ruled), both contractors via EAleks Technology: Eugine Yavorski (wiki/people/eugine-yavorski.md) and Evgeniy Alekseev (wiki/people/evgeniy-alekseev.md). Resolve by context; queue if unclear."
source-count: 17
open-commitments: 2
---

# Eugine Yavorski

Eugine Yavorski (surname confirmed by Val; called "Zhenya" / "Женя" in the transcripts) is a JVL field/deployment engineer who is bringing up the **FlexPay/FlexPort** payment integration on real machines ahead of placing them at the first locations. He is based in Ontario, Canada (the transcript places him "up north," dealing with snow around Barrie/Bradford). [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]] Role somewhat unclear — he could be a JVL field engineer or an operator running the first installs; flagged.

## Role

- On the Feb 18 embedded-group standup, Evgeny is the person running FlexPay on the machine at the first-location site; work stalled because he could not start FlexPay until "Dima" delivered a new FlexPay build that ignores the card dispenser (this embedded build-delivery "Dima" is a developer — not the 3D designer, and not clearly the IT Dima; left UNRESOLVED per the owner ruling). He worked closely and near-continuously with the Minsk team last week, giving Pavel remote access to his machine. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- His encoding tests matched the samples he was sent; he had assembled the pieces individually and needed at least another week to integrate everything. He is targeting placing machines at the first locations, but Val pushed him to allow two weeks (~March 5) rather than one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Embedded group — cash-out edge case (Feb 25)

- On the Feb 25 standup Evgeny ("Женя") raised the **abandoned-cash-out** case: a player presses cash-out and walks away without scanning a ticket / entering a PIN. He had put 5-minute timeouts on the start/scan/PIN steps and asked what to do about a cash-out that removes credits but is never claimed. Val's ruling: cancel the ticket as **"not claimed,"** pull the credits, report to FlexPay, and restore the money on paper via FlexPay during audit if the player returns. He is also verifying he can read a FlexPay-issued ticket and credit it, but a sensor on his device wasn't working. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## Embedded group — integration near-complete (Mar 4, Mar 11)

- **Mar 4:** Evgeny got the FlexPort↔FlexPay **data exchange working at a minimal level**, traced the earlier disconnect to needing to **ping with text messages**, can read a **barcode ticket**, and is adding a **watchdog** and **log file** plus **event-based** state reporting to FlexPay (all-clear / error / recovery / unclaimed-money). Still needs a validator to confirm credits land on the machine. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- **Mar 11:** He reported the integration **nearly feature-complete**, finishing **cash-out** (EGM→FlexPay), with the **firmware update** protocol still to do (~1 week; USB-stick update already works). He is merging his branch into the **main branch owned by [[wiki/people/evgeniy-alekseev.md|Zhenya Alekseev]]** (commit ~175), and planned to bring FlexPorts to the **Toronto office** to test two machines on one bus before shipping. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

Name confirmed by Val as **Eugine Yavorski** (the Mar 11 transcript renders it "Evgeny Yavorsky" / Евгений Яворский). He is a **distinct person** from **[[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]**, the main-branch owner — both are colloquially "Женя"/"Zhenya," and the owner has confirmed they are two different people.

## Embedded standup (Mar 17)

- On the Mar 17 standup (reporting as "Евгений"/Zhenya), Yavorski reported one game machine passing almost all functionality **except cash-out**, with **FlexPay working** at both stations and a new printer printing tickets. He needs to cooperate with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] on the cash-out work, and flagged that the money-transfer protocol currently runs in **one phase** but must be reworked to the **two-phase** request/confirm (reject/commit) model — he is to verify whether funds are debited at phase one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Flex-port-update-March-17-2025.md]] [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]

## Embedded standup (Mar 25)

- Now working **full-time** for JVL (Val: "Женя сейчас фулл-тайм работает"), which Val treats as removing the timezone excuse — he wants Yavorski to pair with the back-end "Dima" ([[wiki/people/dmitri-chudinov.md|Chudinov]]) on FlexPort **daily** (Yavorski can work 7–10am while Dima is available). The remaining FlexPort issue: **cash-out succeeds only once** per ticket (credits leave the gaming machine but don't get credited back to the ticket on repeat). Yavorski is to reproduce it right after the meeting and hand fresh logs to Dima. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]

## Named for the SAS mini-server (Mar 27)

- On the English scope-gap meeting Val named the staffing for the "make-do" local primitive SAS mini-server: "**Evgeniy Alexeev plus Evgeniy Yavorsky. Nobody else.**" See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## FlexPay TITO scope-gap (Mar 28)

- On the Mar-28 TITO meeting Yavorski (Евгений) was assigned the **WSS-protocol implementation** for the new TITO/SAS-server work: he agreed to read the WSS protocol over the weekend and report Monday on how long it would take, estimating **~two weeks**. He asked for a **test machine** to develop against; the plan is for Pavel to instruct the setup remotely and send him the IGT SAS-emulator utility (with "Ira" or "Vlad" helping find the RS-232 port). See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]] and [[wiki/meetings/2025-03-28-flexpay-tito-scope-gap.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## SAS/TITO kickoff week (Apr 1)

- On the Apr 1 standup ([[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]) his plate: test **multiple devices simultaneously on the FlexPay bus** in the office ("у нас пока на шине было только один девайс"), then implement **log/system-state transfer to FlexPay on a button press**. A planned office session had slipped (the office was closed the day before); he arranged to go the same day (Gennady in the office) and asked to be shown how to do a **cash-out** on the gaming machine. His SAS/TITO test bed is an **ECHO countertop machine** that must run in **production (not demo) mode** ("иначе не будет работать"); he needs a **printer and a replacement bill validator** from Gennady (his stopped working) and identified the machine's **DB9** connector as the SAS port. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Embedded weeklies (Apr 15, Apr 22)

- **Apr 15:** on the SMIB/SAS weekly ([[wiki/meetings/2025-04-15-embedded-group-smib-sas-printer.md]]) Yavorski ("Яворский") reported finishing the **Georgia/Florida program build (version 0.15, `update.bin`)** and clarified the flashing sequence (bootloader once for production, after which the flash-drive update stops working); firmware-update-via-FlexPay targeted for end of April. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- **Apr 22:** on the follow-up standup ([[wiki/meetings/2025-04-22-flexport-tito-machine-setup-debug.md]]) Yavorski (rendered "**Егорский**" this time — already established on this page as him) had joined the **PWS/WebSocket** exchange project, was porting settings from the with-screen project to run the FlexPay exchange, and had the **firmware update ~40% done** (paused to prioritise the SAS work, which "must родить something by end of April"). His test machine is a small **red countertop** with no printer (so not TITO-enabled) — he must connect a printer, Factory-Reset, scan the passport and apply an RIS file to enable TITO; Alexei Khamin/Vlad to walk him through it. [[raw/flex_port_update-apr-22-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — read the FlexPay↔FlexPort **WSS protocol** over the weekend, report the effort estimate Monday, then implement the TITO extension — due Monday (report) — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [ ] Eugine Yavorski — run the multi-device FlexPay bus test in the office and implement the log/state transfer-to-FlexPay command — due week of Apr 1 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Apr 16 2025 — dispensing tower is the next embedded stage

On the Genadi hardware call Val named the **Flex self-dispensing tower** (on the FlexPort base) as the next stage of work for "Евгений Алексеев и Евгений Егорский" (Yavorski) after the TITO-architecture pieces. [[raw/fkex_pay_evolution-apr-16-2025.md]] See [[wiki/decisions/2025-04-16-dispensing-tower-first-magnetic-stripe.md]].

## May 7 2025 — WSS side done; day-by-day TITO milestones

On the FlexPort hardware call ([[wiki/meetings/2025-05-07-flexport-two-machines-tito-milestones.md]]) Yavorski reported the **WSS protocol finished** and that he must now integrate with [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s SAS→WSS part; Val pushed him to break the remaining TITO work into **daily testable milestones** (register FlexPort→FlexPay that day; coupon-out by Thu/Fri). See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_port_hardware_update-may-7-2025.md]]

## May 8 2025 — TITO MoneyOut bring-up

On the [[wiki/meetings/2025-05-08-flexport-flexpay-tito-standup.md|May-8 standup]] Yavorski reported connecting the full FlexPort↔FlexPay↔machine hardware chain: **WSS works on version 145** but needs the update to **154** for the latest TITO commands (Sergei Novitsky to update FlexPay); he ran [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s SAS ticket-out commands, **printed and read back a ticket**, and planned today's **MoneyOut** (using a software stub first) and Friday's **MoneyIn**, before two-machine testing and handing to QA Monday. He is building a home version **155** (no dispenser). Flagged an unblockable **SAS code-51** message loop after a failed print. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex_pay_hardware_update-may-8-2025.md]] [[raw/flex_pay_port_hardware_update-may-8-2025.md]]

## May 10 2025 — weekend debug update

On a short Saturday update ([[wiki/meetings/2025-05-10-flexport-flexpay-debug-update.md]]) Yavorski reported the menu-cancel path not yet working — spoofed commands return **"ticket null, code 0"** while init/registration pass; he estimates **~90% his own side** and will inspect closely before escalating to [[wiki/people/dmitri-chudinov.md|Dima]] (Chudinov). He planned to work the office over the weekend (taking the key from [[wiki/people/evgeniy-alekseev.md|Alekseev]]), with Val telling him to email [[wiki/people/arkady-batson.md|Arkady]]/[[wiki/people/genadi-peari.md|Genadi]] to protect his workshop machines. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_flex-pay_update-may-10-2025.md]]

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/Flex-port-update-March-17-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/flex_port_update-apr-22-2025.md]]
- [[raw/flex_port_hardware_update-may-7-2025.md]]
- [[raw/flex_pay_hardware_update-may-8-2025.md]]
- [[raw/flex_pay_port_hardware_update-may-8-2025.md]]
- [[raw/flex-port_flex-pay_update-may-10-2025.md]]
