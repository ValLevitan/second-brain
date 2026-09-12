# Meeting Summary — FLEX-Port v-next discussion
**Date:** September 7, 2026, 8:00–8:59 AM Eastern
**Duration:** ~57 minutes
**Attendees:** Andrei Klimovich (organiser), Val Levitan, Pavel Frolov, Dzmitry Chudzinau, Irina Shishko, Genadi Peari
**Raw transcript:** [[Meeting_Transcript_GACS_Expo_IQ_FlexPorts_and_Ewallet-September-7-2026]]

## Summary

Andrei walked the team through the setup he wants at the next show — GACS in Georgia on October 21 — using a Confluence page he had shared in chat. Val cut the preamble short and used the Bezos method: nobody had read the document, so read and argue it in the meeting. Val also insisted the setup is not a show exhibit. JVL is selling in Georgia right now, Flex-IQ plus ports plus Flex-Pay is the main solution, and the show is only a milestone with a hard date. Andrei agreed and said the setup reflects the team's current reading of what the market needs.

Three setups are planned: Flex-IQ with Flex-Ports operated by a cashier; Pay Slim (Val corrected the name from "Slim Pay"), a Flex-Pay slim configuration with bill acceptor, optical reader, card dispenser and TITO printer; and the recycler with one machine and one Flex-Port, probably on the Texas game software. Val moved the recycler discussion to a separate meeting.

The topology Andrei described puts Flex-IQ on the cashier counter with its own TITO printer, connected to gaming machines each fitted with a touchscreen Flex-Port, all on one router, with Flex-IQ acting as gateway to the cloud and wallet server. He drew a line between self-service solutions and cashier-attended ones; Flex-IQ is cashier-attended.

The most consequential moment was Val reversing his own earlier position. He had previously said Flex-IQ and MudaGoose could run in parallel on the same location. He now ruled that out: when JVL installs its equipment it is obliged to cannibalise MudaGoose, for business reasons and not technical ones. He said plainly that he had misled the team on this. Andrei accepted it and set the frame — by October 21 one topology only, Flex-IQ plus ports, no MudaGoose. If a location insists on keeping MudaGoose it stands as its own separate solution, and JVL will resist it, probably at contract level. Irina questioned how JVL can be "against" something a location wants. Val noted the practical consequence: JVL will have to run its own cabling or its own wireless network and push the incumbent's wiring out of the machine.

Dzmitry proposed a runtime mode switch so a terminal could be told remotely whether to run as MudaGoose or Flex-Port, switching screens, required devices and protocols on the fly. Andrei rejected that as wasted effort — set the mode at build time in the warehouse, and from late October simply stop installing MudaGoose builds. Pavel agreed it is easier to operate. Dzmitry's real concern was deleting functionality they might want again; Andrei was emphatic that nothing gets deleted, the current version is frozen as a separate product, and Pavel added that it should be tagged so everyone knows it was the August 2026 show build while main develops down the new path.

On e-wallet storage Dzmitry argued for creating wallets in the cloud rather than locally on the gateway, for security and for a single point of responsibility. Andrei pressed on what actually changes for security — copying, duplication, forging a wallet. Pavel noted that locally generated tickets carry a small collision risk across locations. Val ruled to stay local for now: JVL will release its own cloud server within about six months and move everything then, the risk is very small, installations will be few, and it is not worth loading anyone's head with it before the show. The accepted limit while local is that a wallet created at location A will never work at location B.

Irina raised the case that drove the next decision: a player who walks straight to a machine, plays, and wants to cash out with nothing in hand. The group concluded the e-wallet must be able to exist with a zero balance, which also turns it into the equivalent of an Aristocrat-style player card. Val challenged this hard and repeatedly — why allow play to start without a wallet at all? Pavel answered that it is not a technical limit, since the bill acceptor can be blocked over SAS, and argued that going through SAS is more reliable than wiring the acceptor to the port. So the question is strategy. Val's position was that if you allow it, it will always be that way, and if you disallow it once you teach the locations the right habit — but he said outright that he does not know which is right and is not insisting. Andrei pushed back that no card system on the market blocks the start of play, that it is the most sacred moment for a player, and that changing that habit so sharply is a bad idea. Val accepted there was serious thought in that. The zero-balance wallet stands.

Wallet lifetime becomes a per-location configurable parameter. Georgia locations typically give TITO tickets 30 days; Andrei saw no problem allowing 60 or 90, and noted the wallet could even be made immortal. The ticket design changes to say plainly that the player should keep it and come back tomorrow with the same ticket. No amounts are printed — the wallet is amount-agnostic.

Genadi asked how a player gets a wallet when there is no printer on the machine. The answer depends on the gateway: with Flex-IQ the cashier prints it on the attached printer and hands it over; with a self-service kiosk such as Pay Slim, the kiosk prints it. Genadi then made the improvement the group liked most — at collect, the Flex-Port sends a command over SAS so the ticket prints at the cashier's IQ printer, so the player does not have to leave a machine holding a win or shout across the room. Pavel shaped it: the cashout step is mandatory anyway, since the player is always asked to present a wallet to credit the win, and on that step you simply add a second button to print a new ticket with the winnings. Dzmitry framed it as a choice between scanning an existing wallet and printing a new one. Andrei approved. Val said the safest arrangement is still a printer on the machine itself, but the cashier-print option works because Georgia locations are small — about six machines on average — and Flex-Pay will stand near the machines.

Andrei noted this deepens the case for a Flex-Port with a touchscreen. Val said that was already decided: Flex-Port keeps the screen, the same design as today, cheapened only by reducing memory.

On printers, Val confirmed one TITO printer and one paper for everything — wallet tickets, receipts confirming card activation and transactions, and short regulator reports. If a report turns out to be long they will email it instead. Genadi challenged the use of a TITO ticket printer at all, since locations already have an ordinary roll printer and the TITO unit needs its own 24V supply and is a non-standard item. Pavel, Dzmitry and Val defended it: receipt paper is thin and semi-transparent, scans poorly, tears, curls out in a coil, and the print wears off, while a TITO ticket is wallet-sized like a hundred-dollar bill and carries its barcode down the sides in the safe zone so folding does not destroy it. The setup stays on one TITO printer. For the show, Val told Genadi to 3D-print the simplest possible enclosure for it and move on; Andrei noted that a competitor they saw on Friday shipped a badly 3D-printed case straight to production.

For Pay Slim the main open item is fitting the card dispenser into the slim chassis. The UI and flow overlap with Flex-IQ by roughly 80%. Genadi said the Slim itself is about two weeks out, the drawings will go in a day or two, which Val translated into drawings leaving Wednesday, the factory starting Monday, air freight, and about two weeks to Georgia.

Flex-IQ changes from card swipe to barcode scanning. The cashier and master PIN login stays as it is. Self-service has no cashier so no cashier PIN there; the player PIN is a separate block of changes. Receipts print automatically, and the PIN becomes a configurable parameter, off — Andrei asked that if it cannot be made configurable in time, its disabling be hard-coded for the show, since it only creates friction.

Val closed on timing. Talking about the show pushes everything into late October, and he is working to get installations in September. He needs the product now, whoever captures this market first will control it, and the team should park regular planned work and switch to overdrive. He needs Flex-IQ and Flex-Pay tomorrow. On resourcing, Pavel named Dima, Sergei, Anton Serёgin and Vladimir Samusenko, with the UI work at roughly a day, and said the main effort falls on Flex-Port. Irina asked who would own Flex-Port; Pavel said that was for the following meeting.

## Decisions Made

- **MudaGoose is cannibalised, not run in parallel** — no Flex-IQ plus MudaGoose installations, and from October 21 the only topology is Flex-IQ plus Flex-Ports. (Val Levitan, on business grounds, reversing his own earlier position)
- **Operating mode is set at build time in the warehouse, not switched at runtime** — Dzmitry's remote mode-switch proposal was not adopted. (Andrei Klimovich; Pavel Frolov agreed it is easier to operate)
- **Nothing is deleted** — the current MudaGoose implementation is tagged and frozen as a separate product version while main moves on. (Andrei Klimovich, Pavel Frolov)
- **E-wallets stay on the local gateway server for now** — JVL's own cloud server is expected within about six months, and everything moves then. (Val Levitan, over Dzmitry Chudzinau's cloud-first preference)
- **Accepted limit while local: a wallet created at location A will never be supported at location B.** (Andrei Klimovich)
- **The e-wallet must be able to exist with a zero balance** — this is what makes the whole flow work and makes it the equivalent of a player card. (Andrei Klimovich and the group; Val questioned it repeatedly but did not block it)
- **Blocking the start of play is a strategy question, not a technical limit** — the bill acceptor can be blocked over SAS. (Pavel Frolov)
- **Wallet lifetime is a per-location configurable parameter**, with about 30 days as the Georgia norm. (Andrei Klimovich)
- **Wallet tickets carry no amounts** — the wallet is amount-agnostic. (Andrei Klimovich, Pavel Frolov)
- **At cashout the player is always asked to present a wallet, with an added option to print a new ticket carrying the winnings**, printed at the cashier's IQ printer via a SAS command. (Genadi Peari proposed; Pavel Frolov shaped it; Andrei Klimovich approved)
- **One TITO printer and one paper for wallet tickets, receipts and short regulator reports**; long reports go by email. (Val Levitan)
- **The TITO ticket printer is kept over the ordinary roll printer** — receipt paper scans badly, tears, curls and wears off, and the TITO barcode sits in a fold-safe side zone. (Pavel Frolov, Dzmitry Chudzinau, Val Levitan, over Genadi Peari's challenge)
- **Flex-Port keeps its touchscreen** — same design as today, cheapened by reducing memory. (Val Levitan)
- **Flex-IQ moves from card swipe to barcode scanning; cashier and master PIN login is unchanged.** (Andrei Klimovich)
- **The PIN becomes a configurable parameter, set off**, with its disabling hard-coded for the show if configurability is not ready in time. (Andrei Klimovich; Val Levitan accepted, Pavel Frolov said it is not difficult)
- **The product is named Pay Slim (a Flex-Pay slim configuration), not Slim Pay.** (Val Levitan)
- **The recycler is moved to its own meeting.** (Val Levitan)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Klimovich | Rename "Slim Pay" to "Pay Slim" throughout the setup document | Sep 7, 2026 | Normal | Val corrected the name mid-call; Andrei said he was doing it |
| 2 | Genadi Peari | Send the drawings for mounting the card dispenser and printer in the Pay Slim slim chassis | Sep 9, 2026 | High | Val: drawings out Wednesday so the factory starts Monday |
| 3 | Genadi Peari | Deliver the first Pay Slim unit | ~Sep 21, 2026 | High | Genadi said about two weeks |
| 4 | Genadi Peari | 3D-print a simple enclosure for the TITO printer sitting beside Flex-IQ | TBD | Normal | Val: simplest possible, then move on |
| 5 | Pavel Frolov | Tag the current MudaGoose Flex-IQ implementation as the frozen August 2026 show version | TBD | Normal | So the team knows main has moved to the new path |
| 6 | Pavel Frolov | Settle who owns the Flex-Port work | Sep 7, 2026 | Normal | Deferred to the following meeting in answer to Irina |
| 7 | Val Levitan | Hold a separate meeting on the recycler | TBD | Normal | Pulled out of this agenda |

## Open Questions

- Whether to install on MudaGoose locations for a couple of months during the pilot while the new version is finished. Andrei asked directly; Val said he does not know and thinks it would only create confusion. Unresolved.
- Whether allowing play to start with a zero-balance wallet is the right strategy. Val said explicitly that he does not know the right answer and is not insisting either way; "life will tell" once it is a setting.
- Whether two gateway devices — Flex-IQ and a self-service kiosk — can work together on one location. Andrei flagged it as deserving its own discussion and the group assumed one gateway per location for now.
- Who owns Flex-Port development. Deferred to the next meeting.

## Dispatch Log

---
*Processed from Teams transcript on September 7, 2026*
*Source meeting: FLEX-Port v-next discussion*
