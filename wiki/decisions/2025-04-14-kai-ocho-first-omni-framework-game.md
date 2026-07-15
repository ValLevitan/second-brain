---
type: decision
title: Port Kai-Ocho as the first game on the Omni framework, target June 1 for GLI
date: 2025-04-14
aliases: [Kai-Ocho on Omni, Kayo Ocho Omni, Kali-Ochi Omni, first Omni game decision]
status: active
source-count: 5
---

# Port Kai-Ocho as the first game on the Omni framework — target June 1 for GLI

## The decision

- Instead of building the new Omni framework against a brand-new game, JVL will **port the just-released game Kai-Ocho** (transcript renderings: "Kayo Ocho", "Kali-Ochi") **onto the Omni framework first** — "мы решили делать Kayo Ocho первая на Omni Framework … эту игру мы уже сделали, мы сейчас ее переводим на Omni Framework." Val wants it **fully assembled for GLI by June 1 2025** ("Я бы хотел бы ее видеть 1 июня"). [[raw/daily_omni_progress-apr-15-2025.md]]
- **Rationale (Val, recounting the Apr-14 morning meeting):** a framework and a game both evolving at once is "очень много variables" — like shooting an apple tossed in the air; "Лучше яблоко поставить" — pin the game still by using one already released, so only the framework moves. [[raw/cms_svn_github-april-14-2025.md]]
- **Port order agreed (the designer "Dima"):** base game / main scene + resources first, then dashboard, then the "видег" (as transcribed; base-game screens only), then tilts and big wins — "этого набора будет достаточно, чтобы показать … минимальный" game result. Math dependency: Kai-Ocho's math is in the old land-based format and must become a **container** usable for both land-based and online — to be discussed with [[wiki/people/efim-podvoiski.md|Efim]]. [[raw/daily_omni_progress-apr-15-2025.md]]
- **GLI completeness constraint:** setup screens can't be stubbed with the old screens ("Абсолютно нет") — GLI needs the full set (history, reports, settings); [[wiki/people/ihar-hrybko.md|Ihar Hrybko]] owns those setups and joins the next meeting. Integration tests to be built by Anton ([[wiki/people/anton-leshkevich.md|Anton Leshkevich]], context) working with [[wiki/people/alexander-biratka.md|Sasha Biratka]]. Features to be planned at ≤2 weeks each, with a time schedule tracked from the next-morning meeting. [[raw/daily_omni_progress-apr-15-2025.md]]

## The origin meeting — Apr 14 morning ([[wiki/meetings/2025-04-14-omni-framework-mvp-kai-ocho.md]])

The decision was taken in the Monday-morning Omni progress review (internally-duplicated transcript, §12), where Val overrode [[wiki/people/alexander-biratka.md|Sasha]]'s "build a game to learn what the framework needs" approach: [[raw/omni_progress-april-14-2025.md]]

- **The disagreement:** Sasha held the framework is "по большому счету готов" and evolves per game; Val called that "как стрелять из лука в летающее яблоко" (shooting an arrow at a tossed apple) and insisted — "яблоко поставить, прикрепить жестко" — pin the game by using an **already-released** title so only the framework moves. Val's other reasons: JVL has built frameworks before and knows what it needs; the framework MVP features are already broken into Features/Stories in Jira (~50% marked non-MVP); and designers will "never" say they have everything they need. [[raw/omni_progress-april-14-2025.md]]
- **Why Kai-Ocho specifically:** it is the freshest released game ("наши руки уже наладились"), simpler than Fortune Fu Paws, and removes the most unknowns; the **Diamond Link bonus can be faked/stubbed** at first (entered only via enough Diamond symbols, so avoidable) — base game + free-spins is enough to exercise the framework. Its assets are not all reusable ("ресурсы символов не годятся") and need rework, but less than a new game. Val: "меньше всего нервотрепки." [[raw/omni_progress-april-14-2025.md]]
- **Cadence set:** Val ended his hands-off period ("эта свобода закончилась") and scheduled a **daily 6:30 am** planning meeting; features to be walked in Jira ("на 75% reliable") and planned under "Diamond Link Kaya-Ocho." Delivery/testing pressure: he flagged that [[wiki/people/dmitriy-khandov.md|Dima Khandov]] had **moved the math deadline three times** — [[wiki/people/andrew-khandov.md|Andrei Khandov]] does the math implementation while Dima does the new bonuses; [[wiki/people/irina-makarych.md|Irina]] told to push "нагло и беспощадно" for test cases; a feature can't ship without integration tests. [[raw/omni_progress-april-14-2025.md]]

## Apr 17 2025 — naming ruling and the asset-port method

- **Naming (ruled Apr 17):** the Omni port can't reuse the name "Calle Ocho" (already assigned to the released game and its assets/repos), so it ships to GLI as **"Kayo Ocho Omni"** (hyphenated) — Val: "I would call it Kayo Ocho Omni… put a hyphen in between"; Sasha had been blocked for three days needing a repository name. [[raw/game_development_update-apr-17-2025.md]] [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **Asset-port method (adopted):** not a straight as-is re-export (Lena's plan A, May-1) nor a full rebuild (Sasha's plan B, ~2 months), but Dima's **middle approach** — port what's portable, properly rework only what recurs across future games — driven by the June-1 pressure. Detail on [[wiki/topics/game-art-animation-production-pipeline.md]]. [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
- **Deploy the current Coyote meanwhile:** Val will keep deploying the **current** Coyote once its bill-validator bug is fixed, in parallel with building the Omni version. [[raw/game_development_update-apr-17-2025.md]]

## Relation

- Continues the "printing press for games" program on [[wiki/topics/omni-core-advancement-and-game-templating.md]] and the freeze rule [[wiki/decisions/2025-03-24-freeze-core-capabilities-before-game-production.md]].
- Kai-Ocho itself: the game Juan test-played in March (see [[wiki/topics/slot-game-design-principles.md]]).

## Sources

- [[raw/omni_progress-april-14-2025.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/game_development_update-apr-17-2025.md]]
- [[raw/graphical_assets_redesign_omni_calle_ocho-apr-17-2025.md]]
