# Meeting Summary — Transactional MVP1 sync
**Date:** October 9, 2026, 8:01 AM – 8:25 AM Eastern
**Duration:** ~24 minutes
**Attendees:** Andrei Klimovich, Pavel Frolov, Irina Shishko, Andrei Bosik, Ivan Shpak, Dzmitry Chudzinau, Alexander Biratko, Alexey Khamin
**Raw transcript:** [[Meeting_Transcript_Transactional_MVP1_Test_Machines_and_Unclaimed_Funds-October-9-2026]]

## Summary

Held in Russian. Organized by Andrei Klimovich.

**Georgia SAS setup (Elizabeth).** Ivan helped Elizabeth set up SAS for many hours. Early on the cable did not fit this emulator; she bought another cable and it got better, but it still did not start. Claude, running on Ivan's work laptop, did the same steps Ivan did, and then it worked. Ivan does not know what made the difference; he thinks the port was restarted "under the hood". It all worked by 9 PM Minsk time yesterday. Pavel then worked with Elizabeth until about 2 AM bringing up modems on machines, so she likely did not test further.

**Readiness for other makers' machines.** Andrei asked what must still be checked before taking machines from other manufacturers. Irina: there is still a lot to test; tests keep hitting issues (for example, re-flashing the emulator to see what happens on a machine limit or tilt). She said taking the machines for one day while not ready wastes time. Pavel: those are very rare cases; the main workflow is ready, and the team can already see which commands go for deposit, collect and status. Dzmitry: formal MVP1 development is finished as planned. The team now finds cases not discussed before (memory ran out, log traffic tuning, autotests failing on the port with a machine). Sounds were added. Andrei: the first machines can be arranged for Oct 15–16.

**Previously registered terminals.** Dzmitry: if a terminal was registered before (same TG environment), its secrets must be wiped. At the end of the SD-card install, on the player screen, press each letter 4 times in a row. This wipes old secrets and puts the terminal into registration mode, so new certificates for cloud updates are made. Register it again; the same number is fine. Andrei asked to put this in the install instructions as a separate red section. Dzmitry said he already updated the instructions.

**Production.** Dzmitry plans to deploy the production web service over the weekend and try the production environment. Andrei Bosik: once one terminal registers in production on the new version, run a real transaction. Andrei Klimovich agreed: as with the earlier 3 transactions, do it before the first real location, next week.

**Andrei Klimovich's return.** He flies back Monday and goes straight to Georgia; he expects to be there from Tuesday, full time. First priority: rebuild the full environment and test Flex IQ from the product side on all main flows. He will review Dzmitry's gap document. Irina already moved the team's changes and Dzmitry's documents (run through Claude) into the requirements, marked in red, and tagged Andrei. He only has to agree or disagree with each item.

**SIM cards, Minsk cards, InComm, Nayton.** The SIM card payment problem was fixed, so it should work. The thread on ordering cards for Minsk was dropped; Andrei will revive it today. InComm: still waiting for official approval of JVL as broker so JVL can issue their cards. Andrei pinged them this morning, and a reply came during the call; he must check it. On the Nayton side, invoices are issued and money is transferred.

**Georgia show.** A short show in Georgia around Oct 21–22; Andrei goes with Sebastian. Plan: show Flex IQ working with ports (MVP1), and possibly the Flex Pay Slim card dispenser. Alexander: he works on Flex Pay (rotated screen, for Slim). He wants Andrei to review all screens and the main flow, because much has changed. He offered a build that runs on a PC with virtual devices if no hardware is ready. Andrei will ask Gennadiy about the Slim hardware (dispenser in the cabinet, new door wiring); he is almost sure it has not moved. Revisit next Tuesday or Wednesday.

**Bootloader on new boards.** Pavel asked if the bootloader and USB install still work after the recent firmware memory changes. Alexey: on the new boards nothing works; the fix is not in the repository; the developer says it works for him locally, then silence. Pavel will write to him. Dzmitry asked Pavel to also look at an old item hanging on the port.

**Collect money after a port crash.** Irina: a player collects money from the machine, scans a wallet, and the port reboots before the money reaches the wallet. The money does not go to the scanned wallet. Dzmitry: it goes to unclaimed now. He said Flex Port might store the target wallet and send the money there after reboot, but some cases break this (for example the port is moved to another master/IQ). Pavel: if Flex Port loses power, the money stays on Flex Port until power is back; also the player may have thrown the wallet away. Andrei: for MVP1, all such money goes to unclaimed; unclaimed is a safe state. Auto-sending to a known wallet is a good idea for later. Pavel: maybe in MVP3 a cashier could see the saved wallet on an unclaimed item and credit it. Dzmitry: park it as unclaimed; autotests should target that.

## Decisions Made

- **First test machines from other operators can be arranged for Oct 15–16.** Dzmitry says MVP1 development is formally done; Irina wanted more testing first. (Decided by Andrei Klimovich)
- **Install instructions get a separate red section on wiping secrets for terminals that were registered before.** (Decided by Andrei Klimovich; Dzmitry Chudzinau says it is already done)
- **Run a real transaction in production before the first real location, as was done before (3 transactions).** (Raised by Andrei Bosik; decided by Andrei Klimovich)
- **MVP1: collect money that does not reach the scanned wallet after a port crash goes to unclaimed; unclaimed is a safe state; autotests target this.** Auto-sending to a known wallet is left for later. (Decided by Andrei Klimovich, Dzmitry Chudzinau)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Arrange test machines from operators with Philipp (likely Felipe) | Oct 15–16, 2026 | High | Machines borrowed to the office |
| 2 | Andrei Klimovich | Ask Elizabeth to connect Flex IQ, install the latest builds with the secrets wipe, and join it to the full setup | Oct 9 or Oct 12, 2026 | High | "today or Monday" |
| 3 | Dzmitry Chudzinau | Mark the secrets wipe in the install instructions as a red section | Done Oct 9, 2026 | Normal | Dzmitry: "I already fixed it" |
| 4 | Andrei Klimovich | Ask Gennadiy about Flex Pay Slim hardware readiness (dispenser, door wiring) | TBD | Normal | Needed for the Georgia show |
| 5 | Dzmitry Chudzinau | Deploy the production web service and try the production environment | Oct 10–11, 2026 | High | Weekend |
| 6 | Andrei Klimovich | Run a real transaction in production on the new version | Week of Oct 12, 2026 | High | Before the first real location |
| 7 | Andrei Klimovich | Revive the thread on ordering cards for Minsk | Oct 9, 2026 | Normal | Thread was dropped |
| 8 | Andrei Klimovich | Check InComm's reply and push for official broker approval | Oct 9, 2026 | High | Reply arrived during the call |
| 9 | Andrei Klimovich | Rebuild the environment in Georgia and test Flex IQ on all main flows; review Dzmitry's gap document and Irina's red-marked requirements | From Oct 13, 2026 | High | Back Monday, in Georgia from Tuesday |
| 10 | Pavel Frolov | Write to the developer of the firmware memory changes about the bootloader on new boards | TBD | Normal | Alexey: nothing works on new boards, fix not in repo |
| 11 | Pavel Frolov | Look at the old item hanging on the port | TBD | Low | Dzmitry's request |
| 12 | Andrei Klimovich | Revisit Georgia show content (Flex IQ with ports, Flex Pay Slim) and review Flex Pay screens | Oct 13 or 14, 2026 | Normal | Alexander can make a PC build with virtual devices |

## Open Questions

- What exactly fixed the SAS setup at Elizabeth's site? (Raised by Ivan Shpak)
- Exact date of the Georgia show (about Oct 21–22). (Raised by Pavel Frolov)
- Is at least one Flex Pay Slim machine with a card dispenser built? (Raised by Andrei Klimovich)
- Does the bootloader work on new boards after the memory changes? (Raised by Pavel Frolov)
- Later: should unclaimed money go automatically, or by cashier action, to a known saved wallet? (Raised by Dzmitry Chudzinau, Pavel Frolov)

## Dispatch Log


---
*Processed from Teams transcript on 2026-10-14*
*Source meeting: Transactional MVP1 sync*
