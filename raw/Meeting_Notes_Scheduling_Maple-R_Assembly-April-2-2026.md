# Meeting Summary — Scheduling Maple-R Assembly
**Date:** April 2, 2026, 1:05 PM Eastern
**Duration:** approximately 1 hour 46 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Genadi Peari

## Summary

The meeting focused on building out and refining the Jira schedule for the **Maple-R retrofit project** — the code name for a cabinet retrofit destined for Texas (~80 units total). The team worked live in Jira Plans throughout the session, creating tasks, linking dependencies, and setting dates.

### Jira Structure and Task Linking

Val opened by asking to see the current Jira schedule. The main umbrella items are **IP-10-33** (application software for Maple nat retrofit) and **IP-10-47** (electromechanical part). Val asked to link these two items so that a single schedule view would show the full picture. Irina initially suggested they could run in parallel as independent tracks, but then acknowledged that Elizabeth cannot launch the software version assembled under IP-10-33 until IP-10-47 (specifically IP-10-45) is completed — confirming the dependency. Val pushed to have them linked in Jira accordingly.

The team also reviewed **HFM-477**, which is the parent feature containing the hardware integration stories. Val had created user stories under HFM-477 and asked the team to verify dates. Genadi confirmed the schedule looked correct, with April 22 as the target completion. Val noted that some linked tasks under Genadi's items had dates that caused scheduling conflicts — one task was set to April 14 while its predecessors were earlier — and asked Genadi to fix the dates and save changes.

### Prototype Cabinet Assembly (HFM-482)

A key gap was identified: there was no Jira task for Elizabeth to physically assemble prototype cabinets. Genadi raised this, noting that Elizabeth has one cabinet already (he spoke with her yesterday) and needs to assemble a prototype even before the full software is ready. Pavel pointed out that the sooner Elizabeth assembles a unit, the better — if there are touchscreen inversion issues or other hardware problems, early discovery is critical.

The team created **HFM-482** — "Assemble 2 Maple cabinets" — assigned to Elizabeth, starting today (April 2) with an expectation that she'll have something assembled by Monday (April 7). The acceptance criteria for this task are strictly hardware: a component list (BOM) defining what must be physically present in the cabinet. Val directed Genadi to write these acceptance criteria using his existing BOM document. Pavel showed Genadi how to use Jira's "Improve Description" AI feature to convert a component list into proper acceptance criteria format.

### Alpha Release Integration Test (HFM-483)

After HFM-482 (physical assembly), the next step is **HFM-483** — installing the alpha software release on the assembled cabinet and running basic validation. This task is linked to **ST-56-45** (a software story under IP-10-33) as a dependency — the alpha software must be ready before Elizabeth can test it.

The acceptance criteria for HFM-483 include: software installs from flash drive, upper monitor displays correctly, touchscreen calibrates and responds, no display offset or overlap between monitors, and basic button functionality works. Elizabeth's feedback from this test will determine whether the software team needs to fix issues before the production release.

Pavel initially created HFM-483 under the wrong parent (HFM-483 appeared under a different feature), and the team corrected the linking during the meeting. Irina confirmed the final structure: HFM-482 (assemble) → HFM-483 (alpha test) → continue to production release, with HFM-483 also linked to ST-56-45 from the software track.

### Label/Roll Printer Integration (HFM-478)

Val questioned why HFM-478 ("Integration of label and roll printer") was a single story spanning 2 weeks. Genadi explained it involves: designing a mounting bracket, ordering the bracket, possibly changing the harness, adjusting button board location, and physical installation. Val argued that a 2-week story should be broken down — it's either multiple stories or sub-tasks. After extended discussion about the right level of detail, the team agreed to:

- Keep HFM-478 as a single story but compress the timeline to 1 day (April 7–8)
- Add **5 sub-tasks** underneath it covering: bracket design, bracket ordering, harness modifications, component relocation, and final installation
- Move the ordering lead-time concern into the existing "Parts Ordering" track rather than bloating HFM-478

Val walked Genadi through the sub-task creation process in Jira, emphasizing that sub-tasks are visible under the parent in the Jira plan view. Genadi confirmed he could see the sub-tasks after they were created.

### Workflow and Transparency Discussion

A significant portion of the meeting was Val explaining to Genadi why detailed task breakdowns matter. Val emphasized that with a distributed team working across time zones and languages, visual schedule alignment is essential. He noted that he has been raising this issue for roughly 5 years. Val explained that the goal is not micromanagement but transparency — when tasks are broken down and statused, Val doesn't need to call and ask for updates; he can simply look at the board. Val also pointed out that Claude (AI) can now help create tasks from verbal descriptions, reducing the typing burden that Genadi finds friction-heavy. Genadi can dictate in Russian or Hebrew and have tasks generated automatically.

### Component Ordering

Genadi raised the question of order quantities. Val confirmed all Maple units are destined for Texas (~80 total). Genadi listed items that need ordering: brackets, relay panels, button panels, button inserts/legends. Val decided to start with an initial order of **20 sets** rather than the full 80, then order the remainder. Genadi noted that Elizabeth should check what she already has on hand and identify what needs to be purchased. The button legend files are already prepared — Genadi will print legends and Elizabeth will insert them.

### Production Machine Assembly

After the alpha test passes, the team needs Elizabeth to begin production assembly. Pavel added a new task under HFM-477 for **assembling the first 10 production machines**. The initial date proposed was April 18, but Irina flagged it as a Saturday. The team adjusted to **April 21** as the target for the first 10 production machine release. Pavel noted the timeline might be achievable earlier if there are no issues, but Irina cautioned that this isn't the only project the team is testing. Val confirmed he's satisfied with April 21.

### Closing Actions

Val stated he needs to prepare a message to Elizabeth summarizing the published Maple-R schedule, highlighting her key milestones and emphasizing that she needs to begin production assembly now to hit the April 21 target for the first 10 machines.

## Decisions Made

- **All Maple-R units (~80) are destined for Texas.** Initial component order will be for 20 sets, not the full 80. (Decided by Val and Genadi)
- **HFM-482 created for Elizabeth to assemble 2 prototype cabinets**, starting immediately (April 2). Acceptance criteria = BOM component list. (Decided by team)
- **HFM-483 created for alpha release integration test**, linked to ST-56-45 as a dependency. (Decided by team)
- **HFM-478 (printer integration) compressed to 1 day (April 7–8)** with 5 sub-tasks for bracket design, ordering, harness, relocation, and installation. (Decided by Val and Genadi)
- **First 10 production machines targeted for April 21 release.** (Decided by Val, confirmed by team)
- **IP-10-33 and IP-10-47 to be linked in Jira** so the full schedule is visible in one view. (Decided by Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Prepare button legend print files and print legends for button inserts | April 7, 2026 | Normal | Needed for cabinet assembly; Genadi confirmed files are ready |
| 2 | Elizabeth [via Genadi] | Check what components she has on hand and identify what needs to be ordered for cabinet assembly | April 7, 2026 | High | Genadi spoke with her yesterday; she has one cabinet — needs to verify parts availability |
| 3 | Elizabeth [via Genadi] | Assemble 2 prototype Maple-R cabinets (HFM-482) | April 7, 2026 | High | Prototype assembly — early hardware validation before alpha software arrives |
| 4 | Val Levitan | Write a message to Elizabeth (via Claude) summarizing the published Maple-R schedule, highlighting her key milestones: HFM-482 (assemble 2 prototypes), HFM-483 (alpha test), and production assembly of first 10 machines by April 21. Emphasize that she needs to begin production assembly now to hit the April 21 target, as she is the critical checkpoint for machine release. | TBD | High | Elizabeth needs a clear, consolidated view of what's expected of her and the sequencing — the Jira plan is complex and this message distills her responsibilities |

## Open Questions

- **Which printer model for the Maple-R cabinet?** Either the Reliance or Phoenix printer, both made by Pyramid. Genadi needs to physically verify which model fits before finalizing the bracket design for HFM-478.

---
*Processed from Teams transcript on April 2, 2026*
*Source meeting: Scheduling Maple-R Assembly*