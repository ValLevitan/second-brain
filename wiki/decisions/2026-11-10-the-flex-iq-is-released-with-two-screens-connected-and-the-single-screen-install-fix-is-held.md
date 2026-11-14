---
type: decision
title: The Flex IQ production install fails with only one monitor — at the hardware level an unplugged second HDMI screen acts like an unmounted SD card, so the installer fails, and a board started without it boots but raises no network interface; Pavel made a fix, but after talking with Andrei Klimovich it is not applied now — the release goes out with two screens connected and the problem is discussed later
date: 2026-11-10
aliases: [Flex IQ single-screen install failure, Flex IQ fails to install with one monitor, с одним монитором у нас не идёт, release with two screens, выпускать будем с 2 экранами, second HDMI acts like an unmounted SD card, black box with no network interface, черный неподключенный ящик, HDMI plug workaround, заглушка, boards from China]
source-count: 4
status: active
open-commitments: 1
open-questions: 2
---

# The Flex IQ is released with two screens connected; the single-screen install fix is held (Nov 10 2026)

**Where and who.** Reported at the [[wiki/meetings/2026-11-10-daily-standup-flex-iq-single-screen-install-failure-and-mvp2-release-november-20.md|Nov-10 Minsk stand-up]] (Russian; [[wiki/people/pavel.md|Pavel]] absent, [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] ran the round) by [[wiki/people/alexei-khamin.md|Alexei Khamin]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]. The ruling itself is Pavel's after talking with [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], passed on second-hand by Chudinov [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

## What was found

- On Nov 9 Khamin, with Chudinov, worked on installing production on the Flex IQ ("установки прода туда"); it would not install "потому что с одним монитором у нас не идёт" — "надо менять инструлятор вообще"; [[wiki/people/irina-shishko.md|Irina]]: maybe the board does not support it; Khamin: "или плата да или как, както мы обходить можем или не можем обходить" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].- Chudinov, on what he and Pavel worked out: at the board's hardware level, unplugging the second (HDMI) screen is "аналогично сигналу, размонтированный с декарта" — the installer fails; and if the screen is not connected from the start, the board "вроде как загружается, но они не подымают ни сетевый интерфейс и ничего" — "черный неподключенный ящик" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

## The ruling (as passed on)

"Паша там сделал фикс какой то, но… он там с Андреем переговорил. Пока эти фикси никуда не вносим выпускать будем с 2 экранами и дальше обсуждать что с таким делать." Kovalchuk named the Andrei: "Андреем климовичем" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

**Consequence if it is a board defect** (Chudinov): on all boards that came from the factory in China, installation is possible "только через 2 экран там либо с заглушкой" [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]].

## How it sits against earlier rulings

- The production install appears to be the MVP 1 release step set for Monday Nov 9 internally — [[wiki/decisions/2026-11-05-mvp-1-is-planned-for-monday-november-9-internally-and-the-client-is-told-wednesday-and-the-pyramid-bill-acceptor-is-tested-remotely-on-an-echo-cabinet-in-georgia.md]] (**inference** from the dates; the sources say only "production").
- Robust installation is one of the MVP 2 pillars — [[wiki/decisions/2026-11-05-mvp-2-is-kept-narrow-wi-fi-with-the-flex-iq-as-access-point-or-client-remote-flex-port-update-robust-installation-and-install-diagnostics-due-november-20-and-the-rest-goes-to-mvp-3-around-january-20.md]] (Nov-10 note there).

## Open questions

- Is the single-screen failure a defect of the Flex IQ boards from China, and if so is the answer always a second screen or an HDMI plug, or a fix to the installer? (Irina: "это вот потом следующим шагом") — [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]] — *partly answered Nov 11 2026: for the factory-firmware SD-card boot Pavel calls the HDMI dependence "хардварная проблема на платье" and plans cable flashing; the one-monitor production install itself is not discussed — kept open* — [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]

## Note, Nov 11 2026 — Pavel: the MVP 2 firmware installs over JVL's old firmware, but a board with factory firmware boots from the SD card only with an HDMI monitor — a board hardware problem; the first firmware will most likely be flashed by cable, as for the RK3576, and a production flashing document will be written

At the [[wiki/meetings/2026-11-11-daily-standup-flex-pay-to-mvp3-and-sound-names-in-lua-scripts.md|Nov-11 stand-up]] (Russian) [[wiki/people/alexei-khamin.md|Khamin]] asked who looks at terminals that do not flash from the SD card. [[wiki/people/pavel.md|Pavel]]: "Я это в понедельник закрыл… наша новая прошивка ну MVP 2, она будет нормально ставиться поверх старой нашей прошивки, но это не будет работать для заводской прошивки"; with factory firmware, "Раньше мы нажимали кнопку бут и подавали питание, и она с нашей с дкарты загружалась и ставилась. При условии наличия HDMI монитора без HD mi монитора это работать не будет… Это хардварная проблема на платье" — "мы будем думать в будущих релизах, как прошивать самую первую прошивку на плату с завода? Скорее всего, будем кабелем прошивать так же, как и для р к 35, 76" (heard; the notes read RK3576) [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. Khamin wanted it logged so it is not forgotten, perhaps for [[wiki/people/evgeniy-alekseev.md|Alekseev]] as the board specialist ("Алексеев там специалист по оплатам", heard — **inference**); Pavel: the task is closed, "мы просто будем делать новую какието документацию по тому, как расшивать плату на производство" [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. [[wiki/people/dmitri-chudinov.md|Chudinov]] asked about an HDMI plug; Pavel: "скорее всего подтянуть какимито резисторами можно… но я про это даже не думал" [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. This is the same HDMI-monitor dependence as the Nov-10 one-monitor install failure, seen at the factory-firmware stage (**inference** — the sources do not link them); it partly answers the open question below (Pavel calls it a board hardware problem).

### Open commitments (Nov 11 2026)

- [ ] Unassigned (Pavel: "мы… будем делать") — write a production document on how to flash boards that carry factory firmware — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]

### Open questions (Nov 11 2026)

- Could an HDMI plug or pull-up resistors let a factory-firmware board boot from the SD card without a monitor? (Chudinov; Pavel had not thought about it) — [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_IQ_Single_Screen_Install_Failure_and_MVP2_Release_November_20-November-10-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
