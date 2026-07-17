---
type: meeting
title: Aaron AI session — PDFX report-ingestion tool and SurfSense (2025-05-15)
date: 2025-05-15
aliases: [PDFX, SurfSense, PDF access, ai aaron may 15]
source-count: 3
---

# Aaron AI session — PDFX report-ingestion tool and SurfSense (2025-05-15)

Three short recorded segments (2:56 / 9:47 / 4:31, transcribed 2025-05-19) of one working session between [[wiki/people/aaron.md|Aaron]] and [[wiki/people/val-levitan.md|Val]] in which Aaron shows the **actually-built** PDF-to-graph-memory tool (**PDFX** / "PDF access") that turns a sectioned PDF into structured per-page content for insertion into the terms / memory-graph database — the working continuation of the May-14 dictated method. Aaron also flagged an open-source local tool called **SurfSense**. Substance and the full pipeline live on [[wiki/topics/transcript-knowledge-base-tooling.md]].

- Aaron will "wrap up the memory graph generator for PDF documents" so each PDF becomes a queryable "sphere of information," because current models "don't have enough context length" to consume a whole report at once. [[raw/ai_aaron-may-15-2025.md]]
- Demo of the **PDFX** output on four yearly by-state gaming-report PDFs: a structured per-page index (each page described, grouped by state) plus extracted markdown text — an index of "exactly what's in the page," ready to feed the language model chapter-by-chapter for insertion into the memory graph. Only the token-spend/insertion step remained. [[raw/ai_aaron-may-15-2025 (1).md]]
- Hands-on terminal walkthrough: `cd` into the `docx` project (PDFX lives inside it), `source` the Python venv, then `PDFX process <path-to-pdf> <path-to-output>`. [[raw/ai_aaron-may-15-2025 (2).md]]

## Note on the three files (§12)

These three files are **not** duplicates of one another — they are **three distinct segments** of the same session (different durations, different transcription timestamps, and non-overlapping content). All three are cited as source of record. See the batch log for the dedup analysis.

## Sources

- [[raw/ai_aaron-may-15-2025.md]]
- [[raw/ai_aaron-may-15-2025 (1).md]]
- [[raw/ai_aaron-may-15-2025 (2).md]]
