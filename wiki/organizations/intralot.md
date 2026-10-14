---
type: organization
title: Intralot (Georgia's central-system operator; route ambitions)
date: 2026-10-14
aliases: [Intralot, Intralot Georgia, Bally Intralot, the new Bally Intralot, intra lot, intraday, the interlod, Interlock, Intralock, Interlot, Interloch, Interlord, IntraLa, intro, Intro lap, Incelot, InfraLott, Intellicom, intralight, Intralot lab, Intralot site controller, the site controller, set controller, side controller, Intralot reports, Georgia central monitoring system, state monitoring system]
source-count: 9
open-commitments: 3
open-questions: 3
---

# Intralot

**Intralot runs the central monitoring system for Georgia's COAM machines.** Every JVL machine in Georgia reports to it, it holds the machine's primary SAS port, and it is the party that can disable a game [[raw/CMS- Block Diagram_Arch.md]]. Its only customer in Georgia is the [[wiki/organizations/georgia-lottery-corporation.md|Georgia Lottery]]: "**we only have one customer, the Georgia Lottery. Nobody else**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

Until October 2026 the corpus met Intralot only second-hand — as the source of reports JVL distrusts, as the host of the Lottery's test lab, and as the system behind the machine lock. On **October 13 2026** [[wiki/people/val-levitan.md|Val Levitan]] and [[wiki/people/felipe-miranda.md|Felipe Miranda]] met Intralot face to face for the first time, at its office in Duluth, Georgia — see [[wiki/meetings/2026-10-13-intralot-machine-lockouts-test-lab-and-route-partnership.md]]. Val: "**we never met. I was never here, and we've been doing business here for quite a while**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]] [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

**Name note.** Transcripts garble the name often: "Interlock", "Interlot", "intro", "Incelot", "Intellicom" and others (all kept as aliases). Each page that reads a garble as Intralot marks it as an inference. On Oct 13 the transcript also says "intraday" and "intra lot"; the notes read both as Intralot [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## People

- [[wiki/people/bill-avgeris.md|Bill (Avgeris)]] — the technical and operations contact JVL deals with at Intralot; on Sept 10 the Lottery said it has worked with "Bill at Interlock" (read as Intralot) "quite a bit" [[raw/Meeting_Transcript_Georgia_Lottery_Class_A_Guidance_and_Prize_Card_Compliance-September-10-2026.md]].
- [[wiki/people/christos-tzoumaras.md|Chris (taken to be Christos Tzoumaras)]] — an Intralot executive who set out Intralot's route plans to Val on Oct 13.
- A technical person (Plaud Speaker 7, not named) who spoke of an earlier investigation into a JVL lock case [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Shane** — per [[wiki/people/georgios-zazanis.md|George Zazanis]] of ARC, "**the operation manager here in Georgia**"; Val recalled him as "a guy in the meeting, not Greek" on Oct 13 [[raw/Meeting_Transcript_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]].
- **Petro** ("Kabilis", as transcribed) — per George, a tester who "**was the one that doing it**" [[raw/Meeting_Transcript_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]].
- **[[wiki/people/byron-booth.md|Byron]]** (surname Booth, from the ARC lunch) — per Chris, a board member at [[wiki/organizations/arc-gaming.md|ARC]] who "**was our CEO for years, and he was the lobbyist also for Intralot**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## Ownership and group (as Chris described it, Oct 13 2026)

- **Soo Kim, chairman of Bally's, bought Intralot** from the Greek owner (transcribed "Kokalis") and holds "**a sixty percent**" stake. Val said he had negotiated with Kokalis twenty years ago [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- The group: the Bally's casinos (outside Intralot, under Soo Kim); Intralot in lottery; **Bally's Interactive** (iGaming), already acquired; and a sports-betting group being acquired "**by the end of the year**" — "**It's William Hill, Triple Eight, and Mr. Green**" (the buyer's name is rendered "Evolve"; the notes suggest "Evoke?") [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]] [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **What is missing is the route business.** "**what is missing is the route business. We are going to make a very strong effort to get into the route business.**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]

## What Intralot does for JVL in Georgia

- **Central system and primary SAS.** Georgia mandated dual SAS on newer machines; "**primary SAS is reserved to Intralot. That's the state monitoring system. So they're the ones that can disable the game**" [[raw/CMS- Block Diagram_Arch.md]].
- **Reports.** Intralot reports "**mask our machine serial number with a state generated ID number that means nothing to us**" [[raw/CMS- Block Diagram_Arch.md]]. JVL has called them unreliable for most of 2026 — see [[wiki/topics/machine-data-repurchase-program.md]] and [[wiki/projects/georgia-market-rollout.md]].
- **The site controller.** At each location a site controller sits between the machines and Intralot. "**The set controller will disable the machines… As soon as it notices something**… Irregularities" (Bill, Oct 13; "set controller" = site controller). Felipe dates JVL's lock problem to the new site controller, "**It's been three years**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **The lab.** The Lottery hosts many prototypes at Intralot's lab, including an old JVL tabletop — [[wiki/decisions/2026-09-10-the-transactional-equipment-demonstration-goes-to-intralot.md]]. On Oct 13 Bill said the lab has **ten ports** [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Who may use the test environment.** Bill: "**Right now we are providing access to only the to the certification labs and the lottery**" — so access for JVL is a Lottery decision [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## Oct 13 2026 — the lockout meeting

Full meeting: [[wiki/meetings/2026-10-13-intralot-machine-lockouts-test-lab-and-route-partnership.md]]. The lock itself is on [[wiki/decisions/2026-10-12-build-4333-is-tested-in-the-office-on-the-sas-simulator-for-the-intralot-lock-unlock-problem.md]] (Oct-13 update).

- **What Intralot sees.** Bill: if two or three JVL machines are disabled, "**We consider it, you know, day - to - day operations**". Asked whether that is because Intralot does not see the lockout signal: "**We don't see the lockout**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **An earlier Intralot finding.** A technical person: "**the machine takes longer to respond to a signature request from the site controller, and that's what times it out**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Million-dollar payouts explained.** Bill: "**The million dollar is when people are ram clearing the machines without telling us**." The system reads it as a meter rollover; the amount "**is staying pending until we have corrected with the correct amount and authorized by the lottery, which is taking like two to three days**", and is not counted "**in the average or anywhere**". It happens to "**Any type of machine**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Decided:** ten JVL machines go into Intralot's lab now, and Intralot scans the whole field for JVL machines — [[wiki/decisions/2026-10-13-ten-jvl-machines-go-into-intralots-lab-now-without-waiting-for-the-lottery.md]]. Val's letter to the Lottery — [[wiki/decisions/2026-10-13-val-asks-the-lottery-in-one-letter-for-a-site-controller-or-testing-at-intralot.md]].
- **Transactional equipment is not Intralot's business.** Asked whether Flex-IQ, the kiosk and Flexport must be tested there: "**We don't connect with these gears. We have nothing to do**" (Chris), and "**That's all outside of the game**" (the Lottery representative) [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## Oct 13 2026 — Intralot's route plans, and a possible partnership

Chris spoke after the Lottery representative had left. He was clear it is not settled: "**Nothing is signed**"; "**Nothing is in contract finalised. This is conceptual.**" Val checked he was speaking for the company; Chris: "**I'm conveying what… will try to do in certain jurisdiction in the future**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

- **The idea: the lottery as route operator**, with lottery-branded machines in lottery locations. In Wyoming he wants to call them "**a lottery machine**", slot play on the front and "**Lottery law, mechanics, and regulation at the back**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Nebraska.** "**There are thirty operators there. We have the system with the lottery.**" Intralot may not be allowed to be the operator directly. He put the idea to the Nebraska Lottery and the Tax Commissioner, and "**the lottery says, 'Oh, I love this idea.'**" Of the lottery's "**2, 000 locations, maybe**", "**We pick 500**". He expects it "**in 2027**". See [[wiki/projects/nebraska-skill-market.md]] [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Ohio** — not with the lottery. If Ohio regulates ("**We think that the new governor will regulate. 2027. Yes, at the beginning**"), partner with a large Class A operator "**that has jukeboxes**… **1, 300 locations**". Bill expects Class B, "**But regulated**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Wyoming.** "**the lottery has five hundred locations in Wyoming. I want to get into two hundred.**" "**we have the lottery contract**". The director is "**John Claunch**", "**We are very close friends**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Idaho.** A legal pull-tab machine, because "**pull tabs are allowed are not slots**"; "**We already have the system that these pull tabs machines need to to connect to**". He told the new lottery director his lottery does "**426 million in revenues. Let's take it to the to the 650 level**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Also named:** "**Maybe Arkansas**", "**Puerto Rico, the Dominican, other routes**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **What he wants.** "**I need a partner for the route, and I need a partner for the machines.**" Terms are open: "**Maybe we decide we go revenue share everywhere. Maybe you want cap**", or Intralot taking "**equity on the manufacturer**". His board asked for 2027 specifically [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **A "full solution" for lotteries:** Intralot, "**this game manufacturer called JVL that has good software**", and a repair depot. He named **Renova**, a small Georgia shop that fixes Aristocrat equipment (the notes read it as bill acceptors), run by the owner's son **Luigi**, who joined the dinner that evening [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]] [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].
- **Georgia Class A.** Chris wants Class A to be regulated and do well in Georgia, so he can say to the Lottery "**Let's put the system now**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

**Val's answer.** "**we're trying to do the same thing.**" He said JVL has outside capital ready (a family office) and is building a budget street machine (see [[wiki/topics/low-cost-street-machine.md]]). "**I will happily participate with you in meetings**", and of Wyoming: "**I would love to operate in Wyoming**". On Nebraska he was frank: "**We have Nebraska license. We have Nebraska machines. But our machines have not been tested, have not been testing well. We're not making money.**" [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]

The talk was to go on at dinner that evening [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]].

## Oct 13 2026 (afternoon, in absentia) — how ARC's COO, an ex-Intralot man, says to work with Intralot

At the [[wiki/meetings/2026-10-13-arc-zazanis-lunch-trade-in-and-2027-volume.md|1:00 PM lunch]] the same day, [[wiki/people/val-levitan.md|Val]] told [[wiki/people/georgios-zazanis.md|George Zazanis]] of [[wiki/organizations/arc-gaming.md|ARC]], who used to work at Intralot ("**When I was at Intralot**"), about the morning. Everything below is George's view [[raw/Meeting_Transcript_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]].

- **The Lottery will not change.** Val had asked the Lottery's Chris for a site controller again and was refused. George: "**The revenue from the COAM business year after year goes up. So in the eyes of the state, they're doing great.**" When he was at Intralot he lost the same fight: "**I lost this battle many years ago.**" See [[wiki/people/chris-boncek.md]] (Oct 13, ARC lunch).
- **The lab test is not a special favour.** Val: "**today they agreed to allow Intralot to have my machines and to test my machines in house**". George: "**they do this for every manufacturer**"; Intralot's QA room holds "**every single machine**". It is convenience: easier than "**having you on the phone every other day**". What counts is GLI: "**As long as GLI approves it, then you don't have to do anything else**" (see [[wiki/organizations/gli.md]]).
- **His tip: ask for a Nebraska site controller.** Val: "**isn't it the same site controller?**" George: "**Exactly the same.**" "**In theory, yes**" it would work for Georgia, "**But the rules they are different**". Intralot runs Nebraska and ARC has "**zero presence in Nebraska**". George: "**You may say site controller for Nebraska, since you cannot give me one for Georgia.**" Val: "**You just gave me a good idea.**" See [[wiki/projects/nebraska-skill-market.md]].
- **Who decides in the Georgia lab: "Chris".** "**Chris is the guy… You don't need to go to 50 people… Chris will delegate the work. Let Chris bring Bill.**" Reading this Chris as [[wiki/people/christos-tzoumaras.md|Christos Tzoumaras]] and Bill as [[wiki/people/bill-avgeris.md|Bill Avgeris]] is an **inference**; the notes flag several Chrises as unclear [[raw/Meeting_Notes_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]].
- **Montana.** "**Intralot has the lottery there**" (George).

## History

- **2014.** "**Back in twenty fourteen, Intralot won the bid to become the central monitoring system**" (Billy Liu's account) [[raw/Meeting_Transcript_Billy_Liu_PlayPay_Georgia_Payment_Ecosystem_and_Float_Economics-September-15-2026.md]].
- **Mar 2025.** Juan understood Intralot "**may be in the running**" for Nebraska's planned central system [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]].
- **Jun 2025.** Nebraska's Intralot system had a go-live date of July 1, and its SAS was described as "**pretty much almost the same**" as Georgia's [[raw/eclipse_nebraska_testing_requirement_review-june-4-2025.md]].
- **Sept 10 2026.** The Georgia Lottery steered JVL's transactional demonstration to Intralot's lab — [[wiki/decisions/2026-09-10-the-transactional-equipment-demonstration-goes-to-intralot.md]].
- **Oct 5–12 2026.** Felipe raised the lock that strands machines, and JVL set a build test for it — [[wiki/decisions/2026-10-12-build-4333-is-tested-in-the-office-on-the-sas-simulator-for-the-intralot-lock-unlock-problem.md]].

## Open commitments

- [ ] Bill (Intralot) — investigate the JVL lock case and get back to JVL: "**We get the case. We will get back to you by Friday**" — due Fri Oct 16 2026 — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [ ] Intralot engineers — scan the whole field for JVL machines that lock or are disabled — due unspecified — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [ ] [[wiki/people/val-levitan.md|Val Levitan]] — ask Intralot (Bill / Chris) for a site controller for Nebraska, on George Zazanis's tip — due unspecified ("So I will ask Bill") — [[raw/Meeting_Transcript_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]]

## Open questions

- Why do JVL machines lock — a site-controller signal, a timing issue, or the machine itself? Val: "**I don't know whether my machine locks up on its own or whether your controller sends a signal to lock it up**" — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- JVL says many cases, Intralot sees two or three. Is the gap because Intralot does not see the lockout? Chris: "**it's more than what is reported… to us**" — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- Will JVL and Intralot partner on routes — which states, revenue share, cap or equity, and when? Nothing is signed — [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]

**§15.8:** clear — company and market figures only; no named-person compensation. **Personal matters:** not recorded. Gossip about a third party's finances was not recorded.

## Sources

- [[raw/Meeting_Transcript_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]]
- [[raw/Meeting_Notes_ARC_Gaming_Zazanis_Lunch_Trade_In_and_2027_Volume-October-13-2026.md]]
- [[raw/Meeting_Transcript_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [[raw/Meeting_Notes_Intralot_Machine_Lockouts_Test_Lab_and_Route_Partnership-October-13-2026.md]]
- [[raw/CMS- Block Diagram_Arch.md]]
- [[raw/Meeting_Transcript_Billy_Liu_PlayPay_Georgia_Payment_Ecosystem_and_Float_Economics-September-15-2026.md]]
- [[raw/Application_Nudge_Skill_for_Nebraska_2025-03-14.md]]
- [[raw/eclipse_nebraska_testing_requirement_review-june-4-2025.md]]
- [[raw/Meeting_Transcript_Georgia_Lottery_Class_A_Guidance_and_Prize_Card_Compliance-September-10-2026.md]]
