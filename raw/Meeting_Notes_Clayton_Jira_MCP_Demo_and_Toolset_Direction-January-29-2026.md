# Meeting Summary — Clayton Chancey: Jira MCP demo and toolset direction

**Date:** January 29, 2026, 10:01 AM Eastern
**Duration:** approximately 59 minutes (including a post-meeting Val–Aaron segment)
**Attendees:** Val Levitan, Clayton Chancey (running the meeting), Lena Zhukova, Aaron Bockelie, Michael Gottlieb (present at the top). Note on Plaud labels: the speaker tagged "Michael Gottlieb" through the demo is actually **Clayton** (Val: "it's Clayton who's gonna run the meeting"); Speaker 2 = Lena, Speaker 4 = Aaron.
**Raw transcript:** [[Meeting_Transcript_Clayton_Jira_MCP_Demo_and_Toolset_Direction-January-29-2026]]
**Source:** Plaud recording (offline), via Plaud-Inbox/JVL
**Calendar pairing:** Outlook event "Clayton-Aaron-JVL", 10:00–11:00 AM ET, organiser Clayton Chancey. Confirmed on both keys.
**Context:** the promised Thursday follow-up to the Jan 27 orientation — the read-only prototype demo, delivered on schedule.

## Summary

**The demo: Game Status.** Clayton showed the read-only MCP tool he built against JVL's Jira — implemented in **19 minutes** after Claude itself suggested it from the Jan 27 transcript ("recursive self-improvement": he loaded the MCP into Claude Code so it could test itself, then had it validate the transcript's claims against Jira as the source of truth). One tool call wraps many API calls with JVL's domain knowledge baked in — game hierarchy, market variants, Omni vs Rage split, feature/story templates, completion status. Lena's verdict: "definitely useful for a status review… I like it"; she'll need IT for the token/connection. The philosophy, stated: embed JVL game-design conventions in the MCP so nobody has to think in Jira's terms — "these tools don't have ChatGPT-versus-Claude opinions embedded in them, they have JVL opinions embedded in them."

**Val's rulings.**
- **Tokens:** "Let's stop making reference to tokens. I don't care… please don't save money on tokens."
- He already uses Aaron's MCP daily with a Claude-generated prompt for per-person/company-wide reports and has shared the prompt with Lena; her real time sink is task entry.
- **GitHub migration restated:** convert content to .md and park it "together with the developers' code" as Omni migrates — QA and everything included.
- **Cloning is the essence of the business:** correcting Clayton's uncertainty about the "create adaptation" tool — "we create clones all the time… we cannot create fresh content most of the time; creating a clone is the essence of our business." Frame/math/timing/peaks stay, theme/music/tone change.

**The toolset agreed (Claude-suggested, Clayton to build).**
1. *Create game from template* — name/market/initiative dictated loosely; generates initiative, standard features, stories, naming conventions, blocking relationships in one go. Lena's requirement folded in: image handling — her AI-assisted (never raw) JPEG/PNG/PSD assets must attach to the right stories by naming convention (e.g. "La Rosa symbol Goldenback → attach to the proper story"), with animation descriptions added manually after.
2. *Create adaptation (clone)* — clone the full functional/technical/logical Jira structure, then let Claude apply the thematic rename (savannah → Mexico) automatically, prompting for theme changes before executing. Val extended the vision: eventually bypass Lena's manual comp/texture/coloration design by generating directions from descriptions — "if it's not possible today, it will be possible in a year." Clayton mapped the architecture: Jira/GitHub text becomes the prompt basis for diffusion models (Gemini/Nano Banana class) — generative text first, image generation integrated after.
3. *Granular conversational tools* — single-ticket operations in natural language (Val is against manual deletion; automation removes the manual effort).
- Testing needs a sandbox — Aaron: ask Andre to recreate it; Clayton to email him.

**Process doctrine (Aaron).** Conversations in chat get lost — push the negotiation into GitHub comments/issues so the cadence is written; the same MCP could run through a bot on GitHub. "Aim for where things will be, not where they're at — start leading your target." Clayton's counterweight: "walk before run" — pattern first, tools second, no ecosystem lock-in.

**The escape from ChatGPT.** Lena is attached to her trained ChatGPT project for art references (subscription ends February 6 — she needs a replacement recommendation). Val's framing: "you were captured by an OpenAI ecosystem — you are a victim to that prison"; Aaron: "we would rather build our own prison where we hold the keys." Direction: provider-agnostic JVL tooling, traceable image sources.

**JVL School of Game Design / the truth pipeline (Val).** The game producer expresses all design reasoning vocally; those Lena–producer conversations must be recorded and turned into "JVL truth" — guiding principles for comp/theme design — because "JVL value will be in JVL knowledge, and when Lena leaves JVL the knowledge cannot escape." Clayton committed to a session (with Aaron) training Lena on the transcript loop: record → transcribe → feed to Claude with the MCP → scaffold cumulative design truth. Aaron sketched the future: live transcript integration plotting content as you speak — "Bravo."

**Scheduling.** Next session: Tuesday, same time — Lena shares her screen, zero preparation, Claude Code install to first working use, doubling as the JVL onboarding pattern. Post-meeting, Val and Aaron booked **Monday 10 AM** for the knowledge-graph introduction with Eli (an hour to start; "meeting will continue until morale is improved"). Aaron's parting warning about Lena("Atlanta" in the garble): she "likes to dive into corner cases of justification — be careful."

## Decisions Made

- **Toolset scope approved: create-game-from-template, create-adaptation/clone (with AI thematic rework), granular conversational tools** — Clayton builds, next-session hands-on training with Lena. (all)
- **Token economy talk banned.** (Val)
- **Image-generation migration off ChatGPT before Feb 6**, to a provider JVL controls (Gemini/Nano Banana candidates). (direction set; tool choice open)
- **Design-truth capture from producer–Lena conversations becomes a standing loop** feeding the JVL School of Game Design. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Clayton Chancey | Build the remaining tools (create game, create adaptation, granular ops) | Before Tuesday | High | "I can probably do it in the next hour" for some |
| 2 | Clayton Chancey | Email Andre about recreating the Jira sandbox | ASAP | High | Safe testing of create-game |
| 3 | Lena Zhukova | Get Claude Code installed (with IT); come to Tuesday with a blank slate | Tuesday | High | Screen-share, zero-prep onboarding |
| 4 | Clayton + Aaron | Transcript-loop training session with Lena | Next week | High | The design-truth pipeline |
| 5 | Aaron Bockelie | Knowledge-graph introduction with Val + Eli, Monday 10 AM | Monday | High | Invite sent on the call |
| 6 | Aaron / Clayton | Recommend the ChatGPT image-generation replacement | Before Feb 6 | High | Lena's subscription lapses |

## Open Questions

- Which image-generation stack replaces Lena's ChatGPT project (Nano Banana floated; "many ways — local inference, Stable Diffusion").
- Sandbox availability (Andre).
- How multiple MCP servers coexist per role (Aaron: overlap is fine, descriptions route tool choice — explained to Val at the end).

## Possible mis-transcriptions (not in glossary — confirm before fixing)

- The demo speaker tagged "Michael Gottlieb" is **Clayton Chancey** throughout the tool demo (voice-profile misassignment).
- "MCT / MCD / MCP" — all **MCP**; "blind / Klein" (00:08:22) — **Cline**; "Atlanta" (00:55:36) — **Lena**; "Mr. Axford" (00:42:42) — unclear, possibly a joke name for Val's process; "Lana" — **Lena**; "ATI request" (00:02:39) — **API request**; "boilerplate Banilla" (00:02:09) — garbled ("vanilla" as in plain — NOT the manufacturer; glossary auto-correction produced this artifact); "Eli" (00:58:37) — possibly **Ilya**, confirm; "Jirad/Dimitri" (00:25:29) — **Dmitri**, IT.

## Dispatch Log

---
*Processed from Plaud recording on September 24, 2026 (backlog batch 3)*
*Source recording: 01-29 AI-Powered Jira Automation Toolset Development for Game Design Workflow (Plaud)*
