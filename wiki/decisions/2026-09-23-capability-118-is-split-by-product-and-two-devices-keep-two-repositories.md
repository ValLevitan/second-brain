---
type: decision
title: Capability 118 is split so FlexPay has its own capability apart from Flex IQ / Flex-Port, and the two devices keep two separate repositories for now
date: 2026-09-23
aliases: [CAP-118 split, capability 118 split, кап 118, do not mix products in one capability, не мешать в одной капабилити продукты, two devices two repositories, 2 девайса 2 разных репозитория, one repository built two ways]
source-count: 3
status: active
open-commitments: 1
open-questions: 1
---

# Capability 118 is split by product; two devices keep two repositories

Decided at the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian) by [[wiki/people/pavel.md|Pavel Frolov]], after [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] pressed for it [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].

## The problem

- **Finished Flex IQ work could not be closed.** Capability 118 held items for both products. [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] said the items he did were done "в рамках флекса айкью". Irina: "это нельзя проверить… и закрыть, потому что flexpay ещё не готов, а флексайкю готов" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].
- **Chudinov had warned about this.** "я вам говорил не мешать в одной капубилике продукты, что будет геморрой?… постоянно будет такое" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].

## The ruling

- **Split it, one side for FlexPay.** Pavel: "Хорошо, ладно, если так будет легче всем… разбираться, когда тестировать и что тестировать. Ну давайте разделим один будет flexpay" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].
- **How Irina did it, live:** "я сейчас сделаю от этого клон и разделю кап 118 будет порт и ф п, который делал Сергей а 12 03 12 04 в тот IP, который для флекспея и туда перенесу." She said "Я уже делю" before Pavel finished [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]. This is the same **clone-and-split** method used on capability 144 on Sept 18 (see [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]]).

## Two devices, two repositories — restated, not changed

- **Sergey's question.** If FlexPay and Flex IQ are so alike, why not one repository built two ways? "почему нету ни один репозиторий… в зависимости от этого собирать"; now "одно и то же реализуем условно там и там" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].
- **Chudinov: maybe later, not now.** He had thought about it "на будущее", but now there would be more conflicts — for example moving native libraries, and C++ mode switching ("2 плюс плюс переключение режимов", read as C++ — **inference**). "если стабилизируем на будущее, тогда… сможем" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].
- **Pavel recalled the earlier ruling:** "было принято решение, что 2 девайса все таки 2 разных депозитория" [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]. When and where that first ruling was made is not in this source.

## Why it matters

The split follows the product line already set for MVP 1: Flex IQ goes first and FlexPay is MVP 2 (see [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]]). A capability that holds both cannot close while FlexPay waits. *(This link is an inference; nobody on the call named the MVP 1 decision.)*

## Update, Sept 23 2026 (8:00 AM) — Irina reports the split to the MVP 1 call

Three hours later, at the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM call]], [[wiki/people/irina-shishko.md|Irina Shishko]] told Klimovich: "там сегодня ещё нашлись 2 капылити, в которых было flexpay и флекс айкю. Разделили их на… отдельно… то что flexpay на MVP 2 передвинула, чтоб опять же это не путалась в одно". She speaks of **two** capabilities; the stand-up record above names only **118**. Whether a second one was split is **not clear** from either source [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Open commitments

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — finish cloning and splitting capability 118: the Flex-Port / Sergey's item stays, 12-03 and 12-04 move to the FlexPay capability — due unspecified (started in the meeting) — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

## Open questions

- **Can FlexPay and Flex IQ later share one repository built two ways?** Sergey raised it; Chudinov said possibly, once things stabilise — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

**§15.8:** clear — work organisation only.

## Sources
- [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
