---
type: meeting
title: Payment-hub ACH module spec review — undertakings, Plaid & QA testing (Nov 10 2025)
date: 2025-11-10
aliases: [ACH spec review Nov 10, Payment HUB ACH module specification Nov 10, ACH module spec session 3]
source-count: 1
---

# Payment-hub ACH module spec review — undertakings, Plaid & QA testing (Nov 10 2025)

**Date:** 2025-11-10 (7:04 AM recording; the "12:04PM" header line is a processing stamp — §11) · **Duration:** ~1h 36m · **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/juan-martinez.md|Juan Martinez]], [[wiki/people/nathan-carver.md|Nathan Carver]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (transcribed "Dzmitry Chudzinau"), [[wiki/people/irina-shishko.md|Irina Shishko]], [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]], [[wiki/people/alexei-khamin.md|Alexei Khamin]]. Bilingual (English/Russian).

Session 3 (arc complete) of the **ACH-module specification review arc** (Nov 5 → 6 → 10). Val opened by reviewing an **AI-summarised undertaking list** from the prior two recordings, and asked the team to adopt that meeting-prep discipline going forward. Settled the **Plaid-hosted bank-account entry** decision (JVL stores no bank/routing numbers — only the Dwolla/Plaid ID), scoped **QA test strategy** for the ACH module (state-machine-driven testing, ~20 InComm test cards to Minsk, simulated volume rather than physical), and named Pavel the meeting **driver**. Substance and the arc sequencer live on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (Nov-10 ACH-spec section).

**§15.8:** no compensation material — vendor/module economics and process only.

## Sources

- [[raw/Payment HUB_ACH module specification_10.11.25.md]]
