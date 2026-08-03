# Meeting Summary — hardware_repo (Segment 2 of 2)
**Date:** July 29, 2026, 9:05 AM to 9:28 AM Eastern
**Duration:** about 22 minutes
**Segment:** Segment 2 of 2
**Attendees:** Val Levitan, Genadi Peari, Andrei Bosik, Pavel Frolov
**Raw transcript:** [[Meeting_Transcript_Hardware_Repo_SolidWorks_GitHub_Large_Files-Part_2-July-29-2026]]

## Summary

Val called the meeting to let the team ask questions about the hardware repo email he had sent, rather than trade messages back and forth. He said he wants to stay at the center of the conversation because a new standard will grow out of it, and he is adding new standards to GitHub as they settle.

**Why the repo matters to billing.** Val explained the chain he is building. Subcontractor approvals are tied to making the contractor deposit the artifact into the repository where they do their work. At month end the subcontractor submits an invoice naming a Feature, its description, and Done. Done means the contractor marked the Feature complete after adding the code or the artifact. Claude then sees that the artifact changed, sees that the prose description changed with it, compares the prose against the Feature description, and does a sanity check that the Feature really is finished. Val called the cycle simple and said it should work almost flawlessly. With Nathan Carver it is about 75 percent organized and reconciliation works well; Nathan has no prose yet but could add it easily. RK3568 is at some level, lower than Nathan. Other repositories do not work this way yet, and Genadi's repository is not set up at all. That is why the meeting was called.

**What Genadi's files actually are.** Genadi described three kinds of SolidWorks development files: parts, assemblies and drawings, arranged in a SolidWorks hierarchy. SolidWorks has its own PDM system that follows changes. Today all of this happens locally on his computer. When development finishes he takes the whole project and deposits it; last time he put it on SharePoint. He can put it on git, but he said that is not good practice. His reading is that GitHub is not really designed for this work, and that the recommended pattern is an intermediate repository for large files where the exchange happens, with GitHub used afterward.

**Large-file limits.** Genadi said an average project is about 10 GB. Val thought Git LFS allowed 100 GB. Andrei corrected him: LFS is a way to hold binary rather than text files, and it has two limits, one on individual file size (around a gigabyte) and one on total volume (around 40 or 50 GB). A 10 GB project could go into one repository, but the question is the size of each individual file inside it. Genadi said the individual files are smaller than that ceiling. Andrei added two warnings: LFS stores a pointer to a binary, so a new version of a file replaces the previous version rather than diffing against it, and pulling or pushing 10 GB every time will not be fast. Genadi said he read the best practices just before the meeting, there are several options, and it needs a calm review. Whatever is chosen has to work with the cloud, because moving files by hand every time is impossible. He noted that when there was a server, backups happened automatically and there were no problems; there is no server now.

**Tooling and licensing.** Val said that once it is set up correctly it works, and that JVL needs to buy a licensed version of SolidWorks, configure it properly, and configure Genadi's computer so he can work remotely from any location, plus whatever else he needs so his working conditions are normal (the specific item Val named there is garbled in the transcript).

**Downstream documents.** Genadi raised the simpler topics: after development ends there are manufacturing documents needed for purchasing and for suppliers, in other formats including STEP files, and then documentation released to other people for assembly. Val said the manufacturing documents belong in Microsoft Dynamics Business Central, and that all documentation must be in GitHub. Genadi pointed out that the people who need it, Elizabeth among them, would then need GitHub access. Val said an environment could be provisioned elsewhere, for example on Azure, and that this part is simpler and depends on what is practical. He added that Claude gets woven into all of it because it is convenient to work with.

**Who deposits the artifact.** Genadi described what happens today: Alekseev works in a free online PCB tool directly on that vendor's server, and Genadi manually exports the finished project and moves it into GitHub after completion. Val objected on principle. He does not understand why Genadi should do this and not Alekseev as part of his deliverables, and he framed it as culture: if you ask to be paid, part of your obligation is to convey what you did and package it the way the payer needs it, because the work was a service performed for them. He did not want the culture point waved away, calling it the center of the matter. Genadi answered that he has been through this before and he needs to check what Alekseev did. Val's response was that the check belongs in the pull request: the contractor prepares the whole package, opens the pull request, and Genadi reviews it there and agrees to the merge.

**Whether a PCB export can be reviewed at all.** Andrei asked whether Genadi needs to open Alekseev's file before or after export. Pavel explained that the file cannot simply be opened: it can only be viewed inside the online tool, or the export can be uploaded back into the same online service under your own account and opened there. No third-party tool will open it. Genadi said the export involves producing the bill of materials correctly, adding certain items, and the Gerber file, delivered as a folder containing that set of files. Pavel observed that a pull request here is therefore not quite like a software pull request, and that Genadi could ask an AI to check whether the bill of materials was generated and what components it contains.

**Industry context.** Val described an interview he did with a hardware layout engineer, about 42 years old, who subcontracts for SpaceX and also does development for Dell, and lives in Austin near both. That engineer told him almost nothing is done by hand now: layout and documentation are done through AI. Val could not remember the tool's name; Genadi and Pavel both supplied Altium. Pavel's read is that Alekseev uses the online tool because it is free to him, and Altium is a paid license. Val believes Altium sells a full development license and a cheaper intermediate viewer. Genadi said cost is not the only reason: the online service automatically produces a bill of materials using the cheapest components on the market, whereas with Altium you have to source parts manually. Val thought Altium has supplier linkage too, but said he does not have first-hand data and may be wrong, and that this can be worked out with a little research and Claude.

## Decisions Made

- **Genadi Peari and Andrei Bosik own the hardware repo question, working together directly.** Val said this can proceed without him and without Pavel. What he needs back is the policy the two of them agree on: Andrei understands what JVL does and how Val wants it to work, and Genadi knows what he does and how it must work for him. (Decided by Val Levitan)
- **Pavel Frolov joins on the PCB design tooling side.** Pavel asked who covers the tools used for PCB design as distinct from SolidWorks; Val told him to plug in there, because Pavel has more knowledge of how JVL works. (Decided by Val Levitan)
- **JVL will buy a licensed version of SolidWorks** and configure it, plus Genadi's computer, so he can work remotely from anywhere. (Decided by Val Levitan)
- **Manufacturing documents go into Microsoft Dynamics Business Central; documentation goes into GitHub.** (Decided by Val Levitan)
- **Next meeting Friday at 10:00**, after Genadi and Andrei have done the reading. Val offered Monday instead; Genadi noted the long weekend, and Pavel, Andrei and Genadi all confirmed Friday. (Agreed by all)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Genadi Peari | Read the SolidWorks and GitHub best practices and work out with Andrei how the system should be built, including the large-file approach | July 31, 2026 | High | Val estimated two to four hours of research; Genadi has Wednesday and Thursday |
| 2 | Andrei Bosik | Work through the SolidWorks and GitHub best practices hand in hand with Genadi and bring back an agreed policy | July 31, 2026 | High | Val: read the best practices "hand in hand with Andrei"; Andrei's one spoken "Согласен" came during the Friday scheduling exchange, so his explicit sign-off on the research task itself is not on the record |
| 3 | Genadi Peari | Send Andrei the SharePoint link to where the hardware files are currently stored | July 29, 2026 | High | Andrei asked for it so he can point Claude at it |
| 4 | Andrei Bosik | Run a surface analysis of the SharePoint hardware files using Claude | July 31, 2026 | Normal | Depends on undertaking 3 |
| 5 | Pavel Frolov | Cover the PCB design tooling side of the same question | July 31, 2026 | Normal | Raised by Pavel, assigned by Val |
| 6 | Val Levitan | Schedule the follow-up meeting for Friday at 10:00 | July 29, 2026 | Normal | Val said he was scheduling it in the meeting |

## Open Questions

- Which large-file approach JVL adopts: Git LFS directly, or an intermediate repository for large files with GitHub used afterward. Genadi read that there are several options and wants a calm review. Raised by Genadi Peari.
- Whether individual SolidWorks files stay under the LFS per-file ceiling of roughly one gigabyte, and whether the roughly 40 to 50 GB total volume limit is workable given 10 GB projects. Raised by Andrei Bosik.
- How the people who need manufacturing documentation, Elizabeth among them, get access, and whether a separate environment such as Azure is provisioned for them. Raised by Genadi Peari.
- Whether Altium has the same supplier and cheapest-component linkage as the free online tool Alekseev uses. Val said he does not have first-hand data. Raised by Val Levitan and Genadi Peari.
- Whether a PCB export can be reviewed at all without uploading it back into the vendor's online service, and what that means for reviewing a hardware pull request. Raised by Andrei Bosik and Pavel Frolov.
- **Whether the contractor deposits his own artifact, or Genadi continues exporting and depositing it.** Val argued in the meeting that it is the contractor's own obligation and that acceptance belongs in the pull request, framing it as a matter of culture. Genadi pushed back that he has to check the work first, and Pavel established that a PCB export cannot be opened outside the vendor's tool at all. The point was left unresolved in the meeting, and **after the meeting Val held off on the demand** pending a full assessment of how this actually works and what a workable hardware review looks like. Not a decision; an open question. Raised by Val Levitan.

## Dispatch Log

---
*Processed from Teams transcript on July 29, 2026, 9:45 AM Eastern*
*Source meeting: hardware_repo*
