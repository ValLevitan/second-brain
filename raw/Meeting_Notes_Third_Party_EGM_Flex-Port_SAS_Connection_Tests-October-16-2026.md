# Meeting Summary — 3rd party EGM's connection tests
**Date:** October 16, 2026, 10:01 AM – 10:08 AM Eastern
**Duration:** ~7 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Third_Party_EGM_Flex-Port_SAS_Connection_Tests-October-16-2026]]

## Summary

Held in Russian. Organized by Andrei Klimovich. Short status and next steps on Flex-Port tests with third-party EGMs (machines from other makers) over SAS.

**Test setup.** Each third-party machine is connected to one router that Minsk can reach by VPN. A Flex IQ on staging is connected to the same setup.

**Results so far (Andrei).** Since yesterday all ports are active; they see the IQ and the machine they are connected to. On some machines money was loaded through the port and also cashed out.
- One machine (heard as "Bally"): neither load nor cash-out worked.
- Aristocrat: load always works. Cash-out is a floating bug: it may work 2–3 times, then it locks and no more cash-out until the whole machine is rebooted.
- IGT: load seems to work; cash-out never worked.
- Light & Wonder (as heard): Andrei does not remember the result.
- When cash-out fails, the port does not change state and shows no money to scan. The IQ does receive the error: a failed cash-out attempt with an extra status (heard as "reef Houston"; meaning unclear).
- Andrei thinks not all SAS settings on the machines are understood yet. Sebastian will spend time today on those settings.

**Next steps (Pavel).** The router link alone does not help Minsk, because they know nothing about these machines and likely cannot connect to them. Instead:
1. Put the debug Flex-Port build on every port. It has a console that lets Minsk pull much more data with AI and emulate events remotely (for example send or accept money without scanning a ticket). Dima earlier enabled logging of all SAS commands for such third-party machines; it is best viewed on the debug build.
2. Label each Flex-Port with its IP address, so each case can be tied to a port and a machine.
3. Then move on to reading the SAS logs machine by machine.

The debug build is flashed with ST-Link; Elizabeth knows how. Pavel can emulate holding a ticket to the port, but cannot press cash-out on the machine, so people on site are needed. Andrei and Sebastian will be on hand.

**Deadline.** The machines must be returned on Wednesday (October 21, 2026), so the remaining days must be used.

## Decisions Made

- **Install the debug Flex-Port build on every port of the third-party EGM test setup** — gives Minsk a console to pull data and emulate events. (Proposed by Pavel Frolov, agreed by Andrei Klimovich)
- **Map each port's IP address to its machine, and share the Flex IQ IP** — so every case can be tied to a port and machine. (Pavel Frolov, Andrei Klimovich)
- **Keep the Flex IQ connected in the setup; do not unplug or remove it** — it is needed for all tests. (Andrei Klimovich, confirmed by Pavel Frolov)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Email the link to the debug Flex-Port build, with Elizabeth in copy so she can download it herself | 2026-10-16 | High | Machines go back Oct 21 |
| 2 | Andrei Klimovich / Elizabeth Palomino | Flash the debug build (ST-Link) onto every Flex-Port in the setup | TBD (before 2026-10-21) | High | Elizabeth knows the ST-Link flashing |
| 3 | Andrei Klimovich | After builds are installed, send the list of port IP addresses with the machine each belongs to, plus the current Flex IQ IP | TBD (before 2026-10-21) | High | |
| 4 | Sebastian | Spend time today studying the machines' SAS settings | 2026-10-16 | Normal | Some settings may still be wrong |
| 5 | Pavel Frolov (Minsk) | Review SAS logs machine by machine on the debug build | 2026-10-21 | Normal | Starts after items 1–3 |
| 6 | Andrei Klimovich, Sebastian | Be on hand for physical steps on the machines (e.g. press cash-out) during remote tests | 2026-10-21 | Normal | Pavel cannot press cash-out remotely |

## Open Questions

- Why cash-out fails on Aristocrat (locks after 2–3 tries) and never works on IGT — raised by Andrei Klimovich.
- What the extra failure status (heard as "reef Houston") means — raised by Andrei Klimovich.
- Result for Light & Wonder was not remembered — Andrei Klimovich.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-16 12:10 PM Eastern*
*Source meeting: 3rd party EGM's connection tests*
