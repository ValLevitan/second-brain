# Meeting Summary — Daily Standup meeting
**Date:** October 14, 2026, 4:47 AM – 5:29 AM Eastern
**Duration:** ~42 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Leshkevich, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_MVP1_Extension_and_RK3576_Game_Library-October-14-2026]]

## Summary

Held in Russian. Anton Leshkevich asked to join the standup and Pavel added him.

**Alexander.** Finished capability 134. Is finishing capability 135: the validator check with pulled cables was missing on his validator. Next is capability 116: partly done, but the checks on the link with the terminal hub (license off/on and so on) are missing. Pavel asked him to set a start date on "FP 12 09" (item as heard), because without it the board shows a gradient.

**Alexey.** Works on the transactional repository autotests. It is hard to set up all runs at once. Many tests depend on simulators (terminal hub, FlexPort, emulator in the repo). He will create a task to run tests on real hardware, so there is some run closer to the MVP1 end. Pavel: "how much closer — tomorrow is the 15th." Alexey will take the Flex IQ device. Irina still needs it to finish Flex IQ tests. Pavel: Dzmitry works on Flex IQ for his last day today and goes on vacation tomorrow, so his device may free up. Anton (surname not stated) may also get a new Flex IQ today after his experiments, which would allow three parallel streams.

**FlexPort firmware by USB stick.** Pavel caught Evgeny Alekseev two days ago and reminded him: for the October 15 release, FlexPort software update must work at least by USB stick. Evgeny Alekseev promised a build tonight. Tomorrow morning the team must first check that FlexPort firmware goes by USB. Without it ports can only be flashed by cable.

**Anton Seregin.** His three Flex IQ tasks (67 and others) all wait on the terminal. He now has access rights. He changed the installer, will build an image and try to install it.

**Daniil — RK3576 ARM platform.** He fixed memory leaks and upgraded Pixi to version 8.22. The AI already created a Jira task for the leaks (project "NE…", not yet on the team dashboard; Dmitri Kovalchuk should add it). A second task will cover the Pixi upgrade. Pavel explained the context for Anton Leshkevich: the RK3576 ARM board is cheap, compact and low power, for low-cost "street" machines (South Dakota, Texas; non-casino locations). Daniil has been trying to run the new games on it. One limit is 8 GB of memory. Video was too heavy: the decoder did not support VP8, so Daniil re-encoded to VP9 with alpha. Open point: when to decode video — at game entry or at feature entry. Entering a bonus gives about a half-second micro-freeze. Pavel, citing Alexander: no stutter is allowed inside one game; bonus video may load at game entry, not on the way into a feature. Daniil agreed: decode all of a game's videos at game entry and keep them. 8 games may not fit; about 5 may fit in 8 GB.

**Next step for RK3576.** Pavel wants to talk with Igor and split work among Igor, Anton and Daniil: take the South Dakota games now on RAID, convert them with AI (including resources and video) into NOVA vertical games, and try to fit a library of about 5 games on this processor. Anton must pick which game to take. Pavel may call Igor later today so he can explain his scripts for converting horizontal games to the other platform.

**Dzmitry.** FlexPort 124, 125, 126 are in progress; he will close them today. Someone again said they do not match the mockups; he will answer in comments. Last night with Andrei Klimovich he brought up a production Flex IQ and re-registered an old one. It registered fine. He installed version 1, then pushed an update. The update installed but much slower than in the office: about 6 Mbit/s by the logs, about 2–3 times slower. Pavel suggested the building may be a metal hangar. Dzmitry: signal level in the logs is good. He will add useful logs, remove junk logs, push one more update, and with Pavel (who has the prod keys) connect over the local network to check ping to the terminal, together with Andrei. He also brought all transactional web services in line with Andrei's standards (prose and contracts all green). Only FlexPay and RIS remain (with Sergey). He goes on vacation but stays in the country; people can write to him.

**Remote RIS over the network.** Dzmitry: with the scheme discussed, remote RIS will stop working properly. Today the machine sends no software info, so the server takes the latest stub by last installation. A new protocol is needed so new machines send their software version. Pavel: keep backward compatibility — new software sends its version (protocol v2) and the server picks the matching RIS; old machines follow the old path. Sergey: it works for new machines, not old ones; he also asked why the machine protocol must change if all goes through the host. Pavel moved this to a separate meeting.

**Evgeny.** Finished passport work. All devices report, tested on a real machine. Some devices are detected as missing at once, others only after work; partly a hardware limit, partly the library. Given little time, he left the device logic as is. Today he tests the battery (task 246) and has a matching sub-task for testing. Then MVP2 tasks.

**MVP1 date.** Pavel: extend the MVP1 date to about November 8 or 9; tasks now marked MVP2 will be done in MVP1. Evgeny asked if the team still delivers the old (originally cut) version. Pavel and Irina: yes, the same scope, just a longer time.

**Data center boot loops.** Pavel asked Evgeny to study a capability: can the data center use hooks to recover from boot loops (for example, after 3 boot loops, partly clear storage)? Evgeny: unlikely; you do not know where the bad state was written; storage is large. Erasing records may also go around the gaming commission if money is involved. Evgeny: such boot loops are rare; likely echoes of machines that were frozen once. Pavel: Val said in a meeting that this must never happen; the machine must always recover to a working state. Evgeny proposed a recovery mode: boot into a clean machine that still reaches games, then run the saved storage through an algorithm to find the problem and tell the user if it can be fixed (like Windows recovery). Evgeny: a big, complex task, hard to test, unlikely by the deadline. Pavel will not put it in MVP1 and has not approved it, since the goal is not yet clear.

**Irina.** Three autotests in progress, then she moves on (65, or similar). Her VPN made her audio break up; she said she needs it for Claude.

**Ivan.** Pavel reached Ivan's tasks only around 9 PM. He closed a few. On 128, Claude ran about 400 sequential transactions overnight and could not reproduce the problem; recent commits may have fixed it. Ivan will rebuild the port, install it and rerun; if questions remain, he will meet Pavel. Two more tasks are almost done. Then he takes autotests from Irina (66).

**Sergey.** Closed stories and studied task 3522 [as heard]. A plan for implementation must be discussed.

**Vladimir.** Part of the autotests moved to Done. Requirement blocks remain only on 31: many numbers must be set, because autotests lack criteria. 71 and 72 wait for the port (it cannot reach some screens). In progress: 27, 32 and another; tests are written, but requirements or tickets need work; some scenarios fail. Pavel: some of our non-functional requirements are too strict. Vladimir and Irina: softer would not help; one-line requirements are vague (for example, log volume, when a repeat starts, what to do with lost entries). Irina: we will now demand detailed requirements.

**AI task agent.** Dmitri Kovalchuk showed the chat where Andrei's agent posts a daily digest at 11:30 of items not yet in Jira. It merged yesterday's and today's items and created the leak task on Daniil. It confuses people with the same name (Andrei Bosik vs Andrei Klimovich; Dmitri Kovalchuk vs Dzmitry Chudzinau). Items it listed: how to free, load and decode bonus video; how to handle a release branch (Dmitri and Dzmitry agreed Sergey was right — a release branch is likely, but it must be cut and marked); emulator smoke test on each commit; Flex IQ not scanning tickets in the dark room (Dzmitry has not checked yet today). The agent is very cautious about creating Jira tasks. Pavel: keep reviewing it and see where it leads. Pavel noted yesterday's two-hour meeting with Sergey, Dzmitry and Irina is not in it. Dmitri thought that call had no transcript access. Pavel said it was a full scheduled meeting at 4:30. Dmitri said the digest may cover only this standup; he will ask Andrei. Irina asked if the transcript can be fed to the agent; Dmitri: yes, post it in the chat.

**Close.** Anton must pick today which game he will experiment with; tasks will then be created for that game.

## Decisions Made

- **Extend the MVP1 date to about November 8 or 9; tasks marked MVP2 are done inside MVP1. Scope stays the version that was first cut, with more time.** — schedule. (Decided by Pavel Frolov; confirmed by Irina Shishko)
- **No stutter inside a game: bonus and feature videos are decoded at game entry, not on the way into a feature.** — micro-freeze of about 0.5 s is not acceptable. (Decided by Pavel Frolov, citing Alexander; Daniil agreed)
- **Separate Jira tasks for Daniil: one for the memory leaks (AI-created) and one for the Pixi upgrade.** (Decided by Pavel Frolov)
- **Data center boot-loop recovery is not in MVP1 and not approved yet.** — goal not clear, hard to test. (Decided by Pavel Frolov)
- **Remote RIS protocol versioning moves to a separate meeting.** (Decided by Pavel Frolov)
- **Keep reviewing the daily AI agent digest to see where it leads.** (Decided by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Finish capability 135 (validator pulled-cable check), then start capability 116 (terminal hub link checks) | TBD | Normal | |
| 2 | Alexander Biratko | Set the start date on "FP 12 09" [as heard] | Oct 14, 2026 | Low | Board shows a gradient without it |
| 3 | Alexey Khamin | Create a task to run autotests on real hardware; take the Flex IQ device | Oct 14, 2026 | High | MVP1 end; device shared with Irina |
| 4 | Evgeny Alekseev | Release the FlexPort build that updates firmware by USB stick | Oct 14, 2026 (evening) | High | Promised to Pavel; needed for Oct 15 release |
| 5 | Alexey Khamin, Pavel Frolov | First thing in the morning, check FlexPort firmware update by USB stick | Oct 15, 2026 | High | |
| 6 | Anton Seregin | Build the image with the changed installer and try to install it | TBD | Normal | Flex IQ tasks blocked on terminal |
| 7 | Dmitri Kovalchuk | Add the AI-created leak task (project "NE…") to the team dashboard | TBD | Low | |
| 8 | Pavel Frolov | Talk with Igor; split RK3576 game conversion among Igor, Anton and Daniil; Igor to explain his conversion scripts | Oct 14, 2026 (maybe) | Normal | Goal: about 5 NOVA vertical games on RK3576 |
| 9 | Anton [Needs Val's confirmation which Anton] | Pick the South Dakota game to convert and test on RK3576; tasks to follow | Oct 14, 2026 | Normal | |
| 10 | Dzmitry Chudzinau | Close FlexPort 124, 125, 126; answer mockup remarks in comments | Oct 14, 2026 | Normal | Last day before vacation |
| 11 | Dzmitry Chudzinau | Improve update logs, push another update to the production Flex IQ, check ping to the terminal over LAN with Pavel and Andrei Klimovich | TBD | Normal | Update speed ~6 Mbit/s |
| 12 | Evgeny Kharetski | Test the battery (task 246), then move to MVP2-marked tasks | TBD | Normal | |
| 13 | Evgeny Kharetski | Study the data center boot-loop recovery capability | TBD | Low | Not in MVP1 |
| 14 | Ivan Shpak | Rebuild the port, install, rerun 128; meet Pavel if questions remain | TBD | High | Irina: urgent |
| 15 | Ivan Shpak | Then take autotests from Irina (66) | TBD | Normal | |
| 16 | Dmitri Kovalchuk | Ask Andrei why the two-hour meeting is not in the AI digest | Oct 14, 2026 | Low | |

## Open Questions

- Remote RIS: new protocol on the machine, or version info via the host? Old machines will not send a version. (Dzmitry Chudzinau, Sergey Tsimanov)
- How many games fit in 8 GB on RK3576 when all video is decoded at game entry — 5? (Daniil Stauskiy)
- Why is the production Flex IQ update only ~6 Mbit/s when the signal is good? (Dzmitry Chudzinau)
- Which Flex IQ device does Alexey use while Irina still needs one for tests? (Irina Shishko)
- Exact new MVP1 date: November 8 or 9? (Pavel Frolov)
- Some devices are detected as missing only after work; device logic left as is. (Evgeny Kharetski)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: Daily Standup meeting*
