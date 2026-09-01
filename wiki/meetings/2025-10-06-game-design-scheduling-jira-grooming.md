---
type: meeting
title: Game-design scheduling / Jira grooming — South Dakota keno pack + migrate game design off Jira to Git (Oct 6 2025)
date: 2025-10-06
aliases: [game design scheduling Oct 6, Black Hills Keno Deluxe, Solar Keno, Liberty Keno, keno package GC260, Swift Cache Progressive, Fiery Ice nudge, comp art rename, game design to git]
source-count: 1
open-commitments: 3
open-questions: 1
---

# Game-design scheduling / Jira grooming (Oct 6 2025)

**Date:** 2025-10-06 (3:44 PM) · **Attendees:** [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], [[wiki/people/juan-martinez.md|Juan Martinez]] (dropped off mid-meeting to board a flight), [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/pavel.md|Pavel Frolov]] (host/tooling). English.

A working Jira-grooming session laying out schedules, deliverables and dependencies for the **South Dakota VLT keno pack** and grooming the game-design workflow — the game-development counterpart to the core-development restructuring. Substance on [[wiki/topics/slot-game-design-principles.md]] (Oct-6 section), [[wiki/projects/south-dakota-vlt-market.md]] and [[wiki/projects/georgia-market-rollout.md]]; the migrate-to-Git direction ties to [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]]. §15.8: nothing sensitive.

- **Migrate game-design thoughts off Jira/Confluence → Git.** Val's directive: now that **core development is organized**, do the same for **game development** — Michael's valuable design thinking must **migrate out of Jira and Confluence (both "the wrong location")** into **Git** as a revision-control repository. Interim step: break each game's description into **deliverables in Jira**, **collapsing story levels** (features only, no stories). Michael objected on efficiency grounds; Val held the decision. [[raw/game design scheduling-october-6-2025.md]]
- **Deliverable vocabulary settled.** For each game concept: **abstract** (holds game mechanics too), **main screen comp art** (the "comp art" header renamed to "main screen comp art" to stop confusion with design-stage compartments — it is one still image of the conceivable main screen), and a **pay table reference/draft** (Juan-supplied, explicitly *inspirational* not final — a competitor's pay table can't be copied 1:1 for legal reasons). Game mechanics stay **part of the abstract**, not a separate deliverable. [[raw/game design scheduling-october-6-2025.md]]
- **Black Hills Keno Deluxe (GC281 / IP882) scheduled.** JVL's answer to **Caveman Keno (Plus)**; the first keno game. Abstract started **Sept-22**, ~70% done (enough for the artist). Comp art starts **Monday (~Oct-13)**, **3 weeks → ~Oct-27**, worked by the new artist **[[wiki/people/anastasia.md|Anastasia]]**. The keno games get a **brand-new keno UI** that becomes JVL's standard (a JVL-branding matter) — and it is **NOT** the liquid-glass style (a separate keno UI). Fixed date removed so it rolls up. [[raw/game design scheduling-october-6-2025.md]]
- **Solar Keno (GC280) and Liberty Keno (GC279) waterfall behind Black Hills.** Solar = JVL's answer to **Da Vinci Diamonds** (more complex, ~3 weeks comp art); Liberty is furthest out (awaiting customer data on whether the word "Liberty" hits resistance — may just be renamed). Michael keeps developing their abstracts (GC263 Solar / GC269 Liberty) concurrently, but the **team** won't start them until Black Hills is figured out. Val's rule: **"you cannot work on it if it's not planned"** — so Michael's abstract work on Solar/Liberty was itself put on the schedule (abstract → Michael, comp art → Lena, pay table → Juan). [[raw/game design scheduling-october-6-2025.md]]
- **The "package" (GC260) is dead — three discrete games, not a package.** The **"package of keno games for South Dakota VLT" (GC260)** was declared **stillborn** ("there is no package; there are three discrete games") and its scaffolding deleted: the **games-themes level (QC275)** and duplicate Solar/Liberty theme items removed, GC260 itself deleted after checking nothing of Juan's requirements was lost. Val created/used an **archive** initiative (IP952) and pushed to change the whole game-design **workflow** ("this is not the ideal workflow"). [[raw/game design scheduling-october-6-2025.md]]
- **New multi-game home screen (GC265) — liquid-glass, in design.** Initial comp art done; Lena is preparing an **animated presentation** at design stage; the parent concept item is kept because direction may still shift. Market-specific multi-game home screens differ enough that they diverge at design (per-market stories), so the concept-level generic item (GC268 comp art) was dropped. [[raw/game design scheduling-october-6-2025.md]]
- **South Dakota VLT Swift Cache Progressive (GC264) — the "concept post-requirement" argument.** The plan is to **re-release the SD one-pack incorporating Swift Cache** (a modification of a finished product → goes essentially straight to **production**). This triggered a long process debate: Val argued **requirements live OUTSIDE Jira** and the **concept stage exists post-requirement**, so an item with nothing to conceptualize (no schedule, no capacity draw) shouldn't sit in the concept stage. Michael held that the requirement "needs to live somewhere" and JVL habitually parks REQs in concept. Left unresolved ("I disagree… but I don't have the energy to argue — leave it there"); interim compromise: an **abstract (Juan)** + **comp art of the V-deck/meter (Lena)** as deliverables, waiting on Juan's requirement after the trade show. [[raw/game design scheduling-october-6-2025.md]]
- **Fiery Ice Link (GC266, Georgia) — nudge.** Needs two features: a **nudge comp art** (done but not yet formally approved, pending liquid-glass approval) and **game mechanics / math guidelines** ([[wiki/people/efim-podvoiski.md|Efim]] to draft with Juan + Michael). See the Fiery-Ice progressive/nudge history on [[wiki/topics/slot-game-design-principles.md]]. [[raw/game design scheduling-october-6-2025.md]]
- **Housekeeping.** **Jackpot Rush** theme confirmed done/in production and removed from the board. **Florida-market** games (**Calle Ocho 2**, **Cash Kittens** GC554) are **not being worked on → archived** — Val: "don't do any work if it's not planned." Efim flagged **vacation Oct 18 → Nov 2**. Val booked a follow-up **grooming meeting Wednesday 11:30** to groom the game-design stage the same way. [[raw/game design scheduling-october-6-2025.md]]

## Open commitments

- [ ] Juan Martinez — deliver the **Swift Cache (GC264) requirement/abstract** after the trade show; supply pay-table references for the keno games — [[raw/game design scheduling-october-6-2025.md]]
- [ ] Efim Podvoiski — draft the **Fiery Ice math/mass guidelines** with Juan and Michael (starting the week after next; ~1 week) — [[raw/game design scheduling-october-6-2025.md]]
- [ ] Val Levitan + Pavel Frolov — **grooming of the game-design stage** follow-up meeting (Wed 11:30) — [[raw/game design scheduling-october-6-2025.md]]

## Open questions

- Should the "concept stage" hold items that are pure modifications of finished products (no conceptualization, no schedule) — or should requirements/REQs live entirely outside Jira? Val and Michael disagreed; left unresolved. [[raw/game design scheduling-october-6-2025.md]]

## Sources

- [[raw/game design scheduling-october-6-2025.md]]
