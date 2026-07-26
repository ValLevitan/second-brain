# Summary — Game Development Meeting (Feb 27, 2026)

**Participants:** Val Levitan, Michael Gottlieb, Lena Zhukova, Juan Martinez, Efim Podvoiski
**Duration:** 1h 14m 15s

---

## Nebraska — Top Priority (Cash-Critical)

Val declared Nebraska the **#1 priority** for the company, explaining that the current state is blocking sales and the ability to convert trials into revenue.

### Key Decisions

#### GC369 — New Primary Skill Feature ("Dual Box")
- **Replace** the power meter primary skill game entirely (no toggle/fallback — single solution going forward)
- New mechanic: overlay with two boxes, player chooses the "larger coin" — one box has a small dull coin, the other a large shiny coin with gold tracer; correct pick = 100% win, wrong = 0%
- Box placement (left/right) must be **random**, not fixed
- Inspired by Light and Wonder's approach in Nebraska; framed internally as a "new primary skill feature" (not an "update") — Val insisted on this language to avoid regulatory/legal exposure
- Michael renamed it from "primary skill game update" to **"primary skill feature"**
- **Schedule:** Concept by March 4, design by ~March 10-11, production by March 19, testing March 20-23

#### GC370 — Secondary Skill Trigger Button UI Update
- Make the "touch here to pattern match" button less prominent: reduce border, shrink font, change text color from white to a darker tone that blends into the background
- Straightforward — couple of days for Lena

#### GC372 — Liquid Glass for Nebraska: DELETED
- Unanimous decision to **remove this entirely** (not even backlog)
- Would take 30-60+ days, delay Georgia, and create a fork between Nebraska/Texas software
- Can revisit after Georgia ships (summer timeframe)

#### Submission Target: March 23 to Eclipse
- Val has a deal with Eclipse: 20% premium for 10-day turnaround
- Juan to give Eclipse advance notice of the upcoming submission

#### REQ-1010 Updated
- Juan removed the power meter on/off switch and added the random box-position statement

---

## Power Meter Removal — Rationale

A significant portion of the meeting was spent debating whether to keep the old power meter as a fallback option. The team concluded:

- **Val's position (adopted):** Maintaining two interfaces is unnecessary and taxing; the power meter has failed in the field; regulatory risk of the new approach is slim; even if challenged, the company would have 30-60 days to comply with an alternate solution
- **Juan's concern (acknowledged but overruled):** Keeping the power meter as a safety net in case regulators challenge the Light-and-Wonder-inspired approach; agreed it's "not a hill to die on"
- **Michael's observation:** Vanilla's similar power meter games are dead last in performance; JVL may be getting lumped in with Vanilla's poor reputation, making the power meter a distinct negative

---

## Game Concept Pipeline

| Item | Status |
|------|--------|
| **GC356 (Twin Bison abstract)** | Michael making good progress; symbol hierarchy focus with white bison variant in free spins |
| **GC366 (Lion's Riches abstract)** | Next after Twin Bison; includes pay table revision |
| **GC361 (in-game symbols)** | Lena has material ready for review next week |
| **GC360 (bonus)** | Not yet started |

## Games in Production

| Game | Status |
|------|--------|
| **Black Hills Kino** (IP 969986) | Near complete; help screens done, ball animation coming next build, audio created but not yet integrated |
| **Kukat Kino** (IP 985) | In production |
| **La Rosa** (IP 988) | Gun symbol animation approved (toned down to match hierarchy); fresh build sent to Michael |
| **Rodeo Spins** (IP 987) | Fresh build under review |
| **Line Switches** (IP 998) | Work started, not yet in build |
| **Dragon Pace** (IP 997) | In to-do |
| **Wild Gold** (IP 995) | In to-do |
| **SD Liquid Glass Home Screen** (IP 984) | In production |

## Design Stage

- **IP 1018 (Dragon Face update)** — Full design update in progress; Lena extending deadline by ~2 weeks due to Nebraska reprioritization

## Georgia Timeline

- **Hard deadline:** Viewable by 2nd week of August (annual gaming show)
- **Realistic completion:** June (Lena and Val agreed)
- Lab submission by end of May at latest (30-45 day approval cycle)

## 8-Pack Base Game Configuration (Georgia)

- 2 Jackpot Rush games + 2 Fiery Ice games + 4 Lines & Ways games (default enabled)
- 6 Lines & Ways titles total (operator can toggle); tiered pricing for 10- or 12-game packages
- Lion's Riches and Twin Bison will use a new condensed pay-table layout: symbol pay row + large character art on the vertical screen instead of full pay table display
- Game selection discussion pending (likely swap Bayou Riches for Lion's Riches, possibly Queen of Luxor for Twin Bison)

## Process / Tooling

- Lena + Clayton to test MCP/Claude automation on Tuesday: creating Jira issues from transcripts across different spaces (concept, design, production) and attaching images
- Efim needs a dedicated Jira IP for his math engine work — to discuss separately with Val
