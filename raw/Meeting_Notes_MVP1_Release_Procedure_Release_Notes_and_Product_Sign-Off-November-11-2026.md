# Meeting Summary — MVP1 Release, MVP2 Scope and CAPs/REQs review
**Date:** November 11, 2026, 8:31 AM – 8:55 AM Eastern
**Duration:** ~24 minutes
**Attendees:** Andrei Klimovich (organizer), Irina Shishko, Pavel Frolov, Ivan Shpak, Dzmitry Chudzinau, Val Levitan
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_MVP1_Release_Procedure_Release_Notes_and_Product_Sign-Off-November-11-2026]]

## Summary

Andrei had only 30 minutes, so the meeting covered MVP1 only: what stops the official release. In Jira the capabilities are "Complete", not "Closed", and the version is still unreleased. Ivan (release manager) was invited.

**Conditions for release.** Irina: capabilities move to Closed only when all work is done. Pavel: the production artifacts must be on the production store, and there must be release notes. Ivan's release notes compare Jira features and capabilities with what is written in prose and with autotest results. They show 37 capabilities, 36 closed; Irina said the last one is closed too, and Ivan will re-check. The last IQ build on prod is from November 3; Pavel and Irina confirmed it is the latest release build — later builds were for development only and never went to prod.

**Link between build and release notes.** Andrei, as product owner, cannot tell from prod which build is the release. CAP-311 required the shipment page to show the release or link to its notes; this is missing. Dzmitry said it was not planned for MVP1 and suggested MVP2. Andrei said it formally was in CAP-311 (already closed) but accepted living with it. As a fix for now, Ivan will put the build names at the top of the release notes. For IQ the build reference is enough; for the port the version label is unclear ("v1" plus a commit instead of the full version) and must be made clearer.

**Order of steps.** Irina asked whether Andrei accepts the release before capabilities are closed. Pavel: a build on the prod server does not by itself make it installable. Andrei reviews the release notes, installs the software himself (Flex IQ, Flexport), checks it against requirements and services. If he finds gaps, work continues in the same capabilities, or — since Closed capabilities are not reopened, as agreed — a new "amendment" capability is opened. Agreed flow: Ivan updates the release notes today; Andrei reviews and gives a go/no-go; then the release manager moves all capabilities to Closed and releases the version in Jira. Andrei expects the green light by tomorrow evening if all is well. He will also check this against best practices today.

**Val's points.** Val asked why the team invents its own process: the world already does this, there are standards (Jira, GitHub), "we just did not finish reading the book." He said the wrong people were in this meeting: developers like Sasha, Dima and Sergey are not needed here, while Andrei Bosik (CI/CD) was missing. Val asked if Andrei had installed IQ; Andrei had not installed the latest build yet, but downloaded the builds and checked CAP-311 download from the interface.

Ivan offered to shorten the release-notes text; Andrei said no, keep this first version and correct later after comments. MVP2 review moves to tomorrow morning. After the meeting Val asked Pavel to call him.

## Decisions Made

- **MVP1 release flow:** Ivan updates release notes → Andrei (product) reviews and gives go/no-go → release manager moves capabilities to Closed and releases the version in Jira. (Agreed by Andrei, Pavel, Irina)
- **Closed capabilities are not reopened; gaps found later go into a new amendment capability.** (Pavel and Irina, confirming an earlier agreement; Andrei accepted)
- **Release notes show the build names at the top** in place of the missing CAP-311 build-to-notes link for now. (Andrei and Irina)
- **Release notes stay in their current length for this first run.** (Andrei)
- **MVP2 review meets tomorrow morning (Nov 12).** (Andrei)

*Considered and superseded: holding MVP1 for the CAP-311 build link — accepted as missing; Dzmitry proposed MVP2 for it.*

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Ivan Shpak | Update the MVP1 release notes with build names at the top; re-check the 37th capability | Nov 11, 2026 | High | Release gate |
| 2 | Ivan Shpak | Make the port version label clear in the release notes (full version, not just "v1" + commit) | Nov 11, 2026 | Normal | Andrei found it unclear |
| 3 | Andrei Klimovich | Review the release notes, install the builds and give go/no-go | Nov 12, 2026 (evening) | High | "Tomorrow evening we get the green light" |
| 4 | Andrei Klimovich | Check the release procedure against best practices | Nov 11, 2026 | Normal | After Val asked to follow standards |
| 5 | Ivan Shpak | After green light, move all capabilities to Closed and release the version in Jira | After Andrei's go | High | Release manager step |
| 6 | Andrei Klimovich | Set the MVP2 review meeting | Nov 12, 2026 (morning) | Normal | CAPs/REQs for MVP2 commented in Jira |
| 7 | Pavel Frolov | Call Val after the meeting | Nov 11, 2026 | Normal | Val's request |

## Open Questions

- When will the CAP-311 build-to-release-notes link be built — MVP2? (Dzmitry suggested; not confirmed)
- Who should attend release meetings — Val wants Andrei Bosik (CI/CD) in and developers out. (Val)

## Dispatch Log

---
*Processed from Teams transcript on November 11, 2026 (scheduled meeting-watcher)*
*Source meeting: MVP1 Release, MVP2 Scope and CAPs/REQs review*
