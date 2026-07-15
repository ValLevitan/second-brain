---
type: decision
title: Port Kai-Ocho as the first game on the Omni framework, target June 1 for GLI
date: 2025-04-14
aliases: [Kai-Ocho on Omni, Kayo Ocho Omni, Kali-Ochi Omni, first Omni game decision]
status: active
source-count: 2
---

# Port Kai-Ocho as the first game on the Omni framework — target June 1 for GLI

## The decision

- Instead of building the new Omni framework against a brand-new game, JVL will **port the just-released game Kai-Ocho** (transcript renderings: "Kayo Ocho", "Kali-Ochi") **onto the Omni framework first** — "мы решили делать Kayo Ocho первая на Omni Framework … эту игру мы уже сделали, мы сейчас ее переводим на Omni Framework." Val wants it **fully assembled for GLI by June 1 2025** ("Я бы хотел бы ее видеть 1 июня"). [[raw/daily_omni_progress-apr-15-2025.md]]
- **Rationale (Val, recounting the Apr-14 morning meeting):** a framework and a game both evolving at once is "очень много variables" — like shooting an apple tossed in the air; "Лучше яблоко поставить" — pin the game still by using one already released, so only the framework moves. [[raw/cms_svn_github-april-14-2025.md]]
- **Port order agreed (the designer "Dima"):** base game / main scene + resources first, then dashboard, then the "видег" (as transcribed; base-game screens only), then tilts and big wins — "этого набора будет достаточно, чтобы показать … минимальный" game result. Math dependency: Kai-Ocho's math is in the old land-based format and must become a **container** usable for both land-based and online — to be discussed with [[wiki/people/efim-podvoiski.md|Efim]]. [[raw/daily_omni_progress-apr-15-2025.md]]
- **GLI completeness constraint:** setup screens can't be stubbed with the old screens ("Абсолютно нет") — GLI needs the full set (history, reports, settings); [[wiki/people/ihar-hrybko.md|Ihar Hrybko]] owns those setups and joins the next meeting. Integration tests to be built by Anton ([[wiki/people/anton-leshkevich.md|Anton Leshkevich]], context) working with [[wiki/people/alexander-biratka.md|Sasha Biratka]]. Features to be planned at ≤2 weeks each, with a time schedule tracked from the next-morning meeting. [[raw/daily_omni_progress-apr-15-2025.md]]

## Relation

- Continues the "printing press for games" program on [[wiki/topics/omni-core-advancement-and-game-templating.md]] and the freeze rule [[wiki/decisions/2025-03-24-freeze-core-capabilities-before-game-production.md]].
- Kai-Ocho itself: the game Juan test-played in March (see [[wiki/topics/slot-game-design-principles.md]]).

## Sources

- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
