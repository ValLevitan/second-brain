---
type: meeting
title: Nebraska release-schedule requirements walk-through — REQ-998 / 1007 / 1010 (Feb 27 2026)
date: 2026-02-27
aliases: [Nebraska release schedule Feb 27 2026, Schedule Nebraska Feb 27, REQ-998 audit ticket, REQ-1007 whole-dollar rounding, REQ-1010 Nebraska graphical skill, no liquid glass Nebraska, requirements to features process]
source-count: 2
---

# Nebraska release-schedule requirements walk-through — REQ-998 / 1007 / 1010 (Feb 27 2026)

A working call on the **Nebraska game-release schedule and requirements** (recording header **27 February 2026, 01:02pm**, 49m5s; §11 the header time wins over the `_080239` filename stamp). Attendees: [[wiki/people/val-levitan.md|Val]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/irina-shishko.md|Irina Shishko]]. This is the earlier, requirements-focused half of the day; the design detail behind these changes was worked out that evening on the [[wiki/meetings/2026-02-27-game-development-review.md|7:05pm game-development review]].

**§4 resolution — "Irina."** The QA/testing/certification-interpretation "Irina" here (walks the audit-ticket UI, tests the rounding behaviour, supplies attendant-screen screenshots) is [[wiki/people/irina-shishko.md|Irina Shishko]] (Director of QA), not the game-developer Irina Makarych, per the owner ruling 2026-07-18.

**§12 derived-document family (one meeting → one stub).** The transcript [[raw/Schedule_Nebraska-February-27-2026.md]] and its §3 derived summary [[raw/Summary_Schedule_Nebraska-February-27-2026.md]] are the same meeting; the summary is folded in rather than given its own page. Both cited (source-count 2), so claims cite inline per §12.

**Routing choice.** Nebraska already has a full project page — [[wiki/projects/nebraska-skill-market.md]] — which is the natural home for the release schedule, the three requirements, and the regulatory/lab detail; no new project page was created (a Feb-27 section was added there instead of `wiki/projects/nebraska-market-release.md`, per the "prefer reusing an existing page" instruction).

One-line purpose: reprioritize Nebraska to the forefront, walk the three engineering requirements, and set the plan to build the features into the next sprint and rush Eclipse approval — without waiting for liquid glass.

Substance is recorded where it belongs:

- **The three Nebraska requirements** — **REQ-998** (operator-requested audit ticket, manual print only via the setup/attendant menu, fields matching the South Dakota one, for Nebraska and Texas); **REQ-1007** (whole-dollar rounding on TITO cash-out tickets with an on/off toggle, fractional cents left on the credit meter to trigger the last-bet/risk feature); **REQ-1010** (the master requirement — remove the power meter, replace with a 50/50 icon selection, make the pattern-match skill prompt less visible; liquid glass deferred) — and the **no-liquid-glass-for-now decision** (it would add 30–90 days; without it the three REQs plus game changes submit to Eclipse in ~2 weeks), plus the Intralot CRC/checksum registration requirement → [[wiki/projects/nebraska-skill-market.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]] [[raw/Summary_Schedule_Nebraska-February-27-2026.md]]
- **The requirements→features workflow gap** — Val's difficulty understanding how written requirements get linked to Jira features (he sees "two parallel inventories"), Pavel's answer (a requirement, even published, isn't worked until someone creates a feature and schedules stories under it), and Val's conclusion that a missing **engineering/architecture-decision layer** should sit between requirements and features and that the linking bureaucracy should be handed to Claude → [[wiki/topics/ai-assisted-development.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]]
- **Marching orders** — Juan to groom the three requirements until Irina and Pavel have no questions; Pavel to create the linked features and schedule them into the next sprint (starting Thursday); Irina to supply attendant-screen screenshots for the audit-ticket flow — noted on [[wiki/people/pavel.md]] and [[wiki/people/irina-shishko.md]] (Feb-27). [[raw/Schedule_Nebraska-February-27-2026.md]] [[raw/Summary_Schedule_Nebraska-February-27-2026.md]]

§15.8 clear — RTP, schedule dates, JIRA/REQ keys and market economics only; no named-person compensation.

## Sources

- [[raw/Schedule_Nebraska-February-27-2026.md]]
- [[raw/Summary_Schedule_Nebraska-February-27-2026.md]]
