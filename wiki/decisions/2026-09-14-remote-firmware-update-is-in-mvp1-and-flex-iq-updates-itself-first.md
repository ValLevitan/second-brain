---
type: decision
title: Remote firmware update is in MVP 1 — Flex IQ and FlexPay update themselves first, then distribute firmware to the Flex-Ports
date: 2026-09-14
aliases: [firmware upgrade in MVP1, remote firmware update, OTA firmware, приоритет номер один это чтобы обновлялся флекс ай кю, flash the FlexPorts, Flex IQ to FlexPort protocol, доперфек]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# Remote firmware update is in MVP 1, and Flex IQ updates itself before it updates anything else

Settled at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept 14 2026 12:04 PM call]] (Russian). [[wiki/people/val-levitan.md|Val Levitan]] set the requirement; [[wiki/people/pavel.md|Pavel Frolov]] set the order of work.

## The requirement

Val put it as non-negotiable and left the device open: "**нам обязательно в MVP один… То ли это касается IQ, то ли киоска, то ли флэкспорта — нам нужно [firmware upgrade]**" — it must be in MVP 1, whether it concerns IQ, the kiosk or the Flex-Port [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The transcript renders the capability as "**forwaprade**" and later "**фейервер**" — garbles of "firmware upgrade" / "firmware". The derived notes head the section "Firmware over-the-air update"; **the words "over the air" and "remote" are the notes' gloss, not Val's** — he names the capability without saying how it travels. Recorded as the source has it.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

And the quality bar, twice over: "**это дело нужно допи[лить] доперфек[т], это должно быть проф[екшен]**" — it has to be taken to perfection, it has to be production. What he wanted inside it: "**все там [нодес] там какието. Пинги кудато? Какието верификации, вот таймер — всё, чтобы вот это [firmware] и верификация должна работать**" — **pings**, **verifications** and a **timer**, and the verification has to work [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The derived notes list this as "verification, timer, confirmation". **"Confirmation" is not in this passage** — the transcript has "пинги" (pings); Val's word "подтверждение" (confirmation) comes later in the call, about ticket printing, not firmware. Corrected here against the source.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## The order of work

Pavel accepted the direction — "**Ну да, да, мы на это и идём**" — and split it in two [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

1. **Priority one — the gateways update themselves.** "**Приоритет номер один — это чтобы обновлялся флекс ай кю и флек[с]pay**."
2. **Priority two — the gateways update the ports.** "**приоритет номер 2 — это уже, чтобы они могли раздавать прошивки для флекспортов и их прошивать**" — so they can distribute firmware to the Flex-Ports and flash them.

This sits on top of the device scope already fixed for MVP 1 — Flex IQ alone, no kiosks — on [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]], and it is the mechanism behind the same-day 8:01 AM ruling that nobody downloads and installs builds by hand ([[wiki/decisions/2026-09-14-nobody-downloads-and-installs-builds-thirty-day-target.md]]).

## Who does it

Pavel named the sequence of people, not just of tasks: "**сначала её сейчас дима чудинов проработает со своей стороны. Может быть, какнибудь там улучшить протокол? Общение между флекса IQ и портами — и, возможно, как раз по этой задаче нам понадобится Алексеев, ну по[-]моему там на него тоже задача висит**" — [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] works the Flex IQ ↔ Flex-Port communication protocol from his side first and may improve it; [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] may be needed on the same task, and Pavel thinks a task is already assigned to him [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(§4 resolutions: "дима чудинов" → **Dmitri Chudinov**, the back-end architect (the derived notes render the Belarusian spelling "Dzmitry Chudzinau"); "Алексеев" → **Evgeniy Alekseev**, the embedded-code owner who works on Genadi Peari's hardware-adjacent projects — the registry's Zhenya-by-context rule, and the fit is exact here.)*

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — work the Flex IQ ↔ Flex-Port firmware-distribution protocol from his side, and improve it if he can — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — deliver firmware update in MVP 1 to a production standard, with pings, verification and a timer — due with MVP 1 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open questions

- **Is Evgeniy Alekseev actually assigned to this?** Pavel's own wording is hedged — "**возможно… по[-]моему там на него тоже задача висит**" — and nothing in the source confirms it — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**§15.8:** clear — product scope and task assignment only; no compensation or performance judgement for any named person.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
