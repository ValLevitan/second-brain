---
type: topic
title: Docs-as-code and the plan to exit Atlassian
date: 2025-02-21
aliases: [docs as code, documentation site, GitHub Pages, GitHub Docs, mermaid, Confluence exit, Atlassian exit, single source of truth, template repo, contact sheet, GDD]
source-count: 7
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
- **Hold the GDD for now.** The **Game Design Document** is not committed yet — [[wiki/people/efim-podvoiski.md|Efim]] and [[wiki/people/michael-gottlieb.md|Michael]] are still writing it together (in Confluence, work in progress, images inserted); Val agreed to wait before moving it into the repo. Aaron also wants the eventual docs to **isolate the automated document generation from the human-written documentation**. [[raw/Git_progress_check_in_2025-02-28.md]]
- **The commit-to-main lesson.** A live gitignore **merge conflict** arose because designers had committed directly to `main` (adding Blender `blend1` temp files + logs), which broke Aaron's open pull request. He walked them through resolving it in the GitHub UI, and drew the lesson: **don't blindly commit to `main`** — pending pull requests must be merged in the right order, and the **repo owner merges the PR** (a contributor requests, the owner pulls it in). [[raw/Git_progress_check_in_2025-02-28.md]]
- **Contact-sheet automation.** [[wiki/people/andrey-bosik.md|Andre]] fixed the GitHub Action in the repo's `.github` folder (the Photoshop→contact-sheet automation) and is to set up Git-access credentials for it and modify its YAML so it can commit; the Wednesday-9am demo target is to commit a Photoshop file and see it added to the contact sheet. Aaron noted [[wiki/people/aaron.md|Aaron]] himself should be used as a **consultant, not an employee**. [[raw/Git_progress_check_in_2025-02-28.md]]

## History — the origin debate, Bitbucket era (late Jan–early Feb 2025)

The doctrine above was first argued out weeks earlier, while JVL was still on Bitbucket ([[wiki/meetings/2025-02-01-docs-in-git-vs-confluence.md]]; day placeholder — dated by content to before the Feb 7–10 GitHub transfer): [[raw/the_importance_of_storing_artifacts_in_git.md]]

- **Learn Git in Git:** a practice repository was being set up ("Dimitri is setting up a repository for people to practice using Git"), and Aaron insisted its instructions live in Git itself — "We learn how to drive Git by operating in Git, not reading about it in Confluence or Word." [[raw/the_importance_of_storing_artifacts_in_git.md]]
- **Confluence = convenient throwaway; engineering docs pair with code:** Confluence "provide[s] convenience of interface," but a doc like Efim's *Jackpot Rush Georgia* math concept "is forever paired with the actual XML files and framework and game pieces" once committed — surviving Confluence refactors. Update flows work either **idea-centric** (edit docs → edit code → commit both in one PR) or **code-centric** (edit code → update docs → same PR). [[raw/the_importance_of_storing_artifacts_in_git.md]]
- **Val's resistance:** "at least 50% of our company… are Confluence comfortable and Bitbucket uncomfortable"; people won't voluntarily deposit into the repo; JVL lacks the "**culture of courtesy**" Aaron's model assumes ("we're not courteous to each other. Even with… how we say good morning") — "I don't know if you could force non-courteous people to have a courteous repository." [[raw/the_importance_of_storing_artifacts_in_git.md]]
- **What converted Val — the QA hook:** "Actually, I think you just convinced me, because I understood what the hook is. It's the QA" — a QA engineer testing from the docs beside the code (plus the pull-request reviewer) is the enforcement mechanism that keeps docs current. [[raw/the_importance_of_storing_artifacts_in_git.md]]
- **The live branch-discipline lesson:** "Dimitri" had committed **LFS documentation as .docx straight to main** that morning; Aaron used it to teach the flow — commit to a development branch, PR to main, reviewer flags format ("this has to be in markdown format, not doc format," fixable via pull-request commentary rather than a meeting). [[raw/the_importance_of_storing_artifacts_in_git.md]]

## The canonical repo tree — "lux standard" and the template repo (Apr 9 & 11 2025)

Two April sessions turned the docs-as-code principle into a concrete, mandated repository tree.

**Apr 9 — Val's case for a standard ([[wiki/meetings/2025-04-09-github-master-tree-structure-philosophy.md]]).** Val argued to [[wiki/people/andrey-bosik.md|Andrei Bosik]] and [[wiki/people/pavel.md|Pavel]] that JVL's repos (many carried over from SVN with no thought to structure) should follow one canonical tree he called a "**стандарт люкс**" (lux standard) that "автоматически… открывал бы это дерево" the same way on every repo — with a README maintained per directory. He said he learns best practice from **Anthropic's Claude 3.7 Sonnet** ("более человеческим голосом объясняет") and from **Cline recursive-memory** sessions (his "Home Renovation" folder analogy — a README + a Cline recursive-memory file let an agent re-orient in 3 minutes). Andrei's caution: a README can go stale, so a **GitHub Action that scans the directory and updates the README** would be needed to keep it "objective." Val's ruling: build a template with mandated master directories, each carrying its own README saying what belongs there; empty subdirectories need a placeholder file because **GitHub won't push an empty directory**. [[raw/github_master_tree_structure-april-9-2025.md]]

**Apr 11 — the template tree worked out ([[wiki/meetings/2025-04-11-github-repo-template-tree.md]]).** Andrei built an actual **GitHub template repository** ("use this template" button) and the group (Val, Pavel, Andrei Bosik, [[wiki/people/irina-makarych.md|Irina]], "Yuri") edited its tree live — a universal *developer* template, with **graphics repos to get a separate template** (they lack sources etc.). Rulings: [[raw/github_repo_structure-april-11-2025.md]]

- **`docs/` holds `diagrams` + `guides`** — "instructions" was dropped (Pavel: developers would confuse diagram vs instruction) and folded into `guides` (renamed from a `developer guide`); a speculative `product design` folder was **removed** to avoid two places for the same document. Diagrams = Mermaid or images (block/flow/functional-product diagrams). [[raw/github_repo_structure-april-11-2025.md]]
- **README vs index.md** — top-level **README** (rendered by default) links to a `docs/index.md` that lists the docs-folder contents; a lower-level README is optional (added only when the top README grows too long). **`install.md`** is a step-by-step build/run guide living in `guides`, linked from the top README, and belongs "on the same level as the documents" (one per repo, or one per platform for multi-platform). [[raw/github_repo_structure-april-11-2025.md]]
- **Top level:** `manifest` (kept at top level, not in docs), `build/` (build scripts only — "build" = compile to a jar; using the artifact happens in GitHub Actions), `src/` (with its own README; run-time/target-platform **scripts moved into `src`**, not the top level or `tools`), `resources` (kept; **`externals` removed** — resources can hold external libs), `tools` (binaries used to build/convert), `common` (kept over "core"/"native"), `config`. **`assets` and `artifacts` removed** from the dev template (assets belong to the separate graphics template; artifacts get created at build time). Empty dirs use a **GitKeep**-style placeholder ("болванка"). [[raw/github_repo_structure-april-11-2025.md]]

## Confluence whiteboard as the current diagram home (~Mar 19 2025)

- By mid-March the interim state was: JVL **left Miro** ("мы же ушли от мира") and Val had emailed everyone that **"we are switching to Confluence"** — Confluence has a whiteboard — as the place for architecture diagrams, with **Mermaid** in active use for drawing (Chudinov drew his diagram in "Мермейн" — Mermaid — having been told "сейчас рисуют через Мермейн"). [[wiki/people/dmitri-chudinov.md|Dima Chudinov]] had saved his Miro exports but not yet transferred them; access reportedly requires Git accounts. (Consistent with the Feb rule that Confluence is transitional — this is the sandbox tier, while committed markdown remains the source of truth.) See [[wiki/meetings/2025-03-19-back-office-architecture-chudinov.md]]. [[raw/back_office_next_step_forward_dzima_chudinov.md]]

## Open questions

- The initial Confluence-to-Markdown export was **incomplete**: the symbol table (symbol names + export naming) that exists in Confluence did **not** port. Aaron said Confluence's export may be lossy and it must be reconciled. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Sources

- [[raw/the_importance_of_storing_artifacts_in_git.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/Evolution_of_Migration_to_GitHub_for_Graphic_designers_2025-02-26.md]]
- [[raw/Git_progress_check_in_2025-02-28.md]]
- [[raw/back_office_next_step_forward_dzima_chudinov.md]]
- [[raw/github_master_tree_structure-april-9-2025.md]]
- [[raw/github_repo_structure-april-11-2025.md]]
