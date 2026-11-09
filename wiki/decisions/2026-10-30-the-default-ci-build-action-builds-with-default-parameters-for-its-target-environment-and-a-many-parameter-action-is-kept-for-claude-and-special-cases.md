---
type: decision
title: The default CI build action, run with its default parameters, must build for its target environment — no study of the ~80 parameters; a separate many-parameter action may be kept for Claude and special cases; Chudinov gets a Jira task to revise CI/CD, including the branch-then-main version conflict (Pavel, Oct 30 2026)
date: 2026-10-30
aliases: [default CI build rule, default action with default parameters, экшн по умолчанию с параметрами по умолчанию, без танцев с бубнами, Flex IQ build fails, 80 build parameters, CI version conflict branch then main, CI/CD revision task for Chudinov]
source-count: 6
status: active
open-commitments: 1
open-questions: 2
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

- [x] [[wiki/people/pavel.md|Pavel Frolov]] — create a Jira task for [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] to revise CI/CD: a simple default build, and the branch-then-main version conflict — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]] — *done Nov 2 2026: an AI-PM draft task exists ("это то, что лёша просил… heam freendle"); Pavel moves it to To Do, Chudinov sets the reporter (that this is the task — inference)* — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]

## Open questions

- Which priorities should the CI/CD revision follow (Chudinov: easy, fast — they pull against each other)? Not set — [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]

**§15.8:** clear. **§15 #9:** none.

## Update, Nov 2–3 2026 — the CI/CD task exists as an AI-PM draft; the Flex IQ release action builds the release and the SDK with one button, no SDK-version parameter for now

- **Nov 2.** At the [[wiki/meetings/2026-11-02-daily-standup-flex-port-release-build-and-rust-sound-library.md|Nov-2 stand-up]] Pavel asked Chudinov about a task drafted by the AI PM ("от II draft", heard); Chudinov: "это то, что лёша просил… heam freendle" (a human-friendly build — the notes' reading); Pavel: it is current, he moves it to To Do, and Chudinov adds the right reporter and sees what to correct [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]. Read as the task in the commitment above (**inference**) — marked done.
- **Nov 3.** At the [[wiki/meetings/2026-11-03-daily-standup-sim-traffic-alert-and-flex-iq-release-action.md|Nov-3 stand-up]] Chudinov took the Flex IQ CI/CD task ("вся айсидиев лекса i ko", heard). There is also an SDK release; a one-button action would have to run the SDK release too — check for commits since the last release, build, wait, release. Pavel: or pick a particular SDK release, not the latest; Chudinov: "опять начинаются создания полей… Давайте версию не будем указывать"; Pavel: as it stands "Без Клода невозможно разобраться"; Chudinov: if one button, then build everything "и там и там"; Pavel: "И там и там делаем [релиз] тогда и с д к делаем" [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].
- **The ruling.** Pavel would have liked one parameter — the SDK version: a ready, latest or specific one, or a rebuild; [[wiki/people/alexei-khamin.md|Khamin]]: rolling back to an SDK version is not "прям популярный случай"; Pavel: fine — releases will be made and "всё будет соответствовать версии с д к будет соответствовать версии флекса айкью"; "Может быть в будущем… Добавим функционалу, чтобы иметь возможность специфицировать, какой конкретно с д к брать" [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]. The notes record it as decided by Pavel, Chudinov and Khamin [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].
- **Access.** Chudinov needs developer access so the Flex IQ repository can see the SDK repository and run its action; who grants it is not named [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]].

### Open commitments (Nov 3 2026)

- [ ] [[wiki/people/dmitri-chudinov.md|Dmitri Chudinov]] — build the one-button Flex IQ release action (release plus SDK) and get developer access to the SDK repository — due unspecified — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]

### Open questions (Nov 3 2026)

- Who grants Chudinov developer access so the Flex IQ repository can run the SDK repository's action? — [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]] [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Default_CI_Builds_and_Flex-Port_Merge_Lock-October-30-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Release_Build_and_Rust_Sound_Library-November-2-2026.md]]
- [[raw/Meeting_Transcript_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_SIM_Traffic_Alert_and_Flex_IQ_Release_Action-November-3-2026.md]]
