---
type: person
title: Evgeniy Alekseev
date: 2025-03-11
aliases: [Evgeniy Alekseev, Evgeny Alekseev, Zhenya Alekseev, Женя Алексеев, Alekseev]
disambiguation: "One of TWO Zhenyas (owner-ruled), both contractors via EAleks Technology: Eugine Yavorski (wiki/people/eugine-yavorski.md) and Evgeniy Alekseev (wiki/people/evgeniy-alekseev.md). Resolve by context; queue if unclear."
source-count: 9
open-commitments: 1
---

# Evgeniy Alekseev

Evgeniy Alekseev (name confirmed by Val; "Zhenya Alekseev" / "Женя Алексеев" in the transcript) is a JVL developer who owns the **main code branch** of the FlexPort↔FlexPay embedded software. On the March 11 2025 embedded standup, the integration engineer ([[wiki/people/eugine-yavorski.md|Eugine Yavorski]]) said the main branch is "with Zhenya Alekseev" and that he would merge his own branch into Alekseev's to create the common project. [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]

**Owner-confirmed (2026-07-13):** Evgeniy Alekseev and [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] are **two different people**, both colloquially "Женя"/"Zhenya." Past "Zhenya"/"Женя" facts on Yavorski's page belong to the integration engineer; this page is only the main-branch owner.

On the Mar 17 standup, [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] again said he needs to **cooperate with "Женя Алексеев"** to finish the **cash-out** work — reinforcing that Alekseev owns the code the integration must land in. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/Flex-port-update-March-17-2025.md]] [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]

On the Mar 25 standup, Alekseev is again the one who **can see behaviour the others cannot** on the FlexPay/machine side (Val: "то, чего мы сейчас не видим, а Евгений Алексеев видит"), so the cash-out debugging depends on him and Yavorski working together. (The transcript also renders a "Женя Львовский"/Zhenya Lvovsky, likely a mis-transcription of Yavorski — flagged, see Owner Decisions.) [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]

On the Mar 27 2025 scope-gap meeting, Val named the pair for the "make-do" local primitive SAS mini-server: "**Evgeniy Alexeev plus Evgeniy Yavorsky. Nobody else.**" — over Pavel's objection that they don't know the FlexPay operating system. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]

## The SAS implementation (Apr 1)

On the Apr 1 standup ([[wiki/meetings/2025-04-01-flexport-flexpay-dev-update.md]]) Alekseev took the **low-level SAS communication** build for the TITO/SMIB work — "создание проекта и написание исходного кода" plus hardware prep (machine, printer, validator, cable). He had studied the SAS protocol from "эти документы, которые Дмитрий приготовил" and sized it at "недели три займет" (~3 weeks; "Я-то затягивать не буду. Будет быстрее, иначе будет быстрее" when pushed); hardware needed only from the following week ("Эту неделю просто буду писать код"). Technical points he engaged: the **8-bit + 1 wakeup-bit** SAS serial quirk ("я там не вижу каких-то хитростей" — only when to send the bit was unclear), a constant address "1" per machine (one SAS-host connection each), the **IGT "SAS-тест" utility** as a test host, and that USB-to-RS232 adapters suffice. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Open commitments

- [ ] Evgeniy Alekseev — build the low-level SAS project (code this week, hardware assembled by next week), targeting ~3 weeks or faster — due ~late Apr 2025 — [[raw/flex-port_pay_dev_update-april-1-2025.md]]

## Apr 16 2025 — dispensing tower is the next embedded stage

On the Genadi hardware call, Val placed the **Flex self-dispensing tower** (on the FlexPort base) as the next stage of work for Alekseev and Yavorski, after the TITO-architecture pieces (SMIB, FlexPort, Local TITO Server). He deprioritized the legacy machines that don't support FlexPort (a protocol issue on Alekseev's side) — ~3,000 of ~35,000 machines, "не первый, не второй приоритет." [[raw/fkex_pay_evolution-apr-16-2025.md]] See [[wiki/decisions/2025-04-16-dispensing-tower-first-magnetic-stripe.md]].

## SMIB/SAS bring-up (Apr 15, Apr 22)

- **Apr 15:** on the SMIB weekly ([[wiki/meetings/2025-04-15-embedded-group-smib-sas-printer.md]]) Alekseev reported **getting the SMIB↔machine SAS exchange working** after connecting Pavel's **AGT emulator** on COM1 and tracing the packets — the key discovery that the machine won't respond until it receives an **"81" packet** (a SAS PING carrying the machine address). He is building the SMIB on the **existing FlexPort board** for now (to be cannibalised into a cheap dedicated board later), with a basic Minsk-debug variant promised for the following week. See [[wiki/topics/flexpay-mobile-app-and-service-advocates.md]]. [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- **Apr 22:** on the follow-up ([[wiki/meetings/2025-04-22-flexport-tito-machine-setup-debug.md]]) his coding was done but **debugging was blocked** — his test machine wouldn't run in TITO mode and a Factory Reset alone didn't enable it; the group worked out the printer-connect → Factory-Reset → passport-scan → RIS → Enable-SAS procedure, and he needs Yavorski to enable TITO on his machine too. [[raw/flex_port_update-apr-22-2025.md]]

## Sources

- [[raw/Embedded_Group_alignment_and_update_2025-03-11.md]]
- [[raw/Flex-port-update-March-17-2025.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-18.md]]
- [[raw/Embedded_Group_alignment_and_update_2025-03-25.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/flex-port_pay_dev_update-april-1-2025.md]]
- [[raw/fkex_pay_evolution-apr-16-2025.md]]
- [[raw/weekly_embedded_group_flex_port_progress-apr-15-2025.md]]
- [[raw/flex_port_update-apr-22-2025.md]]
