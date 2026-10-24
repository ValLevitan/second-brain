# Meeting Summary — refinement of RIS improvement Pros
**Date:** October 20, 2026, 10:49 AM – 12:15 PM Eastern
**Duration:** ~65 minutes of meeting (recording runs 86 minutes; after 01:05 only Felipe stays connected, with side talk)
**Attendees:** Val Levitan, Felipe Miranda Giorgi, Pavel Frolov, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_RIS_Improvements_Release_Notes_Review-October-20-2026]]

## Summary

Val went through the RIS Improvements release notes point by point (9 points) to fix the wording. Point 1 was reviewed earlier without recording; Val repeated the changes on the record. Some parts are in Russian and parts of the transcript are garbled (about 00:08–00:18, 00:26–00:27, 00:33–00:36 and 00:46–00:50). There is no speech from 00:50 to 00:55.

**Point 1.** Remove the word "new" in "new setup file on the USB". Remove the sentences "A lost date and time is no longer a critical error", "will the clock need to be set up again" and "I do not know yet".

**Point 2 — software upgrade.** Rewritten by Val and agreed: today every upgrade needs a new setup file from JVL on USB for each machine. After the release the machine keeps its full configuration through an upgrade (cabinet, peripherals, games, bet buttons, denominations). If the game math does not change, a new setup file is not required. If a new setup is required, the machine gets it through a modem or a USB. Pavel noted that one USB stick can hold the RIS files for several machines. Irina: if games or main settings change (bet buttons, game percentages), a new RIS from USB is needed; otherwise the old RIS can be reused. Pavel: a new setup file is exported from the CMS.

Felipe shared replies he got from Intralot: there is no restriction on when a hard reset is done, and a soft reset needs no decommissioning because lifetime meters are not affected. Val said he thought this was known already and kept the talk on the release notes.

**Point 3.** The soft-reset question is removed. The statement stays: no hard reset, no new setup files, no USB, no call to JVL (Pavel confirmed). Felipe asked if the printer on/off switch is available at any time before a hard reset. Pavel: yes, even with money on the machine. Felipe has another question about wrong printer firmware, but said it does not belong here.

**Point 4 — lease when records do not match the machine.** After the release the lease is issued on its own for the software on the machine, with no action at JVL and no passport step. Pavel: someone still has to scan the updated lease, but anyone can do it, no login needed. The lease keeps the end date of the previous installation; it is not extended (fully paid machines run to 2030, end of life). Val added: "The current lease period will remain unaltered."

**Point 5 — replacing a peripheral.** Val changed "part" to "peripheral, such as a bill acceptor", and "today" to "currently" (and asked to make that change everywhere). Currently, at the next reset, the machine stops at the passport screen, and a technician must photograph a QR code, send it to JVL, wait for a code and enter it. After the release the machine registers the new peripheral on its own and goes back to play. Pavel: to the user it looks like that; inside, the passport update waits until the next lease scan, which needs no login. Val: that detail does not matter for the notes.

**Point 6 — machines missed during an upgrade.** Felipe did not like the wording. His example: 20 cabinets are upgraded, 2 are missed; today, at the lease re-scan, the machine shows a settings mismatch and the technician must come to JVL for the setup file. After the release the missed machine keeps working on its old RIS until the lease date set at installation. Pavel: the CMS will report machines that still use an old RIS when a new one exists. Pavel gave three options for the lease scan in this case: refuse the lease and require a reinstall; keep issuing the lease until the old lease end; or issue it until the new RIS lease date. Felipe proposed giving one more lease interval with a warning that a software upgrade is required by a set date (about a month), and then stop. Pavel said this can be done; Felipe called it the best option. Val said he lost focus during this part, is fine with any wording, and his goal is satisfied Georgia customers. Irina raised the case of a new RIS on the same software with a different set of games (15 games, 8 at a time); this part is mostly garbled. Val then put Felipe's written paragraph in as point 6.

**Point 7 — critical errors.** Pavel: the team is not ready for a new list of error codes now. The error screen will show a message that names the cause; the QR code will carry the error code, serial number and software version. Felipe's idea: the QR code opens a page with the most likely causes and troubleshooting steps. Pavel: server-side help, maybe with AI, can come later. Val's wording: after the release, the screen will name the cause of the error.

**Point 8 — lease renewal.** Clear, no change.

**Point 9 — last paragraph (transaction history).** Pavel suggested a filter on the transaction screen (for example, cash-outs only). Felipe: that does not fix the real problem — the log is small (about 81 pages of 20 records) and is overwritten within about two hours of play. Left as written.

**Close.** Felipe asked for the final draft; Val said this is the clean draft and asked Felipe to print it for the operator visit. Val suggested the team update the task descriptions in the repository, the capability, and the requirements and acceptance criteria to match the release notes, so automated tests are possible and manual testing stops. Val told Pavel he will try not to disturb him tomorrow so he can catch up on today's undertakings.

## Decisions Made

- **Point 2 uses Val's rewritten text** (full configuration kept; no new setup file if game math does not change; otherwise modem or USB). (Val; agreed)
- **Point 4 adds "The current lease period will remain unaltered."** (Val; Pavel agreed)
- **Point 5 says "peripheral, such as a bill acceptor" and "currently" instead of "today".** (Val)
- **Point 6 uses Felipe's paragraph.** (Val)
- **Point 7: no new error-code list now; the screen will name the cause of the error.** (Pavel, Val)
- **Point 9 stays as written.** (Pavel, Felipe)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Print the clean release notes for the operator visit | Oct 20, 2026 | High | Val: "we got around to see the operator" |
| 2 | Pavel Frolov, Irina Shishko | Update task descriptions, the capability, and requirements/acceptance criteria to match the release notes | TBD | Normal | Val's suggestion, so automated tests are possible |
| 3 | Pavel Frolov | Catch up on today's undertakings | Oct 21, 2026 | Normal | Val will try not to interrupt him |

## Open Questions

- Point 6 behavior: is the rule "one more lease interval with an upgrade warning, then stop" final? Pavel and Felipe agreed; Val did not decide. (Pavel)
- Which RIS is allowed when a new RIS on the same software changes the game set (15 games, 8 at a time)? (Irina) — mostly garbled, no answer recorded.
- Wrong printer firmware not recognized by the machine. (Felipe) — set aside as not relevant to these notes.

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-20 14:20 ET*
*Source meeting: refinement of RIS improvement Pros*
