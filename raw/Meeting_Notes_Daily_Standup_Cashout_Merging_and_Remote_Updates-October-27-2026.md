# Meeting Summary — Daily Standup meeting
**Date:** October 27, 2026, 4:45 AM – 5:23 AM Eastern
**Duration:** ~38 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Evgeny Kharetski, Igor Metelski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Cashout_Merging_and_Remote_Updates-October-27-2026]]

## Summary

Held in Russian. The audio is poor in places (Evgeny was hard to hear). Unclear names, numbers and words are marked "heard".

**Flex-Port meter pulses.** Pavel closed PORT-127 and PORT-165, and one more task (20/173, heard): a new command that shows pulse statistics. With it they found that one machine brand ("Banilla", heard) sends meter pulses every 125 ms, not 100 ms. The current accept band (about 30–70 ms) may have rejected some pulses at the edge. Today Pavel widens the logic: accept a pulse period from 30 to 150 ms; 2 seconds of silence resets the count. Alexander asked who configures this per machine. Pavel: no configuration needed for now; the new debug output will show what other machines do.

**Repeat cash-out.** Irina: on some machines part of a cash-out is paid normally and part shows as a second cash-out / unclaimed. Pavel thinks this is a different cause — machine settings or a 2-second stall in the meters. Pavel proposed: if the player presses cash-out again before the Flex-Port timeout (about 30 seconds) ends, add the new amount to the pending one and reset the timeout. Evgeny suggested resetting the timeout on the game-start signal; Pavel said in BV mode the machine does an interrogate at game start, so they can catch that. Alexander first preferred a separate cash-out, then agreed it is logical because the Flex IQ transaction has not started yet.

**Remote update (Val's email of Oct 26).** Pavel wrote a one-page executive document with links to the capability and requirement; he is not sure the acceptance criteria are clear. Proposals are due by Thursday's meeting with Val; Alexander noted a meeting is also set for Friday. Points raised:
- It is remote update of all JVL software, not only games.
- Adding games is hard: SAS maps each game to an index (limit about 255), and the numbers are fixed when the build goes to the Eclipse lab. For Georgia, new games mean going through Eclipse again with the extended game list.
- Least painful case: change a game but keep its IDs (graphics, video).
- Possible levels: replace the whole image (no USB stick), replace one game, or patch a game.
- On NOVA the math is separate, so math updates also need thought.
No decision.

**Nebraska.** Anton Leshkevich cleaned old files and ported Sparkle Seven (heard), the last game on the list; it has no math yet. Igor: Efim already updated the math; it sits in the Jackpot Rush Nebraska config (Sparkle Seven and Sapphire Star). Anton will add it today. Pavel asked for a task for the Sparkle Seven port (as a task under the feature). Igor will add the icon and update the data center image, including Efim's fix for progression levels resetting after draws (no separate task).

**Other updates.**
- Alexander: more than half of the BV-driven tasks are done; he is closing them. Now on Andrei's new requirement 1926 (heard), which changes capability 272 — timeouts in BV mode.
- Anton Seregin: tasks 243 and 180 (heard) closed — printer scenarios. Cleaned up the spike questions; the team needs to go through them. Pavel: meet today at 2:00 (time zone not stated) on Flex-Port setup: Wi-Fi access point via QR, with Alexey.
- Daniil: NC6 (heard) nearly committed. Next: buttons in the framework — the framework implements the buttons, each game sets their look and layout; several games need rework. Pavel: open a task.
- Evgeny: mostly inaudible. Working on a library (LGS, heard) and an assistant for the new RIS integration (heard). Asked to be invited to the remote-update meeting or sent its transcript; Pavel agreed to invite him.
- Igor: reworked a feature (heard "primaries skill") per updated requirements from Michael and Efim; integrating new resources; thinks designers' integration tasks are enough, no extra tasks. Working on an AI tool for building game scenes. Pavel asked him to fix Dutch Mill items 21–22 (heard). Igor: the vertical Nebraska Dutch Mill task can close; he will merge branches to main after Daniil finishes today. He believes he already closed Dragon Pays (heard); will check.
- Irina: bill validator requirements; reviewing all autotests.
- Ivan: checking an old install with Evgeny, then RIS, then the server to see machine status (rent payment, heard).
- Pavel: installer task for clearer error messages (bad USB stick, cannot repair disk, I/O board not found). He will send a document with all error screens on one page, also useful for service techs. To test, replace the installer file in the latest Georgia build.
- Sergey: port update. Today he checks how firmware reaches Flex IQ; the scheme changed. The AWS service bypasses RAUC (heard), so they need their own checksum check. Also fixing stories Ivan created.
- Vladimir: port bugs — closed 136, 37 and 34 (heard). Needs the right text color for amounts and buttons; then will retest these bugs and the modem in one run.
- Alexey: closed his hanging tasks; continuing hardware autotests; deleted extra branches. Raised a concern: one developer ("Egor", heard) merged 3 old, long-open branches last week with very long PR texts; the code needs re-checking, and one touches bill validator mode just as the team goes live. Pavel: the project has moved far since those branches opened. No decision.
- Dmitri: the agent now finds candidate requirements in chats, checks if they exist, then comments on the existing one or creates a new one. Irina moved the ones he sent to draft.

**Follow-up today.** NOVA requirements meeting with Alexander, Anton Leshkevich, Pavel (and Irina) at 12:30 Minsk time (about 5:30 AM Eastern). Pavel creates the meeting.

## Decisions Made

- **Flex-Port accepts meter pulse periods of 30–150 ms, 2 s silence resets the count, no per-machine configuration for now** — one machine pulses at 125 ms. (Pavel; Alexander agreed)
- **A repeat cash-out before the Flex-Port timeout ends is added to the pending amount and the timeout is reset** — avoids split / unclaimed cash-outs; the Flex IQ transaction has not started yet. (Pavel, Alexander)
- **Data center image update (Sparkle Seven + Efim's progression fix) needs no separate task** — it is a small commit. (Igor; Pavel accepted)
- **NOVA requirements meeting today at 12:30 Minsk time** (Pavel, Alexander, Irina, Anton Leshkevich)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Widen pulse logic to 30–150 ms period with 2 s silence reset | Oct 27, 2026 | High | "Banilla" 125 ms |
| 2 | Pavel Frolov | Implement adding a repeat cash-out to the pending amount and resetting the timeout | TBD | High | Started last night |
| 3 | Pavel Frolov, Alexander Biratko | Send remote-update proposals before Thursday's meeting with Val | Oct 29, 2026 | High | Val's email Oct 26 |
| 4 | Anton Leshkevich | Add Sparkle Seven math from the Jackpot Rush Nebraska config | Oct 27, 2026 | Normal | |
| 5 | Anton Leshkevich | Create a task for the Sparkle Seven port | TBD | Normal | Pavel's request |
| 6 | Igor Metelski | Add the Sparkle Seven icon and update the data center image with Efim's progression fix | TBD | Normal | |
| 7 | Igor Metelski | Fix Dutch Mill items 21–22 (heard); merge branches to main and close the vertical Nebraska task | Oct 27, 2026 | Normal | After Daniil finishes |
| 8 | Igor Metelski | Check that Dragon Pays (heard) is closed | TBD | Low | |
| 9 | Daniil Stauskiy | Open a task for framework buttons | TBD | Normal | |
| 10 | Pavel Frolov | Invite Evgeny to the remote-update meeting | Before Oct 29, 2026 | Normal | |
| 11 | Pavel Frolov | Send the installer error-screen document | TBD | Normal | |
| 12 | Ivan Shpak | Read Pavel's installer error document and work out how to test it | TBD | Normal | Pavel: swap the installer file in the latest Georgia build |
| 13 | Sergey Tsimanov | Check firmware delivery to Flex IQ; add own checksum check | TBD | Normal | AWS bypasses RAUC (heard) |
| 14 | Vladimir Samusenko | Confirm text colors, then retest port bugs and modem in one run | TBD | Normal | |
| 15 | Alexey Khamin | Send the list of last week's merges from old branches | Oct 27, 2026 | Normal | To Irina / Pavel |
| 16 | Pavel Frolov | Create the NOVA requirements meeting (12:30 Minsk) | Oct 27, 2026 | Normal | |
| 17 | Pavel Frolov, Anton Seregin, Alexey Khamin | Meet at 2:00 on Flex-Port Wi-Fi setup via QR and spike questions | Oct 27, 2026 | Normal | Time zone not stated |

## Open Questions

- How to update games remotely when SAS game indexes are fixed at Eclipse testing (Alexander, Pavel).
- How NOVA math updates will be delivered (Alexander).
- What to do about the old branches merged last week without review (Alexey).
- Cause of split / unclaimed cash-outs on some machines (Irina) — Pavel thinks machine settings.

## Dispatch Log

---
*Processed from Teams transcript on October 27, 2026*
*Source meeting: Daily Standup meeting*
