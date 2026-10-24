---
type: decision
title: Hardware repositories start with three — harness, display and sheet metal — from Nathan's folder list; each repository is one project with free-form content plus readme, Prose and data contracts, and the agent generates the data contracts from the data sheets and drawings Genadi has vetted
date: 2026-10-19
aliases: [first three hardware repos, harness display sheet metal, repository equals project, one repository per project, free-form repository, readme Prose data contracts, data contracts are generated not hand-written, a release is a bill of material, only vetted items go in, 13 repositories, about 15 repositories, hardware manufacturing repo name, Andrei opens repos Dima opens projects]
source-count: 3
status: active
open-commitments: 4
open-questions: 1
---

# Hardware repositories start with harness, display and sheet metal; the agent generates the data contracts (Oct 19 2026)

Agreed by [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/genadi-peari.md|Genadi Peari]] and [[wiki/people/nathan-carver.md|Nathan Carver]] in segment 1 of the [[wiki/meetings/2026-10-19-github-msbc-repositories-per-project-mery-purchasing-endpoints-and-ai-coo.md|Oct 19 2026 "GitHub-MSBC" meeting]] (5:02–5:36 PM, English). It puts the [[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md|Oct-5 repo model]] into practice. Quotations are from the transcript [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] unless marked.

## How it came up

- **Why now.** Val: "we have about 45 days left in this year"; "Michael will be leaving", and "Mary cannot work off of the same format" as Michael's own framework and reports; "I don't have time to bring somebody else on board", and "I cannot allow Genadi spend time on purchasing." He believes the architecture he presented "should work for Mery." Nathan: "Yes, I agree." See [[wiki/decisions/2026-10-08-mary-takes-over-mikhail-perelmans-ordering-role-with-training-from-october-19.md]].
- **Genadi's question.** Before he loads his product and component data into GitHub, he wanted the repository structure confirmed: "how do we do tags… organize the read me files", and "How you access each component? Through what? Through the part number, where it's stored, how it's stored." He referred to a "hard repository standard"; Val: "We don't have hardware repository standard. We have repository standard."

## What was agreed

- **A repository is a project.** Val: "Each repository is… Equal to a Project." "Monitors is a project of its own in Jira, repository of its own in Github." Genadi checked: all the harnesses for all products in one repository, all the metal in one? Val: "Yes."
- **Free-form content.** Val: "The structure of Github repository… is not structured, it's freestyled. You put as much information into that repository as possible" — data sheets and drawings from suppliers, or drawings Genadi made when a supplier had none. "Just like code… There is no structure to it." He does not see tables inside a repository.
- **What every repository has.** "each repository will have a readme file. It will have… a folder for Prose. It will have a folder for… Data contract." Nathan: "Yes." Prose and data contracts are how the AI knows what is needed; "Github Action… Collects all of it into a release. So, a release to me is a bill of material."
- **Nathan's spike is the starting list.** Nathan showed, on a branch not yet merged, folders that stand in for future repositories; Val read out "sheet metal, power supply, plastics, peripheral, money devices… Labels, harnesses, display" and said "this is exactly what my table is." Each folder holds "a collection of YAML files" that define the component. There is no Prose folder and no ADR yet; Nathan: "that can be added in as we go." Each repository will also need a folder for the data sheets and other source files that the agent reads. Val: "good enough to start with"; repositories can later be deleted, added, moved, renamed or combined.
- **Data contracts are generated, not hand-written.** Val: "we do not physically by hand write data contract?" Nathan: "Correct, we generate." Val: "data contract is taken from data sheets and drawings… That's why we need the files." Nathan: each repository can carry "its own unique instructions for its own problems", and the agent builds the contract files from them.
- **Mistakes are caught at assembly.** Val: "I assume there will be mistakes. I intend to catch these mistakes during the final assembly… If data contracts don't match, it cannot assemble." The fix is made at the source; with a correct source JVL "could seek a new vendor… assemble new bill of material… check pricing."
- **Only vetted items go in.** Val: what Genadi puts into GitHub is "approved items… JVL is going with this" — "Displays with displays, harnesses with harnesses. Money devices with money devices. Plastics with Plastics" — everything he would need "To put the machine together by hand."
- **Three repositories first.** Genadi asked for one repository as a working example; Val: "do 2 repositories… or three… a harness. A few displays and maybe some sheet metal, something that was assembled together." Genadi: "Yeah, sure." Nathan: "Three repositories, okay."
- **Who opens them.** Genadi asked who opens the repositories; Val: "Andrei" ([[wiki/people/andrey-bosik.md|Andrey Bosik]], by context — **inference**). Val: "Dima at the same time opens projects. You have to have projects in order to have a repository," and later "ask Dmitri Kovalchuk… To create 3 projects" ([[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]]). Nathan will make the request; Genadi signed off on the names: "whatever you have, it's good here."

The derived notes record the same four decisions [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]].

## How it sits against earlier sources

**Evolution, not contradiction.** Oct 5 set the model; Oct 8 named a 13-repo table and said the data contracts lie "полностью на вас" (Genadi), while noting the AI mostly builds them from datasheets; Oct 9 showed Nathan's folders as future repositories ([[wiki/decisions/2026-10-05-hardware-follows-the-developer-repo-model-one-jira-project-one-repo-zero-trust-data-contracts-no-monorepo.md]]). Oct 19 turns the folders into the starting repo list, names the first three, and makes the agent the writer of the contracts, with Genadi supplying the vetted files. The data-contract-not-CAD rule of [[wiki/decisions/2026-10-13-the-agent-builds-the-bom-as-a-control-gate-taught-by-data-contracts-not-cad-and-genadi-finds-why-it-is-wrong.md]] stands.

## Open commitments

- [ ] [[wiki/people/nathan-carver.md|Nathan Carver]] — request the three repositories (harness, display, sheet metal) — due Oct 20 2026 (notes) — [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [ ] Nathan Carver — ask Dmitri Kovalchuk to create the three matching Jira projects — due Oct 20 2026 (notes) — [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [ ] [[wiki/people/genadi-peari.md|Genadi Peari]] — load his vetted data sheets and drawings into the three repositories — due after the repositories exist — [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
- [ ] Genadi Peari, Nathan Carver — find Val's earlier repository table (email or Teams) and compare it with the folder list — due unspecified — [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]

## Open questions

- How many repositories, and with what names? Val: "Thirteen"; Genadi: "about 15". Genadi: "I don't understand hardware manufacturing" — sheet metal, plastics and harnesses already cover it, "so basically nothing left in there"; Val: "it's possible that the names are also incorrect." Genadi also thinks Val's earlier table "was better". — [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]

**§15.8:** clear. **§15 #9:** clear.

## Sources

- [[raw/Meeting_Transcript_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Repositories_per_Project_and_Data_Contracts-October-19-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
