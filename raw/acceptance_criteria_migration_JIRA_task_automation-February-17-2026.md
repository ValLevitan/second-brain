**Acceptance Criteria Field Migration**

Task Brief & Jira Feature Draft

Based on Aaron Bockelie consultation --- February 16, 2026

Prepared for Val Levitan, President, JVL Systems

# PART 2: Jira Feature & Stories (Draft --- Pending Val's Approval)

*The following is a draft of the feature and its stories to be created under IP-807. This will NOT be posted to Jira until Val explicitly confirms.*

## Feature: Migrate Acceptance Criteria Custom Field to Issue Descriptions

**Parent: IP-807**

**Description:**

When JVL's Jira instance was set up approximately five years ago, acceptance criteria was placed in a dedicated custom field separate from the issue Description. At the time, this was the correct decision: the only way to extract structured data from Jira programmatically was through the API, and separate fields ensured clean, predictable data retrieval. There was no AI or natural language processing available to intelligently parse a combined text field.

With the introduction of AI and the Model Context Protocol (MCP), this architectural choice has become a liability rather than an asset. AI agents connected via MCP can now read a single Description field and intelligently distinguish context from requirements from acceptance criteria --- without needing separate database fields. Meanwhile, the separate custom field creates unnecessary complexity: every MCP integration must be explicitly configured to address a non-standard field, team members must check two places to understand the full scope of a task, and any new tooling requires custom setup to account for this field.

This feature consolidates all acceptance criteria into the Description field, preserving historical data while simplifying the issue structure. The migration follows a two-track approach: completed issues receive an automated merge with no manual review, while active and future issues (In Progress, To Do, Backlog) are reviewed by team leads after migration to ensure the combined text reads correctly. Upon completion, the Acceptance Criteria custom field will be retired and permanently removed from Jira.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  Every issue across all JVL Jira projects that had content in the Acceptance Criteria custom field now has that content appended to its Description field, separated by a clear visual marker.

<!-- -->

1.  A backup of all original Acceptance Criteria data exists in an accessible location (CSV and JSON export) created before any modifications were made.

2.  All active issues (In Progress, To Do, Backlog) have been reviewed by the responsible team lead to confirm the migrated text reads correctly within the Description.

3.  The Acceptance Criteria custom field has been removed from all Jira screens, workflows, and field configurations.

4.  The Acceptance Criteria custom field has been permanently deleted from Jira, with Val's explicit confirmation obtained before deletion.

### Story 1: Extract and Back Up All Acceptance Criteria Data

**Description:**

Before making any changes, extract a complete snapshot of every issue that has content in the Acceptance Criteria custom field. This export serves as the safety net for the entire migration. The export must include: issue key, project, status, current description preview, and the full acceptance criteria text. Save this in both CSV and JSON formats to a shared location accessible to the team.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  A CSV and JSON file exist containing all issues with populated Acceptance Criteria fields.

<!-- -->

1.  The export includes: issue key, project key, current status, description preview, and full acceptance criteria text.

2.  The files are stored in a shared, accessible location (Confluence page or shared drive) and the location is communicated to Val.

3.  A count summary is provided: total issues exported, broken down by project and by status category (active vs. completed).

### Story 2: Migrate Acceptance Criteria into Description for All Issues

**Description:**

Run the migration script against all JVL Jira projects. For each issue that has content in the Acceptance Criteria custom field, append that content to the end of the existing Description field. Use a clear visual separator (horizontal rule and heading) so it is obvious where the original description ends and the migrated acceptance criteria begins. Process in batches to avoid Jira API rate limits. Log every issue that was updated and any that failed.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  Every issue with a populated Acceptance Criteria field has had its content appended to the Description.

<!-- -->

1.  Migrated content is visually separated from the original description with a horizontal rule and the heading "Acceptance Criteria (Migrated from legacy field)."

2.  A migration log exists listing every issue key that was updated, along with a success or failure status.

3.  Any failed updates are documented with the error reason for follow-up.

### Story 3: Generate Review Report for Active Issues

**Description:**

After migration, produce a filtered report containing only issues that are currently active or upcoming (In Progress, To Do, Backlog, Open, or equivalent). This report will be distributed to team leads so they can verify the migrated acceptance criteria reads correctly within the description. Completed issues do not require review --- we accept the automated merge as-is for historical tasks.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  A CSV report exists listing only active and future issues that were migrated, with columns: issue key, project, status, assignee, summary, and a direct link to the issue.

<!-- -->

1.  The report is distributed to the relevant team leads with clear instructions to review each issue on their list.

2.  A tracking mechanism exists (checkbox column or similar) so team leads can mark issues as reviewed.

### Story 4: Team Lead Review of Active Issues

**Description:**

Team leads review every issue on the active-issues report from Story 3. For each issue, confirm that the migrated acceptance criteria text reads correctly within the description and still makes sense for the work ahead. If adjustments are needed (reformatting, clarifying, removing duplicated content), make them directly in the issue. Mark each item as reviewed on the tracking sheet.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  Every issue on the active-issues report has been opened and reviewed by the responsible team lead.

<!-- -->

1.  Any issues requiring adjustment have been edited directly in Jira.

2.  The tracking sheet shows 100% of active issues marked as reviewed.

### Story 5: Retire and Delete the Acceptance Criteria Custom Field

**Description:**

Once the team lead review is complete and all active issues are confirmed, remove the Acceptance Criteria custom field from all Jira screens and field configurations. Then delete the custom field itself. This is the final irreversible step --- it completes the simplification that makes JVL's Jira instance cleaner for all future MCP and AI integrations. This step should only be executed after explicit confirmation from Val.

**Acceptance Criteria --- How This Will Be Accepted as Done:**

1.  The Acceptance Criteria field has been removed from all Jira screens and field configurations.

<!-- -->

1.  The Acceptance Criteria custom field has been permanently deleted from Jira.

2.  Val has explicitly confirmed the deletion before it was executed.
