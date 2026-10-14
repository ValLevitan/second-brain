---
type: decision
title: The AI PM goes live in real Jira projects on Monday Oct 12 on its current architecture (change it later if needed); Lena's meetings leave the pilot; the agent deletes only what it created and only comments on the rest; the agent is not genderless and gets a name
date: 2026-10-08
aliases: [AI PM live October 12, боевой режим, launch with current architecture, Lena out of the AI PM pilot, agent deletes only its own items, AI Draft status, AI Draft lifetime, Dasha, the AI PM is not genderless, two kinds of draft]
source-count: 9
status: active
open-commitments: 5
open-questions: 3
---

# The AI PM goes live on Oct 12 on its current architecture

Set on the [[wiki/meetings/2026-10-08-ai-pm-listener-scope-draft-lifetime-and-october-12-go-live.md|Oct 8 2026 AI-PM review]] (Russian), chaired by [[wiki/people/val-levitan.md|Val Levitan]], with [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]. It continues [[wiki/decisions/2026-09-29-bosik-owns-the-ai-pm-the-meeting-bot-waits-and-the-second-brain-is-built-first.md]]. The whole picture is on [[wiki/projects/ai-project-manager-and-company-second-brain.md]].

## 1. Launch on the current architecture; change it later if needed

Val challenged the design. The Listener does too much: it reads the meeting, judges which capability a topic belongs to, writes features, improves itself and audits itself. He does not believe one agent can carry all that, and he thinks it will not hold up for a real-time agent in MVP 2, 3 or 4. He said he saw, the day before, a demo of a system that takes part in meetings in real time, and he knows who builds it. His proposal: the Listener only listens and adds to a vocabulary (taxonomy) of words and phrases; a separate agent does the processing [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

Bosik: he built a frame for MVP 1 so that it works at all; it is "не бетоном не залит" and can be split into more agents later. Pavel: the task had been "Сделайте за неделю"; the design copies a person who sits in a meeting, then reads the repositories and Jira, then writes tasks — one linear flow; branching into parallel agents is the more advanced system everyone ends up with. Kovalchuk: the first aim was to stop losing tasks discussed at meetings and to take the load off Pavel; a live participant is a different thing [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

Val closed: "давайте запустим… Если надо, поменяем архитектуру" [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## 2. Live mode in real Jira projects from Monday Oct 12

Bosik: "в понедельник я включаю боевой режим, фичи начнут создаваться уже в своих проектах"; earlier, "мы планируем к 12 октября это включить". Until then the features go to a test project. Val: on Monday the system is switched on and "мы можем посмотреть, как она работает" [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## 3. Lena's meetings leave the pilot for now

Bosik had set up collection for six people: Pavel, Irina, [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/lena.md|Lena]], Kovalchuk ("димины") and himself. Val asked to remove Lena for now and add her team in a second stage. His reason: keep the team out of needless arguments until it can say the tool has worked for a month and brings real value. Bosik argued that more knowledge of the whole company helps the agent, then agreed to remove her [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## 4. The agent deletes only what it created; on everything else it only comments

Bosik: the agent may delete a feature or story only "при условии, что само его создавало", so that it does not delete other people's items. On items it did not create it can only leave a comment. It does not edit descriptions; a duplicate found later gets a comment, not a rewrite. Wider rights maybe later — "давайте мы пока посмотрим, как это будет работать" [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## 5. The agent is not genderless and gets a name

The image prompt had said genderless; the generated face came out female. Val: "я настаиваю в нашей компании такого я не позволю, чтоб бесполый был… дайте ей имя". After Irina named "Даша", Val: "назовите её дашу" [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]. The notes record "Dasha" as proposed, not final [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## Not settled — how long an "AI Draft" item lives

Everything the agent creates in Jira has the status "AI Draft"; a person must move it to To Do or reject it. Untouched items are deleted after a set time "чтобы не накапливать мусор". The previous meeting set one day (Bosik: "на прошлом митинге решили один день у меня было 3 написано"). Kovalchuk: a meeting at 19:00 Minsk time will not be seen by morning. Bosik: the morning report comes in the morning, so the window must be more than one day — "Давайте хотя бы 2 сделаем". Pavel and Kovalchuk agreed with more than one day. Pavel: weekends must not count — a Friday item must not be deleted before Monday; Bosik had planned this but not built it [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

Val then argued against seeking the middle of all opinions. In his words, that leads to "разжижению бульона"; he would rather rely on one person's position, even a wrong one, because the mistakes then belong to one person and can be found and fixed. He asked why keep "гарбич" a small team cannot read and will discuss again at the next meeting anyway [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

No value was ruled. Later in the call Bosik twice described deletion "на 2 день" [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]. The notes: "No final value was clearly stated" [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — remove Lena from the list of people whose meetings the agent collects — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — improve the Teams agent so it gives real answers (Val: "в понедельник посмотрим") — due Monday Oct 12 2026 — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — make the AI Draft deletion skip weekends (planned, not built) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — add an "AI Draft" column per person to the morning report (Pavel: include a Jira link filtered by person) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

## Open questions

- How long does an AI Draft item live before deletion — one day (the previous meeting) or two or more days (Bosik, Pavel, Kovalchuk)? Not ruled — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- Will one Listener that does everything scale to a real-time agent in MVP 2 and later? (Val) — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- When does the agent get access to the second brain? Val asked; Bosik answered only with today's four sources — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

**§15.8 / personal:** remarks about the character of named people and personal remarks are not recorded. No pay matters. **§15 #9:** none.

## Update, Oct 9 2026 — "Dasha" runs in test mode; production on Monday "if we make it"; tasks arrive as drafts to accept or reject

At the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian) [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]: "Мы запускаем в тестовом режиме вот этот вот агент её будут звать пока что даша, возможно потом переименуем" — tasks may appear in the test project, "не пугайтесь". "Планируется запуск уже в работу в прод в понедельник… если мы все успеем." Pavel: each person gets it in the daily email report, with links to the tasks on them. Kovalchuk: the tasks will have a draft status ("статус айдрафт") and must be accepted or rejected; there will likely be a link to the meeting where it was discussed [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

The same morning Chudinov told the bot not to create a task from his weekend roll-out remark ("пометка для бота не создавай") — the team already speaks to the agent in meetings [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## History

- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — switch on live mode so features are created in the real Jira projects — due Monday Oct 12 2026 — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] — discharged on the day, as reported: at the Oct-12 stand-up Pavel said "у нас всё с сегодняшнего дня начинается" and Kovalchuk that it has started; that the items land in the real projects is not said in words (**inference**) [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [x] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — give the agent a name ("Dasha" proposed) — discharged: on Oct 9 Kovalchuk said it is called "Dasha" for now, maybe renamed later — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

## Update, Oct 12 2026 — it starts on the day; the team reviews "AI Draft" tasks from the next morning

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) Pavel asked [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] to tell the team "что у нас всё с сегодняшнего дня начинается". Kovalchuk: "Ну вот оно уже всплыл, да с сегодняшнего дня тестов запускаем. Мы смотрим, как оно всё будет работать." [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]

- **The routine.** Pavel: "нам надо будет с завтрашнего утра брать по какомуто фильтру задачи" — from tomorrow morning (Oct 13) everyone takes the tasks by a filter. Kovalchuk: tasks "со статусом [AI Draft]", to judge whether the agent proposes something true or not.
- **How to say no.** Chudinov asked how to close one that is not needed. Kovalchuk: "Ты выбираешь реджект и выбираешь в резолюшн, почему то реджект. Там некоторые варианты есть и можно еще текстом комментарии написать." "Пока что так, если этого будет недостаточно, то будем изменять."

So the Oct-12 go-live date held (**evolution** from the Oct-9 "если мы все успеем"). The draft lifetime question below is not touched. The derived notes date the review "From October 13" [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]].

## Update, Oct 13 2026 — the PM agent's questions are merged and discussed the next day

At the [[wiki/meetings/2026-10-13-daily-standup-video-decode-memory-and-release-task-type.md|Oct-13 Minsk stand-up]] (Russian) [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] asked whether to discuss what the PM agent wrote that morning: it had marked the tasks discussed, "но это не совсем фичи", more like questions, "что бы оно не потерялось". Pavel: "Давайте тогда для нашего IPM попросим все вопросы, которые на вчерашний митинг он собрал[,] консолидировать с вопросами сегодняшнего митинга и завтра мы их обсудим." [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]

The notes leave the person who asks the agent **unassigned** [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]].

### Open commitments (Oct 13 2026)

- [x] Unassigned — ask the PM agent to merge the Oct-12 and Oct-13 questions; the team discusses them on Oct 14 — due Oct 14 2026 — [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]] — **discharged Oct 14 2026**: Kovalchuk — "агент объединит вчерашние задачи. Сегодняшние, собственно, он это и сделал"; the list was gone through at the stand-up — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

## Update, Oct 14 2026 — the merged list is reviewed; the agent mixes up people with the same name; "посмотреть, к чему это приведёт"

At the [[wiki/meetings/2026-10-14-daily-standup-mvp1-extension-and-rk3576-game-library.md|Oct-14 Minsk stand-up]] (Russian) [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] shared the chat where the agent posts [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]:

- **The daily digest.** "Андрей настроил то, что он присылает нам каждое утро в 11:30" — a list of what did not get into Jira. The Andrei is likely [[wiki/people/andrey-bosik.md|Bosik]], who owns the AI PM (**inference**). The team should say for each item whether it belongs in Jira, is only for understanding, or is not needed. Pavel: "можем обсуждать, посмотреть, к чему это приведёт на самом деле." The notes record this as a decision: keep reviewing the digest [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]].
- **The merge worked.** The agent merged the Oct-13 and Oct-14 items, as asked, and created the leak task on Daniil (see [[wiki/topics/nova-platform-architecture.md]] (Oct 14)).
- **Same-name mix-ups.** It "не всегда понимает про какого, например, Андрей идёт речь" — Andrey Bosik or Andrei Klimovich — or which Dima, Kovalchuk or Chudinov; it sometimes confuses them.
- **Items it listed:** how to free, load and decode bonus video; how to treat a release branch (see [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]], Oct-14 update); an emulator smoke test on each commit (garbled); the Flex IQ not scanning tickets in the dark room (Chudinov had not checked yet).
- **Cautious.** Kovalchuk: "у него сейчас гайки закручены" — it hesitates a lot before creating anything in Jira.
- **A gap.** Pavel: the two-hour meeting the day before with Sergey, Dima and Ira is not in the list. Kovalchuk thought it was a call without transcript access; Pavel: it was a full meeting scheduled at 4:30. Kovalchuk then said this digest may cover only this stand-up's topic; he will ask Andrei. Irina asked whether the transcript can be fed to the agent; Kovalchuk: yes, post it in the chat.

### Open commitments (Oct 14 2026)

- [ ] [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] — ask Andrei (Bosik likely — inference) why the two-hour Oct-13 meeting is not in the AI digest — due Oct 14 2026 — [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]

## Sources
- [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Video_Decode_Memory_and_Release_Task_Type-October-13-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026.md]]
