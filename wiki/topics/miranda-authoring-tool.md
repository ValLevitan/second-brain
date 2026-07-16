---
type: topic
title: Miranda — the Unity game-authoring plugin suite
date: 2025-03-21
aliases: [Miranda, Miranda plugin, Miranda plugin suite, Miranda 8, Miranda 9, Miranda exports, translatable images]
source-count: 10
open-questions: 3
---

# Miranda — the Unity game-authoring plugin suite

Miranda is JVL's in-house **plugin suite inside Unity** that lets designers assemble casino-game content and produce **"exports" ready for the Pixie graphic engine**. Development-side threads: [[wiki/people/andrew-khandov.md|Andrew Khandov]] (its C# developer), [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (design-side integration and, per the Mar 2025 coaching, its de-facto product owner), the Miranda 8/9 feature-branch work ([[wiki/meetings/2025-02-03-feature-branch-discipline-coaching.md]]), and the Miranda→math test tool ([[wiki/topics/slot-game-design-principles.md]]). Production usage lives on [[wiki/topics/game-art-animation-production-pipeline.md]].

## What Miranda is (the developer's own description)

From the 3-part explainer session ([[wiki/meetings/2025-03-21-miranda-explainer-and-product-ownership.md]]):

- **"More than a bridge"** between the Unity design framework and the Pixie engine: "a set of special objects designed specifically for our casino games and the bridge functionality included… just one class for bridging." It is "like environment inside the Unity environment." [[raw/Explain Miranda.md]]
- It **produces "exports" that are ready for the Pixie engine**. (The part-1 transcript renders the word as "experts" — "It produces what we call experts that are ready for Pixie engine" — while part 2 has "export"; read as *exports*.) [[raw/Explain Miranda.md]] [[raw/More on Miranda.md]]
- It has its own menus, supports special external scripts written for this game type, and provides **"combined objects"** — special objects for JVL's games that "Unity doesn't have." [[raw/Explain Miranda.md]]
- It supports separate exports from programs like Photoshop — e.g. **"translatable images"**: text entered in Photoshop, marked as a special object in Unity, then passed to the Pixie engine; translations are loaded into Miranda itself. [[raw/Explain Miranda.md]]

## The manifest module

- Aaron pictured the "manifest" as a cross-cutting capability; the developer corrected him: **"it's just a module that reads the manifest and compares it to the export… inside the Miranda and give the results to the designer"** — i.e. it tells the designer whether an export is usable. [[raw/More on Miranda.md]]
- The Confluence documentation for Miranda's tools largely exists already; **the manifest page is the one piece not yet written**, "because it's still in the development process." [[raw/More on Miranda.md]]
- (The manifest concept — an asset-creation guideline for designers — dates to the Jan 17 FP7 bottleneck work; see [[wiki/decisions/2025-01-17-remain-on-fp7-hardware-ceiling.md]].)

## Docs vs code — how Miranda should be managed

- Aaron's model: picture Miranda as a tree — **the plugin → several tools → many features per tool** — and document it that way; AI tools can then help write good descriptions. [[raw/More on Miranda.md]]
- Two truth-directions, both legitimate: **"the actual code that's in the code repo… is the actual truth. Everything else is some degree of wrongness"** vs the documentation/roadmap-as-truth view (the code "is always to some wrongness because it's not matching up with what your desires are in the documentation"). Mismatches become, respectively: docs to fix, features to document, or work to plan in Jira. [[raw/More on Miranda.md]]

## Product ownership (Aaron's coaching of Dimitri)

- Aaron urged **"Dimitri"** (resolved by context to [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]) to take "an ownership perspective on the entire tool": controlling releases, "negotiating it with JVL," and sequencing features against real capacity — because the **dedicated Miranda developer is his dad** ("the development team, which is your dad, right? You two are working on it"), whose availability (vacations, fatigue) is the real constraint. [[raw/Even more on Miranda.md]] *(Inference, queued for owner confirmation: the dedicated developer = [[wiki/people/andrew-khandov.md|Andrew Khandov]], the owner-confirmed C# Miranda developer — which would make Andrew Dmitriy's father.)*
- The Jira **timeline view is the actual backlog** — "literally actually what we're going to work on next"; Aaron asked for a roadmap/mission and **storytelling** in the Confluence pages instead of the current "flat wall" of feature descriptions ("it sucks reading them… very informative… not very exciting"). [[raw/Even more on Miranda.md]]
- Miranda is described in passing as "an asset management tool called Miranda that plugs into Unity." [[raw/Even more on Miranda.md]]

## Val's investment framing — the "no programmers" promise (Feb 10)

On the Feb 10 repo-structure meeting ([[wiki/meetings/2025-02-10-github-repo-structure-part-1.md]]), when told a programmer is still needed for games with special effects/bonuses, Val pushed back hard: **"When I was told that if we design Miranda, then we don't need programmers. So I've invested a shitload of money into designing this Miranda"** (amount not stated) — threatening rhetorically to "scrap Miranda" rather than live under an illusion; the team's answer was that pure **reskins need no programmer** (copy, change resources, release), while new mechanics/bonuses still do — "That's Miranda. Probably." Val also recounted "Dima Khandov comes to me and says… let's design this feature in Miranda that could implement this piece of code" as the pattern for closing the artist-vs-programmer gap. [[raw/github _structure-pavel-aaron-andrei.md]]

## Open questions

- ~~Is the dedicated Miranda developer ("your dad") Andrew Khandov?~~ **RESOLVED (owner ruling 2026-07-14): yes — Andrew Khandov is Dmitriy Khandov's father** and the dedicated Miranda developer. (Owner correction is its own citation.)
- Who are "Pavel and Arena" whom Dimitri should negotiate Miranda's development with — "Arena" is a garbled name (Irina? Lena?). — [[raw/Even more on Miranda.md]]
- **Adopt Unity (with its casino engines) and drop Miranda entirely?** Raised May 1 2025 as a real reconsideration now that Unity charges no per-game/per-install fee; revisited May 6 (Val's "why do we need Miranda?" probe — see below); **still unresolved** (needs C# adoption + assessment of refactoring Miranda's logic). — [[raw/unity_instead_miranda-may-1-2025.md]] [[raw/the_reason_for_miranda-may-6-2025.md]]

## Apr 28 2025 — GitHub versioning and Dmitriy's commit hygiene

On a short working session ([[wiki/meetings/2025-04-28-miranda-github-versioning.md]]) Val set how Miranda is versioned in Git: the repo should be named just **"Miranda"** (not "Miranda 8" — "maybe a couple of repositories… depending on how modular it is"), and **versions are Git release tags** on a commit ("this commit represents… version 8"), **never versions in Jira** ("that means the tail is wagging the dog. The version should come from the Git repo, which will be the truth"). Reviewing [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]'s work, Val found a single **"V8" commit of ~12,000 files** ("we asked him to, with all fairness"), stale branches open for two months, and commits going straight to `main` — "no organizational skills related to keeping a clean, planned… release." A meeting was set for the next day (8 am Eastern) to coach **continuous commits**. [[raw/miranda_github-apr-28-2025.md]]

- Related (Apr 30): Val wants Dmitriy Khandov's **Unity license placed into the CI actions** (via the secrets-management platform) so **Miranda can be built in GitHub CI** and other people's build actions can use it — see [[wiki/topics/infosec-and-server-infrastructure.md]]. [[raw/secrets_server-apr-30-2025.md]]

## May 1 2025 — the "organizing Miranda" action list

Continuing the Apr-28 thread, [[wiki/people/aaron.md|Aaron]] met [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] (~Apr 29) and, on the [[wiki/meetings/2025-05-01-organizing-miranda-github.md|May-1 recap with Val]], laid out the action list for Dima to clean up the Miranda repo before wrapping the math emulator back in: [[raw/organizing_miranda_github-may-1-2025.md]]

- **One repo, versions are just versions.** There is **only one repo for Miranda**; "Miranda 8" and "Miranda 9" are versions of it (consistent with the Apr-28 release-tag ruling). Miranda 8 is completed; **Miranda 9** is in process, with three features near end-stage. [[raw/organizing_miranda_github-may-1-2025.md]]
- **The clean-up steps (before integrating the emulator):** create a **`.gitignore`**; **purge unnecessary files** (logs, libraries) from the repo; **delete the old/stale branches**; establish a **basic packaging strategy** (e.g. zip the libraries during the commit of a new Miranda version). Only then start a **new feature branch** to weave the simulator/math-emulator integration back into Miranda. [[raw/organizing_miranda_github-may-1-2025.md]]
- **Move the math game-emulator out of Miranda 9** into either a **separate repository or a separate product — not yet decided.** (This is the same emulator discussed on the [[wiki/meetings/2025-05-01-game-design-review.md|game-design review]] — see [[wiki/topics/slot-game-design-principles.md]].) [[raw/organizing_miranda_github-may-1-2025.md]]
- Aaron was **unsure Dima fully understood** ("nodded his head… whether he truly understood or not"). Next Miranda meeting set for the following Tuesday (~May 6). Aaron also noted Teams now auto-generates meeting summaries + full transcripts. [[raw/organizing_miranda_github-may-1-2025.md]]

## May 1 2025 — "Unity instead of Miranda?" (decision-in-motion)

On a separate May-1 call ([[wiki/meetings/2025-05-01-unity-instead-of-miranda.md]]) Val and Aaron asked [[wiki/people/alexander-biratka.md|Sasha (Alexander Biratka)]] whether JVL could adopt a **licensed Unity development ecosystem — including Unity's casino engines — and drop Miranda entirely**. This is a genuine strategic reconsideration of the authoring tool; **no decision was taken** (flagged as a decision-in-motion). [[raw/unity_instead_miranda-may-1-2025.md]]

- **Unity is now effectively free (the trigger).** Val's premise: Unity has **charged no per-installed-game / per-machine license fee since 2024** — it walked back the per-install revenue-share plan after industry backlash and now charges **per revenue tier of the company**. Val: "the moment they stop charging per game, that's a game changer" — and "then we don't need Miranda, am I correct? Yeah." [[raw/unity_instead_miranda-may-1-2025.md]]
- **Sasha's technical read.** Unity for **land-based** should give good performance; a **native** app is fine; a **browser** build (like Pixi) historically had bad performance, though Unity has "made huge improvements." Unity's engine language is **C#** — a language JVL doesn't currently use (Sasha's ~10 Unity people are **designers using Unity only to create the theme/view, no logic**), so adopting it means new infrastructure/tech ("like Java, but other technology"). Whether Miranda's existing project logic could be refactored to run in Unity Engine is **unknown** — depends how much game logic is externalised to the remote gaming server / remote math. Aaron noted C# can be compiled on Linux (no OS-license cost). [[raw/unity_instead_miranda-may-1-2025.md]]

## May 6 2025 — "The reason for Miranda" (the Unity question, continued)

On a short probe ([[wiki/meetings/2025-05-06-the-reason-for-miranda.md]]) [[wiki/people/val-levitan.md|Val]] pressed [[wiki/people/dmitriy-khandov.md|Dima (Dmitriy Khandov)]] — "why do we need Miranda?" — if JVL embeds the now-fee-free Unity engine for land-based, and asked him to "sell me on Miranda." **Still no ruling** (the decision-in-motion continues). [[raw/the_reason_for_miranda-may-6-2025.md]]

- **Val's licensing math (a hypothetical, not Unity's actual pricing):** if Unity charges only for the software per seat, "let's go crazy and say it's $2,000 per seat… 20 seats… my maximum exposure for licensing is $40,000 a year" — trivial next to Miranda, "so why do I need Miranda?" (Val flags both figures as deliberate over-estimates — "obviously not true on both ends.") [[raw/the_reason_for_miranda-may-6-2025.md]]
- **Dima's answer:** **Pixie is "a really light engine"**; **Miranda is a plugin to set data for the Pixie engine**, and even without Pixie it "is still capable of playing games… it can spin the reels." [[raw/the_reason_for_miranda-may-6-2025.md]]
- **Aaron's "sell":** Miranda, "without Pixie anymore, fully nestled in the Unity ecosystem, is a tool that **mocks up the slots games** JVL produces… manages all of the structures, objects, resources, and gameplay logic necessary to connect it to JVL software backend infrastructure to produce games… distributed at both online and in-app purchases," then compiled into the Unity engine to run in the JVL software stack. [[raw/the_reason_for_miranda-may-6-2025.md]]
- **Visual quality is not the engine.** Dima: "It's not about the visual quality. Visual quality comes from the game designers… same video files, same font files, same Photoshop, PNG files." Aaron cited a Unity 2D game faithfully reproducing 1930s cell animation as proof the 2D engine can carry any look. [[raw/the_reason_for_miranda-may-6-2025.md]]

## May 6 2025 — organizing Miranda in GitHub (the follow-through)

The "next Tuesday" Miranda session ([[wiki/meetings/2025-05-06-miranda-github-organization.md]]) foreshadowed by the [[wiki/meetings/2025-05-01-organizing-miranda-github.md|May-1 recap]]. [[wiki/people/dmitriy-khandov.md|Dima]] had done the cleanup [[wiki/people/aaron.md|Aaron]] asked for; Aaron reviewed it and coached the next steps. Transcript loops/duplicates — facts taken once. [[raw/miranda_organization_github-may-6-2025.md]]

- **What Dima did:** reduced "lots of data," reworked the repo so it **rebuilds itself after a Git checkout**, kept working in the **existing repo** (a new branch, not a new repo), added a **`.gitignore`** and a `cleanMirandaTool.config`, cut a **V8.1 release**, and built a drag-and-drop **Unity package** (the file Unity consumes). Unity does the compilation; you can point Unity at the zip or at the Git repo. [[raw/miranda_organization_github-may-6-2025.md]]
- **Packaging/distribution:** Aaron urged talking to **Andre ([[wiki/people/andrey-bosik.md|Andrey Bosik]]) and Dima K ([[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]])** about **NuGet** (a Microsoft-platform package, auto-installable via a rule) / an **MSI-style installer**, so a non-technical user has the fewest steps; **never commit the ~2GB engine** — use references/an installer script. Distribute the **Unity package in releases**, not the source-code tarball. [[raw/miranda_organization_github-may-6-2025.md]]
- **README "TLDR" structure:** a concise, concrete description of what Miranda actually does (not "streamline/automate/enhance" filler — it "prepares game assets for deployment in the **Pixie Engine**"), then **three-step** install for those who know Unity, then extended step-by-step for novices (one level below), then technical docs + **contribution guidelines**. Model the capability docs on **Unity's own documentation tree** ("when in Rome"). Use AI to comment the code and to write capability docs from two directions until they meet. [[raw/miranda_organization_github-may-6-2025.md]]
- **Git hygiene:** the cleanup PR removed **~782,000 lines across ~5,000 files** — Aaron warned that history now carries that bulk forever, so Dima should **rebase / fresh-start with Andre's help**; write **more verbose pull requests**; **delete the merged branch**; and have someone (e.g. **Sasha**) **review** PRs. Aaron's frame: good docs are a **"value multiplier"** on money already spent building Miranda. [[raw/miranda_organization_github-may-6-2025.md]]
- Val's recurring insistence: "**I need to know capabilities**… I don't understand the technicalities" — so the features (which came from Jira) should be re-documented as Miranda's **capabilities** (animation, asset management, build management, core mechanic, localization). [[raw/miranda_organization_github-may-6-2025.md]]

## Open contradictions

- **What language is the Unity engine?** [[wiki/people/alexander-biratka.md|Sasha]] (May 1) said "Unity's engine language is **C#**"; [[wiki/people/dmitriy-khandov.md|Dima]] (May 6) said "Unity is a different engine. **It's a C++ engine.** It's quite heavy on production." Both dated close together, about the same fact — recorded, not resolved. [[raw/unity_instead_miranda-may-1-2025.md]] [[raw/the_reason_for_miranda-may-6-2025.md]]

## Sources

- [[raw/Explain Miranda.md]]
- [[raw/More on Miranda.md]]
- [[raw/Even more on Miranda.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
- [[raw/miranda_github-apr-28-2025.md]]
- [[raw/secrets_server-apr-30-2025.md]]
- [[raw/organizing_miranda_github-may-1-2025.md]]
- [[raw/unity_instead_miranda-may-1-2025.md]]
- [[raw/the_reason_for_miranda-may-6-2025.md]]
- [[raw/miranda_organization_github-may-6-2025.md]]
