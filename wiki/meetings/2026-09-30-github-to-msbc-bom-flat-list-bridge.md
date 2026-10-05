---
type: meeting
title: GitHub to MSBC BOM integration — one flat list in GitHub, grouping in MSBC by automation, part numbers from the standard, and Nathan to experiment items-first; Val ends it early (Sept 30 2026, 10:00–10:51 AM)
date: 2026-09-30
aliases: [GitHub_to_MSBC_BOM_Integration, GitHub to MSBC BOM Flat List Bridge, GitHub to MSBC BOM bridge, flat list bridge, Sept 30 BOM meeting, 550 nominations, engineering territory and administrative territory, non-penetrable border, the transcriber, build script, items first then BOMs, I don't want to be a therapist, this meeting is not productive]
source-count: 4
open-commitments: 0
open-questions: 0
---

# GitHub to MSBC BOM integration — the flat-list bridge (Sept 30 2026, 10:00 AM)

**Date/time:** September 30 2026, **10:00 – 10:51 AM Eastern** (about 48 minutes of talk), from the `**Date:**` header line. Teams title "GitHub_to_MSBC_BOM_Integration". **Language: English** throughout (not Russian, unlike the Sept 23 and Sept 24 calls on the same subject) [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

**Who spoke** (speaker labels): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/lev-rudky.md|Lev Rudky]] [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]. This is the "separate meeting on GitHub and its sync with MSBC" Val promised on Sept 23 — held with Nathan and Lev; [[wiki/people/andrey-bosik.md|Andrey Bosik]], whom Val had named then, was not on it.

**Purpose.** Val set the objective: Genadi keeps updating drawings and supplier specs; every change becomes a revision in GitHub; the BOM and costs in MSBC update from it; supplier and financial data live only in MSBC, engineering files only in GitHub, and neither side edits the other. He asked for concerns "instead of rejections". Genadi supported the engineering half and could not see how a BOM lives in GitHub; Val answered that GitHub holds one flat list and the grouping into assemblies happens in MSBC by automation; Nathan framed it as a build script and asked for real examples; Lev warned that a new item in BC needs accounting fields too. Genadi proposed phases (items first), Nathan agreed and will experiment. Val then called the meeting unproductive, released Nathan and Lev, and moved to a separate meeting with Genadi [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]].

**§12 — one meeting, two files.** The notes and the transcript share the date, time and title and link each other. A corpus-wide grep for both filenames, "GitHub_to_MSBC", "Flat_List_Bridge", "550 nominations", "build script" and "10:00 AM" + "September 30" found no page citing either file and no earlier stub for this slot. It continues the [[wiki/meetings/2026-09-23-texas-flex-slim-release-street-cabinet-and-bom-source-of-truth.md|Sept 23]] and [[wiki/meetings/2026-09-24-hardware-repo-bom-source-of-truth-and-street-cabinet-layout.md|Sept 24]] calls but is a distinct event (different day, Nathan and Lev present). The follow-on Val–Genadi meeting the same day is the [[wiki/meetings/2026-09-30-solidworks-flat-parts-list-parked.md|12:04 PM "How to get from Solid Works… to a flat list of parts" recording]] — its notes name this meeting as the one it follows [[raw/Meeting_Notes_Solid_Works_Flat_Parts_List_Parked-September-30-2026.md]]; it was parked after two minutes and has its own stub (a separate recording and title, not a segment of this one). The Oct 1 meetings on the flat BOM continue the thread — the timeline on the decision page is left open. New meeting.

Substance lives on:

- [[wiki/decisions/2026-09-23-the-bom-source-of-truth-is-the-latest-design-in-github-and-sync-runs-one-way.md]] (Sept-30 update) — one flat list in GitHub (agreed), grouping into assemblies in MSBC by automation (Val) versus "build the BOM in MSBC" (Genadi, still not seeing the gain); Nathan's build-script framing; phases, items first; the Sept-23 "separate meeting" commitment discharged
- [[wiki/decisions/2026-09-30-engineers-never-change-msbc-and-administration-never-changes-github.md]] — the border rule, and the "transcriber" tool that carries flat revisions one way
- [[wiki/decisions/2026-09-30-a-new-part-number-is-assigned-by-claude-from-the-standard-in-github-and-pushed-to-msbc-once.md]] — the part-number flow Genadi called "Perfect", and Lev's accounting-fields caveat
- [[wiki/topics/business-central-erp-implementation.md]] (Sept 30) — the same thread from the BC side; how Genadi builds a BOM today (SolidWorks numbers entered by hand, standard parts added at BOM time)
- [[wiki/topics/github-release-management-pipeline.md]] (Sept 30) — the standards repo as the home of the part-number standard; the flat list as the GitHub artifact
- People: [[wiki/people/genadi-peari.md]] (Sept 30, 10:00 AM) · [[wiki/people/nathan-carver.md]] (Sept 30) · [[wiki/people/lev-rudky.md]] (Sept 30) · [[wiki/people/val-levitan.md]] (Sept 30, 10:00 AM) · [[wiki/people/mikhail-perelman.md]] and [[wiki/people/elizabeth.md]] (named in absentia)

**§4 name calls** [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]:

- "Michael" (Val: "you tell Michael which lock he orders") = [[wiki/people/mikhail-perelman.md|Mikhail Perelman]], **by context** (procurement/ordering parts; his page carries "Michael" as an alias) — inference.
- "Elizabeth" (Val: "you tell Elizabeth which lock goes where") = [[wiki/people/elizabeth.md|Elizabeth]], **by context** (Georgia assembly) — inference.
- "Nathan" = [[wiki/people/nathan-carver.md]] (speaker label "Nathan Carver"). "Lev" = [[wiki/people/lev-rudky.md]] (label). "Genadi" / "Gennady" = [[wiki/people/genadi-peari.md]] (label).
- "Claude" (Val: "Claude reads the standard… gives it a part number") = the AI tool, not a person.
- "light and wonder" (Genadi's example: "we need to supply cable for light and wonder") = Light & Wonder, a customer in his example; no page created (one hypothetical mention).
- "Mandy" ("give Mandy the"), "Sam" (Nathan's one-word line) and "In London for somebody else" (Lev) are read as garble, not people.

**Where the notes and the transcript diverge** (transcript followed; notes [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]):

1. **The separate Genadi meeting "booked for 12:00 PM the same day".** The transcript has no time: "I will switch to a different meeting with Genadi… I'm going to invite Genadi to the different meeting." The 12:00 PM is the notes' addition (possibly from a calendar). **Now answered:** that meeting was recorded **12:04 – 12:06 PM** with Genadi Peari as the only other speaker, and was parked after two minutes — [[wiki/meetings/2026-09-30-solidworks-flat-parts-list-parked.md]] [[raw/Meeting_Transcript_Solid_Works_Flat_Parts_List_Parked-September-30-2026.md]].
2. **"Genadi agreed to that part-number flow."** The transcript: "Perfect" and "OK, good. No, no questions" — then "I can create it in Github. It's perfect. Or Msbc, it doesn't matter." So he agreed to Claude assigning the number from the standard, and was indifferent to where it is first created. Recorded with that caveat.
3. **Undertaking "Genadi provides Nathan with example BOM structures".** The notes themselves call it implied. In the transcript Nathan states what he needs ("examples or actual actual BOM structures that you're using now"); nobody is assigned. Recorded as Nathan's stated need, not as Genadi's commitment.
4. **Omitted by the notes:** Val's "550 nominations" per machine (Genadi's figure, as Val relays it); the ten-locks example and "you tell Michael… you tell Elizabeth"; Val's "Navision was designed 50 years ago, got obsolete 30 years ago, and was taken offline 20 years ago"; "I don't want to be a therapist"; the "transcriber" tool that could run "hourly… by minute"; Val's "there should probably be a standard how a bill of material is formed. Maybe, I don't know."
5. **Language.** The notes do not state it; the transcript is English.

**§15.8:** Val's exasperated remarks at Genadi in the middle of the call ("I don't know why you keep quiet… why you don't follow me") and a crude line about nobody in the company acting without Genadi's instruction are read as personal and are **not recorded**; the substance (nothing in the machine is improvised; every part has a drawing or an approved supplier drawing) is. "I'm just burning their hours" is a process remark and is kept. Nobody's pay or performance is recorded. **Personal matters not recorded** (none met). **§15 #9:** clear — "highly confidential banking information" for a vendor is named as a category only; no value appears.

## Sources
- [[raw/Meeting_Notes_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Transcript_GitHub_to_MSBC_BOM_Flat_List_Bridge-September-30-2026.md]]
- [[raw/Meeting_Notes_Solid_Works_Flat_Parts_List_Parked-September-30-2026.md]] *(cross-reference only — the follow-on meeting)*
- [[raw/Meeting_Transcript_Solid_Works_Flat_Parts_List_Parked-September-30-2026.md]] *(cross-reference only — the follow-on meeting)*
