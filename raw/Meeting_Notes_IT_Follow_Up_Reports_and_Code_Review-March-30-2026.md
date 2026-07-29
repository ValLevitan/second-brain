# Meeting Summary — Follow-up IT Tasks

**Date:** March 30, 2026, 11:02 AM Eastern
**Duration:** ~39 minutes
**Attendees:** Val Levitan, Andrei Bosik

## Summary

### GitHub Compliance and Branch Audit Reports

Andrei presented a new consolidated reporting system he built. All reports that were previously generated manually or through older methods have been migrated into a single GitHub repository. Reports are now auto-generated in GitHub and displayed as web pages. Andrei shared the link in Teams chat. The reports are currently in beta — some calculations may not be fully accurate yet, so they're being monitored.

There are two report types:

1. **Daily Compliance Report** — sent to developers in chat each morning. It tracks: whether there were commits to main, whether pull requests were used (vs. direct pushes), pull request size (current threshold: 400 lines — flagged if exceeded), how many days since last activity, and whether code review was done by someone other than the author. Val and Andrei walked through the report, noting that developers like Vladimir Samusenko and Zhenya Koretsky show clean compliance. The report flags self-approved PRs, though Andrei noted this is sometimes unavoidable for single-developer projects.

2. **Weekly Branch Audit Report** — generated on Mondays. This is the successor to the branch hygiene emails Andrei used to send manually. It categorizes "improper" branches into three sections:
   - **Section 1:** Jira feature status is Complete or Closed, but the GitHub branch still exists (not deleted).
   - **Section 2:** Branch has had no push activity for more than 90 days, regardless of Jira status.
   - **Section 3:** Branch has no link to any Jira feature — cannot be identified or associated with any work item.

   The report also shows active (sanctioned) branches and who is working on them, plus a per-user summary table of improper vs. active branches and a "remaining work" table.

### Claude Code Review Expansion

Val asked about expanding Claude Code Review to more repositories. Currently it is connected to only 3 repositories (Flex POS, Flex Dispenser, and Miranda). Andrei explained the cost model: based on recent data, 8 pull requests across the 3 repos cost ~$400, roughly $50 per pull request on average. Val calculated that at an expected rate of 1 PR per feature (every 3-4 days per developer), the cost would be approximately $250-350 per developer per month, or roughly $3,500/month for 10 developers — which Val considers very affordable.

Val emphasized that even if Claude Code Review is only 75% effective today, that's excellent value. He noted that the codebase is currently undocumented, which limits review quality, but as documentation improves, the reviews will become more effective. Val also noted that moving away from C/C++ (the hardest language for AI review) toward other languages would further improve review quality.

**Resolution:** Val directed Andrei to expand Claude Code Review to all active repositories, starting with Flex Sport POS. Andrei will look at the top repositories by recent activity and add more.

### Report Formatting Changes

Val requested several formatting changes to the weekly branch audit report:

- **Rename "garbage branches"** to "improper branches" — the word "garbage" is too harsh.
- **Restructure the report into two color-coded sections:**
  - **Red section (top):** Non-sanctioned branches — all three categories of improper branches, plus the per-user breakdown (currently called "remaining work"), renamed to "Non-sanctioned branches sorted by person."
  - **Green section (bottom):** Sanctioned active branches — currently labeled "active work branches," renamed to "sanctioned branches."
- **Dynamics display:** Val questioned whether showing only one week of change history is sufficient for trend analysis. He suggested that single-step dynamics may be misleading — things may look like they're improving when in reality one data point isn't enough. Andrei agreed to consider showing more history.
- **Enforcement workflow:** Andrei explained that the weekly report will be sent to developers so they can self-correct. If there's no reaction after a week, Andrei's team will follow up directly with the developer asking why their branch doesn't comply.

### Release Technical Documentation

Andrei raised the item "Release Technical Documentation" from the follow-up list. Val clarified this refers to release process documentation — not technical docs, but documentation of the release workflow itself. This is relevant for Ivan Shpak (QA). Val had previously emailed about this topic, but Andrei hasn't had time to start on it yet. Andrei agreed to create a Jira ticket in the main project (moving it from Service Management) and to begin conversations with Ivan Shpak and Aaron about establishing the release process.

### Management Reporting Specification

The last agenda item was "Management Reporting Specification." Val couldn't recall exactly what this was intended to cover. He initially connected it to the idea of building documentation as microservices — a system where engineering documentation (architecture, ADRs, etc.) would be built as callable services, with a software architect "role" prompt that could check for documentation completeness. Andrei recalled that Val had already sent a prompt for an architect role and that they'd started working with Ivan on ADRs. Val also mentioned wanting to build documentation workflows using a microservices approach. However, Val decided to "park" this topic and go back to his notes to recall the original intent before discussing further. A meeting with Clayton about a linguistics/transcription microservice was scheduled for later that day, which may clarify some of this.

## Decisions Made

- **Expand Claude Code Review to all active repositories** — starting with Flex Sport POS, then other high-activity repos. Cost per developer (~$250-350/month) deemed acceptable. (Decided by Val)
- **Rename "garbage branches" to "improper branches"** in all reports. (Decided by Val, agreed by Andrei)
- **Restructure weekly branch audit report** with red (non-sanctioned) and green (sanctioned) color coding, reorganized sections, and renamed labels. (Decided by Val, agreed by Andrei)
- **Move release documentation task to main Jira project** from Service Management. (Decided jointly)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Expand Claude Code Review to additional repositories — start with Flex Sport POS, then review top repos by activity and add more | TBD | High | Val wants all repos covered; cost analysis shows it's affordable at ~$50/PR |
| 2 | Andrei Bosik | Reformat the weekly branch audit report: rename "garbage" to "improper," restructure into red (non-sanctioned) / green (sanctioned) sections, move per-user breakdown into the red section, update all labels | TBD | High | Val wants to review the reformatted report before it gets distributed to developers |
| 3 | Andrei Bosik | Regenerate the reformatted branch audit report and send the link to Val for review | TBD | High | Val explicitly asked to see the updated format before wider distribution |
| 4 | Andrei Bosik | Create a Jira ticket in the main project for release process documentation (moved from Service Management) | TBD | Normal | Needed to begin the release documentation workflow with Ivan Shpak and Aaron |
| 5 | Andrei Bosik | Begin conversations with Ivan Shpak and Aaron about defining the release process | TBD | Normal | Val wants to start this discussion; Andrei acknowledged he hasn't begun yet |
| 6 | Val Levitan | Review personal notes to recall the original intent behind "Management Reporting Specification" | TBD | Normal | Val parked this topic because he couldn't remember what it was supposed to cover |

## Engineering Signals

### Confirmed Signals

- **Resolution: Claude Code Review expansion to all active repositories** — Val decided to expand Claude Code Review from 3 repositories to all active ones. The cost analysis ($50/PR, ~$350/dev/month, ~$3,500/month total for 10 devs) was discussed and deemed acceptable.

- **Solution: Automated compliance and branch audit reporting via GitHub Pages** — Andrei consolidated all manual reports into a single GitHub repository that auto-generates and publishes reports as web pages. Daily compliance and weekly branch audit reports replace manual email-based processes.

### Suspected Signals

- **Possible REQ: Minimum PR frequency standard per developer** — Val stated that each developer should produce at least one pull request every 3-4 days (per feature branch), in the context of cost estimation.

- **Possible ADR: Move away from C/C++** — Val stated the need to move away from C/C++, citing it as the hardest language for AI code review. No timeline or migration plan discussed.

- **Possible CAP: Documentation-as-microservices with AI architect role** — Val described a vision of building engineering documentation as microservices with a software architect prompt that checks documentation completeness. Parked for further review.

## Open Questions

- **Branch audit dynamics depth:** Val questioned whether showing only one week of comparison is sufficient for trend analysis. No resolution — Andrei to consider showing more history.
- **Management Reporting Specification:** Val parked this topic entirely, needing to revisit his notes to recall the intent.
- **Clayton's linguistics/transcription service:** A meeting with Clayton was scheduled for later on March 30 to demo the transcription microservice. Outcome unknown from this transcript.

---
*Processed from Teams transcript on 2026-03-30*
*Source meeting: Follow-up IT Tasks*