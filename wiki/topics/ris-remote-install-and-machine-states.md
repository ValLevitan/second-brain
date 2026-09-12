---
type: topic
title: RIS (remote install/setup system) and machine states
date: 2026-02-06
aliases: [RIS, component allow-listing, validator swap fraud, remote initial setup, remote install system, remote setup, RIS modernization, machine states, sold-machine RIS, RIS subscription, manual override screens, participation financed debt-free]
source-count: 6
open-questions: 3
---

# RIS (remote install/setup system) and machine states

**RIS** is JVL's system for **installing and configuring the settings on a gaming machine** — pushing the correct screen values (progressive settings, RTP/bet buttons, payout order, devices, SAS/system, denomination, game selection) onto a machine from a **USB stick or a remote connection**, instead of a technician entering 30–40 pages of settings by hand. Each issued RIS carries its own **unique number**, distinct from the software version [[raw/ris_business_central_integration-april-3-2025.md]]. This page synthesises what RIS is, how JVL uses it to keep control of machines it sells, and the **Feb-6-2026 direction** to modernise it for sold machines.

*(Naming note: some staging labels call RIS a "reporting/integration system"; the sources consistently describe it as the machine **install/setup** system — that is what is recorded here.)*

## Why RIS matters to the business

- RIS lets JVL install several machines very fast — Juan cited **four to six machines in as little as 30 minutes** in South Dakota / Nebraska, versus competitors who deliver a machine and leave technicians to enter data "page after page." [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- RIS is also JVL's **control point**. JVL wanted to control the firmware and what goes inside its machines to prevent field abuses Val has seen over 45 years of operating — e.g. Latin-American technicians swapping a brand-new bill acceptor out of a JVL machine for a used one, or a crew that "doesn't care which product goes where" as long as the machine stays on the floor. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- Licensing/enforcement sits on top of RIS: JVL licenses **software to an operator by a count of installations** (per-seat / concurrent-install), not to a specific machine, enforced through the **RIS manager fed by Business Central invoice data** — see [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]]. [[raw/ris_business_central_integration-april-3-2025.md]]

## The problem Feb-6-2026 opens

The current RIS was "designed with the requirements of the past" — mainly **profit-sharing (participation) machines in locations**. That is no longer the only case: JVL now **sells** machines. The existing 80/20-rule participation logic is fine and Val does not want to touch it; what needs new requirements is the **sold-machine** case, where the new owner ("the new ideologist / operator") may run the machine however they like and JVL's forced restrictions may be resented, rejected, or actively worked around. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Proposed direction (Val's "ideology," not yet a locked decision)

- **Three machine states** instead of the current participation-vs-sold flag: **participation**, **financed** (sold but still owed money — Val also floated "lease"), and **debt-free purchase** (sold and fully paid). Val wants a clean taxonomy rather than "faking the intent" the way Nebraska is handled today (a machine put in participation and later moved to sold once paid). The **participation RIS stays as-is** — a good product he does not want to dilute. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Manual *override*, not manual *entry*.** Pavel argued a full manual mode (entering every screen by hand) would be a very large project; the cheap path is to keep using the **same RIS screens** but **enable editing on specific fields per case** (e.g. progressive value, RTP per game, which devices/games are installed). Val and Pavel converged on a **flexible flag marking which screens are editable and which are locked** — quite a bit more achievable than full manual mode. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **RIS as a paid subscription (business idea Val floated).** When a machine is fully paid, JVL could **disable RIS and turn the machine to manual-only**, then **charge the operator a recurring fee** to keep RIS/server access as a positive feature; if the operator stops paying, RIS becomes unenforceable and every allowable screen is manually editable. A legitimate operator may also simply decline RIS and enter fields manually. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Lock/unlock feature (onus on the operator).** Once a machine is sold and fully paid, allowable screens open for editing; but the operator can choose to **lock screens from editing for a set period (up to ~180 days)** and, staying registered on JVL's server, **scan the machine to see whether any screens were overridden** — a control service the operator opts into on a recurring calendar. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Controls that cannot be sacrificed (Val, explicit)

- **Roll-back to restrictions must remain possible** — engineering must not treat "sold" as "no more restrictions ever," because JVL may need to re-assert jurisdiction control (example: a machine sold into loose-jurisdiction Puerto Rico must not come back to the US mainland). [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Finance control is absolute.** JVL frequently finances the machines; **until it is paid, JVL keeps every restriction it needs** ("please don't mix freedom with owing us money"). Val wants **tighter, less-manual control over the owing-money case** — check Business Central: if the balance for that serial number is **zero**, then (and only then) allow the move to a long lease, possibly automatically — rather than relying on someone (his example: Mery messaging Dima) manually granting a 99-year lease as a favour, which "could be a critical mistake." [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Approved software only.** In every US jurisdiction there is a regulator; only approved software can be installed. Software selection stays RIS-pushed and is **out of scope for phase one** — no messing with software/game-theme selection yet. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Juan's field constraints (why flexibility is needed now)

- **Regulated-jurisdiction timing (Florida game conversion).** For a linked progressive, Juan cannot burn the RIS USB two days ahead (the Gaming Commission wants the software 24–48h early for a GLI/Kobetron certification check) because the casino only turns the machines off the night before / morning of; today Sebastian waits in the parking lot to burn the RIS the morning of. Juan wants the ability to **push defaults down and manually override certain fields on site**, with **secure fields (progressive contribution) settable once, then locked** — changing them again forces a full **factory reset** that alerts supervisors and the Commission. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Grey-market resale reality.** Used machines come off the floor, sit in a container/warehouse for months untouched, and are bought to be set up manually wherever they land (the IGT model — no manufacturer help). JVL wants its machines to be resaleable the same way, so a new owner who is **not a JVL customer** can set the machine up **manually** without JVL giving them server access (which Juan warned would make JVL **legally liable** for enabling a machine in an invalid jurisdiction). [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Reinitialisation anchor (engineering)

- Pavel: if a sold machine's **RAM is cleared**, it needs the RIS previously used on it re-applied to keep operating. Val pressed for an **irrevocable reference number that survives a RAM wipe**; Pavel confirmed today that ID relates to the **Dallas one-wire "cube" that holds the passport information** on the CPU board. The restore can only ever return the machine to **the last state JVL officially sold it at**. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## July 8 2026 — RIS personas and a field-editable RIS

By July 2026 the RIS **code had been reverse-engineered into human-readable requirements**, which surfaced five "personas" (role archetypes, not real people) — the actors the RIS redesign must serve. Two same-day working sessions worked through them: [[wiki/people/val-levitan.md|Val]] with [[wiki/people/juan-martinez.md|Juan]] first ([[wiki/meetings/2026-07-08-ris-persona-clarity.md|2:45 PM]]), then Val with [[wiki/people/pavel.md|Pavel]] and [[wiki/people/irina-shishko.md|Irina]] ([[wiki/meetings/2026-07-08-ris-persona-roles-engineering-review.md|3:46 PM]]). The full persona framework (the five roles, their renames, and the operator-side additions) lives on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (July-8 section); the RIS-specific design points are here.

- **RIS stays, but becomes field-editable.** A key design intent: keep RIS because it makes installation fast, but allow the configuration to be **tweaked in the field after install** — which cannot be done today. This is the same "manual *override*, not manual *entry*" direction opened Feb-6-2026 (editable-per-screen flags), now attached to the persona work. (Juan, endorsed by Val.) [[raw/Meeting_Notes_RIS_Persona_Clarity-July-8-2026.md]]
- **The reverse-engineering produced only 22, too-coarse requirements.** Because the RIS code ties whole pages to one person, the 22 requirements bundle too much; Val wants each split into five or more finer, singular requirements. The redesign method: first document how RIS works today, then use that gap analysis to design new personas → requirements → features → code. [[raw/Meeting_Notes_RIS_Persona_Clarity-July-8-2026.md]]
- **The field workflow the redesign enables.** Persona 5 builds the **immovable frame** (the absolute limits no one can cross); Persona 1 — a JVL role renamed **"Production Personnel"** — prepares the machine and sets default modes before the operator takes it; if the master operator does not want those modes, someone under him reconfigures the machine as the operator wishes and releases it that way; location personnel have only **limited capabilities at the site**. Market-specific limits (e.g. different values for Georgia, Nebraska, Texas) are set by Persona 4 but only within Persona 5's frame. [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]
- **New operator-side roles mean new front-end work.** Three of the personas — **master operator, operator administrator (renamed "Operator Production Supervisor"), and location personnel** — sit on the operator's side, outside JVL. These are roles JVL never had, so the RIS rebuild needs new capabilities and front-end screens written for them; Pavel and Irina are to write those once the personas are settled. [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]
- **An undecided control point.** Val flagged it as still open whether **location personnel (and tips) can influence a machine's configuration**, or whether selling a machine hands full control to the operator. [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]

## Dated timeline (RIS thread)

- **Apr 3 2025** — RIS ↔ Business Central licensing: license software **per operator by installation count**, enforced via the RIS manager reading BC invoice data; Georgia-first. [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]] [[raw/ris_business_central_integration-april-3-2025.md]]
- **Apr 24 2025** — first Omni release ships legacy setup screens **plus** the new **React-based remote/USB initial-setup screens** (the RIS "installation test" screen presents settings loaded from USB or remote). [[wiki/decisions/2025-04-24-omni-first-release-legacy-plus-remote-setup-screens.md]] [[raw/set_up_screen_omni-apr-24-2025.md]]
- **Feb 6 2026** — modernise RIS for the **sold-machine** world: three machine states, editable-per-screen flags (manual override), RIS-as-subscription, lock/unlock + override reporting — while keeping finance/jurisdiction control absolute. Undertaking: a **decision-flow diagram** of RIS across the states; follow-up Wed the 11th. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- **Jul 8 2026** — the RIS code, reverse-engineered into requirements, surfaced **five personas**; two same-day sessions clarified and refined them (with three new operator-side roles) and confirmed the direction to keep RIS but make it **field-editable** after install. The 22 reverse-engineered requirements were judged too coarse (split each into 5+). Full persona framework on [[wiki/topics/persona-driven-design-and-orchestration-platform.md]] (July-8). [[raw/Meeting_Notes_RIS_Persona_Clarity-July-8-2026.md]] [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]

## Sept 2 2026 — the customer-facing rationale for component locking, and the first offer to switch it off

The [[wiki/meetings/2026-09-02-lucky-coin-service-and-upgrade-offer.md|Sept-2 Lucky Coin visit]] is the only place in the corpus where Val explains **to an operator** why JVL's machines require a reset when hardware changes — and it is the first time he offers to remove the control on request [[raw/Meeting_Transcript_Lucky_Coin_Service_and_Upgrade_Offer-September-2-2026.md]].

- **The reason is validator-swap fraud, learned as an operator.** "**I'll tell you why we require [a] reset**, and you tell me if you don't need this feature. **We require [a] reset when we restrict certain things.** For example, we don't want certain bill acceptors installed on our machines. We don't want certain bill acceptors to be replaced on our machines, **and that comes from my experience being an operator**." The mechanism: "if I install a brand new validator on the machine and I put it on my route, and I have a **disgruntled technician**… he will take my validator, **sell it on the side, and replace it with the used validator**. That was **prevalent in Latin America**."
- **So the machine is trained, not just configured.** "we **allow and disallow certain changes, allow and disallow certain components**. For that reason, we build [a] **remote initial setup structure that guides the machine, trains the machine a certain way** — how we want to build it."
- **He named the cost of it in the same breath.** "then, if I want to quickly swap a validator, and you, as the business owner, set it up not to allow it — **well, it's inconvenient for the technician**."
- **The question he says it really poses is the operator's, not JVL's.** "**How should a business be run? Should I have serialized inventory control, or should I not? Should I have inventory control by brand, or should I not? Should I have a twenty-five cents bet on the machine, or should I not?** So certain locations do, certain locations [do] not. **All of this could be set through remote initial setup, and now downloaded through a mo[dem]**."
- **And his own account of why the fight happens at all:** "we just sometimes [are] not getting the decision maker, the operator who really makes a decision in the business, to listen to us. **That creates a lot of inconveniences. We can remove all of this, but in the long run, I'm not sure that we are servicing the business correctly.**" He put it as an open dilemma: "**On one hand, we're pushing it forward. On [the] other hand, we're saying, should we not do that and just be like everybody else? I don't have an answer.**"
- **The offer, made on the spot, when the customer said he had never suffered the fraud:** "**Then you don't need that feature, and we should remove it.** Then we should remove it." He attached a counter-offer rather than an argument: "**I will just report your acceptance rate to you on your validators. You'll be surprised.**" (That data offer is on [[wiki/topics/machine-data-repurchase-program.md]].)

**Why it matters to this page:** RIS is documented here mostly as an internal control problem — jurisdictions, finance, resale. This source shows the control being **negotiated with the customer as a product option**, per location, which none of the earlier sessions contemplates. It is also the operator-side cost of the same lock-down: the **decommission / re-flash / recommission** cycle that made this customer's service complaint (see [[wiki/organizations/lucky-coin.md]]), and which Val committed to reduce without a date.

## Open questions

- How a **not-yet-JVL-customer new owner** gets any RIS benefit on a machine that has been off the floor for months, without JVL granting server access it does not want to grant (legal-liability concern) — discussed, not resolved. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- Whether **participation** machines (Florida, Colombia) fit the invoice/licensing model — carried over unresolved from the Apr-3-2025 session. [[raw/ris_business_central_integration-april-3-2025.md]]
- Whether **location personnel** (and tips) can influence a sold machine's RIS configuration, or whether full control passes to the operator once the machine is sold — flagged undecided Jul-8-2026. [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]

## Sources

- [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
- [[raw/Meeting_Notes_RIS_Persona_Clarity-July-8-2026.md]]
- [[raw/Meeting_Notes_RIS_Persona_Roles_Engineering_Review-July-8-2026.md]]
- [[raw/Meeting_Transcript_Lucky_Coin_Service_and_Upgrade_Offer-September-2-2026.md]]
