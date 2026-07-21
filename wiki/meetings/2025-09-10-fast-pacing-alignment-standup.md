---
type: meeting
title: Fast-pacing general-alignment stand-up — series opener (Sept 10 2025)
date: 2025-09-10
aliases: [fast-pacing stand-up, fast-passing general alignment stand-up, general alignment stand-up Sept 10, spec as touchstone, reverse Omni spec]
source-count: 1
---

# Fast-pacing general-alignment stand-up — series opener (Sept 10 2025)

**Date:** 2025-09-10 (3:31 PM) · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]]. Russian.

The **first of a recurring "fast-pacing / general-alignment stand-up" series** ([[wiki/meetings/2025-09-17-fast-pacing-alignment-standup-spec-prototyping.md|session 2 is Sept-17]], which moves this opener's "reverse Omni into a spec" directive into a working AI-spec prototype + interview plan; a Sept-24 session follows). Pavel gives a development status pass; Val delivers a management directive on **spec-driven development and testing**. Testing/spec substance on [[wiki/topics/test-automation-strategy.md]] (Sept-10 section); architecture threads relate to [[wiki/topics/persona-driven-design-and-orchestration-platform.md]].

Durable points (single source):
- **Auto-tester hire.** A new automated-tester started the prior Friday, working with [[wiki/people/anton-leshkevich.md|Anton]]; evaluating **Playwright** vs Selenium, plus glue Anton wrote to connect Playwright to JVL's setup. Working evenings (~4–8 PM) until ~October, then joining full-time after leaving his current job. Recruiting continues (rabota.by vacancy refreshed).
- **Release status.** Nebraska/Texas slipped a little (a feature took longer; hoping to ship in a day or two after a final bug fix). Also finishing **JPS / Any Bet** and **Fiery Reeling** re-release; a **credits/money-switching** change (green-buttons screen) still needs review by Lena/[[wiki/people/michael-gottlieb.md|Michael]] (maybe [[wiki/people/juan-martinez.md|Juan]]). Key release change = progress display of level-switching; math checked. Target: start of next week.
- **Payment hub + platform architecture.** [[wiki/people/eugine-yavorski.md|Evgeniy Yavorski]] promised his first update this week; architecture of the **payment hub** ("Raymond/pay-mint hub" — ASR mangle of *payment hub*) in progress. Pavel to draw the **top-level view** of the new-platform components ("Omni platform / Flex platform"), reviewed **Tuesday**. The payment hub is both service and product — an independent application **deployable on Amazon**, cloud-hosted, deployable per-country (e.g. close to the Georgia market). Jan-1 release requirement drives which MVPs ship and in what order; est. ~2 months with parallel Flex-POS / FlexPay work (FlexPay must be modified to run **through the payment hub**, not directly to InComm). [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (transcribed "Цыганов"/Tsyganov — a spelling drift, owner-ruled 2026-07-20) did a **Mother Goose** data-flow → printer spike for Flex-POS.
- **Product/game work.** A machine being reworked (Dima); free-spins/bonus states nearing done (Sasha = [[wiki/people/alexander-biratka.md|Biratka]] on bonus states); **progressive-drawing behavior** goes to [[wiki/people/igor-metelski.md|Igor Metelski]]; risk feature done on [[wiki/people/dmitriy-khandov.md|Dima Khanov]]'s side, pending Sasha/Igor. [[wiki/people/irina-shishko.md|Ira]] ran first machine trials.
- **Val's spec directive (the meeting's core).** The **spec** is the "**touchstone**" (камень соприкосновения) between developers and QA engineers, embodied in the branch — it must be neither over-complex (unbuildable) nor too simple (vague). **Officially drop "auto-tests"** as a goal; instead **write tests *for the spec*.** JVL must **reverse-engineer Omni into a spec** ("reverse Omni") — a permanent, ~10-year effort — then write tests per spec; an integration test is part of the **pull request** when a feature/capability is ready to merge to main; a caught bug sends you back to the spec (mis-interpretation vs code error). Method: **2-hour sessions daily/every-other-day** walking Omni module by module, recorded → transcript → **AI converts code to spec** → group discussion refines it. This is [[wiki/people/pavel.md|Pavel]] + [[wiki/people/irina-shishko.md|Irina]]'s undertaking to institute; developer skepticism is expected/natural. Pavel proposed a proof: independently write one small piece from a spec via AI to show it works. Val will make these stand-ups daily/weekly.

## Sources

- [[raw/fast-passing-general-alignment_stand-up-september-10-2025.md]]
