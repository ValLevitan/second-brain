# Meeting Summary — NOVA sync meeting
**Date:** November 23, 2026, ~8:14 AM – ~9:45 AM Eastern (recording)
**Duration:** ~91 minutes
**Attendees:** Val Levitan, Alexander Biratko, Pavel Frolov, Irina Shishko, Igor Metelski, Evgeny Kharetski, Anton Leshkevich, Alexey Khamin, Vladimir Samusenko (left early), Emma (AI-PM bot)
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_NOVA_Sync_IP-481_Root_and_Weekly_MVP_Plan-November-23-2026]]

> Val said twice in the meeting: this work is secret inside the company. Only the people in the meeting should have this information.

## Summary

**What the project is (Alexander).** The project builds and releases games as a flow. It has two parts: the games, and the system of tools that moves a game from idea to a final image on the hub. Evgeny's agent writes a brief. The brief goes into Anton's studio, which shows step by step what exists and what is missing, and ends with a game running in the engine. Open work: parts in LGS, system libraries and the engine; the same on the cheaper RK platform; and a set of test games for Texas or Georgia.

**The final goal (Val).** Street-operation machines have a mobile modem. JVL reads which game parameters work best in a territory, builds new games from those signals, sends them to the lab, and after approval sends them through the modem to specific machines in a specific location. After install the machine must verify the checksum that the lab signed. Pavel: this also means single components (for example a printer service fix) can be released without touching the games. Igor and Alexander: test "add or update a game" as early as possible, because it pulls changes in RIS, LGS and statistics.

**AI commissioning (Val, new idea).** In Georgia COAM each machine must be linked to the Intralot computer ("commissioning"). Today a technician does it by phone with an Intralot engineer; it takes 20 minutes to 2 hours depending on who you ask. Val wants an AI bot on the JVL side to do the call, hand over to the technician if needed, and send a report. JVL should not design the voice technology; it should pay a vendor and do a good integration. Val has at least one offer; the call cost is $4 per hour. Val already spoke with Intralot and they like the idea. Nobody was assigned.

**Names and Jira structure.** Use "NOVA" everywhere, not "NOVA-2" (Alexander: Jira is confused now). IP-481 is the root initiative for all this work, under value stream IP-90. All capabilities and MVPs go under it. Whether the games themselves go under IP-481 stays open. Initiative owner: Alexander Biratko. Team: Igor, Evgeny, Anton, Daniil.

**MVP plan.** One MVP holds everything (hardware platform, system, studio), not one MVP per product. The name is NOVA-MVP-1. Val wants an MVP about every week, small and often. Pavel gave December 1 as an example date; no date was fixed. Pavel's view of MVP 1 for hardware: a base game on the new engine with the current services and LGS on RK3576, about one week. A senior producer starts January 15 from outside the team; the studio must be usable by then. The studio is tested as a separate product like the others.

**Math in the pipeline.** The pipeline has no math step. Igor: math is needed very early, because it sets the symbols, payouts and bonuses; so far the team only worked with games that already had math. Igor said Efim says AI cannot write the math. Anton: for now take math from the library of existing models, since most first games will be reskins, and check in parallel if math can be made on the fly. Val does not believe math cannot be written. Agreed direction: math and mechanics are discussed together with the brief (producer plus mathematician), so this belongs in Evgeny's brief agent, not in the studio. The agent should ask if math exists, attach it, or offer to develop it. The agent does not do this today; Val: finish this first.

**Sound in the pipeline.** The pipeline also has no sound step. Val: add sound to the brief; ask at design time if a sound is needed and of what kind. Val: today's sounds are final and approved, so pull them all out and make them a standard, the same way Igor did with frames, and put them into the brief. Igor can add technical sound data to the existing briefs (when it starts, its name, maybe its length), but not the character of the sound, because Claude cannot listen to audio. Alexander: the studio needs a step to add or adjust sound, with a list of sounds and where they play.

**Onboarding a new designer and secrecy.** Anton: the designer logs in with a JVL account, downloads the studio, the studio installs what it needs, and a guide explains the steps. Val: people who are not loyal will try to copy this, so give away fewer secrets. Ideas: compiled tools instead of readable scripts (a black box), hide the generated prompts, lock access to a JVL account. Anton is to think about security while building. Val insisted that MVP 1 includes a simple way for a new designer to install everything alone from one page, not through a Dropbox link and a phone call.

**Old capabilities and requirements.** Many NOVA capabilities in Jira were made earlier by Daniil in the flow and their requirements do not fit. Irina is writing requirements from the RAGE platform (the RAGE code is the source of truth) and will link them to the cleaned capabilities; unsuitable requirements are removed. Capability 228 (game select) exists and Anton already built the screen. Alexander proposed that the LGS catch-up to the data center be one feature with stories, not new capabilities; Irina pointed out that the team now works from requirements, and said she understood his path.

**Setup screens.** The new setup exists only in LGS. Evgeny went through init setup with scripts, not with a real RIS. The team treats setup as done until testing shows otherwise.

**Emma (AI-PM bot).** Val asked the team to say their undertakings out loud so Emma creates the capabilities. Emma answered only with short phrases. Val: we will see what Emma creates; if she does not, the team finishes it by hand.

## Decisions Made

- **Use the name "NOVA" everywhere, not "NOVA-2"; the MVP name is NOVA-MVP-1** — Jira is confused by two names. (Proposed by Alexander; Val set the MVP name)
- **IP-481 is the root initiative for all NOVA work, under value stream IP-90** — all capabilities and MVPs are built under it. (Proposed by Pavel, accepted by Val)
- **Initiative owner is Alexander Biratko; team is Igor, Evgeny, Anton, Daniil.** (Val)
- **One MVP holds hardware platform, system and studio work together** — easier to filter all tasks and to write release notes. (Pavel proposed, Val agreed)
- **MVPs go week by week.** (Val)
- **MVP 1 stays narrow but working** — Anton does not widen the symbols step now (3D model plus video approach is put off); he builds the base game step. (Val, Alexander)
- **MVP 1 includes a simple self-install path for a new designer.** (Val)
- **Math and sound belong in the brief stage (Evgeny's agent), not as studio inputs** — the studio input is a finished brief. (Igor, Val agreed)
- **The studio is tested as a separate product.** (Alexander, Val)
- **Setup screens are treated as done until testing proves otherwise.** (Evgeny, Val agreed)
- **The team meets with Val every Monday; the team itself meets daily.** (Val, Evgeny)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Leshkevich | Add the base game step to the studio (background video, reels frame, maybe a preview to play the base game) | Nov 30, 2026 | High | MVP 1 |
| 2 | Anton Leshkevich | Build CI/CD for the studio and a simple way to install and update it; a page where a new designer installs everything alone (GitHub page was suggested) | Nov 30, 2026 | High | Val insisted |
| 3 | Anton Leshkevich | Define the full pipeline; list all missing steps as placeholders | Nov 30, 2026 | Normal | |
| 4 | Anton Leshkevich | Think about security of the studio while building | TBD | Normal | Black-box tools, hidden prompts |
| 5 | Evgeny Kharetski | Bring the local game server (LGS) repository up to date with the data center changes (multi-progressive, modem, setup and others) | Nov 30, 2026 | High | |
| 6 | Evgeny Kharetski | Bring up the whole NOVA platform on RK with the games ready by then | Nov 30, 2026 | High | One game now, maybe more |
| 7 | Evgeny Kharetski [Needs Val's confirmation] | Make the brief agent handle math (ask if math exists, attach it, or offer to develop it) and sound | TBD | High | Val: "finish this first"; no clear owner was named |
| 8 | Igor Metelski | With Evgeny: extend the pipeline to build several games on GitHub and load them into the ISO image; test on a machine; games for the RK platform | Nov 30, 2026 | High | |
| 9 | Igor Metelski | Merge main into his test branch of framework and engine, then merge it to main | Nov 30, 2026 | Normal | Needed for release versions |
| 10 | Igor Metelski | Add sound data to the existing briefs and prepare the sound standard; discuss at the next meeting | Nov 30, 2026 | Normal | Val wants all current sounds pulled out and standardized |
| 11 | Irina Shishko | Write requirements from the RAGE platform for NOVA, link them to the cleaned capabilities under IP-481, remove the unsuitable ones | ~Nov 30, 2026 | High | "About a week" |
| 12 | Alexander Biratko | Review the existing NOVA requirements and capabilities; create capabilities for the NOVA engine; align with Irina's framework requirements; lead the MVP 1 discussions | Nov 30, 2026 | High | No coding, he is on the recycler |
| 13 | Pavel Frolov | Work with Alexander on requirements; move Anton's capabilities under the right initiative; help Evgeny start everything on RK | Nov 30, 2026 | Normal | |
| 14 | Daniil (absent) | Move all system and transactional messages from the RAGE framework into the new framework | Nov 30, 2026 | Normal | Reported by Alexander; capability exists |
| 15 | Emma (AI-PM bot) | Create capabilities for: studio symbols step, base game scenes, studio CI/CD, and capabilities and features for Evgeny's and Igor's work | TBD | Normal | No confirmation in the transcript that she did it |
| 16 | [Unassigned — needs clarification] | Merge all waiting branches, including Daniil's | Nov 30, 2026 | Normal | Alexander: minimum for MVP 1 |
| 17 | [Unassigned — needs clarification] | Test adding or updating a game on a machine as early as possible | TBD | Normal | Igor and Alexander raised it |

## Open Questions

- Are the games themselves developed under IP-481? Val: leave it open for now.
- What exactly is in MVP 1 and on what date? (Igor) Pavel's example was December 1; not fixed.
- Can AI write slot math, or only reuse existing models? (Alexander, Igor, Val)
- How to protect the studio know-how from being copied? (Val)
- AI commissioning bot for Georgia COAM: who owns it, which vendor? (Val)
- Did Andrei Bosik remove the extra repositories and create the new ones? (Irina) Pavel thinks the new ones exist.
- LGS catch-up: one feature with stories, or requirements and capabilities? (Alexander, Irina)

## Words to confirm

The recording is unclear in these places:
- "Аракаби" / "aver commertin" (00:14:52–00:18) — read as "AI commissioning".
- "клипс или challine" (00:11, 00:13) — read as "Eclipse or GLI".
- "синерпродюсер" (00:26:29) — read as "senior producer".
- "Тамил да цой тамил" (00:21:54) — read as "Daniil".
- "$4 в час" (00:17) — read as call cost of $4 per hour.
- "на р к. Тензе" (01:10:48) — unclear word after "RK".
- "влад, который наш звук инженер" (00:44) — sound engineer Vlad; full name not said.

## Dispatch Log

---
*Processed from Teams transcript on November 23, 2026, ~12:20 PM Eastern*
*Source meeting: NOVA sync meeting (Daily Standup meeting series, Pavel Frolov organizer)*
