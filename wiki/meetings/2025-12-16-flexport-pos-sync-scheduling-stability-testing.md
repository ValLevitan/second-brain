---
type: meeting
title: FlexPort / FlexPOS sync + scheduling — long-term stability testing, the cancel command tested, stack-ranking into the holidays (Dec 16 2025)
date: 2025-12-16
aliases: [Flex-Port Flex-POS sync and scheduling, FlexPort POS sync Dec 16, long-term stability testing, HFM 346, HFM 339, HFM 340, HFM 353, HFM 278, HFM 258, HFM 268]
source-count: 1
open-commitments: 4
---

# FlexPort / FlexPOS sync + scheduling — long-term stability testing, the cancel command tested, stack-ranking into the holidays (Dec 16 2025)

**Date:** 2025-12-16 (recording header 12:00PM; base name `Flex-Port, Flex-POS sync and scheduling-20251216_070053`) · **Duration:** 50m 13s · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/eugine-yavorski.md|Eugine Yavorski]], [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (Genadi referenced for payments). Russian.

Weekly FlexPort/FlexPOS sync and scheduling — the last sync before the holiday break. Continues the [[wiki/meetings/2025-12-08-flexport-smib-pos-sync-cancel-command-user-screens.md|Dec-8 sync]]. Substance folds into [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Dec-16).

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and grepped/read the whole wiki: `raw/Flex-Port, Flex-POS sync and scheduling.md` is cited on no content page. It is the **Dec-16 12:00PM** Val/Pavel/Yavorski/Alekseev sync — separate in date and content from Dec-1/Dec-8 (this one shows the cancel command tested at home and about to be verified on the floor, HFM-340 branched-off/closed, the long-term stability test now running all four machines, and Val's stack-ranking/holiday-schedule push). Confirmed new.

Durable points (single source):

- **Long-term stability testing (HFM-346) now running.** Yavorski has **finished docking each machine individually** (last was a **Fusion 5**) and now runs them **continuously** — each machine talks over **two interfaces at once**: the **WSS** link to the kiosk and the **DCC3 (protocol 1030)** link to the gaming machine — checking it never hangs, visiting once or twice a day to print/read a ticket. **Fusion 5 ran a week continuously with no issue**; he now wants all **4 machines** on the floor running the same way for ~2–3 weeks. Pavel asked to also **log FlexPort self-reboots** (it reboots itself on a hang); Yavorski to fold reboot-fact logging into the log task (**HFM-278**, export logs to FlexPay). Kept a test-type item under FM-191 so it doesn't distort the schedule. [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- **HFM-339 cancel command tested; HFM-340 closed.** Yavorski **added the new "cancel"/"cancel-transaction" command** (the one Dima built for him) and tested it at home; he wants to verify it on the **production floor** and will close HFM-339 ~the next day. **HFM-340** = he **separated the old cashout implementation into its own feature-flagged branch** (so it doesn't interfere with the coming changes and can be reverted easily) — done, **closed** on the call. [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- **This-week plan / stack rank (Yavorski).** After 339: **HFM-353** (multi-denomination chain — debug on one bill, then the denomination chain) + **HFM-278** logs this week; then **HFM-351** user screens (the 3 screens re-confirmed: progress / remaining-on-ticket / limit-reached); **HFM-352** reporting (under FM-191); **HFM-344** ($0-cashout error fix); **HFM-256** (cashout negative scenario — needs Dima's command but Yavorski will code his own side, aim before New Year); **HFM-342** (fix the missing box-full message thrown from the validator to the machine, ~2–3 days, next week). The **firmware update** (~1–1.5 weeks, a task they keep pushing) deferred to **~Dec 29**. Yavorski estimates his backlog is **~3 weeks** of work. [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- **Board / validator work (Alekseev).** **HFM-258** (integrate 2 validators with the machine) in progress, ~today/tomorrow; then **HFM-268** (Windows tool for Flex Sport — reads validator statistics from a log file). Three dependent tasks **186 / 188 / 189** wait on 268 (they're written but need 268 to read/decode/verify the data). Alekseev wants **new boards** on the 4 machines. Pavel floated giving Alekseev a **Pyramid-printer investigation** ("Windows reaches them faster than us"); **Val declined — "we're not ready for that."** [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- **Val's process frustration — stack-ranking and testability.** Val repeatedly lost the thread of the Jira numbers and demanded a **stack-rank** (in-progress at the top). Two durable observations: (1) **not one task carries acceptance criteria / exceptions**, so QA cannot test any of it — the features have grown "mega-large" and won't be testable without acceptance criteria at the feature level (Pavel conceded the current criteria are "extremely little"); (2) task **268** was linked to a **year-old task**, making Jira show a task "lasting a year" — Val: a task can't last a year, it was mis-recorded; re-date or re-open cleanly. [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- **Holiday schedule.** Break starts after Monday. **Both engineers plan to work through the holidays** (Yavorski: "I plan to work the whole time"; Alekseev has spare weekend time). Firmware left for **Dec 29**; next meeting **after Jan 5**. Val closed by asking where all the code is stored — answer: **Git**. [[raw/Flex-Port, Flex-POS sync and scheduling.md]]

## Open commitments

- [ ] Eugine Yavorski — verify the HFM-339 cancel command on the production floor and close it; then HFM-353 (multi-denomination chain) + HFM-278 (logs) this week; HFM-351 screens, HFM-352 reporting, HFM-344, HFM-256, HFM-342 next; do the firmware update ~Dec 29 — due through year-end (~3 weeks of backlog) — [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- [ ] Evgeniy Alekseev — finish HFM-258 (2-validator integration) ~today/tomorrow, then HFM-268 (Windows/Flex Sport log tool) which unblocks 186/188/189; put new boards on the 4 machines; add task descriptions/docs — due this week — [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- [ ] Pavel Frolov — re-plan the mis-dated/year-old-linked tasks (esp. 268) cleanly, and push acceptance criteria at the feature level so QA can test — due unspecified — [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
- [ ] Val Levitan / team — reconvene after Jan 5; hold the Pyramid-printer investigation until JVL is ready — due ~Jan 5 — [[raw/Flex-Port, Flex-POS sync and scheduling.md]]

**§15.8:** clear — only device/board, protocol and machine-config content. No named-person compensation; figures are ticket/credit values and task-effort estimates.

**Same-name note (§4).** "Евгений Алексеев / Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] (embedded + board work, Genadi orbit); "Евгений яворский" = [[wiki/people/eugine-yavorski.md|Eugine Yavorski]] (FlexPort/FlexPay integration software); "Дима" (built the cancel command; loaded elsewhere) = [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (FlexPay back-end/Java). [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/genadi-peari.md|Genadi Peari]] as usual. Closing "Иван до свидания" is a passing sign-off (Ivan the tester per prior sessions — no page, left unlinked); garbled proper nouns ("Сергея" the network helper, "Сижу ем"/Fusion machine names) left unresolved, not force-matched.

## Sources

- [[raw/Flex-Port, Flex-POS sync and scheduling.md]]
