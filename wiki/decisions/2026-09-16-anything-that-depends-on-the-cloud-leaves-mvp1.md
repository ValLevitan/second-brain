---
type: decision
title: Anything that depends on the cloud comes out of MVP 1 — Val orders the whole requirement list swept against what will actually work on October 1, and the rule is then applied requirement by requirement
date: 2026-09-16
aliases: [be honest with yourselves, уберите это, capability 116, capability 177, requirement 1379, requirement 1431, requirement 1444, requirement 1450, requirement 1483, requirement 1485, requirement 1486, single cloud channel, cloud wording removed, MVP2 cloud capability, local store only, open items capability, самим себе врать нельзя, capability 229, capability 158, requirement 1514, requirement 1515, requirement 1516, requirement 1543, payment hub is only the card]
source-count: 5
status: active
open-commitments: 1
open-questions: 1
---

# Anything that depends on the cloud comes out of MVP 1

The organising ruling of the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept 16 2026 8:01 AM call]] (Russian). It turns the narrow Sept-14 finding — that one balance requirement assumed a cloud MVP 1 does not have ([[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]]) — into a sweep rule applied to every remaining item on the list [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## How it surfaced: capability 116 assumes something that does not exist

Requirement **1379**, "single cloud channel", under **capability 116**, asked what happens when the channel is down. [[wiki/people/dmitri-chudinov.md|Chudinov]] stopped to ask *which* channel — "канал взаимодействия IQ и клауд[-]сервисов или канал взаимодействия флекс[-]портов и мастера устройств[?]" — and [[wiki/people/andrey-bosik.md|Bosik]] answered it: "уже написано сингл клауд[ ]ч[а]н[е]л… в общем, внешний канал связи" — the external communication channel, not the local one [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

[[wiki/people/andrei-klimovich.md|Klimovich]] then described what he assumed the behaviour was — Flex-Ports stay connected to the gateway, a wallet can be created locally but not in the cloud, and "как только он вернул[ся] [интернет], эти все вол[еты], созданные локально, должны будут продублироваться в клауд[е]" — and Chudinov flatly contradicted him [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Нет, не… в текущей реализации. Текущая реализация[ —] только локал стор[идж]. Конкретного мастера устройства.**
>
> *(No — not in the current implementation. The current implementation is local storage only. On the specific master device.)*

[[wiki/people/irina-shishko.md|Irina]] named the problem the capability therefore creates: "это capability 116, и она у нас стоит как MVP один… по нашим требованиям это всё должно работать к 1 октября, но не будет работать" — the capability is marked MVP 1, its requirements say it all works by October 1, and it will not [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. Her argument for removing rather than rewording was release legibility: "как нам делить, что сделано, что не сделан[о]?"

**Klimovich had already flagged the dilemma two calls earlier and left it unresolved** — "у нас многие [ка]п[а]б[и]лити [и реквайрмент]с написаны исходя из Того, что у нас будет всё с клаудом работать, и мы говорили[:] нам всё переписать, убрать упоминания клауда. Или…" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Val's ruling

[[wiki/people/val-levitan.md|Val]] cut it off in four sentences [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]:

> **Уберите это. Надо быть честн[ым] с самим собой. Мне важно, чтобы работал[о] 1 октября. Всё, что мы не можем сделать 1 октября, уберите.** … **Не надо[,] не надо самим себе врать нельзя.**
>
> *(Remove it. You have to be honest with yourself. What matters to me is that it works on October 1. Everything we cannot do by October 1 — remove it.* … *No, no — you must not lie to yourselves.)*

It is the same instrument as the Sept-15 rule that unwritten things do not exist ([[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]]), pointed the other way: there, nothing counts unless it is written; here, nothing may stay written unless it will actually ship.

## Where the cloud material goes — capability 177, provisionally

The destination is the MVP 2 cloud capability Klimovich created the previous day: "[ка]п[а]билити… я уже вчера создал, да, котор[ая] касательно клауд[а] именно[,] всё, что у нас… висит на MVP 2" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. **That creation is the first confirmation in the corpus that the capability promised on Sept 14 and still outstanding on Sept 15 now exists** — see the Sept-16 update on [[wiki/decisions/2026-09-14-mvp1-stays-local-and-the-cloud-balance-requirement-moves-to-mvp2.md]].

**Its number is recorded as provisional, not asserted.** Neither Klimovich nor Irina could identify it with confidence on screen. Irina first rejected 177 ("[капа]билит[и] 177, где клауд [и]волет[?] нет, это не то"), Klimovich recognised it as the balance one ("это про баланс? Да, это касательно именно было баланса"), and Irina's reason for settling on it was ordinal rather than substantive: "177 тогда возможно, потому что наверно выше нет ничего, чем 177 [капа]билити" — 177 then, probably, because there is nothing numbered higher. Klimovich's instruction was correspondingly tentative: "**давайте пока туда повесим**" (let us hang it there for now) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]. *(This is consistent with the Sept-15 record, where the new capability was created around the cloud **balance** requirement; the corpus does not establish 177 as its identifier.)*

Only requirement 1379 moved, not the whole capability — Klimovich asked "весь 116 переез[жа]ет тогда в MVP 2?" and Irina refused: "не весь… мы [ска]зали только 1379". Capability 116 carries three requirements in total [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## The rule applied down the rest of the list

| Requirement | What it is | Where it went |
|---|---|---|
| **1379** | single cloud channel (capability 116) | to the MVP 2 cloud capability, provisionally 177 |
| **1431** | ticket PIN, wrongly hung on Flex IQ capability 141 | unlinked; **"пин[-]кодов на флекс[е] [ай]кью нету в принципе"** — there are no PIN codes on Flex IQ at all — so it becomes a FlexPay item in MVP 2 |
| **1444** | Flex Pay Slim / Flex Recycler | MVP 2 |
| **1450** | money taken, player walks away from the wallet-creation confirmation screen | MVP 2 — "будем решать потом" |
| **1483** | after redemption, FlexPay self-service | moved to FlexPay |
| **1485** | self-service | MVP 2 — Klimovich: "почему они остались в MVP один[?] это я что[-]то не досмотрел" |

All rows: [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]], corroborated by [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**One self-service item was deliberately kept.** Requirement **1486**, the emailed receipt: Chudinov recalled the team had agreed email was not needed at all, and Klimovich kept it anyway for the self-service screen — "это… нужно для селф[-]сервиса[,] пускай будет. Экономия бумаги немного" (a little paper saved) [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**Requirement 1431 is now orphaned.** Chudinov unlinked it from capability 141 but had not found a FlexPay capability to attach it to — "я её отвязал, но не успел привязать на fl[e]xpay[,] не знаю куда… привязать" — and Klimovich deferred it: "в MVP 2 тогда решим" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Val's parking rule for open items

Separately, and against deleting requirements wholesale, Val proposed a holding pen: if you do not know what to do with an open item, "заведите себе [open] it[e]ms [ка]п[а]билити и положите всё туда. Когда закончится этот митинг, мы решим, что делать, или оставим просто открыты[м]" — create yourselves an open-items capability, put everything in it, and decide after the meeting. *(The passage is heavily garbled and is recorded as a proposal made, not as an instruction adopted; nobody created such a capability on the call.)* [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — find the FlexPay capability that requirement 1431 (ticket PIN) should hang off, now that it is unlinked from Flex IQ capability 141 — due unspecified — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]


## Update, Sept 17 2026 — one more data point on the number, and it is still not enough

The [[wiki/meetings/2026-09-17-transactional-mvp1-skillpay-multi-product-and-device-network-security.md|next morning's call]] sent four more orphan requirements (**1431, 1030, 1413, 1421**) to the same MVP 2 parking bucket, and produced the only fresh evidence about its identifier: Irina Shishko, reading a note off the screen, said 1431 is attached to "**кап[,] там что[-]то 170 с чем[-]то**" — a capability *somewhere in the 170s*. Klimovich confirmed only that he had linked it and that it is "**наш паркинг для [MVP] 2**" [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]].

That is consistent with 177 and establishes nothing. **177 stays provisional and is not asserted.** A second uncertainty was added at the same time: Klimovich describes creating a *placeholder capability for orphan requirements* "yesterday" (Sept 16), having described creating the *cloud* capability "yesterday" (Sept 15) on the previous call — one capability or two is unstated. See [[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]].

## Update, Sept 21 2026 — capability 229, and the last cloud mentions come out

The [[wiki/meetings/2026-09-21-transactional-mvp1-flexport-and-iq-ux-design.md|Sept-21 8:02 AM call]] opened on this rule. [[wiki/people/irina-shishko.md|Irina Shishko]]: "Я получается создала capaбилити 229 туда сейчас… вынесла то, Что касается клауда, чтоб оно не мешало текущей разработке, то есть это нужно будет потом" — she created **capability 229** to hold the cloud material, out of the way of current work, "На MP 2" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. **This is the first spoken number for a cloud capability that is not a guess.** It does not say whether 229 replaces the provisional 177 or sits beside it.

[[wiki/people/andrei-klimovich.md|Klimovich]] was running the rest of the list through Claude during the call and had found more: requirements **1514, 1515, 1516 and 1543** under **capability 158**, which mention the payment hub working with wallets. Irina expected nothing cloud to be left in 158: "Не должно было быть уже в 158, ничего." His rewrite: because the payment hub is a cloud service, "работа с валитами у нас локальная на машине" — the whole wallet life cycle stays local [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. [[wiki/people/dmitri-chudinov.md|Chudinov]] asked everyone to mark it the same way in future reviews: the payment hub only handles the card; "на терминале… все балансы и создания по вольтам идут локально. Карточка это пхаб" [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]. Klimovich put the finish at about ten minutes after the call.

## Update, Sept 22 2026 — the cloud wording is out of MVP 1

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 8:01 AM call]] Klimovich reported the clean-up done: "был ещё должок по поводу упоминания всяких клаудов. Теперь все чисто". MVP 1 is now "[аг]ностична по отношению к тому, где хранится [волет]" — nowhere does it say that transactions are created, stored or verified against the cloud [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

Why it matters came up the same hour. Chudinov recalled why he had asked for the requirements to be fixed: because the cloud was written in, Claude "начал на п[эй]м[ент] хабе создавать фичи [по] поведению волета" — on a repository where none belong (the transcript's "п мхабе" read as the payment hub — **inference**). See [[wiki/topics/ai-assisted-development.md]] (Sept 22) [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

## Open questions

- **Which capability is actually the MVP 2 cloud capability.** The team hung requirement 1379 on 177 because it was the highest-numbered, while recognising 177 as the balance-related one; the number is not established — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]] *(Sept 21: Irina names capability **229** as the one she created for the cloud material; how it relates to 177 is not stated, so the question stays open.)* [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]

**§15.8:** clear — release scope and Jira hygiene only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no licence, registration, tax or account number appears in this material.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_SkillPay_Multi_Product_and_Device_Network_Security-September-17-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_and_IQ_UX_Design-September-21-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
