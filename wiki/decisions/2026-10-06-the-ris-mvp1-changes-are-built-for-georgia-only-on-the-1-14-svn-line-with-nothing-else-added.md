---
type: decision
title: The urgent RIS changes (CAP-252, 255, 246, 254) are built for Georgia only, on the 1.14 SVN line, with nothing else added — Kharetski does them before his own work, and the statistics carousel is dropped for this branch
date: 2026-10-06
aliases: [RIS Georgia branch, Georgia only 1.14 branch, 1.14 plus these changes and nothing else, continuation of Peach 3, carousel for Liza dropped, карусель для лизы, statistics only when scanned, срочные задачи о доработке рис и паспорта]
source-count: 13
status: active
open-commitments: 5
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

## Update, Oct 8 2026 — task 1239, a new lease for the old GA COAM; the old release cannot move to Git

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[wiki/people/evgeny-kharetski.md|Kharetski]]: he is on "12:39" (the notes read task 1239) — "Новая лиза для гаккуан старого" (the notes: a new lease for the old GA COAM). The version is old and there are old and new protocols, so the server side had questions; "вчера уже там… Решения приняли". He had hoped to move the release of this version to Git, "но не получится, потому что… старая там всё на некс завязано" (the notes: it depends on Nexus). He also fixed a bug where a tab did not show, and re-released [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].

Whether 1239 is one of the CAP items above is not stated. Pavel's Oct-6 offer to move the branch to git is the nearest context; Oct 8 says that move does not work for the old release (**inference** that the two refer to the same release line).

*On the open question below:* in this thread "лиза" is read by the notes as "lease" on Oct 8. The Oct-6 "карусель для лизы" may also mean lease, not a person — **inference only**; the question stays open.

## Open commitments

- [ ] Evgeny Kharetski — do CAP-252, 255, 246 and 254 for Georgia on the 1.14 line before his other work — due about the end of next week (notes: about Oct 16 2026) — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [ ] Pavel Frolov — move the RIS features to To Do and estimate them — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [ ] Irina Shishko — find which 1.14 data-center version the Georgia build ran with — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Open questions

- Who is "Лиза", for whom the carousel was made? Not resolved — [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]

## Update, Oct 9 2026 — Kharetski on 1238; the server side is Tsymanov's; the lease code without a full statistics scan is urgent for the middle of next week; the old RIS at factory reset is planned, not scheduled

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]:

- **[[wiki/people/evgeny-kharetski.md|Kharetski]].** On "12 38" (the notes: task 1238, lease work for the old software). Pavel asked whether the fixes for "этого старого софта" need server work; Kharetski: "Ну а Сергей стоят задачей, я куда контракт описывает" — [[wiki/people/sergey-tsymanov.md|Tsymanov]] has the task, with the contract described.
- **The urgent lease-code task.** Pavel to Tsymanov: "там задачи есть, которые для жени по лизам… когда обновление лиза, чтобы разрешать машине применять код, если она не отсканировала? Всю статистику" — let a machine apply the lease code even if not all statistics were scanned. Tsymanov: "Это это ж в другом проекте, да?" Pavel: "Да… Это тоже срочно… надо, чтобы к середине следующей недели было сделано." Tsymanov: "Приоритетно. Хорошо." *(This matches the Oct-6 server item above — passing a code so not all statistics QR codes must be scanned — **inference**.)*
- **The old RIS at factory reset.** Pavel offered Kharetski the next piece: "Использование… старого риса. Сохранённого на жёстком диске. При [фактори ресет]." Kharetski: "да какомто планах." Pavel: "он в планах. Просто он сейчас не… запланирован." Kharetski does not load his plan far ahead "изза Того, что я могу напланировать… потом вы мне говорите, что нужно делать другое."

*On the open question below:* here "лиза" again reads as lease ("по лизам", "обновление лиза"). Still **inference only**; the question stays open.

### Open commitments (Oct 9 2026)

- [ ] [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] — the server side: let a machine apply the lease code without a full statistics scan — due the middle of the week of Oct 12 2026 ("к середине следующей недели"; the notes: about Oct 14) — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

## Update, Oct 12 2026 — Kharetski near the end of "1241"; he tests it himself; "до 22"

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) [[wiki/people/evgeny-kharetski.md|Kharetski]]: "я сейчас в 12:41 лжай закончу… последние… работке" (the notes read task 1241, "number unclear"). "в целом все запросы, которые были [—] джоджи выполнена" — the garbled word may be Georgia (**inference**); "наверное, там серёга доделает" (Tsymanov — **inference**). "можно будет… Тестировать, начинать." [[wiki/people/irina-shishko.md|Irina]]: Ivan is on autotests to the 15th and cannot test it; "Можешь сам потестировать". Kharetski: "И при этом до 22 мы хотим выпустить этот." Irina: "Да." [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

Which release "до 22" names is **unclear** (the object is garbled). Reading task 1241 as part of this Georgia RIS branch is an **inference** from Kharetski's assignment here. If it is, the Oct-22 aim sits three days after the Oct-19 Jira date on [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]] — not recorded as a contradiction, since the link is not stated.

### Open commitments (Oct 12 2026)

- [ ] [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — finish 1241 (number unclear) and test it himself — due before Oct 22 2026 — [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

## Update, Oct 13 2026 — Kharetski closes "1241"; why "RIS" is in the release name; a separate meeting after lunch

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]:

- **[[wiki/people/evgeny-kharetski.md|Kharetski]]:** "12 41 я закрою сейчас" — he will close 1241 now and test while Ivan is busy. Whether it is closed is not in this source, so the Oct-12 commitment above stays open.
- **The evening topic goes to its own meeting.** [[wiki/people/irina-shishko.md|Irina]] asked whether Kharetski should wait, since what was discussed the evening before might change things. Pavel: "то, что мы вчера вечером обсуждали, мы это отдельно соберёмся после обеда."
- **[[wiki/people/sergey-tsymanov.md|Tsymanov]]** took the task discussed the evening before and said it needs a separate meeting. He does not see "при чём здесь рис ну конкретно в данной задаче". Pavel: "так повелось, что этот релиз назвали там рисом… только по этой причине." Reading this release as the RIS MVP 1 line on this page is an **inference**; the transcript does not name the line. What the evening topic was is not said.

### Open commitments (Oct 13 2026)

- [x] [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — a separate meeting on the evening-before task, with Tsymanov's questions as a list — due Oct 13 2026 (after lunch) — [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]] — **discharged Oct 13 2026, as reported on Oct 14**: Pavel spoke of "вчера… двухчасовой митинг с Сергеем Димой и ирой", "назначен в 04:30"; that it is this meeting is an **inference** from the people named — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

## Update, Oct 14 2026 — Kharetski finishes the passport work and tests the battery (task 246); MVP 1 to about November 8–9; the two-hour meeting was held

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]:

- **[[wiki/people/evgeny-kharetski.md|Kharetski]].** He finished the passport work the day before ("закончил вчера… паспорта"; the verb is garbled). That this is work on this branch is an **inference** from his assignment here. He tested it on a real machine himself: all devices report. One problem: some devices are detected as missing at once, others only after work; in some places it is a hardware limit, in others the library. With little time, he left the device logic as it is — changing it "достаточно серьёзная вещь". Today he tests the battery — task 246 — with a sub-task for the test. Then MVP 2 tasks.
- **The date.** Pavel extended MVP 1 to about November 8 or 9, with the MVP 2-marked tasks inside it; the team still delivers the old version, the one first cut — [[wiki/decisions/2026-10-14-mvp1-is-extended-to-about-november-8-or-9-and-the-mvp2-marked-tasks-are-done-inside-it.md]] (read as this RIS line — **inference**). The Georgia-only, 1.14-line scope of this page is not changed.
- **The separate meeting.** Pavel spoke of a two-hour meeting the day before with Sergey, Dima and Ira, scheduled at 4:30 — read as the Oct-13 "after lunch" meeting (**inference**). Tsymanov: after "последних нашего обсуждения" a plan for building his task (heard as "бип 35 22") must be discussed. The meeting itself is not in the corpus.
- **1241** is not mentioned; the Oct-12 commitment stays open.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_RIS_Georgia_Branch_and_Critical_Error_Text-October-6-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Test_Coverage_First_and_AI_Task_Numbers-October-7-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
