---
type: decision
title: JVL will support both dual SAS and single SAS — decided in a customer meeting on the distributor's insistence — and definitely not MudaGoose
date: 2026-09-09
status: active
aliases: [dual plus single, we're going with both, you just made up our decision, definitely not going with MudaGoose, dual saws or single saws, no final decision on SAS, ten thousand machines with no secondary SAS, secondary sats, AFT through the bill acceptor, MVP1 dual SAS only, MVP1 locations fully equipped with dual SAS]
source-count: 7
open-commitments: 0
open-questions: 0
---

# JVL supports both dual SAS and single SAS — and definitely not MudaGoose

Decided on the spot by [[wiki/people/val-levitan.md|Val]] in front of a customer at the [[wiki/meetings/2026-09-09-rao-machine-performance-and-exclusivity-offer.md|Sept-9 2026 10:04 AM Rao meeting]], after [[wiki/people/narasimha-rao-namburi.md|Rao]] told him a single-protocol product would not sell [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]].

**The exchange, in full:**

> **Val:** "Sorry, we have **no final decision whether we go dual [SAS] or single [SAS]**, but **we're definitely not going with [MudaGoose]**."
> **Rao:** "Okay, but you **definitely should go with dual plus single**. Okay, without it's not [going to work]."
> **Val:** "Okay, so **you just made up our decision. We're going with both**, but we're definitely not going with [MudaGoose]."

*(The transcript renders MudaGoose as "mudagus"; SAS as "saws". Both are garbles and are named in the wiki's own voice here, left as spoken inside the quotation.)*

## Why MudaGoose is out, in the same breath

Val's next sentence gives the reason, and it is the collection argument, not a technical one: "**Because if we, if there is another system present in location, we will never get paid. We can't collect our money. We have to be able to be exclusive in the location.**" So the MudaGoose exclusion here is the [[wiki/decisions/2026-08-31-transactional-equipment-only-with-location-exclusivity.md|Aug-31 exclusivity condition]] being applied, not a protocol choice. Val had also just told Rao, of the incumbent wiring: "you have to **remove [the MudaGoose modules] and you have to wire machines directly**." [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

## The consequence taken up immediately

A JVL colleague turned it into a test condition in the same conversation: "So **dual source and single source deal. Thank you for the feedback.** In October, if it's doable, we would prefer to start with a location where **all the machines are dual source**. Just for test." Rao: "There already all of them do it." [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

## Sept 15 2026 — the segment gets a size, and a reason to keep it

Six days later, explaining his collection mechanism to [[wiki/people/billy-liu.md|Billy Liu]] at the [[wiki/meetings/2026-09-15-billy-liu-playpay-nda-and-georgia-float-economics.md|Sept-15 evening session]], [[wiki/people/val-levitan.md|Val]] put the **first number in the corpus on the no-secondary-SAS population** — and described serving it rather than abandoning it [[raw/Meeting_Transcript_Billy_Liu_PlayPay_Georgia_Payment_Ecosystem_and_Float_Economics-September-15-2026.md]]:

> "**it's approximately ten thousand machines in the field that don't have secondary [SAS], and that is easier for me because I come down with my bill… acceptor, because there is no secondary [SAS]. I take the bill acceptor. I plug my AFT into the bill acceptor, and I plug the bill acceptor into my AFT. At the moment I shut down my AFT, the bill acceptor shuts down too.**"

- **He calls it *easier*, not a segment to drop** — the bill-acceptor wiring gives him a kill switch on money in and money out without touching the machine, which the Lottery forbids switching off. Commercial context on [[wiki/topics/georgia-prize-card-processor-economics.md]].
- **The figure is Val's own estimate**, given conversationally and prefixed "approximately"; nothing in the source attributes it to a report, and no other source in the corpus sizes the segment.
- **This is a dated data point on the contradiction below, not a resolution of it.** Sept 7 says drop the old-machine segment; Sept 8 leans the same way; Sept 9 says support both; Sept 15 describes a concrete mechanism for exactly the machines Sept 7 would abandon — but it is said to an outsider in a commercial argument, not as an engineering ruling. **Nothing is resolved.**

## Sept 18 2026 — the first release picks a side, and the business question is restated as open

At the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept-18 MVP 1 call]] the engineers settled it **for MVP 1 only**: [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] ruled "**[MVP] один — только д[у]о[ ]сас**", with MVP 1 pilot locations chosen so every machine is dual-SAS, and the bill-acceptor / counter-emulation route deferred. [[wiki/people/pavel.md|Pavel Frolov]] backed it on testing cost — "**поддерживать оба — это почти икс 2 тестирования**". See [[wiki/decisions/2026-09-18-mvp1-supports-dual-sas-only-and-locations-are-chosen-to-match.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**This resolves nothing below, and Klimovich said so himself in the same breath:** "**это нерешённый до конца ещё бизнес вопрос[:] у нас одни операторы говорят, что мне достаточно д[у]о сас[,] я все машины[;] другие говорят…**" — the sentence trails off unfinished on the recording [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Recorded as a dated data point of a different kind.** Sept 7, 8, 9 and 15 are statements about what *JVL the product company* supports; Sept 18 is a statement about what the *first release* covers. They are not the same claim, so this neither contradicts nor confirms any of them — but it is the first time a JVL decision has deliberately excluded the single-SAS half of the market with a date attached, and a reader tracking the argument should have it here. **The contradiction below stays open.**

## Oct 6 2026 — MudaGoose comes out of the code

At the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] Chudinov said he will remove MudaGoose ("мутагусь") from the code entirely — screens, the mode, tests, likely the old Payment Hub parts, the activation protocol. Pavel confirmed "у нас уже есть решение о том, что нам не нужен он вообще"; git history is the way back if it is ever needed. Irina: it still appears in requirements and Claude has to be stopped from using it [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]. See [[wiki/decisions/2026-10-06-mudagoose-is-removed-from-the-code-entirely-and-git-history-is-the-way-back.md]]. This carries out the "not MudaGoose" half of this decision; the dual-versus-single-SAS question below is untouched.

## Open contradictions

**Whether JVL supports single-SAS machines at all (Sept 7/8 vs Sept 9 2026).** Three statements inside three days point in opposite directions. Recorded, **not resolved**.

- **Sept 7, internal engineers' alignment, Russian — drop the segment.** "Проект флекс[-]порт сда[ё]тся с[о] [SAS]. Мы уходим от этого гибкого подключения, и **мы не будем адресовать ту часть рынка, которая сегодня стоит на старых машинах**" — the Flex-Port goes with SAS, the flexible connection is dropped, and JVL will not address the part of the market on old machines. See [[wiki/decisions/2026-09-07-flex-port-goes-sas-and-jvl-drops-the-old-machine-segment.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- **Sept 8, to a master licensee — hedged, but the same direction.** "**We're thinking maybe we shouldn't even support single-[SAS]. Just let it go, and connect to a second-[SAS] port**"; "this market will disappear within three years." [[raw/Meeting_Transcript_Dixie_Amusement_Georgia_Transactional_Equipment_and_Bundle_Economics-September-8-2026.md]]
- **Sept 9, to a distributor — both.** "We're going with both" (above). [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

**Why this is held open rather than treated as a straightforward evolution.** The three statements are two days apart — the same period — and the incompatibility is direct. But they are not the same kind of statement: Sept 7 is an internal engineering ruling about how the Flex-Port connects, Sept 8 is explicitly a thought in progress ("we're thinking maybe"), and Sept 9 is a sales-room concession whose wording ("dual saws or single saws") is garbled enough that it is not certain Val is answering the same question the engineers were. **No source mentions any other, and nothing withdraws the Sept-7 ruling.** Both are recorded, on this page and on the Sept-7 decision; neither page asserts which governs.

**§15.8:** clear — protocol and market-segment decisions only; no named-person compensation.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Notes_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_Dixie_Amusement_Georgia_Transactional_Equipment_and_Bundle_Economics-September-8-2026.md]]
- [[raw/Meeting_Transcript_Billy_Liu_PlayPay_Georgia_Payment_Ecosystem_and_Float_Economics-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
