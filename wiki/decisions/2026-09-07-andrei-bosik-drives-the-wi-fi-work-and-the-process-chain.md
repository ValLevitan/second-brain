---
type: decision
title: Andrei Bosik becomes the driver for the Wi-Fi work and writes it up in Jira — the existing ticket is not to be amended, and the chain runs use cases (Klimovich) → capabilities → features (Pavel) → feature branch → commit carrying code plus prose plus data contracts
date: 2026-09-07
aliases: [Bosik is the driver, if it is not in Jira there is no work, do not amend the existing ticket, you are driving a tank, use cases not capabilities, capabilities broken into features, docs/contracts directory, prose and data contract, set him up on Claude Code]
source-count: 5
status: active
open-commitments: 5
open-questions: 0
---

# Bosik drives the Wi-Fi work into Jira, and the process chain is restated

Two halves of the same ruling, made across both [[wiki/people/val-levitan.md|Val]]'s Monday meetings on Sept 7 2026: the **assignment** (9:08 call, [[wiki/meetings/2026-09-07-wifi-on-flex-port-and-qr-provisioning.md]]) and the **chain of artifacts** the assignment has to produce (restated at the 10:02 call, [[wiki/meetings/2026-09-07-sas-aft-on-flex-port-and-remote-update.md]], with the roles named). Both in Russian.

It sits on top of the standards already ruled: [[wiki/decisions/2026-08-24-single-prose-writing-standard.md]], [[wiki/decisions/2026-09-03-module-contracts-and-nova-integration-repository.md]], [[wiki/decisions/2026-09-04-data-contracts-closed-every-repository-by-september-11.md]] and [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md]]. What is new here is who does it for Flex-Port/Wi-Fi.

## The assignment

- **The premise.** Val: "чтобы начать работу[,] у нас [всё] должно быть расписано в джире. [Е]сли нету, значит работы нету" — if it is not written up in Jira, there is no work [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **The reason for handing it out:** "Здесь нужно расписать довольно многое, раздать задание. На Павла ложится очень много работы" — too much currently sits on [[wiki/people/pavel.md|Pavel Frolov]]. Val's candidates were [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] and [[wiki/people/andrey-bosik.md|Andrei Bosik]] — "А можно ли это передать? …Диме Ковальчуку, Андрею Климовичу и Андрею Босику. Мне нужна помощь в этом" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Pavel named the actual question:** "кто будет… общаться с клодом по постановке cap[abilities] и f[e]atures?" — who talks to Claude to set the capabilities and features [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Bosik takes it.** Val: "я бы хотел, чтобы с Павла это ушло[,] много на нём лежит сейчас. Андрей Босик, вы на себя можете это взять?" Bosik: "Да да[,] я[,] давайте конечно" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **What "driver" means, spelled out.** "Сегодня начните, пожалуйста, это делать. Возьмите все это под свой контроль. Это значит, что вы должны общаться… с этим коллективом, который сейчас… на этом митинге… вы драйвер… вы задаете темп." And the pressure: "поскольку мне нужно это завтра, то вы вчера должны были начать это делать." Bosik: "Все понятно, вопросов нету." Val's closing image: "вы за рулём[,] понимаете да?… у вас не просто легковая машина[,] у вас танк… через стенки должны проехать" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **The existing ticket is NOT to be amended.** [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] proposed the shortcut — "может, просто сейчас текущую джейру дописать? Что можно добавить модуль и всё?" — and Val refused it flatly and repeatedly ("Нет, нет, нет, нет, нет"), giving his reason: "Давайте пусть больше будет ответственн[ости]." Alekseev accepted ("Хорошо") [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].
- **Who does the building.** Val read the split back: "Евгений Алексеев и Геннадий[ Peari] — они делают доработку портов." He then asked whether Alekseev also reworks the Flex-IQ; Alekseev said the IQ should just work ("не[,] айкью должен работать"), and Val assigned the check to Pavel instead: "ктото его должен проверить. Павел, вы возьмите на себя ответственность проверить это" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## The chain of artifacts, with roles (10:02 call)

Val reopened it — "нам всётаки опять нужны… [капа]билити[с,] ре[к]ва[йр]мент[ы,] features… То, что я на прошлом митинге поднимал" — and then corrected Klimovich's terminology, which is the substance of the ruling [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]:

- Klimovich offered: "с меня точно [капабилити]… связаны с пользовательским опытом и, в частности, пинкод[ —] его наличие[,] отсутствие."
- Val: "Это юз[-]кейсы, вы говорите про юс[-]кейсы?… Добавить юз[-]кейсы[;] в юс[-]кейсы прикрепите ка[па]билити[с] и ре[к]ва[йр]мент[ы]. На этом… заканчивается ваша функция. После этого Павел берёт эти капа[билитис], начинает их дробить на фичи."
- "После этого открывается f[ea]t[u]re br[a]nch. Когда делается ко[мм]ит[,] туда кладется код[,] и в коде кладётся проза и дейта контракты."
- Pavel accepted ("Да, хорошо") and named what it costs him: "мне надо будет сделать реверс[-]инжиниринг… на готовый код… то, что уже есть в[о] Флекс[-]Порт[е]… с тем, что Владимир делает[ —] скиллы и плагин для создания прозы… Задним числом тогда список каких-то капа[билитис], которые относятся к флекс[-]порту, ну и изменения, которые нам необходимо сейчас сделать, и новые, которые надо сделать" — see [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]].
- Pavel's technical read of the scope: "мы, наверное, можем оставаться в рамках существующих протоколов и команд со стороны flex pay [и] Flex-IQ… команды по WS, за исключением тех случаев, где… нам надо сверить или передать настройки вайфай[,] возможно. Вот эту вот часть надо будет подумать."

## The prose-and-data-contract standard, as explained to Alekseev

Val told Alekseev his commits must carry two things beside the code — "когда вы кладёте код[,] рядом с кодом… 2 вещи: это проза должна быть. И… как он называется, Паша?… дейта контракт" — and asked Pavel to state the standard so he would not mangle it. Pavel: "в репозитории должен быть каталог d[o]c[s]. А внутри каталога d[o]c[s] должен быть каталог контракт[ы], в которой кладётся MD файл[,] с помощью [Клода] сгенерированный, который описывает, что данный репозиторий, точнее артефакт, собранный из этого репозитория, предоставляет для других модулей — то есть он умеет общаться, например… с флекспеем… [по такому-то] API. И вот это описание этого API в этом документе должно быть" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

Alekseev said it already exists for his repository — "оно ж есть уже. Написали" — and Val let it stand ("если есть[,] хорошо"). Val added the linkage: "и проза должна общаться с [acceptance criteria]." Alekseev's blocker was access, not willingness: "мне надо туда подключиться[ —] для начала, чтоб ктото меня подключил, ввёл [в] курс дела, как это работает"; Val put Bosik on it and Bosik undertook to call him that day: "Созвонимся с вами, Евгений… сегодня[,] и настрою." Val's endorsement of Bosik as the person to explain it: "Андрей глубоко в этом разбирается, он был частью всей этой гимнастики" [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]].

## Update — Sept 9 2026: it worked, and Val widened it

Two days later [[wiki/people/val-levitan.md|Val]] opened Bosik's email during the [[wiki/meetings/2026-09-09-september-resource-plan-and-flex-port-readiness.md|Sept-9 7:02 AM call]] — "он создал огромное количество [рекваймент]" — and [[wiki/people/pavel.md|Pavel Frolov]] confirmed the shape was right: capabilities first, then requirements under them, across both Flex-IQ and FlexPay [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]. The Wi-Fi capabilities named on that call were **145, 143, 142 and 140**, with 145 explicitly outside the first release [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]].

Val then generalised the arrangement beyond Wi-Fi: Pavel is to stop planning by hand, talk the work through in **daily recorded sessions** with Bosik and [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]], and let them turn the transcripts into capabilities and requirements — "хотя бы на 75[–]80%." Full ruling on [[wiki/decisions/2026-09-09-planning-handed-to-bosik-and-kovalchuk-with-daily-recorded-sessions.md]].

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — write the Wi-Fi capabilities, break them into features in Jira, own the pace and coordinate the group from this meeting — **partly discharged Sept 9 2026**: the capabilities and requirements exist and were emailed round (Wi-Fi capabilities 140/142/143/145), but Pavel expected them to cover "5% в лучшем случае" of kiosk behaviour and put a review in front of the next step; the coordination half continues — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]] [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrei Bosik]] — call Evgeniy Alekseev and set him up on Claude Code so he can generate prose alongside his code — due Sept 7 2026 — [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — write the use cases for the user-experience changes (the PIN above all) and attach capabilities and requirements to them; his function ends there — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]] [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — take the capabilities and break them into features; open the feature branch — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — reverse-engineer prose and a retrospective capability list onto the Flex-Port code that already exists, using Vladimir Samusenko's prose skills and plugin, plus the changes needed now and the new ones — due unspecified — [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]

**§15.8:** clear — process and role assignment only; no named-person compensation.

## Sources
- [[raw/Meeting_Notes_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026.md]]
- [[raw/Meeting_Notes_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_SAS_AFT_on_FlexPort_and_Remote_Update-September-7-2026.md]]
- [[raw/Meeting_Transcript_September_Resource_Plan_and_FlexPort_Readiness-September-9-2026.md]]
