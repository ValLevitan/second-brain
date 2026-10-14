---
type: decision
title: The urgent RIS changes (CAP-252, 255, 246, 254) are built for Georgia only, on the 1.14 SVN line, with nothing else added — Kharetski does them before his own work, and the statistics carousel is dropped for this branch
date: 2026-10-06
aliases: [RIS Georgia branch, Georgia only 1.14 branch, 1.14 plus these changes and nothing else, continuation of Peach 3, carousel for Liza dropped, карусель для лизы, statistics only when scanned, срочные задачи о доработке рис и паспорта]
source-count: 4
status: active
open-commitments: 3
open-questions: 1
---

# The RIS MVP1 changes go to Georgia only, on the 1.14 line, with nothing extra

Set by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] at the [[wiki/meetings/2026-10-06-daily-standup-ris-georgia-branch-and-critical-error-text.md|Oct-6 Minsk stand-up]] (Russian), for [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]]. It follows the Oct-5 release scope: [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]].

## What was said

- **First, before his own plans.** Pavel to Kharetski: "Женя до вот этих всех… изменения, которые ты сейчас задумал… есть срочные задачи, которые всплыли о доработке рис и там паспорта." (Before the changes you planned, there are urgent RIS and passport tasks.) [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **The list.** "252 255 246. 254 и… 258 это просто… Типа сборка" (258 is just the build). The changes are "В основном LGS." [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]] CAP-250, on the Oct-5 list, is not named here.
- **Time.** "2 недели даже наверное чуть меньше уже да до конца следующей" (two weeks, maybe less, to the end of next week). [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]] The notes put this at about Oct 16 [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]. *(Inference: this fits the Oct-19 release date set on Oct 5.)*
- **Georgia only.** Kharetski asked whether it also goes to Dakota. Pavel: "Нет, это только для Джорджия?" Later: "Это джорджиа всё Джорджия с вн" (Georgia, SVN). Pavel may move the branch to git "без всех лишних камитов, если так будет проще". [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **Nothing extra.** Irina: take the version delivered as 1.14 and build from it — "всё то, что у них есть плюс это и больше ничего лишнего". [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **Which base.** Pavel: "Версия, которую нас была там печь 3 да, то есть это продолжение. По сути пич 3." Irina: better to say 1.14, "потому что там они все были из одной один 14 все печи". Pavel: the data-center part matters more; Irina will find which 1.14 data center it ran with. [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **Features.** Pavel had already written the features. He will move them to To Do on the board; "их надо будет ещё да оценить". [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **The carousel is dropped.** Some tasks need server work, for example passing a code so that not all statistics QR codes must be scanned. Kharetski: "мы делали карусель для лизы, и Сейчас мы это отказываемся, правильно понимаю?" Pavel: "Да да." "Для вот конкретно этой." Kharetski: statistics only "когда они захотят отсканить статистику". Pavel and Irina: yes. [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- **More may join.** If these go fast, unplanned capabilities such as reusing the RIS saved in non-volatile memory after a factory reset ("Применить старый рис") will likely be added. [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Why

The Oct-5 release was cut to what fits about two weeks ([[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]]). On Oct 5 Pavel named Kharetski as the free developer. Keeping the branch to 1.14 plus these changes keeps the Georgia build small. *(The "small" reason is an inference; no one stated a reason on Oct 6.)*

## Update, Oct 7 2026 — error handling first, then the QR and statistics come out

At the [[wiki/meetings/2026-10-07-daily-standup-test-coverage-first-and-ai-task-numbers.md|Oct-7 Minsk stand-up]] (Russian) Kharetski: he went over the tasks he was given with Claude, which "решил, что разумнее начинается обработки ошибок" — error handling is, in principle, done. The task numbers he read are garbled ("12 40", "2", "39"). Next, by Pavel's summary: "типа выпили кюар и статистике" — remove the QR and the statistics (by context the statistics-QR item of Oct 6 above — **inference**). He also mentioned the release made the day before and a question from Ivan to be handled later [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]].

## Open commitments

- [ ] Evgeny Kharetski — do CAP-252, 255, 246 and 254 for Georgia on the 1.14 line before his other work — due about the end of next week (notes: about Oct 16 2026) — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [ ] Pavel Frolov — move the RIS features to To Do and estimate them — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [ ] Irina Shishko — find which 1.14 data-center version the Georgia build ran with — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Open questions

- Who is "Лиза", for whom the carousel was made? Not resolved — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
