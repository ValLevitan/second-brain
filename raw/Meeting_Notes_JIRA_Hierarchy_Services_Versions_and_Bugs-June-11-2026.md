# Meeting Summary — JIRA Hierarchy Sandbox: Services, Versions & Where Bugs Live
**Date:** June 11, 2026, 7:31 AM (Eastern)
**Duration:** ~1h 7m
**Attendees:** Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Dmitri Kovalchuk, Irina Shishko
**Initiative:** [[Initiatives/JIRA Hierarchy Standard/statement_of_purpose|JIRA Hierarchy Standard]]
**Prior in series:** NOVA/Galaxy Hierarchy Planning (June 1) → JIRA Hierarchy Sandbox Structure (June 2) → IQ Deployment Jira Structuring (June 5) → Capabilities & Sandbox Sync (June 8)

> Note: spoken in Russian, summarized in English. The speech-to-text was rough and proper nouns were garbled (Transaction Galaxy, Flex IQ, Flex Recycler, capability/"capobility", IP). Both Dzmitry Chudzinau and Dmitri Kovalchuk are called "Dima" — positions are attributed via the transcript's speaker labels. Worth a sanity check on exact wording.

## Summary

This continues the JIRA hierarchy work (June 1 planning → June 2 sandbox → June 5 IQ deployment). The session worked through how to structure the hierarchy for **Transaction Galaxy**, and three things dominated: whether to keep "services" in the hierarchy, how to handle product versions on the timeline, and where bugs belong.

**Drop the broken-out services.** Pavel opened with a point raised earlier with Dmitri and Irina: the separately listed services (terminal hub service, authorization service, etc.) aren't needed in the product hierarchy. Val agreed strongly and gave the reasoning: the business/executive side doesn't really understand "services" — developers taught them the term by explaining the architecture, and they now use it loosely. The natural business language is **capabilities**. Services are an architecture concept that lives between developers, expressed in ADRs and in the repo standard (the repos build themselves per that standard — that's the contract). When you look at it you see services, but only from the architecture point of view. So services should not pollute the JIRA product hierarchy.

**Cross-cutting work like authorization.** They worked the example of a cloud service that lets a customer/operator log into the web platform, view their terminals, and see cashier/setup PIN codes. Val's point: this is neither Flex IQ nor Flex Recycler — it's a platform thing. Two options were debated: model it as its own product, or open an authorization **capability under each product** as needed. Dzmitry pushed putting a **marker/category field** (multiple values allowed) on each capability so a cross-cutting capability can belong to several groups and be found by filter, instead of being force-fit into one folder. The trade-off: filtering is great for automation (ask Claude "when does the last Flex IQ capability finish"), but you lose the human-friendly timeline "summary bar" that Dmitri Kovalchuk and Pavel want. They landed on: **no standalone authorization service** — put the capability under each product, accepting some duplication (consistent with June 2's "new capability per product/market").

**Products and versions.** The products become **Flex IQ** and **Flex Recycler**, each with several version groupings (Flex IQ v1 = IP-902, v2 = IP-903, etc.), with capabilities living under the version IP. Val clarified these aren't really "versions" — they're release/timeline groupings of capabilities that should close by a given release; nothing changes in GitHub (same repo), it's just the visual representation of where you are on the timeline. Within one grouping there can be multiple actual releases. Dzmitry worried the numbering could multiply (100 versions in a year); Dmitri Kovalchuk flagged someone has to track the latest version number. Who creates a version IP: decided at a joint team/product-owner session. Capabilities get written parentless first, then attached to a product/version once the team studies them.

**Where bugs live — the main unresolved item.** Val pushed hard, repeatedly: bugs currently sit at the **feature level**, and that's wrong — "Aaron told us this 20 times, bugs don't nest here." Per Aaron's guidance, a bug should spawn a **new feature** under the relevant capability. Val's model: a bug has only three root causes — (1) an incomplete/missing requirement (or missing acceptance criterion) on the capability, (2) a misinterpreted capability/feature (built something other than intended), or (3) a badly written test that didn't catch it. The fix is to revise the test, revise the feature, or add the missing requirement. The **missing-requirement case** is the one Val can't answer and wants to settle. Crucially, the fix attaches to the **already-shipped version in the field** (in main, or even archived) — **not** the current in-progress version. Val explicitly disagreed with Pavel, who wanted it on the current/next version.

**Consult "virtual Aaron."** A recurring theme: Val wants Pavel (with Andrei) to work through the hard parts with an AI profile of Aaron Bockelie — how leading firms (Anthropic, Google) structure Product/Capability/Feature autonomously, and specifically how to treat bugs that surface in already-released production. Val is confident there's an established answer they just don't know yet.

## Decisions Made

- **Remove the separately broken-out services from the product hierarchy.** Services are architecture (ADRs + repo standard), not business-facing hierarchy; the business works in capabilities. (Val, endorsed by Dzmitry and Pavel)
- **No standalone authorization service.** Put the authorization capability under each product as needed, accepting some duplication. (Dzmitry, agreed by the group)
- **Products = Flex IQ and Flex Recycler**, each with version groupings (Flex IQ v1 = IP-902, v2 = IP-903…); capabilities live under the version IP. (Pavel, Irina, Val)
- **Versions are release/timeline groupings, not code branches.** Same GitHub repo; the version is a visual representation of timeline position, and can contain multiple releases. (Val)
- **Bugs do not nest under features.** A bug spawns a new feature under the relevant capability, and the fix attaches to the already-shipped version in the field — not the current in-progress version. (Val, per Aaron's repeated guidance; Pavel partially disagreed on which version)
- **The transactional model fits; the gaming side needs its own pass.** (Dzmitry)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Work the open questions through with an AI profile of Aaron Bockelie (with Andrei): how leading firms structure Product/Capability/Feature, and especially how to treat bugs that surface in already-released production — including the missing-requirement case | Mon June 15 (next session) | High | Val is sure there's an established answer; this is the gating question |
| 2 | Val Levitan | Hold the follow-up session — Monday June 15, 7:00 AM ET — to hear Pavel's proposal on treating production bugs in released products | June 15, 2026 | Normal | Val is travelling this week |

## Open Questions

- **Missing-requirement bugs** — what to do when a production bug traces to a requirement that was never written. Deferred to the "virtual Aaron" consult.
- **Authorization / cross-cutting capabilities** — capability-under-each-product with some duplication vs. a marker/category field for filtering. Direction set (under each product) but the marker-field idea isn't fully closed.
- **Version-number sprawl** — how to keep Flex IQ v1/v2/v3… manageable and track the latest number.
- **Gaming side** — only the transactional side was modeled; the gaming hierarchy still needs its own session.

---
*Processed from Teams transcript on June 11, 2026.*
*Source meeting: Hierarchy_JIRA_sandbox-20260611_073109*
