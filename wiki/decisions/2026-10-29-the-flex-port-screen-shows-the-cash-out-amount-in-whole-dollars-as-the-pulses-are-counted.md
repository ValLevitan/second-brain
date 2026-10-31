---
type: decision
title: The Flex-Port screen shows the cash-out amount while the meter pulses are still being counted, so the player sees money moving in real time; it counts in whole dollars (one pulse is $1), not in steps of $5; the counted part stays on the port if the machine goes off (requirement 1960, heard — Pavel, Biratka agreeing, Oct 29 2026)
date: 2026-10-29
aliases: [cash-out progress screen, кошаут прогресс скрин, requirement 1960, регламент 19 60, real-time cash-out amount, whole dollars on the port screen, кратно долларов, one pulse is one dollar, каждый клик это $1]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# The Flex-Port screen shows the cash-out amount in whole dollars as the pulses are counted (Oct 29 2026)

Settled at the [[wiki/meetings/2026-10-29-daily-standup-cash-out-progress-screen-and-pulse-mode-installs.md|Oct-29 Minsk stand-up]] (Russian; Val absent) by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/alexander-biratka.md|Alexander Biratka]] agreeing [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]. It belongs to the bill-validator-and-pulses mode for other makers' machines — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]].

## Where it came from

- **A new requirement.** Pavel brought up the "кошаут прогресс скрин". He and "Андрей" (the notes: Andrei Klimovich — **inference**) talked the day before and saw that "как только пульсы начали считаться уже выводить на экран порта, какая сумма вывелась", so the player "Видел в реал тайме, что деньги переводятся, а не ждал несколько секунд, прежде чем сумма появилась на экране." Pavel: "Будем такое делать." [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- **Not part of requirement 1926.** Biratka asked whether it is inside "регларименс 19, 26" or extra. Pavel: "это вот весь регламент 19 60 новый создан это по результатам вчерашних разговоров" — a new requirement, 1960 (heard). He called it "не сложная для порта" [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]. Pavel also asked why it had been put on "иру" (Irina) — this led to the question of who owns agent-made requirements; see [[wiki/decisions/2026-10-28-a-story-under-a-completed-feature-does-not-reopen-it-automatically-and-the-storys-creator-moves-the-feature-or-picks-another-parent.md]] (Oct-29 update).

## Biratka's question — what if the machine goes off?

- Biratka: we show the player 5, 10, 15; if the machine is switched off when 10 have passed, the player says "я видел у меня 10 перевелось где мои 10", but in fact nothing was transferred [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]].
- Pavel: "они перевозятся на порт они не на тикет переводятся." Biratka: then if the machine goes off, "реально на проте останется 10 баксов, например, из 20"; Pavel: "Да." Biratka: "теоретически да можно такое сделать." [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]

## Whole dollars, not steps of $5

- Pavel first thought fractions make no sense and perhaps steps of $5. Biratka: "может по 5 и считаем наверное." [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- Pavel: "каждый клик это $1, то есть теоретически там может быть $6 и 7." On some machines (he thought the Banilla — "у ванил или у кого") a cash-out showed $12 on the screen. The old port logic, after a timeout "В районе там 2 секунд", took it that all the money was out and skipped the later clicks, "или точнее, добавлял их в анкле" ("анкле" read as unclaimed — **inference**). "на последних белдах" the port adds them up — "к этим $12 добавит те, которые там 8 довыводятся" — even after a timeout [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]].
- So the screen counts in whole dollars. Biratka: "Однократно долларом. Ну да." Pavel: then at least it is clear what is happening — $12 out, a delay, then the rest [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]].

In one line: **while the meter pulses are being counted, the Flex-Port screen shows the amount so far, in whole dollars; the counted money is on the port, so a machine switched off mid-way leaves the counted part there.**

## How it sits against earlier items

- It builds on the pulse rules and the repeat cash-out of Oct 27, now in the latest port builds — [[wiki/decisions/2026-10-27-flex-port-counts-meter-pulses-from-30-to-150-ms-and-a-repeat-cash-out-inside-the-timeout-joins-the-pending-one.md]] (Oct-29 update).
- The Oct-22 cash-out screen faults (amount screens, timing) were given to Biratka — [[wiki/decisions/2026-10-20-machines-without-working-aft-connect-by-bill-validator-emulation-and-pulses-in-mvp1-and-the-port-mode-is-set-per-port.md]]. Who builds the progress screen was not said.

**§15.8:** clear — the dollar figures are play examples. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Cash-Out_Progress_Screen_and_Pulse_Mode_Installs-October-29-2026.md]]
