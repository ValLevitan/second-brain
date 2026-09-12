---
type: decision
title: Error recovery, handshaking, heartbeat and error detection are MVP and come ahead of extra functionality — the non-functional requirements go into the capabilities with single-line acceptance criteria so the tests can be automated
date: 2026-09-07
aliases: [non-functional requirements first, error recovery before features, MVP requirement handshaking, heartbeat, self-diagnostics, drop-off and reconnect, single-line acceptance criteria, ask Claude to find the existing requirements, positive path first then failure cases, error table]
source-count: 4
status: active
open-commitments: 2
open-questions: 1
---

# Robustness before features

The one thing [[wiki/people/val-levitan.md|Val]] said in both Monday-morning meetings on Sept 7 2026 ([[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|9:08]] and [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|10:02]], both Russian). It is the shape the capabilities have to take, and it is stated as a trade he is willing to make.

## The ruling

Val, at the 10:02 call: "это должно быть M[V]P[-]re[qui]rement[:] handsha[king,] эр[р]ор детекшн[,] эр[рор ре]ко[в]ери. Это должно [быть] в первую очередь. Мне лучше меньше функционала добавить, но все эти эр[рор ре]ко[в]ери [и] сервис ит[е]мс мне нужно впереди" — he would rather add less function and have all the error-recovery and service items in front [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

His list, restated later in the same call: "меня волнует хе[нд]ш[е]йки, меня волнует [heartbeat], меня волнует hard bad, меня волнует, если чтото повисло, зависло, застряло, заело. Не подключилось, ни[ ]детект[и]ровалось" *(the transcript renders one item as "hard bad"; the derived notes read the list as handshakes, heartbeat and hard-bad states — recorded with the garble flagged, no term substituted)* [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

At the 9:08 call he had already told [[wiki/people/andrey-bosik.md|Andrei Bosik]] what the capabilities must contain: "когда вы пишете кей[па]билити[с,] там будут… в основном много очень нон[-]funct[io]nal re[quire]ment[s]. Технических, например, как се[лф-]диагностика, какойто дроп[-]офф[ —] если сигнал будет[,] переподключения; какие-то двухсторонние там [хендшейки]; потом [heartbeat] какой то, чтоб мы постоянно знали, что мы в сети находимся. Вот эти все вещи нужно расписать, под них иметь ре[к]ва[йр]м[енты], чтобы мы могли их протестировать, чтоб можно было сделать a[u]t[o]m[a]te[d] test[s]" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

- **They already exist, and are to be found rather than re-invented.** [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]: "у нас же сейчас[,] по-моему, есть это всё уже в протоколе вебсокет." Bosik agreed it is largely the same as what was built for Ethernet — "для [Ethernet], наверное, это то же самое, что делали… или по крайней мере бо́льшая [часть] этого… должна была быть." Val's instruction: "попросите [Клода], чтоб он нашёл эти ре[к]ва[йр]мен[т]с[;] их нужно прикрепить [к] кей[па]билити[с]. Иначе мы не сможем сделать автоматические тесты[ —] его потом руками будем всё расхлёбывать" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **The form each requirement takes:** "нам обязательно ре[к]ва[йр]м[ент]ы нужно иметь… с [single-]line [acceptance] критерия, который потом прикрепится к самому коду, к самой прозе кода" — a single-line acceptance criterion that attaches to the code and to the code's prose [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]. This is the same acceptance-criteria discipline recorded on [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md]] and [[wiki/decisions/2026-09-03-acceptance-criteria-settled-by-experiment.md]].

## How much of it is actually done — implemented is not verified

The most useful exchange of the 10:02 call. Alekseev: "насколько я понимаю, это всё реализовано." [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] corrected him in one line: **"но реализовано, но не проверялось"** — implemented, but never verified. Alekseev then narrowed his own claim: "там [heartbeat] это точно реализовано" and, on the rest, "обработка ошибок всяких ситуаций там реализована. Не знаю, может не 100%, но… 80 наверное" — about 80 percent. The group settled on verifying and completing it [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## The verification method [[wiki/people/pavel.md|Pavel Frolov]] proposed

"Для нас самое простое сделать позитив[ный путь]. А потом думать, какие могут варианты привести к сбоям — то есть в какойто момент времени пропадает связь[,] интернет, в какойто момент происходит перезагрузка. Вот эти вот кейсы… надо будет активненько проработать с клодом… потому что… они будут приводить к ошибочным состояниям" — build the positive path first, then work the failure cases through with Claude, because those are what produce error states [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

- [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] added a failure nobody had listed: "состояние экрана ещё — может тачскрин отключиться, например, перестать действовать." Alekseev asked whether it can even be detected; Val's answer was that it is a passive device ("это пассивный де[вайс]") [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **There is an existing error table to work from.** Alekseev: "сейчас мы имеем там набор ошибок… таблица ошибок, которая выдаёт этот флэкспорт. И насколько я понимаю, сегодня их часть точно обрабатывается… но вполне могут новые появиться. И вот… может[,] кл[а]уд нам даст там ещё какие-то варианты" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — ask Claude to find the existing non-functional requirements in the WebSocket protocol (handshake, heartbeat, reconnect, self-diagnostics) and attach them to the Wi-Fi capabilities, each with a single-line acceptance criterion — due unspecified, high priority; without them there can be no automated tests — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — build the positive path, then work the failure cases through with Claude against the existing Flex-Port error table (connection loss, mid-transaction reboot, unresponsive touchscreen) — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Open questions

- **How complete Flex-Port error handling actually is.** Alekseev estimates about 80 percent and is certain only about the heartbeat; Chudinov says it is implemented but has not been verified. Unresolved on the call — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

**§15.8:** clear — engineering requirements only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
