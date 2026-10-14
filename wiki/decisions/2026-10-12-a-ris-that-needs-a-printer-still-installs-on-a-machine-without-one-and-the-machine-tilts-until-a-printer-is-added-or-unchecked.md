---
type: decision
title: Working position — a RIS that requires a printer can still be applied on a machine with no printer; the machine then shows a tilt until a printer is installed or the printer is unchecked in setup (Pavel; the case is written down to think about)
date: 2026-10-12
aliases: [RIS requires printer but no printer, no printer on machine RIS require printer, continue installation without printer, tilt until printer installed, uncheck printer in setup, capability 250 case]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# A RIS that needs a printer installs anyway; the machine tilts until fixed

A working position of [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-12-ris-mvp2-scope-and-release-timing.md|Oct-12 RIS MVP 2 call]] (English), on a case raised by [[wiki/people/sebastian.md|Sebastian]] about capability 250. Pavel said the case is written down "and we will think about this", so this is **not final**. Quotations from [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]].

## The background: capability 250

Pavel: the printer feature is "already implemented by mistake, I would say. How a developer made it even not for Mvp one, but already created." If a printer is connected to a machine whose RIS has none, "it will appear in the system. And if you enter setup screens, it will be an additional option to set a check mark, use printer or not use." If selected, "it will be added into a list of cash out… possible device before the hand play, but after Aft." Felipe: "Fantastic." Pavel: "we have not tested this feature"; something may be needed on the server side.

## Sebastian's case

"if for any reason I reinstall the software and I apply the RIS that has the printer added… What… will happen". Today: "if I try to apply an RIS with printer added, if I don't have the printer installed, I can't do that."

## The answer so far

- Pavel first: "during the initial setup, it should be a message saying that RIS require a printer, but you don't have this printer."
- Felipe: "But will it let it continue?… it should, because if later I can say that there is no printer and a checkmark, it should apply it, correct?"
- Pavel: "I think this is up to us to decide this." "Okay, let's write down this case and we will think about this. No printer on machine… A RIS. Require printer."
- Then: "looks like we will… be able to continue installation even in this case. But then, on the machine, it will be a tilt saying that we cannot work until you install printer, or… you will need to enter. Set up and uncheck printer. And it will enable working without printer in this case."

The derived notes record it as Pavel's position, "to think about" [[raw/Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]].

## Related

The TITO question from the same call — customers want TITO in without TITO out, and the TITO menu appears only with a printer — is on [[wiki/topics/ris-remote-install-and-machine-states.md]] (Oct 12). The Oct-5 MVP 1 list had CAP-250 as "enable or disable printer during initial setup": [[wiki/decisions/2026-10-05-ris-improvement-mvp1-is-five-jira-capabilities-in-one-release-due-october-19.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — settle the "RIS requires a printer, machine has none" case with the developers — due unspecified — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]

## Open questions

- Is the tilt-until-fixed behaviour the final rule? Pavel: "we will think about this" — [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
- [[raw/Meeting_Notes_RIS_MVP2_Scope_and_Release_Timing-October-12-2026.md]]
