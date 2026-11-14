---
type: meeting
title: Flex-Recycler Slim — Biratka has the recycler up and needs two more days of bring-up; the old capabilities lack acceptance criteria; Val wants the product owner to groom MVP 1, MVP 1 on the production server by Thursday and MVP 2 a week later, cut scope never the date; only the ISO from production; Texas, e-wallet only, no TITO; the typical Texas install; a $20 AFT promo bonus changed from $2 at 92% to $1 at 90%; the bonus on the recycler screen; Metelski's Rage conversion for the Texas V43 line into GitHub with CI/CD; Pavel creates releases right after meetings (Nov 12 2026, 6:53–7:24 AM)
date: 2026-11-12
aliases: [Flex-Recycler Slim short meeting, Flex-Recycler Slim rollout date and Jira, Flex Recycler Slim MVP1 by Thursday and 20 Dollar Promo Bonus, Nov 12 recycler meeting, Val's recycler meeting 14:45]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Flex-Recycler Slim — MVP 1 by Thursday and a $20 promo bonus (Nov 12 2026, 6:53 AM)

**Date/time:** Thursday November 12 2026, **6:53 – 7:24 AM Eastern**, about 31 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]] [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]. Teams title: "Flex-Recycler Slim: short meeting (rollout date and Jira)". **Language: Russian.** This is the meeting the [[wiki/meetings/2026-11-12-daily-standup-recycler-rust-service-and-no-features-before-capability-review.md|Nov-12 stand-up]] said Val had set ("На 14 45 митинг"; 14:45 Minsk is 6:45 AM Eastern — **inference**).

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (organizer), [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko"), [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]].

**Purpose.** Set the recycler rollout date and its Jira releases.

## Where the substance lives

- [[wiki/decisions/2026-11-12-the-recycler-gets-its-own-mvp-1-on-the-production-server-by-thursday-november-19-and-its-mvp-2-a-week-later-scope-is-cut-never-the-date.md]] — status, the MVP 1 / MVP 2 rule, ISO from production only, Texas e-wallet only, CI/CD, releases right after meetings; commitments and questions.
- [[wiki/decisions/2026-11-12-the-texas-twenty-dollar-promo-bonus-is-one-dollar-per-twenty-with-machines-at-ninety-percent.md]] — the $20 AFT bonus, the 102% objection, $1 at 90%, the screen.
- [[wiki/projects/texas-used-machine-distribution.md]] (Nov 12) — the typical Texas install.
- [[wiki/decisions/2026-10-08-texas-rage-games-convert-to-vertical-nova-unchanged-and-igor-ports-dutch-mill-first.md]] (Nov-12 note) — Metelski's Rage conversion for the Texas V43 line into GitHub; who writes its CI/CD.
- [[wiki/decisions/2026-09-10-requirements-come-first-and-the-recycler-is-out-of-both-mvps.md]] (Nov-12 note) — the recycler's own MVP track.
- [[wiki/topics/github-release-management-pipeline.md]] (Nov 12) — the ISO-only rule and the release habits.
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/pavel.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/irina-shishko.md]] (all Nov 12, 6:53 AM) · in absentia: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/igor-metelski.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/alexei-khamin.md]]

## Notes on the sources

- **§12 — new meeting.** The notes and transcript share date, time and title and link each other. A corpus-wide search for both filenames, "Recycler_Slim", "20_Dollar_Promo" and "6:53" found no page citing either file. It sits between the [[wiki/meetings/2026-11-12-daily-standup-recycler-rust-service-and-no-features-before-capability-review.md|6:14 AM stand-up]] and the [[wiki/meetings/2026-11-12-mvp2-capability-review-goods-category-master-role-and-release-split.md|8:33 AM MVP 2 review]].
- **Notes vs transcript.** The notes' "MVP 2, dated one Thursday later" is Val's "через неделю в четверг… Не, не на следующей неделе, а через неделю", but at the close he said "MVP 2 на следующий четверг" — left **unclear**. The notes' "refitted T27 horizontal cabinets from Pennsylvania" is "пэушные горизонтальные машины т 27" (heard; "Pennsylvania" is the notes' reading). The notes' "Igor's converted Rage games" is "Миссельского. Программы, которую конвертировал" (heard). The notes name Andrei Klimovich as product owner; the transcript says only "Андрей" and "продактонер".
- **§4 name calls.** "Андрей" (product owner, screens, the bonus text) = [[wiki/people/andrei-klimovich.md|Klimovich]] (**inference**, as the notes have it). "Андрей босик" = [[wiki/people/andrey-bosik.md|Andrey Bosik]]. "саша" = Biratka. "Паша" = Pavel. "метельского" / "Миссельского" / "Игорь метельские" = [[wiki/people/igor-metelski.md|Igor Metelski]]. "Алексей хамин" = [[wiki/people/alexei-khamin.md|Alexei Khamin]]. "ефиму" (Biratka, once, on the bonus maths) = [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] by name (**inference**). "Владимир" (Irina, among those writing autotests) — [[wiki/people/vladimir-samusenko.md|Samusenko]] by the test work (**inference**). "ксенияша" (also writing autotests) — matched to no one; left **unresolved**. "валере" ("представим это валере") — **unclear**.
- **Garbles kept as heard.** "ресайтлер" / "рисайклер" / "рисайлэр" / "wesicler" / "sikler" = recycler; "copility" / "копбилетиях" / "побилити" = capability; "экспертность критерий" / "аксепс, критерии" / "эксептанс критерия" = acceptance criteria; "реклайрменс" / "регламенты" / "рекламентс" = requirements; "груm" = groom; "I dandafies" = identify; "скетживал" / "скетчу" = schedule; "SICD" / "CICD" = CI/CD; "Forber на GCMR сайтлы" — **unclear**; "даф" / "д ф с тг" / "с т г" = DEV / STG; "техсос" = Texas; "еволет" = e-wallet; "тито" = TITO; "белых сектора" = bill acceptor; "AFT ficher" = AFT feature; "промошн crew" = promotional credit; "арти пи" = RTP; "киашин" = cash in; "Пианино" — **unclear**; "рейч" / "рейд" = Rage; "гидхабе" / "детхаге" / "ged have" = GitHub; "вифори фри" = V43; "сиди" = CI/CD; "Юбыл добрать медицинский" — **unclear** (by context Metelski); "инваймент" / "баймен" = environment; "pasvay" = pathway; "Я ставлю резор с планирования для вас паром" — **unclear**.
- **Skipped as chatter.** The opening; Val's joke near the 26-minute mark; the back-and-forth over what "иишка" (AI) is called; the goodbyes.
- **Not recorded:** none beyond the chatter; no personal passage in either file.
- **§15.8:** clear — the $1 / $2 bonus is a player promotion and 90% / 92% are machine returns. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]
- [[raw/Meeting_Notes_Flex_Recycler_Slim_MVP1_by_Thursday_and_20_Dollar_Promo_Bonus-November-12-2026.md]]
