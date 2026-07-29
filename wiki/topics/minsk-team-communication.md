---
type: topic
title: North America ↔ Minsk communication and the feedback loop
date: 2026-03-05
aliases: [Minsk communication breakdown, hygiene of alignment, one-way valve, feedback loop, Hourensou, context not control, Minsk cultural problem]
source-count: 3
open-questions: 1
---

# North America ↔ Minsk communication and the feedback loop

How information moves — and fails to move — between JVL's North-American executive/market side and its Minsk engineering team. Worked out on a Mar-5 2026 exchange between [[wiki/people/val-levitan.md|Val]] and [[wiki/people/pavel.md|Pavel Frolov]] ([[wiki/meetings/2026-03-05-communication-breakdown-minsk.md]]) plus two same-day written analyses Val authored around it. This is the **human/cultural counterpart** of the same-month engineering-visibility push (the [[wiki/topics/github-release-management-pipeline.md|Jira↔GitHub transparency thread]], Mar-4 "culture of information hygiene" → Mar-6/9/10 visibility work) and sits under JVL's stated [[wiki/topics/jvl-operating-principles.md|operating principles]] (one source of truth; if it was not recorded, it was not decided). Recorded factually as a structural/process diagnosis, not a judgement of any individual.

## The diagnosis Val put forward

- Val's framing: the company is **fragmented** — executive branch and market in North America (itself split across small offices), engineering in Minsk — and Covid-era remote work deepened it into "a collection of isolated individuals connected only by scheduled calls," with cultural and language barriers on top. [[raw/Describing_the_cultural_problem_in_Minsk.md]]
- His core claim: information flow is **one-directional** — North America pushes directives, requirements, context and strategy toward Minsk; Minsk absorbs, interprets, executes and delivers code, but **the interpretation, questions, tradeoffs and assumptions do not travel back**. Misalignment surfaces only when the delivered result does not match intent. He calls the missing discipline **"hygiene of alignment" (гигиена согласования)** — the proactive, two-way exchange between the people who define *what* to build and the people who decide *how*. [[raw/Describing_the_cultural_problem_in_Minsk.md]]
- Val stresses the behaviour is **not malice or incompetence**: formulating objections across a language and cultural barrier feels like a daunting distraction from "the real work" of writing code. His recurring line: **"I do not read minds"** — nobody can, so making your counterpart aware of a concern, question or disagreement has to become part of the job, not an afterthought. [[raw/Describing_the_cultural_problem_in_Minsk.md]]

## The frameworks Val uses to describe it

All drawn from Val's written analysis as illustrative analogies (labelled as his framing, not JVL policy): [[raw/Describing_the_cultural_problem_in_Minsk.md]]

- **Hourensou (報告・連絡・相談 — Report / Inform / Consult):** report what happened without being asked, inform affected colleagues before they find out themselves, consult before deciding when uncertain. Val's read: the Minsk→North-America channel has none of this, so he becomes a "bottleneck interrogator" extracting on every call what should have been volunteered — and the team develops an "allergic reaction to conversations."
- **"Context, not control" (Netflix):** leaders supply the *why* and people make good decisions — but it needs context flowing both ways; Val's read is that downward context is received as a bare command (the *why* discarded) and upward context is silent until delivery.
- **Command vs context culture:** Val traces a legacy "an order came from above, we do it" pattern (the "Boris era") that persists as the default operating mode.
- **Genchi Genbutsu (Toyota, "go and see")** and **Hansei (structured reflection):** with the company fragmented across home offices there is no "place" to go and see, and no reflection loop that reaches North America — nobody surfaces that a wrong path cost three days because a clarifying question was not asked. He also cites Amazon's silent-reading-in-meetings as evidence that even a perfect document package would not, on its own, produce a return flow of questions.

## Pavel's response and where the two landed (Mar-5)

The Mar-5 exchange **refined** the diagnosis rather than disputing it:

- Pavel **agreed** the return feedback loop does not reach North America with the right form or regularity, but added context: on genuinely contentious issues Minsk does **not** stay silent — it initiates meetings, almost always live conversations rather than comment threads, and roughly **90% of decisions on services and the GUI went through Val, Juan and the team**, usually over several iterations. So some two-way dialogue exists; the gap is that it is not systematic. [[raw/communication_break_down_Minsk-March-5-2026.md]] [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]
- Val's key distinction: **a point of contention is black-and-white and easy to resolve; the permanent state of work lives in the everyday feedback loop, and that is where it breaks** — not in contention. [[raw/communication_break_down_Minsk-March-5-2026.md]]
- Pavel reframed the structure: feedback loops **do** exist but are **fragmented by level** — one loop at the executive level, others among developers, QA, and Pavel/Irina — and each segment communicates within itself while signals between segments travel poorly. It is a classic hierarchical model where information moves vertically and gets **filtered at each layer**; the alternative (a flat organization where anyone shares context with anyone) is an open question about whether JVL is ready for it. Val located the break specifically at the **Minsk middle layer not transferring developers' accumulated context upward** across the boundary. ("Irina" here is the QA/middle-management counterpart to Pavel; by that context it leans [[wiki/people/irina-shishko.md|Irina Shishko]], but the two-Irina cluster is not force-resolved.) [[raw/communication_break_down_Minsk-March-5-2026.md]] [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]
- Both agreed the sharpest instance is **undocumented architectural decisions**: Minsk deliberates over subjects and arrives at fundamental choices that affect the company for years, and those decisions and their reasoning are usually **not documented or communicated** to North America. Pavel added that many individual questions seem minor enough to resolve locally, but undocumented they **accumulate into critical changes** later perceived as deviations from the original requirements. (Val softened his own "nowhere and never" to Pavel's more accurate "not always" and "not properly.") [[raw/communication_break_down_Minsk-March-5-2026.md]] [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]
- **Where they landed:** the diagnosis shifted from "Minsk is silent" to a more precise statement — **Minsk communicates internally, but the output of that communication, especially architectural decisions and accumulated local judgments, does not cross the boundary to North America in documented form.** The loops are not absent; they are fragmented and filtered. The task is therefore **not to create communication from nothing but to bridge the segments** so what Minsk already discusses becomes visible to North America. Pavel expressed genuine willingness to improve and simplify processes, increase reliability and add transparency. [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]

## Open questions

- What does "bridging the segments" look like in practice — the concrete mechanism to make Minsk's internal decisions (especially architectural ones) visible to North America in documented form? Named as the explicit next step, undefined as of Mar-5. [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]

## Sources

- [[raw/communication_break_down_Minsk-March-5-2026.md]]
- [[raw/Describing_the_cultural_problem_in_Minsk.md]]
- [[raw/Mutual_standing-Communication_breakdown_Minsk.md]]
