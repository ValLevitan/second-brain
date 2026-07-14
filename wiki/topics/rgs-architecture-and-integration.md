---
type: topic
title: RGS architecture and operator integration
date: 2025-02-01
aliases: [RGS, remote game server, RGS API, math container, direct integration, reverse integration, Golden Palace, Digitain, Hub88, BetConstruct, Comtrade Gaming, Postman, OpenAPI, RGS scaling, 1000 casinos, container model, custom portal]
source-count: 6
open-questions: 3
---

# RGS architecture and operator integration

How JVL's **RGS** (remote game server) is built and how JVL connects it to online-casino operators and platforms. This is the technical/engineering side of the online-games business; the commercial/market side lives in [[wiki/topics/online-games-rgs-distribution.md|Online games / RGS distribution]]. Owned technically by [[wiki/people/efim-podvoiski.md|Efim Podvoiski]] (the RGS author). [[raw/Aaron_Val_2025-02-11.md]]

## What the RGS is (Efim's description)

- The RGS sits **between the online game (running in the browser) and the wallet**, and connects the game to its **math container**. Its two jobs: connect the game UI to the math, and connect the game to the wallet so real-money bets and wins work. It does **not** hold game mechanics itself — mechanics live in the browser game and the math lives in the math container. [[raw/Aaron_Val_2025-02-11.md]]
- Internally it is a **set of containers orchestrated by Kubernetes**, with a transaction database of current sessions; described as a "temporary storage and transport framework." Nothing in it is secret except the **math**; the protocols/tables could be shared if the database were protected. [[raw/Aaron_Val_2025-02-11.md]]
- The **math container is the only dynamically changing part**: to add a game you drop in a new math container; the RGS and its API do not change. [[raw/Aaron_Val_2025-02-11.md]]
- The API is **very narrow — roughly four calls** (start session/get player parameters, bet, win, plus roll-back/repeat-win); a few optional operator→RGS calls are used to synchronise/check wins and show games in a back office. [[raw/Aaron_Val_2025-02-11.md]]

## Two ways to integrate

- **Reverse integration** — the RGS implements the API the platform dictates (JVL adapts to them). [[raw/Aaron_Val_2025-02-11.md]]
- **Direct integration** — JVL dictates which API the platform uses (the operator adapts to JVL's API). [[raw/Aaron_Val_2025-02-11.md]]
- Efim says JVL's API is no more complicated than the APIs JVL itself integrated with by reverse integration, and integrators reading the document have not called it unusual or hard. [[raw/Aaron_Val_2025-02-11.md]]

## Current integrations (as of Feb 1 2025)

- **Digitain** — the **first** integration; it was **reverse** (JVL integrated to them) and is **complete**. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Golden Palace** — the **first Direct integration**; JVL gave them documentation for JVL's API. As of Feb 1 it is **still in progress** (Efim believes they have no more integration questions, but no formal "integration complete / start rolling out games" green light had been given). JVL has no shared task board with the operator, so visibility into their progress is limited. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Hub88** and **BetConstruct** (transcribed "Bad Construct") — aggregators JVL is integrated with via its RGS; connecting through Hub88's API reaches the wallets Hub88 supports without integrating each wallet separately. [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **EveryMatrix** — the aggregator the land-based/online games reach operators through (see [[wiki/topics/online-games-rgs-distribution.md]]). [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- **Comtrade Gaming** and others (Intzimmer, Chromatic, Intergame — spellings as transcribed) — named by Aaron as example remote-gaming-server vendors that publish specifications, examples, and known capabilities, held up as the pattern JVL should follow. [[raw/Aaron_Val_2025-02-11.md]]

## Where the source lives and the Git migration

- The RGS source is in **SVN** ("RSVN"), not Git, and there was **no plan yet** to move it (Feb 11). Aaron pushed that it must move to Git before any real analysis can start. [[raw/Aaron_Val_2025-02-11.md]]
- In the Feb 11 repo-structure meeting, moving RGS to GitHub was sequenced as migration **step 2** (after Omni, Miranda and FlexPay), because Efim said it is a real production project and a multi-day job. See [[wiki/decisions/2025-02-11-git-migration-sequence.md]]. [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- The RGS deploys on a **Kubernetes cluster** in JVL's cloud (three AWS regions: Canada, Europe, Singapore); JVL also runs its online application from a hosted Kubernetes cluster. [[raw/JFrog transcript - February-6-2025.md]] [[raw/Aaron_Val_2025-02-11.md]]

## The diagram walkthrough — player flow and protection lines (~Mar 26)

From Efim's one-on-one architecture walkthrough for Val ([[wiki/meetings/2025-03-26-rgs-architecture-explainer.md]]; date inferred from transcription stamp): [[raw/Explain RGS.md]]

- **Player flow:** the platform forms the correctly-parameterised **URL** that loads the game (via a CDN from storage that is "как бы часть RGS"); the game then makes **Open and Init** requests through the RGS to the platform, which answers with player identity, country, language, currency and balance (Efim's example: an Argentine player, Spanish, 150,000 pesos). [[raw/Explain RGS.md]]
- **Bets are abstract in the math:** the math knows nothing about currencies — "Математика тоже не знает ничего про аргентинские песо" — the RGS converts the math's abstract bets into the player's currency and enforces **jurisdiction bet restrictions and max-win caps** ("Или мы хотим ограничить, например, MaxWin. Как мы сейчас обсуждаем") before telling the game what bets are allowed. [[raw/Explain RGS.md]]
- **Play-request hardening:** the play endpoint sits behind a firewall but is plain HTTP that "любой может прийти и послать"; the **Gaming API** validates the request format and the stored **session object** (created at open, kept in the database) before the math server plays; the wallet is told the bet (and can refuse for insufficient funds) and the win — only then are the reels shown to the player. [[raw/Explain RGS.md]]
- **Protection lines:** best not to expose the **math engine and RNG service**; the RNG is "не секретный, а защищённый" (protected from manipulation, not secret); the master database's design could be shown unless treated as trade secret, but everything inside must be protected because "они работают, в общем-то, с деньгами." The resource server and Gaming API entry point are freely shareable ("хочешь, пиши свое вообще"). [[raw/Explain RGS.md]]
- **Single-client RGS:** if the RGS talked to exactly one casino, the **integration gateway falls away** (it exists because integrations are many), and databases might be merged, but "принципиально все части остаются." The **demo wallet** exists **only for JVL's own testing** ("кроме нас демо валет не нужен никому… они нам не дадут потестировать так, как нам надо"). [[raw/Explain RGS.md]]

## Giving the RGS away and automating distribution (~Mar 26)

- Val's probe: **copy the cloud RGS instance and give it to a direct casino client for free**, helping them implement the hooks ("Я пытаюсь скопировать наш RGS. И отдать им for free… И не только отдать. А помочь им еще сделать… все вот эти вот хуки") — extending the Nov-2024 rent/open-the-code idea above. Efim's sizing: the client side is ~4–5 requests, "проект на неделю" for a developer who has integrated before; hooking the game-launch URL into an already-integrated wallet is ~a day. [[raw/Explain RGS.md]]
- **Per-wallet direct integrations ≈ a month each** ("Это в размерах где-то месяца"), so pre-integrating ~10 prominent wallets ≈ "работа на год приблизительно"; Efim wrote the first direct-integration documentation "практически я один ее делал" and expects each next integration to be easier, without guarantees. Val's scaling complaint: "I cannot scale. Мне нужно какой то пакет. Положить на our website… Весь сет документации." [[raw/Explain RGS.md]]
- **New-game distribution is manual today:** "как-то сейчас работает Андрей, говорит, а вот у нас тут новая игра вышла, хотите взять?" — technically it means dropping the game's **math container** into the client's instance and having them place the icon. The **Golden Matrix** container insertion required going into "их гид" [their git] and "нажать какие-то там 10 кнопок"; Efim allowed it "наверное, это можно свозить к одной кнопке" if he and "Андрей" think it through (which Andrei is not stated — queued). Val floated the demo-site link flow: an operator likes a demo on "наш Netflix сайт" and a link auto-attaches the game to their RGS. [[raw/Explain RGS.md]]
- *Name confusion note:* early in the session the current direct-integration company is named with a self-correction — "Она называется golden matrix. Ок. Прошу прощения. Она называется golden palace" — while later the completed container work is attributed to "совле-матрикс" [Golden Matrix]. Both are known first direct integrations (see [[wiki/topics/online-games-rgs-distribution.md]]); which one this session's "integration we did" refers to is **unclear**. [[raw/Explain RGS.md]]

## The "easy-integration" goal (Aaron and Val)

- Aaron pressed that JVL should be able to hand an operator a **Postman collection** for the RGS API and/or expose it as an **OpenAPI** document, so tools can read the endpoints directly — the basic hygiene needed before offering integration to outsiders. Efim had not used Postman. [[raw/Aaron_Val_2025-02-11.md]]
- Val's larger vision (his "dream integration"): an operator self-serves on a JVL website — reviews/marks-up/signs the contract online — and then RGS integration happens almost automatically, "like downloading an installer," instead of engineer-to-engineer Skype threads. Val cited having connected Atlassian and GitHub via MCP through VS Code (done for him by an IT person in ~45 minutes) and Cline's new MCP marketplace as proof such near-automatic connection is possible. See [[wiki/topics/online-games-rgs-distribution.md]] (marketplace). [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- Efim's counter-view: the important thing to protect is the math container (plus 2–3 nodes); everything else can be documented and published, and each integration makes the docs better. Val respects but does not fully accept this — he notes Efim is a mathematician, not an architect, and did not design/program the RGS. (Recorded as differing views, not a contradiction between sources.) [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]

## History — the 1,000-instance scaling challenge (Nov 12 2024)

An older source (staged 2025-03-29, internally dated **Nov 12 2024**) predates the Feb-2025 material above and is recorded as history. On that call [[wiki/people/val-levitan.md|Val]] set the goal of scaling the RGS from ~**150 casino accounts** to ~**1,000**, integrated **directly** (see the vision on [[wiki/topics/online-games-rgs-distribution.md]]). The engineers (incl. [[wiki/people/efim-podvoiski.md|Efim Podvoiski]]) flagged what has to change. See [[wiki/meetings/2024-11-12-online-vision-and-rgs-scaling.md]]. [[raw/online_vision_efim_2025-03-29.md]]

- **Two integration models named:** via **containers** (as with EveryMatrix, JVL's first integration) or via the **RGS directly**; the operator configures the rest itself. [[raw/online_vision_efim_2025-03-29.md]]
- **Current architecture assumes tens of accounts, not thousands** — each new casino needs manual setup (config entries / per-instance data), and the "JVL PIR/RGS" part must be re-architected to work from a database for ~1,000 instances. The team judged "1,000 instances" as sounding strange and needing rethinking; a **custom portal** where casinos enter their own data (with human validation of that data) would likely be needed. [[raw/online_vision_efim_2025-03-29.md]]
- **Platforms seen as increasingly unnecessary:** content doesn't come from the platform; the **RGS + wallet** are what matter, and land-based casinos in well-regulated markets already own/buy their platform. Val floated **renting the RGS (~$100/year)** or even **opening its code** to undercut the platform business. [[raw/online_vision_efim_2025-03-29.md]]
- **Releasing one game/week** would require minimising the current ~1 hour of manual game-parameter entry per game; a manifest/testing step still needs a human, so the target was to reduce (not fully eliminate) manual work. A follow-up architecture meeting was set for ~**Dec 10 2024**. [[raw/online_vision_efim_2025-03-29.md]]

## Open questions

- Which "Андрей" is meant to co-design the one-button game-container deployment with Efim — Andrey Bosik (DevOps) or Andrei Klimovich (online commercial)? Not resolvable from context. — [[raw/Explain RGS.md]]
- Can the near-automatic "installer-magic" RGS integration actually be achieved, given that JVL cannot control the (varying) API quality on the operators' side? — [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- Is the Golden Palace direct integration actually finished? (Efim thinks the questions are done; no formal completion confirmation was seen.) — [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]

## Sources

- [[raw/recap_with_andrei_klimovichonlineecho212025_2025-02-01.md]]
- [[raw/JFrog transcript - February-6-2025.md]]
- [[raw/Aaron_Val_2025-02-11.md]]
- [[raw/online_vision_efim_2025-03-29.md]]
- [[raw/Git_repo_structure_part_2_2025-02-11.md]]
- [[raw/Explain RGS.md]]
