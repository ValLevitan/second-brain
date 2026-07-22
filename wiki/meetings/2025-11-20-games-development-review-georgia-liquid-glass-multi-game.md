---
type: meeting
title: Games development review — Nebraska licensed, South Dakota 7-game slate, Georgia liquid-glass multi-game (depart from Peach) (Nov 20 2025)
date: 2025-11-20
aliases: [games development review Nov 20, Georgia liquid glass multi-game, depart from Peach, 12 enabled games Georgia, three progressives Georgia, Nebraska approval draft letter, South Dakota seven games, Jackpot Rush Georgia sameness, Felipe Georgia variety]
source-count: 2
open-commitments: 2
open-questions: 2
---

# Games development review — Nebraska licensed, South Dakota 7-game slate, Georgia liquid-glass multi-game (depart from Peach) (Nov 20 2025)

**Date:** 2025-11-20 · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]] (Georgia sales). English.

The weekly game-development review, with Felipe brought on to argue the Georgia product strategy. Threads: [[wiki/projects/georgia-market-rollout.md]] (Nov-20 section), [[wiki/topics/slot-game-design-principles.md]], [[wiki/topics/game-production-throughput-strategy.md]]. **Distinct** from the [[wiki/meetings/2025-11-06-game-development-review.md|Nov-6 review]] (which introduced Liquid Glass UI, La Rosa South Dakota, Cool Cat, $0.25 bet) and the Nov-13 "Development Review" — this is the Nov-20 session and its centre of gravity is the **Georgia** multi-game decision.

**§12 — ONE meeting recorded in two segments (not two meetings).** Both raw files share the Teams recording base name **`Games_development_review`**: [[raw/Games_development_review.md]] is the **8m 12s opening** (header 10:00 PM, base `…_220856UTC`) and [[raw/Games_development_review (1).md]] is the **1h 8m 45s main body** (header 10:08 PM, base `…_170849`). The opening ends with Val telling the group to "focus on Felipe" and Felipe beginning his Georgia pitch about Jackpot Rush; the main body begins with Felipe **continuing that exact pitch** — same attendees, same topic, ~contiguous. Recording split, not two meetings → **one stub, facts recorded once**, each cited to its segment. Corpus-wide `qmd update` + grep confirms neither file is cited elsewhere. (The 8-min opening carries unique material — the Nebraska letter and the South Dakota 7-game slate — that the main body does not repeat.)

## South Dakota / Nebraska status (opening segment)

- **Nebraska is essentially licensed.** Juan received the **Nebraska approval draft letter** from the regulator; one more affidavit is needed and JVL is licensed — target to **start selling in Nebraska around December 1**. JVL has shipped **10 machines to South Dakota**, 5 of which have been sent on to a partner in Nebraska (hoping to install before the December holidays). [[raw/Games_development_review.md]]
- **South Dakota performing well.** JVL is the **#1 win-per-unit** of all manufacturers there despite having only **6 games**; win-per-unit dipped slightly on bad weather but coin-in stayed relatively high. [[raw/Games_development_review.md]]
- **Michael proposed a 7-game South Dakota slate** (concepts, all subject to art rework): **La Rosa** (a clone of Lion Riches, chasing that top performer), **Jungle Jaguar Extreme** (JVL's answer to IGT buy-a-bonus games — pay-for-free-spins mechanic), **Midnight Money** (a fresh "2026" version), **Cold Cash**, **Keops Wild Plus** (Egyptian), **Chinese Dragons** (5-line Chinese theme, to replace the underperforming 3×3 Dragon Pays), and a **dual-screen Rodeo Spins** test (one-line/3-reel, soft math like Liberty Spins). Michael's rule: nearly all these older titles get their art "retouched, redone, reworked." [[raw/Games_development_review.md]]

## Georgia — the core decision (main segment)

- **Felipe's complaint: the 5 Jackpot Rush games all feel the same.** All are 25-line, center-reel-nudge games; players at the Gamoa event asked "is it the same game?" Felipe argues that with only a few machines per location, each title must feel different — Georgia players respond to changes in **reel format, line style and feature structure**. He cited that Aristocrat / Light & Wonder mix 1-line, 40/50-line, 243-ways and 1024-ways in one package, and that the popular **Mo Money** is a **one-line game** in Georgia (three lines in bonus) — which surprised Michael. [[raw/Games_development_review (1).md]]
- **Decision — Georgia vertical liquid-glass multi-game product; three categories, three progressives.** The group agreed to build a **vertical, liquid-glass** multi-game that combines three distinct categories — the **6 existing Peach/lines-and-ways vertical titles**, the **5 Jackpot Rush titles**, and the **6 Fiery Ice Link titles** — each with its **own independent progressive** (Jackpot Rush's progressive tower, Fiery Ice, and Peach cannot share; Efim/Lena flagged the three-progressive presentation as the hard part, with input already sought from **Irina**). All titles would be **submitted**, but only **12 enabled on screen** at once, operators toggling via **RIS** to reduce Eclipse submission cost. Michael's summary, confirmed by Juan: liquid-glass vertical, 6 + 5 + 6, three distinct progressives "to figure out." Juan to **write the requirements / REQ** and adjust the Jira plans; Val corrected "design stage" to "concept stage." [[raw/Games_development_review (1).md]]
- **Depart from the "Peach" brand; drop the Georgia Lottery logo.** Val and Juan want to retire the dated "Peach" / Georgia-Peach branding and the Georgia Lottery logo (no competitor advertises the lottery), using the liquid-glass launch as the clean break. The new theme should be **neutral / "aspirational wealth"** — explicitly **not** Georgia-native, historical or cowboy (players are largely Hispanic / African-American / South American; Val: "something hip, cooler"), and repurposable outside Georgia (e.g. Colombia). Theme to be decided later. [[raw/Games_development_review (1).md]]
- **Val's pricing angle:** enable all the games and **raise the price ~$2,000**, framed on the industry-wide **tariff** increases buyers expect this year; run **12 games with the new interface**, starting with **vertical** to see how the market reacts before revisiting dual-screen. [[raw/Games_development_review (1).md]]
- **Strategy shift on machines-per-location.** Val laid out the market math: Georgia now has ~**35,000 machines across ~6,500 locations** (~5.5 machines/location ≈ one machine per vendor) versus ~24,000 machines / ~6,000 locations when JVL and IGT were the main players. Brands now include **IGT, Light & Wonder, Aristocrat, JVL, Novomatic** and newly **Konami**. Because JVL now targets **one machine per location** (not 2–3), a **larger game library per machine** is more appealing — though Val flagged the risk of a library "arms race" (enable 12, Novomatic enables 40) and the "paradox of choice" (Efim/Juan: too many games = players swipe instead of play; 12 is "aplenty"). [[raw/Games_development_review (1).md]]
- **Product background aired.** The original **Diamond Link** had incorrect math ("a baseball bat to the face") and was corrected into **Diamond Link Deluxe** / Diamond Link Georgia. **Fiery Ice Link** is a next-generation hold-and-respin (three diamonds across the top, free spins, perceived-persistence elements) that Lena and Michael concocted — **not** based on Diamond Link. A dual-screen **Taj Mahal** title exists as **comp art only** (not developed), kept for a future dual-screen push. The group also revisited the **enhanced/highlighted nudge** (which tells the player which reel to pick) vs the old "true nudge," and competitors' **pick-the-pig** overlay mechanic. [[raw/Games_development_review (1).md]]

## Open commitments

- [ ] Juan Martinez — write the requirements / REQ for the Georgia vertical liquid-glass multi-game (6 Peach + 5 Jackpot Rush + 6 Fiery Ice, 12 enabled, 3 progressives, remove Georgia Lottery logo) and adjust the Jira plans / properly assign the work — due unspecified — [[raw/Games_development_review (1).md]]
- [ ] Michael Gottlieb — research a neutral "aspirational wealth" theme to replace Peach branding (symbiotic with liquid glass, repurposable outside Georgia); analyse competitor top-performers once Felipe supplies specifics — due unspecified — [[raw/Games_development_review (1).md]]

## Open questions

- Which six vertical titles make the Georgia pack — keep the current Peach vertical six, drop the 2–3 weakest, and add vertical versions of top dual-screen performers (e.g. Lion Riches, Crazy Spins)? Depends on per-game performance data JVL largely lacks. [[raw/Games_development_review (1).md]]
- How to present three independent progressives on one busy vertical selection screen without cluttering it (per-category top progressive in attract mode vs none) — "not a hill to die on." [[raw/Games_development_review (1).md]]

**§15.8:** clear — game/market/product economics only (machine counts, price/tariff, win-per-unit); no named-person compensation.

**Same-name / attribution notes (§4):** [[wiki/people/felipe-miranda.md|Felipe Miranda]] rendered "Felipe Miranda Giorgi" here. "**Irina**," consulted by Lena on the multi-category progressives, is engineering/product context → [[wiki/people/irina-shishko.md|Irina Shishko]] per the owner ruling (2026-07-18) routing QA/engineering to Shishko; flagged for the provisional two-Irina cluster. Michael's garbled "Athima" ≈ **Efim** ([[wiki/people/efim-podvoiski.md|Efim Podvoiski]]). Michael's predecessor "**David**" on the Georgia/Peach initiative is a historical mention only (no page).

## Sources

- [[raw/Games_development_review.md]]
- [[raw/Games_development_review (1).md]]
