---
type: decision
title: The SAS command logs from the machines are collected on the Flex IQ and not sent to Grafana by default — off unless switched on, read on demand by connecting to the IQ — because sending them would clog the modem channel; Chudinov reviews the weekend's total traffic
date: 2026-10-02
aliases: [SAS command logs collect do not send, SAS logs off by default, логи с машины саскоманд, пускай он лучше не шлёт но собирает, не на порте а на IQ, selective per machine, засорять канал через модем, SAS command logs on the Flex IQ, review total traffic over the weekend, collections door open close]
source-count: 5
status: active
open-commitments: 2
open-questions: 2
---

# The SAS command logs are collected on the Flex IQ and not sent by default

Settled at the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian) between [[wiki/people/pavel.md|Pavel Frolov]] and [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. It shapes the SAS-command logging that Chudinov described on Oct 1 — "мы получим вообще всё, что машина присылает… мы будем логировать все эти команды" ([[wiki/topics/flexpay-business-architecture-payout-devices.md]], Oct 1, 8:02 AM) — and it continues the log-traffic thread of Sept 28 (about 3 GB a month at idle) on [[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]].

## What Chudinov planned

His next item after capability 175: "По следующим планам, тогда у меня идёт к этой же капбилити. Это логи с машины саскоманд… Графа она, наверное будет все это передавать. Ну я посмотрю наверное займусь" — the SAS command logs from the machine, to be passed to Grafana [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. ("к этой же капбилити" — the same capability as the one just named; which one is not clear, and the Oct-1 question whether the SAS logging is its own capability or part of 241 stays open.)

## Pavel's objection

"Дима давай, может быть не будем сейчас передавать логи команд на графану, а сделать это както. Избирательно, то есть чтобы выбрать, для какой машины ты хочешь передавать эти логи? И чтоб их по умолчанию они были выключены, а чтоб мы могли их включить?" Chudinov: "Причина." Pavel: "Ну потому что мы будем очень сильно засорять канал через [—] модем." Chudinov: "Так мы шпинги уберем а там останетсято я моё" (the pings will be removed; what remains is small — reading). Pavel: "Ну не знаю, не знаю" [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]].

## The ruling

Chudinov: "Давай давай сделаем, посмотрим, я всё равно буду делать ревью трафика. Скорее всего, на выходных как раз у нас. Если будет стоять прошивкой, машина там будет работать, поделаем там коллекции открытия закрытия дверей, там ещё чтонибудь посмотрим. Суммарно на весь трафик. Если что, ну будем смотреть, мы же можем собирать, например, но нет не отправлять." Pavel: "Я просто к тому, что ну отключить на [порте] это в принципе да, небольшая задача. Ну то есть просто иметь параметр включено или выключенный." Chudinov: "**Нет, отпускаю пускай это будет пускай это будет лучше не на порте, а на IQ. Пускай он лучше не шлёт, но собирает. То есть, что тогда всегда можешь подключиться и посмотреть.**" Pavel: "**Да да, всё верно.**" Chudinov's reason for the IQ rather than the port: "Такие порт спорт девайс такой далёкий с ним работать сложнее" — the port is a remote device, harder to work with [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]].

In one line: **the Flex IQ collects the SAS command logs and does not send them; sending is off by default and can be switched on selectively; anyone who needs them connects to the IQ and reads them there.** The derived notes record the same ruling and the same two names [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]].

## Where it sits

- It is the "collect first, notify or display second" split of Sept 17 applied to a new log stream — and the first time the second half is explicitly turned off by default ([[wiki/decisions/2026-09-17-signal-quality-in-mvp1-means-remote-visibility-not-a-screen.md]]).
- The purpose of the logs is unchanged from Oct 1: statistics on which SAS commands other makers' machines send, to know which to implement ([[wiki/topics/flexpay-business-architecture-payout-devices.md]], Oct 1, 8:02 AM).
- The modem-channel worry is the same one behind the Sept-28 "3 GB a month" measurement and Pavel's Oct-1 "трафик… должен быть копеечный" (link is context, not a citation).

## Update, Oct 5 2026 — the traffic review has begun: polling and "handpay 51" look noisy; Kharetski or Ivan to say whether that is normal

At the [[wiki/meetings/2026-10-05-daily-standup-autotest-stand-debate-and-jira-reopen-rules.md|Oct-5 Minsk stand-up]] (Russian) [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Вот основное садиться, смотреть, что там машина по сассу шлёт. Вот эти вот [поединг] 51 этот хэндпэй. Чтото он там сильно мусорит, надо разбираться нормально, ненормально женя скажет ваня, я не знаю." [[wiki/people/pavel.md|Pavel]]: "Ну на 1 взгляд выглядит, что ненормально." ("51" sits between "polling" and "handpay"; the derived notes read "polling, handpay 51" [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].) Whether the total weekend traffic was measured, and whether the collect-not-send build exists, was not said [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]].

## Open contradictions

- **Are the SAS command logs sent to Grafana or not?** Oct 2 2026 (stand-up): the ruling above — the Flex IQ collects them and does not send by default — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]. Oct 5 2026 (8:01 AM call): [[wiki/people/dmitri-chudinov.md|Chudinov]] said that over the weekend the function was built and "теперь получаем все [SAS] команды с машины на порт на IQ и вклады в графа"; to [[wiki/people/pavel.md|Pavel]]'s "логи саса… собираются на флекс айтю и дальше они както отправляются кудато в графану или" he answered "Да да да, в графана" — [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]. Not resolved here: it may be the test set-up with sending switched on, or the rule not yet built. Recorded, not resolved.

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — build the SAS-command logging so the Flex IQ collects and does not send, with sending off by default and switchable per machine — due unspecified (his next item after 175) — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — review the total traffic over the weekend of Oct 3–4 2026 with the machine running on the firmware: collections, door open / close, "там ещё чтонибудь посмотрим" — due Oct 5 2026 (after the weekend) — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]] — *Oct 5 2026: in progress — he is looking at what the machine sends over SAS; polling and "handpay 51" look noisy; no total was given* — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]

## Open questions

- Is the polling / "handpay 51" traffic the machine sends over SAS normal or not? Pavel: at first sight not; Chudinov: "женя скажет ваня" — [[wiki/people/evgeny-kharetski.md|Kharetski]] or [[wiki/people/ivan.md|Ivan]] to judge, nobody assigned — [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- Is the SAS-command logging its own capability or part of 241? Chudinov said "к этой же капбилити" without a number — the Oct-1 question on the FlexPay topic page stays open — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]

**§15.8:** clear — device logging and traffic only. **§15 #9:** none.

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Autotest_Stand_Debate_and_Jira_Reopen_Rules-October-5-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Port_Screens_Unclaimed_Money_and_Printer_Models-October-5-2026.md]]
