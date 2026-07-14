---
type: topic
title: JVL contractor billing process
date: 2026-07-13
aliases: [contractor billing, invoice process, jira billing rules, billability rules]
source-count: 1
---

# JVL contractor billing process

How JVL processes and authorises contractor invoices (absorbed 2026-07-13 from the `Contractors Control/_Standard/` rules; **rates/amounts redacted per §15.8**). This is the process JVL runs each month; the roster of who the contractors are is on [[wiki/topics/jvl-contractor-roster.md]].

## Submission standard

- A canonical invoice **template + guide** was rolled out **2026-02-11**; every contractor submits in that format. Standing exception: **Bulldozer / Inna Levitan (Chairman)** may submit PDF. [[raw/jvl_contractor_roster_2026_names-only.md]]

## Engineering-contractor billability rules (v1.4, approved 2026-04-19)

Applies to any contractor whose work product is code or JIRA-tracked deliverables. [[raw/jvl_contractor_billing_rules_v1.4_2026.md]]

- **Feature is the sole billable unit.** Stories are work-decomposition units, not billing units.
- **Reporter-Done is acceptance of delivery** — contractors do not self-accept; the reporter's Done resolution unlocks billability.
- **Completion must fall inside the billing period.** A Feature accepted Done outside the service month belongs on a different invoice; **no backdating**.
- **No double-billing** (a closed-Done Feature is billed once) and **no reopening** (follow-on work → new Feature/Story).
- **Feature-level reassignment is exceptional**, not routine — a contractor carries a Feature end-to-end.
- Every Feature must carry a link to its **GitHub repository** in the ticket.
- **Feature sizing target: 3–4 days** of work, ≤10–15 Stories per feature branch.
- A billable line = one Closed-Done Feature with: JIRA key, description, reporter-Done date, merged-PR reference, in-scope assignee. (Rate/amount columns exist on the real invoices but are held per §15.8.)

## Authorisation validation (per invoice)

- **HR file cross-reference:** the invoiced terms are compared against the contractor's signed agreement in `Initiatives/HR/Records/` (compensation section) — a **held** sensitive source, not ingested.
- **Manager confirmation:** if the contractor reports to a manager (e.g. [[wiki/people/andrei-klimovich.md|Andrei Klimovich]]'s reports), the manager's email approval must be on file.
- **Cross-month double-billing check:** a Feature key recurring across consecutive invoices without reaching Closed-Done flags a compliance gap.

## Sources

- [[raw/jvl_contractor_billing_rules_v1.4_2026.md]]
- [[raw/jvl_contractor_roster_2026_names-only.md]]
