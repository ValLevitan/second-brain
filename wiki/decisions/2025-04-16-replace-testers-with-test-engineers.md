---
type: decision
title: Replace manual testers with Test Engineers who write automated tests
date: 2025-04-16
aliases: [fire the testers, test engineers, automated integration tests, QA to test engineers]
source-count: 1
status: active
---

# Replace manual testers with Test Engineers who write automated tests

Announced by Val in the Apr-16 Omni daily ([[wiki/meetings/2025-04-16-daily-omni-feature-story-planning.md]]) while discussing integration tests for the Money-In/Cash-out messages.

## What was decided

- **JVL will have no manual testers.** Val: "Тестировщики. Мы их увольняем. У нас не будет ни одного тестировщика. У нас будет Test Engineers. И вот эти Engineers будут писать automated тесты." [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- **Current staff get a chance to level up, or be replaced.** Those not qualified will be helped to raise their qualifications "если они захотят"; if they won't, [[wiki/people/irina-makarych.md|Irina]] already has "3-4" (then "пять") new people she is ready to bring in "даже завтра." [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- **Anton trains the QA engineers — he does not write the tests himself (changed decision).** Val: "Я поменял свое решение. Я не хочу, чтобы вы сами руками писали эти тесты. Я хочу, чтобы вы начинали учить наших QA-инженеров, как писать эти тесты." [[wiki/people/anton-leshkevich.md|Anton]] is to prepare a presentation of what he expects and how they will write integration tests, and run a kickoff meeting with Irina and Pavel — Val offered to attend at **6:30 am Friday**; the three QA (incl. "Vlad" and "Lesha") plus [[wiki/people/yuri-zakharenko.md|Yuri Zakharenko]] to be invited. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Rationale

Omni development writes integration tests as part of the build ("мы пишем интеграционные тесты"); Val wants an engineering QA function that authors automated tests rather than clicking through checks, consistent with the DevSecOps "security is more tests" stance on [[wiki/topics/infosec-and-server-infrastructure.md]] and the test-automation direction on [[wiki/topics/test-automation-strategy.md]].

## Status

Active as of 2025-04-16. This supersedes Val's earlier expectation (voiced Apr-15) that Anton would build the integration tests directly — the current state is Anton teaching QA engineers to write them.

## Sources

- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
