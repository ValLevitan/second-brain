---
type: decision
title: A collect timeout must never destroy the player's money — it goes to unclaimed money, built as a wallet that is created and funded but never printed; the specification to work from is AFT plus state banking law, starting with Juan Martinez and then GLI, and none of it is in MVP 1
date: 2026-09-15
aliases: [unclaimed money, anklaim money, анклейм мани, timeout money evaporates, money never lost, wallet without printing, unclaimed wallet, AFT specification, GLI consulting fee, деньги испаряются, escheatment]
source-count: 3
status: active
open-commitments: 2
open-questions: 3
---

# A timeout sends the money to unclaimed money — the player never loses it

Settled at the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian). Triggered by a question from [[wiki/people/alexander-biratka.md|Alexander Biratka]], answered by [[wiki/people/val-levitan.md|Val Levitan]] as an absolute, and then routed by Val out of the room entirely.

## The finding that started it

[[wiki/people/andrei-klimovich.md|Klimovich]] had tested the current behaviour himself the day before. Asked by Biratka what happens when the collect timeout expires: "**вчера я протестировал этот кейс на текущих [Flex-Порт]ах, и у нас происходит то, что деньги… испаряются**" — the money evaporates. [[wiki/people/irina-shishko.md|Irina]]: "исчезают в никуда" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The measured length of that timeout — "сейчас он что то в районе 30 секунд, то всё потом эти деньги исчезают" — Klimovich had already reported the previous day [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]; see [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]].

Klimovich framed his own answer as a preference: "блин, ну как из гуманистических соображений? Я бы хотел, чтобы игрок эти деньги не потерял, но я думаю, что…" Val did not let him finish [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **Нет, нет, нет, нет, нет, простите. Простите, игрок никогда не может потерять свои деньги[ —] невозможно[,] нельзя.**

## The rule

- **A timeout hands the funds to unclaimed money, not to nobody.** Val: "тогда происходит таймаут, и эти деньги идут в анклейм[ные]" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Unclaimed money is a regulated item, per state.** Val: "**в каждом штате есть свои… банковский регулейшенс[ — ]когда эти деньги можно экспро[приировать]. И причем некоторые Штаты требуют налог за анклей[м] мани**" — each state has its own banking regulations on when such funds may be expropriated, and some states tax them [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].
- **Chudinov supplied the framing Val was answering:** the player has actively made an effort *not* to take the money — "игрок сделал усилие, чтобы не забрать[ —] что делать с этими средствами" — and recalled JVL having done unclaimed-money work before without being able to place the country: "у нас была задача, я только не помню, на какой стране сделали" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The implementation shape — a wallet that is never printed

Biratka's proposal, which Pavel and Irina immediately recognised as almost-existing behaviour ("Это так[ ]ча[стично] сделано" / "Ну так и будет"):

> "**Мы можем создать пустой е[в]олет, перевести на него деньги и пометить его как [unclaimed]**… мы его создаем виртуально[,] в базе данных он существует, его можно посмотреть там, в какомто списке [unclaimed money]… но мы его просто не печатаем. **То есть это будет по факту то же самое, что человек нажал… кнопку нью[ ти]кет[ —] только без печати тикета**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

His reason for wanting a real wallet rather than a bare ledger entry is that a transfer has to be a transaction: "нам же надо всё равно транзакцию сделать… идёт перевод денег с флек[спорта] на е[в]олет" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**Chudinov dissented and the dissent stands.** He would rather it were not a wallet at all: "я м[ог] бы всё-таки делал это не как [е]волят, а как отдельн[ую] сущность, как баланс, потому что на следующ[ий] [MVP] у нас появится [cloud] волет и с этими деньгами потом… реально надо будет больше сложностей" — the cloud wallet arriving in the next MVP makes wallets the harder object to carry this on [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. That is the [[wiki/decisions/2026-09-02-e-wallets-move-to-the-cloud.md|cloud-wallet]] move he is protecting against.

Klimovich's own open questions on the wallet route, left unanswered: how long such a wallet must live ("возможно, там требование будет не 30 дней, а дефолтных, а может продолж[ать] дольше существовать") and who has access to it [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The 30-day default is [[wiki/decisions/2026-09-14-ewallet-ttl-defaults-to-thirty-days-and-is-set-per-location.md]].

## Val stops the design debate and names the sources

> **Да друзья, послушайте, вы сейчас тратите время на то, что уже давно разработано без нас.**

His routing [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

1. **[[wiki/people/juan-martinez.md|Juan Martinez]] first, because he costs nothing.** "Есть 2 [source]а знаний, один это хуан, я бы начал бы с него[,] нам ничего не стоит." Klimovich accepted it as his own action the same day: "я обязательно этот сегодня же поговорю с хуаном". *(Val's first rendering of the name in the transcript is "Иваном"; Klimovich's reply and Val's own later references are "хуан", and the regulatory-question-list role matches Juan Martinez, so it is resolved to him — see [[wiki/people/juan-martinez.md]].)*
2. **Then [[wiki/organizations/gli.md|GLI]], as a paid consultation.** "Если хуан не сможет этот разговор поддержать… то тогда Павел[,] назначьте встречу с [GLI], они с нас возьмут консалтинг фи[з]. Или даже напишите им." Same paid-consultation route as [[wiki/decisions/2026-09-11-the-game-change-question-goes-to-gli-as-a-paid-consultation.md]].
3. **The specification is AFT, not Class B.** Pavel suggested taking the GLI specification "для класс[а]… класс би"; Val corrected him: "**Класс би нет, это нет, это нужно брать спецификацию на AFT. [AFT] покрывает все эти транзакции**", plus "можно взять ещё разных Штатов legislat[ion], которые говорят, что делать с [unclaimed] ма[ни] — это банковские ри[гу]лейт[ions]". He added that it is obtainable immediately and can be handed to Claude: "Это мы можем получить прямо сейчас. Это мы можем отдать [Клод]у."

Pavel also offered a market data point Val rejected: that casinos collect unclaimed money for a month and then must hand it back to other players as bonuses. Val: "это не так. Это… только джекпот касается" — that rule is about jackpots, not unclaimed money [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Explicitly out of MVP 1

Klimovich asked for the release disclaimer directly — "окей[,] ли нам, если это не будет реализовано в рамках MVP один[,] готовы ли мы зарелизи[ться]?" Val, without hesitation: "**Конечно, конечно, конечно, конечно, никаких проблем в этом нету, но это должно быть сделано… Скоро. Я не знаю [MVP] 2 и [MVP] 3[,] но де[фи]н[итли] это [не] MVP один**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. He then closed the topic: "Все на этом… я хочу эти дебаты закрыть, идём дальше."

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — speak to [[wiki/people/juan-martinez.md|Juan Martinez]] about unclaimed money: where the entity lives, who is obliged to create and hold it, and who owns the balance — due the same day (Sept 15 2026); "я обязательно этот сегодня же поговорю с хуаном" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — book a meeting with [[wiki/organizations/gli.md|GLI]] on unclaimed money if Juan cannot cover it, accepting a consulting fee — due after Klimovich's call with Juan — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Where the unclaimed-money entity lives and who owns the balance.** Klimovich asked whether JVL is obliged to create and hold it, and whose money it then is — "не [JVL] же принадлежит, он принадлежит лакейшн". Val did not know: "или оператору, или GLC, или лакейши[ну], или налоговой[,] но неважно… я говорю, кто должен держать это?" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **Wallet or separate entity?** Biratka's create-fund-mark-do-not-print wallet is the simpler route; Chudinov wants a separate entity because the cloud wallet lands in the next MVP. Unresolved — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **One unclaimed wallet updated forever, or a new one per event?** Klimovich raised it; Biratka guessed a new one each time, "только он должен какого-то определённого типа быть". Not settled — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — regulatory and money-flow design only. No named person's pay, rate or performance judgement appears in either source; nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
