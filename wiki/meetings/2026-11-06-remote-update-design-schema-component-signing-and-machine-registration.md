---
type: meeting
title: Remote update architecture review, NOVA and Galaxy — Pavel's design schema (CI/CD to S3, Cloud Galaxy compatibility map, Update Manager, Validation and Signing, delivery, two slots); every component signed separately with one server signature at update time; RIS, machine registration, jurisdictions and operators go into Cloud Galaxy; certification per jurisdiction (Georgia BIN file, Florida full list); use cases before capabilities; Val owns the machine-registration use cases; a Saturday working session (Nov 6 2026, 9:03–10:24 AM)
date: 2026-11-06
aliases: [Remote update architecture review NOVA and Galaxy, Remote Update Design Schema Component Signing and Machine Registration, Nov 6 remote update review, design schema, дизайн схема, NOVA and Galaxy remote update, remote update review 2]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Remote update architecture review, NOVA and Galaxy (Nov 6 2026)

**Date/time:** Friday November 6 2026, **9:03 – 10:24 AM Eastern**, about 80 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]] [[raw/Meeting_Notes_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]]. Teams title: "Remote update architecture review, NOVA and Galaxy" [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]]. **Language: Russian.** It is the Friday 9:00 AM review Val promised on Oct 30 — [[wiki/meetings/2026-10-30-nova-remote-game-update-architecture.md|the Oct-30 remote-update talk]] — and the "сегодня в 04:00" NOVA remote-update meeting Pavel mentioned at the morning stand-up (4:00 PM Minsk) [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (host), [[wiki/people/pavel.md|Pavel Frolov]] (presented), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]]. Samusenko, invited at the stand-up, has no speaker label.

**Purpose:** Pavel walked through a top-level design schema of remote updates for the new Galaxy/NOVA system (a link posted in the meeting chat); the group questioned it and agreed next steps [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]] [[raw/Meeting_Notes_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-06-every-component-is-signed-separately-with-one-server-signature-at-update-time-ris-and-machine-registration-go-into-cloud-galaxy-use-cases-come-first-and-val-owns-machine-registration.md]] — the schema end to end; the signing argument with Chudinov; RIS and registration into Cloud Galaxy; certification per jurisdiction; base image vs games; the compatibility manifest; "design schema, not architecture"; Val's frustration and the use-case rule; the LGS side; the Saturday session; commitments and open questions.
- [[wiki/decisions/2026-10-30-nova-remote-update-is-nova-only-and-texas-first-and-the-full-architecture-is-written-before-the-mvp-split.md]] (Nov-6 update) — Pavel's and Val's Oct-30 commitments discharged; the self-check commitment and the open questions annotated.
- [[wiki/topics/nova-platform-architecture.md]] (Nov 6, 9:03 AM) — the sequencer entry.
- [[wiki/topics/ris-remote-install-and-machine-states.md]] (Nov 6, 9:03 AM) — a new revision of RIS inside Cloud Galaxy; updates that do not touch games leave the RIS alone.
- People: [[wiki/people/pavel.md]] (Nov 6, 9:03 AM) · [[wiki/people/dmitri-chudinov.md]] (Nov 6, 9:03 AM) · [[wiki/people/val-levitan.md]] (Nov 6, 9:03 AM) · [[wiki/people/alexander-biratka.md]] (Nov 6, 9:03 AM) · [[wiki/people/andrey-bosik.md]] (Nov 6, 9:03 AM) · [[wiki/people/irina-shishko.md]] (Nov 6, 9:03 AM) · in absentia: [[wiki/people/juan-martinez.md]] (Nov 6 — "we lost our product owner", read as Juan by the notes) · [[wiki/people/evgeny-kharetski.md]] (to be invited Saturday)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "Remote_Update_Design_Schema", "November 6, 2026, 9:03" and "9:03 – 10:24" found no page citing either file. The Oct-30 9:03 AM meeting is the previous session of the same thread and has its own stub; the Nov-6 6:15 AM stand-up only announced this meeting. A Saturday Nov-7 working session was agreed here; it is not in this unit's sources and is not cited.
- **Notes vs transcript.** The notes call Pavel's page a "Confluence design page"; the transcript says only "в том линке, который вот в чате лежит". The notes read "(Juan)" for the lost product owner; the transcript has "мы потеряли кродок тонера [product owner]… У нас некому… его заменить" with no name (heard "one") — Juan is the notes' reading, kept as an **inference** from his VP-product-owner role. The notes name "Evgeny" as invited to Saturday; the transcript has "женю" (Bosik) — read as Kharetski by the NOVA integration-repository context, **inference**. The notes' undertaking 5 (Pavel and Chudinov describe the Update Manager, software manager and Validation and Signing as capabilities) is the notes' allocation; on the transcript Pavel proposes the next step and Chudinov lists the Galaxy-side capabilities without a named owner.
- **§4 name calls.** "Дима" / "дима" throughout = [[wiki/people/dmitri-chudinov.md|Chudinov]] (he answers; Galaxy/server context); "Саша" / "сашу" on the LGS = [[wiki/people/alexander-biratka.md|Biratka]]; "Андрей" = Bosik (present, label); "Паша" = Pavel; "Ира" = Irina Shishko; "Евгений, Александр" read by Val from the table's owner column — Kharetski and Biratka by context (**inference**).
- **Garbles kept as heard.** "сошка" / "исо" = ISO image; "с 3 хранилища" = S3; "раук" = RAUC; "эклипс" = Eclipse; "джила" / "jaly" / "жилая сертификация" = GLI; "Ларида семенол" = Florida Seminole; "байенфайл" = BIN file; "сас проверки" = SAS check; "FP seven или это вэ 1000" — FP7 and a second x86 platform name, **unclear**; "рк 35 икс икс" = RK35xx; "Сидней счет чек" / "сигнича" = signature check; "vidation and sailns" / "valledation insing" = Validation and Signing; "кродок тонера" = product owner; "anton ant тесты" = end-to-end tests; "скоб габс" = scope gaps; "по IPIC" = by IPC (**inference**); "ремоутадей" = the remote-update branch; "230" does not appear here.
- **Skipped as chatter.** The audio check at the start ("А я вас не слышу… Скажите что-то"), "Пятница", the screen-share fumble, the calendar arithmetic for Saturday, goodbyes.
- **§15.8:** clear. **§15 #9:** clear — no identifiers; the checksums and keys are described, never quoted.

## Sources

- [[raw/Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]]
- [[raw/Meeting_Notes_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026.md]]
