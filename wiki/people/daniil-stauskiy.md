---
type: person
title: Daniil Stauskiy
date: 2026-11-08
aliases: [Daniil Stauskiy, Daniil, Даниил, Daniil Stauski]
source-count: 4
open-commitments: 0
open-questions: 0
---

# Daniil Stauskiy

A developer on JVL's Minsk engineering team (speaker label "Daniil Stauskiy" in the daily stand-ups run by [[wiki/people/pavel.md|Pavel Frolov]]) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. In November 2026 his work is the game sound library for the new engine: he is rewriting the sound repository in Rust on PulseAudio after dropping the Kira library, with a converter that turns the existing FMOD sounds from FSB into FLAC with JSON descriptions — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]]. He appears by first name on earlier pages (the engine capabilities he drafted, his RK3576 board tests, a server-side player-video spike) — see [[wiki/decisions/2026-10-29-the-new-engine-is-fully-described-and-split-into-mvp-1-2-3-with-schedules-and-a-test-environment-before-code-and-anton-igor-and-alexander-build-it-together.md]], [[wiki/decisions/2026-09-14-the-street-cabinet-board-is-the-rk3576-not-the-rk3568.md]] and [[wiki/people/anton-leshkevich.md]]; those mentions are cited there, not here. Page created Nov 8 2026 from the Nov 2–3 stand-ups, where he speaks for himself; the role wording above is the wiki's (**inference** from the work described, not a title given in a source).

## Nov 2 2026 — the sound spike: Kira dropped, PulseAudio, Rust, FSB → FLAC + JSON

At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] he asked how to write up the spike's outcome in the task's comments, then reported: "Сейчас мы переписываем в репозиторе звука на rast"; Kira dropped for now — it cannot send sound to the top and bottom speakers separately and has no event system, saving only about 200 lines; with PulseAudio there will be one ready library for the LGS that plays on Windows and ARM; a converter tool already exists; FSB becomes FLAC and the sound description a JSON file [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. Pavel and Biratka turned it into the rewrite in Rust inside the engine — [[wiki/decisions/2026-11-02-the-game-sound-library-is-rewritten-in-rust-on-pulseaudio-inside-the-engine-kira-is-dropped-for-now-and-the-fmod-sounds-are-converted-to-flac-with-json-descriptions.md]], where his commitment is tracked.

## Nov 3 2026 — moving the library to Rust; dependency requests

At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]: "Делаю задачу ахмад 4" (heard — a task name, **unclear**), moving the sound library to Rust ("на раз"), and in parallel looking at dependency requests that came in ("во франки пришли", heard; the notes read Dependabot) — what to merge and what to decline [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
