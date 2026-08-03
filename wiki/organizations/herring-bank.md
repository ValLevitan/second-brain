---
type: organization
title: Herring Bank
date: 2026-07-10
aliases: [Herring Bank, Herring]
source-count: 3
---

# Herring Bank

Herring Bank is a US bank JVL began exploring in July 2026 as a partner for its **Georgia gaming** business, on two fronts: (1) as a **cash-management partner** running the **armored-car / cash-in-transit (CIT)** service that picks up and deposits the cash accumulating in JVL's slim-recycler drop cassettes; and (2) as the **network-sponsor bank** that authorizes card-initiated cash dispensing on JVL's transactional machines and supports InComm's **Prize Play card**. Herring describes itself as **"a fintech masquerading as a 127-year-old financial institution"** — a third-generation, family-run bank with many shareholders, whose approach is to architect its own solutions and integrate technically with its customers. The relationship started with a first, exploratory call on 10 July 2026 introduced by John Houseal of [[wiki/organizations/incom.md|InComm]]. [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]] [[raw/Meeting_Notes_Herring_Bank_Prize_Play_Card-July-31-2026.md]]

## Contact

- **Maya Fuentes** — Herring Bank; JVL's payments contact and, per the Jul-31 call, **Val's business liaison**. Also described as an ATM Association of the US board member; 25+ years in the payments space, based in Morristown, New Jersey. Email **Mfuentes@herringbank.com**. External rep — no separate person page. [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]] [[raw/Meeting_Notes_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Campbell** — a **principal of Herring Bank** (his great-great-grandfather's name is on the building). Joined the Jul-31 call as the decision-maker Maya brought in. External rep — no separate person page. [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Ricky Rodriguez** — runs Herring Bank's **product side**; will lead the integration/testing with JVL. The working group is Val, Maya and Ricky. External rep — no separate person page. [[raw/Meeting_Notes_Herring_Bank_Prize_Play_Card-July-31-2026.md]]

## Jul 10 2026 — first cash-management exploration call

On the [[wiki/meetings/2026-07-10-herring-bank-cash-management-partnership.md|Jul-10 call]] Val walked Maya through JVL's background and the slim-recycler use case, then reached the banking question. Full Georgia-rollout context on [[wiki/projects/georgia-market-rollout.md]] (Jul-10). [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]]

- **What Herring offers JVL.** Herring would manage the **armored-car / cash-in-transit (CIT)** back end for periodic pickups of the cash in the recyclers' locked **drop cassettes**, depositing it into **JVL's account at Herring Bank**. Val had flagged it would be hard for JVL to deposit cash into banks itself — this is the gap Herring fills. [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]]
- **Where the cash routes.** When Val asked about using other banks, Maya said the cash would move from the armored car, through CIT, to the **Fed**. (The recording ends here.) [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]]
- **Next step (per Val's post-call note).** Maya recommended a call between Val and **Herring Bank's owner**; Val is following up to arrange it and to get details on Herring's cash-management/CIT service (coverage, account setup, pricing). This was an introductory, exploratory call — no formal decisions. §15.8: banking/cash-management terms are company economics — recorded; no named-person compensation appears. [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]]

## Jul 31 2026 — second call: network sponsorship, the Prize Play card, and a single-agreement structure

On the [[wiki/meetings/2026-07-31-herring-bank-prize-play-card.md|Jul-31 introductory call]] Maya brought in **Campbell** (a bank principal) to talk through network-sponsoring JVL's ATM-style cash-dispensing machines and supporting InComm's Prize Play card. Val gave his background — JVL manufactures slot machines sold in **Georgia, Nebraska and South Dakota**, and in Georgia is introducing transactional products, one with **ATM-style cash-dispensing** functions — and asked whether such a machine must be registered with an ATM network. [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]

- **What triggers network sponsorship.** Campbell: if a **network card initiates a cash dispense**, it is the **card activity** that requires network sponsorship. The flow is: the card triggers the transaction → **Herring approves/clears it** → the machine executes the dispense → a **settlement process** follows. As a **principal network member bank** with its own APIs, Herring can hold balances, transmit money, and dispense or receive cash — "you say a transaction is legal, we agree it's legal and we support it." JVL writes its own software and offers the hardware/peripheral devices; Herring does not make software and is happy to integrate to JVL's API (or JVL to Herring's). [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **The Prize Play card is the driver.** The product is InComm's **Prize Play card** (John's product; Val was unsure of the exact name). Two use cases discussed: a **player cashing out from the card at a machine**, and **machines accepting the card directly**. Campbell asked whether JVL wants machines to accept **all** network cards or only **loaded** cards; Val deferred — he will follow **market requirements** (undecided). See the recycler-as-ATM / Skill-Pay card thread on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul-31). [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Single-agreement business structure.** JVL is **not the operator**, and Herring wants its **economic agreement with whoever owns the cash in the machine**. Rather than have Herring deal with many separate operators, **Val will consolidate the operators under one agreement with himself and route them all to Herring "one way"** ("embed everything into one line agreement… otherwise it's going to be chaos") — Campbell welcomed it. Herring would then hold a **non-economic support agreement with JVL** for the machine and software, with the economic agreement sitting with the cash owner. [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Rough costs (Campbell, explicitly loose — "throwing gel on a wall").** Cost of the **cash in the machine ≈ prime + 1%**; **per-transaction fee ≈ 2–10 cents**. Real pricing depends on the use cases and volumes. [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Other services.** Herring can provide **general banking** across the three states, and **ATM cash replenishment** through their armored service — Maya can set that up for Val or his customers. (This is the same CIT/armored service discussed on the [[wiki/meetings/2026-07-10-herring-bank-cash-management-partnership.md|Jul-10 call]].) [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- **Counterparty and next steps.** The contract will be signed with **Herring Bank**. Campbell/Maya will get Val **into Herring's system** and schedule a call with **Ricky Rodriguez** (product) to start integration and testing; Val will **draft the use cases** and circulate them to Maya and Ricky; and Val will provide **a JVL machine to Herring's lab** for testing. **Maya will attend the Georgia Co-op Expo** for a day, where JVL has a booth and Val will show the equipment. **§15.8:** banking / card-product / network-sponsorship terms are company economics — recorded; no named-person compensation appears. [[raw/Meeting_Notes_Herring_Bank_Prize_Play_Card-July-31-2026.md]]

## Sources

- [[raw/Meeting_Notes_Herring_Bank_Prize_Play_Card-July-31-2026.md]]
- [[raw/Meeting_Transcript_Herring_Bank_Prize_Play_Card-July-31-2026.md]]

- [[raw/Meeting_Notes_Herring_Bank_Cash_Management_Partnership-July-10-2026.md]]
