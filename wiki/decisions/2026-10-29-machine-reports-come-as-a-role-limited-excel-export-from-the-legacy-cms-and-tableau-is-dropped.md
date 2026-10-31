---
type: decision
title: Machine reports come as a role-limited Excel export from the legacy CMS — by game, operator, jurisdiction and date, six months at most per export, each user seeing only their own region — not Tableau and not an MCP; Tableau is no longer maintained and its licence goes once the export ships; target November 7 (Val, Oct 29 2026)
date: 2026-10-29
aliases: [Tableau replaced by legacy CMS Excel export, Excel export from the legacy CMS, legacy CMS Excel export, табло не нужен, мне табло не нужен вообще, bury Tableau, drop the Tableau licence, six-month export limit, полгода максимум, role-based Excel export, game statistics export, account statistics export, Tableau reports fix incomplete and outdated data]
source-count: 2
status: active
open-commitments: 4
open-questions: 2
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

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — extend the legacy CMS export: a role-based Excel export of account statistics by game, operator, jurisdiction and date, six months at most, with each user's region limits — due Nov 7 2026 (start Mon Nov 2) — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — give Efim full access to all the data — due with the export — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [ ] [[wiki/people/andrey-bosik.md|Andrey Bosik]] — stop updating the Tableau reports and give up the licence once the Excel export is delivered (licence runs to May) — due after the export ships — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] [[raw/Meeting_Notes_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [ ] Owner not named — turn the meeting transcript into capabilities and tasks and open the project; Val said the AI project manager might do it ("у нас же есть этот как его пиям, может быть это сделает уже") — due unspecified — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]] (see [[wiki/projects/ai-project-manager-and-company-second-brain.md]])

## Open questions

- Who is "Екатерина филипповна" in the user list — one person, or "Ekaterina" and Felipe? — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- Are the Georgia modem machines' Tableau numbers reliable? Val's opening question was set aside, not answered — [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
- [[raw/Meeting_Notes_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026.md]]
