---
type: meeting
title: OneDrive / SharePoint file-architecture discussion — replacing email-shuttled Excel files (Sept 15 2025)
date: 2025-09-15
aliases: [OneDrive SharePoint discussion, SharePoint file architecture, payment-proposal SharePoint, document management SharePoint, Georgia Sales Funnel site]
source-count: 1
---

# OneDrive / SharePoint file-architecture discussion (Sept 15 2025)

**Date:** 2025-09-15 (4:01 PM) · **Attendees:** [[wiki/people/alka-sood.md|Alka Sood]] (host), [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] (IT), [[wiki/people/andrey-bosik.md|Andrei Bosik]] (IT), [[wiki/people/igor-donis.md|Igor Donis]], [[wiki/people/felipe-miranda.md|Felipe Miranda Giorgi]]. English. (Source file cited verbatim with its irregular spacing: `One-Drive _ Sharepoint_discussion.md`.)

A working demo/decision session where [[wiki/people/alka-sood.md|Alka]] pushed to stop emailing Excel files around the finance team and instead share them from a secured cloud location, with [[wiki/people/dmitri-kovalchuk.md|Dmitri Kovalchuk]] live-demonstrating SharePoint. Related IT context on [[wiki/topics/infosec-and-server-infrastructure.md]]; the finance-workflow context on [[wiki/topics/jvl-finance-back-office.md]] and [[wiki/people/alka-sood.md]].

Durable points (single source):

- **The problem Alka wants to fix.** The weekly **payment proposal** she sends Val each Monday/Tuesday (he reviews the payments to authorize, adds comments, sends the spreadsheet back) breaks in two ways: if Val doesn't save it properly the instructions can be lost, and the file **gets corrupted moving around over email**. Her target solution: send Val a **link** to a file on OneDrive or SharePoint — he clicks, adds comments, closes, and the team has it instantly — eliminating the corrupting email traffic.
- **Security + lock requirements.** Access must be limited to a few named people; there are **four or five categories of files**, and not every participant should see every file. Example: the **pre-authorized customer-payment file** holds sensitive banking details and should be visible only to Alka, the person setting up the payment, and Val (even [[wiki/people/felipe-miranda.md|Felipe]] shouldn't see everything in it). Alka also wants Val to be able to **lock** a file once he authorizes it, so no one can override his instructions ("his instructions are final").
- **SharePoint vs OneDrive (Dmitri).** SharePoint is a **site**; OneDrive is a **storage system** — they feel the same in use but are different locations. Dmitri demonstrated creating a **private team site** (Microsoft-credential sign-in, members added, owner/edit rights). Working files (Word/Excel) open online; other files (e.g. PDF) download. A OneDrive path shows "/my…"; a SharePoint path shows the site domain.
- **Decision: start on SharePoint.** Val: "why don't we start working with SharePoint and we'll see… we will quickly understand if we like it or not." Alka will start sending Val the **payment proposal via SharePoint next week**, and she and Val will begin working the **cash flow** on it the next day.
- **Alka's site design (to be structured).** She anticipates ~**5–6 sites**: an **accounting site** (holding the payment folder, cash-flow projection, monthly reports, PO authorization), an **executive site** for the management reporting she and Val share, and others (action list, reporting checklist, control-sheet files). Governance concern: **not everyone should be able to create sites** ("we don't want a whole bunch of rubbish in there"). Members to add later: **Chris and Laura** (accounting), **Elizabeth and Felipe** (sales side).
- **Business Central link (aspiration).** Val wants the payment/PO report **built in Business Central and linked to SharePoint** — click an invoice on the SharePoint site and open it in Business Central. Dmitri hadn't tried it; Val expects a Microsoft product to support it. Igor tasked to explore connecting Business Central as an app, with help from Andrei/Dmitri.
- **Accounting-folder migration.** Dmitri proposed moving the local-office **accounting folder** onto SharePoint; Alka agreed but wants to **clean it up first** — only the **last three years** of files, not older material (nothing from 2011–2012).
- **Felipe's live setup.** Felipe created a SharePoint **team site named "Georgia Sales Funnel"** and moved his weekly-sales file onto it (it had been on his personal SharePoint/OneDrive), sharing the site link with Val.

## Open commitments

- [ ] Alka Sood — start sending Val the weekly payment proposal via a SharePoint link next week; begin working the cash flow with Val on SharePoint the next day — due ~week of Sept 15 — [[raw/One-Drive _ Sharepoint_discussion.md]]
- [ ] Alka Sood — design the SharePoint site structure (~5–6 sites: accounting, executive/management-reporting, payment folder, etc.) with governance over who can create sites — due unspecified — [[raw/One-Drive _ Sharepoint_discussion.md]]
- [ ] Igor Donis — connect Business Central as a linked application to the SharePoint site (with help from Andrei/Dmitri) — due unspecified — [[raw/One-Drive _ Sharepoint_discussion.md]]
- [ ] Dmitri Kovalchuk / Alka — migrate the local-office accounting folder onto SharePoint after cleaning it to the last three years of files — due unspecified — [[raw/One-Drive _ Sharepoint_discussion.md]]

## Sources

- [[raw/One-Drive _ Sharepoint_discussion.md]]
