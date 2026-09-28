# Meeting Summary — Daily Standup meeting

**Date:** September 22, 2026, 4:48 AM - 5:30 AM Eastern
**Duration:** approximately 42 minutes
**Attendees heard:** Pavel Frolov, Irina Shishko, Dmitri Kovalchuk, Dzmitry Chudzinau, Alexander Biratko, Alexey Khamin, Daniil Stauskiy, Evgeny Kharetski, Sergey Tsimanov, Vladimir Samusenko, Ivan Shpak
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026]]
**Source meeting:** Daily Standup meeting — Microsoft Teams

## Summary

A normal round-the-table standup that turned into two longer arguments: what status a capability should carry while it is being tested, and how to handle the FlexPort screens Andrei delivered as an HTML page.

**Round-the-table.**
- **Alexander Biratko** finished the touch panel and the move to the new monitor — it works and looks right. He is now on CAP-137, software antivirus management, creating features to port the mechanism already built in FlexIQ (CAP-122). He asked whether the capability itself sits on him or only its features; Pavel confirmed he owns the capability.
- **Alexey Khamin** is moving pull requests from Versky into Pavel's branch for testing.
- **Anton** is absent — he arranged leave and will work Saturday.
- **Daniil Stauskiy** is porting buttons and the repository into the framework, and is blocked on the game-selection screen — it does not exist in the repositories. Alexander explained his original architecture: the game select screen should load into the game as a separate module, the way the framework loads a game, and be pointed at the game resources to draw the previews. Agreement: Daniil and Alexander talk the architecture through first, decide whether it is a separate repository or an artefact built by default in the framework repository, and prove the flow with two duplicated games before worrying about art.
- **Dzmitry Chudzinau** — updates almost frozen, the kernel is rebuilding from the SDK. He picked his features, is deploying to STG in parallel, and works CAP-152 next. He warned the PE resealer build will probably break; each overlay has to be moved separately, which Alexander can do for FlexPay.
- **Evgeny Kharetski** re-rolled the new version yesterday, quiet so far, now on the contract (LGS-1185).
- **Irina Shishko** is finishing the differences in the GKM3 document, then looking at the MVP1 capability requirements. A maths error surfaced in Clover Fortune; Ivan is installing the version and she will work it with him.
- **Sergey Tsimanov** finished the export block and fixed the connection failure. He is now on forwarding and collecting metrics for the modem connection. He asked whether the metrics should go through Grafana at all, since today only logs go there. Dzmitry warned there is no time for this before the 1st. Sergey also asked whether he may change platform SDK 35.68 — Claude reports no signal-to-noise parameter for WiFi. Pavel approved adding it but noted WiFi is barely implemented and is definitely not MVP1.
- **Vladimir Samusenko** worked on the FlexPort contracts and chose Syncope for describing them; he lacks the expertise to verify it himself and will send a pull request to Pavel. He raised that Daniil has no access to the JVL knowledge repository and therefore did not know the data-contract standards exist — two people did the same task in parallel and produced two different results.
- **Ivan Shpak** needs the CMS server component release done today — he asked yesterday and it is still not out. Pavel assigned it to Sergey as urgent.
- **Dmitri Kovalchuk** has a draft report ready: personal mailouts to each person listing overdue tasks, tasks ending today, tasks running more than 14 days, tasks whose parent is already closed but which are still open, and tasks with no end date. Backlog items are excluded — only To Do. He wants feedback before it goes out.

**Argument 1 — capability status while testing.** Irina flagged CAP-122 sitting In Progress with all its features closed. Dmitri said capabilities are not closed until tested or a test plan is written, and proposed a new status. Pavel resisted adding statuses ("too many statuses"), first suggesting the capability just stay In Progress with a visible testing task under it. Irina argued that In Progress reads as "development not finished" and hides the real state from her. Dmitri wanted two statuses — development done, and testing running. Alexey framed it as a stabilisation stage. The group ended on: one status after In Progress (Request Review or similar) is probably needed, and under it there must be a test plan or an integration-test task — if nothing sits under it, it has no business being in that status.

**Argument 2 — what is actually testable.** Dzmitry challenged the premise that features can be tested at all: a feature like the AWS class one crosses services with no access from the test side. He argued the capability is the unit that gets tested, because that is the user's view; features are intermediate points from A to B. Pavel conceded that where a feature implements one acceptance criterion it could be tested, but acceptance criteria hang on requirements, not features, and several features can implement one requirement — so the requirement cannot be fully tested feature by feature. Agreed landing point: at feature level only unit or contract tests; the capability level is where integration testing happens, and autotests are written in parallel with development rather than after it. Dzmitry raised the unresolved case: Andrei is adding a capability of user screens up to card issue, while balance recalculation and wallet interaction sit in a different capability — neither can be tested without the other, and there is no capability describing the overall flow. Pavel will ask Andrei about it at today's meeting.

**Argument 3 — the FlexPort GUI.** Andrei published the FlexPort screens as an interactive HTML page. Pavel says the workflow matches about 95%; button positions, fonts, and similar do not. He proposed two stages: first move the existing components to match Andrei's layout, which Claude should handle easily, then a full rework of colours and button shapes. Vladimir objected on principle — the design should be in Figma with design tokens and a component library, not an HTML page that will be lost and never found again, as has happened before. Irina said they cannot now tell Andrei to redo it all in Figma. Vladimir accepted he will do the work and was speaking about the future approach. Pavel added a technical caveat: FlexPort screens are not HTML at all — they are built with the TouchGFX Designer utility and its own markup, so converting from HTML to code may be easier than from Figma to code. Vladimir will install TouchGFX Designer (Pavel will send the installer, since it is not available on the ST site), pull the FlexPort project, import it, and see what is workable. Pavel also noted the existing Figma given to the external Evgenys and what is drawn now are two different things.

**Housekeeping.** Pavel cannot move a story from Request Review to Complete — something in the HFM project settings. Dmitri will look at it later.

## Undertakings

| # | Who | What | Due | Priority | Context |
|---|-----|------|-----|----------|---------|
| 1 | Sergey Tsimanov | Release the CMS server components that were changed | Today | Critical | Ivan: "absolutely must be done today"; asked yesterday, still not out |
| 2 | Daniil Stauskiy + Alexander Biratko | Talk through and write down the game-select-screen architecture; decide separate repository or framework-repository artefact | Not set | High | Daniil is blocked — the screen does not exist in any repository |
| 3 | Pavel Frolov | Ask Andrei at today's meeting how the cross-capability flow is tested, and why no capability describes the overall screen flow | Today | High | Dzmitry: screens and balance recalculation are in different capabilities and cannot be tested apart |
| 4 | Pavel Frolov | Create the GUI conversion task for Vladimir once Andrei has linked his capability | After Andrei's meeting | Normal | No new capabilities are linked to that item yet |
| 5 | Pavel Frolov | Send Vladimir the TouchGFX Designer installer | Today | Normal | Not downloadable from the ST site |
| 6 | Vladimir Samusenko | Install TouchGFX Designer, import the FlexPort project, and report what can be worked with | Not set | Normal | Stage one is only moving components to Andrei's layout |
| 7 | Vladimir Samusenko | Finish the contract tests, review, and send the pull request to Pavel | Not set | Normal | He lacks the expertise to verify Syncope alone |
| 8 | Dmitri Kovalchuk | Check why a story cannot move from Request Review to Complete in the HFM project | Not set | Low | Pavel hit it this morning |
| 9 | Dmitri Kovalchuk | Confirm Daniil's access to the JVL knowledge repository — it should be open to everyone by default | Not set | Normal | Its absence caused two divergent data-contract results |
| 10 | Dmitri Kovalchuk | Finish the overdue-task report and send personal lists to each person | Not set | Normal | Draft may still contain wrong or missing logic |
| 11 | Alexander Biratko | Build the antivirus-management features on CAP-137 by porting the FlexIQ mechanism from CAP-122 | Not set | Normal | The CAP text names FlexIQ as the source |
| 12 | Alexander Biratko | Move the overlay for FlexPay when the PE resealer build breaks | Not set | Normal | Dzmitry expects the break |
| 13 | Irina Shishko + Ivan Shpak | Work the Clover Fortune maths error | Not set | High | Surfaced when Ivan installed the version |
| 14 | Sergey Tsimanov | Add the signal-to-noise parameter to platform SDK 35.68 | Not set | Low | Approved by Pavel; WiFi is not MVP1 |

## Decisions

- Alexander Biratko owns CAP-137 as a whole, not only its features.
- A status between In Progress and Complete is needed (Request Review or similar) to show development is finished and testing is running — but only one new status, not two. Pavel rejected adding more.
- Whatever that status is, a capability sitting in it must have a test plan or integration-test task under it; if nothing is under it, it does not belong there.
- Testing is done at capability level, not feature level. Features get at most unit or contract tests; integration tests belong to the capability.
- Autotests are written in parallel with development, not after it.
- FlexPort screen rework is split into two stages: move existing components to Andrei's layout first, then rework colours and button shapes.
- Design work will not be sent back to Andrei to redo in Figma; the HTML page is accepted for this round, with Figma and design tokens as the intended future approach.
- FlexPort updates stay out of MVP1 and go to MVP2 — though Dzmitry said a new list arrives every day, so this is not settled in practice.
- The overdue-task report covers To Do items only; backlog is excluded.

## Open Questions

- What to call the new status — Request Review, Integration, Stabilisation. Not settled.
- How to group capabilities so a flow can be laid out cleanly against a single test plan. Dzmitry could not see how; to be raised with Andrei.
- Whether modem connection metrics should go to Grafana at all, and whether there is time before the 1st. Sergey questioned the need; Dzmitry said there is no time.
- Sergey asked where the term MVP even comes from here, since this looks like a finished product rather than a minimum one. Not answered.
- Whether the design tokens and component library from the earlier Figma can still be used, given the delivered Figma and the current screens are two different things.
