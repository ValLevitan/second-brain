---
type: decision
title: Andrey Bosik walks Evgeniy Alekseev through JVL's code standards and practices explaining the reasons rather than issuing the order — booked for the next morning inside his 07:00 window
date: 2026-09-14
aliases: [Alekseev coaching, explain the reasons not the order, Bosik takes Alekseev through the standards, 07:00 window, onboarding Alekseev onto the code standard, single developer no branches, code on the local machine, large portions of code, tell me and I will implement it]
source-count: 2
status: active
open-commitments: 2
open-questions: 1
disambiguation: "Evgeny/Zhenya cluster — EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name): [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] = FlexPort/FlexPay integration software (alias Egorsky); [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] = LGS/Omni backend (payroll \"Kharetski Yauheni\"; garble-aliases Koretski/Khorvatsky). Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. NO fourth Zhenya exists — a mention fitting none clearly is a mis-heard non-Zhenya (cf. Ethan/Efim), so treat as garble/mishearing and queue; NEVER create a new Zhenya. This page: Alekseev ('Алексеев', named in full in the source), resolved by embedded/Flex-Port context."
---

# Bosik takes Alekseev through the standards — reasons first, not an order

The personnel-adjacent half of the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|September 14 2026, 7:37 AM code-standards call]] (Russian, ~21 minutes). The engineering rules themselves are on [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]]; this page carries the **process and resourcing** ruling that came out of them.

**§15.8 — what is deliberately NOT on this page.** The call contains repeated personal and performance assessments of [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] by [[wiki/people/val-levitan.md|Val Levitan]] — how good an engineer he is, what kind of person he is, and whether he is worth keeping. **Those judgements are excluded from the wiki by §15 #8**, together with any compensation or engagement terms (none appear in the source in any case). What is recorded below is the **engineering working method, the coaching instruction, the scheduling constraint and the resourcing contingency** — the facts a reader needs to understand what happened to the work.

## The working-method problem, stated as engineering

Alekseev is described as landing code in very large units because he does the work locally first:

> "**Кладёт код… большими порциями. Там огромное количество строчек, потому что он работает у себя на локальном компьютере, всё делает, а потом…**"

— he puts code in in large portions, a huge number of lines, because he works on his own local machine, does everything there, and only then [lands it] [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**He works as a single developer with no branching off his branch.** Val, explaining why [[wiki/people/pavel.md|Pavel Frolov]]'s long-lived-branch objection does not apply to Alekseev's situation: "**Алексеев он в принципе делает он сингл девелопер. У нас нету там ответлённых бранчей, и он берёт бранч он его, он выполняет его, потом у него втягивает мень**" — he is effectively a single developer, there are no branched-off branches there, he takes a branch, completes it, then it is pulled into main [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**Val's causal account ties the behaviour to the missing documentation, not to the person.**

> "**он привык работать в старой системе, где он делает, где он держит весь код. Он считает, что это его код… Должен его охватить своими руками, и он должен быть в курсе всех дел, потому что нету ни прозы, ни описания, ни релиз[-ноутз]… ничего нету этого. Потому что он держит у себя на локальной машине.**"

— he is used to the old system where he holds all the code, considers it his code, has to cover it with his own hands and stay across everything, *because there is no prose, no description, no release notes, none of that* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. This is the mirror image of the main-branch rule: the assumption "anyone can pull main and install it" only works if the prose and release notes exist. See [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]].

**The consequence Val names is a rule about who may touch the code.** Alekseev's position, as Val reports it: "**хорошо, если есть ошибк[а], ты её нашел. Так скажи мне, я это сделаю, я это внедрю. Но не лезь сам своими руками туда**" — fine, if there is a bug and you found it, tell me, I will do it, I will implement it — but do not go in there yourself. Pavel confirmed the characterisation: "**Это было примерно так**" — it was roughly like that [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. That is the direct opposite of paragraph 2's "the code belongs to the project".

**Val's diagnosis of the cause:** "**Я просто думаю, что ему сказали делай так без объяснений без ничего. И он импровизирует, как ему нужно делать, как ему удобно делать**" — he was told *do it this way* with no explanation, so he improvises whatever is convenient [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

## What was decided

- **[[wiki/people/andrey-bosik.md|Andrey Bosik]] books a meeting with Alekseev and takes him through the standards and practices.** Val: "**Я бы хотел бы, чтобы Андрей [Бо]сик… Назначил с ним митинг и проговорил все эти варианты и объяснил, почему мы это делаем**" — book a meeting, talk through all these variants, explain why we do this [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Reasons, sequence and dependency — not an order.** Val specified what the explanation must contain: "**объяснил ему причину, почему мы так хотим делать? Почему мы от этого зависим? Какая должна быть последовательность?**" — the reason, why we want it this way, why we depend on it, and what the sequence should be. And what it must *not* be — an instruction delivered as "do it because we said so" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Bosik: "**Нет, я умею объяснять нормально**" — I know how to explain properly [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Bosik had already started the same thing independently.** "**Он мне еще не ответил, но я ему писал по поводу Того, что нам надо запланировать с ним время, как раз настроить код, провести небольшое обучение, и как раз я его введу в наши, так сказать, стандарты и практики, как мы разрабатываем**" — he had written to Alekseev about scheduling time to set the code up, run a short training and introduce him to *our standards and practices, how we develop*, and was waiting for a reply [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. That continues the Sept-7 undertaking to get him onto Claude Code — see [[wiki/people/evgeniy-alekseev.md]] (Sept 7).
- **The meeting goes in the 07:00 window, the next morning.** "**в 07:00 он может взять митинг в 8 он уже бежит на работу к себе. У вас есть час… назначить с ним митинг? Пожалуйста, на завтра утром**" — at 07:00 he can take a meeting; by 8 he is off to his own job; you have an hour; please set it for tomorrow morning. Bosik: "**Хорошо**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. *("Tomorrow morning" = **September 15 2026**; Alekseev holding a separate job of his own is stated by Val here, and matches the weekend-only working pattern recorded on his page from Sept 7–9.)*
- **The fallback is a resourcing one, and Bosik is the judge of it.** "**Если вы чувствуете, что мы с этим человеком никуда не продвинемся, и если наш коллектив чувствуешь, что так это не получится. То, конечно, нам нужно искать другого [девелопера]. Сейчас не хотелось бы… я бы хотел бы эту ситуацию спасти и улучшить, но не поломать**" — if you feel we will get nowhere and the team feels it will not work this way, then of course we need to look for another [developer]; but not now if it can be helped — I would rather save and improve the situation than break it. Bosik: "**Всё понятно**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. *(The word rendered "**другого договора**" is read as **другого девелопера** — another developer — which is how the derived notes read it as well [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Flagged, not certain.)*

## Manner of delivery — Val closes with a joke about it

Val ended the call by telling Bosik his father's old joke about the soldier sent to tell a wife her husband had been killed at the front, who knocks and opens with "**Здравствуйте, здесь живёт вдова Иванова**" — *hello, does the widow Ivanova live here* [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. It is the instruction restated as a warning about how the conversation opens.

Bosik's answer is his own stated method and does not concede the point: "**Я знаю этот [анекдот]… но я всегда считаю лучше прямо и сразу сказать, чем какимито обходными путями**" — better to say it directly and straight away than to go around [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]. Recorded on [[wiki/topics/jvl-operating-principles.md]] (Sept 14).

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — book a meeting with [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] for the next morning inside his 07:00–08:00 window and take him through JVL's code standards and practices, explaining the reasons, the dependency and the sequence rather than issuing an instruction — due **Sept 15 2026** — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — tell Val if he judges, after that meeting, that the new way of working will not be adopted — due after the meeting above — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Open questions

- **Whether the meeting happened and what came of it.** Alekseev was not on this call — "**На этом митинге его нету… Он не сидит на месте**" — and no later source in the wiki reports the outcome — [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]

## Sources

- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
