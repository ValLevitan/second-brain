# Engineering-Contractor Billability Rules

**Status:** Live (v1.4)
**Applies to:** Any contractor whose work product includes code or JIRA-tracked deliverables.

## Purpose

JIRA and GitHub are the authoritative records of engineering work. Every billable deliverable flows as **Feature → Stories → commits → pull request → merge into `main` → Feature closed by assignee → reporter resolves Feature Done (acceptance of delivery)**. The completion of a Feature is the minimum billing interval, and that completion must fit inside the billing period.

## Rules

1. **JIRA-assigned work only.** Invoices cover tickets assigned in JIRA to the contractor under their own Jira account. Pre-agreed principal/co-contractor arrangements are permitted.
2. **Feature ownership.** Once assigned, the contractor carries the Feature end-to-end. Feature-level reassignment is exceptional; Story-level reassignment inside an open Feature is ordinary grooming.
3. **No double-billing.** A Closed-Done Feature is billed once. Reassignment does not create a second billable event.
4. **Closed Features stay closed.** Follow-on work after close → open a new Feature. Follow-on work while still open → add a new Story under the existing Feature.
5. **Feature sizing.** Roughly 3–4 days of effort, decomposed into Stories sized in hours. Maximum 10–15 Stories per feature branch; larger scope splits into additional Features.
6. **Merge via PR only.** Every PR reviewed by Claude Code Pull Reviewer. Once merged to `main`, the assignee closes the Feature; the reporter then resolves it Done as acceptance of delivery.
7. **Completion inside the billing period.** A Feature is billable only in the period in which the reporter-Done acceptance occurs. Effort timing does not matter — the acceptance date does.
8. **No Story-level billing.** Stories are work-decomposition units for planning and tracking, not billing units.
9. **JIRA is the source of truth.** Tickets are not created, edited, or backdated after the fact to match an invoice.
10. **No ticket, no billing.** Billable work has a ticket opened beforehand by the reporter/manager, assigned to the responsible contractor, worked, reviewed, merged, and resolved Done by the reporter.
11. **Feature ↔ GitHub link.** Every Feature must carry, inside the JIRA ticket itself, a link to the corresponding GitHub repository (and, where applicable, to the feature branch and the merged PR). When a Feature is referenced on an invoice, that link must be identifiable inside the Feature — so any invoice line traces cleanly back to the code that delivered it.
12. **No DRAFT invoices.** Submissions must be non-DRAFT in the standard template with all required fields populated.

## What a billable line item looks like

Each line = one Closed-Done Feature whose reporter-Done date falls inside the billing period. Required: JIRA Feature key, description, reporter-Done date, merged-PR reference, in-scope assignee, hours (summed from the Feature's closed-Done Stories), rate, amount.

Not billable: closed Stories under an open Feature; in-progress or Request-Review Stories; unmerged branches; Features without reporter-Done acceptance; line items without a JIRA Feature key.

## Contractor obligations before submitting

1. Confirm each Feature: assigned in-scope, all Stories Closed-Done, branch merged via Claude-reviewed PR, Feature closed by assignee, reporter-Done acceptance recorded, acceptance date inside the billing period.
2. If something is off, raise it with the reporter/manager first. Invoice after the correction.
3. Use the standard template. Non-DRAFT. All fields populated.
4. Respect the billing-period boundary. Acceptance on the 1st of the next month belongs on next month's invoice.
5. Do not double-bill. Do not reopen closed Features or Stories.

## Reporter/manager obligations

Acceptance belongs to the reporter, not the contractor. Contractors do not self-accept. Feature-level reassignment is exceptional; it does not retroactively change past billing entitlement. Reopening closed Features or Stories is not the path for follow-on work. Creating backdated tickets to legitimise an invoice violates Rules 9 and 10.

## Cross-Month Double-Billing Check

Every invoice must be cross-checked against the contractor's invoices from the prior two billing periods. For each JIRA key on the current invoice, verify it does not appear on any earlier invoice. If a key recurs across months:

1. **Confirm no double-billing.** The same Feature billed Closed-Done in a prior period cannot be billed again. Rule 3 applies regardless of how many months apart the invoices are.
2. **Flag recurring open Features.** A Feature key appearing on multiple consecutive invoices without ever reaching Closed-Done status indicates incremental billing against an open Feature. This is a compliance gap: under Rule 7, a Feature is billable only in the period in which reporter-Done acceptance occurs. Hours logged against it in earlier periods are not separately billable.
3. **Cumulative exposure.** When a recurring key is found, sum the total hours and dollars billed against it across all periods. Include this in the reconciliation review.

This check is mandatory before authorizing payment. Findings are documented in the invoice approval remarks.

## Enforcement

Non-compliant invoices are **rejected**, **partially authorised**, or **parked for executive review**. Repeated non-compliance leads to renegotiation of the arrangement.
