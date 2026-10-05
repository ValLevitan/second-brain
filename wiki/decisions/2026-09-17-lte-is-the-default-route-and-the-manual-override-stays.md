---
type: decision
title: LTE is the default route and the manual override stays — automatic route priority waits for Wi-Fi in MVP 2
date: 2026-09-17
aliases: [requirement 1405, route priority, route metric, LTE first then LAN then Wi-Fi, metric zero, basement location, manual connection priority, admin settings connection priority, зачем это приоритезировать руками, в подвале где-то]
source-count: 3
status: active
open-commitments: 0
open-questions: 1
---

# LTE is the default route; the manual override stays, and automatic priority waits for Wi-Fi

Settled on the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept 17 2026 8:02 AM call]] (Russian), working through [[wiki/people/andrey-bosik.md|Andrey Bosik]]'s network list requirement by requirement. The requirement is **1405** — spoken by [[wiki/people/irina-shishko.md|Irina Shishko]] as "14, 05" when she opened it [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## What Bosik wrote

Route priority expressed as metrics: "**должен быть у маршрут[ов] приоритет… с нулём всегда должен быть л[]т[]е модем, чтобы весь трафик шёл через него**", and then "**с десяткой… [LAN], с двадцаткой вай фай**" — **metric 0 = the LTE modem**, **metric 10 = LAN**, **metric 20 = Wi-Fi**. His stated intent for the wired leg: when a device is attached by Wi-Fi or LAN, that link is preferred "**для работы с внутренними [хостами] внутри сетей**" — for talking to hosts inside the local network — while the internet always goes out over LTE [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(The metric-10 leg is garbled on the recording; LAN is read from the surrounding sentence and from Bosik's own ordering, and is recorded as an inference.)*

This is a device-level statement of the standing architecture that every JVL device carries its own LTE modem and SIM ([[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]]).

## What already exists, and the argument that kept it

[[wiki/people/andrei-klimovich.md|Klimovich]] said the capability is already shipped on Flex IQ — "**у IQ сейчас… в админ[ ]сетингах есть уже приоритизация коннекта, есть выбор лана, есть выбор л[]т[]е, и можно их приоритизировать**": the admin settings already let a technician prioritise LAN against LTE by hand [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

Bosik's objection was that it should not need a hand: "**Зачем это приоритезировать руками, если это должно приоритезироваться в принципе автоматической системы?**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]

**[[wiki/people/pavel.md|Pavel Frolov]]'s counter carried it, and it is a field argument, not an engineering one:** "**для каких[-]то лакейш[е]нов может быть л[]т[]е вообще не работает. Вот в подвале где[-]то[,] и тогда им придётся проводной. А если у тебя эта [логика] прибито гвоздями, ты ничего не сделаешь**" — in some locations LTE does not work at all (a basement), the location then has to run on wire, and a hard-nailed priority leaves the technician no way out [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

[[wiki/people/dmitri-chudinov.md|Chudinov]] proposed the middle: "**[По] дефолт[у] будет стоять на л[]т[]е[,] так логично**" and "**Я бы дефолтами это сделал**" — do it by defaults. Bosik accepted in two words: "**Окей, согласен**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

## The ruling

Klimovich closed it: "**то, как мы сейчас проговорили, оно уже работает, не надо ничего в [MVP] один пока менять[;] в [MVP] 2 вернёмся к этому вопросу**" — what exists already works, nothing changes in MVP 1, the question comes back in MVP 2 [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. The derived notes summarise the same outcome as "make LTE the default, leave the manual override, revisit with Wi-Fi in MVP2" [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**The reason MVP 2 is the right place is Wi-Fi.** Bosik immediately qualified his own acceptance — "**Частично работает, потому что вай фай сценарий не покрываем пока ещё**", and "**точно должно быть автоматически то, что когда у тебя вай фай и кабель подключен**" — the automatic case that genuinely needs solving is Wi-Fi and cable connected at once, and Wi-Fi is not in MVP 1. Pavel and Irina both put it in the second release: "**когда вай фай будем делать во 2 этом, да[,] то там мы будем рассматривать**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

That is consistent with the Wi-Fi work already being owned by Bosik and sequenced second ([[wiki/decisions/2026-09-07-andrei-bosik-drives-the-wi-fi-work-and-the-process-chain.md]], [[wiki/decisions/2026-09-09-wi-fi-is-second-in-urgency-and-october-november-run-wires.md]]).

## Update, Sept 29 2026 — with the modem as default gateway, the progressive link keeps dropping and broadcast traffic leaks to the modem

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian) [[wiki/people/pavel.md|Pavel Frolov]] reported what "группкой людей" found the evening before: "**когда у нас включен модем, он является дефолтным гитлеем. У нас прогрессив перестает работать**" — with the modem switched on it becomes the default gateway and the progressive stops working. "**Получается, что нам надо это держать в уме и для всех наших транзакшнл продуктов**" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

- **[[wiki/people/evgeny-kharetski.md|Kharetski]] corrected the symptom.** "**не так… это мне не перестать работать просто. Он постоянно реконнектится, у них теряет связь и восстанавливает**" — the progressive does not stop; it keeps losing and restoring the link, though the signal looked fine. His lesson: "**на эту сеть полагаться для каких то коммуникаций долгосрочных нельзя**" — that network cannot be relied on for long-lived connections. [[wiki/people/alexander-biratka.md|Biratka]]: it reconnected and carried on; it just has to be allowed for [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **Shadow traffic.** Pavel's second point: with the modem as default gateway, "**пакеты, которые там всякие бруткастые, которые не на конкретные айпишника… в первую очередь будут пытаться уйти на модем и создавать нам теневой трафик**" — broadcast packets not addressed to a specific IP go out to the modem first and create shadow traffic. He wants to cut them off and send them to the internal network [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]. *(This bears on the Sept-28 log-traffic figure on [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]] — a link made here, not on tape.)*
- **What he will try.** On the machine Kharetski and Ivan are working on: filter the ports the progressive controller uses — "**порты, по которым работает прогрессив контроллер… отфильем и скажем, что посылает только на внутреннюю сеть**" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **Terminals have the same shape of problem.** A terminal "попытается отправить в модем, ничего не получит. В ответ ну перейдёт на другую сесть" — it tries the modem, gets nothing, falls back to another interface; "не совсем проблемка", but "надо… в будущем разобраться и сделать правильно" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

This is a data point against the Sept-17 ruling above, not a reversal: LTE stays the default route, and the finding is that local traffic (progressive, broadcast) must not follow that default. No decision was taken; see the open question.

### Open question (Sept 29 2026)

- How to keep broadcast and progressive-controller traffic off the modem on machines and on terminals when the modem is the default gateway — Pavel will try port filtering on one machine; no design or owner beyond that — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]

**§15.8:** clear — network configuration only; no named person's pay, rate or performance judgement appears. **§15.9:** no IP address, APN, credential or SIM identifier value was spoken; the discussion stays at the level of route metrics and interface names.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
