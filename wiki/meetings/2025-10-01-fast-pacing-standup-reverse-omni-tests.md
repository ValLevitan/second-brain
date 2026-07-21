---
type: meeting
title: Fast-pacing general-alignment stand-up — session 4 (reverse-Omni: tests-first, spec-second; read-aloud method) (Oct 1 2025)
date: 2025-10-01
aliases: [fast-pacing stand-up session 4, fast-pacing general alignment stand-up Oct 1, reverse-Omni tests first, read aloud transcript method, Biratka spec extraction, coffee-machine stand-up]
source-count: 1
open-commitments: 2
open-questions: 1
---

# Fast-pacing general-alignment stand-up — session 4 (Oct 1 2025)

**Date:** 2025-10-01 (1:31 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]. Russian. (Val jokingly framed it as a relaxed "conversation by the coffee machine.")

**Session 4** of the recurring fast-pacing / general-alignment stand-up series — sequenced to the [[wiki/meetings/2025-09-10-fast-pacing-alignment-standup.md|Sept-10 opener]] (s1), [[wiki/meetings/2025-09-17-fast-pacing-alignment-standup-spec-prototyping.md|Sept-17 spec-prototyping]] (s2) and [[wiki/meetings/2025-09-24-fast-pacing-alignment-standup-pipeline-interviews.md|Sept-24 pipeline-interviews]] (s3). What advanced since Sept-24: the AI-generated Omni spec/diagrams from the [[wiki/people/alexander-biratka.md|Sasha Biratka]] interviews now exist in git (~60–65% accurate), and Val reframed the next step as a **tests-first, spec-second** loop plus a **read-aloud transcript method**. Substance on [[wiki/topics/test-automation-strategy.md]] (Oct-1 section) and the reverse-Omni thread on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]].

Durable points (single source):

- **Extraction from Sasha Biratka is exhausted.** [[wiki/people/alexander-biratka.md|Sasha Biratka]] (transcribed "Александр братко" / "пиратка", the Omni framework author) has been "squeezed for all we could get" — 6 more meetings Monday walking how to build a game on the framework's buckets (Kaiocho example). The transcriptions + source code were fed to AI, which generated **architecture diagrams and a 2-version framework spec** now sitting in the git repo — but Pavel judges it only **~60–65% (maybe 50%)** of what a real spec should be, and admits he has hit a point of fatigue with it. [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- **The read-aloud method (Val's directive).** Rather than let each engineer read the AI-generated spec alone (the "lazy path" that just re-scatters tribal knowledge fragmentarily), Val prescribed **live meetings where the group reads the material aloud paragraph-by-paragraph, poking at "why / where"**, recording those meetings, then feeding the fresh transcript back to the AI to iterate. He does this himself with a colleague (name unclear in transcript — "Erwin"/"зерно"), attributing the practice to a well-known executive's written-notes-read-aloud-at-the-meeting method (name garbled here; cf. the Jeff-Bezos attribution on [[wiki/topics/test-automation-strategy.md]]). Rules of thumb: **mornings only** (afternoons Val can't focus), **~1 hour** per session (naturally stretching to ~2 with several people, but no more), start tomorrow morning with Sasha + Ira + Igor + Zhenya on the architecture diagram. [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- **Google Meet checked and rejected (for now).** [[wiki/people/dmitri-chudinov.md|Dima]] ran experiments and reported Google Meet transcribes **Russian even worse than Teams**, so JVL stays on **Teams** but still re-runs each meeting through Pavel's **offline transcription tool** (~1 hr/meeting) because it is much closer to what was actually said. (Updates the Sept-24 "try Google Meet + Gemini" recommendation — evolution, not contradiction: tested, and Teams retained.) [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- **The tests-first, spec-second loop.** Because "we can't write tests without a spec" but the spec is only ~65% real, Val flipped the order: assign each reverse-Omni participant to **propose 5–10 tests** (start with **3**, chosen to hit different areas like "a spider's legs"), abstracting away from whether the test hooks exist yet. The engineers are expected to ask the trick questions — **"where is the spec?"** and "what are we testing?" — which is exactly the point: from the tests they will surface what the spec must contain (drivers, addresses, hooks; engineering descriptions; game-creator descriptions from Lena). Participants Val named: **Koretski** ([[wiki/people/evgeny-kharetski.md|Evgeny Kharetski]] — the Koretski/Zhenya garble resolved by the LGS/Omni-backend + reverse-Omni context per §4 registry, Tier-A queued), **[[wiki/people/igor-metelski.md|Igor Metelski]]**, an **Anton** ([[wiki/people/anton-leshkevich.md|Anton Leshkevich]] by the test-framework context), a **new "Alexander"** (Tumanov by the Sept-24 new-hire context, inference), and **Irina Makarych** ([[wiki/people/irina-makarych.md|Makarych]]). [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- **Test hooks still missing.** Pavel noted test-writing stays "very limited" until someone adds the required **hooks into the test framework's code** to reach the game/framework internals — **Anton hasn't done this yet** (nor has anyone), and Val accepted it "will come later," maybe a week, maybe two months. (Same open dependency as the July-11 "developer writes the test hooks" idea.) [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- **Interview Lena for the game-UI/dashboard description.** The game's dashboard/UI (what a board is, what it shows, what it's made of) is undocumented — Sasha never described it. Plan: **interview [[wiki/people/lena.md|Lena]]** the same way (record it), combine with the generated game images in Jira and the existing game requirements/spec. Val's 2-year bet: recorded conversations + exponentially improving AI logic will let JVL convert the whole system to "fairly precise logic." [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]

## Open commitments

- [ ] Pavel Frolov + Irina Shishko — run **read-aloud** review meetings (mornings, ~1 hr) over the AI-generated Omni architecture diagram / spec with Sasha + the reverse-Omni group; record and re-feed transcripts to AI — starting tomorrow morning — [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
- [ ] Pavel Frolov + Irina Shishko — have each reverse-Omni participant (Kharetski, Metelski, Anton, the new Alexander, Makarych) come back in a couple of days with **5–10 proposed tests** (start with 3) and the spec elements those tests require — [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]

## Open questions

- When will the missing **test-framework hooks** (into the game/framework internals) actually be added — the precondition that keeps test-writing "very limited"? Left open (a week to two months). [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]

## Sources

- [[raw/fast-pacing-stand-up_meeting-october-1-2025.md]]
