---
type: decision
title: Remote software update is mandatory for the Flex-Port and is taken off Eugine Yavorsky — Val does not want tasks sitting with him; Evgeniy Alekseev takes it after the Wi-Fi work, and nothing has ever been implemented or tested on the Flex-Port side
date: 2026-09-07
aliases: [remote firmware update, remote software update mandatory, taken off Yavorsky, I find it very hard to work with him, not implemented on Flex-Port, version reported on next connect, tested against his own simulator, it was a priority a year ago]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# Remote firmware update is mandatory, and it is taken off Yavorsky

The gap the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|Sept 7 2026 10:02 AM engineers' alignment]] (Russian) exposed. [[wiki/people/val-levitan.md|Val]] asked a simple question — "ф[ё]рм[в]а[р]ы на лету можем делать апдейт на портах, а на IQ и на [Flex-]пей? Мы можем это делать или нет?" — and the honest answer was no, not on the Flex-Port [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

It continues the thread on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Jul 28 2026, where remote update became priority 1 for the IQ pilot).

## The state of play, device by device

- **Flex-IQ / Flex-Pay — in progress.** [[wiki/people/pavel.md|Pavel Frolov]]: "Дима сейчас заканчивает это… систему" — [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] is finishing it. Chudinov on the IQ: "я думаю, к моменту релиза уже сможем," with reworking still needed. Pavel on Flex-Pay: "это то же самое, по сути будет," but it needs work [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Flex-Port — nothing.** Pavel, flatly: "фирм[в]а[р] апдейт ещё не реализован на флекс[-]порт… протокол там разработан, Дима какую-то версию сделал, но это ещё никто не реализовал на стороне флекс[-]порта и, соответственно, никто не тестировал" — the protocol was designed, Chudinov made some version of it, nobody has implemented it on the Flex-Port side and nobody has tested it [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **What [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] actually tested, a year ago.** "ремо[у]т апде[й]т тестировал ещё год назад." Val asked whether that was over USB; Alekseev: "Нет — [тестировал] симулятором… который себе написал простенький" — against a simple simulator he wrote himself [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **How a successful update is confirmed.** Val asked whether there is a handshake back or a checksum. Pavel: "при следующей загрузке, при следующем коннекте [Flex-]порта к flexpay он сообщает свою версию. Мы видим, что был коннект с одной версией, стал коннект с другой версией" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## The reassignment

Pavel named the owner: "я просто знаю, что эта задача висит на Евгении Яворском, и он ещё её не начинал" — the task sits with [[wiki/people/eugine-yavorski.md|Eugine Yavorsky]] and he has not started it [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

Val's answer was to take it off him, and he said why, twice: **"Давайте мы Яворского снимем, потому что [с] Яворским мне очень тяжело работать"** and **"я бы не хотел на Яворского иметь какие-то таски — с ним что-то я не умею с ним работать"** [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

Alekseev volunteered: "давайте после вайфая я реализую вот этот ремо[ут]" — after the Wi-Fi work. His read of the difficulty: "то, что я точно знаю, что внутри это реализовано — то есть приём данных, запись и перезапуск… Оно возможно с w[eb]s[ocket] se[ss]ion что-то недоделано, я так предполагаю" — receiving data, writing it and restarting are there; something on the WebSocket session side may be incomplete. Val: "мы должны это проверить, правильно?" Alekseev: "Да, конечно — ну дописать, если оно не работает" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

*(Scope note: the removal was spoken about the remote-update task specifically, but Val's second sentence is general — he does not want tasks sitting with Yavorsky at all. The consequence for the Sept-4 SAS assignment is annotated on [[wiki/decisions/2026-09-04-port-the-smib-sas-module-into-the-flex-port-main-branch.md]].)*

## Why everyone agreed it is mandatory

Pavel drew the conclusion and nobody dissented: "сходимся на том, что нам ремо[ут] софт апдейт нужен обязательно. Потому что в реальных условиях мы наверняка будем чтото вылавливать, и нам надо будет оперативно эти ошибки исправлять на работающих устройствах. Удаленно" — in real conditions they will certainly find things and will have to fix errors remotely on working devices [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

Alekseev noted it had seemed a priority a year ago — "мне так казалось, что это было приоритетом год назад… приоритетной задачей." [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]'s reply: "Теперь это тоже приоритет, видите? Всё константно" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## Open commitments

- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — implement and verify the remote firmware update on the Flex-Port after the Wi-Fi work; internals believed present, WebSocket session side may be incomplete — due after Wi-Fi, high priority — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

## Open questions

- **Which release the on-the-fly firmware update lands in for Flex-IQ and Flex-Pay.** Klimovich asked twice — "К какому моменту релизу?" and "В момент релиза — это что? …какая версия чего?" — and got only "Какой-то релиз" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

**§15.8:** clear — task assignment and engineering state. Val's difficulty working with Yavorsky is recorded as his stated reason for the reassignment, not as a performance or compensation matter.

## Sources
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
