---
type: decision
title: The virtual test system attempts full ARM-processor emulation running the production build plus simulated devices first — Docker or a daemon-mode simulation is the fallback, because the simpler options do not cover the full functionality
date: 2026-09-07
aliases: [virtual test system, emulators, virtual Flex-Pay, virtual gaming machine, virtual Flex-Port, ARM emulation, same build as on the machines, Docker fallback, daemon mode, bare remote-update tool, redeploy all the hardware from scratch]
source-count: 25
status: active
open-commitments: 11
open-questions: 3
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

## Update, Sept 30 2026 — the printer and scanner emulation fit Flex IQ, the card dispenser is not used, the LTE modem is not emulated, and the Flex-Port side is empty

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian) [[wiki/people/anton-seregin.md|Anton Seregin]] reported on the Flex IQ emulator [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **What fits.** "Проверял ticket принтер эмулятор. Если баркот скайнер, как оно согласуется с флексом IQ? Там как бы она работает" — the ticket-printer and barcode-scanner emulation work against Flex IQ.
- **The card dispenser is out.** Asked whether it is used at all: [[wiki/people/dmitri-chudinov.md|Chudinov]] — "Диспенсер не используется"; [[wiki/people/pavel.md|Pavel]] repeated it. (Flex IQ has no dispenser; the dispenser is FlexPay's — see [[wiki/people/alexander-biratka.md|Biratka]]'s capability 134.)
- **LED backlight on events.** "он ещё предлагает делать… подсветку вот симулировать надо на ивенты" — something (who "он" is — the tool, by context — is **unclear**) proposes simulating the LED backlight on events. Not ruled on.
- **The LTE modem is not emulated.** Pavel: "может мы как раз как раз не трогать л т е модем… слишком специфическая область." Seregin agreed.
- **The Flex-Port side.** Nothing exists in Flex IQ for Flex-Port updates, and the FlexPay code is untested — on [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Sept-30 update).
- **An instruction.** "скинул в чат этот аккумулятор. Большую инструкцию, если интересно" — a long emulator instruction posted in the chat ("аккумулятор" read as emulator — **inference**, as throughout). Pavel will read it later.

The derived notes record the dispenser and LTE points the same way and call "the Flex IQ emulator will not simulate the LTE modem" a decision by Pavel [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]].

**At the 8:03 AM call** ([[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept 30]]), emulators came up from the other side: Pavel, on the receipts the testers print — "пользуйте эмуляторы"; [[wiki/people/irina-shishko.md|Irina]]: "не эмуляторы нужны, потому что не очень удобно" — the testers share one Flex IQ and queue for it; Pavel: a second Flex IQ as bare boards on a table is enough for tests. See [[wiki/topics/test-automation-strategy.md]] (Sept 30, 8:03 AM) [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]].

**Anton's Sept-23 and Sept-24 commitments below stay open** — the move to Flex IQ is being checked device by device; Khamin's delay-case item was not mentioned.

## Update, Oct 1 2026 — verifying the Flex IQ emulator against the device: a register of checked versions, "one instance per device" so it goes to work sooner, and someone else brings it up next

At the [[wiki/meetings/2026-10-01-daily-standup-sas-mode-flag-and-feature-status-rules.md|Oct-1 Minsk stand-up]] (Russian) [[wiki/people/anton-seregin.md|Seregin]] reported on the Flex IQ side ("по [Flex IQ]… дошел до как бы до стадии") [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]:

- **The check.** "шаблону для верификации. Ну корректность короче эмуляции… Сверить его с тем, что на… устройством" — run a scenario ("положить деньги, распечатать тикет… клиента забрал") on the emulator and on the device and compare the logs: "Не подмешивается ли чегото там дополнительного, либо, допустим, какойто [эвент] пропускается." [[wiki/people/irina-shishko.md|Irina]]'s worry — tests pass on the emulator and "на реальном устройстве. Будет ерунда" — and [[wiki/people/pavel.md|Pavel]]'s answer — "у нас не стоит задач полностью соответствовать… если находятся разночтения. Ну [фиксятся]" — are on [[wiki/topics/test-automation-strategy.md]] (Oct 1, 4:48 AM).
- **A register.** "есть версия у самого эмулируемого устройства… у него есть поле к какому какой модели. И её прошивки. Было верифицировано. [Клод]… предлагает делать? Вести такой типа регистр. Он как бы уже сделал, просто он не заполнял. Реальной [сверки] с… устройством не было." Daemon versions as spoken: "на принтер вот этот демон он там ноль ноль 8 версия… И ноль ноль 6. Fix pay… Там там не поднимали версию. Вот но есть какието отличия" — 0.0.8 against 0.0.6 on FlexPay (reading).
- **One instance per device.** Pavel: "у нас наверное, будет одно устройство. Например, если смотрим на принтер, там наверное для эпика надо сейчас делать… Даже наверное, этот картдиспенсер, хоть у нас там и 2 возможно использовать, наверное, лучше сделать всё пока что в в единичном экземпляре. В пользу Того, чтобы быстрее этот [эмулятор] пошёл в работу, чтобы все могли его использовать." Seregin: "Оно единственный экземпляре одна" — it already is. ("акмулятор" read as emulator — inference, as throughout.)
- **Today, then the next priority.** Seregin: "попробуй за за сегодня это всё. Закрыть" and look for more cases. Pavel: "следующей задачей может быть даже приоритетной… попробовать этот [environment] твой поднять. У кого нибудь ещё, то есть там с лёшей поработать там или с Владимиром или там с ирой… в отличном [environment] от твоего смотреть, как оно работает там, например, с реальным флекса [IQ]" — [[wiki/people/alexei-khamin.md|Khamin]], [[wiki/people/vladimir-samusenko.md|Vladimir]] or Irina brings it up elsewhere. Seregin: "Угу."

The derived notes record the same five points [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]. His Sept-29 Flex-Port-update task was not mentioned (see [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]]).

### Open commitments (Oct 1 2026)

- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — finish the Flex IQ emulator verification (the scenario comparison and the register of checked device models and firmware) and look for further cases — due Oct 1 2026 ("за сегодня") — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: in progress — scenarios "102 103" set up to build diffs, then "с реальным устройством. Прогнать на нём сценарий"; Irina: if the tests pass "ты закончил"; Seregin: "мне устройство бы еще проверить на устройстве" — not declared done* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — next, have the emulator environment brought up by someone else (Khamin, Vladimir or Irina) in a different set-up, for example against a real Flex IQ — due unspecified; Pavel's next priority for him — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]] — *Oct 2 2026: in motion — Khamin: "Антон попросил ещё этот [эмулятор] попробовать… Можно наверно сегодня"* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

### Open questions (Oct 1 2026)

- Which device model and firmware version each emulator release was verified against — the register exists but is empty — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

## Update, Oct 2 2026 — scenarios 102 / 103 build the diffs, then the same scenario on a real device; Khamin is asked to try the emulator

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian) [[wiki/people/anton-seregin.md|Seregin]]: "Над 102 103. Я поставил и не загружается контент остановиться" (garbled); "такие типа сценарии, которые. Строять дифы… а потом, ну после этого надо будет с реальным устройством. Прогнать на нём сценарий? И вот он сравнит как бы. То, что [на эмуляторе] и то что [на устройстве]. Их логически это тот же самый процесс… как оно вот на систему будет на одном смотреть?" — the Oct-1 comparison method, now with numbered scenarios (the notes read "scenarios 102/103"). Pavel: "Хорошо." Later [[wiki/people/irina-shishko.md|Irina]]: "Антон, у нас один с симулятором. В принципе, если тесты пройдут нормально, то ты закончил." Seregin: "Но мне устройство бы еще проверить на устройстве… пробовать можно уже по крайней мере." [[wiki/people/alexei-khamin.md|Khamin]], in his own status: "Антон попросил ещё этот [эмулятор] попробовать… Можно наверно сегодня" — the "someone else brings it up" step of Oct 1 has started with Khamin (Anton = Seregin by context — inference) [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. Nothing new on the register of verified versions.

## Update, Oct 5 2026 — FAQ-105 to 108 closed, the printer scenarios still need a real device, location binding was emulated; the emulator is built from repository scripts (main by default), an artifact per Flex IQ build is too heavy; and "kiosk" becomes "terminal"

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]:

- **[[wiki/people/anton-seregin.md|Seregin]]'s status.** "позакрывал стори. Для. Верификация… [с]верки, короче, как проходит [аннуляция] работы [с] принтером? Ну там fa q 105 106 107 108 закрывал. Это не входит в 67. Перекинь. Выше" (the prefix and "67" as spoken; the notes read FAQ-105 to 108 and "reconciliation of printer work" [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]). What is left: "по сценариям сверки осталось. Ну для принтера осталось это свериться с реальным устройством, то есть пройти те же сценарии там их несколько в наборе там успешные есть. Есть сценарий, который там типа бумага замялась фейл самого принтера. Типа дисконнект принтера, вот такие вот их нужно на реальном устройстве получить их же провести. Вот тогда можно их пометить, что [верифицированы]. И для [баркод-сканера] ну там совсем там попроще." A detail: "Поэтому принтера нам нужно было. Симулировать привязку к [локейшн], потому что он печатается [локейшн]. Пришлось еще вот это эмулировать [—]." "По факту вот осталось как бы физическое сравнение вот этих 2 разных путей. Вот и тогда можно сказать, что. Болееменее, он как бы работает это всё." Pavel: "Тогда занимайся этим." The Oct-1 verification method is thus part-done: the emulator side is closed, the device side is not.
- **A FlexPay-derived task to block.** Pavel: "здесь что то висит вот до 2 октября тут надо либо сроки." Seregin: "это, скорее всего, вообще блок надо, потому что это с флекс [пэем] мы так ничего не поняли, как что там дальше делать?… это было каких то. Начинаниях там флекс. Свои киоски. Но он как там просто какоето описание было всё, что он нашёл. На этом невозможно ничего [инаследовать]." Pavel: "Имплементация там какаято была там протокол какойто был." Seregin: "он не [смержил] никуда. Вот какойто там ветки то ли что." Pavel: "[FlexPay], ты имеешь в виду?" — "Да." Pavel: "Ладно." Not ruled; see [[wiki/decisions/2026-09-30-an-autotest-task-that-cannot-finish-goes-to-blocked-not-closed.md]] (Oct-5 annotation).
- **How the emulator follows the main code — [[wiki/people/alexei-khamin.md|Khamin]]'s question.** "откуда он собирается этот [эмулятор]? То есть сейчас, допустим, [Дима] несёт правки в код там про [анклеймед мани], как мы это на эмуляторе получим?" Seregin: "собираешь там есть скрипты внутри [репозитория]? По дефолту там берётся из мейна. Ну ты можешь указать с какой то ветки хочешь… можно уже готовый образ. Поднимать весь ну этот стек? Сам эмулятор киоск. И их общение внутри сервиса? Они на основе готовых уже собранных докера имиджа… это же для ускорения работы." Irina: "принтер там присутствует?" — "Принтер да. Сканер [—]." Pavel: "флекс IQ здесь у нас [билл-эмулятор]. Вот это правильно." Khamin wanted the package rebuilt on a GitHub Action run — Seregin: "Там долго эта сборка, поэтому и она создаёт лишний образ ну образ это как бы и деньги компании. На хранение этого всего идёт и время занимаем… если тебе нужно конкретная версия, то можно собирать. Отдельно"; images are overwritten, not accumulated ("перетирает они"). Khamin: "мне нужно, чтобы эмулятор соответствовал… коду основного приложения."
- **An emulator artifact per Flex IQ build — considered, judged too heavy.** Pavel: "если бы на этапе сборки основного вот флекса ай кю вот этой сборки сюда клался артефакт ещё и эмулятора, то это тебя устроило." Khamin: "конечно только непонятно. Ну не слишком ли это вес? Добавит сборкам. Если он будет там собираться и за счёт этого там в 2 раза дольше, то както надо отдельное решение. Плюс артефакт… на каждый [билд] будет ещё один артефакт достаточно тяжёлый." Pavel: "Ну да"; then "подход тут альтернативный это чтото из Того, что наверное Антон и сделал… Пакет с набором скриптов, например, и со ссылками на. Но докер контейнер… этот скрип запускаешь, он сразу стартует этот докерконтейнер подгружает туда. Этот инсталлер [Flex IQ]." Seregin: "так этот скрипт есть, он в репозитории… у него есть параметризация… Можно в какую хочешь версию собирать"; adding the action "с киоском… просто удлиняет процесс сборки." Pavel: "Да да да." Khamin: "Посмотрю, что что есть и потом уже оттуда можно будет [—] хорошо." The notes record the per-build artifact as "considered and superseded" [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].
- **"Kiosk" becomes "terminal".** Khamin: "ты видел там письмо было по поводу Того, что мы [уходим] немножко [от] название киоск. Называем терминал." Seregin: "это просто оно. Транслировалось этого с флекспэя мы сюда перенеслась ну поправимся." Khamin: "У нас и в [Jira] тоже эти фичи названы тоже с киоском. Такой себе." Pavel: "**Ну я думаю в описании это легко поменять в джире. Наверное, это тоже легко поменять, а в [коммитах] нет смысла уже как есть, так есть.**" The letter is not in the corpus. The notes call it a decision by Pavel [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]. (The name "terminal emulator" was already Pavel's Sept-23 wording above.)

**Seregin's Oct-1 commitments below stay open** — the device side of the verification is the remaining half; the "someone else brings it up" step is now Khamin's build question. Khamin's Sept-29 delay-case item was not mentioned. The stand the card autotests would need is a separate, larger question — [[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]] (Chudinov: "даже несколько сложнее, чем [э]мулятор порта и IQ").

### Open commitments (Oct 5 2026)

- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — run the printer scenarios (the successful ones, paper jam, printer failure, printer disconnect) and the barcode-scanner ones on a real device, compare the two paths, and only then mark them verified — due unspecified ("занимайся этим") — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — look at the emulator's repository scripts and parameters and build it to match the main application's code — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] ("ну поправимся"; not assigned by name) — change "kiosk" to "terminal" in the Jira feature names and descriptions, leaving commits as they are — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Update, Oct 12 2026 — no Flexport emulator for now; the port is tested on real hardware

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) Pavel said a Flexport emulator was never planned ("Апорт никто никогда не собирался его делать"): the port is an STM32 processor with many hardware interrupts, and the known STM32 emulators are unlikely to be good enough. CI for the port runs on real ports through the internal runner, and the Flex IQ emulator can run in Docker on that runner; a study of STM32 simulators is "явно не MVP один и… вряд ли [MVP] 2" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]. Full ruling: [[wiki/decisions/2026-10-12-flexport-ci-tests-run-on-real-ports-through-the-internal-runner-and-no-port-emulator-is-built-for-now.md]]. This follows Pavel's Sept-29 order above (**evolution**). The Sept-7 "virtual Flex-Port" in Alekseev's request is, for now, not being built.

Also that morning [[wiki/people/dmitri-chudinov.md|Chudinov]] said he brought the machine (EGM) emulator close to the SAS standard, though real machines differ from it [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — add the delay / hang test cases to the EGM emulator himself, as a separate tab or panel of test functions — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — attempt the virtual test system as a full ARM-processor emulation running the production build, with simulated devices settable by command; fall back to Docker / daemon-mode simulation only if that fails — due within a week or two — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — talk to Alexander Biratka and Dmitri Chudinov about what can be stood up quickly on the Flex-Pay emulator side; Alekseev writes the gaming-machine emulator himself — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — merge the emulator branch into main, then clone the work for Flex IQ and build the terminal emulator that works with a real device — due unspecified; named priority one — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — see that features for the Flex IQ emulator are created, by analogy with FlexPay, with the Flex-Port firmware-update protocol as its own feature — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — move the FlexPay emulator across to Flex IQ — due Sept 24 2026 ("За сегодня") — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]] — *Oct 1 2026: on the Flex IQ side he is at the verification stage (see the Oct-1 update); the move itself is not declared done* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

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
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
