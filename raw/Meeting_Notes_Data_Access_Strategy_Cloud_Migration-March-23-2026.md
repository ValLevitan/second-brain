# Meeting Summary

## Data Access Strategy: Dashboards or Conversational Queries

| | |
|---|---|
| **Date** | March 23, 2026, 1:34 PM Eastern |
| **Duration** | ~46 minutes |
| **Attendees** | Val Levitan, Dzmitry Chudzinau, Dmitri Kovalchuk, Sergey Tsimanov, Andrei Bosik |
| **Location** | Microsoft Teams |

---

## Summary

### Background and Meeting Purpose

Val opened the meeting by acknowledging that the team had been struggling to align on a data access strategy through async chat. He explained that positions were clear but the implementation path for the final proposal was not, and called this meeting to stimulate ideas and reach concrete next steps. Val stated he was inclined toward going with MCP (Model Context Protocol / conversational AI queries) directly, seeing very few benefits in the intermediate Tableau-based approach currently in place.

### Current Architecture and Its Limitations

The team discussed the existing data access stack in detail. The current system is a legacy infrastructure built approximately 10 years ago, consisting of:

- **MSSQL database** — the primary data store
- **OLAP cube** — refreshes every ~30 minutes by pulling data from the database, processes large data sets quickly without indexes
- **Excel files** — connect to the OLAP cube with hardcoded connection strings containing URLs and passwords, distributed to end users
- **Tableau** — connects to the Excel files as a visualization layer, producing dashboards
- **CASS WH (Warehouse Host)** — an intermediate application that all machines connect to via certificates, aggregating data before periodically pushing it to the main CASS database

Dzmitry Chudzinau raised a critical concern: MCP lacks visual conveniences — no dropdown lists to filter by operator or machine, no persistent session memory between queries, no built-in charting comparable to dashboards. Each query requires typing prompts and remembering parameters.

Dmitri Kovalchuk confirmed that Excel cannot connect to external cubes from the cloud (browser) version. Only the desktop version supports cube connections, requiring hardcoded credentials in the data source configuration.

Sergey Tsimanov provided historical context: the Excel-based approach was built around 2017, with credentials hardcoded because it was designed for internal network use.

### Security Concerns with Excel Approach

Dzmitry Chudzinau highlighted a major security issue: the Excel files contain database credentials in plain text. Anyone who obtains a file gets full access to the cube/database, with no way to revoke it per-file. This makes the Excel approach fundamentally insecure for distribution.

Val asked whether Excel could authenticate via Microsoft SSO instead of hardcoded credentials. Dmitri Kovalchuk responded that SSO would likely only work with a cloud-based cube, not the current on-premise OLAP. Moving OLAP to the cloud to enable SSO would require migrating the entire infrastructure.

### Can the Infrastructure Be Migrated Piecemeal?

Val asked whether the architecture could be moved to the cloud in pieces. The unanimous answer was no — the components (CASS DB, OLAP cube, CASS WH) are tightly interdependent. Dzmitry confirmed: "If we move, we move everything — each piece pulls the next."

Sergey raised whether moving just the OLAP cube to the cloud was feasible while keeping the database on-premise. Dmitri Kovalchuk said this needs investigation. Andrei Bosik suggested this could potentially work through a VPN tunnel but raised cost concerns about data transfer volume.

### The Move Away from On-Premise Imperative

Val laid out two fundamental drivers for change:

- **Manual data preparation** — the current workflow requires manual work to prepare data, which the team wants to eliminate
- **No one to maintain on-premise servers** — the company needs to move to cloud solutions because there is insufficient staff to service physical servers

Val stated this is a known direction the team has discussed before. The final architecture is clear — cloud-based, without Tableau as it exists today.

### Val's Interim Proposal

Val proposed a two-phase approach:

1. **Short-term (up to 6 months):** Connect MCP directly to the existing OLAP cube. Use this for the transition period. No external casino reports needed — that business has ended. Only Val and possibly Juan use Tableau today.
2. **Long-term:** Complete the full migration to a modern cloud architecture.

Val emphasized that Claude Code can generate dashboards and reports from prompts effectively. He sees no reason each team member couldn't create their own saved prompts/scripts for routine queries.

### Cloud Migration — Technical Assessment

Dzmitry Chudzinau outlined the key technical considerations for a full cloud migration:

- **Codebase** — the CASS platform's code is mostly modern and could be upgraded with framework versioning. Claude Code would simplify this.
- **SQL migration** — SQL scripts and stored procedures would need conversion. Target database matters: if not MSSQL, everything must be rewritten.
- **Authentication** — current LDAP-based auth will not exist in the cloud. Replacement: Azure AD / Entra ID with SSO.
- **Architecture** — could migrate as-is (lift-and-shift) or redesign. Consensus: start with as-is.
- **CASS WH** — the intermediate data collection host must also be migrated; everything is interconnected.

### Cost Discussion

Nobody knows the actual cloud costs, which could range from $100 to $10,000/month. MSSQL cloud licensing is known to be expensive. Dzmitry proposed migrating to PostgreSQL as an alternative, which would require rewriting SQL but offers free/low-cost hosting. Val expressed 75% confidence that a managed cloud SQL service would be better.

Dmitri Kovalchuk estimated that setting up the cloud infrastructure (2–3 servers, networking) using Claude Code would take approximately one week. Software-side configuration and migration would be additional.

---

## Decisions Made

- **MCP as interim data access method** — Connect MCP directly to the existing OLAP cube for the transition period (up to 6 months), replacing Tableau dashboards for internal users. (Proposed by Val, team acknowledged)
- **No external casino reports needed** — The business of providing reports to external casino operators has ended. This simplifies the transition. (Stated by Val)
- **Full cloud migration is the long-term direction** — The entire CASS infrastructure must be migrated as a unit. Piecemeal migration is not feasible. (Consensus)
- **No role-based access needed in interim** — Only Val and Juan currently use the data access tools; security/access concern is deprioritized short-term. (Confirmed by Val and Dzmitry)
- **PostgreSQL should be evaluated as MSSQL alternative** — To avoid high MSSQL cloud licensing costs. (Proposed by Dzmitry, supported by Andrei)
- **Azure AD / Entra ID to replace LDAP** — Authentication will shift from on-premise LDAP to Microsoft SSO when moving to the cloud. (Consensus)

---

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|---|---|---|---|---|
| 1 | Dmitri Kovalchuk | Create a block diagram / structural schema of the current CASS infrastructure (servers, database, OLAP cube, CASS WH, data flows, Excel/Tableau connections) | March 30, 2026 | High | Needed by Andrei for cost estimates and by Dzmitry/Sergey for new architecture proposal |
| 2 | Andrei Bosik + Dmitri Kovalchuk | Estimate monthly/yearly cost of running current CASS in the cloud. Two scenarios: (1) MSSQL on Azure, (2) PostgreSQL or equivalent | March 30, 2026 | High | Determines whether lift-and-shift is viable or DB migration to PostgreSQL is necessary |
| 3 | Dzmitry Chudzinau + Sergey Tsimanov | Produce new cloud architecture proposal — straightforward as-is lift-and-shift, no optimization | March 30, 2026 | High | Architectural blueprint needed alongside cost estimate for migration decision |
| 4 | Val Levitan | Compile and distribute meeting summary document from transcript | Before March 30 | Normal | Meeting record for team alignment |
| 5 | Val Levitan | Schedule follow-up meeting for March 31, 2026 with all attendees | ASAP | Normal | Review findings and decide next steps |

---

## Open Questions

- Can the OLAP cube support role-based access natively? Sergey suggested it might have built-in per-user visibility controls. Needs verification.
- How to secure MCP's connection to the on-premise OLAP cube? Andrei proposed an auth proxy; no concrete solution decided.
- What does MSSQL cloud licensing actually cost? Part of undertaking #2.
- Can a VPN tunnel between cloud infrastructure and local servers work for interim or migration? Raised by Andrei; not investigated.
- What is the actual data volume for OLAP cube refreshes? Debated but not quantified.

---

*Processed from Teams transcript on March 26, 2026*
*Source meeting: Data Access Strategy: Dashboards or Conversational Queries*
