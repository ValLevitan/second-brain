---
type: decision
title: MVP 1 keeps wallet balances on the terminal — requirement 1538 comes off capability 158 and moves to a new MVP 2 cloud capability, and the MVP 1 dashboard shows activated cards only
date: 2026-09-14
aliases: [requirement 1538, MVP1 cloud scope is two things, device online status, issued cards dashboard, operations dashboard specification, machine statistics premium tier, capability 158, cloud balance moves to MVP2, local terminal storage, dashboard shows activated cards only, eWallet movement reporting deferred, Claude closing a capability wrong, рекламент 1538, requirement 1436, data retention, factory reset wipes everything, capability 177]
source-count: 6
status: active
open-commitments: 3
open-questions: 2
---

# MVP 1 stays local; the cloud-balance requirement moves to MVP 2

Settled at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]]. Raised by [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]], agreed by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] and [[wiki/people/pavel.md|Pavel Frolov]], with the release-clarity argument supplied by [[wiki/people/irina-shishko.md|Irina Shishko]].

## The mismatch Chudinov flagged

Chudinov: "рекламент 15[]38… прилетел на [MVP] 1. У него сильный акцент на то[,] что у [e-]волетов… облачный баланс, то есть доступ с разных терминалов, и обсчёт идёт там. У нас такого мы пока не обсуждали, и вынесли это на будущее." MVP 1 reality: "[т]ерминал ведёт свой баланс, баланс волитов своих" — the terminal keeps its own wallet balances. Klimovich confirmed the standing scope: "мы говорили, что в [MVP] один мы остаёмся на локальном… условно локальная логика" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**The requirement is literally numbered 1538 and hangs off capability 158** — "он висит на к[а]пбилити 158" — leaving what Chudinov called a straight contradiction: "как бы [capa]bili[ty] готова, но требования не удовлетворяет" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. *(Both numbers are audible and stated plainly; the derived notes carry the same two numbers, while cautioning that capability and requirement numbers in this recording are spoken, never spelled out.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## The practical reason it matters — Claude builds the cloud into MVP 1

Chudinov's real complaint was a tooling one, and it is the first time the corpus records the AI assistant misfiring on the capability workflow itself: "**потому что мы это собираемся делать позже, и Клод начинает с ума сходить. Я собираюсь типа закрывать [capa]bilit[y —] ну слушайте, у нас тут баланс должен быть в облаке[ —] я начинаю создавать эти фичи**" — he goes to close a capability, the requirement demands a cloud balance, and features start getting created for it [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## What Klimovich refused, and what was agreed instead

Klimovich would not rewrite the capability set down to local: "[а] стоит ли переписывать эти все к[е]пюбилит[и], рекламу[,] убирать оттуда упоминания облако? Я когда писал, я специально писал их[ —] версии, куда мы хотим прийти[ —] и было бы очень странно сейчас везде прописывать, что окей, это [local] локал локол локол" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Chudinov's narrower fix won: detach that one requirement — "не переписать[,] просто… вот конкретно этот рекламент отвязать." Klimovich turned it into the agreed action: "**я могу для [MVP] 2 создать… [capability], говорящи[й] про облако[,] уже полностью облачную логику[,] закинуть туда 15[]38**." Chudinov: "так лучше"; Pavel: "согласна" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**Irina supplied the reason it is worth the bookkeeping:** "[м]ы выпустим 1 октября[ —] как ты закроешь эти к[е]пбилити, что мы выпустим, чтобы понимать, что вот в этом релизе мы сделали вот это, а теперь мы будем делать следующее." The October-1 release has to be legible as a closed set [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. The date itself is unchanged — see [[wiki/decisions/2026-09-09-first-transactional-installation-planned-for-october-1.md]].

## The consequence for reporting

Klimovich asked what follows for the dashboard while storage is local. Chudinov drew the line:

- **The MVP 1 dashboard shows activated cards only** — "[д]а[ш]борт мы показываем по карточкам[;] уже нас интересует выпущенные карточки… мы по[м]ожем сказать, кто, где, когда, почём" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].
- **All wallet movement on a terminal stays local and is not exported** — "все движения по какому[-]то волю[ту], котор[ые] на каком[-]то… терминале[, ] мы это никуда не выгружаем, он хранится локально." That is "отдельная группа задач", better done with the move to cloud: "я склоняюсь к тому, что на [MVP] один мы это не сделаем, а если мы будем переходить на облачн[ое], то нам уже лучше сделать это всё вместе и правильно." Klimovich: "[д]оговорились, согласен" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Pavel filed it where it belongs: "это похоже на репортинг именно вот этой вот новой… [capability], которы[й] ты только что озвучил, что ты создашь" — i.e. reporting for the new MVP 2 cloud capability [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Klimovich noted in passing that the card-only dashboard is inherited from MudaGoose and that the port changes what is possible: "ну да, это было для [MudaGoose;] сейчас[, с] появлением порта, и когда у нас контроль есть над всей экосистемой, мы можем гораздо больше интересной информации показывать[ —] ну окей, это в любом случае не [MVP 1]" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

**A separate dashboard need surfaced in the same session and is NOT deferred:** Chudinov argued the cashier needs a view of "тикетов, которые были созданы, но не напечатаны" — wallets created but not printed — and Klimovich said that exact block had been added the day before. That belongs to [[wiki/decisions/2026-09-14-the-ewallet-is-created-before-its-ticket-prints.md]], not to the deferred cloud reporting [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Update, Sept 15 2026 — the cloud scope is pinned to exactly two things, and 1538 has still not moved

At the [[wiki/meetings/2026-09-15-transactional-mvp1-balance-naming-and-ui-flow-walkthrough.md|Sept-15 8:03 AM call]] Klimovich began to describe an MVP 1 cloud dashboard in aspirational terms — "чтото вообще такое красивое чистенькое с лакейш[н,] трекинг[,] юниты[,] транз[э]кшнс[,] инвойсы… перформанс" — and Chudinov cut the scope down to a list of two [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]:

> **не фантазируй[,] давай на MVP один… на веб сервис[ах] то, что вот мы в [клауде] отображаем[ — ]это репорт по карточкам. То есть мы можем показать[,] девайсы оператора подключены[,] онлайн… работает[,] не работает. И даш[б]орт по выпущенным карточкам… Все остальное обсуждаем[ое] и на MVP 2[ или ]3.**

So MVP 1 in the cloud is **device/operator online status** plus the **issued-cards dashboard** — the second of which is exactly the "activated cards only" line already ruled above. Klimovich accepted: "хорошо, я понял." Asked about invoices, Chudinov kept billing where it is: "всё, что с биллингом[,] остаётся, оно будет работать[,] как работа[ет] сейчас", and Pavel confirmed "инвойсы это остаются" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**Requirement 1538 has still not been moved.** Klimovich, the next morning: "рек[вайрмент] 15[ ]38[ — ]то, что вчера проговорили[ — ]ещё не вынес[,] вынесу. Сегодня оно должно будет уйти в новый к[а]п[абилити] для 2 MVP и тогда уберу оттуда." [[wiki/people/val-levitan.md|Val]] asked [[wiki/people/andrey-bosik.md|Bosik]] to prepare the ground so the status change can be made the moment Klimovich finishes. The commitment below stands with a restated due date [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**Val refused an abstract MVP 1 promise.** Klimovich said some part of the dashboard would definitely appear in MVP 1; Val: "**но вы не можете абстрактно говорить, что чтото будет в [MVP] один без точного указания, что будет**… то есть вы говорите, что будет [operations dashboard], но вы ещё не обусловили, какие репорты в нём будут… в стадии [MVP] один". Klimovich accepted and gave a sequence: close everything needed for the IQ device and the ports that day, including the whole transaction set, "после этого я переключаюсь на… о[пера]ционный дэшборд MVP один версию… конкретно, какие параметры, какие репортинги" — delivered "буквально в ближайши[е] пару дней" [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

**And the deferred half got a commercial shape.** Chudinov raised that JVL can now collect statistics from the machines over SAS and could give the operator machine-level statistics. Val: "**абсолютно абсолютно… это это наш гвоздь программы**" — our showpiece. Klimovich: "это огромн[ый], один из самых сладких и важных кусочков, которые мы будем добавлять поэтапно", to be sold in blocks from the web service — "хотите расширенный пакет? пожалуйста, вот столько стоит[;] там ужатый пакет[ —] столько стоит" — while the location itself sees only "очень сжатая информация только для этого лакейш[на,] [в] самом минимальном формате" (Val). None of that is MVP 1 [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]].

## Update, Sept 16 2026 — the MVP 2 cloud capability now exists, and the local rule is generalised to the whole requirement list

At the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]] Klimovich confirmed the capability has been created — "[ка]п[а]билити… я уже вчера создал, да, котор[ая] касательно клауд[а] именно[,] всё, что у нас… висит на MVP 2" — i.e. on Sept 15, after that morning's call. **That discharges the creation half of the commitment below; the corpus still contains no confirmation that requirement 1538 itself has been moved onto it** — 1538 was not mentioned at all on Sept 16 [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Its number is unresolved.** The team settled on **177** for want of a better candidate — Irina's reasoning was ordinal ("177 тогда возможно, потому что наверно выше нет ничего") and Klimovich recognised 177 as the balance-related capability before saying "давайте пока туда повесим". See [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]], where the whole sweep is recorded and the number is carried as provisional [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The one-requirement ruling became a rule for everything.** Val: "уберите это. Надо быть честн[ым] с самим собой… всё, что мы не можем сделать 1 октября, уберите" — and requirements 1379, 1431, 1444, 1450, 1483 and 1485 left MVP 1 in the same hour [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**"Local" was also given a retention meaning (requirement 1436).** Chudinov: "срок хранения[,] в случае, если образ не переустанавливает[ся,] — бесконечность. При переустановке нового инсталлера будет полное затирание[,] с потерей всех данных" — while the data lives on the device it is kept indefinitely; a full re-image from the SD card (the team reached for "factory reset" as the name) wipes everything. Pavel set the expectation that this is rare: "переустановка софта с [SD-]карточки[ —] это будет крайне редкое событие. Мы рассчитываем, что обновление всё[-]таки будет через воздух… с сохранением" — updates come over the air with data preserved, which is the remote-update path ruled into MVP 1 on [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]]. Klimovich noted the whole question changes once records live in the cloud and are merely pushed to the machine [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**The operations-dashboard specification is still outstanding.** Klimovich's Sept-16 status was "продолжаю заниматься [UI] и… дэшборд[ом]" — still in progress, nothing delivered [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — move requirement 1538 onto the MVP 2 cloud capability, off capability 158 — restated Sept 15 2026 as due **that day**. **Partially discharged Sept 16 2026**: the MVP 2 cloud capability was created on Sept 15; the move of 1538 is still unconfirmed — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — produce the MVP 1 operations-dashboard specification naming which reports it actually contains — due within a couple of days of Sept 15 2026, after closing the IQ and port capabilities; **still in progress as of Sept 16 2026** ("продолжаю заниматься [UI] и… дэшборд[ом]") — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]] [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — prepare the ground so requirement 1538's status can be changed as soon as Klimovich moves it — due Sept 15 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

## Open questions

- **Whether machine statistics collected over SAS become a paid premium tier on the web service, and in which MVP each block lands.** Val calls it the showpiece and Klimovich describes a tiered package model, but no tier, price or release was fixed — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- **What the location gets versus what the operator gets** in report form. Klimovich named it as needing thought, with [[wiki/people/juan-martinez.md|Juan Martinez]] and the locations as the sources — "с вами[,] и[з] хуаном[,] и собрать побольше информации от лак[ей]шн[о]в… какой тип информации нужен" — [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]

**§15.8:** clear — scope, tooling and product-tier economics only; no named person's compensation appears.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Balance_Naming_and_UI_Flow_Walkthrough-September-15-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
