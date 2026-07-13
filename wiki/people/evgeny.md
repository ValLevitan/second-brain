---
type: person
title: Evgeny
date: 2025-02-18
aliases: [Evgeny, Yevgeny, Zhenya, Женя, Евгений]
source-count: 2
---

# Evgeny

Evgeny (called "Zhenya" / "Женя") is a JVL field/deployment engineer who is bringing up the **FlexPay/FlexPort** payment integration on real machines ahead of placing them at the first locations. He is based in Ontario, Canada (the transcript places him "up north," dealing with snow around Barrie/Bradford). [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]] Role somewhat unclear — he could be a JVL field engineer or an operator running the first installs; flagged.

## Role

- On the Feb 18 embedded-group standup, Evgeny is the person running FlexPay on the machine at the first-location site; work stalled because he could not start FlexPay until [[wiki/people/dmitry-khandov.md|"Dima"]] delivered a new FlexPay build that ignores the card dispenser (see Owner Decisions — this embedded "Dima" is not attributed). He worked closely and near-continuously with the Minsk team last week, giving Pavel remote access to his machine. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- His encoding tests matched the samples he was sent; he had assembled the pieces individually and needed at least another week to integrate everything. He is targeting placing machines at the first locations, but Val pushed him to allow two weeks (~March 5) rather than one. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]

## Embedded group — cash-out edge case (Feb 25)

- On the Feb 25 standup Evgeny ("Женя") raised the **abandoned-cash-out** case: a player presses cash-out and walks away without scanning a ticket / entering a PIN. He had put 5-minute timeouts on the start/scan/PIN steps and asked what to do about a cash-out that removes credits but is never claimed. Val's ruling: cancel the ticket as **"not claimed,"** pull the credits, report to FlexPay, and restore the money on paper via FlexPay during audit if the player returns. He is also verifying he can read a FlexPay-issued ticket and credit it, but a sensor on his device wasn't working. See [[wiki/meetings/2025-02-25-embedded-group-flexport-flexpay.md]] and [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]

The transcript does not give Evgeny's last name.

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-02-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-02-25.md]]
