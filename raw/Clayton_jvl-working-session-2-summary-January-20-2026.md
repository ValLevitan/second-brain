# JVL Working Session – January 29, 2026

**Attendees:** Clayton Chancey, Lena Zhukova, Val Levitan, Aaron Bockelie

---

## Overview

This session focused on demonstrating the custom JVL Atlassian MCP tools Clayton developed, discussing the AI-augmented workflow approach, and planning next steps for tool adoption.

---

## Demo: Game Status Tool

Clayton demonstrated the `game_status_get` tool using Calle Ocho as an example. The tool returns a plain-English overview of a game's progress across all market variants, aggregating completion percentages, status breakdowns, and active work items. This information previously required manually navigating through multiple Jira projects and counting issues across dozens of features.

Clayton explained the development approach: a 40-minute build cycle from scratch to working demo, enabled by a recursive research loop where Claude Code explored JVL's Atlassian instance using tools it had built itself. This research generated several recommendations for additional utility tools, starting with `game_status_get`.

---

## Discussion: Manual vs. Automated vs. AI-Augmented

The group discussed different mental models for how these tools fit into existing workflows:

- **Lena's perspective:** Current work is highly manual; automation needs to account for the unique creative and artistic elements in each game
- **Val's perspective:** Automation should reduce the bureaucratic burden and enable more games with fewer people
- **Clayton & Aaron's perspective:** With sufficient high-quality context scaffolded intelligently, an LLM can determine *which* pieces to automate and *how*. This is not blind automation, but judgment-informed augmentation.

---

## Technical Requirement: Image Handling

Lena raised an important requirement: when creating Jira structures for new games, she needs to upload artistic images and reference artifacts directly into ticket descriptions. The `create_game_from_template` tool must support embedding a predetermined set of images. This remains a research item.

---

## Clone vs. Blanket Structure

Discussion arose around how to handle game adaptations for new markets:

- Lena prefers a single broad structure applied universally, with non-applicable elements removed case-by-case
- Val emphasized that cloning is key to their use case
- Both acknowledged that while Jira issue structure and game function can be cloned, art elements (images, descriptions, themes) must be unique per adaptation

---

## Next Steps

**Tuesday, February 4 (next session):** Lena will share her screen, and Clayton will walk her through:

1. Installing Claude Code via command line
2. Pulling down and configuring the custom MCP tools for her local Claude Desktop instance
3. Exploring and experimenting with the tools in Claude Desktop

This hands-on, guided experience is intended to build the AI-augmentation muscle memory necessary for new usage patterns to displace existing manual workflows.

---

## Authorization

Val authorized up to 10 additional hours (beyond the 2 hours already spent this week) for Clayton to build out the tools discussed in this session.
