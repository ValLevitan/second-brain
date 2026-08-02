# Meeting Summary — Modem_JIRA
**Date:** July 20, 2026, 6:06–6:22 AM Eastern
**Duration:** ~16 minutes
**Attendees:** Val Levitan, Pavel Frolov, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_LTE_Modem_Jira_Structure-July-20-2026]]

## Summary

The goal is to add LTE modem support to the Flex (V1000) machines and set this work up in Jira using the team's documented planning standard. Dmitri confirmed the standard is written, unchanged, and in GitHub; he posted the link in the meeting chat. Key rule from the standard: each repository gets its own Jira project; initiatives live in one project.

Pavel explained the build situation. There are no source files for the V1000 operating system today — only a prebuilt binary package (Linux plus OS files) sitting on the builder, reused for every product build. Two options: (1) the old way — rebuild the OS with modem support, about 3–5 days; (2) build a proper git-based build system like the existing RK3568 platform SDK repository, about 2–3 weeks. Pavel recommended the git-based approach: it unifies the SDK style across platforms (V1000, FP7, ARM), the team already has a Linux kernel mirror in its own repository (made by Andrei), and the work runs in parallel with other projects since Claude can grind on this isolated task with occasional check-ins. Val agreed, noting it also fits the direction from Friday of possibly moving RAGE to Nova, which would pull repository reorganization and GitHub Actions builds along with it.

For Jira structure, Pavel proposed placing the work under IP-90 Applications (value stream), under initiative IP-481 Nova Gaming Platform Land-based: create a capability stating the platform supports LTE modems, with features under it depending on which project needs fixes. One project will relate to the operating system. No new Jira project is needed until the repository exists. A new repository will be needed: an x86 platform SDK (analog of the RK3568 platform SDK), named something like "Platform SDK x86 Gaming."

A kernel question was raised but deferred: V1000 is on kernel 5.15, RK3568 is on 6.12 — whether to spread 6.12 to the Nova transition needs a decision later, not at this meeting. Val ended the recording so the transcript itself could serve as the working spec: he will send it to Pavel to work through with AI, and they will create the Jira structure together at 2:00.

## Decisions Made

- **Build LTE modem support via a git-based build system (separate repository, unified SDK style) instead of the quick OS rebuild** — worth the extra time because it unifies build style across platforms and runs in parallel with other work. (Decided by Val Levitan and Pavel Frolov)
- **Create a capability "platform supports LTE modems" under initiative IP-481 Nova Gaming Platform Land-based (under IP-90 Applications)** — follows the documented Jira standard. (Decided by Val Levitan, Pavel Frolov, Dmitri Kovalchuk)
- **Do not create a new Jira project until the repository exists** — the standard ties projects to repositories. (Decided by Val Levitan, Dmitri Kovalchuk)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Post the link to the Jira planning standard in the meeting chat | Done in meeting | Normal | Standard lives in GitHub |
| 2 | Val Levitan | Send this meeting transcript to Pavel | July 20, 2026 | Normal | Transcript serves as the working spec |
| 3 | Pavel Frolov | Work through the transcript with AI and prepare the Jira structure (LTE modem capability under IP-481) | July 20, 2026 | Normal | Val and Pavel to create it together at 2:00 |
| 4 | Pavel Frolov | Create the x86 platform SDK repository (analog of RK3568 platform SDK, e.g. "Platform SDK x86 Gaming") | TBD | Normal | Part of the git-based build approach, ~2–3 weeks of work |

## Open Questions

- Whether to move to Linux kernel 6.12 for the Nova transition (V1000 is on 5.15; RK3568 is on 6.12). Raised by Pavel Frolov; deferred — Val said maybe for Nova, but not for V1000 in Georgia for now.

## Dispatch Log

---
*Processed from Teams transcript on July 20, 2026, 8:01 AM Eastern (scheduled watcher run)*
*Source meeting: Modem_JIRA*
