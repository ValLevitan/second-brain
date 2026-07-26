Pavel, Dmitri, Andrei,

Good day.

I understand that our internal meetings at JVL Minsk are recorded. Please confirm this assumption and let me know where those recordings and transcripts are stored — I assume somewhere central, perhaps Azure, but I don't know for certain.

The idea behind this message is simple: we should be getting more value out of those recordings than we currently are. Right now they sit somewhere after the meeting ends, and the knowledge discussed in them — decisions, trade-offs, commitments, technical direction — lives only in people's heads.

I'd like to suggest a possible approach and get your thinking on whether this is the right architecture, or whether you see a better way.

The concept is a pipeline with a few stages:

First, an automated gathering layer. Rather than anyone manually reviewing recordings, a scheduled job runs daily in the cloud (something like n8n, Make.com, or a similar automation platform — roughly $20/month). It picks up new transcripts since the last run, feeds them through an AI model, and extracts structured information. The key here is that this runs headlessly — no one needs to remember to trigger it, and it doesn't depend on someone's laptop being open.

The types of things we'd want to extract from meetings include: action items and who owns them, architecture decisions and the alternatives that were considered, technical risks or blockers raised, dependencies between teams or systems, design patterns or approaches agreed upon, open questions left unresolved, and integration points where systems need to talk to each other. You would know better than I do what else belongs on this list — please add to it.

Second, a review layer. The AI output should not go directly into any official record. Engineering leads would review the daily extract, correct anything the AI got wrong, and approve what gets published. This keeps quality high and prevents garbage from accumulating.

Third, a GitHub knowledge base. Validated extracts — particularly Architecture Decision Records (ADRs) and technical documentation — would live in a dedicated GitHub repository. This gives us version control, pull request approval workflows, and keeps the documentation where engineers already work. The repository would need a well-organized folder structure from day one.

Fourth, graduation to Jira. Here's the rule I'd suggest: if an ADR implies work that someone needs to do, it gets promoted into Jira as a Requirement with proper assignees, dependencies, acceptance criteria, and tracking. If it's purely a record of a decision already made, it stays in GitHub as reference documentation. This gives us traceability from meeting conversation all the way through to a trackable work item, and it gives everyone — including non-engineers — visibility through Jira dashboards without needing to navigate GitHub.

I'm presenting this as a suggestion. The architecture, implementation, and ongoing maintenance of this pipeline is yours to own. You know the tools, the team's workflows, and the technical constraints better than I do. If you see a better approach to achieving the same goal — turning our recorded meetings into lasting engineering knowledge — I'm open to it.

What I'd like from you:

1. Confirm where meeting recordings and transcripts currently live and whether they can be accessed programmatically.
2. Your assessment of this approach — does it make sense, what would you change, what's missing?
3. A proposed architecture if you agree with the direction, or an alternative if you don't.
4. A scope estimate for a proof-of-concept using one week's worth of meeting recordings.

Let's discuss.

Val
