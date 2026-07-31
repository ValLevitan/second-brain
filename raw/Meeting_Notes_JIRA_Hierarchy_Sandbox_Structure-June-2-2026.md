# Meeting Summary — JIRA Hierarchy Sandbox Mockup
**Date:** June 2, 2026, 12:03 PM (Eastern)
**Duration:** ~2h 10m (recording stopped for a 15-min break to bring in Andrei Bosik)
**Attendees:** Val Levitan, Pavel Frolov, Dmitri Kovalchuk, Irina Shishko

> Note: spoken in Russian; summarized in English. Product/platform names (Rage, Redge, GQUAM, LGS, DC, LiquidGlass, WebDeck) were transcribed phonetically and the speech-to-text was rough — worth a sanity check on exact spellings.

## Summary

The team worked live in a JIRA sandbox to agree on how to structure the product hierarchy. The sandbox is a snapshot from about May 6, used only to look at structure — not live data. Refreshing it would take ~1 hour to copy plus ~3 hours to rebuild the links, so Val said don't bother for now.

The hierarchy they worked with: **Value Stream → Product (IP) → Capability → Feature → Story**. Features also carry a **Project** (e.g. Framework, DC, Math), and they discussed adding a **Component** or **Market** field for filtering.

Most of the session was one question: when does something become its own capability, and when is it just features under one capability? They used **LiquidGlass** (the shared graphic UI) as the worked example, across two markets — **Georgia / GQUAM** (vertical cabinet) and **South Dakota** (horizontal cabinet).

Two ideas got settled. First, you do **not** split designer work and developer work into separate capabilities — that's artificial. A capability is one complete piece of functionality; the design-vs-development split happens lower down, at the Feature level. Second, you **do** open a new capability for each new product or market, even if it's nearly identical, because each one has its own delivery date, can be closed and released on its own, and is the only thing features (and therefore code) can attach to.

Val explained it with a building-permit analogy: a capability is like a permit to install a well-specified elevator in a building. The same elevator design goes in many buildings, but each building needs its own permit, and you close the permit when that building is done. Reusing the elevator in the next building means a new permit — i.e. a new capability to hang the reuse work on.

Dmitri floated removing the top levels (Value Stream, Product) and replacing them with custom fields for filtering, keeping Capability as the top. Val and Irina pushed back — you'd lose the big-picture view and get lost, since nobody recognizes every capability by its ID. The top levels stay; Component/Market can be an extra filter, not a replacement.

They also clarified that framework-level things like **Match-3** and **LiquidGlass** live under a framework/platform product (Rage), not under individual games, because they're built once and reused.

The recording was stopped for a 15-minute break to bring in **Andrei Bosik** and settle one open item: whether design artifacts and code live in one repository or two.

## Decisions Made

- **A capability is one complete piece of functionality, regardless of who builds it.** Don't create separate capabilities for design vs development — that split belongs at the Feature level. (Pavel, endorsed by Val and Dmitri)
- **Delete the redundant cap-35; fold its work into cap-34 as features.** Cap-34 already covers the functionality. (Val, Pavel)
- **Open a new capability for each new product/market variant, even if near-identical.** Reason: each has its own delivery date, closes independently, and is the anchor for features and code. Capabilities are never loosely "reused" — you open a new one (Jira "clone" is just a shortcut to copy ~95% then adjust). (Val, agreed by Pavel)
- **LiquidGlass restructure:** make IP-966 a general "LiquidGlass" product; cap-34 = LiquidGlass GUI for vertical machines (GQUAM v2); add a second capability for horizontal machines (South Dakota v2). Vertical vs horizontal genuinely differ (cabinet, game sets, progressives, resources). (Val, Pavel, Irina)
- **Keep the Value Stream and Product levels in the hierarchy.** Rejected collapsing them into custom fields. Component/Market can be an additional filter only. (Val, Irina)
- **Framework-level capabilities (Match-3, LiquidGlass) live under the framework/platform, not under individual games.** (Val, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Rework the sandbox per the agreed model: make IP-966 a general "LiquidGlass" product, rename cap-34 to LiquidGlass GUI – vertical (GQUAM v2), add a capability for LiquidGlass GUI – horizontal (South Dakota v2), delete cap-35 and re-express its work as features under cap-34 | TBD (next session) | Normal | Makes the agreed structure visible to the team |
| 2 | Val Levitan | Bring Andrei Bosik into the reconvened session to settle the one-repo-vs-two-repos question; share the written guidance he found with the team | Same day (after break) | Normal | Repo structure is the main open blocker |
| 3 | Irina Shishko / Pavel Frolov | Ask Lena how South Dakota (horizontal) home-screen and resources differ from Georgia (vertical) before finalizing the horizontal capability | TBD | Normal | Pavel said not to guess — get details from Lena |

## Open Questions

- **Repository structure** — one repo (one branch) for both design artifacts and code, or separate repos? Leaning toward one repo based on an earlier discussion with Andrei Bosik and Dima Khandov's git trial, but not confirmed. This is why Bosik was invited back.
- **Market tagging** — use a Component field, a Market field, or just describe the market in the capability description? Leaning toward writing it in the description (simplest), since a maintained component/market list risks becoming unmanageable.
- **Graphic-department workflow** — only the development side was worked through. Dmitri flagged the graphic side needs its own pass; deferred to later.

---
*Processed from Teams transcript on June 3, 2026*
*Source meeting: Hiearchy_sandbox_mockup-20260602_080347*
