# Meeting Summary — GitHub scope and large math assets (SVN legacy, artifacts, platform-math_engine-assets)
**Date:** October 23, 2026, 9:02 AM – 9:20 AM Eastern
**Duration:** about 18 min
**Attendees:** Val Levitan, Efim Podvoiski, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Math_Excel_Files_Stay_on_GitHub-October-23-2026]]

Held in Russian. Some terms are garbled in the transcript.

## Summary

**The problem.** When Val's Claude reviews the repository, it sees the big Excel math files and reports that they are not documented. Efim confirmed they were never documented.

**How Efim uses the files.** The Excel files calculate RTP. They hold the reels and other math settings. Efim changes the reels, runs a macro to export them, and puts the result into the game config file. The game config then goes to production. This is a manual process. The Excel files are not part of the build.

**Why not document them now.** Efim sees no simple way. There are many files and many look alike. He does not think Claude can document Excel files today. He builds a new game by changing a previous one, so changes pile up over time. Moving all this into Python or a tool is not realistic now; it is a lot of work. He will document the files if and when he automates this part.

**Move into the math engine repo?** Andrei suggested moving these files into the math engine repo, so its prose covers both code and these files. Efim said the game configs already live in the math engine repo. The Excel repo was kept apart because it is very large and is not part of the build. This was not settled.

**Keep them on GitHub.** Andrei asked if the files need to be kept at all. Efim: yes, he goes back to them when he makes a similar game. Andrei compared GitHub with Microsoft SharePoint and chose GitHub, because it is easier if the files are automated later.

**Prose for these files.** Andrei asked what such prose would contain; maybe a good README or Claude files is enough. Val said prose is needed for end-to-end tests built on acceptance criteria in the requirements. Later, game mechanics will be described in requirements with acceptance criteria to help test the math. Andrei noted this repo is not part of any tests today. Val does not want to force prose on these files.

**Future tools.** Efim hopes Claude will learn to work with Excel directly. Val: Excel works for now; the team will wait for Claude, Grok or another AI to do this and use it later as a tool.

**Close.** Val said he understands the issue now and has no more questions. Efim asked if these folders could be excluded from the repo scan. Val will not deal with that now; he will ignore that report and set it up later, when there is time.

## Decisions Made

- **The math Excel files stay on GitHub, not SharePoint.** — Efim needs them for similar games, and GitHub is easier for later automation. (Andrei, Efim; Val did not object)
- **No prose is forced on these Excel files for now; Efim keeps working in Excel by hand.** — Claude cannot work with Excel well today; wait for AI tools to catch up. (Val)
- **Val ignores Claude's "not documented" report for these files; excluding the folders is left for later.** (Val)

## Undertakings

No undertakings recorded.

## Open Questions

- Should the math Excel files move into the math engine repo? (Andrei) Efim noted the repo is very large and not part of the build. Not settled.
- What should prose or a README for this repo contain, if anything? (Andrei)
- Can these folders be excluded from the repo scan? (Efim) Val deferred it.
- After automation, will the work still be in Excel or in a new tool? (Andrei) Efim does not know.

## Dispatch Log

---
*Processed from Teams transcript on October 23, 2026*
*Source meeting: GitHub scope and large math assets (SVN legacy, artifacts, platform-math_engine-assets)*
