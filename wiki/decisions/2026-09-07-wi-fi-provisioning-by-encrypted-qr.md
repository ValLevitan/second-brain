---
type: decision
title: Wi-Fi credentials are entered once on Flex-Pay and handed to each Flex-Port by an encrypted QR code — and the connection/installation event is captured and sent home, buffered when there is no internet
date: 2026-09-07
aliases: [encrypted QR provisioning, QR handoff to Flex-Ports, no password screen on the Flex-Port, install telemetry, who connected what and when, offline buffering, cloud logging server, Grafana section]
source-count: 6
status: active — Oct 15 2026: for Flex IQ's own access point the credentials are set on the location's dashboard page and the QR is generated there, not typed on Flex-Pay; the QR hand-off to each port stands (see the Oct-15 update); Oct 19 2026: Pavel confirmed the QR is encrypted, now with a key personal to each location, and carries all settings, not only Wi-Fi (see the Oct-19 update)
open-commitments: 3
open-questions: 0
---

# Wi-Fi provisioning by encrypted QR, and the install event gets sent home

Designed by [[wiki/people/pavel.md|Pavel Frolov]] on the [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md|Sept 7 2026 9:08 AM call]] (Russian), approved on the spot by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] ("Да. Отлично"), with a requirement attached by [[wiki/people/val-levitan.md|Val]]. It is the answer to a problem the hardware ruling creates: once [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md|the ports go wireless]], every screenless port needs the network name and password.

## The flow

- **Credentials are typed once, on Flex-Pay.** Pavel: "мы на [Flex-]pay… будет экран ввода… поиск сетей, выбор сети и ввода пароля" — a screen that searches for networks, picks one and takes the password [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **A QR is then generated and carried to each port.** "имеется возможность сгенерировать… QR… ты сканируешь… и подносишь к каждому из флекс портов, чтобы они тоже присоединились к этой сети. Чтобы не делать никакие [дополнительные] экраны ввода пароля прямо… на флекспорте" — so no password-entry screen is ever built on the Flex-Port itself [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Every device type already has a reader.** [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]: "QR код мы можем читать вот на нашем… сканером." Val, summarising: "[Flex-]порт[,] flex pay[,] flex IQ[ —] все устройства имеют QR" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **It must NOT be the ordinary phone network-sharing QR.** Pavel was explicit: "это должен быть не просто QR код, который вот на телефоне, когда ты делишься сетью[ —] он в незашифрованном виде отдаёт название сети и пароль. А нам… этот пароль всё таки надо каким то образом шифровать и уже потом на флекс па[р]те расшифровывать" — the password is encrypted in the QR and decrypted on the Flex-Port [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **One manual step survives, at the router.** Pavel: "1 раз взяв голый роутер[,] ты либо используешь его дефолтный пароль, либо ты должен зайти через веб интерфейс… задать новый… это всё равно ручная процедура один раз[;] дальше ты должен уже флекс[-пей] или флекс[-]айкью подключиться и ввести тот же самый пароль." [[wiki/people/andrey-bosik.md|Andrei Bosik]]'s router-QR-sticker idea, which would remove even that typing, stayed an open question on the hardware decision page [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## Val's telemetry requirement, attached to the same flow

Val: "коль мы это делаем, нам нужно тогда передавать себе тайм[,] d[a]t[e a]n[d] location stamp[ —] кто[,] когда, что подсоединил?… Плюс передавать серийные номера портов, которые по[дсоедин]или. И вообще, что где[,] когда установили." He framed the purpose as engineering and **onboarding** information, not compliance [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

Klimovich's objection was the current state: "у нас всё в офлайне, сейчас у нас вообще ничего наружу не передаётся, пока, насколько я знаю." Val's answer was the cell modem — "сейчас у нас уже стоит, у нас будет [LTE] модем, поэтому всё, что мы подсоединили[,] этот [QR-код] перенесли[,] все порты подсоединили[,] сеть заработала… мы всю эту информацию должны капча[ть] и передавать на свой сер[вер]" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

Pavel said the pipe already exists: "есть логирование данных, которые приходят… на клауд логинг сервер. И там… добавление отдельной какой то секции[ —] можно будет получать информацию о том… какие флекс порты, в какой момент подключились," reached "через графану" — **Grafana** [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]. Mechanically the port itself has no internet: "У него не будет интернета, он будет просто получать какие то [ивенты]… и у него есть коннект с флекс пэем. Вот в момент коннекта можно расширить сообщение и сказать, что вот это моё… соединение, я… в такое время присоединился" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

**The offline case is the part that costs.** Bosik: "это при условии, что… устройство в момент подключения имело доступ к интернету. А если интернета не было?… он где то должн[о] записать[,] прихоронить до момента выхода к интернету." Pavel agreed and said so plainly: "бесплатно это не получится, то[ —] все равно надо дорабатывать передачу" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## Update, Oct 15 2026 — the credentials now come from the location's dashboard page, and the QR is made there

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[wiki/people/pavel.md|Pavel]] described the flow differently: the access-point name and password are set on the location's page in the dashboard, beside the cashier and master PIN codes; Flex IQ, as its own access point, receives them from the cloud by modem; from a phone the installer generates a QR on that page and scans it on every Flexport, which binds the ports to that Flex IQ and sets the Wi-Fi. [[wiki/people/val-levitan.md|Val]] approved it and added registered installers, a test walk-through by phone and a first set-up record with date and time (the "location map") [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. Full record: [[wiki/decisions/2026-10-15-installers-set-up-a-location-by-phone-with-a-qr-code-from-the-location-dashboard-the-location-map.md]].

- **Against the title.** "Entered once on Flex-Pay" is replaced, for the own-access-point mode, by "set on the location dashboard". The QR hand-off to each port survives. Whether the QR is still encrypted was not discussed. With an external router Pavel still sees a manual step at the router's web interface — as on Sept 7.
- **Val's telemetry requirement** (who connected what, when, where) returns as the first set-up record. Pavel's Sept-7 commitments below are not reported done.

## Update, Oct 19 2026 — the settings QR is encrypted with a per-location key, made only by authorised staff; a plain QR is refused

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian; Val absent) [[wiki/people/pavel.md|Pavel]] set out the MVP 2 work "применения настроек" for Flex IQ and the Flex-Ports [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]:

- **What it carries.** The Wi-Fi access point and password, the order of networks ("модем или л т е"), and Flex IQ parameters such as PIN codes and binding — "короче большой список параметров" [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **Where it is made.** The QR is generated on a server page for the location. A user logged in as the location owner or as a technician bound to that location opens a page, runs "экспорт настроек", and the export opens as a QR [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **Encrypted per location.** "Этот QR код должен быть закодирован… ключом персональный для этого лакейшего"; the registered Flex IQ has its own key, decrypts on the fly when it scans, and applies the settings "скрытно" [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **When the QR is the only way.** Flex IQ can also get the settings over the network, but if Wi-Fi is its only network, it cannot get them without the QR; for the Flex-Ports the QR "будет единственный вариант передачи параметров, скорее всего" [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **A plain QR is refused.** [[wiki/people/anton-seregin.md|Anton Seregin]] had tried a Wi-Fi QR on a bank scanner: it beeps but nothing is processed at the kiosk. Pavel: it existed before, may have broken, "но не зашифровано. То есть это нас не устраивает" — anyone could press "поделиться сетью" on a phone, hold the QR to the terminal, "и он перестанет работать на реальной сети". "Только авторизованные персонал может такое сделать" [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **How to start.** Begin on the server side, collect the list of parameters, and perhaps first run a spike on how to organise it architecturally, including decryption on the Flex-Ports. The task is to be created for Seregin. [[wiki/people/alexei-khamin.md|Alexei Khamin]] asked whether terminals read a QR from a phone screen; Pavel: "Ну да… по крайней мере обычный QR" [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

The notes record it as Pavel's decision: "Settings QR for Flex IQ / Flex-Ports must be encrypted per location and created only by authorized staff on a server page; a plain Wi-Fi QR is not acceptable" [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

- **Against the Oct-15 update.** "Whether the QR is still encrypted was not discussed" on Oct 15 — now answered: yes, with a key per location. The page the QR comes from matches the Oct-15 location page. This restates Sept 7 (no plain phone QR) and widens the QR from Wi-Fi credentials to all device settings.
- **On the commitments below.** Pavel's Sept-7 build commitment is not reported done; the Oct-19 task is a step toward it. Both stay open.

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — build the Wi-Fi provisioning screens on Flex-Pay and Flex-IQ and the encrypted-QR handoff to the Flex-Ports, diagnostic screens included — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — extend the cloud logging to record connection and installation telemetry (time, date, location, port serial numbers, what was installed where), including store-and-forward when there is no internet at the moment of connection — due unspecified — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the server-side task for the encrypted settings QR (parameter list; maybe an architecture spike on decryption on the Flex-Ports) for [[wiki/people/anton-seregin.md|Anton Seregin]] to work — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

**§15.8:** clear — device telemetry design only; the captured data is installer/engineering event data, no named-person compensation.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
