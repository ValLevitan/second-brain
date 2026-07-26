# Jira Custom Fields Cleanup — Action List
**Meeting:** IT Custom Fields Alignment
**Date:** February 20, 2026
**Participants:** Val Levitan, Dmitri Kovalchuk

---

## Context

JVL's Jira instance currently has **165 custom fields**, of which 94 are system-protected (cannot be deleted). This meeting addressed the remaining fields to reduce clutter and simplify the MCP integration being built by Aaron Bockelie.

**Safety note agreed upon:** Deleted fields go into a 60-day recycle bin. Values are preserved and can be fully restored within that window. Dmitri also created a sandbox snapshot of today's state as an additional safety net.

---

## Decisions Made

### 1. Cancel Linksee Plugin Subscription — $40/month savings
- **Action:** Dmitri to cancel the Linksee ("Linx Fields") plugin subscription.
- **Reason:** The plugin created 5 custom fields. Ira (and others consulted) confirmed they do not use these fields. Jira's built-in tools provide the same functionality.
- **Fields affected:** 5 Linksee fields → **delete**.

### 2. Delete Jira Product Discovery Fields (~35 fields)
- **Action:** Dmitri to delete the two Jira Product Discovery projects (the "Example Discovery" project and the "MD/EXP" project created by Aaron).
- **Reason:** These projects were created during a trial of an Atlassian product that JVL never adopted. The 35 duplicate/associated fields will be automatically removed when the projects are deleted. Any that don't auto-delete can be batch-removed.
- **Fields affected:** ~35 Product Discovery fields → **delete**.

### 3. Delete 12 Potentially Unused Fields
- **Action:** Dmitri to delete the 12 fields currently showing zero usage across all screens and projects.
- **Reason:** No activity recorded. Confirmed with field owners (Yulia Aksamit and others) that any apparent "use" was accidental clicks with no actual values entered.
- **Fields affected:** 12 fields → **delete**.

### 4. Delete 3 Fields from Jira Service Management (from a set of 16)
- **Action:** Dmitri to delete fields #12, #14, and #15 from the JSM field group.
- **Reason:** These 3 fields reference legacy "Assets" configurations from previous iterations of the setup. They likely contain no meaningful data.
- **Fields remaining:** 13 JSM fields stay as-is for now.
- **Fields affected:** 3 fields → **delete**.

### 5. Move "Acceptance Criteria" from Custom Field to Description
- **Action:** Dmitri to remove the "Acceptance Criteria" custom field (Exceter/Eteria) and migrate that content into the standard **Description** field using an `.md` template format.
- **Reason:** Val's reasoning — since the team interacts with Jira through the MCP/Claude integration, data should live in the standard, widely-visible Description field rather than a narrow custom field. This makes it accessible to AI queries without a rigid, specialized interface.
- **Timeline:** Not today. To be scheduled by Dmitri.

---

## Pending Review (Next Step — Not Yet Decided)

### 6. Audit the 26 "Active" Fields (Used at Least Once in Last 12 Months)
- **Action:** Dmitri to go through all 26 fields that showed activity in the past year and assess whether each one is truly necessary or can be replaced by a standard Jira field.
- **Val's preliminary observations from the call:**
  - "Date Picker 6" (due date variant) — likely redundant; standard due date field should be used instead.
  - "Planned Start" — likely not needed.
  - Story Points fields #22 and #23 — Val believes JVL does not use these.
  - "Workaround" field (#26) — never filled in; check with Irina before deleting (relevant if used for bug tracking).
- **Dmitri's approach:** For each field in question, pull all issues where the field has any value, review actual usage, then make a recommendation.

---

## Ongoing Policy — Agreed Going Forward

- **Minimize custom fields.** Be very conservative about creating new ones. The goal is the smallest possible set of fields that are genuinely in use.
- **No label sprawl.** Labels (free-text tags) were discussed and flagged as a risk — they accumulate duplicates and misspellings. Agreed that structured custom fields (with controlled values) are preferable to open-ended labels where filtering matters.
- **AI-assisted governance (future consideration).** Val suggested periodically running a Claude prompt to surface newly created labels and flag potential duplicates or misspellings for Juan (or Ira) to review. Not a formal commitment yet — noted as a future option.

---

## Timeline / Schedule

| Action | Owner | Target |
|---|---|---|
| Cancel Linksee subscription | Dmitri | Next week |
| Delete 5 Linksee fields | Dmitri | Next week |
| Delete ~35 Product Discovery fields (via project deletion) | Dmitri | Next week |
| Delete 12 unused fields | Dmitri | Next week |
| Delete 3 JSM fields (#12, #14, #15) | Dmitri | Next week |
| Prepare work schedule and share with Val | Dmitri | Beginning of next week |
| Audit 26 active fields and make recommendations | Dmitri | TBD — Dmitri to propose timeline |
| Migrate Acceptance Criteria to Description field | Dmitri | TBD — after field audit |

> **Note:** Dmitri confirmed he will not rush this work — accuracy matters more than speed given the risk of irreversible data loss after the 60-day recycle window.

---

## Summary Totals (Fields to Be Deleted in Round 1)

| Category | Fields |
|---|---|
| Linksee plugin fields | 5 |
| Jira Product Discovery fields | ~35 |
| Unused/zero-activity fields | 12 |
| Jira Service Management (3 of 16) | 3 |
| **Total Round 1** | **~55** |
