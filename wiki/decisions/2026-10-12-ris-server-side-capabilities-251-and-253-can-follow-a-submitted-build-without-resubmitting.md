---
type: decision
title: RIS capabilities 251 and 253 are server-side work that can be added after the build is submitted to the lab, without submitting the build again
date: 2026-10-12
aliases: [capability 251, capability 253, CAP-251, CAP-253, add it after without submitting again, server part after submission, added for already submitted version]
source-count: 2
status: active
open-commitments: 0
open-questions: 0
---

# Capabilities 251 and 253 can follow a submitted build

Stated by [[wiki/people/pavel.md|Pavel Frolov]] and accepted by [[wiki/people/felipe-miranda.md|Felipe Miranda]] at the [[wiki/meetings/2026-10-12-ris-mvp2-scope-and-release-timing.md|Oct-12 RIS MVP 2 call]] (English), while Pavel went through the RIS capabilities on screen. Quotations from [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]].

## What was said

- Pavel first named "241", then described "This tool capabilities actually. Related to Sierra looks like" (garbled; the derived notes call them server-side [[raw/Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]).
- Pavel: "If we submit Mvp one version, we can add this further after the release and make it separately."
- Felipe: "You can add it after without submitting again." Pavel: "Yes, yes, yes. That's why I think this is not a problem. It will be added for already submitted version."
- Felipe: "Okay, which one? Capability 251?" Pavel: "and 253".

In one line: **251 and 253 do not hold up a lab submission; they can be added to a build that is already submitted.** What the two capabilities do is not stated in the source.

## Why it matters

It is one of Pavel's arguments, at the end of the call, that little machine-side work is left for MVP 2: "It will require server side, but server side could be released afterwards." The same reasoning is applied, more loosely, to the server part of capability 250 (the printer): "server part could be implemented further after submission, but yeah, better to implement it together with release." See [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 12).

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
