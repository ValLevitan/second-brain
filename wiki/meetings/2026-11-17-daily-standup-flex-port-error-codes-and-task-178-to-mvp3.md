---
type: meeting
title: Daily stand-up — only what is needed for Thursday stays in 21, the rest is marked 22; capability 372 adds Flex-Port error codes that Flex IQ cannot decode, so a decoding feature is needed for offline storage and Grafana; task 178 moves to capability 298 (MVP 3); Pavel's faster bill-acceptor status goes to the next release; Wi-Fi between Flex IQ and Flex-Ports works in access-point mode, through the GL 2 router only with the MAC registered; due dates stay; a feature belongs to whoever closes the last story (Nov 17 2026, 3:44–4:14 AM)
date: 2026-11-17
aliases: [Daily Standup meeting Nov 17 2026, Daily Standup Flex-Port Error Codes and Task 178 to MVP3, Nov 17 stand-up, task 178 to MVP 3, Emma in the stand-up]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Daily stand-up — Flex-Port error codes and task 178 to MVP 3 (Nov 17 2026)

**Date/time:** Tuesday November 17 2026, **3:44 – 4:14 AM Eastern**, about 29 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]]. Teams session "Daily Standup meeting". **Language: Russian.** The previous stand-up is [[wiki/meetings/2026-11-16-daily-standup-morning-standups-and-sms-fix-release.md|Nov 16]], where the stand-ups were moved to the morning.

**Who spoke** (speaker labels): [[wiki/people/pavel.md|Pavel Frolov]] (led), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/alexei-khamin.md|Alexei Khamin]] (label "Alexey Khamin"), [[wiki/people/anton-seregin.md|Anton Seregin]], [[wiki/people/daniil-stauskiy.md|Daniil Stauskiy]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov"), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]]. Val was not present [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]].

**Purpose.** Round-the-table status.

## Where the substance lives

- [[wiki/decisions/2026-11-12-mvp-2-splits-into-mvp-2-1-iq-and-port-and-mvp-2-2-web-services-lottery-becomes-goods-and-the-inspector-report-becomes-the-audit-report.md]] (Nov-17 note) — 21 vs 22 marking; the Flex-Port error codes and the Flex IQ decoding feature; task 178 to capability 298 (MVP 3); Pavel's faster bill-acceptor status to the next release; Wi-Fi between Flex IQ and Flex-Ports.
- [[wiki/decisions/2026-11-09-a-task-moved-to-to-do-gets-a-due-date-from-whoever-moves-it-claude-sets-it-under-the-standard-and-jira-does-not-block-an-empty-date.md]] (Nov-17 note) — moving dates by chat works; due dates stay; a feature belongs to whoever closes the last story.
- People (all Nov 17): [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/sergey-tsymanov.md]] · [[wiki/people/vladimir-samusenko.md]] · [[wiki/people/ivan.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/anton-seregin.md]] · [[wiki/people/evgeniy-alekseev.md]] (in absentia, name call queued)

## Smaller status items, kept here only

Before the start Kovalchuk was trying a voice assistant in the call ("эмма"): "Мы хотели потестить еще, мы не успели сегодня, так что давайте пока ее игнорировать". Daniil: Biratka reviewed "PRP 1340" (the notes: PR 1340); he will commit a change so it stops uploading to Nexus and merge it, then continue "нью джин 54" (the notes: NewGin-54). Kharetski: "Создание лица. Его установка" (heard; the notes: ISO creation and install). Seregin: the port tests now pass ("Под 212 тинтам", the notes: TINT-212), the emulation part works, and he checks against a real port today, done "гдето 2 30" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]].

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Error_Codes", "Task_178" and "3:44" found no page citing either file. The Nov-16 stand-up is a separate recording.
- **Notes vs transcript.** The notes call this the "first morning standup"; the transcript does not say so, and the Nov-16 stand-up (6:14 AM) was also in the morning — not used. The notes' "Irina said the 20th; Ivan proposed Wednesday next week" for task 178 came before the move to capability 298; the final date is not said. The notes say Dzmitry "tried" the date move; the line is "Дима дима попробовал, подвинула" (who tried is **unclear**). The notes read "реклариментах" as regulations; elsewhere "регламент" is used for requirements.
- **§4 name calls.** "Саша" = Biratka; "Алексей" = Khamin; "Антон" = Seregin (he answers); "Даниил" = Daniil; "дима" in the round = Chudinov (he answers) and "слово диме" at the end = Kovalchuk (he answers); "женя" in the round = Kharetski (he answers); "женя добавил" (Ivan, the modem UI) = Kharetski by his Nov-16 LTE work (**inference**); "как вот женя правильно сказал" (Kovalchuk) — which Zhenya is **unclear**, not forced; "Ира" / "Иран" = Irina; "ваня" = Ivan; "Сергей" = Tsymanov; "Владимир" = Samusenko; "дэй климович" = [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]; "этот Алексеев" (Port-157) = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] by surname and his Flex-Port work (**inference**, queued); "шувал" (Khamin) = Val (**inference**); "с Андреем" (Chudinov's CI/CD) and "Андрея" (Tsymanov's router question) — which Andrei is **unclear**; "Игоря" (Irina: who is missing) — **unclear**; "Андрес" (Seregin at the end) — **unclear**.
- **Garbles kept as heard.** "к побилити" / "capolity" / "кап" = capability; "кликс спорт" / "флегспорт" / "флекс спорт" = Flex-Port; "флекс IQ pay" / "флексайте" / "рефлекса кюра" = Flex IQ; "шифровка" = decoding (the notes' reading); "оффлайн бита" = offline storage (the notes); "графану" = Grafana; "лекции сайт леру" / "флексри сайтлер" = (Flex) recycler; "випия один" = MVP 1; "пауэркап" / "попал бы кап" / "power back апп" = power backup; "Эф 178" / "fort 178" = task 178; "билвалидатор" / "билаксептора" = bill validator / bill acceptor; "сас" / "с вас" = SAS; "02:01" = 2_1; "м в п 3" = MVP 3; "эксвершим" / "К свершим" = fix version; "как 314" = CAP-314; "т е" / "алтошку" = LTE (the notes' reading); "эстегэ" / "с т г" = STG; "смску" = SMS; "Пофиг 206" = FIG-206; "тим 69" — **unclear**; "кюсики вай фай деливери" = Flex IQ Wi-Fi delivery (CAP-287); "Сергею грине" — **unclear** (the notes: Sergey); "рек 18, 33" = REQ-1833; "Порт 157" = Port-157; "Икса спойнта" / "20 пойнта" = access point; "джиэль" / "дживель" / "джил" = GL (router name, as heard); "14:00" = 14 days (the notes' reading); "12 от силы" = 1–2 at most (**inference**).
- **Skipped as chatter.** The voice-assistant jokes at the start, the goodbyes.
- **Not recorded:** none; no personal passage.
- **§15.8:** clear. **§15 #9:** clear — task, test, PR and capability numbers only.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Error_Codes_and_Task_178_to_MVP3-November-17-2026.md]]
