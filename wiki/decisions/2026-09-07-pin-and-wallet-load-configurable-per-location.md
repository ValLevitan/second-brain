---
type: decision
title: On Flex-Port under SAS the PIN becomes a per-location option — where a location runs without one, all its tickets are accepted automatically — and loading funds from the wallet to the machine becomes configurable the same way, partial-amount screen or credit everything
date: 2026-09-07
aliases: [PIN optional per location, tickets accepted automatically, partial load, load everything, wallet to machine configurable, $50 $20 or all, the PIN is what changes for the player]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# PIN and wallet load become per-location configuration

Settled at the [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md|Sept 7 2026 10:02 AM engineers' alignment]] (Russian), as part of working out what the move to SAS actually changes for the player.

This is the **implementation requirement** for a policy already ruled: [[wiki/decisions/2026-08-24-drop-pin-from-evoucher-flow.md]], whose titular "drop the PIN" element was softened on Sept 2 2026 into a per-location switch. Sept 7 is where that switch acquires its behaviour on the Flex-Port.

## What was decided

- **The PIN request is optional per location, and a no-PIN location auto-accepts.** [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] asked for it — "просто даже надо сделать пин[-]код этот опциональный" — and [[wiki/people/pavel.md|Pavel Frolov]] turned it into the requirement: "и [во] флекс[-]порт[е]… у нас вот новое требование, что мы должны опционально пин[-]код запрашивать — то есть… если лакейшн настроен на работу без пинкода, то все его тикеты должны автоматически приниматься" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Loading funds from the wallet to the machine becomes configurable too.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "и загрузка средств с [в]оллет[а] на машину тоже опционально. Там у нас сейчас есть parti[a]l — загрузить не всё, а на выбор игрока; это тоже должно быть сконфигурировано" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].
- **Both paths described, and confirmed.** Pavel: "мы либо этот экран отображаем, где показываем там **$50, $20 или [all]**… [либо,] если настроено для лакейшена зачислять всё, то мы просто этот экран не показываем, и все деньги, которые были, они зачисляются туда — и обратно [то же самое]." Klimovich: "Именно" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

## What actually changes for the player

Klimovich asked it directly — Pavel had said user behaviour changes because of the move to SAS, and Klimovich wanted to know what exactly: "ты сказал[,] пользовательское поведение из[-]за перехода на sas. Вот расскажи, пожалуйста, что именно[?]" Pavel's whole answer was one word's worth: "вот этот я имел в виду как раз пин[-]код." Klimovich: "Понял, окей" [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

These are the capabilities Klimovich then volunteered to own — and which Val re-labelled as **use cases** — on [[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]] [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]].

**§15.8:** clear — product configuration only.

## Sources
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
