# Meeting Summary — RIS- Capabilities and Requirements Review
**Date:** September 28, 2026, 11:07 AM – 11:36 AM Eastern
**Duration:** about 28 minutes
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko, Sebastian Cortes
**Raw transcript:** [[Meeting_Transcript_RIS_MVP1_Capabilities_Walkthrough_and_Jira_Handover-September-28-2026]]

## Summary

**Roles.** Val explained the roles. Felipe plays product owner: he states each capability and asks questions until he and engineering are aligned. Pavel drives from the engineering side and demands capabilities that are clear, simple and high level. A capability closes once it is built. A requirement lives on with the product. Its acceptance criteria let QA test the product. Val told Felipe to be short: "Capability, requirement, move on." English is a second language for the engineers.

**The nine capabilities Felipe read out:**

1. **Replace the CPU battery without a factory reset.** Today, if the machine is powered off and the battery is replaced before the QR code is scanned, it goes into critical error and needs a hard reset (30 minutes to 2 hours of downtime). Pavel: clear.
2. **Upgrade software without creating a new RIS.** The machine keeps its configuration on upgrade. JVL can pick one, some or all machines, without recreating installations in CMS (today every installation is made per serial number, about 2,500 times). Irina and Pavel suggested splitting this: (a) reuse the pre-saved RIS on the machine after a factory reset, without a USB stick, with the same software version; (b) keep the RIS across a software version change. Pavel said (b) is harder, because on the server today each RIS file is tied to one software version. He thinks it is possible but could not say how long it will take.
3. **Recover from a boot loop without a hard reset or a technician**, keeping meters, credits, game settings and RIS. Pavel: the requirement is clear but the fix is "in the fog". Reboots come from the watchdog, but a storage fault (for example a bad sector) will not be fixed by clearing settings. One idea: after three boot loops, do a soft factory reset. Felipe said a boot loop this morning was said to be a printer without power, and boot loops existed before the watchdog. No logs are sent during a boot loop. Val reminded everyone of the switch to the cell modem, and said this can be done in steps, but the market needs a quick improvement or the product will be rejected. Pavel: the first step will likely be extra logging to understand the cases.
4. **Add or remove the printer without a hard reset** and without a new RIS. Meters and settings stay the same; CMS shows the new setting after the next lease QR scan. Felipe said whether the TITO menu should always be available is open. Pavel: today the printer and bill acceptor can only be added at initial setup. It needs investigation, but it can probably be done.
5. **Issue a lease when the machine and CMS installations do not match.** For example, a customer upgrades most cabinets but misses a few. The mismatch must not block the lease, with no action at JVL and no passport scan or JVL code. Pavel: description clear; server-side changes unknown, needs investigation.
6. **Replace a part without a passport QR.** Parts can be swapped today, but after any hard reset a passport update is required. The goal is no passport update, or an automatic one. Pavel: clear.
7. **Detect missed upgrades before the lease expires.** CMS shows upgraded and pending machines. Ten days before lease expiry JVL gets an email with the count and serial numbers. The missed machine still gets its lease renewed and shows an "upgrade pending" message. Pavel: clear.
8. **Show the real cause of a critical error** and what is needed to fix it. Today the technician sees only a yellow screen and a QR code, and arrives unprepared. Pavel: in most cases the cause is unknown until the crash logs are studied; an error-explanation tool with a central database was discussed before. **Val moved this to MVP 2.**
9. **Renew the lease with one QR scan** instead of four to six. Pavel and Irina: clear and simple.

**Handover.** Val said the capabilities must now go into Jira with the requirements linked. Sebastian owns this from now on and works directly with Pavel; Felipe helps in the background so he is free for other work. Pavel creates the features and schedules people and work. Irina manages the acceptance criteria. Val then said no automated tests will be made for this.

Val also asked Sebastian to watch the machine that needs to be restored; a technician was on the way, and Sebastian did not need Irina's help. The meeting ended with Val wishing Felipe a happy birthday.

## Decisions Made

- **Capability 8 (show the real cause of a critical error) moves to MVP 2.** — Not needed now; the cause is usually unknown until crash logs are studied. (Decided by Val)
- **Sebastian takes over managing the RIS capabilities and requirements in Jira; Felipe supports in the background.** — Val wants Felipe free for other work. (Decided by Val)
- **Pavel creates features and schedules work; Irina manages acceptance criteria. No automated tests will be made for this.** — Val first said Irina's department would build automated tests, then corrected himself. (Decided by Val)
- **Boot-loop recovery (capability 3) may be delivered in steps; the first release will likely add logging.** — Pavel does not know the causes yet; Val accepted a multi-step release. (Pavel proposed, Val agreed)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Sebastian Cortes | Enter the RIS MVP1 capabilities in Jira and link the requirements to them, working directly with Pavel | TBD | High | Val: "it's on you" |
| 2 | Felipe Miranda Giorgi | Support Sebastian in the background on the Jira capabilities | TBD | Normal | |
| 3 | Pavel Frolov | Create features in Jira and schedule resources and work for the capabilities | TBD | High | |
| 4 | Irina Shishko | Manage the acceptance criteria for the capabilities | TBD | Normal | No automated tests for this |
| 5 | Pavel Frolov | Investigate effort for capability 2b (keep RIS across software versions), 4 (printer on the fly) and 5 (lease on mismatch, server side) | TBD | Normal | Pavel could not estimate yet |
| 6 | Pavel Frolov | Think through the boot-loop recovery approach; likely start with extra logging | TBD | Normal | Val: "why don't you think about it" |
| 7 | Sebastian Cortes | Follow the machine that needs to be restored (technician on the way) | Sep 28, 2026 | High | |

## Open Questions

- Should the TITO menu always be available, or only when a printer is enabled? (Felipe)
- How long will capability 2b (keep RIS across software versions) take? (Pavel could not answer)
- What causes boot loops besides the watchdog (storage fault, printer without power)? No logs are sent during a loop. (Felipe, Pavel)
- Which release (MVP 1, 2 or 3) does capability 2b belong to? (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026, 2:20 PM Eastern*
*Source meeting: RIS- Capabilities and Requirements Review*
