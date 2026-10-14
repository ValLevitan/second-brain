---
type: decision
title: Test work to October 15 follows 80/20 — close the main functions first and leave rare and complex tests for the last day; tests tied to the port, the machine and the Flex IQ come before cloud tests, because servers can be deployed at any time
date: 2026-10-09
aliases: [80 20 tests, принцип 80 20, main functions first, rare and complex last, port machine IQ first, порт машина IQ, servers can deploy any time, сервера можно деплоить в любой момент, tests 80 percent by the 15th, TIN-56 cloud, capability 122]
source-count: 3
status: active
open-commitments: 0
open-questions: 0
---

# Tests to October 15: 80/20, and device tests before cloud tests

**Set** by [[wiki/people/pavel.md|Pavel Frolov]], with [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]]'s refinement, at the [[wiki/meetings/2026-10-09-daily-standup-weekend-service-rollout-and-stats-blocking.md|Oct-9 Minsk stand-up]] (Russian).

## What was said

- **Where the tests stand.** Pavel: "В целом выглядит так, что тесты к 15 числу по большому закроются." [[wiki/people/irina-shishko.md|Irina]]: "Ну процентов. На 80 может быть закроется, потому что мне кажется, сейчас побыстрее пойдёт." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **Some are hard.** [[wiki/people/vladimir-samusenko.md|Vladimir]]: some fly through, but TIN-56 needs the cloud — a test about "Доставку обновлений на машину и там вообще всё непонятно… дай бог, если половину теста получится взять." Irina: then it is not MVP 1 — "хотя он на кап 122. Но ничего облачное мы не делали." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]] (The notes read "стинг 56" as TIN-56 [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].)
- **The rule.** Pavel: "80 20. То есть пытаемся сделать. Максимально закрыть функциональность, всё, какоето там редкое и сложное, пока она на последнее. Последний день." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **Device tests first.** Chudinov: "я бы предложил вариант закрыть больше вариантов, которые связаны порт машина IQ. Потому что сервера можно депловить в любой момент… А с девайсами сложнее." Pavel: "Да." — "Поэтому в общемто клауды и откладываются." [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- **The cost, named.** [[wiki/people/alexei-khamin.md|Khamin]]: then there are no automatic runs — "нет, амуляторов соответственно нет. Автоматом, гдето разворачивание окружения." Pavel: that is the next meeting — how to simulate cloud services, "Особенно платежные" ([[wiki/decisions/2026-10-05-the-payment-hub-autotest-stand-is-not-mvp1-and-a-separate-meeting-with-andrei-designs-it.md]], Oct-9 update) [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]].

## Where it sits

This is the test-side version of the date in [[wiki/decisions/2026-09-28-october-15-replaces-october-1-as-the-mvp1-date.md]]. The notes record it as a decision of Pavel and Chudinov [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]. More on the test plan: [[wiki/topics/test-automation-strategy.md]] (Oct 9).

**§15.8:** clear. **§15 #9:** none; TIN-56 and capability 122 are work references.

## Update, Oct 12 2026 — one autotest a day each for Ivan and Vladimir, to fit by the 15th; remote Flex IQ firmware tests last

At the [[wiki/meetings/2026-10-12-daily-standup-flexport-emulator-and-jira-auto-progress-rule.md|Oct-12 Minsk stand-up]] (Russian) [[wiki/people/irina-shishko.md|Irina]] split the autotests between Ivan and Vladimir: "Сейчас стоит один день один автотест… просто чтобы вписать до 15, чем быстрее будете брать, тем лучше." A test that touches the cloud goes aside at once; one that can only be checked by hand gets a comment and goes aside. Pavel: the Flex IQ firmware-update tests were put off "до самой самое последнее"; Irina said updates are by hand for now, and Pavel made clear he meant the remote update "для флекса ай кью не для порта" [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]. This applies the 80/20 rule above (**evolution**).

## Sources
- [[raw/Meeting_Transcript_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Weekend_Service_Rollout_and_Stats_Blocking-October-9-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_FlexPort_Emulator_and_Jira_Auto_Progress_Rule-October-12-2026.md]]
