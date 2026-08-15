# Meeting Summary — NOVA architecture design — session 2 of 5
**Date:** August 11, 2026, 5:15 AM – 6:40 AM Eastern
**Duration:** ~1 hour 24 minutes
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Irina Shishko, Evgeny Kharetski, Alexey Khamin, Anton Seregin, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_NOVA_Architecture_Design_Session_2-August-11-2026]]

## Summary

This was the second design session for NOVA, the new gaming platform. The meeting was in Russian. The team worked through the platform one "persona" at a time — for each persona they asked "if this person had one wish for NOVA, what would it be?" — and captured the wish as a requirement.

**Service size (carried over from session 1).** Pavel opened the question of how large the services should be. His position, shared by Alexander Biratko, was that anything running inside the IOBoard should not be split into separate services. Val polled everyone by name — Evgeny, Alexey, Anton, Vladimir and Irina all agreed — and closed the point.

**Game designers.** Their one wish is a fast feedback loop: see an idea running in the game as quickly as possible. Today scenes are built in Unity and converted to Pixi (PixiJS) by a script that runs inside Unity and outputs a group of files for the engine. Alexander proposed a live link ("hot reload") so a change made in Unity auto-converts and appears in the running game/browser within a few seconds, so designers catch conversion errors and misalignments immediately. They gave it the working name **"Game HotReload."** Evgeny pushed back on why Unity→Pixi conversion is kept at all and suggested building a proper scene editor over Pixi; Val noted a full Unity license was rejected on cost (~$1,000 per machine, so ~$1M over 1,000 machines). A zoom tool for spotting one-pixel misalignments was discussed (the Georgia GKUM progressive meters were once shifted a pixel); Alexander noted zoom already exists in Unity and in the game.

**Operator.** Wants to update games on a running machine remotely and independently — swap a game, fix a game, or add a new game on the fly, provided each piece carries its own checksum and is lab-certified. Alexander broadened this to updating any certified software component (for example a fix in the math module), which raised the open question of how the gaming commission treats a partial/component checksum when only a single composite CRC is checked today. The team also wants the operator to enable/disable games within a RIS on the fly, not only at setup.

**Product manager (Juan Martinez).** Wants a manual override on the setup ("override on the InstaSetup") to change game sets and settings — for example more or less aggressive bet-button settings — after the machine is in the field, possibly on a calendar/time schedule (this calendar-driven idea was parked as a "future"). Also wants a real-time dashboard (on computer and phone, with alarms) showing accounting and service feedback and game performance (popularity, button/money performance), for both operator and product manager, with the ability to push changes back to the machine.

**The "nail of the program" — certified install confirmation.** Val stressed the headline feature: push an approved software build with its checksum to the machines and get back a certified confirmation of exactly what installed — not a self-reported claim. This assumes the machine has an internet connection (casino permitting); without internet the same is done manually but still with install confirmation.

**Service / reliability — the Georgia freeze must never recur.** Val recounted the Georgia disaster: machines froze on an open screen (an AMD processor freezing on Linux kernel 4.19); players simply moved to competitor machines, so JVL machines quietly stopped making money. It took roughly 1.5–2 years to find, nearly cost the business, and machines had to be given away free to rebuild trust. The fix was upgrading the kernel from 4.19 to 5.15. Requirements captured to prevent recurrence:
- A health-check / heartbeat that covers LGS and every critical service.
- A **"Black Box"** service (Val's name, like an aircraft black box) that records health checks and events (power on/off, calendar time, possibly GPS), stored for a full year, moved off the IOBoard onto disk so it is not space-limited.
- A watchdog/timer that cannot be disabled by any software upgrade (an old watchdog existed decades ago but got turned off in a later revision).
- Distinguish uptime from "work time" — a machine can be powered on while the game is frozen. A hardware-level record (in IOBoard firmware SRAM, e.g. the last ~100 power events) should capture power on/off even when the OS never fully boots.
- Health data must reach JVL in an active mode when internet is available, and in a passive mode when it is not — piggybacked on periodic field visits (QR / license scans). The team wants to move beyond QR-only toward wider-bandwidth data transfer where the law allows.

**Player.** Added near the end: let a player re-live and share a big win. On a large win the player scans a QR that points to a cloud service, which reconstructs the winning session and generates a shareable video (download, send to friends, possibly upload to YouTube). Alexander framed it broadly as "the player should be able to re-live their win experience." Alexey added auto-reconnect: if a non-critical service dies, the machine should try to restart it without dropping the player from the session.

**Next steps.** Val will send the team the recordings from session 1 (yesterday) and session 2 (today). Pavel and Irina will each write up their side of the "delta" (what exists today versus what NOVA needs, per persona) and then combine. No meeting Wednesday Aug 12 (internal writeup; Val is away). Thursday Aug 13 they summarize jointly and begin discussing the work schedule; Friday Aug 14 is reserved to formalize that schedule.

## Decisions Made

- **Do not split what runs inside the IOBoard into separate services** — keep it as one unit rather than many microservices. (Proposed by Pavel Frolov and Alexander Biratko; agreed by Evgeny, Alexey, Anton, Vladimir and Irina; closed by Val.)
- **Three-day working cadence** — Wed Aug 12: internal writeup, no meeting; Thu Aug 13: joint summary and start scheduling the work; Fri Aug 14: formalize the schedule. (Decided by Val; agreed by Pavel and Irina.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Write up his side of the NOVA persona "delta" (current state vs NOVA target, per persona), then combine with Irina's | Thu, Aug 13, 2026 | High | Feeds the Thursday joint summary and the work-schedule discussion |
| 2 | Irina Shishko | Write up her side of the same NOVA persona "delta", then combine with Pavel's | Thu, Aug 13, 2026 | High | Pairs with undertaking #1 |
| 3 | Val Levitan | Send the team the recordings from session 1 (Aug 10) and session 2 (Aug 11) | TBD | Normal | Inputs for Pavel and Irina's writeups |
| 4 | Val Levitan / team | Take the partial/component-checksum certification question (remote update of one certified piece) to Juan Martinez, who knows the topic best | TBD | Normal | Blocks the remote-update and certified-install-confirmation design |

## Open Questions

- Will machines have an internet connection in the field (casino-permitting)? This determines whether health-checks run in active mode or only passive mode. (Raised by Alexander Biratko — unresolved.)
- How does the gaming commission treat a partial/component checksum when today only a single composite CRC is verified? (To be discussed with Juan Martinez.)
- Calendar/time-based game settings (e.g. bet-button aggressiveness by day or hour) — parked as a "future," not designed.
- Exact mechanism for the manual override on setup (Juan's long-standing request) — captured as a requirement, mechanism TBD.

## Dispatch Log

---
*Processed from Teams transcript on August 11, 2026, ~8:05 AM Eastern (scheduled meeting-watcher run)*
*Source meeting: NOVA architecture design — session 2 of 5*
