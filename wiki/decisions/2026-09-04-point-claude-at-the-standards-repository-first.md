---
type: decision
title: Standing instruction — use the standards, add to the standards, and point your Claude at the standards repository first (Knowledge Base / Standards in GitHub, access verified for all 39 accounts)
date: 2026-09-04
aliases: [point your code at the standards, standards repository instruction, Knowledge Base Standards folder, 39 accesses verified, write narrow granular standards, moving away from Confluence]
source-count: 25
status: active
open-commitments: 7
open-questions: 1
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

## Update, Sept 22 2026 — a developer without access, and two results for one task

At the [[wiki/meetings/2026-09-22-daily-standup-capability-test-status-and-flexport-gui.md|Sept-22 Minsk stand-up]] (Russian), [[wiki/people/vladimir-samusenko.md|Vladimir Samusenko]] reported that the student developer Daniil "нет доступа к ноутджбэй с репозиторию" (garbled; read as the knowledge repository — **inference**), so "он не видел, не знал про стандарты, которые там есть". His Claude did not know the standards either. Two people did the same data-contract task in parallel and got "2 разных результата". [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]: "должно всех доступен быть… По дефолту"; Vladimir: "Еще раз проверится" [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]].

*This sits against the Sept-4 statement that access was checked for all 39 accounts. Daniil may have joined after that check; the source does not say. Recorded as an open question, not a contradiction.*

## Update, Sept 22 2026 (8:01 AM) — Val restates the rule, and names an owner for the texts

At the [[wiki/meetings/2026-09-22-transactional-mvp1-jira-cleanup-and-e2e-tests.md|Sept-22 MVP 1 call]], Klimovich asked for an English–Spanish text library that anyone responsible can edit. Val gave it an owner and tied it to this rule [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]:

- **Owner:** "Андрей Босик, я считаю, должен быть хозяином" — [[wiki/people/andrey-bosik.md|Andrey Bosik]].
- **The standard is hard and mandatory:** "абсолютно жёсткий стандарт", "Я бы это сделал как [мэндатори]", pointing at the standards repository ("Standerds… Rupo").
- **Everyone adds to it:** "если чего-то не дописано в стандарте… я настаиваю, чтобы стандарты постоянно дополнялись".
- **Small and single-purpose:** standards must be "симплистик" and each about one thing — "будет сотни и сотни… MD файлс… описывают… один стандарт", growing all the time.

How the texts themselves are stored (the Flex-Port's XML file, compiled at build) is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]] (Sept 22, 8:01 AM).

## Update, Sept 23 2026 — the file-naming standard, and "half your answers are in the standards"

At the [[wiki/meetings/2026-09-23-transactional-mvp1-requirements-cleanup-and-autotests.md|Sept-23 8:00 AM call]]:

- **Mock-up files get dates.** [[wiki/people/dmitri-chudinov.md|Chudinov]] asked Klimovich to put a date in the file names of each new mock-up, so Claude can compare versions. Pavel: "У нас у нас есть стандарт наименование файлов… И там и там как раз в конце есть эта дата" — "В репозитории сейчас я тебе сброшу ссылку". Klimovich: "Хорошо сделаю" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Tests.** When Khamin asked how autotests should be stored and structured, [[wiki/people/andrey-bosik.md|Bosik]]: "половина если не больше ответов на твой вопросы описаны уже в стандартах" [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].
- **Plain English for Claude.** Val told the team to instruct Claude to limit sentence count and write in "e sl. Типом английского языка" — see [[wiki/decisions/2026-09-23-open-requirements-are-settled-on-the-call-and-only-slow-ones-are-parked.md]] [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]].

## Update, Sept 24 2026 — the integration repository, ADRs in docs, and Bosik takes it on

On the [[wiki/meetings/2026-09-24-transactional-mvp1-flexport-money-loss-bugs-and-release-date.md|Sept-24 8:01 AM call]] (Russian) [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]:

- **Where the autotests live.** [[wiki/people/andrey-bosik.md|Bosik]]: "У нас есть интеграционный репозиторий, который как раз и создавался… для Того, чтобы внутри него находились скрипты и CI процесс, которые проверяют взаимодействие между устройствами." Irina: the tests span Flex-Port and Flex IQ, so they cannot go in either device's repository.
- **Repository = project code.** Val: "мы сказали, что у нас репозитории это равняется коду проекта." Bosik agreed a Jira project should then exist for the integration repository. Asked whether it does, Bosik — "Я не готов щас ответить" — and Pavel could not say either.
- **Point Claude at the standard.** Val to [[wiki/people/alexei-khamin.md|Khamin]]: "Вы… можете поинт свой клод на этот стандарт… Тогда он организует вам правильно репозиторий. Я вам очень советую посоветоваться с Андреем босиком".
- **ADRs go in docs.** Pavel: what he sees is "устаревший подход к [ADR;] по новому стандарту, наверное, [ADR] должен в докс лежать."
- **Bosik owns it.** Val: "Вы можете на себя взять этот, чтобы мне не нужно было чейса туда?" Bosik: "Да да да, я сделаю все это."

## Update, Sept 30 2026 (11:07 AM) — Efim is walked through the standards one-on-one

On the [[wiki/meetings/2026-09-30-repo-standards-walkthrough-with-efim.md|Sept-30 11:07 AM "REPO standards" call]] Val applied the rule to [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] in person. The transcript is mostly unreadable (Russian speech rendered as English, per the notes [[raw/Meeting_Notes_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]); what is readable is Val's "I pointed I pointed you to a repo standards", "standards, material", "it's for GitHub", and the subjects he ran through — "repository organ zone [organisation]… zero trust… data contract repository", "ADRs", "discussion", "Pull request pull request", "Claude Reviewer is to cache the pull request" (verb **unclear**; the notes read "checks"), "Local computer" — and, near the end, "it's a standard" and "I encourage you" [[raw/Meeting_Transcript_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]. No undertaking by Efim is readable, so none is recorded. *(The owner of the RGS / maths-engine codebase thus joins Metelski (Sept 4), Khamin (Sept 24) and the Minsk team in being pointed at the standards; whether Efim has read them, or has access, the source does not say.)*

## Update, Oct 2 2026 — Val's written message to put the repositories in order "касается всех"; the transactional repositories split between Chudinov and Tsymanov; no prose for archived repositories

At the [[wiki/meetings/2026-10-02-daily-standup-sas-log-collection-policy-and-new-arm-boards.md|Oct-2 Minsk stand-up]] (Russian) [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]:

- **Val's message.** [[wiki/people/alexander-biratka.md|Biratka]]: "[Вал] мне написал по репозиториям что надо ну. Привести в порядок там проза проза и всякое всякое там. Побыстрее." [[wiki/people/irina-shishko.md|Irina]]: "Это, в принципе, всех касается. Здесь написано [—] и порядок в репозитории навести это касательно всех." [[wiki/people/dmitri-kovalchuk.md|Kovalchuk]]: "Да, это [Вал] всем написал." The message itself is not in the corpus; its content is known only from these words. [[wiki/people/alexei-khamin.md|Khamin]]'s weekend plan — "Я буду надо привести [репозиторий в] порядок" — follows it. [[wiki/people/sergey-tsymanov.md|Tsymanov]] also had a note from Val about a GitHub feature branch that does not match Jira — on [[wiki/topics/ai-assisted-development.md]] (Oct 2).
- **The transactional repositories.** [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Разделили с Сергеем там на пополам репозиторий, там где то 78 у него у меня. Вот и. Ну постепенно репозиториям. Проза [ADR]. Приведены в стандарт. Это то, Что касается транзакшенных системы." Pavel: "Отлично." ("78" as spoken; the derived notes read "7–8 repos" [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]].) Tsymanov: "прозы параллельно вёл. Сейчас вот прозы заканчиваю."
- **No prose for archived repositories.** Chudinov: "у нас есть [репозитории], которая уже. Наверное, ближе к статусу архив. Мы будем на них прозу делать. Это старая [updater]." [[wiki/people/pavel.md|Pavel]]: "**Нет, нет, там, скорее всего может быть прозы нету, но там [description] вполне себе нормальный был, но нет смысла нет смысла на него мы его точно не будем использовать.**" — the old updater and repositories near archive status get no prose.

## Update, Oct 26 2026 — "a link to the company standards in Claude's context" stops the branch mess

At the [[wiki/meetings/2026-10-26-daily-standup-claude-branch-hygiene-and-autotest-environment.md|Oct-26 Minsk stand-up]] (Russian; Val absent) [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]] [[wiki/people/andrey-bosik.md|Bosik]] asked everyone to make Claude keep the standards on branches and commits. [[wiki/people/sergey-tsymanov.md|Tsymanov]]: the standard is written down somewhere, and his Claude found it. [[wiki/people/pavel.md|Pavel]]: if the context has a link saying "use the company standards" — in the session, or in a memory file or "клодом ди" (read as CLAUDE.md — **inference**) — Claude keeps to it "и не будет таких проблем." This is the Sept-4 rule applied to branches — [[wiki/decisions/2026-10-26-claude-made-branches-carry-a-jira-key-and-are-deleted-when-the-task-closes-and-claude-is-never-a-commit-co-author.md]].

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — bring his repository into order over the weekend of Oct 3–4 2026, following Val's message — due Oct 5 2026 — [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [ ] Everyone (engineering and the game team) — use the standards, add narrow granular standards to them, and point Claude at the standards repository as part of routine work — ongoing standing rule — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]] [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] [[wiki/people/lena.md|Lena Zhukova]] — move the graphics team's existing Omni/NOVA naming documents into the Knowledge Base standards folder — due unspecified — [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [ ] [[wiki/people/igor-metelski.md|Igor Metelski]] — read the repository standard and correct his repository structure to match — due unspecified; he said "я могу смог ознакомиться и поправить под стандарт" — [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — set up the integration repository to the standard (check the matching Jira project, ADRs in docs) so Val does not have to chase it — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — point his Claude at the repository standard and consult Bosik on the test repository — due unspecified — [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]

## Open questions

- Does every developer — including Daniil — now have access to the knowledge repository? Kovalchuk said it should be open by default; a re-check was mentioned, with no owner named — [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]

## Update, Oct 30 2026 — Val's reminder: put your own standards in the repository

At the [[wiki/meetings/2026-10-30-nova-remote-game-update-architecture.md|Oct-30 remote-update meeting]] Val reminded everyone that the GitHub standards repository holds all the standards; he points his own Claude at it to ask whether a standard exists for what he is working on, and asked each person to put their own standards there too [[raw/Meeting_Transcript_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]] [[raw/Meeting_Notes_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]].

### Open commitments (Oct 30 2026)

- [ ] Pavel Frolov, Dmitri Chudinov, Alexander Biratka and Irina Shishko (all attendees) — add your own standards to the GitHub standards repository — due unspecified — [[raw/Meeting_Transcript_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]] [[raw/Meeting_Notes_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]]

## Note, Nov 4 2026 — the release standard goes into the standards repository

At the [[wiki/meetings/2026-11-04-mvp1-transactional-release-definition-and-pilot-watch.md|Nov-4 MVP 1 release meeting]] (Russian) [[wiki/people/val-levitan.md|Val]] asked [[wiki/people/pavel.md|Pavel]] to write the release flow agreed there as a standard, with Claude, and post it: "Это стандарт попадет в наш nolight bace. Репозитории, которая называется стандарты… все, которые туда направляют свой клод… поставить какието gard raails" — the same repository and the same rule as above; Pavel: "Стандарт по по релизам" [[raw/Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]] [[raw/Meeting_Notes_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]. The commitment is tracked on [[wiki/decisions/2026-11-04-a-release-is-done-only-when-the-cleaned-build-is-on-the-production-server-under-a-number-ivan-is-release-manager-with-claude-written-release-notes-and-an-exception-report-and-request-review-leaves-the-feature-workflow.md]]. Val also said the bug-documentation standard already lives there [[raw/Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]].

## Note, Nov 16 2026 — Genadi's folder and part-number standards are in the repository; "even two sentences"

At the [[wiki/meetings/2026-11-16-genadi-unguided-bom-test-and-standards.md|Nov-16 4:05 PM call with Genadi]] (Russian) [[wiki/people/val-levitan.md|Val]] said he writes standards into the repository called standards in the new GitHub space and points his own Claude at it; the AI-COO, AI-HR and the project manager agent all read it ("Они все смотрят на эти стандарты"). He asked [[wiki/people/genadi-peari.md|Genadi]] to have Claude write any standard he has — "Любой маленький стандарт даже 2 предложения" — in markdown and put it there [[raw/Meeting_Transcript_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026.md]] [[raw/Meeting_Notes_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026.md]]. Genadi said the standards for the hardware repository's category folders and for how part numbers go inside them are written and are in the standards repository: "Да да, абсолютно" [[raw/Meeting_Transcript_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026.md]]. The commitment is on [[wiki/decisions/2026-11-16-the-agents-build-the-bom-unguided-from-a-product-description-and-the-data-contracts-the-data-sheet-is-the-source-of-truth-and-nathan-spikes-a-simple-sub-assembly.md]].

## Note, Nov 16 2026 (5:56 PM) — Lev Rudky writes the standards; Val sends him bullet points

On the [[wiki/meetings/2026-11-16-lev-standards-ownership-and-po-standard.md|Nov-16 5:56 PM call with Lev Rudky]] (Russian part) [[wiki/people/val-levitan.md|Val]] said he made [[wiki/people/lev-rudky.md|Lev]] the authority on standards, not himself, and agreed to stop putting standards into GitHub himself: "так я я я не буду писать за стандарты пишешь да?" — Lev: "Я пишу да." Val will send Lev bullet points instead. Val's advice for overlaps: once a week (or once a month) point Claude at the standards and ask for a list of similar ones and a grooming; and before a commit, ask Claude whether a conflicting standard exists [[raw/Meeting_Transcript_Lev_Standards_Ownership_and_PO_Standard-November-16-2026.md]] [[raw/Meeting_Notes_Lev_Standards_Ownership_and_PO_Standard-November-16-2026.md]]. The call is about Business Central standards; whether it covers every standard Val writes is not said (open question on [[wiki/decisions/2026-11-16-lev-rudky-writes-the-standards-val-sends-him-short-bullet-points-instead-and-the-purchase-order-topic-becomes-a-po-standard.md]]).

## Note, Nov 20 2026 — two more uses: Genadi's purchasing standards and a daily PO agent; finance mistakes become standards

- **~3:09 PM, with Genadi** ([[wiki/meetings/2026-11-20-genadi-data-sheets-in-github-and-po-check-agent.md|stub]], Russian). Val said the knowledge base has "репозитории, которые называются стандарты" and his AI-COO reads them before acting; he will write a standard from the call himself; [[wiki/people/genadi-peari.md|Genadi]] is to write his purchasing knowledge into GitHub as standards and build an agent that checks all POs against them once a day [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]] [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]. Record: [[wiki/decisions/2026-11-20-genadi-works-only-on-the-bom-with-nathan-not-procurement-and-his-purchasing-know-how-goes-into-standards-checked-daily-by-his-own-po-agent.md]].
- **~3:32 PM, with the finance team** ([[wiki/meetings/2026-11-20-finance-team-ach-authorization-delay-and-standards-agents.md|stub]], English). "Standards need to be filed in GitHub. We have knowledge base repository called standards. So when we make mistakes and we discover these mistakes, we write a standard"; each person's own agent checks their email against them [[raw/Meeting_Transcript_Finance_Team_ACH_Authorization_Delay_and_Standards_Agents-November-20-2026.md]] [[raw/Meeting_Notes_Finance_Team_ACH_Authorization_Delay_and_Standards_Agents-November-20-2026.md]]. Record: [[wiki/decisions/2026-11-20-a-mistake-found-becomes-a-written-standard-in-github-and-each-finance-team-member-runs-their-own-email-checking-agent-against-the-standards.md]].

## Sources
- [[raw/Meeting_Notes_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Transcript_Rage_Nova_Conversion_Readiness-September-4-2026.md]]
- [[raw/Meeting_Notes_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Capability_Test_Status_and_FlexPort_GUI-September-22-2026.md]]
- [[raw/Meeting_Transcript_Transactional_MVP1_Jira_Cleanup_and_E2E_Tests-September-22-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Requirements_Cleanup_and_Autotests-September-23-2026.md]]
- [[raw/Meeting_Transcript_MVP1_FlexPort_Money_Loss_Bugs_and_Release_Date-September-24-2026.md]]
- [[raw/Meeting_Notes_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]
- [[raw/Meeting_Transcript_Repo_Standards_Walkthrough_with_Efim-September-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]
- [[raw/Meeting_Transcript_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]]
- [[raw/Meeting_Notes_NOVA_Remote_Game_Update_Architecture-October-30-2026.md]]
- [[raw/Meeting_Transcript_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]
- [[raw/Meeting_Notes_MVP1_Transactional_Release_Definition_and_Pilot_Watch-November-4-2026.md]]
- [[raw/Meeting_Transcript_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026.md]]
- [[raw/Meeting_Notes_Genadi_Unguided_BOM_Test_and_Standards-November-16-2026.md]]
- [[raw/Meeting_Transcript_Lev_Standards_Ownership_and_PO_Standard-November-16-2026.md]]
- [[raw/Meeting_Notes_Lev_Standards_Ownership_and_PO_Standard-November-16-2026.md]]
- [[raw/Meeting_Transcript_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [[raw/Meeting_Notes_Genadi_Data_Sheets_in_GitHub_and_PO_Check_Agent-November-20-2026.md]]
- [[raw/Meeting_Transcript_Finance_Team_ACH_Authorization_Delay_and_Standards_Agents-November-20-2026.md]]
- [[raw/Meeting_Notes_Finance_Team_ACH_Authorization_Delay_and_Standards_Agents-November-20-2026.md]]
