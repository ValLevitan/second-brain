# Meeting Summary — NOVA capabilities checkpoint — LGS prose (Evgeny + Vlad)
**Date:** August 24, 2026, 8:42–9:16 AM Eastern
**Duration:** ~34 minutes
**Attendees:** Val Levitan, Vladimir Samusenko, Evgeny Kharetski, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_NOVA_LGS_Prose_Standard_Checkpoint-August-24-2026]]

## Summary

This was a checkpoint on the "prose" experiments. Prose is a plain-language description of what code does, written with Claude's help. Capabilities are then pulled out of that prose. The work covers the NOVA project and the older LGS (legacy game server) code.

**Vladimir's result.** He wrote prose for the frontend part. He told Claude to describe the code exactly as it is — no fixing, no guessing — in plain words, no technical terms. He first tuned Claude on one small example until the output matched what he wanted, then ran it over the whole project. He did not read all ~2,000 lines himself. To prove the method works, he took the same capability built two ways — once in the old LGS code (about 10 years old) and once in the new code — and checked that the capabilities recovered from the prose came out the same in both cases. They did. He got 29 capabilities from the experiment.

**Val's earlier experience.** Val and Andrei Bockelie tried the same thing. Writing prose from code alone gave weak results. What worked well was giving Claude the product's overall architecture first, then the code.

**Evgeny's result.** His output was good. He treated it as a cycle across ~26 modules — agree a rule set, then repeat module by module. He is more interested in the capabilities than in reading every line of prose. He also found many suspected bugs while writing prose — about 30-plus across modules as of last Friday — and recorded them in the same documents instead of stopping to fix them. Vladimir did the same but left them as open questions rather than confirmed defects.

**The gap.** There is a standard for writing capabilities, but no standard yet for writing the prose itself — document structure, whether technical detail belongs in it, how to extract capabilities consistently. Everyone is currently producing prose in their own shape (Val's, Dima Chudinov's, Vladimir's, Evgeny's). Val agreed a single standard is needed and said he is not the right person to author it.

**Where prose lives.** Prose and ADRs live next to the code, not inside Jira. Pavel proposed a `docs/prose` folder in every project; Val agreed. Capabilities and requirements (регламенты) live in parallel — not in a hierarchy. Features live under capabilities.

**Backend vs frontend overlap.** Vladimir and Evgeny each wrote prose for the same area from different sides (backend and frontend), so their two capability sets will overlap and conflict. They will merge them into one capability set after the standard exists. Val expects Claude can merge them quickly once it understands there are two sides.

**Timeline.** Val wants the whole team caught up by the end of September — clean linkage between the code+prose repositories and the capabilities/features in Jira. Evgeny estimates ~16 modules left, one to two per day, so one to two weeks. Val left the day-to-day scheduling to Irina and Pavel.

## Decisions Made

- **A single prose-writing standard will be created and placed in the standards repository.** Built from the best of the existing prose variants, then Claude is run over existing prose to bring it in line. (Decided by Val; owners Vladimir and Evgeny, with Dima Chudinov consulted.)
- **No code is committed without matching prose.** Any committed code must carry prose for that portion; when code changes, the old prose is replaced. This goes into the CLAUDE.md rules. (Decided by Val, agreed by Evgeny.)
- **Prose lives in a `docs/prose` folder next to the code in every project.** (Pavel proposed, Val agreed.)
- **Capabilities and requirements live in parallel, not in a hierarchy; features sit under capabilities.** (Restated by Val.)
- **Bugs found during prose writing are recorded in place, not fixed now.** They will be handled later in separate, focused sessions. (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Vladimir, Evgeny | Meet (local) to agree one prose-writing standard, then run Claude over existing prose to normalize it | Aug 25, 2026 | High | Evgeny proposed a meeting "tomorrow" |
| 2 | Vladimir, Evgeny | Place the agreed prose standard in the standards repository | ~Aug 26, 2026 | High | Val will monitor; "within a couple of days" |
| 3 | Vladimir, Evgeny | Merge the overlapping backend and frontend capability sets into one, after the standard is set | TBD | Normal | Val thinks Claude can do this in ~30 min |
| 4 | Evgeny | Finish prose + capabilities for the remaining ~16 modules | ~1–2 weeks | Normal | 1–2 modules per day |
| 5 | Pavel, Irina | Schedule daily team time to fill capabilities and open questions against already-written code; drive the whole team to catch up | End of Sep 2026 | Normal | Val's end-September target for full repo↔Jira linkage |
| 6 | Pavel, Irina | Assign Sergey Tsimanov (back from vacation) to write prose/capabilities for the backend/CMS and to verify the prose Val gave Dima is accurate | TBD | Normal | Dima Chudinov is busy / heading on vacation |
| 7 | Evgeny | Discuss with Andrei how to enforce a "no updated prose, no merge" rule on the repositories | TBD | Normal | Andrei was the initiator of the docs-folder idea; feasibility of the PR rule is unconfirmed |

## Open Questions

- Can a repository rule actually block a PR that changes code but has no updated prose folder? Evgeny is unsure; to be worked out with Andrei. (Which Andrei — Bockelie or Klimovich — is not clear from the transcript.)
- Whether the prose Val already handed to Dima Chudinov matches the current code still needs someone to verify it (proposed owner: Sergey Tsimanov).

## Dispatch Log

---
*Processed from Teams transcript on August 24, 2026, 10:02 AM Eastern (scheduled meeting-watcher)*
*Source meeting: NOVA capabilities checkpoint — LGS prose (Evgeny + Vlad)*
