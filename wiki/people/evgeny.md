---
type: person
title: Evgeny
date: 2025-02-18
aliases: [Evgeny, Yevgeny, Zhenya, Женя, Евгений, Evgeny Yavorsky, Yavorsky, Яворский]
source-count: 4
---

# Evgeny

Evgeny (called "Zhenya" / "Женя") is a JVL field/deployment engineer who is bringing up the **FlexPay/FlexPort** payment integration on real machines ahead of placing them at the first locations. He is based in Ontario, Canada (the transcript places him "up north," dealing with snow around Barrie/Bradford). [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]] Role somewhat unclear — he could be a JVL field engineer or an operator running the first installs; flagged.

## Role

- On the Feb 18 embedded-group standup, Evgeny is the person running FlexPay on the machine at the first-location site; work stalled because he could not start FlexPay until [[wiki/people/dmitry-khandov.md|"Dima"]] delivered a new FlexPay build that ignores the card dispenser (see Owner Decisions — this embedded "Dima" is not attributed). He worked closely and near-continuously with the Minsk team last week, giving Pavel remote access to his machine. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- His encoding tests matched the samples he was sent; he had assembled the pieces individually and needed at least another week to integrate everything. He is targeting placing machines at the first locations, but Val pushed him to allow two weeks (~March 5) rather than one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Embedded group — cash-out edge case (Feb 25)

- On the Feb 25 standup Evgeny ("Женя") raised the **abandoned-cash-out** case: a player presses cash-out and walks away without scanning a ticket / entering a PIN. He had put 5-minute timeouts on the start/scan/PIN steps and asked what to do about a cash-out that removes credits but is never claimed. Val's ruling: cancel the ticket as **"not claimed,"** pull the credits, report to FlexPay, and restore the money on paper via FlexPay during audit if the player returns. He is also verifying he can read a FlexPay-issued ticket and credit it, but a sensor on his device wasn't working. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

## Embedded group — integration near-complete (Mar 4, Mar 11)

- **Mar 4:** Evgeny got the FlexPort↔FlexPay **data exchange working at a minimal level**, traced the earlier disconnect to needing to **ping with text messages**, can read a **barcode ticket**, and is adding a **watchdog** and **log file** plus **event-based** state reporting to FlexPay (all-clear / error / recovery / unclaimed-money). Still needs a validator to confirm credits land on the machine. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- **Mar 11:** He reported the integration **nearly feature-complete**, finishing **cash-out** (EGM→FlexPay), with the **firmware update** protocol still to do (~1 week; USB-stick update already works). He is merging his branch into the **main branch owned by [[wiki/people/evgeny-alekseev.md|Zhenya Alekseev]]** (commit ~175), and planned to bring FlexPorts to the **Toronto office** to test two machines on one bus before shipping. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

The Feb 18 transcript does not give Evgeny's last name. The Mar 11 transcript refers to the integration developer as **"Evgeny Yavorsky"** (Евгений Яворский) — recorded here as an inferred surname for this recurring engineer — and separately names **Zhenya Alekseev** as the main-branch owner (a distinct person, [[wiki/people/evgeny-alekseev.md]]). Both are colloquially "Женя," so the split is flagged (see Owner Decisions).

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-04.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
