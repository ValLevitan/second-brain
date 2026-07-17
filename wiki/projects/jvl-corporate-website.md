---
type: project
title: JVL corporate website (new site, three modules)
date: 2024-11-06
aliases: [JVL website, new website, corporate site, client portal, website redesign, JVL public client portal]
source-count: 4
open-questions: 2
---

# JVL corporate website (new site, three modules)

The rebuild of JVL's public website, run by [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] under Val, planned in **three business modules** — (1) **online games** (a B2B portal for casino operators), (2) **ECHO / eco-amusement** (Amazon-supported consumer device), (3) **land-based cabinets** — built by an external contractor on a fixed-price basis. The founding alignment call is [[wiki/meetings/2024-11-06-website-architecture-and-design.md]] (Nov 6 2024); the sequencing/Brand-Registry ruling is [[wiki/decisions/2024-11-06-website-online-first-brand-registry-for-echo.md]]. Later 2025 sources show the vendor contract being signed (~Feb 1 2025, via Monica — see [[wiki/people/andrei-klimovich.md]]), so the plan below is the **as-of-Nov-2024 baseline**, not verified current state. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

## Goals & KPIs (Nov 2024)

- Goals: build JVL brand **recognition and credibility**, drive organic traffic, grow social-media engagement. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
- KPI targets set by Andrei: **+30% organic traffic** to the site and **+20% social-media audience** within the **first year of operating the full (three-module) site**. Val challenged how this justifies the spend; Andrei's logic: a share of visits converts to leads across the three modules (online → aggregation platforms/operators taking games; land-based → machine buyers). [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
- The online module is a **B2B site**: the target visitor is the casino operator's **game-content manager**, who must be able — without registration — to see a game's key facts (mechanics, lines, reel configuration, volatility, visual theme) and **play free spins in one click**, then reach a contact form. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

## Release ladder (as planned Nov 6 2024 — dates were targets, not commitments)

1. **Release 1 — online core:** new design + landing pages, online-game collection, per-game profile (with in-browser play), contact/lead form, About Us, terms pages. Target: **first half of March (~Mar 10 2025)**, assuming the Polish contractor's holidays are accounted for. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
2. **Release 2 — marketing layer:** blog module + latest-news widgets, reviews, **partner page** (reciprocal links with review sites for SEO); after this JVL starts pumping search presence with keyword articles. Target ~end of March. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
3. **Release 3 — closed client module:** a login-gated area where connected operators self-download marketing archives (screenshots, icons, certificates), cutting support communication. Target ~end of April. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
4. **Release 4 — ECHO landing:** a light page redirecting to the Amazon store page (no own e-commerce yet), plus **multi-language support** added at this stage (B2C needs at least Spanish; earlier B2B stages manage in English). Val judged a heavy ECHO module low-value if machines sell via Amazon ("я бы не делал"). Target ~Apr 15. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
5. **Release 5 — e-commerce + customer finance:** integrate an e-commerce solution ("условный Shopify") and a customer-finance solution ("условный Кларна") so ECHO can sell and be redirected to marketplaces. Target ~end of May. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
6. **Then self-service, then cabinets:** Val re-ordered the tail — after ECHO, build the **online-games self-service** ("Self-Service for online games distribution", architecture designed in advance, delivery ~Nov 1 2025); the land-based **cabinets module comes last** ("я пока за кабинет не очень волнуюсь"). [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

**Contract model:** fixed-price per stage; releases 1–2 contracted first (Val's ruling — see [[wiki/decisions/2024-11-06-website-online-first-brand-registry-for-echo.md]]); wireframes + specifications for the first releases were already prepared. Services expected from the contractor: artistic direction, design, content, web development, third-party integrations; **deployment, hosting and hosting costs stay with JVL** (contractor gets no access — provides documentation/support only). [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

**The "final frontier" vision** Val asked to append to the contractor brief — a self-service portal where a new operator can read the template agreement, execute it via DocuSign, receive the RGS and deploy games without talking to anyone — is recorded with the online-business material on [[wiki/topics/online-games-rgs-distribution.md]] (2023–2024 History). Val wanted the horizon written as releases on a ~1.5-year line so the contractor's architects design for it (e.g. Jira integration hooks, deployment triggers). Terminology agreed on the call: **"deployment"** = pushing the site/product to where it operates; **"release"** = a slice of functionality shipped. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

## The requirements specification (epics document)

A written requirements pack — general requirements plus epics with user stories and acceptance criteria ("JVL website 2.0 epics") — exists as a source document; it matches the release-1/2/3 scope above. Undated; consistent with the Nov-2024 "specifications ready for the contractor" state. Highlights: [[raw/jvl_website_20_epics_use_cases_and_accpt_criteria_2025-03-29.md]]

- **General requirements:** support latest+2 browser versions (Chrome/Safari/Firefox/Edge) and latest+1 iOS/Android; responsive breakpoints (≤480px / 481–768 / 769–1024 / 1025+); **WCAG2** accessibility; page load **<2 seconds** on average with acceptance tests run from the key markets **US, Colombia, Mexico, Peru, EU**; capacity for **10,000 users** and up to **100 concurrent** over 5 years; breadcrumbs everywhere except the landing page; architecture built for constant content/feature expansion; the **blog is the main SEO area**. [[raw/jvl_website_20_epics_use_cases_and_accpt_criteria_2025-03-29.md]]
- **Epics (visible in the pack):** EPIC-1 Landing page (header/menu, JVL info cards, "Discover Our Games" theme cards, footer with LinkedIn/YouTube/18+ logos and licence text); EPIC-2 Games section (games list of 20/page, featured game, search from 2nd character, filters by theme/features/volatility, single-game view with video + 4–5 screens + reels/paylines/features, an **iFrame demo** of each game); EPIC-3 general pages (About Us with history timeline/mission/values/partners; Contact Us with four form types — Casino / Platform / Media Partner / General — each creating a **lead in the integrated CRM**; Partners page; latest news; blog with CMS + meta tags); EPIC-4 **Online user role** — manually-provisioned registered users sign in to see game assets (asset package, game rules by language, game sheet, help screens; single files **up to 30 GB**), general assets (master game list, supported currencies, RGS materials, vendor materials) and gated game attributes (Game ID, RTPs, max win, min/max bet, certificates). Future roles anticipated (e.g. "Cabinets Viewer"). [[raw/jvl_website_20_epics_use_cases_and_accpt_criteria_2025-03-29.md]]
- **References used:** UI/content references to yggdrasilgaming.com (contact, news) and slotmatrix.com (login, clients-area structure); UI mockups on a Miro board. (The pack also contains working login credentials for a reference portal — **not reproduced here**; flagged to the owner per the no-credentials rule.) [[raw/jvl_website_20_epics_use_cases_and_accpt_criteria_2025-03-29.md]]

## Status — near launch-ready (Apr 15 2025)

- Klimovich to Val: "back-end готов, front-end готов, контент менеджмент систем … тоже готовы, все лежит и ждет нашего approval." He was sending Val an updated, "более цветастой" design version the next day (the prior look "казалось … слишком темная"); after a minimal-redesign approval, going live "это уже вопрос пару дней" — plus roughly a week of content work (game images, texts) to fill the site. [[raw/andrei _klimovich_update-apr-15-2025.md]]

## May 16 2025 — "release it now, sign off 30 days later"; Echo page slips past June

From the May-16 Klimovich update ([[wiki/meetings/2025-05-16-klimovich-update-echo-website-pace.md]]; English): [[raw/andrei_klimovich_update-may-16-2025.md]]

- **First release ready but untested.** The first version looks "more or less stable" to Andrei (some known defects); [[wiki/people/ivan.md|Ivan]] wanted at least a day of deep technical testing, but "we don't have somebody" experienced in testing digital products. [[raw/andrei_klimovich_update-may-16-2025.md]]
- **Val's contract move — release now, defer sign-off.** Rather than block on testing, **release as-is and don't sign off acceptance for ~30 days**; the vendor's pre-release defect-fix commitment simply **moves to a post-release window** under the same frame contract (each release is separately estimated: prepayment on approval, balance on acceptance). Val: the downside is tiny — the vendor charges **$30/hour**, ~10 hours of fixes ≈ **$300** exposure — "sitting in one spot is not a solution." Practical steps: **withdraw the testing request** from the vendor (so it isn't hanging over him), find bugs on the fly using in-house people to exercise the site — **Sebastian, Lev, Mary, Anibal (Peru)** — and add a light "found something? tell us" disclaimer. Go-live "on Monday." [[raw/andrei_klimovich_update-may-16-2025.md]]
- **Launch shape:** a landing with **About JVL / Contact** basic pages now; **partners + reviews** (online games) in ~a week; **Flex** (land-based) and **Echo** just **redirect to the current existing pages** for now ("better than not to redirect anywhere"). New Flex/Echo designs come **after** Echo, with the **same web design/development team** (still Andrei coordinating). [[raw/andrei_klimovich_update-may-16-2025.md]]
- **Echo page slips:** the earlier "Echo on the website by early June" target is off — "it takes more time to test and stabilize… than I expected"; Andrei to re-estimate the Echo module with the vendor the following week. This continues Val's incremental-not-perfect coaching (10→20→40 in steps, don't "marinate") — recorded on [[wiki/people/andrei-klimovich.md]]. [[raw/andrei_klimovich_update-may-16-2025.md]]

## Open questions

- Did the website ship on anything like the Nov-2024 release ladder (R1 target ~Mar 10 2025)? Jan–Mar 2025 sources confirm only that the vendor contract reached signature (~Feb 1) — no launch record in the wiki yet. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
- Who is the website contractor? The call implies a candidate **from Poland** ("Если мы берем контрактора из Польши, будут польские праздники") but never names the firm. [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]

## Sources

- [[raw/business_architecture_and_the_website_design_for_online_2025-03-29.md]]
- [[raw/jvl_website_20_epics_use_cases_and_accpt_criteria_2025-03-29.md]]
- [[raw/andrei _klimovich_update-apr-15-2025.md]]
- [[raw/andrei_klimovich_update-may-16-2025.md]]
