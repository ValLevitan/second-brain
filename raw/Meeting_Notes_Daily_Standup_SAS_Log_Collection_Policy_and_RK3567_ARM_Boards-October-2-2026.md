# Meeting Summary — Daily Standup meeting
**Date:** October 2, 2026, 4:50 AM – 5:25 AM Eastern
**Duration:** ~35 minutes
**Attendees:** Pavel Frolov, Alexander Biratko, Alexey Khamin, Anton Seregin, Daniil Stauskiy, Dzmitry Chudzinau, Vladimir Samusenko, Evgeny Kharetski, Irina Shishko, Ivan Shpak, Sergey Tsimanov, Dmitri Kovalchuk
**Raw transcript:** [[Meeting_Transcript_Daily_Standup_SAS_Log_Collection_Policy_and_RK3567_ARM_Boards-October-2-2026]]

## Summary

Round-robin standup run by Pavel. Held in Russian.

**SAS command logs: collect, do not send.** Dzmitry's next item was sending SAS command logs from the machine to Grafana. Pavel pushed back: do not send by default, make it selective per machine and off by default, because it would flood the modem channel. Dzmitry proposed keeping the collection on the Flex IQ and not sending; anyone can connect and read it there. Pavel agreed. Dzmitry will review total traffic over the weekend anyway (door open/close, collections).

**New ARM boards.** Pavel: the RK3567 boards with 8 GB memory arrived. Plan: run the new game on it in the browser, one monitor first, and see where it breaks. Biratko: also try compiling Rage for ARM; the FMOD sound library may be the blocker (sources and ARM version uncertain).

**Device services bugs.** Biratko found bugs in the new validator and IO board services (HWBB-8): the IO board misread a sensor, and validator statuses after reboot or a half-swallowed bill were restored wrongly. 3–4 tasks opened and closed in the IO board and bill acceptor repos. LED strip from the IO board uses the same protocol, one channel instead of three. Still testing.

**Video codec.** Daniil finished feature 1386. Rage videos were VP9; the repo uses VP8, which loses quality. He re-encoded with the Rage settings but is unsure the machine browser supports it. Biratko: VP8 ran faster in earlier tests; check the machine browser and talk to the designers about conversion.

**Transactional.** Dzmitry: requirement gaps collected; PO-175 dashboard mostly done but stays open for enrollment entities; Flex IQ connect/disconnect done; needs Pavel's PR approval (port and arrows), then a new build on 84. Andrei did a security policy; SDK rebuild needed. Repo standards: he and Sergey split 7–8 repos; prose and ADRs are to standard for the transactional system. Claude found some issues with the login agent. Vladimir: file Claude-plugin bugs in the plugin repo; he will send the link. Pavel: no prose for archived repos such as the old updater.

**Eclipse and South Dakota.** Ivan is sending files to Eclipse; certificate drafts may come today; build 43.33 uploaded. Irina: give the build number and amounts the certificate lists. Efim wrote about South Dakota: minimum bet changed from 50 cents to 40. Irina: create a RIS with 40 cents and check the machine comes up; no rebuild, there were no commits. South Dakota is not released yet.

**Jira hygiene.** Sergey's red tasks: a feature Vladimir reopened with stories, date not updated. Irina: whoever takes a feature into work must update its schedule through Pavel or her. Val wrote to Sergey that a GitHub feature branch does not match Jira; probably a prefix issue from a Claude-created branch. Pavel: keep watching Claude, it opens branches and invents names instead of checking Jira. Kovalchuk: keep Jira discipline, ask Claude to move dates. Jira shows today's date in red; Kovalchuk will drop that from his report and check if Jira itself can change.

**Other.** Evgeny closes LGS-12, 17, 19 and CC Talk today. Anton builds emulator diffs for scenarios 102/103, then compares with a real device. Vladimir reviews Lyosha's work and finishes task 34 (blocks); he lacks context for the Jira stories he creates. Pavel: talk it through with Irina or Lyosha first. Irina starts acceptance criteria and tests for FlexPay; asks Vladimir, Lyosha and Vanya to mark done items in Jira. Weekend: Dzmitry Saturday and Sunday, Sergey yes, Biratko Saturday, Khamin repo cleanup. Val's repo grooming message applies to everyone.

## Decisions Made

- **SAS command logs are collected on the Flex IQ and not sent to Grafana by default.** — Sending would flood the modem channel; the IQ can be read on demand. (Decided by Pavel Frolov, Dzmitry Chudzinau)
- **Whoever takes a feature into work updates its schedule with Pavel or Irina.** — Reopened features were showing stale red dates. (Decided by Irina Shishko)
- **No prose for archived repos such as the old updater.** — They will not be used. (Decided by Pavel Frolov)
- **South Dakota: build a RIS with the 40-cent minimum bet; no rebuild.** — No code commits were involved. (Decided by Irina Shishko, Ivan Shpak)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Approve Dzmitry's pull request (port and arrows) | TBD | High | Blocks the new build on 84 |
| 2 | Dzmitry Chudzinau | Build and deploy new build on 84 after approval; review total modem traffic over the weekend | 2026-10-05 | Normal | SAS log policy |
| 3 | Daniil Stauskiy | Check the re-encoded video on the machine browser and settle the codec with the designers | TBD | Normal | Feature 1386, VP9 vs VP8 |
| 4 | Pavel Frolov | Run the new game on the RK3567 8 GB board in the browser | TBD | Normal | One-monitor setup first |
| 5 | Alexander Biratko | Try compiling Rage for ARM; check FMOD availability | TBD | Low | His own proposal, for the record |
| 6 | Evgeny Kharetski | Close LGS-12, LGS-17, LGS-19 and CC Talk (58) | 2026-10-02 | Normal | Statistics, LEDs, IO board |
| 7 | Ivan Shpak | Send files to Eclipse; give Irina the build number (43.33) and certificate amounts | 2026-10-02 | Normal | Certificate drafts expected |
| 8 | Ivan Shpak | Create a RIS with the 40-cent minimum bet for South Dakota and test it | TBD | Normal | Per Efim's note |
| 9 | Sergey Tsimanov | Update the dates on the reopened feature | 2026-10-02 | Normal | Red tasks in Jira |
| 10 | Vladimir Samusenko | Send Dzmitry the Claude-plugin repo link | 2026-10-02 | Low | For filing plugin bugs |
| 11 | Dzmitry Chudzinau | Collect the Claude-plugin issues and file them | TBD | Low | Session still open |
| 12 | Dmitri Kovalchuk | Remove today's-date red highlight from the report; check if Jira can be changed | TBD | Low | |
| 13 | Vladimir Samusenko, Alexey Khamin, Ivan Shpak | Mark completed items in Jira so Irina can refresh the schedule | TBD | Normal | |

## Open Questions

- Does the machine browser support the VP9-style encoding Daniil used? Raised by Daniil Stauskiy.
- Is FMOD available for ARM to compile Rage? Raised by Alexander Biratko.
- What exactly did Val flag in Sergey's GitHub feature branch? Raised by Sergey Tsimanov, not resolved.

## Dispatch Log

---
*Processed from Teams transcript on October 5, 2026*
*Source meeting: Daily Standup meeting*
