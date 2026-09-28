---
type: decision
title: Remote firmware update is in MVP 1 — Flex IQ and FlexPay update themselves first; distributing firmware to the Flex-Ports left MVP 1 on Sept 17 and came BACK into MVP 1 on Sept 28, when the date moved to October 15
date: 2026-09-14
aliases: [firmware upgrade in MVP1, capability 146, PORT-13, remote FlexPort update back in MVP1, remote firmware update, OTA firmware, приоритет номер один это чтобы обновлялся флекс ай кю, flash the FlexPorts, Flex IQ to FlexPort protocol, доперфек, priority two deferred, FlexPort firmware by USB stick, capability 144 to MVP2, capability 144 cloned, no rollback, roll forward only, requirement 1367]
source-count: 9
status: active — priority two (remote update of the Flex-Ports) left MVP 1 on Sept 17 2026 and RETURNED to MVP 1 on Sept 28 2026 (capability 146); rolling BACK to a previous build stays out of MVP 1 (Sept 18 2026); see the dated updates below
open-commitments: 2
open-questions: 0
---

# Remote firmware update is in MVP 1, and Flex IQ updates itself before it updates anything else

> **Read the Sept-17 and Sept-28 updates below before relying on the second half of this decision.** Priority one (the gateways updating themselves) still stands and is confirmed. Priority two (updating the Flex-Ports remotely) was moved out of MVP 1 on Sept 17 and **brought back into MVP 1 on Sept 28**, once the MVP 1 date moved to October 15.

Settled at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept 14 2026 12:04 PM call]] (Russian). [[wiki/people/val-levitan.md|Val Levitan]] set the requirement; [[wiki/people/pavel.md|Pavel Frolov]] set the order of work.

## The requirement

Val put it as non-negotiable and left the device open: "**нам обязательно в MVP один… То ли это касается IQ, то ли киоска, то ли флэкспорта — нам нужно [firmware upgrade]**" — it must be in MVP 1, whether it concerns IQ, the kiosk or the Flex-Port [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The transcript renders the capability as "**forwaprade**" and later "**фейервер**" — garbles of "firmware upgrade" / "firmware". The derived notes head the section "Firmware over-the-air update"; **the words "over the air" and "remote" are the notes' gloss, not Val's** — he names the capability without saying how it travels. Recorded as the source has it.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

And the quality bar, twice over: "**это дело нужно допи[лить] доперфек[т], это должно быть проф[екшен]**" — it has to be taken to perfection, it has to be production. What he wanted inside it: "**все там [нодес] там какието. Пинги кудато? Какието верификации, вот таймер — всё, чтобы вот это [firmware] и верификация должна работать**" — **pings**, **verifications** and a **timer**, and the verification has to work [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The derived notes list this as "verification, timer, confirmation". **"Confirmation" is not in this passage** — the transcript has "пинги" (pings); Val's word "подтверждение" (confirmation) comes later in the call, about ticket printing, not firmware. Corrected here against the source.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## The order of work

Pavel accepted the direction — "**Ну да, да, мы на это и идём**" — and split it in two [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

1. **Priority one — the gateways update themselves.** "**Приоритет номер один — это чтобы обновлялся флекс ай кю и флек[с]pay**."
2. **Priority two — the gateways update the ports.** "**приоритет номер 2 — это уже, чтобы они могли раздавать прошивки для флекспортов и их прошивать**" — so they can distribute firmware to the Flex-Ports and flash them.

This sits on top of the device scope already fixed for MVP 1 — Flex IQ alone, no kiosks — on [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]], and it is the mechanism behind the same-day 8:01 AM ruling that nobody downloads and installs builds by hand ([[wiki/decisions/2026-09-14-nobody-downloads-and-installs-builds-thirty-day-target.md]]).

## Who does it

Pavel named the sequence of people, not just of tasks: "**сначала её сейчас дима чудинов проработает со своей стороны. Может быть, какнибудь там улучшить протокол? Общение между флекса IQ и портами — и, возможно, как раз по этой задаче нам понадобится Алексеев, ну по[-]моему там на него тоже задача висит**" — [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] works the Flex IQ ↔ Flex-Port communication protocol from his side first and may improve it; [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] may be needed on the same task, and Pavel thinks a task is already assigned to him [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(§4 resolutions: "дима чудинов" → **Dmitri Chudinov**, the back-end architect (the derived notes render the Belarusian spelling "Dzmitry Chudzinau"); "Алексеев" → **Evgeniy Alekseev**, the embedded-code owner who works on Genadi Peari's hardware-adjacent projects — the registry's Zhenya-by-context rule, and the fit is exact here.)*


## Update, Sept 17 2026 — priority two leaves MVP 1, and a USB stick does it instead

At the [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept-17 8:02 AM call]] the team went through [[wiki/people/andrey-bosik.md|Bosik]]'s capability 144 — the master that would let the Flex-Ports "**отправлять их телеметрию, обновлять их ф[ё]рв[а]ры и идентифицировать их… в клауде**" — which [[wiki/people/pavel.md|Pavel]] had moved up into MVP 1 before the call. **It came back out.**

- **[[wiki/people/irina-shishko.md|Irina Shishko]]'s argument carried it:** "**Обновить можно из флешки[,] 6 штук — это не проблема[;] мы 3000 машин обновляем с флешки**" — six Flex-Ports off a USB stick is not a problem when JVL already updates 3,000 machines that way. [[wiki/people/andrei-klimovich.md|Klimovich]] added the correction that sharpened it — "**обновляем не мы[;] обновля[ют] те техники владельцев машин**" — and accepted: "**[MVP] один согласен, это мы переживём**". Irina closed it: "**значит, убираем на MVP 2**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **Priority one is explicitly unaffected.** Asked directly whether anything still updates remotely, [[wiki/people/dmitri-chudinov.md|Chudinov]] answered "**IQ в [MVP] один будет обновляться**" — Flex IQ updates in MVP 1 [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **A condition was attached in exchange**, and it is a logging condition, not a firmware one: Klimovich required that MVP 1 still make it visible that a device is not working "**чтобы хотя бы была информация, что надо ехать с этой флешкой**" — so that at minimum somebody knows to drive out with the stick [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **Requirement 1413** — the specific "deliver updates through a master node and keep the images where the Flex/kiosk firmware already lives" requirement — was moved to the MVP 2 parking capability in the same pass [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

The full sweep, including what happened to capability 144's own label, is on [[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]].

**The Sept-14 commitments below are unchanged in substance but narrowed in scope:** the Flex IQ ↔ Flex-Port protocol work Chudinov took on Sept 14 is now MVP 2 work for the distribution half, while the gateway self-update remains MVP 1. Neither was restated or discharged on Sept 17, so both stay open.

## Update, Sept 18 2026 — rolling *back* is removed from MVP 1 outright, and capability 144's fix version is settled by cloning

Two things at the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept-18 8:03 AM call]] finish the picture this page has been carrying.

**1. The rollback requirement is out of MVP 1, and the team's policy is roll-forward only.** [[wiki/people/dmitri-chudinov.md|Chudinov]] named requirement **1367** under **capability 122** as the one he could not build — the database schema moves with the code, so an older build meets a schema it does not match and may come up empty or not at all. [[wiki/people/andrey-bosik.md|Bosik]] turned it into policy ("**надо придерживаться всегда форвард**") and [[wiki/people/val-levitan.md|Val]] wrote in the chat to remove it. **This does not touch priority one above — Flex IQ still updates itself in MVP 1.** Full argument on [[wiki/decisions/2026-09-18-no-rollback-to-a-previous-build-and-the-team-rolls-forward-only.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**2. Capability 144's own fix version — the open question below — is answered, and the answer is "both, on two objects".** [[wiki/people/irina-shishko.md|Irina Shishko]] proposed **cloning** the capability rather than moving requirements out one at a time: the trimmed original keeps a handful of requirements and **stays in MVP 1**, the clone holds the rest and **goes to MVP 2**. [[wiki/people/andrei-klimovich.md|Klimovich]] did it live — "**Клон я закину на MVP 2**". 144 then reappears in the MVP 1 feature-planning walk on the same call. Detail on [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Neither Sept-14 commitment below was mentioned on Sept 18**, so both stay open — Chudinov's protocol work and Pavel's production-standard firmware update (pings, verification, timer) went unraised, as did the open question about whether [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] is assigned.

## Update, Sept 22 2026 — the MVP 2 move restated, and doubted in practice

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 Minsk stand-up]] (Russian), [[wiki/people/dmitri-chudinov.md|Chudinov]] warned time is very short "если сейчас захотят апдейты на флекспорты". [[wiki/people/pavel.md|Pavel]]: "Так вроде же уже принято решение, что дейтэфлекс портов идут на ревизию. Ой на версию MVP 2." Chudinov: "Я не знаю… каждый день мы получаем новый список." This confirms the Sept-17 move above as Pavel's understanding; Chudinov's reply is a complaint about changing lists, not a reversal [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Update, Sept 22 2026 (8:01 AM) — the Flex IQ half is closed

Three hours later, at the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|8:01 AM MVP 1 call]], [[wiki/people/dmitri-chudinov.md|Chudinov]] offered it as the good news of the date argument: "Самое верхнее [капабилити] 122 сегодня закрыто это ремоут апдейтс", and he would test it now. Pavel confirmed which one: "Ремонт апдейт флекса… флекс айкью" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. So **the Flex IQ self-update capability, 122, is closed as of Sept 22** — the same capability the 4:48 stand-up saw In Progress with all features closed and tests pending ([[wiki/topics/test-automation-strategy.md]], Sept 22). The Flex-Port half stays in MVP 2.


## Update, Sept 23 2026 — Flex-Port firmware named as the emulator's most critical use

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian), Pavel said the most critical use of the kiosk emulator is "обновление прошивок для флекспортов", so the work can be handed to [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]]. He described the flow as he remembers it: new firmware placed in a set location becomes available, a connected Flex-Port sees it and downloads it "по своему протоколу". [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

- **Not a reversal of the Sept-17 MVP 2 move.** Pavel did not say which MVP this serves. Recorded as spoken.
- **On the open question below:** Alekseev is again named as the intended user, but no one assigns him. The question stays open.
- The emulator detail is on [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] (Sept-23 update).

## Update, Sept 24 2026 — how firmware reaches the device is not defined yet, and a spike is proposed

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **The Flex-Port firmware protocol comes first.** Pavel, on the Flex IQ emulator: "Необходим в первую очередь именно протокол обновления прошивок флекс портов", as its own feature. He said this is "более приоритетно даже сейчас". He did not say which MVP it serves. Recorded as spoken; it does not by itself reverse the Sept-17 MVP 2 move above.
- **Chudinov would revisit his own scheme.** Asked whether the team keeps the firmware-transfer scheme he built: "Я бы я бы пересмотрел". It was not properly tested — Pavel: "никто не тестировал, Кроме тебя". Chudinov does not know if the current port-to-IQ contract still holds, and the server side is different now: "там с друг бокс Загрузка всё там уже точно по другому" (read as a Dropbox-style download — **inference**).
- **Pavel's conclusion:** "способ доставки прошивки на флекс ай на флекс пэй пока не определён. Ну то есть не сделан." The open part is the step where firmware sits on the FlexPay and is handed to the ports.
- **A spike, proposed.** Pavel: give [[wiki/people/anton-seregin.md|Anton Seregin]] a spike on how the current contract covers the needed function, and whether to change it. Chudinov wanted to feed the finished work to an AI first, to see if it finds faults. His answer to the spike itself is unclear in the transcript.
- **The same behaviour for firmware update.** Pavel: "для обновления прошивки… это будет одинаковое поведение, чтоэкспорта, что с флекса айкюл" — read as FlexPay and Flex IQ (**inference**; the first device name is garbled).

**On the commitments below:** Chudinov's protocol work is not discharged — he now proposes to rethink it. Pavel's production-standard commitment was not raised.

## Update, Sept 28 2026 — remote Flex-Port update comes back into MVP 1, and PORT-13 stays with Alekseev

At the [[wiki/meetings/2026-09-28-transactional-mvp1-remote-updates-and-october-15-target.md|Sept-28 8:02 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]:

- **Pavel reopened it.** The plan was Flex IQ updates in MVP 1 and port updates not; "такое плохая практика, наверное", and with MVP 1 moving to October 15, "можем постараться сделать и обновление флекспортов к этой дате". Val checked the earlier ruling: "мы решили флекс порты не обновлять [н]а MP один, но обновлять на м в пи 2" — Pavel: "Да да".
- **Klimovich agreed.** The USB-stick plan ("надо было бы приехать физически в эти 10 локаций") "казалось, окей" within MVP 1; with October 15 the real date, "я поддерживаю".
- **Val added it.** "Так давайте тогда поменяем… Добавим" into MVP 1. Irina named the capability: "Capobility 146".
- **PORT-13 stays with Alekseev.** Pavel: part of the tasks "[с]тояла на алексееве, но поскольку он работает только в выходные", and offered to take "порт 13 по доставке новой прошивке на flexport" himself; his port tasks are done and he expects the RK3576 board ("рк 35, 76") this week. Val asked why, then: "Я бы оставил бы это алексееву." Pavel accepted.
- **The dashboard exists.** For Flex IQ, Chudinov showed the terminal-management Updates tab: the device list with OS and application versions (Minsk's two Flex IQ terminals), the builds list with SD-card installers, and update campaigns with per-terminal status. Terminals made before the new certificates cannot be updated remotely; they first get the new software by SD card and will likely ask to re-register. New builds come out daily. Dev, staging and prod are separate; a staging terminal moves to prod only by SD card. A FlexPay tab will sit next to the Flex IQ one later.
- **Georgia is the first remote test.** Klimovich: the Georgia Flex IQ on remote access with a KORE SIM is "отличный пример". [[wiki/people/elizabeth.md|Elizabeth]] installs the latest build by SD card; then remote update is tested on it. Khamin and Biratka suggested installing the previous build and updating remotely to the newest.

**On the open question below:** it is answered. Alekseev carries the firmware-delivery story PORT-13, and Val kept it with him. **On the commitments below:** not discharged. Pavel's production-standard update (pings, verification, timer) and Chudinov's protocol work now serve MVP 1 again.

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — work the Flex IQ ↔ Flex-Port firmware-distribution protocol from his side, and improve it if he can — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — deliver firmware update in MVP 1 to a production standard, with pings, verification and a timer — due with MVP 1 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open questions

- ~~**Is Evgeniy Alekseev actually assigned to this?**~~ Pavel's own wording was hedged — "**возможно… по[-]моему там на него тоже задача висит**" — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]. **Answered Sept 28 2026:** the firmware-delivery story PORT-13 is on him, and Val kept it with him — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- ~~**Whether capability 144 itself now carries an MVP 1 or MVP 2 fix version.**~~ **Answered Sept 18 2026:** the capability was **cloned** — the trimmed original stays in MVP 1, the clone carrying the removed requirements goes to MVP 2. See the Sept-18 update above — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — product scope and task assignment only; no compensation or performance judgement for any named person.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
