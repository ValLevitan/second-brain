---
type: decision
title: Every payment terminal gets a swappable backup battery read by the main processor through a BMS, so it can report "power lost" and service can be called if power does not return — and a lost link is retried for seconds, then alerted, logged and counted
date: 2026-10-15
aliases: [backup battery in payment terminals, power-loss alert, исчез пауэр, power lost flag, BMS, battery management board, battery in the Flex IQ stand, swappable battery pack, three-year battery, UPS in the kiosk stand, 12 V battery, zero downtime, no reconfiguration after a power cut, сами обратно себя найти, retry then alert, date stamp on every drop, devices that drop often get replaced, Flexport red out of service, link up link down events, we need Genadi]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# Payment terminals get a backup battery and report power loss

Worked out at the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) by [[wiki/people/val-levitan.md|Val]], [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/pavel.md|Pavel Frolov]] [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Val's starting rule — no downtime, no reconfiguration

Val: all these decisions are made "с понятием, что у нас не может быть даун". Bosik: downtime can only come from a power cut. Val: even then, when power comes back, "мы должны сами обратно себя найти, мы не можем каждый раз делать реконфиг[урацию]." Bosik: of course — devices find each other and reconnect after boot, "само собой разумеющиеся вещи". Val wanted it in the tasks: "это будет [zero downtime]" (garbled; the notes read zero downtime) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## From a battery on the router to a battery in the terminal

- **Val first asked for a battery on the router.** Bosik: such routers exist, but a cheap UPS is cheaper ("раньше… самые простые там 30 $40 стоили" in Belarus); then the machines and Flex IQ would need UPS power too. Pavel: then one UPS powering both router and Flex IQ. Val: that makes the install much longer — wires to bring together in one place [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **The router cannot send the alert.** Val's purpose: be told the power is gone and, if it does not come back, call service — "пример через 15 минут". Bosik: "у нас маршрутизаторы они без интернета. У нас интернет непосредственно на самих терминалах через модем". A MikroTik could be scripted to create events, he added, "но… как мы будем на эти события реагировать?" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **So the terminal.** Val: Flex IQ has the cell modem; put in "небольшую батарею… 2 минуты… или 5 минут"; the screen can go dark while the inside holds on and sends "что исчез пауэр" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **What exists today.** Bosik: Flex IQ already sees the interface state (link up / link down) and sends it to the log when it loses the network; "мы не обрабатываем события потери электричества" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## The design that was agreed

- **Where it goes.** Bosik: the Flex IQ stand is hollow — a battery fits there and makes it stand more firmly. Pavel: "Там можно огромный аккумулятор засунуть"; about four cells would last "5 10" minutes [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **A BMS the processor reads.** Bosik: a charge controller is needed — Pavel: "Б м с." Pavel: "надо, чтобы с этим контроллером умел говорить наш основной процессор, чтобы он читал состояние" — for example that 20% charge is left [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Val's flow.** With the battery, Flex IQ can say it no longer sees the ports or the router and is waiting for power; it may report the battery level ("на 30% … 70%"); and if power is not restored, "вызываете сервис" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Swappable, with a record.** Bosik: the pack must be replaceable; it lives "в среднем… 3 года", by his experience. Pavel: ideally it clicks out from below. Val: then diagnostics are needed — when a new battery went in and when the next is due. Bosik: "Завяжем клиентов на свой запчасти." Val: "мне нравится такой подход". Pavel agreed [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **All payment terminals, not only Flex IQ.** Val: "мы аккумулятор, и все эти предупреждения мы вводим на [Flex] IQ" — but what if a location has no Flex IQ? Bosik: add it to all terminals. Pavel: payment terminals are Flex Pay, the recycler, the Flex dispenser — "всё, что может общаться с игроком или с кассиром для выдачи денег или карт". Val: "мы добавляем этот функционал… по всем" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Two forms.** Pavel: a portable device gets a small battery with its own charging, power and event circuit; a kiosk on its own stand has room below for a ready-made UPS. Bosik: an ordinary 12-volt battery, the kind used in motorcycles, changed by two clamps. Val: the battery then most likely belongs in JVL's own power supply ("паршу пар", garbled — **inference**); Pavel: "Возможно да." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **Genadi is needed.** Pavel: "Да тут нам нужен уже Геннадий" — [[wiki/people/genadi-peari.md|Genadi Peari]], for the battery hardware [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

The derived notes record it as a decision of Val, Andrei Bosik and Pavel: payment terminals get a backup battery and power-loss alerts, the battery swappable with a BMS the processor reads [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Val's rules for a dropped link

Val: a link can drop from static, a spike, anything. "Вопервых, сразу об этом оповещать не нужно. Нужно постараться [ре]конект… в секунды. Тогда нужно оповещать." Every event gets a date stamp; if the same device drops often, it must be replaced, and that goes into a report or dashboard; presumably pings run between devices all the time [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

**What the Flexports do today.** Pavel: on losing the host (Flex IQ), in about 2 seconds ("или там 5 секунд. Я не помню точно") the small lamp goes from green to red with "аутов сервис, ноу коннекшнс… с хостом"; they keep trying to reconnect and, once the host is back, return to work and clear the error by themselves [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

*(The "retry, then alert" order is Val's requirement; whether alerts and per-device drop counts already exist anywhere is not said — inference: the counting and reporting part is new.)*

## Where it sits

- It answers, at the design level, Val's Sept-15 demand for non-functional requirements on devices that fall off the network ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]) and adds power loss to the remote-visibility line of [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]].
- The alerts are cloud data — [[wiki/decisions/2026-10-15-service-diagnostics-go-to-the-cloud-with-role-based-access-not-to-the-local-screen.md]].
- Which MVP carries the battery is not said. *(Inference: it is not on Val's MVP 2 list the same day.)*

## Open commitments

- [ ] Unassigned (Pavel: "нам нужен уже Геннадий") — bring [[wiki/people/genadi-peari.md|Genadi Peari]] in on the battery and BMS hardware — due unspecified — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Open questions

- What does JVL do when a power-loss alert arrives — call the location? Bosik asked; Val: first decide what goes into the architecture, the procedure comes later — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- Which MVP carries the battery and power-loss alerts? Not said — [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear — equipment and market prices only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
