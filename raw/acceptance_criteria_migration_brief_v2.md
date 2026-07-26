**Acceptance Criteria Field Migration**

Task Brief & Jira Feature Draft

Based on Aaron Bockelie consultation --- February 16, 2026

Prepared for Val Levitan, President, JVL Systems

# PART 1: Task Brief for Engineering Team

## Background: Why We Had a Separate Field

Approximately five years ago, when JVL's Jira instance was first set up, acceptance criteria was placed in its own dedicated custom field, separate from the issue Description. This was a deliberate architectural decision that made sense at the time.

The reasoning was straightforward: back then, the only way to programmatically extract structured information from a Jira issue was through the API, and the API works best when each piece of data lives in its own distinct field. If a script or integration needed to pull just the acceptance criteria --- without the description, without comments, without anything else --- it could query that one custom field directly. There was no AI, no natural language processing, and no way for an application to "read" a description and intelligently separate what was a requirement from what was context. Separate fields meant clean, predictable data extraction.

## Why We Are Merging It Now

The landscape has fundamentally changed with the introduction of AI and the Model Context Protocol (MCP). Today, an AI agent connected to Jira via MCP can read a single Description field and intelligently understand which parts are context, which parts are requirements, and which parts are acceptance criteria --- without needing them in separate database fields. The AI provides the human-like interpretation layer that did not exist five years ago.

Keeping acceptance criteria in a separate custom field now creates unnecessary complexity:

- MCP integrations must be configured to look at a non-standard custom field in addition to the standard Description, adding fragmentation and setup overhead.

<!-- -->

- Team members must check two places to understand the full scope of a task.

- Any new tool, integration, or AI agent must be explicitly taught about this custom field --- whereas every tool already knows how to read a Description.

By consolidating acceptance criteria into the Description field, we simplify the data model, reduce integration complexity, and make every issue self-contained in a single standard field that any tool --- AI or otherwise --- can work with out of the box.

## Guiding Principle for This Migration

> ***We accept mediocrity and incompleteness for the past. We focus on perfecting the future.***

Do not spend time verifying or cleaning up acceptance criteria on tasks that are already completed. The only tasks that warrant human review after migration are those that are still active or upcoming.

## Two-Track Approach

### Track A: Completed Tasks (No Review Required)

For any issue with a status of Done, Closed, Resolved, or any equivalent terminal status:

- The script appends the Acceptance Criteria field contents to the end of the Description field.

- A clear visual separator is used (horizontal rule and a heading reading "Acceptance Criteria (Migrated)") so the migrated content is visually distinct.

- No human review is needed. Whatever was in the field gets appended as-is.

### Track B: Active and Future Tasks (Review Required)

For any issue with a status of In Progress, To Do, Backlog, Open, or any equivalent active status:

- The same append operation runs automatically.

- A report is generated listing these issues for team leads to review.

- Team leads verify that the migrated acceptance criteria reads correctly within the description and still makes sense for the work ahead.

- If adjustments are needed, team leads make them manually in Jira.

## Step-by-Step Execution Plan

1.  **Identify the Custom Field ID.** In Jira Admin, navigate to Custom Fields and find the field named "Acceptance Criteria." Note its ID (it will look like customfield_10XXX). This is required for the migration script.

<!-- -->

1.  **Take a Backup.** Before running anything, export a full CSV and JSON dump of all issues that have the Acceptance Criteria field populated. This is the safety net. Store it in an accessible shared location (e.g., a shared drive folder or Confluence page).

2.  **Run the Migration Script.** The script (provided separately as Part 3) processes all issues across all projects. It appends the acceptance criteria to descriptions using a clear visual separator and runs in batches to avoid overloading Jira. Run it first in DRY RUN mode to preview, then switch to live mode.

3.  **Generate the Review Report.** The script produces a CSV file listing only the active and future issues (In Progress, To Do, Backlog). Distribute this list to the relevant team leads for review.

4.  **Team Lead Review (Active Tasks Only).** Team leads check each issue on the review list to ensure the migrated text reads correctly within the description. Fix anything that looks off. Mark each item as reviewed on the tracking sheet.

5.  **Retire the Custom Field.** Once all active tasks have been reviewed and confirmed, delete the Acceptance Criteria custom field from Jira Admin. This is the final step and requires Val's explicit confirmation before execution.
