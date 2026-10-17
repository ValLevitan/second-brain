---
type: decision
title: Flex IQ gets a switch — its own Wi-Fi access point or an external router; MVP 2 starts with the switch and an external router, and the router moves inside JVL hardware in MVP 3 or later
date: 2026-10-15
aliases: [router or Flex IQ access point, Flex IQ as access point, свой точка доступа или внешняя, переключатель режим роутера, router mode or client mode, switch between access point and router, router moves inside in MVP 3, MVP 3 4 or 5 router inside, soldered Wi-Fi chip on the RK3568, not industrial grade Wi-Fi chip, antenna in the plastic cover, Bosik Wi-Fi spike, separate JVL Wi-Fi unit, Wi-Fi always included]
source-count: 2
status: active
open-commitments: 2
open-questions: 4
---

# Flex IQ gets a switch: its own access point or an external router

Settled at the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) by [[wiki/people/val-levitan.md|Val]], with [[wiki/people/pavel.md|Pavel Frolov]] agreeing and [[wiki/people/andrey-bosik.md|Andrei Bosik]] proposing the form [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Where it started

- **The earlier choice.** Pavel: at earlier meetings "принимали решения, что на локешене будет ставиться роутер с вай фай", because a router has its own antennas and a better signal than almost any module JVL could fit. Bosik: it is also simpler — a ready product, no own code; a small router on the ceiling covers a room of about 40 square metres on 2.4 GHz [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. That choice is [[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]], with the brand on [[wiki/decisions/2026-09-29-mikrotik-is-the-location-router-and-val-leaves-the-brand-to-the-team.md]].
- **The router is only local Wi-Fi.** Val thought the payment terminal reaches the outside through the router. Pavel: "он напрямую он не через роутер, он через [LTE] модем." Val: "Тогда зачем роутер нужен?" Pavel: as the Wi-Fi access point. Bosik: also as the DHCP server; that can be put on JVL's terminal, but he "бы не смешивал эту функцию" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. The modem-in-every-terminal rule is on [[wiki/decisions/2026-09-15-every-device-carries-its-own-lte-modem-and-sim.md]] (Oct-15 update).

## Val's challenge

"Я понимаю, что легко пойти купить раутер. Но это стоит деньги, это надо устанавливать к этому надо вести какието провода" — "это индустриальная система". He listed the install burden: a router "под потолок" needs permission first (Irina: "Разрешение получил"), a worker with a ladder, at least a power cable, and the router will end up "около какойто глухой стенки", not where JVL wants it [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Flex IQ as the access point — the facts

- **It can be done.** Pavel: "Без роутера может выступать в качестве точки доступа сам флекса айкью. У него есть модуль вай фай, его можно поднять в режиме точки доступа." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **The chip is weak and fixed.** Pavel: the module is "довольно таки какой то там старый", reliability "явно не не индастриал грейд". It cannot be chosen: "он запаян на материнской плате" — "это ж китайское рк 35 68 готово" (the ready-made RK3568 board). A supplier would fit another chip only for a paid custom board [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **A better module is possible.** It would most likely be a USB device on a cable; or JVL makes a new version of its interface board with its own module soldered on. Pavel: the motherboard has 4 USB connectors ("беленькие разъёмчики"), and USB can also be routed on the interface board [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **The antenna.** Bosik: the terminal may sit in one corner and a machine in the far corner, about 15 m away (Pavel and Val's figure). Val: an antenna fits "очень элегантно" in Flex IQ — "мы сейчас оттуда сняли 2 экран… и закрываем его пластиковой крышкой. В эту пластиковую крышку можем [антенну] завернуть." Bosik: or around the screen inside the frame, as in laptops; the task is to choose a module that takes an external antenna [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **The software.** Bosik: the OS and the app must make the device a router — NAT, DHCP and DNS. Pavel: "Don'n s ему не надо"; it "не выглядит слишком сложной задачей" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Same chip elsewhere.** Val: Alekseev has already laid out Wi-Fi on the port boards (not tested yet); Flex Pay carries the same chip as Flex IQ — Bosik: "Все то же самое там" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## The ruling

- Val: this is "более индустриальный подход", is it not? Pavel: "Я не уверен… я бы не отказывался от 2 варианта… Настраивать прямо на флекс айкью выбрать вариант. Свой своя точка доступа или внешняя точка доступа." Val: "Хорошо… Я согласен с этим." Bosik: "Переключатель такой сделать, что режим роутера, либо режим этого." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **Val:** "тогда в MBP 2 сделаем вот этот переключатель сначала. И будем использовать внешний [роутер]… MBP 3 или 4 или 5, мы уже этот раутор внесём вовнутрь, хотя бы у нас будет уже логический шаг и продуманное решение… Договорились." Pavel: "Согласен." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **Restated later.** Val: in MVP 2 "мы пока включаем просто переключатель. И ставим раутор"; in MVP 3 the own solution and the router goes. Pavel: "Может быть даже [M]VP 2 лучше сразу закладываться под 2 решения" — run the own access point with its own set-up screen in parallel, "за неделю можно сделать". Val moved on to another topic; this was **not confirmed** [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- The derived notes record the same decision, "Decided by Val, agreed by Pavel", and Pavel's parallel idea as not confirmed [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Val's separate Wi-Fi unit — raised, not adopted

Val asked, "не в своём амплуа", whether JVL should leave the on-board chips alone and build its own unit — Wi-Fi, an amplifier, its own cell modem and a battery. Pavel: "по факту мы сделаем свой роутер"; ready open-source designs and boards exist. Bosik: it "увеличит стоимость конечному заказчику"; a Wi-Fi module in the existing terminal is "существенно дешевле" — "отдельное устройство пока бы не планировал." Pavel: first test the current module, "возможно, что это всё надумано"; fewer devices may mean higher reliability. Bosik: but if the terminal fails, nothing works — "Резервирование надо тогда" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Notes for later

- **Several devices at one location (MVP 3).** Pavel: when Flex Pay and Flex IQ each have their own modem and access point, they must agree "кто главный". Bosik: the same switch answers it — router mode or client mode [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **A router stays the fallback.** Pavel: where Flex IQ stands "за углом" and no good link is possible, plan a harder install — a router prepared in advance with its password, placed where Flex IQ and all ports can see it [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **Wi-Fi is "probably included".** Bosik asked whether Wi-Fi is an option for the customer. Pavel: "Скорее включена… для нас это дешёвый апгрейд всей системы, а для инсталляции это не тянуть провода это большой бенефит." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Where it sits

- **Evolution, not a reversal.** The Sept-7 external router stays the MVP 2 path; the new part is the switch and the plan to move the router inside later. On Sept 7 Val had himself proposed using JVL's own device and withdrawn it; this time the idea comes back as a planned later step ([[wiki/decisions/2026-09-07-wi-fi-module-on-flex-port-with-an-external-router.md]], Oct-15 update).
- Installer set-up fits the own-access-point mode best — [[wiki/decisions/2026-10-15-installers-set-up-a-location-by-phone-with-a-qr-code-from-the-location-dashboard-the-location-map.md]].
- Wi-Fi heads Val's MVP 2 list — [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — spike: connect an antenna to the current Wi-Fi module, run it as an access point with several Flexports (about 4) in parallel and phones, and measure range and signal — due about one week (Pavel: "можешь даже ты сделать там в течение недели") — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] Unassigned — build the Flex IQ switch (own access point or external router) for MVP 2 — due with MVP 2 — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Open questions

- In the long run, is Flex IQ's own access point better than an external router? Pavel: "Я не уверен" — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- Should MVP 2 build the own-access-point mode in parallel (Pavel), or only the switch and the router (Val)? — [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- Which Wi-Fi module and antenna, if the soldered RK3568 chip is not good enough — USB module, or a new interface board? — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- Is Wi-Fi always included, or an option for the customer? Pavel: "Скорее включена" — not ruled — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear — product design and equipment only. **§15 #9:** clear — Wi-Fi names and passwords are discussed as a design matter; no value was spoken.

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
