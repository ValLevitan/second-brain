---
type: decision
title: First NOVA product = South Dakota VLT-2 (owner ruling, 2026-09-01) — supersedes the Aug-14 "South Dakota Vertical 01 first" sequencing
date: 2026-09-01
aliases: [first NOVA product, South Dakota VLT 3, VLT3 vs VLT-2, first Nova release, SD VLT-2 first on NOVA, South Dakota VLT-2 first NOVA product, NOVA release sequencing ruling]
source-count: 4
status: active
open-commitments: 0
open-questions: 0
---

# First NOVA product = South Dakota VLT-2 (owner ruling, 2026-09-01)

**This is an owner ruling, not a meeting decision.** Val ruled directly on 1 September 2026, answering the question the wiki had queued as LIVE OPEN #29 after he reopened it himself on the [[wiki/meetings/2026-08-26-alignment-planning-nova-september-releases.md|Aug-26 alignment call]]. Per §16 an owner correction is its own citation — there is no `[[raw/…]]` source for this page and none should be fabricated.

<!-- owner note -->
Asked "which product is first on NOVA, and does the ~Nov-1 certification target still stand?", Val answered: **"SD VLT-2"**.
<!-- /owner note -->

## What was ruled

- **The first product on NOVA is South Dakota VLT-2** — the direct Rage→NOVA migration track, not the South Dakota **Vertical 01** named in the [[wiki/decisions/2026-08-14-first-nova-product-south-dakota-vertical.md|Aug-14 sequencing decision]].
- This selects **track (a)** of the two parallel candidates Val put forward on Aug-26. Track (b) — a new Georgia COAM version on NOVA built on **D27, explicitly not vertical** — was not chosen as first; the ruling does not say it is abandoned, only that it is not the first release.

## What this supersedes, and what still stands

**Superseded:** the titular claim of the Aug-14 decision, that the first NOVA product is **South Dakota Vertical 01 (~March 2027)**. That page has been retitled and its status annotated so its headline is not read as current state.

**Still standing from Aug-14** (untouched by this ruling): Nebraska D2702 stays on Rage and releases toward end-2026; Georgia's V3 stays on the current platform for the Sept-1 target with NOVA as a later "V4-like" Georgia release; [[wiki/people/lena.md|Lena Zhukova]] builds NOVA games in parallel while the platform matures; South Dakota Vertical still needs three brand-new games (Solar Keno, Aaron's Pub, Dakota Bison) built rather than converted. The Aug-26 ownership and timing decisions also stand — see [[wiki/decisions/2026-08-26-pavel-irina-own-nova-capabilities-to-jira-through-september.md]] (capabilities → MVP → Jira through September, developers onto NOVA ~Oct 1).

## Why this is coherent with the recent engineering work

The migration experiments through August ran **horizontal-to-horizontal on the South Dakota product**, not on the vertical machine — Val explicitly directed that on Aug-18. The [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] demonstrated exactly that path working on real maths. Choosing South Dakota VLT-2 as the first NOVA product therefore lands on the track the team has actually been proving out, rather than on the vertical product that still needs three new games built from scratch. *(This paragraph is the wiki's inference from the recorded meeting sources, labelled as inference — Val's ruling itself gives no rationale.)*

## Certification — ruled the same day (owner, 2026-09-01)

<!-- owner note -->
Asked whether the ~Nov-1 GLI target still stands and whether Calle Ocho is still the certification vehicle, Val answered: **"no more"** (Calle Ocho), and **"GLI still stands for September 1st, although it is being delayed by two days."** Asked to separate the two GLI items, he clarified: **"September first is the current schedule for RAGE-based SD-VLT-2 submission (not for NOVA). There is no date for NOVA yet."**
<!-- /owner note -->

**These are two different submissions. Do not conflate them.**

- **RAGE-based South Dakota VLT-2 → GLI: planned September 1 2026; slipped ~2 days in execution, actual ≈ September 3 2026.** This is a **RAGE** submission on the current platform — it is *not* a NOVA submission. The owner was explicit that the slip changes nothing structural: *"the schedule simply slipped, which happens from time to time. The original schedule should not be changed, but the factual date should be acknowledged."* So the **plan of record stays September 1** and the **actual (~Sept 3) is recorded beside it**, never over it. (Owner ruling 2026-09-01.)
- **NOVA → GLI: there is NO date yet.** The owner stated this plainly. The [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug-18]] target of "first NOVA platform version to GLI by ~Nov 1" (which Val called "the plan, not yet a hardened schedule" even then) is **no longer a current date**. Nothing replaces it — the correct current state is *unscheduled*. Do not infer a NOVA GLI date from the September-1 RAGE date. (Owner ruling 2026-09-01.)
- **Georgia V3 → Eclipse: planned September 1 2026; slipped to September 15 2026** (owner, 2026-09-05: *"Eclipse slipped further to September 15th."*). This is the **other** Sept-1 item recorded on the [[wiki/meetings/2026-08-18-rage-nova-migration-experiment-review.md|Aug-18 call]] — Georgia V3 with 15 games + the LTE modem, going to the **Eclipse** lab, not GLI. Same plan-vs-actual handling: **plan of record stays September 1**, revised actual **September 15** recorded beside it. Note the two Sept-1 items have now moved differently — GLI/South Dakota VLT-2 by ~2 days (≈ Sept 3), Eclipse/Georgia V3 by two weeks (Sept 15).
- **Calle Ocho is NO LONGER the GLI certification vehicle.** The [[wiki/decisions/2026-08-14-first-nova-product-south-dakota-vertical.md|Aug-14 decision]] had named Calle Ocho — already running on NOVA — as the game to submit to GLI to certify the platform, aiming at approval ~January. That is dead. The [[wiki/decisions/2026-08-03-no-en-masse-rage-to-nova-migration.md|Aug-3]] ruling not to finish or certify standalone Calle Ocho is the consistent earlier signal. (Owner ruling 2026-09-01.)

**Plan vs actual — the general principle the owner stated here.** A schedule slip is not a decision change. Keep the planned date as the plan of record and record the actual date beside it; do not rewrite a plan because delivery moved by a couple of days. (Owner ruling 2026-09-01.)

## Sept 4 2026 — corroborated in the game-development meeting, and NO NOVA GLI date was set

The [[wiki/meetings/2026-09-04-naming-convention-standards-and-nova-conversion.md|Sept-4 afternoon game-development meeting]] (English) is the first source in which the product team itself states the Rage→NOVA cut-over, and it matches this ruling. **These are sources, not owner rulings**; the ruling above stands unchanged [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]:

- **Nebraska is the last release on Rage; everything after it is NOVA.** Val: "my understanding that South, South… no, hold on… **Nebraska is the last stage, the last release for OnRage**." Michael: "Correct. Everything is basically **everything is Nova from here on out**." Val: "Yes, yes, correct."
- **The next South Dakota VLT release is the NOVA one.** Val: "**South Dakota VLT. The next… South Dakota VLT is… a nov[a]**"; Lena: "start in January, South Dakota will be No[va]." Tentative start of the conversion is **October 1** — "starting 1st of October, tentatively, we're planning for a conversion of **South Dakota VLT from RAGE to… Nova**" — with Lena noting it starts a little later in practice because developers are on Nebraska in October, and she will do all the design screens for South Dakota Real Keno meanwhile.
- **Conversion has been tested on two games and both went smoothly.** Val: "we've tested automatic conversion from Rage to Nova… we've tested **two games**. [O]ne to vertical and one to from **dual screen to dual screen**. And in both cases, it went very smoothly. I think Ke[no] will be easier, to be honest with you. But this is my own **professional opinion**." Michael's plan: start by converting the best-performing titles already in South Dakota D2703 and "use those as our test bed."
- **C43 Curve is a NOVA product** — "C43 Nova will be introduced at the Georgia show. It'll be developed in Nova" (Michael). See [[wiki/decisions/2026-09-04-d27-discontinued-curve-c43-premium-line.md]].
- **The regulator question was raised — and NO NOVA certification date was set.** Juan: "just from a compliance standpoint, **do we want to deal with GLI and Nova this early? Or should Eclipse get Nova first** to help us troubleshoot anything?" Val declined the premise rather than naming a date: "**Eclipse doesn't test anything. Eclipse only tests us**… they're not traversing in any depth through anything that we're doing. **They're testing SAS.** So it's nothing." His reason for confidence was the development and testing ecosystem being built — "I'm going to give you… an incredible development environment… I'm going to set up an incredible testing ecosystem around this. And even if we make an error in anything, it will be much easier for me to find it, to fix it permanently. So, hands down, **we're ready**." **No date for a NOVA submission to GLI appears anywhere in this source.** The owner ruling above — *NOVA → GLI is unscheduled* — is unaffected, and the Oct-1/January dates here are **development** dates, not certification dates. Do not convert them into a GLI date.
- **One related product constraint confirmed the same day:** JVL is **not** moving to 4K resolution. Lena asked twice; Val: "No, we're not moving. There's absolutely zero reason right now to move to 4K… There's 0 benefit."

## Sept 11 2026 — checked again in the game team's own meeting: still no NOVA GLI date, and a version-number mismatch surfaces

The [[wiki/meetings/2026-09-11-rage-sunset-and-class-a-on-nova.md|Sept-11 1:00 PM game-development call]] is the next source in which the product team plans NOVA releases out loud. **These are sources, not owner rulings**; the ruling above stands unchanged [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]:

- **GLI is not mentioned once in either source of that meeting.** No NOVA certification date is set, proposed or implied. **NOVA → GLI remains unscheduled**, exactly as ruled on 2026-09-01. The Class A goal discussed there — **February 1** [2027 — year inferred] — is a **product delivery** goal, not a certification date, and must not be converted into one. See [[wiki/decisions/2026-09-11-georgia-class-a-v43-is-built-on-nova-not-rage.md]]. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **The Sept-1 RAGE submission is not mentioned either**, so nothing in this source disturbs the plan-of-record-September-1 / actual-≈-September-3 handling above.
- **The first NOVA release is restated as South Dakota, dual screen**, consistent with this ruling and with Sept-4: [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], "**we finished up NAD D2702 and then South Dakota D2703, which is our first Nova release**"; [[wiki/people/lena.md|Lena Zhukova]], "**our first release [i]n No[va] was scheduled for dual screen.**" [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **But the room calls that product "South Dakota VLT 3", not VLT-2.** Lena: "**we are planning on 1st Nova is South Dakota V[LT]3**" and "**IP 1180, it's for South Dakota VLT 3, which will be designed in Nova**"; Val used the same term back to her. **Recorded, not resolved** — the owner's ruling names the first NOVA product **South Dakota VLT-2**, and this source names it VLT 3. Two readings are possible (same product, different digit; or genuinely successive releases), and the wiki asserts neither. The full note is on [[wiki/projects/south-dakota-vlt-market.md]] (Sept 11, 1:00 PM). **Queued for the owner.** [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- **A second RAGE South Dakota track is confirmed dead**, which is consistent with everything above: Michael, "**One's the Nova D27 and the other one's the Rage V43, which we just recently decided we're not going to pursue**", with its games migrating into the D27 NOVA product. [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

## Carry-forward

- Acknowledge the **~2-day slip on the September-1 RAGE-based SD VLT-2 GLI submission (actual ≈ Sept 3 2026)** in the next weekly update — owner's explicit instruction, 2026-09-01. *(Written for the Friday 4 September 2026 run, which did not fire; carries forward to whichever run happens next.)*
- **NOVA has no GLI date.** Watch for one being set; until then the wiki must say *unscheduled*, not carry the lapsed ~Nov-1 figure. *(Checked again against the Sept-4 2026 sources: the question was asked in the room and Val answered with readiness, not a date. Checked again against the Sept-11 2026 1:00 PM sources: GLI is not mentioned at all. Still unscheduled.)*

## Sources
- [[raw/Meeting_Transcript_Naming_Convention_Standards_and_Nova_Conversion-September-4-2026.md]]
- [[raw/Meeting_Notes_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]
- [[raw/Meeting_Transcript_Rage_Sunset_and_Class_A_on_Nova-September-11-2026.md]]

*(The owner rulings above carry no `[[raw/…]]` source and none should be fabricated — §16. The sources listed here back only the Sept-4 and Sept-11 corroboration sections.)*
