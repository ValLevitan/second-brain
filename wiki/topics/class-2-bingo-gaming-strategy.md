---
type: topic
title: Class II bingo gaming strategy (bingo engine, rules, market)
date: 2025-03-20
aliases: [Class II, Class 2, bingo engine, bingo game rules, auto-dobbing, asynchronous bingo, tribal gaming, Mikazuki, single ticket system, game-ending pattern]
source-count: 1
open-commitments: 2
open-questions: 3
---

# Class II bingo gaming strategy (bingo engine, rules, market)

JVL's exploration of entering **Class II gaming** — bingo-based slot machines for US tribal casinos — led by [[wiki/people/will-jones.md|Will]] (ex-SDG/"Valley" Class II expert) with Val, [[wiki/people/juan-martinez.md|Juan]], and the mathematician on the call (transcribed "Ethan" — **owner-confirmed 2026-07-15: [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]**). All from the ~86-minute Class II bingo-engine session, ~Mar 20 2025 (date inferred — see the meeting stub [[wiki/meetings/2025-03-20-class-2-bingo-engine-call.md]]). [[raw/class_2_bingo_engine.md]]

## Why Class II is open ground: the standards omit bingo game rules

- Will's history: pre-standards tribal gaming "felt like the Wild West" — one (unnamed) tribe wasn't scanning incoming vouchers at all; regulation ranged from strict Washington-state tribes to "Oklahoma, the crazy, crazy Wild West." Standards arrived "sometime around 2000… 2005, 6, 3, I don't remember." [[raw/class_2_bingo_engine.md]]
- The key gap: the Class II standards contain **no definition of what a bingo game is** — no bingo game rules. The vendor defines the game rules; the **tribal authority's approval** is what a placement needs. GLI (or another lab) certifies Class II standards compliance, but "our game is, in fact, bingo" needs its own support. [[raw/class_2_bingo_engine.md]]
- Old-school conservative interpretations (every game needs at least two live players) produced uncompetitive games — Juan-side memory: at "two, three in the morning" no second player was available, and Class III casinos "rubbed that in our faces." [[raw/class_2_bingo_engine.md]]

## Implied rules (to keep) and accepted norms (to embrace)

Implied rules Will says a bingo game must keep: players compete against one another (not each alone against the system); balls are drawn and marked on unique player cards; a predefined card pattern gives a player win; one pattern is the game-ending function. [[raw/class_2_bingo_engine.md]]

Accepted norms in today's tribal market that a competitive product must embrace: [[raw/class_2_bingo_engine.md]]

1. **Asynchronous play** — a player can play any time, even within a shared bingo session.
2. **Inter-game prizes/patterns plus one game-ending pattern** — of a million patterns, almost all can map to prizes or no-wins; one ends the game session.
3. Long-lived sessions supporting those asynchronous events.
4. **Prize scoring** — scoring on patterns (not just pattern matching) creates pay tables "almost equivalent to class three."
5. **Auto-dobbing** — the machine marks the card and claims the win; the player never has to yell bingo.

## The candidate game-rule design (with the mathematician)

- Only the **very first session in a machine's life** requires two players before play commences (covering the freak case of a game-ending outcome on the first play); casinos' routine **coin tests** would create that first session before any real player sits down. After that the system auto-creates enough sessions that no player ever waits. No "master BGM" concept is needed (Will). [[raw/class_2_bingo_engine.md]]
- Scoring: patterns are scored by the **index of the ball at a special spot on the card**, yielding "hundreds of millions of different potential outcomes" and pay tables mapped probabilistically (big prizes on low-probability events). [[raw/class_2_bingo_engine.md]]
- The mathematician's assessment: the approach's many very-fine-probability events, grouped, can "reproduce the pay distribution of a slot game practically… exactly"; he is comfortable he can match a game's actual distribution to bingo outcomes. His caution: a fill-the-card game-ending win at ~30 balls drawn is too improbable ("the game will never end") — draw more balls, or allow more than one winning pattern. [[raw/class_2_bingo_engine.md]]
- Candidate game-ending pattern (Will): **four corners in the first four balls**, ~1 in 1.3 million — a prize can be tied to it but need not be. The mathematician's objection: it breaks the one-ball-index scoring rule ("we'll work on it"). [[raw/class_2_bingo_engine.md]]
- **Ties/split prizes:** essentially eliminated — asynchronous play means the first game request wins a progressive and the second gets the reset (in the old days simultaneous-hit solutions "didn't happen in the field, basically"). [[raw/class_2_bingo_engine.md]]
- Ideas parked: Rocket Gaming's "**Golden Ball**" (flooding extra balls when a progressive is due — a must-hit-by feature, run as a separate premium product at $0.25 with its own math); progressive segmentation by denomination (penny games on one progressive, 5-cent on another) from the pre-multi-denom era. [[raw/class_2_bingo_engine.md]]
- A player-facing wish (raised from the floor-operations side): keep an **ever-changing bingo card the player can toggle** (the SDG version's touch-and-change card bred decades of player praise and superstition rubbing). Will: the design doesn't eliminate it, but card-switching must never give knowledge of an already-drawn ball sequence; also mind the finite card set so the game-ending card can't be burned through. [[raw/class_2_bingo_engine.md]]

## Integration and architecture

- Target casinos now run consistent **single-ticket systems**: every ticket comes from one system (e.g. Bally SDS — transcript spells "Bali"), with each machine connected by an S2S interface — unlike the early days of four isolated, color-coded ticketing systems on one floor. [[raw/class_2_bingo_engine.md]]
- JVL's games would connect **via SAS (6.0 / "SAS 6xx") to the casino's player-tracking/accounting system**, plus a second, Ethernet connection to the JVL Class II system handling the game/bingo portion — a dual connection on every machine. No new software invention needed if the games are SAS-compliant. [[raw/class_2_bingo_engine.md]]
- **Cloud vs on-site:** plan for cloud-hostable services but never exclude on-premise — the Seminoles "freaked out" at a mention of Amazon AWS, believing off-reservation data is accessible to the federal government (transcript renders a name "McNabb" here — unclear). [[raw/class_2_bingo_engine.md]]
- **Fault tolerance is the big technical risk:** a server-based game means a system or connection failure can take down a whole bank or floor of JVL games, so the system needs adequate fault tolerance — and remote access, which Class II regulators tolerate ("I could dial into the system from my house… things that class three regulators frowned on"). Remote RIS (remote initial setup) "is totally expected and acceptable in the class two world." **Daily fees** per machine/system are also accepted in Class II, funding that remote support. [[raw/class_2_bingo_engine.md]]
- Val's architecture question: JVL's back-office framework is "very old" and may need architectural redesign, while Class III is switching to the HTML5-based omni-channel framework — so now may be the time to assess the whole backend. Will: don't assume none of it is reusable — ask first; a new bingo service space could later extend to HHR, VLT "or something else under the sun." [[raw/class_2_bingo_engine.md]]
- Sequencing vs HHR: Val — "we have our HHR course charted… I have no doubts that we could probably squeeze this architecture before we even have to jump into HHR." [[raw/class_2_bingo_engine.md]]

## Market

- **First target customer: "Mikazuki"** (transcript spelling) — formerly a "bounty one" system (unclear), switched ~two years earlier to **Aristocrat Oasis**, 100% single ticket floor on SAS 6xx (Juan). [[raw/class_2_bingo_engine.md]]
- **Texas:** at least two of three tribal casinos already run Bally SDS; Bally told Juan ~two months earlier they were close to converting the third — "by the end of summer, realistically, they'll all be on a Bally SDS single ticket system." [[raw/class_2_bingo_engine.md]]

## IP and legal path

- The game rules may tread on others' IP — "the space is pretty clogged." Plan (from Will's former-colleague advice): outside expert legal review validating the engine is bingo (paper to carry into the first customer), a proper patent search by an outside team, and in the best case a patent of JVL's own method. Juan-side offer: a good relationship with "the tribes attorney that handled all their Class 2 work and the state compact." [[raw/class_2_bingo_engine.md]]

## Open commitments

- [ ] Val — conference with Efim on the Class II architecture pairing and get back to Will "probably Monday" — due ~2025-03-24 (the Monday after; inferred) — [[raw/class_2_bingo_engine.md]]
- [ ] Will — next-step document defining the game rules well enough for outside legal review — due unspecified — [[raw/class_2_bingo_engine.md]]

## Open questions

- ~~Is the transcribed "Ethan" the same person as Efim Podvoiski?~~ **RESOLVED (owner ruling 2026-07-15): yes.** — [[raw/class_2_bingo_engine.md]]
- Exact identity/spelling of the first target customer "Mikazuki" and of the attorney "Losh." — [[raw/class_2_bingo_engine.md]]
- What "bounty one" (the system Mikazuki replaced) refers to — unclear in the source. — [[raw/class_2_bingo_engine.md]]

## Sources

- [[raw/class_2_bingo_engine.md]]
