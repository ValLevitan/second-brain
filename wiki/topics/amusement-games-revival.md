---
type: topic
title: Amusement-games revival (porting the legacy C++ library to HTML/Pixi)
date: 2025-07-31
aliases: [amusement games revival, reviving amusement games, echo console games, HTML game framework, Pixi games, Rage Studio games]
source-count: 2
open-questions: 3
---

# Amusement-games revival

On **Jul 31 2025** [[wiki/people/val-levitan.md|Val]] opened an exploration into **reviving JVL's aged library of amusement games** — the old non-slot arcade-style games (poker, skateboarding, monster-truck, word/spot-the-difference games, etc.) — by re-building them on JVL's modern **HTML-based framework** for the **Echo platform / a dedicated console**. He ran the question twice the same day with two different groups: a team/scope conversation with [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] + [[wiki/people/lena.md|Lena Zhukova]] ([[wiki/meetings/2025-07-31-amusement-games-revival-efim-lena.md]]), and an engineering/framework conversation with [[wiki/people/pavel.md|Pavel Frolov]] ([[wiki/meetings/2025-07-31-amusement-games-revival-pavel.md]]). These are the amusement/arcade games behind the **ECHO Amusement** product (go-to-market on [[wiki/topics/echo-home-gaming-device.md]]); this page is the development-side thread.

## The problem — the old format is unrecoverable

- The old games are written in **C++** under **Rage Studio** (or an even earlier in-house format), and the developers who wrote them are **no longer with JVL**; Val considers the old **development format impossible to restore**. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- JVL still has the **graphic files**, but their usefulness is limited — the screen format has migrated from **3:4 to 16:9** since the games were made. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- Consequence (agreed with Efim/Lena): JVL can keep the **idea** of a game, but the whole game must be **re-built from assets all the way to framework programming** — "we can take the idea of the game, but the whole game needs to be re-designed… from assets all the way to framework programming" (Val; Efim "Yes," Lena "I think so"). Reusable are the **game concept, name, scenes, and character/concept design** — not the assets themselves; heavy-3D games can reuse the least. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]

## Scope & scale

- **~150 games** in the library (Val: "150," "close to"; Efim hadn't realised it was that many). [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] The set is uneven — many **simple** games (word games, spot-the-difference with different skins, near-clones) and some **very complex** ones (physics- or strategy-based); some are **outdated even by idea** and may not be worth reviving, and some would have to be **reinvented**. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- **Timeline:** roughly **2 years minimum for ~50 games** (both Efim and Lena landed on ~2 years); a pace of about **one game every two weeks** is "optimistic" — a team of ~2 programmers, ~2 weeks per game, and there is **no common frame to build from** (each game is largely bespoke). [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- Approach (Pavel): take the **list of all games of interest**, split into **simple vs complex**; simple ones are easy to implement even without the old game's logic; where an old game used a **tricky mechanic / know-how**, find the old sources and rewrite that logic on the new framework. Reusing old-game **resources** saves designers' time (though scenes still get redone). [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Team composition (counts only — no compensation, §15.8)

- **Programmers:** the Efim/Lena session landed on **two game programmers** (passionate, creative, willing to iterate); the Pavel session judged **one TypeScript programmer** (per-game) could be enough. (Recorded as said — the two sessions differ on the count.) [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Designers:** **one senior graphic designer + two more junior ("average") studio designers**, plus a **sound editor**. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Language shift:** the work needs **no C++** — the programmer profile is "someone like [[wiki/people/igor-metelski.md|Igor Metelski]]" (named as the archetype), writing in **TypeScript**. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Math/standby:** [[wiki/people/efim-podvoiski.md|Efim]] (as mathematician) on standby for the complex games needing physics or a mathematical apparatus to place elements. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Named candidates:** Pavel floated giving the **simplest** games to [[wiki/people/irina-makarych.md|Irina (Ira) Makarych]] ("Макаревич"); [[wiki/people/efim-podvoiski.md|Efim]] and [[wiki/people/lena.md|Lena]] can advise as they know the whole history. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]] In the Efim/Lena session an **"Anton"** was named a "great candidate" (experienced with these games) — **which Anton is unresolved and queued** (see Open questions). A former developer **"Ivan"** was praised (creative, lots of ideas) but is **no longer with JVL**. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- **Outsourcing** was floated (Lena) as a fit because the project is **self-contained** — no integration with JVL's other products. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]

## Framework & platform direction

- **Assemble scenes in [[wiki/topics/miranda-authoring-tool.md|Miranda]]** (Val: "probably will have to do scenes in Miranda"; Pavel: faster in Miranda now); graphic designers work in **Miranda + Pixie + the HTML framework**. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Pixi (PixiJS) as the 2D framework.** Pavel prefers Pixi because it already **works with scenes JVL's designers create** (a large reusable chunk) and there is a large pool of Pixi developers who wrote simple internet games; he did **not** favour switching to a different engine. Caveat: the current framework is written on the assumption that **all JVL games are slot games**, so the amusement games may need a **per-game framework for each game's mechanic** (Pixi is itself only a 2D-game framework), and two different games share very little — which complicates the "one Omni framework" idea. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Physics:** JVL has prior experience (Monster Truck, a bear-on-a-cart physics game, a Rage-Studio candy-store using real physics) and can **port C++ coordinate libraries / algorithms**; the team wants to **avoid real 3D** ("new territory"). The most complex old game was **poker (Texas Hold'em)**, now heavily outdated. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- **Platform / "open it as a platform" idea (Val):** provide a **basic kit** — the framework + a **ported test game** + a **documented API** — so third-party ("white-label") developers can build games on the base. Pavel said he'd need to involve **[[wiki/people/alexander-biratka.md|Sasha]]** to see what he's missing. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Hardware platform:** with the Pixi-framework + data-center combination JVL has a near-ready platform on **x86** (a standard platform; a specific board name in the transcript is garbled — recorded as **unclear**); an **ARM** target would need its own OS/scripts/libraries, but the **game code itself should be universal** across both. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Cost:** Val asked whether today's product could be made **cheaper without reworking the games**; Pavel's answer — the platform **cannot be made cheaper**, JVL is **tied to the platform / motherboard**. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Data center / server role:** for the old games the data center mainly did **lease management and accepting payment for the game**, but was otherwise minimal (the machines had only simple controls — buttons, joystick); Pavel is unsure a local gaming server is even needed. Val (thinking home-user only for now) expects some server will be needed for **modern content filters, content management, and possible integrations with other apps** (e.g. music) or additional hardware. [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Market framing

- The revived games would compete against **Unity-based games, mobile phones (millions of games), and internet games**; Efim was uncertain how **captive** the console audience is. Lena noted the revival is aimed at a **different market** than mobile/internet. [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]

## Open questions

- **Which "Anton" is the game-programmer candidate?** Named a "great candidate" for the amusement games but with no role signal matching the known Antons ([[wiki/people/anton-leshkevich.md|Leshkevich]] = Omni/RGS, [[wiki/people/anton-seregin.md|Seregin]] = payroll/front-end, [[wiki/people/anton-smm.md|SMM contractor]]) — left unresolved, not forced. — [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- **Is one programmer enough, or two?** The Efim/Lena session said two game programmers; the Pavel session said one TypeScript programmer per game could suffice. Unreconciled. — [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]] [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
- **Is a local gaming server / data center needed at all?** Pavel unsure; Val expects one will be needed for filters/CMS/integrations (home-user framing). — [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]

## Sources
- [[raw/amusement_games_development_revival-july-31-2025-efim_lena.md]]
- [[raw/amusement_games_development_revivial-july-31-2025-pavel.md]]
