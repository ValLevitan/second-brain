---
type: decision
title: The MVP 1 capability list is walked item by item before the Monday freeze — the FlexPay capabilities leave for MVP 2, requirements come off developers, and every remaining capability gets an owner and a status
date: 2026-09-18
aliases: [capability cleanup, MVP1 capability sweep, capability 178, capability 144 clone, capability 151, capability 163, capability 174, capability 175, capability 176, capability 180, capability 148, capability 149, capability 150, capability 116, capability 117, capability 79, capability 80, capability 156, requirements are not hung on developers, требования вешать на разработчика это странно, clone the capability instead of moving requirements one by one, location block enforcement, audit ticket, daily audit printout, capabilities without features, empty capability, test executions instead of features]
source-count: 2
status: active
open-commitments: 9
open-questions: 3
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
## Open commitments

- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — rewrite capability 144's description to match the trimmed requirement set, clean it and move it to the next status — due **today, Sept 18 2026, end of day**; he said he would do it straight after the meeting — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — create the features under capability 144 as well — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the reworked window designs, starting with capability 178; Chudinov named them as his single biggest blocker — due **Monday Sept 21 2026** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — confirm whether the cloud-referencing logic in capability 175 is described elsewhere, then decide whether 175 moves to MVP 2 — due unspecified; he refused to move it before checking — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — finish the daily audit-ticket reporting capability and keep it inside MVP 1 — due **Monday Sept 21 2026**; Irina: "**ты отметь себе, чтоб она точно была в [MVP] один, а не уехала куда[-]то**" — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — create features under all of his capabilities, which are currently bare, then tell the others so planning can continue; nothing else in MVP 1 can be planned until he does — due unspecified, and it blocks the rest — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/irina-shishko.md|Irina Shishko]] — meet after the call and walk his capabilities and features to set real dates rather than invent them in the meeting; he refused to guess — "**я как сейчас с головы дату возьму?**" — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — plan his own features (165, FlexPort 9 and 10, 173; 160 was also named as his) and check which branch the in-progress feature with no commit against it merged into, before deciding whether to close it as a duplicate — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [ ] [[wiki/people/alexander-biratka.md|Alexander Biratka]] — port Chudinov's implementation of 156 across to FlexPay once it is done, and set his dates after Chudinov's — due after Chudinov delivers — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Open questions

- **Whether capability 175 duplicates reporting already covered elsewhere.** Irina raised it — "**не будет ли это у нас дубл[ь]… делали же какие[-]то отчёты[,] и… на IQ обсуждали в рамках других**" — and it was marked rather than answered — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **Which capability hosts the daily audit-ticket requirement.** Klimovich could not remember — "**я не помню, в как[ой]… там хостится [реквайрмент] этот**" — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- **Whether capability 156 itself changes fix version.** The port to FlexPay and the ownership split are clear; the version wording in this passage is garbled and no clean statement of a move is on the recording. The derived notes list 156 among capabilities moving to MVP 2; **recorded as unclear, not asserted** — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — Jira scope, ownership and device behaviour only. No named person's pay, rate, bonus or performance judgement appears in either source; Klimovich's jab at Bosik's reading of his own capability is recorded as a working exchange, not as an assessment, and nothing was excluded on §15.8 grounds. **§15.9:** no identifier, credential, card number or UPC value appears — card data is discussed only as something InComm has yet to supply.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
