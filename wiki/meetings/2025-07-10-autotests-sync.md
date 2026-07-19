---
type: meeting
title: Autotests sync — test-environment configuration & RIS (July 10 2025)
date: 2025-07-10
source-count: 1
---

# Autotests sync — test-environment configuration & RIS (July 10 2025)

Test-automation sync; transcription started by [[wiki/people/pavel.md|Pavel Frolov]]. Attendees: [[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]], [[wiki/people/anton-leshkevich.md|Anton Leshkevich]], [[wiki/people/irina-shishko.md|Irina Shishko]], Pavel Frolov, [[wiki/people/alexei-khamin.md|Alexey Khamin]], [[wiki/people/vladislav-gurin.md|Vladislav Gurin]], **Ivan Shpak** (Shpak is a recurring QA engineer without his own page). Date is explicit in the transcript header (July 10 2025) — the first ingested source dated to July.

Substance — the test-automation team's plan to make the test environment configurable — is on [[wiki/topics/test-automation-strategy.md]]. Key points: build large JSON objects/sectors to configure tests on the fly; save/read machine "passport" settings to files for persistence across restarts; the real-vs-virtual-device problem (machine tests use real devices, hard to substitute); connect to machines over SSH to swap config files before a test; add pre-test setup hooks in LGS (Anton — the framework currently assumes the environment is already set up); the LISA problem (LISA is per-machine/version, ill-suited to automation; on the "tabachny" version LISA falls and is ignored, only etap applies — a temporary workaround); and the **RIS implementation plan** (Kharetski provides the JSON structure + an endpoint for submitting RIS; Anton builds JSON builders ~2–3h; tests drive the UI for user actions and use the API only for configuration). Decisions: tests interact with UI for actions and API for configuration only; prioritise RIS before virtualisation; start with simple machine configs (Shishko) — though Kharetski pushed to provide proper unified tooling from the start rather than incrementally.

## Sources

- [[raw/autotests_sync_meeting.md]]
