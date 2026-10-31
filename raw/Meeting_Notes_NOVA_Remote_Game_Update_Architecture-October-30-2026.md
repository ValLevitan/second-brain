# Meeting Summary — Discussion: downloading games to remote machines via modem
**Date:** October 30, 2026, 9:03 AM – 10:44 AM Eastern
**Duration:** about 1 hour 41 minutes
**Attendees:** Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Alexander Biratko, Irina Shishko
**Raw transcript:** [[Meeting_Transcript_NOVA_Remote_Game_Update_Architecture-October-30-2026]]

Held in Russian. Val opened the meeting to build a technical brief for engineers on remote game delivery, then stepped back and let the team talk.

## Summary

**Scope.** Remote update is for the new NOVA platform only. The current platform cannot do it. First target market is Texas, where there are no certification limits on updates.

**Three kinds of markets.** Pavel: strict locations that allow no updates; middle markets where we decommission, update, and the lab (Intralot named) knows the new checksums; and free markets where we can change anything. Val: even with no outside control, we must keep our own control at the same level.

**How an update works (Pavel's model).** A cloud server holds every released version with signatures. The machine downloads, computes checksums, sends a "fingerprint" of everything installed to the server, and switches only if the server approves. Two partition slots (A/B, RAUC-style, as on Transactional): update the spare slot, switch, reboot; after 3–4 failed boots the machine falls back to the old slot. The master partition holds separate modules: games, math containers, LGS, bonuses, progressive controller, HAL packages. Each module can be replaced alone if the server accepts the new set.

**Components and compatibility.** Dzmitry: split today's build into components with versions, stored with a description (S3 named). The hard part is the compatibility map: which game can go on which LGS, framework and progressive controller version. Proven by automatic test runs on a stand, which then write a manifest the server uses. Pavel: AI should track component compatibility. Dzmitry wants a tool that compares two builds and lists the component differences.

**Patch vs full image.** Pavel: in checksum-controlled markets, skip file patches and send the full new system image (about 1 GB), so checksums are known. Alexander and Dzmitry want delta updates — much smaller transfers. Dzmitry: on Flex-IQ, 300 MB took 20–30 minutes at about 6 Mbit/s; 1 GB would take hours. Pavel expects the Linux system to change rarely; most changes go into small modules on the master partition, where files are signed one by one. Not settled; needs testing.

**Math.** Today math is one certified Docker image for many games. Alexander asked why not math per game. Pavel: shared image is certified once at GLI and reused. Agreed point: if the contract between game and math stays the same, math can be updated alone, which sends less data — but the lab must test the build.

**Storage and statistics.** Adding or removing a game is not supported in LGS storage today. Old game counters and daily stats must be hidden or removed. Options: reserve space for future games, or dump and regenerate storage after a game change. Alexander: keep last records in fast storage and move them to the database when the machine is idle; writing to two places at once can split a transaction. ARM uses slower eMMC; Pavel suggests the database on a replaceable SD card. Alexander and Dzmitry want the same approach on x86 and ARM.

**Who runs the update.** Val: an admin dashboard must exist, and sold machines must be able to use our management platform. Dzmitry: on Flex-IQ a RAUC-style agent starts first, talks to the server, checks checksums, and rolls back. Who manages the update on NOVA (LGS or a separate agent) was raised, not decided.

**After the update.** Alexander: after an update, run a self-check (checksums, boot, screen). Pavel: fake test spins on all games at startup, kept out of statistics. Val: if no money enters the machine for about 24 hours after an update, that is a problem. Alexander: if nothing was played, roll back and alert; once games are played, rollback is no longer safe. Rollback must also restore LGS storage data. If the machine holds the progressive master, move the master first, then update the others.

**Process.** Val: copy proven practices for updating devices (Apple named) instead of inventing everything. Split releases into MVPs. Jira release names: project name, then MVP number. Irina: keep names short. Val reminded everyone that the standards repo in GitHub holds all standards, and asked each person to add their own standards there.

## Decisions Made

- **Remote update is for NOVA only, not the current platform** — the current design cannot support it. (Pavel, Irina, Alexander)
- **First target market is Texas** — no certification limits on updates there. (Val, Irina)
- **Write the full architecture first; split into MVPs and schedules after** — Val wants the final picture (for example MVP 10) agreed now, then the MVP split. (Val; Dzmitry agreed)
- **The list of allowed updates must exist the same way for our machines and sold machines** — sold machines' owners can use our management platform. (Val)
- **Architecture decisions are recorded in the NOVA integration repository** — it touches all repositories. (Pavel proposed; Val: "agreed")
- **Release names in Jira follow a standard: project name, then MVP number** — exact name for this work not settled. (Val)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Pavel Frolov | Update the remote-update architecture document with today's discussion, plus a list of capabilities and open questions | Fri Nov 6, 2026 | High | Review meeting in one week |
| 2 | Val Levitan | Schedule the review meeting for 9:00 AM next Friday | Fri Nov 6, 2026 | Normal | Review the updated architecture document |
| 3 | Dzmitry Chudzinau | Organize sessions on Galaxy questions: machine registration, jurisdictions, users, changes to server work | Next week (TBD) | Normal | Feeds the Galaxy architecture |
| 4 | Alexander Biratko | Work out how LGS fits into remote update and into NOVA | TBD | Normal | [Needs Val's confirmation] — Pavel proposed it; Alexander did not confirm |
| 5 | [Unassigned — needs clarification] | Write requirements for automatic self-check after an update | TBD | Normal | Alexander: "for the transcript"; tests to be defined later |
| 6 | All attendees | Add your own standards to the GitHub standards repository | TBD | Low | Val's request |

## Open Questions

- Patch (delta) updates or full image in checksum-controlled markets? Pavel prefers full image; Alexander and Dzmitry want deltas. Needs a test. (Pavel, Alexander, Dzmitry)
- Math per game or one shared certified image? (Alexander)
- LGS storage: how to add or remove games without losing history; counters vs database. (Alexander, Dzmitry)
- Who manages the update on the machine: LGS or a separate first-start agent? (Alexander)
- How operators get update packages — the same list or a per-operator list? (Pavel, Dzmitry)
- Real experiments must wait until Evgeny finishes the NOVA integration repository (one full build). (Pavel)

## Dispatch Log

---
*Processed from Teams transcript on October 30, 2026, 12:20 PM Eastern*
*Source meeting: Discussion: downloading games to remote machines via modem*
