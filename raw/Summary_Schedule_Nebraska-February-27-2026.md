# Summary — Schedule Changes for Nebraska (Feb 27, 2026)

**Participants:** Val Levitan, Juan Martinez, Pavel Frolov, Irina Shishko
**Duration:** 49m 5s

---

## Context

The team is reprioritizing to push Nebraska skill game software changes to the forefront. A competitor (Light and Wonder) has entered the Nebraska market using a more flexible approach to skill game regulation, prompting the team to adjust their own implementation.

## Three Requirements Under Discussion

### REQ-998 — Audit Ticket
- Operator-requested feature for book reconciliation at locations
- Manual print only (not auto-print on door open, unlike South Dakota)
- Accessed via the setup/attendant menu; fields match the existing South Dakota audit ticket
- Will apply to both Nebraska and Texas
- **Status:** Moved to **Published**

### REQ-1007 — Whole Dollar Rounding on Cash-Out Tickets
- Kiosk locations cannot dispense coins, so TITO tickets must print only whole-dollar amounts
- Fractional cents remain on the credit meter and trigger the last-bet/risk feature so the player can continue
- Must be an **on/off toggle** (default: on), adjustable per location via attendant key
- AFT payouts would still include the full fractional amount
- Juan to update the requirement description with risk-bet behavior details per Irina's request
- Applies to both Nebraska and Texas
- **Status:** Moved to **Review** (pending description update)

### REQ-1010 — Graphical & Skill Game Changes
- Remove the power meter primary skill; replace with a simpler **50/50 icon selection** (choose which icon has more coins) to speed up gameplay
- Make the "touch the pattern match" skill prompt less visible (smaller font, darker color, no border) — aligning with competitor approach
- Originally included **liquid glass UI overhaul**, but the team decided to **defer liquid glass** to avoid a 30–90 day delay
- **Status:** Moved to **Draft**

## Key Decision: No Liquid Glass for Now

Liquid glass would delay the release significantly (30–90 days). Without it, the three REQs plus game modifications can be submitted to Eclipse (the testing lab) within approximately **2 weeks**. The team unanimously agreed to proceed without liquid glass.

## Marching Orders

1. **Juan** — Finalize and groom all three requirements so Irina and Pavel have no remaining questions; update REQ-1007 with risk-bet behavior details
2. **Pavel** — Create Jira features linked to the requirements; schedule them into the next sprint (starting Thursday)
3. **Irina** — Provide screenshots of existing attendant screen UI for the audit ticket flow
4. **Team** — Complete development within the upcoming sprint cycle, then push for Eclipse lab approval as fast as possible

## Process Notes

- The team is moving toward using meeting transcripts to generate Jira tasks directly (via Claude/MCP automation)
- Val raised a gap in the workflow: a missing **engineering/architecture decisions layer** between requirements and features — noted as something to research and potentially automate
- Dmitri's automated acceptance-criteria migration is creating duplicates in Jira descriptions; the team agreed not to fix manually — MCP tooling will clean it up
