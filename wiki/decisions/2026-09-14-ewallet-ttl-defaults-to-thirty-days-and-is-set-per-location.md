---
type: decision
title: An e-wallet gets a lifetime (TTL) — 30 days by default, set per location between 1 and 365 days, and printed on the ticket as a validity period
date: 2026-09-14
aliases: [eWallet TTL, TTL thing, wallet lifetime 30 days, minimum one day maximum 365, wallet valid for X days, empty wallets are simply kept, expiry printed on the ticket, срок жизни волета]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# An e-wallet expires on a TTL: 30 days by default, 1–365 per location

Settled at the [[wiki/meetings/2026-09-14-transactional-mvp1-use-cases-and-ewallet-ticket-recovery.md|Sept 14 2026 8:01 AM call]]. [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] introduced it as part of the e-wallet logic block; [[wiki/people/val-levitan.md|Val]] pushed on it and then accepted it.

## What was decided

Klimovich, when Val asked what "expired" actually means: "у нас вводится понятие TTL… то есть у нас в момент[…] создания [e]volet[a] ему придаётся какой[-]то срок жизни по дефолту." Asked for the number: "**[п]о дефолту есть предложение установить 30 дней, но это конфигурируем[ый] параметр для каждой отдельной локации. Минимум один день, максимум 365**" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

- **Default 30 days**, per-location configurable, **minimum 1 day, maximum 365 days.**
- An expired wallet cannot be worked with; a separate dialogue shows the player a plain error — "мы не должны поддерживать работу с этим [е]волетом… [под] это будет отдельный диалог, показывающий явную понятную игроку ошибку" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## Val's objection, and the answer that closed it

Val's question was why an **empty** wallet should be held for 30 days: "если… он пустой и прошло 20[…] 04:00[…] [з]ачем его держать 30 дней? Или 04:00 или 08:00? Я не знаю сколько, но зачем его держать[…] в системе[,] совсем пустой?" *(the transcript mangles the hour figures Val names; the point — hours rather than days — is clear, the exact hours are not)* [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

[[wiki/people/pavel.md|Pavel Frolov]] answered on build cost, not on policy: "**[н]ам проще его держать, чем придумывать отдельную логику работы с пустыми тикетами**" — keeping it is cheaper than building separate handling for empty tickets. Val accepted immediately and said so: "[д]а, это это хороший ответ… [т]о есть 30 дней, да?" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

## What gets printed on the carrier

[[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] asked whether the expiry is printed on the ticket itself. Klimovich had already laid the ticket out: "есть отдельный регламент, я там уже сверстал дизайн ти[т]о этого тикета нашего, но есть предложение писать *[wallet] valid for … days*… [п]люс на этом тикете будет дата и время создания. **Мы специально не[…] указыва[ем] дату [c]reation[, ] мы указываем время действия, срок жизни**" — deliberately the life span, not just the creation date [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

Chudinov's follow-up was the awkward case: a ticket printed while the default was 30 days, after which the location changes its setting to, say, 45. Klimovich said the rule for that is written up **in the separate regulation, not in a use case** — "[я] прописал это отдельно, это… отдельный ре[г]ламент есть на это[;] я не помню точно[, ] я там это продумывал" — and settled the one part he was sure of: **already-printed tickets are not reprinted.** "[н]о перепечатывать тикет, мы в этом случае точно не будем. То есть если случится так, что там было напечатано 30[, ] мы потом поменяли на другую дату срок[ —] ну ничего страшного" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]].

## How this sits with the rest of the e-wallet rules

The TTL runs alongside two rules restated in the same block and unchanged from the [[wiki/meetings/2026-09-11-transactional-mvp1-scope-and-priorities.md|Sept 11 call]]: an e-wallet is where the player's balance lives outside the machine, and **one wallet has exactly one carrier, existing in a single copy** — "у одного [e]волят[а] только один [c]arrier, то есть билетик… [о]н существует в одном ч[и]сле" [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]. That is the same rule the Sept-11 call had moved out of the capability set and into the regulation; the capability number is recorded there, not here — see [[wiki/decisions/2026-09-11-one-card-at-a-thousand-dollars-and-the-rest-stays-on-the-ticket.md]].

## Open questions

- **What happens to an already-created wallet when its location changes the TTL setting.** Klimovich says a rule exists in the regulation but could not recall it on the call; only "the printed ticket is not reprinted" was settled out loud — [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

*(The derived notes record the same figures — "30 days by default, configurable per location, minimum one day and maximum 365" — and the same reasoning from Pavel about empty wallets.)* [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]

**§15.8:** clear — product configuration only.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
