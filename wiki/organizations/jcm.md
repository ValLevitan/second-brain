---
type: organization
title: JCM (bill validator / recycler vendor)
date: 2025-05-20
aliases: [JCM, JCM Global]
source-count: 4
open-questions: 1
---

# JCM (bill validator / recycler vendor)

JCM is a gaming-hardware vendor that makes **bill validators/acceptors, printers, and bill recyclers** JVL uses in its machines and payment devices. It appears throughout the FlexPay/FlexPort hardware thread: JVL's spec requires FlexPay to work with **JCM UBA** and **JCM iVision** validators [[raw/commission_flex-pay-may-16-2025.md]]; JVL's printer library supports **Gen 2 / Gen 5 (JCM)** printers [[raw/Alignment_outstanding_subjects_2025-02-19.md]]; and on the May-12 product-discovery session Val noted **JCM makes a bill-to-bill recycler** similar to the one his old company **Cash Code** built. [[raw/theory_product_discovery_process-may-12-2025.md]] The May-20 2025 recycler evaluation call is stubbed at [[wiki/meetings/2025-05-20-jcm-bill-recycler-eval.md]].

## May 20 2025 — bill-recycler product evaluation (with Cliff)

Val evaluated JCM bill recyclers with JCM contact [[wiki/people/cliff.md|Cliff]] as a candidate cash-in/cash-out device for JVL's payout-device line (Val: "I think we have a market for this product … the business model lends itself for the use of these type of devices"). He wants acceptance of **$1/$5/$10/$20** and two recycling cassettes configured to give change in **$20 and $5**. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]

- **iPro-RC — end of life.** The **iPro-RC** recycler uses the **iPro head**, which is end-of-life; **firmware support ends at the end of 2025**, and it **cannot be updated to accept the new US $10 note** expected in **2026 or 2027** (it will still accept current $10s). ~**400 in stock**. Val ruled JVL will not go with the iPro. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- **UBA Pro-RC — the replacement.** Same unit with the newer **UBA Pro head** (different sensor technology); **form, fit, functionality and protocol identical** — a head-only change. **>1,000 in stock**; expected to cost more (Cliff awaiting a price). [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- **RC = friction-feed recycler.** Holds roughly **70–80 US notes** (rated 100, rarely achieved). Bins are key-locked; can be **hand-loaded** (one denom per bin) or loaded through the acceptor. It **does not denominate on the way out** — on dispense it reads note *thickness*; if it pulls a too-thick/too-long (double) note it diverts both to the cash box and reports only "an issue," so hand-loading the wrong denom into a bin means the wrong bill is paid out. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- **RT = twin-drum recycler ("belt"/Mylar-tape technology).** The **UBA Pro RT** stores notes on **two drums** using **Mylar film tape**; must feed notes **one at a time through the acceptor** (no bulk feeder — ~10 min per drum of 30) to load. Capacity **~30 notes per drum** (half the RC), but the drum guarantee is "if it went on the drum, it comes off the drum." Drums are **detachable** (can be pre-loaded off-site and delivered loaded). Same **form/fit/protocols** as the RC. The **RQ** is a larger **four-drum** variant. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- **Protocols:** JCM-proprietary — **ID-003** (RS-232 serial) and **ID-008** (USB); ID-003 is what JVL already uses on its regular bill acceptor (with extra commands for the recycling functions). Val asked for the updated **ID-003** protocol doc. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- **Reliability concern (open):** Cliff estimated (unpublished) **MTBF ≈ 250,000 cycles** on the RT; Val called that "very low" and asked JCM to verify it (and the cassette/tape MTBF). Cliff to send RT/RQ brochures with dimensions and get pricing on the RT and UBA Pro-RC. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]

## Open questions

- Does the RT denominate notes on the way *out*? Cliff was ~99% sure it tracks which drum holds which denomination (so pre-loaded drums stay correct) but had to confirm. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/theory_product_discovery_process-may-12-2025.md]]
- [[raw/commission_flex-pay-may-16-2025.md]]
- [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
