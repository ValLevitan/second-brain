# Meeting Summary — Clayton / Val / Lena: Jira-MCP Design Workflow
**Date:** June 10, 2026, ~2:01 PM Eastern
**Duration:** ~33 minutes
**Attendees:** Clayton Chancey (Precipia — external), Lena Zhukova (JVL), Val Levitan (JVL)

## Summary

Working session to unblock Clayton's MCP server work for the design team's Jira. Clayton needed answers to finish a feature; Lena and Val gave them, plus some new requests.

**Game-name recognition.** Lena said the current MCP/Claude tooling often gets game names wrong; her example, "Fire and Ice," gets transcribed as "Fire and Eyes." She does not want to load every brand name into a vocabulary list (too many, and it is temporary). Clayton will fix it with prompting so the tool checks existing Jira names first instead.

**Screenshots into Jira.** Lena wants to paste 5 or 6 screenshots of review comments (from her chats with Michael, the game producer) and have Claude sort them into proper issues, ideally attaching the screenshot images to the issues. Clayton confirmed Claude reads text from images well and will add prompting so images get attached automatically when appropriate.

**Timeline/plan dates.** Lena wants the MCP to populate and read dates on tickets from the Gantt/plan. Clayton confirmed the plan maps to the native start date and due date fields (not "target start" / "target date," which are empty). Dmitri Kovalchuk deliberately hid these fields inside tickets so people only change dates on the timeline view. Clayton has what he needs; he will look up the custom field IDs.

**Status changes.** Confirmed the MCP can already update ticket status (same permission as creating tickets).

**Jira hierarchy change.** Val is moving to a Capability, Feature, Story hierarchy, with Capabilities linked to many Requirements. A capability is "done" when its set of features is delivered; capability becomes a layer of the Gantt chart. Two Jira projects already exist: Requirements (REQ) and Capabilities (CAP). Features and stories stay the same. Val drew the parallel to dev work: a feature becomes a feature branch / deliverable artifact in GitHub, and the design group is building the same model (a feature is a set of artifacts, with ADRs and a data contract per repo). Everyone acknowledged "feature" now collides in meaning (dev branch vs. design deliverable vs. PM tracking unit) but accepted it as normal Agile complexity.

**Not yet on GitHub.** Lena noted that even after the hierarchy changes, the design team will keep working in SVN (not GitHub) for several more months. Changing the hierarchy is the management foundation, not immediate GitHub adoption.

**AI attribution.** Val had asked whether Jira could show when a status was changed by AI. Clayton's solution: actions run under the requesting person's own account with a prepended note ("AI action, requested by [name]"). The alternative, a dedicated bot/service account, would break native Jira search for who drove the change. Val decided it is not worth it.

**Side note.** Clayton and Aaron Bockelie (both now at Precipia, an Anthropic partner) attended an Anthropic event and won the closing hackathon against Deloitte/PwC/McKinsey-type firms.

## Decisions Made

- **AI attribution: no bot account.** MCP actions run under the requesting user's account with a prepended "AI action / on behalf of [user]" line. Reason: a service account would break native Jira search for the real driver; not worth the complexity. Already built; Clayton just flips the feature flag to deploy. (Decided by Val)
- **Date fields confirmed.** The plan/Gantt maps to the native start date and due date fields, not "target start"/"target date." (Confirmed by Clayton, endorsed by Val/Lena)
- **Hierarchy = Capability, Feature, Story**, Capabilities linked to many Requirements; capability done when its features are delivered. (Decided by Val)
- **Screenshots into Jira issues with attached images** is the agreed workflow for review comments. (Val/Lena/Clayton)
- **Design team stays on SVN** for several more months despite the hierarchy change. (Lena)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Resolve which GitHub repo the ADRs go into (discuss with Andrei) and send Clayton the link | ~June 17 | High | Blocks Clayton; a "knowledge ADRs" repo exists in JVL Core but is unconfirmed |
| 2 | Val | Arrange Clayton's access to the Requirements (REQ) and Capabilities (CAP) Jira projects | ~June 17 | High | Blocks Clayton's feature work; email to Dmitri Kovalchuk sent June 10 |
| 3 | Val | Meet with the game design team to define the tagging convention (tag = "game design" + game name) for capabilities/requirements | TBD | Normal | Needed before tags can be applied |
| 4 | Clayton | Finish the timeline/plan feature (MCP reads/writes start date + due date fields), test with the group, roll out | ~June 17 (next meeting) | High | Main deliverable; "just changing a few fields in scripts I already wrote" |
| 5 | Clayton | Fix game-name recognition: prompt the MCP to check existing Jira names before creating, to resolve transcription ambiguity | TBD | Normal | "Fire and Ice" mis-transcribed as "Fire and Eyes" |
| 6 | Clayton | Add screenshot-to-Jira capability: sort pasted review-comment screenshots into issues and attach the images | TBD | Normal | Lena's review-comment workflow with Michael |
| 7 | Clayton | Message Val and Lena as MCP tools become ready between now and next week | ~June 17 | Normal | — |

## Open Questions

- Which exact GitHub repo for ADRs (pending Val + Andrei).
- Visual representation of requirements/capabilities: Val noted an Atlassian add-on (a "spider web" / Big Picture-style view) but said the visual is currently missing.
- The "feature" terminology collision was acknowledged but consciously left unresolved (accepted as Agile complexity).

---
*Processed from Teams transcript on June 10, 2026*
*Source meeting: Clayton-Val-Lena Meeting Series-June-10-2026*
