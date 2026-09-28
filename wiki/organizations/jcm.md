---
type: organization
title: JCM (bill validator / recycler vendor)
date: 2025-05-20
aliases: [JCM, JCM Global, GCM, G 7, G C M]
source-count: 8
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

## Aug 12 2026 — a four-drum JCM recycler as the second source

On the [[wiki/meetings/2026-08-12-hardware-github-standard-bc-sync-design.md|Aug-12 Val–Genadi session]] (the transcript renders JCM as "GCM" / "G 7"; the notes read it as JCM) [[wiki/people/genadi-peari.md|Genadi]] reported on JCM's recycler. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

- **Four real drums, 30 notes each**, which JVL can fill in any mix it wants (Genadi's example: 60 × $20 = $1,200, 30 × $10 = $1,500, and one drum of fives). Width fits JVL's recycler space; it is longer, which is fine; cassette sizes can be chosen. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **Better than MEI on this point.** Genadi: MEI ("MI") must keep one drum partly empty to swap notes when it searches for a denomination, so JVL would be limited in banknotes; "you can't compare four barrels." (Compare the CPI/MEI first-drum constraint on [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Jul-31.) [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **JCM has opened up.** JVL now has the full SDK, all documentation and contact with JCM's engineering sustaining team. [[wiki/people/cliff.md|Cliff]] wrote that they do not give a sample; the price for one unit is 1,850 (currency not spoken; the notes read it as dollars), and delivery to Minsk takes about a month. Val recalled that earlier JCM had wanted JVL to sign something, which JVL did not; Genadi did not know why the earlier friction happened. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- **Val: two suppliers, integrate both.** "Even if it will be so, I still would like to have two suppliers. And the price seems to be the same, more or less." "I don't want to depend on anyone else." Outcome: **buy one unit**. JCM said it has stock; Val suggested routing it "through CMA" (not identified) rather than asking JCM to ship to Minsk. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- *(Inference, not stated in the source: the four-drum unit fits the "larger four-drum RQ" variant Cliff described in May 2025; the model is not named on Aug-12.)*
- **A bezel problem (vendor not named).** Genadi said "they" sent a unit without a bezel and the narrow bezel cannot be obtained ahead of a show; a European bezel he found does not fit. The derived notes pin this on JCM; the transcript does not name the vendor. [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]

## Aug 18 2026 — an outside maker's view: ID-003 papers held back, and JVL cannot buy the connectors

At a show-week [[wiki/meetings/2026-08-18-mutha-goose-maker-supplier-dinner.md|dinner]] the maker of the Mutha Goose ([[wiki/organizations/rks.md|RKS]] by context) described JCM as hard to get documents from. [[raw/Meeting_Transcript_Mutha_Goose_Supplier_Dinner_Intel-August-18-2026.md]]

- **ID-003 editions are not shared.** "JCM's pretty tight-lipped on all their editions they've done. I've got ID zero three documented, But then all of a sudden new calls show up, and they won't give me the latest ID zero three paperwork." His last official copy came "from Paceomatic" ([[wiki/organizations/pace-o-matic.md|Pace-O-Matic]]) after he signed a confidentiality agreement. [[raw/Meeting_Transcript_Mutha_Goose_Supplier_Dinner_Intel-August-18-2026.md]]
- **Others publish.** "MEI, they they publish theirs openly. Even incredible technologies, they'll let you know anything you want to know about their protocols." [[raw/Meeting_Transcript_Mutha_Goose_Supplier_Dinner_Intel-August-18-2026.md]]
- **JVL's connector problem.** Val: "We… were trying to uh get one of their connectors. JCM connectors… And they they're not selling… We haven't been able to find." The maker said it is "really close to an automotive part" (Molex). The table agreed the plastic housing can be 3D-printed ("We print the plastic connector" / Val: "that's not an issue. But the pins?") — the pins are a Molex-type pin, and "if the pin is not sitting correctly, it's a lot of problems." Val's view: "Clearly GCM is just this difficult company to do business with" ("GCM" = JCM). [[raw/Meeting_Transcript_Mutha_Goose_Supplier_Dinner_Intel-August-18-2026.md]]
- *(How this sits with Aug 12 above: there Genadi said JCM "has opened up" and JVL now has the full SDK. Six days later Val still could not buy the connector. Different items — documents vs parts — so recorded as both, not as a contradiction.)*

## Aug 25 2026 — kept as the parallel source while CPI is tried

On an [[wiki/meetings/2026-08-25-texas-install-recycler-sourcing-cpi.md|Aug-25 call]] about a 25-machine Texas install (the transcript renders JCM "G C M"), [[wiki/people/genadi-peari.md|Genadi]] said that on configurability "JCM product is better". Val: "I don't know whether there will be enough capacity or not. And the fact that we have JCM product is fantastic. Let's continue working with JCM, but I also want to try the new C[PI]." — i.e. [[wiki/organizations/crane-cpi.md|CPI]]'s stackable unit. Two suppliers remain the line, as on Aug 12. [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]

## Open questions

- Does the RT denominate notes on the way *out*? Cliff was ~99% sure it tracks which drum holds which denomination (so pre-loaded drums stay correct) but had to confirm. [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/theory_product_discovery_process-may-12-2025.md]]
- [[raw/commission_flex-pay-may-16-2025.md]]
- [[raw/JCM_meeting_Cliff__bill_recycler-may-20-2025.md]]
- [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Mutha_Goose_Supplier_Dinner_Intel-August-18-2026.md]]
- [[raw/Meeting_Transcript_Texas_Install_Recycler_Sourcing_CPI-August-25-2026.md]]
