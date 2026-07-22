---
type: meeting
title: Framework Changes / Tasks and Management — a spec-driven workflow for design-driven framework changes (Nov 27 2025)
date: 2025-11-27
aliases: [Framework Changes Tasks and Management, framework change workflow, design-driven framework changes, requirement-spec-feature-test workflow, Reich Rises, IP 327]
source-count: 2
open-commitments: 3
open-questions: 1
---

# Framework Changes / Tasks and Management — a spec-driven workflow for design-driven framework changes (Nov 27 2025)

**Date:** 2025-11-27 · **Two recording segments under the same base name** — part 1 (03:33 PM header, 33m 14s): [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]; part 2 (04:31 PM header, 13m 35s, explicitly labelled "part-2"): the same three plus [[wiki/people/lena.md|Lena Zhukova]]. Russian, with some English. This stub cites both segments; because it draws on more than one source, citations are inline per claim (§3).

**§12 multi-segment decision — ONE meeting in two parts.** Evidence: (1) identical recording base name "Framework Changes – Tasks and Management"; (2) part 2 is explicitly filename-labelled "**part-2**"; (3) the two segments are **~1 hour apart** (03:33 PM / 04:31 PM); (4) **part 1 ends with Val saying he will pull the transcript and "schedule a meeting in half an hour with Lena"** [[raw/Framework Changes – Tasks and Management.md]], and **part 2 opens with Val linking back to "our first meeting" with Lena now present** [[raw/Framework Changes – Tasks and Management - part-2.md]] — part 2 is that follow-up. Same topic throughout (the framework-change workflow). Treated as **one meeting, two segments → one stub, facts recorded once**. (Part 1 is Val working the process out with Pavel and Irina; part 2 presents it to Lena for sign-off.)

**§12 corpus-wide cross-check — distinct meeting.** Ran `qmd update` and grepped the whole wiki: neither segment is cited anywhere but `log.md`, and no existing page carries this Nov-27 framework-change-workflow content. It **extends** the spec-driven-development thread (see below) but is a distinct new session. Confirmed new.

## What the meeting is about

Val wants to replace the **informal, undocumented way framework changes happen today** — requested by the graphics/design department through a "secret, magic path" with no clear "conductor" [[raw/Framework Changes – Tasks and Management.md]] — with a **documented, specification-driven workflow**. His governing principle, stated twice: **"if it is not written down somewhere, that truth does not exist; if you cannot show where it is written, it does not exist"** — a phrase he says he picked up from an earlier conversation and now hears constantly [[raw/Framework Changes – Tasks and Management.md]]. This is a direct continuation of the [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md|capability/GitHub-mapping + spec-driven-development decision]] (the Aug–Sept "record the conversation → AI writes the spec" method), now applied specifically to **framework changes stimulated by the design department**.

## Current state (the problem)

- Framework changes of **any size** originate from **designers' requests**; when something big is needed, **Lena** raises it [[raw/Framework Changes – Tasks and Management.md]].
- A **weekly meeting** already exists to align Lena's design department with the development department — attendees named: Lena, Yulia, Nastya, Igor, Ira/Irina, sometimes Sasha — but it is **mostly about the state of Omni** and coordination, not a structured intake for framework work [[raw/Framework Changes – Tasks and Management.md]].
- Today the spec is discussed **only verbally** and everyone writes it down in their own shorthand, so it drifts and gets re-litigated later ("file" becomes "fal," "lies here" becomes "l") — the failure Val wants to end [[raw/Framework Changes – Tasks and Management.md]].

## The proposed workflow (recorded once)

1. **Design + developer + tester meet; the designer explains verbally, and the conversation is recorded.** Lena (or the relevant designer) explains what she needs, in any language; the developer (Anton or Igor Metelski) and the tester (Ivan) can ask clarifying questions in the **same conversation** — the more precision captured in one recording, the better (make it longer if needed) [[raw/Framework Changes – Tasks and Management.md]] [[raw/Framework Changes – Tasks and Management - part-2.md]].
2. **The designer turns the transcript into a requirements list via AI**, then corrects it (AI over-suggests; it must be trimmed) [[raw/Framework Changes – Tasks and Management.md]] [[raw/Framework Changes – Tasks and Management - part-2.md]].
3. **The developer turns {transcript + requirements} into an engineering specification via AI** ("make me a specification, engineering, for my framework"), producing one revision of the spec; gaps can be talked through with Pavel or [[wiki/people/efim-podvoiski.md|Efim]] and those conversations are also recorded [[raw/Framework Changes – Tasks and Management - part-2.md]].
4. **The developer breaks the spec into features; each feature gets acceptance criteria** [[raw/Framework Changes – Tasks and Management.md]] [[raw/Framework Changes – Tasks and Management - part-2.md]].
5. **The tester (Ivan) turns {transcript + requirements + spec + acceptance criteria} into test cases via AI**, which combine into tests for the functionality [[raw/Framework Changes – Tasks and Management.md]] [[raw/Framework Changes – Tasks and Management - part-2.md]].
6. Result: **documentation plus the framework changes** needed to implement all the graphic changes — achieved without weeks of writing everything by hand ("if we write this all by hand we are talking about weeks; we don't have that time") [[raw/Framework Changes – Tasks and Management.md]].

## The AI tooling behind it

- Val uses **ChatGPT with a direct integration to the Atlassian MCP**; ChatGPT had to be put into a **"development mode,"** which **[[wiki/people/andrey-bosik.md|Andrey Bosik]] configured for him** [[raw/Framework Changes – Tasks and Management.md]].
- With it Val can pull all the Atlassian/Jira information, **overlay a conversation transcript onto the facts**, determine which **IP (Jira issue) number** it belongs to, **highlight conflicts**, produce a synopsis, and list **what the conversation did not cover** [[raw/Framework Changes – Tasks and Management.md]].
- Aside: Val also uses AI to **name meetings and Jira issues consistently** so the calendar, the chat and Jira all carry the same title — otherwise things are hard to find later [[raw/Framework Changes – Tasks and Management.md]].

## Jira structure named, and the "Reich Rises" rename

- The hierarchy Val walked: **IP 90 = the application**; under it **IP 747 = the "Systems" definition**; under that either **IP 726 = Omni progressive** or **IP 327 = Reich** (the Reich game framework) [[raw/Framework Changes – Tasks and Management - part-2.md]].
- Val proposed **renaming IP 327 to "Reich Rises"** for clarity/focus [[raw/Framework Changes – Tasks and Management - part-2.md]].
- **Scope: the workflow applies to both frameworks — Omni and Reich Studio.** The old framework (Reich Studio) can't implement things planned for the new one (Omni), but **kino (cinema) games** — new game types — will force changes into the old Reich Studio framework whether JVL likes it or not [[raw/Framework Changes – Tasks and Management - part-2.md]].

## Roles and assignment

- **Lena** owns the **requirements** (design side); **[[wiki/people/pavel.md|Pavel Frolov]]** owns the **specification and the planning/scheduling** of the work — Lena "hands the reins to Pavel." Val wants Pavel to lead the framework-change flow but **not be over-loaded** (he and Irina have many other tasks), so the day-to-day is pushed to the developer/tester pair [[raw/Framework Changes – Tasks and Management.md]].
- **[[wiki/people/anton-leshkevich.md|Anton]]** is currently the **less-busy developer** (he finished the framework preparatory work and hadn't been assigned tests yet), so Lena's framework changes are assigned to him — Val's principle: an idle capable person should be put to use ("a person who isn't loaded — you must harness his capacity") [[raw/Framework Changes – Tasks and Management.md]]. For **Reich**, the developer is **Anton or [[wiki/people/igor-metelski.md|Igor Metelski]]** (Piratka does not work on Reich Studio) [[raw/Framework Changes – Tasks and Management.md]] [[raw/Framework Changes – Tasks and Management - part-2.md]].
- **[[wiki/people/ivan.md|Ivan]]** writes the **tests** (at the merge/commit stage) [[raw/Framework Changes – Tasks and Management.md]].
- Val wants **only two people** talking on any given change — the fewer people involved, the better [[raw/Framework Changes – Tasks and Management.md]].
- **Lena does not know the functional requirements and does not attempt an engineering approach** — she describes what she needs in words; that gap is exactly what the requirements-then-spec chain is meant to bridge [[raw/Framework Changes – Tasks and Management.md]].

## Personnel note

- Val wants to **promote Natasha into a more senior Production Manager role** — he likes that she has ambition, wants to prove herself and wants to earn, and wants to "harness" that drive; Nastya and Yulia are also in the production/design mix [[raw/Framework Changes – Tasks and Management.md]]. (No compensation figures stated — see §15.8.)

## Output

- Val will **generate the transcript and a written summary and distribute them**; **Lena asked specifically for a written summary organised by bullet points** (not just video) so each lead can pass a short bulletin to their own people [[raw/Framework Changes – Tasks and Management - part-2.md]].

## Open commitments

- [ ] Lena Zhukova — for each framework change, produce the **requirements list** from the recorded design conversation (AI-drafted, then corrected) — due per change — [[raw/Framework Changes – Tasks and Management - part-2.md]]
- [ ] Pavel Frolov — own the **specification and scheduling** of framework changes; slot the requirement work under the right IP and plan the timeline — due ongoing — [[raw/Framework Changes – Tasks and Management.md]]
- [ ] Val Levitan — generate the transcript + a **bullet-point written summary** and distribute it to the leads — due after the meeting — [[raw/Framework Changes – Tasks and Management - part-2.md]]

## Open questions

- Which **"Dima"** writes the framework-change requirements that **"Sasha Belyatko"** implements (part 2: "Dima writes the regulation, Sasha Belyatko [implements] in the framework")? By the design/Liquid-Glass context this is plausibly **Dima Khandov** (3D graphics) and **Sasha = [[wiki/people/alexander-biratka.md|Alexander Biratka]]** (the Omni framework author; "Belyatko" reads as a transcription of Biratka) — but neither is force-matched. Queued (Tier A / Tier B). [[raw/Framework Changes – Tasks and Management - part-2.md]]

**§15.8:** clear — process/workflow, tooling, Jira-structure and role-assignment content only. Val's wish to promote Natasha and his remark that she "wants to earn money" are stated **without any figures**; no per-person compensation is recorded.

## Sources

- [[raw/Framework Changes – Tasks and Management.md]]
- [[raw/Framework Changes – Tasks and Management - part-2.md]]
