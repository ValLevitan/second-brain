---
type: decision
title: The virtual test system attempts full ARM-processor emulation running the production build plus simulated devices first — Docker or a daemon-mode simulation is the fallback, because the simpler options do not cover the full functionality
date: 2026-09-07
aliases: [virtual test system, emulators, virtual Flex-Pay, virtual gaming machine, virtual Flex-Port, ARM emulation, same build as on the machines, Docker fallback, daemon mode, bare remote-update tool, redeploy all the hardware from scratch]
source-count: 4
status: active
open-commitments: 2
open-questions: 1
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

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — attempt the virtual test system as a full ARM-processor emulation running the production build, with simulated devices settable by command; fall back to Docker / daemon-mode simulation only if that fails — due within a week or two — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — talk to Alexander Biratka and Dmitri Chudinov about what can be stood up quickly on the Flex-Pay emulator side; Alekseev writes the gaming-machine emulator himself — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

## Open questions

- **Whether Pavel's existing groundwork is fit to hand over.** He said he is not sure it is ready, against Val's "50 % done" — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]

**§15.8:** clear — tooling only.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
