# Meeting Summary — Code_standard

**Date:** September 14, 2026, 7:37 AM - 7:58 AM Eastern
**Duration:** approximately 21 minutes
**Attendees:** Val Levitan, Pavel Frolov, Andrei Bosik, Irina Shishko, Alexey Khamin
**Language:** Russian (raw transcript is kept in Russian)
**Raw transcript:** [[Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026]]
**Source meeting:** Code_standard — Microsoft Teams

## Summary

A short session built around an email Val had sent minutes earlier, addressed to Pavel Frolov and Evgeniy Alekseev with the others copied. Irina Shishko said she had not received it. The email set out code standards; the meeting was Val checking that the team already works this way, and deciding how to bring Alekseev onto the same footing.

**The person problem.** Val was direct about Alekseev: a very capable engineer, worth keeping, but working in an old format. He keeps the whole code on his local machine and then puts it in in very large portions — huge numbers of lines at once. Val described his own way of working as the contrast: write part of the code, let GitHub hold the versions, check how it integrates, commit two to four times a day in small pieces, run the integration tests each time to see whether anything broke, so that the reviewer gets a sane chunk of work to look at instead of a week's worth. That way everything moves forward in step.

Val's reading of the cause was that nobody explained the reasons — Alekseev was told to do it a certain way with no explanation, so he improvises what is convenient for him. Val's view of the man was consistently positive: not difficult, a big professional, and likely to agree if the reasoning is explained properly rather than delivered as an order.

**The instruction.** Andrei Bosik is to book a meeting with Alekseev and walk him through the standards and practices, explaining why JVL depends on them and what the sequence should be. Bosik said he had already written to Alekseev about scheduling time to set up his environment and run a short training session, and was waiting for a reply. Val added the practical window: Alekseev can take a meeting at 07:00; by 08:00 he leaves for his own job. Val asked for it to be set for tomorrow morning. If Bosik judges that this will not work with the man, then he is not a fit and JVL has to do something else — but Val was explicit that he wants to save the situation, not break it.

**Paragraph two of the standard — main must always build.** Val read out the sentence: the main branch must always contain correct working code, and anyone at any time must be able to pull it and build a working installer. His reading: if code is in main, everyone assumes it is not broken. Any person on the team — QA, or a new developer being brought in — can take main and install it on a device using the release notes that exist today. If Alexey Khamin takes that code and simply cannot install it on a machine, then either the code does not work, or the release notes are wrong, or the prose is wrong — something somewhere is wrong, and the priority is to make it work.

Pavel Frolov accepted this "in general" and pushed on one case: a development branch held off main that becomes the mainstream for a while. He gave his own live example — he branched off the FlexPort platform project to add the SAS/AFT work. Val's answer was that the rule bites at the merge point: once it is pulled into main, Khamin may take that piece from main and it has to work. Khamin confirmed it is possible to build from a branch and check it. Pavel said his branch stays under his own checking until they are ready for main to build both variants, the old one without SAS and the new one with it. Val agreed in principle that a branch can carry its own narrower promise — you can say only this and this must work in the branch.

**Where Val turned the branch argument into a capability.** Pavel described roughly thirty capabilities for the Flex release due October 1 — fewer for the port, around ten — all in one branch because they are interrelated and to avoid mixing with what was in main. Val challenged the need for that: if the work is a set of pieces that switch on and off optionally, what is probably missing is a capability that holds the filter — a selection in main that decides what is switched on. He accepted Pavel's example as a good one and turned it back on himself: since Val wrote yesterday that FlexPort must also work on machines without SAS, and that breaks what Pavel had already built, then Val had under-specified — he should have said there must be a selection screen. That is a capability, not a reason for a long-lived branch. Pavel agreed in substance and restated it his own way: FlexPort must have a way to set its operating mode, either at build time or by a parameter on an assembled device.

**Pull requests.** Bosik's one caveat on the email was that it is not always someone else who merges a pull request — sometimes you have to merge your own. Val agreed: someone else always should, but exceptions are found often, and it is preferable rather than absolute.

**Paragraph two, last sentence — the code belongs to the project.** Val read it as: the code belongs to the project, not to any one developer. If a tester or QA installs something and it does not work, then especially today with Claude Code they can propose the fix, make the fix, and raise a pull request. The reviewer on that pull request looks at it, agrees it is right, and merges it. Val named these two points — small frequent commits, and code belonging to the project — as exactly what Alekseev skips, and tied it back to the same cause: he holds everything himself because there is no prose, no description and no release notes, so he has to be across everything by hand.

**Yavorsky.** Bosik asked whether Yavorsky's account can be switched off, since nobody tells them. Val said not yet, for diplomatic reasons, but JVL gives him no work. He called him a very intelligent man whose thinking Val could not keep up with.

**Close.** Val told an old joke of his father's about the soldier sent to tell a widow her husband had been killed and opening with "does the widow Ivanova live here" — his way of asking Bosik to handle the Alekseev conversation carefully. Bosik said he knows the joke and that he always prefers saying things directly rather than going around.

## Decisions Made

- **The main branch must always contain working, buildable code.** Anyone must be able to pull it and build a working installer using the current release notes. Confirmed as already in force. (Val Levitan; agreed "in general" by Pavel Frolov and Andrei Bosik)
- **If main cannot be installed, that is a defect somewhere** — code, release notes or prose — and fixing it takes priority. (Val Levitan)
- **A development branch may carry its own narrower promise**, but the full rule applies the moment it is merged into main. (Val Levitan, accepted by Pavel Frolov)
- **Someone other than the author should merge a pull request** — a preference, not an absolute; self-merge is an accepted exception. (Andrei Bosik raised, Val Levitan accepted)
- **Small, frequent commits with integration tests** rather than large batches, so review happens on a sane chunk of work. (Val Levitan)
- **The code belongs to the project, not to a developer.** Anyone who finds a fault may propose and make the fix as a pull request; the reviewer decides. (Val Levitan)
- **The FlexPort SAS / no-SAS split is a missing capability, not a reason for a long-lived branch.** Val accepted the specification gap was his own. (Val Levitan; Pavel Frolov restated it as a build-time or device-parameter mode setting)
- **Alekseev is to be coached, not ordered.** If he will not adopt the standards, JVL looks for another developer — but saving the situation is the preferred outcome. (Val Levitan)
- **Yavorsky's account stays open for now**, with no work given to him. (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Book a meeting with Evgeniy Alekseev for tomorrow morning (he is free around 07:00, leaves for his own job by 08:00) and take him through JVL's code standards and practices, explaining the reasons rather than issuing orders | September 15, 2026 | High | Bosik had already written to him about setting up the environment and running a short training session, and is waiting for a reply |
| 2 | Andrei Bosik | Tell Val if he judges that Alekseev will not move to the new way of working | After the meeting above | Normal | Val's stated fallback is looking for another developer |
| 3 | Pavel Frolov | Treat the FlexPort operating mode (SAS / no SAS) as a capability with a selection, at build time or by a device parameter, instead of keeping it as a separate long-lived branch | Not set | Medium | Agreed in substance; no date or JIRA item named in the meeting |

## Open Questions

- **How the main-branch rule applies to a long-lived development branch that becomes the mainstream for a period.** Val accepted the principle that a branch can promise less, but no written rule came out of the discussion.
- **Whether FlexPort's mode is set at build time or by a parameter on an assembled device.** Pavel raised both; nothing was chosen.
- **Who merges when there is no second person available.** Named as a frequent exception, not resolved.
- **Irina Shishko did not receive the standards email.** Noted in the call and not followed up.
- **Yavorsky.** Account left open, no work assigned, no decision on ending the arrangement.

## Notes on the transcript

The meeting was held in Russian and the Teams transcription garbles most English technical terms. Readings that are near-certain from context: "мейн" / "мэйн" / "мень" / "мей" / "men" = main (branch); "менbran" / "menbrange mast always contank crind working cor" = "the main branch must always contain correct working code"; "пулреквест" / "полреквест" / "пурек" / "пол реквест" = pull request; "камит" / "камид" / "камин" = commit; "бранч" / "брайч" / "браче" = branch; "таги" = tags; "флекспорт" / "флегспорт" / "флекс порт" = FlexPort; "сас" / "с. А. С." / "sass" = SAS; "кейпобилети" / "копбилити" / "побилась" = capabilities; "клад коуд" = Claude Code; "релиз ноут" / "лист ноутз" = release notes; "киуэй" / "qвей" = QA; "Алексеев" = Evgeniy Alekseev; "яворский" = Yavorsky; "босик" = Andrei Bosik; "хамин" = Alexey Khamin.

Worth confirming with Val before being treated as fact: the exact subject of the email he sent (the transcription of the subject line is not recoverable), and the exact count of capabilities Pavel quoted for the October 1 Flex release — he said around 30 across all systems, corrected by Bosik to fewer for the port, and Pavel then offered "well, 10" without checking. The raw transcript is preserved unchanged, in Russian.

## Dispatch Log

*(empty — captured by the scheduled meeting-watcher sweep, no dispatch)*

---
*Processed from Teams transcript on September 14, 2026, 10:05 AM Eastern*
*Source meeting: Code_standard*
