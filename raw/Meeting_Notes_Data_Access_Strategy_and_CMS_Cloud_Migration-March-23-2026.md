# Meeting Summary — Data Access Strategy: MCP vs Excel/Tableau, and CMS Cloud Migration
**Date:** March 23, 2026, 1:34 PM Eastern
**Duration:** ~46 minutes
**Attendees:** Val Levitan, Dzmitry Chudzinau, Dmitri Kovalchuk, Sergey Tsimanov, Andrei Bosik
**Language:** Russian (summarized in English per Val's standard)

## Summary

The meeting opened on a narrow question — should JVL's BI access path go through MCP (conversational queries against the OLAP cube), Excel-as-bridge, or Tableau — but quickly pivoted into the deeper architectural question Val has been circling: **moving the entire legacy CMS / OLAP stack into the cloud**, with SSO-secured access, and using Claude Code to do the heavy lift. The meeting ended with a concrete one-week action plan and a follow-up scheduled for the next Monday.

### Opening — Val's leaning: MCP direct, drop Tableau / Microsoft BI

Val opened by saying he's leaning toward MCP as the access mechanism and sees very few benefits in continuing the Tableau / Microsoft Power BI route. He acknowledged Dzmitry had previously sent a comparison table in chat. Val explicitly said he doesn't read minds well and they don't write up positions well, so this meeting is to break the silence.

### MCP — what works, what doesn't

Dzmitry surfaced the core ergonomic limitation of pure-MCP access: there's no dropdown filter, no remembered selection. Each query requires re-prompting. The user has to keep machine numbers, operator names, etc. in their head. Dmitri Kovalchuk added that MCP doesn't give you the panoramic, all-at-once view that an app's UI does — comparing slices visually is awkward. MCP also can't draw charts the way a dedicated app can.

Val agreed with all of that, but pushed back on the framing: the question isn't whether MCP is as nice as a finished BI app — it's whether MCP is good enough as a stop-gap for the next several months while the team builds the proper architecture.

### Excel-as-bridge — current state and why it's ending

Today's working pattern: Excel files sit somewhere on the network with hard-coded credentials, connected directly to the OLAP cube (since 2017). Anyone with that .xlsx can pull live cube data — no real auth gate.

Discussion of whether cloud Excel could connect to the on-prem cube. Dmitri Kovalchuk: cloud Excel does not have an integration to an external on-prem cube via standard mechanism — Microsoft's regular Excel needs the data-source connection string with explicit credentials, and that's typically only used inside an organization's internal network. Even if you exposed the cube externally for cloud Excel, you'd be punching the firewall open for everyone.

Val pushed: Excel is used everywhere; the connection isn't *necessarily* hardcoded. Dmitri Kovalchuk: cloud Excel and on-prem cube connectivity is not a normal flow; Microsoft doesn't provide a built-in tool for that.

Andrei Bosik: the bigger structural problem is that the current pattern produces casino-specific Excel files (Colombia, Mexico, etc.) for data segmentation — that doesn't scale, doesn't role-gate properly, and is fundamentally manual.

Val's conclusion: **the Excel-as-bridge pattern has no remaining benefit** — it's either insecure, manual, or both. Time to move on.

### Cube role-based security — does it work?

Dzmitry asked: if MCP connects directly to a regular cube, can we attach role-based policies? Dmitri Kovalchuk: not on a regular cube — to slice access by user, you'd need either separate cubes per consumer ("each role gets its own cube") or you'd need to migrate to a cube technology that supports row-level security.

Sergey thought there might be cube-level filtering settings that allow restricting visible cells per user (potentially through dimensional security), but he wasn't sure. Worth checking.

### The cloud-migration question — short answer: not piecemeal

Val asked whether they could move just the cube to cloud while leaving CassDB and Wahit (the legacy intermediate casino-host application) on-prem. Dmitri Kovalchuk: theoretically possible, but you'd need to expose the on-prem CassDB to the cloud cube — punching the firewall and creating a lot of network/security overhead.

Andrei Bosik: data volumes aren't that bad — the cube doesn't refresh from scratch every 30 minutes; it incremental-loads. Maybe a VPN tunnel between cloud and on-prem could carry it. But Andrei also raised the broader question: should they even keep the OLAP cube architecture, or move to something else entirely?

Val's framing: **piecemeal migration of a 10-year-old architecture is not migration — it's stitching.** If they're going to cloud, they migrate the whole stack — CassDB, Wahit (which Val confirmed mid-meeting is a "Walleria Host" intermediate app where machines push data via certs, before periodic batch into the main casino DB), the cube, and the auth layer. Anything else creates worse problems.

The team converged on this: full migration or none.

### Cloud cost estimate — nobody knows the number

Andrei: critical first step is sizing the cloud bill. Could be $100/month, could be $10K/month. The team has no current data point. The MS SQL → cloud SQL Server license alone is "very expensive" per Andrei and Dmitri Kovalchuk. Migrating to PostgreSQL is a viable alternative path that would cut that cost meaningfully — Postgres can run as self-hosted cloud or as a managed service.

Val: "I'm 75% confident MS SQL → PostgreSQL via Claude Code is doable, painlessly, and that PostgreSQL is the better long-term answer." Dmitri Kovalchuk pushed back: not painlessly — significant time. Setting up the infra (a couple of servers, network) via Claude Code is roughly a week, but the software-side configuration (data migration, SQL→PostgreSQL syntax, stored procedures, app changes) takes longer.

Dzmitry: PostgreSQL would be cheap, but they'd lose LDAP auth — would need a new auth solution. Andrei clarified: with cloud move, LDAP → Microsoft Entra ID (formerly Azure AD) becomes the auth target via SSO/SAML. Val confirmed.

### Architectural framing — ex-CMS plus new POS, both must converge

Val reaffirmed (consistent with earlier conversations): JVL can't look at CMS in a vacuum — it's now "ex-CMS plus new POS." Both architectures need to be designed jointly, on paper first, then migrated. The cloud move and the OMNI 2 redesign converge at the top.

### Claude Code-driven migration

Val argued throughout that Claude Code substantially de-risks the migration. He works with it daily ("10 prompts a day") — has Claude Code build dashboards, compose summaries, generate scripts. He believes:
- Each engineer can have ~5 personal Claude-driven scripts to do dashboards
- MS SQL → PostgreSQL conversion is largely automatable
- Setting up cloud infra (Postgres instance + servers + networking) is roughly one week of Claude-Code-assisted work

Dzmitry raised the implementation reality: someone still has to write/own/review the scripts; the team can't fully outsource judgment to Claude. Val agreed — engineers remain the specialists, just doing less line-by-line typing.

Val also referenced his **"Constant Diamond Loop"** — the persistent Claude-driven knowledge system on his computer where he accumulates all of this thinking. He repeated his recommendation that the team build their own.

### Wahit / Walleria Host — what it is

Mid-meeting clarification (since Val didn't fully remember what "Wahit" stood for): Walleria Host (W-host) is the intermediate application all machines connect to via certificates. It pre-processes data, then periodically dumps it into the main casino DB. It's a buffering layer so the machines don't directly pound the production DB. Val confirmed he understood; the migration plan needs to carry this layer too.

### The agreed plan and assignments

Val's framing: take a week, produce documents, no code yet. He asked each participant to verbally state their undertaking ("undertaking" — Val asked Andrei for the Russian word; Andrei suggested "we, the undersigned"). Val will compile the document from the transcript.

The plan that emerged:

**1. Current-state architecture diagram (Dmitri Kovalchuk):** produce a block diagram of the *current* CassDB / Wahit / cube infrastructure, as it stands today, no optimization. Just the as-is. Useful as the canvas everyone reasons against.

**2. Cloud cost estimate as-is (Andrei + Dmitri Kovalchuk):** assume the as-is architecture is lifted-and-shifted to cloud. What does it cost per month? Two scenarios:
   - Scenario A — keep MS SQL on cloud (likely expensive)
   - Scenario B — migrate to PostgreSQL (managed-service or self-hosted), keep everything else equivalent

**3. Production-side migration estimate (Sergey + Dzmitry):** what's involved in migrating the CMS / production codebase straight-line to cloud, no optimization. Codebase is roughly modern (frameworks need version bumps), migration of stored procedures and SQL scripts is moderate (depends on target DB), authorization layer rewrite (LDAP → Microsoft Entra) is a known-cost item.

**4. Reconvene next Monday** (~March 30).

### Closing — short-term MCP path remains in scope

Val's concluding framing: while the cloud migration is being scoped, the **short-term** answer for the next ~6 months is to connect MCP directly to the existing on-prem cube, with whatever auth gate is feasible. This unblocks Val's day-to-day BI need without blocking the longer architectural redesign. The team didn't disagree; they just need to validate the security model for that direct MCP→cube connection (which auth layer, exposed how, with what scoping).

## Decisions Made

- **Drop Tableau / Microsoft Power BI as JVL's go-forward BI path.** Val sees little benefit; team didn't push back. (Decided by Val.)
- **Drop the Excel-as-bridge pattern entirely** (manual files, hardcoded credentials, casino-specific .xlsx files). It's insecure, doesn't scale, and adds maintenance burden. (Decided by Val with team consensus.)
- **Short-term BI access (~6 months): MCP connects directly to the existing on-prem OLAP cube** with whatever auth is feasible. Specific auth design TBD but must not be wide-open. (Decided by Val.)
- **Long-term direction: full migration of the CMS stack — CassDB + Walleria Host + cube — to cloud, all together, not piecemeal.** Architecture-first design before any code. (Decided by Val with team agreement.)
- **Target DB on cloud: PostgreSQL preferred over MS SQL Server** (subject to cost validation). MS SQL Server licensing on cloud is "very expensive." (Strong preference from Val and team.)
- **Auth migration: LDAP / Active Directory → Microsoft Entra ID (cloud SSO via SAML).** (Decided by Val and Andrei.)
- **Architectural design happens jointly with the new POS / OMNI 2 work** — CMS cannot be redesigned in isolation. (Decided by Val.)
- **One-week scoping pass with three deliverables, then reconvene next Monday** to make the actual go/no-go decision on the cloud migration. (Decided by Val with team agreement.)
- **Claude Code is the assumed force multiplier for the migration** (DB conversion, infra automation, script writing). (Decided by Val.)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Dmitri Kovalchuk | Produce a block-diagram of the current CassDB / Walleria Host / OLAP cube infrastructure as it is today (no optimization, no redesign — just the as-is canvas) | Next Monday (~Mar 30) | High | Becomes the reference everyone reasons against; gates the migration estimate |
| 2 | Andrei Bosik + Dmitri Kovalchuk | Produce a cloud-cost estimate for lift-and-shift of the as-is architecture, in two scenarios: (a) keep MS SQL on cloud, (b) migrate to PostgreSQL (managed or self-hosted) | Next Monday (~Mar 30) | High | Need a real $/month number — could be $100, could be $10K. Decision-gating |
| 3 | Sergey Tsimanov + Dzmitry Chudzinau | Production-side migration estimate: framework version bumps, SQL/stored-procedure migration scope, auth-layer rewrite (LDAP → Microsoft Entra), code touchpoints. Straight-line, no optimization | Next Monday (~Mar 30) | High | Sizes the engineering effort, not the infra cost |
| 4 | Dzmitry Chudzinau | Validate whether OLAP cube supports per-user role-based filtering (cell-level / dimension-level security) so MCP-to-cube can be role-gated without per-user separate cubes | TBD | Normal | Critical for the short-term MCP path |
| 5 | Dzmitry Chudzinau | Validate whether Excel-via-cube auth via Microsoft 365 SSO is a real flow or a dead end (Val suspected possible; team thought not) | TBD | Low | Settles a lingering disagreement; if dead, fully closes the Excel path |
| 6 | Val Levitan | Compile the meeting transcript into a documented version of these undertakings and circulate | TBD | Normal | Val explicitly committed to do this from the transcript |
| 7 | Val Levitan | Schedule the follow-up meeting for next Monday (~Mar 30) | Soon | Normal | Already promised in meeting close |

## Engineering Signals

### Confirmed Signals

- **ADR — Drop Tableau and Microsoft Power BI as the BI access path forward.** No longer worth maintaining; usage has collapsed (only Val and possibly Juan still consume Tableau).
- **ADR — Drop Excel-as-bridge to cube.** Manual, insecure, casino-specific files don't scale, hard-coded credentials. Pattern is end-of-life.
- **ADR — Short-term: MCP connects directly to the on-prem OLAP cube.** ~6-month bridge until full cloud migration. Auth design TBD but must not be wide-open.
- **ADR — Long-term: full CMS stack migration to cloud, all-or-nothing.** CassDB, Walleria Host, cube, auth — all migrated together, no piecemeal. Piecemeal creates worse problems than full move.
- **ADR — DB target on cloud: PostgreSQL** (preferred over MS SQL Server on cost grounds). Subject to cost validation in the one-week scoping.
- **ADR — Auth migration: LDAP/Active Directory → Microsoft Entra ID (cloud SSO via SAML/OIDC).**
- **ADR — Claude-Code-assisted migration.** Used both for infra setup (servers, networking) and for code/SQL conversion. Val: "MS SQL → PostgreSQL via Claude Code, 75% confident it's straightforward."
- **ADR — Architecture-first discipline.** No migration code is written until current-state diagram, cost estimate, and production-side estimate are all in hand. Confirmed at next Monday's reconvening.
- **CAP — Cloud-resident OLAP cube + role-based access via Microsoft Entra SSO** (target capability for the migrated stack).
- **Solution — Claude-driven personal scripts for engineers** (Val: "5 personal scripts each — that's enough for most BI needs"). Reduces dependency on Tableau/dashboard tooling.

### Suspected Signals

- **Possible REQ — Per-consumer / per-casino role-based data filtering on the cube** (e.g., Colombia operator only sees Colombia data). Today this is done via separate Excel files; the cloud / MCP design needs an explicit answer. Should this be a formal requirement? *(Val — REQ candidate?)*
- **Possible CAP — VPN tunnel between cloud cube and on-prem CassDB** as a transitional pattern (Andrei raised it). May or may not survive the "no piecemeal" decision; reserved if the full-migration timeline drags. *(Val — CAP candidate or transitional only?)*
- **Possible ADR — Move from OLAP-cube technology to a different analytical store** entirely (Sergey raised it: "should we even keep cubes?"). Not decided. The team's current default is to keep cube architecture in cloud; Sergey's question is open. *(Val — ADR candidate to explore?)*
- **Possible REQ — MCP UX pattern for stateful query selections** (remembered filters, named views, persistent context across prompts) so MCP becomes ergonomic enough to replace dashboards. Not formalized. *(Val — REQ candidate?)*

## Open Questions

- What is the cloud cost as-is? Until Andrei + Dmitri produce the estimate, the migration decision is unmade. Could be cheap, could be prohibitive.
- Can the OLAP cube support per-user / per-dimension role filtering, or do we need separate cubes per consumer? Dzmitry to investigate.
- For the short-term MCP-to-cube path, what auth gate is feasible without exposing the cube wide-open? Open design question.
- For the long-term cloud move, is there a hybrid pattern worth considering (cube in cloud, CassDB on-prem with VPN tunnel) if full migration cost is too high? Tentatively rejected by Val ("no piecemeal") but reserved if cost forces it.
- Migration timeline overall — Val asked but no number was committed. Andrei: "depends entirely on the cost estimate."
- Does PostgreSQL on cloud cleanly handle the existing stored procedures / SQL feature set? Sergey + Dzmitry to assess.

---
*Processed from Teams transcript on 2026-04-25*
*Source meeting: Data_Access_Strategy-March-23-2026 (Teams recording)*
*Stale-meeting processing — no email drafts, no calendar reminders, no follow-up actions dispatched per Val's standing feedback (Mar 23 → Apr 25 = 33 days).*
