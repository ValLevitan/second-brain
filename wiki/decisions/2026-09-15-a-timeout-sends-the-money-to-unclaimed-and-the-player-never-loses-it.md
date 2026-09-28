---
type: decision
title: A collect timeout must never destroy the player's money — it goes to unclaimed money, built as a wallet that is created and funded but never printed; the specification to work from is AFT plus state banking law, starting with Juan Martinez and then GLI, and none of it is in MVP 1
date: 2026-09-15
aliases: [unclaimed money, anklaim money, анклейм мани, timeout money evaporates, money never lost, wallet without printing, unclaimed wallet, AFT specification, GLI consulting fee, деньги испаряются, escheatment, requirement 1430, unconfirmed money, анконференд мани]
source-count: 8
status: active
open-commitments: 3
open-questions: 5
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

## Update, Sept 16 2026 — requirement 1430, and an unresolved word

The last item of the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]] was [[wiki/people/dmitri-chudinov.md|Chudinov]] pointing [[wiki/people/andrei-klimovich.md|Klimovich]] at a requirement that had been closed off the wrong capability: "Андрей[,] помет[ь] еще одно требование… не из этой [ка]п[а]бил[ити;] это **14[ ]30**[ —] это про [анконференд] мани, котор[ое] мы вчера обсуждали, и ты там говорил, что создашь [ка]п[а]бил[ити] под неё[ —] вот это требование к ней будет". Klimovich: "14[ ]30[,] хорошо[,] я гляну" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Which money he means is genuinely unclear and is not resolved here.** The transcript renders the term "анконференд мани" — phonetically *unconfirmed* money — whereas the Sept-15 subject of this page is rendered throughout as "анклейм/анклейд/онклайнт мани", *unclaimed* money. The derived notes read 1430 as **unconfirmed** money [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Two things argue each way: Chudinov ties it to "what we discussed yesterday", which on this page is unclaimed money; but the Sept-15 transcript contains **no** promise by Klimovich to create a capability for unclaimed money, and the Sept-16 call did settle a separate *pending / unconfirmed* transaction state for a silent InComm answer ([[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]]). Recorded as unclear rather than assigned.

## Update, Sept 17 2026 — the Georgia rule, as a master licensee states it

Two days later a customer supplied the state-law half Val had named. At the [[wiki/meetings/2026-09-17-dynamic-gaming-georgia-master-licensee-and-cashless-pitch.md|Dynamic Gaming meeting]] the visiting master of [[wiki/organizations/dynamic-gaming.md|Dynamic Gaming]] set it out. **This is one operator's account, not the statute, and he was unsure of the period himself.** [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]

- **The store owner holds and reports it.** "**Once there is an unclaimed fund, you have to report on your tax return as a store owner. That's my obligation.**" And: "**If he walks out without paying the twenty dollars, you are liable to pay the state of Georgia the twenty dollars as an unclaimed fund.**"
- **Seven years, then reporting is mandatory.** "**They can do it before, but after seven years, it's mandatory**" — but also "**Five years or seven years? Just need to confirm that.**"
- **No dormancy fee and no service fee:** "**there shouldn't be any dormancy on that. There shouldn't be any service fee on that, as per law.**"
- **Two ways to settle it.** "**Either he keeps forty-three point five percent, give thirteen percent to Georgia Lottery, and give forty-three point five percent to Masters**… **Or he can keep the profit hundred percent, but he has to show that I claim this as an unclaimed funds**", and pay tax on it.
- **What JVL's side said it keeps.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "**In the clouds, there is a record created**… **So we have the track and all the records**", and for "**reporting to a regulatory… or unclaimed funds, you get this report.**" [[wiki/people/val-levitan.md|Val]] called the expiry setting "**a hole in our… design**" — see [[wiki/decisions/2026-09-14-ewallet-ttl-defaults-to-thirty-days-and-is-set-per-location.md]] (Sept 17).

**What this does to the open question below.** It gives one answer to "who must hold it" — the **location (store owner)** — from a customer's mouth. It does not replace the routing to [[wiki/people/juan-martinez.md|Juan Martinez]] and GLI; nothing here says that call happened. The owner question stays open.

## Update, Sept 21 2026 — unclaimed turns up inside the MVP 1 screen walk

On the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 call]], the port's answer to a failed print was to send the money to unclaimed and let the cashier print it from there — Pavel: "в любом случае, где мы не можем перечислить деньги на его лет на порте мы это всё скидываем в анклейт, а из анклейт уже может напечатать кассир"; Chudinov: "Да, согласен" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. See [[wiki/decisions/2026-09-21-at-the-counter-no-printer-no-wallet-at-the-port-the-wallet-goes-to-unclaimed.md]]. **Nobody said whether this puts any part of the unclaimed handling into MVP 1**, against Val's Sept-15 "definitely not MVP 1". Recorded as an open question, not as a contradiction: the Sept-15 ruling was about the regulated side (who holds the money, state law), and the Sept-21 point is a screen the cashier prints from.

## Update, Sept 24 2026 — Val questions the 30 seconds, and MVP 1 only keeps the money

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- **Val asked why a working Flex-Port sends money to unclaimed after 30 seconds.** "вы дали ему 30 секунд, если 30 секунд прошло и он… не знает, что ему делать, то его деньги исчезли." He asked for a PIN, as with an AFT card, so the money stays tied to the player. Pavel: SAS allows about 8 seconds on the machine, after which the money must move and the port be freed. Klimovich: money on the Flex-Port is not tied to any wallet; tying it means a real player account. He said the wait could be one minute instead of 30 seconds.
- **The rule of this page held.** Klimovich: the money falls into unclaimed "чтобы не было пропавших вообще денег они сохранены, пока непонятно, чьи они."
- **Nothing to process it in MVP 1.** Klimovich: "даже в [MVP] один мы не предлагаем никаких экшнов сейчас даже для обработки… Наша задача пока сохранять эти деньги." What a cashier may do with it — Pavel's nearest-wallet match, Val's PIN, Khamin's replay — goes to MVP 2; Val: "Андрей прав, мы это сейчас не поднимем." See [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]].
- **Two new routes into unclaimed.** A Flex-Port that dies holding money sends it to unclaimed when it comes back (bug 349). A Flex-Port with no gateway link does not take the money at all (bug 354). Same page.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — check requirement 1430 ("unconfirmed money" as the transcript renders it) and attach it to the capability created for it — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — speak to [[wiki/people/juan-martinez.md|Juan Martinez]] about unclaimed money: where the entity lives, who is obliged to create and hold it, and who owns the balance — due the same day (Sept 15 2026); "я обязательно этот сегодня же поговорю с хуаном" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — book a meeting with [[wiki/organizations/gli.md|GLI]] on unclaimed money if Juan cannot cover it, accepting a consulting fee — due after Klimovich's call with Juan — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Is the Sept-21 "print from unclaimed" path part of MVP 1?** Designed in the MVP 1 screen walk; its release is not stated — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]] *(Sept 24: Klimovich said MVP 1 offers no actions for processing unclaimed money, and the cashier gets no way to move it. Whether that covers printing from unclaimed was not said — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]])*
- **Where the unclaimed-money entity lives and who owns the balance.** Klimovich asked whether JVL is obliged to create and hold it, and whose money it then is — "не [JVL] же принадлежит, он принадлежит лакейшн". Val did not know: "или оператору, или GLC, или лакейши[ну], или налоговой[,] но неважно… я говорю, кто должен держать это?" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] *(Sept 17: a Georgia master says the store owner holds it and reports it on his tax return, with a 43.5 / 13 / 43.5 split or 100% kept and taxed — one operator's account, unverified.)* [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]
- **Wallet or separate entity?** Biratka's create-fund-mark-do-not-print wallet is the simpler route; Chudinov wants a separate entity because the cloud wallet lands in the next MVP. Unresolved — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **Is requirement 1430 about unclaimed money or unconfirmed money?** The Sept-16 transcript renders it "анконференд мани" while tying it to the previous day's discussion; the corpus does not settle which topic it belongs to — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- **One unclaimed wallet updated forever, or a new one per event?** Klimovich raised it; Biratka guessed a new one each time, "только он должен какого-то определённого типа быть". Not settled — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — regulatory and money-flow design only. No named person's pay, rate or performance judgement appears in either source; nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
