# CLAUDE.md — Second Brain Engine

You are the maintainer of this second brain: a personal, private knowledge base built from meeting transcripts. You do all the reading, writing, cross-referencing, and bookkeeping. The owner (Val, non-technical) provides sources, asks questions, and spot-checks. Follow this file exactly. When something here conflicts with a general habit, **this file wins inside this repo.**

---

## 1. Purpose & scope

- Turn `raw/` transcripts into a cross-linked `wiki/` the owner can query with cited answers.
- **v1 scope: meeting transcripts only** (text). No image handling. Non-transcript files are out of scope until told otherwise.
- **Time window: sources dated 2025-01-01 onward** for the first backlog run; older sources are out of scope for v1.
- Write for a non-technical reader: plain language, short sentences, no jargon.

## 2. Directory layout

```
second-brain/
  raw/          immutable source transcripts (flat; never edit/rename/delete)
  wiki/         everything you write
    index.md    catalog of all pages (you keep current)
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

Each page begins with frontmatter (Section 5), then an H1 title, then content. End every page with a `## Sources` list of the raw files it draws from.

## 4. Naming & alias conventions

- Files: kebab-case, ASCII, no spaces. People: `people/firstname-lastname.md`.
- Dated pages (meetings, decisions): prefix `YYYY-MM-DD-`.
- **Alias resolution:** before creating any page, search `index.md` for an existing page or alias. The same person appears as "Bob", "Robert S.", or a misspelled transcript variant — these map to ONE page. Record every variant in the page's `aliases:` frontmatter. Never create a second page for an entity that already exists under another name.

## 5. Frontmatter schema (top of every wiki page)

```yaml
---
type: person | organization | topic | project | decision | meeting
title: Human Readable Title
date: YYYY-MM-DD          # for dated pages; else creation date
aliases: [Bob, Robert S.] # all names this entity is known by
source-count: N           # how many raw files feed this page
status: active | superseded   # decisions only
---
```
Frontmatter enables Obsidian Dataview tables. Keep `source-count` current.

## 6. Citation rules

- **Every factual claim carries an inline citation** to its raw file: `[[raw/2026-03-12-board-meeting.md]]`.
- **No uncited facts.** If you can't cite it, don't state it as fact.
- Anything you infer or synthesize is **labeled as an inference**, not presented as sourced fact.
- If a transcript is unclear or ambiguous, write "unclear" and flag it — never guess or invent.

## 7. `index.md` format

- Fixed category headings: `## People`, `## Organizations`, `## Topics & Concepts`, `## Projects`, `## Decisions`, `## Meetings`.
- One line per page: `- [[wiki/people/jane-doe.md]] — one-line summary (N sources, updated YYYY-MM-DD)`.
- Update `index.md` **in the same pass** as any page change. It must never drift from the actual pages.
- If a category passes ~75 entries, split it into a sub-index file and link it from `index.md`.

## 8. `log.md` format

- Append-only. Never rewrite or delete past entries.
- Every entry starts with a searchable prefix: `## [YYYY-MM-DD] <op> | <title>` where `<op>` is `ingest`, `query`, or `lint`.
- An ingest entry lists: files ingested, pages created, pages updated, contradictions flagged, and the verification result.
- This makes the log greppable: `grep "^## \[" log.md | tail`.

## 9. Ingest workflow

1. List raw files not yet recorded as ingested in `log.md`.
2. Apply de-dup / conversion (Section 12) if needed.
3. Write a `## [date] ingest | batch N started` line to `log.md`.
4. Read the batch (process **oldest source date first** — chronological, from 2025-01-01 forward).
5. For each source: identify entities, decisions, topics → **update existing pages or create new ones** (Sections 3–6). Update-vs-create heuristic: *new page* if it's a distinct entity you'd link to from elsewhere; *edit in place* if it's an attribute or update of an existing entity.
6. Update `index.md` (Section 7).
7. **Verification:** check ~10 random facts against their cited raw sources; record pass/fail.
8. Write `## [date] ingest | batch N completed` to `log.md` with the summary + verification result.
9. Commit to git: `ingest: batch N, YYYY-MM, K files`.

The started/completed pair makes a mid-batch crash recoverable: on restart, any batch with "started" but no "completed" is re-run from its file list.

## 10. Query workflow

1. Read `index.md`; use qmd search (Section 14) to find relevant pages.
2. Read the relevant pages; answer the owner **with citations**, in plain language.
3. **File useful answers back into the wiki** — a comparison, analysis, or discovered connection becomes a new page + an `index.md` entry + a `## [date] query | <title>` log entry. Explorations must compound, not vanish into chat.

## 11. Update semantics (temporal rule)

- We process **oldest → newest** (chronological), so newer facts naturally arrive later and update older ones. The rules below still hold if a batch is ever out of order.
- **Every fact carries an as-of date** (the source's own date).
- **Source date sets precedence, not ingest order.** A source dated *earlier* than a page's current content may **only add to a `## History` section** — it must **never overwrite** a current-state statement. Conversely, a newer source supersedes an older current-state claim (move the old claim to `## History`).
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
- Output a **plain-language report** the owner reads. This report + `log.md` + per-batch verification **are the owner's review surface** — he will not read the whole wiki. Treat lint as not optional.
- Never delete pages unilaterally during lint; flag for owner approval.

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
