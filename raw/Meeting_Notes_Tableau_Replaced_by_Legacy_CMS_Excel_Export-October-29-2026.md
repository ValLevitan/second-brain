# Meeting Summary — Tableau reports: fix incomplete and outdated data
**Date:** October 29, 2026, 8:31 AM – 8:58 AM Eastern
**Duration:** ~26 minutes
**Attendees:** Val Levitan, Dzmitry Chudzinau, Andrei Bosik, Dmitri Kovalchuk, Sergey Tsimanov
**Raw transcript:** [[Meeting_Transcript_Tableau_Replaced_by_Legacy_CMS_Excel_Export-October-29-2026]]

## Summary

Held in Russian. Unclear names and words are marked "heard".

**The problem.** Georgia machines now ship with LTE modems and report data to the server. Nobody understands the Tableau reports or knows if they can be trusted. Sergey: how a machine connects does not matter; the team's job was to get data into the Tableau source. Dzmitry: Tableau has no game statistics report. For Juan he ran database queries and sent Excel files by hand.

**Tableau is not needed.** Dzmitry suggested web reports like the Transactional system instead, since Claude cannot work with Tableau. Val: Tableau is not tied to anything; the database is the source of truth. No one outside the company has report access anymore; the old Lucky Bucks reports are not updated. Outside access will come later with the Galaxy platform and its access control.

**Options weighed.** An MCP server for Claude (Val liked it), a web portal using Transactional login, or an Excel export. Dzmitry: an MCP cannot enforce per-user limits. Andrei: it would load the database. Andrei and Dzmitry: Excel export from the legacy CMS is fastest; the user logs in and the CMS already knows what they may see. The legacy CMS already has an export section; it will be extended. Sergey: in the past, unlimited exports of one or two years were slow and broke, which is why OLAP was used.

**Agreed approach (Dzmitry's recap).** A function for internal JVL users with a special role. It exports account statistics for our machines from the production database by game, operator, jurisdiction and date, maybe more. Each user sees only their own scope: Marta only Colombia, Felipe only Georgia. Val must see all, including Salta (heard) and Nebraska (heard). Users: Val, Marta, Felipe, Ekaterina (heard), Pavel, Irina, Efim, Dima Kovalchuk.

**User flow.** Felipe logs into the legacy CMS with his own login, opens the report page, picks filters, clicks Apply, and the browser downloads an Excel file. He then uses it on his own or with Claude. If he has questions on the numbers he asks Efim, who gets full access.

**Tableau license.** License runs to May. Val: stop updating Tableau reports, bury the Tableau structure, and drop the license once the Excel export is delivered.

## Decisions Made

- **Reports come as an Excel export from the legacy CMS, not Tableau and not an MCP** — simple, uses existing logins and limits, and Felipe works well with Claude. (Val; Andrei and Dzmitry agreed)
- **One export covers at most six months** — older data stays; the limit is only for the report. (Val)
- **Keep region limits** — Marta sees Colombia, Felipe sees Georgia; Val sees all. (Val)
- **Stop maintaining Tableau; drop the license once the Excel export is delivered.** (Val; Andrei accepted)
- **Target: ready by November 7, 2026, work starting Monday.** (Dzmitry)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dzmitry Chudzinau | Extend the legacy CMS export: role-based Excel export by game, operator, jurisdiction and date, 6-month max, region limits | Nov 7, 2026 | High | Starts Monday Nov 2 |
| 2 | Dzmitry Chudzinau | Give Efim full access to all data | Nov 7, 2026 | Normal | Efim supports Felipe |
| 3 | Val Levitan | Post the transcript in the meeting chat | Oct 29, 2026 | Normal | Done in chat at 9:02 AM |
| 4 | [Unassigned — needs clarification] | Turn this transcript into capabilities, features and tasks; open the project | TBD | Normal | Val suggested the AI-PM may do it |
| 5 | Andrei Bosik | Stop updating Tableau reports; drop the license after the Excel export ships | After Nov 7, 2026 | Low | License runs to May |

## Open Questions

- Who "Ekaterina" in the user list is, and what Salta and Nebraska (heard) refer to. Raised by Val's wording; unclear in the audio.

## Dispatch Log

---
*Processed from Teams transcript on October 29, 2026*
*Source meeting: Tableau reports: fix incomplete and outdated data*
