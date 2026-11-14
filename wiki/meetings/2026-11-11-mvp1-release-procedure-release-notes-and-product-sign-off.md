---
type: meeting
title: MVP 1 release procedure — MVP 1 is still formally unreleased in Jira; Ivan's release notes show 37 capabilities, 36 closed; the IQ build of November 3 is the release build; the CAP-311 build-to-notes link is missing and build names go at the top instead; the order is release notes → Klimovich's go / no-go → capabilities Closed and the version released, and Closed is never reopened (an amendment capability instead); Val asks why the team invents its own process and who should be in the room; MVP 2 review tomorrow (Nov 11 2026, 8:31–8:55 AM)
date: 2026-11-11
aliases: [MVP1 Release, MVP2 Scope and CAPs/REQs review, MVP1 Release Procedure Release Notes and Product Sign-Off, Nov 11 MVP 1 release meeting, MVP 1 go / no-go meeting]
source-count: 2
open-commitments: 0
open-questions: 0
---

# MVP 1 release procedure — release notes and product sign-off (Nov 11 2026, 8:31 AM)

**Date/time:** Wednesday November 11 2026, **8:31 – 8:55 AM Eastern**, about 24 minutes, from the `**Date:**` header line of both files [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. Teams title: "MVP1 Release, MVP2 Scope and CAPs/REQs review". **Language: Russian.** Only MVP 1 was covered; MVP 2 moved to the next morning. Val joined from his car ("из машины") [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (ran it), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"; called in as release manager), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/val-levitan.md|Val Levitan]] [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

**Purpose (Klimovich):** "Что нам мешает выпустить версию" — run the MVP 1 release procedure through to the end [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## Where the substance lives

- [[wiki/decisions/2026-11-11-mvp-1-is-released-after-klimovichs-go-no-go-on-the-release-notes-then-capabilities-close-and-the-jira-version-is-released-and-closed-capabilities-are-never-reopened.md]] — where things stood; CAP-311 and the stop-gap; the Flex-Port label; the order of steps; the amendment rule; Val's points; all commitments and questions.
- Earlier decisions annotated: [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]] (Nov-11 note) · [[wiki/decisions/2026-11-05-mvp-1-is-planned-for-monday-november-9-internally-and-the-client-is-told-wednesday-and-the-pyramid-bill-acceptor-is-tested-remotely-on-an-echo-cabinet-in-georgia.md]] (Nov-11 note)
- Topic: [[wiki/topics/github-release-management-pipeline.md]] (Nov 11)
- People: [[wiki/people/andrei-klimovich.md]] · [[wiki/people/ivan.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/val-levitan.md]] (all Nov 11, 8:31 AM) · in absentia: [[wiki/people/andrey-bosik.md]] (Val wants him at release meetings)

## Notes on the sources

- **§12 — new meeting.** The notes and the transcript share the date, time and title and link each other. A corpus-wide search for both filenames, "MVP1_Release_Procedure", "Product_Sign-Off", "CAPs/REQs" and "8:31" found no page citing either file. It follows straight after the [[wiki/meetings/2026-11-11-nova-2-mechanics-placement-one-studio-tool-and-game-metrics.md|7:31 AM NOVA-2 follow-up]] (which ran to 8:32) and is a different session; it continues the [[wiki/meetings/2026-11-04-mvp1-transactional-release-definition-and-pilot-watch.md|Nov-4 release meeting]].
- **Notes vs transcript.** The notes' "Flex IQ, Flexport" is "флекса айкью или флекспорта". The notes have "developers like Sasha, Dima and Sergey"; the transcript has "саша дима Сергей" — only Dima is in the room (read as Chudinov, **inference**). The notes' "green light by tomorrow evening" is "завтра к вечеру". The notes' "Ivan offered to shorten the text" matches the transcript. The notes' "37 capabilities, 36 closed" is "всего там 37 закрыто 36".
- **§4 name calls.** "ваня" / "иван" = [[wiki/people/ivan.md|Ivan]] (label "Ivan Shpak"); "Андрей" running the meeting and "как продакт" = Klimovich; "Андрея босика" = [[wiki/people/andrey-bosik.md|Andrey Bosik]] (not present); "Павел" = Pavel; "Маша" (Irina, once, and Ivan's "маша обновить") — **unclear**, not resolved.
- **Garbles kept as heard.** "конфликты" / "комплекте" / "комплитти" = Completed; "клоуст" / "coost" / "coutuse" = Closed; "MVVP один" = MVP 1; "к а п 311" / "capobilis 311" / "катабили 311" = CAP-311; "steorger praction store" = the production store; "джиро" / "juri" / "эджире" = Jira; "побилити amment" = capability amendment; "говно угол" = go / no-go; "без проктисис" = best practices; "кехаби" = GitHub; "CICD" = CI/CD; "Последний бил 3 лиза" — **unclear**; "вы один" = v1; "фп ноль один, а м ar" — **unclear**; "5 47" — **unclear**.
- **Skipped as chatter.** The greetings, "из машины" logistics, Val telling Klimovich to drive to his next meeting, the goodbyes; Val's request that Pavel call him (content not on the transcript).
- **Not recorded:** none; no personal passage in either file.
- **§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
