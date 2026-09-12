---
type: decision
title: Every JVL device with a display or lamps must visually show what it sees — surfaced both in an operator dashboard with per-item signal quality and in a service mode on the device itself
date: 2026-09-07
aliases: [devices show what they see, diagnostic tool on Flex-Pay and Flex-IQ, visual GUI, it is culture, operational dashboard, signal quality per item, service mode, neighbour visibility]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# Every device shows what it sees

A standing requirement [[wiki/people/val-levitan.md|Val]] attached to the Wi-Fi work on the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|Sept 7 2026 9:08 AM call]] (Russian), but stated in general terms about the whole product line. He raised it as soon as [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] settled the router topology: "нам нужно диагностический тул на флекспей и на флекс IQ. И даже она может быть на портах, которые показывают, что они видят. Визуальный[е] гуй… котор[ые] показыва[ют], что он видит" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## The ruling, in Val's words

- **The general form:** "Все наши девайсы, которые имеют дисплей или лампочки, должны показывать, что они видят. Это… один из ре[к]ва[й]рмент[ов]" — a requirement, not a nice-to-have [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Each device shows its own view of its neighbours.** Asked by [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] who is supposed to display it, Val: "флекспей своё показывает, флекс айкью своё показывает, флекспорт своё показывает[;] каждый девайс, который мы производим, должен видеть своих других соседей. Визуально показывать нам" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **More than a phone-style signal bar.** Alekseev asked whether he meant an antenna icon "как… сейчас в телефонах[ —] уровень сигнала"; Val: "с одной стороны, это уровень сигнала, нам нужно видеть все каналы… он должен видеть, например, 5 портов, один айкью, один… [флекс-пей]" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Why:** "это удобно. Это культура, это культура" — Val called it culture [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]. The wider pattern is on [[wiki/topics/jvl-operating-principles.md]].

## The shape Klimovich pinned down, and Val's amendment

Klimovich first read it as purely local — "Показывать на уровне локации, Вал[?] то есть я подошёл к флекспорту и должен увидеть на экране" — and Val said no; Klimovich then offered the remote form: "у нас есть операционный дашбор[д], где… оператор… мы можем залогиниться и увидеть качество сигналов по каждому айтуму" — an operational dashboard the operator logs into, showing signal quality per item. Val agreed and added the local half back: "залогини[ть]ся или поставить на тест… подошёл ктото в каком-то [режиме — ] мы показываем, что мы видим… в каком-то сервисном режиме" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

So the requirement has two surfaces: **an operator dashboard with per-item signal quality**, and **a service mode on the device** for whoever physically walks up to it [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

The build sits inside [[wiki/people/pavel.md|Pavel Frolov]]'s Flex-IQ / Flex-Pay software commitment — "для флекса айкью нам ещё доработать надо будет софт, потому что… диагностические экраны… это установка вайфая[,] соединения с роутером[;] то же самое на флекс пэй" — tracked on [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] rather than duplicated here [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

**§15.8:** clear — product requirement only.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
