---
type: decision
title: The AI PM goes live in real Jira projects on Monday Oct 12 on its current architecture (change it later if needed); Lena's meetings leave the pilot; the agent deletes only what it created and only comments on the rest; the agent is not genderless and gets a name
date: 2026-10-08
aliases: [AI PM live October 12, боевой режим, launch with current architecture, Lena out of the AI PM pilot, agent deletes only its own items, AI Draft status, AI Draft lifetime, Dasha, the AI PM is not genderless, two kinds of draft]
source-count: 2
status: active
open-commitments: 6
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
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — switch on live mode so features are created in the real Jira projects — due Monday Oct 12 2026 — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — improve the Teams agent so it gives real answers (Val: "в понедельник посмотрим") — due Monday Oct 12 2026 — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — make the AI Draft deletion skip weekends (planned, not built) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — add an "AI Draft" column per person to the morning report (Pavel: include a Jira link filtered by person) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]] [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — give the agent a name ("Dasha" proposed) — due unspecified — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

## Open questions

- How long does an AI Draft item live before deletion — one day (the previous meeting) or two or more days (Bosik, Pavel, Kovalchuk)? Not ruled — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- Will one Listener that does everything scale to a real-time agent in MVP 2 and later? (Val) — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- When does the agent get access to the second brain? Val asked; Bosik answered only with today's four sources — [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]

**§15.8 / personal:** remarks about the character of named people and personal remarks are not recorded. No pay matters. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
- [[raw/Meeting_Notes_AI_PM_Agent_Listener_Scope_and_Draft_Lifetime-October-8-2026.md]]
