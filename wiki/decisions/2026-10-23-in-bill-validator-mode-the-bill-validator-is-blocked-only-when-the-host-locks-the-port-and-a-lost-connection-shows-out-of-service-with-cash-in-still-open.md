---
type: decision
title: In bill-validator mode the Flex-Port blocks the machine's bill validator only when the Flex IQ locks the port ("locked by host"); if the connection is simply lost, the screen shows "out of service" and the bill validator stays open (Oct 23 2026)
date: 2026-10-23
aliases: [BV lockout rule, bill validator lockout, locked by host, локт байхост, out of service does not block the bill validator, cash-in disabled, кэшен дизейбл, PORT-162, PORT-163, PORT-164, BV mode messages, lost connection keeps the bill acceptor open]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# In bill-validator mode the bill validator is blocked only when the host locks the port

Settled at the [[wiki/meetings/2026-10-23-daily-standup-bill-validator-lockout-and-atlanta-port-test.md|Oct 23 2026 Minsk stand-up]] (Russian; Val absent). [[wiki/people/irina-shishko.md|Irina Shishko]] read the rule from the requirements during the meeting and [[wiki/people/pavel.md|Pavel Frolov]] accepted it [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]. The notes list it as a decision by Irina, accepted by Pavel, with Biratka's broader rule set aside [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## The question

- **Biratka's work.** [[wiki/people/alexander-biratka.md|Alexander Biratka]] works on PORT-164, 162 and 163 — the messages for working through the bill validator (BV). The port now shows "кэшен дизейбл" (cash-in disabled) when, for example, the machine door is opened. His question: when does the "out of service" screen still appear? [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- **Pavel: "out of service" is for the port's own faults.** Errors of the Flex-Port's own devices, "например, сканер", and problems with the connection to Flex IQ or Flex Pay [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].
- **The port sees little of the machine.** Pavel: "к машине у нас как раз биви только есть. Мы можем только статус биви прочитать." Biratka: the port has only the enable and disable signal on that wire [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].
- **Blocking the acceptor is the only lever.** Pavel: in BV mode, to block the machine "мы можем только заблокировать, ну белаксектор… Машина продолжит играть, как и требовалось" [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].
- **Two cases.** Pavel: when the IQ sends the port a lock command, the screen says "аутов сервис" on top and "локт байхост" (locked by host) in small letters, and the bill acceptor is blocked. But "если у нас просто пропал, пропала связь с… Флекс ай кю. Надо ли нам в таком случае белоксектор блокировать?" [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]

## The arguments

- **Biratka: block on any port problem.** "если какието проблемы с портом, то мы должны блокировать… Валлидатор. Иначе нам всунут деньгу примут её, а мы её не обработаем." [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- **Pavel: not every "out of service".** A bill pushed in still goes into the machine, but "все, что связанное с его летами, не будет работать" (read as the wallets — **inference**). "Я не утверждаю, я как бы призываю подумать. Мне кажется, что не каждый аутов сервис это равно блокировка билаксептора." He suggested asking "Андрею" (Klimovich, the requirements owner for the transactional system, by context — **inference**). He also recalled a possible earlier answer the other way — block, "чтобы никто не пытался обойти работу флекса кью" — but was not sure [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].

## The ruling (from the requirements)

- **Irina, after checking with Claude during the meeting:** "требования только блокировать билвалидатор, если машина заблокирована, ну порт заблокирован со стороны там айкью в других случаях нету. В требованиях такого условия и бил валидатор остаётся доступной." And: "бил валидатор доступен деньги можно вбрасывать в других случаях, если просто связь потеряна. И аутов сервис" [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].
- **Pavel:** "Хорошо понятно." Irina has new autotests for the bill validator [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].
- Whether the question still went to Klimovich is not said.

## A case to test

- Pavel: a port blocked because the location is blocked must be checked in an autotest — "То у нас должен девизаблокироваться". Khamin checked it about three weeks ago. What exactly must happen is **unclear**: the notes read it as "the device must unblock"; the words could also mean the BV must be blocked [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]].

## How it sits against earlier items

- **Builds on the Oct-20 bill-validator mode** — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]]. On Oct 22 Pavel asked that the "out of service" shown on cash-out become a plain "cash-in disabled" notice; Biratka's Oct-23 work is that change (see the Oct-23 update there).
- **Fits the Sept-24 rule** that a Flex-Port with no gateway link goes out of service — [[wiki/decisions/2026-09-24-a-flex-port-that-dies-holding-money-sends-it-to-unclaimed-and-one-without-a-gateway-goes-out-of-service.md]]. The Oct-23 ruling adds what happens to the bill validator in that state in BV mode — **evolution**, not a contradiction.

## Open commitments

- [ ] Owner not named — add the autotest for a port blocked because its location is blocked — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]

## Open questions

- When a port is blocked because its location is blocked, must the bill validator be blocked or released? The spoken line is garbled — [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]

**§15.8:** clear. **§15 #9:** none; the numbers are Jira keys.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Bill_Validator_Lockout_and_Atlanta_Port_Test-October-23-2026.md]]
