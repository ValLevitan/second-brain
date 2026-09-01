---
type: decision
title: Drop the PIN code from the eVoucher flow — a QR voucher is trusted the same way a TITO ticket is
date: 2026-08-24
aliases: [drop the PIN, eVoucher without PIN, no PIN code voucher, TITO trust model, QR voucher security]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# Drop the PIN code from the eVoucher flow

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

## Open questions

- Reliable optical read of a QR shown on a phone screen. Val insisted the sensor must read it "100% всегда" despite glare or low screen brightness, comparing it to airport and customs scanners; Pavel thought JVL's existing scanner should manage it if its illumination is switched off — "Главное, чтоб он бликий не создавал" — and Val still asked for "чтото более надёжное," suspecting off-the-shelf solutions already exist. Unresolved — [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]

## Sources
- [[raw/Meeting_Notes_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Design-August-24-2026.md]]
