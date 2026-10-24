---
type: decision
title: Every gap found on another maker's machine becomes new or corrected requirements with acceptance criteria, plus code and prose, and the machine emulator keeps a mode per maker; Pavel and Irina, not Val, enforce this culture (Oct 18 2026)
date: 2026-10-18
aliases: [emulator per maker, работай как айджи, keep the emulator current, scope gaps into requirements, скоб гапс, new requirements with acceptance criteria, Pavel and Irina enforce the development culture, законодатель культуры, IGT lock command, команда lock, SAS lock, machine emulator, сасмулятор, машинкулятор, reference SAS client, setup screens of other makers, 4K capture adapter, фор кей адаптер, 55 AFT checkboxes, oscilloscope not needed for now]
source-count: 6
status: active
open-commitments: 5
open-questions: 1
---

# Every gap on another maker's machine becomes requirements; the emulator keeps a mode per maker

Set by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-10-18-flex-port-sas-igt-lock-and-emulator-requirements.md|Oct 18 2026, 7:00 AM call]] (Russian, about 29 minutes) with [[wiki/people/pavel.md|Pavel Frolov]], who agreed [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]. The notes list it as Val's decision, Pavel agreeing [[raw/Meeting_Notes_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Where the Flex-Port SAS work stood (Pavel)

- **The machine emulator.** About three weeks earlier Pavel built a reference SAS client — "то, что мы называем сасмулятор… Или… машинкулятор" — that acts like a machine. The team first made the Flex-Port load and take money against it; "довольно быстро получилось там дня за 3". Then they put a JVL machine in its place, and "сразу же ничего не заработало", so they had to adapt to how the JVL machine behaves. "Сейчас мы то же самое ловим для чужих машин": SAS works a little differently on each machine [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **Not the old emulator.** Val remembered the emulator as [[wiki/people/evgeny-kharetski.md|Kharetski]]'s ("хорецкий"). Pavel: what Kharetski made "год назад или 2 года назад" was "эмулятор хоста с асовского" — the other side. That host side now runs, in a different implementation, on the Flex-Port [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **Aristocrat.** A minimal change about timing and the correct order of events; "мы в принципе быстро это поправили" [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **IGT.** It did not work the day before. In the evening Pavel found that "i giшная машина не умеет корректно работать с командой lock на на сасе". In SAS the host first locks the machine, so nothing changes on it, then asks for the money; that is more reliable. The IGT machine seems to just queue the "give me the money" command. Pavel expected IGT to work that day if the Flex-Port does not send the lock command [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].

## What Val decided

- **Gaps become requirements.** Under "Культуры разработки, на которой мы все подписались", a gap found on a machine ("скоб гапс", read as scope gaps — **inference**) means new requirements with additional acceptance criteria, or corrected old ones, plus code and prose in the repository. Val: "давайте мы подтянем эти новые рекламы… под аристократ поддай GTT. Добавим, этот кот Добавим прозу… Самое главное. Новый рекламент с аксептон критериев." Pavel: "Именно так мы и делали." [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- **The emulator keeps a mode per maker.** Pavel had discussed it with Irina the day before: put switches in the emulator — "давай работай как айджи… А сейчас работает как аристократы" — so support for each maker is kept and a fix for the next machine does not break Aristocrat or IGT. Val's reason: to test a future Flex-Port change on all machines, "единственное, что мы можем делать в тот момент это пользоваться тем акмулятором"; otherwise JVL must keep borrowing machines, or rely on people remembering what they did. "И то и то в принципе неправильно." [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- **Emulator first, live machine last.** Pavel: maybe 80% of tests can run on the emulator, "но всё равно финально на всех машинах придётся". Val partly disagreed: a final test on a live machine is desirable, "Ну это уже другой вопрос", but work always starts on the emulator, which holds the latest knowledge of the machines checked [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **Pavel and Irina enforce it, not Val.** Pavel said he had no resistance. Val: "Я не ищу сопротивления. Я ищу сотрудничество"; he wants the culture held up by Pavel and [[wiki/people/irina-shishko.md|Irina]] "через нашу организацию". "Я не хочу быть лидер и инфорсер инженеры." If they do not keep it every day, "Со временем здесь расслабятся… Все распадется." Pavel: "Да я это понимаю." Val repeated it at the end: Pavel and Irina as "ударной силой" for the culture of engineering development [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].

## The setup screens of other makers' machines

- **Photograph them all.** On Friday in Atlanta Val opened the borrowed machines and saw full setup screens, "особенно аристократ лайтэн ig thind" (Aristocrat, Light & Wonder, IGT). He asked that "Все эти скрыны сфотографировали. Все до единого." Pavel had asked "Андрея" the same the day before: "более идеального случая, чтобы снять чужие скрины у нас не будет." ("Андрей" = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], who runs the Atlanta set-up — **inference**.) [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- **How.** The screens are captured with a 4K adapter bought on Amazon, plugged between the CPU and the screen. The old one broke; Val bought a new one that arrives Monday. Val will be back in Atlanta on Monday [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **AI to suggest settings — left to the team.** Val suggested giving AI the Flex-Port description (or the emulator) and all the screens, and asking how to set each machine up; he doubts the makers have bugs and thinks some optional setting may explain cases like the lock. Pavel: the AFT parameters are "ну 55 галочек", only about 2 need checking; doing it by hand is not hard and builds experience for whoever works with these machines later; he does not think AI adds much there. AI could instead compare all the setup screens with JVL's own for user experience. Val closed the topic: up to the team; the screens are still collected and sent to them "чтобы вы имели рекорд этих вещей" [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]] [[raw/Meeting_Notes_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].

## The other machines

- Pavel: on the rest, the team needs access to the machine parameters to change them and see how the port reacts — "Вот это будем уже сегодня, завтра" [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- Val: with Aristocrat and IGT working, "мы в принципе 70% покрываем рынок", but "обязательно нужно ещё лайтен ундер, нам обязательно нужны другие машины" [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]].
- **No oscilloscope for now.** Val asked whether a scope must be rented. Pavel: on the third machine "мы точно видим, что sass подключен, команды ходят", and all Flex-Port activity is logged to Grafana ("графану"), which gives a great deal of information; "Я даже не знаю, понадобится ли нам там даже скоп." [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]

## How it sits against earlier items

- **Builds on Sept 9.** [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] — the borrowed-machine tests; its Oct-16 failures (cash-out on Aristocrat and IGT) now have a fix (Aristocrat) and a likely cause (IGT) — see its Oct-18 update.
- **Consistent with Oct 12.** [[wiki/decisions/2026-10-12-flexport-ci-tests-run-on-real-ports-through-the-internal-runner-and-no-port-emulator-is-built-for-now.md]] ruled out a Flex-Port emulator; this page is about the *machine* (EGM) emulator on the other side, which that page already had. On Oct 12 Chudinov warned that an emulator built to the SAS standard keeps needing changes for each real machine; Val's rule now makes those changes a requirement (link drawn here — **inference**).

## Open commitments

- [x] [[wiki/people/pavel.md|Pavel Frolov]] — get IGT cash-out working by not sending the SAS lock command — due Oct 18 2026 ("сегодня") — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]] — *Oct 19 2026: Pavel told the stand-up the IGT machine does not answer the lock command and keeps reporting locked; not working yet (see the Oct-19 update)* — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] — *Oct 20 2026 (8:31 AM): closed as superseded (not done) — IGT reports SAS 6.03 but its AFT still does not work, and machines without working AFT now connect by bill-validator emulation and pulses (see the Oct-20 update)* — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] / team — write the gaps found on Aristocrat and IGT as new or corrected requirements with acceptance criteria, with code and prose; add per-maker modes to the machine emulator — due unspecified — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]] [[raw/Meeting_Notes_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — set and enforce the development culture every day — ongoing — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] with the Atlanta team (who takes the photos is **unclear**) — capture every setup screen on the Aristocrat, Light & Wonder and IGT machines with the new 4K adapter and send them to Pavel's team — due from Mon Oct 19 2026 (adapter arrives Monday) — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]] [[raw/Meeting_Notes_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] / team — get access to the settings of the remaining machines and test how the port reacts — due Oct 18–19 2026 ("сегодня, завтра") — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]

## Open questions

- Will the remaining machines (Light & Wonder and others) need an oscilloscope? Pavel thinks not for now; Val would rent one, which takes time — [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]

**§15.8:** clear — no pay matters. **§15 #9:** none.

## Update, Oct 19 2026 — Light & Wonder and IGT still fail over AFT; Pavel asks Kharetski and Biratka for ideas

At the end of the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian; Val absent) [[wiki/people/pavel.md|Pavel]] said that in the last two days the team worked with the other makers' machines and "наш флекс спорт… С ними некорректно работает по FT" (AFT, per the notes [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]) [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]:

- **Light & Wonder, first machine.** Money goes in by AFT, but cash-out does not work.
- **Light & Wonder, second machine.** The port sends commands and identification, but it does not reach cash-in or cash-out.
- **IGT.** It does not answer the lock command ("лок там 72", as heard) and keeps saying it is locked.

Pavel asked [[wiki/people/evgeny-kharetski.md|Kharetski]] and "Саша" ([[wiki/people/alexander-biratka.md|Biratka]], by context — **inference**) for advice, "может, что то вы знаете, чего не знает квот" (Claude, as heard — **inference**). Kharetski: look at what the port logs, and whether the machine answered or stayed silent. The others were let go and the talk went on as a new meeting, recorded separately (not in this source) [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

- **Against Oct 18.** On Oct 18 Pavel expected IGT to work that day without the lock command; on Oct 19 IGT is still not working — the commitment below stays open. Light & Wonder, which Val called a must on Oct 18, now has a first result: cash-in on one machine.

### Open commitments (Oct 19 2026)

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] with [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] and [[wiki/people/alexander-biratka.md|Alexander Biratka]] — work out the AFT cash-out failures on the Light & Wonder and IGT machines from the port logs — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] — *Oct 20 2026 (8:31 AM): Pavel: only JVL and Aristocrat work fully; the other machines go to bill-validator emulation and pulses for MVP 1; stays open as the record of the AFT gaps* — [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]

## Update, Oct 20 2026 (8:31 AM) — only JVL and Aristocrat work fully; the other makers' machines go to bill-validator emulation and pulses in MVP 1

At the [[wiki/meetings/2026-10-20-third-party-egm-bv-emulation-mode-and-sas-data.md|Oct-20 8:31 AM third-party EGM call]] (Russian) [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]:

- **The verdict.** [[wiki/people/pavel.md|Pavel]]: "Живел и аристократ. Молодцы." The other machines work only partly with AFT, so they connect by bill-validator emulation (money in) and pulses (money out). IGT reports SAS version 6.03 but AFT does not work; a second Light & Wonder machine says AFT is registered but all its AFT options are zero.
- **What the SAS side shows.** On three machines (not the Banilla) a limited set of commands: handpay state on all, door open/close on some, credit queries on Light & Wonder. [[wiki/people/irina-shishko.md|Irina]]: certified machines must support about 20 commands. Light & Wonder has a setting to report every spin, which needs a factory reset to try.
- **Gaps become requirements.** Val asked that the pulse capability be tied to requirements with acceptance criteria before tests are written — this page's rule in use.

Full detail: [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]] [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]. Nothing was said about the per-maker emulator modes or the setup-screen photos; those commitments stay open.

## Sources

- [[raw/Meeting_Transcript_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [[raw/Meeting_Notes_Flex-Port_SAS_IGT_Lock_and_Emulator_Requirements-October-18-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Transcript_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
- [[raw/Meeting_Notes_Third_Party_EGM_BV_Emulation_Mode_and_SAS_Data-October-20-2026.md]]
