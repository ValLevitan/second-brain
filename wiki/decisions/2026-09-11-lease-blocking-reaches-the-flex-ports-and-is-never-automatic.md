---
type: decision
title: Lease blocking must reach the Flex-Ports as well as the terminal, so players cannot play — and blocking is never automatic, only manual through the hub
date: 2026-09-11
aliases: [block the flex ports too, players cannot play, never block automatically, expired lease in the hub stops everything, lease feature written in so it gets tested, disable the bill acceptor through SAS, we can block Flex IQ FlexPay and the Flex Ports, lease expiry blocks offline too, lease versus internet loss, fresh lease date at start-up]
source-count: 4
status: active
open-commitments: 3
open-questions: 1
---

# Lease blocking reaches the Flex-Ports — and is never automatic

Ruled by [[wiki/people/val-levitan.md|Val]] at the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 2026 8:04 AM call]], in two connected parts: the **scope** of a block, and the **trigger** for one.

## Part one — the lease feature is in phase 1, and must be written down so it gets tested

Val asked whether the lease feature — the one that lets JVL stop a location working — is switched on in phase 1 on Flex IQ. [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]: "[ф]ормально она уже интегрирована, потому что это был[о] интегрировано на базе мото[гус] режима… [м]ы переиспользуем" — formally already integrated, built on the MudaGoose mode and being reused. Val's instruction: "давайте пропишем, чтобы она была… [ч]тоб её протестировали" — write it in so it gets tested [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

*(This is a live consequence of keeping the MudaGoose code in place — see [[wiki/decisions/2026-09-11-mudagoose-never-in-mvp1-and-its-code-comes-out-at-mvp3.md]], where the same call resolved to leave that code alone until MVP 3.)*

## Part two — the block must cover the ports, not just the terminal

Chudinov raised the gap himself: "[к]огда у нас был вариант мото[гус] режим[,] мы блокировали только сам терминал. Сейчас у нас появляются флекспорты. Если у нас какое[-]то решение, например[,] вот лиз, либо не оплата… мы блокируем терминал или мы блокируем и фл[е]кспорты тоже[?]"

> **Val:** "[Ф]лекспорты тоже."
> **Chudinov:** "То есть игроки не могут играть."
> **Val:** "Не могут." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

Val restated the reach a few minutes later, for the record: JVL can block **Flex IQ, FlexPay and the Flex-Ports** — "у нас есть возможность заблокировать flex IQ… флекс пей… и флекс порты" — and, "скорее всего", the bill acceptors too [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

[[wiki/people/andrei-klimovich.md|Andrei Klimovich]] took the screen consequence: "я добавлю требования по поводу экранов [флекс]порта, чтобы он показывал… адекватные состояния" — Flex-Port screens must show adequate states when a location is blocked [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Part three — what state the machine is left in

[[wiki/people/irina-shishko.md|Irina Shishko]] pressed the obvious follow-up: "[ф]лекс[]порт мы блокируем[ —] а машина в каком состоянии остаётся?… там есть бил[л]валидатор." Chudinov: they will not be able to cash out ("[о]ни не смогут кол[аут] сделать"); Irina: but they can still feed money in ("бросить деньги туда смогут"). Val disagreed and gave the mechanism — "[п]о[-]моему не смогут. [М]ожем desable через sas" — [[wiki/people/pavel.md|Pavel Frolov]] thought so too, "вроде мы сможем бил[л ]акс[е]птер задизейбл[ить]", and Val closed it by asking for it to be tested: "давайте про[те]стиру[ем] это" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

## Part four — blocking is never automatic, and an old misunderstanding gets cleared up

Chudinov recalled that the block-on-non-payment function had been switched off and asked whether it was still off. Val reacted sharply — "100[,] 100% мы не отключили[,] 100%[;] я без этой фичер жить не могу" — and then, when told the instruction had come from him, "я 1 раз об этом слышу… для меня это абсолютная новость" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

Klimovich supplied the missing context and it resolved cleanly:

> **Klimovich:** "[М]ы тогда обсуждали, что у нас идёт тестирование реально первых платежей на продакшн сервере через dola play… что делать, если платёж задерживается, если ошибка у нас, если ошибка [у Двола] ещё что[-]то[ —] блокируем ли мы локацию[?] И тогда было чётко сказано, что нет… [р]уками[,] автоматом не блокируем."
> **Val:** "[Д]а[,] я помню это разговор, но мы говорили про автоматическую блокаду… автоматически мы не блокируем." [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**Val then stated the standing rule twice, in absolute terms:** "[а]втоматически нет[,] автоматически мы никогда не блокируем[,] никогда." And the manual path that does work, described by Klimovich and confirmed by Val: "[р]уками мы можем зайти в приманхаб, выбрать локацию, указать ей лиз как expire[d] le[ase] — и автоматически всё заблокируется" / Val: "не автоматически, а в [м]ан[у]ально[м режиме] всё заблокируется"; Klimovich: "после выбора лиз[а] на экспай[р] всё остановится" [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]].

*(The management console Klimovich names is transcribed "приманхаб". The corpus's own term for the transactional management layer is **Terminal Hub** — see [[wiki/decisions/2026-09-10-per-product-components-and-mvp-fix-versions-on-the-capability-project.md]] — but nothing in this source says they are the same thing, so the rendering is left as spoken.)*

**So the settled position is:** the *trigger* is always a human setting a location's lease to expired in the hub; what follows *after* that trigger is automatic and stops everything, ports included. The Dolla Play production-payment testing is the reason automatic blocking on non-payment was disabled, and that disabling was Val's own instruction — recorded here because the misunderstanding was live in the room and is now closed.

## Update, Sept 16 2026 — lease expiry and internet loss are separated, and the device-side mechanism is stated

At the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]] [[wiki/people/dmitri-chudinov.md|Chudinov]] described how the lease actually works on the device: Flex IQ and FlexPay fetch a fresh lease date at start-up, then keep monitoring the last lease they hold, and **block themselves on expiry even while disconnected**, unblocking as soon as a connection returns with a fresh date [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

The meeting then established that **lease expiry and loss of internet are two different things and only lease expiry blocks** — [[wiki/people/irina-shishko.md|Irina]]: "мы тут 2 вещи… в одну свалили" — and that a device with a valid lease now starts up and keeps trading with no internet at all. See [[wiki/decisions/2026-09-16-a-location-keeps-working-without-internet-and-only-the-card-stops.md]], which also records Chudinov arguing the opposite first, from the control requirement recorded on this page: "мы в любой момент должны уметь заблокировать терминал. Сами" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Nothing on this page is superseded** — manual-only blocking and the reach into the ports both stand. What is added is that the *lease* block survives disconnection, and that an internet outage on its own is not a block.

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — add requirements for the Flex-Port screens so they show adequate states when a location is blocked — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — establish whether the bill validator can actually be disabled through SAS when a location is blocked; he took it as weekend work — due Sept 12–13 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — write the lease feature into the MVP 1 scope so it is tested rather than assumed; he said during the call "всё[,] я добавил" but the test coverage was Val's stated reason — due Sept 11 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

## Open questions

- **What state is the machine left in when its Flex-Port is blocked?** Cash-out is agreed to be impossible; whether the player can still feed bills in depends on whether the bill acceptor can be disabled over SAS, which Val asked to be tested rather than assumed — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

*(The derived notes summarise the same two parts — blocking must cover the FlexPorts "so players cannot play", and the standing rule that blocking is never automatic but manual expiry of a location's lease "stops everything".)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — product behaviour and operating policy only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
