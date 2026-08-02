# Meeting Summary — RIS Prose Documentation Standard
**Date:** July 2, 2026, 10:03 AM Eastern
**Duration:** ~1h 00m
**Attendees:** Val Levitan, Dzmitry Chudzinau, Pavel Frolov, Andrei Bosik, Irina Shishko, Sergey Tsimanov

## Summary

Val presented work he did that morning: he generated "prose" (plain-language `.md` documentation) for the **RIS** repository using a tool called **Fable**. Fable scored the code and prose **8 out of 10**. He worked in small steps from roughly 7 AM to 11 AM. The result is about **40 documents across two repositories**.

Val's proposal: prose should live in the repo next to the code, and every pull request should update it as part of the coding standard. He does not want anyone writing prose by hand — it's AI-generated. He cited Anthropic best practice and Boris Cherny's approach: many simple `.md` files, not one big document and not a single index. He asked the team to each read a few of the sample files to confirm they're sensible and not gibberish.

The team pushed back. **Andrei** said prose duplicates the pull-request description and could go stale as code moves ahead; he questioned who actually consumes it. **Sergey** noted the code already has JavaDocs above each method, so prose is duplicating those into separate files. **Dima** saw no benefit — it re-describes existing code method-by-method — and warned the large context would slow Claude down and cause more errors in long sessions. **Pavel** partly agreed the full prose set equals a specification, and suggested it be structured as a tree by module rather than a flat list.

Val disagreed that it's duplication. His main argument: prose creates alignment across the whole company — product, developers, architecture — letting anyone ask in plain language how something works, at any level of detail. He acknowledged it will expose defects in the current 20-year-old architecture, and said that's fine. On the "it slows Claude / makes it hallucinate" concern, he said that's a matter of structuring sessions correctly, and anyone who doesn't want the files read can configure their frontend to ignore them.

Dima also flagged that the RIS repo only covers game-settings creation — it doesn't touch progressives, machine management, or the protobuf output file passed to the legacy system. He wants the **legacy core** repo and the **new frontend** repo added to scope so the whole chain is visible.

Val ended the meeting slightly early to move to a follow-up with Pavel.

## Decisions Made

- **Extend prose generation to the remaining repositories** — add the legacy core repo and the new frontend repo Dima flagged, so the full chain is documented. (Decided by Val)
- **Commit the prose `.md` files back into each repository.** (Decided by Val)
- **Add a rule that every pull request updates prose alongside the code**, with Andrei to enforce it via GitHub tooling since Claude Code review can't enforce it natively. (Decided by Val)
- **Keep prose as many simple `.md` files, not one big document or a single linear index** (Val, citing Boris Cherny). Pavel wants a tree-by-module structure layered on top. (Direction set by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dima | Send Val the links to the extra repos still needing prose (legacy core + new frontend), via the team chat | TBD (soon) | Normal | Needed before Val can finish generating prose for the full chain |
| 2 | Val | Send the behavior-conventions / prose-standard `.md` file to the team chat | TBD (soon) | Normal | Team asked to read it (~30 sec) and endorse it as part of the standard |
| 3 | Val | Generate prose for the remaining repositories, then commit the `.md` files into each repo | TBD | Normal | Completes the RIS pilot across the whole system |
| 4 | Val | Build the pull-request rule that regenerates/updates prose on each PR | TBD | Normal | Makes prose self-maintaining |
| 5 | Andrei | Set up enforcement of the prose-on-PR rule using GitHub tooling | TBD | Normal | Claude Code review can't enforce this natively |
| 6 | Dima, Sergey, Pavel, Irina | Review the sample prose files and give Val feedback on whether they're accurate or gibberish | TBD | Low | Mostly done live; Dima & Sergey to look again once Val sends more |
| 7 | Pavel | Propose a tree/module structure for organizing the prose | TBD | Low | His suggestion — prose shouldn't be a flat list |

## Open Questions

- Does prose duplicate the PR description and JavaDocs (Andrei, Sergey)? Val says no — it serves a different, company-wide alignment purpose.
- Will large prose context slow Claude or cause errors in long sessions (Dima, Pavel)? Val says it's about structuring sessions correctly, and the frontend can be told to ignore the files.
- Does documenting the current "inflexible" code risk baking the same mistakes into new requirements (Dima)? Val says no — it exposes the defects so they can be fixed.
- Who is the target consumer of the prose (Andrei, Sergey)? Val: everyone — product, dev, architecture — not narrowly Claude or one role.

---
*Processed from Teams transcript on July 3, 2026*
*Source meeting: Review_prose_RIS-July-2-2026*
