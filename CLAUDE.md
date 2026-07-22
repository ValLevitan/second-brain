# CLAUDE.md — Second Brain Engine

You are the maintainer of this second brain: a personal, private knowledge base built from meeting transcripts. You do all the reading, writing, cross-referencing, and bookkeeping. The owner (Val, non-technical) provides sources, asks questions, and spot-checks. Follow this file exactly. When something here conflicts with a general habit, **this file wins inside this repo.**

---

## 1. Purpose & scope

- Turn `raw/` transcripts into a cross-linked `wiki/` the owner can query with cited answers.
- **v1 scope: meeting transcripts only** (text). No image handling. Non-transcript files are out of scope until told otherwise.
- **Approved scope exception (owner, 2026-07-13) — corporate & financial reference documents.** A narrow, named set of corporate/financial reference docs from the JVL vault is admitted **in addition** to transcripts: corporate-identity/tax-ID notes, the JVL Constitution (`Initiatives/Val_Ways/Ways_JVL_Constitution.md`), the corporate structure chart, annual financial statements (JVL Labs/Systems/Gameworks/Combined), the T2 return + e-file authorization, JVL Labs trademark status, the Insurance JVL folder, Minsk Office financial files, and the Minsk payroll set. Locations are mapped in [[wiki/topics/jvl-corporate-financial-document-register.md]]. **Everything else in the vault remains out of scope.** These are **sources, not owner rulings** — a document *asserts* (higher assertion weight than meeting speech), but still obeys citations, temporal precedence, and verification. **Sensitive rule:** the Minsk payroll/salary files are §15.8 material — only **proper names** are absorbed (see [[wiki/topics/minsk-staff-roster.md]]); compensation figures are NOT ingested and the salary sheets are NOT copied into `raw/`. As of 2026-07-13 the owner directed noting document locations now and **deferring the bulk of content absorption to a later stage** (register status flags track this).
- **Contractors Control (owner-approved 2026-07-13, names/process only).** The `Contractors Control/` folder (monthly invoices, AP authorizations, cost analyses, `CONTRACTOR_NOTES.md`, `_Standard/`) is admitted for **contractor names/business/role** (see [[wiki/topics/jvl-contractor-roster.md]]) and the **billing *process*** rules (see [[wiki/topics/jvl-contractor-billing-process.md]]) — **rates, invoice amounts, AP totals, cost-per-artifact spend, and HR compensation terms are §15.8 and remain HELD** (not ingested; invoices/authorizations not copied to `raw/`). This is 2026 data, outside the 2025 transcript window — used for entity resolution, not the backlog timeline.
- **Time window: sources dated 2025-01-01 onward** for the first backlog run; older sources are out of scope for v1.
- **Email correspondence is OUT OF SCOPE (owner, 2026-07-14).** The JVL Obsidian vault contains large email-ingestion corpora built under `Vault Admin/Email_Import_Standard.md` (e.g. `Legal/Mexican Tax Litigation/` — `Correspondence/` notes, `Originals/` .eml, audit logs). These are a SEPARATE system with its own runbook and must NOT be swept into this second brain: never stage email notes/.eml into `raw/`, never treat `Correspondence/` folders as transcript sources, and never let email-matter folders alter the transcript-backlog count or batch plan. If a future owner ruling admits a specific email matter, it enters as a named §1 scope exception like the corporate docs — not by default.
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
- **decision** — PRIMARY page type. What was decided, when, by whom, the rationale, the source, and `status: active | superseded`. **When a later source invalidates a decision's *titular* element** (e.g. the Nebraska nudge was killed while the "base on Georgia software" core survived), do not leave an `active` decision whose headline now asserts the opposite of reality: **retitle** to current state (and/or strike the dead element), and either flip `status: superseded` (if the whole decision fell) or annotate the status line to name the dead sub-element and point at the dated Update. A reader scanning titles/status must not be misled.
- **meeting / event** — THIN STUB ONLY: date, attendees, a one-line purpose, and links out to the person/topic/decision pages where the substance actually lives. Do not put analysis on meeting pages.

- **This list is open.** If the material repeatedly produces knowledge that fits none of the existing types, propose a new page type at the next lint pass (name, template, folder) rather than forcing it into a bad fit. New types are added to this section once the owner approves — the schema co-evolves with the content.
- **Multi-session arcs get a sequencer, not scattered stubs.** When one storyline plays out across many dated meetings (e.g. the GitHub↔Jira restructuring over Apr 1/2/3/7/8/9/11, or the FlexPay/SMIB evolution), the individual meeting stubs stay thin, but the **topic or decision page for that thread carries a short dated timeline** ("Apr 1 → … Apr 11 → current state") so a reader reconstructs the sequence without walking every stub. This is the existing topic/decision page doing sequencer duty — not a new page type.

Each page begins with frontmatter (Section 5), then an H1 title, then content. End every page with a `## Sources` list of the raw files it draws from. (Exception: **pointer/register pages** — see §5/§6 — map where source documents live and need no `## Sources` list.)

- **Meeting-stub citation convention:** a single-source meeting stub implicitly cites its one transcript for the whole page (the `## Sources` entry suffices); inline `[[raw/…]]` cites are optional there. A stub citing MORE than one source must cite inline per claim. All non-meeting pages always cite inline per §6.

## 4. Naming & alias conventions

- Files: kebab-case, ASCII, no spaces. People: `people/firstname-lastname.md`.
- Dated pages (meetings, decisions): prefix `YYYY-MM-DD-`.
- **Alias resolution:** before creating any page, search `index.md` for an existing page or alias. The same person appears as "Bob", "Robert S.", or a misspelled transcript variant — these map to ONE page. Record every variant in the page's `aliases:` frontmatter. Never create a second page for an entity that already exists under another name.
- **Short-forms resolve by CONTEXT, never by name alone.** A short form or common given name can belong to several distinct people. Decide who is meant from the *context* of the mention (their role/topic), not the name string. When a page's identity turns on this, put the disambiguation in a `disambiguation:` frontmatter field. If a mention's context fits no known person clearly, **leave it unresolved and queue it — do not force a match.**
- **Owner-ruled same-name registry** (owner corrections; govern all future batches):
  - **"Dima"** = short form of Dmitry / Dmitriy / Dmitri (all full-name variants). Distinct people: **Dmitri Kovalchuk** = IT (GitHub-admin, IT-structure, infrastructure, IT monitoring, AI-tool accounts); **Dmitriy Khandov** = Senior 3D Graphic Designer (graphics/3D/design/video); **Dmitri Chudinov** = back-end architect / Java (backend/server/Java; Belarusian spelling *Dzmitry Dudzinau*; the "Dima Chudinov" of the Observability Platform org). **Andrew Khandov** (C# Miranda developer) is Dmitriy Khandov's FATHER (owner-confirmed 2026-07-14) — two people, one family; note the confusion risk on both pages.
  - **"Misha"** = short form of Mikhail. **Michael Gottlieb** = Senior VP of Game Design (game design/production/slot design, works with Juan); **Mikhail Perelman** = Procurement Manager (procurement/purchasing/parts/vendors/shipments; the retrofit-lead "Misha"). Distinct people; transcripts use Michael/Mikhail/Misha loosely — resolve by context.
  - **"Zhenya / Evgeny"** — **EXHAUSTIVE at THREE per owner (2026-07-20; Zhenya = Evgeniy = Evgeny = Eugine, one name — there is NO fourth Zhenya at JVL):** **Eugine Yavorski** = FlexPort/FlexPay integration software (aliases Egorsky, Nevorsky/Неворский); **Evgeniy Alekseev** = embedded code + hardware-adjacent work (boards/redesigns/electronics, esp. Genadi Peari's projects); **Evgeny Kharetski** = LGS/Omni backend (payroll "Kharetski Yauheni"; garble-aliases Koretski/Khorvatsky/Корецкий/Хорватский) → `wiki/people/evgeny-kharetski.md`. Resolve by context: FlexPort/FlexPay integration software → Yavorski; embedded/hardware-adjacent & Genadi's projects → Alekseev; LGS/Omni backend → Kharetski. **A mention fitting none clearly is a mis-heard non-Zhenya (cf. the Ethan/Efim pattern) — treat as garble/mishearing and queue; NEVER create a fourth Zhenya.**
  - **"Anton"** — three distinct people (owner-confirmed): **Anton Leshkevich** = Minsk engineer (Omni/RGS); **Anton Seregin** = Minsk payroll staff; **Anton (SMM)** = Meta-ads contractor (ECHO marketing). Resolve by context; queue if none fits.
  - **"Igor"** — five distinct people: **Igor Donis** = Financial Controller (finance/corporate/tax); **Igor (Ihar) Nazarenka** (owner-confirmed 2026-07-14) = the "mobile-application Igor" (mobile app/UI + new-market ops/Puerto Rico) → `wiki/people/igor-nazarenka.md`; **Igor Starovoytov** = contractor industrial designer (Flex cabinets; via Genadi Peari); **Igor Metelski** = engineer on Efim Podvoiski's RGS/online-integration codebase (owner-confirmed = the payroll "Igar Miatselski"; Belarusian spelling); **Ihar Hrybko** = UX/UI (payroll "Igar Hrybko"; reconciled Batch 17 via the JVL Insights draft). Resolve by context; queue if none.
  - **"Andrei / Andrey / Andrew"** — three distinct people (owner-confirmed): **Andrey Bosik** = DevOps engineer (Minsk build/GitHub/DevSecOps; owner wording 2026-07-14); **Andrew Khandov** = C# developer for Miranda; **Andrei Klimovich** = online-games/RGS commercial lead. Resolve by context.

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

**Promoted categories** (established; use consistently — survived 5 lint passes): **People** (individuals, one page per person, `disambiguation:` on same-name clusters) · **Organizations** (companies/entities/vendors) · **Topics & Concepts** (subjects, grouped in the index under 6 sub-headings) · **Projects** (bounded initiatives with an end state) · **Decisions** (dated rulings, one page each, grouped under 5 sub-headings) · **Meetings** (thin stubs, grouped by month).

## 8. `log.md` format

- Append-only. Never rewrite or delete past entries.
- Every entry starts with a searchable prefix: `## [YYYY-MM-DD] <op> | <title>` where `<op>` is `ingest`, `query`, `lint`, or `schema`.
- An ingest entry lists: files ingested, pages created, pages updated, contradictions flagged, and the verification result.
- This makes the log greppable: `grep "^## \[" log.md | tail`.

## 9. Ingest workflow

**Batch size:** ~8–10 source files per batch (not per calendar month). The pilot is the first ~2 batches (~15–20 files total).

**What to extract — and what to skip:** record only *durable* knowledge — decisions, commitments, relationships, role changes, recurring topics, open questions. **Never** record scheduling logistics, small talk, or pleasantries. Transcripts are ~90% chatter. If a page would merely restate a single transcript, do not create it.

1. List raw files not yet recorded as ingested in `log.md`. A source whose content has **changed** since it was last ingested (compare by content hash) counts as new — re-ingest it and note the re-ingest.
   - **Staging by systematic enumeration, never thematic selection (mandatory).** Build each batch's file list by enumerating the master in-scope file set in a deterministic order — the vault month-folder in filesystem/date order — and taking the next N not-yet-ingested files. Do **not** hand-pick files by theme, thread, or interest: cherry-picking silently leaves holes (a mid-month file skipped because it "didn't fit the cluster" is invisible until an audit finds it). Thematic coherence is the writer's job via §4 search + §12 cross-file dedup, not a staging filter. The in-scope set is the month folders under the 2025-01-01-onward window (see §1); process month-by-month, and within a month in filename/date order.
   - **Generate the batch list from the vault↔raw pending-sweep diff — NEVER from hand-rolled date-range or exclusion regexes.** The correct enumeration is: for the current month folder, list every file NOT already present in `raw/`, and take the earliest by content/filename date. Do this with a plain "for each vault file, is it in raw/? if not, it's pending" diff — the same diff the per-batch no-file-loss audit runs. **Do NOT** filter with patterns like `grep -viE "…month-3"` to drop day-30 files: `month-3` also matches `month-3-<year>` (the 3rd), silently nuking those files. This exact bug recurred twice (the **June-3** and **July-3** gaps — an exclusion meant to drop `june-30`/`july-30` also excluded `june-3`/`july-3`). The month-close sweep caught both, but staging should never introduce the hole in the first place. Stage from the pending list, not from a bespoke regex.
   - **Filename-collision check at staging (mandatory — generic filenames reused across months).** Some source filenames are GENERIC and recur across month folders (e.g. `finance_recurring_meeting.md` appears in Sept AND Nov). Before `cp <source> raw/<name>`, check whether `raw/<name>` already exists with **different content** (`md5sum` mismatch). If so, it is a COLLISION — a blind `cp` OVERWRITES the earlier month's raw copy while its pages still cite that filename, silently corrupting them (this happened: batch 85's `finance_recurring_meeting.md` overwrote the Sept-9 raw that 5 pages cited). **Never overwrite.** Stage BOTH under dated names (`raw/<name>-<month>-<day>-<year>.md`), re-point any existing citations of the bare name to the correct dated file by context, and remove the ambiguous bare file. Prefer dated raw filenames for any source whose vault name lacks a date. (Schema entry: 2026-07-20.)
   - **The §12-skip ledger — never re-surface a deliberate skip (mandatory).** A file that was staged into `raw/` and then §12-skipped (a re-transcription / numbered-copy / segment already covered by a fuller source of record) is **handled but will never be cited**. A citation-based pending-sweep therefore re-surfaces it every time, and a naive writer may re-ingest it as "new" — violating §12 and prohibition #7. Maintain `wiki/skipped.md` as the authoritative machine-readable ledger: one line per skipped raw file — `raw/<file>` — its cited fuller source of record, and the skip reason. **The pending list is: source/raw files that are NEITHER cited in any wiki content page NOR listed in `wiki/skipped.md`.** This is robust in both directions: it will not re-surface a logged skip, and it WILL surface a file that was staged but never processed (a crash-recovery hole). When a batch §12-skips a file, add it to `wiki/skipped.md` in the same commit. (Prefer the citation-or-ledger sweep over the bare "is it in raw/?" test: raw/-presence wrongly treats a staged-but-unprocessed file as handled.)
   - **Per-batch no-file-loss audit (vault ↔ raw ↔ log).** Before declaring a month done — and as a cheap standing check each batch — diff three sets: (a) every in-scope source file in the vault month folder; (b) every file staged into `raw/`; (c) every file recorded ingested/skipped in `log.md`. Every vault file must appear in raw/ (or be an explained out-of-scope exclusion) AND carry a log disposition (ingested / §12-skip / scope-flag). Any vault file absent from raw/ or from the log is a **staging hole** — stage and process it before moving to the next month. This closes the cherry-pick failure mode: holes cannot persist past a month boundary. Report the diff counts in the batch/lint log. **Make the vault↔raw leg reproducible:** each month-complete log entry must record the vault month-folder path, its file count, and the list (or a checksum of the sorted filename list), so an outside auditor — who can only see raw/ + log, not the vault — can reconstruct and re-check the diff post-hoc. A bare "68/68 complete" assertion is not auditable; the manifest is. (If a month was completed before this rule existed, backfill its manifest retroactively so the ENTIRE backlog — not just recent months — is reconstructable from raw/+log.)
2. Apply de-dup / conversion (Section 12) if needed.
3. Write a `## [date] ingest | batch N started` line to `log.md`. **Before writing any pages, run `qmd update` unconditionally** (no freshness check first — just run it). A stale index makes search-before-create miss existing pages and silently create duplicates; running it every time is cheap and removes the judgment call.
4. Read the batch (process **oldest source date first** — chronological, from 2025-01-01 forward). **Month-folder order ≠ chronological order (learned batches 16–23):** vault month folders demonstrably contain files whose *content* dates to a different month or even a pre-2025 year (export/re-file artifacts). So do a **cheap content-date pre-scan at staging** — glance at each staged file's internal date/header and flag any that are pre-window or clearly mis-filed *before* the writer runs, so History back-fill and scope handling are anticipated, not discovered mid-write. Back-filling earlier content into existing pages' `## History` is the EXPECTED norm here, not an exception (see §11).
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

**Recovering an interrupted batch** (a batch with a `started` but no `completed` log entry). **Assess what's on disk first, then choose one of two paths** — do NOT default to a hard reset:

- **Path A — assess & finish (preferred when the write is complete).** The writer subagent often finishes writing all pages, then the run dies later (e.g. an API/spend-limit error during its own self-check, a killed process). In that case the content is already on disk and re-running would only duplicate it. **Audit the on-disk output:** (1) every raw file in the batch is cited by ≥1 wiki page; (2) no partial/truncated/half-written pages; (3) no duplicate pages or duplicate `index.md` lines; (4) index = pages on disk. If it passes, **finish the batch normally** — run step 7 verification, do the dup/dangling audit, write the `completed` + `verify` log entries **noting the interruption and that the caller verified the completed output**, then commit. (This is the Batch 12 recovery.)
- **Path B — reset & re-run (only when the write is partial or unauditable).** If pages are half-applied, truncated, or you cannot confirm the audit above, **`git reset --hard` to the commit immediately *before* that batch's `started` entry** — i.e. the last commit before the batch began, which may itself be a `lint`, `schema`, or `query` commit, not necessarily the previous ingest batch. This discards only the half-applied batch while preserving legitimate non-ingest commits that landed after the last batch. Then re-run from the batch's file list. (This is the only sanctioned hard reset — it only ever discards an unfinished batch. Confirm the target with `git log --oneline` and verify `raw/` is unchanged after the reset.)

- **Verifier independence:** at least half of the verified facts must be drawn by the verifier directly from the written pages at random — not from the writer's own spot-check list (the writer must not choose everything that gets checked).
- **Registry-change sweep:** whenever the §4 same-name registry changes (new member, rename, owner ruling), the SAME pass must update the `disambiguation:` frontmatter on EVERY page in that cluster to the **same canonical membership block** — one verbatim string listing all cluster members (name + wikilink + one-word role), reused identically on every member page — so lint can diff them mechanically and catch silent count/member drift. Bespoke per-page prose that merely "distinguishes the others" is NOT sufficient (it drifts as the cluster grows); the shared block is mandatory, and a page may add page-specific prose after it.
- **Provisional (not-yet-owner-ruled) clusters get a shared block too.** A same-name pair/set that is *queued* for an owner ruling (e.g. the two Irinas — Makarych vs Shishko — whose split is strained) must still carry ONE shared **provisional** membership block (marked "provisional — owner ruling pending") reused byte-identical across its member pages, so the §13 mechanical diff can check it. Otherwise drift hides exactly in the queued clusters. When the owner rules, the block loses "provisional."
- **Sources-list hygiene:** a page's `## Sources` list must contain every raw file cited in its body (and `source-count` must match). Lint runs a mechanical body↔Sources diff.

## 9a. Commitments & open questions (lightweight capture)

Not a page type — a capture convention so commitments and open questions stay queryable without their own pages (revisit as a first-class type after the backlog if the rollup strains).

- **Capture in place, where it arises.** When a source produces a commitment, record it as a one-line entry on the page where it naturally belongs (the person who owes it, the decision, or the project) under a `## Open commitments` heading, in this exact shape:
  `- [ ] <who> — <committed to what> — due <when / "unspecified"> — [[raw/<file>.md]]`
  Mark it `- [x]` and move it to `## History` when a later source shows it discharged.
  - **`blocked-on-<X>` marker for un-actionable parked items.** When a commitment/direction-item can't progress until an external precondition is met — most commonly an unfilled role (the May-2025 "await the Miami product-manager hire" pattern parks Unity-vs-Miranda, the Jira restructure, Product-Discovery adoption) — tag it `- [ ] (blocked-on: Miami-PM-hire) …`. Lint's rollup **quarantines** `blocked-on-*` items into a separate overview list so they don't inflate the live open-count or false-trip the "monotonically growing queue = finding" rule. Un-quarantine when the precondition clears.
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

- **Two-tier Owner Decisions queue:** Tier A — rulings that steer future ingestion (identity/merge questions, scope calls, §15.8 holds) are surfaced to the owner opportunistically mid-run (next reply, not a stop). Tier B — cosmetic confirmations (dedup calls, dating notes, create-vs-mention) accumulate silently for the end-gate review. Items superseded by later sources are marked superseded in place, not re-asked.
- **Prune the queue at every lint pass (don't let it grow unbounded).** The queue must not balloon toward a thousand-item end-gate. At each lint pass, actively **close** Tier-B items a later source resolved, **mark superseded** ones, and **collapse** duplicates — so the standing queue reflects only genuinely-open items. Report the queue's live open-count in the lint log; a monotonically growing count is itself a finding.
- **Structure: a `## Owner Decisions` section with TWO clearly-separated parts** — (a) a **`### LIVE OPEN (count: N)`** subsection that is the single authoritative list of genuinely-open items, where a recurring item (e.g. the two-Irina strain) is a **single line updated in place**, never re-appended; and (b) the **per-batch journal** below it (the append-only record of what each batch queued). Do NOT let a recurring open item get re-stated near-verbatim across many batch entries as if new — it lives once in LIVE OPEN and is refreshed there. Lint rebuilds LIVE OPEN from scratch each pass.

## 10. Query workflow

1. Read `index.md`; use qmd search (Section 14) to find relevant pages.
2. Read the relevant pages; answer the owner **with citations**, in plain language.
3. **File answers back only when they add durable synthesis** — the answer combines **3+ sources** or captures a genuinely new connection. Do **not** file back answers that merely restate facts already retrievable from existing pages (those are negative value — they rot). When you do file one: **ask the owner first**, then create it as a new page with `type: synthesis` + an `index.md` entry + a `## [date] query | <title>` log entry. **No other page may cite a synthesis page as a source** — synthesis pages cite raw files, never the reverse.

## 11. Update semantics (temporal rule)

- We process **oldest → newest** (chronological), so newer facts naturally arrive later and update older ones. The rules below still hold if a batch is ever out of order. **In practice batches ARE routinely out of order** — month folders mix dates and pre-2025 files surface late — so treat earlier-dated back-fill (adding to `## History`, never overwriting current-state) as the normal path, not a special case.
- **Recording header / content date usually beats a "derived-notes" or processing stamp — BUT a divergent derived-notes date can also be a real second-session date.** When one meeting's artifacts carry different dates, the recording header is normally the meeting's date and a derived-notes stamp is normally a processing artifact. **Exception (owner-corrected, InComm Apr-3/Apr-7):** if the meeting could plausibly have **spanned more than one day** (a multi-session working meeting), the two dates may BOTH be genuine session dates. So do **not** auto-resolve a two-date meeting to the recording date — **queue it** (Tier A) as "possible multi-day meeting" and let the owner confirm; default to one stub, primary = earliest/recording date, later session(s) noted, facts attributed per session where distinguishable. (The Apr-3-vs-Apr-7 case was first auto-resolved to Apr-3 by the rule above, then the owner corrected it to a genuine two-day meeting — reasonable rule, wrong call. Lesson: a derived-notes date is not always just a stamp.)
- **Every fact carries an as-of date** (the source's own date).
- **Date precedence for undated/mis-dated files:** content-internal date (what the meeting says about itself) > audio-file metadata > transcription stamp > filename/folder date. Filename dates are often just export/staging dates. When the date is inferred, label it (`date inferred from …`) on the meeting page; when only a month/era is known, use a placeholder day and flag it.
- **Date-labeled origin paragraphs are permitted in page intros:** a clearly dated sentence like "the Nov-2024 origin of X was …" may sit in an intro for readability without moving to `## History`, provided it cannot be mistaken for current state. Undated old substance still goes under `## History`.
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
- **Corpus-wide cross-check (mandatory — never batch-local).** Every dedup / re-transcription / derived-family check MUST run against the **entire already-ingested corpus**, not just the files in the current batch. A later-staged file can duplicate a meeting ingested long ago (batches or months earlier) — an intra-batch jaccard/similarity pre-check will miss it and create a duplicate page (this happened: `development_review_2` in batch 61 was a re-transcription of `game_development-july-3` ingested in batch ~57; the batch-local pre-check passed it as "new"; only the writer's corpus-wide §12 check caught it). Before creating ANY meeting page, search the whole wiki (`qmd update` then grep/read; NEVER `qmd query`) and compare CONTENT against the closest already-cited source of record. Only conclude "new" after the corpus-wide check clears it. The staging-time pre-check is a convenience, never a substitute. *(Schema entry: owner directive 2026-07-20.)*
- **Re-transcription clusters (the common case in practice):** the same audio often exists as 2–3 separate transcription runs under different filenames. Compare CONTENT, not filenames. Source-of-record selection: the **fullest** copy wins (most words, speaker labels kept, no stuck repetition loops, unique details preserved); skip the rest with a one-line logged reason each. A file that contains **only a title line** is a stub → skip. A transcript that **internally duplicates its own content** (the same passage repeated) is one meeting — take each fact once and note the artifact on the meeting stub.
- **Derived-document families (distinct from same-audio re-transcriptions).** One meeting often yields a *family* of artifacts: the recording/transcript PLUS a derived summary, an action-items doc, and/or hand notes — sometimes stamped with different dates (see the InComm and SMIB cases). Treat the family as **one meeting**: one stub, cite the fullest primary source(s), date by the recording/content date (§11), and expect the derived docs' stamps to diverge from the true meeting date. Cross-check for family membership against ALREADY-INGESTED files, not just within the batch (a later-staged transcript may belong to a meeting already stubbed from its notes — enrich that stub, don't create a second).
- (Phase 0 already deduped/converted the existing backlog; this rule governs new arrivals.)

## 13. Lint / maintenance passes (mandatory)

- Run automatically **every 3–5 ingest batches**, and on demand.
- Check for: contradictions between pages, stale claims newer sources have superseded, orphan pages, important concepts lacking their own page, missing cross-references, duplicate person/entity pages, `index.md` vs page drift.
- **Orphan definition (precise):** an orphan is a **non-meeting content page with zero inbound links from any *substance* page** — `index.md`/catalog links do NOT count as inbound (index links everything, so it would nullify the check), and **meeting stubs are exempt** (they are catalogued by month, reached via the index by design). Only people/orgs/topics/projects/decisions with no substance-page inbound are orphans.
- **Disambiguation-block diff (mechanical, not self-asserted).** For every §4 same-name cluster, extract each member page's canonical membership block substring and assert they are **byte-identical**; report per-cluster as "Anton: 3 members / N distinct blocks" — N must equal 1 or it FAILS. Do NOT report "verbatim" without computing the equality (lint passes 7–8 self-certified this falsely; audit #4 caught Anton drift). A member page may carry a short page-specific role prefix before the shared block, but the shared block itself must match.
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
