# Meeting Summary — Cash Reporting Standardization

**Date:** April 28, 2026, 5:03 PM Eastern
**Duration:** ~22 minutes
**Attendees:** Val Levitan, Igor Donis, Cris Nacarino

## Summary

Val convened Igor and Cris to lock down a unified weekly cash reporting workflow across three artifacts that today live in different formats and folders: (1) the JVL **cash position consolidated** workbook, (2) the **weekly cash flow demand** workbook, and (3) the **vendor payment approval** workbook that Cris sends to Val. The driver is reducing Val's manual reconciliation effort and making the reports machine-readable (specifically, parseable by Claude/AI) so that each participant can independently verify totals.

**Identical reference points across reports.** Val instructed that cash position consolidated and weekly cash demand must publish on the same date — Monday — and must use identical reference points: same JVL account number (e.g., "772"), same standard account set, same totals at top and bottom of every table. The table layout itself is Igor's call ("I don't care what you decide"), but the anchor numbers must match. The rationale: when both reports carry the same numbers on the same date, AI can reconcile them trivially and Igor's manual workload drops.

**Approval workbook redesign — check marks, not colors.** Val wants the vendor approval workbook brought into the same standard. Today approvals are signaled by cell color; Val wants check marks instead, because "check marks could be picked up by artificial intelligence." Checked rows tabulate into a sum, and that sum must equal the corresponding totals in the cash position and cash demand reports. The approval workbook must also carry the same date and reference number as the other two reports — this is what makes three-way reconciliation possible.

**Approval timing relative to publication.** Igor flagged a sequencing concern: the approval Val signs is for *last week's* proposal, but the cash position and cash demand are the *new* Monday snapshot. Val confirmed this is correct — the approval ties to the prior week, the bank statement and cash demand are current week, and Val will reconcile across that one-week offset. For the first cycle of the new process, cash demand will be 0 because there's no prior-week approval yet — both Val and Igor agreed that's acceptable.

**Approval cycle cadence.** Val initially considered Wednesday for receiving payment proposals, then revised: Igor sends the payment proposal to Val on Monday, Val takes the week to approve it, forwards approval to Cris by Friday, and Cris incorporates it into the following Monday's cash position + cash demand publication.

**SharePoint storage — weekly folders.** Val asked where to keep these three reports. For now, SharePoint. The structure: per year, 52 weekly subfolders (Week 1, Week 2, … Week 52). When the year ends, start fresh next year. Each weekly folder contains all three artifacts for that week — cash position, cash demand, and vendor approval — together. Today is week 17 (April 28, 2026).

**Forecasting model — cash actual + cash committed.** Val sketched a forward-looking idea: the opening cash for next week should approximately equal closing cash this week, but not exactly because some committed payments won't have cleared yet. He proposed modeling this with two figures — "cash actual" and "cash committed" — so the next-week opening can be forecasted with an adjustment for outstanding commitments. Val wants to experiment with the logic before committing to a structure.

**Visual formatting standard.** Val complimented Igor's current visual work and asked him to formalize it into a JVL formatting standard. The proposed mechanism: take an existing Excel as input, prompt Claude to "develop a JVL formatting standard prompt" focused only on formatting, save the resulting prompt, and reuse it for every future JVL Excel report so all workbooks look identical. Constraint: numbers must be legible — not too small for Val to read.

**Each participant uses AI for their own checks.** Val closed the framing point: once the three reports share dates, reference numbers, account sets, and totals, Val will use Claude to verify "consolidated cash position equals weekly cash flow position, and approval totals equal what I have here." Igor and Cris can each use AI to check whatever they care about. The standardization unlocks independent verification by all three.

## Decisions Made

- **Cash position consolidated and weekly cash demand publish on the same Monday with identical reference points** (date, reference number, account set, top/bottom totals). Rationale: AI reconciliation. (Decided by Val)
- **Vendor payment approval workbook converts from color-based to check-mark-based**, with checked rows tabulating to a sum that must equal the cash position/demand totals. (Decided by Val)
- **Approval cycle:** Monday Igor sends proposal → Val approves through the week → Igor forwards to Cris by Friday → Cris integrates into next Monday's cash reports. First cycle has cash demand = 0 (acceptable). (Decided by Val and Igor)
- **SharePoint storage:** per-year folder with 52 weekly subfolders, each containing all three artifacts for that week. (Decided by Val)
- **JVL formatting standard** to be developed via a reusable Claude prompt and applied to every JVL Excel artifact going forward. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Igor | Reformat cash position consolidated and weekly cash demand workbooks so both share identical date, reference number, account set, and top/bottom totals; both published the same Monday. | First Monday after draft approval | High | Foundation for AI-reconcilable reporting. Blocks every other change in this meeting. |
| 2 | Igor | Convert vendor payment approval workbook from color codes to check marks; checked rows must sum to a total that equals cash position/demand totals; carry same date + reference number as the other two reports. | Same as #1 | High | Closes the three-way reconciliation loop with Val's approvals. |
| 3 | Igor | Adjust approval cadence: send proposal to Val on Monday, route Val's approval to Cris by Friday, Cris publishes both reports the following Monday. | Effective immediately | High | Sequencing locked; no rework needed once #1 and #2 are in place. |
| 4 | Igor | Set up SharePoint folder structure: `2026/Week_1 … Week_52`; place cash position, cash demand, and vendor approval together in each weekly folder. Today's slot is Week 17. | Before publishing the next cycle | Normal | Single canonical storage location for all three artifacts per week. |
| 5 | Igor | Use Claude to derive a "JVL formatting standard" prompt from an existing Excel; save it; apply it to all JVL Excel artifacts going forward. Numbers must remain legible. | Draft to Val for review | Normal | Visual consistency across every JVL Excel report. |
| 6 | Igor | Produce a first draft of the redesigned reports (cash position, cash demand, approval workbook with check marks, formatting standard applied) and send to Val for review. | TBD ("allow me time") | High | Val wants to iterate on the new format before it goes live. |
| 7 | Val | Experiment with logic for "cash actual" + "cash committed" forecasting model so next-week opening bank balance can be predicted with adjustment for outstanding commitments. | TBD ("let me play with it") | Normal | Self-assigned exploration; informs whether/how this gets added to the standard. |

## Engineering Signals

### Confirmed Signals

- **Solution — Check marks over colors for AI-parseable approvals:** Val explicitly chose check marks because "check marks could be picked up by artificial intelligence" while colors cannot. Checked rows tabulate; sum must match cash position/demand totals.
- **ADR — Shared identifier across three cash reports:** Cash position consolidated, weekly cash demand, and vendor payment approval must carry the same date and the same reference number. Rationale stated by Val: "if it has the same number, then AI is easy to reconcile."
- **CAP — Three-way AI-assisted reconciliation:** Each participant (Val, Igor, Cris) uses Claude to independently verify their slice. Val's check: "consolidated cash position is equal to weekly cash flow position, and my approval totals are equal to whatever I have here."
- **Solution — 52-week-per-year SharePoint archive:** Per-year folder with 52 weekly subfolders, each holding all three artifacts for that week.
- **Solution — Reusable formatting prompt:** Generate a JVL formatting standard prompt from an example Excel via Claude, save it, reuse on every future workbook.

### Suspected Signals

- **Possible CAP — Forward-looking cash forecast (cash actual + cash committed):** Val sketched a model where next-week opening = current-week closing minus uncleared commitments. Not yet defined; Val wants to "play with the logic" first.

## Open Questions

- Exact date when the new format goes live — depends on Igor's first draft being approved by Val.
- Whether the "cash actual + cash committed" model will be folded into the standard reports or kept as a separate analytical view — Val to decide after experimenting.

---
*Processed from Teams transcript on 2026-04-28*
*Source meeting: cash_status_cash_demand-April-28-2026*
