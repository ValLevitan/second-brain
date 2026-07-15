---
type: decision
title: Insert a "capability" level in Jira as the executive-demonstrable unit mapped to GitHub feature branches
date: 2025-04-03
aliases: [capability level, Jira capabilities, capability vs feature, GitHub Jira mapping, feature branch capability, repository is a product, repository is an artifact, no test no pull, one week feature branch, capabilities bundle of features]
source-count: 4
status: active
open-questions: 1
---

# Insert a "capability" level in Jira as the executive-demonstrable unit mapped to GitHub feature branches

**Decision (Val, worked out with [[wiki/people/aaron.md|Aaron]] over Apr 1–2 2025 and presented to the Minsk team Apr 3):** add a new level in Jira called **capabilities**, sitting **between feature and product**, as the unit an executive can understand and physically demonstrate. A capability is a **bundle of features** (roughly three–four features per capability); a JVL product is described by its capabilities. This resolves the Mar 31 "how do GitHub and Jira line up" homework (see [[wiki/meetings/2025-03-31-github-jira-alignment.md]] and [[wiki/projects/jvl-2025-plan-and-jira-roadmap.md]]). [[raw/gut_hub_jira_relationship-april-2-2025.md]] [[raw/github_jira_setup-april-3-2025.md]]

## Why capability, not feature (the Apr 2 breakthrough)

- Val had assumed a Jira **feature** maps one-to-one to a GitHub **feature branch**, giving him a clean "demonstrate this feature" checkpoint. [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- Aaron showed with a diagram that this breaks: making one real feature work usually requires changes across **several repositories** at once (e.g. the application *and* a shared library), each a separate **story/branch** — so a Jira feature already maps to **multiple** GitHub branches, not one. The demonstrable thing is the **pull-request view** of everything that changed together. [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- Val's resolution: "in my mind, I would connect Git feature branches to a JIRA **capability**… business mind, like mine, and those executives that I communicate with, we talk in capabilities… what should be demonstrable to us is a capability." Aaron noted he was **not** proposing renaming feature→capability; the point is that the demonstrable executive unit is the capability. [[raw/gut_hub_jira_relationship-april-2-2025.md]]

## Repository = product, and "a product is an artifact in motion" (Apr 1)

- Ground rule Aaron set and Val adopted: a **code base / repository is never a product**. Running the build produces an **artifact** (the ISO, executable, output files); "a product is an artifact **in motion**" — an artifact moved over time to market. So a Jira product/ownership item should **not** be equated with a code base. [[raw/git_jira_correlation-april-1-2025.md]]
- Working mapping Val settled on: **feature branch = a Jira feature; stories = the commits under it; when a feature branch is pulled into main, the feature is "done"; the sum of all features → the ISO → the product; repository = a product** (Val: "which I agree might be wrong"). Aaron pushed back that repository-per-product over-simplifies engineering reality — a repository is a **collection of deposits by concern** (library, service, application, firmware), not a product. [[raw/git_jira_correlation-april-1-2025.md]]

## The rules Val set for the team (Apr 3 lecture)

- **SVN → GitHub is locked** — "это уже решили… мы уже перешли" (already decided, already moved); not up for further debate. [[raw/github_jira_setup-april-3-2025.md]]
- Two tools only for this: **GitHub** (development camp) and **Atlassian Jira** (executive camp); **Confluence deliberately left out** of this discussion. Capabilities/features are the "clutch" coupling the two camps. [[raw/github_jira_setup-april-3-2025.md]]
- **Feature branches kept short — max one week.** [[raw/github_jira_setup-april-3-2025.md]]
- **Lengthen the sprint to ~3–4 weeks** (four "feels a bit much," two "too short") so a sprint can **deliver two–four features**; Val deliberately does not sit inside the sprint but controls **delivery of features** and watches commit velocity. [[raw/github_jira_setup-april-3-2025.md]]
- **Who writes what:** product managers ([[wiki/people/juan-martinez.md|Juan]], Val, or Felipe) describe **capabilities** and the user experience; [[wiki/people/pavel.md|Pavel]] sits with Juan to write **features**; **developers** (Val named Igor Metelski/"Мительский" and a "Харецкий"/Haretsky) write the **stories**. If features/stories aren't written down and forced, delivery goes chaotic and unplannable. [[raw/github_jira_setup-april-3-2025.md]]
- **"No test, no pull."** Val invited [[wiki/people/irina-makarych.md|Irina]] because a feature must be **testable**: when a feature opens, QA flags it for an automated test wedged **into the pull into main** — no passing test, no merge. Val's goal is for the engineers under Irina to write the tests themselves. [[raw/github_jira_setup-april-3-2025.md]]
- Val will pull the **ISO himself** — he asked [[wiki/people/andrey-bosik.md|Andrei]] to build him **GitHub Actions** so he can take a capability's code, load it on a machine, and read the capability. [[raw/github_jira_setup-april-3-2025.md]]
- **Repository = product** for now (e.g. **FlexPay is a repository**), though Val admits he still only "loosely" understands what a developer builds inside it (libraries, applications). [[raw/github_jira_setup-april-3-2025.md]]
- **AI/MCP tooling is what makes this possible** — Aaron gave Val a Jira/Atlassian **MCP** so Val can interrogate Jira in plain language ("summarize these features, what capability do they make; where are the scope gaps"), plus the **sequential-thinking MCP**; with Claude/Sonnet + ChatGPT this "diff table" of scope gaps is now easy, in any language. [[raw/github_jira_setup-april-3-2025.md]] [[raw/git_jira_correlation-april-1-2025.md]]

## The gears/clutch analogy and the role split (Apr 3 Aaron session)

On a long Apr-3 English one-on-one ([[wiki/meetings/2025-04-03-github-jira-capability-aaron-session.md]]; the transcript loops/duplicates heavily — facts taken once) Aaron and Val settled the *mechanism* coupling the two tools, extending this decision: [[raw/github_jira_integration_relationship-april-3-2025.md]]

- **Gears and a clutch:** Aaron drew an AI-generated gears animation — commits (fastest) → pull requests → stories → **features (purple, in GitHub)** → **capabilities (green, in Jira)** → product → value stream (slowest). Val "clutched to it." The **clutch** that couples green to purple is the **negotiation/agreement between the executive branch and the engineering branch** (Aaron: tangibly, the **stack-rank order of work in a sprint**). [[raw/github_jira_integration_relationship-april-3-2025.md]]
- **"Don't interfere with the sprint"** — once work is committed to a sprint you must step back and let people work; interfering "breaks everything" ("It's like trying to shift without using the clutch"). Contract negotiation happens *after* the sprint. [[raw/github_jira_integration_relationship-april-3-2025.md]]
- **Run the task list in GitHub, keep the source of truth in Jira (for now):** GitHub issues are a light task list ("they literally call them the same thing that JIRA calls them"); don't track stories/features in GitHub, only **branches of work**. A Git branch name is just a human label to a commit — "feature," "bugfix" etc. are social conventions Git doesn't enforce. Keep developers in their IDE, project managers in project-manager land ("if you ask developers to work in Jira, now they're Jira engineers and not writing code"). [[raw/github_jira_integration_relationship-april-3-2025.md]]
- **Role split:** [[wiki/people/juan-martinez.md|Juan]] = the **non-technical product manager** who ideates/aims capabilities; [[wiki/people/pavel.md|Pavel]] = the **technical product manager** who breaks capabilities into features (he doesn't write code); [[wiki/people/alexander-biratka.md|Sasha]] = the **architect/developer** (Aaron named Sasha the "architect of the Omni framework") who supplies feasibility, estimation, alternatives. "A blend of Pavel and Juan is one product manager." A **feature is born out of negotiation** to deliver a capability within a set time (~one week per feature) — "almost like negotiating MVPs." [[raw/github_jira_integration_relationship-april-3-2025.md]]
- Aaron's scale caveat: this whole approach works only for a **team under ~20 people** (JVL's dev org is under 20) — bigger and "you're just farming it off to India." Val's recurring exhibit: his AI-driven **cottage-office renovation** — recording the contractor walkthrough, feeding it to AI to find scope gaps and generate a signable quote — the same method he applies to reconcile feature branches to a capability. [[raw/github_jira_integration_relationship-april-3-2025.md]]

## Why it matters to Val (Apr 1, in his own words)

Val framed the whole exercise as being about his own comfort and control, not engineering elegance: "My function is to create alignment and symbiotic movement from requirements to code commit… unless I can smoothly and comfortably move between the requirements and the ISO image, everything else is immaterial to me." He recounted his prior company being sold to a billion-dollar American acquirer at ~30%/yr top-line growth and ~44% net margin, then hollowed out (margin to 10%, out of business in 15 years) after being moved onto **SAP** and split into departments — his cautionary tale against structure-for-structure's-sake. [[raw/git_jira_correlation-april-1-2025.md]]

## Open questions

- **Flatten GitHub to one organization, or keep many orgs?** Unresolved. Aaron pushed hard to **flatten all repos into one org** with a naming convention (e.g. `framework-omni-renderer`), citing Block/Square keeping ~30 repos in one space, and warned Val's per-org control is "a precarious knife edge." Val **refused to flatten** — he cannot achieve executive alignment without the org/concern structure — but conceded there are "too many orgs" today and that people are already committing into an unvetted new org ("wild west"). Aaron's model of the org level = a **concern** (manufacturing, finance, marketing, sales, HR), with repositories under it named by purpose (library/service/application/firmware). This revisits, and does not yet supersede, [[wiki/decisions/2025-02-11-github-org-naming-and-structure.md]] and [[wiki/decisions/2025-01-20-github-orgs-mirror-value-streams.md]]. [[raw/git_jira_correlation-april-1-2025.md]] [[raw/gut_hub_jira_relationship-april-2-2025.md]]

## Sources

- [[raw/git_jira_correlation-april-1-2025.md]]
- [[raw/gut_hub_jira_relationship-april-2-2025.md]]
- [[raw/github_jira_setup-april-3-2025.md]]
- [[raw/github_jira_integration_relationship-april-3-2025.md]]
