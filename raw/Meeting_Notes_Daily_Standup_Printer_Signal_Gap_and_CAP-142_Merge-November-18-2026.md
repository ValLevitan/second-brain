# Meeting Summary — Daily Standup meeting
**Date:** November 18, 2026, 3:45 AM – ~4:30 AM Eastern (recording ran to 4:50 AM)
**Duration:** ~45 minutes of meeting; recording ~65 minutes
**Attendees:** Pavel Frolov (led), Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dmitri Kovalchuk, Dzmitry Chudzinau, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Vladimir Samusenko, Emma (AI-PM voice assistant)
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_Printer_Signal_Gap_and_CAP-142_Merge-November-18-2026]]

## Summary

**Emma (AI-PM) in the call.** Irina asked Emma to wait 10 minutes for Pavel. Dmitri K: answer Emma's questions in chat; questions form a queue and she will not send new reminders until earlier ones are answered. Irina told Emma not to create tasks from the side talk about images. Dzmitry said Emma asks him to move a date on requirement REQ-1864, but requirements have no dates; Dmitri K asked for the number to check.

**Messages resources (Daniil's task).** Alexander: take the old engine's resources as placeholders now; a designer (Lena) can pick new images later. Irina worried we will lose track of what must be redone. No final decision.

**Scope gap: printer on new Flex IQ interface boards (Georgia).** Pavel: yesterday in Georgia the printer did not work on the new interface boards. The new board revision passes the signal straight through when Flex IQ is off; when Flex IQ boots it must set one signal to switch the lines. Flex IQ software does not set it, so Gen 2 / Epic printers get no signal on the new boards. About one hour of work; Pavel will create the task and do it today. Dzmitry and Vladimir objected that there are no requirements for the Mutoguz/printer setup; Pavel: forget Mutoguz — many new boards are out and must work with a normal printer.

**Duplicate capability CAP-142.** Vladimir asked if he can take CAP-142 (Wi-Fi setup by QR code on the Flex IQ screen). It has only spikes and TINTs, no features, and sits in MVP 3. Sergey said the function is already done. Pavel: Sergey finds which capability the work was done under; then Claude merges the two capabilities, otherwise autotests will be duplicated. Vladimir takes CAP-289 and other autotests meanwhile.

**Status by person:**
- **Alexander:** bill validator spray mode works; he will close his test task. Not working: paying an arbitrary sum (e.g. $289) mixed across drums — the amount per drum must be given. Spray will be default; switching mode from the terminal is possible. The SD installer builds like Flex IQ; update packages (OS/app) do not build yet. Irina asked him to review recycler capabilities and put the right ones in MVP 1 (unknown → backlog); he agreed.
- **Alexey:** worked on state law vs our requirements for Val; another meeting with Val coming. Doing hardware tests in parallel. Irina: tests need real time, not "a little".
- **Anton S:** will close in-progress items today. Left: run the port power-off scenario by hand; check USB firmware matches network firmware. Open TINT questions: after a reboot during an update, the port restarts the download instead of resuming as the rules say. Sergey does not remember when it resumes; Irina: Anton checks the code. Pavel: a report said prose for RK3568 is thin; Sergey: a job updates prose on each PR.
- **Daniil:** opened his NewGin task; needs access to the old RAGE engine and framework (SVN). Pavel: ask Igor where the engine repo is. Alexander: start with the framework only; admins to give Daniil SVN framework access. Later Dmitri K said Daniil already has HD engine and HD casino access; Irina and Alexander said that is enough for now; Igor will say if more is needed.
- **Dzmitry:** Flex IQ builder — the agent fixed flaky tests; split into 2 tasks; he works on it now. With Andrei, the new stack is deployed and works. LTE checked on STG today; data arrives. Asked about an old task with no requirements or capability; Pavel: close it with a comment that it was a placeholder (Dzmitry cannot delete). Pavel: Val cares about readiness, not task state.
- **Evgeny:** ISO build with math done, testing now. Many hardware-service changes (constant device monitoring). Components can now be built from any source, not only a release. Answered Ivan's RIS questions; 3 fixes.
- **Irina:** autotests and requirements for the old framework. Overdue tasks dated 16th–17th are deferred items; she is moving them.
- **Ivan:** LTE tests passed; data reaches the server; LTE could be closed (question: how much for Georgia). RIS continues: yellow board left, a couple of days of tests. Irina wants Felipe's answer; ping him when nearly done. Bugs: Igor made fixes, Ivan has not reviewed yet; 2 bugs wait for answers from the other party (not named; likely the RIS/Felipe side). Efim noted a paytable/math update is needed — do not forget. Ivan still has no access to their system; Irina: ping them again today.
- **Sergey:** finished lotteries and the new ticket; closing the PR; next is phone numbers on the help screen.
- **Vladimir:** autotests for CAP-245/287; sent questions to Andrei/Sergey.

**Other.** Dmitri K: watch due dates. Anton: Jira comments load badly for him (VPN); others had no issue. Irina will give Anton more autotests when he finishes.

## Decisions Made

- **Fix the printer signal on new Flex IQ interface boards now (~1 hour task).** — New boards are in the field and printers get no signal. (Decided by Pavel)
- **CAP-142 duplicate: Sergey finds the capability where the QR Wi-Fi work was done, then Claude merges them.** — Avoid duplicate autotests. (Decided by Pavel)
- **Old placeholder task without requirements is closed with a comment.** — Cannot delete; does not meet the standard. (Decided by Pavel)
- **Daniil starts with the access he has now (HD engine, HD casino); Igor says if more is needed.** (Dmitri K, Irina, Alexander)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Create and do the task: Flex IQ sets the signal at boot so printers work on new interface boards | Nov 18, 2026 | High | Georgia printer problem |
| 2 | Sergey Tsimanov | Find which capability holds the QR Wi-Fi setup work (CAP-142 duplicate) | TBD | Normal | Then Claude merges capabilities |
| 3 | Alexander Biratko | Review recycler capabilities and place them in MVP 1 / backlog | TBD | Normal | Irina's request |
| 4 | Alexander Biratko | Close the spray-mode test task | Nov 18, 2026 | Low | Spray mode tested and works |
| 5 | Anton Seregin | Check the code for when the port resumes vs restarts a firmware download | TBD | Normal | Rules say resume |
| 6 | Anton Seregin | Close in-progress items; run port power-off scenario by hand | Nov 18, 2026 | Normal | |
| 7 | Dzmitry Chudzinau | Close the old placeholder task with a comment | Nov 18, 2026 | Low | |
| 8 | Dmitri Kovalchuk | Check why Emma asks to move a date on REQ-1864 | TBD | Low | Requirements have no dates |
| 9 | Dmitri Kovalchuk | Daniil's repo access (HD engine, HD casino) — in place; handle any further access | Done Nov 18, 2026 | Low | Igor says if more is needed |
| 10 | Ivan Shpak | Finish RIS tests and tell Irina when near the end so she can ping Felipe | TBD | Normal | |
| 11 | Ivan Shpak / Irina Shishko | Ping the other party (likely RIS/Felipe side) again today about access and bug answers | Nov 18, 2026 | Normal | |
| 12 | Ivan Shpak | Review Igor's bug fixes; do not forget Efim's paytable/math update | TBD | Normal | |
| 13 | Vladimir Samusenko | Work on CAP-289 and other autotests while CAP-142 is sorted | TBD | Normal | |

## Open Questions

- Messages resources: use old images as placeholders or redraw first? (Alexander vs Irina, not settled)
- LTE: close it now, and how much is needed for Georgia? (Ivan)
- When should the port resume vs restart a firmware download? (Anton; Sergey does not remember)

## Dispatch Log

---
*Processed from Teams transcript on November 18, 2026*
*Source meeting: Daily Standup meeting*
