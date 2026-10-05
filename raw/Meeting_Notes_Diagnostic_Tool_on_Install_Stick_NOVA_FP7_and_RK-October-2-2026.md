# Meeting Summary — EGMs diagnostic tool - NOVA-FP-7
**Date:** October 2, 2026, 9:01 AM – 9:15 AM Eastern
**Duration:** ~14 minutes
**Attendees:** Pavel Frolov, Genadi Peari (Val Levitan present, asked questions in chat only)
**Raw transcript:** [[Meeting_Transcript_Diagnostic_Tool_on_Install_Stick_NOVA_FP7_and_RK-October-2-2026]]

## Summary

Pavel presented an idea for the new platform (the NOVA framework on new x86 motherboards, FP-7). Held in Russian.

**The idea.** JVL software is always installed from a USB stick. Nothing stops the team from putting the diagnostic tool on that same stick. A technician plugs in the stick and chooses: install the current game version, or open the diagnostic menu and check every component on the machine. Benefits: no separate diagnostic stick to keep; if some hardware is missing, not flashed or the wrong version, the technician sees why the install fails right away. This answers the problem Felipe raised recently: install errors with unclear descriptions.

**Keep it current.** If the diagnostic tool lives in the SDK project and repository, it stays up to date automatically. When the SDK gains a new modem or driver, the diagnostic tool gets it too. The SDK Linux builds are used on every game build and every release.

**Security question.** Genadi asked what happens if the tool falls into the wrong hands and whether someone could steal from JVL. Pavel: the old tool had an optional Dallas firmware section that was probably never enabled. If the tool makes no changes to the machine, it is safe. It only reads: which boards are present, light LEDs, check that the bill acceptor and printer work, all before installation and without touching the software.

**Val's chat question: sell mode and modem.** Can diagnostics run during installation and be sent out through the modem? Pavel: in theory yes, but the data has to land on a server, so the server side must be designed first. What is proposed now is only what the technician sees on screen. Genadi: once the tool runs, the machine can create logs and maybe allow a connection; fixing problems, not just diagnosing them, could be a next step. Pavel: modem use cases need thought and can come from Val, Andrei or Felipe. Pavel will think through what the minimum is, which steps are needed, who to involve, and when resources free up after Transactional. Vladimir could then do a modern GUI. Much of the old back end can be reused.

**Two products.** For the record: the RK-based ARM platform (street machines) will go faster. The FP-7 x86 platform is mainly for casinos. For RK the back end will differ by 50–60 percent; the GUI can be reused fully. With Claude, rewriting the GUI is an iterative task but not a long one.

No objections. Pavel will work out both variants.

## Decisions Made

- **Put the diagnostic tool on the installation USB stick and keep it in the SDK repository.** — One stick, always current, diagnoses failed installs. (Decided by Pavel Frolov, no objections from Genadi Peari)
- **Work out both variants: RK (ARM, street machines) and FP-7 (x86, casino).** — No remarks raised. (Decided by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Work out the minimum scope, steps, people and timing for the diagnostic tool on both platforms, including modem use cases | TBD | Normal | Resources free up after Transactional |

## Open Questions

- Modem and sell-mode diagnostics during installation need a server side; use cases to come from Val, Andrei and Felipe. Raised by Val (in chat).
- Whether the tool should also fix problems, not only diagnose them. Raised by Genadi Peari.

## Dispatch Log

---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: EGMs diagnostic tool - NOVA-FP-7*
