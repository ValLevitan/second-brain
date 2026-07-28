---
type: meeting
title: Data access strategy (MCP vs Excel/Tableau) and CMS cloud migration
date: 2026-03-23
aliases: [Data Access Strategy Dashboards or Conversational Queries, Data Access Strategy and CMS Cloud Migration, MCP vs Excel Tableau]
source-count: 3
---

# Data access strategy (MCP vs Excel/Tableau) and CMS cloud migration

Thin stub — substance lives on the topic pages linked below.

- **Date/time:** 2026-03-23, 1:34pm (recording header; §11 header date wins over the derived-notes processing stamps of Mar-26 and Apr-25). ~46 min, Russian.
- **Attendees:** [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] (transcribed "Dzmitry Chudzinau", back-end architect), [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (IT), [[wiki/people/sergey-tsymanov.md|Sergey Tsymanov]] (transcribed "Sergey Tsimanov"), [[wiki/people/andrey-bosik.md|Andrei Bosik]] (DevOps). [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- **Purpose:** decide JVL's near-term business-intelligence access path — conversational **MCP queries against the OLAP cube** vs continuing with **Excel-as-bridge / Tableau** — and, underneath it, whether to migrate the whole legacy casino-management-system (CMS) stack to the cloud. Ended with a one-week scoping plan and a follow-up set for the next Monday. [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]

Substance routed to:
- [[wiki/topics/olap-power-bi-architecture.md]] — the BI-access decision (drop Tableau/Excel-bridge; MCP-to-cube as the ~6-month interim) and the full CMS cloud-migration scope (all-or-nothing migration; PostgreSQL vs MS SQL; LDAP→Entra ID; the intermediate host layer).
- [[wiki/topics/ai-assisted-development.md]] — the MCP-as-data-access angle and Claude Code as the assumed migration force-multiplier.

§12 derived-document family: ONE meeting, THREE staged artifacts — the transcript (primary) plus TWO distinct derived notes (a 17KB "MCP vs Excel/Tableau, and CMS Cloud Migration" summary processed Apr-25, and a separate 9KB "Dashboards or Conversational Queries" summary processed Mar-26; the two notes are not byte-duplicates). All three cited below; facts on the topic pages are drawn from the transcript (fullest source of record). [[raw/Meeting_Notes_Data_Access_Strategy_and_CMS_Cloud_Migration-March-23-2026.md]] [[raw/Meeting_Notes_Data_Access_Strategy_Cloud_Migration-March-23-2026.md]]

§15.8 clear — tooling / data / cloud / CMS / licensing economics only; no named-person compensation.

## Sources
- [[raw/Meeting_Transcript_data_access_strategy_and_cms_cloud_migration-March-23-2026.md]]
- [[raw/Meeting_Notes_Data_Access_Strategy_and_CMS_Cloud_Migration-March-23-2026.md]]
- [[raw/Meeting_Notes_Data_Access_Strategy_Cloud_Migration-March-23-2026.md]]
