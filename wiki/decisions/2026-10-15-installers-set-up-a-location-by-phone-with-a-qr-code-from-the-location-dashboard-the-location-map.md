---
type: decision
title: Installers set up a location by phone — a QR code generated on the location's dashboard page is scanned on each Flexport, binding the ports to that Flex IQ and setting the Wi-Fi; installers are registered with JVL, the set-up is walked through and tested by phone, and the first set-up is recorded with a date and time (the "location map")
date: 2026-10-15
aliases: [location map, лакейшн map, location topography, installer set-up by phone, QR code from the location dashboard, scan the QR on each Flexport, bind Flexports to the location's Flex IQ, foreign Flexport cannot join, registered installers, все должны быть к нам подписаны, first set-up record with date and time stamp, reverse install record, Wi-Fi name and password set from the dashboard, PIN codes on the location page]
source-count: 4
status: active
open-commitments: 0
open-questions: 1
---

# Installers set up a location by phone, with a QR code from the location dashboard

Proposed by [[wiki/people/pavel.md|Pavel Frolov]] and approved by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## The problem Val set

Val: "для меня весь финт" is that everything arrives, is set up, power is switched on, and the devices "друг с другом… поговорили, договорились и подключились." [[wiki/people/andrey-bosik.md|Bosik]]: not quite — the ports must be told the access-point name, or else other devices could join; only if preset at the factory. Pavel did not like one setting for the whole fleet [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Pavel's plan

- **On the location page.** When a location is created in the dashboard, PIN codes for the cashier and for the master access are already set there; "Там же иметь возможность настраивать название точки доступа и пароль. На той же странице." [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- **Flex IQ gets it from the cloud.** With its own access point it is simple: Flex IQ connects to JVL's cloud by modem, and the configured location passes it the PIN codes and the access-point name and password [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **A QR for the ports.** "Через веб интерфейс… к нашему [location]… генерируем QR код" — from a phone, press generate, get a QR, "прошли по всем [Flex]портам отсканировали этот QR код. Тем самым мы привязали порты именно к этому [location]… с этим флекс ай кю и сказали название точки доступа… и… пароль" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **It also legitimises the ports.** Pavel: the same step means a foreign Flexport brought in without binding to the location cannot join JVL's Flex IQ automatically [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Val's approval and his additions

- "На телефоне… мне очень нравится, потому что все кто делают установки наших портов все должны быть к нам подписаны. Я хочу знать, кто они такие." With that he can have direct contact with all of them ("Я могу тогда иметь прямую связь со всеми"); what he would offer them is garbled ("Предложить им быть Антон апдейт leest" — perhaps an update list, **inference**) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **His use case.** Everything arrives at the location, is unpacked and powered; the installer opens the phone app, logs in to the portal, sees what is at this location and says "вот эти 5 вещей подключить, а 6 [лишняя]"; then a confirmation; then a test run by phone through every stage — hold the phone here, read this, scan the QR on the screen or on the reader. "Тогда мы знаем… где подключилась" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- **The first set-up record.** Val: usually JVL sends data to the location; here JVL receives it and fixes it — "вот с этого мы начали наш [location]. Какого то числа дейт тайм [стэмп]… Вот это был начальный сет[ап]". He first called it a passport or a reverse install record; Pavel: "Скорее это лакейшн map какой то." Val: "Мап хорошо" — or "топографию" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].
- Pavel: "примерно так мы себе и представляли" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

The derived notes record it as a decision, "Proposed by Pavel, approved by Val" [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## It fits the own access point best

Pavel: the phone scheme "хорошо ложится в вариант, когда у нас точка доступа на flex IQ", because JVL sets it remotely and everything works by itself. With an external router someone still has to enter the router's web interface — "нужен уже человек немножко более умный или опытный" — or the router needs some protocol through which JVL can hand it the network name and password. Bosik: with a third-party router the technician picks the network and types the password from the sticker on the back; either way someone walks round each Flexport with the QR [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. Pavel also confirmed the Flexports are powered from the machine [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]].

## Why install speed matters to Val

Bosik asked for customer feedback. Val: "я думаю, что с января месяца взорвётся"; he now mostly watches how Felipe and Andrei talk with customers. With the second revision, with Wi-Fi, "мы улетим вперед". Today, for other makers' systems, an install takes "2 человека… 03:00" on site (read as 3 hours) plus about an hour's drive each way; "я думаю, что это больше" [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. *(Inference: a phone-and-QR set-up is how JVL expects to beat that.)*

## Where it sits

- It changes **where the Wi-Fi credentials come from** in [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]]: on Sept 7 they were typed once on Flex Pay and carried to the ports by QR; now, for the own-access-point mode, they are set on the location's dashboard page and the QR is generated there. The QR hand-off to each port survives. Whether the QR is still encrypted was not discussed (Oct-15 update there).
- Val's first-set-up record builds on his Sept-7 requirement to send home who connected what, when and where (same page).
- The switch between own access point and external router — [[wiki/decisions/2026-10-15-flex-iq-gets-a-switch-between-its-own-access-point-and-an-external-router-and-mvp2-starts-on-the-router.md]].

## Note, Oct 19 2026 — the QR is encrypted per location

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian) [[wiki/people/pavel.md|Pavel]] settled what Oct 15 left open: the QR made on the location's server page is encrypted with a key personal to that location, only the location owner or a technician bound to it can export it, and a plain phone network-sharing QR is refused. It carries all settings (Wi-Fi, network order, PIN codes, binding), not only Wi-Fi [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]. Detail: [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-19 update). The open question below (third-party routers) was not taken up.

## Open questions

- How are the Wi-Fi name and password set on a third-party router without a skilled installer? Pavel named the gap — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

**§15.8:** clear — install effort is a market observation about other makers, no one's pay. **§15 #9:** clear — PIN codes, network names and passwords are discussed as fields on a page; no value was spoken.

## Sources
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
