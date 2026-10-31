---
type: decision
title: A story created under a Completed feature does not reopen the feature automatically and no new "needs rework" status is added — the person who creates the story moves the feature back to To Do or In Progress, or picks a different parent, because people and AI sometimes set the wrong parent; tasks with no repository may still go to the Core Technology projects, but work should move to the new projects (Oct 28 2026)
date: 2026-10-28
aliases: [no automatic reopen of a completed feature, story under a Completed feature, needs rework status, нуждаются в доработке, lateral link instead of parent, боковой связи, notice to the story creator, wrong parent, Core Technology and BEP projects, draft closed as duplicate]
source-count: 2
status: active
open-commitments: 1
open-questions: 1
---

# A story under a Completed feature does not reopen it automatically; the story's creator moves the feature or picks another parent

Settled at the end of the [[wiki/meetings/2026-10-28-daily-standup-flex-port-firmware-delivery-and-reopening-completed-features.md|Oct-28 Minsk stand-up]] (Russian; Val absent) by [[wiki/people/pavel.md|Pavel Frolov]], on a question from [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].

## The question

Kovalchuk: a developer moved a feature to Completed; then a story was created under it, "как будто это бак". What should happen? His options [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]:

1. move the parent feature back into work automatically;
2. leave it Completed and hang the story on the feature by a side link ("боковой связи"), not as its parent, so it does not depend on the feature's status;
3. add a status after Completed, for example "нуждаются в доработке", which turns to In Progress when the developer takes the work;
4. any other idea.

## The ruling

- **No automatic move.** Pavel: "Я бы наверное автоматически не не переводил". The case can be tracked and a message sent to the story's creator that the parent is closed, asking him to move it [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].
- **No extra status.** Pavel: "Лишний статус как то это? Ну это усложняет зачем?" Kovalchuk answered that statuses are now moved almost entirely by automation, so tracking by status is easier [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].
- **The creator decides.** Pavel: the feature must go from Completed to To Do or In Progress when rework appears and the feature is not closed, and "это должен, тот создает сделать, потому что бывает такое, что неправильно. Аппарат то указывают… Или искусственный интеллект, если создает, может не Того пара то выбрать" ("Аппарат то" / "пара то" = the parent, garbled). A person should look and either move the story to another parent or move the feature to To Do or In Progress. Kovalchuk: "Хорошо." [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]

In one line: **a story under a Completed feature does not reopen it by itself and there is no "needs rework" status; whoever creates the story moves the feature back or picks the right parent.**

## Same session — two smaller Jira points

- **The old projects.** Kovalchuk asked whether tasks may still be created in the Core Technology and "бэп" (heard) projects. Pavel: those take tasks that have no repository; but since things have moved to the new projects, "надо стараться всё переделывать на новые проекты" [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].
- **A draft closed.** Kovalchuk said Pavel had one draft task. Pavel: close it — the work was done in another task. Kovalchuk: he can set the resolution to duplicate [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]].

## How it sits against earlier items

- **Drops the automation of Oct 5 — evolution.** On Oct 5 the team agreed that a story under a Completed feature moves the feature to To Do and its capability from Request Review to To Do, automatically, with Kovalchuk to build it — [[wiki/decisions/2026-10-05-a-capability-moves-itself-to-request-review-when-all-its-features-are-completed-and-a-new-story-sends-feature-and-capability-back-to-to-do.md]]. Pavel now rules the feature move is done by hand by the story's creator. The capability's move was not discussed on Oct 28.
- **Keeps the Oct-1 rule.** A found problem is still a story and the feature still goes back from Completed — [[wiki/decisions/2026-10-01-completed-is-the-developers-last-step-and-a-found-problem-sends-the-feature-from-completed-back-to-to-do-as-a-story.md]]. Only who moves it changes.
- **Wrong parents** were a live problem: on Oct 22 Kovalchuk raised tasks open under closed parents — [[wiki/people/dmitri-kovalchuk.md]] (Oct 22).

## Open commitments

- [ ] [[wiki/people/pavel.md|Pavel Frolov]] — close his draft task as a duplicate — due Oct 28 2026 — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]] [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]

## Open questions

- Will a notice to the story's creator ("the parent is closed") be built, and by whom? Pavel said it "можно отследить и отправить письмо"; no owner was named — [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]

**§15.8:** clear — Jira process only. **§15 #9:** none.

## Sources

- [[raw/Meeting_Transcript_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
- [[raw/Meeting_Notes_Daily_Standup_Flex-Port_Firmware_Delivery_and_Reopening_Completed_Features-October-28-2026.md]]
