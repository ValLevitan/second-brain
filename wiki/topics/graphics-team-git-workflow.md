---
type: topic
title: Graphics team Git workflow (PR discipline, CI tickets, deploy pipeline)
date: 2025-03-12
aliases: [designer git workflow, graphics PR discipline, pull request discipline, contact sheet action, assets deploy pipeline, fork from template, help desk CI tickets, performative pull request, pull request back to template, template per game type]
source-count: 13
---

# Graphics team Git workflow (PR discipline, CI tickets, deploy pipeline)

The working practices JVL's design team follows on GitHub, as coached by [[wiki/people/val-levitan.md|Val]] and [[wiki/people/aaron.md|Aaron]] on the Mar 12 2025 "GitHub for graphic design" check-in with [[wiki/people/andrey-bosik.md|Andrei Bosik]], [[wiki/people/lena.md|Lena]], [[wiki/people/yulia.md|Yulia]], [[wiki/people/anastasia.md|Anastasia]] and [[wiki/people/dmitriy-khandov.md|Dima Khandov]]. Builds on the earlier design-team decisions ([[wiki/decisions/2025-02-21-separate-game-and-design-repos.md]], [[wiki/decisions/2025-02-26-designer-branching-workflow.md]]) and the docs-as-code direction ([[wiki/topics/docs-as-code-and-atlassian-exit.md]]). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## The PSD-commit conflict complaint

- The team reported that committing new **PSD files** produces merge conflicts when two people open pull requests to `main` at nearly the same time (Andrei/Lena/Anastasia hit it). Andrei diagnosed the cause: the **auto-generated `index.md`** for the contact sheet contains a **"generated on" date/time line** that changes every run, so he proposed **deleting that line** to stop the conflicts. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- Aaron's framing: work on **separate feature branches** with separate files shouldn't truly conflict; the contact-sheet **Action just runs twice on `main`** after two merges, and if that breaks you fix the script rather than debug it live in a meeting with eight people. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Report tooling/CI problems as help-desk tickets, not in meetings

- Val/Aaron's rule: when the art team's tools or CI **Actions** break, they should open a **ticket in the help desk (`help.jvl.ca`)**, not save it for a meeting. The support team (Andrei's group, able to dispatch to **Anton**, **Sasha** or **Pavel**) then commits the fix connected to the pull request / commit — treating a broken contact-sheet feature as "just another feature." "Everybody is made the same" — support people make features and improvements in the same repos as everyone else. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## The assets → game deploy pipeline

- Artists commit to the **production source game assets** repo (with production manifests). A **GitHub Action automatically archives and deploys to the game repo** — producing a zip archive / "complete assets bundle artifact." A next step is meant to **trigger an Action in the game-mechanic-logic repo**, but **that step did not work yet** as of this meeting ("about that step we speak only today"). Game assets and game-mechanic logic are **separate repositories**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Pull-request discipline (Val's coaching)

- The assets repo had **one branch (`main`)** and **29 closed pull requests**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Reference the Jira ticket** in every PR (the test PR "UDE dev environment added for main FFP game" had none, because it was a test; all future ones will). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Assign the PR** (an assignee, not just reviewers). [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **No giant PRs:** Julia had **approved a ~940-file PR** ("did you really review 940 files in an hour?") — it was **Dima's Miranda catch-up** commit, a legitimate special case (technical debt), but a PR should never have ~1,000 files unless it is that kind of special catch-up. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- **Make PRs "performative":** Val's lesson — write descriptive commentary explaining your **intention** so people **outside** the tight team can understand what happened; a PR is "stop, review this, acknowledge its existence, commit" — not a wink or a note slid across the hallway. "A year from now… you'll thank yourself." [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## When to create a repo for a new game — "fake the review"

- [[wiki/people/lena.md|Lena]] asked at what stage to create a repo for a new game (e.g. **Cache Kittens**), since Michael, Juan and Yefim aren't on Git yet and early design still happens in **Zephyr** — so no one could approve her commits. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- Answer (Aaron/Val): **start the repo now and "fake the review"** — give **Julia/Anastasia or Dima Khandov** access to approve. Practice what you preach; build incremental successes and enroll the others later. Val isn't ready to bring Michael/Juan/Yefim onto Git yet. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Generic template + fork workflow

- Lena has a **Fortune Fupa (FFP)-specific** template; Andrei is to build a **generic base template** repo. New games are created by **forking (not cloning)** from the generic template so designers can't accidentally push back to it. Andrei had **disabled** fork-from-template "for security reasons"; Val overrode this (his "paper door lock" analogy — a fork is no less secure than a clone for copying to public space) and Andrei **enabled fork-from-template for all repos**. Captured as [[wiki/decisions/2025-03-12-fork-game-repos-from-generic-template.md]]. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Side note — current design workload

- The team is **not full-time on Fortune 4 (FFP)** this period; **Heat Game 6** and **Georgia** are the urgent side projects, and **Natasha** is continuing Georgia while Lena returns to FFP. The next check-in was set for the **26th** (Wednesday, two weeks out); Val books these meetings for **30 minutes or less**. [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]

## Template repo check-in (Mar 26 2025)

A follow-up "GitHub commits" check-in where [[wiki/people/andrey-bosik.md|Andrei]] demoed the working **template repository** (with [[wiki/people/val-levitan.md|Val]], [[wiki/people/lena.md|Lena]], [[wiki/people/dmitri-kovalchuk.md|Dima Kovalchuk]], and an "Igor" whose identity is unresolved — see Owner Decisions). [[raw/github_commits-march-26-2025.md]]

- The template can be **instanced with one button** into a new repo (a variable/repo with a single initial commit, all pre-structured) and carries **predefined GitHub Actions** for contact sheets, sprites, and **migrating/updating pull requests**. Val's forward idea: on instancing, an Action does **word-replacement across the docs** so a new project's README/files are auto-named. [[raw/github_commits-march-26-2025.md]]
- **Close the loop back to the template (Val's main point):** there was **no process to return improvements to the parent template**. Val pushed hard on the *culture*: when a game produces something worth keeping, feed it back into the template **via a pull request** ("I request you to pull my good changes into your thing"), so the template doesn't go stale — you'd **fork** the template, incorporate changes from the working repo, and PR them back. Use Git terms, not "I'll just edit it by hand." [[raw/github_commits-march-26-2025.md]]
- **Signals it's time to update the template** (Val's coaching, with Lena): a **new reusable script** useful across all games; or finding yourself **repeatedly adding the same things** after cloning each new project. [[raw/github_commits-march-26-2025.md]]
- **Templates per game type (Lena):** the current base template just holds shared structure; in future JVL will have separate templates for **Georgia / Omnia framework games**, **Persistence games**, and **classical games**, each with a more appropriate structure per game mechanic. [[raw/github_commits-march-26-2025.md]]
- **Follow-up:** GitHub-commits check-in set for **April 9, 9:30am Eastern** (later merged with the MCP test — see [[wiki/meetings/2025-03-26-mcp-unity-visualcode.md]]). [[raw/github_commits-march-26-2025.md]]

## Moving art-asset evolution out of Jira into GitHub (stated Mar 26)

In the Val–Gottlieb one-on-one (same day as the template check-in above), Val stated the review flow itself is changing: "as of this moment, we already experimenting with **not putting it into Jira**, because Jira has multiple reiterations. We want to have only one asset… and an account of this evolution" — moved into **GitHub**, where each person works in a local **sandbox** and pushes when ready, so reviewers see the final with a **"differential evolution"** (rollback shows what changed — "purple was changed to green"). Val's claims for it: educational replay for young designers ("these are the errors that you're making"), and instant **scale-up/scale-down** of outside hires with no learning curve. He added that Jira/GitHub can now be driven by a **human-language interface** ("we don't even need to know GitHub") and predicted JVL can eventually "push away from Jira." Gottlieb noted the team had put everything **into** Jira under Val's own earlier direction — recorded as evolution of that instruction, not a contradiction. See [[wiki/meetings/2025-03-26-gottlieb-val-one-on-one.md]]. [[raw/michael_gottlieb_val_meeting-26-2025.md]]

## Designer asset validation — the "resource validation tool" (Mar 24 2025, date inferred)

On the DevOps-container session ([[wiki/meetings/2025-03-24-devops-container-approach-omni.md]]), the designer flow was re-drawn for the Omni era — artist exports a scene, inserts it into the game repo with a JVL tool, validates **locally**, commits to a short-lived feature branch, CI/CD builds and deploys for a browser check: [[raw/devops_container_approach_for_omni.md]]

- The proposed "**JVL Resource Management**" tool was cut down by Val to a "**resource validation tool**" — a yes/no validator ("да-нет, да-нет") the designer runs on their own machine (catching, e.g., a missing balance field that would crash the game) instead of waiting for a pipeline email; it can start as a command-line tool. [[raw/devops_container_approach_for_omni.md]]
- [[wiki/people/alexander-biratka.md|Alexander]] already built a **browser previewer** on OmniFramework ("создано как отдельная игра, просто она работает как превьюшка") — view/scale/toggle an exported scene; already pushed to a repository. Visual preview also catches Unity→Pixi exporter breakage that structural validation misses ("структурная сцена правильная, но визуально… она сломана"). [[raw/devops_container_approach_for_omni.md]]
- Gaps named: **sounds are never validated** today (check IDs, maybe lengths); land-based updates also require **XML config edits** — "то, чем сейчас Ира занимается, Макарыч" ([[wiki/people/irina-makarych.md|Irina Makarych]]) — with no written spec of the file organization. Val's fix: reverse-engineer the most advanced game into "atomic binary requirements" the validator enforces. [[raw/devops_container_approach_for_omni.md]]
- Whether merges of designer assets need formal **approval by Lena or Michael** (vs review) was debated and left unresolved — Aaron: require it and "they will freak out… it's too much responsibility and it will halt our creative process"; don't, and "they'll do whatever they want." [[raw/devops_container_approach_for_omni.md]]

## History — the Feb 7 origin of the problem

Before any of the above existed, Val framed the need on the Feb 7 homework session: "I don't understand how to guide our graphic designers. I need to tell them okay look put your art in here… none of them is capable of doing it and trying to engage them… is the exercise of futility… we just need to tell them that just put your stuff in here… so in order to tell them put your stuff in here we have to create those repositories." See [[wiki/meetings/2025-02-07-github-homework-and-bitbucket-transfer.md]]. [[raw/GitHub repository structure.md]]

## Apr 28 2025 — Miranda commit hygiene (a graphics-team Git lesson)

The Apr-28 Miranda GitHub review ([[wiki/meetings/2025-04-28-miranda-github-versioning.md]]) surfaced the graphics side's weak Git discipline: [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] had dumped a single **"V8" commit of ~12,000 files**, left stale branches open for two months, and committed straight to `main` — the opposite of the continuous-commit / clean-release discipline this page describes. Fix: **versions as Git release tags** (not Jira), and coaching toward continuous commits. Detail on [[wiki/topics/miranda-authoring-tool.md]]. [[raw/miranda_github-apr-28-2025.md]]

## May 1 2025 — the Miranda clean-up action list (a repo-hygiene lesson)

Extending the Apr-28 review, [[wiki/people/aaron.md|Aaron]]'s May-1 recap with Val ([[wiki/meetings/2025-05-01-organizing-miranda-github.md]]) set [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] a concrete repo-hygiene action list for the **Miranda** repo — the same discipline this page describes: add a **`.gitignore`**, **purge logs/libraries** from the repo, **delete stale branches**, and adopt a **packaging strategy** (zip libraries on commit of a new version), before opening a feature branch for the emulator integration. Detail on [[wiki/topics/miranda-authoring-tool.md]]. [[raw/organizing_miranda_github-may-1-2025.md]]

## May 6 2025 — Miranda repo cleanup executed (packaging, rebase, PR discipline)

The follow-through Miranda session ([[wiki/meetings/2025-05-06-miranda-github-organization.md]]) is another graphics-team Git lesson: [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]] had done the May-1 cleanup (reworked repo, `.gitignore`, V8.1 release, drag-and-drop Unity package), and [[wiki/people/aaron.md|Aaron]] coached the next practices — distribute a **package** (NuGet/MSI) not the source tarball (talk to [[wiki/people/andrey-bosik.md|Andre]] + [[wiki/people/dmitri-kovalchuk.md|Dima K]]); never commit the ~2GB engine (reference it); a README "TLDR" (three-step install first, extended steps one level below, then technical + contribution docs); **more verbose pull requests**; **delete the merged branch**; have **Sasha review** PRs; and **rebase / fresh-start** the repo (with Andre) because the cleanup PR baked **~782k removed lines across ~5,000 files** into history. Detail on [[wiki/topics/miranda-authoring-tool.md]]. [[raw/miranda_organization_github-may-6-2025.md]]

## May 19 2025 — main-only vs Dev branch debate (Omni dev team)

A [[wiki/people/val-levitan.md|Val]] ↔ [[wiki/people/pavel.md|Pavel]] schedule/branch review ([[wiki/meetings/2025-05-19-github-branch-structure-debate.md]]; Russian; an "Igor" also present asking process questions) that turned into a git-workflow argument — the Omni-dev-team counterpart to the graphics-team PR discipline above. (Val runs these every ~2 days, ≤30 min; format: open Jira Plans, walk features, name task numbers, keep a minimal feature branch and confirm each has a GitHub repo where code is deposited.) [[raw/github_branch_structure-may-19-2025.md]]

- **State on GitHub:** each branch is named for its feature/story; **5 pull requests already closed** — the team has started working PR-per-feature as agreed. Integration tests aren't in the flow yet (they're behind). Several finished branches are being **held open** (Pavel wants to keep them for tests-to-be-written). [[raw/github_branch_structure-may-19-2025.md]]
- **The dispute — one main branch vs main + Dev.** Pavel's team merges everything into **Dev**, promoting to `main` only for a release version (main = tested/released "gold"). Val argues a small company should have **`main` only** — a Dev branch loses traceability of who did what / what's releasable, and pushes fixes into "**tribal knowledge**." Val: "imagine Dev is main for you" — the only difference is Dev holds untested changes, which is exactly what he objects to. Pavel: with no releases yet, Dev is justified for now; they'll drop it once there are many releases. Left **unresolved** ("we'll come back to this more than once"), Dev kept for the moment. [[raw/github_branch_structure-may-19-2025.md]]
- **Feature granularity is the real fix (Val).** JVL's error is defining a **feature as something big and permanent** — features should be **narrower, measurable, less complete**, with dynamic growth (reopen a closed feature branch or open a new one to extend). A **capability** is the stable, long-lived thing that defines the product; a product ≈ ~9 capabilities, each with many small features. Stories matter less; devote attention to small features, and only define features foreseeable in the next month or two. (Example: **VDEC** is a *capability* of the machine — video vs mechanical-button VDEC — not one giant feature; today "VDEC" has been in progress ~a month because it was scoped as one big feature.) [[raw/github_branch_structure-may-19-2025.md]]
- **Every merge to main = a version.** Reaffirmed in the same series: when a tested feature lands in `main`, bump the release version. [[raw/github_branch_structure-may-19-2025.md]]
- Val is deliberately **not breaking the current setup before the first Omni release** ("what's built today is much better than two years ago, but still not right"). The QA-department leverage side of this debate (pressure QA to write tests into `main`) is on [[wiki/topics/test-automation-strategy.md]]. [[raw/github_branch_structure-may-19-2025.md]]

## June 3 2025 — the designer moves into Core Development; commit-per-change and the "no signals" rule

An Omni feature-branch redistribution review ([[wiki/meetings/2025-06-03-omni-feature-branch-redistribution.md]]) is the graphics-team Git counterpart to the Omni-dev workflow — it resolves how designer [[wiki/people/dmitriy-khandov.md|Dmitriy Khandov]]'s exported artifacts flow into a testable branch. Full schedule/feature detail on [[wiki/topics/omni-core-advancement-and-game-templating.md]]; the workflow lesson: [[raw/Omni_redistribution_feature_branches-june-3-2025.md]]

- **A design-only feature-branch is untestable → fold the designer into Core Dev.** Because feature **AA4807** held only Dima's resources (nothing to test against), [[wiki/people/val-levitan.md|Val]] ruled to destroy it and move the stories under [[wiki/people/alexander-biratka.md|Sasha]]'s testable code feature — "practically we took Dima as a graphic designer and moved him into the Core-Development team," reporting under Sasha. This enacts the standing plan (Mar-24/Apr-17) to move Dima Khandov from design to core technology. [[raw/Omni_redistribution_feature_branches-june-3-2025.md]]
- **Commit for everything; stop the side-channel hand-offs.** Val's coaching restated the PR/commit discipline this page tracks: **make a commit for every piece of work you do**, and — pointedly to Dima — **stop coordinating through "signals, blinks, biotoks, sign-language"** between people; put the work in the **feature-branch** where the whole department (who treat Dima as the standard) can see it and learn the same practice. [[raw/Omni_redistribution_feature_branches-june-3-2025.md]]

## Nov 20 2025 — refine Git for artists, don't roll back; reduce the interaction surface

On the [[wiki/meetings/2025-11-20-github-for-graphic-design-team-git-lfs.md|Nov-20 "GitHub for graphic design team" session]] ([[wiki/people/val-levitan.md|Val]], [[wiki/people/aaron.md|Aaron]], the design generalist [[wiki/people/sergey-kleimenychev.md|Sergey Kleimenychev]], and [[wiki/people/andrey-bosik.md|Andrei Bosik]]), Sergey — who had complained Git/LFS is a poor fit for artists — conceded the **decision won't be rolled back** (GitHub was chosen for the company, not the designers; "learn the tool or cannot work for JVL," per Val). The work agreed is to **refine usage**: [[raw/application of GitHub for graphic design team.md]]

- **Reduce the artist interaction surface** — clone/pull/push at a button press via onboarding scripts + aliases so nobody hand-manages `git lfs install` (a miss leaves blob pointers, not blobs); document the **stash + LFS** pitfall. [[raw/application of GitHub for graphic design team.md]]
- **Squash merges** to keep history tidy and let old big blobs be pruned (daily renders ~1 GB/person/day); Sergey noted LFS only pulls the current commit (his original worry that a pull fetches every blob was wrong). [[raw/application of GitHub for graphic design team.md]]
- **Aaron's tooling + no-crutches line:** prefer **GitHub Desktop** over VS Code for artists; Andrei to add commit hooks/blocks and LFS-usage **monitoring dashboards** plus scheduled cleanup — but artists must still learn Git, not just lean on scripts ("do not let them be lazy"). [[raw/application of GitHub for graphic design team.md]]
- **Ownership:** Sergey took the simplified artist Git-flow as a "product" (with Andrei); Val bought no new tools — "setting up existing tools," and asked to be CC'd on the design work. Art committers number ~5. [[raw/application of GitHub for graphic design team.md]]

## Jun 1 2026 — how Lena runs the design/review loop with Michael Gottlieb

A short [[wiki/meetings/2026-06-01-lena-design-review-mcp-jira-workflow.md|Jun-1 ~2:49pm ET call]] ([[wiki/people/val-levitan.md|Val]] ↔ [[wiki/people/lena.md|Lena Zhukova]]) captured how Lena actually works with [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] day to day. (The MCP/Jira-tooling asks from the same call are on [[wiki/topics/ai-assisted-development.md]], June-1.) [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]

- **No set meeting with Michael — text and screenshots.** They exchange text or call as needed. Michael sends **review comments in Teams as text plus screenshots**, often circling the areas he dislikes, because written comments are clearer than verbal ones. [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]
- **Lena sorts and routes his comments.** She splits Michael's comments — developer comments go to the developers, art comments to the responsible team member. When he asks for something that can't fit the current release, she clarifies the technical details and **pushes to defer it to the next release**. [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]
- **Who changes issue status.** Whoever an issue is assigned to moves it from Action Item → In Progress when they start; Lena, Julia and Anastasiya do the later status changes by hand. The exception is Michael — he **never changes statuses**, so Lena closes and updates issues on his behalf. [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]
- **Recording practice.** Major issues are discussed by Lena, Anastasiya, Julia and Dima. Calls with other members (Natalia, Arturo, Vitaliy) are occasional and **not recorded** — usually short clarifications, since stories are written to be clear enough on their own. §15.8 clear — workflow only; no named-person compensation. [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]

## Jun 10 2026 — the design team's new Jira hierarchy (Capability/Feature/Story), and staying on SVN for now

On the [[wiki/meetings/2026-06-10-mcp-jira-design-workflow.md|Jun-10 ~2:01pm ET session]] ([[wiki/people/clayton-chancey.md|Clayton Chancey]] (Precipia, external), [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/val-levitan.md|Val]]) Val laid out where the design group's Jira model is heading, and Lena confirmed the design team's source-control status. The MCP/AI-tooling asks from the same call are on [[wiki/topics/ai-assisted-development.md]] (Jun-10). [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]

- **Capability → Feature → Story, with Capabilities linked to many Requirements.** Val is moving the design group to a **Capability, Feature, Story** hierarchy; a **capability is "done" when its set of features is delivered**, and a capability becomes a **layer of the Gantt chart**. Two Jira projects already exist — **Requirements (REQ)** and **Capabilities (CAP)** — while features and stories stay the same. Val drew the parallel to dev work: a **feature becomes a feature branch / deliverable artifact** in GitHub, and the design group is building the **same model** (a feature is a set of artifacts, with **ADRs and a data contract per repo**). [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]
- **"Feature" now collides in meaning — accepted as normal Agile complexity.** Everyone acknowledged **"feature"** now means three things (a dev branch vs a design deliverable vs a PM tracking unit) but consciously **left it unresolved**, accepting the overlap as normal Agile complexity. [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]
- **Design team stays on SVN for several more months.** Lena noted that even after the hierarchy change, the **design team keeps working in SVN (not GitHub)** for several more months. Changing the hierarchy is the **management foundation**, not immediate GitHub adoption. [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]
- **A tagging convention is still to be defined.** Val is to meet the game design team to define the tagging convention (**tag = "game design" + game name**) for capabilities/requirements before tags can be applied; a visual representation of requirements/capabilities (an Atlassian "spider web" / Big-Picture-style add-on view) was noted as currently missing. §15.8 clear — Jira/design-tooling workflow only; no named-person compensation. [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]

## Sources

- [[raw/Meeting_Notes_Clayton_MCP_Jira_Workflow-June-1-2026.md]]
- [[raw/GitHub repository structure.md]]
- [[raw/GitHub_for_Graphic_Design_evolution_2025-03-12.md]]
- [[raw/github_commits-march-26-2025.md]]
- [[raw/michael_gottlieb_val_meeting-26-2025.md]]
- [[raw/devops_container_approach_for_omni.md]]
- [[raw/miranda_github-apr-28-2025.md]]
- [[raw/organizing_miranda_github-may-1-2025.md]]
- [[raw/miranda_organization_github-may-6-2025.md]]
- [[raw/github_branch_structure-may-19-2025.md]]
- [[raw/Omni_redistribution_feature_branches-june-3-2025.md]]
- [[raw/application of GitHub for graphic design team.md]]
- [[raw/Meeting_Notes_MCP_Jira_Design_Workflow-June-10-2026.md]]
