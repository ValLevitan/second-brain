# Meeting Summary — Remote update architecture review, NOVA and Galaxy
**Date:** November 6, 2026, 9:03 AM – 10:24 AM Eastern
**Duration:** ~80 minutes
**Attendees:** Val Levitan (host), Pavel Frolov, Dzmitry Chudzinau, Alexander Biratko, Irina Shishko, Andrei Bosik
**Language:** Russian
**Raw transcript:** [[Meeting_Transcript_Remote_Update_Design_Schema_Component_Signing_and_Machine_Registration-November-6-2026]]

## Summary

**Purpose.** Follow-up to the October 30 remote-update meeting. Pavel presented a top-level design schema for remote updates in the new Galaxy/NOVA system (link posted in the meeting chat). The group questioned it, then agreed on next steps.

**Pavel's schema, end to end.**
- **CI/CD** builds each component on its own or a final ISO image. Every component we may want to update later goes to S3 storage with its checksum and a manifest.
- **Cloud Galaxy** keeps the compatibility map: which components belong to which products, with which checksums, and where they may be applied.
- **Update Manager** is the user interface. A person picks the machines (one or a fleet), the components or component sets, and a schedule (now, at night, or at the next idle). It also holds the rules on what may be installed: the compatibility matrix plus jurisdiction limits. Val: this is a big topic and implies an administrative web UI; not MVP 1, maybe not MVP 2 or 3, but the architecture cannot avoid it.
- **Validation and Signing** service. It signs the set of components on a machine so the machine can check at every boot, with or without internet, that nothing was replaced by a third party. If the check fails the machine goes to tilt. Pavel: at the first stage this can be a very simple service that holds the private key, takes input, encrypts it and returns the signature.
- **Delivery**: internet or LTE modem, or USB. A background process on the machine downloads the firmware.
- **Cabinet**: two platforms, x86 and RK35xx. Software lives in two slots. Slot A is active. For an update the current components are copied to slot B, the new ones are downloaded there, and after verification a quick command switches the slots; the next boot runs the new set.
- **Signature check**: old machines combined two partition checksums into one, encrypted it with the private key and stored it. New approach: sign every component separately (Linux system partition, local game server, progressive controller, printer module, bill acceptor module, and so on). During an update, after delivery and before the slot switch, the machine sends its list of new checksums to Validation and Signing, gets a signature back, writes it, and switches. On boot the local game server recomputes the checksums and compares them against the decrypted signature.

**Why not sign at CI (Dzmitry).** Pavel: at CI time we do not know which combination of components a machine will end up with. Dzmitry suggested asking CI/CD to build a new ISO instead of duplicating its job; Pavel: the point is to download one small component, not a whole image. Agreed wording: it is like releasing a new ISO that may never exist physically. Dzmitry also said the server side is small: the machine works autonomously after one signature.

**What is missing from the schema.**
- RIS. Val asked where RIS fits. Agreed: a new revision of RIS goes into the Cloud Galaxy box, together with machine registration (passports), jurisdictions and operators. Delivery channels stay internet/LTE or USB.
- Dzmitry: for a minimal MVP the Galaxy side has no machine registration service, so the server does not know which machines exist. He called it the cornerstone blocking topic.
- Updating components that do not touch games should leave RIS as is. New games may require decommissioning and commissioning. Irina: a certified LGS cannot be installed at will; it must be checked against the lab document.

**Certification (Andrei Bosik's question).**
- Bug fix in LGS only: the build takes the old components and rebuilds only LGS. Eclipse sees that nothing else changed, which should simplify submissions.
- Georgia: what matters at the SAS check is the BIN file (the data-center jar files combined), one of three checksums (OS, games, BIN). The ISO signature is not what they check.
- Florida / Seminole (GLI, Class 3): the lab signs a full component list. After a remote update the machine must show exactly that list, nothing extra and nothing missing. How it was delivered should not matter.
- Removing a game is a new ISO and a new certification. Proposal: verify the checksums of the new installed state; if it matches what went to the lab, the signature is the same.
- Dzmitry: Galaxy needs a software manager that knows checksums and jurisdiction rules (Florida strict, Georgia looser). Pavel: that is the Validation and Signing module; Dzmitry: probably two services together.

**Base image vs games (Andrei Bosik).** He proposed a console-and-cartridge split: base system image plus separate games. Alexander: we already split by modules for cheaper certification, but most jurisdictions still require a signature of the whole ISO. Pavel: the OS partition stays one piece of more than a gigabyte; it is tested once and not changed in parts.

**Component compatibility.** Dzmitry: each component carries a meta-description of its version and the versions it works with, so the server can build a matrix (this LGS works with this framework and this math; no downgrade). Val: is this not already in the data contracts? A hand-kept table ages fast. Pavel: the manifest should be a generated file based on data contracts and the autotests run at build time. Val: we will solve this.

**Design schema, not architecture.** Val: what we have is a design schema (Andrei Bosik's term) or a shared understanding; to start work we need use cases, then requirements and capabilities. Pavel: the Confluence page also has use cases (Russian and English), basic timing diagrams, and a table "what blocks the decision" with owners; Alexander: those are spikes. ADRs are in the remote-update branch of the integration repo, not yet merged to main, including ADRs for the integration repository itself.

**Machine registration owner.** Dzmitry asked to start the discussion on registering a new machine (passports, countries, jurisdictions, operators, ownership levels as in the old CMS). Val: write the use cases for how it will work, then see what can be moved from the old CMS; we lost our product owner (Juan) and nobody replaces him, so Val will organize the process himself. Val is recorded as owner of a separate line, "machine registration," in the table.

**Val's frustration.** Dzmitry said the Galaxy side cannot write capabilities without the registration sketch first. Val: not every Galaxy use case depends on registration; there are hundreds of use cases, and without them there are no acceptance criteria and no end-to-end tests. If code already exists, map the use cases back to it and find the gaps. Pavel: everyone agrees on the use-case approach, and nothing is written for Galaxy machines yet.

**Next step agreed.** Work on the Update Manager assuming registered machines, customers and countries already exist: which components exist and the structure of install permissions. Dzmitry listed the capabilities to describe: CI/CD build to S3; a software manager that reads S3 and compares releases; machine registration, then an update and communication service; Validation and Signing as a simple key-holder service. Irina: we cannot move without RIS; Val: RIS must be part of the description.

**LGS side (Alexander).** Keep history on update: back up before and after, support rollback. Pavel proposed a self-check of the new LGS on a temporary storage before switching slots. Alexander: the system does not know what is in slot B until it boots; better add it as an extra health-check step at the first boot from slot B, rolling back to slot A if it fails. Pavel agreed: not a background job, an extra health-check step at the slot switch.

**Follow-up session.** Saturday, November 7, 6:00–8:00 AM Eastern (2:00 PM Minsk). Pavel sends the invite under the NOVA/Galaxy name; Evgeny invited too. Alexander may not start at 6.

## Decisions Made

- **A new revision of RIS, machine registration (passports), jurisdictions and operators go into the Cloud Galaxy part of the schema; delivery channels are internet/LTE or USB** — (Val, Pavel, Dzmitry)
- **Every component is signed separately; the machine gets one signature from the server at update time and checks all components at every boot offline; mismatch means tilt** — Dzmitry's CI-signing alternative was discussed and set aside. (Pavel)
- **The OS partition stays one piece of over a gigabyte; it is not updated in parts** — (Pavel)
- **Val owns the machine registration use cases, as a separate line in the decisions table** — (Val)
- **Use cases first, then requirements and capabilities, then code; nothing exists yet for Galaxy machines** — (Val, Pavel)
- **The check of the new slot is an extra health-check step at the first boot from slot B with rollback to slot A, not a background self-check** — (Alexander, Pavel)
- **Follow-up working session Saturday, November 7, 6:00–8:00 AM Eastern** — (Val, Pavel)

## Undertakings

| # | Who | What | By When | Priority | Context |
|---|-----|------|---------|----------|---------|
| 1 | Val Levitan | Write the use cases for machine registration (passports) in Galaxy | TBD | High | Val took this on himself after Dzmitry called it blocking |
| 2 | Pavel Frolov | Send the invite for the Saturday Nov 7, 6:00–8:00 AM ET session; include Evgeny | Nov 6, 2026 | Normal | Alexander may not attend at 6 |
| 3 | Pavel Frolov | Add RIS, machine registration/passports and the other Galaxy pieces to the schema; add Val's "machine registration" line to the table | TBD | Normal | |
| 4 | All attendees | Read the Confluence design page (use cases, timing diagrams, decision-blocker table) and the ADRs in the remote-update branch | Nov 7, 2026 | Normal | Pavel asked everyone named to read before Saturday |
| 5 | Pavel Frolov, Dzmitry Chudzinau | Describe the Update Manager constraints, software manager, and Validation and Signing as capabilities | TBD | Normal | Next step agreed near the end |
| 6 | Alexander Biratko | Think through the LGS side: history and backup on update, rollback, health-check step on slot switch | TBD | Normal | |

## Open Questions

- Should the compatibility manifest be generated from data contracts and autotests, or kept as a structured description per component? (Val, Dzmitry, Pavel)
- Which MVP gets the Update Manager administrative UI and jurisdiction/operator rules? (Val, Dzmitry)
- What from the legacy CMS (countries, jurisdictions, operators, sale/participation ownership) moves to Galaxy? (Andrei Bosik, Pavel)
- Does the Georgia BIN-file checksum model also hold for strict Class 3 locations after remote updates? (Pavel thinks yes)

## Dispatch Log

---
*Processed from Teams transcript on November 6, 2026, 12:15 PM Eastern (scheduled meeting-watcher)*
*Source meeting: Remote update architecture review, NOVA and Galaxy*
