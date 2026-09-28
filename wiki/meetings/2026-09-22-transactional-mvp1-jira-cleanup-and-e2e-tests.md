---
type: meeting
title: Transactional MVP 1 — the last Jira clean-up, the October 2 date challenged, and the first end-to-end test set as a one-hour micro-step (Sept 22 2026, 8:01–9:23 AM)
date: 2026-09-22
aliases: [Transactional MVP1 CAPs REQs UI/UX Sept 22, MVP1 Jira Cleanup and E2E Tests, day seven of the MVP1 series, Sept 22 8am transactional call, the E2E micro-step call]
source-count: 2
open-commitments: 0
open-questions: 0
---

# Transactional MVP 1 — Jira clean-up and end-to-end tests (Sept 22 2026)

**Date/time:** September 22 2026, **8:01 – 9:23 AM Eastern** (about 82 minutes), from the recording header [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. **Series:** the Teams session "Transactional MVP1: CAPs, REQs, UI/UX", the **seventh** morning call (after Sept 14, 15, 16, 17, 18 and 21) [[raw/Meeting_Notes_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]. **Language: Russian.**

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]] (chaired; he is back after missing two calls, by his own words), [[wiki/people/andrei-klimovich.md|Andrei Klimovich]], [[wiki/people/pavel.md|Pavel Frolov]] (shared his Jira screen), [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik") and [[wiki/people/alexander-biratka.md|Alexander Biratka]] (label "Alexander Biratko") [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**Purpose.** The first MVP 1 call where Val speaks since Sept 16 (Sept 17 and 21 had no Val turn; Sept 18 he was in the chat only). Four blocks: Klimovich's screen status, a live pass over the MVP 1 capabilities still out of place in Jira, the release date, and the missing end-to-end tests, which took most of the time and ended in a one-hour test to run by the next day [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. The same day's other transactional stub, [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md]], is a different meeting (4:48 AM stand-up, Val absent, different attendees and content). A corpus-wide search found no other stub for this 8:01 session. It is a new meeting.

Substance lives on:

- [[wiki/topics/flexpay-business-architecture-payout-devices.md]] — the MVP 1 series timeline (Sept 22, 8:01 AM entry): screens, texts, naming, the date, the KORE SIM
- [[wiki/decisions/2026-09-22-autotests-go-inside-the-existing-capabilities-and-the-first-e2e-test-is-a-one-hour-micro-step.md]] — the test ruling
- [[wiki/topics/test-automation-strategy.md]] (Sept 22, 8:01 AM) — why no end-to-end tests exist, and who writes them
- [[wiki/decisions/2026-09-18-the-mvp1-capability-list-is-walked-item-by-item-and-every-capability-gets-an-owner.md]] — Sept-22 update: 115, 157, 148, 180, 152, FIQ-34
- [[wiki/decisions/2026-09-17-jvl-supports-multiple-incomm-products-not-a-fixed-pair.md]] — Sept-22 update: 178 still shown under MVP 1 in Jira
- [[wiki/decisions/2026-09-11-mvp1-goes-with-flex-iq-alone-and-one-kiosk-per-location.md]] — Sept-22 update: the October 2 end date challenged, the initiative split
- [[wiki/decisions/2026-09-11-accepted-means-reviewed-taken-into-work-is-the-move-to-to-do.md]] — Sept-22 update: the green Accepted colour again
- [[wiki/decisions/2026-09-15-the-week-goes-to-non-functional-requirements-and-monday-september-21-is-the-deadline.md]] — Sept-22 update: still no feature lock
- [[wiki/decisions/2026-09-16-anything-that-depends-on-the-cloud-leaves-mvp1.md]] — Sept-22 update: the cloud wording is gone
- [[wiki/decisions/2026-09-14-remote-firmware-update-is-in-mvp1-and-flex-iq-updates-itself-first.md]] — Sept-22 update: capability 122 closed
- [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]] — Sept-22 update: the text library and the standards
- [[wiki/decisions/2026-09-07-virtual-test-system-tries-full-arm-emulation-first.md]] — Sept-22 update: a FlexPay emulator is being built
- [[wiki/topics/ai-assisted-development.md]] (Sept 22) — how Claude turns a capability into features
- [[wiki/topics/github-release-management-pipeline.md]] (Sept 22) — dependency updates stay manual
- [[wiki/projects/georgia-market-rollout.md]] (Sept 22, 8:01 AM) — the KORE SIM into the IQ, and the office router
- People: [[wiki/people/val-levitan.md]] · [[wiki/people/andrei-klimovich.md]] · [[wiki/people/pavel.md]] · [[wiki/people/dmitri-chudinov.md]] · [[wiki/people/irina-shishko.md]] · [[wiki/people/andrey-bosik.md]] · [[wiki/people/alexander-biratka.md]] · [[wiki/people/alexei-khamin.md]] · [[wiki/people/ivan.md]] · [[wiki/people/evgeniy-alekseev.md]] · [[wiki/people/dmitri-kovalchuk.md]] · [[wiki/people/elizabeth.md]]

**§4 name calls** [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]:

- "Андрей" who shows screens and owns capabilities = Klimovich. "Андрей Босик", named in full by Val as owner of the text library = Bosik. "без Андрея" in Chudinov's cloud-testing warning = **Bosik, by context (inference)** — he runs the cloud side.
- "Чудинов" and "Дима" on capabilities = Chudinov. "Диме Ковальчуку" = [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]] (named in full). "Биратко" / "Саша" = Biratka.
- "Лёша" who writes the first test = [[wiki/people/alexei-khamin.md|Alexei Khamin]]; Val names "Алексея Хамина" in full at the end.
- "Иван" / "Ивана" = [[wiki/people/ivan.md|Ivan]] (roster "Shpak, Ivan"), by context: he is in Pavel's list of test writers with Khamin. **No surname is spoken; "Ivan Shpak" in the notes comes from the roster, not the recording.**
- "Евгений Алексеев" = [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]], named in full by Pavel as one who will run tests. The bare "Женя" offered to help write tests is **most likely the same man (inference)** — named in the same passage, and hardware testing fits his registry role. Not asserted as fact.
- "Элизабет" = [[wiki/people/elizabeth.md|Elizabeth]] (Georgia office).
- **Not resolved:** "Антон", who is building the FlexPay emulator — no surname, and none of the three Antons on file fits clearly. "Владимир", said to be busy with screens, is probably [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] (he took the screen redraw at the 4:48 stand-up) — **inference**, not asserted.

**Where the notes and the transcript diverge** (transcript followed):

1. **"Blank".** The notes say Val's correct word is "blank". The transcript has "правильное слово блэк". Reading it as "blank" is an **inference** (it replaces "empty").
2. **FIQ-34.** The notes say Chudinov "put it into the backlog". In the transcript Pavel says it *is* in the backlog and needs a date some time ("Он в бэклоги надо будет тоже его когда-то поставить"); Chudinov answers "Сейчас поставил" — he scheduled it.
3. **Where the autotests go.** The notes give only Pavel's position. In the transcript Chudinov first said a separate capability was better ("лучше отдельная [капабилити]"); Pavel preferred building them into the existing ones, and Val backed that.
4. **The first test's idea.** Chudinov floated it first ("тест на подключение флекспорта к машине, либо флекспорта к флекс айкю"); Pavel then made it concrete. The notes credit Pavel alone.
5. **The Texas case.** The notes drop Val's own caveat — "Я знаю, что у нас ещё нету диспенсера" (JVL does not have the dispenser yet).
6. **Omitted by the notes:** Chudinov's report that capability 122 (Flex IQ remote updates) was closed that day; Chudinov's and Biratka's answers that MVP 1 is clear to them; Chudinov's point that the shared registration mechanism now means changing 2 repositories instead of 6; Bosik's idea to keep capabilities like an ADR, with a dated change line; Irina's note that Vladimir is busy with screens; Val's remark that Klimovich sat beside him.

**§15.8:** clear. The meeting is scope, Jira, testing and tooling. Val's rough language during the date argument is not recorded. No pay, rate or personal judgement appears; nothing was withheld. **§15 #9:** no corporate identifier appears. Capability, requirement and ticket numbers (115, 122, 148, 152, 156, 157, 173, 178, 180, REQ-1473, FIQ-34) are work references. No phone number was spoken.

## Sources
- [[raw/Meeting_Notes_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
