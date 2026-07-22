---
type: meeting
title: Standing up Jira Service Management for Georgia field service — WhatsApp/SMS to tickets (Oct 21 2025)
date: 2025-10-21
aliases: [JSM Georgia, Jira Service Management, field service desk, WhatsApp to ticket, ChatOps, SMS support MVP, service call ticket]
source-count: 1
---

# Standing up Jira Service Management for Georgia field service (Oct 21 2025)

**Date:** 2025-10-21 (1:45pm) · **Attendees:** [[wiki/people/aaron.md|Aaron Bockelie]], [[wiki/people/val-levitan.md|Val Levitan]]. 11m. English.

Val asks Aaron how to start thinking about using **Jira Service Management (JSM)** for JVL's customer/field service in Georgia. Substance rolls up to [[wiki/topics/jira-service-management-field-service.md]] and ties to [[wiki/projects/georgia-market-rollout.md]]. §15.8: no compensation material.

Durable points (single source — see the topic page for the synthesis):

- **There is already an established JSM service-desk environment.** Aaron noted JVL has an existing JSM service desk (he hasn't reviewed how it's used); the Georgia support need becomes "just another project"/help-desk inside it, with dedicated staff, on-call and dispatch. [[raw/implimenting_JIRA_service-october-21-2025.md]]
- **MVP = capture the existing WhatsApp support culture in JSM (ChatOps).** JVL already runs a WhatsApp support discussion; there are **Jira/JSM apps that integrate WhatsApp**, adding the Jira issue as a participant so the WhatsApp back-and-forth becomes **comments on a support ticket**. Val's chosen minimum viable product: just capture those discussions as tickets first, then synthesise problems and open/close tickets from there. Aaron named the general term **ChatOps** (operating a platform via chat — not limited to WhatsApp; Teams or other tools work too). [[raw/implimenting_JIRA_service-october-21-2025.md]]
- **The golden-path flow.** Customer initiates (phone call or WhatsApp) → a ticket must be opened in JSM → the service person's job is to close it fast and satisfy the customer. Aaron pushed to pick the single highest-value initiator ("golden path") and follow it end-to-end rather than model every trigger at once. [[raw/implimenting_JIRA_service-october-21-2025.md]]
- **SMS-to-JSM over call-recording.** Val floated recording service calls and transcribing them (his technicians speak poor English); Aaron warned capturing the audio endpoint on a mobile is hard and instead recommended configuring **JSM to accept SMS** — everyone has SMS — so a text registers a ticket, after which JSM can run a flow (ask for the customer, match the name) and send the customer an official JVL support link they can click on mobile to track/continue the ticket. The goal is the customer seeing an **official JVL support connection**, not a random phone number. [[raw/implimenting_JIRA_service-october-21-2025.md]]
- Val's close: he will investigate how service works today, formalise his thinking, and revert to Aaron. [[raw/implimenting_JIRA_service-october-21-2025.md]]

## Sources

- [[raw/implimenting_JIRA_service-october-21-2025.md]]
