# Meeting Summary — Review - AI voice Game Design Assistant, first pass
**Date:** October 24, 2026, 7:56 AM – 9:11 AM Eastern
**Duration:** ~75 minutes (real talk starts at ~13 min; first minutes are sound checks)
**Attendees:** Val Levitan, Evgeny Kharetski, Igor Metelski, Pavel Frolov, Andrei Bosik, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_AI_Game_Design_Assistant_and_Code_as_Source_of_Truth-October-24-2026]]

## Summary

Held in Russian. Some words are unclear in the transcript.

**What the agent does.** Evgeny showed the AI game design agent. It runs in Teams, hosted in Amazon cloud (set up with Andrei), on the same principle as the AI-PM. Its main job: help the game producer build a brief (specification) for a new game. It asks questions and proposes options. Evgeny loaded into it: game cards from Confluence (all game design documents), Efim's Dutch Mill math (two files sent as a Teams attachment; the agent parsed RTP, pays, symbols and bonuses), and Igor's three layout specifications. It can also answer questions about past games ("which 5x3 games did we make", "which Egypt games") and help invent themes. Idea for later: join Michael's, Lena's and Efim's game meetings and write the brief and the game page from the discussion.

**Math.** Val said Efim told him Claude cannot understand his Excel math files; Val doubts this. Igor: when he ported games to NOVA, Claude learned each game well by sending spin requests to the math server. Andrei: the agent could query the math server in the cloud. Val: next step, give the agent all of Efim's working files and all game layouts (3x3, 3x5, 4x5).

**Old game code (SVN).** Igor's local copy of the SVN repo is 6.55 GB for 6 games. Pavel and Evgeny: the agent does not need old game code now. Val agreed: no mess; build universality step by step in new, clean code.

**Confluence is not the source of truth.** Val: designers do not keep Confluence exact; small and big errors go unnoticed. The only source of truth is code. Igor: the Rage framework is one big monolith, and game behavior also depends on data center settings, so old game code alone may not be a complete source. Andrei proposed a one-time job: Claude goes into SVN and builds a wiki page per old game (text plus images) from the real code; Confluence is then removed as a knowledge source. Val agreed (like Andrej Karpathy's wiki). Val: the output must answer Igor's specification — sizes, geometry, symbols. Evgeny noted this shifts the plan a little; Val: it is a scope gap found early, which is good.

**Demo.** Evgeny asked for a Dutch Mill game with a Japanese garden theme. The agent asked about symbols and proposed Japanese replacements (for example an origami crane instead of the goose; koi carp; torii gate), then produced a brief document. It can park one game, switch to another, and come back in the same chat.

**Sound and pictures.** Andrei suggested the agent also ask about sound; Igor: the team has no sound skills yet. Andrei wanted pictures right in the chat. Igor: roles are split — the producer gives a brief, the designer makes art. Igor's own tool (MVP-1) turns the brief into prompts for an outside image service (ChatGPT or Grok); the user copies them across. Val prefers Grok. Val: support the idea, but do it in steps; Evgeny and Igor are the two people doing it. Pavel suggested seasonal styles (New Year, Halloween, spring); Val: good idea, back to basics first.

**Timing.** Igor expects MVP-1 (brief to finished game scenes) on Monday, if his weekly Claude limit lasts (it resets Monday 11:00 Minsk time). Val did not want to hear about limits; Igor will ask for another account. Val is off until Thursday. Next review: Thursday October 29 at 7:00 AM.

**Competitor games.** Val wants the agent to take a new competitor game, break it into components, and describe what it does — first the mechanics, then math for those mechanics, automatically. Val believes within about six months math will be made this way and Efim will only check it. Ideas: casino blogger videos on YouTube; split video into frames with ffmpeg (Igor did this for game resources; Andrei found it slow); Val can likely get access to the newest machines at the test labs, play demo mode, and record through a capture box (~$40 on Amazon), as was done for the Aristocrat setup screens. Evgeny will first try a YouTube video. Results go to a separate session, not the Thursday meeting.

## Decisions Made

- **Confluence is not a source of truth for the agent; knowledge of old games will come from the code.** One-time job: Claude builds a per-game wiki from the SVN code, sized to answer Igor's specification. (Proposed by Andrei; agreed by Val, Pavel)
- **Old SVN game code is not moved into GitHub or the agent; universality is built step by step in new, clean code.** (Val, with Pavel, Andrei, Evgeny)
- **Image generation comes in steps:** the agent makes the producer's brief now; art comes through Igor's tool, MVP-1 giving prompts for an outside service. (Val)
- **AI agents are named with a dash: "AI-" plus the name.** (Val)
- **Next review Thursday October 29, 7:00 AM; competitor game breakdown reviewed separately on Friday October 30, 8:00 AM Toronto time.** (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Evgeny Kharetski | Test the hypothesis: teach the agent to break down a competitor game into components and mechanics (start with a YouTube video) | 2026-10-30, 8:00 AM | High | Val's request |
| 2 | Igor Metelski | Finish MVP-1: full cycle from brief to game scenes | 2026-10-29 | High | Shown at Thursday review |
| 3 | Igor Metelski | If possible, add MVP-2 work so Thursday shows one or two games built from the brief with math in place | 2026-10-29 | Normal | "Would be great" |
| 4 | Evgeny Kharetski | If possible, add MVP-2 work to the agent before Thursday | 2026-10-29 | Normal | |
| 5 | Evgeny Kharetski | Load all of Efim's working math files and all game layouts into the agent | TBD | Normal | Val: "next step" |
| 6 | [Unassigned — needs clarification] | One-time job: Claude builds a per-game wiki from SVN code; remove Confluence as the agent's source | TBD | Normal | Andrei proposed; Val agreed; no owner named |
| 7 | Evgeny Kharetski | Rename the agent with the "AI-" dash prefix | TBD | Low | Evgeny: "later" |
| 8 | Igor Metelski | Ask for another Claude account so the weekly limit does not block work | TBD | Normal | |
| 9 | Val Levitan | Schedule the Thursday October 29, 7:00 AM review | 2026-10-29 | Normal | |

## Open Questions

- Can old Rage game code alone fully describe a game, given that the framework is a monolith and behavior also depends on data center settings? (Igor)
- Should the agent also cover sound design? The team has no sound skills yet. (Andrei, Igor)
- Should brief and art be one tool or two? Val: do it in steps. (Andrei, Igor)
- Best way to analyse competitor games: video frames, special AI models, or recording at test labs? (Andrei, Igor, Val)
- Who runs the SVN-to-wiki job? (no owner named)

## Dispatch Log

---
*Processed from Teams transcript on October 26, 2026*
*Source meeting: Review - AI voice Game Design Assistant, first pass*
