---
type: topic
title: Docs-as-code and the plan to exit Atlassian
date: 2025-02-21
aliases: [docs as code, documentation site, GitHub Pages, GitHub Docs, mermaid, Confluence exit, Atlassian exit, single source of truth, template repo, contact sheet, GDD]
source-count: 3
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

## Docs into the repo + template repo (Feb 28)

The Feb 28 Git check-in put these principles into practice on the **Fortune Foo Paws** repo. [[raw/Git_progress_check_in_2025-02-28.md]]

- **General repo-usage instructions go into the repo now, not Confluence.** The designers had drafted general "how to pull/push/resolve conflicts" rules in Confluence and hesitated to put them in the game-specific repo. Aaron's rule: **"general instructions are better than no instructions at all"** — put them into the repo (a Markdown file in the README or the `docs` folder), because a file-structure/rules diagram kept only in Confluence "will be lost forever." [[raw/Git_progress_check_in_2025-02-28.md]]
- **Clone the game repo as a template.** JVL will use the Fortune Foo Paws repo as the base for future game repos — mature it, clean it out, rename it as a **template**, keep it as a template, and clone it for each new game. [[raw/Git_progress_check_in_2025-02-28.md]]
- **Hold the GDD for now.** The **Game Design Document** is not committed yet — [[wiki/people/efim-podvoiski.md|Efim]] and [[wiki/people/michael-game-producer.md|Michael]] are still writing it together (in Confluence, work in progress, images inserted); Val agreed to wait before moving it into the repo. Aaron also wants the eventual docs to **isolate the automated document generation from the human-written documentation**. [[raw/Git_progress_check_in_2025-02-28.md]]
- **The commit-to-main lesson.** A live gitignore **merge conflict** arose because designers had committed directly to `main` (adding Blender `blend1` temp files + logs), which broke Aaron's open pull request. He walked them through resolving it in the GitHub UI, and drew the lesson: **don't blindly commit to `main`** — pending pull requests must be merged in the right order, and the **repo owner merges the PR** (a contributor requests, the owner pulls it in). [[raw/Git_progress_check_in_2025-02-28.md]]
- **Contact-sheet automation.** [[wiki/people/andrei.md|Andre]] fixed the GitHub Action in the repo's `.github` folder (the Photoshop→contact-sheet automation) and is to set up Git-access credentials for it and modify its YAML so it can commit; the Wednesday-9am demo target is to commit a Photoshop file and see it added to the contact sheet. Aaron noted [[wiki/people/aaron.md|Aaron]] himself should be used as a **consultant, not an employee**. [[raw/Git_progress_check_in_2025-02-28.md]]

## Open questions

- The initial Confluence-to-Markdown export was **incomplete**: the symbol table (symbol names + export naming) that exists in Confluence did **not** port. Aaron said Confluence's export may be lossy and it must be reconciled. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Sources

- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
