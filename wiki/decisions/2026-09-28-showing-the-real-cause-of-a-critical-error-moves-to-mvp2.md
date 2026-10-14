---
type: decision
title: Showing the real cause of a critical error (RIS capability 8) moves out of the RIS rework MVP1 into MVP 2 — SUPERSEDED Oct 5 2026 (back in MVP1, as words on the screen plus the QR)
date: 2026-09-28
aliases: [show the real cause of a critical error, capability 8, let's move it to MVP 2, we don't need it right now, error explanation tool, yellow screen critical error]
source-count: 3
status: superseded
open-commitments: 0
open-questions: 0
---

# The real cause of a critical error moves to MVP 2 (superseded Oct 5)

**Status: superseded.** On Oct 5 2026 the critical-error capability was back in the RIS improvement MVP1 release: the screen shows the real cause and the fix in words and keeps the QR code. See [[wiki/decisions/2026-10-05-the-critical-error-screen-shows-the-cause-and-fix-in-words-and-keeps-the-qr-code-in-mvp1.md]] [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]].

Ruled by [[wiki/people/val-levitan.md|Val Levitan]] at the [[wiki/meetings/2026-09-28-ris-mvp1-capabilities-walkthrough-and-jira-handover.md|Sept-28 11:07 AM RIS review]]. All quotations from [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]].

## The capability (Felipe)

"Show the real case of a critical error. The AGM shall show the real cause of a critical error and was needed to fix it." Today the machine "shows a full yellow screen, large warning triangle, and the words critical error. The QR code returns only information was sent to JBL customer support. The technician learns that the error is critical, not the cause, not the fix, not the parts required, and arrives unprepared." ("AGM" and "JBL" are read as EGM and JVL — **inference**.)

## Why it cannot be done now (Pavel)

"In most cases, we do not know beforehand, before we investigate crash logs, what was the reason of this crash." He recalled "some special tool, error explanation tool", with a "Central… Database of all" (the rest is cut off).

## The ruling

Val: "This could be moved to the second MVP. We, we don't need it right now." Then: "Let's move it to MVP 2." Felipe: "Clear."

## Background

This is case 8 of Felipe's Sept-23 list ("The critical-error screen says nothing"). On Sept 24 the engineers recalled the same explanation tool (Pavel "года 3 назад", Evgeny "лет 6 назад") and said it had to be thought out separately. See [[wiki/topics/ris-remote-install-and-machine-states.md]] (Sept 23 and Sept 24).

The derived notes record the move as a decision by Val, which matches the transcript [[raw/Meeting_Notes_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]].

## Update — Oct 5 2026 (evolution)

At the [[wiki/meetings/2026-10-05-ris-mvp1-scope-and-peach-packaging.md|Oct-5 11:00 AM RIS review]] the release summary included the critical-error capability. Val: "Mvp one, we adding the description along the QR code. So we have a QR code and we have a description." Real-time data for the technician stays a later goal: "Right now, in the Mvp one, the technician will not get anything by scanning." No source says why the capability came back. This is a newer ruling on the same capability, so it is **evolution**, not a contradiction [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]].

**§15.8:** clear.

## Sources

- [[raw/Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026.md]]
- [[raw/Meeting_Transcript_RIS_MVP1_Scope_and_Peach_Packaging-October-5-2026.md]]
