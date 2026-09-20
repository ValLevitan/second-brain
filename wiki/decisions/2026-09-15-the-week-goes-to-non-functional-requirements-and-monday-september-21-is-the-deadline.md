---
type: decision
title: Val repoints the rest of the week at the non-functional requirements, names the five people who own them, and sets Monday September 21 as the deadline for a grooming pass over the whole of MVP 1
date: 2026-09-15
aliases: [if it is not written it does not exist, non-functional requirements owners, nonfunctional requirements week, September 21 deadline, MVP1 grooming meeting, engineering ideology, architecture ideologist, это не написано этого нету, нон фанкшинал, Sonos analogy]
source-count: 2
status: active
open-commitments: 3
open-questions: 1
---

# The week goes to the non-functional requirements; Monday September 21 is the deadline

The closing block of the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept 15 2026 8:03 AM call]] (Russian), and the sharpest [[wiki/people/val-levitan.md|Val]] has been in this series. It escalates the standing Sept-7 ruling that error recovery and non-functional requirements come before extra functionality ([[wiki/decisions/2026-09-07-error-recovery-and-non-functional-requirements-come-first.md]]) from a priority into a schedule with named owners and a dated gate.

## What worries him, in his own list

Val, stopping the meeting before it could end: "у нас есть ряд нон фа[нкшнл]… Меня очень волнуют вещи, как вот таймер, hanch[sh]aking… [en]cryptions… **чтото зависло[,] какие то коммуникейшнс не прошли[,] пенги между девайсами**… Потом у нас вайфай, мы собираемся ввести… **юнит[иф]икейшнс юник намберс**" — timers, handshaking, encryption, hung states, communications and pings between devices that never arrive, the Wi-Fi about to be introduced, and unit identification / unique numbers [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. *(The last item is garbled in the transcript; "unit identification numbers" is the derived notes' reading and is recorded here as an inference, not as spoken text.)* [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**The Sonos analogy carries the point.** Val described the multi-room audio system he has at home — devices that sit on Wi-Fi, each one a separate device configured once, fed by a music provider over the internet — and then the failure mode: "иногда выключается там какой то… девайс… и я про это не знаю". Applied to a location: "**у нас будет на лакейши[не] своих какихто куча вай фай девайсов. Меня очень волнует, что мы думаем, что они подключены, что они работают… а на самом деле они отвалились. Но… у нас это невозможно. Мы не можем позволить, чтоб чтото отвалилось. Как это будет обратно подключаться, как мы об этом будем знать? Как будет подниматься тревога?**" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## "If it is not written, it does not exist"

[[wiki/people/dmitri-chudinov.md|Chudinov]] answered with what exists rather than what is written: "**могу сказать, что требования не прописанные, но у нас реализована система графана, где в будущем возможны настройки на алерты различных ситуаций**" — Grafana is in place, alerting could be configured in future. Val cut him off [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **давайте начнём с Того, что я устал. Мне надоедает слушать, что мы знаем, но это не прописано. Давайте закончим это… Это, если это не написано, этого нету.**
>
> *(let us start from this: I am tired. I am sick of hearing that we know it but it is not written down. Let us end this… If it is not written, it does not exist.)*

The rest of the demand, in one run [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

- **The prose in the repository must match the capabilities and carry tests.** "У нас должно быть прописано. У нас должен быть на этой репозитории… должна быть проза[,] проза должна совпадать с этими [capabilities]… На это должны быть [авто]тесты." *(The transcript renders the test word twice as "Антон тесты" and "not тесты"; read as **auto tests** from the identical Sept-7 demand, and flagged as an inference.)*
- **There must be an ideology set from above.** "**должна быть инженерная идеология с… сверху. Должен быть идеолог архитектуры[,] которые это диктует.**" His split of concerns: "инженера должно волновать это вот так, а меня волнует, а как это будет работать? А как обеспечить стопроцентно?"
- **Transcription removes the last excuse.** "**Особенно, что сейчас можно все разговоры записать на транскрипт. Очень удобно их выложить через [Клод], расписать[ —] не надо больше на это время тратить[,] это быстро делается.**"
- **Without them the product cannot ship.** "**то есть у нас нету идеологии, у нас нету на это планов[,] у нас нету на это реква[йр]мент[ов]. Мы не можем выпустить продукт без этого, потому что мы не можем сделать [авто]тесты.**"

## The five owners, named aloud

Val named them so the record would be unambiguous — "чтобы все знали, что кто из [спонсоров] я назову по имени" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **Это дима чудинов, Андрей босик, Ирина шишко, Александр биратко и Павел Фролов.**

That is [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/pavel.md|Pavel Frolov]] — five engineers. [[wiki/people/andrei-klimovich.md|Klimovich]] is deliberately **not** on the list; his job in the same days is the other half. Earlier in the same block Val had already pointed at the same people and asked whether the requirements exist anywhere; Chudinov answered "для флекс[а] и кью я создавал" — he had created some for Flex IQ — and Val widened the scope to "[Флекс] пей, флекс[ ]порт… и флекс айкью" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## The week, fixed

- **Tomorrow's 8:00 AM meeting is repointed.** "давайте завтра мы не будем фокусироваться на климовиче, задачах или кейпобио[лити]с. А будем концентрироваться на ваших нон фа[кт]… значит, завтра митинг… в 08:00, который посвящается вот именно этому."
- **Wednesday, Thursday and Friday finish them.** "у нас есть среда, четверг и пятница, где мы добьём нонфа[нкшнл] реквамус." Val cannot attend Thursday — "В четверг я не смогу быть на митинге" — and will be back Friday — "[Фрай]дэй я смогу опять быть на митинге."
- **Klimovich uses the same days for his side.** "За это время Андрей климович добьёт все свои кейпа билетис, [ре]квайме[нт]с[,] всё почистит."
- **Monday September 21 is the gate.** "**и в понедельник давайте 21 числа… мы проведем митинг, который груми[нг] и всё соберёт на MVP фанкшин[ал] и нон фанкшин[ал], и мы быстро бегло пробьём[,] пройдём по всем кейпобит[и]с[;] к этим кейпобило[ти]с будут уже… фанкшин[ал] и нон фанкшне[л][ — ] в понедельник, 21 числа это последний день.**"

Val asked for agreement and got it from Pavel ("Окей"), Bosik ("Да") and Klimovich ("Окей") [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]. Klimovich's own proposal in the same minutes — that the daily call become standing practice, "я предлагаю сделать это постоянной практикой[;] судя по всему, нас каждый день есть что обсуждать" — was accepted by Val as "хорошая практика" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Why this is an escalation and not a repeat

The Sept-7 ruling said non-functional requirements come first and named their form (a single-line acceptance criterion per requirement, so the tests can be automated). Eight days later they still did not exist in writing — Chudinov's "требования не прописанные" is the admission. What Sept 15 adds is ownership by name, three working days cleared for the work, and a dated assembly point where every capability must arrive with both its functional and its non-functional requirements already attached.

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/pavel.md|Pavel Frolov]] — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ (timers, handshaking, encryption, hung states, device pings, the incoming Wi-Fi, unit identification numbers) — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish and clean every MVP 1 capability and requirement during Wednesday–Friday, ready for the Monday grooming pass — due Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — run the Monday Sept 21 grooming meeting across the whole of MVP 1, capability by capability, functional and non-functional together — due Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Who the "architecture ideologist" is.** Val says the engineering ideology has to be dictated from above by an architecture ideologist; nobody was named to the role on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — process and engineering ownership only. Val's remarks name people as owners of work, not as performance judgements, and no pay, rate or HR assessment appears in either source; nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
