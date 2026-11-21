---
type: meeting
title: Daily stand-up — a failed Flex-Port firmware update is not shown on the port's own screen (it stays in the terminal log and the operations dashboard); how the port really falls back is for "Евгений" to confirm; hardware-only autotest scenarios (about 10 of Samusenko's Wi-Fi set) are marked manual-only in a separate feature and kept in the repository; machine 84 gets the spare Wi-Fi board; obsolete capabilities are deleted, not archived; release notes on the operations dashboard become a capability; Docker dev images get a clean-up step; Emma's voice is a Bulgarian model (Nov 20 2026, ~3:44–~4:34 AM)
date: 2026-11-20
aliases: [Daily Standup meeting Nov 20 2026, Daily Standup Firmware Rollback and Manual Only Autotests, Nov 20 stand-up, firmware rollback stand-up, manual-only autotests]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — firmware rollback and manual-only autotests (Nov 20 2026)

**Date/time:** Friday November 20 2026, **~3:44 – ~4:34 AM Eastern** (recording), from the `**Date:**` header line of the transcript [[raw/Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]]; the notes give the same time and "~50 minutes" [[raw/Meeting_Notes_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The previous stand-up is [[wiki/meetings/2026-11-19-daily-standup-cloud-test-environment-and-short-claude-messages.md|Nov 19]].

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/igor-metelski.md|Igor Metelski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]], and the voice agent "Emma (AI-PM)". Val was not present [[raw/Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]].

**Purpose.** Round-the-table status, then Bosik's questions.

## Where the substance lives

- [[wiki/decisions/2026-11-20-a-failed-flex-port-firmware-update-is-not-shown-on-the-port-screen-and-hardware-only-autotest-scenarios-are-marked-manual-in-a-separate-feature.md]] — the firmware-rollback talk and its ruling; manual-only scenarios; the Wi-Fi test machines; capability housekeeping; release notes; Docker clean-up; all commitments and questions.
- [[wiki/topics/test-automation-strategy.md]] (Nov 20) — hardware-only scenarios marked manual.
- [[wiki/projects/ai-project-manager-and-company-second-brain.md]] (Nov 20) — Emma's picture and voice.
- [[wiki/decisions/2026-11-19-the-november-20-mvp-2-1-date-will-not-hold-each-reporter-cleans-up-their-own-2-1-items-before-a-follow-up-call-and-cap-267-is-closed-into-cap-146.md]] (Nov-20 note) — Pavel moved the requirements he reviewed to request review; Irina wants CAP-146 split.
- People (all Nov 20): [[wiki/people/pavel.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/evgeny-kharetski.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/ivan.md]] · [[wiki/people/daniil-stauskiy.md]]

## Smaller status items, kept here only

- **Daniil** continues machine-state messages (agreed with "саша" how it will look), will put the sound library in so it can be connected to the new engine, close task "ньюанджин 54 26" (heard) and create a task for the machine-state work [[raw/Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]].
- **Stand-up length.** Igor: "Слишком много вопросов для далика… надоели эти отчитываемся за то, что сделали… он короткий должен быть"; "он у нас делик почти на час". Irina: "меня не интересует, что ты сделал меня интересует, что будет сделано в ближайшее время." Bosik: questions touch everyone, so they belong here [[raw/Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide grep for both filenames, "November-20-2026", "2026-11-20" and "3:44" found no page citing either file and no other Nov-20 stub. The 9:02 AM Klimovich call the same day is a different recording ([[wiki/meetings/2026-11-20-andrei-mvp2-1-release-november-25-and-master-role-in-2-2.md]]).
- **Notes vs transcript.** They agree in substance. The notes' "about 10 of ~23 scenarios" is "у меня есть 10 сценариев там 23, 10 из которых я не могу выполнить" on tape — 10 of 23 is the notes' reading. The notes' "SAS updates" for Seregin is "suss bo проверить" (heard). The notes' "Andrei K's new recycler screen requirements" — the transcript says only "Андрей"; Klimovich is an **inference** from the product-owner context. The notes name "Evgeny (likely Evgeniy Alekseev)" for the rollback check — kept as an inference on the decision page.
- **§4 name calls.** "Саша" = Biratka; "Алексей" / "лёша" = Khamin (he answers); "Антон" in the round = Seregin (he answers); "Даниил" = Daniil; "Дима" in the round = Chudinov (he answers); "Женя" in the round = Kharetski (he answers); "жены" in Igor's line ("жду от жены обратной связи", games CI) = a garble of "Жени" — Kharetski (**inference**, he builds the game ISO); "Евгений" for the Flex-Port board button and the rollback = Alekseev (embedded/firmware context — **inference**; he was not in the call); "Алексея надо было?" (Pavel, on who knows the port update) — Khamin or Alekseev is **unclear**; "Игорь" = Metelski; "Ира" = Irina; "Иван" / "ваня" = Ivan; "Сергей" = Tsymanov; "Владимир" = Samusenko; "Андрей" in the round and with the questions = Bosik (labelled, answers); "Андрей" who adds recycler requirements = Klimovich (**inference**); "Андреем" who wrote acceptance criteria apart from the implementation (Pavel) — which Andrei is **unclear**; "Филиппа" = [[wiki/people/felipe-miranda.md|Felipe Miranda]] (RIS battery context — **inference**); "с Лизой" (Irina) — **unclear**; "Майкл" (said once by Chudinov) — **unclear**.
- **Garbles kept as heard.** "пола сайтеру" / "риса айкелера" / "рисайклер" = Flex Recycler; "рек 84 до рек 107" = REQ-84 to REQ-107; "MBP" / "VP" / "BP" = MVP; "capaбилити" / "копбилити" / "каполете" = capability; "эксептон критериям" / "акцептонск критерии" = acceptance criteria; "онли мэниал" = manual only; "хардбарон" — read as a hardware marker (**inference**); "десижнс" = decisions (a category); "Джерри" / "джире" = Jira; "гетхаб" = GitHub; "флекспорт" / "флекс порта" = Flex-Port; "peration desbord" / "areastin dos bords" / "даш бородок" = operations dashboard; "сошка" / "исошкой" = ISO; "клада" / "клаутера" / "клода" = Claude; "ca и для игр" = CI for games; "р к" / "рка" = RK (ARM board); "докер" / "доки рымыш" = Docker image; "экшена" = GitHub Actions; "релиз, нотос" / "релиз ноту" = release notes; "эмди" = .md; "дфстг" = dev/STG; "от так 10" = the notes' "ot-10" item; "лендер 20" — **unclear**; "suss bo" — **unclear**; "один рис" = RIS; "Рикол сервис называется recol i" — the TTS service name, **unclear** (kept as heard).
- **Skipped as chatter.** The picture-for-Emma jokes beyond her own answer, camera and screen-share trouble, Anton's Saturday half-day (logistics), Irina's "я сегодня злая", the "Киркоров" joke, goodbyes.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** clear — capability, requirement and test numbers only.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Firmware_Rollback_and_Manual_Only_Autotests-November-20-2026.md]]
