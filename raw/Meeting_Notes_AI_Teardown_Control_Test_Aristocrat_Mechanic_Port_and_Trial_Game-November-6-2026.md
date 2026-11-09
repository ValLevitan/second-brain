# Meeting Summary — AI teardown review 2, control test on our own GA-COAM V2 games
**Date:** November 6, 2026, 8:00 AM – 8:58 AM Eastern
**Duration:** ~56 minutes
**Attendees:** Val Levitan (host), Evgeny Kharetski, Igor Metelski, Pavel Frolov, Irina Shishko, Andrei Bosik
**Language:** Russian (a short stretch in English)
**Raw transcript:** [[Meeting_Transcript_AI_Teardown_Control_Test_Aristocrat_Mechanic_Port_and_Trial_Game-November-6-2026]]

## Summary

**Purpose.** A control test: record our own GA-COAM V2 games as if they were a competitor's machine, with no special access (no wiki, no source), video only, and see whether Claude can pull the mechanics out.

**Phone video is enough (Evgeny).** Evgeny recorded two games. The first with a capture card and a laptop: best quality, one screen only, fine for vertical cabinets; 400+ spins, no bonus because that machine had no show mode. The second hand-held on a phone. Key finding: we do not need hundreds of spins. The 300+ games in the first meeting's document were for math (bonus frequency); for mechanics it is enough to film the help pages and each bonus round, five to seven short videos. The phone is more than enough: no capture box, put the phone on a tripod next to the machine and play. The only problem was sending the video through Telegram, which compressed it so Claude misread some help text; give it the original file. Three artifacts: analysis of the capture-card game, analysis of the phone game, and a note on phone-recording drawbacks. Val's takeaway: a selective recording (demo mode, help screens, bonuses) is what is needed, not a full-day recording, which may show no bonus at all.

**Aristocrat mechanic ported in under a day (Igor).** Igor took Evgeny's earlier YouTube teardown of an Aristocrat game (heard as "Timberwolf") and had Claude build its bonus in a Rage-engine game: a meter fills during the base game (Aristocrat fills it on certain symbols; Igor used any win), and when full a hold-and-spin type bonus starts, a ladder where bonus lines open as symbols land in the cells. First built on placeholder scenes, then generated art and made real scenes. Not connected to math or RTP yet. Time: Friday evening he wrote the task, checked at about 10 PM and the bonus was ready; Sunday he cleaned bugs and profiled; a couple of hours on art. Less than a day; a repeat would take 5 to 10 hours. Val: "when I said one widescreen game a month, I lied." Caveat: the YouTube bloggers never won the bonus, so Claude assumed how it plays; help screens settle that. Val: take the YouTube video plus photos of the help screens from the machine.

**Math.** Igor: the intermediate states of a bonus do not affect RTP, only the final payout. So an existing bonus already in the RTP can be re-skinned with a new mechanic as long as the final payout matches. Pavel's rough approach: trigger probability 1/N spins times the mean bonus value. Val: Efim is our man and works with us; involve him and have him teach Claude the math. We do not need competitor math: we take the mechanic, fit our own math, give the bonus a contribution percentage and let it work out the play.

**Graphic style template.** Val wants JVL's graphic style described, the way Lena's games are recognizable, then: "here is a new theme, here is a mechanic, make the game in our style." Andrei called it a brand book; Val: not marketing, a style template. Andrei: the graphics team may already have a document on symbol and coin style; Irina: it is in Confluence. Igor already broke the style down for art prompts during the vertical-version experiments and will consolidate it. He also templated 15 games from the GA-COAM 3 product with tone and style points.

**Assignment: trial game.** Igor builds a trial game with an Aristocrat mechanic Val named (heard as "progressive persistence"), using the graphics of the three latest Georgia games (wolves, lions, bison) adapted to the mechanic, in the described style. Val gives the game name and the help screens if he can get them. Review Tuesday or Wednesday; Val schedules Wednesday around 7:00. Math: Efim to be pulled in.

**Interactivity idea rejected (Andrei).** Andrei proposed more player interaction: a character (the leprechaun) following the player through a camera, announcements of upcoming games via the modem. Val: every interactivity attempt in gambling over 50 years failed, hundreds of millions of dollars; the last was Zynga, about $300M. Players play for one reason, to win; anything in the way irritates them. The machine must be sharp and focused on the player who wants to win; the player sits at a machine because he trusts it to give him a fair chance.

**Anton Leshkevich's NOVA 2 status email.** Val asked about Anton's report sent yesterday at 17:00 Canadian time. Igor explained it: a designer studio integrated with Jira; it pulls a task, loads an existing game's resources and runs them on Anton's own engine. The summary table shows 12 capabilities (under an epic heard as CAP-299) and 60 requirements; counts read out as 23 done and 28 floating, and 7 done, 17 in progress, 7 to start. Scenes use the Pixi scene structure exported from Miranda, but the engine is not tied to Miranda. "Lua" in the report is a scripting language for scene behaviour. Val: how does Igor's work connect? Igor: at the asset-loading stage; scene creation (now Rage) would move into Anton's studio; to be discussed with Anton. Irina: the engine must first be written, then Rage replaced. Pavel: Anton's speed grows now that the requirements are written. Igor also raised the modularity requirement for Anton's framework; no meeting with Anton was on the schedule.

**Follow-up meeting.** Val and Pavel: meet Anton today, about an hour and a half later, on how the pieces merge into NOVA 2 (Irina: a merge, not an idea integration). Efim, Igor, Pavel, Irina invited; Andrei and Evgeny said yes. Val sends the invite.

## Decisions Made

- **Phone video is enough for a competitor teardown; no capture card. Film help screens and bonus rounds selectively and give Claude the original files** — (Evgeny, Val)
- **Competitor math is not needed: port the mechanic and fit JVL's own math with Efim; intermediate bonus states do not affect RTP** — (Val, Igor)
- **Igor builds a trial game: the named Aristocrat mechanic with the wolves, lions and bison Georgia graphics in the described JVL style; Val supplies the game name and help screens; review Wednesday ~7:00** — (Val, Igor)
- **Interactivity features (camera-tracking character, announcements) are rejected: players play only to win** — (Val)
- **Meeting with Anton Leshkevich today on merging the NOVA 2 pieces; Efim, Igor, Pavel, Irina, Andrei, Evgeny invited** — (Val, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor Metelski | Describe JVL's current graphic style as a style template document | Nov 11, 2026 | Normal | Consolidate his prompt analysis; Confluence has a graphics doc |
| 2 | Igor Metelski | Build the trial game with the Aristocrat mechanic on the wolves/lions/bison graphics | Nov 11, 2026 | High | Weekend plus Monday if Val writes today |
| 3 | Val Levitan | Send Igor the game name and mechanic; help screens if he can get them | Nov 6, 2026 | High | |
| 4 | Val Levitan | Schedule the trial-game review for Wednesday around 7:00 | Nov 6, 2026 | Normal | Tuesday as fallback |
| 5 | Val Levitan | Send the invite for today's NOVA 2 merge meeting with Anton | Nov 6, 2026 | High | Efim, Igor, Pavel, Irina, Andrei, Evgeny |
| 6 | Val Levitan | Bring Efim into the math for the trial game | TBD | Normal | |

## Open Questions

- How do Igor's Rage-based mechanic work and his web graphics tool connect to Anton's engine and studio? (Igor, Val) — for the Anton meeting.
- What does the "framework on games Lua" line in Anton's report mean? (Val)
- Trial game math: JVL's own or fitted with Efim? (Igor)
- Modularity requirements for Anton's framework. (Igor)

## Dispatch Log

---
*Processed from Teams transcript on November 6, 2026, 10:05 AM Eastern (scheduled meeting-watcher)*
*Source meeting: AI teardown review 2, control test on our own GA-COAM V2 games*
