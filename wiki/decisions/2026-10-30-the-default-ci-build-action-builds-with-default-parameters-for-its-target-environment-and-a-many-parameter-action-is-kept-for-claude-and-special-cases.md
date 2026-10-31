---
type: decision
title: The default CI build action, run with its default parameters, must build for its target environment — no study of the ~80 parameters; a separate many-parameter action may be kept for Claude and special cases; Chudinov gets a Jira task to revise CI/CD, including the branch-then-main version conflict (Pavel, Oct 30 2026)
date: 2026-10-30
aliases: [default CI build rule, default action with default parameters, экшн по умолчанию с параметрами по умолчанию, без танцев с бубнами, Flex IQ build fails, 80 build parameters, CI version conflict branch then main, CI/CD revision task for Chudinov]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# The default CI build action builds with default parameters; a many-parameter action stays for Claude

Set by [[wiki/people/pavel.md|Pavel Frolov]] at the [[wiki/meetings/2026-10-30-daily-standup-default-ci-builds-and-flex-port-merge-lock.md|Oct 30 2026 Minsk stand-up]] (4:45 AM Eastern, Russian); [[wiki/people/alexei-khamin.md|Alexei Khamin]] raised it and agreed [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].

*(Quotes come from an unpunctuated Russian speech-to-text transcript, kept word for word.)*

## What happened

- **The Flex IQ build failed again.** Khamin tried to build Flex IQ the day before and it fell over; Sergey had said he and "Дима" would fix it, "но походу ничего не пришали"; there are so many parameters that the build "начинает просто задыхаться и падать" [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **The cause, per Tsymanov.** He added no new parameters. Nobody had built for dev before; he did once while testing, and a parameter that reuses a build already made from main picked the last build, made for dev — a conflict. The fix is to choose the parameter for the branch [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Khamin's point.** That is exactly the problem: there are about 80 parameters, "и в них я не должен разбираться, чтобы мне просто получить бил"; if the others are away and it fails, he would have to send Claude in to build [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Chudinov's view** (label "Dzmitry Chudzinau"). Two options: leave it, or make one for a human. The parameters were set up for a reason; he almost never starts a build by hand — he tells Claude Code to run it, and it asks what to switch. Caches make builds fast but can conflict if one does not know which parameter to switch [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].

## The ruling (Pavel)

- "я всётаки я поддержу лёшу": a person opening a build should not have to puzzle over it. General rule: "экшн по умолчанию с параметрами по умолчанию должен собираться в… инваймент, под который делается сборка." Other parameters may be changed at will, but the defaults must be the ones that build. A separate action with a long parameter list may be kept "для Клода для какихто особых кейсов"; the main action must be simple and run "без танцев с бубнами" [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]. The notes record it as decided, with Khamin agreeing [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **A second bug.** Khamin: after a build from a branch, the next build from main takes the version of main's last build and hits a conflict, because that version already exists from the branch [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]].
- **Through a task, not chat.** Chudinov: "заведите на какую нибудь задачу" — requests reach him from every side in chats, and he has his own work; CI/CD is a feature too; he asked for clear priorities. Pavel (joking): "Легко, быстро и с красивыми лампочками выберите 2 из трёх." Pavel: a task is to be created on Chudinov to revise it [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]. "Дима" here is Chudinov — he is the one who answers.

## How it sits with earlier rulings

- It fits Val's Oct-20 wish that a release build be documented so a non-developer (or Claude) can make it — [[wiki/decisions/2026-10-20-flex-port-mvp1-needs-only-an-easy-release-build-and-the-usb-update-and-alekseev-writes-stm32-freertos-rules-for-claude-review.md]] (**inference**: the link is not said in the meeting).
- Background on the build pipeline and its parameters: [[wiki/topics/build-pipeline-parameterization.md]]; the main-branch rule: [[wiki/decisions/2026-09-14-main-branch-must-always-build-and-the-code-belongs-to-the-project.md]].

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — create a Jira task for [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] to revise CI/CD: a simple default build, and the branch-then-main version conflict — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]

## Open questions

- Which priorities should the CI/CD revision follow (Chudinov: easy, fast — they pull against each other)? Not set — [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
