# Meeting Transcription to Engineering Knowledge Base — Summary

## Context

JVL Minsk internal meetings are recorded via Microsoft Teams. Transcripts are currently stored in **MS SharePoint**. The goal is to build an automated pipeline that extracts engineering knowledge from these transcripts and turns it into actionable artifacts (ADRs, requirements, action items, architecture documentation).

This document captures the current state of discussion, proposed architecture, labeling taxonomy, and open items.

---

## Proposed Pipeline (5 Layers)

| Layer | Purpose | Description |
|-------|---------|-------------|
| **1 — Gathering** | Automated extraction | Daily scheduled job (n8n or similar) pulls transcripts from SharePoint, runs AI extraction prompts |
| **2 — Review** | Human validation | Engineering leads review AI-extracted content before publication |
| **3 — Storage** | Version-controlled knowledge | Validated ADRs and technical documentation stored in a dedicated GitHub repository with PR approval |
| **4 — Graduation** | Actionable work | ADRs implying work get promoted to Jira as Requirements with assignees and dependencies. Pure decision records stay in GitHub |
| **5 — Visibility** | Dashboards | Jira provides project managers and compliance a view of active requirements |

---

## Open Item: SharePoint Access

Before any pipeline work can begin, **access to SharePoint transcripts must be resolved**. Two approaches:

1. **MCP (Model Context Protocol) for SharePoint** — Configure an MCP server that provides authenticated access to SharePoint, allowing AI agents to read transcripts directly. This keeps the pipeline self-contained and avoids manual file transfers.

2. **Storage relay** — Export/sync transcripts from SharePoint to an intermediate storage (Azure Blob, S3, local filesystem) that the pipeline can access. Simpler to implement but adds a moving part.

**Decision required:** Which approach to pursue. This depends on IT/admin policies around SharePoint API access and authentication.

---

## Meeting Labeling Taxonomy

Each meeting transcript should be tagged with multi-faceted labels to enable structured knowledge retrieval. Labels are organized into independent facets:

### Facet 1 — Product / System

Which products or systems are discussed. Multiple labels per meeting.

| Label | Description |
|-------|-------------|
| `product:flex-pay` | Flex-Pay payment terminal system |
| `product:flex-pos` | Flex-POS point-of-sale terminal system |
| `product:flex-cashdispensor` | Flex-CashDispensor terminal system |
| `product:orchestration` | Central orchestration layer |
| `product:auth` | Authentication and authorization service |
| `product:gateway` | API gateway |

### Facet 2 — Domain (Architectural Area)

| Label | Description |
|-------|-------------|
| `domain:registration` | Terminal registration flows |
| `domain:payments` | Payment processing |
| `domain:security` | Authorization, roles, permissions |
| `domain:networking` | Inter-component communication |
| `domain:deployment` | Deployment and configuration |
| `domain:integration` | Cross-system integration |

### Facet 3 — Concern (Engineering Activity Type)

| Label | Description |
|-------|-------------|
| `concern:architecture` | Architectural decisions |
| `concern:api-design` | API contracts, interfaces |
| `concern:data-model` | Data schemas |
| `concern:dependency` | Cross-system dependencies |
| `concern:requirements` | Requirements, scope definition |
| `concern:incident` | Incident review, postmortems |
| `concern:tech-debt` | Technical debt discussion |
| `concern:performance` | Performance, scalability |

### Facet 4 — Decision Status

| Label | Description |
|-------|-------------|
| `status:exploring` | Under discussion, no decision yet |
| `status:decided` | Decision made |
| `status:action-items` | Concrete tasks assigned |
| `status:blocked` | Blocked by external dependency |

### Facet 5 — Cross-cutting Dependencies

Explicit directional labels showing which system depends on which:

```
dependency:orchestration→flex-pos
dependency:auth→registration
dependency:gateway→flex-pay
```

### Labeling Process

- **AI proposes labels** based on transcript content (Layer 1)
- **Engineer confirms or corrects** labels during review (Layer 2)
- Labels use a **controlled vocabulary** — no free-text tags to prevent drift (e.g., `flex-pos` vs `FlexPOS` vs `Flex POS`)

### Example: Meeting on "Orchestration/Flex-POS Registration"

```
product:flex-pos
product:orchestration
product:auth
product:gateway
domain:registration
domain:security
concern:architecture
concern:dependency
concern:api-design
status:exploring
dependency:orchestration→flex-pos
dependency:auth→registration
```

---

## Knowledge Extraction Categories

The following types of information should be extracted from each transcript:

| Category | What to look for |
|----------|-----------------|
| **Decisions** | "We decided to use X instead of Y" |
| **Action Items** | "Ivan will do Z by Friday" |
| **Risks Raised** | "If we do this, it could break..." |
| **Dependencies Identified** | "This blocks / depends on..." |
| **Technical Debt Acknowledged** | "Doing a workaround now, will fix later" |
| **Architecture Constraints** | "We cannot do X because Y" |
| **Open Questions** | Questions raised without resolution, need follow-up |
| **ADR Candidates** | Significant decisions that warrant a formal Architecture Decision Record |

---

## Risks and Recommendations

1. **Transcript quality is the foundation.** If Teams transcription is poor (accents, background noise, mixed languages), everything downstream suffers. Validate real transcript quality before building the pipeline.

2. **Start with an MVP.** Take 5–10 real transcripts, run extraction prompts manually, evaluate output quality with engineering leads. Only then automate.

3. **Avoid premature Jira integration.** Automatic ticket creation from AI output risks spamming the backlog. Start with manual promotion from GitHub to Jira.

4. **Use a prompt chain, not a single prompt.** Different extraction tasks (action items, decisions, ADR candidates) require specialized prompts with different instructions and output formats.

5. **Diagrams from transcripts are unreliable.** AI can extract *descriptions* of architecture but cannot produce accurate diagrams without human refinement. Set expectations accordingly.

---

## Next Steps

- [ ] Resolve SharePoint access — MCP integration or storage relay
- [ ] Obtain sample transcripts and evaluate quality
- [ ] Draft extraction prompts for each knowledge category
- [ ] Run manual MVP on 5–10 transcripts
- [ ] Present results to engineering leads for feedback
- [ ] Design automation pipeline based on validated approach
