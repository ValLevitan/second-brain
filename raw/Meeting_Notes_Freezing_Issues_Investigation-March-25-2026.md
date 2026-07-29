# Meeting Summary — Digging into Freezing Issues
**Date:** March 25, 2026, 9:32 AM Eastern
**Duration:** ~25 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Alexander Biratko

## Summary

### Software Architecture & Release Context

The team discussed the software stack powering their gaming machines. The stack consists of a **HAL (Hardware Abstraction Layer)** at the lowest level, a **DC (Data Center)** layer containing application logic, **SAS** protocol communications, and a **framework** layer. The software was primarily written by Dima, with significant contributions from Zhenya (Evgeny) and Sasha (Alexander) on later features.

The release history is relevant to the freezing investigation: the original releases (around versions 1.12/1.17) shipped on the "Pech 123" machines. A subsequent release — approximately **version 1.14** — added support for **two SAS connections** and a **printer**, along with a new skill. The printer-related work was done at the DC level, not the HAL level. Pavel clarified that the HAL for the printer is the same as the Florida version — changes were specifically in the DC layer to make the printer operational. Irina confirmed that both Sasha and Zhenya contributed to these changes. Pavel also noted there was significant work around **IT and limit handling** due to Georgia's regulatory restrictions on print permissions and EFT (electronic fund transfer) authorization.

### Problem 1 — Georgia Location Freezing

The core mystery: **new machines freeze, but old machines running earlier software do not.** The hardware between old and new machines is unchanged. The only difference is the software release with the new skill feature. Val is attempting to chronologically isolate what changed to identify the cause.

In Georgia specifically, **printers are not installed**, so printer code paths are not directly triggered. Pavel confirmed the HAL between Class 3 and Georgia is "99.9% identical." However, the DC layer saw significant internal logic changes. Val raised the possibility that even though the printer isn't physically present in Georgia, instabilities in the DC and printer code could combine to cause different behavior — they're part of the same assembly/build.

Pavel highlighted that in **South Dakota**, the audit ticket procedure (which does use the printer) involves large data transmissions to a slow printer, creating potentially unstable behavior that hasn't been sufficiently tested or analyzed. However, this code path doesn't exist in Georgia (no audit tickets there).

Val mentioned that **Alekseev** (external or separate team member) believes the printer routine is written incorrectly. Pavel pushed back, noting the same code worked in Class 3, but Val urged the team to listen to Alekseev's concerns constructively rather than dismissively: *"Instead of taking it as an attack, let's say OK, what's the error? Let's figure it out."*

An important observation from Pavel: **casino machines are rebooted daily**, which may mask freezing issues. The Georgia locations ("lokeyshns") may have different power cycling patterns.

### Problem 2 — South Dakota QR Code Race Condition

Irina raised a second, separate issue: **machines in South Dakota crash and reboot when scanning QR codes.** Denis reported machines going into reboot. Juan sent a video demonstrating the behavior. The team found the cause yesterday and **successfully reproduced it today** (though they had to artificially create conditions since their test machines behave slightly differently).

Alexander explained the root cause — a **race condition** in the game disable/tilt sequence:

1. All games on the machine are disabled via SAS (`SAS lock`)
2. Games are then unlocked sequentially
3. **Before the DC can set a tilt state**, the framework queries for available games
4. The framework sees zero games (they've all been disabled) and **crashes**
5. The timing window between disabling the last game and setting the tilt state is small but occasionally hit

Val pushed on this: *"The framework should tell the DC 'wait, it's not your time to ask.'"* Alexander explained there are agreed-upon state contracts — if the state is inconsistent, the DC should be in tilt — but the operations weren't atomic. **The game disable and tilt activation were sequential rather than transactional**, and the framework could query in the gap between them.

### Approach — Claude Code Review

Val proposed running the changed code through **Claude Code** for automated code review to identify potential instabilities. Alexander expressed skepticism: without knowing specifically where to look, the results would be "fairly abstract" — Claude Code might flag style issues rather than the actual freezing cause. Val countered that even abstract findings become actionable when reviewed by engineers with the domain expertise to judge which findings are serious: *"If Claude Code tells me there are errors, I'd just say 'yes, bad code.' But if it tells you there are errors, you have the practical and academic knowledge to say 'this one is probably harmless, but this one is probably bad.'"*

Pavel added that the review should approach from **two sides**: the DC layer changes (commits) and the HAL changes, since a crash in the DC could trigger unexpected behavior in the HAL.

The team agreed to proceed. Alexander and Pavel will identify the exact version boundaries for comparison, with Irina providing the specific version numbers.

## Decisions Made

- **Proceed with Claude Code review of DC and HAL changes** — despite uncertainty about results, Val's position is that inaction guarantees no progress. Alexander and the team agreed. (Decided by Val, accepted by team)
- **Pull Zhenya off current work to focus on freezing analysis** — Val directed that both Alexander and Zhenya should concentrate on this. (Decided by Val)
- **Review from two sides** — both DC layer changes and HAL changes need examination, not just one. (Proposed by Pavel, agreed by team)
- **Listen constructively to Alekseev's printer concerns** in the follow-up call rather than being defensive. (Directed by Val)
- **South Dakota race condition root cause confirmed** — the sequential (non-atomic) game-disable + tilt-set operations create a timing window. Fix approach implied but not explicitly specified. (Confirmed by Alexander)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Alexander Biratko | Run the DC and HAL code changes through Claude Code for review, focusing on potential instabilities and freezing causes. Work with Zhenya on this. | 2026-03-25 (same day, ~4 hours) | High | Blocking diagnosis of Georgia freezing issue. Val will call back in ~4 hours for update. |
| 2 | Pavel Frolov | Review the specific commits and changes between the old version and release 1.14, identifying what changed in both the DC and HAL layers. | 2026-03-25 (same day) | High | Need to establish exactly what code differs between the working (old) and freezing (new) versions. |
| 3 | Irina Shishko | Provide the exact version numbers — the version that shipped in the first machines (Pech 123) and the version currently deployed — so the team can do a precise diff. | 2026-03-25 (ASAP) | High | Alexander and Pavel need this to start their analysis. Most foundational blocker. |
| 4 | Alexander Biratko + Zhenya | Fix the South Dakota QR code race condition — make game disable + tilt activation atomic rather than sequential. | TBD | High | Machines are crashing in production in South Dakota. Race condition was reproduced today. |

## Engineering Signals

### Confirmed Signals

- **Possible ADR — Atomic state transitions in DC/framework interface:** Alexander described how the game-disable and tilt-set operations are currently sequential, creating a race condition. The discussion implies a need for an architectural decision about transactional state management between the DC and framework layers. Val explicitly questioned the architecture: *"The framework should tell the DC 'wait, it's not your time to ask'"* and *"I still insist that our [interface] between file lock and DC is wrong."*

- **Engineering Solution — South Dakota race condition fix:** The root cause was identified: game disable and tilt activation must happen atomically (in one transaction) rather than sequentially. Alexander stated: *"We should have either disabled the last game and set tilt in one transaction... but we had it sequentially, and sometimes [the framework] hit that gap."*

### Suspected Signals

- **Possible REQ — Printer/DC interaction stability requirements:** The discussion around printer communication instabilities (large payloads to slow printers, insufficient testing of audit ticket procedures in South Dakota) suggests there may be unwritten reliability requirements for printer interaction that should be formalized.

- **Possible ADR — Framework error handling for inconsistent state:** Val raised that the framework should handle cases where the DC reports inconsistent state (e.g., zero games without tilt) gracefully rather than crashing. This touches on fault tolerance architecture.

## Open Questions

- **What exactly changed in the DC logic between the old and new versions?** The team doesn't yet have a precise diff — Irina needs to provide version numbers first.
- **Why do old machines not freeze if the software is the only difference?** Not yet answered — the code review is meant to investigate this.
- **Could daily power cycling in casinos mask the freezing issue?** Pavel raised this hypothesis but it wasn't confirmed or investigated.
- **What specifically does Alekseev think is wrong with the printer routine?** To be discussed in the follow-up call at ~11:00 AM.
- **Is the Georgia freezing related to the South Dakota race condition, or are they independent issues?** Val asked if they could be connected; the team acknowledged the possibility but didn't confirm.

---
*Processed from Teams transcript on 2026-03-25*
*Source meeting: Digging into Freezing Issues*
