# Meeting Summary — Nova 2 and Galaxy
**Date:** November 7, 2026, 6:31 AM – 7:39 AM Eastern
**Duration:** ~68 minutes
**Attendees:** Val Levitan, Pavel Frolov (organizer), Dzmitry Chudzinau, Alexander Biratko, Irina Shishko, Andrei Bosik, Evgeny Kharetski
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Machine_Registration_One_Scan_Server_Serial_and_Dallas_Replacement-November-7-2026]]

## Summary

**Purpose.** Saturday working session booked at the end of the November 6 remote-update review. Pavel asked Dzmitry to open. Almost the whole hour went to one topic: how a new machine gets registered (cabinet serial, passport, Dallas chip) in the new Galaxy/NOVA system. Val closed by saying he needs the transcript and time to think. Nothing about the registration flow was finally decided.

**Component manifests (Dzmitry's opening).** While Val works on machine registration, Dzmitry proposed to study all the software components of the new ISO (operating system, LGS, application services, each in its own repository with its own data contract) and draft a description format, a manifest, that says how one component depends on another and which versions are compatible. Alexander: the purpose is compatibility, not registration. It answers "can this new LGS version be installed on a machine with this set of components, or this game added, or this framework updated." Dzmitry called it a future paradigm rather than a spike. Nobody objected; no deadline was set.

**Why registration blocks updates.** Dzmitry: remote updates depend on machines being registered in the system. Without registered machines nothing can be selected on the server, so no update test is possible. Pavel added that today you cannot pick software, games or battle sets for a machine that does not exist in the database.

**How registration works today, and what goes wrong.**
- At manufacture a technician scans the passport QR on the machine screen with a phone, then scans a barcode of the cabinet serial (a number like CM08… whose digits depend on month and year).
- The metal plate on the cabinet carries plain stamped digits only, no barcode. Alexander and Andrei both thought it had a barcode. Someone types the digits by hand into a barcode generator, which is where the errors come from: Cyrillic letters, the letter O for zero, extra spaces. Some machines later have to be re-registered because the wrong plate went on the wrong machine.
- Serial numbers are reserved about a month ahead by a chief engineer because the metal plates have to be made in advance. Dzmitry does not know whether these numbers are also entered into Business Central (Navision) in advance.
- Val: this process comes from the time JVL made about 1,000 Echo machines a month and had to order labels in print runs. Now JVL makes single machines at much higher prices, so the label process can change. If Genadi or Lev enter numbers in BC in advance, that can change too, but they must be brought into the conversation.
- Dzmitry also said the barcode scanning on some iPhone versions is unreliable; the technicians at Novitski's report it often.

**Proposal A: one scan, server generates the serial (Dzmitry).** The machine connects to the server by default and waits. The technician, logged in with the right role, scans the passport QR. The server checks that this set of hardware (for example this IO board) was never registered, generates a cabinet serial from the cabinet type and today's date, sends it to the machine. The machine writes it to the Dallas chip and confirms. The technician sees "registered" on screen, then prints the number as a barcode label and sticks it on. Dzmitry: this is like the Flex IQ flow minus the barcode scan. Pavel: a logged-in person is still required so that someone cannot run the software on any computer and mint fake machines; this was the original fool-proofing. Dzmitry said the same scheme can also issue each machine its own encryption key for future communication; Andrei agreed. Dzmitry: "I like the whole proposed scheme." Val at the end: needs to think.

**Proposal B: machine self-registers (Pavel).** Boot from a USB stick with a diagnostic; once the base passes its tests, the machine asks the server for a number by itself. Pavel first suggested this could remove the human from the loop. Dzmitry and Pavel then agreed a human login is still needed, so B folded into A.

**The label.** Pavel: the root problem is a plate with stamped digits and no barcode; either stamp a real barcode or QR on the plate, or try to read the digits. Alexander: an RFID tag, or a plate with a Dallas built in. Pavel: RFID tags are not vandal-proof and do not solve telling the casino or location owner its number. Val's proposal: stop relying on the metal plate. The Dallas is the keeper of truth. At the very last step print a label, barcode plus human-readable digits, on waterproof plastic, and reprint it any time it is lost, damaged or mixed up. Pavel: if the technician printed several labels and mixed them up, he must be able to boot some software and read what is in the Dallas; Val: the number can also be shown on screen while sticking the label. Pavel: writing the number into the Dallas was built about 3 years ago; what was never built is the CMS showing that number back. Alexander asked whether this is a big enough problem to change the flow; Dzmitry: not big, but the goal has always been fewer actions and fewer errors.

**Dallas chip replacement.** Pavel: if the serial lives in the Dallas, there must be a procedure to reuse the cabinet serial on a new chip. Today that is a re-registration: scan the plate again, scan the passport again. Val: how hard is it physically? The harness with the Dallas is swapped, the machine boots and says "I don't know who I am." Options discussed:
- Dzmitry: keep a duplicate of the number in a store (database or disk) and have the machine compare Dallas against the store at every boot and react to a mismatch.
- Pavel: the non-erasable storage on disk already survives reinstalls; keep the last Dallas content there. With a new empty Dallas the machine sees its components match the saved passport, offers to restore the old cabinet serial, and in the ideal case works again at once even with no internet.
- Dzmitry: this must go through the server, and the machine must send its full component list (CPU box, bill validator, printer), because the server has to tell a Dallas replacement apart from a new machine built from a scavenged CPU box. Done offline it can collide: a CPU box moved from another machine confirms a number that does not match the barcode on the plate.
- Val: the core question is that a machine with a new Dallas boots empty, as if it were new manufacture, and someone must decide whether this is a new manufacture or a replacement. Not resolved.

**Assembly and Business Central (Andrei B).** Andrei: the order of events is really spec first, assemble second, confirm third, so the new CMS should also look at the assembly process; maybe this belongs in Business Central. Dzmitry: a BOM in BC is very wide (wires, plastics); the link could be BC creates the build request, the server assigns the serial to the request, and registration attaches the machine automatically. Alexander and Val: first define what problem is being solved. Open.

**Peripherals and RIS.** Andrei asked what happens when a printer fails right after registration and is replaced. Evgeny: after the latest changes it depends on RIS settings; the passport screen shows only when the Dallas is empty, otherwise the machine waits for RIS. Pavel: RIS is not a manufacturing step; manufacturing often makes a bare machine with no bill acceptor or printer, and those are added depending on which operator it ships to. Val stated the direction and everyone said yes: at manufacture only the base must come up (CPU box, IO board, monitors, the base game). Topper, bill validator and printer can be switched on, off, added, swapped at any time; JVL does not control peripherals. Irina: the current RIS improvements add, remove and change printer and bill validator on the fly. Evgeny: printer works fully; for the bill validator, changing the model works but add and remove do not yet. Irina: to discuss later. Pavel: if there is no passport screen, the mandatory passport update happens when the lease is scanned; the data goes to the server even if the machine is offline and the activation code writes the new passport to the Dallas. Val: "Why? I need to sit and think."

**Jurisdiction check at registration.** Dzmitry suggested the technician also states the jurisdiction so the server can check the required devices are present (so a Florida location does not get a dead bill validator). Pavel: do not add limitations now, we only shoot ourselves in the foot. Val: this is not manufacture, it is the sales process controlled by RIS and recorded in Business Central, and RIS is being decoupled from the old jurisdiction binding (for example Mexico machines not allowed a bill acceptor). Irina: whether a bill validator works has no bearing on creating the passport and number.

## Decisions Made

- **At manufacture only the base must work: CPU box, IO board, monitors, base game. Peripherals (topper, bill validator, printer) are not checked at registration and can be added, removed or swapped at any time.** — Reason: JVL does not control peripherals and does not want to force a technician to redo RIS when a device is added on the fly. (Stated by Val, confirmed "yes" by Irina, Pavel, Dzmitry)
- **No jurisdiction or device-completeness check at registration.** — Reason: that is the sales process, handled by RIS and Business Central, and adding limits now only hurts. (Pavel, Val)
- **Considered and not decided:** server-generated serial with one passport scan; reprintable barcode label instead of relying on the stamped plate; Dallas replacement recovery (offline vs server-confirmed); BC/BOM integration; passport update via lease scan. Val: "I need the transcript and time to think."

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val | Read this transcript, think through the registration scheme (one-scan server serial, printed label, Dallas replacement) and come back with a position | TBD | High | Val closed the meeting with this (1:07:17) |
| 2 | Dzmitry | Study the components and repositories and draft a manifest format describing component dependencies and compatibility, for the group to review | TBD | Normal | Self-proposed at the start (0:00:38); nobody objected, no date set |
| 3 | [Unassigned — needs clarification] | Ask Genadi or Lev whether cabinet serial numbers are entered into Business Central in advance from the BOM | TBD | Normal | Dzmitry raised it (0:35:28); Val said they must be involved; nobody took it |
| 4 | Irina, Evgeny | Follow up on bill validator add/remove on the fly, which does not work yet (model change works) | TBD | Normal | Irina: "we'll talk about this later" (1:04:09) |

## Open Questions

- Should the server generate the cabinet serial at registration with one passport scan, replacing pre-reserved numbers? (Dzmitry; Val to think)
- Replace the stamped metal plate with a printed, reprintable barcode label, the Dallas being the source of truth? (Val; Alexander suggested RFID or a plate with built-in Dallas)
- How to keep the cabinet serial when a Dallas chip is replaced: offline restore from disk storage (Pavel) or server-confirmed with the full component list (Dzmitry)? How does the machine know "replacement" vs "new manufacture"? (Val)
- Should registration integrate with Business Central and the BOM / build request? (Andrei B, Dzmitry)
- Passport update through lease scan plus activation code when there is no passport screen: Val did not accept it yet. (Pavel)
- Bill validator add/remove on the fly not working. (Evgeny)

## Dispatch Log

---
*Processed from Teams transcript on November 8, 2026, 8:45 AM Eastern (meeting-watcher scheduled run)*
*Source meeting: Nova 2 and Galaxy*
