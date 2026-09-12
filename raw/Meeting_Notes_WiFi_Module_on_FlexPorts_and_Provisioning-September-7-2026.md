# Meeting Summary — Wifi_Ports_IQ_Pay
**Date:** September 7, 2026, 9:08–9:55 AM Eastern
**Duration:** ~47 minutes
**Attendees:** Val Levitan (organiser), Evgeniy Alekseev, Andrei Bosik, Pavel Frolov, Genadi Peari, Andrei Klimovich
**Raw transcript:** [[Meeting_Transcript_WiFi_Module_on_FlexPorts_and_Provisioning-September-7-2026]]

## Summary

Val opened by asking whether a reliable wireless link is possible for Flex-Ports, so JVL does not have to run cable at every location. Evgeniy Alekseev said yes: add a Wi-Fi module to the Flex-Port and replace the current wired-only router with a Wi-Fi router.

Val's worry, which Pavel put into words, is that Wi-Fi is easy to flood — a cheap jammer saturates the channels and the whole network drops. Andrei Bosik confirmed such devices exist and will fill the entire 2.4 GHz band, but argued the attacker has to be physically inside the premises, so it is not a realistic threat, and asked who would bother. Val accepted the logic, with the fallback that if a location does get jammed they will run cable there.

Evgeniy laid out the options. On hardware, an external module versus a module soldered onto the Flex-Port board — the board option is much cheaper and simpler, roughly $4–5 per board. On software, either use the module's standard firmware, which needs nothing written because it works over AT commands on a UART and the existing WebSocket channel is simply duplicated (one wired, one Wi-Fi — Evgeniy thought Claude could probably do it), or write their own mesh firmware, which needs an MQTT-style server on an access point and takes considerably longer. Val rejected mesh outright: he understands its advantages in theory but it is for larger locations, and extenders or amplifiers will do, especially since modern extenders support mesh anyway.

The access-point question produced the one reversal of the meeting. Andrei Bosik asked whether to use a commercial router or make one of JVL's own devices the access point, and preferred the latter; Pavel pointed out that the RK3568 in Flex-IQ and Flex-Pay already carries the module. Val initially agreed — do not spend money on a router — then withdrew it himself, saying he had given a dumb idea and said it without thinking. Evgeniy and Genadi both argued the router is about reliability rather than cost: the IQ chip is weak, with only one or two antennas, and doing without a router means writing router functionality yourself. Genadi put it plainly, that removing the router is not a saving. The external commercial router stays.

Andrei Klimovich then settled the topology: the router can sit hidden somewhere in the gaming area, near the ceiling for safety, with Flex-IQ talking to it over Wi-Fi and all the Flex-Ports talking to it over Wi-Fi too. Val added that wires remain wires — where there is somewhere to plug in, JVL will run cable, will test it, and it must work. Andrei Klimovich also asked about a limit on how many machines can connect; Andrei Bosik answered that since the router is a third-party device the only limit is the router's own.

Antennas were the least settled topic. Evgeniy preferred a module with its own onboard antenna and said he has built four devices that way, including one inside a fully closed metal box, with no problems. Val pushed back hard: a module with its own antenna never works, he has stepped on that rake every time an engineer assured him it would. Pavel backed Val — the Flex-Port sits in a huge metal enclosure with only a small plastic piece protruding. Genadi pointed out the Flex-Port protrudes outside the machine and has a large plastic bezel with a perimeter an antenna could be routed around. Evgeniy's constraint is regulatory, not physical: modules are certified together with specific antenna types, so you cannot fit your own antenna and keep certification, and once a module is soldered with its internal antenna you cannot switch later. Genadi asked for an optional socket for a certified external antenna to be fitted anyway; Evgeniy said the pinouts are the same so either could be soldered, possibly both, but did not commit. Pavel and Genadi did confirm the whole front panel is covered by a plastic housing, so there is no radio problem in that direction.

Board space came up as a real constraint. Genadi suggested dropping a flash bank, then asked whether Flex-Port needs two serial connectors. The answer was no — one is enough, which frees both space and a UART for the Wi-Fi module. Genadi noted the printer UART is free in this variant since there is no printer, and that he has already sent the SAS arrangement.

Pavel designed the provisioning flow. Flex-Pay gets a screen to search for networks, pick one and enter the password; it then generates a QR code which is scanned by each Flex-Port so they all join the same network, avoiding password-entry screens on the Flex-Port itself. All three device types carry QR readers. Pavel was specific that it must not be the plain phone-style network-sharing QR, which hands over SSID and password in clear text — the password has to be encrypted in the QR and decrypted on the Flex-Port. Andrei Klimovich approved.

Val attached a requirement to that flow: capture and send home the time, date and location of who connected what and when, along with the serial numbers of the ports that were connected and what was installed where. He wants it as engineering and onboarding information. Pavel said it is not difficult since device logging already reaches the cloud logging server through Grafana and a section can be added. Andrei Bosik raised the offline case — if there is no internet at the moment of connection, the event has to be stored and forwarded later. Pavel agreed and said that part will not come free.

Val's other standing requirement was diagnostics. Every JVL device with a display or lamps must visually show what it sees: Flex-Pay shows its own view, Flex-IQ its own, Flex-Port its own, each seeing its neighbours. He called it culture, and a requirement rather than a nice-to-have. Andrei Klimovich clarified the shape — an operational dashboard the operator can log into showing signal quality per item — and Val agreed, adding a service mode on the device itself for when someone walks up to it.

Router brands became a geopolitical question. Val requires American routers because Chinese ones will be banned in the US in due course. Andrei Bosik offered Cisco, and noted Linksys is Cisco's home and small-office sub-brand at roughly half the price. Nokia (Finnish) and MikroTik (Lithuania, so EU) were both acceptable to Val. Bosik added that some routers carry a QR sticker that could be scanned instead of typing SSID and password, though he was not sure which manufacturers do it.

Val then turned to process, and this is where the assignment happened. His rule: if it is not written up in Jira, there is no work. A lot has to be specified and handed out, and too much of it currently sits on Pavel. Val asked whether it could go to Dmitri Kovalchuk, Andrei Klimovich and Andrei Bosik, then named Andrei Bosik as the driver — write the capabilities, break them into features, take it all under his control, start today, and set the pace, talking directly to the people in this meeting. Val's framing was that since he needs it tomorrow, Bosik should have started yesterday, and that he is not driving a car but a tank that has to go through walls. Bosik accepted. When Evgeniy later suggested simply amending the existing Jira ticket to say a module should be added, Val refused flatly and repeatedly — he wants it written up properly with responsibility attached.

On what the capabilities must contain, Val was specific: mostly non-functional requirements — self-diagnostics, drop-off and reconnection when the signal is lost, two-way handshakes, and a heartbeat so the device always knows it is on the network — each carrying requirements with single-line acceptance criteria so automated end-to-end tests can be written. Evgeniy said most of this already exists in the WebSocket protocol, and Bosik agreed it is largely the same as what was done for Ethernet. Val's instruction was to ask Claude to find those existing requirements and attach them to the capabilities, because without them there can be no automated tests and everything gets unpicked by hand afterwards.

Val also told Evgeniy that when he commits code he must put two things beside it: prose and a data contract. Pavel explained the standard on Val's request — the repository has a `docs` directory, inside it a `contracts` directory holding a Claude-generated markdown file describing what the artifact built from that repository offers other modules, for instance how it talks to Flex-Pay and over which API. Evgeniy said it has already been written. Val added that the prose must connect to acceptance criteria, and Andrei Bosik undertook to call Evgeniy after the meeting and set him up on Claude Code.

Evgeniy closed with a request he has made before: emulators and a virtual test system — virtual Flex-Pay, virtual gaming machine, virtual Flex-Port, bill validator, IQ — because to test Wi-Fi today he has to redeploy all the hardware from scratch. Val said Pavel is about half way there; Pavel said he has some groundwork but is not confident it is ready to hand over, and will talk to Sasha Biratko and Dzmitry Chudzinau about what can be stood up quickly. Evgeniy said he can write the gaming-machine emulator himself; what he actually needs is someone to write the Flex-Pay side. On hardware, Evgeniy will produce the new board configuration with Genadi and tell him what to add; on software he put the standard-firmware route at a couple of weeks maximum, noted there are no boards yet, and offered a temporary mock-up in the meantime.

## Decisions Made

- **Wi-Fi goes onto the Flex-Port board as a soldered module** at roughly $4–5 per board, rather than an external module. (Evgeniy Alekseev — cheaper and simpler)
- **Mesh networking is rejected** — standard Wi-Fi with extenders or amplifiers where reach is short. (Val Levitan; mesh suits larger locations, and modern extenders support it anyway)
- **An external commercial router stays as the access point** rather than making a JVL device the AP — Val withdrew his own suggestion to save the router cost. (Evgeniy Alekseev, Genadi Peari: reliability, not economy)
- **Router sits hidden in the gaming area; Flex-IQ and all Flex-Ports connect to it over Wi-Fi.** (Andrei Klimovich)
- **Wired connection stays supported and must be tested** — Wi-Fi does not replace cable. (Val Levitan)
- **Routers must be American or allied-country brands** — Cisco/Linksys, Nokia, MikroTik — because Chinese routers are expected to be banned in the US. (Val Levitan)
- **A certified antenna must be used**, since certification covers the module and antenna together and a soldered internal antenna cannot be switched later. (Evgeniy Alekseev)
- **Flex-Port drops to one serial connector**, freeing board space and a UART for the Wi-Fi module. (Genadi Peari, Pavel Frolov)
- **Wi-Fi provisioning by encrypted QR** — credentials entered once on Flex-Pay, then a generated QR is scanned by each Flex-Port; the password must be encrypted in the QR, not shared in clear text. (Pavel Frolov; Andrei Klimovich approved)
- **Connection and installation telemetry is captured and sent to JVL's server** — time, date, location, port serial numbers, what was installed where — and buffered when there is no internet. (Val Levitan; Pavel Frolov to extend the existing cloud logging)
- **Every JVL device with a display or lamps shows what it sees**, surfaced both in an operator dashboard with per-item signal quality and in a service mode on the device. (Val Levitan, shape clarified by Andrei Klimovich)
- **Andrei Bosik is the driver for this work** — writes the capabilities, breaks them into features, sets the pace and coordinates the group, starting today. (Val Levitan)
- **Work does not exist unless written up in Jira**, and the existing ticket is not to be amended to cover this. (Val Levitan, refusing Evgeniy Alekseev's suggestion)
- **Capabilities must carry the non-functional requirements** — self-diagnostics, reconnect on drop, two-way handshake, heartbeat — each with acceptance criteria so end-to-end tests can be automated. (Val Levitan)
- **Evgeniy Alekseev's code ships with prose and a data contract** in `docs/contracts` per the standard. (Val Levitan; Pavel Frolov explained the standard)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Andrei Bosik | Write the Wi-Fi capabilities, break them into features in Jira, own the pace and coordinate with this group | Start Sep 7, 2026 | High | Val: "since I need it tomorrow, you should have started yesterday" |
| 2 | Andrei Bosik | Ask Claude to find the existing non-functional requirements in the WebSocket protocol — handshake, heartbeat, reconnect, diagnostics — and attach them to the capabilities | TBD | High | Without them there can be no automated tests |
| 3 | Andrei Bosik | Call Evgeniy Alekseev today and set him up on Claude Code | Sep 7, 2026 | Normal | So Evgeniy can generate prose alongside his code |
| 4 | Evgeniy Alekseev | Produce the new Flex-Port board configuration with the Wi-Fi module and tell Genadi what to add | Before the large board order | High | Genadi asked for it to go in before ordering the big quantity |
| 5 | Evgeniy Alekseev | Implement the Wi-Fi link on Flex-Port using the module's standard firmware, duplicating the WebSocket channel | ~2 weeks max | High | No boards yet; temporary mock-up offered sooner |
| 6 | Genadi Peari | Provide board space and an optional socket for a certified external antenna within the Flex-Port plastic perimeter | TBD | Normal | Not fully agreed with Evgeniy — see Open Questions |
| 7 | Pavel Frolov | Build the Wi-Fi provisioning screens on Flex-Pay and Flex-IQ and the encrypted-QR handoff to the Flex-Ports | TBD | High | Includes diagnostic screens |
| 8 | Pavel Frolov | Extend the cloud logging to record connection and installation telemetry, including offline buffering | TBD | Normal | Grafana pipeline already exists; offline case needs work |
| 9 | Pavel Frolov | Talk to Sasha Biratko and Dzmitry Chudzinau about standing up a Flex-Pay emulator / virtual test system quickly | TBD | Normal | Evgeniy can write the machine emulator himself |
| 10 | Pavel Frolov | Verify the Flex-IQ side of the Wi-Fi work | TBD | Normal | Val asked him to take responsibility for checking it |

## Open Questions

- Whether a module's internal antenna can coexist with an optional external certified antenna on the same board. Evgeniy said the pinouts look the same and "possibly both" could be fitted, but would not commit; certification is the binding constraint.
- Which router manufacturers ship a scannable QR sticker for provisioning. Andrei Bosik raised it and said honestly he was not sure.
- Whether Pavel's existing emulator groundwork is fit to hand over. Pavel said he is not sure it is ready.

## Dispatch Log

---
*Processed from Teams transcript on September 7, 2026*
*Source meeting: Wifi_Ports_IQ_Pay*
