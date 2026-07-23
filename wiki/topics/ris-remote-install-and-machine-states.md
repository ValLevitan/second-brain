---
type: topic
title: RIS (remote install/setup system) and machine states
date: 2026-02-06
aliases: [RIS, remote install system, remote setup, RIS modernization, machine states, sold-machine RIS, RIS subscription, manual override screens, participation financed debt-free]
source-count: 3
open-questions: 2
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

## Dated timeline (RIS thread)

- **Apr 3 2025** — RIS ↔ Business Central licensing: license software **per operator by installation count**, enforced via the RIS manager reading BC invoice data; Georgia-first. [[wiki/decisions/2025-04-03-license-software-per-operator-not-machine.md]] [[raw/ris_business_central_integration-april-3-2025.md]]
- **Apr 24 2025** — first Omni release ships legacy setup screens **plus** the new **React-based remote/USB initial-setup screens** (the RIS "installation test" screen presents settings loaded from USB or remote). [[wiki/decisions/2025-04-24-omni-first-release-legacy-plus-remote-setup-screens.md]] [[raw/set_up_screen_omni-apr-24-2025.md]]
- **Feb 6 2026** — modernise RIS for the **sold-machine** world: three machine states, editable-per-screen flags (manual override), RIS-as-subscription, lock/unlock + override reporting — while keeping finance/jurisdiction control absolute. Undertaking: a **decision-flow diagram** of RIS across the states; follow-up Wed the 11th. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]

## Open questions

- How a **not-yet-JVL-customer new owner** gets any RIS benefit on a machine that has been off the floor for months, without JVL granting server access it does not want to grant (legal-liability concern) — discussed, not resolved. [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- Whether **participation** machines (Florida, Colombia) fit the invoice/licensing model — carried over unresolved from the Apr-3-2025 session. [[raw/ris_business_central_integration-april-3-2025.md]]

## Sources

- [[raw/RIS Modernization & Operator Flexibility Alignment.md]]
- [[raw/ris_business_central_integration-april-3-2025.md]]
- [[raw/set_up_screen_omni-apr-24-2025.md]]
