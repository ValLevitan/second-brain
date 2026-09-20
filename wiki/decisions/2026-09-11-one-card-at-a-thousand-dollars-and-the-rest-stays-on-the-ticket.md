---
type: decision
title: A payout over the card limit issues one card at $1,000 and leaves the remainder on the player's ticket — splitting across several cards is rejected and parked on MVP 2
date: 2026-09-11
aliases: [one thousand dollars per card, the rest stays on the ticket, split across several cards rejected, split logic out of MVP 1, receipt shows both amounts, five or ten dollar auto-fail, minimum and maximum card limits, second screen removed]
source-count: 4
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

## Update — Sept 14 2026: the other end of the min/max rule is settled

Three days later, at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 8:01 AM use-case call]], Klimovich walked redemption again — "ре[де]мшн… это, собственно, сердце всего этого сейчас процесса" — and closed the **minimum** side that the Sept-11 call had left as rework.

- **The InComm card itself is unchanged in this version:** "[в] этой версии у нас карточка инкомовская[ —] принципиально никаких изменений." What is added is the min/max logic, and it needs a different approach from the one used for MudaGoose: "мы для [MudaGoose] там была одна логика, здесь требуется другой подход" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **Below the floor, nothing happens and MVP 1 offers no fallback.** "[Е]сли у нас на [e-]волите баланс меньш[е,] чем… плюс [activation] fee… сейчас мы ничего с этой транзакцией делать не можем и не хотим. То есть мы сейчас не добавляем в MVP один никаких [lottery] ticket[,] ничего подобного." The flow is blunt: the cashier scans, "IQ прямо скажет, что это нельзя загрузить на карточку[;] он ему вернёт этот тикет[,] скажет[: ] ну иди ещё проиграй или добавь сюда денег" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. *(The transcript drops the word for the minimum itself — Klimovich says "меньший, чем ⟨…⟩ плюс активэйшн фи" — so the floor is recorded as "the card minimum plus the activation fee", which is how the derived notes read it, with the gap noted rather than filled.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- **The $1,000 maximum and the repeat-issuance loop are restated unchanged:** "у нас на карточку $1000 максимальная загрузка[;] то мы можем выпустить одну карточку[,] остаток баланса остаётся на [e-]волите… снова просканировали этот тикет, выпустили ещё одну карточку, и так можно [redeem] весь баланс" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **The play-through rule survives the whole redesign, and it nearly got lost.** [[wiki/people/dmitri-chudinov.md|Chudinov]] flagged that it had not been said out loud: "у нас же остаётся режим[:] деньги на [e-]волет положили, но их надо проиграть, прежде чем вывести." Klimovich had, a minute earlier, implied a player short of the card minimum could simply top up and cash out; he retracted it on the spot — "**не[,] это неправильный комментарий с моей стороны[;] нет, так не должно быть**" — and confirmed the **dual balance stays**: "должен быть… двойной баланс… [deposited] и [playable]", visible everywhere a balance is communicated, including on the cashier's IQ screen: "если мы… кассиру показываем баланс, он должен быть разделён на 2… логические группы" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- Klimovich offered to add a capability for the dual balance so it could not be lost again; [[wiki/people/pavel.md|Pavel]] suggested it may already exist as a requirement inside an existing capability — "это похоже на ре[кваймент] внутри какой[-]то к[а]пбилити существующе[й]… можно поискать" — and Klimovich agreed to search first: "я поищу и добавлю" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Also settled the same morning:** on activating a card, once the card is confirmed active, a receipt prints immediately showing how much was loaded and the fee — "тут же должен быть распечатан [receipt], подтверждающ[ий] эту транзакцию[:] сколько денег загружено, сколько f[ee]" — and a broken or empty printer does **not** block card issue (Biratka asked; Klimovich: "[н]ет, не блокируем") [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**§15.8:** clear — product limits and player flow only; the dollar figures are device/card limits, not anyone's compensation.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
