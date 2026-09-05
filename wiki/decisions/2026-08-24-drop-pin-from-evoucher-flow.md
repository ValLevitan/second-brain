---
type: decision
title: The eVoucher flow runs without a PIN — a QR voucher is trusted the same way a TITO ticket is; from Sept 2 2026 the PIN survives as a per-location switchable option rather than being removed
date: 2026-08-24
aliases: [drop the PIN, eVoucher without PIN, no PIN code voucher, TITO trust model, QR voucher security, PIN as a switchable option, PIN per location]
source-count: 3
status: active
open-commitments: 0
open-questions: 1
disambiguation: "Status note: the core ruling (no PIN by default; TITO-style trust) stands. The titular 'drop the PIN' element was softened on Sept 2 2026 — the PIN is kept as a switchable per-location option, not killed. See the Update section."
---

# The eVoucher flow runs without a PIN

At the [[wiki/meetings/2026-08-24-flex-port-mini-capabilities.md|Aug 24 2026 Flex-Port-Mini session]] (Russian), [[wiki/people/val-levitan.md|Val]] pressed to remove the PIN that today protects a voucher, because the PIN forces a screen and a keypad onto the port and so blocks the cheap [[wiki/decisions/2026-08-24-flex-port-mini-via-second-sas-only.md|Flex-Port-Mini]]. [[wiki/people/pavel.md|Pavel Frolov]] had raised the PIN as the reason a screen is needed at all — "Мы на экране вводим пинкод" — and Val's answer was "Без пинкола" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## What was decided

- **The PIN goes.** Val repeatedly: "Я всё равно не понимаю, почему нужно пинкод." Pavel conceded it can be dropped — "в принципе, мы можем отказаться… От пинкода. Можем" — while stating the cost plainly: "Ну не будет защиты, как бы любой может повторить, ну, сфотографировать и… Повторить этот баркод?" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- **The trust model becomes the TITO ticket's.** Val: "Та же самая логика как тито тикет та же самая у тебя есть тикет, его можно сфотографировать, его можно акишевать. И это это твой кэш? Береги не показывай" — same as a TITO ticket: it is your cash, look after it, don't show it around. Pavel: "Ну в целом да в целом да" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## Rationale — the code is single-use, so a duplicate is worthless

- Val walked the attack through: a malicious customer photographs the barcode and makes a duplicate, presents the good one, JVL absorbs it and loads the machine; then he presents the copy, "Мы считаем, что этот баркод уже был использован, мы его дальше никуда не не берём, что он может сделать?" — we treat it as already used and go no further. "Чем ему помогает пин код?" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- Val's rule, stated flatly: "1 тикет он всегда оригинальный, 2 же не оригинальный" — the first ticket is always the original, the second one is not [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- Pavel's residual concern was a **different** player being defrauded rather than JVL: the copy-holder loads a machine, plays and cashes out, and then "приходят реальный игрок с реальным тикетом. Поскольку он не защищен." His summary of what the PIN used to do: "раньше мы игрока защитить защищали тем, что он сам вводил защитный код. Без знания которого невозможно было оперировать этим тикетом" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- Pavel also noted the pre-existing physical mitigation: with paper, "оригинальный тикет всегда съедается билаксептором… И его на руках нету" — the original is eaten by the bill acceptor and is no longer in anyone's hands [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## What replaces the PIN as a control

- **Pavel's server-registration idea, accepted by Val.** Embed a **URL to JVL's cloud service inside the QR code**, so scanning it opens the browser at that address plus a code and the transaction registers centrally: "Клаудсервиса… И тем самым мы эту информацию отправляем на наш сервис мы можем регистрировать все… Транзакции все его литы сразу на центральном сервере." Val: "Окей, хорошо" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
  - Limit stated by Pavel: the server can only record that a given amount was loaded onto the wallet at the start — "Мы можем только фиксировать сам факт" — the rest of the history runs through Flex IQ or the Flex Recycler [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
  - A useful by-product: the player can scan the QR at any time and be told the balance. Val: "мы выдаем quode в любой момент ты можешь просканировать этот q своим телефоном, и мы тебе скажем, сколько денег там" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
  - The server can also grant **promo credits per location** — Pavel: "если там начислил $50 давать там $5 например промо, которые можно только проиграть, но невозможно… Снять" (playable only, not withdrawable). Val called this "очень очень важно," and it is one reason the SAS connection is mandatory: without SAS "у нас нету выхода на эти на эти счетчики" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].
- **A local validation server is still required.** Pavel: "у нас должен быть локальный сервер, который по сути работает как… Бэкофис… Чтобы иметь единую систему валидации. Вот этих вот QR кодов," and codes must be non-sequential and specially encoded. Val's reason: "Для Того, чтобы просто не печатали фейковые QR коды" [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]].

## Update — Sept 2 2026: the PIN is kept as an option, not killed

On the [[wiki/meetings/2026-09-02-flex-iq-pre-pilot-updates-after-the-show.md|Sept 2 2026 Flex-IQ pre-pilot call]] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] asked directly whether the PIN theme survives ("у нас [и]лет на… текущей реализации flex[ ]pay было с пин кодом на флекс айкью. Эта тема остаётся[?]"). [[wiki/people/val-levitan.md|Val]] softened the Aug-24 position rather than reversing it [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]:

- **Val: "Я бы пинкод не убивал, но я б[ы] сделал бы как фичер"** — I would not kill the PIN, I would make it a feature. [[wiki/people/pavel.md|Pavel]] supplied the word "Option" and reported [[wiki/people/andrei-klimovich.md|Andrei]]'s written position: "пинкод это опция, которая может включаться для лакейшна или выключаться в зависимости от Того, как захотят операторы" — switchable per location as operators want [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **The default remains PIN-less, and one path is PIN-less by definition.** Andrei: "если [e]оля создаётся на IQ… там кассиром[,] то никакого пинкода здесь быть не может. То есть это уже без пинкодовая система тогда" — a wallet created on IQ by a cashier cannot carry a PIN [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].
- **The hardware cost of keeping the option** is what the Aug-24 ruling had been trying to avoid, and it was re-acknowledged: a PIN forces "тачскрин или какаято физическая панель с кнопками" (Andrei), which erodes the flexibility of the cheap port. Pavel judged a small ~4-inch touchscreen probably cheaper than a button panel. See [[wiki/decisions/2026-09-02-flex-port-sas-universal-with-scanner-touch-vs-non-touch.md]] [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]].

**Net effect:** the trust model and the no-PIN default are unchanged; what changed is that the PIN is no longer removed from the product — it is a per-location switch, and Flex-Port variants must be priced with that in mind.

## Open questions

- Reliable optical read of a QR shown on a phone screen. Val insisted the sensor must read it "100% всегда" despite glare or low screen brightness, comparing it to airport and customs scanners; Pavel thought JVL's existing scanner should manage it if its illumination is switched off — "Главное, чтоб он бликий не создавал" — and Val still asked for "чтото более надёжное," suspecting off-the-shelf solutions already exist. Unresolved — [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Barcode_Receipt_Ewallet_Strategy-September-2-2026.md]]
