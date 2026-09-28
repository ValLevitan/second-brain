---
type: decision
title: The main branch must always contain working code anyone can pull and build, and the code belongs to the project rather than to any one developer — confirmed already in force
date: 2026-09-14
aliases: [main branch must always build, main must always contain correct working code, the code belongs to the project, not to any one developer, paragraph 2 sentence 1, paragraph 2 sentence 4, code standards email September 14 2026, small frequent commits, 2-3-4 commits a day, someone else merges the pull request, menbrange mast always contank crind working cor, code standard]
source-count: 3
status: active
open-commitments: 0
open-questions: 4
---

# Main must always build, and the code belongs to the project

On the morning of **September 14 2026** [[wiki/people/val-levitan.md|Val Levitan]] sent a **code-standards email** — "**Адресован Павлу и алексееву**", addressed to [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] — with the others on the call in copy ([[wiki/people/andrey-bosik.md|Andrey Bosik]] had read it, [[wiki/people/alexei-khamin.md|Alexei Khamin]] confirmed "**Да это есть**", and [[wiki/people/irina-shishko.md|Irina Shishko]] had **not** received it), and called a **21-minute meeting minutes later** ([[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|Sept 14 2026, 7:37 AM]]) to read two of its sentences aloud and have the team confirm the rules already hold. Val opened with "**У нас есть вы вы получили мой email да? Я только что отправил**" — "did you get my email, I've just sent it" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

The meeting was held **in Russian** and the Teams transcription garbles nearly every English technical term; the quotes below are given as rendered, with the reading in brackets.

**This is a confirmation, not a new rule.** Val's framing: "**Правила, которые я описал стандарты, которые описал. Они нами приняты, и они у нас, насколько я понимаю, у нас работают, да?**" — the rules and standards I described are accepted by us and, as far as I understand, already work here. Bosik, who had already read the email: "**Я уже прочитал, да там в принципе. Ну очевидные вещи, да, которые у нас они и так уже и работают**" — obvious things that already work here [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Paragraph 2, sentence 1 — main must always build

Val read the sentence out in English through Russian phonetics, twice:

> "**да ты я дань бранчэйн бранч масс олвейс контейн corrent working cord**" … "**Энни уан ундэтим мост эйбл туполэд and and bealld ay working in stoler and eny thine**" … "**Энэфмей дознот. Белт. Тогда фикси бекам**"

Read as: *the main branch must always contain correct working code; anyone at any time must be able to pull and build a working installer at any time; and if main does not build, then fixing it becomes [the priority]*. The last clause is cut off in the transcription and the priority word is not recoverable — Val states the priority in his own words a minute later instead [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Later in the call he quotes the same sentence again as "**menbrange mast always contank crind working cor**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

His own gloss, in Russian:

- "**Потому что менее может быть поломан**" — read as *because main cannot be broken*; the negation is missing in the transcription, but the following sentence makes the sense certain: "**Имеем в себе не может иметь скот, который не работает, который не собирается**" — main cannot contain code that does not work, that does not build [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **The point of the sentence is an assumption other people are entitled to make.** "**если в men… есть коуд то мы о сум, что этот кот не поломанный**" — if there is code in main, we assume that code is not broken. "**его любой человек из команды, или это qвей или это другой девелоп… может рассчитывать, что этот код работает. Он берёт этот код мейн и может в принципе установить этот девайс. С теми лист ноутз, которые существуют на сегодняшний день**" — anyone on the team, QA or another developer, can count on that code working, take main, and install it on the device using the release notes that exist today [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. *(The clause naming the second kind of person, "**про который мы даём новый Саймон**", is not recoverable; the derived notes read it as a new developer being brought in. Not asserted here.)*
- **The failure test is named against a real person — the QA engineer.** "**если Алексей берет этот код и не может установить его, просто взять и установить на машину. Это значит, что код не работает или релиз ноут неправильный. Или проза неправильная, но чтото гдето неправильно работает. Значит, приоритет должен быть на то, чтобы это работало**" — if [[wiki/people/alexei-khamin.md|Alexei Khamin]] takes the code and simply cannot install it on a machine, then either the code does not work, or the release note is wrong, or the **prose** is wrong; something somewhere is wrong, and the priority must be making it work [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. "Prose" is JVL's plain-language in-repo documentation standard — see [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]] and [[wiki/topics/github-release-management-pipeline.md]].

**The team confirmed it, with a qualifier Val accepted and then adopted himself.** Val: "**Поправьте, поправьте меня, если я не прав**" — correct me if I'm wrong. Pavel: "**Инженерал все правильно инженерал**" — *in general*, all correct. Val took the hedge deliberately: "**давайте будем говорить ingeneral, потому что сейчас вы проведёте какойто такой пример искажённый, который я почешу голову и скажу, ну не знаю. А просто, поскольку я ещё и не инженер, то мне вообще тяжело на эту тему говорить**" — let us say *in general*, because you will produce some twisted example and I will scratch my head; and since I am not an engineer it is hard for me to argue this. Bosik: "**Так и есть**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Paragraph 2, sentence 4 — the code belongs to the project

Val: "**Теперь давайте рассмотрим 4 последнее предложение в этом параграфе**" — now the fourth, last sentence in this paragraph — then read it: "**Да коут белон студэ проджект. Not to andy wand developers**" — *the code belongs to the project, not to any one developer* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

His expansion turns it into a right that QA holds:

> "**Не девелопер он дестил или киуэй… Если он чтото ставит и не работает. И особенно сегодня с использованием клад коуд. Он может предложить исправление, может инф исправить этот колд. И может сделать камид этого кот не камит, а сделать пулурек… Репортер на этот полреквест может этот пурек посмотреть и сказать да. Это действительно правильно. И сделать камид и втянуть его в мень.**"

Read as: *not a developer — a tester or QA — if he installs something and it does not work, then especially today with **Claude Code** he can propose the fix, make the fix, and raise a pull request rather than a commit; the reviewer on that pull request looks at it, says yes this is genuinely right, commits and pulls it into main* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Bosik: "**Все верно**"; Pavel: "**Да**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

*Two readings flagged rather than asserted: "**Репортер**" is read as **reviewer** (the role that examines a pull request), which is how the derived notes read it too — but "reporter" is the literal rendering and the transcription is not decisive [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. The phrase immediately before, "**Со email the stermen**", is not recoverable and nothing is claimed from it.*

This is the **AI-assisted** half of the rule: Val's argument is that a non-developer can now act on the code at all, and the reason he gives is Claude Code. See [[wiki/topics/ai-assisted-development.md]] (Sept 14).

## The working practice Val holds up as the model

Described in the first person, as the contrast to holding code on a local machine:

> "**Я написал часть кода китхаб хорошо сохраняет персионность… Давайте я проверю, как этот код интегрируется… когда его втягивают в мень я прохожу все вот эти тесты, и я там иду по 300 линий кода, значит, это понемножку понемножку я делаю камин 234 раза в день. И каждый раз я проверяю через интеграционные тесты не поломала я чтото, а потом [реви]к может взять и сделать [ревью] тоже на какойто вменяемый кусок работы, а не на огромный кусок работы, который неделю нужно проверять. Тогда все синхронно двигается вперед.**"

Read as: *write part of the code; GitHub holds the versioning well; check how it integrates; when it is pulled into main run all the tests; go in roughly 300 lines of code at a time; commit **2, 3, 4 times a day**; each time check through integration tests that nothing broke; then the reviewer gets a sane chunk of work to review rather than a huge one needing a week — and everything moves forward in step* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

*The "300 lines" figure is quoted as rendered ("**я там иду по 300 линий кода**") and is Val describing his own habit, not a stated standard. "**камин 234 раза в день**" is read as 2–3–4 times a day. The word for what the reviewer does ("**сделать no and**") is garbled; review is the reading, from the "**вменяемый кусок работы**" contrast.*

## Pull requests — someone else should merge, but it is a preference

Bosik raised the only objection to the email: "**Единственное там по поводу только полриквестов. У меня есть замечание, что не всегда. Кто то другой должен мержить? Пол реквест бывает так, что иногда надо самому замерзть**" — it is not always someone else who merges; sometimes you have to merge your own [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

Val agreed on the spot and softened the rule to a preference: "**Всегда ктото должен, но мы всегда или часто находим исключение… Это Я согласен. Но желательно, чтоб ктото другой [мержит]**" — someone else always should, but we often find an exception; it is preferable. Bosik: "**Ну мы так и стараемся делать**" — that is what we try to do [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Why Val says the team can teach this

"**Тем стандартам, которые мы совсем недавно сами адаптировали, то есть для нас они тоже были новые. Мы тоже мучились, и мы тоже не понимали, как это работает. И нам тоже было тяжело**" — the standards were new to us too, very recently; we also struggled and did not understand how it works [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Bosik said the same about the team, twice: "**Через это все прошли**" — everyone went through this [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

That places this email at the end of the standards-writing arc that runs through [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]], [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]] and [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] — *(the link between the email and that repository is an inference; no source states where this code standard is stored)*.

## What the email itself is

**Not recoverable from these sources.** Val names the subject once — "**Называется флегспорт иголог metruzan proyrice**" — and the transcription is unusable; the derived notes flag the same thing and recommend confirming the subject line with Val before treating it as fact [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. What is certain is that it has **numbered paragraphs with numbered sentences** (Val cites "paragraph 2, sentence 1" and "the fourth, last sentence in this paragraph"), is written in **English**, and covers at least: main-branch build health, pull-request review, and code ownership [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## Update, Sept 24 2026 — the 300-line habit becomes an instruction

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM MVP 1 call]] (Russian), [[wiki/people/ivan.md|Ivan]] said his new connection-test work was "пока что у меня только локально на компьютере никуда не комичено". Irina explained he had done it that morning and would commit in the evening [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]].

Val: "Я, я категорически я категорически против этого." Then, as a rule for everyone [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- "у нас должен быть comid в йетхабе малта полтай day" — read as a commit to GitHub multiple times a day (**inference**; he says "китхаб" and "Акит хаб" in the same passage).
- "Я хочу видеть 300 лайнзов… comits в среднем. Это может быть 10 раз в день."
- "Я не хочу, чтобы на локал компьютере было больше, чем 300 лайнов." Reached 300 lines — push it.
- "Я не хочу… эксьюсис… Эти эксьюсис это прошлое… все получили амнистию." And: "я за ним слежу, я хочу видеть прогресс."

**What changed.** On Sept 14 the 300 lines and "2, 3, 4 times a day" were Val describing his own habit, not a stated standard (above). On Sept 24 he states them as what he wants from every developer: about 300 lines per commit on average, and no more than 300 lines held locally. Treated as **evolution** (§11), not a contradiction.

## Open questions

- **What the code-standards email's subject and full contents are.** The subject-line transcription is unrecoverable; only two sentences of paragraph 2 were read aloud — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]] [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- **Who merges a pull request when no second person is available.** Named by Bosik as a frequent exception and accepted as one; no rule was written — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- **[[wiki/people/irina-shishko.md|Irina Shishko]] did not receive the email.** "**У меня нет… Интересно, а почему меня не хочет меня присылать? Ну ладно**" — she was not on it and no one followed up in the call — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- **Which two "points 1 and 4" Val meant.** He says "**Вот эти 2 пункта 1 и 4 это что Алексеев пропускает?**" — these two points, 1 and 4, are what Alekseev skips — immediately after reading sentence 4, so the plain reading is sentences 1 and 4 of paragraph 2. The derived notes instead gloss the pair as "small frequent commits, and code belonging to the project" [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. **Recorded as unresolved; neither reading is asserted** — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

**§15.8:** clear on this page — engineering rules and process only. The personnel-adjacent half of the same meeting is held separately and partly withheld; see [[wiki/decisions/2026-09-14-alekseev-is-walked-through-the-standards-by-bosik-not-ordered.md]].

## Sources

- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
