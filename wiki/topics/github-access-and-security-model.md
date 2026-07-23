---
type: topic
title: GitHub access and security model
date: 2025-02-12
aliases: [Codespaces, audit log, least privilege, Entra ID SSO, GitHub security, role-based access, access revocation]
source-count: 2
open-questions: 1
---

# GitHub access and security model

How JVL will control who can see and change code once its repositories live in the GitHub enterprise. Worked out on the Feb 12 2025 GitHub check-in (Val, [[wiki/people/aaron.md|Aaron]], [[wiki/people/andrey-bosik.md|Andrei]], [[wiki/people/pavel.md|Pavel]], [[wiki/people/alexander-biratka.md|Alexander]]). The core ruling — repos private by default, access granted per repository — is on [[wiki/decisions/2025-02-12-github-repos-private-by-default.md]]. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Private vs internal repositories

- GitHub offers two non-public repo types inside an enterprise: **internal** (visible to every enterprise member, whichever org they belong to) and **private** (visible only to invited members). JVL cannot change this GitHub-imposed behaviour, so it defaults everything to private. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Least-privilege access

- Val's principle: **no blank check** — "checks and balances." A new user is added to an organization with read access at most, and no write rights for roughly the first three months; the organization manager grants finer access per repository as needs arise. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- Val nonetheless dislikes managing access per-repo one user at a time (potentially 50+ repos), and wants organization managers to own that. Whether GitHub **teams/groups** can bundle users with the same rights was raised as unknown and left to research. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Codespaces (protecting sensitive code)

- Aaron introduced **Codespaces** — a virtualized development environment and machine hosted inside GitHub, run in the browser, so code never lands on the local workstation. He suggested it especially for the **math** project/organization, as a way to let people work without the source ever leaving GitHub. Presented as "a piece of the puzzle," not the whole answer. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- Val was initially skeptical ("a person could take a picture with a phone"); Aaron's framing is **trust but verify** — you cannot fully stop a trusted developer copying code, so control the workstation, the network, and the access instead. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Audit log and activity-based revocation

- Aaron pointed to GitHub's **audit log** (who did what, when) and an access-hygiene pattern Val liked strongly: if a user has rights to a repo but has not committed to or touched it for a long time (e.g. six months), that unused access is a risk and should be cut off ("nothing personal"); if someone only ever browses a repo they don't contribute to, question why they have access. Val said this supervision "will be the most used tool for me." [[raw/Check_in_on_GitHub_2025-02-12.md]]
- Aaron described how large enterprises (his example: **Ford**, moved from on-prem to cloud GitHub) enforce this with VPN, corporate network egress, man-in-the-middle inspection, and infosec monitoring — infrastructure JVL cannot afford, so JVL scales what it can: trusted workstations, trusted engineers, on/off accounts, role-based source isolation, and Codespaces. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Entra-ID / SSO administrator account (the recurring friction)

- Val repeatedly objected to a generic **"IT" / global administrator** account appearing in GitHub; he insists the identity should be the person (e.g. Andrei), not "IT." Andrei explained the account was created automatically by **Microsoft Entra ID** when SSO was configured. Aaron's position: with SSO set up correctly via the SAML trust you should not need a standalone JVL administrator account in GitHub at all — something in the current Entra/GitHub configuration is creating it. Homework: rebuild the org setup from scratch and eliminate the generic admin identity. [[raw/Check_in_on_GitHub_2025-02-12.md]]
- Aaron pointed Andrei at the **"Well-Architected GitHub"** enterprise architecture guide (security/design/collaboration best practices, enterprise policies + checklist that repos can inherit) and reminded him that paid GitHub support should be used for hard setup problems. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Feb 6 2026 — Bitbucket-migration leftover identities + JVL-credentials-only directive

On the [[wiki/meetings/2026-02-06-ui-claude-code-adaptation.md|Feb-6-2026 UI/Claude-Code session]] Aaron's live Claude Code run over the LGS repo surfaced an **"unnamed" contributor** in the code-owner / commit history. [[wiki/people/andrey-bosik.md|Andrei Bosik]] explained it was **carried over from the Bitbucket→GitHub migration** ("a name from Bitbucket"), not a live account. Val pushed back hard — he had directed GitHub be "cleaned out" — and gave two directives: **clean out those leftover names**, and **establish the rule that nobody without JVL credentials can access GitHub**. Andrei cautioned that historical commit names may not be fully removable. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

- **Authentication timeout for agent tools.** Andrei had set the GitHub identification/auth timeout to **8 hours**; Aaron flagged that frequent re-authentication (being prompted again after ~20 minutes away) **breaks agentic coding tools**, which fail whenever continuous authentication drops — so auth stability is now an engineering concern, not just a convenience. [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
- **Governance-as-code.** The same session committed a **CODEOWNERS file (file ownership + automatic reviewer assignment)**, **PR / bug-report / feature-request templates**, and a template-chooser config into the repo — moving access/ownership rules into the repo itself (the "well-formed GitHub project" scoring Aaron had pointed Andrei at earlier). Substance of the handbook is on [[wiki/topics/ai-assisted-development.md]] (Feb 6 2026). [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]

## Open questions

- Can GitHub **teams/groups** bundle users with shared access rights so managers don't set permissions per user per repository? Raised as unknown; to be researched. [[raw/Check_in_on_GitHub_2025-02-12.md]]

## Sources

- [[raw/Check_in_on_GitHub_2025-02-12.md]]
- [[raw/UI_Claude_Code_adaptation-February-6-2026.md]]
