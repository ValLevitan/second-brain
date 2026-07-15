---
type: project
title: Georgia market rollout (Peach1234 / DLKG)
date: 2025-02-19
aliases: [Georgia, Georgia co-op, Peach1234, DLKG, Georgia Lottery, GLC, Eclipse, dual SAS, third printer port, Peach 1, Peach 2, Peach 3, Peach 4, JPRE, curved monitor cabinet, flex curve, Georgia 1, Georgia 2, conservative nudge, enhanced nudge, La Rosa, El Jaguar, nudge animation freeze]
source-count: 12
open-questions: 3
---

# Georgia market rollout (Peach1234 / DLKG)

JVL's core land-based market — the conventional **Georgia co-op / COAM** business — and the software releases (**Peach1234** and **DLKG**) needed to keep it and roll out the new payment-kiosk/printer support. Worked through on the Feb 19 2025 outstanding-subjects alignment call with [[wiki/people/val-levitan.md|Val]], [[wiki/people/pavel.md|Pavel]], [[wiki/people/irina-makarych.md|Irina]] and [[wiki/people/juan-martinez.md|Juan]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Why it matters (Val's revenue warning)

- Val expects a **~40% drop in JVL's conventional Georgia revenue** because two main competitors entered last year. If the main market's revenue falls and the new markets aren't rolled out, JVL "cannot pay wages" / sustain the company. He distinguished **rollout priority** (getting the product into the *marketplace* in Georgia, South Dakota, and Puerto Rico) from development priority — GLI and the Eclipse lab "don't care about timing," so a release manager must drive market rollout. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Dual SAS + third dedicated printer port

- Georgia previously required **dual SAS** (two independent SAS ports on two DB9 connectors, primary + secondary, with the primary controlled by the Georgia Lottery Corporation / "GLC") — implemented last year. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Now that pay-kiosks (relying on the TITO model) need an on-board printer, JVL is adding a **third dedicated printer port**: a new DB9 connector (a **harness**, not a "jumper") inside the CPU box, driven by a **hardware-abstraction-layer library** (Pavel corrected Val that "firmware" is wrong — the printer's firmware sits on the printer; JVL's side is a HAL library). Two printer library types: **Gen 2 / Gen 5 (JCM) + nano-optics** share one communication language; **Epic** uses a different one. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Design intent (Juan/Val): the third COM port is **always the printer**, defaulted so operators don't reassign SAS ports by mistake (SAS 1 must stay primary per Georgia rules; SAS 2 can be reassigned only on a COM 1 malfunction). Pavel to remove/relabel the printer connection in the SAS-port selection UI so the wrong port can't be picked. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Bally iview reporting mismatch (Peach1234)

- On the last test, **Irina** reviewed the **Bally iview** logs and found JVL is correctly matching and sending the right data to Bally, **but Bally's final report is not correct** — JVL doesn't understand how iview produces that report. Val doesn't fully trust the Bally reports (on the Georgia machine he can't select "secure enhance"/"system"). Path forward: build the software, get it to the **Eclipse** lab, and test with the system; Val to call Eclipse. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Peach1234 / DLKG shared build

- Peach1234 and DLKG will use the **same LGS version** to simplify submission to Eclipse, and the same **Progressive Controller** setup approach as the Florida "JPRE" market (an initial-setup screen picks the controller on the network; an **embedded progressive controller** works for a single machine, since Georgia locations usually have one machine). [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- **Felipe** has the current **Diamondlink** software that supports the printer; the printer work is urgent for him. See [[wiki/people/felipe-miranda.md|Felipe Miranda]]. [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Release cadence — staged "Peach" packages (Mar 7)

- Georgia will be released in **four staged packages** — **Peach 1, Peach 2, Peach 3, Peach 4** — at roughly **six games at a time**, on ~one-to-two-week intervals, rather than all games at once. Staging is more expensive on **Eclipse** approvals but necessary because [[wiki/people/lena.md|Lena]]'s team is a bottleneck implementing changes across all games. [[wiki/people/felipe-miranda.md|Felipe]] confirmed the tests passed, so releasing can start. [[raw/game_design_meeting_march_7_2025.md]]
- **Sequencing:** Peach 1 and Peach 2 make up ~**80%** of what's installed in the field; Peach 3 has little install base and Peach 4 isn't installed yet. **Diamond Link** is to be "snuck in" right after Peach 2 (to help sell that machine), then Peach 3 and 4 follow. **Ivan** (release) needs ~**10 days** from starting with Eclipse to issuing a purchase order and submitting the FTP link; Val asked to add a 25% time buffer. [[raw/game_design_meeting_march_7_2025.md]]
- **Pay-table-ID risk:** JVL wanted operators to be able to check the **pay table ID**, but **United** said on a call they **can't** do that — so JVL must take a "leap of faith" that the E9 team's pay table IDs work. Val flagged he dislikes it. [[raw/game_design_meeting_march_7_2025.md]]
- **Old framework for Georgia:** **Jackpot Rush** (and **JPRE**) for Georgia stay on the **old framework** with the **curved-monitor cabinet** targeted for the **summer / gaming show (August)**; only new games go on the new "omni" framework, starting with the Fortune Foo Paws pilot. Keeping new product on the old framework means maintaining Rage Studio and the old stations longer, and the **nudge mechanic** needs updating — parked for a later meeting. [[raw/game_design_meeting_march_7_2025.md]]

## Peach 3/4 "finished but not deployed" (Mar 12)

- On the Mar 12 Gottlieb call, [[wiki/people/michael-gottlieb.md|Michael]] relayed that per Juan and Felipe, only **Peach 1 and Peach 2** are really deployed — **Peach 3 and Peach 4 are finished but not yet in the field** (Jackpot Rush too) — and questioned why Val kept pushing for more product when what's done isn't deployed. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- **Val's explanation:** there is **latency between perception and reality** — two large competitors entered the market with worthwhile innovations, which consumed operators' resources (slowing JVL's deployment) and weren't detected immediately; there was also hesitance about the new payment system. He **pressed the brakes at Peach 4** once demand was seen to have dropped, and said in hindsight he would not have pushed Peach 4 — though he'd partly treated it as an "insurance policy" / show-floor bragging rights. Going forward he favours **amortizing the existing library** (e.g. HHR as least-investment/most-revenue, or reviving a 20-year-old "wolves" animal title in class three) over building Peach 5/6. [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]

## "Georgia 1" vs "Georgia 2" nudge, and the Nebraska spin-off (Mar 14)

- Val's framing on the Mar 14 Nebraska call: **Georgia 1** is the current **conservative skill nudge**; **Georgia 2** is the **advanced/enhanced skill nudge** the competitors are introducing. The advanced feature is to be deployed onto **Nebraska as it rolls out for Georgia** — acceptance risk being lower than depending on it from launch. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- Nebraska reuses the Georgia Peach 1/2/3 software (hands removed, nudge reverted to conservative, other enhancements kept) — the full plan is its own project: [[wiki/projects/nebraska-skill-market.md]] and [[wiki/decisions/2025-03-14-base-nebraska-on-georgia-conservative-nudge.md]]. [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]

## New Georgia financial product (Mar 23, from the Doug update)

- Beyond slot machines, JVL developed a **new financial product for Georgia** — **not a slot machine** — built to support **changed Georgia legislation** and **symbiotic** with JVL's slot product. **Mandatory installation is by June 2026.** Val expects purchases to start ~**November 2025** and intensify toward mid-2026. JVL is one of **three players** in that market, with ~**6,000 installations** in play; the machine sells for ~**$12,000**. This is the diversification hedge against the Georgia slot-revenue decline. [[raw/doug_update_jvl-march-23-2025.md]]

## System compatibility and Peach 1 (Mar 24, games/markets)

- On the Mar 24 markets call, Val noted the Georgia system providers include **Win Systems** and **Access**, both on the standard **SAS 6.0** protocol; JVL verified full **SAS compatibility** with the Georgia system a few weeks earlier — relevant because the same systems (or Access specifically) may appear in Nebraska/Puerto Rico. [[raw/games_markets-march-24-2025.md]]
- **Peach 1** revision / nudge-enhancement items were mostly closed and on track for completion by month-end (Michael reviewing). The Peach bonus is being reskinned with a corn-stalk theme for Nebraska (see [[wiki/projects/nebraska-skill-market.md]]). [[raw/games_markets-march-24-2025.md]]

## Peach 2 nudge-freeze and Peach 4 reskins (Mar 28)

- On the Mar 28 game-design review, **Peach 1** revision was awaiting Juan's review (he planned to go into the office the following Tuesday). **Peach 2** got a new **nudge animation-freeze** requirement — its games run particle animations on the frame border that clash with the nudge arrows, so all animation now freezes during a nudge event except the correct arrow; this makes **Peach 2 longer** but **Peach 3** should be back on track. See [[wiki/topics/slot-game-design-principles.md]]. [[raw/games_design_meeting-march-28-2025.md]]
- **Peach 4** remains **uncommitted / undeployed** — its games (**La Rosa**, **El Jaguar**, **5X Peppers**, **Cold Cash**) are the testbed for reskinning existing games (details on [[wiki/topics/jvl-machine-lineup.md]]). Games ship as **packs of six**. [[raw/games_design_meeting-march-28-2025.md]]

## FlexPay kiosk demo for GAMOA (Apr 18, planned as of Mar 27)

- On **April 18** [[wiki/people/felipe-miranda.md|Felipe]] is to demo the FlexPay kiosk **in a private room at a hotel** "for the Gamoa" (transcript rendering — the Georgia operators' audience; spelling unclear), a repeat of the show demo. The 3D-printed prototype kiosk in the Georgia office is to be discarded; newly assembled hardware ships from Toronto. See [[wiki/meetings/2025-03-27-flexpay-scope-gap-discovery.md]]. [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- **Date evolution (Apr 7–11):** later sources put the demonstration on **"the 17th" — "Next Thursday at 4 p.m."** (Apr 17 2025 was the Thursday; the Mar-27 "April 18" reading is taken as superseded/imprecise) — showing **one V43 machine with Diamond Link**. [[raw/flex_pay_tito_smib_port-april7-2025.md]] [[raw/evolution_flex_pay-april-11-2025.md]] Event scale per the Apr-8 recap: "not a trade show. This is just a Gamoa meeting, two hour thing," maybe ~10 masters; demo config = one Flex-S with FlexPort + bill acceptor + FlexPay on a TP-Link router, Diamond Link software, no competitor machine, no TITO shown. See [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- **Market friction (Apr 11):** GAMOA's **Mike Patel** told Felipe he "will not be buying our kiosk solution because if we offer pulse capture, it is not secure"; the team's rebuttal (Mother Goose is itself pulse-based; JVL keeps pulses inside the cabinet) is on [[wiki/topics/flexpay-business-architecture-payout-devices.md]]. Juan visits Georgia the week of ~Apr 14 to put the question to the masters directly. [[raw/evolution_flex_pay-april-11-2025.md]]

## Software-upgrade-kit pricing and financing (Apr 1)

- On an Apr 1 commercial call (Val, [[wiki/people/felipe-miranda.md|Felipe]], [[wiki/people/juan-martinez.md|Juan]], [[wiki/people/pavel.md|Pavel]], + an unnamed American commercial colleague), JVL decided to **charge for the COAM software-upgrade kits** (the "Peach"/PH1 enhanced software) for the **first time** — retail **~$2,900**, floor **~$2,500**. The kit adds a SAS port, printer integration, all games reworked with the nudge feature, and TITO/legislative compliance, effectively renewing an old cabinet. Full detail (cost basis, competitor comparison, financing strategy, and Val's 2026 kiosk-vacuum market-sizing) on [[wiki/decisions/2025-04-01-price-georgia-coam-upgrade-kits.md]]. [[raw/upgrade_ga-coam_kits-april-1-2025.md]]
- **Financing rule:** kits have a **~zero bill of material**, so JVL finances them generously (12–24 months, zero interest) — but only against **kiosk orders**, and only under a **signed installment contract** (repossession/service-suspension rights); third-party financing (to 5 years) goes through **Elevate**. This complements the Mar-23 financial-product note above (same ~6,000-installation, June-2026-deadline picture). [[raw/upgrade_ga-coam_kits-april-1-2025.md]]

## Open questions

- Was routing Jackpot Rush / JPRE for Georgia onto the **old framework** (curved cabinet) a deliberate plan or an oversight? Val said he didn't recall discussing it and parked it for a later meeting. [[raw/game_design_meeting_march_7_2025.md]]
- Why does the Bally iview final report disagree with the (correct) data JVL sends, and does the iview system need a protocol JVL can't currently select? [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- Will the third dedicated printer port become JVL's standard on all future machines? (Raised, not settled.) [[raw/Alignment_outstanding_subjects_2025-02-19.md]]

## Sources

- [[raw/Alignment_outstanding_subjects_2025-02-19.md]]
- [[raw/game_design_meeting_march_7_2025.md]]
- [[raw/developing_games_faster_michael_gottlieb_march_12-2025.md]]
- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/doug_update_jvl-march-23-2025.md]]
- [[raw/games_markets-march-24-2025.md]]
- [[raw/games_design_meeting-march-28-2025.md]]
- [[raw/flex_pay_scope_gap-mach-27-2025.md]]
- [[raw/flex_pay_tito_smib_port-april7-2025.md]]
- [[raw/flex_port_recap_felipe_juan_pavel-april-8-2025.md]]
- [[raw/evolution_flex_pay-april-11-2025.md]]
- [[raw/upgrade_ga-coam_kits-april-1-2025.md]]
