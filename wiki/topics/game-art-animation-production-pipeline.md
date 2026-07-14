---
type: topic
title: Game art & animation production pipeline (comp art → Miranda)
date: 2025-03-12
aliases: [animation production, comp art pipeline, CompArt, storyboards, Spine, Blender, After Effects, placeholder build, Miranda scene assembly, art production stages]
source-count: 1
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

## Sources

- [[raw/Game Development How animation are made with Lena - March 12-2025.md]]
