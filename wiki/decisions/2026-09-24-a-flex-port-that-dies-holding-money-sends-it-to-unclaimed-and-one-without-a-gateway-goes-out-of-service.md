---
type: decision
title: Two lost-money bugs get simple MVP 1 rules — a Flex-Port that dies while holding money keeps the transaction and sends it to unclaimed when it comes back; a Flex-Port with no gateway link goes out of service and the money stays on the machine; what a cashier may do with unclaimed money is moved to MVP 2
date: 2026-09-24
aliases: [bug 349, bug 354, 349 баг, 354 бак, Flex-Port dies holding money, Flex-Port reboot money lost, power loss on the Flex-Port, quick blink, быстрый блинк, clever cashier, хитрый кассир, no gateway no collect, Flex-Port out of service without gateway, cashier redirect of unclaimed money, unclaimed handling MVP 2, nearest wallet matching, PIN-bound wallet idea]
source-count: 8
status: active
open-commitments: 4
open-questions: 4
---

# Two lost-money bugs get simple MVP 1 rules

Ruled on the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM MVP 1 call]] (Russian). [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] brought the two bugs as product owner. He called the five lost-money bugs "очень хорошие баги классные", because they tell the product team early what to change in the requirements [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. These are two of the lost-money Flex-Port bugs that were sent to capability 231 on Sept 23 ([[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]]) — that 349 and 354 are among those five is an **inference**; no source lists the five numbers.

## Bug 349 — the Flex-Port dies while it holds the money

**The case.** The player collects. The money leaves the game machine and sits on the Flex-Port, which waits for a ticket scan or a new wallet. Then the Flex-Port reboots or loses power and comes back. Klimovich: "судя по всему, деньги у нас теряются в этот момент. Но у нас такая логика нигде не была описана" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**The argument.**

- [[wiki/people/dmitri-chudinov.md|Chudinov]] (label "Dzmitry Chudzinau"): the money is unconfirmed, because nobody knows how long the power was off — "Может он на следующий день поднялся, может его увезли в are house". He first offered a time rule: if little time has passed, show the scan screen again; anything longer goes to unclaimed [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- [[wiki/people/irina-shishko.md|Irina Shishko]] asked why a player still standing at the port cannot scan his ticket [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- [[wiki/people/pavel.md|Pavel Frolov]]: after a restart, continue the timeout, or start the minute again [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- Chudinov showed the risk: a player collects, "я в это время там гашу", the player leaves, and "я подхожу на включённую машину и забираю его коллег себе. Как хитрый кассир." Pavel and Klimovich both called it a good case. [[wiki/people/ivan.md|Ivan]] added that machines and Flex-Ports start up at different speeds [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- Klimovich asked whether the pending transaction survives in the Flex-Port's own memory. [[wiki/people/alexei-khamin.md|Khamin]] doubted it is built that way today, and Irina said "Оно нереализовано сейчас". Chudinov set the expectation: "как минимум транзакция должна сохраниться и не потеряться" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**The rule (Klimovich, agreed by Pavel and Chudinov).** "Давайте простую какуюто логику… пока примем… потом будем наблюдать в реальности". The transaction is saved locally on the Flex-Port. When the port comes back and can reach a gateway, the money goes to unclaimed automatically — "как Только этот порт получит возможность для этого, то есть он будет подключён к какомуто гейтвейю". No dialog is offered to the player, "даже если это секундный какойто, блинк". Pavel: "Да". Chudinov: "Да" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. His summary at the end: "в момент его возвращения к жизни он сразу же старается эти деньги отдать через гей и создать их в банклейнт" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

## Bug 354 — the Flex-Port loses its gateway link

**The proposal (Klimovich).** If the Flex-Port has no link to the gateway, "[п]орт считается нефункционален, он не должен позволить… [в]ыводить деньги". He explained why this link is special: today the port-to-gateway link is cabled — "У нас прям кабели проложены" — while the gateway itself may lose the internet, and that is fine: "gatway, пока он связан с партом, должен позволить эти деньги выводить и создавать валюты" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**The alternative he put up himself** — take the money anyway, keep it in the port's memory, and retry the gateway later. Pavel: then it goes to unclaimed, and the player cannot use it and has to argue with the cashier — "Поэтому лучше на машине оставить." Chudinov: for a player "это уже сложно, он же не знает вся этой кухни." Pavel also floated letting the player choose, and asked whether that is worth the complexity [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**The rule.** No gateway link → the Flex-Port goes out of service with a message, collect is not allowed, and the money stays on the machine. Pavel: "Я согласен, лучше пусть на машине остаются и деньги." Klimovich asked for objections; Chudinov: "Нет, нет… В целом согласен." Klimovich's summary: "мы не разрешаем пользоваться фэкспортом, если… нету установленной связи с гитвей" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. Chudinov expects the unclaimed statistics to show how often the Bug-349 case really happens [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

## Val challenges the 30-second timeout, and cashier handling goes to MVP 2

**Val's challenge.** [[wiki/people/val-levitan.md|Val]] asked why a fully working Flex-Port sends money to unclaimed after 30 seconds: "флек абсолютно работающий флегспорт. Полностью функционирует, но деньги ушли." His scenario: a friend walks up, the player turns, "Прошло 30 секунд, он смотрит на это, а где мои деньги?" He asked for a PIN, as with an AFT card, so the money stays tied to the player: "может быть, нам нужно оставить пин код" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. *(A PIN was taken out of MVP 1 for Flex IQ on Sept 11 — [[wiki/decisions/2026-09-11-mvp1-boundary-bill-escrow-and-pin-out-remote-update-and-master-device-in.md]]. Val's idea did not reopen that.)*

**The engineers' answers.**

- Pavel: SAS gives about 8 seconds in which the money may stay on the machine, "[п]о спецификации сас"; after that it must move, and the port must be freed — "мы должны освободить машину… Мы не знаем, игрок ушёл или отвлекся" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- Klimovich: money leaving a machine is not tied to any wallet — "они уволят агностик". Tying it to a player means registering a player session, which is "настоящий плеер аккаунт, который надо менеджрить, верифицировать" — a large change. He also said the 30-second wait could be made one minute [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- Pavel's middle way: match the unclaimed money to the nearest earlier wallet that started a session on the same machine, so a cashier can confirm it fast. Val: "Это очень хорошая". Klimovich: the logs already hold this — the deposit transaction has the machine, the time code and the wallet ID; only a cashier filter is missing [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].
- Counter-points: [[wiki/people/alexander-biratka.md|Biratka]] (label "Alexander Biratko") warned a cashier could invent a way to steal it. Chudinov gave a case where the nearest wallet belongs to someone who lost everything, while the real owner fed cash through the bill validator. Khamin suggested the cashier could replay the withdrawal to the port [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

**The ruling.** Klimovich would not give the cashier any way to move unclaimed money yet: "забирать деньги с анклейн кудато выводить их не хочу пока давать… [в] мвпи 2 мы можем вернуться к этому вопросу." In MVP 1 "мы не предлагаем никаких экшнов сейчас даже для обработки… Наша задача пока сохранять эти деньги." Val closed it: "давайте на [MVP] один это дело оставим[,] Андрей прав, мы это сейчас не поднимем… Перенесём это" [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. The considered options — Val's PIN idea, Pavel's nearest-wallet matching, Khamin's replay — are not adopted and not rejected; they wait for MVP 2.

**How this sits with earlier rulings.** It keeps Val's Sept-15 rule that the player never loses the money and that unclaimed handling is not MVP 1 ([[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]], Sept-24 update). The 30-second collect wait is [[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]]; it was questioned, not changed.

## Update, Sept 30 2026 — Ivan reads the network-loss behaviour back for his tests; Pavel confirms "an error is better than unclaimed"; the no-bill-validator case and the SAS-link checkbox stay open

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian) [[wiki/people/ivan.md|Ivan]] asked, "для теста", what a machine does when the Flex-Port loses its network [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **Ivan's reading.** "машина ж не упадет в [тилт], она просто будет говорить, что коллект можно сделать. Ты жмёшь [коллект], но она упадёт дальше в ошибку, потому что нет, [нет] куда вывезти… И там у нас есть [ретрай], и если вдруг… сеть восстановятся, то будет [ретрай] и мы сможем [довести], если [нет] — всё на машине осталось." Pavel: "Да, я думаю что так." He meant the local network ("Я говорю про локальную сеть"), not SAS.
- **Pavel's reason.** The current behaviour — "На данный момент выдается ошибка" (Ivan) — is right: "**Это лучше, чем передать на порт. На порте пройдёт 30 секунд таймаута, и они потом пометятся как [unclaimed]. И при следующем коллекции они придут как [unclaimed]**." The 30-second wait is the one on [[wiki/decisions/2026-09-16-the-mvp1-timing-numbers-two-hundred-milliseconds-and-thirty-seconds.md]].
- **The key unknown is a third-party machine.** Pavel: "тут будет ключевой момент с чужой машиной, как себе чужая машина ведёт" — the Sept-9 rule on [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]].
- **Two channels.** Ivan: the Flex-Port "общается по 2 каналам, один из интернет 2 ну сас линг назовём его так"; if the port has no connection it "будет аутосервис" — [[wiki/people/irina-shishko.md|Irina]]: "Порт будет ауто сервис" — the Bug-354 rule above. [[wiki/people/dmitri-chudinov.md|Chudinov]] asked whether a port "должен принять деньги. Даже если он в [out of service]?" — Pavel: with no network the port reports an error; it cannot.
- **Irina's case: no bill validator.** "Есть ли порт потерял связь с айкю… [о]н становится… [out of service]… Машина продолжает играть, потому что можно бросить деньги через билвалидатор, но если нет бил валидатора, то тогда и машина тоже должна блокироваться." Ivan: "я пока даже не смотрел ситуацию, что нету [bill validator]"; Irina: for now there should be one. Pavel doubted it: "Мы как бы рассчитываем на то, что если пропадает связь, то она не навсегда… И зачем на этот короткое время машину блокировать?" Irina: "я же говорю, что машина продолжает работать." Not settled.
- **The SAS-link checkbox.** [[wiki/people/evgeny-kharetski.md|Kharetski]]: there is "галочка… [п]оказывает [fault], если [SAS] линк даун". Ivan: "я не ставлю ее пока специально… никто не говорил, что нужно её ставить." Kharetski: "никто не говорил, но никто не запрещает ей ставить." Not settled.

The derived notes record the same exchange and list the three open points [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]. Against the rules above: Bug 354's "no gateway link → out of service, money stays on the machine" is confirmed as the behaviour the tests expect; nothing is changed.

### Open questions (Sept 30 2026)

- Should a machine with **no bill validator** lock when its Flex-Port is out of service? Irina: yes; Pavel: a short outage is expected, why lock — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- Should the "fault if SAS link down" checkbox be set? Nobody has asked for it; nobody forbids it — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]

## Update, Oct 5 2026 — unclaimed money is shown in cashier Records; the cashier sees it and cannot pay it out

At the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 8:01 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]:

- **The gap.** [[wiki/people/dmitri-chudinov.md|Chudinov]], now on capability 141: money that does not reach the machine is not lost — it is passed to the IQ — "Но кассиры то посмотреть не сможет, нету дошбардак, где можно посмотреть анкл деньги" (the port screens are admin-only — [[wiki/decisions/2026-10-05-flex-port-and-connection-settings-screens-live-under-the-admin-role-not-the-cashier.md]]).
- **The answer.** [[wiki/people/andrei-klimovich.md|Klimovich]]: the cashier's IQ screen with all transactions already has an unclaimed status. Chudinov: "Сделать это в рекордах… хорошо я туда помечу… мы сейчас этими деньгами ничего не делаем, ничего не пересоздаём". [[wiki/people/irina-shishko.md|Irina]]: "Это будет в записях, но их нельзя сейчас отдать игроку." Klimovich: "мы пока не решили, что делать с этими записями, но сам факт наличия записи уже создаёт как бы защиту, что это не потеряно и пускай кассир видит"; to the player, "условно говоря, позвоните дживи эль".
- **Machine-to-port transactions in Records.** Klimovich said they should already be there as their own types, "Депозит и коллект"; Chudinov: "клод сказал что нема… посмотрим повнимательнее".

This keeps the Sept-24 ruling: cashier action on unclaimed money stays in MVP 2. The derived notes record "Unclaimed money is shown in cashier Records; no action on it for now" as decided by Klimovich and Chudinov [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

### Open commitments (Oct 5 2026)

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — flag unclaimed money in the cashier Records screen (visible, no action) — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — check that the deposit and collect transaction types between machine and port appear in Records — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — add the two logic changes from bugs 349 and 354 to the MVP 1 requirements — due Sept 24 2026 ("2 изменения, которые будут добавлены сегодня") — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [ ] (blocked-on: MVP-2) [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — return to what a cashier may do with unclaimed money (redirect to a wallet, nearest-wallet matching, PIN) in MVP 2 — due MVP 2 — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Open questions

- **Does the Flex-Port save a pending transaction in its own memory today?** Khamin and Irina said it is not built that way now; the rule needs it — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## History (answered questions)

- ~~How will locations deal with unclaimed money in MVP 1, when the cashier has no action to release it?~~ Pavel asked; Chudinov: "Ваши деньги… я их вижу, но я вам их не отдам. Моя кнопочки нет." — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]] — **answered Oct 5 2026:** the cashier sees it in Records and cannot pay it out; the player is, "условно говоря", told to call JVL — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

**Notes vs transcript.** The notes' account of both rules matches the transcript [[raw/Meeting_Notes_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]. They leave out Chudinov's first time-based proposal, Klimovich's one-minute option and Val's praise of Pavel's nearest-wallet idea.

**§15.8:** clear — product logic only. **§15 #9:** none; 349 and 354 are bug numbers.

## Update, Oct 9 2026 — collect money that does not reach the scanned wallet after a port crash goes to unclaimed in MVP 1; sending it to the known wallet is for later

On the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|Oct-9 Transactional MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]:

- **Irina's case.** A player collects money from the machine and scans a wallet; before the money reaches the wallet, the port reboots. The money does not go to the scanned wallet. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Это это уже анклей." [[wiki/people/andrei-klimovich.md|Klimovich]]: "мы с Димой говорили на эту тему приняли пока такое решение." Pavel: money taken off the machine "Назад они уже вернутся не могут, поэтому они только либо на кошелек, либо в анклы всё."
- **Could it go to the scanned wallet?** Chudinov: "Теоретически, если человек отсканировал кошелёк… флик спорт может сохранить, на какой кошелёк планировала сумма? И если произошёл ребут при поднятии эти деньги отправить на кошелёк." Irina: today it does not. A case that breaks this: the Flex Port is connected to another master, "например, заменили IQ". Pavel: if the Flexport loses power, the money stays on it until power returns; and "вдруг уже игрок выбросил этот кошелек?" Chudinov: "Неважно… Главное, что мы их не потеряли."
- **The MVP 1 rule.** Klimovich: "в рамках м випи один мы сделаем так что всё в ант[клейм] лежит. Мы ещё мы воспринимаем этот статус как с охранный." Auto-sending to a known wallet is "идея хорошая", but all cases need thought. Chudinov: "Хорошо." — "запаркуем как анкэйм ты пускай авто тесты на это будут заточены."
- **A later idea.** Pavel: "возможно, в будущем в какомнибудь 3" — the cashier sees a saved wallet on an unclaimed item; the player shows the ticket, the cashier presses a button and the money appears on the player's wallet. *(The notes read "3" as MVP 3 [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].)*

This repeats, for one more case, the Sept-24 rule above (money a Flex Port holds goes to unclaimed). It is **evolution**, not a contradiction.

### Open questions (Oct 9 2026)

- Later: should unclaimed money go to the known saved wallet automatically, or by a cashier's action (Pavel's MVP 3 idea)? — [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]

## Sources
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Notes_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
