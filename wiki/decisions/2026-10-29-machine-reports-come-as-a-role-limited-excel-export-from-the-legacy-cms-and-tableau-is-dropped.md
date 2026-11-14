---
type: decision
title: Machine reports come as a role-limited Excel export from the legacy CMS — by game, operator, jurisdiction and date, six months at most per export, each user seeing only their own region — not Tableau and not an MCP; Tableau is no longer maintained and its licence goes once the export ships; target November 7 (Val, Oct 29 2026)
date: 2026-10-29
aliases: [Tableau replaced by legacy CMS Excel export, Excel export from the legacy CMS, legacy CMS Excel export, табло не нужен, мне табло не нужен вообще, bury Tableau, drop the Tableau licence, six-month export limit, полгода максимум, role-based Excel export, game statistics export, account statistics export, Tableau reports fix incomplete and outdated data]
source-count: 10
status: active
open-commitments: 3
open-questions: 3
---

# Machine reports come as a role-limited Excel export from the legacy CMS; Tableau is dropped

A Russian working call on Oct 29 2026, 8:31 – 8:58 AM Eastern — [[wiki/meetings/2026-10-29-tableau-replaced-by-legacy-cms-excel-export.md]]. Present: [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (label "Dzmitry Chudzinau"), [[wiki/people/andrey-bosik.md|Andrey Bosik]] (label "Andrei Bosik"), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] and [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (label "Sergey Tsimanov") [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. The longer history of the reporting stack (OLAP cube, Tableau, the Mar-23 2026 MCP plan) is on [[wiki/topics/olap-power-bi-architecture.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## Why the meeting was called

- **Modems in Georgia.** Val: machines in Georgia are starting to go out with LTE modems; they connect to some system and report data to our server. Whether they always connect reliably, he does not know [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. (The modem rule itself: [[wiki/decisions/2026-10-06-every-machine-ships-with-a-modem-and-customers-are-told-reports-are-free-for-a-limited-time-with-an-opt-out.md]].)
- **Nobody can read Tableau.** Val: "никто не понимает, как её читать"; can the reports from Tableau be trusted, and how should they be read? He knows JVL is going to leave Tableau and move to the Galaxy platform, but that is still being built [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Tsymanov.** How a machine connects does not matter to them; their job was to get the data into the source Tableau uses. They hardly saw the reports themselves [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Chudinov.** In recent months Juan asked for game statistics. Tableau has no such report, so he ran queries on the database and, with Pavel or Irina, made Excel files and passed them on [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. ("хуан" read as [[wiki/people/juan-martinez.md|Juan Martinez]] — **inference** from his game-performance role.)

## Tableau is not needed; the database is the source of truth

- Chudinov proposed web-interface reports, as in the Transactional system, instead of Tableau — easier for Claude, which does not know Tableau (Bosik: "клод про табло вообще ничего не умеет") [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- Val: "Табло вообще ни к чему не привязывают… меня табло не волнует." Chudinov: the main source of truth is "наша база данных" [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **No outside viewers.** Bosik asked whether anyone outside the company still views Tableau reports. Kovalchuk: there were reports (Lucky Bucks, Bosik recalled) and access was given, but they are not updated. Val: no one outside the company has access to JVL reports any more — "Это это было раньше, но это всё умерло." Outside access matters again later, once the new platform with access control is out [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Galaxy status (Chudinov).** The Transactional stack planned on the server side is ready; the next step is to discuss the machine side. They cannot code it before it is discussed and capabilities are created — for example, per-spin statistics: the machines are not ready, and data volumes over the LTE modem must be checked [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. See [[wiki/topics/nova-platform-architecture.md]] for Galaxy.

## Options weighed

- **A web portal** behind the Transactional system's login, with reports Claude draws (Bosik) — a quick crutch for the old machines tied to the legacy CMS until the new CMS / Galaxy exists [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **An MCP for Claude.** Chudinov listed it as possible. Val said the point is to give more flexibility to people able to use an MCP. Against it: Kovalchuk called it an unneeded layer; Chudinov said an MCP cannot enforce the restrictions and permissions — whoever gets access reads all the data; Bosik said it would raise the load on the database [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **An Excel export.** Tsymanov: give users an export, they download an Excel file and Claude builds whatever they want from it; it can be done quickly on "нашем старом" system. Bosik: log in to the legacy CMS, press download, give the file to Claude; fastest, with no authorization, token or security work, since the CMS already knows the user and which filter to apply. Chudinov: the legacy CMS already has a reports section and part of the function; it needs updating and bug-fixing [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **History (Tsymanov).** Such an export already exists in the export section. In the past it had no time limit; users pulled a year or two of data, which loaded slowly and often broke, and that is why the move to OLAP was started [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].

## The ruling

- **Excel.** Val: "я бы хотел бы sell файл" — Marta will want an Excel file, and Felipe works very comfortably with Claude; "Экселфайл это очень просто" [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Six months at most.** Chudinov offered a limit of a year and a half; Kovalchuk said a month might be enough; Val: "давайте экселфайл, давайте полгода максимум." He added that the rest of the data is not to be erased — the limit is only for the report [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Region limits stay.** Val: Marta looks only at Colombia, Felipe only at Georgia. Chudinov: then the same limits stay, so Marta cannot see the USA and Felipe cannot see Colombia; Val: "Ну желательно." Val himself must also see "салта" and "не братка" [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] — read as South Dakota (the owner-ruled "Salta" garble) and Nebraska (**inference**).
- **What gets built (Chudinov's recap).** A function for internal JVL users with a special role that exports from the production database account statistics for our machines, by game, operator, jurisdiction and date, possibly with more later [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Users** named by Val: himself, Marta, Felipe, "Екатерина филипповна" (**unclear** — one person or "Ekaterina" plus Felipe), Pavel, Irina, "Фима" and Dima Kovalchuk [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. "Фима" read as [[wiki/people/efim-podvoiski.md|Efim Podvoiski]], as the notes do [[raw/Meeting_Notes_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]. Marta read as [[wiki/people/marta.md|Marta]] of Colombia (**inference**, from the Colombia scope).
- **The user flow (Chudinov).** Felipe logs in to the legacy CMS with his own credentials, opens a page he has access to, picks filters, presses Apply, and the browser downloads the file to his computer. He then uses it alone or with Claude to build any report he wants. If he has questions on how to read the numbers, he can go to Efim, who gets full access to everything [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Date.** Chudinov: work may start on Monday; ready "до 7 ноября 26" [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].
- **Tableau.** Bosik asked whether Tableau can then be dropped. Val: "Мне табло не нужен вообще." Kovalchuk: the licence runs until May. Val: stop updating the reports, bury the whole Tableau structure, and later give up the licence — on condition that the Excel export is delivered. Bosik: "Принято" [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]].

## How it sits against earlier rulings

- **Mar 23 2026** chose an MCP to the on-prem cube as a roughly six-month interim, with a later full cloud migration — [[wiki/topics/olap-power-bi-architecture.md]]. On Oct 29 the MCP route was weighed and not taken; the interim is now the legacy-CMS Excel export. This is a change of plan (evolution), not a contradiction. Whether the cloud migration plan still stands was not discussed.
- The Mar-23 call deprioritized role-based access because few people used the reports. On Oct 29 per-user region limits are a requirement (Val: "желательно").

## Open commitments

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — give Efim full access to all the data — due with the export — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — stop updating the Tableau reports and give up the licence once the Excel export is delivered (licence runs to May) — due after the export ships — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] [[raw/Meeting_Notes_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [ ] Owner not named — turn the meeting transcript into capabilities and tasks and open the project; Val said the AI project manager might do it ("у нас же есть этот как его пиям, может быть это сделает уже") — due unspecified — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] (see [[wiki/projects/ai-project-manager-and-company-second-brain.md]])

## Open questions

- Who is "Екатерина филипповна" in the user list — one person, or "Ekaterina" and Felipe? — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- Are the Georgia modem machines' Tableau numbers reliable? Val's opening question was set aside, not answered — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Update, Nov 2–3 2026 — the report is built; the prod deploy waits on checking Tsymanov's vacation-time work; STG today or tomorrow

- **Nov 2.** At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] [[wiki/people/dmitri-chudinov.md|Chudinov]] must hand over the legacy CMS report ("на легость с м с репорт", heard — read as CMS, **inference**) "как 1 часть" and wants to deploy it to prod; but [[wiki/people/sergey-tsymanov.md|Tsymanov]]'s tasks from Chudinov's vacation (RIS, passport, lease — as heard) were tested by [[wiki/people/ivan.md|Ivan]] on STG only, and nobody knows what was checked; Ivan and Chudinov talk on Wednesday; "В пятницу мне надо будет отчитываться, почему я это ещё не сделал" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]].
- **Nov 3.** At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]]: "Отчёт сделал", plus a log analysis — the current logs break and do not save statistics; if a game is not found or a machine is not registered, the record goes to a separate table so transfer is not blocked; deploy to STG today or tomorrow; open: recheck the machine and its statistics first, or verify on production [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. [[wiki/people/pavel.md|Pavel]]: the legacy CMS's machine-state view, basic diagnostics and tilts should keep working for connected machines; Chudinov: if nothing broke — the current machines are far ahead of those the logic was built for [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].

### Open questions (Nov 3 2026)

- Recheck the machine and its statistics before the deploy, or verify on production? — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]

## Update, Nov 4 2026 — Irina takes the check of Tsymanov's server-side work so Chudinov can release; the passport deploys too if approved

At the [[wiki/meetings/2026-11-04-daily-standup-release-build-handoff-and-nad2-product-code.md|Nov-4 Minsk stand-up]] (Russian; Val absent) [[wiki/people/irina-shishko.md|Irina]]: "Мне нужно сейчас посмотреть, если чтото со стороны сервера не проверено да проверить, и тогда ты сможешь релизить"; [[wiki/people/pavel.md|Pavel]]: the items Sergey did ("борисовруман", "парисо" — heard: RIS, passport); [[wiki/people/sergey-tsymanov.md|Tsymanov]]: "Дима будешь, если дадут добро, то паспорт тоже" deploy; [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Хорошо" [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]. This takes over the Nov-2 "Chudinov and Ivan meet on Wednesday" item (annotated on [[wiki/people/dmitri-chudinov.md]]); whether the STG deploy of Nov 3 happened is not said. The commitment is on [[wiki/people/irina-shishko.md]] (Nov 4). Chudinov also reported "Я сделаю рот вчера. Прелиз экю" (heard: the IQ release made yesterday) and work on host and server reporting [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]].

## Update, Nov 11 2026 — the machine-statistics export is closed and released, and Chudinov wrote to Val that it is ready

At the [[wiki/meetings/2026-11-11-daily-standup-flex-pay-to-mvp3-and-sound-names-in-lua-scripts.md|Nov-11 stand-up]] (Russian) [[wiki/people/dmitri-chudinov.md|Chudinov]]: "Вчера сегодня закрыл. Экспорт статистики по машинам war celine [heard]… сделан релиз… отписанный письмо о готовности" (the notes: he made the release and wrote to Val that it is ready); some tasks that did not get done under these capabilities (bugs, other features) still need marking [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]. The export commitment below is discharged. Whether Efim's full data access is done is not said; Bosik's Tableau step can now start (**inference** from the "after the export ships" condition).

## History

- [x] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — extend the legacy CMS export: a role-based Excel export of account statistics by game, operator, jurisdiction and date, six months at most, with each user's region limits — due Nov 7 2026 (start Mon Nov 2) — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] — *Nov 3 2026: "Отчёт сделал"; STG deploy today or tomorrow; prod waits on verifying Tsymanov's vacation-time work* — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] — *done Nov 11 2026: "Экспорт статистики по машинам… сделан релиз… отписанный письмо о готовности"* — [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [[raw/Meeting_Notes_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Release_Build_Handoff_and_NAD2_Product_Code-November-4-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex_Pay_to_MVP3_and_Sound_Names_in_Lua_Scripts-November-11-2026.md]]
