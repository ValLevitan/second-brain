---
type: decision
title: Flex-IQ must support multiple clearing houses, selectable per device — not in the MVP
date: 2026-08-27
aliases: [multiple clearing houses, clearinghouse selection per device, clearance provider choice, Flex-IQ provider switching]
source-count: 3
status: active
open-commitments: 1
open-questions: 2
---

# Flex-IQ must support multiple clearing houses, selectable per device — not in the MVP

Ruled by Val on the seven-minute [[wiki/meetings/2026-08-27-flex-iq-multiple-clearinghouse-selection.md|Aug 27 2026 call]] with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]. It is a capability request against [[wiki/topics/flexpay-business-architecture-payout-devices.md|Flex-IQ]], driven by Val's expectation that [[wiki/organizations/incom.md|InComm]] will not stay unopposed.

## What was decided

- **At device registration there must be a selection of who the clearance is done with.** Val: "For when we register with income… Any sort of registration of, let's say, IQ or further devices. I would like to have a **selection screen of who we are going to do our clearance with**." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **The wording Val fixed:** "**Multiple clearing houses** should be accessible either by… selecting a clearinghouse **in the setting or on the fly**." When Andrei proposed "per location", Val corrected him: "**Not per location, per device**" — reasoning that Flex IQ is one thing that needs clearing and "we could have, let's say, a self-attending device. That's a different story." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **The hard requirement is switching cost, not the switch itself:** "We just need to have this capability that we could easily switch on a fly. **I don't want to be re-approving the software. I don't want to be designing the software again.**" [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **Not part of the MVP** — Val, unprompted: "And it doesn't have to be a part of the MVP." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **Do not approach other clearing houses yet.** Andrei asked directly whether this means starting to contact other clearinghouses; Val: "No… Not for now. **We're fine for now.** But yeah, it could be possible." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **Andrei records it as a capability (or a small set), kept deliberately minimal** — "I will create this capability, maybe a set of capabilities, but again, it's very minimal as for now." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]

## Why

- **Val's stated premise is competition, and visibility of the choice:** "I predict, I predict that that income will have competition, and I'd like to be able to choose. Either income or somebody else, and I'd like it to be visible… for our technicians or for whoever it is, I'd like to make it **pronouncedly visible. That there are choices**." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- **The use case Andrei brought (from a conversation the previous day, and NOT what Val was asking for):** some locations run more than one card provider at once — the transcript's example is "**FirePay** plus income" (rendered "**Fiery Pay**" moments later; JVL's known competitor of that name is tracked on the [[wiki/meetings/2026-08-12-fiery-pay-competitive-analysis.md|Aug-12 competitive analysis]]) — so if a player wins **$8,000** and one supplier's daily cap of "let's say **5K**" is reached through InComm, "the location still has an opportunity to issue the rest of **3K**" through the other provider. Val's answer: "**The goal is to have that choice, but I'm not necessarily saying that it should be the location that chooses it**", "Because I'm not sure that the location is the right… selector of who to choose. But regardless, who is choosing, that's a different story." [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]

## Update — Sept 2 2026: restated by Andrei as a business pillar, and widened to card providers

On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept 2 2026 Flex-IQ pre-pilot call]], while [[wiki/people/val-levitan.md|Val]] was listing the business pillars for the device family, [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] added this one himself: "я докину ещё один [pillar] для бизнес требования… Поддержка… разных… карт[-]провайдер[ов], то есть сейчас у нас только инк[омм], но нам надо уметь поддерживать всех, кто есть на рынке." Val endorsed it immediately: "Абсолютно. Точно." [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

Two things changed shape: the requirement is now stated by Andrei rather than pulled out of him by Val, and it is framed as **card providers** generally rather than clearing houses specifically. The Aug-27 limits (per device, not per location; not in the MVP; do not approach other clearing houses yet) were not revisited and stand.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — capture multiple-clearing-house selection as a capability (or small capability set), per device, selectable in settings or on the fly, kept minimal so it is not lost — due unspecified; explicitly not MVP — [[raw/Meeting_Notes_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]

## Open questions

- **Who ultimately selects the clearing house** — the location, or a central decision? Val explicitly left it for later — [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- Whether the capability should be unwound into formal requirements now or only recorded so it is not lost. Andrei asked; Val's answer on the recording is a bare "Yeah, yeah" after an interjection, so **the answer is unclear** and is not asserted here — [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Multiple_Clearinghouse_Selection-August-27-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
