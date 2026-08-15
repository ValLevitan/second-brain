# Meeting Summary — NOVA architecture design — session 4 of 5
**Date:** August 13, 2026, ~5:13–6:45 AM Eastern
**Duration:** ~1 hour 31 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko (Sasha), Evgeny Kharetski (Zhenya), Alexey Khamin, Anton Seregin, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_NOVA_Architecture_Design_Session_4-August-13-2026]]

## Summary

Fourth NOVA platform design session. The team reviewed a capabilities document Pavel built from earlier meetings (using Claude to consolidate and add ideas), then worked through new capability ideas for technicians, players, and operators, and set a plan for documenting the platform's capabilities before a mid-September presentation.

**Technician service capabilities.** Three ideas came up. (1) QR check-in/out: a technician scans a QR code at the machine to log arrival and departure at a location and record what was done, working offline. Val agreed. (2) Board-level hang detection: if the machine hangs (watchdog fails), the peripheral boards that keep running log the event and light red LEDs to draw the attendant's attention. Val agreed with the idea. (3) Audio-jack data channel: pull extended logs out through the headphone jack using audio-encoded data, modem-style, above 20 kHz so it stays inaudible; a 4-contact (mic) jack would allow a two-way error-checked protocol. Alexander estimated bandwidth at roughly 1 kbit/s (a few MB per hour) — too slow to move large logs but fine for control signals. Anton flagged that a transmit-capable device could look like spying; reading is lower risk than transmitting. The jack could be justified publicly as a hearing-accessibility output. Left as an interesting extra channel, not adopted.

**Critical-systems release gate (main decision).** The team worried a new programmer could accidentally disable the watchdog or another critical service. They agreed to build an automated acceptance test that checks critical parameters and services (watchdog enabled, log collection works, remote ping/server connectivity, etc.). It runs fast on an emulator for any build, but the mandatory gate is on real hardware for the pre-release (release-candidate) build — a build cannot go to field or lab until it passes. The result is attached to the release as a record of what was tested. This needs a written standard defining which critical nodes must be checked, plus a repository/inventory of critical services and scripts, which does not exist yet and must be created. Irina stressed this is mandatory, not optional. Pavel's added idea of also checking machine metrics (CPU load, temperature, framerate after boot) was pushed back by Irina as belonging to earlier testing, not the release gate.

**Faster game production.** Val wants games produced far faster than a month, with ideas sketchable directly on screen. Discussion of what takes longest (video/animation, new bonus logic) and the difference between new games and clones (clones are already fast). No decision — exploratory.

**Extension math.** Pavel proposed splitting base-game math from extension/bonus math so bonuses could attach to any base game (progressive-style). Alexander noted bonuses change RTP and are tightly coupled to the math, so this needs Efim (math). Mystery/progressive can already be added to any game on the new LGS. Deferred to a discussion with Efim.

**Multiple simultaneous games.** Val asked whether four games could run at once on a split screen. Alexander: not four at once today, but if the games are base-only (no bonuses/free spins) they can run sequentially yet appear parallel to the player, which is easy to build. Start with two. Whether this capability is wanted is a product call for Michael and Juan — Val took that action.

**Player passport / ticket.** Alexander proposed using the player's ticket (Flex Pay / Flex Recycler) as a "player passport" — attaching behavioural data (bet size, play frequency, preferences) without personal identity, so no personal data is taken. It could tailor the machine (e.g. bigger buttons for high rollers). It works best with a QR scanner wired directly to the machine, or if Flex Port is upgraded to SAS to report more (games played, money spent, average bet per session). Flex Port is limited today.

**Documenting capabilities (planning decision).** Today's capabilities live implicitly in Jira (epics/features/stories) and in people's heads. The plan is to write "prose" descriptions of how each subsystem works and derive baseline capabilities from that prose using Claude, then add the prose to the repository. Owners were assigned (see undertakings). The team accepts that current LGS capabilities will be heavily rewritten under the new service-split architecture (Evgeny: "strongly affected — modules rewritten"), but documenting now is still worth it — Val's point: if you never commit to documenting, it never gets documented.

**Schedule.** Tomorrow's (Aug 14) 12:00 NOVA meeting is cancelled. Aug 21 — Flex Recycler capabilities (Val, Anton). Aug 24 — checkpoint to walk through documented capabilities. Sept 15 — presentation of implemented and new capabilities to Michael and Juan for their input. (A separate Sept 8 meeting exists on a different topic.)

## Decisions Made

- **Mandatory critical-systems acceptance test as a release gate** — an automated test verifying critical services (watchdog enabled, log collection, remote ping/connectivity) must pass on the real-hardware pre-release build before any release to field or lab; the result is attached to the release. Requires a written standard and a critical-systems/services inventory, both to be created. Explicitly mandatory, not optional. (Val, Pavel, Irina)
- **Capabilities-from-prose documentation drive** — document existing platform capabilities by writing prose per subsystem and deriving capabilities via Claude, adding the prose to the repository, with per-subsystem owners. (Val, Pavel)
- **Cancel the August 14 NOVA meeting.** (Val, Irina)
- **Follow-up schedule set:** Aug 21 (Flex Recycler capabilities), Aug 24 (checkpoint on documented capabilities), Sept 15 (presentation to Michael and Juan). (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Irina Shishko | Cancel tomorrow's (Aug 14) 12:00 NOVA meeting | Aug 13, 2026 | Normal | No longer needed |
| 2 | Val Levitan | Ask Michael and Juan whether a capability to run multiple games (start with 2, up to 4) simultaneously on one screen is wanted | Before Sept 15, 2026 | Normal | Product decision on multi-game |
| 3 | Val Levitan | Send email invite for the Aug 21 meeting on Flex Recycler capabilities | Aug 14, 2026 | Normal | With Anton |
| 4 | Evgeny Kharetski | Write prose + baseline capabilities for the LGS backend | Checkpoint Aug 24; final by Sept 15, 2026 | High | Capabilities-from-prose drive |
| 5 | Alexander Biratko | Write prose + baseline capabilities for the framework and one base game (Kaliocha) — after finishing Recycler/Dispenser and returning from vacation | After ~Aug 31; before Sept 15, 2026 | Normal | On vacation until ~Aug 31 |
| 6 | Vladimir Samusenko | Write setup-side (frontend/setup) prose/capabilities and plan the partial-manual setup / operator recycler-change research | Before Sept 15, 2026 | Normal | With Anton |
| 7 | Anton Seregin | Experiment: write prose for the RS installation module (platform/CMS side) | Before Aug 24, 2026 | Normal | With Dima; Anton has capacity |
| 8 | Val Levitan | Insert the installation-module prose draft into the repository | TBD | Low | Draft already handed off |

## Open Questions

- Is a multi-simultaneous-game capability actually wanted, and at what scope (2 vs 4)? — needs Michael/Juan (raised by Val).
- Can extension/bonus math be cleanly separated from base-game math without breaking RTP? — needs Efim (raised by Pavel/Alexander).
- Is the audio-jack data channel worth pursuing given ~1 kbit/s bandwidth and the transmit-side legal concern? — unresolved (raised by Pavel/Anton).
- Who covers an installed LGS site if both Dima and Sasha are on vacation at once? — partly answered (Sergei Tsymanov returns before Dima leaves; possibly Sasha back by then), not fully settled.

## Dispatch Log

- 2026-08-13 (dispatch, "draft everything / all undertakings") — Email drafts (Russian, drafts-only, in Val's Outlook Drafts) created for: Irina (#1), Evgeny (#4), Alexander (#5), Vladimir (#6), Anton (#7). Val's own items (#2, #3, #8) → no email. Calendar reminders created for all dated undertakings (Val check-ins, 9 AM ET): #1→Aug 14, #3→Aug 14, #7→Aug 22, #4→Aug 24, #2→Sep 8, #5→Sep 1, #6→Sep 12. #8 (insert prose to repo) excluded — deadline TBD.
- 2026-08-13 (Val review) — CC Pavel + Irina added to all team drafts (Irina's own draft: CC Pavel only). Irina draft (#1) **deleted** — Val cancelled the Aug 14 meeting himself; its Aug 14 confirmation reminder also removed. Vladimir draft (#6) revised: RIS/installation prose + capabilities already drafted by Val and handed to Dima Chudinov — Vladimir/Anton build on that, not from scratch. **Sent (approved by Val):** Evgeny Kharetski (#4), Anton Seregin (#7), Alexander Biratko (#5) — verified in Sent Items 13:29 UTC. Vladimir draft (#6) left in Drafts pending Val.

---
*Processed from Teams transcript on August 13, 2026 (scheduled meeting-watcher run)*
*Source meeting: NOVA architecture design — session 4 of 5*
