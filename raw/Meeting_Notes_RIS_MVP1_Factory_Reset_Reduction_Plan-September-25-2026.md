# Meeting Summary — RIS features follow-up: fewer factory resets
**Date:** September 25, 2026, 10:34 AM – 11:33 AM Eastern
**Duration:** About 58 minutes
**Segment:** 2 of 2
**Attendees:** Val Levitan (organizer, chair), Pavel Frolov, Irina Shishko, Felipe Miranda Giorgi
**Raw transcript:** [[Meeting_Transcript_RIS_MVP1_Factory_Reset_Reduction_Plan-September-25-2026]]

## Summary

Mostly English, with some parts in Russian. Speech recognition is poor in the Russian and mixed-language parts (about minutes 12–15, 30–37). Some points below come from those parts and are marked as unclear. Segment 1 (small talk) is here: [[Meeting_Notes_RIS_Pre_Meeting_Travel_Productivity_Chat-September-25-2026]]. Earlier related meeting: [[Meeting_Notes_RIS_Serial_Binding_and_Factory_Reset_Focus-September-24-2026]].

### Goal: "RIS rework MVP1 release"
- Val said the last meeting lost focus. He wants **one, two or three items** that remove **50–60% of the issues**. He called this the **"MVP1 release of the RIS rework."**
- The goal is **immediate relief** in the field. The biggest pain is that **almost everything needs a factory reset**. Val said this design fits use cases from 20 years ago, not today.
- If item #1 can be done fast, Val may put it into MVP1 or even into the **V3 release** with a quick re-approval. "Even if we can get it next week, OK."
- Val told Felipe that all of this is **"patching, not really fixing."** The real fix is **moving machines to a modem**.

### Pavel's numbered list (final version, near minute 37–41)
1. **Remove statistics from the RIS scan.** (Speech recognition unclear: "Remove statistics from scanning Lease.") Irina, in Russian, also said the RIS should carry only the needed data and no statistics.
2. **Remove the passport QR screen after factory reset.** Save the passport data and send it at the **next QR scan** (for example, when a technician visits to collect location statistics). Val added: or send it by **modem** when there is one. Val asked if passport (component exchange) changes can be handled without a hard reset; Pavel said the flag works on the fly with a reboot, but during factory reset the data must be applied and sent to the "serial" (as transcribed).
3. **Allow component changes inside the remote initial setup.** Example: the setup was made without a printer, but the location wants a printer. Pavel said this needs changes on the machine and also on the "serial" (as transcribed). Felipe asked for the same (manual printer / no printer change) to avoid another hard reset.
4. **Reuse the last applied RIS** after factory reset, if the same software version is still on the machine. Pavel thinks this fixes **more than 50% of cases** where a technician must go to the office, download the file, put it on a USB stick and come back. It does **not** remove decommissioning and commissioning.
5. **Investigate a "soft factory reset."** Idea: if the machine reboots 2–3 times with the same error, it does an **automatic soft reset**. It **keeps meters and game settings**, and clears game history and error state. Pavel said this looks **difficult** and needs investigation. Val's logic: tilt repeats after reboot → automatic soft (silent) reset → if that fails, show a final tilt → then hard reset. **Val: the silent reset must leave a record** (in setup mode, or sent by QR scan).
6. **Better messages when devices are not found** during install or boot. Today the message is a general "hardware not detected." Pavel will split it (for example counter board, IO board). Pavel said this is not very difficult.

Also discussed:
- **Error code 2 and 3 at boot** (Felipe: very frustrating for technicians). Pavel said it is in most cases the USB stick, and the message can be changed to say the data cannot be read from the USB stick. Pavel said there is no special USB stick brand or spec to buy.
- **IO board problems.** Felipe said the firmware from engineering was rolled out as widely as possible. He said Genadi suggested moving the IO board connection to another port, and this helps a lot (a hardware fix).
- Felipe listed which of the **8 use cases** need a hard reset now: use cases 1, 3, 4, 5, 6 and 8 (battery change, software crash, add/remove printer, and others). All of these could reinstall the same software version. He has a log of in-house repairs; most are hard resets for critical errors and software crashes. He has no log of phone/text support.
- Pavel and Felipe agreed: **clearing meters needs decommissioning** (the lottery must know). Felipe said he needs to confirm this.
- **Money transfer error:** Felipe said it happens mainly when the printer has the wrong firmware at first install; after correction there are no more problems.

### Release approach (not decided)
- **Scope: Flex machines only.** Felipe asked; Val confirmed. "Altera is done." Val said about 2,000–3,000 machines. Sebastian would help upgrade the machines in the field.
- Val first said the release would **not change games**; it only removes hard resets. Pavel said there are many software versions in the field, so the fix must go into each version or machines must move to the latest software.
- Val then compared **about 20 upgrades (20 approvals)** with **2 upgrades (2 approvals)**: one for **dual-screen** and one for **vertical**, bringing all machines to the latest version. Val said this would also change games, which may be a problem for some customers (Peach 1, Peach 2).
- **Felipe's concern:** earlier there were 5 new versions (3 dual, 2 vertical) with nudge and watchdog, and not everyone updated. Customers on **build 1919** complain little and have the **highest performance**. Getting everyone to upgrade will be hard.
- **Pavel:** for certification, the cheapest option is **one bundle with 18 games** in one package (Peach 1+2+3 for dual screen). Felipe said that would be ideal: technicians would carry one dongle instead of three. A new RIS is still needed the first time for the new version.
- Pavel said the software update can also add the **option to enable the modem**, even on old software. Felipe: "even if the boards are five years old."

### Modem connectivity
- Felipe asked about modem use in locations with bad signal. Val said yes, it is a concern (signal may be spotty, interference, weather). For a small number of bad locations, a **cellular amplifier (about $300)** could fix it, or the machine could be turned off.

### Felipe's idea: keep the RIS in the cabinet
- Felipe suggested the RIS could **stay inside the cabinet permanently** (like a USB stick or a Dallas chip) so it is never lost. Today the USB stick hangs on the cabinet side with an extender, but technicians remove it. Val said it may be "an interesting idea." Pavel said **updating** it would be harder than today. Felipe also sends settings to technicians by WhatsApp and gave them phone USB adapters.
- Felipe described how Aristocrat saves a machine setup on a USB stick and loads it on other machines. Val said this was a workaround, not the right way.

### Next step and roles
- Val said he cannot yet see clearly what must be done from Pavel's list. He wants another meeting to groom the ideas.
- **Felipe acts as product owner** (normally Juan's role; Juan was not present). Val explained: the product owner takes the spec from design out of engineering into the field, then hands it to a **product manager** — here **Sebastian** — who manages the product in the field.
- Process Val set: **use cases → capabilities → requirements with acceptance criteria**. Felipe hands the package to **Pavel**. Pavel assigns resources and negotiates features for each capability. Each **feature becomes a feature branch in GitHub**.

## Decisions Made

- **The RIS rework release covers Flex machines only, not Altera** — Altera is finished. (Decided by Val Levitan)
- **Felipe acts as product owner for the RIS rework** — Juan was not present; Felipe grooms the ideas into use cases, capabilities and requirements, then hands off to Pavel; Sebastian later manages it in the field as product manager. (Decided by Val Levitan)
- **Next meeting Monday, September 28, 2026, 10:00 AM Eastern, to review Felipe's use cases, capabilities and requirements** — Val could not yet see a clear plan from the list. (Decided by Val Levitan, agreed by Felipe)
- Considered and not settled: "no game changes, only the reset feature" versus "two upgrades (dual + vertical) to the latest version, which changes games." See Open Questions.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Felipe Miranda Giorgi | Groom everything said in the meeting into a short, compressed summary of needed changes, in ESL-style English; then write new positive use cases, break them into capabilities, and write requirements with acceptance criteria | Mon Sep 28, 2026, 10:00 AM | High | Acting as product owner |
| 2 | Felipe Miranda Giorgi | Send the meeting invitation for Monday Sep 28, 10:00 AM Eastern (Val, Pavel, Irina) | Before Mon Sep 28, 2026 | High | Val: "I'm expecting a meeting invitation" |
| 3 | Felipe Miranda Giorgi | Confirm whether clearing meters always needs decommissioning | TBD | Normal | Felipe: "I need to confirm, but I am pretty sure" |
| 4 | Val Levitan | Post the meeting transcript "here" (the meeting chat) | Sep 25, 2026 | Normal | Source for Felipe's grooming |
| 5 | Pavel Frolov | After Felipe's package: assign resources and negotiate features for each capability (each feature = GitHub feature branch) | TBD, after Sep 28 review | Normal | |
| 6 | Pavel Frolov | Investigate the soft factory reset idea (point 5) | TBD | Normal | Pavel: difficult, needs investigation [Needs Val's confirmation] |

## Open Questions

- **Release packaging:** fix each field version separately (about 20 upgrades and approvals) or move all Flex machines to the latest version with 2 upgrades (dual + vertical), or one 18-game bundle? Val raised; Felipe worried that build 1919 customers will not upgrade; Pavel favors one bundle for certification cost.
- **Game changes:** Val first said no game changes, later said the 2-upgrade approach changes games. Not resolved.
- **Which items go into MVP1 or V3**, and the time for each — Val asked for this at the start; no dates or percentages per item were given.
- **Modem coverage** in bad-signal locations (Felipe raised). Val suggested amplifiers; not settled.
- **Keeping the RIS inside the cabinet** (Felipe's idea). Val found it interesting; Pavel said updates are harder. Not settled.
- **Soft factory reset** is possible or not — needs Pavel's investigation.

## Dispatch Log

---
*Processed from Teams transcript on September 28, 2026 (meeting-watcher recovery sweep)*
*Source meeting: RIS features follow-up: fewer factory resets, Segment 2 of 2*
