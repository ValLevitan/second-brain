---
type: decision
title: The MVP 1 capability list is walked item by item before the Monday freeze — the FlexPay capabilities leave for MVP 2, requirements come off developers, and every remaining capability gets an owner and a status
date: 2026-09-18
aliases: [capability cleanup, MVP1 capability sweep, capability 178, capability 144 clone, capability 151, capability 163, capability 174, capability 175, capability 176, capability 180, capability 148, capability 149, capability 150, capability 116, capability 117, capability 79, capability 80, capability 156, requirements are not hung on developers, требования вешать на разработчика это странно, clone the capability instead of moving requirements one by one, location block enforcement, audit ticket, daily audit printout, capabilities without features, empty capability, test executions instead of features, capability 115 to MVP 2, capability 157 emptied, requirement 1473 on 156, FIQ-34, capability 152 dates, change list for Claude, capability 234, capability 235, capability 230, capability 231, FIQ fort FP DTP repositories]
source-count: 9
status: active
open-commitments: 15
open-questions: 5
---

# The MVP 1 capability list is cleaned item by item, and everything gets an owner

The working half of the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept 18 2026 8:03 AM call]] (Russian) — the fifth and last morning session before the Monday Sept 21 gate ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]). [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] filtered the board for everything sitting **below "In Progress"** or **unassigned** — "**мы смотрим, что у нас есть ниже прогресс[а]… [или] туду[,] что требует обсуждения**" — and the team went down the list [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Why walk it twice.** [[wiki/people/andrey-bosik.md|Bosik]] objected that they had already done this — "**Мы вроде это уже делали[;] не зачем мы 2 раз[а] их открывать**" — and Klimovich gave two reasons: "**вопервых[,] Вал предлагает это делать. Вовторых, у нас изменилась[сь с] последней проходки[:] там… [капа]билити добавились**". So the re-walk was **Val's instruction** plus new capabilities added since. *(Neither the objection nor Val's role in ordering the re-walk is in the derived notes.)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## The sweep, capability by capability

| Capability | What it is, as described on the call | Result |
|---|---|---|
| **178** — InComm card configuration | "**ИНКОМ карт конфигур[ейшн капа]билити… то, что мы вчера обсудили[:] поддерживать несколько продуктов**" | **Not moved on.** Klimovich: "**он не доработан, он не может переехать дальше, он требует ещё работы**". He is finishing its windows. Scope contested — see below |
| **144** — Bosik's FlexPort master | a separate project in Pavel's reading, not deliverable inside MVP 1 in full | **Cloned** — trimmed copy stays MVP 1, clone holds the rest on MVP 2. See below |
| **117**, **79**, **80** | "**это… опять же flex pay. Здесь полностью flexpay**" | **MVP 2**, with [[wiki/people/alexander-biratka.md|Alexander Biratka]] ("Саша занимается flexpay['ем]"). Irina's read on why they were still there: "**её просто пропустили в прошлый раз, когда передвигали**" |
| **116** | "**вообще… флекспей сплошной**" — solidly FlexPay | **MVP 2**; responsible changed from [[wiki/people/dmitri-chudinov.md|Chudinov]] to Biratka, "**потому что все фичи саши[ны]**" |
| **156** | FlexPay; the same function on the other product | Chudinov builds the implementation; **Biratka then ports it across** — Pavel: "**как только дима сделает имплементацию, саша просто возьмёт и перенесёт её… это простое[,] по идее[,] копирование**". Biratka's dates follow Chudinov's |
| **151** — Flex IQ in the port environment | "**общая [капабилити]… что флекса IQ должен работать в порт[ ]энвайменте[,] чего у нас не было до начала работы… по MVP один**" | **Text cut** — the cloud wording ("**еволет транзакш[н]с на клауд**") and the MG/MudaGoose scope item removed; assigned to **Chudinov**. Opened the dual-SAS question ([[wiki/decisions/2026-09-18-mvp1-supports-dual-sas-only-and-locations-are-chosen-to-match.md]]) |
| **163** — access to the e-wallet | "**Служит доступом к нашему [е]волюту**"; has a design and its own logic; features exist | **Chudinov.** Pavel's shape: "**будут 2 фичи[:] одна на порте, одна на флекс айкью, а сессия… одна**" |
| **the location-block capability** *(no number spoken)* | "**всё, что связано с нашей возможностью заблокировать операцию по локации**" | **Chudinov**, and features still to be created under it |
| **174** — reprint | Klimovich: "**припринт[ —] всё, я его перевёл, переработал**" | **Chudinov** |
| **175** — wallet records | e-wallet record creation, balance updates, ACH and cloud — "**как нам хранить все записи по [е]волет[у,] что создание[,] их[,] обновление баланса**" | **Held.** Irina called it MVP 2 and a possible duplicate; Klimovich refused to move it until he checks. **Chudinov** meanwhile |
| **176** — how money is withdrawn | "**Как будет выводиться деньги**"; "**здесь это всё расписано**" | **Chudinov**; Chudinov asked for the FlexPay references in the body text to be struck — "**уберите в текстах фликспей[;] там в середине**" |
| **148**, **149** | Chudinov's existing work; 148 already in To Do correctly | **Chudinov** |
| **150** — balance display | "**это [гейм] агностик[:] на любом гей[ме] нужно показывать баланс**"; the form is spelled out in the requirements | **Chudinov.** Gap described below |
| **180** — FlexPort session life | "**логика флекс[ ]порта[,] сешен лайф[:] есть режим ожидания… есть инактив[и]ти таймаут**"; previously "**гдето кусками сделано, но сейчас оно всё собрано в одну [капабилити]**" | **Reassigned from Biratka to [[wiki/people/pavel.md|Pavel Frolov]]** on principle — see below |
| **the audit ticket** | the daily audit printout at a location — Pavel: "**то, что на лакейш[е]не нам надо какое[-]то дневное аудит распечатать**" | **Klimovich's own, unfinished**, and stays in MVP 1 |

Klimovich's own summary at the end of the pass: "**[капаби]лити, которые в любом статусе, пригодном для работы, а не [асса]йн[ed] — у нас больше не осталось**" — nothing is left that is unassigned or in an unworkable status [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Capability 144 is cloned, not emptied — and that settles its fix version

[[wiki/people/irina-shishko.md|Irina Shishko]]'s method is the ruling, and it replaces moving requirements out one at a time [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**либо склонировать его[,] и в т[ом], которы[й] [MVP] один[,] оставить часть — там сколько[,] 2[,] 3[,] 4 требования. Остальные требования уезжают в тот клон, который будет на [MVP] 2, потому что если так перебрасывать[,] это… дольше[,] будет потерять.**"

Klimovich agreed and acted on it live: "**Клон я закину на MVP 2[,] и мы вернёмся к этому[ ]44. Мы выкинем из него всё лишнее**". Irina had already stated the split in the same terms a minute earlier: "**мы только эти требования выделим и сделаем[,] в [MVP] один будет сделано. Всё остальное переезжает в 2**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**This answers the question the Sept-17 recording left open** — whether capability 144 itself carries an MVP 1 or an MVP 2 fix version ([[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]]). The answer is **both, on two objects**: the trimmed original **stays in MVP 1**, the clone **goes to MVP 2**. 144 duly reappears in the MVP 1 feature-planning walk later in the same call — "**144 — это то, что Андрей будет переписывать[,] и фичи точно так же сделает**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**What Bosik kept and what he gave up.** He read the surviving requirements out loud and at first concluded none could go — "**Пока выглядит, как будто там всё осталось нужным**", "**тут по ходу всё, что нужно[,] осталось**", "**здесь всё нужно и осталось после вчерашнего**". Klimovich needled him for it once Pavel found one to cut — "**это оставит под сомнение твоё предыдущее заявление, Андрей**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

- **Kept: requirement 1410.** "**смотрю на 14 10[ —] оставляем[;] это то, что мы вчера говорили, что мы должны видеть всё**" — the Flex-Ports must be visible. *(That places 1410 in the MVP 1 copy of capability 144, which is what the Sept-17 derived notes asserted and the Sept-17 transcript did not settle. This source supports it.)*
- **Kept, and not a developer's job:** a requirement to buy routers on the local market — Pavel: "**то, что там надо покупать роутеры локального рынка… это простое требование, оно не к разработчикам**". *(Absent from the derived notes.)*
- **Cut: the master-board requirement.** Pavel read it out — "**Изменения мастер[ ]бортов… не должно терять деньги… и должно быть задокументировано**" — and killed it on scope: "**Если это речь идёт о выпущенных тикетах[,] и какой[-]то тикет не обналичен, и у нас сейчас нету клауд[-]версий тикетов[,] то они… не переносятся на новое устройство… это не MVP один, значит**". Bosik: "**Тогда убираю**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

Bosik owns the rest: rewrite the description to match what survives, clean it, move it to the next status — Klimovich: "**Андрей, сделай это сегодня[,] пожалуйста, до конца дня**"; Bosik: "**Я прямо сейчас сделаю[,] после митинга**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## The principle that came out of capability 180 — requirements do not hang on developers

180 was assigned to [[wiki/people/alexander-biratka.md|Biratka]], and both Pavel and Irina called that wrong. Pavel: "**на Александре[ —] вот это вот на Александре неправильно висит**". Irina, generalising it: "**вопервых[,] требования вешать [на] разработчика — это вообще странно**". Klimovich did not know who had done it — "**Я не знаю[,] кто вешал**" — and Irina declined to investigate: "**давайте мы не будем искать, почему**". Pavel took it: "**Перевесь на меня лучше тогда**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

*(A related Jira constraint surfaced on 144: only the author can change a reporter. Klimovich: "**Репортёра нельзя менять[:] тот, кто создал, тот репортёр**", and again "**только автор может [репортёров] менять**". Bosik, as 144's author, made the change.)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Two capabilities that are not as finished as they look

- **150, the balance display.** Irina's reading was that it does not exist — "**у нас этого ещё нет, его нужно сделать**"; Klimovich's was that something exists but is not what the requirements describe: "**В каком[-]то виде оно есть, но оно явно не очень**". His standard is the release, not the demo: "**Мы же говорим ещё о релизной версии[,] о том, чтобы показывать людям чтото на экране[ —] в хьюман[-]рид[абл] пригодном виде[,] и там описаны детали, как это должно выглядеть**". Pavel expects the gap to be cosmetic — "**оно будет выглядеть так, как будто бы это уже сделано, и разница будет расходиться только в дизайне[:] что ты задумал одним дизайном, а сделано другим**" — and Irina drew the line before anyone could act on it: "**мы не будем переделывать дизайн**" *(this last is absent from the derived notes)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].
- **Capabilities with no features under them are many, and were not counted.** Klimovich offered to filter for them; Chudinov said don't bother — "**я думаю[,] не надо, потому что уже видели, что их много**" — and Irina put the obligation on the owners instead: "**нужно просто[,] чтоб те, у кого [капа]билити, посмотрели свои [капа]билити и создали фичи**". **Pavel's amendment is the useful part:** where a capability describes functionality that already works, what gets added is not a feature but **test executions** — "**то, что уже работает[,] — нам там надо добавить будет тест[-]экзекушен[ы] какие[-]то… и эти самые автоматизированные тесты[.] Тогда [у] нас не будет пуст[ых капа]билити**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Capability 178 — the one item the meeting did not reconcile (SETTLED afterwards by owner ruling, 2026-09-20)

Klimovich stated his position as near-final: "**я склоняюсь к тому, что 2 продукта мы к [MVP] один не будем делать[;] я могу вам почти уже финально это заявить**". Chudinov had just named the split-across-two-products-and-two-cards requirements as one of his two biggest blockers, "**потому что они визуально… сильно меняют логику значительно**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

Irina then read Val's chat message aloud — "**178 — [маст би MVP] один**", confirmed by Pavel as "**текст от Вала**" — i.e. **Val's written instruction is that 178 must be in MVP 1** [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

Klimovich's answer was a fallback, not a reversal: "**мы можем сделать поддержку одного продукта… у нас сейчас уже всё работает. Мы можем сделать поддержку [скилпей]**" — one product, SkillPay, because it already works. Pavel costed it as small: "**со стороны сервера это можем очень легко сделать[,] в интерфейс добавить для оператора**", needing "**данные по карточкам**" and a graphical check, "**и с точки зрения бэкэнда это будет сделано**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**Nothing was reconciled on the call** — Irina cut the discussion off to keep the meeting moving ("**давайте мы не будем сейчас это много говорить**") and the action taken was only that Klimovich finishes 178's windows. Recorded as an open contradiction on [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]].


**Settled after the fact.** Asked directly on **2026-09-20**, the owner ruled: **"Klimovich is correct."** Capability 178 / two-product support is **not in MVP 1**, and the owner's own chat instruction is withdrawn. The multi-product payment-hub design is unaffected; only its MVP 1 delivery is cut to a single product. *(An owner ruling is its own citation — §16.)* See [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]].
## Update, Sept 22 2026 — a developer owns a capability outright

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 Minsk stand-up]], [[wiki/people/alexander-biratka.md|Biratka]] asked whether capability 137 "должна на мне висеть или… только фичи". Pavel: "ответственного назначили по capility на тебя, значит, ты будешь за неё отвечать." Biratka took it: "значит я ее на себя саю". He is building its features by porting the mechanism already built for Flex IQ under capability 122 [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

## Update, Sept 22 2026 (8:01 AM) — one more pass, live on Pavel's screen

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM call]], with Val in the chair, Pavel shared Jira and the team walked what was still out of place [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

| Capability | What was said | Result |
|---|---|---|
| **178** | Pavel: "единственное… в [пропоузд] состоянии ещё из MVP один" | Klimovich will take it to Accepted that day, with requirements and mock-up links. **Owner ruling 2026-09-20 stands: not in MVP 1** — see [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] (Sept-22 update) |
| **152** | In Progress, "но не стоит в какой день" | Chudinov will set the feature dates himself; he started one "10 минут назад" |
| **115** — FlexPay registration | Irina: "мы… flex pay в MVP [один] не проверяем и не выпускаем". Chudinov: it was created and built earlier; the registration mechanism is shared, so a new terminal means changing "не 6 репозиториев, а всего 2" | **MVP 2.** Val: "Я согласен с Ириной, давайте просто передвинем это на MVP 2" |
| **157** | Chudinov: abstract, overlaps other capabilities, partly built — "Я бы ее убирал". Klimovich: it holds the rule for a new wallet at the Flex-Port collect — on IQ a ticket prints, on self-service kiosks no auto-print, a claim code instead | **Emptied and moved to MVP 2.** Val: "всегда можно [реквайрмент] передвинуть на другой [капа]билити… этот спор… никому не нужен". Irina: requirement 1473 already sits on 156 (Flex-Port). Klimovich will decide later whether 157 is needed at all |
| **148** | Named by Chudinov as the capability for issuing the wallet on Flex IQ | Where 157's wallet-issue requirements belong |
| **180** — Flex-Port session life cycle | Pavel: maybe it just needs writing up properly; Klimovich: "вот сюда тогда дизайн и ляжет" | **Takes the Flex-Port design** instead of a new capability (Pavel: "чтоб новая не создавать, потому что это дублирует"). Klimovich moves it to To Do once filled |
| **FIQ-34** | Pavel: in the backlog, needs a date | Chudinov: "Сейчас поставил" |

**Chudinov and Biratka say MVP 1 is clear.** Val asked them directly. Chudinov had reviewed MVP 1 for Flex IQ and the Flex-Port: "критичных расхождений нету"; some requirement may still be added or dropped as he goes capability by capability. Biratka: the FlexPay capabilities are MVP 2 and he has screen questions for later; where Flex IQ and FlexPay coincide, "у меня вопросов нету" [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**Klimovich's change list.** New requirements will keep landing in existing capabilities as the design goes in. He will send a plain list of which capabilities changed so the developers can ask Claude to re-read them; Pavel: "Это будет очень полезно", because today such features surface only at implementation. Bosik suggested keeping capabilities like an ADR — a date and what changed. How to flag a changed capability is left for later; Irina ruled out In Progress ("Только не инпрогресс") [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. More on [[wiki/topics/ai-assisted-development.md]] (Sept 22).


## Update, Sept 23 2026 — 137's features, 152 hits a certificate clash on STG, 118 is split, and new items nobody discussed

At the [[wiki/meetings/2026-09-23-daily-standup-terminal-emulator-and-capability-split.md|Sept-23 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]:

- **137.** [[wiki/people/alexander-biratka.md|Biratka]] created three features under it. **FP-1249** (update work) is almost done — "уже поставил на киоск изменения и проверяю". A second, independent item is a logging bug ("не логировал нормально"). **FP-1250** and **FP-1251** are also update work.
- **152 (card activation) hits the STG setup.** [[wiki/people/dmitri-chudinov.md|Chudinov]] started installing it on STG. The STG and DEV cluster sit "в одном регионе… в одной группе", so a terminal registered on DEV clashes with STG and its certificate must be unbound. Two options: extra functionality for constant unbinding, or a thing-name with the environment in it — "флексайкю дефис там энваймент дефис номер платы" instead of Flex IQ plus board number. "Мне не нравится оба варианта." Pavel: "Или перенести?" Chudinov said Andrei had argued the shared setup saves "кучу денег" (that Andrei = [[wiki/people/andrey-bosik.md|Bosik]] is an **inference**). Production probably does not have the problem ("Добро вроде как такой проблемы не будет" — "прод" is an inference).
- **118 is split by product** — see [[wiki/decisions/2026-09-23-capability-118-is-split-by-product-and-two-devices-keep-two-repositories.md]].
- **New items nobody had discussed.** Pavel: "Какие то новые копбилитис появились? Не обсужденные." Chudinov: "там Андрей чтото создал… ремы 14, 60… про эти программы карт" — read as **REQ-1460** on card programs. Pavel: a multi-card item was accepted "но не привязал ни на кого"; Chudinov: "Вешай пока она меня" — read as "put it on me for now" (**inference**). Pavel parked them for a meeting later that day. That this Andrei is [[wiki/people/andrei-klimovich.md|Klimovich]] is by context — he writes the capabilities.
- **180.** At the start Pavel looked for the capability Andrei should have created for the graphical user interface; Irina: "180", which he was to correct. This matches the Sept-22 plan that 180 takes the Flex-Port design (above).

The notes carry the same items [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]].

## Update, Sept 23 2026 (8:00 AM) — the UI/UX capabilities 234 and 235, 180's screen feature moves, and 230/231/234 need features by tomorrow

At the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM MVP 1 call]] (Russian) [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]:

- **Two new capabilities hold the UI/UX package.** [[wiki/people/andrei-klimovich.md|Klimovich]]: "у нас появилось 2 капбити 22, 34 и 2, 35 одна для IQ, одна для порта" — **234** (Flex IQ) and **235** (Flex-Port). Each holds the mock-ups, the text library and the requirements for the screens, written "довольнотаки технические, то есть это как раз то, что нужно для Клода". He owns keeping them current and telling the team when they change. Claude's Jira access cannot download attachments, so each capability carries a note telling Claude to ask a person to download and feed it the file.
- **Owners.** Chudinov: "добавь флекса и кё на меня вот этот вот Аффлек спорт на на Владимира" — the Flex IQ capability to him, the Flex-Port one to Vladimir ([[wiki/people/vladimir-samusenko.md|Samusenko]], **inference**).
- **180's screen feature moves to 235.** Pavel: "капбилити 235. Вот переделка экранов"; a feature for it already sat under 180. Klimovich: "мы её перенесём эту фичу просто в этот кополицу новый", because "180 там и без Того хватает другой логики".
- **Still to plan: 178, 230, 231, 234, 235.** Pavel: Chudinov should create features "до завтра… По крайней мере 231, 234 и 230". They look mostly built — perhaps filters on the card reports and the issued-card search are missing. Pavel: the Flex IQ side will be ready, "но серверная часть это, наверное, уже будет после… м в п один". **231** also takes the lost-money bugs — see [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]].
- **173 goes back to In Progress** — same decision page.
- **Repository names**, asked by Val: Flex IQ = **FIQ**, Flex-Port = **fort**, FlexPay = **FP**; for the server Pavel first said BIP, and Chudinov corrected it to **DTP** — Pavel: BIP "значит были то, что ещё старые задачи открыты".
- **Chudinov's working preference:** close one business topic at a time across devices — e.g. card activation — rather than return to it a week later.

## Update, Sept 24 2026 — features raised on the new capabilities, capability 237 appears, and the new Flex-Port screens are not MVP 1

At the [[wiki/meetings/2026-09-24-daily-standup-firmware-delivery-and-capability-statuses.md|Sept-24 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]:

- **Chudinov raised the features.** "По этим копобилити, которые новые были созданы Андреем на все завёл фиччи с этими с датами со статусом". The numbers then read out are garbled — "88? 230? 231? 203? 4?". That 230, 231 and 234 are among them is an **inference**; see the commitment below.
- **Capability 237 is new.** Pavel read out "237… Терминал сервис рэдин из гейт" and did not know it. Chudinov checked its history: created "13:00 назад", probably by Andrei ([[wiki/people/andrei-klimovich.md|Klimovich]], by context). It is assigned to no one. Pavel: "это надо всем вычитать тогда".
- **Capability 137.** [[wiki/people/alexander-biratka.md|Biratka]] is closing feature 13-49; 12-50 and 12-51 are blocked until new endpoints are added on the Amazon services side, so the app can update.
- **Capability 152.** Chudinov continues it (card activations).
- **The new Flex-Port screens are not MVP 1.** Screens in Klimovich's design that were never built become separate tasks. Pavel: "это будет задача не MVP один, то есть мы мы её делаем. Но не гарантируем, что это будет к 1 октября сделано и протестировано" — said so that no one expects it. Detail on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 24).

## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — rewrite capability 144's description to match the trimmed requirement set, clean it and move it to the next status — due **today, Sept 18 2026, end of day**; he said he would do it straight after the meeting — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — create the features under capability 144 as well — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the reworked window designs, starting with capability 178; Chudinov named them as his single biggest blocker — due **Monday Sept 21 2026** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] — **discharged in substance Sept 21 2026:** the reworked Flex IQ and Flex-Port screens were walked on the [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 call]] ("функционально уже всё зафиксировано"); polish and the Jira load remain; capability 178 itself is out of MVP 1 by owner ruling — [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — confirm whether the cloud-referencing logic in capability 175 is described elsewhere, then decide whether 175 moves to MVP 2 — due unspecified; he refused to move it before checking — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the daily audit-ticket reporting capability and keep it inside MVP 1 — due **Monday Sept 21 2026**; Irina: "**ты отметь себе, чтоб она точно была в [MVP] один, а не уехала куда[-]то**" — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — create features under all of his capabilities, which are currently bare, then tell the others so planning can continue; nothing else in MVP 1 can be planned until he does — due unspecified, and it blocks the rest — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — meet after the call and walk his capabilities and features to set real dates rather than invent them in the meeting; he refused to guess — "**я как сейчас с головы дату возьму?**" — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — plan his own features (165, FlexPort 9 and 10, 173; 160 was also named as his) and check which branch the in-progress feature with no commit against it merged into, before deciding whether to close it as a duplicate — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — port Chudinov's implementation of 156 across to FlexPay once it is done, and set his dates after Chudinov's — due after Chudinov delivers — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [x] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — fill capability 180 with the Flex-Port design and move it to To Do — due unspecified ("Да договорились") — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] — **superseded Sept 23 2026:** the Flex-Port design went into the new capability 235 instead, and the screen feature under 180 moves there — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — decide whether capability 157, now empty on MVP 2, is needed at all — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — send the team a list of capabilities where he added requirements, so they can ask Claude to re-read them — due "в ближайший день 2" — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]] — **Sept 23 2026:** restated; he will post the collection of changed requirements and capabilities to the chat right after the call — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — set the feature dates under capability 152 himself — due Sept 22 2026 (he had started) — [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — settle the STG certificate clash (constant unbinding vs an environment in the thing-name) with Andrei — due unspecified; it blocks installing 152 on STG — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — read the new capabilities and requirements Andrei created (REQ-1460 on card programs; the unassigned multi-card item) and take them to the later meeting — due Sept 23 2026 — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — create the features under capabilities 230, 231 and 234 — due Sept 24 2026 (Pavel: "до завтра") — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] — **Sept 24 2026:** he said he raised features on all the new capabilities Andrei created; the numbers read out are garbled, and 231 was his own, so this stays open until a source confirms all three — [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create a feature under capability 178 for supporting an additional card type — due unspecified — [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]] *(owner ruling 2026-09-20: two-product support is not in MVP 1; this does not reopen it)*

## Open questions

- **Whether capability 175 duplicates reporting already covered elsewhere.** Irina raised it — "**не будет ли это у нас дубл[ь]… делали же какие[-]то отчёты[,] и… на IQ обсуждали в рамках других**" — and it was marked rather than answered — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **Which capability hosts the daily audit-ticket requirement.** Klimovich could not remember — "**я не помню, в как[ой]… там хостится [реквайрмент] этот**" — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **Whether capability 156 itself changes fix version.** The port to FlexPay and the ownership split are clear; the version wording in this passage is garbled and no clean statement of a move is on the recording. The derived notes list 156 among capabilities moving to MVP 2; **recorded as unclear, not asserted** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **Does the Sept-18 principle cover capabilities too?** On Sept 18 Pavel and Irina said requirements should not hang on a developer (capability 180 moved off Biratka). On Sept 22 Pavel confirmed Biratka, a developer, as the responsible for capability 137. The two were not linked by anyone — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]

- **Which way does STG go — constant certificate unbinding, an environment in the thing-name, or moving the cluster?** Chudinov dislikes both of his options; Pavel asked about moving it — [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]

**§15.8:** clear — Jira scope, ownership and device behaviour only. No named person's pay, rate, bonus or performance judgement appears in either source; Klimovich's jab at Bosik's reading of his own capability is recorded as a working exchange, not as an assessment, and nothing was excluded on §15.8 grounds. **§15.9:** no identifier, credential, card number or UPC value appears — card data is discussed only as something InComm has yet to supply.


## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Terminal_Emulator_and_Capability_Split-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Firmware_Delivery_and_Capability_Statuses-September-24-2026.md]]
