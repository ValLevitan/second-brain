---
type: topic
title: Docs-as-code and the plan to exit Atlassian
date: 2025-02-21
aliases: [docs as code, documentation site, GitHub Pages, GitHub Docs, mermaid, Confluence exit, Atlassian exit, single source of truth]
source-count: 2
open-questions: 1
---

# Docs-as-code and the plan to exit Atlassian

A workstream, driven by [[wiki/people/aaron.md|Aaron]] with [[wiki/people/val-levitan.md|Val]], to move JVL's documentation (and eventually issue tracking) out of Confluence/Jira and into Git, where the documents live alongside the code. Surfaced in the Feb 21 2025 LFS/GitHub session with [[wiki/people/lena.md|Lena]] and reinforced Feb 26. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## What docs-as-code means here

- Documentation is written as **Markdown files committed into the git repo**, right alongside the code. Markdown is a lightweight format between plain text and HTML; **WYSIWYG editors** exist (web or desktop) so non-technical writers get bold/headings/images without hand-writing markup. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- On every commit, a pipeline **auto-regenerates a full, self-contained documentation website** for that project and publishes it (GitHub Pages) — viewable in **one click** at a per-project URL (Aaron's example: `fortune-foo-pause.jvl.github.com`), always up to date with the source, with images rendered in place. This answers Lena's worry that Markdown would be inconvenient for Juan and Michael and would force a "pull the repo to read a doc" workflow. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- Aaron showed **GitHub Pages** (a rendering pipeline that turns repo content into a hosted docs site) and **GitHub Docs** as examples; he said there are "many different frameworks and we haven't chosen one yet." No specific third-party framework was named in the source. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Mermaid** text-syntax diagrams will most likely replace Confluence whiteboard diagrams: written as plain syntax in the markdown (not a proprietary binary), so many editors can produce them and they can be generated from — and inform — the game flow / source code. Confluence stays only as an informal "sandbox" for kicking ideas around. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- Longer term Aaron wants **docs generated from the game artifacts themselves**: e.g. a program shrinks the actual symbol graphics from the game into thumbnails placed in the docs tree (no LFS needed for the docs tree), so the documentation always matches the real game instead of being maintained separately. A Feb 26 example: an action that turns committed **Photoshop files into a contact-sheet of thumbnails** on the repo README. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]] [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]

## "The only source of truth is what's in git"

- Aaron's rule, which he said he would push to everyone: **the only source of truth is what is checked into a git repo**; everything else — Confluence, whiteboards, discussion — is just a "sandbox" / "sandcastle" until it is committed. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]] (This is the same principle Val applies to feature progress — see [[wiki/topics/ai-assisted-development.md]].)

## The Atlassian exit

- Aaron told the team that his and Val's goal is to **get rid of Atlassian products entirely**. Confluence is "a transitional tool" that helped organise their thoughts but they are "moving past it." [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- Asked what issue-tracking system would replace Jira, Aaron said **GitHub** (cards, boards, sprints all in GitHub). He stressed this is "a long way off — a year or two," not a near-term change, and framed it as consolidating for cost and effectiveness. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- **Migration plan for Fortune Foo Paws docs:** Aaron will pull the existing Fortune Foo Paws content out of Confluence into an initial GitHub docs site (a first "confluence import" branch — a raw export, to be refined), show Lena the formatting possibilities, then eventually **lock Confluence edits** for that game and move all doc contributions to GitHub. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Open questions

- The initial Confluence-to-Markdown export was **incomplete**: the symbol table (symbol names + export naming) that exists in Confluence did **not** port. Aaron said Confluence's export may be lossy and it must be reconciled. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Sources

- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
