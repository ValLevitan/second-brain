---
type: decision
title: An e-wallet gets a lifetime (TTL) — 30 days by default, set per location between 1 and 365 days, and printed on the ticket as a validity period
date: 2026-09-14
aliases: [eWallet TTL, TTL thing, wallet lifetime 30 days, minimum one day maximum 365, wallet valid for X days, empty wallets are simply kept, expiry printed on the ticket, срок жизни волета, requirement 1451, expired wallet display, expired wallet wording]
source-count: 6
status: active
open-commitments: 1
open-questions: 3
---

# An e-wallet expires on a TTL: 30 days by default, 1–365 per location

> **Status note (Sept 17 2026):** still `active` — no later engineering source withdraws it. But three days later, in front of a customer, Val called the expiry "**a hole in our design**" and Andrei said wallets "**should have a ceiling up to seven years**". See the Sept-17 update below. Whether the TTL is replaced is queued for the owner.

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

## Update, Sept 16 2026 — how an expired wallet is shown is still an open UI question (requirement 1451)

At the [[wiki/meetings/2026-09-16-transactional-mvp1-open-questions-and-offline-operation.md|Sept-16 8:01 AM call]], requirement **1451** was the last item on the list. [[wiki/people/andrei-klimovich.md|Klimovich]] confirmed the behaviour — a scanned wallet that has expired is shown as expired — and said the only unanswered part is wording: "мы будем показывать, если просканирован какой[-]то вол[ет], который [э]кспа[йр]ед… тут вопрос к [UI] чисто[:] просто какими словами всё это будет названо" [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

**This is the one open question the meeting deliberately left in place for a reason of its own**: Klimovich kept the placeholder so he would not forget to remove it — "давайте я оставлю эту [толпу] на этом пока[,] и потом, когда UI добавится, я удалю его отсюда". [[wiki/people/irina-shishko.md|Irina]] had the requirement's status taken off Published at the same time; her following words naming the target status are garbled and are not reconstructed here [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]].

## Update, Sept 17 2026 — "a hole in our design": a customer says Georgia law needs seven years

At the [[wiki/meetings/2026-09-17-dynamic-gaming-georgia-master-licensee-and-cashless-pitch.md|Dynamic Gaming meeting]] (3:17 PM) the visiting master licensee challenged any expiry at all. [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]

- **What he had been told.** Felipe: "**If you say that you can take the ticket for 30 days or 60 days or 90 days because Andre said it was configurable per location, they could take the TITO for 30 days and said you must have it for seven.**" That is this page's per-location setting, as a customer heard it.
- **His rule.** "**If he walks out without paying the twenty dollars, you are liable to pay the state of Georgia the twenty dollars as an unclaimed fund**"; "**it cannot expire. It cannot disappear from the terminal**"; "**there shouldn't be any dormancy on that. There shouldn't be any service fee on that, as per law.**" He was not sure of the period: "**Five years or seven years? Just need to confirm that.**" The full unclaimed-funds rule he gave is on [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]].
- **Val accepted the point.** "**Good point. It's a it's a hole in our… design.**" And: "**we absolutely have no issue keeping you for seven years… the limit of 30 days or 15 days or five days or 10 days is irrelevant to us.**"
- **Andrei drew the design change.** "**So our U wallets should have a ceiling up to seven years. There is no point for confirmation.**" Val: "**Then we don't have to configure it.**"

**Evolution or contradiction?** Sept 14 set a 30-day default with a 365-day maximum; Sept 17 says seven years with no setting. They are about the same product, three days apart, and the later one is newer. **But it was said to a customer, not decided in an engineering session, and nothing after it (the Sept-18 call) records a change to requirement 1451 or the TTL.** So the TTL stays current on this page, the Sept-17 position is recorded here, and the call is queued. [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]

*(The derived notes also say "JVL's design charges $5/month on unused funds from month 13". The recording does not support that: Val's line "**It's charging five dollars per month for unused funds on the account starting month 13**" follows "**a really good question about income**" and names no subject. This page's Sept-14 rule has no monthly charge. See the meeting stub.)* [[raw/Meeting_Notes_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]] [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]

## Open commitments

- [ ] [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] — remove the open-question placeholder from requirement 1451 once the expired-wallet UI wording is added — due after the UI is added — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Open questions

- **Does the TTL survive the Sept-17 "seven years" position?** Val called the expiry "a hole in our design" and Andrei proposed a seven-year ceiling with no setting, in front of a customer; no engineering source has yet changed the TTL — [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]
- **What an expired wallet is actually called on screen.** Behaviour agreed; the wording is a UI question left open on purpose — [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Use_Cases_and_eWallet_Ticket_Recovery-September-14-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Open_Questions_and_Offline_Operation-September-16-2026.md]]
- [[raw/Meeting_Notes_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]
- [[raw/Meeting_Transcript_Dynamic_Gaming_Georgia_Master_Licensee_and_Cashless_Pitch-September-17-2026.md]]
