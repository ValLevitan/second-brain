---
type: decision
title: The game sound library is rewritten in Rust on PulseAudio and lives in the engine, not the LGS — the LGS drives it through an API; the Kira library is dropped for now; the existing FMOD sounds are converted by a tool from FSB to FLAC with JSON descriptions, so Vlad's work is kept and he can go on with his own tools (Pavel, Biratka and Daniil Stauskiy, Nov 2 2026)
date: 2026-11-02
aliases: [sound library in Rust, Rust sound library, PulseAudio sound library, Kira dropped, FSB to FLAC, FMOD sounds converted, JSON sound description, sound library lives in the engine not LGS, самодостаточный пульс аудио, библиотека на расте, маленький конвертер]
source-count: 8
status: active
open-commitments: 2
open-questions: 3
---

# The sound library is rewritten in Rust on PulseAudio inside the engine; Kira is dropped; the FMOD sounds are converted (Nov 2 2026)

Settled at the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov 2 2026 Minsk stand-up]] (5:15 AM Eastern, Russian) by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/alexander-biratka.md|Alexander Biratka]] on [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]]'s report of his spike [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. It closes the "which sound library?" question left open on [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Oct-29 and Oct-30 notes), where Anton Leshkevich had recommended Kira and Daniil had found no free library that fully replaces FMOD.

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What Daniil found

- **Kira is out, for now.** "От киры… решила отказаться пока что, потому что не выводят звук на разную колонки типа на верхнюю и нижнюю только на дну да и не имеет свой системы эвентов" — it cannot send sound to different speakers (top and bottom) and has no event system of its own; it would save only "200 строк кода" while the output stream would have to be rewritten anyway [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **PulseAudio instead.** "с помощью полиса аудио" there will be one ready library ("одна Готовы… библиотека") that can be put into the LGS and that plays sound "и на венде, и на армию" — on Windows and on ARM [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **Rust.** "Сейчас мы переписываем в репозиторе звука на rast" — the sound repository is being rewritten in Rust [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **Conversion.** Pavel: a self-contained PulseAudio — "Все, что было сделано на fode [FMOD], можно будет конвертировать"; Daniil: "Все звуки да" — one tool, a converter, "он сейчас есть"; the sound format becomes FLAC instead of FSB ("не ф с б, а флаг"), and the description of a sound — how it reacts, to which parameters — becomes a JSON file ("jess формат") instead of the old companion files [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].

## The ruling

- **Vlad keeps his tools; JVL converts.** Pavel asked whether Biratka had talked to Vlad; no — "влад может даже и… не знать про это всё дальше продолжать работать со своими Системами"; it changes nothing for JVL: "Просто конвертируем свой формат… Маленький конвертер" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. ("Влад" is the author of the existing game sounds by context; the wiki ties that Vlad to [[wiki/people/vladislav-gurin.md|Vladislav Gurin]] only through a June-2025 source — not confirmed here.)
- **The library lives in the engine, not the LGS.** Biratka: "библиотеку, которую мы будем писать… для звука она будет, скорее всего, находиться в движке. Сейчас не в эл j [LGS]"; the LGS must be able to control it through some API — with a websocket inside the app the two sides can talk both ways, so the LGS can play a sound in setup or change the volume; "потребителем и пользователем звука является у нас в любом случае движок" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. Pavel's question why websockets if PulseAudio can talk through internal channels was answered as app-level LGS-to-engine communication, not audio transport [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **One language.** Biratka: what Daniil made "надо, наверное, будет переписать под раст Чтобы уже все было… На одном языке написано" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **Pavel's close.** "тогда рождается отсюда из спайка уже переделка, реально библиотеки на расте, да" — the spike becomes the real rewrite of the library in Rust [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. The notes record it as decided by Pavel, Alexander and Daniil [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **Leshkevich** thanked Daniil for trying Kira, which he had recommended without trying it himself [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].

## How it sits against earlier rulings

- On Oct 30 Daniil had found no free library covering all that the 13 FSB banks need, and Biratka wanted the finished game sounds kept rather than redone — [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Oct-30 note). Nov 2 keeps them by converting FSB to FLAC plus JSON, and replaces the player rather than the sounds. **Evolution** of the Oct-30 open question, not a contradiction.
- Nov 3: Daniil continues "переношу Библиотеку звуковой на раз [Rust]" — [[wiki/people/daniil-stauskiy.md]] (Nov 3).

## Open commitments

- [ ] [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]] — rewrite the sound library in Rust on PulseAudio, with the FSB → FLAC + JSON converter — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]

## Open questions

- Which API the LGS uses to drive the engine's sound library (Biratka: "какойто там IPI, я не знаю"; a websocket if one exists) — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Note, Nov 4 2026 — the pull request is open; NC-1 can be closed

At the [[wiki/meetings/2026-11-04-daily-standup-release-build-handoff-and-nad2-product-code.md|Nov-4 stand-up]] (Russian) [[wiki/people/daniil-stauskiy.md|Daniil]]: on the rewrite of the sound repository in Rust "я уже открыл пиар", after solving a few problems; he also closed dependency requests; the parent "н ц один" (heard; NC-1), with all child tasks done, can be closed — Pavel: "Думаю, что можно закрывать… новое вроде не планируется"; Daniil has no task now and Pavel and Biratka will find him one tomorrow [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]. The commitment above is not shown merged, so it stays open.

## Note, Nov 5 2026 — the sound board: left speaker and subwoofer work, the right channel is silent; Pavel's goal — sound returns after a sound-card power loss without a reboot

At the [[wiki/meetings/2026-11-05-daily-standup-new-engine-capabilities-and-georgia-handpay-tilts.md|Nov-5 stand-up]] (Russian) [[wiki/people/daniil-stauskiy.md|Daniil]] has no task created yet and is working "со звуковой платой. Я уже проверил сейчас левая колонка из сабвуфе работает, а вот на правую колонку почемуто звук ещё пока не выводится. Ну будут смотреть, разбираться." [[wiki/people/pavel.md|Pavel]] set the aim for the future framework: if the sound card has a problem — "питание там пропало, что если её назад вернули, включили?" — "Чтобы у нас звук просто. Прозрачно появлялся на играх без каких то? Необходимости перегружать машину то, как, например, на старой машине." Daniil: "Ну да" [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]. Biratka suggested Daniil could take a limited engine capability once his sound tasks run out — [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]] (Nov-5 note).

### Open commitments (Nov 5 2026)

- [x] [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]] — get the right channel working on the sound board, and make sound recover after a sound-card power loss without rebooting the machine — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]] — **discharged Nov 6 2026:** "на 2 колонках работается" and, after pulling the USB and the power from the sound board, "при подключении звук восстанавливается, воспроизводится"; Pavel: "Отлично отлично то что надо" — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]

## Note, Nov 6 2026 — sound on both speakers but quiet; the 85% master-volume slider on the old Flex cabinets; sound comes back after a USB and power pull; the overload case that only a reboot cured

At the [[wiki/meetings/2026-11-06-daily-standup-modem-off-confirmation-capability-and-cap-287-in-mvp2.md|Nov-6 stand-up]] (Russian) [[wiki/people/daniil-stauskiy.md|Daniil]]: "Samsung [heard] уже проверил на 2 колонках работается… играет, почему то тихо причём… сам по себе усилитель точно работает, потому что звук то выводится на Колонки"; the sound banks hold the same loudness as before in the LGS; "Я по сути через пульс аудио могу его усилить… он как бы будет погромче звучать, но я просто не знаю как бы так должно, либо усилитель сам по себе уже должен усиливать до такой степени". [[wiki/people/pavel.md|Pavel]]: on the old Flex cabinets "выставлялся ползунок мастер громкости… не в максимум… 85 знак процента. И она влияла на этот общий звук"; Daniil: the old FMOD library ("вмодовская") passed sound through PulseAudio too, "а я именно на ну на Ростовской [Rust] библиотеке проверял". The old crash where the LGS fell when another board was unplugged: "сейчас я и ю с б вытягивал и питание отключал именно с платы звуковой. Потом при подключении звук восстанавливается"; Pavel: "Отлично отлично то что надо". [[wiki/people/alexander-biratka.md|Biratka]] asked how the old sound problem reproduced; Pavel: one case was a too-loud start — the amplifier ("ванпли", heard) went into reboot, the sound vanished and "Устройство с USB по моему пропадало тоже и до следующей перезагрузки… не возвращался… Вряд ли мы эту проблему решим"; perhaps track the case where the USB device stays but the audio path shuts down from overload "чтобы мы могли перенициализировать… Но если у нас не будет USB устройства, то мы с этой платой ничего не сделаем. Ну либо какойто внешний его джедок [watchdog]" [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]. The right-channel problem of Nov 5 is not mentioned; "на 2 колонках работается" is read as resolved (**inference**).

### Open commitments (Nov 6 2026)

- [ ] [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]] — sort out the quiet sound on the RK3576 board (boost in PulseAudio, or the amplifier) — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]

### Open questions (Nov 6 2026)

- Quiet sound: boost the signal in PulseAudio, or should the amplifier do it (and does the 85% master slider of the old cabinets apply)? — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- Can an audio-path shutdown from an amplifier overload be detected and re-initialised while the USB device remains, and is an external watchdog the only answer when the USB device vanishes? Pavel: "над этим можно будет подумать" — [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_New_Engine_Capabilities_and_Georgia_Handpay_Tilts-November-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Modem_Off_Confirmation_Capability_and_CAP-287_in_MVP2-November-6-2026.md]]
