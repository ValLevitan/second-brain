---
type: decision
title: A wallet balance is three lines everywhere — Total, Playable only, Redeemable — with no separate engineering and player vocabulary; Val declared it an ADR that must live in the repository
date: 2026-09-15
aliases: [balance naming, Total Playable only Redeemable, playable only, playbolo onli, three lines, тотал плейбл онли редимобл, dual balance naming, the balance ADR, ADR in the repo, promo balance parked, promo money to MVP2, withdrawal priority playable first]
source-count: 3
status: active
open-commitments: 1
open-questions: 2
---

# Balance is Total, Playable only and Redeemable — the same three words everywhere

Settled at the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian). Raised by [[wiki/people/alexander-biratka.md|Alexander Biratka]], argued out by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/irina-shishko.md|Irina Shishko]], and closed by [[wiki/people/val-levitan.md|Val Levitan]] naming it an architecture decision on the record.

## The confusion being fixed

Biratka opened it as a naming problem that had already cost him time on his own product: "иногда иногда иногда возникает просто путаница именно возможно в наименовании" — and, concretely, "**я когда делал flex pay, я столкнулся с этой проблемой, что оно путает меня. То есть вроде бы есть какойто плейбол и редибл и мне так хочется их сложить, но по факту нельзя их слаживать**" — a screen showing "playable" and "redeemable" invites you to add them, and you must not, because redeemable money is also playable [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. He confirmed the containment first with Klimovich and Pavel: redeemable money is also playable, "**редима был это не баланс, это часть парт**" — a part, not a balance [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Klimovich's player-side version of the same complaint: "смотрите я как игрок, я как игрок, если я гдето увижу этот баланс, я это сразу понимаю, так что я могу играть только на $10… ну это неправда я играть могу на 60" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The split that was refused

Klimovich's first move was to split the vocabulary in two — "давайте разделим это на 2 логических блока, один это как мы внутри компании во первых разработки и как это в коде фигурирует одна история а 2 история, как это игроку будет доноситься, как это на экране показывается?" Both Val and Biratka refused it in the same breath. Val: "**Но я не я не согласен. Я хотел чтобы это была**…" Biratka: "**Я тоже не согласен, надо чтоб одинаково было**" — it has to be the same everywhere, because the split is exactly what produces the confusion [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Val's own contribution was the third line: "**Почему бы вам не добавить еще 3 линию тогда станет все четко. Добавьте баланс или назовите это то[тал]**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The three lines, and why "only" is load-bearing

- **Total** — everything on the ticket, and the figure the gaming machine shows and loads.
- **Playable only** — the part that cannot yet be withdrawn.
- **Redeemable** — the part that can be taken out.

Klimovich's objection to a bare third line was arithmetic: "тотал будет всегда равняться… плейвел, у нас получится плохая арифметика, то есть у нас тотал 100 плейбл 100, [реди]ма[бл] был 50." Biratka answered it with the word *only*: "**если мы напишем playbolo wonli, тогда тут как раз таки будет не вся сумма**", and Pavel closed it: "**Если мы напишем плей был онли, тогда это будет 3 строчки и плей был онли плюс ре[ди]ма был равно тотал**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Biratka's summary: "плейбол онли плюс резимы был равно тотал всё. **Чётко и красиво**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**The term is not JVL's invention.** Biratka: "**кстати такая же терминология присутствует и в сас спецификации как раз таки там используется playbal only**" — the SAS specification uses "playable only" for exactly this money [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. That sits with the Sept-14 ruling that capabilities are written against the published standard ([[wiki/decisions/2026-09-14-capabilities-are-written-against-the-published-sas-standard.md]]).

*(One Val line in the middle of this exchange — "Нет, нет, нет, он неправильное слово" — is not clearly attached to a specific proposal in the transcript, and is recorded as **unclear** rather than read as an objection to "playable only". He did not re-open the point once the arithmetic was demonstrated.)* [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## How it is shown to the player

Pavel's proposal, accepted: "**Давайте давайте для игрока большими цифрами, большими цифрами, напишем тотал $100 и маленькими снизу playbel on[ly]. [Реди]ма был и всё**" — total in large type, the two components small underneath — "и у игрока не будет вопроса, на какие деньги играть?" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Val declares it an ADR, on the record

"**Это является ad r. Кстати, транскрипт у нас идёт.**" — then, explicitly for the transcript: "Для транскрипта то, что вот последнее решение называется [ADR]… арки[тектурное] решение", and "**и мы в repo должны иметь всегда эй диарс**" — the repository must always hold the ADRs [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. ADRs are an established JVL practice — adopted on every feature in June 2026 and stored per repository under `docs/adr` rather than in Jira ([[wiki/topics/github-release-management-pipeline.md]], Jun-10; see also [[wiki/meetings/2026-03-13-capabilities-requirements-adr-storage.md]]). What is notable here is Val applying it live, naming a conclusion an ADR in the moment and asking the recording to capture it as one. It is the same "if it is not written, it does not exist" pressure he applied at the end of the same meeting — see [[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]].

## Internally, the two balances stay — Chudinov's reason

Chudinov made the engineering case and Klimovich accepted it outright ("Прекрасно. Я поддерживаю"):

- "с нашей стороны с инженерной всё равно остаются плейбл у редимого, потому что есть есть дилеммы. **Откуда брать деньги и куда их возвращать?**"
- "**Мастеру устройства должен понимать, куда эти деньги возвращать, откуда они ушли**" — if $30 is pushed from playable to the Flex-Port and the port refuses it, the engine must know which side to return it to. Otherwise "иначе он попадёт в какойто абстрактный тотал и потом превратиться. Так мы можем их выводить или нет. **Поэтому формально баланса 2**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**Withdrawal priority is playable first, then redeemable.** Chudinov: "Откуда собирайте денежку приоритет 1 плей был деньги плейбл деньги, если их не хватает, начинаем забирать из резимы был, если их вообще суммарно не хватит, тогда отказ". Pavel had put the same rule first: "если ты берёшь, что там говоришь $20, то мы сначала должны забрать из плея был эти деньги" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**How many counters is left slightly ambiguous in the source.** Chudinov says "формально баланса 2"; Irina says "**3 будет счётчика**"; Klimovich, describing the internals, says "тотал внутри нашей всей системы тотал плейбл и redimal". The consistent reading is two stored balances with total as their sum, but the transcript does not state that in one sentence, so the count is recorded as spoken and **not resolved here** [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Biratka pressed separately for the internal database field itself to be named "playable only" and not "playable" — "**для нас, для программистов**" — and Val widened it: "**Нет, а для всех**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The arithmetic, walked aloud and confirmed by the room

Klimovich worked a worked example through and the group answered each step [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

| Event | Total | Playable only | Redeemable |
|---|---|---|---|
| Player loads $20 into an empty wallet | 20 | 20 | 0 |
| Plays it all off; wins and collects $150 | 150 | 0 | 150 |
| Cashier adds $50 at the counter | 200 | 50 | 150 |

The machine reads the ticket and shows **total** at every step — asked "какой мы баланс показываем тотал или плейбл онли?", Biratka and Klimovich both answered "тотал", and at the $200 stage Biratka answered "200 200" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Klimovich's closing line was "Всё, всё всё я спокоен, хорошо… Всё всё отлично. Я понял спасибо."

The derived notes carry the same table and the same three names [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Promotional money — a fourth kind, parked to MVP 2 or 3

Pavel raised it: outside Georgia a ticket already carries two kinds of money, "там какието промо деньги могут начисляться на твой баланс. **И эти промо ты можешь переносить из машины в машину, и они остаются промо они не становятся этими редимой был**" — promo moves machine to machine without ever becoming redeemable [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

Val put a date pressure on it rather than a deferral: "**Андрей климович это в джорджии станет актуальной темой очень, очень скоро**" — because, as Klimovich put it, "уйдут хенды" and, in Irina's words, "прома деньги придут". Val's reason is commercial: "мы [JVL] хочет толкать промо спецификлы, потому что мы пользуемся флекспортом как AFT… Это это точно падает в наш… бизнес план" — JVL intends to push promotional specifics through the Flex-Port acting as an AFT device, and it is in the business plan [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. *(The clause naming who "wants to push" is garbled in the transcript — "мы дев хочет толкать" — so the subject is read as JVL from context and flagged as an inference.)*

Irina drew the line and it held: "**Давайте, если мы хотим до 1 числа и промо деньги нам не до 1 числа, мы это сделаем MVP 2[ или ]3, потому что там всё очень сложно с этим**". Klimovich parked it — "Согласен, спасибо Ирина, давайте припаркуем эту тему. Это очень хорошая, важная тема, но она не поможет нам 1 октября релизи[ться]" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. The October-1 date is [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]].

Whether promo is a separate balance type or only a protocol flag was argued and not settled — Klimovich: "это скорее создаёт дополнительный тип баланса… это отдельный промо баланс"; Biratka: "**он не добавляет новый тип денег**… он требует у нас в протоколе продолжать держать этот… баланс как тип баланса в протоколе" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Relationship to what the corpus already held

The dual-counter fact is not new — the Aug-2025 CMS block-diagram document already recorded that the e-wallet ticket carries two counters, playable-only and redeemable [[raw/CMS- Block Diagram_Arch 082225.md]] (see [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Aug-20 2025). What Sept 15 adds is (a) **Total** as a named, displayed third line, (b) the rule that there is no separate internal vocabulary, and (c) the ADR obligation. It also discharges the Sept-14 commitment to get the dual-balance logic into the capabilities — see [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]] for the neighbouring capability bookkeeping.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — record the Total / Playable only / Redeemable naming as an ADR in the repository — due unspecified; Val named it an architecture decision on the call and asked the transcript to capture it — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Two stored counters or three?** Chudinov says "формально баланса 2", Irina says "3 будет счётчика", Klimovich describes three inside the system. Not reconciled on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **Is promotional money a third balance type or only a protocol flag?** Klimovich says a separate promo balance; Biratka says no new money type, only a balance type that has to stay in the protocol. Parked with the whole promo topic — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — product and money-flow design only. The dollar figures on this page are illustrative player balances walked through on a whiteboard, not anyone's pay; nothing was excluded on compensation grounds.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/CMS- Block Diagram_Arch 082225.md]]
