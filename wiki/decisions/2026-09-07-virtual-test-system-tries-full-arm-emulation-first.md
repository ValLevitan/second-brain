---
type: decision
title: The virtual test system attempts full ARM-processor emulation running the production build plus simulated devices first — Docker or a daemon-mode simulation is the fallback, because the simpler options do not cover the full functionality
date: 2026-09-07
aliases: [virtual test system, emulators, virtual Flex-Pay, virtual gaming machine, virtual Flex-Port, ARM emulation, same build as on the machines, Docker fallback, daemon mode, bare remote-update tool, redeploy all the hardware from scratch]
source-count: 15
status: active
open-commitments: 6
open-questions: 2
---

# The virtual test system: try full ARM emulation first

[[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] raised this in both Monday meetings on Sept 7 2026 ([[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08]] and [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02]], Russian), and it is an old request of his, not a new one. It is the natural successor to the environment-rebuilding problem both engineers named on [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]], and it takes up the stage-2 debug environment [[wiki/people/pavel.md|Pavel Frolov]] proposed on Sept 4 (see [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Sept 4).

## The standing request

"Когда начинали flexport, я всё время просил сделать какие-то эмуляторы: там flexp[ay-]эмулятор, там гейм[-]машин[ы]… сделать… виртуальную систему тестирования — виртуальный [Flex-Pay], виртуальная машина, виртуальный fla[x]port, билл[-]валидатор, айкью." His reason: "сейчас мне, если тестировать вай фай, мне нужно разворачивать всё железо заново" — to test Wi-Fi today he has to redeploy all the hardware from scratch; with the emulators "я просто взял[ бы] на одной машине, всё запустил и тестировал бы одну только железяку" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

He repeated it an hour later against remote update specifically: "если бы… была программа на компьютере, то это было бы намного быстрее — [проверять] то[т] же ремо[ут] апдейт" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

**What he can and cannot do himself:** "[эмулятор] машины я могу и сам написать, там ничего такого" *(the transcript renders the word as "регулятор"; the derived notes read it as the gaming-machine emulator — garble flagged)*; "меня больше… интересует: вот если [Flex-Pay] кто-то это… написать" — the Flex-Pay side is what he needs from someone else [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## What exists, and the timeframe

[[wiki/people/val-levitan.md|Val]] said Pavel was half way there — "у Павла на 50% это готово уже, чем хвастался" — and Pavel would not accept that: "не готова, у меня какие-то наработки есть… я пока не уверен, что они готовы к тому, чтобы их отдать." Val put a limit on it anyway: "для вас это не больше, чем неделя работы," and at the 10:02 call restated it as settled: "эту виртуальную систему мы договорились, что Павел доделает в течение недели[-]2" — within a week or two. Pavel's answer both times was to try: "мы подумаем, что с этим можно сделать" / "я попробую это организовать" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## The three options, and the order they are tried in

- **Alekseev's minimum:** a bare tool exercising only the remote update, without Flex-Pay — "если, допустим, Дмитрий может сделать вот просто… чистый[,] не всю функциональность… хотя бы вот эту вот часть — ремо[ут] апдейт — чтоб без flex pay можно было… может не кнопочка, хотя бы command[-line] какой-то интерфейс" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s middle option:** "скорее, Паша, проще будет запустить как… в докер[е] либо… в каком-нибудь режиме дем[о]на… [с] симуляцией некоторых данных" — **Docker** or a daemon mode with simulated data [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Pavel's choice, which is the ruling:** "попробуем пойти по пути… виртуальной машины, которая полностью [э]мулирует работу арм[-]процессора… с тем же б[и]лдом, который мы сейчас используем на машинах[,] возможность симуляции каких-то устройств. Если это не получится, тогда уже будем какие-то более простые варианты." His reason for the order: "более простые варианты, они не покрывают весь функционал." Alekseev agreed it would be ideal and asked for a front end — "какие-то кнопочки — там послать, принять… какой-то интерфейс графический" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## Who Pavel will pull in

"Я поговорю с Сашей Бираткой, с Димой Чудиновым — что можно сделать относительно быстро" — [[wiki/people/alexander-biratka.md|Alexander Biratka]] and Chudinov [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## Update, Sept 22 2026 — a FlexPay emulator is being built

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM MVP 1 call]], when Irina looked for developers to help with tests, Pavel kept one of them where he was: "Антон сейчас делает эмулятор для флекспея. Это как раз то, что вам понадобится. И вам и Евгению Алексееву ещё кому-то, кто будет проводить тесты" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

- This is the **Flex-Pay side** [[wiki/people/evgeniy-alekseev.md|Alekseev]] said on Sept 7 he needed from someone else. It is now being built, and Alekseev is named as one of its users.
- **Which Anton is not resolved** — no surname is spoken, and none of the three Antons on file clearly fits. Not linked.
- Whether this emulator is part of Pavel's full ARM-emulation attempt or a separate piece is not said. Pavel's commitments below stay open.


## Update, Sept 23 2026 — the emulator's new priority one: a terminal emulator that works with a real Flex IQ

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian), [[wiki/people/anton-seregin.md|Anton Seregin]] (speaker label) reported on the kiosk emulator. **The Sept-22 "Антон" above is very likely him (inference)** — same work, next day. [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

- **What he fixed.** He built on the existing validator daemon ("Поверх вот этого демона"), which another Anton had written (not resolved). Before, it could not change currency or bill denominations, a bill-cheating error "никак не всплывала", and there was no fail pause — "события срабатывали мгновенно", so the kiosk skipped steps and its logic broke. He added escrow cases and the disconnect case "когда купюра типа съелась, но не прошла транзакция". He is still checking it. [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- **Pavel named the most critical use.** "наиболее критичное направление для использования этого эмулятора киоска это обновление прошивок для флекспортов" — so it can be handed to [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. Anton: the Flex-Port is not in the emulator at all — "такого как бы устройства даже нет". [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- **Priority one, first version:** "Эмуляцию полную протокола общения с флекспортом." [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- **Then narrowed.** Pavel: do the same for Flex IQ — "брать уже именно флекса и кюшны проект, потому что он тоже более приоритетный флекс пэй он как бы будет 2 номером." Anton's working branch can be merged into main, then cloned for Flex IQ. The Flex-Port protocol already sits in the backend; it needs checking somehow, and "Как это сделать, пока не знаю". [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- **A piece to reuse.** [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] had built a Flex-Port emulation for an earlier task, but "он у меня локально" — never in a repository. Anton: "По идее, можно переиспользовать." [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- **Final wording:** "приоритет номер один это эмулятор терминала, чтобы с ним можно было работать реальным устройством. Не не эмулятору другому а реальному устройству." Anton: "IQ который". Pavel: "Да да." [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

The notes read it the same way: priority one is a terminal emulator against a real Flex IQ; FlexPay second [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]. Whether this is part of Pavel's full ARM-emulation attempt is still not said.

## Update, Sept 23 2026 (8:00 AM) — the FlexPay emulator is to be copied for Flex IQ

At the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM call]], answering Khamin's problem with a money-crediting test, Pavel described the emulator work: without real hardware it must be able to issue and redeem wallets — "сделать эмуляцию операций, которая делает реальный бэкенд". It is "тот же самый бэк энд, который на боевой машине только он будет работать с фейковыми устройствами", run "в докер контейнере", deployable on a developer's computer or a server [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]. *(The transcript renders "emulator" as "аккумулятора" — read as "эмулятора", an **inference**; the notes say emulator.)*

**Status.** Asked when the IQ emulator is due: "Не запланирован, пока сейчас он заканчивает флекс певский эмулятор. Ему сейчас надо завести задачу на то, чтобы он это размножил на флекс айкю" — "пару дней наверно". "He" is Anton — [[wiki/people/anton-seregin.md|Anton Seregin]] by **inference** (same work he reported at the 4:48 stand-up) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

**Reading against the ruling above (inference):** the Docker container was this page's fallback, and full ARM emulation the first choice. This call describes the emulator as a Docker-hosted backend with fake devices. Whether that means the fallback was taken, or the container simply hosts the emulation, is **not said**.

## Update, Sept 24 2026 — the Flex IQ emulator is the FlexPay one, moved across

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Features to be raised.** Pavel asked [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] to see that features for the Flex IQ emulator are created "по аналогии с флекс пэем". Kovalchuk: "Это мне надо сделать задачу." Pavel said Claude could create them from the previous day's recording, or they could be made by hand, and then read and agreed by all.
- **Little change expected.** [[wiki/people/anton-seregin.md|Anton]] asked if the devices use the same models, protocol and contracts. Pavel: yes, apart from workflow and screens — Flex IQ has its own screens where the cashier enters data. Anton: "я же… эмилирую конкретно поведение устройств". Pavel: "Даже, скорее всего, всё заработает."
- **Anton moves it today.** "перенесу, пока этот аккумулятор… За сегодня… На IQ" (read as "эмулятор" — **inference**, as on Sept 23).
- **It runs only on his machine.** Nobody else has looked at it yet; running it in the cloud is pointless, but anyone can run it locally. Pavel: someone should look "когда выкроится на это время".
- **The spike** on the firmware contract is on [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-24 update).

**Anton's Sept-23 commitment below stays open** — the move to Flex IQ was due that day, but no later source confirms it.

## Update, Sept 26 2026 — the firmware simulator is not ready

At the [[wiki/meetings/2026-09-26-flex-port-telnet-console-and-gui-harness.md|Sept-26 Flex-Port development sync]], [[wiki/people/pavel.md|Pavel]]: "пока что на симулятор не готов для прошивок. И, наверное, сегодня завтра не будет готов." Reading this as the virtual test system on this page is an **inference** (he names no project). His commitment below stays open. [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]

## Update, Sept 28 2026 — a plan to move the emulator to Flex IQ, first step done

- **At the 4:56 AM stand-up** ([[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept 28]], Russian), [[wiki/people/anton-seregin.md|Anton Seregin]] said he finished a move ("закончил переносом") on Saturday and "составил план переноса на fex IQ аккумулятора" ("аккумулятора" read as the emulator — **inference**, as on Sept 23–24). The first task "[в]роде выполнил, сейчас это всё проверяю". The work is to fit it to the Flex IQ contract: a bridge that "[с] 2 сторон контракт принимает от флекса IQ и аккумулятора". His AI tool set its own dates; Irina: "Но не до 21 октября явно." Pavel asked that it write autotests for each task; Anton said it already writes quick endpoint tests that run in the GitHub Actions build [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]].
- **At the 8:02 AM call** ([[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept 28]]), Khamin asked who builds emulators. Irina: "Этим занимается Антон." [[wiki/people/alexander-biratka.md|Biratka]]: he made one, but "внутри [ф]лекс pay", with the card dispenser. Pavel: "Он должен сейчас перетянуть это все в флексей кю[]" [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]].

**Anton's Sept-24 commitment below stays open** — the move is planned and started, not finished.

## Update, Sept 29 2026 — the Flex IQ emulator comes before any Flex-Port emulation, and the EGM emulator gets delay and hang cases

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]:

- **[[wiki/people/anton-seregin.md|Seregin]]'s status.** "по сичии, как бы вроде всё закрыл" (read as CI — **inference**); he is re-checking "[в]се эти истории, которые клод заводил по плану" — the stories Claude created from the plan; "[р]абота на флекс… [т]о, что переносил аккумулятор" (the move of the emulator, "аккумулятор" read as before — **inference**). He wanted to open a Flex-Port feature "[ч]тобы поизучать… [к]ак он будет [э]мулировать".
- **Pavel's order.** "**нам, наверное, [Флекс-П]орта особо не надо**"; first the Flex IQ emulator and the Flex-Port firmware update through it; a Flex-Port emulation only if "совсем просто" — something that answers commands. Detail and the feature on [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-29 update).
- **The EGM emulator cannot delay or hang.** [[wiki/people/alexei-khamin.md|Khamin]]: "я несколько сценариев не могу написать, потому что там нет функционала, типа там остаться, повисеть" — the "эмулятор этот е г м с, а с" (the EGM / SAS emulator) has no way to hang or delay. He had written up three points the day before and asked whether Pavel does it or he does. Pavel: "**бери бери бери себе**" — but as a separate tab or panel of test functions, "список кейсов… что типа отвечать с задержкой на следующей, например, пакет там 72 лонгпола" (answer the next long poll 72 with a delay). Khamin: it fits the existing design, just "[в]ыставлять флаг какойто".

**Anton's Sept-23 and Sept-24 commitments below stay open** — the emulator move is still in progress.

## Update, Sept 29 2026 (10:06 AM) — an x86 emulator exists and is good, the RK3568 one is weaker, and "the image boots in an emulator" is the one useful SDK test

At the [[wiki/meetings/2026-09-29-dev-environments-rk3568-sdk-amd-spike-and-ai-pm-direction-check.md|Sept-29 "Dev_environments" call]] (Russian) [[wiki/people/pavel.md|Pavel]] described the processor emulators as they stand [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]] [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]:

- **Status.** Asked by Val whether an emulator must be made: "Для икс 86 [э]мулятор есть. Он хороший. [Эмулятор] для рк 35 68 он тоже какойто помоему есть, но он не не настолько будет хороший как для икс 86" (the transcript says "стимулятор" and "аккумулятор"; read as emulator — **inference**, as on the Sept 23–29 updates above).
- **What it is for in the SDK.** The only useful direct test of a build environment is "что текущая сборка… собралась и на ней может загрузиться. Эмулятор… просто чтобы сказать, что полученный имидж рабочий" — the built image boots in an ARM-processor emulator; it presumes an emulator one trusts ("при условии, что мы доверяем [эмулятором]"). See [[wiki/topics/test-automation-strategy.md]] (Sept 29, 10:06 AM).
- **Reading against the ruling (inference):** a full ARM-processor emulation running the production build is this page's first choice; "какойто… есть, но… не настолько хороший" is the nearest the corpus has to its status. Pavel's commitments below stay open; the call names no emulator project.

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — add the delay / hang test cases to the EGM emulator himself, as a separate tab or panel of test functions — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — attempt the virtual test system as a full ARM-processor emulation running the production build, with simulated devices settable by command; fall back to Docker / daemon-mode simulation only if that fails — due within a week or two — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — talk to Alexander Biratka and Dmitri Chudinov about what can be stood up quickly on the Flex-Pay emulator side; Alekseev writes the gaming-machine emulator himself — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — merge the emulator branch into main, then clone the work for Flex IQ and build the terminal emulator that works with a real device — due unspecified; named priority one — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — see that features for the Flex IQ emulator are created, by analogy with FlexPay, with the Flex-Port firmware-update protocol as its own feature — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — move the FlexPay emulator across to Flex IQ — due Sept 24 2026 ("За сегодня") — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]

## Open questions

- **Whether Pavel's existing groundwork is fit to hand over.** He said he is not sure it is ready, against Val's "50 % done" — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

- **How is the backend's Flex-Port firmware protocol checked?** Pavel said it must be checked "какимто образом" and did not yet know how — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

**§15.8:** clear — tooling only.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_FlexPort_Telnet_Console_and_GUI_Harness-September-26-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_RK3568_SDK_and_Pavel_Bottleneck-September-29-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]
