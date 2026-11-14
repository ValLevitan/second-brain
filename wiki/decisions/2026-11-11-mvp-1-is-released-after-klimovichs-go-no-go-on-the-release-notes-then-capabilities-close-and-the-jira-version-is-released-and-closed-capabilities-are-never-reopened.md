---
type: decision
title: MVP 1 is formally released in this order — Ivan updates the release notes (build names at the top, a clearer Flex-Port version label), Andrei Klimovich as product reviews them, installs the builds and gives a go / no-go, and only then the release manager moves all capabilities to Closed and releases the version in Jira; a Closed capability is never reopened — a gap found later goes into a new "amendment" capability; the missing CAP-311 build-to-release-notes link is accepted as missing for MVP 1; the release notes keep their length for this first run (Nov 11 2026)
date: 2026-11-11
aliases: [MVP1 Release, MVP2 Scope and CAPs/REQs review, MVP1 release procedure, Nov 11 MVP 1 release meeting, product go / no-go, зелёный свет, green light by tomorrow evening, release notes then go-no-go then Closed, amendment capability, побилити amment, Closed is not reopened, клоуст не переоткрывается, CAP-311, к а п 311, build names at the top of the release notes, 37 capabilities 36 closed, IQ build of November 3, why do we invent the process, мы просто не дочитали книгу, wrong people at the release meeting]
source-count: 2
status: active
open-commitments: 6
open-questions: 2
---

# MVP 1 is released after Klimovich's go / no-go on the release notes; then capabilities close and the Jira version is released; Closed is never reopened (Nov 11 2026)

Agreed at the [[wiki/meetings/2026-11-11-mvp1-release-procedure-release-notes-and-product-sign-off.md|Nov 11 2026, 8:31 AM release meeting]] (Russian) by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]], with [[wiki/people/ivan.md|Ivan]] as release manager [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. It puts into practice [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]].

*(Quotes are from an unpunctuated Russian speech-to-text transcript, kept word for word; garbles are marked "heard". "конфликты" / "комплекте" = Completed and "клоуст" / "coost" = Closed, as on the Nov-4 page.)*

## Where things stood

- **Not yet released.** Klimovich had only half an hour, so the meeting covered MVP 1 only: "Что нам мешает выпустить версию, потому что она как бы официально у нас ещё не зарелижена" — the capabilities sit at Completed, "но не клоуст", and the version is "в анрелиз статусе" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. Irina had Ivan called in, "Чтоб у нас не было передаточных механизмов" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The conditions.** Irina: capabilities close "когда мы говорим, что всё выпустили, мы больше ничего не делаем". Pavel: the production artifact "должен лежать на steorger praction store" (heard; the production store), and there must be release notes, "который вот иван сейчас как раз сделал", comparing the Jira features and capabilities with "написано в прозе и как прошли автотесты" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The count.** Ivan's release notes: "всего там 37 закрыто 36"; Irina: "она закрытая"; Ivan: the page is not live, "Я досмотрю" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. Near the end one feature still hung ("одна фичак это подвисла", Klimovich) [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The IQ build.** Klimovich: "последняя сборка IQ, которая на проде висит она 3 ноября"; Irina: "мы после этого ничего не собирали"; Pavel: later builds were "исключительно для девелопмент нужд" and never reached prod [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## The build-to-release link (CAP-311)

- Klimovich, as product, cannot tell from prod which build is the release: "я вот, например, как продакт об этом не знаю". "к а п 311" (heard; CAP-311) asked that the shipment holding the build carry a link or text naming the release; "Вот этой связки у нас сейчас нету" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"): "Запланируем этот функционал на MVP 2"; for MVP 1 "Функционал такой не закладывался". Klimovich: formally it was, in "capobilis 311, которая числятся как клоуст уже даже ну окей, хрен с ним переживём" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The stop-gap.** Irina: not a link so much as the build name for these release notes; Klimovich: "хотя бы так, да этого достаточно будет"; Ivan puts it "в шапке" (in the header) [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The Flex-Port label.** For the Flex IQ the build reference ("206", Ivan) is enough; for the port only "вы один" (heard; v1) plus a commit is shown — Klimovich: "С партом надо ну както более понятно это сделать" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## The order of steps — the ruling

- **Irina's question.** Must Klimovich accept the release before the capabilities close, or after? Klimovich: "Хороший вопрос, это правильный вопрос" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. He first leaned to the team closing the capabilities, the version staying unreleased, then his review and "финальное говно угол" (heard; go / no-go) [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **Pavel.** A version on the production server "это ещё не триггер" for letting people install it. Klimovich reads the release notes and, for "флекса айкью или флекспорта", installs it himself and checks it against the server side and the requirements; if it falls short, work goes on inside the same capabilities, or, if they are already Closed, "нам придётся открывать тогда новый capility, там побилити amment" (heard; a capability amendment). Irina: "мы договаривались, что клоуст не переоткрывается"; Pavel and Klimovich: "Да" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The agreed flow.** Klimovich: "ваня сегодня обновит релиз ноут", he checks that everything is covered and "Я даю зелёный свет… потом релиз менеджер переводит все кплитис в coutuse и версия религизится в juri всё" (heard; Closed, Jira). Timing: "я думаю, что завтра к вечеру мы получим зелёный свет. Если у нас всё хорошо"; if not, a list of fixes [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **Install check.** Val asked whether Klimovich had installed the IQ. Klimovich: "Последний бил 3 лиза еще не ставил" (heard); he downloaded it and checked "катабили 311" — "из этого интерфейса всё скачивается, всё работает" — and has the port's USB builds in hand to install [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **The release notes keep their length.** Ivan offered to shorten the text; Klimovich: "не надо сейчас ничего специально сжимать… прогоним эту первую версию в том виде, как ты это сейчас сделал" — he reads it through AI anyway [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## Val's points

- "а почему мы всё выдумываем?… весь мир уже это делает"; "А Сейчас мы 1 раз пытаемся это сделать по стандарту. Но стандарт мы как бы почитали до сих пор, а вот дальше не почитали"; "мы просто не дочитали книгу… мы ничего не должны выдумывать" — Jira and GitHub ("В кехаби" — heard) already describe it [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. Klimovich: "я могу это взять на себя. Я могу сегодня это изучить", and "чекнуть, это против без проктисис" (heard; best practices) [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].
- **Who should be in the room.** "здесь на митинге неправильные люди" — "саша дима Сергей" are developers who work at the level of features and commits and are not needed; missing is "Андрея босика, потому что он занимается CICD" [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]. Who "саша" and "Сергей" are is **unclear** (not in the room); "дима" is most likely Chudinov, who was (**inference**).
- Val also asked whether the build can go on location yet ("мы можем ставить это на локеченной или нет" — heard); Klimovich: they want to finish the procedure, since in Jira the release is formally not released [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]].

## How it sits against earlier rulings

- **Nov 4.** The Nov-4 flow had the release manager settle exceptions with product ownership and then move capabilities to Closed; Nov 11 makes Klimovich's go / no-go the explicit gate before Closed and adds the amendment rule — [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]] (Nov-11 note). The Done-vs-Closed question for features stays open there.
- **The MVP 1 date.** The Nov 9 internal release had not been formally closed by Nov 11 — [[wiki/decisions/2026-11-05-mvp-1-is-planned-for-monday-november-9-internally-and-the-client-is-told-wednesday-and-the-pyramid-bill-acceptor-is-tested-remotely-on-an-echo-cabinet-in-georgia.md]] (Nov-11 note).
- **Process.** Logged on [[wiki/topics/github-release-management-pipeline.md]] (Nov 11).

## Open commitments

- [ ] [[wiki/people/ivan.md|Ivan]] — update the MVP 1 release notes with the build names at the top and re-check the 37th capability — due Nov 11 2026 ("сегодня") — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [ ] [[wiki/people/ivan.md|Ivan]] — make the Flex-Port version label clear in the release notes (not just "v1" plus a commit) — due unspecified (the notes: Nov 11 2026) — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review the release notes, install the builds and give the go / no-go — due Thu Nov 12 2026 evening ("завтра к вечеру") — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — check the release procedure against best practices — due Nov 11 2026 ("сегодня") — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [ ] [[wiki/people/ivan.md|Ivan]] (release manager) — after the green light, move all MVP 1 capabilities to Closed and release the version in Jira — due after Klimovich's go — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — set the MVP 2 review meeting ("Давайте митинг назначим"); the MVP 2 capabilities and requirements are commented in Jira — due Thu Nov 12 2026 morning ("завтра утром") — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]

## Open questions

- When is the CAP-311 build-to-release-notes link built — MVP 2, as Chudinov proposed? Not confirmed — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- Who should attend release meetings? Val wants Andrey Bosik (CI/CD) in and the developers out — [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]] [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]

**§15.8:** clear. **§15 #9:** none — "206" is a build reference, not an identifier.

## Sources

- [[raw/Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
- [[raw/Meeting_Notes_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026.md]]
