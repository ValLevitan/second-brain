---
type: decision
title: Minimal touchscreen fix in Rage now; affirmative touch deferred to Omni
date: 2025-03-19
aliases: [touch fix decision, affirmative touch deferral]
source-count: 1
status: active
---

# Minimal touchscreen fix in Rage now; affirmative touch deferred to Omni (≈Mar 19 2025 — date inferred)

**Decided:** in the current **Rage** framework ("Rage Studio") JVL makes only the low-effort touchscreen fixes — the active **perimeter around each button is narrowed** and the **denomination buttons are shifted left** (both already done, tested by "Ира") — while **affirmative touch** (press-duration validation, swipe-vs-tap discrimination via coordinate change) becomes a **technical requirement for the Omni framework**, because in Rage it would mean modifying the event loop/engine ("довольно сложно" per Anton's write-up, and swipe/tap take roughly the same milliseconds). The customer requirement is simply "reliable touch"; everything deeper is a technical requirement for Omni. [[raw/products_puerto_rico_touch_fix.md]]

**Also resolved on the call:**
- Swapping the VDEC's buttons and emitters (to raise the elbow-rest dead zone) is a **no-go** for now; Val will ask Lena what she settled with the producer/product owner ("Хуан и Майкл" — [[wiki/people/juan-martinez.md|Juan]] and [[wiki/people/michael-gottlieb.md|Michael]]). [[raw/products_puerto_rico_touch_fix.md]]
- The darkened-screen state must **time out back to the normal VDEC** when a player cashes out — called a scope gap/misinterpretation of scope, to be fixed in GQAM **and all other releases**. [[raw/products_puerto_rico_touch_fix.md]]
- **Undertaking for Lena:** narrow the button perimeters on **every game** to the pattern she made for GQAM (each product has its own VDEC, so per-product changes). [[raw/products_puerto_rico_touch_fix.md]]
- **Val's ideas parked for the producer/product-owner:** a "lock my favourite button" mode where a player can make one bright active button and dim the rest. [[raw/products_puerto_rico_touch_fix.md]]

**By:** Val, with Anton (touch experiments — context fits [[wiki/people/anton-leshkevich.md|Anton Leshkevich]]), [[wiki/people/pavel.md|Pavel Frolov]] (system side: an X.org-driver rewrite judged "серьезный проект," too heavy), [[wiki/people/genadi-peari.md|Genadi Peari]]. [[raw/products_puerto_rico_touch_fix.md]]

**Follow-on (Omni architecture):** Val put on the agenda (~mid-April) a full **Omni driver-architecture review** — list of all drivers, block diagram, and the third-party driver/library update-support policy — for Pavel to own with Alexander ("Бератко" — [[wiki/people/alexander-biratka.md|Alexander Biratka]]) and Anton, after the current releases ship. [[raw/products_puerto_rico_touch_fix.md]]

## Sources

- [[raw/products_puerto_rico_touch_fix.md]]
