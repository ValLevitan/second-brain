# Meeting Summary — RIS+Modem Flex-GACOM Status update
**Date:** November 25, 2026, 11:02 AM Eastern
**Duration:** 28 minutes
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko
**Language:** Russian (about 00:33–06:05 was transcribed as broken English and has no usable content)
**Raw transcript:** [[Meeting_Transcript_RIS_Modem_Sebastian_Checklist_and_SD_VLT_RIS_Port-November-25-2026]]

## Summary

**Modem testing in Georgia (Sebastian).** Val spoke with Sebastian yesterday. Sebastian had 75 acceptance criteria to check for RIS. Val liked this and wants the same for the modem. Pavel: for the modem Sebastian checks only what was asked in the change. If the machine is offline, a QR window shows; he scans it, the phone says the request is accepted, and he enters the activation code. He does not test all Wi-Fi functions. Irina: the modem capability has no requirement with acceptance criteria (the link points to the wrong requirement). But there is a test plan for the LTE modem with test cases.

**Why instructions are needed anyway.** Val does not want Sebastian to do half the work or spin his wheels. Pavel: we need modem instructions in any case — how to check it works with the vendor tool, in setup, and in the setup of regular games; how to see its state and find problems. Field support will need this months from now. Val added: how to know the data reaches the server.

**Plan.** Sebastian stops testing the modem today. Ivan turns his LTE modem test plan into a simple checklist and sends it by tomorrow evening (Minsk time). Sebastian finishes the modem test when he is back on Friday.

**South Dakota VLT build.** Val proposed adding the new RIS. Pavel and Irina agreed. Val: do not add the modem. Irina: a machine without a modem gives GLI nothing to test; if GLI sees the code, we say it is not for the South Dakota market. GLI found some errors; part are fixed. For two issues JVL asked GLI for more detail; GLI is slow but has started to answer. It is not clear these are real problems. So the next build needs the new RIS and answers to these two issues.

**Jira for the SD VLT RIS work.** There is a Jira release for SD VLT fixes with RIS improvements, capabilities about 304–310. These capabilities have no features yet; Evgeny has not moved them. Val asked if they should move to GitHub. Irina: no, they were placed there on purpose for GLI. Val agreed. Pavel: ten capabilities is too many for this work. One capability ("apply RIS improvements to SD VLT") with one feature for moving the commits, then testing by Ivan, would do. Irina: it is a merge of existing changes into another branch, not new development. Val accepts any option.

**Timing.** Evgeny can move the changes as soon as asked. Testing: about one week if all goes well, because GLI will review it again and many RIS cases must be re-checked. Val accepted one week.

## Decisions Made

- **Sebastian stops modem testing today and finishes on Friday with Ivan's checklist.** (Val; Pavel and Irina agreed)
- **South Dakota VLT gets the new RIS but not the modem.** (Val)
- **The SD VLT RIS capabilities stay where they are (not moved to GitHub), because of GLI.** (Irina; Val agreed)
- **About one week of testing is accepted for the SD VLT RIS port.** (Irina estimate; Val accepted)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Ivan (via Pavel / Irina) | Turn the LTE modem test plan into a simple checklist for Sebastian and send it | Nov 26, 2026 (Minsk evening) | High | Also first version of modem check instructions |
| 2 | Sebastian | Finish the modem test with the checklist | Nov 27, 2026 | High | Back at work Friday |
| 3 | Pavel Frolov / Irina Shishko | Have modem support instructions written: how to check the modem, its state, data to the server, and problems | TBD | Normal | Needed for field support |
| 4 | Pavel Frolov | Plan the SD VLT RIS capabilities on the Minsk side (possibly one capability, one feature) | TBD | Normal | |
| 5 | Evgeny | Merge the RIS improvement commits into the SD VLT branch | TBD | Normal | As soon as asked |
| 6 | Ivan | Test the SD VLT build with the RIS changes | About Dec 2, 2026 | Normal | About one week |
| 7 | [Unassigned — needs clarification] | Answer GLI on the two open SD VLT issues once GLI sends more detail | TBD | Normal | |

## Open Questions

- Are the two issues GLI raised real problems? Waiting for GLI. (Irina)
- The modem capability links to the wrong requirement; no requirement with acceptance criteria exists yet. (Irina)
- Heard unclearly: "соборщивым" (taken as Sebastian); capability "297"; "скетчёл".

## Dispatch Log

---
*Processed from Teams transcript on November 25, 2026, ~12:30 PM Eastern*
*Source meeting: RIS+Modem Flex-GACOM Status update*
