---
type: meeting
title: Daily stand-up — Clover Fortune runs on NOVA in both layouts and another texture format saves 1–1.5 GB of video memory; the settings QR for Flex IQ and the Flex-Ports must be encrypted with a per-location key; Irina moves Flex Pay to MVP 3 herself; Light & Wonder and IGT still fail over AFT (Oct 19 2026, 4:46–5:17 AM)
date: 2026-10-19
aliases: [Daily Standup meeting Oct 19 2026, Daily Standup Clover Fortune on NOVA and Encrypted Settings QR, Oct 19 stand-up, encrypted settings QR stand-up, SP 1360, FAKE 171, FAKE 67, NDP 1]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Clover Fortune on NOVA and the encrypted settings QR (Oct 19 2026)

**Date/time:** October 19 2026 (a Monday), **4:46 – 5:17 AM Eastern**, about 31 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The Minsk team's morning stand-up, run by Pavel, who joined about 7 minutes late. The previous stand-up is [[wiki/meetings/2026-10-16-daily-standup-mvp2-wi-fi-scope-and-modem-mac-rollback.md|Oct 16]]. The next is [[wiki/meetings/2026-10-20-daily-standup-io-board-firmware-via-github-and-vp9-video-decode.md|Oct 20]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/anton-seregin.md|Anton Seregin]], Daniil Stauskiy (no page), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]. Val was not present.

**Purpose.** Monday round-the-table status. Pavel also set the design of the encrypted settings QR for MVP 2 and raised the AFT failures on other makers' machines, which went on in a separate meeting [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-09-07-wi-fi-provisioning-by-encrypted-qr.md]] (Oct-19 update) — the settings QR is encrypted with a key per location; made on a server page only by the location owner or a bound technician; a plain phone QR is refused; a server-side task for Seregin, maybe a spike first.
- [[wiki/decisions/2026-10-15-installers-set-up-a-location-by-phone-with-a-qr-code-from-the-location-dashboard-the-location-map.md]] (Oct-19 note) — the same QR, now with its encryption settled.
- [[wiki/decisions/2026-10-15-mvp2-is-flex-iq-wi-fi-remote-update-diagnostics-and-galaxy-reporting-and-flex-pay-moves-to-mvp3.md]] (Oct-19 update) — Flex Pay still sits in MVP 2 in Jira; Irina moves it to MVP 3 herself; MVP 2 tests.
- [[wiki/topics/nova-platform-architecture.md]] (Oct 19) — Clover Fortune on NOVA in both layouts; the WebP texture finding; Efim's maths container; Daniil's dependency feature, bonus modifier and screens.
- [[wiki/decisions/2026-10-18-rage-is-closed-dutch-mill-reaches-nova-by-wednesday-and-a-reskin-from-a-new-theme-tests-the-tools.md]] (Oct-19 update) — Leshkevich invited to the Wednesday Dutch Mill review; did Efim make maths for all 6 games?
- [[wiki/decisions/2026-10-18-every-gap-found-on-another-makers-machine-becomes-requirements-and-the-machine-emulator-keeps-a-mode-per-maker.md]] (Oct-19 update) — Light & Wonder and IGT still fail over AFT.
- [[wiki/decisions/2026-10-18-evgeny-kharetski-owns-a-voice-ai-game-design-assistant-with-a-first-pass-reviewed-oct-25.md]] (Oct-19 note) — Kharetski starts the agent; a Jira project is still needed.
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] (Oct-19 update) and [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Oct 19) — Biratka's IO board firmware update and the Terminal Hub spoofing checks.
- [[wiki/topics/test-automation-strategy.md]] (Oct 19) — Khamin's CI tests; Seregin's printer scenarios done and the Wi-Fi QR on a bank scanner; Irina's tests; Ivan's battery questions.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 19) — Tsymanov's lease work on STG and the passport task.
- [[wiki/decisions/2026-10-08-the-ai-pm-goes-live-in-real-jira-projects-on-october-12-on-its-current-architecture-without-lenas-meetings.md]] (Oct-19 update) — an AI Draft on Biratka; about 11 tasks under a closed parent; Claude-set due dates.
- People: [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/anton-leshkevich.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/efim-podvoiski.md]] (in absentia) · [[wiki/people/igor-metelski.md]] (in absentia)

- **Follow-up:** the Wednesday Dutch Mill review Leshkevich was invited to took place on Oct 21 at 8:02 AM — [[wiki/meetings/2026-10-21-dutch-mill-on-nova-and-native-engine.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "October-19-2026", "2026-10-19", "SP 1360" and "FAKE 171" found no page citing either file and no stub for this session. The other Oct-19 raws (two GitHub/MSBC sessions) have different titles and content. The AFT discussion Pavel moved to "новый митинг" is not in this pair; if it reaches the corpus it is a separate stub.
- **§4 name calls.** "Саша" = Biratka (he answers). "Алексей" = Khamin (he answers). The first "Антон" (games) = Leshkevich and "Антон серегин" (printer) = Seregin, by speaker label and name. "Даниил" = Daniil Stauskiy. "Дима" = Kovalchuk (he speaks about Jira). "Женя" = Kharetski (speaker label; he answers). "Ваня" = Ivan. "Игорь" (Dutch Mill) = [[wiki/people/igor-metelski.md|Igor Metelski]] by context. "ефим" = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]. "Владимир" whose task Seregin closed = [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] — **inference**. The "Андрей" who does part of the cloud hub changes and the "Андрей" who owns capabilities are not named in full — **not identified** (Bosik and Klimovich are the candidates; not resolved).
- **Garbles kept as heard.** "кловер форчен" / "клаверфур фурчен" / "клоуфорчу" / "klerfore" / "хлоя пончика" = Clover Fortune (the notes); "рейч" = RAGE; "ногу" / "ново" = NOVA; "дачмил" / "точмел" = Dutch Mill; "веб пи" / "вэппи" = WebP; "геобарде" / "айлборт" / "айборда" = IO board (the notes); "термину хабо" = Terminal Hub; "jessica… в CIC" = the CI build (the notes); "аи драфт… Сп 13 60" (the notes: "SP 1360" as heard); "фейки 171", "фейки 67", "fi 8 sei" (as heard); "н д п один" (the notes: "NDP 1"); "Джаст" = Jest (the notes); "пализии" / "лиза" / "лизу" — the notes write "LISA"; on Oct 6–8 the notes read "лиза" as lease, so lease is likely (**inference**); "14:00 3" = Sergey's "within about 3 days" per the notes; "лок там 72" = the SAS lock command, "72" as heard; "лайт энд бандер" / "лайтен" = Light & Wonder; "FT" = AFT (the notes); "квот" = Claude by context (**inference**).
- **Where the notes and the transcript differ.** None of substance. The notes give the Wi-Fi QR test as done "on a normal bank scanner"; the transcript says "обычном этом банков сканере".
- **Skipped as logistics or chatter.** Who had seen Pavel, the late start, Irina's proposal to move the stand-up to 12:00 (Pavel: "Подумаем"; not decided), greetings and goodbyes.
- **§15.8:** clear. Nobody's pay or rate appears. Comments on when people finished work the night before are not recorded. **§15 #9:** clear; the numbers are Jira keys, a SAS command and dates. No network name, password, PIN or key value was spoken.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Clover_Fortune_on_NOVA_and_Encrypted_Settings_QR-October-19-2026.md]]
