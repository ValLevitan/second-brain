---
type: organization
title: Crane CPI
date: 2026-02-23
aliases: [CPI, Crane CPI, Crane, BNR, BNR Advance, BNR BNF, SCR, SCR Advance, SC Advance, Jacob Blair]
source-count: 5
open-commitments: 3
open-questions: 1
disambiguation: "Crane CPI is the bill-acceptor / bill-recycler vendor. It is not the same thing as Val's old company CashCode, which Val says he sold to 'Crane' or 'CPI' (renderings vary; see [[wiki/people/val-levitan.md]]). 'CPI-477' on the FlexPay topic is a Jira ticket key, not this company."
---

# Crane CPI

**Crane CPI** makes bill acceptors and bill recyclers. JVL met it on **Feb 23 2026** to choose a recycler for its cash-handling devices ([[wiki/meetings/2026-02-23-crane-cpi-bnr-vs-scr-recyclers.md]]). From July 2026 it is the "CPI" whose recycler JVL is building into its payout kiosks (see [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Jul 31 and Aug 26 2026).

**Name note.** The company name is never spoken in the Feb-23 transcript. It comes from the file header and the derived notes' calendar pairing ("Crane CPI Recyclers - JVL Discussion") [[raw/Meeting_Notes_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]. What the transcript does show is that the company makes the **SC Advance**: "the SC Advance. That's our that's our bill acceptor" [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]].

## People

- **Jacob** (surname **Blair** per the derived notes) — ran the Feb-23 call. "I am based out of Cincinnati, Ohio. But I am actually in Seattle today", on a customer visit [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]] [[raw/Meeting_Notes_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]. His job title is not stated. No person page.
- **Chad** and **Lewis/Louis** were invited but did not join. Chad was "in in uh Germany forum the Euro shop trade show" (read: in Germany for EuroShop) [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]. The notes give them as Chadwick Pinson and Luis Fuller [[raw/Meeting_Notes_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]].

## Products, as presented on Feb 23 2026

All figures as Jacob gave them; prices are his ballpark, not quotes. [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]

- **BNR Advance** ("banknote recycler"). Recycles up to four denominations — "ones, fives, tens and twenties". Two recycling cassettes of 90 notes each (180 in total), each a roller cassette with two drums; a 600-note cash box; a loader cassette of up to 250 notes that takes bills in any orientation, checks each one at the head and sorts it into the right drum, and refills low drums on its own. The chassis is configurable, up to three recycling cassettes, but still four denominations. $50 and $100 bills are accepted but go only to the cash box. Not marketed for gaming: it lives in retail self-checkout ("Walmart, Target, um big box retailer five below") and transport. Price "in the four to five thousand range… really on the high side"; volume tiers "fifty, one hundred, two hundred and fifty five hundred"; the 250 tier would need "some sort of minimum" commitment.
- **BNR BNF** ("Bunch Note Feed"). Same family; takes up to 50 notes at a time from the front, loader optional, room for three recyclers; "right around the same price".
- **SCR Advance.** The SC Advance acceptor with recycling added: two recyclers, 120 notes in total (60 each; 30 per denomination at four denominations); cash box of 600 or 1,200 notes; bills loaded one at a time. Same accepting head and top unit as the SC Advance. Price "close to the… two thousand, twenty five hundred range", set against Fujitsu's dispenser.
- **Integration.** BNR: "our UAPI… device level integration… Java plus". SC: "really only two interfaces with RS232 and USB".

## Relationship thread

- **Feb 23 2026 — consultation.** JVL leaned to the SCR if $50/$100 recycling is not available. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Feb 23 2026). [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- **Jul 31 2026 — the drum-order rule.** Genadi reported that CPI's logic makes the first drum hold the lowest denomination; Val called this unusable and wanted it changed [[raw/Meeting_Notes_Flex_Recycler_Georgia_Show_Readiness-July-31-2026.md]].
- **Aug 26 2026 — a bigger CPI recycler.** Val told Genadi to source a larger-capacity recycler from CPI; Pavel named the model only as "some BNR or BNP, I think BNR", and said its library would not work with JVL's [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]].
- *Inference, not stated in any source:* the Feb-23 lean was to the smaller SCR; the Aug-26 order points back to the larger BNR. Recorded as sequence only.

## Link to Val's CashCode story

Val tells the story of selling his company CashCode in 2006. On Sept 17 2026 he said "Sold it to Crane National Vendor, CPI now" [[raw/Meeting_Transcript_J_and_J_Gaming_Nebraska_Entry_and_Effingham_Evaluation-September-17-2026.md]]. The Feb-23 derived notes also say CashCode "is a Crane brand" [[raw/Meeting_Notes_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]. **The Feb-23 transcript does not mention CashCode at all**, so this meeting adds no evidence to the open "who bought CashCode" question on [[wiki/people/val-levitan.md]].

## Open commitments

- [ ] Jacob (Crane CPI) — confirm with engineering whether the BNR and the SCR can recycle $50 and $100 bills today — due unspecified ("as soon as I have an answer") — [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- [ ] Jacob (Crane CPI) — have engineering share the SDKs, APIs and integration files, by GitHub if possible (Val: "We prefer GitHub"; Jacob had proposed a OneDrive link) — due unspecified — [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- [ ] Jacob (Crane CPI) — send the BNR/SCR data sheets ("I can send you guys these sheets as well") — due unspecified — [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]

## Open questions

- Can either recycler take $50 and $100 notes into a recycling drum? Jacob was "ninety nine percent sure" the BNR logic is "not configurable for fifties and one hundred s"; Val was "ninety nine point nine percent sure" it is only a matter of the engineers' willingness. No answer is recorded in the corpus — [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]

**§15.8:** clear — product and price economics only. **§15 #9:** no identifiers.

## Sources

- [[raw/Meeting_Transcript_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- [[raw/Meeting_Notes_Crane_CPI_Jacob_Blair_BNR_vs_SCR_Recyclers-February-23-2026.md]]
- [[raw/Meeting_Notes_Flex_Recycler_Georgia_Show_Readiness-July-31-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Planning_NOVA_and_Sept_Releases-August-26-2026.md]]
- [[raw/Meeting_Transcript_J_and_J_Gaming_Nebraska_Entry_and_Effingham_Evaluation-September-17-2026.md]]
