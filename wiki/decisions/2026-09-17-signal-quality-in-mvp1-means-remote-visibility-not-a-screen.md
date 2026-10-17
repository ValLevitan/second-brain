---
type: decision
title: Signal quality in MVP 1 means remote visibility — periodic metrics into the logs, buffered offline, surfaced through Grafana
date: 2026-09-17
aliases: [log traffic, 120 MB a day, three gigabytes a month, junk logs, TPT-INT Grafana dashboard task, signal quality, decibels, signal to noise, SNR, jammer, глушилка, антенки, remote diagnostics, periodic metrics, log buffering, Grafana alerts, modem telemetry, удалённо мы должны видеть децибелы]
source-count: 9
status: active
open-commitments: 5
open-questions: 2
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

## Update, Sept 22 2026 — Tsymanov takes the modem metrics, and the Grafana route is questioned

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 Minsk stand-up]] (Russian), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] said he has taken tasks on forwarding and collecting metrics on the modem connection ("по пересылке сбору метрик по подключению… Модема"). He asked why this should go through the logs, and said he would first check whether Flex IQ already transports metrics to Grafana, and build that if not [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

- **What goes to Grafana today.** Pavel asked what Flex IQ sends; Tsymanov: "Мы шлем только логи." Pavel: information about connected ports is probably not sent at all yet [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Not necessarily Grafana.** Tsymanov: "нам, наверное, не обязательно реализовывать на стороне через графану". He floated keeping a map of connected devices in a cache instead [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **The date.** [[wiki/people/dmitri-chudinov.md|Chudinov]]: "мы не успеем все до 1 числа. Андрей там уже это предлагал" — what Andrei proposed is not said [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].
- **Signal-to-noise on Wi-Fi.** Tsymanov asked whether he may change the platform SDK repository, because, per Claude, the Wi-Fi link has no SNR parameter. Pavel: "Потом, да можешь добавлять", but Wi-Fi is basic only and "это точно не VP один" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Update, Sept 28 2026 — the logs cost about 3 GB a month, and the Grafana dashboards may already exist

At the [[wiki/meetings/2026-09-28-daily-standup-log-traffic-and-nova-rename.md|Sept-28 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]:

- **How much traffic.** [[wiki/people/dmitri-chudinov.md|Chudinov]] left a test running overnight to see how much traffic logs and metrics use: "в районе 120 м в сутки" — "на текущем чуть больше трёх гигов в месяц". This is idle mode with no updates: "это без апдейтов, это просто вот обычный ночной… режим". Pavel: "немало".
- **What can be cut.** Some logs are junk: "принтер сервис какойто шлёт от это сканер чтото шлёт одно и то же". They can go through a cache — send only if something changed — or once every 5 minutes. Chudinov: "может раза в 2". Pavel: half is nicer, "а в 3 было бы вообще хорошо, то есть один гигабайт". Going further means lower log levels — "вместо добага ставить инфо, но тогда мы не получим чтото детальное" — and checking what the operating system sends.
- **Who judges.** Chudinov: "Нужно будет Андрею сказать об этом, чтоб он посмотрел критично это или не критично." Which Andrei is **not resolved**.
- **The Grafana dashboard task.** [[wiki/people/sergey-tsymanov.md|Tsymanov]] has a task of type "т п т инт" in the integration repository. He has seen dashboard templates — "заглушки даже бордов" — for Grafana in the Flex IQ project, and thinks the task is to configure a dashboard for "тех вот метри[к], которые мы научились отправлять в флекс айкью там по качеству связи там всяких л т е модемов". He believes he already updated those dashboards when he added the link-quality metrics. Irina: a task belongs in the integration repository only if its result is committed there. Pavel: if it is done, "просто прокомментируй и закрой".

**On the open questions below:** the link-quality metrics are now sent from Flex IQ, and Grafana dashboard templates exist in the project (Tsymanov's account). Whether a person sees the numbers in MVP 1 is still not stated, so both questions stay open.

## Update, Oct 2 2026 — the SAS command logs stay on the Flex IQ, off by default, because of the modem channel

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian) the traffic worry of Sept 28 decided the shape of a new log stream: [[wiki/people/dmitri-chudinov.md|Chudinov]] planned to pass the SAS command logs from the machines to Grafana ("Графа она, наверное будет все это передавать"); [[wiki/people/pavel.md|Pavel]] — "не будем сейчас передавать логи команд на графану… Избирательно… чтоб их по умолчанию они были выключены… потому что мы будем очень сильно засорять канал через [—] модем"; Chudinov — "пускай это будет лучше не на порте, а на IQ. Пускай он лучше не шлёт, но собирает… всегда можешь подключиться и посмотреть"; Pavel — "Да да, всё верно." Chudinov will "делать ревью трафика… на выходных… Суммарно на весь трафик" with collections and door open / close on the running firmware. Ruling: [[wiki/decisions/2026-10-02-sas-command-logs-are-collected-on-the-flex-iq-and-not-sent-to-grafana-by-default.md]] [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. This is the first stream where "task 2" (display) is switched off by design rather than left for later. Chudinov's Sept-28 junk-log commitment below is not mentioned; the weekend traffic review is its nearest follow-up.

## Update, Oct 8 2026 — the Flexport's own signal quality does not reach the kiosk; that is MVP 2 work

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[wiki/people/alexander-biratka.md|Biratka]], working on Wi-Fi and the Flexport link, asked whether the Flexport now sends its signal level and quality to the kiosk side. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Нет." Biratka: his requirements speak of the network in general, not Wi-Fi or LAN — dropouts, or pings that are too long. [[wiki/people/pavel.md|Pavel]]: "Вайфай это был как MVP 2"; Biratka works only on MVP 2. Pavel, for the record: tasks are needed on Flexport and Flex IQ for MVP 2, so that the Flexport sends the data and Flex IQ catches it and passes it on. Biratka named an existing port task ("спорт 106" — read as 106) and a Flex IQ task ("13, 28" — the notes read 1328) [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].

This matches the Sept-22 line above that Wi-Fi is "точно не VP один". It is about the Flexport's own network link, not the modem metrics of MVP 1. Evolution, not contradiction.

## Update, Oct 15 2026 — Val: all service diagnostics go to the cloud in MVP 2, with role-based access

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[wiki/people/val-levitan.md|Val]] ruled that service and diagnostic data are made available in MVP 2 "обязательно в клауд", not on the local screen, with access by role (RBAC). Bosik: Grafana dashboards today are for staff only; RBAC is partly built by Tsymanov and went to production two days earlier — [[wiki/decisions/2026-10-15-service-diagnostics-go-to-the-cloud-with-role-based-access-not-to-the-local-screen.md]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. **On the open question below** ("whether the numbers ever reach a person in MVP 1"): not answered for MVP 1, but for MVP 2 the direction is now set — the data must reach people in the cloud, by role. The question stays open for MVP 1.

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — remove junk logs (caching repeat messages or sending them every 5 minutes) to cut the traffic, and tell Andrei about the ~3 GB a month so he can judge if it is critical — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [ ] [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] — check whether the Grafana dashboard task is already done; if so, comment and close it — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — as owner of the request, make sure a requirement exists for remote visibility of signal quality (decibels and signal-to-noise), and add it if it does not — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — find or create the Jira capability covering logging to the cloud server; nothing was found on the call — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [ ] Unassigned (Pavel asked; Biratka named port task 106 and Flex IQ task 1328) — plan MVP 2 tasks for the Flexport to send its signal quality and for Flex IQ to catch and forward it — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Open questions

- **Whether modem metrics go through Grafana at all, and whether any of it is ready by the 1st.** Tsymanov questioned the Grafana route; Chudinov said there is no time before the 1st — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- **Whether the numbers ever reach a person in MVP 1.** Klimovich wanted the signal figures on the operations portal for a role-holder; Chudinov said the collected data cannot be shown to anyone as it stands, and the Grafana dashboard/alerting half was explicitly labelled "task 2". No date or owner was set for it — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**§15.8:** clear — device telemetry and tooling only; no compensation or performance judgement for any named person. **§15.9:** no credential, key, certificate, APN or address value was spoken — the discussion stays at signal level, noise ratio and log transport.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Log_Traffic_and_NOVA_Rename-September-28-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
