---
type: decision
title: Val repoints the rest of the week at the non-functional requirements, names the five people who own them, and sets Monday September 21 as the deadline for a grooming pass over the whole of MVP 1
date: 2026-09-15
aliases: [if it is not written it does not exist, non-functional requirements owners, nonfunctional requirements week, September 21 deadline, MVP1 grooming meeting, engineering ideology, architecture ideologist, это не написано этого нету, нон фанкшинал, Sonos analogy, half the requirements have open questions, Claude refuses past an open question, focus rule, Monday scope freeze, nothing more may fly into MVP1, больше ничего никуда долетать нельзя, acceptance criteria second pass, requirements inherit the capability fix version, no feature lock today, feature lock maybe tomorrow, no lock on Sept 22 either]
source-count: 8
status: active
open-commitments: 6
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

## Update, Sept 16 2026 — the non-functional work is blocked by the functional requirements' own open questions

The next morning's call ([[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16, 8:01 AM]]) opened with [[wiki/people/irina-shishko.md|Irina]] reporting why she had not got far. She had started on the non-functional requirements and run into the state of the functional ones [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **[Я] стара[ла]сь поработать с требованиями… нон фан[кшнл,] и столкнулась с тем, что у нас половина требований имеют открытые вопросы, и как только Клода просишь с этим поработать, мы тут же получаем[:] "у тебя там открытый вопрос". На них нужны ответы, иначе уводят неизвестно куда… нам нужно вот эти все требования почистить, то есть либо дать ответ, либо если это не актуально[ —] убрать этот вопрос.**
>
> *(I was trying to work on the requirements — the non-functional ones — and ran into the fact that half our requirements carry open questions, and the moment you ask Claude to work with one, straight back comes "you have an open question there". They need answers, otherwise it leads nowhere… we have to clean all these requirements: either give an answer, or, if it is no longer relevant, remove the question.)*

That is the concrete mechanism by which unanswered questions block the Sept-21 gate: the team's AI-assisted requirement workflow refuses to proceed past one. **Val's plan for the Sept-16 meeting therefore did not hold as stated** — it was to be devoted to the non-functional requirements and instead went, end to end, to clearing open questions out of the functional ones. The gate itself is unchanged and nobody re-opened the date.

[[wiki/people/andrei-klimovich.md|Klimovich]] entered one qualification: not every open question is his to answer. Some he flagged deliberately as engineering questions — "это решение не на уровне продукта или бизнеса… это скорее ответ на вопрос, как это должно быть сделано[;] это в поле инженеров" — while conceding the rest really are business logic needing a decision [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Val closed the Sept-16 call by restating the focus rule unchanged:** "[и]нженер[ы] продолжа[ют] работать на одном [функциональном рек]в[а]йрмент[е] и продолжа[ют] делать[;] кроме [этого] никто ничего не программирует. Фокусируемся на этом" — nothing outside the one functional requirement set gets programmed [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].


## Update, Sept 17 2026 — partial progress, and Val adds remote device operation to the Monday list

The [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|Sept-17 8:02 AM call]] opened with a round of status on this commitment. **None of the three commitments below is discharged; all three moved.**

- **[[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/pavel.md|Pavel Frolov]] — partly done, and reworked rather than merely written.** Pavel had handed over "**нонфан[кшн] требования, которые вчера с Кло[дом] делали**"; Irina had been through part of them — "**частично мы тут посмотрели кое[-]что… я позволила себе с Кло[дом] дописать, переработать там кое[-]что[,] разделили**" — and Pavel judged there was still "**много чего ещё лишнего**". The agreed next step is that she finishes and sends the list to [[wiki/people/andrei-klimovich.md|Klimovich]] to look over. **These are the Flex-Port non-functional requirements specifically**; Pavel said the Flex IQ ones Chudinov created had already been reviewed the previous day [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — partly done.** "**я по 122 там закрыл все открытые [вопросы] и добавил там новых**" — all open questions on capability 122 closed and some new requirements added — plus "**парочку нефункциональных… на работу сети**", a couple of non-functional network requirements. What is **not** done and was stated as not done: "**остаётся ряд по логам, по графан[е;] запланировано, оно ещё не сделал**" — the logging and Grafana requirements are planned and unwritten [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **[[wiki/people/andrey-bosik.md|Andrey Bosik]] — his contribution arrived as a document in the chat rather than as Jira requirements**, and he asked for it to be discussed rather than filed: "**я вон на лицо не хочу это добавлять в MVP один. Я хочу, чтобы… что[-]то обсудили**". That discussion is this meeting, and it produced [[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]]. He left it owing at least one written requirement — the signal-quality one Klimovich assigned him ([[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].
- **Klimovich's own Wednesday-to-Friday cleanup is what this call largely was** — capability by capability, with him taking requirement 1410 and the multi-product write-up onto his own list [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

**And the Monday gate acquired a fourth item.** Klimovich, recalling Val: "**я помню, что вал говорил о том, что… условно к понедельнику нам надо ещё продумать всю вот эту вещь, связанную с оперированием устройств по удалёнке**" — by Monday the team also has to have thought through operating the devices remotely. He used that to set the MVP 1 boundary for signal telemetry [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]. *(Val is not on this recording; this is Klimovich reporting Val's instruction, and is recorded as such.)*

## Update, Sept 18 2026 — the gate holds, the freeze is restated, and two of the five named owners are not heard from

The [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept-18 8:03 AM call]] is the **last session before the gate**. Klimovich restated the deadline in the team's own words, unchanged from Val's [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**У нас был дедлайн, пред[ъявленный] перед нами, что в понедельник у нас всё[:] [капабилити]с[,] все фичи[,] все нон[-]факс[.] Всё уже создано, всё продумано[,] в нужных статусах[,] нету [анассайнд]. Вот к этому нам надо прийти.**"

**And the freeze after it was stated for the first time in this form** — as a rule binding the product owner too: "**в понедельник… точка[,] [MVP] один[ —] вот то, что мы в понедельник. И начинаем работать[,] и больше ничего никуда долетать нельзя. Это в том числе сам себе говорю**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

### Status of each obligation, as of this call

- **Klimovich's own cleanup — in hand but hedged.** "**Я вижу всё, что сейчас на меня завязано[,] я дожимаю всё это[;] то есть с моей стороны постараюсь к понедельнику всё закрыть**" — *постараюсь*, he will try. He said the same of the team: "**к понедельнику надо постараться всё сделать**". The working half of the same meeting was that cleanup being done live ([[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]]) [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **Non-functional requirements — mostly created, details outstanding.** Irina Shishko's report: "**ещё не все[;] то есть мы с Пашей над флекс[ ]портом работали, Дима над флекс[ ]IQ… Вот Андрей тоже со своей стороны, но в принципе получается, наверное, то, что должно быть покрыто**". Chudinov's: "**Значительная часть точно покрыта, возможны какие[-]то[,] просто детали остались**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **⚠ Two of Val's five named owners are not heard from on this call.** Irina's account covers **herself and Pavel Frolov** (Flex-Port), **Chudinov** (Flex IQ) and **Klimovich** (his own side, though he was deliberately excluded from Val's five). **[[wiki/people/andrey-bosik.md|Andrey Bosik]] and [[wiki/people/alexander-biratka.md|Alexander Biratka]] are named nowhere in the non-functional-requirement status.** Bosik was in the room and was given other work; Biratka was in the room and spoke five times, none of it about this. **Their share is neither reported nor discharged** [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **A second pass is still to come, and it is not finished before Monday.** Irina and Pavel agreed to sit together and walk the non-functional list, Flex-Port side first, with Chudinov's Flex IQ set after it. Irina separately wants to re-check the **acceptance criteria** on every MVP 1 requirement — "**я видела, что во всех требованиях они есть, но ещё раз… пройдёмся и посмотрим, что они полностью описаны, что нигде ничего не потеряно для всех наших [MVP] один**" — present everywhere, completeness unverified. Neither task carries a date [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **A mechanical point Irina made that governs the whole gate:** requirements inherit their capability's release — "**если [капабилити] в [MVP] один, значит все требования, которые под [капабилити], будут в [MVP;] не выставляем фикс[ ]версию**". The team does not set a fix version on a requirement at all [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

### What Chudinov named as the two things that would block him most

Asked by Klimovich to prioritise, he gave exactly two: "**Дизайн окон новый[,] переработанный**", and "**побились требования на 2 продукт[а,] на 2 карточки**" — the reworked window designs, and the requirements split across two products and two cards, "**потому что они визуально… сильно меняют логику значительно**". Both are Klimovich's to clear. **The window designs are the single biggest named blocker going into the gate, and they are not done** [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

### The planning itself is blocked behind one person

Irina closed the meeting on it: "**по [MVP] один мы… больше ничего не распланируем, пока Дима не сделает фичи. Дима делает фичи[,] даёт нам знать, и мы планируем дальше**" — Chudinov's capabilities are bare of features, and nothing more can be scheduled until he creates them [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

### Cadence and the weekend

Klimovich confirmed the daily call continues **Monday to Friday** at the same time — "**с понедельника… по пятницу каждый день продолжаем практику[,] в то же самое время**" — and made himself available through the weekend: "**можем завтра встретиться[,] можем в воскресенье[,] как вам угодно… если возникают любые вопросы, не ждите понедельника[,] пишите**", with the intent stated openly: "**это я так мягко намекаю… что в принципе в выходные дни тоже можно работать**". Irina answered for two: "**мы[,] я[,] Паша будем в воскресенье**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

### Read on the gate

**MVP 1 goes into Monday with its scope cleaned but not closed.** Every capability now has an owner and a status, and several have been cut or moved; but features do not yet exist under Chudinov's capabilities, nothing may be marked complete until the conflict findings are absorbed ([[wiki/decisions/2026-09-18-nothing-is-closed-until-the-conflict-findings-are-worked-back-in.md]]), two of the five non-functional-requirement owners are silent, the acceptance-criteria pass has not run, and the designs that unblock the largest capability are outstanding. **Nobody re-opened the date, and nobody claimed the work would be finished by it** — the strongest statement made was *постараюсь*.

## Update, Sept 21 2026 — the gate day: the designs arrive, and the feature lock slips to "maybe tomorrow"

The one recorded call on the gate day is the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM session]] (about 52 minutes, Russian). **It is not the grooming meeting Val promised to run.** Val has no speaker turn on it, and it was a walk of Klimovich's Flex-Port and Flex IQ screens, not a capability-by-capability pass over functional and non-functional requirements together [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. Whether Val's grooming meeting happened at another time is not in the sources.

**No feature lock.** Klimovich, at the end: "У нас какойто. Торжественного фича лока и не будет сейчас ещё да, потому что от меня ещё доедут [капабилити и] рекламус… может завтра тогда его сделаем". He checked that nobody is waiting on him — "у вас же сейчас всё равно есть всё, чтобы вы не сидите, не ждёте меня правильно" — and Pavel said yes [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. **So the Sept-18 freeze ("в понедельник… точка") did not land on Monday.** Nobody objected.

**Klimovich's own side, as of the call.** Cloud clean-up: "буквально минут через 10, после завершения нашего звонка я закончу чистку клауды". UI/UX into Jira after the call; asked by Irina "Что сегодня ты это сделаешь?", he said yes, "я чувствую что это блогер сейчас" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. Features under the new screens cannot be made until that is loaded.

**Non-functional requirements.** Irina will hand Klimovich the Flex-Port list she and Pavel produced, for him to review with his Claude and comment. Chudinov said his main Flex IQ ones exist: "свои основные осоздал. Остальные может, будут только добавлять" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. Nothing was said about Bosik's or Biratka's share.

## Update, Sept 22 2026 — the day after the gate: Val is back, and the lock is still not declared

The [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM call]] is the first of the series where Val speaks since Sept 16 (he was in the chat only on Sept 18). It was not called a grooming meeting, but it did walk the MVP 1 capabilities still out of place, live in Jira ([[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]], Sept-22 update) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

- **Klimovich's side is still loading.** He needs "3–4" more hours to finish the IQ and port design and put it into Jira, then about 2 hours on capability 178; he expects to close both that day "если всё пойдёт хорошо" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. No feature lock was declared on this call.
- **Irina's Flex-Port non-functional list reached him.** Klimovich: "Ирина вы скинула… вчера этот список [нон-]фанкшнл", but he has not got to it: "максимум, что могу завтра попробовать сделать — это превью" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].
- **Acceptance criteria: about two-thirds checked.** Irina: "60 70%… мы там с [Клодом] их пересматривали, они все удовлетворяют", but some requirements still lack them, and Klimovich adds more that day. This is progress on her second pass below, not its end [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].
- **Val's Sept-15 fear came true on tests.** He had said the product cannot ship without autotests. On Sept 22 none of the end-to-end tests existed; see [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]].

## Open commitments

- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/pavel.md|Pavel Frolov]] — sit together and walk the non-functional requirement list, Flex-Port side first — due unspecified, and before the Monday gate in intent — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — make a second pass over the acceptance criteria on every MVP 1 requirement, to confirm none is half-written — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], [[wiki/people/andrey-bosik.md|Andrey Bosik]], [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/alexander-biratka.md|Alexander Biratka]] and [[wiki/people/pavel.md|Pavel Frolov]] — write the non-functional requirements for FlexPay, Flex-Port and Flex IQ (timers, handshaking, encryption, hung states, device pings, the incoming Wi-Fi, unit identification numbers) — due Monday Sept 21 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish and clean every MVP 1 capability and requirement during Wednesday–Friday, ready for the Monday grooming pass — due Sept 21 2026; **not finished on Sept 21** — capabilities and requirements still to be loaded, feature lock moved to "maybe tomorrow" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — run the Monday Sept 21 grooming meeting across the whole of MVP 1, capability by capability, functional and non-functional together — due Sept 21 2026; the one recorded Sept-21 call is not it (no Val speaker turn) — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

- [x] [[wiki/people/irina-shishko.md|Irina Shishko]] — give Klimovich the Flex-Port non-functional requirement list she and Pavel produced — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]] — **discharged Sept 21 2026:** Klimovich on Sept 22, "Ирина вы скинула… вчера этот список" — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — review that list (with his Claude) and comment — due after Irina hands it over — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]] — **Sept 22:** not started; "at most a preview" on Sept 23 — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]

## Open questions

- **Who the "architecture ideologist" is.** Val says the engineering ideology has to be dictated from above by an architecture ideologist; nobody was named to the role on the call — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — process and engineering ownership only. Val's remarks name people as owners of work, not as performance judgements, and no pay, rate or HR assessment appears in either source; nothing was excluded on that ground.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
