# Meeting Summary — GCOAM Match3 Progressive Development Sync
**Date:** May 29, 2026, 10:03 AM Eastern
**Duration:** ~25 minutes
**Attendees:** Val Levitan, Pavel Frolov, Igor Metelski, Evgeny Kharetski (Zhenya), Anton Liashkevich, Irina Shishko, Lena Zhukova
**Also referenced:** Juan (product), Michael (stakeholder), Ivan Shpak / "Vanya", Dima

## Summary

A short status sync on the GCOAM Match3 progressive game. The headline problem: the team still cannot actually run and look at the build, so nobody — not Juan, not Michael, not Lena — has seen the progressive working. Everything else flows from that.

**Why it's blocked.** Anton finished updating the game resources and home screen yesterday and is now recompiling the games. But to view games you need a "RIS" (the config the data center uses to bring games up), and right now the RIS only covers Igor's 3 games. The Linux build kept failing because game files were missing from it, so the machine never came up. During the meeting Anton said he found the compilation error and committed a fix, and Irina started a fresh Linux build.

**The plan everyone agreed on: Linux first.** Get the build to compile, bring the machine up on Linux, confirm the progressive actually contributes and draws. Once that works, Evgeny copies the known-good settings over for Windows testing and freezes a Docker image to hand to designers. Building proper auto-deploy (CI/CD) infrastructure was ruled out for now — it won't be ready by June 7.

**Progressive draw is the real unknown.** Evgeny can run the progressive in Docker but they have never successfully drawn (won) a progressive. He thinks it's a settings problem but can't prove it until the machine is up. On the framework side, Igor reports a BaseValue that gets recalculated by the math and doesn't match the progressive's value; his frontend also throws stack overflows. Igor won't sign off on multiprogressive support until he sees both the data center and the framework behave correctly end to end.

**Match3 framework work.** Igor added baseline framework support for a Match3 progressive. The snag: the math engine initializes much earlier than the progressive manager, so progressive parameters (level / center type, plus a minimum bet) need to be passed in at math init. Igor needs an extra request to the data center for this. Evgeny offered a quick temp-storage workaround; Pavel rejected it and insisted on a proper standard API, "no crutches." Igor can start the Match3 bonus build in stages before this lands, but only partly — it can't be fully verified until the progressive works.

**Designer hand-off.** Pavel framed running the progressive controller on Windows as an open worry; Evgeny pushed back — it's just Docker, designers only need to be taught to use it. Once the team confirms it's ready for testing, Evgeny will write a short step-by-step Docker guide. Designers had Docker Desktop installed for Cline and can reinstall it. Pavel called this the smaller problem versus building the Windows games.

## Decisions Made

- **Linux first.** Get the build compiling and the machine running on Linux before doing anything for Windows or designers — so the team can finally see the progressive draw. (Proposed by Irina, agreed by Lena and the room.)
- **Builder fix is top priority.** No point inserting more resources while nobody can see the result. (Lena; endorsed by Pavel.)
- **Freeze a Docker image / RIS snapshot for designers** rather than building new auto-deploy infrastructure — the latter can't be ready by June 7. (Evgeny.)
- **Parameter passing must use a standard API, not a temp-storage workaround.** (Pavel, overruling Evgeny's quick-fix offer.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Anton Liashkevich | Committed the compilation fix found during the meeting; keep recompiling the games with the updated resources | In progress | High | Was blocking the Linux build |
| 2 | Anton Liashkevich | Modify the builder to build all games by default and add a launcher selector so designers pick which RIS/variant to run | TBD | Normal | Lets designers run any build without rebuilding |
| 3 | Irina Shishko | Launch the Linux build now and post the build result in the team chat so everyone can see it passed | May 29, 2026 | High | First gate for the whole plan |
| 4 | Evgeny Kharetski | Get the progressive to draw on Linux; once it works, copy the known-good settings for Windows testing and freeze a Docker image for designers | TBD | High | Unblocks everyone downstream |
| 5 | Evgeny Kharetski | Provide Igor a proper data-center request/API to deliver the progressive level + minimum bet at math init (no temp-storage workaround) | TBD | High | Needed for Match3 progressive at startup |
| 6 | Evgeny Kharetski | Write a short step-by-step Docker guide for designers once the build is ready for testing | After build is testable | Normal | Pavel called this the smaller problem |
| 7 | Igor Metelski | Continue Match3 bonus build in stages (math, then game logic + resources); keep the multiprogressive-support ticket open until the progressive draw is verified | TBD | High | Can start partly "blind" before full progressive support |

## Open Questions

- **How to deliver the progressive parameter to Igor at math init** — Evgeny proposed a temp-storage copy of the last RIS; Pavel wants a standard API instead. Resolution pending; Igor said he just discussed it with Dima.
- **BaseValue mismatch** — the framework reports a recalculated BaseValue that doesn't match the progressive's. Root cause not confirmed (settings suspected); needs the Linux machine up to verify.
- **Whether designers reinstall Docker Desktop** — they had it for Cline, dropped it for Claude. Minor; Evgeny to supply instructions.

**JIRA tickets referenced (numbers approximate — garbled in transcript):** ~1195 (Match3 progressive completion), ~1198 (multiprogressive support), plus a "Match3 progressive bonus implementation" task.

---
*Processed from Teams transcript on May 29, 2026*
*Source meeting: GCOAM Match3 progressive development sync (transcribed May 29, 2026)*
