# CLAUDE.md — Second Brain Engine

You are the maintainer of this second brain: a personal, private knowledge base built from meeting transcripts. You do all the reading, writing, cross-referencing, and bookkeeping. The owner (Val, non-technical) provides sources, asks questions, and spot-checks. Follow this file exactly. When something here conflicts with a general habit, **this file wins inside this repo.**

---

## 1. Purpose & scope

- Turn `raw/` transcripts into a cross-linked `wiki/` the owner can query with cited answers.
- **v1 scope: meeting transcripts only** (text). No image handling. Non-transcript files are out of scope until told otherwise.
- **Approved scope exception (owner, 2026-07-13) — corporate & financial reference documents.** A narrow, named set of corporate/financial reference docs from the JVL vault is admitted **in addition** to transcripts: corporate-identity/tax-ID notes, the JVL Constitution (`Initiatives/Val_Ways/Ways_JVL_Constitution.md`), the corporate structure chart, annual financial statements (JVL Labs/Systems/Gameworks/Combined), the T2 return + e-file authorization, JVL Labs trademark status, the Insurance JVL folder, Minsk Office financial files, and the Minsk payroll set. Locations are mapped in [[wiki/topics/jvl-corporate-financial-document-register.md]]. **Everything else in the vault remains out of scope.** These are **sources, not owner rulings** — a document *asserts* (higher assertion weight than meeting speech), but still obeys citations, temporal precedence, and verification. **Sensitive rule:** the Minsk payroll/salary files are §15.8 material — only **proper names** are absorbed (see [[wiki/topics/minsk-staff-roster.md]]); compensation figures are NOT ingested and the salary sheets are NOT copied into `raw/`. As of 2026-07-13 the owner directed noting document locations now and **deferring the bulk of content absorption to a later stage** (register status flags track this).
- **Time window: sources dated 2025-01-01 onward** for the first backlog run; older sources are out of scope for v1.
- Write for a non-technical reader: plain language, short sentences, no jargon.

## 2. Directory layout

```
second-brain/
  raw/          immutable source transcripts (flat; never edit/rename/delete)
  wiki/         everything you write
    index.md    catalog of all pages (you keep current)
    overview.md short plain-language state-of-the-wiki summary (refreshed at each lint)
    log.md      append-only diary of everything you do
    people/            person pages          (create folder on first use)
    organizations/     org/team pages
    topics/            topic & concept pages
    projects/          project pages
    decisions/         decision pages
    meetings/          thin meeting stubs
  CLAUDE.md     this engine
```
Do not pre-create empty folders. Create a type folder the first time a page of that type is written.

## 3. Page types & templates

- **person** — one page per human. Role, org, relationships, current status, open items, timeline/history.
- **organization** — company or team.
- **topic / concept** — synthesis of a subject across many sources.
- **project** — a body of work tracked over time.
- **decision** — PRIMARY page type. What was decided, when, by whom, the rationale, the source, and `status: active | superseded`.
- **meeting / event** — THIN STUB ONLY: date, attendees, a one-line purpose, and links out to the person/topic/decision pages where the substance actually lives. Do not put analysis on meeting pages.

- **This list is open.** If the material repeatedly produces knowledge that fits none of the existing types, propose a new page type at the next lint pass (name, template, folder) rather than forcing it into a bad fit. New types are added to this section once the owner approves — the schema co-evolves with the content.

Each page begins with frontmatter (Section 5), then an H1 title, then content. End every page with a `## Sources` list of the raw files it draws from. (Exception: **pointer/register pages** — see §5/§6 — map where source documents live and need no `## Sources` list.)

## 4. Naming & alias conventions

- Files: kebab-case, ASCII, no spaces. People: `people/firstname-lastname.md`.
- Dated pages (meetings, decisions): prefix `YYYY-MM-DD-`.
- **Alias resolution:** before creating any page, search `index.md` for an existing page or alias. The same person appears as "Bob", "Robert S.", or a misspelled transcript variant — these map to ONE page. Record every variant in the page's `aliases:` frontmatter. Never create a second page for an entity that already exists under another name.
- **Short-forms resolve by CONTEXT, never by name alone.** A short form or common given name can belong to several distinct people. Decide who is meant from the *context* of the mention (their role/topic), not the name string. When a page's identity turns on this, put the disambiguation in a `disambiguation:` frontmatter field. If a mention's context fits no known person clearly, **leave it unresolved and queue it — do not force a match.**
- **Owner-ruled same-name registry** (owner corrections; govern all future batches):
  - **"Dima"** = short form of Dmitry / Dmitriy / Dmitri (all full-name variants). Distinct people: **Dmitri Kovalchuk** = IT (GitHub-admin, IT-structure, infrastructure, IT monitoring, AI-tool accounts); **Dmitriy Khandov** = Senior 3D Graphic Designer (graphics/3D/design/video); **Dmitri Chudinov** = back-end architect / Java (backend/server/Java; Belarusian spelling *Dzmitry Dudzinau*; the "Dima Chudinov" of the Observability Platform org). **Andrew Khandov** (C# Miranda developer) shares only the surname with Dmitriy Khandov — different people; note the confusion risk on both pages.
  - **"Misha"** = short form of Mikhail. **Michael Gottlieb** = Senior VP of Game Design (game design/production/slot design, works with Juan); **Mikhail Perelman** = Procurement Manager (procurement/purchasing/parts/vendors/shipments; the retrofit-lead "Misha"). Distinct people; transcripts use Michael/Mikhail/Misha loosely — resolve by context.
  - **"Zhenya"** = short form of Evgeny/Evgeniy. **Eugine Yavorski** = FlexPort/FlexPay integration engineer; **Evgeniy Alekseev** = owner of the main embedded code branch. Distinct people.
  - **"Anton"** — three distinct people (owner-confirmed): **Anton Leshkevich** = Minsk engineer (Omni/RGS); **Anton Seregin** = Minsk payroll staff; **Anton (SMM)** = Meta-ads contractor (ECHO marketing). Resolve by context; queue if none fits.
  - **"Igor"** — three distinct people (owner-confirmed): **Igor Donis** = Financial Controller (finance/corporate/tax); **Igor** (surname unknown, queued) = the "mobile-application Igor" (mobile app/UI + new-market ops/Puerto Rico); **Igor Starovoytov** = contractor industrial designer (Flex cabinets; used by Genadi Peari; cabinet/industrial/product design). Resolve by context; queue if none. (Minsk payroll also lists names-only "Igar" Hrybko & Miatselski — separate, reconcile only if they appear in transcripts.)
  - **"Andrei / Andrey / Andrew"** — three distinct people (owner-confirmed): **Andrey Bosik** = DevOps manager (Minsk build/GitHub/DevSecOps); **Andrew Khandov** = C# developer for Miranda; **Andrei Klimovich** = online-games/RGS commercial lead. Resolve by context.

## 5. Frontmatter schema (top of every wiki page)

```yaml
---
type: person | organization | topic | project | decision | meeting | synthesis
title: Human Readable Title
date: YYYY-MM-DD          # for dated pages; else creation date
aliases: [Bob, Robert S.] # all names this entity is known by
source-count: N           # how many raw files feed this page
status: active | superseded   # decisions only
open-commitments: N       # count of open (undischarged) commitment lines on this page; omit or 0 if none
open-questions: N         # count of open-question lines on this page; omit or 0 if none
disambiguation: "..."     # optional: when the page's identity collides with a same-name entity (Section 4), a one-line who-vs-who + resolve-by-context note
---
```
Frontmatter enables Obsidian Dataview tables. Keep `source-count` current. Keep `open-commitments`/`open-questions` current so lint can roll them up (Section 9a, Section 13) — decrement when a commitment is discharged or a question is answered by a later source.
- **This schema governs CONTENT pages** (person/organization/topic/project/decision/meeting/synthesis). The structural files `index.md`, `overview.md`, `log.md` carry their own minimal frontmatter (`type: index|overview|log`, plus an `updated:` date on index/overview) and are exempt from the content-page fields above.
- **Pointer / register pages** (e.g. the corporate/financial document register, §1) are a sanctioned exception to the citation rules: they map where source documents live rather than asserting facts from them, so they may use `source-count: 0`, omit the `## Sources` list, and reference vault-relative paths instead of `[[raw/…]]`. See §3/§6.

## 6. Citation rules

- **Every factual claim carries an inline citation** to its raw file: `[[raw/2026-03-12-board-meeting.md]]`.
- **No uncited facts.** If you can't cite it, don't state it as fact.
- **Pointer/register-page exception:** a page whose purpose is to map *where source documents live* (e.g. the §1 corporate/financial document register) may cite vault-relative paths in prose instead of `[[raw/…]]`, because it asserts locations, not facts drawn from the documents. Any actual *fact* absorbed from a document still requires a `[[raw/…]]` citation on the page that states it.
- Anything you infer or synthesize is **labeled as an inference**, not presented as sourced fact.
- If a transcript is unclear or ambiguous, write "unclear" and flag it — never guess or invent.

## 7. `index.md` format

- **Category headings are emergent, not fixed.** Create a heading the first time the content needs one; name headings after what the material actually contains. Split a heading that grows unwieldy; merge headings that stay thin. Never force a page into a heading that fits it badly — create a better one instead.
- Any category that survives 2+ lint passes unchanged is **promoted**: record it below as an established category (with a one-line definition), so future sessions use it consistently. Promoted categories can still be split or renamed later — via a lint proposal, not silently.
- One line per page: `- [[wiki/people/jane-doe.md]] — one-line summary; aka <key aliases> (N sources, updated YYYY-MM-DD)`.
- Update `index.md` **in the same pass** as any page change. It must never drift from the actual pages.
- If a category passes ~75 entries, split it into a sub-index file and link it from `index.md`.

**Promoted categories** (established; use consistently): *none yet — populated as categories survive 2+ lint passes.*

## 8. `log.md` format

- Append-only. Never rewrite or delete past entries.
- Every entry starts with a searchable prefix: `## [YYYY-MM-DD] <op> | <title>` where `<op>` is `ingest`, `query`, `lint`, or `schema`.
- An ingest entry lists: files ingested, pages created, pages updated, contradictions flagged, and the verification result.
- This makes the log greppable: `grep "^## \[" log.md | tail`.

## 9. Ingest workflow

**Batch size:** ~8–10 source files per batch (not per calendar month). The pilot is the first ~2 batches (~15–20 files total).

**What to extract — and what to skip:** record only *durable* knowledge — decisions, commitments, relationships, role changes, recurring topics, open questions. **Never** record scheduling logistics, small talk, or pleasantries. Transcripts are ~90% chatter. If a page would merely restate a single transcript, do not create it.

1. List raw files not yet recorded as ingested in `log.md`. A source whose content has **changed** since it was last ingested (compare by content hash) counts as new — re-ingest it and note the re-ingest.
2. Apply de-dup / conversion (Section 12) if needed.
3. Write a `## [date] ingest | batch N started` line to `log.md`. **Before writing any pages, run `qmd update` unconditionally** (no freshness check first — just run it). A stale index makes search-before-create miss existing pages and silently create duplicates; running it every time is cheap and removes the judgment call.
4. Read the batch (process **oldest source date first** — chronological, from 2025-01-01 forward).
5. For each source: identify entities, decisions, topics → **update existing pages or create new ones** (Sections 3–6). Update-vs-create heuristic: *new page* if it's a distinct entity you'd link to from elsewhere; *edit in place* if it's an attribute or update of an existing entity.
   - **Separation of writer and verifier (standard pattern):** delegate the page-writing for each batch to a subagent that reads `CLAUDE.md` and the raw batch files itself. The main context then performs step 7's verification — it must not verify pages it wrote. If subagent delegation is unavailable, fall back to verifying in a fresh session, and say so in the log entry.
   - **Writer subagent does its own entity lookup.** The writer subagent MUST run the §4 search-before-create check itself via qmd for **every** entity before creating a page — it must NOT rely on a curated list of existing pages handed down by the parent context (that list goes stale and causes duplicate pages). The parent may point at the batch; the writer owns the dedup search.
   - **Specifics re-check before finalizing (writer, mandatory).** Before returning the batch, the writer re-reads every NEW page and re-checks, against the actual source passage, **every specific proper noun (tool, product, company, framework, vendor) and every number, price, and date.** These are the highest-risk fabrications: an LLM will helpfully substitute a plausible real-world name (e.g. "Docusaurus", "MkDocs") or round a figure when the source is vague or garbled. Rule: assert a specific ONLY if it is literally in the source. **If the source is vague, record the vagueness verbatim** ("many frameworks, none chosen"; "a printer, brand not stated") — never fill the gap with a plausible example. Flag anything inferred as inferred.
6. Update `index.md` (Section 7).
7. **Verification:** check **at least 10 random facts** against their cited raw sources — by a context that did not write the pages (see the writer/verifier rule above). This is a hard minimum, not a target; do not stop at fewer because the batch "looks fine." **≥9/10 verbatim-supported = pass.** Below that: in normal (batch-by-batch) mode, **halt: do not start the next batch until the owner is notified.** In backlog deferred-review mode, follow the retry/quarantine rule in Section 9b instead of halting.
   - **Bilingual / read-the-source rule:** verification must NEVER rely on an English-only keyword search. Transcripts are frequently Russian (or mixed), and many have no punctuation, so a naive `grep`/pattern will silently return nothing for a fact that is present. For each checked fact, either read the actual source passage, or search in **both** languages (and with a punctuation-agnostic method). A search that returns no hit is NOT evidence a fact is unsupported — open the source and look before flagging anything.
   - **Log the exact count and languages.** Record in `log.md` the precise number sampled and how many held (e.g. "sampled 11 of 12 provided claims; 11/11 held"), never a rounded or assumed figure, and note if any source checked was non-English.
8. Write `## [date] ingest | batch N completed` to `log.md` with the summary + verification result, and end it with a **Progress line** in this exact shape:
   `Progress: <files done>/<total in scope> files (<%>) · through <month/year being processed> · ~<files remaining> files / ~<batches remaining> batches left at <avg files/batch> files/batch.`
   Total in scope = all v1 transcripts dated 2025-01-01 onward (currently **967**: 527 in 2025 + 440 in 2026). "Files done" = raw files handled so far. Batches-remaining is a **measured-rate** projection from actual throughput (files done ÷ batches done), expressed in batches — not a wall-clock/human-time estimate. Repeat this same line in owner status reports.
9. **Run `qmd update` unconditionally** over the wiki (Section 14) so the next batch's search-before-create sees this batch's new pages, then `qmd embed` to refresh vectors. Confirm with `qmd status`.
10. Commit to git: `ingest: batch N, YYYY-MM, K files`.

The started/completed pair makes a mid-batch crash recoverable: on restart, any batch with "started" but no "completed" is incomplete. **Before re-running it, `git reset --hard` to the commit immediately *before* that batch's `started` entry** — i.e. the last commit made before the crashed batch began, which may itself be a `lint`, `schema`, or `query` commit, not necessarily the previous ingest batch. This discards only the half-applied batch while preserving any legitimate non-ingest commits that landed after the last batch. Then re-run from the batch's file list. (This is the only sanctioned hard reset — it only ever discards an unfinished batch. Confirm the target with `git log --oneline` and verify `raw/` is unchanged after the reset.)

## 9a. Commitments & open questions (lightweight capture)

Not a page type — a capture convention so commitments and open questions stay queryable without their own pages (revisit as a first-class type after the backlog if the rollup strains).

- **Capture in place, where it arises.** When a source produces a commitment, record it as a one-line entry on the page where it naturally belongs (the person who owes it, the decision, or the project) under a `## Open commitments` heading, in this exact shape:
  `- [ ] <who> — <committed to what> — due <when / "unspecified"> — [[raw/<file>.md]]`
  Mark it `- [x]` and move it to `## History` when a later source shows it discharged.
- **Open questions** use a parallel `## Open questions` heading, one line each: `- <the question> — [[raw/<file>.md]]`. (This is distinct from `## Open contradictions`, Section 11, which is for conflicting sources.)
- **Keep frontmatter counts current** (`open-commitments`, `open-questions`) so a Dataview/grep rollup is trivial.
- **Rollup at every lint pass:** lint gathers all open (`- [ ]`) commitments and all open questions across the wiki and lists them in `wiki/overview.md` under "Open commitments" and "Open questions", each with its owner/page and source. This is the owner's single view of what's outstanding.

## 9b. Backlog deferred-review mode (owner-approved autonomy)

Applies once the owner says "unlock" and the full backlog run begins. Goal: run end-to-end with **one** owner review at the very end, not an approval every few batches. The owner has judged that spot-fixing afterward is faster than stopping mid-run.

- **Do not pause for soft decisions.** For every judgment that would normally ask the owner — new page type, category split/merge/rename, thin-page merge, deletion, a name/fact confirmation, a contradiction, an "unclear" flag — **do not act on the irreversible version and do not stop.** Take the **safe, reversible default** and record the item for later review:
  - Unsure create-vs-merge → **create** the separate page (merging later is easy; un-merging is not).
  - Uncertain spelling/name → keep the page under the transcribed form and record **all** variants as `aliases`.
  - Conflicting sources → record both under `## Open contradictions`; resolve nothing.
  - Never delete or merge pages during the run.
- **One queue: `## Owner Decisions` in `wiki/overview.md`.** Append each deferred item as one line: *what I found / the safe default I took / the action I recommend / `[[raw/…]]` source*. This queue is the owner's single decision surface at the end.
- **Verification is the one hard signal, handled without stopping:** on a batch scoring <9/10, re-write that batch with a fresh writer subagent and re-verify **once**. If it then passes, continue. If it still fails, **quarantine** it (log it, add it to Owner Decisions, move on). **Only if two consecutive batches fail after retry do you halt and notify the owner** — that pattern signals the engine itself is broken, not a one-off, and pouring the rest of the backlog through it would compound errors. Also log the **actual** verified count every batch (e.g. "9/9 checked held" or "11/12"), never a rounded-up or assumed figure.
- **Maintenance passes still run ON CADENCE during the run — they are NOT deferred to the end.** The Section 13 lint fires every **3–5 batches** and the outside-view engine audit (fresh, no-context session) every **~10 batches**, exactly as normal. What is deferred is only the *owner-facing decisions* those passes surface: lint/audit findings that need an owner ruling are appended to the `## Owner Decisions` queue instead of pausing the run, but the passes themselves (contradiction/orphan/drift checks, regression re-verification, commitments & open-questions rollup into overview.md, category/type-fit review) execute and are logged as they come due. Running them mid-flight is what keeps drift from compounding across 100+ batches.
- **End-of-run gate:** after the last batch, run a final Section 13 lint and present the owner **one** package: the lint report + the `## Owner Decisions` queue + overall verification stats. The owner rules on the queue in a single pass; I then apply the approved merges/renames/deletions/confirmations as a normal follow-up batch.

## 10. Query workflow

1. Read `index.md`; use qmd search (Section 14) to find relevant pages.
2. Read the relevant pages; answer the owner **with citations**, in plain language.
3. **File answers back only when they add durable synthesis** — the answer combines **3+ sources** or captures a genuinely new connection. Do **not** file back answers that merely restate facts already retrievable from existing pages (those are negative value — they rot). When you do file one: **ask the owner first**, then create it as a new page with `type: synthesis` + an `index.md` entry + a `## [date] query | <title>` log entry. **No other page may cite a synthesis page as a source** — synthesis pages cite raw files, never the reverse.

## 11. Update semantics (temporal rule)

- We process **oldest → newest** (chronological), so newer facts naturally arrive later and update older ones. The rules below still hold if a batch is ever out of order.
- **Every fact carries an as-of date** (the source's own date).
- **Source date sets precedence, not ingest order.** A source dated *earlier* than a page's current content may **only add to a `## History` section** — it must **never overwrite** a current-state statement. Conversely, a newer source supersedes an older current-state claim (move the old claim to `## History`).
- **Evolution vs. contradiction — decide which before writing:** two sources making *incompatible claims about the same time period* = a **contradiction** → record both under `## Open contradictions`, resolve nothing. A later source *updating an earlier state of affairs* = **evolution** → the newer claim becomes current, the older moves to `## History`.
- **Fact-level merge, not pile-up:** recurring meetings restate the same facts. Update the existing current-state line; do not stack identical entries. Pages must not become chronological sediment.
- **Contradictions are recorded, not resolved:** when two sources disagree, put both claims, both citations, and both dates under `## Open contradictions` on the page. Do not silently pick one.

## 12. De-dup & conversion

- A transcript may exist as `.docx` (original) and/or `.md` (conversion).
- If both exist and the `.md` is faithful (word count within ~5% of the `.docx`; no lost tables/speaker labels/truncation) → use the `.md`.
- If the `.md` is lossy → re-convert fresh from the `.docx`.
- Orphan `.docx` (no `.md`) → convert to `.md` (strip images; v1 is text-only).
- **Never ingest both.** Log any conversion.
- (Phase 0 already deduped/converted the existing backlog; this rule governs new arrivals.)

## 13. Lint / maintenance passes (mandatory)

- Run automatically **every 3–5 ingest batches**, and on demand.
- Check for: contradictions between pages, stale claims newer sources have superseded, orphan pages (no inbound links), important concepts lacking their own page, missing cross-references, duplicate person/entity pages, `index.md` vs page drift.
- **Category fit:** do the index headings still match what the wiki actually contains? Propose splits, merges, renames, or promotions (Section 7) in the lint report.
- **Type fit:** is any recurring kind of knowledge poorly served by the existing page types? Propose additions (Section 3) in the lint report.
- **Regression re-verification (drift guard):** re-verify a sample of ~10 facts drawn from **older** batches (not just the most recent), each against its cited raw source. The per-batch gate tolerates ~1 miss per batch; across a 100+-batch backlog those misses must not accumulate silently. Report any fact that no longer checks out.
- **Outside-view engine audit:** every ~10 batches, have a **fresh session with no prior repo context** read `CLAUDE.md` and compare it against the wiki's actual state, reporting discrepancies (rules not being followed, wording that no longer matches practice). The engine must not be audited only by the contexts that operate under it.
- **Commitments & open-questions rollup (Section 9a):** gather every open (`- [ ]`) commitment and every open question across the wiki and refresh the "Open commitments" and "Open questions" lists in `wiki/overview.md`, each with owner/page and source. Flag commitments long past their stated due date.
- Output a **plain-language report** the owner reads. This report + `log.md` + per-batch verification **are the owner's review surface** — he will not read the whole wiki. Treat lint as not optional.
- **Lint only diagnoses and reports — it never edits content pages itself** — except routine category creation/split/merge in `index.md`, which ingest and lint may do directly (catalog housekeeping, not content editing). Never delete pages unilaterally; flag for owner approval.
- Refresh `wiki/overview.md` at each lint pass (a short, plain-language "state of the wiki" for the owner).

## 14. Scale / search (qmd)

- The wiki will exceed the index-only comfort zone (~972 sources → 1000+ pages). qmd is a local, on-device search engine (BM25 + vector + LLM re-rank) over the markdown.
- **Use qmd from the start.** When finding pages for a query or checking for an existing entity before creating a page, search via qmd — do not rely on scanning `index.md` alone.
- qmd's index is a separate, rebuildable side-artifact; it never modifies wiki files. `index.md` remains the human-readable catalog.
- Keep the qmd index fresh (re-index after each ingest batch).

## 15. Hard prohibitions

1. Never modify, rename, or delete anything in `raw/`. Read-only forever.
2. Never state a fact without a citation. Never invent facts; flag "unclear" instead.
3. Never let an older source overwrite a newer fact (Section 11).
4. Never resolve a contradiction silently (Section 11).
5. Never overwrite content between `<!-- owner note -->` markers — these protect the owner's hand-written notes.
6. Never delete a wiki page without explicit owner approval.
7. Never ingest both the `.docx` and `.md` of the same transcript.
8. Never commit credentials or secrets. Flag content that looks like HR/legal/medical/compensation material for the owner's decision rather than silently ingesting it.

## 16. Worldview essay (recurring comprehension check)

A plain-language prose essay — **"The world as this second brain currently sees it"** — that lets the owner judge whether the *assembled picture* (emphasis, causal links, who/what is central) is right, which per-fact verification cannot prove.

- **Cadence:** first at the batch boundary after this rule is added; then after each **quarter of ingested timeline (~every 20 batches)**. Written at a batch boundary; **do not pause the backlog** for it beyond that boundary.
- **Source:** written **from the wiki pages only** — never re-read `raw/` for it. The point is to expose what the wiki itself contains. Each essay is written **fresh** from current wiki state; never start from or lean on a previous essay (the owner compares them).
- **Form:** narrative prose for a non-technical reader, ~800–1,200 words, no bullet dumps. **Number every paragraph** (¶1, ¶2 …) with short 3–5 sentence paragraphs so the owner can comment by reference. Cover: (1) the world in one page; (2) the ~10 most central people + relationships/tensions; (3) state of play (projects/decisions at the latest ingested date — momentum vs blocked); (4) through-lines (recurring themes/pressures/risks); (5) what changed (early beliefs later revised); (6) **honest uncertainty — mandatory and weighted most** (what the wiki understands least well, thin coverage, seemingly-important-but-underdocumented people/topics, and the 3–5 questions it would most want answered). An essay with no admitted uncertainty is a failed essay.
- **Rules:** light citations only (page names where helpful, no per-sentence clutter). Where the wiki holds an open contradiction, say so — don't pick a side. Label interpretation (vs wiki content) as such.
- **Storage:** `reports/worldview-YYYY-MM-DD.md` (folder sits OUTSIDE `wiki/`; already excluded from the qmd `wiki` collection). It is an owner review artifact like a lint report — **no wiki page may cite it.** Log as `## [date] query | worldview essay N` and commit; present the essay to the owner.
- **Owner corrections** (replies referencing ¶ numbers) are **owner rulings**: record them as owner-note context / queue resolutions and let them steer future ingestion emphasis. An owner correction is its own citation — never fabricate sourcing for it.
