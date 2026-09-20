---
type: decision
title: A kiosk can be de-enrolled from a location but never from the cloud database — once registered, a device is registered forever
date: 2026-09-16
aliases: [requirement 1378, capability 115, de-enrolment, dan rolald, enrolled kiosk, warehouse status, online status, nothing is deleted, QR code registration, serial number registration, дэн ролд, деенролл]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# A kiosk is de-enrolled from a location, never from the cloud database

Settled at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian), the first item on [[wiki/people/irina-shishko.md|Irina Shishko]]'s list of MVP 1 requirements carrying unanswered open questions. The requirement is numbered **1378** and sits under **capability 115** [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## What the open question was

The requirement was authored by [[wiki/people/pavel.md|Pavel Frolov]] — [[wiki/people/andrei-klimovich.md|Klimovich]] read it off the screen and said so: "я смотрю на этот рекла[мент] и это авторство Павла, но я понимаю суть вопроса" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The open question asked whether a kiosk can be de-enrolled on the cloud side.

Klimovich's first answer was simply yes, from what the Payment Hub already does: "наш пэймент хаб интерфейс клауд[ ]сервиса… позволяет руками ба[й]ндить какой[-]либо киоск или IQ на конкретную локацию… так же, как он [э]нроллится, так же он может быть и д[е]-[э]нролд руками со стороны клауд[-]сервиса" — the Payment Hub cloud-service interface lets you bind a kiosk or a Flex IQ to a specific location by hand, and the same interface can unbind it by hand [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The objection that produced the ruling

[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] stopped the quick answer, on the grounds that the word itself is ambiguous: "понятие д[е]-[э]нролл[а] тут каждый… может подразумевать по[-]своему" — everyone here will read "de-enrol" their own way. His own position was categorical [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Считай], что зарегистрировано, зарегистрировано навсегда. Оно может быть либо [на] лакейшне, либо в [у]эрихаузе. Либо тогда предусматривать вариант архивации… Без практики[,] с методологи[ей] ничего не удаляется.**
>
> *(What is registered is registered forever. It can be either at a location or in a warehouse. Or else you provide for an archiving option… as a matter of method, nothing is deleted.)*

Klimovich accepted it and restated the behaviour as it actually works: the device "остаётся… в статусе онлайн висит у нас или в статусе war[e]house, как Дмитрий говорит, но он не исчезает" — it stays in an online status or a warehouse status, but it does not disappear [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The ruling, in the wording written into the requirement

Pavel dictated it and then read back what he had saved: "[En]rolled kios[k] can be d[e-]en[]rol[le]d from [the] location but never from the cloud [database]" — his Russian framing a moment earlier was "может быть д[е]йн[-]ролд фром[ ][л]окэйшн, но никогда не d[e-]en[rolled] from [the] cloud da[ta]ba[se]" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The derived notes carry the same outcome [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## How a device gets into the database in the first place

Klimovich described the enrolment side in the same breath, which is worth keeping because it is the only place in this meeting the registration mechanics are stated: "он создаётся, появляется у нас в момент, когда мы его регистрируем… [п]росканировали QR[-]код на экране… потом создали для него [сериал] намбер, и он регистрируется" — the record is created at registration: scan the QR code shown on the device's screen, a serial number is created for it, and it is registered from that moment [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. That is consistent with the QR provisioning flow already recorded on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

*(Chudinov also floated "предусматривать вариант архивации" — providing an archive state — as the alternative to permanent retention. Nobody adopted or rejected it; it is recorded here as raised, not as agreed.)* [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

**§15.8:** clear — device registration and database design only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** the "serial number" discussed here is a device serial created by JVL's own registration flow, not a licence, tax or account identifier; no such value appears in either source.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
