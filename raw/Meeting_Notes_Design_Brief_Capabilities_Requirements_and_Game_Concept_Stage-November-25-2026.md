# Meeting Summary — Design Guide to Capabilities list - REQ as part of brief and CAP
**Date:** November 25, 2026, 7:59 AM Eastern
**Duration:** 1 hour 51 minutes
**Attendees:** Val Levitan, Evgeny Kharetski, Alexander Biratko, Irina Shishko, Pavel Frolov, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Design_Brief_Capabilities_Requirements_and_Game_Concept_Stage-November-25-2026]]

## Summary

**Why the meeting.** Val opened with yesterday's talk with Evgeny. Evgeny thinks one design brief needs only one capability: "we make a game" (a set of artifacts). The tool then creates features, each with a feature branch, and the capability closes when all artifacts are made. Val said he has no strong argument against it. But a bigger question came up: where use cases and requirements fit, and how they point to capabilities.

**Standards come after the logic.** Evgeny said this does not fit the current standards (requirements must be created, and every feature must have a due date). Irina and Val said: do not fit the process to the standards now. First agree on the right process. Then fix the standards.

**Alexander's proposal: drop the capability layer.** Alexander said the current structure is slow and heavy at today's fast speed of development. One capability links about 10 requirements, each with about 10 acceptance criteria, and the capability may meet only 2 of them. It is hard to know what to test. He proposed:
- Keep only a brief (a versioned specification in the repository) and features with acceptance criteria. Claude updates the brief from meeting transcripts and checks pull requests against it.
- Or turn the hierarchy around: the requirement is the parent, and capabilities and features sit under it.
- Or copy requirements per product instead of reusing them.

**Why the team kept requirements and capabilities.** 
- Val: the product owner talks to the market, not to developers. He writes use cases and requirements in plain words. From them he defines capabilities and gives them to Pavel. Developers turn capabilities into features. The capability is the "touch point" where the market side and the development side meet.
- Val: Jira also holds the planning work of non-developers (service, market research). He wants to leave Jira and move to GitHub one day, but not now. Breaking this step now would break other work he is trying to sync.
- Irina: requirements are reused. With 1,000 games over time, 90% repeats. Tests written for a requirement stay in the right place and show that a new version did not break old acceptance criteria.
- Andrei: "We do not like everything either, but nobody has found a better solution yet."
- Val: today's system is better than two years ago, when it was very bad. Alexander agreed it is better but wants it better still. He said the proposals he made were all rejected.

**What is tested.** Pavel: the capability is checked; it closes only when all development tasks under it are closed and all automatic tests pass. Val agreed a capability closes only after the tests pass. But Val said the tests check the acceptance criteria in the requirements, not the capability itself.

**The real problem: requirements conflict.** Pavel said each capability got its own requirements, made separately. So requirements from different capabilities overlap and can break each other. Irina said this is what slows her: new requirements contradict old ones, and today she could not release a version because of it. Val said JVL started writing requirements only 1 to 1.5 years ago, in the middle of development, with no base built over the years.
- Pavel proposed an agent that checks all requirements (also non-functional ones) before development, to remove overlaps and conflicts. He thinks this can fix about 80% of cases.
- Val would close conflicting items automatically ("easier to drop and open new"). Irina and Alexander did not want automatic closing. Irina wants a person to review what the agent proposes. Not decided.
- Val compared it to his own standards work: the more standards he writes, the more conflicts and gaps Claude finds. He said the company needs a few agents in a constant loop that groom standards and requirements.
- Val mentioned a proposal: write requirements from the existing code, because the code is the source of truth for machines already in the field.

**How tests must be written.** Val said when Claude writes acceptance tests, it must be told clearly: do not look at the code and do not look at the prose. Use only use cases, requirements and acceptance criteria. Only then can a test find the gap between what was planned and what was built. If Claude reads the code, the test is wrong. Irina said she tests against acceptance criteria, and Claude reads the code only to find hooks. Alexander said with today's structure Claude does not have enough data to do it any other way. Pavel and Alexander said tests may need contracts (hooks, emulators, stand setup). Val said he must think about contracts.

**Use cases are missing.** Pavel said JVL has almost no use cases as a separate item. They sit inside capabilities as a few sentences. Irina agreed. Andrei wrote use cases for Transactional at the start (in Confluence), but nobody used them later. Val said this may be one of the problems. His example: when a standard needs data from Business Central that the MCP does not have, Claude writes a use case and Val sends it to Nathan, who extends the MCP. This works well.

**When a requirement changes.** Val: a closed capability is never reopened. It is finished. To change the product, edit the current requirement and its acceptance criteria and open a new capability for the fix. His example: the Transactional board had revision 1, then revision 2 with a multiplexer for printing, then revision 3 without the printer. Each revision's capability "died" and a new one was made. Pavel said there is already a "capability amendment" type for such cases. Alexander worried Claude will still find old closed capabilities in Jira and follow wrong context. Irina said closed items show the history of each version in the field.

**Back to the brief.** Val said it seems one capability per brief is enough: "make a set of assets for this brief." But he had a doubt: to write a brief you must know what the market needs, and today that is described by use cases and requirements. Pavel said a brief is in effect a set of requirements from the market.

**Val's four stages for the studio** (all agreed "as a concept"):
1. Today: the studio is a front-end tool to copy games. It has the layers of existing games. The designer can only repeat them with new stories and artifacts.
2. Add new layers, timing diagrams and physics (transitions).
3. Take signals from the machines and make new stories from them.
4. Film other companies' machines, decode the video into JVL's layers, timing, geometry and physics, and build the missing layers automatically.
Stages 3 and 4 may swap.

**Signals instead of people.** Val's long goal: machines send signals (math, statistics, hardware). JVL turns them into a "market request" and then a design brief automatically, and the game is built automatically. A self-learning loop. Today these signals do not exist. They come from people (interviews, field visits, photos, video), so JVL needs a very strong product owner.

**Game concept, game design, game production.** Val showed the value stream: game concept → game design → game production. Mechanics (reels, symbols, expanding wild, bonus, 3x5) are set in game concept. Story and symbols are set in game design. Production is the builder. Val said the studio works in game design and the builder replaces production.

**Evgeny's question about his agent.** Evgeny asked what his agent is for if everything is already decided before a person comes to it. Andrei: it collects everything and checks nothing is missing. Val: the agent turns a person's "analog" idea into "digital" structure, by guiding questions. By the end the group agreed: the brief is the result of the game concept stage and the entry point to the studio. Andrei, Pavel and Irina said Evgeny's agent covers the game concept stage, and the brief is its output.

**Open point at the end.** Val asked what artifacts mark the end of the game concept stage. Evgeny said the only result is the brief document. Val said there must be some artifacts or parameters. This was not answered. Val stopped the meeting and said he will schedule it again.

## Decisions Made

- **Agree the right process first, then correct the standards. Do not fit the process to today's standards.** (Decided by Val and Irina)
- **Keep the current structure: use cases and requirements with acceptance criteria on the market side, capability as the touch point, features on the development side.** Alexander's proposals to drop or invert the capability layer were not taken. Alexander did not agree. (Decided by Val, supported by Irina, Pavel and Andrei)
- **A closed capability is never reopened. A change means editing the current requirement and acceptance criteria and opening a new capability.** (Decided by Val; Pavel: "Okay, accepted")
- **Acceptance tests must be written only from use cases, requirements and acceptance criteria. Claude must be told not to look at the code or the prose.** Contracts are still open. (Decided by Val)
- **The design brief is the result of the game concept stage and the entry point to the studio. Evgeny's agent covers the game concept stage.** (Agreed by Val, Evgeny, Andrei, Pavel and Irina)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Schedule this meeting again | TBD | Normal | Meeting stopped before the brief question was answered |
| 2 | Val | Think about contracts (hooks, emulators) in writing acceptance tests | TBD | Normal | Val: "I must think about this" |
| 3 | [Unassigned — needs clarification] | Define what artifacts mark the end of the game concept stage (the input for the game brief), after listening to the transcript | Before the next meeting | Normal | Val: "I leave you with this topic" |

## Open Questions

- Does one design brief need one capability ("make a set of assets") or more? Val said it seems one, then raised a doubt. Not decided.
- What artifacts or parameters are the result of the game concept stage, besides the brief document?
- Pavel's requirements-check agent: who builds it, and do conflicts close automatically (Val) or after a person's review (Irina, Alexander)? Not decided.
- Val's idea of grooming agents in a loop for standards and requirements. No owner.
- Evgeny raised that the standard says every feature must have a due date. Not answered.
- Irina asked if "Closed" means released to market and "Complete" means tests passed. Not clearly answered.
- Heard unclearly: "IP 531" (concept design stream in Jira); "Liquid" (a storage Val named); "origin agent"; "mutagus" (Alexander's Transactional example); "capability amendment" type made by "Andrei or Dima"; "Michael" (producer); "Nathan" (writes the Business Central MCP); "Georgia COAM V43 Nova, class A" (Val's backlog example); "Elena" (Val, likely meant Irina).
- The Teams recording is 2h38m long, but the transcript timestamps end at 1:51:16.

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, ~12:30 PM Eastern*
*Source meeting: Design Guide to Capabilities list - REQ as part of brief and CAP*
