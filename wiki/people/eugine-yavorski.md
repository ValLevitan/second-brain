---
type: person
title: Eugine Yavorski
date: 2025-02-18
aliases: [Eugine Yavorski, Evgeny Yavorsky, Yavorski, Yavorsky, Яворский, Evgeny, Yevgeny, Zhenya, Женя, Евгений]
source-count: 8
open-commitments: 1
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

## FlexPay TITO scope-gap (Mar 28)

- On the Mar-28 TITO meeting Yavorski (Евгений) was assigned the **WSS-protocol implementation** for the new TITO/SAS-server work: he agreed to read the WSS protocol over the weekend and report Monday on how long it would take, estimating **~two weeks**. He asked for a **test machine** to develop against; the plan is for Pavel to instruct the setup remotely and send him the IGT SAS-emulator utility (with "Ira" or "Vlad" helping find the RS-232 port). See [[wiki/decisions/2025-03-28-flexpay-support-tito-non-jvl-locations.md]] and [[wiki/meetings/2025-03-28-flexpay-tito-scope-gap.md]]. [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Open commitments

- [ ] Eugine Yavorski — read the FlexPay↔FlexPort **WSS protocol** over the weekend, report the effort estimate Monday, then implement the TITO extension — due Monday (report) — [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/Flex-port-update-March-17-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/scope_gap_tito_flex_pay-march-28-2025.md]]
