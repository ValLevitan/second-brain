---
type: decision
title: Mary gets answers from Business Central by asking through MCP in Spanish or English, not from special reports; Nathan adds MSBC endpoints for end-to-end inventory control, driven by AI COO use cases that Val writes (use cases → capabilities → endpoints)
date: 2026-10-19
aliases: [no special reports for Mery, Mery asks through MCP, multi-contextual protocol, Spanish or English questions, more MSBC endpoints, end-to-end points, AI COO use cases, use cases to capabilities to endpoints, AI COO scans Business Central and emails, purchase invoices not handled correctly, prepayment does not register, vendor shipping notice, 40 days lead time, agent writes its own MD notes, no custom MSBC reports, Lev for invoicing]
source-count: 4
status: active
open-commitments: 2
open-questions: 1
---

# Mary asks Business Central through MCP; Nathan adds endpoints from AI COO use cases (Oct 19 2026)

Set by [[wiki/people/val-levitan.md|Val Levitan]] in segment 2 of the [[wiki/meetings/2026-10-19-github-msbc-repositories-per-project-mery-purchasing-endpoints-and-ai-coo.md|Oct 19 2026 "GitHub-MSBC" meeting]] (5:36–5:50 PM, English); [[wiki/people/nathan-carver.md|Nathan Carver]] agreed and [[wiki/people/genadi-peari.md|Genadi Peari]] added to it. Quotations are from the transcript [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]] unless marked.

## Why

Val: [[wiki/people/mary.md|Mary]] ("Mery") is "not an engineer. Michael is an engineer", so she needs "an administration environment". "We have a tool. The tool is… Business Central. But we don't have the environment created within this tool that allows Mery for easy use or easy access." The hand-over is on [[wiki/decisions/2026-10-08-mary-takes-over-mikhail-perelmans-ordering-role-with-training-from-october-19.md]].

## What was decided

- **No special reports; questions through MCP.** Val: "We need to move away from building specialized reports. It has to be done through a multi-contextual protocol… she has to be able to write in Spanish or English and get an answer."
- **More MSBC endpoints.** Val to Nathan: "you need to advance your Msbc when it comes to inventory control to cover all end to end" with more "API points… Right now I believe it's limited." Nathan: "No, I think that's right." Later: "It's not a tool. Nathan needs to add more endpoints."
- **The flow of work.** Val: "I will ask Claude… create a set of use cases for AI hyphen CO, AI based Chief Operating Officer, as a controlling character… In tracking. All of the actions associated with. Material management." "From use cases, we create more capabilities, pass it on to Nathan. And Nathan will add additional endpoints into the Msbc." Nathan: "Yes. Sounds good to me." Val will start with "maybe 10 use cases, maximum", not polished; Nathan and Genadi review them.

The derived notes list the same two decisions [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]].

## The gaps behind it

- **Count versus invoices.** Genadi: the material requirements report data is there — "We have issues that not exact count on the Msbc, but we have all the data." Val: "No, no, no, we don't have all the data. The count is more or less okay now… What we don't have, we don't treat… Purchase invoices correctly."
- **Prepayments.** A vendor asks for a prepayment on a purchase order; "right now our process, it doesn't register against the invoices."
- **Shipping notices.** "The vendor says, I'm ready. I'm shipping. Right now all of this is verbal. Verbal emails between Michael and the vendor… Our system needs to know that vendor has shipped." Val's example of lead time: "on the boat for, let's say, 25 days and then by truck another 15 days. Here's 40 days lead time."
- **Every step confirmed.** Genadi: "All the steps needs to be confirmed: PTO, PO approval, PO deposit, invoicing, payment, shipping, lead time" ("PTO" as heard, not explained).
- **The payment flow.** Val: "I don't know exactly the flow of it. So I need to meet with Lev and get him to explain to me the flow of payment and administering purchase invoices" — see [[wiki/decisions/2026-10-16-val-and-lev-focus-together-on-inventory-control-so-mary-can-run-ordering-alone.md]] (Oct-19 update).

## The AI COO, as Val described it

An agent that "scans through Business Central" and says "hey, we didn't make a payment, or hey, we didn't get a advice from the supplier that he shipped, and he should have." Genadi added that for questionable points it should "search the emails and put information from the e-mail to responses of the vendor for this particular line", as Mikhail wanted his notes kept ("these notes basically needed to be taken from the emails"). Val: "Of course"; the agent traverses emails and MSBC, "because that's… the your source of truth." Genadi warned "we don't have much time because she needs to start working very fast." More on the AI COO idea: [[wiki/topics/ai-assisted-development.md]] (Oct 19).

## How it sits against earlier sources

**Evolution.** On Oct 13 Val ruled that procurement reports come only from MSBC, built by Lev's consultant, with Nathan linking the endpoints into MCP ([[wiki/decisions/2026-10-13-procurement-reports-come-only-from-msbc-and-the-excel-export-report-goes-away.md]]). Oct 19 keeps MSBC as the source and MCP as the way in, but now says to move away from specialized reports, and the endpoint list comes from Val's AI COO use cases. The consultant is not mentioned on Oct 19; whether the consultant's report work still stands is not said.

## Oct 20 2026 update — the draft is reviewed; the agent keeps its own notes, so no custom MSBC reports

At the [[wiki/meetings/2026-10-20-github-msbc-repo-tags-and-light-and-wonder-bracket.md|Oct 20 2:15 PM meeting]] (Russian; Val and Genadi) [[raw/Meeting_Transcript_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]]:

- **The draft.** Genadi: "мы с нейтаном посмотрели ваш драфт"; "я не закончил. Честно говоря, я не успел", and Nathan "сейчас пошёл изучать". They went through the capabilities "брифли очень". Val: "юз кейсы более не менее понятно, правильно?" Genadi: "Абсолютно."
- **The agent's notes.** On an idea to store data so the agent does not regenerate a report each time, Val: the agent "пишет MD fill… накапливает… файл, который потом читает… для себя записки пишет". Genadi: "мы же не хотим, чтобы он генерил этот репорт… каждый раз."
- **No custom MSBC reports.** Val: with this logic and the agents "нам не нужно, чтобы сделать кастом репорта"; Genadi: "вообще не нужно репорт никакие… Там все будет." The notes: "No custom MSBC reports are needed when agents are used" [[raw/Meeting_Notes_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]].
- **Invoicing.** Genadi: "в какой то момент надо будет лёва подключить… В плане инвойсинг" ("лёва" = [[wiki/people/lev-rudky.md|Lev Rudky]] by context, **inference**). When was not said.

**Against this page: consistent** — it confirms "no special reports" from the agent side.

## Open commitments

- [ ] Nathan Carver, Genadi Peari — review Val's use cases — due on receipt — [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]] *(Oct 20: started — Genadi had not finished; Nathan was studying it [[raw/Meeting_Transcript_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]])*
- [ ] Nathan Carver — add more MSBC endpoints for end-to-end inventory control, from the use cases — due unspecified (Val asked all three to "achieve something by Wednesday"; the notes date it Oct 21) — [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]

## Open questions

- Is the useful engineering data in Genadi's emails, and does it need an agent to pull it out? Val: "if it's in your emails… We can… set up an agent to to go through your emails." Not decided. — [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]

**§15.8:** clear — no pay or rates; the only numbers are lead-time days. **§15 #9:** clear.

## History

- [x] Val Levitan — write a first set of AI COO use cases (up to about 10) for tracking material management and send them to Nathan and Genadi — due Oct 19 2026 ("I will get on it today") — [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]] [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]] *(discharged — on Oct 20 Genadi and Nathan were reviewing "ваш драфт", read as this use-case set by the notes and context, **inference** [[raw/Meeting_Transcript_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]])*

## Sources

- [[raw/Meeting_Transcript_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Mery_Purchasing_Endpoints_and_AI_COO_Use_Cases-October-19-2026.md]]
- [[raw/Meeting_Transcript_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]]
- [[raw/Meeting_Notes_GitHub_MSBC_Repo_Tags_and_Light_and_Wonder_Bracket-October-20-2026.md]]
