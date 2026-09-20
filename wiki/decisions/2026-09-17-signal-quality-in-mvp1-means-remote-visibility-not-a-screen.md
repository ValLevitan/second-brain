---
type: decision
title: Signal quality in MVP 1 means remote visibility — periodic metrics into the logs, buffered offline, surfaced through Grafana
date: 2026-09-17
aliases: [signal quality, decibels, signal to noise, SNR, jammer, глушилка, антенки, remote diagnostics, periodic metrics, log buffering, Grafana alerts, modem telemetry, удалённо мы должны видеть децибелы]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
---

# For MVP 1, signal quality has to be visible remotely — not on the device screen

Settled on the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]] (Russian). It is the first concrete answer in this series to [[wiki/people/val-levitan.md|Val]]'s Sept-15 demand for non-functional requirements about devices that quietly fall off the network ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]).

## Why bars are not enough — the jammer argument

[[wiki/people/andrey-bosik.md|Andrey Bosik]] asked for the signal to be readable in **two forms at once**: "**хочется видеть графическое исполнение, это когда… антенки[,] лесенки рисуются[,] и 2 вариант — это когда пишется там в децибелах**" — the drawn bars *and* the figure in decibels [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

His reason is the failure the bars hide: "**если кто[-]то принесёт глуш[и]лку какую[-]нибудь… антенки будут показываться великолепно… но сеть работать при этом не будет, и это как раз будет видно за счёт показателей децибел[,] шумов**" — next to a jammer the bars look perfect while the network is dead, and only the decibel and noise figures show it [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**What Flex IQ already has:** [[wiki/people/pavel.md|Pavel Frolov]] confirmed the admin settings do show decibels — "**Там показываются децибелы**" — but not the ratio: "**это не снр, не отношение сигнал[/]шум… это чисто уровень сигнала… провайдера**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## The ruling — remote, not local

Bosik himself moved off the screen — "**может быть и правда нет смысла показывать это на экране, только всю [телеметрию] лить к нам сразу**" — and [[wiki/people/andrei-klimovich.md|Klimovich]] set the MVP 1 boundary against Val's standing Monday item: he recalled that "**вал говорил о том, что… условно к понедельнику нам надо ещё продумать всю вот эту вещь, связанную с оперированием устройств по удалёнке**", and read the signal question into it — "**это можно интерпретировать в MVP один как то, что мы должны видеть все эти параметры у себя удалённо[,] не локально на машине… удалённо мы должны видеть децибелы**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Klimovich had also floated putting the numbers in front of a role on the payment hub / operations portal — "**в пэймент хабе… для кого[-]то с какой[-]то ролью видеть**" — and [[wiki/people/dmitri-chudinov.md|Chudinov]] refused that framing flatly: "**Нет, нет, не сможем… это просто лог информации… эту информацию мы получаем, мы можем как[-]то анализировать, интерпретировать; показывать никому не сможем**" — what arrives is log data, analysable but not displayable to a person as it stands [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## The mechanism Chudinov specified

Asked whether signal — a thing that changes constantly — can be carried in a log at all, he described the existing log transport and said the modem can ride it [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]:

1. **Periodic sampling into metrics** — "**можно… периодически снять его в этих метрик**".
2. **Automatic send when there is internet** — "**отсылка идёт автоматически, если есть интернет**".
3. **Buffer to file when there is not, and flush on reconnect** — "**если нет, то он скидывает этот файл[;] и как только сеть появляется, он всё это отсылает**".
4. **Same path as everything else** — "**Это касается всех логов системы[,] аппликешн… также можно для модема сделать**".

This is the same offline-tolerant behaviour the Sept-16 ruling depends on ([[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]]).

**Interpretation is a second, separate task — Grafana.** "**это 2 часть[:] графана[,] можно сделать, например, дашборд или систему а[]лертов**", with notification out to email; and he split the work explicitly: "**Задача 1 как[-]то собирать[,] 2 как[-]то уведомлять либо показывать**" — collect first, notify or display second. Klimovich accepted it as sufficient: "**Супер, отлично, хорошо, для [MVP 1] этого достаточно**". The derived notes record the same outcome — for MVP 1, signal quality means remote visibility, collected periodically into the logs, buffered offline and surfaced through Grafana [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

*(Grafana was already in place and was Chudinov's answer to Val two days earlier, when Val cut him off with "if it is not written, it does not exist". This call is where it acquires an owner and a shape, though still not a written requirement — see the open commitments below.)*

## Where it is not written down yet

Asked whether anything in Jira covers it, Pavel searched live and found nothing: "**Я пересмотрел по логированию на клауд[-]сервер… ничего не нашёл, надо будет через Клода поспрашивать**" — nothing on logging to the cloud server; he will have to ask Claude. Klimovich's instruction was to find or create the capability and its requirements: "**Надо будет найти этот [капабилити] и создать его, найти рек[вайрментс] или добавить их**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

And he put the signal requirement on the man who raised it: "**ты как о[у]нер… этого запроса должен убедиться, что есть нужный рек[вайрмент] для этого[;] если его нету, то добавить**". Bosik: "**Хорошо**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — as owner of the request, make sure a requirement exists for remote visibility of signal quality (decibels and signal-to-noise), and add it if it does not — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — find or create the Jira capability covering logging to the cloud server; nothing was found on the call — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

## Open questions

- **Whether the numbers ever reach a person in MVP 1.** Klimovich wanted the signal figures on the operations portal for a role-holder; Chudinov said the collected data cannot be shown to anyone as it stands, and the Grafana dashboard/alerting half was explicitly labelled "task 2". No date or owner was set for it — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**§15.8:** clear — device telemetry and tooling only; no compensation or performance judgement for any named person. **§15.9:** no credential, key, certificate, APN or address value was spoken — the discussion stays at signal level, noise ratio and log transport.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
