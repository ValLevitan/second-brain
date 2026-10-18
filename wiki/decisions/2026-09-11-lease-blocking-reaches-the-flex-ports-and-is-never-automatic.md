---
type: decision
title: Lease blocking must reach the Flex-Ports as well as the terminal, so players cannot play — blocking a sold machine for non-payment stays manual; in the payment-processing flow the Oct-14 automatic location block applies (owner ruling 2026-10-18)
date: 2026-09-11
aliases: [block the flex ports too, players cannot play, never block automatically, expired lease in the hub stops everything, lease feature written in so it gets tested, disable the bill acceptor through SAS, we can block Flex IQ FlexPay and the Flex Ports, lease expiry blocks offline too, lease versus internet loss, fresh lease date at start-up]
source-count: 9
status: active, narrowed by owner ruling 2026-10-18 — "never automatic" now applies only to machine sales (a customer who does not pay for a Flex gaming machine is blocked by hand); for the payment-processing flow the Oct-14 rules apply (automatic location block, MVP 1.5). The reach into the Flex-Ports stands.
open-commitments: 4
open-questions: 2
---

# Lease blocking reaches the Flex-Ports — manual for unpaid machine sales, automatic in the payment flow

**Owner ruling 2026-10-18:** the Oct-14 interpretation is right — [[wiki/decisions/2026-10-14-jvl-sets-the-location-daily-cap-backs-it-with-a-guarantor-account-and-a-card-and-the-automatic-location-block-is-mvp-1-5.md]] sets the rules of engagement for the **payment-processing flow** (warnings, then the backup account, then an automatic location block). One caveat: when a customer does not pay for a **Flex gaming machine they bought**, the machine is blocked **by hand**. The Sept-11 "never automatic" rule below now applies to that case.

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

## Update, Oct 8 2026 — the lease expired on the test terminals and every Flexport stopped; which screen shows is not settled

At the [[wiki/meetings/2026-10-08-daily-standup-lease-expiry-scenarios-and-flex-signal-quality.md|Oct-8 Minsk stand-up]] (Russian) [[wiki/people/irina-shishko.md|Irina]] asked when the "out of service — lease expired" screen shows: only when the lease runs out by itself, or also when JVL switches a location off for some reason [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].

- **Today the server works only with the date.** [[wiki/people/dmitri-chudinov.md|Chudinov]]: "По текущей работе мы работаем только с датой" — the date can be moved forward or back. There is no function yet to switch off a location ("у нас нет функционала отключения лакейшена"). He described the idea of a button that stops time without touching the date, as for the current machines; whether it exists on the server is unclear. [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- **It worked this morning.** Chudinov: "сегодня лиза за их спарилась. Все феликспроте остановились" — the lease on the test terminals expired today and all the Flexports stopped. Irina: so for now only expiry exists. Chudinov: yes. [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- **What the regulation says.** [[wiki/people/vladimir-samusenko.md|Vladimir]]: when a lease expired, show out of service with the reason "lease expired"; when a lease was revoked, show out of service with no reason; "судя по тому, что говорит клод, так оно реализовано". [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- **A terminal unlinked from its location.** [[wiki/people/alexei-khamin.md|Khamin]] asked. Chudinov: it should be handled, "Но надо проверять". Pavel: a different screen shows; Chudinov: the terminal has no location of its own, it is assigned to nobody. [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- **Two scenarios.** Vladimir: the scenario should become two — lease expired (for any reason, shortened or run out) and terminal unlinked from the location. Chudinov: he sent all these scenarios in files and they must be reviewed with "Андрей", because what was in the requirements is not enough; either leave it as it is and watch how it works, or reopen the discussion. Nothing was settled. [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

"Андрей" who wrote the requirements is [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] by context — he took the Flex-Port blocked-screen requirements on Sept 11 above (**inference**). The notes record the same two open questions [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]].

**Nothing above is superseded.** Manual-only blocking and the reach into the ports stand; Oct 8 shows the lease block working on the test terminals.

## Update, Oct 14 2026 (3:49 PM) — an automatic location block is planned for "MVP 1.5", at the end of a funds chain

At the [[wiki/meetings/2026-10-14-transactional-mvp1-launch-plan-brackets-daily-caps-and-mvp2-scope.md|Oct-14 3:49 PM launch-plan meeting]] (Russian), [[wiki/people/andrei-klimovich.md|Klimovich]] described a chain for a location that cannot pay: primary account, then secondary, then the master, "дальше идет автоблокировка локейшн". [[wiki/people/val-levitan.md|Val]] wanted notices and a chance to recover first, and said the block reaches the Flexports: "Локации, это значит и флекс порты тоже." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

Klimovich reminded him: "Мы договорились, что автор блокировки пока у нас не будет." Val: "давайте назовем это MVP один из половины… Пару машин можно поставить без этого. Извиняюсь, пару лакейшнок." [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]] The notes: "Location auto-block moves to 'MVP 1.5'; a couple of locations may start without it." [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]

So: **for MVP 1 the manual-only rule stands**; an automatic block on unpaid funds is now planned for "MVP 1.5". This is **evolution** of the Sept-11 "никогда" — a planned change, not yet built. Detail: [[wiki/decisions/2026-10-14-jvl-sets-the-location-daily-cap-backs-it-with-a-guarantor-account-and-a-card-and-the-automatic-location-block-is-mvp-1-5.md]].

## Update, Oct 14 2026 (5:33 PM) — the lockout lease in sales practice: 90 days, 30 for risky accounts, rarely used

On the [[wiki/meetings/2026-10-14-sales-q4-trade-in-plan-and-transactional-momentum.md|Oct-14 5:33 PM sales call]] Val asked about machines that "**have leases on them**". Felipe: "**If they're not fully paid, they all have these.**" — "**We do ninety days unless it's a risky account, which I do one month at thirty days.**" He has used it "**Maybe twice with [one customer] and once with another customer. That was it.**" Val: "**I prefer to do everything in my power not to use it.**" When a machine is locked, Felipe talks the owner into paying on a promised date and then unlocks it [[raw/Meeting_Transcript_Sales_Q4_Trade_In_Plan_and_Transactional_Momentum-October-14-2026.md]]. *(This is the existing machine lease, run by people — consistent with "never automatic" above. Customer name not recorded.)*

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — add requirements for the Flex-Port screens so they show adequate states when a location is blocked — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — establish whether the bill validator can actually be disabled through SAS when a location is blocked; he took it as weekend work — due Sept 12–13 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — write the lease feature into the MVP 1 scope so it is tested rather than assumed; he said during the call "всё[,] я добавил" but the test coverage was Val's stated reason — due Sept 11 2026 — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] (by context) — review the lease-expired, lease-revoked and terminal-unlinked scenarios against the requirements — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

## Open questions

- **What state is the machine left in when its Flex-Port is blocked?** Cash-out is agreed to be impossible; whether the player can still feed bills in depends on whether the bill acceptor can be disabled over SAS, which Val asked to be tested rather than assumed — [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- **Which out-of-service screen shows for lease expired, lease revoked, and a terminal unlinked from its location?** The regulation (per Vladimir) gives two screens; unlinking is untested; switching a location off does not exist yet on the server — [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]

*(The derived notes summarise the same two parts — blocking must cover the FlexPorts "so players cannot play", and the standing rule that blocking is never automatic but manual expiry of a location's lease "stops everything".)* [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]

**§15.8:** clear — product behaviour and operating policy only.

## Sources

- [[raw/Meeting_Transcript_Sales_Q4_Trade_In_Plan_and_Transactional_Momentum-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Scope_and_Priorities-September-11-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Lease_Expiry_Scenarios_and_Flex_Signal_Quality-October-8-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Launch_Plan_Brackets_Daily_Caps_and_MVP2_Scope-October-14-2026.md]]
