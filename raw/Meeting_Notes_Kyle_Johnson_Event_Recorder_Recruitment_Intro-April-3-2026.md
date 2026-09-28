# Meeting Summary — Kyle Johnson: event recorder (black box) recruitment intro

**Date:** April 3, 2026, 1:07 PM Eastern
**Duration:** approximately 32 minutes of content (66-minute recording; ~10 minutes of Teams/camera failures at the top, migrated to Google Meet)
**Attendees:** Val Levitan, Nathan Carver (the introducer), Kyle Johnson (embedded systems engineer, RTX aerospace/aeronautics division, Arizona; ex-colleague of Nathan's at "Ion").
**Raw transcript:** [[Meeting_Transcript_Kyle_Johnson_Event_Recorder_Recruitment_Intro-April-3-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Scheduling Introductory Call and Compatibility", 1:00–1:30 PM ET, organiser Val. Nathan named in the transcript; confirmed.

## Summary

Recruitment intro for the **gaming machine event recorder** — Val's "in-flight black box": a module wedged on top of the JVL system recording all inter-module events (button presses, touchscreen, framework↔data-center traffic, watchdog-timer failures), so a hung machine can be investigated like a crash. Envisioned as an embedded solution sitting on a redesigned I/O board with a USB or cellular-modem exit path. No architecture exists yet; Kyle confirmed he can own the architecture himself "as long as we have a basic understanding of the requirements and goals."

**Kyle's profile.** RTX aerospace: critical-system software, export compliance, FAA/EU flight-safety testing. Embedded background: TI microprocessors, ARM Cortex (M0s, ARM5/7, A55 experience confirmed when Val showed the candidate SoC — a quad-core Cortex-A55 board, Rockchip family, which JVL would re-spin with its own chip), embedded Linux with drivers/device trees, bare metal, in-house RTOSes. He has done extraction-of-information transformations for verification in certified/regulated markets — a close fit.

**Val's candor about the engagement.**
- The company is "built on Soviet Union era engineers" — top-class design theory, but records/exchange culture and language are "unbearable"; Val wants North American expertise and culture enforcement, the same reason Nathan was hired. Nathan's honest brief on the culture: quiet, non-assertive in meetings, information must be actively driven out of them — "they won't initiate with you unless you're actively pushing." Kyle was unfazed (has worked such environments; leads with "here's how I see it — is this how you see it?").
- Engagement model: part-time around Kyle's RTX job, capacity-based like Nathan's arrangement; the recorder is "not schedule critical — I can snap it in when it's ready," but no five-year project either.
- Time zones: engineers at UTC+3 (Minsk), Kyle at UTC-6/7 (Arizona) — a ~9-hour spread; Kyle is a night owl ("sometimes I'm up to the morning in Europe"), will figure the schedule.
- Val's longevity condition: "if I start going with you, I like to know there is longevity — you're not gonna quit in the middle… if something doesn't feel comfortable, just let me know and we either fix it or we just don't go for it."

**Close.** Kyle takes a week to decide; free to talk to engineering or Val again before then.

## Decisions Made

- **Kyle decides within one week** whether to take the event-recorder engagement. (Kyle, at Val's invitation)
- **Engagement shape if yes: part-time consulting, capacity-based, architecture ownership with JVL engineering support.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Kyle Johnson | Decision on the engagement | ~April 10 | High | "I'll have a decision in a week" |
| 2 | Val / Nathan | Facilitate any engineering conversations Kyle wants before deciding | On request | Normal | Offered |

## Open Questions

- Final SoC choice (Cortex-A55 / Rockchip-family board shown; JVL wants its own chip on a redesign).
- Exit path (USB vs cellular modem) and I/O board redesign scope.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 3)*
*Source recording: 04-03 Embedded Systems Engineer Recruitment for Gaming Machine Event Recorder (Plaud)*
