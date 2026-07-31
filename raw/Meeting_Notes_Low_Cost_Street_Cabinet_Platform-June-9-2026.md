# Meeting Summary — RK3568 HW as a Platform for Simple Slot Games
**Date:** June 9, 2026, 12:07 PM Eastern
**Duration:** ~22 minutes
**Attendees:** Val Levitan, Genadi Peari, Pavel Frolov, Alexander Biratko
*(Spoken mostly in Russian; summarized in English. Follows the June 8 "Low-Cost Street Machine Design" session — this is the feasibility read Val wanted from Biratko and Pavel.)*

## Summary

The team discussed building a low-cost "street" slot machine to compete in price-sensitive markets like Texas, where JVL's Flex cabinet is too expensive to sell.

The plan is to strip the cabinet, not cheapen the games. Genadi described the target: one vertical touchscreen, at most two buttons, one or two backlights, no topper, no video board, no amplifier, no separate counter board. Val was firm that this is not a low-quality product — games keep normal resolution and color. Biratko's animation-only online games were raised as an example, but Val rejected that level of downgrade.

Savings come from components, not visuals. Val's examples: switching the bill acceptor saves about $600 and lets them simplify to a single nightstand-style door (no front access). Dropping the topper and video board lets them move off x86 to a cheaper ARM board. NOVA already runs on ARM, so it isn't tied to x86.

On hardware, they have RK3568 (Rockchip) boards but only at 2 GB RAM, which is too little. Pavel and Genadi favor stepping up to the RK3588 — about twice the cores, 4x video decode, handles 8K — for only ~$10 more. RK3576 is an in-between option.

Memory was the main sizing question. Each game is ~500-700 MB and must load fully into RAM to switch quickly (that's why Flex uses 16 GB). Capping the machine at ~6 games — which fits the planned subscription/ELT model — means 4 GB might work, but 6-8 GB gives headroom, especially with progressives. Decision: order 8 GB samples, measure real use, then size down if possible.

Val rejected buying an Orange Pi 5 (RK3588, 16 GB) locally in Minsk; he prefers ordering proper samples from China. He asked Genadi to bring two boards, not one, from a more reliable/cost-effective manufacturer, and to standardize on that manufacturer for support across all products.

Testing: port Calle Ocho — the only game currently on NOVA — strip the topper and video-decoder components, run it, then load 5-6 copies at once to measure memory and performance. This can start now on the existing RK3568 boards while the RK3588 samples are ordered.

Genadi noted prices are rising: the RK3568 supplier now wants $100 (up from $50 in December), driven by memory.

Side idea: because street machines stand close together vertically, add a shared progressive jackpot displayed across the bank like a scoreboard.

## Decisions Made

- **Build a low-cost "street" cabinet** — single vertical touchscreen, ≤2 buttons, cheaper bill acceptor (~$600 saving), simplified single door, no topper, no video board, no amplifier. Reason: enter cheap markets like Texas. (Val, Genadi)
- **Keep game quality** — normal resolution/color, not the cut-down online-game level. (Val)
- **Cap at ~6 games per machine** — enables smaller memory, fits the subscription/ELT model. (Val)
- **Target the RK3588 platform** — far more powerful than RK3568 for ~$10 more. (Pavel, Genadi, Val)
- **Order 8 GB sample boards, measure, then size down** rather than guessing. (Pavel, Genadi)
- **Order from China, two boards, more reliable manufacturer** — not the local Orange Pi 5; standardize on that manufacturer for support. (Val)
- **Test by porting Calle Ocho** (strip topper + video), then run 5-6 instances. (Pavel, Alexander)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi | Contact the supplier and report the RK3588 board price | June 10, 2026 | High | Gates the sample order |
| 2 | Genadi | Order two RK3588 sample boards (8 GB) from China from the more reliable manufacturer; fold that manufacturer into support for all products | TBD | High | Avoids local Orange Pi; sets the supply chain |
| 3 | Pavel | Port Calle Ocho to the RK board — remove topper and video-decoder components and run it (can start now on existing RK3568) | TBD | High | Calle Ocho is the only current NOVA game |
| 4 | Alexander | After it runs, load 5-6 copies at once and measure memory use and performance smoothness | TBD | Normal | Validates the memory sizing |

## Open Questions

- Final RAM size (4 / 6 / 8 GB) — decide after measuring real use on an 8 GB sample.
- RK3588 price and which manufacturer to standardize on — Genadi to confirm.

---
*Processed from Teams transcript on June 9, 2026*
*Source meeting: RK3568 HW as a platform for simple slot games*
*Initiative: Street Machine Design Direction (a.k.a. Street Cabinet)*
