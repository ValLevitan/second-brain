---
type: decision
title: Every device at a location carries its own LTE modem and SIM and is self-sufficient — the location router is not the shared modem — and Val asks the team to work out whether the spare modems can back each other up when Wi-Fi fails
date: 2026-09-15
aliases: [LTE modem per device, own SIM per device, no shared router modem, self-sufficient devices, modem failover map, mesh network, Wi-Fi resilience, two communication channels, каждое устройство свой модем]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# Every device carries its own LTE modem and SIM

Settled at the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian), in answer to a direct question from [[wiki/people/andrey-bosik.md|Andrey Bosik]], who owns the Wi-Fi work ([[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]]).

## The question

Bosik had been assuming the location's existing router could be the shared LTE modem for everything: "я изначально рассматривал вариант, что… поскольку у нас на каждой локации есть маршрутизатор, что мы можем этот маршрутизатор использовать как л[ ]т[ ]е модем… и все будут через него ходить, но я правильно понимаю, что мы идём к той мысли, что у нас каждое устройство… абсолютно самодостаточн[ое]? То есть у нас в каждом киоске всегда есть [LTE-]модем с сим картой" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The ruling

[[wiki/people/val-levitan.md|Val]] extended it past the kiosk to everything on the floor [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **и в каждом [Flex ]I[Q]… и в каждой машине, и в каждой машине… Если у нас на лок[ации] есть IQ, наших пару машин, наш киоск, то все 4 или 5 девайсов в себе имеют L[T]E modem[,] живут самодостаточно. И могут друг друга видеть в сети через вайфай, но всё равно живут со своими модемами.**

Bosik accepted it — "всё[,] я понял" — and immediately drew the consequence for his own design: if that is so, the question becomes whether a separate Wi-Fi access point is worth installing at all. "тут на самом деле, если это так, то вообще возникает вопрос… [стоит] ли… как вай фай точку… вставить[ —] я понял, ну надо подумать" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The Wi-Fi module and external router position is [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]].

**The cost rationale is garbled in the source and is not asserted here.** Val gave a reason beginning "потому что нам симкарт[ы] и дата стоит очень…" and continuing "не очень маленькие деньги" — literally "not very small money". The derived notes gloss the same sentence as *SIM cards and data are cheap*, which is what the argument requires but the opposite of what the words say. Recorded as **unclear**; the ruling itself does not depend on it [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The follow-on Val asked the team to think about

Having put a modem in every box, Val asked whether the redundancy can be used: "если есть возможность улучшить вай[-]фай связь за счёт того, что у нас есть… множество сим… [баз]… трансми[т]тер[ов] — у меня тоже это радует", and then the shape of it — devices that discover each other over Wi-Fi agreeing a map, "**создадим карту, что если вот ты не работаешь, то я работаю[ — ]вот такого типа… логику**". He was explicit that he does not know whether the technology allows it: "я не знаю, есть ли на этой технологии или нет, поэтому стоит это продумать" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

- **Bosik flagged that this is the mesh idea already set aside:** "это то, что мы говорили[ — ]в машин[ы] сети[ —] но мы ж всё отказались пока от этого идти" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **[[wiki/people/pavel.md|Pavel]] pointed out the simplest version already exists:** a machine has two communication channels — "один через флекспорт[,] а 2 через модем. Если чтото у нас произошло с вайфаем, то мы можем через модем[,] по крайней мере[,] на сервер… о чём[-]то сказать". His verdict on the wider failover map: "это надо подумать, что из этого можно вытащить" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

This sits directly under the non-functional-requirements demand Val made minutes later — how a device reconnects, how JVL finds out, how the alarm is raised ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] and [[wiki/people/pavel.md|Pavel Frolov]] — work out whether the per-device modems can be used as a failover map for each other when Wi-Fi drops, and whether a separate Wi-Fi access point is still worth installing — due unspecified; Val asked them to think it through — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Whether the technology allows a modem failover map at all.** Val said plainly he does not know; Bosik notes the mesh route was already set aside; Pavel will look at what can be extracted from the two channels a machine already has — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — network architecture only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
