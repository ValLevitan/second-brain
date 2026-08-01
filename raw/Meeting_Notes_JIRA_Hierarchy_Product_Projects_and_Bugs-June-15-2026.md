# Meeting Summary — JIRA Hierarchy: Product-as-Project & Where Bugs Live (virtual-Aaron review)
**Date:** June 15, 2026, 12:02 PM (Eastern)
**Duration:** ~58 min
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Dmitri Kovalchuk
**Initiative:** [[Initiatives/JIRA Hierarchy Standard/statement_of_purpose|JIRA Hierarchy Standard]]
**Prior in series:** NOVA/Galaxy Planning (Jun 1) → Sandbox Structure (Jun 2) → IQ Deployment (Jun 5) → Capabilities & Sandbox Sync (Jun 8) → Services, Versions & Bugs (Jun 11)

> Spoken in Russian, summarized in English. Speech-to-text was rough and proper nouns were garbled (capability/"capobility", Flex IQ, Flex Recycler, Wallet Management/"его лет менеджмент", value stream, requirement/"reclament"). Worth a sanity check on exact wording. This session is the "virtual Aaron" consult promised on June 11 — Pavel presenting findings from running the open questions past several AIs (Gemini, GPT) as stand-in expert reviewers.

## Summary

Pavel presented his findings from consulting several AIs on the two unresolved questions from June 11: how to position Product in the hierarchy, and how to handle bugs in already-shipped work.

**Finding 1 — Product comes out of the hierarchy.** Putting Product at level 2 was wrong; a product is essentially a static asset, not a time-bound deliverable. The AIs say model a product either as a JIRA **Component** or as its own **Project**. The level-2 slot (currently "Product/Service") should be renamed **Initiative** — a goal over a 3/6/9-month horizon that contains products and capabilities. Val floated "platform," "family," or "union" (союз) as the umbrella word. All AIs agreed Capability sits cleanly in the structure, and requirements live in their own project linked to capabilities.

**Product → its own JIRA Project (the idea that gained the most traction).** Dmitri objected to calling a product a "component" — a product is *made of* components, not one itself. Pavel's better option: give each product its own JIRA Project, so it genuinely owns its components. The worry was too many projects, but Dmitri countered that projects don't appear on the timeline (only the type hierarchy does) — they're just containers, and every developer already has access to all of them. He ended up strongly favoring one project per service/product. Pavel came around, mainly because it maps JIRA 1:1 to GitHub (one project ≈ one repo), killing the current BEP-style confusion where one project spans 15–25 repos and a newcomer doesn't know where to look. Components then become true product components (backend, frontend, library). Pavel's trade-offs: a long list of project spaces (which they'd worked to shorten), and per-project upkeep (teams, filters, kanban boards, Plans scope) landing on Dmitri — though Dmitri said the upkeep is manageable.

**Service = product = project; capabilities can be cross-product.** A service is not an initiative. An initiative (e.g., a configuration-management system) contains capabilities; a capability can span products.

**Bugs — two firm agreements.** (1) **Never reopen a closed feature for a bug** — all AIs agreed, matching Aaron's repeated guidance. (2) **Bugs do not belong in the forecastable hierarchy.** Val's strong position: the hierarchy exists for forecasting, and bugs can't be forecast — they wedge in and eat time. So a bug should attach to a feature as a **side link/dependency**, not nested in the parent chain. Dmitri confirmed: if you don't want bugs on the timeline, they live separately and just get linked. For accumulated bugs, Val wants a **"technical-debt paydown" track** under the project at planning time, rather than the AIs' suggested artificial "stabilization capability" (Gemini's "Payment Core Stabilization" example) or a "Maintenance" feature.

**Irina's alternative — capabilities never close, they change status.** Per GPT's advice to her: a capability is a business capability that lives as long as the product does and dies only with it; it moves between statuses (active, etc.) rather than closing. Her bug flow: create the bug → investigate root cause → code error, test error, or missing requirement; if a requirement was missing, update the requirement and spawn a new feature to implement it. Val found this genuinely appealing — specifically that capabilities don't close, they change status — and said he'd never considered it.

**Pavel's counter (his view shifted since Friday).** Everything inside the hierarchy should be **closeable**, because each item needs a target release date or it slips forever. The product is the asset and shouldn't live inside the hierarchy as a closeable item — it stays open as a component/project, while all the real work under it closes.

**Capability sprawl & versioning (left open).** Irina's concern: a capability like "Wallet Management" keeps spawning "Wallet Management 2…10" as new requirements arrive, all about the same thing — and if capabilities close, you must drag old requirements forward each time. Val and Pavel see versioning at the **product-release** level (each release lists the capabilities it shipped), living in GitHub, not as a separate capability version. To tell which capability is newest you'd trace which product versions it belonged to — which Dmitri flagged as hard to navigate at scale.

**Close.** Val asked Pavel and the team to assemble Irina's proposal plus the agreed ideas into a **new presentation with a visual diagram** — he thinks the scheme works but can't commit without seeing it laid out. Follow-up set for the **same time tomorrow (June 16)**. Val left for the airport (travelling this week); parting read: "we're going in the right direction."

## Decisions Made

- **Product comes out of hierarchy level 2.** Strong lean to model each product as its own JIRA Project (≈ one Git repo each); rename the level-2 slot "Initiative." Endorsed by Pavel and Dmitri, liked by Val — to be confirmed once visualized.
- **Never reopen a closed feature for a bug.** (All AIs; matches Aaron's guidance.)
- **Bugs are not nested in the forecastable hierarchy** — a bug attaches to its feature as a side link/dependency. (Val, confirmed by Dmitri.)
- **Requirements live in their own project, linked to capabilities; capabilities can be cross-product.**
- **Accumulated bugs handled as a "technical-debt paydown" track** under the project at planning time, rather than artificial maintenance/stabilization features. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Build a new presentation with a visual diagram capturing Irina's proposal + the agreed ideas (product→project, capability handling, bug-on-the-side) | June 16 (next session) | High | Val explicitly asked; he needs the visual to commit to the scheme |
| 2 | Pavel, Irina, Dmitri | Keep working the open points (capability close-vs-status, exact bug mechanism) and bring further proposals | June 16 | Normal | Carries the unresolved items into tomorrow |
| 3 | Val Levitan | Hold the follow-up session — same time tomorrow, ~12:00 PM ET June 16 | June 16, 2026 | Normal | Val travelling this week |

## Open Questions

- **Do capabilities close, or only change status and live as long as the product?** Irina's status model vs the closeable / "stabilization capability" model. Explicitly NOT decided — deferred to the visual session.
- **Capability sprawl & versioning** — how to avoid "Wallet Management 2…10" and how to identify the latest capability.
- **Exact bug mechanism** — side-link to feature agreed in principle, but where the fix-work attaches and whether any "stabilization"/"maintenance" container is used is open.
- **Project-count / upkeep** of one-project-per-product (filters, boards, Plans scope, team assignment) — flagged by Pavel, not resolved.

---
*Processed from Teams transcript on June 15, 2026.*
*Source meeting: JIRA Hierarchy — Production Bugs & Missing Requirements (virtual-Aaron review)-20260615_080202*
