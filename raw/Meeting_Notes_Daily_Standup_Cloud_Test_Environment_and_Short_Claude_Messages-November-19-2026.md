# Meeting Summary — Daily Standup meeting
**Date:** November 19, 2026, ~4:00 AM – ~4:43 AM Eastern (recording started 3:59 AM)
**Duration:** ~40 minutes of meeting; recording ~44 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Andrei Bosik (joined mid-meeting), Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Cloud_Test_Environment_and_Short_Claude_Messages-November-19-2026]]

## Summary

**Cloud test environment — meeting set.** Vladimir: many of his autotests are blocked because there is no test environment for the cloud services (signing, LTE setup through the cloud, etc.). He asked Andrei three times to set up a meeting. Andrei Bosik joined: he did his part earlier and told Pavel then. Meeting set for today 13:00–14:00 (team local time); Andrei sends the invite. Vladimir asked to add Alexey as owner of the TINT repository.

**Claude-written messages must be short.** Irina: questions and comments written by Claude are too long to read; ask Claude to write simpler. Andrei: he got 26 points from one person across requirements. Vladimir: he sends a short version in Teams and full context in Jira comments (for Claude to read). Pavel: agreed — keep context narrow; do not send big Claude texts to people. Andrei: ask Claude to follow "Simple English" globally; Val has said this many times.

**Release 21 / capability 314 versions.** Dzmitry: on capability 314 (bill validator / SAS data, not SIM cards) Pavel's feature was marked complete while the story on Dzmitry stayed open — Pavel: that is a mistake. The capability is in 22 but features sit in 21. Agreed to put them on 22; Irina created version 22 for Flex IQ so it can be set. Pavel: dates on items not due on the 19th must be moved.

**Port error codes.** Alexander added about 16 new error codes on the port. Flex IQ needs a text for each, otherwise they go to Grafana with no description (nothing breaks). Pavel: a short, clear message, 2–3 words. Dzmitry asked whether to take it into this MVP; not settled.

**Release timing.** Pavel: release was planned for today. Irina: not today, Anton is out; she would say by the weekend. Vladimir: unlikely by the weekend — without the test environment half the tests will not run.

**Status by person:**
- **Alexander:** Flex Recycler MVP 1 is practically closed: tested on the bench — accepts and pays notes, talks to the port, the new user UI from Andrei K works (setup not touched). Closing the last ~3 tasks that waited on Andrei's answers. Has unit-type tests; the other side cannot run them without a recycler (they ordered one). Removed a module from the build because Pavel said it is not needed. Has not yet cleaned MVP 1 capabilities; will do it after the tasks. The recycler image is not yet put to S3 like transactional builds; keys must be created — he has the task (part of the recycler update steps).
- **Alexey:** hardware tests; adapting added tests to run offline; reviewing PRs against TINT repo standards. After yesterday's meeting with Val: building an agent structure that semi-automatically reads the law repository and writes requirements not tied to one product (NOVA first). Irina asked him to review TINTs on one capability (~50); he has no time — anyone free can take them.
- **Daniil:** moving system messages and dialogs to the new engine. Collecting all messages and how they are shown; will then discuss with Alexander and write it up.
- **Dzmitry:** Flex IQ builder done; answers from Andrei closed. ARM host on GitHub — full deploy there; Jenkins can be forgotten. Took the SIM card task.
- **Evgeny:** waiting for Igor's games; should finish today. Builds are too slow — over an hour after a Rust change, because the packer runs on a 2-core hub VM. Proposes a self-hosted runner for local/test builds; keep only the last build. Working through bugs with Ivan.
- **Irina:** cleaning tests against the requirements the two Andreis rewrote.
- **Ivan:** created a couple of bugs; hopes to finish by end of week.
- **Sergey:** finished the ticket yesterday; now on support phone numbers (Pavel: moved to 22).
- **Vladimir:** autotests for CAP-289 and CAP-287 (Wi-Fi, keys, Wi-Fi setup by QR). Not taking new ones while blocked items come back.
- **Igor:** Nebraska — one vertical bonus integrated yesterday; today anticipation / scatter-stop effect per Michael's request. Ported one more game to NOVA 2 and setting up its CI. Will send Pavel, Evgeny and maybe Andrei a short doc with what was done and his questions; Pavel: share it as an artifact.

**Jira clean-up standard (Dmitri K).** Val asked yesterday for a standard: tasks with no owner/assignee older than ~3 months, initiatives without capabilities, and initiatives without a value stream are removed; backlogs stay small (~10 is small). Dzmitry already closed his old placeholder items with comments; suggests starting with features/stories without a repo prefix (old portfolio projects). Dmitri K will collect such items and ask owners before closing. Anyone can close their own old tasks now.

## Decisions Made

- **Cloud test environment meeting today 13:00–14:00 (team time).** — Autotests blocked. (Pavel, Irina, Andrei Bosik)
- **Messages to people stay short; keep context narrow; no long Claude texts.** — Hard to read. (Pavel)
- **Capability 314 features move to version 22.** — Capability is in 22. (Pavel; Irina created the version)
- **Port error code texts: short, 2–3 words.** (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Send the invite for the cloud test environment meeting; add Alexey | Nov 19, 2026 | High | Autotests blocked |
| 2 | Alexander Biratko | Close the last MVP 1 recycler tasks, then review recycler capabilities | TBD | Normal | No task for capabilities; may forget |
| 3 | Alexander Biratko | Change build keys so the recycler image goes to S3 | TBD | Normal | Recycler update steps |
| 4 | Daniil Stauskiy | Collect system messages and how they show; discuss with Alexander and write it up | TBD | Normal | |
| 5 | Dzmitry Chudzinau | SIM card task | TBD | Normal | |
| 6 | Evgeny Kharetski | Finish game work once Igor's games arrive | Nov 19, 2026 | Normal | |
| 7 | Igor Metelski | Share short doc (artifact) with Pavel, Evgeny, maybe Andrei | TBD | Normal | |
| 8 | Irina Shishko | Clean tests against the rewritten requirements | TBD | Normal | |
| 9 | Ivan Shpak | Finish current work | Nov 20, 2026 | Normal | |
| 10 | Dmitri Kovalchuk | Collect stale Jira items; ask owners before closing; draft the clean-up standard | TBD | Normal | Val's request |
| 11 | [Unassigned — needs clarification] | Review TINTs on capability (~50 items) that Alexey cannot reach | TBD | Low | Anyone free |
| 12 | [Unassigned — needs clarification] | Move dates on 21 items not due on Nov 19 | TBD | Low | Pavel raised |

## Open Questions

- Release 21 date: by the weekend (Irina) or later because of the missing test environment (Vladimir)?
- Port error code texts: in this MVP or not? (Dzmitry)
- Self-hosted build runner to cut build time? (Evgeny)

## Dispatch Log

---
*Processed from Teams transcript on November 19, 2026*
*Source meeting: Daily Standup meeting*
