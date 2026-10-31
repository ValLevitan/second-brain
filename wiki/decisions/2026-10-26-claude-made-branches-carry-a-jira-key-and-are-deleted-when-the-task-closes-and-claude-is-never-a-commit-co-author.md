---
type: decision
title: Claude branch and commit hygiene — every branch Claude creates is tied to a Jira issue (no "fix/…" or "claude/…" names), a branch is deleted when its Jira task closes, and Claude must not add itself as a commit co-author; keep the company standards in the session or Claude's memory so it follows them (Andrey Bosik's request at the stand-up, Oct 26 2026)
date: 2026-10-26
aliases: [Claude branch hygiene, Claude co-author in commits, delete branches when the Jira task closes, Jira-linked branch names, claude/ branches, fix/ branches, 160 branches, Claude as co-author]
source-count: 2
status: active
open-commitments: 2
open-questions: 0
---

# Claude-made branches carry a Jira key, are deleted when the task closes, and Claude is never a commit co-author

Raised by [[wiki/people/andrey-bosik.md|Andrey Bosik]] (DevOps) at the [[wiki/meetings/2026-10-26-daily-standup-claude-branch-hygiene-and-autotest-environment.md|Oct 26 2026 Minsk stand-up]] (Russian; Val absent), as a request to all developers; [[wiki/people/pavel.md|Pavel Frolov]], who ran the stand-up, added how to make Claude keep to it, and nobody objected [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]. The notes log it as an undertaking for all developers [[raw/Meeting_Notes_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]. That it stands as a team rule is an **inference** from the lack of objection; Val was not there.

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## The three points

1. **Delete branches.** Bosik: some people work with Claude "очень немножко, бездумно" — for example "у лёша под 160 веток" (Lyosha = [[wiki/people/alexei-khamin.md|Alexei Khamin]]); branches must be watched so they get deleted. Khamin: he meant to clean them up that day. Bosik: it is not only him; tell Claude to keep the standards — "если задача в жире закрыта, то ветку соответственно нужно удалять." [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]
2. **Branches tied to Jira.** If Claude creates branches, they must really be associated with Jira tasks, "потому что очень много веток с названием. Фикс слэш и какойто текст клод слэш какойто текст" [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]].
3. **No Claude co-author.** Claude "периодически себя дописывает как соавтором в камита" — this must not be allowed: it breaks reports, "потому что у нас появляется неизвестный пользователь под названием клод… или он себя может написать там френдли клод" [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]].

## How to make Claude keep to it

- **Pavel's experience.** When Claude starts creating branches on its own it uses its own scheme ("фикс или там фит слэш"); he had to tell it to add the prefix of the real Jira issue; it works for a while, then sometimes slips back [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]].
- **[[wiki/people/sergey-tsymanov.md|Tsymanov]]:** the standard is written down somewhere — his Claude found it and said so [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]].
- **Pavel's fix.** If the context holds a link saying "use the company standards" — in the session, or in a memory file or "клодом ди" (read as CLAUDE.md — **inference**) — Claude keeps to it all the time "и не будет таких проблем." Bosik: "Да." [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]] This repeats Val's standing instruction — [[wiki/decisions/2026-09-04-point-claude-at-the-standards-repository-first.md]].

## How it sits against earlier items

- On Oct 2 Pavel called it "такая война" with Claude opening and naming branches on its own instead of looking in Jira — [[wiki/topics/ai-assisted-development.md]] (Oct 2 2026). Oct 26 turns that complaint into three concrete rules (**inference**).
- Branch naming with the Jira key also follows the earlier branch rules — [[wiki/decisions/2026-09-14-flex-port-sas-mode-is-a-selection-capability-not-a-long-lived-branch.md]] (no long-lived side branches). The link is an **inference**; the stand-up did not cite it.

## Open commitments

- [ ] [[wiki/people/alexei-khamin.md|Alexei Khamin]] — delete his old branches (about 160, heard) — due Oct 26 2026 — [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]
- [ ] All developers — keep Claude to the branch and commit standards (Jira-linked branch names, delete closed branches, no Claude co-author) — due ongoing — [[raw/Meeting_Notes_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Claude_Branch_Hygiene_and_Autotest_Environment-October-26-2026.md]]
