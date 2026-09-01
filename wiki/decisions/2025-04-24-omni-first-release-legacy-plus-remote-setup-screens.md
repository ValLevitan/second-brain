---
type: decision
title: First Omni release ships legacy setup screens plus new remote/USB initial-setup screens
date: 2025-04-24
aliases: [June 1 GLI submission, Omni setup screens scope, legacy screens plus new initial setup, IP 853, Omni LGS setup screens]
source-count: 1
status: active
---

# First Omni release ships legacy setup screens plus new remote/USB initial-setup screens

Val's directive on the Apr-24 2025 Omni setup-screens review ([[wiki/meetings/2025-04-24-omni-setup-screens-june-scope.md]]), resolving a scope argument about what can be finished for the first GLI submission. See [[wiki/topics/omni-core-advancement-and-game-templating.md]].

## What was decided

- **Target: submit the first Omni release to GLI by June 1** (Val used "June 1st" and "June 3rd" interchangeably, allowing "a couple of days off"). "June 1st means submission to GLI." [[raw/set_up_screen_omni-apr-24-2025.md]]
- **Incorporate the current/legacy setup screens and configuration unchanged** ("with exactly the same business logic, no changes") **plus the new React-based remote/USB initial-setup screens**; the rest of the setup screens stay **legacy**. Val: "Please release only these particular screens for approval to [[wiki/people/juan-martinez.md|Juan Martinez]]… This is an order." [[raw/set_up_screen_omni-apr-24-2025.md]]
- Screens in scope for the release: **language, passport, date, configure, USB/remote install, installation test** (presents RIS settings loaded from a USB stick or remote connection), **payout order, progressive settings** (select progressive controller — external controller assumed), and **game settings** — under a new **"installation" tab**. Most were already present in the **Calle Ocho** software release, in the new design. [[raw/set_up_screen_omni-apr-24-2025.md]]

## Rationale

- Only ~one month remains and there are effectively **two developers** ([[wiki/people/anton-seregin.md|Anton Seregin]], the front-end developer, and [[wiki/people/ihar-hrybko.md|Igor Hrybko]], the UI/UX designer). The setup tab alone was estimated at 60+ days; transferring all legacy business logic from the old **XJS** framework (2006/2008) to the new **React/TypeScript** framework cannot be done by June 1. [[raw/set_up_screen_omni-apr-24-2025.md]]
- The **legacy screens work with LGS** (the local gaming server) unchanged — [[wiki/people/alexander-biratka.md|Sasha Biratko]] confirmed by phone that "in case of using legacy screens, nothing needs to be changed in LGS." So the release can use the new remote/React initial-setup screens on top of the legacy data-center logic. [[raw/set_up_screen_omni-apr-24-2025.md]]

## Execution details

- Repo/JIRA: **IP 853 = "Omni LGS Setup Screens"** (under Core Technology IP 90 → Gaming Platform IP 481). In-progress features **LGS 554 / 564 / 561** (assigned to Anton Seregin) target completion ~May 4–7; **LGS 555** (bank setup) moved to backlog (needs back-end changes); a new **LGS 630 (6.3.0)** multi-language feature for the initial setup goes to Igor Hrybko, scheduled **May 3–17**. The **LGS UI screens repo moves from Bitbucket to GitHub** (LGS back-end is already on GitHub); [[wiki/people/andrey-bosik.md|Andrei Bosik]] helps open branches. [[raw/set_up_screen_omni-apr-24-2025.md]]
- Val's process directive: put a **serial/ID number on each Figma screen (bottom-left corner)** so every screen can be referenced by a stable ID through the project's life. [[raw/set_up_screen_omni-apr-24-2025.md]]
- Testing responsibility for now sits **on the developer**, not QA — "we stopped putting things on the QA department; we're turning QA into QA engineering" — until integration testing ramps up. [[raw/set_up_screen_omni-apr-24-2025.md]]

## Status

Active as of 2025-04-24. Deadline of record is the June-1 GLI submission; the setup-screen features themselves complete ~May 17.

## Sources

- [[raw/set_up_screen_omni-apr-24-2025.md]]
