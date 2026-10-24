# Meeting Summary — chat by the coffee machine
**Date:** October 23, 2026, 11:02 AM – 12:04 PM Eastern
**Duration:** about 62 min
**Attendees:** Val Levitan, Pavel Frolov, Irina Shishko, Andrei Bosik
**Raw transcript:** [[Meeting_Transcript_Technician_Loyalty_and_Developers_as_Product_Owners-October-23-2026]]

Informal coffee chat, held in Russian. Some words and names are garbled in the transcript.

## Summary

**Current work (Pavel).** The team is finishing Flex-Port work and discussing MVP-1 and MVP-2. Pavel wrote a workflow document for an automatic voice assistant that calls the regulator to arrange decommissioning and commissioning, and sent it to Andrei Bosik. Today he also drafted, with Claude, a diagnostic tool for the stager.

**Why Georgia sales are hard (Val).** Two years ago the worry was that JVL games paid less than the competition. Some fixes were right (for example the skill feature rework). Val gave numbers: JVL average RTP in the last release is about 95.5%; competitors run about 90–92%. By his count JVL machines need about 40% more play to make the same money, which he called impossible. Pavel added that players stay longer on JVL machines but do not bet more.

**The real problem: technicians.** Val's new view: the operators' technicians have learned to hate the JVL machine. Commissioning with the lottery (Intralot) takes from half an hour to two hours, and JVL needs a factory reset and re-commissioning far more often than others, because of the RIS and passport design. Val does not want to drop RIS/passport, only design it right. The technician tells the owner "do not buy this again", and the owner listens. So the technician is the person JVL must satisfy.

**Plan.** First step: the lighter RIS release in November. Then keep giving technicians tools that make work on JVL machines easier. Ideas raised:
- Machine self-diagnostics that tells the tech what part to order, with a QR code on screen (Val).
- Watch SSD health (SMART) and ship a replacement disk early; a disk swap needs no re-commissioning (Pavel).
- Track bill validator reject rate per machine (for example 5% → 15% → 30%) and act on it (Val).
- Send messages to the technician's phone, timed to where he is; do not flood him with reports (Val).
- With a modem in the machines, collect many metrics and analyse them with AI (Andrei, Pavel).

Pavel said the key is to remove re-commissioning from every case that does not need it (for example printer change). Irina said the bill validator and printer are what force a factory reset today.

**Setup lock when money is on the machine.** Irina said this checkbox was added long ago against casino technicians changing progressives on a live machine. Today most risky settings (games, show mode, progressives, denominations) can no longer be changed in setup anyway, so the lock may be out of date and now blocks safe changes (device with SAS, limits). Progressives must stay locked. Val did not want to answer now. Not decided.

**Cloud maintenance window (Andrei).** Cloud services need about 25–30 minutes of maintenance once a month (Amazon updates). Val said do it at night, 2–4 AM Eastern (morning in Minsk). Andrei said that was his plan.

**Developers as product owners (Val).** Val thinks the classic programmer role is ending: developers now direct Claude or many agents and become product owners. Pavel and Andrei said hand-made agents are less needed now, because Claude picks its own helpers; Val said the point stands. Irina asked who coordinates if each developer is a product owner; Val's answer: a "council of product owners", one per project, meeting at the start of each product. Val wants to bring developers (he named several, names garbled) into early problem talks, as he now does with Andrei Klimovich. Pavel thinks they will gladly take more responsibility.

**AI cost and speed.** Andrei: speed and quality went up a lot (example: Galaxy, the cloud system for Flex devices, built by two people). Val: most companies do not work this way; Minsk now costs JVL about 25% more. Irina: autotests took about 3 weeks instead of a half year or more.

**Other.** Tomorrow (Saturday) there is a meeting at 3:00; Irina asked if Igor agreed, Val thinks yes. Korecky's agent works (built on Andrei's base, works in Teams). Val described a friend's insurance company that sells by phone with an AI voice agent that sounds human.

## Decisions Made

- **Goal for Georgia: win back technicians by making their work on JVL machines easier** — technicians' opinion drives owners' buying. First step is the lighter RIS release in November. (Val)
- **Monthly cloud maintenance runs at night, 2–4 AM Eastern** — lowest machine load. (Val, agreed by Andrei Bosik)
- **Considered, not decided:** remove or reduce the setup lock when money is on the machine. Val did not decide.

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | All Minsk team | Think as a technician and propose tools/features that would make JVL machines easier to service | TBD | Normal | Val's open invitation; collect comments and ideas |
| 2 | Andrei Bosik | Review Pavel's workflow document for the voice assistant that arranges de/commissioning | TBD | Normal | Pavel sent it yesterday |
| 3 | Andrei Bosik | Schedule monthly cloud maintenance (~30 min) at 2–4 AM Eastern | TBD | Normal | Amazon updates |
| 4 | Irina Shishko | [Needs Val's confirmation] Go carefully through all setup settings blocked by the "money on machine" lock | TBD | Normal | Irina said this still needs a careful pass |

## Open Questions

- Keep, reduce or remove the setup lock when money is on the machine? (Irina; Pavel suggested checking the GLI spec; Irina said it is not a GLI rule)
- Will developers accept the "product owner" title, or see it as a step down? (Val)
- Did Igor confirm tomorrow's 3:00 meeting? (Irina)

## Dispatch Log

---
*Processed from Teams transcript on 2026-10-23 14:10 ET*
*Source meeting: chat by the coffee machine*
