# Meeting Summary — Games conversion experiment: GitHub consolidation, Jira project, capabilities and requirements
**Date:** September 25, 2026, 9:02 AM – 9:43 AM Eastern
**Duration:** About 41 minutes
**Attendees:** Val Levitan (organizer, chair), Igor Metelski, Andrei Bosik, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Games_Conversion_Repos_Jira_Capabilities-September-25-2026]]

## Summary

Held in Russian. Speech recognition is poor in places (many product names are garbled, for example "нолочь" for knowledge, "рейдж" for RAGE).

**Why the meeting.** Val sent an email asking for repositories to be created. Andrei Bosik said the team did not create them yet, because there were open questions about where things go. Igor Metelski presented the questions.

**What Igor's work produced.** Igor ran experiments on (1) converting RAGE games to NOVA and (2) making vertical games from horizontal ones. From this work he made a glossary, a list of ADRs, and a document with requirements for art: geometry of elements and timing of elements. Claude also wrote helper tools during the work: a converter (for example for the Dragon experiments) and small scripts, such as a script that takes screenshots.

**Where documents go.**
- **Glossaries and standards** go into the **knowledge repository, in the "standards" folder** (Val; Andrei, Pavel, Irina agreed).
- **ADRs live next to the code.** ADRs about one game go into that game's repository (with links to the game's SVN repository). ADRs about the common framework and the conversion procedure go into the **NOVA framework repository**. Pavel: put links to SVN in the ADRs, commit nothing to SVN, commit only to GitHub.
- **Geometry standard.** Val sees it as a standard for the standards folder, which can be applied to any framework or platform. Pavel said it looks like a separate group, but he is not 100% sure. Val is also not 100% sure. Val said: do not invent anything exotic, do not add a new folder in the knowledge base; "better too much standard than diluted." He said the team can consult internally and he is flexible.
- **Format.** Igor planned to split the geometry document into text Markdown and separate HTML graphics. Val advised against this: convert the graphics into Markdown, because Markdown is easier for Claude and can be turned into any format.

**Converter tool.** Igor first proposed keeping the converter inside the repository of the game being converted, because each game has different scenes. Irina asked if the converter is still needed after a game is converted. Igor said no. Andrei asked how much of the converter is reusable between games (10% = not universal, 90% = universal); Irina said 70–80% is still universal. **Val: the converter has a finite life, so it should not mix with the main framework code. It gets its own Jira project number and its own repository, so it is easy to work with and easy to "bury" later.** Pavel agreed: a developer on a new game can point Claude to the converter repository.

**Small scripts.** Scripts like the screenshot script go into a **"tools" folder inside the related repository** (Pavel and Andrei already do this). Igor accepted this.

**Experiment is ending.** Val said the experiments proved themselves positively. **The experiment should end in "a couple more days":** distribute all results into the right repositories, document them, add the new standards, write prose, and conserve. If the company later wants to convert specific games, that is a separate project with a task schedule, assigned resources and a calendar. Igor said one item is still open: tests (E2E) based on capabilities, which he has started and must finish for a full flow. Val agreed.

**Capabilities and requirements (retroactive).** Igor has draft capabilities locally; they are not in Jira yet and may need updates. Val's process: write prose for the code that exists, go back to the capabilities, attach requirements with **acceptance criteria** (including non-functional requirements), and close the capabilities as done **retroactively**, based on today's code and prose. Igor wants this done properly in Jira; Val agreed. Val: acceptance criteria are **the only basis for automated E2E tests**, and prose integrates well with the acceptance criteria.

**Initiative vs project.** Val said he is confused about "initiative" and "project." Dmitri Kovalchuk: **project = repository**; an initiative joins several projects (he read the standard: an initiative is a long direction with several releases). Dmitri: initiative → capabilities → features → features live in projects. Pavel: the work is a project in Jira with a matching GitHub repository.
- **Structure agreed:** Pavel pointed to the existing initiative **"NOVA Gaming Platform Land-Based"**, with a capability **"RAGE to NOVA conversion"** under it. Under this, **two projects**: (1) **game conversion** (converting one format to another, e.g. horizontal to vertical, RAGE to NOVA) and (2) **a new development standard based on the geometric layout of objects on screen**. Igor asked about a third project for RAGE-to-NOVA; Val put all conversion into the one conversion project.
- **Dmitri Kovalchuk opens the two Jira projects; Andrei creates the repositories.** Dmitri: **create repositories first, then the Jira project**, because Jira project names match repository names. Val asked to put this order into the standard; Pavel said the naming rule is already there.

**Repository rule.** Val: each repository must be **zero-trust and fully autonomous** and contain its **data contract** (term given by Pavel).

**Igor's plan.** Split his one big ADR list by topic per repository (tools, framework, specific game) and commit per standard; write prose inside each repository next to the code; then finish the flow up to testing.

**Next meeting.** Igor asked for one week. Val said no weeks. **Next meeting: Wednesday, September 30, at 7:00** (Val checked the date; time zone not stated). Igor asked for a point-by-point list of what must be ready. Val said he will put the transcript into the meeting so the team can ask Claude to parse it.

## Decisions Made

- **Glossaries and standards go into the knowledge repository, "standards" folder** — keep standards in one place so Claude does not spread its attention. (Decided by Val Levitan; agreed by Andrei Bosik, Pavel Frolov, Irina Shishko)
- **ADRs live next to the code** — game-specific ADRs in the game repository; framework and conversion-procedure ADRs in the NOVA framework repository; SVN only linked, nothing committed to SVN. (Decided by Andrei Bosik, Pavel Frolov, Val Levitan)
- **The converter gets its own Jira project number and its own repository** — it has a finite life and must not mix with framework code; easy to retire later. (Decided by Val Levitan; Pavel Frolov agreed) Considered and superseded: keep the converter inside each game's repository (Igor's first proposal) — replaced by a separate repository.
- **Small helper scripts go into a "tools" folder inside the related repository** — no separate repository for a single script. (Decided by Pavel Frolov, Andrei Bosik; Igor Metelski accepted)
- **Geometry standard goes into the standards folder; no new folder in the knowledge base** — Val's view; Pavel and Val both said they are not 100% sure, and Val left room for internal consultation. (Decided by Val Levitan)
- **Keep the geometry document in Markdown; convert graphics to Markdown instead of a separate HTML** — Markdown is easier for Claude. (Val Levitan advised; Igor Metelski agreed)
- **The experiment phase ends in a couple of days** — results distributed into repositories, documented, conserved. Any future conversion of specific games is a separate project with tasks, resources and a calendar. (Decided by Val Levitan)
- **Structure: initiative "NOVA Gaming Platform Land-Based" → capability "RAGE to NOVA conversion" → two projects (game conversion; geometry-based development standard)** — Considered and superseded: a third separate RAGE-to-NOVA project (Igor) — folded into the one conversion project. (Decided by Val Levitan, Pavel Frolov)
- **Repositories are created first, then the Jira projects, with matching names.** (Decided by Dmitri Kovalchuk; Val agreed)
- **Capabilities are closed retroactively in Jira** after prose is written and requirements with acceptance criteria are attached; acceptance criteria are the basis for E2E tests. (Decided by Val Levitan)
- **Next meeting Wednesday, September 30, 2026, at 7:00.** (Decided by Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Create the repositories for the two projects (including the converter repository) | Before Sep 30, 2026 | High | Repos come before Jira projects; speech recognition unclear on this line |
| 2 | Dmitri Kovalchuk | Open the two Jira projects, named to match the repositories | After repos exist; before Sep 30, 2026 | High | |
| 3 | Igor Metelski | Split the big ADR list by topic and commit each part to the right repository (tools, NOVA framework, specific game) | Sep 30, 2026 | High | |
| 4 | Igor Metelski | Commit the glossary and the standards (including the geometry standard) into the knowledge repository "standards" folder | Sep 30, 2026 | High | |
| 5 | Igor Metelski | Finish the geometry document in Markdown; convert the graphics into Markdown | Sep 30, 2026 | Normal | Val's advice |
| 6 | Igor Metelski | Write prose in each repository, next to the code | Sep 30, 2026 | High | |
| 7 | Igor Metelski | Update the draft capabilities, move them into Jira, attach requirements with acceptance criteria (including non-functional), close the capabilities retroactively | Sep 30, 2026 | High | Drafts exist locally |
| 8 | Igor Metelski | Finish the flow up to E2E tests based on the acceptance criteria | Sep 30, 2026 | High | Already started |
| 9 | Val Levitan | Put the meeting transcript into the meeting so the team can ask Claude for a point-by-point list | Sep 25, 2026 | Normal | Igor's request |
| 10 | [Unassigned — needs clarification] | Add to the standard the rule "create repositories first, then Jira project names" | TBD | Low | Val asked; Pavel said the naming rule is already there [Needs Val's confirmation] |
| 11 | All attendees | Meet again | Wed Sep 30, 2026, 7:00 (time zone not stated) | Normal | |

## Open Questions

- Is the geometry document a standard (standards folder) or a separate group? Raised by Pavel Frolov; Val leans to standard and said the team can consult internally.
- Exact names of the two projects and their repositories were not set in the meeting. (The initiative name was taken from the existing list after Val said he could not name it.)
- Is the "repositories first, then Jira project" rule already in the standard? Pavel says yes; Val asked to add it.
- Time zone for the Wednesday 7:00 meeting was not stated.

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: Games conversion experiment: GitHub consolidation, Jira project, capabilities and requirements*
