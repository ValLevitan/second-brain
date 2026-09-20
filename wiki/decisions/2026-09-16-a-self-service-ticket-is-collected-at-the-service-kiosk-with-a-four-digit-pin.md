---
type: decision
title: Nothing prints at the self-service kiosk — an MVP 2 player takes a four-digit one-time redemption PIN to the service kiosk, and a QR code was rejected because many players have no smartphone
date: 2026-09-16
aliases: [one-time redemption PIN, four-digit PIN, self-service printing, two tickets at once, QR code rejected, wallet access PIN, PIN access enabled, service kiosk redemption, wantime reedin post, MVP2 ticket printing]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# A self-service ticket is collected at the service kiosk, with a four-digit PIN

An MVP 2 design direction stated at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian). It is recorded because it settles a question that keeps recurring in this series — where a winning ticket physically comes out when the player is not standing at the machine that prints it [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The problem [[wiki/people/pavel.md|Pavel Frolov]] raised

He flagged it "просто для записи" — just for the record — and agreed it is not MVP 1: a player presses *generate ticket* on a Flex-Port. Where does it print? If it prints at the FlexPay kiosk, "а другой игрок стоит возле флекспей[,] и у него выезжает тикет" — another player is standing at the FlexPay and someone else's ticket slides out at him [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## [[wiki/people/andrei-klimovich.md|Klimovich]]'s answer: nothing prints at the self-service kiosk at all

"[Э]то продумано уже в [MVP] 2[:] мы предлагаем не печатать сразу на селф[-]сервис киоске тикет, потому что создаёт много проблем. Не только то, что ты описал, но ещё 2 тикета одновременно — это плохо" — the stray-recipient case Pavel named is only one of them; two tickets emerging at once is the other [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

The flow instead, in his words [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Т]ы нажимаешь [create new] уволят[,] и мы тебе предлагаем создать [one-]time [redemption PIN;] ты выбиваешь четырёхзначный пароль[,] и потом идёшь [к] сервис[ному] киоску[,] заходишь в отдельный блок интерфейса, где получить новые тик[еты,] там вбиваешь этот пин[-]код. И он генерирует твой тикет… для твоего волета.**
>
> *(You press create-new-wallet, and we offer you a one-time redemption PIN; you punch in a four-digit password, then you walk to the service kiosk, go into a separate part of the interface for getting new tickets, key in that PIN, and it generates your ticket for your wallet.)*

**The same PIN doubles as the wallet access code** where a location has PIN access switched on — "этот пин[-]код может быть использован как пин[-]код доступа к самому [е]волету, если на локации пин [акс]ес[с] [и]нейбл[д]" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. PIN access was ruled out of MVP 1 on Sept 11 ([[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]), which is consistent with this being MVP 2 work.

Pavel also asked whether the print-a-winning-ticket button on the Flex-Port therefore becomes optional, configurable per location. Klimovich said no — the button stays, and the PIN flow is what sits behind it [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Why not a QR code

Pavel's alternative was to show a QR code the player scans and carries. Klimovich refused it on the player population, and notably refused to invent a number while doing so [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Я] не буду сейчас сочинять процент пользователей, но большой процент… пользоваться не будут[,] ничего фотографировать[;] у больш[инства] пользовател[ей] нету даже смартфонов.**
>
> *(I am not going to invent a percentage of users now, but a large share will not use it, will not photograph anything; many users do not even have smartphones.)*

He then parked the whole subject — "давайте здесь сделаем паузу и вернёмся к этому [в MVP] 2" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The same no-smartphone argument sits behind the physical carrier ticket already recorded on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

**§15.8:** clear — product design only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** the four-digit PIN here is a player-generated one-time code in JVL's own product, not any licence, tax or account identifier; no such value appears in either source.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
