---
type: decision
title: Standing instruction — use the standards, add to the standards, and point your Claude at the standards repository first (Knowledge Base / Standards in GitHub, access verified for all 39 accounts)
date: 2026-09-04
aliases: [point your code at the standards, standards repository instruction, Knowledge Base Standards folder, 39 accesses verified, write narrow granular standards, moving away from Confluence]
source-count: 4
status: active
open-commitments: 3
open-questions: 0
---

# Point your Claude at the standards repository first

Val gave the same standing instruction **twice on September 4 2026** — closing the [[wiki/meetings/2026-09-04-rage-nova-conversion-readiness.md|morning engineering meeting]] in Russian, and again as the deliberate closing statement of the [[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|afternoon game-development meeting]] in English. The two halves of the company got the same rule on the same day; the derived notes of each meeting flag the other as its counterpart [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]] [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]].

## The instruction

**To engineering (morning).** [[wiki/people/pavel.md|Pavel Frolov]] posted the link to the standards repository in the meeting chat, saying he did it so nobody could later claim not to know where the standards live: "я там сбросил, чтобы потом никто не говорил, что я не знаю, где у нас стандарты лежат. Вот пользуйтесь этой ссылкой." Val then closed the meeting with three sentences [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]:

> "Пожалуйста, пользуйтесь стандартом. Пожалуйста, дописывайте стандарты. И, пожалуйста, направляйте свой код как часть вашего рутин на то, чтобы он сначала смотрел стандарты."

— use the standards; add to the standards; and, as part of your routine, direct your code to read the standards first.

**To the game team (afternoon).** "I want to, in the final statement, to make a point that we have a repository which is called **Knowledge Base** in GitHub. Under Knowledge Base, there is a folder called **Standards**. This is where all standards go… when you use a clot [Claude] to do any function, please point your clot to the standards repository. Let it refer to it… And if you want to read manually, you're welcome to." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]

## What else was settled with it

- **Access is granted and was manually verified — all 39 accounts.** Pavel noted "Андрей должен был дать доступ всем на этот репозиторий"; Val confirmed it was done and checked person by person: "Он, он всем дал и проверил каждого аксессу. У каждого есть аксу и отписал, что у каждого есть аксу и он мануально сам всё это проверил **39 аксис**." Repeated in the afternoon: "If you don't have access, then you should, because it's open to everybody." [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]] [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]] *("Андрей" is not surnamed on the call; by context — GitHub access administration — this is [[wiki/people/andrey-bosik.md|Andrey Bosik]]. **Labelled as inference.**)*
- **The repository's contents include the taxonomy and the file naming convention.** "It includes the taxonomy, it includes the filing naming convention… whatever standards you're working with." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **How to write a standard: narrow, not broad; keep adding granular points.** "when you write standards, write… to a narrow point, don't make it a broad standard. So keep on adding narrow standards, narrow points." [[wiki/people/michael-gottlieb.md|Michael Gottlieb]] supplied the word — "Granular." — and Val took it: "Granular. Yeah, thank you very much. I appreciate it." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **Documents that already exist are moved into it rather than rewritten.** [[wiki/people/lena.md|Lena Zhukova]]: "we actually have this kind of documents for… now it's no[va], we we just need to move it… in in proper… repository." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- **JVL is steadily leaving Confluence.** "we're moving, as we switch to Nova, we will probably move away completely, but we're steadily moving away from Confluence." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]] This is the same direction tracked on [[wiki/topics/docs-as-code-and-atlassian-exit.md]], and it is why Val challenged Michael's suggestion of a Confluence page earlier in the same meeting — "Why does it have to be a confluence page?" (Michael: "It doesn't have to be… It can be anything you want it to be.")

## Naming note

The repository Val calls **"Knowledge Base"** here is the one [[wiki/people/pavel.md|Pavel]] corrected him about on [[wiki/decisions/2026-09-03-prose-standard-into-knowledge-repository.md|Sept 3]] — the repository is `knowledge`, with **standards as a folder inside it**, not a repository called "standards." The Sept-4 English wording ("a repository which is called Knowledge Base… under Knowledge Base, there is a folder called Standards") matches that corrected structure, and supersedes the loose "standards repository" phrasing carried on the [[wiki/decisions/2026-08-24-single-prose-writing-standard.md|Aug-24]] and [[wiki/decisions/2026-08-28-reverse-engineer-acceptance-criteria-and-automate-qa-dragon-pays.md|Aug-28]] pages.

## Why Val keeps pressing this

The morning meeting had already produced a live instance: Igor's new repository structure had been built without reference to the written standard, and Igor said he had not read it (see [[wiki/topics/github-release-management-pipeline.md]], Sept-4). The afternoon meeting produced the second instance — a naming convention held as a verbal agreement (see [[wiki/decisions/2026-09-04-asset-naming-convention-must-be-written-down.md]]). Val's own statement of the principle, given to the game team: "there has to be… a repository where all standards are written, and when there is a… file to be named. It cannot be named manually. It should probably be named through a reference by, you know, **Claude**. I would use that… that's how I name my files." [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]

## Open commitments

- [ ] Everyone (engineering and the game team) — use the standards, add narrow granular standards to them, and point Claude at the standards repository as part of routine work — ongoing standing rule — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]] [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — move the graphics team's existing Omni/NOVA naming documents into the Knowledge Base standards folder — due unspecified — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — read the repository standard and correct his repository structure to match — due unspecified; he said "я могу смог ознакомиться и поправить под стандарт" — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]

## Sources
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
