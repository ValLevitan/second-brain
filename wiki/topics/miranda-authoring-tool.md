---
type: topic
title: Miranda — the Unity game-authoring plugin suite
date: 2025-03-21
aliases: [Miranda, Miranda plugin, Miranda plugin suite, Miranda 8, Miranda 9, Miranda exports, translatable images]
source-count: 4
open-questions: 2
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

- Is the dedicated Miranda developer ("your dad") Andrew Khandov, making Andrew and Dmitriy Khandov father and son? (Inference from role match; not stated as a name in the source.) — [[raw/Even more on Miranda.md]]
- Who are "Pavel and Arena" whom Dimitri should negotiate Miranda's development with — "Arena" is a garbled name (Irina? Lena?). — [[raw/Even more on Miranda.md]]

## Sources

- [[raw/Explain Miranda.md]]
- [[raw/More on Miranda.md]]
- [[raw/Even more on Miranda.md]]
- [[raw/github _structure-pavel-aaron-andrei.md]]
