---
type: decision
title: The Flex-Port accepts meter-pulse periods from 30 to 150 ms and resets the count after 2 seconds of silence, with no per-machine setting for now (a Banilla was found pulsing at 125 ms); a repeat cash-out pressed before the Flex-Port timeout ends is added to the pending amount and the timeout restarts (Oct 27 2026)
date: 2026-10-27
aliases: [pulse band 30 to 150 ms, полоса от 30 до 70, 125 ms Banilla, pulse statistics command, 2 seconds of silence resets the count, repeat cash-out, multi cash-out, второй кэшаут, add to the pending cash-out, сбросить счетчик вывода, game-start interrogate resets the timeout]
source-count: 4
status: active
open-commitments: 3
open-questions: 2
---

# The Flex-Port counts meter pulses from 30 to 150 ms; a repeat cash-out inside the timeout joins the pending one

Settled at the [[wiki/meetings/2026-10-27-daily-standup-cashout-merging-and-remote-updates.md|Oct-27 Minsk stand-up]] (Russian; Val absent) by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/alexander-biratka.md|Alexander Biratka]] agreeing [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]. Both rules belong to the bill-validator-and-pulses mode for other makers' machines — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]].

## Why the pulse band moved

- **A statistics command.** Pavel closed PORT-127 and PORT-165 and one more task, "20/173" (heard): an extra command that shows pulse statistics. "После этого комита волшебным образом. Банила заработала." [[wiki/people/irina-shishko.md|Irina]]: "Там вроде они все заработали только с вопросами." [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- **What it showed.** The Banilla's meters run "Периодом не 100 миллисекунд, а 125 миллисекунд". The accept band was "от 30 по моему до 70" ms, so some pulses may have been rejected at the edge [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].
- **The new rule.** Pavel: "От 30 миллисекунд период до там 150… время тишины там 2 секунды, всё 2 секунды ничего нет, значит, мы сбрасываем начало. Счёта." He reworks the logic that day [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].
- **No setting per machine.** Biratka asked who would configure this, and at what stage, for a given machine. Pavel: the duration is not configured; "пока никаких конфигурационных вариантов нам не требуется" — "Думаю нет." Below 30 ms is unlikely, since meters cannot act that fast; if a machine uses a longer period, "мы будем видеть теперь у нас отладка есть" [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].

## The repeat cash-out

- **The symptom.** Irina: on some machines part of a cash-out goes through normally and part shows as a repeat cash-out — "они выводят $20, но сначала первые 12 выводятся как нормальные а… 8 они как будто бы 2 раз нажали кэшаут и они не востребованные" (unclaimed). Pavel: not the pulse timing — probably the machine's settings; later he said the machine seemed to stall, the meters stopped for about 2 seconds and then went on clicking [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].
- **Pavel's rule** (he started on it the night before). A player cashes out $5; the port shows the amount; he still has money but plays three more hands; if he presses cash-out again "у него таймаут не закончился на флекспорте… эти $15 надо прибавить к тем 5" and the cash-out counter is reset. If the timeout has already ended, it is a separate cash-out. Irina gave the timeout as "30 секунд" [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].
- **Resetting the timeout.** [[wiki/people/evgeny-kharetski.md|Kharetski]] (hard to hear) proposed resetting it on game start. Biratka: in BV mode we do not get that. Pavel: in BV mode the machine does an interrogate when a game starts; "мы этот сигнал ловим… Мы можем по этому событию сбрасывать счётчик" until the player finishes and cashes out the rest [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]].
- **Biratka's doubt, then yes.** He first preferred a separate cash-out. Pavel: then the money goes to unclaimed. Biratka: "транзакция же еще не началась на на порт"; Pavel: "Нет, транзакция Спаса флекс айкью еще не началась" ("Спаса" garbled; the notes read it as the Flex IQ transaction). Biratka: "тогда выглядит в принципе достаточно логично… вроде как рабочий." Pavel: "Окей, хорошо." [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]

In one line: **the Flex-Port takes pulse periods of 30–150 ms, 2 seconds of silence ends a count, nothing is set per machine for now; and a second cash-out inside the Flex-Port timeout is added to the first, with the timeout restarting, because the Flex IQ transaction has not yet begun.**

## How it sits against earlier items

- It refines the Oct-20 pulses mode and the Oct-22 cash-out faults on the borrowed machines — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]].
- It keeps money out of unclaimed, the destination set for a timed-out cash-out in [[wiki/decisions/2026-09-15-a-timeout-sends-the-money-to-unclaimed-and-the-player-never-loses-it.md]] (link is context; that the 30-second timeout is the same one is **inference**).

## Update, Oct 28 2026 — does the multi cash-out add up on SAS?

At the [[wiki/meetings/2026-10-28-daily-standup-flex-port-firmware-delivery-and-reopening-completed-features.md|Oct-28 Minsk stand-up]] [[wiki/people/alexei-khamin.md|Khamin]] asked whether the multi cash-out now being built affects BV mode on SAS. Pavel: two cash-outs inside the timeout can happen there too; in SAS the money should add up onto one ticket, "Но есть подозрения, что это сейчас не будет работать". Irina will check it first [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — widen the pulse logic to a 30–150 ms period with a 2-second silence reset — due Oct 27 2026 — [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — build the repeat cash-out: add the new amount to the pending one and restart the timeout — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [ ] [[wiki/people/irina-shishko.md|Irina Shishko]] — check whether two cash-outs inside the timeout add up to one ticket in BV mode on SAS — due Oct 28 2026 — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]

## Open questions

- What causes the split cash-outs (part normal, part unclaimed) on some machines? Pavel suspects machine settings or a 2-second stall in the meters — [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- Do two cash-outs inside the timeout add up to one ticket on SAS today? Pavel suspects not — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]

**§15.8:** clear — the dollar figures are Pavel's and Irina's play examples. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
