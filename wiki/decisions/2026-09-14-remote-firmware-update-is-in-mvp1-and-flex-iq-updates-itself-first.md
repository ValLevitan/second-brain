---
type: decision
title: Remote firmware update is in MVP 1 — Flex IQ and FlexPay update themselves first; distributing firmware to the Flex-Ports left MVP 1 on Sept 17, came back on Sept 28, and left again on Oct 15 — MVP 1 keeps only the Flex-Port update by USB stick, and remote Flex-Port update is MVP 2
date: 2026-09-14
aliases: [firmware upgrade in MVP1, remote FlexPort update moves to MVP2 again, USB-stick update is the only MVP1 gap, capability 146, PORT-13, remote FlexPort update back in MVP1, remote firmware update, OTA firmware, приоритет номер один это чтобы обновлялся флекс ай кю, flash the FlexPorts, Flex IQ to FlexPort protocol, доперфек, priority two deferred, FlexPort firmware by USB stick, capability 144 to MVP2, capability 144 cloned, no rollback, roll forward only, requirement 1367, IO board update on the fly, обновление ио барда]
source-count: 30
status: active — priority two (remote update of the Flex-Ports) left MVP 1 on Sept 17 2026 and RETURNED to MVP 1 on Sept 28 2026 (capability 146); rolling BACK to a previous build stays out of MVP 1 (Sept 18 2026); the delivery design is still open as of Oct 1 2026 (parked "to tomorrow" on Sept 30 and not taken up on Oct 1); see the dated updates below; Oct 15 2026: the IO board is to be updated along with Flex Pay and Flex IQ firmware; Oct 15 2026 (11:04 AM): remote update of the Flex-Ports moved to MVP 2 again — MVP 1 keeps only the USB-stick update, its one remaining gap (see the Oct-15 11:04 AM update); Oct 16 2026: remote update of the ports through Flex IQ confirmed as one of MVP 2's two tasks
open-commitments: 12
open-questions: 3
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

## Update, Sept 29 2026 — Pavel puts the Flex-Port firmware update through Flex IQ first, ahead of any Flex-Port emulation

At the [[wiki/meetings/2026-09-29-daily-standup-firmware-reissue-and-modem-gateway.md|Sept-29 Minsk stand-up]] (Russian) [[wiki/people/anton-seregin.md|Anton Seregin]] planned to open a feature for the Flex-Port, "[ч]тобы поизучать… [к]ак он будет [э]мулировать". [[wiki/people/pavel.md|Pavel Frolov]] redirected him: "**первостепенная это флекс айкью, [э]мулятор и особенно обновление прошивки флекспорта через флекс айкю**" — first the Flex IQ emulator, and above all the Flex-Port firmware update through Flex IQ [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

- **What "update" means here.** Seregin asked whether it is the device firmware or a scenario. Pavel: "**это имплементация протокола передачи самого файла[,] команды на то, чтобы начинай прошивку такого рода**" — the protocol that carries the file itself, and the commands that start the flashing [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **A very simple Flex-Port emulation is optional.** "какую[-]то простую эмуляцию флекспорта наверное можно было бы… но вот совсем просто должно быть" — at most something that answers commands, "уже… второстепенно" if Flex IQ can send the firmware-transfer commands and then "начинай или разрешаю тебе обновиться". Once those commands work, "это можно будет уже пробовать на реальном железе" — which Pavel finds "более… интересно" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].
- **A feature for it.** Seregin: "буду этим заниматься сегодня". Pavel: "я тебе тогда фича[:] проверка… [workflow] по передаче прошивки и непосредственно управления прошивкой" — a feature to check the firmware-transfer and firmware-control workflow. Seregin: "Заведу" [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]].

This sharpens the Sept-24 line above ("протокол обновления прошивок флекс портов" first) into a task with an owner on the Flex IQ side. Chudinov's and Pavel's commitments below are unchanged.

## Update, Sept 29 2026 (8:06 AM) — no Flex IQ install instruction exists; Elizabeth can see the Updates tab; "always the latest build", and tomorrow is the better day

At the [[wiki/meetings/2026-09-29-transactional-mvp1-setup-instructions-and-mikrotik-router.md|Sept-29 8:06 AM MVP 1 call]] (Russian) the Sept-28 SD-card plan for Georgia got its missing piece named [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]:

- **No instruction.** [[wiki/people/irina-shishko.md|Irina]] thought "дима говорил, какая то была инструкция, уже тоже готовая" for Flex IQ. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Инструкции нету… Ничего нет."
- **Elizabeth's access is checked.** "Мы проверили вчера с Сергеем у Элизабет доступ, и она увидит вкладку апдейтс" — with "Сергей" (not resolved) he confirmed the day before that [[wiki/people/elizabeth.md|Elizabeth]] sees the Updates tab. This answers the Sept-28 role question. What the instruction needs: "пару скринов, куда ей зайти, [с]качать", how to write it to an SD card, "[в]ставляйте, что нажимать". He suggested adding "как стереть секреты на терминале" — how to wipe the secrets on a terminal — "если… чтото не заработает сразу".
- **An old instruction as the base.** [[wiki/people/andrei-klimovich.md|Klimovich]]: an SD-card install instruction "которую когдато кто то сделал" exists (where it lies is garbled — "на гипсе"); "мы в своё время инсталлировали все [билды] на IQ. По этой инструкции она была достаточно подробной." He will find the link and post it in the chat; it can be moved to Confluence beside the port instruction and the machine set-up. Chudinov: "скидывай посмотрим… если что там чуть чуть добавится". Who updates it: "Я скину старую там ктото её подхватит, обновит" — not assigned.
- **Which build.** Klimovich asked for a build that works with the Flex-Port, "хотя бы проверку, чтобы сделать". Chudinov: the instruction will say "Берите всегда последний актуальный" — and this will be the standard instruction for every technician taking fresh, empty boards; all builds in the list are compatible, and "чем выше версия, тем больше фич или багов исправлено… смысла брать какойто более ранний нет". Irina sharpened Klimovich's question to *when* — today, tomorrow? Chudinov: "лучше уже, наверное, завтра сегодня будет там большая выкадка, там много чего уже добавили" — a large release lands today, so tomorrow.
- **Sequence for Georgia.** Klimovich: "нам тогда нужна инструкция по инсталляции на IQ… ваня ты в [Confluence] закинешь… свою инструкцию… и нам нужна ещё инструкция по прошивке флекспорта". "если у нас завтра всё готово, то Элизабет сможет сделать уже [первый] этап[,] мы посмотрим[,] как это всё будет работать." The full set-up plan is on [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-29 update).

Klimovich's Sept-28 commitment to have Elizabeth install by SD card is unchanged in substance; it now waits on the instructions (held on [[wiki/people/andrei-klimovich.md]]). Chudinov's Sept-28 role check is discharged on his page.

## Update, Sept 30 2026 — Flex IQ has nothing for Flex-Port updates yet; the delivery design is argued out between Pavel and Chudinov and parked to tomorrow; the port side stays with Alekseev

At the [[wiki/meetings/2026-09-30-daily-standup-flexport-firmware-delivery-and-network-loss.md|Sept-30 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]:

- **What Seregin found.** [[wiki/people/anton-seregin.md|Anton Seregin]], on the Flex-Port side of his Sept-29 task: "В этом флексе [IQ] как бы ничего нет эти обновления" — Flex IQ has nothing for Flex-Port updates; there is FlexPay code, "[н]аписан", but "Дима говорил, что он еще не тестировал его никак" (Chudinov, by context — his untested transfer scheme of Sept 24). "Мне не донимаю, что мне нужно будет сделать" — he does not yet understand what he must do.
- **Pavel doubts the week.** "по передаче прошивок на флекспорт я не знаю, сможем ли мы до конца недели это сделать." [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Времечко тут уже мало. Ну может суммарно с выходными, чтонибудь получится" — then "хотя бы обсудить, как мы это можем сделать".
- **Pavel's scope split.** "нам надо придумать способ… [п]ередачи файла на флекспорт. А дальше мы эту работу оставляем на Алексеева, чтоб он дальше на порте сделал" — the delivery method is theirs; what happens on the port is [[wiki/people/evgeniy-alekseev.md|Alekseev]]'s (consistent with PORT-13 staying with him on Sept 28). Chudinov: "нет, не я имею в виду бизнес логика."
- **The business logic, as argued.** Chudinov: a store holds "прошивку какойто версии"; "Кто решает, какую прошивку забирать всегда последнее терминал решает" (who decides — always the latest? the terminal?). Pavel: "мы с сервера должны иметь возможность отправить команду забери. Вот эту версию прошивки. Централизованно на киоск… для каждого [location]… актуальная версия такаято." Chudinov: then the server must also know what runs — "на каждом терминале показывать портов их прошивкой" — then say "[з]абери всем или каждому", and "ещё и время применения надо выстоять".
- **What the earlier version did.** Pavel remembered the port seeing new firmware on start, downloading and storing it, with a time given later. Chudinov: "там не было никаких времен ничего… Почтал сразу применил" (the first word is garbled; read as "скачал" — downloaded and applied at once), and in fact "открывали список портов и нажимали там типа [применить] прошивку" — an operator opened the port list and pressed apply. Pavel: "можем так и оставить… [л]ибо оператор нажимает кнопку, либо мы удаленно нажимаем кнопку, типа применить эти прошивки."
- **Chudinov's reservation.** "задача большая. Я с последним апдейтом не хочу заставлять ещё" — a big task he does not want forced in with the last update. Pavel: at least work out "способ доставки"; "кто тригерит обновления это следующая, и… обратная связь, то есть получили ли порты эти прошивки, какието статусы". Chudinov: "это основной [скоуп] работы."
- **Parked.** Pavel: "Ладно, поговорим завтра. Может, что придумаем?"

The derived notes read the exchange the same way and list it as "discussed but not decided; moved to tomorrow" [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]. **On the commitments below:** Seregin's Sept-29 task is in progress, not done; Pavel's Sept-29 feature for it was not mentioned; Chudinov's protocol work is now the open design above.

## Update, Sept 30 2026 (8:03 AM) — an old remote-firmware protocol document from January 2025 stays in Confluence; the Flex IQ SD-card instruction was in Confluence after all, and Chudinov writes the new one today

At the [[wiki/meetings/2026-09-30-transactional-mvp1-instructions-complete-and-modem-supply.md|Sept-30 8:03 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]:

- **The old document.** Beside the new Flex-Port instruction [[wiki/people/andrei-klimovich.md|Klimovich]] found "какойто старый [firmware document]… ревизия, последняя от января 25. Это уже не актуальный документ, правильно?" [[wiki/people/irina-shishko.md|Irina]]: everything else is outdated. [[wiki/people/pavel.md|Pavel]]: "здесь как раз прошивка это описание протокола прошивки удалённо не через провод" — it describes the remote (not wired) firmware protocol. [[wiki/people/dmitri-chudinov.md|Chudinov]]: "пока может пока оставить… когда будет ревизия, всего разберём" — leave it; sort it at the next revision.
- **The Flex IQ install instruction.** Klimovich posted the link to the old SD-card instruction: "Я ошибся это было не в гите как мне память подсказывал вчера это было тоже в [Confluence]." Chudinov: "я её сейчас взял в работу, я там инструкцию начал, я возьму часть твоих картинок касательно самого терминала. И распишу откуда там что берётся потом скину ссылку." Klimovich: "сегодня доделаешь" — "Да да". With that, "у нас тогда есть все 3 элемента инструкции" and Elizabeth can start tomorrow — see [[wiki/decisions/2026-09-09-negative-cases-first-and-flex-ports-tested-in-borrowed-non-jvl-machines.md]] (Sept-30 update).

The notes match [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]].

## Update, Oct 5 2026 — the remote update works and is rolled out to a terminal; one terminal's TITO printer stops printing, cause unknown

At the [[wiki/meetings/2026-10-05-transactional-mvp1-port-screens-unclaimed-money-and-printer-models.md|Oct-5 8:01 AM MVP 1 call]] (Russian), [[wiki/people/andrei-klimovich.md|Klimovich]] asked [[wiki/people/dmitri-chudinov.md|Chudinov]] for the status of the remote update. Chudinov: "Работает пока… выкатываем, накатывается на терминал есть один момент". On one terminal the TITO printer stops printing: "не могу сказать, связанных с апдейтом, либо нет… это просто он, потому что через сутки демон поток засыпает, не просыпается, либо связано с апдейтом. Не получается пока словить причину. Она 2 раза воспроизвелась… с прошлой недели больше не воспроизводилось" [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]. *Which update is meant (Flex IQ's own, or the Flex-Ports' through it) is not said; "накатывается на терминал" suggests the terminal (Flex IQ) — inference.* The derived notes read it the same way [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — continue the Flex-Port firmware-delivery discussion: the delivery method first, then who triggers an update and how the ports report back — due Oct 1 2026 ("поговорим завтра") — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: not taken up at the stand-up; the Pavel–Chudinov exchange that morning was the SAS-mode flag ([[wiki/decisions/2026-10-01-sas-or-no-sas-is-set-per-flex-port-on-the-flex-iq-set-up-screen-and-sent-at-registration-with-the-pin-code.md]]), and Chudinov's next item is capability 241 (machine information and command-log forwarding), not delivery* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — finish the Flex IQ SD-card install instruction (reusing Klimovich's terminal pictures, explaining where each piece comes from) and send the link — due Sept 30 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]] — *Oct 1 2026: not mentioned at either call; Klimovich said "мы уже всё на руках у нас есть" for the Georgia check* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]

- [ ] [[wiki/people/anton-seregin.md|Anton Seregin]] — work on the Flex-Port firmware update through Flex IQ (file-transfer protocol and the start/allow commands) in the Flex IQ emulator, with a very simple Flex-Port emulation only if needed — due started Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]] — *Sept 30 2026: in progress — he found nothing in Flex IQ for Flex-Port updates and untested FlexPay code; "не донимаю, что мне нужно будет сделать"* — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]] — *Oct 1 2026: not mentioned; his report was the Flex IQ emulator's verification against the device* — [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create the feature "проверка workflow по передаче прошивки и… управления прошивкой" for Seregin — due Sept 29 2026 — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — work the Flex IQ ↔ Flex-Port firmware-distribution protocol from his side, and improve it if he can — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — deliver firmware update in MVP 1 to a production standard, with pings, verification and a timer — due with MVP 1 — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open questions

- **Why does the TITO printer on one terminal stop printing — the remote update, or a print daemon that sleeps after a day and does not wake?** Seen twice, not since the week before Oct 5 — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]

- **How does Flex-Port firmware delivery work in business terms?** Who decides which version a port takes (server command per location, or always the latest), whether the server shows each port's current firmware, when an update applies, who presses "apply" (operator or JVL remotely), and how the ports report back — argued on Sept 30, not decided — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- **Where does the January-2025 remote-firmware protocol document belong?** Left for the next revision — [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- ~~**Is Evgeniy Alekseev actually assigned to this?**~~ Pavel's own wording was hedged — "**возможно… по[-]моему там на него тоже задача висит**" — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]. **Answered Sept 28 2026:** the firmware-delivery story PORT-13 is on him, and Val kept it with him — [[raw/Meeting_Transcript_Transactional_MVP1_Remote_Updates_and_October_15_Target-September-28-2026.md]]
- ~~**Whether capability 144 itself now carries an MVP 1 or MVP 2 fix version.**~~ **Answered Sept 18 2026:** the capability was **cloned** — the trimmed original stays in MVP 1, the clone carrying the removed requirements goes to MVP 2. See the Sept-18 update above — [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — product scope and task assignment only; no compensation or performance judgement for any named person.

## Update, Oct 9 2026 — USB-stick updates run through RAUC and the old updater repo is archived; a re-used terminal must wipe its secrets to get new cloud-update certificates; the bootloader does not work on the new boards

- **USB and RAUC.** At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 stand-up]] Biratka said the update from a USB stick works the same way as the remote update, through RAUC, checked on Flex Pay hardware; a full reinstall is by micro-SD. Chudinov did not build bundle download for the stick — bundles roll out remotely. See [[wiki/decisions/2026-10-09-the-old-usb-updater-repository-is-archived-because-rauc-now-does-usb-updates.md]] [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Secrets wipe.** On the [[wiki/meetings/2026-10-09-transactional-mvp1-test-machines-and-unclaimed-funds.md|8:01 AM call]] Chudinov: a terminal registered before keeps its old secrets, so "мы не создадим новые сертификаты для. Обновление через облако" — see [[wiki/decisions/2026-10-09-a-terminal-registered-before-must-wipe-its-secrets-and-the-install-instruction-says-so-in-red.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].
- **The bootloader on new boards.** Khamin: "На новых платах ничего не работает"; the fix from the firmware memory changes is not in the repository. Pavel will write to the developer ("алексеевым" — Alekseev by context, **inference**) [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]].

## Update, Oct 14 2026 — for the 15th the Flex-Port update must work at least by USB stick; Alekseev promised a build that evening

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian) [[wiki/people/pavel.md|Pavel]] said he had caught [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] two days before ("От Евгения Алексеева я его всётаки выловил. Позавчера") and reminded him: "у нас к релизу 15 числа надо, чтобы работало обновление софта на flex портах хотя бы через ю с бстик." Alekseev "обещал выкатиться версию сегодня вечером." The first thing on the morning of the 15th is to check that the port firmware goes by USB — "это больше для лёши" ([[wiki/people/alexei-khamin.md|Khamin]]). Without it "мы вообще как бы обновлять порты не в состоянии будем. Только он там кабелем прошивать" [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].

This fits the Sept-17 fallback above (a USB stick when remote update is not ready) and the Oct-9 RAUC route. Whether the Oct-14 build is the bootloader fix for the new boards (Oct 9) is **not said**.

### Open commitments (Oct 14 2026)

- [x] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — release the Flex-Port build that updates firmware by USB stick — due Oct 14 2026 (evening), as promised to Pavel — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]] — *Oct 15 2026: Alekseev sent his branch on the night of the 15th and said to test it; it does not build on GitHub, so Khamin rebuilds from fresh main with his memory-chip changes. That this is the promised USB-update build is an **inference** (Irina tied it to the check due on the 15th); left open until a source shows the USB update working* — [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]] — *Oct 15 2026 (11:04 AM): still not working; the branch is red and could not be merged from fresh main; closed as superseded (not discharged) by his Oct-15 commitment to merge main into his branch (below)* — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [x] [[wiki/people/alexei-khamin.md|Alexei Khamin]] and [[wiki/people/pavel.md|Pavel Frolov]] — first thing in the morning, check that the Flex-Port firmware update works by USB stick — due Oct 15 2026 — [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]] — *Oct 15 2026 (11:04 AM): could not be done — no buildable branch; closed as superseded (not done) by the Oct-16 check below* — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Update, Oct 15 2026 — the IO board is to be updated too, along with the Flex Pay and Flex IQ firmware; Alekseev's branch does not build

At the [[wiki/meetings/2026-10-15-daily-standup-offline-ris-fallback-and-nova-game-conversion.md|Oct-15 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]:

- **The IO board.** [[wiki/people/alexander-biratka.md|Biratka]] asked how the IO board is meant to be updated. [[wiki/people/pavel.md|Pavel]]: before, it was flashed at installation and not touched on the fly afterwards. For the payment terminal there is no obligation not to change firmware on the fly, "поэтому, наверное, надо поддержать… Наряду с с прошивкой флекса pay флекса IQ иметь возможность ещё и платы обновлять, если они так умеют." The notes record it as Pavel's decision: "Support IO board firmware updates together with Flex Pay and Flex IQ firmware" [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]. It sits in capability 135; the requirement exists but needs refining (detail: [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Oct 15). This widens the remote-update scope from Flex IQ, FlexPay and the Flex-Ports to the IO board as well, "if the boards allow it" — **evolution**, not a contradiction.
- **Alekseev's delivery.** Pavel had told Alekseev on Monday that the function must be checked on the 15th; Irina: he sent it on the night of the 15th and said "проверяйте". His branch was cut long ago and does not build on GitHub; Pavel: branch from fresh main and pull in his memory-chip changes; [[wiki/people/alexei-khamin.md|Khamin]] does it. Separately, Khamin built and installed the production FlexPort firmware; cash-out and crediting work. Whether either build updates by USB stick is **not said**.

## Update, Oct 15 2026 (11:04 AM) — remote Flex-Port update leaves MVP 1 again; the USB-stick update is MVP 1's one gap, and Alekseev must merge main into his branch

At the [[wiki/meetings/2026-10-15-wi-fi-router-switch-power-loss-battery-and-mvp2-scope.md|Oct-15 11:04 AM Wi-Fi meeting]] (Russian) [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]:

- **The state.** [[wiki/people/pavel.md|Pavel]]: the Flexports are flashed with a programmer and work, "но у нас нет возможности обновить прошивку не через флэшку, не [remote]". The software was written by "Евгения Алексеев, Евгений яворский", and the changes for the new chips are not checked. [[wiki/people/irina-shishko.md|Irina]]: "мы и проверить не можем, потому что его нет у нас." Val: because the code is not in the repository.
- **The move.** Pavel: "наверно нам надо будет тогда планировать [remote] апдейт портов на следующий MVP". Val: "То есть [remote] апдейт портов мы переключаем на MVP 2." Irina: "да." Pavel: "Но оно и было у нас так" (it was already like that). Until then, JVL comes physically with a stick. [[wiki/people/andrey-bosik.md|Bosik]]: a visit with a stick is needed anyway, to add the update function to the ports; Irina: once at production, then a second time.
- **What MVP 1 lacks.** Val: "всё, что сейчас не хватает в [MVP] один это… [USB] апдейт на флекспорты. А в MVP 2 мы включим уже [remote] апдейт [на] flex порты." Pavel: "Да." Val's recap: "в течение… трёх до 5 дней должно закончиться."
- **What Alekseev must do.** Pavel: merge his branch into main correctly — no conflicts; the processor boots into bootloader mode, takes the update from a USB stick, flashes, the new version comes up and the update function stays active, so it can be updated again; and the build must run on GitHub Actions, "не у него на компьютере". Prose and contracts: "Прозу мы сами обновим… Тоже не проблема". Irina: his PR exists but the branch status is red; "Лёша" ([[wiki/people/alexei-khamin.md|Khamin]], by context — **inference**) tried to merge it from fresh main and failed — "ветка отрезана чёрти когда тысячу лет назад"; so Alekseev must take main into his branch, check it and fix conflicts. This replaces the morning plan for Khamin to rebuild it.
- **Then.** Pavel: Lyosha syncs the capability (now on Alekseev; it speaks of fewer memory chips) with a requirement that USB-stick flashing still works after the chip change, and tests by hand: "здесь авто тесты не работают, здесь надо реальные тесты с реальной флешкой." Val: push Alekseev, then Lyosha. Pavel: Alekseev should manage it over the weekend; if he marks it ready to merge, they check "завтра с утра".

The derived notes record: "MVP1 lacks only the FlexPort USB-stick update; remote update for FlexPorts moves to MVP2. (Val, Pavel, Irina)" [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]. **Against the title:** the Sept-28 return of remote Flex-Port update to MVP 1 is undone — the title is updated. Flex IQ's own remote update is not affected. The MVP 2 list is on [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]].

### Open commitments (Oct 15 2026, 11:04 AM)

- [ ] [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — merge main into his Flex-Port memory-chip branch, fix the conflicts, check that the USB-stick update works and stays active after an update, and make it build on GitHub Actions — due about Oct 18–20 (Val: 3 to 5 days) — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] / [[wiki/people/alexei-khamin.md|Alexei Khamin]] (inference) — check Alekseev's work if it is ready to merge — due Oct 16 2026 (morning) — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]] — *Oct 16 2026: not reported at the stand-up; Khamin said only that a feature for Alekseev's branch exists and its capability is in progress* — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] (inference) — sync the Flex-Port capability with the requirement that USB-stick flashing still works after the chip change, and test it by hand with a real stick — due after Alekseev's merge — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — update the prose and contracts for Alekseev's code — due after Alekseev's merge — [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]

## Update, Oct 16 2026 — remote port update through Flex IQ is one of MVP 2's two tasks; Biratka takes the loader task FP 1335; a feature for Alekseev's branch

At the [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct-16 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]:

- **MVP 2.** [[wiki/people/pavel.md|Pavel]]: MVP 2 holds "исключительно" Wi-Fi and "ремонт апдейт портов через fex IQ" (remote update of the ports through Flex IQ), for the next three weeks. This matches the Oct-15 move of remote Flex-Port update to MVP 2 — **consistent**, not new. Detail: [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Oct-16 update).
- **Biratka — FP 1335.** "Взял работу ф п 13 35. Этот лодер для ivда." He needs at least read access to the firmware repository "Его барда" and will request it. The notes: "a loader; board name unclear in the transcript" [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]. On Oct 15 the IO-board update requirement was heard as "13, 35 задача… Апдейт"; that FP 1335 is that IO-board loader is an **inference**.
- **Biratka — Flex Pay updates through the hub.** He must add parameters to the Terminal Hub "для Того, чтобы можно было короче, flex pay обновлять через. Хап наш"; he can do it himself with repo access. Pavel: Biratka creates a task for adding the parameters to the Terminal Hub project, with git access to that repository.
- **Khamin — Alekseev's branch.** "По флекспорту с изменением Алексеева ветка там для поддержки хип оф памяти тоже заведена фича вроде с правильным родителем… к побилити тоже взял в прогресс." Whether Alekseev merged main into his branch, or whether the USB-stick update was checked "завтра с утра" (Oct 16) as planned, is **not said**.

### Open commitments (Oct 16 2026)

- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — create a task to add the Terminal Hub parameters so Flex Pay can be updated through the hub, and request git access to the Terminal Hub and to the FP 1335 board firmware repository — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]] [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]

## Update, Oct 19 2026 — the IO board firmware built in CI runs on Biratka's board but not yet on gaming machines; the flashing is now in the board service; a flash-and-roll-back test is next

At the [[wiki/meetings/2026-10-19-daily-standup-clover-fortune-on-nova-and-encrypted-settings-qr.md|Oct-19 Minsk stand-up]] (Russian; Val absent) [[wiki/people/alexander-biratka.md|Biratka]] said he has two tasks in work: the IO board firmware update, and checks of the Terminal Hub connection, including attempts to spoof it — for example a terminal connecting with a fake number. Part of the cloud hub changes are done by "Андрей" (not named in full — **not identified**) [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

- **"Never checked on hardware."** Claude told him the IO board firmware built in CI "ни разу не запускали на из железы, это прямо написано в ридме" of the repository. [[wiki/people/pavel.md|Pavel]]: the board in Biratka's Flex Pay is already flashed with that CI build; it was not properly tested on gaming machines, so there may be nuances [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].
- **What remains.** Biratka added the flashing process into the service that manages the board; the remaining step is to build a version with a change (for example the version number), flash it and roll it back through that service [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

*(The roll-back here is a test of the IO board flash path; whether it touches the Sept-18 rule that rolling back to a previous build stays out of MVP 1 was not discussed — **inference** only.)* The Oct-16 Terminal Hub task above is not reported done.

### Open commitments (Oct 19 2026)

- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — test the IO board firmware update and roll-back through the board service with a build that changes the version — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]

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
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Reissue_and_Modem_Gateway-September-29-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Setup_Instructions_and_MikroTik_Router-September-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Firmware_Delivery_and_Network_Loss-September-30-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Instructions_Complete_and_Modem_Supply-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Mode_Flag_and_Feature_Status_Rules-October-1-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Offline_RIS_Fallback_and_NOVA_Game_Conversion-October-15-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Notes_WiFi_Router_Switch_Power_Loss_Battery_and_MVP2_Scope-October-15-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP2_WiFi_Scope_and_Modem_MAC_Rollback-October-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
