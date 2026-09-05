---
type: decision
title: E-wallets move to the cloud — "это даже не обсуждается" — and must survive a hardware swap at the location
date: 2026-09-02
aliases: [e-wallets to the cloud, cloud wallet storage, wallets survive hardware replacement, friendly locations, wallet scoped to location, local wallet storage]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# E-wallets move to the cloud, and must survive a hardware swap at the location

Settled in the strategic half of the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept 2 2026 Flex-IQ pre-pilot call]], starting from a question [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] asked about how the wallet is scoped. It is a direct correction of the current implementation, which the team discovered on the call is local-only.

## What was decided

- **Wallets are still stored locally with no cloud at all — and that changes.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] realised it aloud mid-discussion: "Я только сейчас на самом деле осознал, что у нас [и]волет и попрежнему же локально хранятся никакого клауда нету," and immediately closed the question: "Это даже не обсуждается, это должно быть так" — it is not even up for discussion, it must be so [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **[[wiki/people/pavel.md|Pavel Frolov]] supplied the argument that carried it:** "это должно быть в клауде, потому что это потом легко будет распространяться на мобильные телефоны. Но что без клауда это будет невозможно" — cloud is what later makes phone-based wallets possible; without it that is impossible, or at best "возможно, но [с] дополнительным[и]… сложност[ями]" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Replacing hardware at a location must not affect wallets already created and still active there.** Andrei — answering despite having just said he would follow Val's instruction not to comment on engineering ("следуя заветам вала, я не хочу комментировать инженерные решения") — confirmed: "по поводу замены хардвара на локации это не должно повлиять на [и]волиты созданные и всё ещё активные на этой локации" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]. The derived summary note records the same two rulings — that e-wallets must move to the cloud and that a hardware swap must not affect active wallets [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **This is the one requirement Chudinov named as blocking the rest of the design.** Asked what he needs settled, he answered: "для… Будущих [капабилити] требования надо из основного принять решение… Локальное хранение [и]летов, либо глобальное облачное, потому что все остальные решения у нас так или иначе уже есть — работа с принтером и с работ[ой] с [флекс]портами просто не интегрированы в другие репозитории. Это надо просто научить флекс[ айкью] с этим работать, а вот хранение [и]лет[ов] тут надо будет туда продумывать систем[у]" — printer and Flex-Port work already exist and merely need integrating; wallet storage is the one thing that needs designing [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Left open deliberately: whether a wallet stays scoped to the location that created it

- **Today it does, and Andrei does not propose changing it.** "существует ли [e]воля только в рамках той локации, где он был создан? Думаю, да. Мы это пока не меняем, то есть, если вы создали этот [и]волят на локации а и пошли на локацию б даже Того же оператора, я думаю, он там не полезет." His reason is market demand, or the absence of it: "Других требований у нас пока не поступало от рынка. Каждая локация заинтересована в том, чтобы удерживать своего игрока только у себя. Они не хотят его отдавать никому" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **[[wiki/people/val-levitan.md|Val]] pushed back without ruling:** "Я не уверен, что мы хотим делать такой дизайн." [[wiki/people/irina-shishko.md|Irina Shishko]] restated what is being questioned — "Привязка только к одному лак[ейшену]… Оператору" — and Chudinov added "Игроку тоже интересно" (the player has an interest too). Andrei's response was to put it back as a question: "сейчас у нас так сделано… Вопрос, хотим ли мы поменять это сейчас?" **No ruling was made** [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **Pavel offered the mechanism for later:** with globally-issued QR codes landing in the cloud anyway, "мы можем потом какое то дополнительной опции сказать, что вот эти вот лакейшины, они френдли и они могут… Использовать друг друга [и]лет[ы]. Ну то есть прям на сервере сказать" — a server-side flag marking locations "friendly" so they can share wallets. Andrei: "Да я понимаю да" [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

## Relationship to earlier rulings

The Aug-24 Flex-Port-Mini design already assumed a central component — Pavel's QR-embedded cloud-service URL registering transactions centrally ([[wiki/decisions/2026-08-24-drop-pin-from-evoucher-flow.md]]) — but the wallet itself was never moved off the local device. This ruling closes that gap. It is also what makes the phone-based direction discussed on the same call reachable at all; see [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept-2).

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — design the wallet-storage system for the cloud model, this being the one piece he named as not already existing — due unspecified — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Open questions

- Should a wallet remain scoped to the location that created it? Currently yes; Andrei sees no market demand to change it, Val is "не уверен, что мы хотим делать такой дизайн," and Pavel's "friendly locations" server flag is the proposed later mechanism. **Unresolved** — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- Should the wallet be scoped to the **operator** rather than the location? Chudinov's original question was "[и]лет должен функционировать в рамках оператора или… только на этой лок[ации] или можно вернуться через какое то время на этот лакейшин… после всех там [ресетов] перестановки всех софтов." Andrei answered the hardware-swap half; the operator-scope half was not answered — [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
