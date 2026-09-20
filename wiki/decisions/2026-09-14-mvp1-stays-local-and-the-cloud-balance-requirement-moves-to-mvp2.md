---
type: decision
title: MVP 1 keeps wallet balances on the terminal — requirement 1538 comes off capability 158 and moves to a new MVP 2 cloud capability, and the MVP 1 dashboard shows activated cards only
date: 2026-09-14
aliases: [requirement 1538, capability 158, cloud balance moves to MVP2, local terminal storage, dashboard shows activated cards only, eWallet movement reporting deferred, Claude closing a capability wrong, рекламент 1538]
source-count: 2
status: active
open-commitments: 1
open-questions: 0
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

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — create the MVP 2 cloud capability and move requirement 1538 onto it, off capability 158 — due unspecified; he named it among the things he would work on that day and the next — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — scope and tooling only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
