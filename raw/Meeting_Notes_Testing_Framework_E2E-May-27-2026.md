# Meeting Summary — Testing Framework Evolution for E2E Tests

**Date:** May 27, 2026, 10:05 AM Eastern
**Duration:** 1h 43m
**Attendees:** Val Levitan, Pavel Frolov, Andrei Bosik, Alexander Biratko, Irina Shishko, Dzmitry Chudzinau, Vladimir Samusenko, Sergey Tsimanov, Ivan Shpak, Alexey Khamin, Evgeny Kharetski

## Summary

The team discussed how to know when a CICD-built product is actually "done" — i.e., how to validate the transaction system end-to-end given that development moves dynamically across many self-contained repositories. The conversation centered on the transaction product, which is the closest to Standard 5.1 today.

**Three positions surfaced.** Pavel argued for an over-repository control layer: an integration repo holding a dependency graph (built manually at first, AI-maintained later), metafiles describing how cloud services + Flex_IQ + Recycler combine, and a committed history of AI-driven test runs so the next run can build on the prior one. Dzmitry, Sergey, and Vladimir argued for first building a test platform — deploying cloud infra plus real terminals, then writing auto-tests so QA stops repeating the same manual work. Andrei Bosik described the integration repository that already exists, which holds cross-component documentation; data contracts live inside each product repo and get auto-generated at build time into a versioned `docs-contract/` folder.

**Val pushed back hard on building any "platform" or framework upfront.** His point: every time we build human-style scaffolding for AI, we lock the AI into our rules and force it to ask permission instead of figuring things out. He referenced Andrej Karpathy's approach — let the AI propose, the human corrects, knowledge accumulates in the repo. He told the team: stop designing in the abstract, start assembling the product per Standard 5.1, hit the real problems, and solve those.

**Contract semantics clarified.** Sergey assumed contracts are two-sided agreements between repos. Andrei, Alexander, and Val corrected this: a contract is one-sided — a repo publishes its own contract ("public card," like Twilio's API docs), and any consumer reads it. Every repo must be self-sufficient (zero-trust). If a repo isn't self-sufficient, it's built wrong.

**Standard 5.1 status.** The standard exists and is partly implemented. Pavel admitted he had not seen it (he was on vacation). Val officially released the document company-wide. Alexander Biratko will distribute it; Andrei Bosik will attach a link to the compliance report his framework runs against the standard.

**CLAUDE.md scale limit.** Alexander noted CLAUDE.md works for small repos but degrades as project knowledge grows. Val mentioned Karpathy uses set.md files that grow into a wiki. Pavel suggested a per-repo knowledge base (wiki or Obsidian) referenced from CLAUDE.md.

**Pivot to action.** Val stopped the abstract debate. Instead of meeting again Friday to keep theorizing, the team will attempt a real production release of the transaction system next week (Tuesday/Wednesday/Thursday TBD). Expect failures. Failures will name the actual unsolved problems — secrets management, domain names, databases, MSBC integration, etc. — which become the real Friday agenda.

## Decisions Made

- **Standard 5.1 officially released company-wide.** Alexander Biratko distributes the document to everyone; Andrei Bosik attaches link to the compliance framework report.
- **No upfront test platform / framework will be built.** Team continues per Standard 5.1 and lets real assembly problems surface.
- **Contracts are one-sided, not bilateral.** Each repo publishes its own contract; consumers read it. Repos must be self-sufficient.
- **Production release attempt next week** (Tue/Wed/Thu — exact day chosen by Pavel by tomorrow). Initial attempt excludes Nathan's MSBC/billing/location services to remove known blockers from the first try.
- **Friday meeting (May 29) repurposed** — no more abstract discussion. Agenda is the open-questions list from Andrei plus anyone else's items.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Send Val a list of open questions for the production release (secrets, domain names, database choice, cloud naming, etc.) | May 28, 2026 | High | Val needs to review before Friday's meeting |
| 2 | Val Levitan | Review Andrei's list and call Andrei to walk through it | May 28, 2026 | High | Prep for Friday's productive discussion |
| 3 | Pavel Frolov | Pick the target day next week (Tue/Wed/Thu) for the first production release attempt and communicate it | May 28, 2026 | High | Anchors the rest of the schedule |
| 4 | Pavel Frolov + dev team | Attempt full production release of the transaction system, initially excluding Nathan's MSBC/billing/location services | Week of June 1, 2026 | High | The whole point — surface real problems by trying |
| 5 | Pavel Frolov + dev team | Record every failure and open question that surfaces during the production release attempt | During release attempt | Normal | Feeds Friday May 29 (or next) discussion |
| 6 | Alexander Biratko | Distribute Standard 5.1 document to entire company | ASAP | High | Val officially released it this meeting |
| 7 | Andrei Bosik | Send the compliance-report link alongside the Standard 5.1 distribution | With Standard distribution | Normal | So people can see what's being measured |
| 8 | Pavel Frolov | Host Friday meeting May 29 — walk the questions list, decide what's solvable, defer the rest | May 29, 2026 | Normal | Replaces the originally planned abstract continuation |

## Open Questions

- **Domain naming** for the production transaction services — raised by Andrei, deferred to a separate working session, not this meeting.
- **Secrets management in GitHub** for production — Pavel flagged this as the most obvious gap that will block the first release attempt.
- **Production database strategy** — Sergey raised whether "production" means new infra or just promoting the staging Postgres. Andrei: same DB as staging unless we plug something external. Not resolved.
- **Load testing** — Andrei wanted to do it before the release attempt; Dzmitry said deferred — first just try to bring it up.
- **Knowledge-base format for AI** — wiki vs Obsidian vs set.md per repo. Discussed, not decided; Alexander to consider as part of Standard 5.1 evolution.

## Related

- Initiative: [[Initiatives/E2E Testing Framework Evolution/initiative_statement|E2E Testing Framework Evolution]]

---
*Processed from Teams transcript on May 27, 2026*
*Source meeting: Testing Framework evolution for E2E tests*
