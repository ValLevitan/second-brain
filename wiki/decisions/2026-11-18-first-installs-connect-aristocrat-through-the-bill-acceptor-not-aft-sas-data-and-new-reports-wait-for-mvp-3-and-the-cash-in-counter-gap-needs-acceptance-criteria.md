---
type: decision
title: The first Georgia installs connect Aristocrat machines through the bill acceptor, not AFT — AFT on other makers' machines is unreliable and cannot be re-tested on every release; both modes stay supported, so nothing new is built; SAS data and new reports wait for MVP 3, in steps; the missing cash-in counter in bill-validator mode is a software change that must have acceptance criteria; nothing goes to the field before MVP 2 is tested; a one-hour MVP 2_1 / 2_2 clean-up call on Thursday Nov 19 (Val, on Andrei Klimovich's proposal, Nov 18 2026)
date: 2026-11-18
aliases: [Aristocrat via bill acceptor, Aristocrat via bill validator not AFT, partial AFT vs all BV and counters, GA Ports connections to EGMs, все BV плюс каунтер, подключение аристократа не через AFT, first installation through the bill acceptor, cash-in counter gap, счётчик на кэшин, скоупгап, acceptance criteria not skipped, SAS data in MVP 3, MVP 3.1 3.2, Intralot data inaccurate, Novomatic AFT test, United Gaming four Aristocrat machines, MVP 2 focus drifting, Nov 19 MVP 2 scope call]
source-count: 4
status: active
open-commitments: 3
open-questions: 2
---

# The first installs connect Aristocrat through the bill acceptor, not AFT; SAS data waits for MVP 3 (Nov 18 2026)

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-11-18-ga-ports-aristocrat-via-bill-validator-not-aft.md|Nov 18 2026, 8:00 AM call "GA Ports connections to EGMs: 'partial AFT' VS 'all BV+Counters'"]] (Russian, about 22 minutes), called by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], with [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]. It takes the Oct-20 rule one step further: Oct 20 sent only machines *without* working AFT to bill-validator mode — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] (Nov-18 update).

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are kept as heard.)*

## The question (Klimovich)

- A port on a game machine has two jobs: "трансакционная задача это money in monit, чтобы деньги курсировали", and "данные перформанс игр, аналитика". Today, by maker, the money job is done "или через AFT или через билвалидатор плюс каунтер" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Of all machines on the market, full AFT is supported only by "аристократ GVL" (Aristocrat and JVL), "И, возможно, новоматик, мы это проверим. В пятницу мы одолжим машину" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- His question: "Может быть, нам для всех машин подключаться через билулидатор и каунтер независимо от производителя. И дальше использовать сас подключения для данных." It would make the connection only a matter of bill-validator support, "которое мы уже все поддерживаем"; "Нас везде харнесы есть готовые" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

## For AFT (Pavel)

- Bill-validator emulation pays odd amounts in several steps — "он это делает за несколько операций… если какаято сумма там… Не круглая" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Through the BV, JVL is tied to its protocol and can lose the connection; "О сас там идёт гораздо более надёжная связь. Все пакеты идут с контрольными суммами", so a break "не приведёт к ошибке" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

## Against AFT on other makers' machines

- **Pavel:** "для Джорджия маркета большинство компаний. В общемто этот FT толком не реализовали." He is "фифтифифти": AFT on any non-JVL machine is hard "потому что мы не можем это проверять постоянно на каждом релизе… любое изменение, чтото сломать на чужой машине" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Klimovich — the United Gaming warehouse.** At the [[wiki/organizations/united-gaming.md|United Gaming]] warehouse "у них было там 4 машины аристократа"; settings identical, yet "На одной деньги не выводятся, на другой деньги не принимаются", and only rebooting and reconnecting made them work: "Это очень ненадёжно" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Irina:** "Мы не можем гарантировать, что там реализована FT полностью". The machines already run with a bill validator in the field — "это уже проверено. Протестировано… и мы только немножко туда вклиниваемся" — and with a BV the team knows whether a fault is in the port or in "их FT" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Klimovich — technicians.** JVL wants installs where "мы отправляем порты и люди. По нашим инструкциям сами их ставят"; the BV-and-counter connection is simpler — no machine settings, no RAM clear ("хагризет" — read as RAM clear, the notes' reading) with USB sticks, minimal downtime [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Pavel's split:** "со своими машинами мы можем подключать sas… а с чужими машинами, наверное, лучше" the bill acceptor. Val: "Это то, что Андрей говорит?" Pavel: "Да да" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Nothing to build.** Irina: "Ничего нам не нужно, ничего мы поддерживаем 2 мода и дальше поддерживаем" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

## Klimovich's first plan, then Val's ruling

- Early in the call Klimovich said no final decision was needed that day, and "Эту интеграцию в ближайшую, я думаю, мы всё таки сделаем с AFT. У нас там одна аристократ, машина 2 ig t и один GVL" — the simpler BV route could come up in a version 3 [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]. The notes leave this out.
- **Val's ruling:** "подключение аристократа не через… Эйф ти… А через белый цеп [bill acceptor]". Otherwise at a location "там будет стоять какаято другая софтровая, которую вы не проверили на аристокрации вы будете мучиться… и вам придётся оборот, этот установку" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Klimovich: it needs one check, "но для этого у нас всё есть"; on Friday they go back to the warehouse "проверить оставшиеся бракет и заодно… подключиться… аристократом через бил валидаторы". To Val's partly garbled question ("это такой же хатность, как?"), he answered "Такой же" — it depends on the bill validator — "У нас есть поддержка всех, кто есть на рынке сейчас" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Val, closing: "И вот эту первую инсталляцию делаем подсоединение аристократа через билык сектор. Это очень хорошее решение. Мои мой комплимент Андрею за то, что он продумал этот вопрос" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

In one line: **for the first installs, Aristocrat goes on the bill acceptor like the other makers; JVL's own machines can stay on SAS/AFT; both modes stay in the product.**

## The cash-in counter gap

- Pavel: for the Flex IQ money-flow report — how much money went in and out of a machine — "найден скоупгап": in the BV wiring "использовался один провод, который на кэшаут только работал. У нас не было счётчика на кэшин"; the counter is on the board but "на кэшин он в софте никак не поддерживался" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Val: "это софт… Вам нужно, вам нужно сделать новый апгрейд." Pavel: "я уже внёс это в задачи." Val to Irina: do not let anyone skip the acceptance criteria — "не забудьте… Ирина, если вы комуто дадите… Возможность не дописать акцептность критерия", repeated at the end: "Никому не давайте" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Which release: Pavel does not remember "в версию 21 оно стоит или в версию 22"; Irina will find out. Klimovich: it belongs with the report, and reports are only in version 2, so cover the gap "вместе с отчётом". Irina: "2122 это всё равно финально будет быстрее всего одна один билд" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]. Reading "21" / "22" as MVP 2_1 / 2_2 follows the Nov-12 naming — **inference** — [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]] (Nov-18 note).
- Klimovich checked he understood: money does reach the machine through the BV and the deposits show on the IQ; Irina: the function works, only the report does not count it [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

## The field

- Irina: Thursday's build is unlikely to be the one that goes to the field. Klimovich: "у нас полей ещё нету"; "Сти MP 2 не оттестировали, не убедились, что там всё хорошо. Мы ничего выпускать не будем." Val: as soon as approval comes ("как только мы получим опру" — the notes read approval) he will push installs at locations — of ports and of JVL terminals [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]. Whose approval is not said.

## SAS data waits for MVP 3

- Pavel: optionally connect SAS as well, to read all meters and events — "дверь открыта, там она в телте". Over SAS JVL can get money in, money out, games played, games won and amount won, and total bets — "во всех машинах доступны", not tied to a game title; game-title data "будет зависеть от каждой конкретной машины", and may be given to the primary SAS host but not the secondary. The port already collects some of it, held out of the current release "потому что это проверено не будет толком" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- Klimovich: "В 3 не раньше"; it must be designed into reports "имеющие ценность для пользователя", with a clear business value "для… Оператора для мастера". Irina asked why — operators get data from the system ("интролота"); Klimovich: the [[wiki/organizations/intralot.md|Intralot]] data "неточны", and hard to get — log into a portal, download a PDF, parse it; JVL's value can be everything in one place, sliced by location or game [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].
- **Val:** stop spending time on it — "это придёт натурально, как только люди… будут смотреть на наши репорты. Они скажут, а почему я не могу получить это с других машин?" Then JVL can offer another connection, through AFT or SAS. Now: "срочно перейдём на имплементацию MB 2", then "немедленно на MB pri… поступенчество MBP 3.1 точка 2… но это уже с добавлением всех отчётов". Klimovich: "Окей, согласен" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]].

## The Nov-19 MVP 2 call

- Klimovich: "у нас есть небольшое расползание фокуса. Что у нас в MP 2122 и чего мы хотим вообще добиться?" — a one-hour call the next morning to clean it up. Val wants to attend; they settled on 8 to 9 AM. Invitees: Pavel, Irina, and "Дима Сергей" [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] — read as [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], the MVP 2 developers (**inference**).

## How it sits against earlier rulings

- **Oct 20 — evolution.** Oct 20 kept AFT for machines where it works and put the rest on BV + pulses — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]]. On Oct 29 Pavel said SAS worked only with Aristocrat (same page, Oct-29 update). Now Aristocrat too goes on the bill acceptor for the first installs; only JVL's own machines are named for SAS/AFT.
- **SAS data as a product (Oct 20).** Oct 20 left open whether to read and sell SAS data from other makers' machines; Nov 18 parks it for MVP 3 without a product decision.
- **Gaps become requirements.** Val's insistence on acceptance criteria for the cash-in counter applies [[wiki/decisions/2026-10-18-every-gap-found-on-another-makers-machine-becomes-requirements-and-the-machine-emulator-keeps-a-mode-per-maker.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — at the warehouse on Friday, check the remaining brackets and connect an Aristocrat through the bill validator — due Fri Nov 20 2026 — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — borrow a Novomatic machine on Friday and try to connect, to see if it supports full AFT — due Fri Nov 20 2026 — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — find out whether the cash-in counter work is in 21 or 22, and make sure its acceptance criteria are written, with no one allowed to skip them — due unspecified — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]

## Open questions

- Does Novomatic support full AFT? To be tried on a borrowed machine on Friday — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]
- Whose approval releases the field installs Val will push ("как только мы получим опру")? Not said — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Note, Nov 19 2026 — the clean-up call was held; the field still waits for InComm

The call ran as the [[wiki/meetings/2026-11-19-andrei-mvp2-1-reporter-cleanup-and-release-date-slip.md|Nov-19 8:04 AM clean-up call]] (Russian), about 21 minutes, not an hour. Outcome: the Nov-20 date for 2_1 will not hold and no new date is set; each reporter cleans their own 2_1 items before a follow-up the next day — [[wiki/decisions/2026-11-19-the-november-20-mvp-2-1-date-will-not-hold-each-reporter-cleans-up-their-own-2-1-items-before-a-follow-up-call-and-cap-267-is-closed-into-cap-146.md]]. On the field, Klimovich: "В поле нет, мы всё ждём с инкомом. У нас проблема с регистрацией… Надеюсь, сегодня"; all hardware is in hand [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]].

## History

- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — hold a one-hour call to clean up what is in MVP 2_1 / 2_2, with Val, Pavel, Irina, "Дима" and "Сергей" — due Thu Nov 19 2026, 8–9 AM — [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]] — **discharged Nov 19 2026**: the call ran 8:04–8:25 AM Eastern with Val (briefly), Pavel, Irina and Chudinov; "Сергей" was not on it — [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]] [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]

## Sources

- [[raw/Meeting_Transcript_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]
- [[raw/Meeting_Notes_GA_Ports_Aristocrat_via_Bill_Validator_Not_AFT-November-18-2026.md]]
- [[raw/Meeting_Notes_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
- [[raw/Meeting_Transcript_Andrei_MVP2_1_Reporter_Cleanup_and_Release_Date_Slip-November-19-2026.md]]
