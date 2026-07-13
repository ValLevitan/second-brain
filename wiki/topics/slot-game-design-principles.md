---
type: topic
title: Slot game-design principles and the progressive-bet-incentive debate
date: 2025-02-21
aliases: [game design principles, progressive incentive, perceived persistence, help screens, caban coin, progressive eligibility, bet incentive, V-Deck design, VDEC, jackpot rush, minimum bet, dimming, attract mode]
source-count: 3
open-questions: 0
---

# Slot game-design principles and the progressive-bet-incentive debate

Durable design principles and one live, unresolved product debate from JVL's game-design reviews. Synthesised from the Feb 21 2025 Fortune Foo Paws review with [[wiki/people/val-levitan.md|Val]], [[wiki/people/lena.md|Lena]], [[wiki/people/efim-podvoiski.md|Efim]] (transcribed "Athim"/"Athene"/"Athena") and [[wiki/people/michael-game-producer.md|Michael]]. Game-by-game details live in [[wiki/topics/jvl-machine-lineup.md]]; this page holds the cross-game design thinking. [[raw/game_design_meeting_february_21_2025.md]]

## The progressive-bet-incentive debate (RESOLVED Feb 28 — do it on the V-Deck, not the math)

**Update (Feb 28, with Juan present):** the debate landed on Val's/Juan's side for the *presentation*, not the math. The group agreed to use the **"jackpot rush" flame approach** on bet buttons **3, 4 and 5** — a flame that grows with the bet (small on the 180 button, medium on 300, large on 600; **nothing** on the 60/120 buttons) plus a **pronounced/unique sound** when buttons 3/4/5 are pressed — to nudge players to bet up **without** any textual claim. Michael, who had argued the opposite on Feb 21, proposed this specific mechanism himself, while restating his "bankroll philosophy" caution (many players stay at min-bet no matter what, and over-glamorising high bets risks making the min-bet experience feel "less than"). The math is **not** changed for this. Alongside it, JVL will also A/B a **second math pack** with higher (Chinese) bet levels — see [[wiki/decisions/2025-02-28-fortune-foo-paws-second-math-pack.md]]. [[raw/Game design part 1 - Feb-28-2025.md]] [[raw/Game design part 2 - Feb-28-2025.md]]

The central argument of the Feb 21 call, which this resolves:

- **How JVL's progressive works today (Efim):** the displayed progressive value is the **same at every bet level**; what changes with bet size is the **probability** of winning it (probability is proportional to the bet). So a min-bet player is eligible for the same $25,000 major, just far less likely to hit it. There are two ways to build it — scale the progressive *value* to the bet, or scale the *probability* to the bet — and JVL (like the competitor "Cointreau") uses the probability method. [[raw/game_design_meeting_february_21_2025.md]]
- **Val's objection:** a player **cannot read the math** — the only thing a player perceives is the digits on the meter, which don't change with bet. Passing on [[wiki/people/juan-martinez.md|Juan]]'s point that a player needs a *visible* incentive to bet more, Val argued JVL may be "making the wrong games" if there is no perceptible reason to bet up. He stressed it was an opinion, not an order, and asked to **park it and revisit with Juan**. [[raw/game_design_meeting_february_21_2025.md]]
- **Why the industry does it this way (Michael):** scaling the value to the bet would drop the min-bet jackpot to a non-"life-changing" number (e.g. $5,000), discouraging the many min-bet players; hanging the big $25,000 as reachable "at any bet" (à la IGT Mega Millions/Mega Bucks) gives every player something to chase even though the odds are tiny. Michael conceded it is "kind of deceptive" but is the direction the industry has gone. [[raw/game_design_meeting_february_21_2025.md]]
- **Val's alternative floated and rejected:** award **no progressive at minimum bet** (only at higher bets). Michael/Efim pushed back hard — it would **cripple the game**, because the top-10 performing games all offer **full progressive eligibility at any bet**; only the "quick-hit tower" genre requires max bet, and that is its own category with its own player base. A player would skip a JVL game that isn't eligible at 60 credits when every competitor is. [[raw/game_design_meeting_february_21_2025.md]]
- **Where it landed:** use the **V-Deck (live secondary screen)** and the bottom promo text as the surface to *sell* betting up — sparklier/hotter high-bet buttons, a slightly larger progressive meter, "bet more for a better chance at progressives" copy — rather than changing the math. Val wants Lena to present a **visual proposal on Friday** and the incentive question revisited **with Juan on Tuesday**. [[raw/game_design_meeting_february_21_2025.md]]

## Durable design principles

- **Signage vs game-screen detail:** the ornamental frame is kept on the **game screen** but removed from the **signage/progressive sign**. At 10–50 ft, granular detail "becomes noise" and distracts from what matters on signage — the numbers. Signage exists to be read at distance. [[raw/game_design_meeting_february_21_2025.md]]
- **Help-screen icon versions:** when a symbol is shrunk for the help screens it can lose the detail that distinguishes it (e.g. the subtle red outline that makes a **"golden red" Caban coin** different from a plain **gold** Caban coin). The fix is to make a dedicated **iconographized version** of the symbol for help screens / sticker lines so the player, Ivan, and GLI can tell symbols apart. Help screens should fit on as few pages as possible (competitors' norm; players don't read them) rather than being broken into 25 tiny-font pages. [[raw/game_design_meeting_february_21_2025.md]]
- **Perceived persistence ("fat cat"):** cats grow and shrink on-screen based on fake/real hits; the player chases whichever cat is "fattest / closest to triggering" (a horse-race feel), not a specific colour. Gold/white/blue Caban coins and cats have close-but-not-identical EVs; gold is centred and slightly larger only because gold *connotes* wealth, not because it pays more. In a bank of machines each machine can show a different cat as the largest. [[raw/game_design_meeting_february_21_2025.md]]
- **Topper modes:** "idle mode" shows only meters; "attraction mode" cycles character animation / fireworks / logo. A four-machine "cross" configuration has a different flow than a row. Toppers sit physically higher than players, so character eye-lines are set accordingly. [[raw/game_design_meeting_february_21_2025.md]]
- **Bet levels for Fortune Foo Paws** were set to **60 / 120 / 180 / 300 / 600 credits** (1-2-3-5-10), with Val correcting a placeholder of 240/500 to 300/600. [[raw/game_design_meeting_february_21_2025.md]]
- **Design against the market, not the field:** Val's rule — "only games that make money are the ones we look at… we don't waste time on games that don't make money"; the competitive reference here is **Cointreau** (Juan asked for a game close to it). [[raw/game_design_meeting_february_21_2025.md]]

## The math/mass test tool

- [[wiki/people/dmitry-khandov.md|Dima]] and [[wiki/people/andrey-khandov.md|Andrey]] Khandov are building a **primitive playable game version** that connects **Miranda to the math ("mass") server**, so Michael and Efim can play-test the real math with placeholders (no final animation) — "what we always wanted and never had," and critical because the math can't wait for a finished machine. Val wants QA ([[wiki/people/ivan.md|Ivan]] or [[wiki/people/irina-makarych.md|Irina]]) to verify the brand-new tool, since it is a different product from the shipping game and won't translate one-to-one. The tool needs a **show-mode** menu (to force specific bonus outcomes) in addition to pushing random numbers, but that is for later QA stages. [[raw/game_design_meeting_february_21_2025.md]]

## Further design principles (Feb 28)

- **Attract mode / no-credits vs credits state:** the **FireEyes Wink** build introduced full-screen demo videos of all games in attract mode, which behave **differently with credits on the machine versus zero credits**. Design goal: the attract video **shows off** the visually interesting free-spins mechanic to look winnable, but deliberately **doesn't give away** the deeper "fiery ice" bonus — a tease/"come-on," not a full reveal. [[raw/Game design part 1 - Feb-28-2025.md]]
- **Dimming the non-choice reels (subtle):** when a game dims reels to steer the player to a choice (the sparkly-arrow reel), the dimming must be **very subtle** — the player must still clearly read the symbols on the dimmed reels. This is *not* the heavy overlay some competitors use; it just draws the eye. (Explicitly the opposite intensity from the progressive gray-out on HG-6, which was minimised.) [[raw/Game design part 1 - Feb-28-2025.md]]
- **Denomination buttons must always have one selected:** the selected denom is shown brighter **plus an outline** (brightness alone isn't obviously "selected"); the machine must **default to one selection** and never sit in a state with no denom selected (e.g. 1 cent highlighted at zero credits). Idle/zero-credit state shows an **"insert credits"** message. [[raw/Game design part 1 - Feb-28-2025.md]]
- **Progressive meter layout:** show the two current progressive levels (the majors) on top in place of the old white/blue section; on the V-Deck, keep the two progressive values the **same size** for clean symmetry (Val's push to enlarge/reposition "mega" was dropped). [[raw/Game design part 1 - Feb-28-2025.md]]
- **Minimum-bet direction:** current Fortune Foo Paws min bet is **60 credits**; Michael recommends raising the minimum to at least **70**, noting 70 and 88 credits are "the new norms" among premium competitor boxes. Val prefers to keep the lower minimum on this cabinet and **reserve higher bets for the next cabinet** and the data learned from this game. Framing: in South Dakota/Georgia/Puerto Rico JVL is "a Porsche, not a Toyota"; Florida is a **practice ground** where JVL won't take real floor money until ~mid-2026. [[raw/Game design part 1 - Feb-28-2025.md]]
- **"Maneki-neko"/"Manikineka Cats"** is a Florida-specific product with different math from the South Dakota/Georgia versions. [[raw/Game design part 1 - Feb-28-2025.md]]
- **Taxonomy discipline:** Val asked everyone to use consistent, proper taxonomy in meeting invites/descriptions (Michael links conversations and documentation to specific meetings), and asked Michael to state each meeting's objective in the invite so reviews aren't open-ended standbys. [[raw/Game design part 2 - Feb-28-2025.md]]

## Open questions

- ~~The progressive-bet-incentive question~~ **resolved Feb 28** (see the debate section above): use the V-Deck flame-on-buttons-3/4/5 + sound presentation and A/B a second higher-bet math pack; the base math is unchanged. [[raw/Game design part 1 - Feb-28-2025.md]]

## Sources

- [[raw/game_design_meeting_february_21_2025.md]]
- [[raw/Game design part 1 - Feb-28-2025.md]]
- [[raw/Game design part 2 - Feb-28-2025.md]]
