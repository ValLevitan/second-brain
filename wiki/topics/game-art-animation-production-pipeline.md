---
type: topic
title: Game art & animation production pipeline (comp art → Miranda)
date: 2025-03-12
aliases: [animation production, comp art pipeline, CompArt, storyboards, Spine, Blender, After Effects, placeholder build, Miranda scene assembly, art production stages, spike, sorting, symbol containers]
source-count: 8
---

# Game art & animation production pipeline (comp art → Miranda)

How JVL turns a game concept into finished visual art and animation. Synthesised from [[wiki/people/lena.md|Lena]]'s Mar 12 2025 step-by-step walkthrough for [[wiki/people/val-levitan.md|Val]]. This is the *art production* side; the design/mechanics side is on [[wiki/topics/slot-game-design-principles.md]] and the throughput goals Val wants to impose on this pipeline are on [[wiki/topics/game-production-throughput-strategy.md]]. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## The stages, in order

1. **Concept → brief.** After the market requirements are understood and the game mechanics and math are ready, [[wiki/people/michael-gottlieb.md|Michael]] (in discussion with [[wiki/people/juan-martinez.md|Juan]]) settles a game concept, then **sends Lena an email describing his vision** and asks her to develop **comp art**. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
2. **Fundamentals comp art.** Lena, as art director, first produces the **fundamentals** — how the main screen, bonus, logo and symbols will look — before any animation work. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
3. **Animation design.** Only once the fundamentals are set does she produce more elaborated comp art for the **animations of each symbol and the transitions**. A **complex** animation gets a **storyboard** (comp art showing the milestones of the animation); a **simple** one (e.g. a rooster lifting its head and opening its beak, or a symbol just rotating/enlarging) gets a **verbal description** instead. Storyboards are posted "in conference" and kept with the game-design doc / story description; Lena said she focuses on the creation, not where it is stored. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

Lena stressed that **animation is a production-stage activity, not a design-stage one** — it can only be worked on **after the final comp art is developed** — which is why she personally cannot focus on animation until the comp art is done. She defines what needs to be animated and how (approving it with Michael, and sometimes sending it to Juan, e.g. for signage). A Photoshop storyboard takes **a couple of hours to about a day**, depending on how complex the scenario is. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## How many animations

The number of animations is roughly **predetermined by the game's mechanics/structure**. Each game has a **basic set**: animations for all symbols, the game background, the free-spins background (if the game has free spins), a logo animation, and a bonus-background animation — plus extras if a feature (e.g. a recognition or transition) is decided to involve the main character. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Who does the work

- **Animations** are done by the game artists — named as **Julia** ([[wiki/people/yulia.md|Yulia]]), **Anastasia**, **Sergey**, **Natasha**, or **Dima** ([[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]) — though Dima lately does little game graphics, being focused mostly on **Miranda**. (Sergey and Natasha are named artists with no page yet.) [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- There is **no automation** that produces the animation automatically yet ("not yet, maybe in a pretty close future"). A rooster opening/closing its beak and twisting its head still has to be animated by hand. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- **Placeholder cutting** can be given to any game artist, usually a junior (Natasha, Vitaly, "anybody"). [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Tools — 3D vs illustration

For each symbol the team discusses the most optimal/fastest route: [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

- **3D model** when it is faster or when the symbol needs a different camera view in different parts of the game (e.g. the cats for **Fortune Football**). The 3D model is **post-produced in Adobe After Effects**; the animation is done in **Blender** — JVL is **moving off 3D Max** in the new framework because **Blender is free and not tied to 3D Max versions**. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- **Illustration + Spine** when a character/object is used only once — draw it, cut it into special pieces, animate in **Spine**. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- JVL **almost never uses the raw output** of a 3D program directly — there is always a **post-production pass in Adobe After Effects**. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Assembly in Miranda

- The **final output** (a frame sequence from Spine or After Effects) is applied to an object in a **Miranda scene** that represents a symbol on the reels; on export, that object plays the animation. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- **Placeholder build (fast play-testing):** an entire game can be built for Michael with **just comp-art placeholders and no animations** — textures cut from the Photoshop file — so the reels spin with static/proxy art. This takes about **one day per game**. Michael and Efim asked for this specifically, which is why **Dima worked on integrating the math into Miranda**, so the game can run as soon as possible for them to test gameplay. It isn't produced automatically because each game has different symbol sizes, reel matrices and reel positions, so it would need a special script. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- **History → Miranda:** animations were previously applied in **Rage Studio** (or earlier in "Realtor"); now they are assembled in **Miranda**. **Fortune 4** / Fortune Foo Paws (transcribed "Fortune Food Pause") is the **first game** having its main scene assembled in Miranda (they had done it before for the online games, but Miranda's process is now improved). Running the game live in the browser depends on **Dima and Andrey** finishing the integration of the math/mass server into the game so it runs proper gameplay inside **Miranda 9** without programming. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Iteration example

For the **Queen game** recognition feature, Lena showed Michael one scenario, he asked to try something else, she did, he liked it, then had second thoughts (it looked like "a whip") and asked her to go back to the earlier **silver-horseshoe** version — an iterative creative loop that is why she prefers to storyboard quickly in Photoshop before involving real game animators. [[raw/Game Development How animation are made with Lena - March 12-2025.md]]

## Porting a game's assets to Omni — the Calle Ocho method (Apr 17 2025)

Moving the released **Calle Ocho / Kai-Ocho** game's assets onto Omni forced a choice between three approaches, worked through by [[wiki/people/lena.md|Lena]], [[wiki/people/dmitriy-khandov.md|Dima]], [[wiki/people/alexander-biratka.md|Sasha]] and Val ([[wiki/meetings/2025-04-17-calle-ocho-asset-redesign-omni.md]]): [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]

- **Plan A (Lena's, to hit a May-1 date):** take the videos made for Calle Ocho in **Rage Studio** and just re-export them through **Spine** and **Miranda**, only separating the particles that need **additive** blending (Omni can't do alpha + additive in one video today). Lena's own objection: this reuses nothing for the *next* game. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **Plan B (Sasha's):** rebuild assets "properly" so the control code is reusable in future games — but then no firm time estimate, and Sasha argued ~2 months (Val: 2 months is "a non-starter"). [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **The middle approach (Dima's, adopted):** port as-is the many things that can be (e.g. symbols exported into **Spine containers** with minimal designer effort, without redrawing the internal animation), and **properly rework only what recurs across future games** — the "pigwin"/penguin effect "we'll use in thousands of games," a **flexible BigWin** (swap diamonds↔Chinese coins by scheme, reused straight into Fortune Fu Paws / "HotShenFuPo"), and a shared **Dashboard**. Val's framing: throwing away some Calle-Ocho-only work is a small sacrifice if it launches the engine. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **"Spikes" (unsolved reworks) identified:** a **soft mask** for the negative transition (Omni's mask is a hard geometry mask; the fix is a two-layer video where the second layer is the soft mask); **video-in-button** complex buttons for the **Pick Your Fortune** mini-game (buttons that change skin per state and embed video — never built before); and **sorting** (per-symbol individual sort order, "very important… needed in all games," ~90% on Sasha). [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **Concrete asset rulings for Calle Ocho:** the new **Dashboard** pushes the reels up (Lena to shrink the rooster + logo slightly, remove the "Lions," reposition — **not resize** — the reel matrix); **Royals** redone once in **Spine** as recolourable **skins** (one font, per-game colour sets); **anticipation** and **precognition** kept as video (rework only if performance drops); the **V-Deck** gets the new last-three-buttons flame feature (as on Fortune Fu Paws / Diamond Link Georgia). [[wiki/people/sergey-tsymanov.md|Sergey]] to rebuild the FireEyes progressive Sign for Omni; **Vitalik** cuts resources; **Dima** owns templates + the hardest fixes while others parallelize. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]

## La Rosa enters production (Apr 3 2025)

On the Apr 3 review ([[wiki/meetings/2025-04-03-game-design-vdeck-review.md]]), [[wiki/people/lena.md|Lena]] reported she had **created the production for La Rosa** and the **illustrator will start** on it (the game "contains a lot of illustrations"); art assets get prepared while game artists finish Diamond Link Nudge/Buttons and Peach Tropical, then Peach 4 games are assembled. She had also **begun design work on the Spepper game** (Spepper IP) and flagged **El Jaguar** next — confirming the concept→production hand-off described above for the Peach 4 reskins (game list on [[wiki/topics/jvl-machine-lineup.md]]). [[raw/game_design-april-3-2025.md]]

## Production-time estimation on the Miro board (Apr 18 2025)

Val and Lena walked the **game-production task list in Miro** item by item to estimate **production time per item**, setting creative reiterations aside (Lena's rule of thumb: ~2.5 reiterations on average, not every task) ([[wiki/meetings/2025-04-18-games-production-time-estimation.md]]). [[raw/games_production-apr-18-2025.md]]

- **Unit convention:** a "day" = **8 hours**; e.g. "5 days" = **40 hours** of actual labor time (not thinking time). [[raw/games_production-apr-18-2025.md]]
- **Structure separated for estimating:** the game part vs the **Fiery Ice Link** progressive part. Progressive transitions/bonus are **common to all Fiery-Ice games** and copy-paste between games (the Diamond Link / Jackpot Rush lineage — "developers have the technology to put code inside another game"), so they're pulled out of per-game work; **game math differs per game** and Lena only cares about which symbols are special (visual hierarchy), not the math detail. **Kaio-Ocho** has fewer tasks than **Dragons of Rain** because its bonus/progressive-sign were already done in Dragons. [[raw/games_production-apr-18-2025.md]]
- **The production stages (Lena's map):** CompArt for main scene + free spins → per-symbol **"detailing"** (each symbol's parameters: oversized?, animation length, animation description, anticipation animation) → per-symbol production. **Precog** = an artistic-approach illustration Lena shows Michael for approval; **Anton** draws the objects (illustration, since Anton doesn't do 3D), then **Nastya/Natasha** animate (AI used to combine/cut illustration pieces, then hand-animated). [[raw/games_production-apr-18-2025.md]]
- **Critical resources:** Lena priced only the **critical, non-substitutable** resources (**Dima, Nastya, Yulia**) who run **fully in parallel** — Dima's V-Deck project is completely self-contained (depends on no one). **Anton** shares his time across games (Jet Patrasche / George), so she hadn't priced his tasks and would fill them in the next day with him. Val pushed to estimate **time-per-person first**, then lay out a parallel schedule to expose the resource bottleneck (the "second Dima" thought experiment). [[raw/games_production-apr-18-2025.md]]

## Art status (May 1 2025)

From the [[wiki/meetings/2025-05-01-game-design-review.md|May-1 review]]: [[raw/game_design_review-may-1-2025.md]]

- **Nebraska "Corn Husker" bonus** progressing ([[wiki/people/lena.md|Lena]]): she is toning down the bright corn stalks around the logo and building out the extra screens (second screens for bonus, topper for bonus) noted in the design stories. [[raw/game_design_review-may-1-2025.md]]
- **Regulator video instead of a machine.** For Nebraska, the regulator will accept a **video** rather than a physically shipped machine. **Vitaly** records it Monday (back from holiday); the team will show **one three-reel and one five-reel** game (the classic nudge effect is consistent across games, so one of each covers it) — e.g. Aztec Star + Lion's Riches. **Vlad** does the sound processing on top; Lena's team confirms the preferred audio format. [[raw/game_design_review-may-1-2025.md]]
- **Cuban-rooster reskin idea.** Val floated turning **Jinji Du Li** (a Chinese-rooster clone of Fortune Foo Paws; the other clone is **Cash Kittens**) into a **three-Cuban-roosters** game to build on the traction of the Cuban theme (**Calle Ocho / "Callejo"**) — same mechanics as Fortune Foo Paws. The team was "overwhelmingly in favour"; not a committed decision. [[raw/game_design_review-may-1-2025.md]]
- **2D decks** for **Diamond Link** and **JetPort Rush** (Georgia) to finish "next week," with the discussed changes. [[raw/game_design_review-may-1-2025.md]]

## May 7 2025 — ComfyUI experimentation for asset generation

On the games-design tool-adaptation session ([[wiki/meetings/2025-05-07-games-design-ai-tools-adaptation.md]]) [[wiki/people/lena.md|Lena]] reported building **ComfyUI** (transcribed "Conf UI/Confi UI") workflows to generate a very specific **golden coin** asset — the point being to reproduce exact game-required assets, not just "something beautiful." Findings: fix the seed and parameters, then change only small prompt elements to keep the rest of an image stable; save/load workflows; some models need specific custom nodes and workflows. [[wiki/people/yulia.md|Yulia]] built a dataset of **21 golden-coin images** to train JVL's own **LoRA** style for the workflow. Aaron pointed them to the **ComfyUI Manager** (loads required backend nodes for a shared workflow), an **alpha-transparency node pack**, and a **3D-pack** that generates a full textured 3D mesh; and to **Unity plugins** that import ComfyUI output directly into Unity (2D, transparent, animated, or 3D). Consensus: ComfyUI is powerful but needs deep research and a chosen use case; it is not picked up "in a day or even a week." [[raw/tools_adaptation_games_design_department-may-7-2025.md]]

## May 8 2025 — Golden Cask/Husk production, and the math-emulator stall

From the [[wiki/meetings/2025-05-08-game-design-review.md|May-8 review]] ([[wiki/people/lena.md|Lena]] reporting): [[raw/game_design-may-8-2025.md]]

- **Nebraska "Golden Cask"/Golden Husk bonus** progressing: Lena is finishing the game list for "Cask number one," the **bonus assets** are the main effort (games only need "removing hands"), and the **corn transition** animation (main game → bonus) was reviewed — the corn **fans out and scales toward the player** with sparkles for a "golden field feeling," ending in a large corn field. She adjusted the **Money Birds / Cash Cats** game logos so they don't run over. Production iterations start once Juan approves the list; **Crazy Spins** is the first game to cook, then Midnight Money. A first **video recording** of Crazy Spins was reviewed (good; needs a few still-image screens extended so narration has time). [[raw/game_design-may-8-2025.md]]
- **Math-emulator stalled a week.** The Miranda→math emulator (the Fortune-Foo-Paws first playable from the May-1 review) had **no update for a week** — Val was told graphic work is paused because **[[wiki/people/dmitriy-khandov.md|Dima]] is working with "Peryatka" on "Couch" only** (both transcribed, unclear referents — flagged) on more urgent work; Dima returns to the emulator after a major push lands the game in-browser. [[raw/game_design-may-8-2025.md]]
- **Graphic team + Miranda:** Lena confirmed the graphic team **"love" Miranda** ("a good environment… unique… with additional features") from the online-games work, and that their feedback shaped how Miranda progressed this year. **"Kyva 2"** (transcribed; unclear title) is under construction and expected in-browser next week once **Sasha Ryadko** (a developer) resolves it. [[raw/game_design-may-8-2025.md]]

## May 29 2025 — South Dakota six-pack in production; shared art resources

On the [[wiki/meetings/2025-05-29-games-design-recap.md|May-29 games recap]] [[wiki/people/lena.md|Lena]] moved the **South Dakota VLT** six-pack into production (Bioliches in development, Gypsy Spirit concept/GDD done, production stories starting; **Natalia** and **Vitaly** on feature systems), pausing the Nebraska Golden-Husk/Golden-Fast assets (illustrations + 3D models already prepared). The recurring constraint: art resources (**Dima, Andy, Igor Metelski, Anton**) are **shared with Omni/Calle Ocho**, capping throughput; Vitaly records regulator videos. Production detail on [[wiki/projects/south-dakota-vlt-market.md]]. [[raw/games_design_recap-may-29-2025.md]]

## Sources

- [[raw/games_design_recap-may-29-2025.md]]
- [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
- [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- [[raw/games_production-apr-18-2025.md]]
- [[raw/game_design-april-3-2025.md]]
- [[raw/game_design_review-may-1-2025.md]]
- [[raw/tools_adaptation_games_design_department-may-7-2025.md]]
- [[raw/game_design-may-8-2025.md]]
