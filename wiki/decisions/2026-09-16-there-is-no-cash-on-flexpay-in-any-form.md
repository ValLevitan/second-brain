---
type: decision
title: There is no cash on FlexPay in any form — the "cash returned" end state comes out of card issuance, and the cash-return option comes out of Flex IQ
date: 2026-09-16
aliases: [requirement 1382, requirement 1441, capability 117, capability 148, no cash on FlexPay, cash returned end state, card issue end states, physical or electronic cash return, escrow on the last bill, card stuck in the dispenser, trash box, нету никакого кэша на flixpay]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# There is no cash on FlexPay in any form

Two requirements on [[wiki/people/irina-shishko.md|Irina Shishko]]'s open-question list at the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian) turned on the same mistaken assumption — that money can come back to a player as cash. Both were corrected by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/pavel.md|Pavel Frolov]] from how the products actually behave [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Requirement 1382 (capability 117) — the three end states of card issuance

The requirement, authored by Pavel, said card issuance on the FlexPay kiosk must finish in one of three states: the card handed to the player, **cash returned to the player**, or the operation parked as something needing investigation [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Chudinov killed the middle one outright [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Про какой кэш речь[?] Нету никакого кэша на fl[e]xpay. Ни в каком виде? Не… девайсом типа риса[й]клера, не… оператором[-]кассиром, потому что это… киоск чисто для игрока.**
>
> *(What cash are we talking about? There is no cash on FlexPay. In no form at all — not by a device such as a recycler, not by a cashier-operator, because it is a kiosk purely for the player.)*

His instruction was to strike the option: "я бы просто убира[л] [из] списка… у нас нету кэш [ретёрн] back и всё. Не поддерживается ни в каком виде" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Pavel supplied the replacement logic: the player either receives the card, or hits a card error — "тогда у него деньги остались на его [во]лет[е]", in which case his money simply stays on his wallet [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Why the requirement is in the wrong release.** [[wiki/people/andrei-klimovich.md|Klimovich]] asked why a FlexPay requirement is in MVP 1 at all — "почему у нас это вообще в M[V]P один? Если это чисто флекс[пей]" — MVP 1 is Flex IQ alone ([[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]]). Rather than patch it on the call ("тут надо это переписывать… мы сейчас точечно это не пере[к]ро[и]м"), he took it away to check against the requirements that already cover card issuance on Flex IQ, with the expectation of reworking it for FlexPay in MVP 2 [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**What the FlexPay version will have to handle**, sketched on the call as the reason it needs its own logic rather than a copy of the Flex IQ one:

- The card is issued and activated, InComm loads it with money, "но она по какой[-]то причине не вышла из диспенсера[,] застряла" — and it then jams in the dispenser (Klimovich) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].
- A power cut and reboot: "когда система поднимется, он карточку автоматически скидывает в трешбокс, котор[ую] не успел[ ]…пользовател[ь]" — on start-up the machine drops into the trash box the card the player never collected (Chudinov) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**On Flex IQ none of that exists, because JVL's visibility stops at the activation.** Klimovich: "ты или активировал[,] или не активировал[,] дальше наши… полномочия[ —] всё. И если кассир не отдал карточку по какой[-]то причине игроку, мы этого даже не знаем" — either the card activated or it did not; past that point JVL's authority ends, and if the cashier never handed the card over, JVL does not even know [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Requirement 1441 (capability 148) — physical or electronic cash return

The same misconception, in the reverse direction: a return of cash to the player if the ticket fails. Pavel: "для флекса IQ это как бы не актуально, потому что если тикет не получился, то кассир… деньги не заберёт с игрока" — on Flex IQ it does not arise, because if the ticket did not come out, the cashier simply does not take the money from the player [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

Klimovich's complaint was that he had wanted the requirement written gateway-agnostic and it had come out Flex-IQ-specific anyway — "хотелось бы держать каким[-]то [гейт]в[е]й[-]агностик… но она не получается агностическая[,] сейчас она чисто под айкю" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. The option was deleted: "давайте просто удалим этот [опшен] и всё. И оно работает" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The FlexPay escrow answer, in passing.** Klimovich raised escrow as the FlexPay-side mechanism; Pavel corrected the scope — "эскроу только… на одну последнюю купюру" (escrow holds only the single last bill) — and then noticed the consequence himself: "после 1 купюры мы уже можем печатать ticket". Klimovich confirmed that is how it already works: the first note is inserted and verified, the offer to create an e-wallet follows, the wallet is created, and the player sits in an add-more-money-or-print-a-ticket state with the wallet already in existence [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. That matches the bill-escrow boundary already recorded on [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]] and the wallet-before-ticket ordering on [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — check requirement 1382 against the other requirements covering card issuance on Flex IQ; if it duplicates them, move it to MVP 2 and rework it for the FlexPay dispenser cases — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open questions

- **Whether requirement 1382 duplicates the existing Flex IQ card-issuance logic.** Klimovich took it away to check and did not answer it on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

**§15.8:** clear — product behaviour and device mechanics only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
