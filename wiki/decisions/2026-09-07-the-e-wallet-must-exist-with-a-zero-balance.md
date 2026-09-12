---
type: decision
title: The e-wallet must be able to exist with a zero balance — which turns it into a player card, gives it a per-location lifetime, and changes the ticket to say "come back tomorrow with the same ticket"
date: 2026-09-07
aliases: [zero-balance wallet, empty wallet, wallet is a player card, wallet lifetime configurable, 30 60 90 days, immortal wallet, amount-agnostic ticket, blocking the start of play, the most sacred moment, life will tell]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# The e-wallet must be able to exist with a zero balance

Settled at the [[wiki/meetings/2026-09-07-gacs-show-setup-flex-iq-flex-ports-and-the-e-wallet.md|Sept 7 2026 8:00 AM call]] (Russian). [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] put it as the hinge the whole flow turns on: "чтобы это всё работало, один такой логический вопрос[:] что [и]воля[т] должен существовать с балансом ноль? Если да, тогда всё вот это всё соединяется и всё работает" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## The case that forced it

[[wiki/people/irina-shishko.md|Irina Shishko]] asked about the player who skips the counter: "а если игрок сразу подошёл к машине, поиграл и хочет вывести[,] у него нет ничего на руках[?]" Klimovich first called it a limitation, then corrected himself — "нет, это не ограничение. Это нюанс нашей всей системы" — and described the fallback: the player walks back to the cashier, asks for an empty ticket, and returns to collect [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. This is the same gap first identified in April 2025 as the "no-value wallet" scope gap on [[wiki/topics/flexpay-business-architecture-payout-devices.md]].

## What was decided

- **The wallet can exist empty, and the group concluded it must.** Klimovich, summarising to Val: "Мы сейчас обсуждали вопрос по поводу существования [и]волета с нулевым балансом, что может ли он существовать[,] и пришли к выводу, что да, нам это нужно" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **That makes it the equivalent of a player card.** "По сути дела, наш [и]волет становится аналогом [аксиос] плеер card." *(The brand word is garbled in the transcript as "аксиос"; the derived notes read it as an **Aristocrat**-style player card. Recorded as read by the notes, not asserted from the transcript.)* [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Wallet lifetime becomes a per-location configurable parameter.** The Georgia norm Klimovich has observed: "обычно локации[,] всё, что я видел[,] есть здесь, в Джорджии[ —] они дают 30 дней[,] срок жизни тито тикета," and he sees no problem making it configurable: "[Ло]кация захочет, чтобы у него тикет жил 60 дней[,] 90 дней — это их право." He added that the wallet could go further: "[и]воля[т] вообще можно… бессмертным сделать" — made immortal [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **The ticket design changes to say so plainly.** "Поменять дизайн немного тикета[ —] мы можем прямо откровенно писать[:] [сохраните] этот билет[,] приходите играть завтра с этим же билетом" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].
- **No amounts are printed — the wallet is amount-agnostic.** Chudinov checked it — "так не пишем никакие суммы, ничего[?]" — and both Klimovich and Pavel answered "Нет"; Klimovich: "Они у нас… агн[о]стические в этом плане" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]. This restates the April-2025 rule already on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] that no value is printed on the ticket.
- **Blocking the start of play is a strategy question, not a technical limit.** [[wiki/people/pavel.md|Pavel Frolov]] settled the mechanics: "мы можем по [SAS] запретить [билл-акцептор]," and argued the SAS route is the better one anyway — "если мы уже [идём по SAS], то нам не нужно прямое подключение порт[а к] б[ил]лакцептор[у;] у нас гораздо более надёжно… мы по [SAS] можем сказать[:] б[ил]лакцептор[,] отключись, или б[ил]лакцептор[,] включись." Val accepted the conclusion: "значит[,] это не является лимит[ирующим] фактором… стратегическое решение начинать игру без [e-wallet]… это просто стратегия, это не технологическая лимит[ация]" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]].

## Val challenged it hard and then declined to block it

This is the longest argument in the meeting, and it is worth keeping in full because Val ends it by refusing to rule.

- **His question, asked four or five times:** "почему вы разрешаете, чтоб он начинал игру без [и]волета? В чём логика?… Почему мы не контролируем? Почему вы пришли к такому мнению?" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **His argument:** "Если вы разрешите это делать, то это будет так всегда, а если вы один раз не разрешите, то вы всегда научите [локации], как правильно делать. **Я не настаиваю ни на одном, ни на другом, потому что я не знаю, как сделать правильно.** Но есть большие минусы в том, чтобы разрешить игроку подойти к машине без [и]волета." He added that the habit argument cuts both ways, because the whole transaction system in Georgia is changing anyway: "не забудьте, что вся система транзакций сейчас на лок[ациях] меняется. И в Джорджии люди… поменяют свою привычку[,] как они получают деньги" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Klimovich's rebuttal, which Val accepted as serious:** "ни одно решение на рынке, что мы видели сейчас[,] с игровыми карточками[,] player card… или другие решения[,] они не блокируют старт игры[.] Это самое святое[:] я пришёл, хочу расстаться со своими деньгами[,] и вы меня блокируете… если мы сейчас хотим так кардинально поменять привычку игроков, что вы не можете начать играть на машине, пока не предъявите [и]волят…" Val: "В этом есть серьёзная мысль. Я не сказал, что так не надо делать. Я просто пытаюсь понять, правильно ли так делать… я понимаю, что это святая функция[ —] дать игроку ставить деньги" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **How he left it:** "это жизнь подскажет[.] Если мы это сделаем в [settings], то… жизнь подскажет, как правильно сделать. Поэтому я не очень сильно волнуюсь за решени[е]" — the same "жизнь подскажет" move he made on the QA question six days earlier ([[wiki/decisions/2026-09-01-freeze-existing-manual-test-cases.md]]) [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- **Two mitigations were named and not decided.** Pavel: show a message on the Flex-Port when real money goes into the acceptor — "вам для того, чтобы забрать выигрыш[,] понадобится [и]воле[т]… отобразить 5 секунд и забыть про это" — which Val dismissed ("Никто не будет [это смотреть]"); Klimovich wanted the moment moved to the collect press instead. And Pavel gave the everyday case for allowing it: a player arrives with last week's wallet in his pocket and simply wants to feed in $50 — "Пожалуйста, засовывай[,] и потом используй свой же [и]воле[т] для выигрыша" [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

## Open questions

- Whether allowing play to start without a wallet is the right strategy. Val said explicitly that he does not know and is not insisting either way, and expects the setting to answer it in the field. **Unresolved by design** — [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]] [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]

**§15.8:** clear — product flow and player behaviour only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
- [[raw/Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026.md]]
