---
type: topic
title: Jira Service Management for field service (Georgia)
date: 2025-10-21
aliases: [JSM, Jira Service Management, service desk, field service, WhatsApp to ticket, ChatOps, SMS support, support ticket flow]
source-count: 1
---

# Jira Service Management for field service (Georgia)

JVL's early thinking on using **Jira Service Management (JSM)** to run customer/field service for its Georgia machine business — turning today's informal WhatsApp/phone support into tracked support tickets. Opened in an Oct-21 2025 Val↔[[wiki/people/aaron.md|Aaron]] session ([[wiki/meetings/2025-10-21-jira-service-management-georgia-field-service.md]]). Ties to [[wiki/projects/georgia-market-rollout.md]]. This is exploratory (Val defining an MVP), not a locked build.

## Starting point

- JVL already has an **established JSM service-desk environment** (usage/management not yet reviewed by Aaron). The Georgia support need slots in as **another project/help-desk** inside it, with dedicated staff, on-call and dispatch. [[raw/implimenting_JIRA_service-october-21-2025.md]]
- Field service today runs on an informal **WhatsApp** discussion; one service person answers most questions and reports to a supervisor who also supervises production and controls final product leaving the shop. [[raw/implimenting_JIRA_service-october-21-2025.md]]

## The MVP: capture WhatsApp support as tickets (ChatOps)

- Val's minimum viable product: **capture the existing WhatsApp discussions inside JSM** as support tickets, then synthesise problems and open/close tickets from there — "already a huge step forward" without formalising anything else. [[raw/implimenting_JIRA_service-october-21-2025.md]]
- There are **Jira/JSM apps that integrate WhatsApp**: add the Jira issue as a third participant to a WhatsApp thread and the back-and-forth becomes **comments on the support ticket**. Aaron named the general practice **ChatOps** — operating a platform via chat, not limited to WhatsApp (Teams and others work too). [[raw/implimenting_JIRA_service-october-21-2025.md]]

## The golden-path flow

- Customer initiates (phone call or WhatsApp) → a **ticket is opened** in JSM → the service person's job is to **close it fast and satisfy the customer**. Aaron pushed to pick the single highest-value initiator (the "golden path") and follow it end-to-end rather than model every trigger at once. [[raw/implimenting_JIRA_service-october-21-2025.md]]

## SMS-to-JSM over call recording

- Val floated **recording and transcribing** service calls (his technicians speak poor English). Aaron warned that capturing a mobile call's audio endpoint is hard, and instead recommended configuring **JSM to accept SMS** — everyone has SMS — so a text registers a ticket. JSM can then run a flow (ask who the customer is, match the name) and send the customer an **official JVL support link** to click on mobile and track/continue the ticket, so the customer sees an official JVL connection rather than a random phone number. [[raw/implimenting_JIRA_service-october-21-2025.md]]

## Where it stands

- Val will investigate how service works today, formalise his thinking, and revert to Aaron. Open design question Aaron flagged: **what initiates a service call** (customer reaches out / JVL makes rounds / machine instrumentation flags automatically). [[raw/implimenting_JIRA_service-october-21-2025.md]]

## Sources

- [[raw/implimenting_JIRA_service-october-21-2025.md]]
