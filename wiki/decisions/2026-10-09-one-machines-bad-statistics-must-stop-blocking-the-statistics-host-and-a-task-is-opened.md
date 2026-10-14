---
type: decision
title: One machine's bad statistics must stop blocking statistics for every machine — a task is opened for it; Pavel would drop the bad packet and send an alert instead of stopping all processing; no fix chosen yet, and the old accounting server is expected to live about another year
date: 2026-10-09
aliases: [statistics host blocked, блокирует всем статистику, machine from the Minsk office spammed, заспамили, clean by hand, вручную чистить, drop the bad packet, пакет лучше выбросить, push message for unparsed data, accounting server one more year, аккаунтин сервер, ещё год будет жить, registered test machine, unregistered machines skipped]
source-count: 2
status: active
open-commitments: 1
open-questions: 2
---

# One machine's bad statistics must stop blocking everyone

**Set** at the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian) by [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), with [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") on the server side.

## The problem

- **Why now.** Chudinov: machines are now leaving with modems — Pavel: "В Джорджия с последним софтом джорджии да?" — "будут слать статистику" [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **What happened again.** Chudinov: "у нас сейчас опять машина, у которой с минского офиса. Заспамили. Какимито данными короче оно блокирует всем статистику. Сейчас никто не шлёт на это надо отвлекаться и вручную чистить." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **Why a machine sends bad data.** The machine is registered, but often "либо игры на прод ещё не добавлены либо [машина] на регистрации не совпал по софтам, потому что там инсталляцию сделали не ту" — "вариантов много" [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## The positions

- **Tsymanov — what exists.** A mechanism already skips statistics from machines not registered in the system. But how do we tell that a registered machine is a test one? A spot fix "не избавит от всех проблем" — later a full rework comes anyway [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Pavel — drop the packet.** "если пришел в пакете там кусок данных, относящийся к какойто машине, и он не даёт… Закончить процедуру для всех остальных, то такой пакет лучше выбросить, чем… останавливать всю обработку." Also "какоето пушсообщение… что вот по такойто машине данные не смогли, распарсятся" [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Tsymanov — the chain is not simple.** If the server returns an error, the data is marked unsent and sent again: "цепочка не такая простая" [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].
- **Chudinov — the goal.** "надо будет просто думать, что сделать, чтоб вручную больше это не заниматься." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

## What was settled

Pavel: "значит нам тогда нужна будет задача." No owner and no method were named [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]. The notes: "No solution chosen" [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

**Why it is worth real work.** Chudinov: by what he has heard, the server will not die soon — "ещё год будет жить". Pavel, "для записи": "не помрёт аккаунтин сервер" — the accounting server, not a person [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Open commitments

- [ ] Unassigned (Pavel asked for it) — create a task so one machine's bad statistics no longer block the host for everyone — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

## Open questions

- How should the host stop one machine's bad data from blocking everyone — drop the packet and alert (Pavel), or another way, given the resend chain (Tsymanov)? — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- How can the server tell that a registered machine is a test machine? (Tsymanov) — [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
