---
type: decision
title: The street cabinet's board is the RK3576, not the RK3568 — the 3568 renders badly on a vertical screen
date: 2026-09-14
aliases: [RK3576, RK3568 vertical screen, 3576 target board, аркеи на горизонтальном телевизоре, именно 35 68, Touch Intelligent, RK3576 shipment to Minsk, 8 gigabytes, тач интеллигент, два борта]
source-count: 7
status: active
open-commitments: 3
open-questions: 2
---

# The street cabinet's board is the RK3576, not the RK3568

Settled at the [[wiki/meetings/2026-09-14-hardware-priorities-tito-case-and-street-cabinet.md|Sept 14 2026 12:04 PM call]] (Russian) between [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/pavel.md|Pavel Frolov]]. Part of the [[wiki/topics/low-cost-street-machine.md|low-cost street-machine]] thread.

## The defect that forced it

[[wiki/people/val-levitan.md|Val]] raised it from memory and did not claim the source: "**Мы обнаружили, что аркеи[на] горизонтальном телевизоре работает хорошо на вертикальном плохо**" — we found that the RK works well on a horizontal screen and badly on a vertical one. He added twice that he could not remember who told him: "**Я не помню кто мне сказал я по моему Павел**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

[[wiki/people/pavel.md|Pavel]] confirmed it and narrowed it to one part: "**что то такое есть и это про это китайцы даже в своей документации гдето написали. Но это именно 35 68**" — there is something like that, the Chinese even wrote about it somewhere in their own documentation, and it is specifically the 3568 [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The transcript renders the board only as "35 68" / "аркеи"; the corpus carries it as the Rockchip **RK3568**, the board the team has used since [[wiki/topics/low-cost-street-machine.md|June 2026]]. No document, page or section of the Chinese documentation is named, and none is asserted. The street cabinet is a **vertical single-screen** machine, which is why a vertical-orientation defect is disqualifying.)*

## The ruling

[[wiki/people/genadi-peari.md|Genadi]]: "**Поэтому мы тебе высылаем 35, 76… Который чуть дороже там $15 из 8 гигабайтами и это как раз таргет. Это вот эта машина**" — that is why we are sending you the 3576; a bit more expensive, $15, with 8 gigabytes, and it is exactly the target — this machine. [[wiki/people/pavel.md|Pavel]] accepted it: "**Ну да, будем пробовать именно этот вариант**" [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Val tied it to the cabinet in the same breath: the street machine "**будет делаться на новое платформы**" — will be built on the new platform — and asked Pavel to verify the vertical screen on it [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

*(The source does not say **$15 more than what**; in context it reads as "$15 more than the 3568" — an **inference**, not stated. "8 гигабайтами" is the RAM size as spoken.)*

## What it displaces, and the tension it leaves open

This narrows rather than repeats the earlier board positions on this machine (four in the corpus, counting the Aug-12 antecedent added below) — see the timeline on [[wiki/topics/low-cost-street-machine.md]]:

- **June 9 2026:** the team had RK3568 boards but only at **2 GB**, too little; Pavel and Genadi favoured the **RK3588**, with the RK3576 named as the in-between option [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]].
- **July 29 2026:** measured results put one game plus system plus LGS at ~**5 GB** and each further game at ~**1 GB**, so an **8 GB board covers about two games**, and the decision was to **order an RK3588 with 16 GB** [[raw/Meeting_Notes_RK3588_Game_Performance_Findings-July-29-2026.md]].
- **August 12 2026 (antecedent, back-filled):** Val and Genadi judged a ~$250–290 16 GB board not worth it, Genadi called the **RK3576 with 8 GB** (sample ~$150) "more than enough" for a street machine, and Val ruled "**3576 с 8 гигабайтами и это будем тестировать… давайте мы возьмем два борта**" — test the RK3576 8 GB, take two boards. So the Sept-14 choice was already made, as a test, on Aug-12; the Sept-14 call adds the vertical-screen reason for leaving the 3568 [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]] [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]].
- **September 14 2026 (current):** the target for this machine is the **RK3576 with 8 GB**.

**The tension is real and nobody named it on the call.** The July measurement says 8 GB is about two games; the September choice is an 8 GB board, and Pavel's own next step is to launch a game on it and *then* judge memory. These are statements about different dates, so this page records the September position as current and the July one as what it displaced — it is **not** filed as a contradiction — and the arithmetic is still not reconciled in numbers. The nearest the corpus comes is Aug-12: Genadi proposed limiting the games' size a little to fit 8 GB, with six games as the count spoken, and said he had told "Pasha" this was not a problem [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]. Flagged as an **observation**, not a finding.

## What Pavel has to do before it is usable

"**Ну мы когда получим 35, 76 мы вопервых должны запустить хотя бы одну игру… На текущих версиях мы ни разу не доходили до этого, чтобы игру запустить и сделаем уже тогда заключение. Ну сколько мы памяти съедаем в этом подходе**" — first get at least one game running, because on the current versions they have never once got that far, then draw a conclusion about memory use [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Two pieces of work stand between the board and a running game, both named by Pavel: "**у нас открыт вопрос SDK для 76 платы его надо будет ну переделывать. Этого ещё нет**" — the SDK for the 76 board is an open question and has to be reworked, and it does not exist yet; and "**в остальном там уже много чего заготовок есть это всё надо будет просто объединить и сделать, как я говорил, этот интеграционный репозиторий, в котором это всё собирается**" — otherwise there are plenty of pieces, which need combining into the integration repository he has described before. See [[wiki/topics/nova-platform-architecture.md]] [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

## Getting the boards to Minsk

Val: "**Значит, нам нужно срочно нажать на поставку RK 35 76 Минск. И это кто это контролирует? Это миша контролирует. Миша перельман**" — we need to push the RK3576 delivery to Minsk urgently, and Val named [[wiki/people/mikhail-perelman.md|Misha Perelman]] as the person who controls it [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]].

Genadi did not know where it stood — "**я не знаю статус… Этот инвойс там он вышел пост этот я не знаю. Но мы мы пустили это вперёд**" — then looked the order up live and read out the figures [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]:

- **Supplier**, as rendered in the transcript: "**А тач, интеллигент**" — spoken as "Touch Intelligent". *(The derived notes carry it with "name uncertain". No real-world company is identified here and none is asserted.)* [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- **Amount:** "**3 хандрид плюс… Shipment… 3 секси чтото**" — three hundred plus shipment, "three sixty something".
- **Breakdown:** "**2 сэмпла по 150 и sixy five dola frade. В Минск**" — 2 samples at $150 each and about $65 freight to Minsk.

## Update, Sept 29 2026 — the 3576 lives as a branch in the RK3568 repository, cannot boot from SD, and waits until the two environments are standardised

At the [[wiki/meetings/2026-09-29-dev-environments-rk3568-sdk-amd-spike-and-ai-pm-direction-check.md|Sept-29 "Dev_environments" call]] (Russian) [[wiki/people/pavel.md|Pavel]] gave the first status on the "SDK for the 76 board" named above [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]:

- **Where it is.** "сейчас 76 процессор. Он в виде бранча живёт в р к 35 68… Мне казалось, что там почти всё то же самое, но когда начал работать, оказалось, что там есть расхождения" — a branch in the RK3568 SDK repository; he has started working on it and found differences. "А в целом дальше на 95% репозиторий такой же."
- **The one hard difference.** "для 76 процессора есть отличие от 68, что он не умеет грузиться со с д карточки… нам придётся 76 прошивать. Проводом. Всегда 1 Загрузка будет надо будет подключаться проводам к компьютеру" — no SD-card boot; the first load is always flashed by cable from a computer.
- **One repository or two — open.** It "в принципе можно держать в одном репозитории" so that a tool or network filter added once works for both the 3568 and the 3576; Irina: "А нужно?"; Pavel: "Надо подумать как как лучше."
- **Order.** [[wiki/people/val-levitan.md|Val]]: "Конечно. Но я бы хотел сначала стандартизировать между 2. Девелопментами, а потом уже дальше их развивать" — the RK3568/AMD standardisation first, the 3576 after. Rulings on [[wiki/decisions/2026-09-29-the-amd-environment-is-rebuilt-from-the-rk3568-sdk-pavels-ten-day-spike-and-the-rk3576-waits.md]].

Pavel's SDK commitment below stays open; whether a game has been run on the 3576 is not said.

## Open commitments

- [ ] [[wiki/people/mikhail-perelman.md|Mikhail Perelman]] — push the RK3576 delivery to Minsk (2 samples, ~$300 plus ~$65 freight) — due urgently, Val's word was "срочно". *(Val names him as the person who **controls** the supply; the transcript does not record the instruction being given to him or accepted, and the derived notes flag the same gap as "[Needs Val's confirmation]".)* — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]] [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — on arrival of the RK3576, get at least one game running and report memory use — due on arrival — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — rework the SDK for the 3576 board and build the integration repository — due unspecified — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

## Open questions

- **Where does the RK3576 order actually stand?** Genadi did not know whether the invoice had gone out — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- **Does 8 GB carry the game count this machine needs?** Unmeasured on the 3576, and the July-29 measurement on a different board points the other way (above) — [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]

**§15.8:** clear — board, component and freight economics only; no named-person compensation appears in either Sept-14 12:04 file.

## Sources

- [[raw/Meeting_Transcript_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Hardware_Priorities_TITO_Case_and_Street_Cabinet-September-14-2026.md]]
- [[raw/Meeting_Notes_Low_Cost_Street_Cabinet_Platform-June-9-2026.md]]
- [[raw/Meeting_Notes_RK3588_Game_Performance_Findings-July-29-2026.md]]
- [[raw/Meeting_Notes_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Hardware_GitHub_Standard_and_BC_Sync_Design-August-12-2026.md]]
- [[raw/Meeting_Transcript_Dev_Environments_AMD_SDK_Spike_and_RK3576_Plan-September-29-2026.md]]
