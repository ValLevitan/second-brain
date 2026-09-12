---
type: decision
title: A payout over the card limit issues one card at $1,000 and leaves the remainder on the player's ticket — splitting across several cards is rejected and parked on MVP 2
date: 2026-09-11
aliases: [one thousand dollars per card, the rest stays on the ticket, split across several cards rejected, split logic out of MVP 1, receipt shows both amounts, five or ten dollar auto-fail, minimum and maximum card limits, second screen removed]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# One card at $1,000, and the remainder stays on the ticket

Settled at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]]. [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] proposed splitting a payout across several cards, [[wiki/people/val-levitan.md|Val]] visibly disagreed, and [[wiki/people/pavel.md|Pavel Frolov]]'s simpler answer was adopted.

## The limits as they stand today

- **A minimum that auto-fails, inherited from the old integration and now broken.** Klimovich: "Смута гос[]интеграция. Если мы получаем транзакцию меньше там $5 там по моему или 10, то она у нас автофейл… [с] портал[ом] это уже не работает, логика[,] её надо пересмотреть" — a transaction under about $5 or $10 auto-fails, which does not work with the portal and has to be revisited. He took the rework on himself [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. *("Смута гос" is left exactly as transcribed. It is plausibly the same MudaGoose garble family this session produces elsewhere as "мутагуз / мудагуз", but the source does not say so and it is not asserted here.)*
- **A maximum of $1,000 per card.** "[М]аксимальн[ое] ограничени[е] у нас $1000 на карточку" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The proposal that lost

Klimovich: "мы в рамках интеграции смутого думали вводить такой функционал, как httpay, но мне кажется, сейчас, когда у нас вся экосистема в наших руках[,] мы можем просто сделать сплит[ —] то есть если pay больше 1000, мы сплитаем на несколько карточек." He then read the room himself: "[н]у[,] я вижу[,] вал[,] вал не согласен" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. *("httpay" is the transcript's rendering of whatever the older feature was called; unclear, and not guessed at here.)*

## The answer that was adopted

> **Pavel:** "[Д]аже есть ещё проще решения[:] игрок приходит, он хочет получить карточку[ —] мы выпускаем на тысячу, всё остальное остаётся на его тикете[;] он хочет[ —] может идти и продолжать играть… [е]сли нет[ —] ещё раз поднесёт[,] ещё раз карточку выпустит."

[[wiki/people/irina-shishko.md|Irina Shishko]]'s condition — "но… ему нужно об этом сообщить" — was accepted as obvious ("ну[,] естественно"). [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] pointed out that on FlexPay the cashier drives it, so it is a dialogue: "[на] флекс[пей] это делает кассир, поэтому там просто диалог произойдёт[:] вам на карточку максимум можно [1000,] остальное выводим на следующую или оставляем" *(the transcript renders the figure in this one line as "2000"; the limit is stated as $1,000 twice elsewhere in the same session, so this is recorded as a likely transcription slip and is not reconciled anywhere in the source)* [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Klimovich then confirmed the full flow, and it needs no new logic:**

> "Мы берём тысячу, отправляем на карточку, остальное остаётся на [и]волите. После успешной активации карточки у нас уже есть логика, что мы печатаем ре[си]т[;] на реси[те] указано, сколько денег ушло на карточку и сколько у тебя осталось на [и]волите[;] кассир отдаёт обратно человеку [ре]сит и карточку и его [и]волит… [с]канируем, снова выпускаем следующую кар[т]очку." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## The split logic comes out of MVP 1

Klimovich: "там есть кусок логики про сплит[ —] я бы выкинул… сейчас из [MVP] 1[;] я думаю, что нам не нужно для 1 октября эта логика. Ты можешь его пока на [MV]P 2 поставить[,] и то не факт, что он пойдёт в M[VP] 2" — parked on MVP 2 with open doubt it belongs there either [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Notably, the split is not being dropped for cost.** Chudinov said it is already built — "[ф]ормально он реализован[,] он уже готов[;] нам ничего не стоит этого сделать, ну чуть экран… причесать, чтоб кассиру было понятнее" — with Pavel confirming it is not a bottleneck, back end done and front end done, "[В]ладимир сейчас причесывает все экраны" *([[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] by context — the Minsk React developer who owns the screens)*. Klimovich kept it on MVP 2 anyway, as the first candidate to add back if October 1 arrives with everything else finished: "если случится чудо[,] у нас всё готово [MV]P один и у нас ещё 1 октября не наступило, и мы захотим что[-]то ещё добавить[ —] вот кандидат на добавление" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The second screen is going away

Chudinov checked that the player-confirmation screen had been removed but the second screen was still showing the payout; Klimovich: "не надо[,] мы уберём 2 экран, мы уже работаем над этим" — already under way. [[wiki/people/andrey-bosik.md|Andrey Bosik]] suggested the retail-cashier pattern instead — a prompt on the cashier's own screen telling them what to say to the player, "как… в магазинах, когда кассир пробивает товар… там у него прям пишется[:] скажите спасибо за покупку" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## One carrier per wallet becomes a regulation, not a capability

A capability nobody could place — Pavel read it as "carrier… wallet cred[ential]" and said "мне в голову не лезет этот [кейпа]билити" — turned out to describe the rule that a wallet's carrier exists in exactly one copy: Klimovich, "здесь описана логика[,] что… carri[er] для кошелька существует только в одном… экземпляре." Irina glossed it as "один кошелёк, один… печатный [билет]". **Val ruled it belongs in the regulation:** "я думаю, что это должно быть частью регламента", and Klimovich took it: "давайте я помещу это 163… 163 кап[;] я его в [регламент] превращу" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. This is the same principle as the general rule settled the same morning on [[wiki/decisions/2026-09-11-acceptance-criteria-live-in-the-regulations-not-the-capabilities.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — rework the minimum/maximum card-limit logic for Flex IQ, because the under-$5-or-$10 auto-fail inherited from the old integration does not work with the portal — due unspecified, described as needed quickly — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — convert capability 163 (one carrier per wallet) into a regulation — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **Does the split-payout logic belong in MVP 2 at all?** Klimovich parked it there while saying it may not go there either — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The derived notes record the same outcome and the same $1,000 figure — "issue the card for $1,000 and leave the remainder on the player's ticket" — with the split "pulled out of MVP1 onto MVP2".)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — product limits and player flow only; the dollar figures are device/card limits, not anyone's compensation.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
