---
type: decision
title: Rolling back to a previous build is removed from MVP 1 — the database schema moves with the code, so the team rolls forward only
date: 2026-09-18
aliases: [roll forward only, forward development, no rollback, откат на предыдущую версию, always forward, нашли баг выпустили следующую версию, requirement 1367, capability 122 rollback requirement, firmware rollback dropped, database schema changes between builds, re-cut the version you wanted, Val wrote remove it from MVP1]
source-count: 2
status: active
open-commitments: 0
open-questions: 1
---

# There is no rolling back to a previous build — MVP 1 rolls forward only

Settled in the first ten minutes of the [[wiki/meetings/2026-09-18-transactional-mvp1-capability-cleanup-and-the-monday-deadline.md|Sept 18 2026 8:03 AM call]] (Russian), the fifth and last MVP-1 morning session before the Monday gate. [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] raised it as the one requirement he was certain he could not build, [[wiki/people/andrey-bosik.md|Andrey Bosik]] turned it into a development policy, and [[wiki/people/val-levitan.md|Val Levitan]] — who did not speak on this call but wrote in the meeting chat — ruled it out of MVP 1.

## What the requirement asked for

Chudinov named it before anything else: "**Вариант обновления с откатом на предыдущую какую то прошивку бил**" — an update option that rolls back to some previous firmware build. Asked by [[wiki/people/andrei-klimovich.md|Klimovich]] to put a capability number on it, he shared his screen: "**Это копбилет 122**" — **capability 122**, his own [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The requirement number was self-corrected on air and the correction matters.** He first read it as "**рекламу 13 49**" (requirement 1349), then stopped — "**Я собрал не 13 49**" — and gave "**13 67**", adding "**и мы наверное, на сегодняшнем митинге его убрали в другой капбилити**". So the item is **requirement 1367**, and he believed it had already been moved into a different capability at an earlier session. *(His word is "сегодняшнем" — today's — which cannot be literally right about a meeting still in progress; "yesterday's" is the obvious reading but is **not** what the source says, so it is recorded as spoken and flagged unclear.)* [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]] *(The derived notes carry neither number and neither the capability nor the self-correction.)* [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Why it cannot work — the schema moves with the code

Chudinov's objection is about the database, not the firmware [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**А не для нашего софта. Почему? Потому что у нас есть база данных. Структура база данных во времени меняется. И если мы захотим откатиться на какойто там предыдущий период[,] эта структура не совпадёт… мы можем не подняться.**"

His worked example is the one the corpus should keep, because it is the live cloud migration: a change-set in the new version drops a table — "**Удаляем таблицу волит, потому что мы переезжаем в облако**" — and then the cloud does not work and somebody says go back. "**Но структура б д поменялась. Мы потеряли там, например, все все все данные[,] всё потеряли… Откат назад да[,] подымет[,] но… всё будет пусто. Хотя мы не хотели, чтоб было пусто**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**The right answer, in his words, is to re-cut the version you wanted as a new one:** "**лучший вариант для таких решений[ —] это сделать новую версию, но которая похожа на версию, вот которую мы хотим… достаточно быстро[:] просто поднять нужные комиты и убрать ненужные[;] соответственно, и конфликты с базой не будет, и мы воспроизведём нужный функционал**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

**His second objection is operational and is absent from the notes as a separate point:** nobody is there to supervise such a rollout. "**некому будет за этим следить. Это такую раскатку может делать оператор пульта, а он может не знать… подробностей**" — a control-panel operator could be the one doing it and would not know the details [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Klimovich pushed the real-life case, and it broke both ways

He asked for the field scenario in plain words [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**Мы накатили… апдейт на наши IQ в локациях и выяснилось, что этот бил плохой[,] и нам надо срочно чтото делать[.] Что мы делаем в этой ситуации?**"

Chudinov split the answer in two, and neither half needs a rollback:

- **If the build will not boot at all**, the previous one will not boot either: "**если он буквально не подымается[,] будет просто поднят тот, который был предыдущий[ —] он не подымется**".
- **If something merely displays wrongly** — his example is a fee shown incorrectly to the cashier, "**фи неправильно отображается… для кассер[а]**" — then "**Нам быстрее, наверное, выпустить обновление**", shipping an update is faster.

Klimovich conceded the point without conceding the worry: "**я не буду цепляться за именно откат на предыдущую версию. Это не то, что это мастхэв[;] мы можем убрать это прямо из [MVP] один**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## Bosik turns it into policy — always forward

This is the part that outlives the requirement [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]:

> "**я бы вообще это убрал, потому что, как я уже не раз говорил, есть там разные технологии разработки… можно идти вперёд, можно возвращаться назад. Вот у нас надо придерживаться всегда форвард[ —] оно называется всегда[:] идём вперёд, нашли баг, выпустили следующую версию, накатили, обновили всё, дальше работаем.**"

*(He says "**технологии разработки**" — development technologies. The derived notes render this "development styles"; the substance is the same and the wording is recorded here as spoken.)* [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

## Val closed it from the chat

Val did not speak on this recording. [[wiki/people/irina-shishko.md|Irina Shishko]] read his written message out: "**Вал написал[:] убрать из [MVP] один[,] убрать[,] и продолжим дальше**", and pushed the meeting on — "**давайте двинемся вперед, вот именно**". Klimovich: "**Всё понятно, давайте уберём**". Chudinov: "**Да, правда, это[,] вопросов нет. Продолжаем дальше**" [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]].

## What this does and does not touch

- It **removes the rollback requirement from MVP 1** and establishes roll-forward as the team's stated development policy.
- It does **not** touch the Sept-14 ruling that the gateways update themselves in MVP 1 ([[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]]) — Flex IQ still updates itself; what is gone is the ability to go *back*.
- It does **not** touch the Sept-17 ruling that distributing firmware to the Flex-Ports leaves MVP 1 ([[wiki/decisions/2026-09-17-bosiks-network-list-splits-between-mvp1-and-mvp2.md]]).
- Capability 122 itself survives and is nearly done — Chudinov offered the same morning to run its tests over the weekend and close it if they pass (see [[wiki/decisions/2026-09-18-nothing-is-closed-until-the-conflict-findings-are-worked-back-in.md]], which is why he then could not).

## Open questions

- **Whether a simpler way to handle schema conflicts exists at all.** Chudinov said he would like to work with the idea — "**Можно ли решать конфликты такого рода[ ]какимто… простым способом, чтоб нам не усложнять жизнь?**" — but ruled it straight out of this release: "**на [MVP] точно мы не попадём, потому что достаточно сложно… я даже не знаю, как мы их будем проверять**", the cases being specific and needing verification. Nobody took it forward — [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]

**§15.8:** clear — build and database practice only; no named person's pay, rate or performance judgement appears in either source, and nothing was excluded on that ground. **§15.9:** no identifier, credential or account value appears.

## Sources

- [[raw/Meeting_Transcript_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
- [[raw/Meeting_Notes_Transactional_MVP1_Capability_Cleanup_and_Monday_Deadline-September-18-2026.md]]
