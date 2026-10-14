---
type: decision
title: Flexport tests in CI run on real Flexports through JVL's internal self-hosted runner — no Flexport (STM32) emulator is built now; a study of STM32 simulators is not MVP 1 and likely not MVP 2
date: 2026-10-12
aliases: [no port emulator, Flexport emulator, порт эмулятор, STM32 emulator, стм 32, real ports with hooks, CI through the runner, внутренний селхост раннер, self-hosted runner, Flex IQ emulator in Docker on the runner, tests overnight on real ports]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
---

# Flexport tests run on real ports through the internal runner; no port emulator now

Settled at the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/irina-shishko.md|Irina Shishko]], on a question from [[wiki/people/alexei-khamin.md|Alexei Khamin]]. Quotations from [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]] unless marked.

## The question

Chudinov had just said he brought the machine (EGM) emulator closer to the SAS standard. Khamin asked what the plan is for a Flexport emulator. Pavel: "Это не портмулятор, это е г м эмулятор" — that one is the EGM emulator — and "Апорт никто никогда не собирался его делать" (nobody ever planned to make a port one).

## The positions

- **Tsymanov:** an emulator could be raised as a container from the port's own code, "без хардверной части", for tests.
- **Pavel:** the Flexport runs on an STM32 processor ("стм 32 процессор"). Much of it depends on hardware interrupts, so it would need a full STM32 system emulator; "Какието там базовые варианты есть, но вряд ли они нас устроят по качеству". Anything simpler only imitates behaviour and "это очень далеко будет от реальности".
- **Khamin:** he expects Val sees it differently — "у нас будет полноценное, которое собирается прям да на живой на живом коде, и мы тестируем именно и ловим баги там", not an imitation. An emulator is fine for the gaming machine, because that is not JVL's product; the Flexport "это уже наш продукт… за которым мы отвечаем". *(This is Khamin's reading of Val's view; Val was not present.)*
- **Chudinov:** real machines differ from the SAS standard, so an emulator built to the standard keeps needing changes for each machine.
- **Pavel:** "работа с реальным портом у нас сейчас там все все, что нужно было хуки мы сделали. А портов нам хватает." Tests on real hardware with the hooks are "более надёжное тестировано", because everything is real except the wrappers the tests call from outside.
- **Irina:** real ports do not block anyone — "мы его можем… тесты и на ночь запустил и ушёл. Это нас никак не блокирует."

## The ruling

- Pavel: a study of the STM32 simulators people use can be done, but "это явно не MVP один и и вряд ли м в пи 2".
- Khamin: "у меня то получается на тогда завязывать CI прохождение тестов именно через райнер на реальное устройство так получается" — Pavel: "Да да." Irina: "Для порта да."
- Pavel: through "нашем внутреннем селхостанере" (read as the internal self-hosted runner); "на нём можно запустить этот IQ в докер контейнере там всё для этого есть", so the Flex IQ emulator can see the hardware on the internal network. Chudinov had pointed out that otherwise ("Агерхаби", read as on GitHub — **inference**) the emulator and the hardware "друг друга не найдут".

In one line: **for the Flexport, CI runs the tests on real ports through JVL's own runner; the Flex IQ emulator can run in Docker on that runner; no port emulator is built now.**

The derived notes record the same decision, by Pavel and Irina [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## How it sits against earlier items

- **Sept 7 / Sept 29.** On Sept 7 Alekseev asked for a virtual test system that included a "virtual Flex-Port"; on Sept 29 Pavel said "нам, наверное, [Флекс-П]орта особо не надо" and put the Flex IQ emulator first — see [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]]. Oct 12 confirms that no port emulator is planned for now (**evolution**). Pavel's "nobody ever planned" is his own wording; the Sept-7 request did exist.
- **Oct 7.** Pavel then deferred CI runs on real hardware so Khamin could write tests first — [[wiki/decisions/2026-10-07-cover-the-code-with-tests-first-and-the-ci-hardware-runs-and-product-repository-hookup-wait.md]]. On Oct 12 Khamin is back on bringing up the tests on pull requests and on real hardware, and the route for the port is fixed (**evolution**).

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — wire the Flexport tests into CI through the internal runner on real devices (with the terminal and EGM emulators) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
