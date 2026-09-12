---
type: decision
title: The MVP 1 boundary redrawn — bill escrow, player PIN and remote config move out; remote update, Flex-IQ software/firmware management and the Flex-Port master device stay in
date: 2026-09-11
aliases: [bill escrow moves to MVP 2, PIN moves to MVP 2, Flex IQ is PIN-free, remote update MVP 1 remote config MVP 2, master device in MVP 1, software and firmware management Flex IQ, nothing to configure yet, one Amazon S3 store for all firmware, per-location gateway configuration]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
---

# The MVP 1 boundary redrawn — what left, and what joined

Settled item by item at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]] while the capability list was on screen. The headline scope ruling of the same session — Flex IQ alone for October 1 — is on [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]].

## Out of MVP 1

- **Bill escrow → MVP 2. It is kiosk-only.** [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]: "билл эскроу мы можем тоже убрать из [MVP] один точно[;] это связано напрямую только с киоском", repeated a second time as "[в]от этот бил[л] эскроу давай уберём тоже в [MV]P 2" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **Player PIN protection → MVP 2, and Flex IQ is PIN-free by design.** [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] raised it: the on/off mode was built "как расширение на будущее, потому что на флекс[ ]а[й]к[ью], как я понимаю, смысл пин[-]кода нет[ —] ну кассир же не будет пин вводить за игрока[,] или будет?" Klimovich agreed at once — "пин можно тоже вынести на M[V]P 2[;] это только для селф[-]сер[вис] киоска" — and confirmed there is no player PIN screen on Flex IQ at all ("[д]ля игрока нет"), adding that he had already written IQ up as PIN-free in the regulation: "я это уже описывал в этом регламенте" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **But the hook stays, defaulted off.** [[wiki/people/pavel.md|Pavel Frolov]]: "мы сейчас делаем просто задел на то, чтобы пин мог быть… но по умолчанию его отключаем" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. This is consistent with [[wiki/decisions/2026-09-07-pin-and-wallet-load-configurable-per-location.md]] — the PIN remains a per-location option, it is just not exercised in MVP 1.
- **Remote configuration → MVP 2, because there is nothing defined to configure.** Chudinov: "[н]а MVP [один] я думаю что нет, потому что пока у нас даже предположительно нет[,] што конфигурировать. Нечего закладывать… [к]ак только мы определимся, что мы будем конфигурировать, ну в реализации проблем никакой не будет" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## In MVP 1

- **Remote update is a different thing from remote config, and it stays.** [[wiki/people/val-levitan.md|Val]] separated them: "для меня это разные функции[ —] отослать какой[-]то апдейт[,] это без конфигурации[,] это просто апгрейд отослали. А после этого нужно конфигурировать[ —] это ещё одна посылка." He then put the split to the room as a question and got a yes: "давайте рем[о]т апдейт мы делаем на MVP один[,] r[e]mo[te] confi[g] мы делаем на M[V]P 2[,] правильно?" — Chudinov: "[д]а" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. Chudinov had already put remote update in MVP 1 at "99 и 9" percent confidence [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **Software and firmware management for Flex IQ was moved onto MVP 1** by Pavel during the call: "софтв[эр ]ф[ир]м[в]е[р] менеджмент флекс IQ она у нас есть[;] я… сейчас его вот сюда перенесу… [и] всё назначено на [MV]P один" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].
- **Flex-Port master-device functionality belongs in MVP 1.** [[wiki/people/andrey-bosik.md|Andrey Bosik]] asked whether MVP 1 covers updating Flex-Port firmware remotely; Pavel: "100% нужно будет", but it currently sits on MVP 2 "просто по той причине, что есть опасения, что мы не успеем это всё нормально протестировать." Bosik split it into two tasks — "сначала сделать так, чтобы он мог выбрать мастера[,] а 2 это уже способ распространения апдейта туда" — and asked for the first half in MVP 1: "нам к M[V]P один надо заложить функционал мастера… [м]астер девайс" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## The firmware-distribution staging Pavel laid out

Three steps, in order [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]:

1. **Chudinov extends the existing firmware-dissemination mechanism to all FlexPay and Flex IQ** — "он расширит функционал текущего… механизма диссеми[н]ации прошивок на все флекспей[,] флекс а[й]к[ь]ю." This is the piece "лёша" is checking and fixing now — "это то, что сейчас лёша проверяет, находит там косяки[ и] исправляет." *(The source does not say which Alexey; the only Alexey named in this session is [[wiki/people/alexei-khamin.md|Alexei Khamin]]. Left unresolved.)*
2. **Remote update** as step two.
3. **The whole Flex-Port fleet on one unified update system**, with the kiosks distributing to the ports — "чтобы киоски раздавали портам… обновления прошивок для всех флекс портов… весь флот всех флекс портов, чтобы работали через систему единую обновление."

**Two fallbacks were named and neither was discarded.** The absolute last resort is USB — "на совсем крайний случай флекс порты должны с USB обновиться" — and Klimovich accepted the field cost during the pilots: "в рамках пилотов никто не будет возражать, если мы приедем там поставить апдейт." Chudinov added SSH into the terminal plus a script as a further backstop, and said the important thing is that the Flex-Port can at least act as a client: "главное[,] чтобы как минимум это умел как клиент" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

**Bosik asked, explicitly for the transcript, for one storage location.** Flex-Port firmware should be put by the workflow straight into the same Amazon S3 store that holds all the kiosk firmware and distributed from there — "для транскрипта я добавлю, что прошивки для flex порта желательно… чтобы наш [воркфлоу] вложил сразу на [S]3 хранилища в [А]мазоне, где хранятся прошивки для всех наших киосков[,] и оттуда потом… распространял на флекспорт… чтобы у нас единое место хранения было." He believed he had already written it into a capability: "я помню, кстати, где[-]то это прописывал[,] какой[-]то [капабилити]" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]. The Amazon-hosted artefact store and the web console that picks a version per device are the staging mechanism Bosik described later in the same call — see [[wiki/topics/flexpay-business-architecture-payout-devices.md]], Sept 11.

## Per-location gateway configuration, and the list that does not exist yet

Pavel identified the capability that would carry it: "[п]ер[-]лакейш[е]н гейтвей конфигурейшн[ —] по сути вот это то, что задать параметры для лакейш[е]на." Klimovich said the requirements come later and named one already sketched — the PIN at the location's discretion, "что пин[-]код должен быть на усмотрение лока[ц]ии" — then set the real precondition: "[д]обавим другие [регламенты], когда продумаем, что мы можем конфигурировать для каждого киоска[,] для каждого POS[,] для каждой локации[ —] это отдельный список надо" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — extend the existing firmware-dissemination mechanism to all FlexPay and Flex IQ devices (step one of three) — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — have the Flex-Port firmware placed by the workflow into the same Amazon S3 store as the kiosk firmware and distributed from there; he thinks a capability for it already exists and should be found — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — draw up the list of what is actually configurable per kiosk, per POS and per location, before the remote-config requirements can be written — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — move the Flex-Port remote-firmware-update capability so the master-device half sits in MVP 1 rather than MVP 2 — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **Which Alexey is checking and fixing the firmware-dissemination mechanism?** The transcript says only "лёша" — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **LTE modem in every device, or one LTE router per location?** Bosik argued that with several Flex kiosks at one location a bought router with an LTE modem is simpler — "гораздо проще поставить туда… маршрутизатор с поддержкой [LTE] модема, через который все эти устройства смогут ходить в интернет" and "ни[какого] софт[а не] написано[;] маршрутизатор[ —] это же покупное устройство[;] симку вставил, и он уже раздаёт интернет." Val disagreed on cost grounds — "нам дейт[а] стоит дёшево… нам не стоит устанавливать ещё один девайс, писать софт[ ]под это." Pavel called it the right question and pointed at the FlexPay-plus-Flex-IQ location case; **Val then cut the exchange off and no decision was reached** — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The derived notes carry the same list — bill escrow and PIN out, remote update in and remote config out, software and firmware management for Flex IQ onto MVP 1, and the master-device request — and add that Bosik "recalls writing it into a capability already" for the S3 store.)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — scope and tooling only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
