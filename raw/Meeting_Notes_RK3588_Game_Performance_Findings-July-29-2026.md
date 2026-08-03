# Meeting Summary — Findings_from_RK3588
**Date:** July 29, 2026, 7:00–7:30 AM Eastern (recording 7:03–7:19 AM)
**Duration:** ~16 minutes
**Attendees:** Val Levitan, Pavel Frolov, Alexander Biratko, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_RK3588_Game_Performance_Findings-July-29-2026]]

## Summary

Pavel reported on testing a Nova-platform game (Caliente) on the Rockchip RK3588 board. His team extended the SDK to support the board because the stock software was too limited, then gave the board to Daniil, who installed the game, ran a local gaming server, and launched the game in a browser. It worked.

**Performance.** The base game runs smoothly — clean visuals, no crashes, a steady ~60 FPS. Stutter appears only on transitions into bonus games, wins, or free spins. The cause is memory: the tested board has only 4 GB of RAM, so it runs out and starts swapping textures in and out. The CPU and graphics core otherwise handle video decode and rendering fine, with no visual artifacts.

**Memory sizing.** Alexander estimated the current game is about 500–800 MB short of the RAM it needs to load all textures at once. One game plus the system plus LGS uses roughly 5 GB; each additional game adds at least 1 GB. So 8 games is about 5 + 7 = 12 GB, and a 16 GB board leaves ~4 GB of headroom. An 8 GB board only covers about 2 games. Boards are available in 4, 8, and 16 GB; onboard storage (32–64 GB) is more than enough for years of games. Textures could also be hand-optimized to trim roughly 200 MB per game (from ~1 GB toward ~800 MB) if needed.

**Multi-progressive / multi-product.** Irina asked whether running multi-progressives that mix games from different products (e.g. Caliente + Peaches + Jackpot Rush) would change the memory picture. Alexander said it would add some resources per game but likely isn't critical, and the 16 GB estimate still holds. Irina noted the multi image has grown ~30% versus the old one, approaching ~8 GB.

**Displays.** Everything so far ran on a single Full HD screen. The team should test with two monitors. The board supports at most 2 monitors, so a horizontal cabinet layout isn't possible — only a compact setup (one main screen plus a topper). One of the board's video interfaces is LVDS, which is impractical to connect; they'd prefer a board variant with 2–3 uniform HDMI outputs so all monitors use the same cabling. A progressive controller would add a database and controller app, i.e. a bit more load.

**Board options.** Three boards arrived: RK3568 (same as the old one), RK3576, and RK3588. The 3576 and 3588 are effectively comparable (same CPU cores), so the 3588 serves as the evaluation platform. Pavel checked the RK3399 — it's an older generation and not faster than the 3588. The 3588 is currently the top option.

**Developer access.** Becoming a Rockchip developer costs about $3,000. The earlier application was filed for the RK3568; a fresh request is likely needed for the correct platform (3588), and each platform may be a separate repository/cost. Pavel to look into it. Val noted Pavel is already on the relevant email thread and is better placed to write the specifics.

## Decisions Made

- **Order an RK3588 board with 16 GB RAM** — 16 GB fits up to 8 games with headroom; the 4 GB test board is the source of the bonus-game stutter. (Val, with Pavel/Alexander input)
- **Prefer a board variant with 2–3 uniform HDMI outputs, avoiding LVDS** — LVDS is impractical to connect. (Val/Pavel)
- **Test the game on two monitors** — single-screen testing done; validate the 2-monitor compact layout. (Val)
- **RK3588 is the evaluation platform** — 3576/3588 comparable, 3399 is older and no faster. (Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Send Genadi Peari the board-order request: RK3588 with 16 GB RAM, ideally 2–3 uniform HDMI outputs (no LVDS) | TBD | High | Val said he'd have the transcript produce a draft email to Genadi |
| 2 | Genadi Peari | Order the RK3588 board (16 GB, uniform HDMI outputs); confirm whether a memory upgrade needs a new board (RAM is soldered) | TBD | High | Board RAM is not socketed — a different board is required for 16 GB |
| 3 | Pavel Frolov | Investigate Rockchip developer access (~$3,000) for the correct platform (RK3588, not the earlier 3568); confirm whether each platform is a separate repo/cost | TBD | Normal | Pavel is already on the Rockchip email thread and better placed to write specifics |
| 4 | Pavel Frolov / Alexander Biratko | Connect and test the game on two monitors (compact one-main-plus-topper layout) | TBD | Normal | Board supports max 2 monitors |
| 5 | Alexander Biratko | Optionally hand-optimize textures to trim ~200 MB per game if memory pressure warrants | TBD | Low | Designers' textures were under-optimized |

## Open Questions

- Is Rockchip developer access per-platform (separate repo and separate $3,000 fee) or shared across boards? (Raised by Pavel; his to resolve.)
- Exact memory impact of multi-progressive/multi-product images once ported to Nova — estimated non-critical but not measured. (Raised by Irina.)

## Dispatch Log

- 2026-07-30 — Undertaking #1/#2 dispatched: email "RK3588 board order: 16 GB memory, uniform HDMI outputs" sent to Genadi Peari, cc Pavel Frolov, Irina Shishko, Yuri Zakharenkov (approved by Val).
- 2026-07-30 — Undertakings #3/#4 dispatched: email "RK3588: Rockchip developer access and the two-monitor test" sent to Pavel Frolov, cc Alexander Biratko (approved by Val).

---
*Processed from Teams transcript on July 29, 2026 (scheduled watcher, capture-only)*
*Source meeting: Findings_from_RK3588*
