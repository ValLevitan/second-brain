# Meeting Summary — Flex-POS Repo Architecture Review

**Date:** 13 April 2026, 2:02 pm – 2:28 pm Eastern
**Duration:** 26 minutes
**Attendees:** Val Levitan, Alexander Biratko, Andrei Bosik

## Summary

Val opened by separating two threads from the prior session: (1) confirming the agreed repo architecture is actually being implemented, and (2) Bosik's deployment question (deferred to a separate session). Biratko proposed that bringing repos into compliance with his v2 standard, and monitoring drift, is a simple Claude task — daily or weekly check.

The substantive debate was over **where shared data contracts live**. Biratko's v2 standard introduces a top-level repo (`repo-[product-name]`) holding cross-repo documentation including data contracts, on the principle that *"truth must live in one place"* and otherwise duplication-and-divergence is inevitable — *"if I change the contract in this repo, Claude here doesn't know who else uses it; the others won't change; everything breaks."*

Val resisted the top-level master concept based on his takeaway from Aaron — each repo should be self-describing, like a vendor publishing its own datasheet ("here is what I do, here is what I offer outward"); Claudes should be invoked one-per-repo, not from above, because session memory dilutes with depth. Biratko countered that without a known location for shared contracts, Claudes cannot find each other or know what to coordinate over; deploying to GitHub Actions or some server was floated.

Val invoked Aaron's `Monitor` tool (released 9 April, Claude Code v21.98) and Aaron's `Attend` framework as the missing piece: peers auto-discover, no server required, *"like a forum of agents — one Claude posts a change, the others see it, the one whose repo cares responds."* At minute 21:38 Biratko independently described exactly that pattern in his own words; Val confirmed *"that is exactly what Aaron built."*

Bosik asked at 24:12 whether the v2 document should therefore be discarded. Val refused: *"Stop — what Sasha did is steps forward. We just need to refine the scheme into v3."* Meeting adjourned with the joint Aaron session set for 14 April morning to resolve the architectural questions in front of Aaron.

## Decisions Made

- **Biratko's v2 document is not discarded — it is to be promoted to v3** with revisions agreed in the Aaron session.
- **Tomorrow's joint session with Aaron will resolve the open architectural questions.** (Val + Biratko + Bosik + Aaron.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|---|---|---|---|---|
| 1 | Bosik | Prep for AgentWays cutover (clone repo, decide deployment shape, verify Russian triggers, repoint watcher) | Before 14 Apr session | High | ✅ Email draft created in Outlook with full prep checklist |
| 2 | All | Joint session with Aaron to lock v3 architecture + AgentWays cutover | 14 Apr morning | High | Convergence point for both 13 Apr meetings |

## Engineering Signals

### Parked for 14 April Aaron Session

The following architectural points surfaced during the debate but are deliberately NOT being declared as ADRs/REQs yet — they are the agenda for tomorrow's Aaron session:

- Shared data contracts in dedicated sibling repo(s) vs top-level master repo (Val's position from Aaron, Biratko's v2 position).
- Per-repo self-describing `CLAUDE.md` as the per-repo source of truth.
- Single shared-contracts repo vs per-domain contract repos.
- Drift monitor on the agreed standard (Biratko's proposal — daily/weekly Claude check). **Biratko to raise this with Aaron tomorrow.**

## Open Questions — for Biratko to raise with Aaron tomorrow

1. Where does a task enter the system — how is it assigned to a particular Claude?
2. Cross-host Attend peer discovery mechanism.
3. Runtime — local vs container vs GitHub Actions.
4. Single shared-contracts repo vs per-domain contract repos.
5. Drift monitor on the agreed standard — is daily/weekly Claude check the right pattern?

---
*Processed from Teams transcript on 13 April 2026*
*Source meeting: GitHub Repo Architecture — Flex-POS Implementation Schedule Review*
