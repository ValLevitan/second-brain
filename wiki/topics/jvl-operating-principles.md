---
type: topic
title: JVL operating principles (the JVL Constitution)
date: 2026-07-13
aliases: [JVL Constitution, machines should not break, useless emotions, I will fix it but cannot commit to a date, Ways JVL Constitution, operating principles, governing principles, hypothetical vs factual, factual data doctrine, dollars not discounts, AI flattery guardrail, selling doctrine, 43 years experience, it worked here it doesn't work there, work preventively, there are no weekends, call don't write, my goal is to change your mind, you cannot insult me, nothing changed from 1984, a salesperson should leave the moment the deal is reached, designing to your spec, you'll shine it's your achievement, being the first is not always the best, I'm step one]
source-count: 26
---

# JVL operating principles (the JVL Constitution)

The **JVL Constitution** is the group's foundational governance document — it states what JVL is, how it operates, and the principles behind every decision made in its name. It is version 1.1, last updated 2026-03-16, owned by Val Levitan as President; all other JVL "Ways" operate within it, and it is the fallback when they are silent. (source: JVL Constitution — ~/Projects/Constitution/)

## What JVL is

- JVL is a **gaming technology company**: it builds and operates gaming machines (EGMs), develops software platforms, manages a distributed international workforce, and holds commercial real estate as a **secondary** activity. (source: JVL Constitution — ~/Projects/Constitution/)
- It operates as a group of related entities that share leadership, standards, and operating principles. The Constitution names **JVL Systems Inc., JVL Labs Inc., JVL Gameworks Inc., and JVL Mobi México** as those entities. (source: JVL Constitution — ~/Projects/Constitution/) (The fuller ownership tree — eight entities — is on [[wiki/organizations/jvl.md]].)
- JVL is a **small company and deliberately does not behave like a large one**: every process, document, and decision is judged against "is this necessary?" (source: JVL Constitution — ~/Projects/Constitution/)

## Governing principles

Stated as operational rules, not aspirations: (source: JVL Constitution — ~/Projects/Constitution/)

- **Produce only what is necessary** — anything removable without causing a real problem is removed.
- **One source of truth** — every piece of information lives in exactly one place and is referenced, never duplicated.
- **AI drafts, people decide** — AI produces first drafts of documents, communications, analyses, and recommendations; no person writes a first draft by hand when AI can; but every requirement, decision, and authorization must be read and accepted by a person before it counts.
- **If it was not recorded, it was not decided** — any business or product decision made outside a recorded Microsoft Teams meeting is not a formal JVL decision until re-confirmed in a subsequent recorded meeting. Stated to have no exceptions.
- **The bus-factor rule** — the company must keep operating if any single person leaves; roles, projects, and systems must be documented well enough for a replacement to take over.
- **Traceability is non-negotiable** — code traces to a Feature, a Feature to a Capability, a Capability to a Requirement, a Requirement to a recorded meeting or a regulatory obligation.
- **Idle time is waste** — a person on payroll without active scheduled work is escalated and resolved immediately.
- **Deadlines are real** — a deadline that will be missed is communicated before it expires, not after.

## Decision authority

- **Val Levitan, President, holds final decision authority across all JVL entities and domains.** (source: JVL Constitution — ~/Projects/Constitution/)
- Decisions within a manager's delegated scope don't need Val's approval; decisions outside it — new contractors, exceptions to standing policy, financial authorizations above threshold, regulatory matters — need Val's explicit sign-off first. No policy exception is created without Val's explicit approval, and approved exceptions are recorded. (source: JVL Constitution — ~/Projects/Constitution/)

## The executive–engineering boundary

- The executive/administrative branch produces exactly two things engineering cannot produce itself: **Requirements** and **Capabilities**. Capabilities are the core of the product pipeline (defined by market need and business decisions); Requirements are an independent, reusable reference layer that links to Capabilities for traceability. (source: JVL Constitution — ~/Projects/Constitution/)
- Engineering receives Capabilities and owns everything after the handoff — ADRs, tech-stack decisions, Features. The executive branch makes no architectural decisions; engineering defines no business requirements. (source: JVL Constitution — ~/Projects/Constitution/)

## AI at JVL

- AI is treated as a **first-class participant**: it drafts, reviews, analyses, and recommends, while humans govern, decide, and are accountable. The standard: if a task can be delegated to AI without loss of quality, it is. AI assistants acting for JVL are expected to know these principles, to say when they don't know something, and to correct themselves without resistance. (source: JVL Constitution — ~/Projects/Constitution/)

## The audit doctrine — "find the printer that prints the cheques"

Val's recurring control principle, stated twice in mid-April 2025 (to the CMS team and to the Omni daily) as his method for establishing truth in any organization:

- To audit a large company's accounting you do **not** interview the participants — "процессы, которые связаны с опрашиванием людей … никогда не работает. Потому что каждый человек имеет свою правду" (said of honest people). Instead: (1) get **signing authority on every cheque** at the bank; (2) find **the one printer that prints the cheques** and switch off the other 799; then ask why each cheque exists. "Только таким способом вы сможете сделать контроль в компании." He says he arrived at this himself ("Я пришел к этому кровью и потом") and only later saw it echoed in Elon Musk's government-audit approach. [[raw/cms_svn_github-april-14-2025.md]] [[raw/daily_omni_progress-apr-15-2025.md]]
- Applied to engineering: **committed code is the cheque** — "если мы не будем контролировать код. Где мой код? … То все это бессмысленно"; the requirement→feature→code chain plus the repo audit point replaces bureaucratic status "балет," and incidentally reveals who is useful ("Мы сразу найдем людей, которые не нужны … Но я найду людей, которые мне очень полезны. И я буду продвигать этих людей"). [[raw/cms_svn_github-april-14-2025.md]]
- Applied to game assets: the audit point is the **pull request that lands a compiled asset into the game repository** — "вот этот принтер, про который я всегда говорю … он стоит в game … Когда вот это completed … это значит, что напечатался чек, я на нем буду расписываться"; everything upstream in the designers' sandbox is "вся суета." [[raw/daily_omni_progress-apr-15-2025.md]]

## Traceability — "no feature without a requirement, or you're burning money" (Apr 16)

In the Apr-16 Omni daily ([[wiki/meetings/2025-04-16-daily-omni-feature-story-planning.md]]) Val hardened the traceability principle into a working rule for the engineers:

- **Every feature must be pinned to a requirement, or don't build it.** "Каждый у себя должен спросить, зачем мы это делаем … И если нет Requirement пришитого к этим Feature, то, пожалуйста, это не делайте, потому что вы палите деньги." Un-required work "возбудит давление на людей, как например Уан Мартинес, или на меня, или на Филиппе, или на Марту" — the executive branch owing engineering/testing an explanation. [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- **The description chain:** the sum of a feature's story descriptions must equal the feature description, and the sum of all features must equal the product — testable by having an AI read the stories and reconstruct the feature/product. If it doesn't read sensibly, a story is missing/wrong and "результат программирования, скорее всего, будет неправильным." Write descriptions in the native language first, then translate. (Detail on [[wiki/topics/omni-core-advancement-and-game-templating.md]].) [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]

## Right-size the organization — "I don't need to be Ford" (May 7)

On the May-7 IT-maturity call ([[wiki/meetings/2025-05-07-it-department-maturity-secrets.md]]) Val pushed back on over-engineering the IT function for a small company: [[raw/it_department_maturity-may-7-2025.md]]

- **30-person shop, not Ford or Nestlé:** "I don't need a chief technology IT vice president, chief thinker, chief strategist who read all the books … I can achieve myself, even without you, 80 percent success … I just need to give them enough knowledge and make it in a more binary way." He wants direction given plainly ("they need direction … show me your work"), not theory. [[raw/it_department_maturity-may-7-2025.md]]
- **Progress over perfection — the "Alabama mud" metaphor:** Val's fear is not cost but stalling. "If I made the wrong choice in an application … and I'm losing $1,000 a month, I don't care … What's going to kill me is the Alabama mud … one tire spins, the other does nothing" (My Cousin Vinny) — the fix is to "apply the parking brake" so both wheels turn, i.e. stop philosophizing and move. [[raw/it_department_maturity-may-7-2025.md]]
- **Cross-cultural realism:** he described bridging "two continents" — Kansas-based advisers and the Belarus-based team who "went to Belarusian schools … don't travel the world" — each side must stay respectful of the other's limitations. [[raw/it_department_maturity-may-7-2025.md]]

## Policy before infrastructure — the IT-maturity model (May 28)

On the May-28 IT-maturity review ([[wiki/meetings/2025-05-28-it-maturity-delinea-secrets.md]]) Aaron's "maturity model" framing and Val's own words made the ordering explicit: [[raw/it_maturity_update-may-28-2025.md]]

- **Write the policy/intentions first, then fulfil them with infrastructure** — Val's building analogy: you don't grab materials and start; you build to a plan/spec (he was literally building a chicken shack to US framing conventions, "written down"). "In IT maturity you don't just start doing stuff because it makes sense… you write down your intentions in the form of policy and planning. Then you fulfil the obligations of the policy with infrastructure." The policy is "the foundation for why your infrastructure exists"; without it "there's a ceiling to the maturity you can do." (This is stated as the general operating doctrine, applied on May-28 to IT/secrets — see [[wiki/topics/infosec-and-server-infrastructure.md]].) [[raw/it_maturity_update-may-28-2025.md]]
- **Plan before you act ("call the shot").** Aaron: "when you play golf you call the par… you're calling out what you're going to do before you start, then work the plan" — build the executable backlog with expected outcomes first, so you can say how long a job will take *before* starting and know when it's done. [[raw/it_maturity_update-may-28-2025.md]]
- **Val's limit on measurement.** He resisted the idea that policy can be neatly *measured* ("it's very superficial… hard to measure policies, if possible at all"), and asked for a **visual map** of a policy rather than metrics — his usable "language of communication." [[raw/it_maturity_update-may-28-2025.md]]

## "You'll shine. It's your achievement." — selling to the gatekeeper on his own P&L (Jun 16 2026)

*(Back-filled: this session predates the Aug/Sept-2026 entries below and adds to the record rather than replacing any of them.)*

Over lunch after the [[wiki/meetings/2026-06-16-jj-gaming-nebraska-site-visit.md|J&J Omaha site visit]] ([[wiki/meetings/2026-06-16-jj-gaming-steakhouse-lunch-rick-rees.md]]; **the raw transcript's speaker labels are inverted — see the stub**) Val ran a variant of the selling doctrine on someone who is explicitly *not* the decision-maker. It is worth recording because it is the counterpart to the rule he had stated to the same man's face that morning — that selling to operations people is difficult and decision-makers are bottom-line people. [[raw/Meeting_Notes_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]

- **Establish that the number is personally his, then attach the product to it.** Val first pinned down the scope of [[wiki/people/rick-rees.md|Rick Rees]]'s authority — local profit, local hiring, "what happens here" — and only then made the pitch in those terms: "If my offer is compelling to the company and you bring it in, you can **improve the bottom line, meaning profit for the company here, by reducing expenses because you switch to my equipment. You'll shine. It's your achievement.**" When Rick asked, half-joking, whether the company would take care of him for that, Val: "**You will. I promise.**" The method: where you cannot sell to the buyer, sell the gatekeeper his own credit for the introduction. [[raw/Meeting_Transcript_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]
- **The play did not close, and the counter is the one JVL still has no answer to.** Rick: "**You got a lot of people to impress, not just me. I'm step one.** But especially for a system that **you have nowhere else. So how are you testing it?**" [[raw/Meeting_Transcript_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]
- **Val's rule when caught without an answer: concede the fact, then claim the risk.** He did not dress up the position — "**This will be my first test**" — and when Rick twice repeated "**being the first is not always the best**", Val agreed with him and moved the liability onto himself rather than arguing: "**It's not. I'm not saying that it is. Not at all. That's on me, I know what I'm doing. You'll be impressed.**" This is the same posture as his later "you cannot insult me" opening (Sept 9 2026, below) — absorb the objection, do not contest it, keep the relationship. [[raw/Meeting_Transcript_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]
- **The lunch itself is the method.** The derived notes record taking a new counterpart to lunch after a first meeting as **Val's standing move**, and say that **most of the 78 minutes is relationship-building, not business**. He closed it with a commitment rather than a close: "**nothing's going to happen overnight. We'll keep on experimenting in the meantime.**" [[raw/Meeting_Notes_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]] [[raw/Meeting_Transcript_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]

## "Hypothetical until it is in the market" — the factual-data doctrine (Aug 21 2026)

On the [[wiki/meetings/2026-08-21-post-goam-show-recap.md|Aug-21 post-GAMOA recap]] Val stated, repeatedly and explicitly, the rule he uses to decide when market feedback is allowed to change a product. Applied on that date to Flex IQ — see [[wiki/decisions/2026-08-21-release-flex-iq-as-is-place-units-collect-facts.md]]. [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]

- **Show and conversation feedback is hypothetical; placed units produce facts.** "Everything that we're discussing here is hypothetical, unless… the final stage when IQ is in locations. When IQ is in locations, then the information we're getting is factual. It's no longer hypothetical." [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- **Every hypothesis is valid; none is a licence to act.** "I believe that every hypothesis is valid. We just don't know the facts and go out and start changing things without really understanding how the market operates. It's silly." [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- **Discovery requires volume, not analysis.** "We will never find out until such a time that we have one, 5, 10, 50 units out. You just, you have to go through discovery. The market is new, the market doesn't know what they want. You hear a lot of things, but those are things… It's like different bells, but you don't know that there's no rhythm to it. There's no hard knowledge." [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- **Parked is not dismissed.** He drew the distinction himself when a colleague summarized the ruling: "but we also not dismissing anything; we are at the at the stage of collecting." [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- **Corollary on giving things away, stated the same evening:** "It's very easy to give away things. You know, if I put an idiot… in the market… and I will say, do me a favor, call everybody and give them machines for free. He will do it." And: "you're not selling by giving things away." [[raw/Meeting_Transcript_Georgia_Machine_Sales_Strategy_Post_GOAM-August-21-2026.md]]
- **Corollary on discounts vs currency:** "The moment I give discounts, I could never bring the price back. I'm done" — hence [[wiki/decisions/2026-08-21-keep-jvl-dollars-printed-serialized-cards.md]] and [[wiki/topics/jvl-machine-pricing-strategy.md]]. [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- **Corollary on brainstorming vs direction (his answer when told the direction keeps changing):** "maybe my mistake is including you into my exciting brainstorm sessions. But if I don't include you into my brainstorm sessions, you would be a paper pusher. I am trying to make you into a thinker… I'm giving you all these random things. Maybe this, maybe this. I'm not giving you any directions." [[raw/Meeting_Transcript_Georgia_Machine_Sales_Strategy_Post_GOAM-August-21-2026.md]]

## "AI is programmed to flatter and to agree" — the AI-use guardrail (Aug 24 2026)

Coaching [[wiki/people/genadi-peari.md|Genadi Peari]] on his new AI agents, Val restated the guardrail he had put into the AI executives' Constitution: "Не забудьте что эйай… Запрограммировано. Всегда льстить. И всегда соглашаться" — don't forget AI is programmed always to flatter and always to agree — and therefore "ему нужно указать. Чтоб он не старался соглашаться" (you must instruct it not to try to agree). His first numbered point, about clear instructions, is garbled by an apparent negation in the transcript and is not reconstructed here. See [[wiki/topics/ai-assisted-development.md]] (Aug-24). [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Preamble-August-24-2026.md]]

## "A developer learning is not JVL learning" — the standards-repository rule (Aug 28 2026)

Closing the [[wiki/meetings/2026-08-28-dragon-pays-nova-conversion-review.md|Aug-28 Dragon Pays review]] (Russian), Val restated an existing standing rule and gave the reasoning behind it. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

- **The rule.** "если из этого вырастают какието стандарты, то стандарты надо добавлять… Это репозиторий стандартов. Если там вырастают какието, стандарты их надо добавлять обязательно. Стандарты для компании это наши." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **The distinction it protects.** "мы говорим, что ни девелопер чемуто научился. А что j [JVL] чемуто научился? Это 2 разные вещи да?" Irina and Pavel supplied the same idea as "коллективный коллективный разум." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **The mechanism that makes it pay off.** Standards contributed by earlier developers become directly usable by the tooling: "когда девелопор даже запускает клод, и мы и девелопер говорит, посмотри на стандарты, то те стандарты, которые предыдущие девелоперы внесли уже сюда. Они для Клода становятся прозрачными." [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- **The enforcement he set for himself.** "мне со своей стороны надо смотреть… Матрицу. Какой девелопер создал, какие стандарты я это буду делать" — he will personally review which developer has contributed which standards. [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]

## "Nobody else came here and asked you for business" — the selling doctrine (Aug 26 2026)

At the [[wiki/meetings/2026-08-26-narayani-amusements-trade-in-negotiation.md|Aug-26 Narayani visit]] Val put his whole case for why a lapsed customer should buy from JVL into three moves, in front of the customer. Recorded because he uses the same three repeatedly and they explain how JVL competes without matching Aristocrat's budget.

- **Show up in person, and say so.** "none of the light and wonder, IGT[,] aristocrat decision makers came here and asked you for business. **Not one ever, and never will. And I did.** So when somebody comes and asks you for business in my position, it's a pretty good decision to do business." [[raw/Meeting_Transcript_Narayani_Amusements_Trade_In_Negotiation-August-26-2026.md]]
- **Disagree with the customer to his face, and put the relationship above the argument.** "Would you like me to agree with you or disagree with you? What would you like[,] me to tell you the truth? **I think that you're wrong.** My opinion. You could kick me out of here. It's your place. But **I'm here to do business**… the bottom line for me is to do business with you." He grounded the disagreement in tenure — "I'm telling you from **43 years' experience**" — and conceded the frame immediately where the customer was right: "It's all about return on investment. **I am the first one to admit to it**," and "I fully understand you. Customer dictates." [[raw/Meeting_Transcript_Narayani_Amusements_Trade_In_Negotiation-August-26-2026.md]]
- **Let the counterparty set the number, then bound it.** "Give me a pen. Give me a piece of paper… **You write the deal. I will honor the deal that you will write.** Write a fair deal" — paired with an explicit appeal to fairness ("be fair with me because I'm looking for a **long-term relationship**. Don't screw me") and an explicit walk-away he offered the customer rather than himself ("you may just say, 'You know what? At this stage, I'm not interested in doing business with JVL,' and that would also be fine"). When the customer named $7,000, Val declined and kept the trial alive: "**The answer is no, but I want you to try it.**" [[raw/Meeting_Transcript_Narayani_Amusements_Trade_In_Negotiation-August-26-2026.md]]
- **The stated objective of the visit was the customer's state of mind, not the order.** "When I leave here, **I want you to be happy**." Against which he also priced his own concession out loud — "You're asking me for an incredible deal. You're selling me a four-year-old machine that paid you four times over." [[raw/Meeting_Transcript_Narayani_Amusements_Trade_In_Negotiation-August-26-2026.md]]
- **§15.8:** clear — negotiation conduct and deal economics only; no named-person compensation.

## "Less is more" — Val's sales coaching to Felipe and Andrei (Sept 1 2026)

After the customers left the [[wiki/meetings/2026-09-01-narayani-akshar-mega-hit-demo-and-trade-in.md|Sept-1 Narayani/Akshar demo]], Val spent roughly 35 minutes giving [[wiki/people/felipe-miranda.md|Felipe Miranda]] and [[wiki/people/andrei-klimovich.md|Andrei Klimovich]] direct, unsparing feedback on how they had just sold. It belongs here rather than on a meeting page because it is doctrine he states as general, and because he framed it as correctable technique, not as criticism: "**I'm just giving you factual things. Don't get upset with me**," and at the end, "**By all means, contradict. There's nothing. I don't get offended by you contradicting me.**" [[raw/Meeting_Transcript_Narayani_Amusements_Mega_Hit_Demo_and_Trade_In-September-1-2026.md]]

### The rules, as he gave them

- **Do not take phone calls in front of a customer.** "**you're making a big mistake when you're with the customer answering phone calls.**"
- **Never say "no, but".** "When I said it does something, and you said no, but something else. **Don't do that**… The better way to do it is to say, **actually, this is a great idea, and in addition to it, we do this.**"
- **Volume repels.** "you're repeating yourself frequently, and when you want somebody's attention, what you do is this: a lot of gesticulations, and you start speaking loud. **That's a mistake. So the louder you speak, the more repulsive it is**… So you see that I'm backing away from it."
- **Posture is a tell.** "**when your hands are in your pocket or behind you. That's a sign that you have to hide something.** You're uncomfortable. When your hands are this way, **you're defensive.** The best way is hands quietly normal. **Stand straight… look you in the eyes. Normal tone of voice.**"
- **Cut the speech.** "**your speeches are very long because you know a lot, you want to say a lot, but it's too much. Start from focusing on a gem, on something that is a killer. Stick with it. Less is more. Let them ask questions.**"
- **Never ask "do you have any questions?"** "**The questions will either come naturally or come later. Never ask if you have a question**… If he doesn't have a question, is he stupid? Or did you not do a good job? **It's too controversial.**"
- **Lead with the one differentiator, not the feature list.** The Steve Jobs argument: "**Steve Jobs, when he made that downloadable music iPod, he wasn't talking about the music. He was talking about ten thousand tunes in your palm.** He wasn't talking about my player plays louder… **He went into a bullseye. One thing that people understood**"; and the counter-example, "**When BlackBerry was selling security**… **Steve Jobs was selling minutes.** … Nobody gave a [damn] about security." He also cited Jobs on market research: "**Steve Jobs had always considered that marketing always does a lousy job because they ask people what they want**… Where Steve Jobs always started: **You need this. You want this.**" JVL's own bullseye, in his words: "**This is the only machine where you are in control of how to fine tune your games.**"
- **Know which audience gets the technical version.** "if you talk about it with [[wiki/people/michael-gottlieb.md|Michael Gottlieb]], **that's a good conversation to handle**, or with Lena… **But when you talk to the guys who make a decision on buying the machines, you need to get to the point very quickly.**" *(Michael Gottlieb is JVL's Senior VP of Game Design; "Lena" is read as [[wiki/people/lena.md|Lena]], who leads game design/art — an inference from role, since the source gives only the first name.)*

### Felipe's counter, and Val partly conceding

This is a rare recorded instance of Val being argued with at length by a direct report and giving ground. [[raw/Meeting_Transcript_Narayani_Amusements_Mega_Hit_Demo_and_Trade_In-September-1-2026.md]]

- **Felipe's objection was vocabulary, not content.** "**I'm a little confused. I feel I'm using terms that they wouldn't know.** Remote initial settings, modem. Are you here to talk about the game? What remote? What modem? Why are you talking about that? You were showing me the game. **That's how I would perceive what you just said. I don't think that explains the game.**" And: "**They don't care what the game does. They don't care if the lion roars. That's not important to them**… **They came here to see a game.** I just get excited about talking about it."
- **Val conceded the point and re-framed rather than retreating.** "**You're absolutely right. It doesn't explain the game. But no matter what, I will tell you about the game.**"
- **He also stated why it matters commercially, from the buyer's side:** "**These are two operational guys, and they want to look good at the end. Their purchase has to be justified. This gives them the biggest chance to customize their purchase to their location.**"

### "One line of garbage and the whole report is garbage" — and the pushback

The same session carried a second, harder doctrine — an evidential rule about reports — which Felipe did **not** accept. Recorded with both positions because the disagreement was never closed in the room. [[raw/Meeting_Transcript_Narayani_Amusements_Mega_Hit_Demo_and_Trade_In-September-1-2026.md]]

- **Val:** "**Any report that could generate one line of gross garbage — the whole report is garbage. You will never see any mathematician, any statistician, any engineer ever accepting a report where there is one line of garbage. If there is one line of garbage, the whole report is dismissed.**" His definition of a report: "**A report is the generation, or decoding, of a stream of data that is streaming from remote devices to a server. If you find one line of garbage, you need to dismiss the whole thing.**" And the concrete case: "**the report that shows that a machine pays out a million dollars in one week is garbage. It doesn't matter which machine.**"
- **Felipe's pushback:** the industry has used these reports "**since twenty thirteen**," the disputed line was about a **game**, not a machine, and it is "**a different report**." Val's answer was to restate rather than reconcile: "**It's a mathematical fact. If the report comes out with one line of garbage, you can assume that other lines are also garbage.**" Val's own concession elsewhere in the exchange: "**I agree. People use a lot of garbage to disseminate information that serves them.**"
- **This is the reporting-distrust half of the modem case**; the commercial programme it feeds is on [[wiki/topics/machine-data-repurchase-program.md]], and the "hypothetical until it is in the market" factual-data doctrine above is its internal counterpart.

**§15.8:** clear — selling technique and reporting doctrine only; no named-person compensation.

## "The machine should not break. Period." — how Val takes a service complaint (Sept 2 2026)

Faced with a customer's account of why JVL is not his primary supplier ([[wiki/meetings/2026-09-02-lucky-coin-service-and-upgrade-offer.md|Sept-2 Lucky Coin visit]]; full complaint on [[wiki/organizations/lucky-coin.md]]), Val did four things in sequence that read as doctrine rather than as one meeting's manners [[raw/Meeting_Transcript_Lucky_Coin_Service_and_Upgrade_Offer-September-2-2026.md]].

**1. He refused to let the conversation become a negotiation about whose fault it was.** When the argument drifted into whether the operator ought to notice a frozen machine, he stopped it himself:

> "I need to say something because I believe that the conversation **diverts from the essence**. **I don't think that our machines should be breaking. Period.** For whatever reason, it just shouldn't be breaking. **We should be making machines that don't break**, and that is the essence of the conversation."

And, a minute later, on where the burden belongs: "**I don't believe you should know about it, and I don't believe it should be a problem. And I believe it should be my problem.** And I think that I should know about it first… Number one, that machine never breaks. Number two, **if it broke, I should be the first one to know**." The customer's own framing of the same boundary, which Val accepted outright: "**You should not be burdened with my invention.**"

**2. He admitted he had not understood the problem until he watched it.** "**I now understand what needs to be addressed. I will address it. I cannot address it tomorrow**… **But I never understood what the issue was.** And yesterday I went on a location. **I saw it myself**… I saw a technician spending over an hour in a location trying to recommission the machine. To me, it has always been 'well, commission — what's the big deal?' **But you're right.**" On the regulator's system in the middle of it: "**Intralot is not the sharpest pencil in the box, but it's our box and it's our pencils. That's what we deal with.**"

**3. He refused to give a date, explicitly and repeatedly.** "**I will fix it. I just cannot commit to a date.** [I] just don't know how to put it into process — to fix it and what needs to be fixed. Even when you tell me all of this, **I still did not wrap it around my mind what exactly needs to be fixed**." His account of why a promise would be worthless: "it will take me time to put it through the **engineering cycle**. Then it will take me time to **roll it out in the market**. It will take a very long time, and by then, **all my promises… will go unnoticed, and people will continue being frustrated**." What he offered instead was explicitly a stopgap and labelled as one: "**the only thing I can do today is to put more of my own tech[s] on the road to mask the problem** that you're having and help you… I could provide **extra replacement inventory**… **I could compensate it price-wise, but that's all I can do.** To stand here in front of you now and tell you that it will be fixed tomorrow — **it's crazy.**"

**4. He apologised for conduct he could not verify, without disputing it.** On the refusal to help with third-party integration: "**That should not happen. If it happens** — I have no reason not to believe you. Obviously, I believe you. All I can say is **I regret that it happens**… **I apologize for that.**" And on the technicians in the middle of it, from his own history: "I started my career repairing mechanical jukeboxes and mechanical pinball machines in locations… **So I know what these guys are going through. I know how hard it is** and how tiring it is at the end of the day to hear somebody else on the phone tell you how… to do a thing that you've done ten thousand times."

### "Useless emotions. You cannot put it on the spreadsheet." — the debrief

After the customer left, [[wiki/people/felipe-miranda.md|Felipe]] was still shaken by the criticism — "I'm very surprised. I can't help it" — and Val cut it off. It is the sharpest statement in the corpus of how he wants bad news handled [[raw/Meeting_Transcript_Lucky_Coin_Service_and_Upgrade_Offer-September-2-2026.md]]:

> "this is **useless emotions. Useless**… They're worth zero… **You cannot quantify them. You cannot put it on the spreadsheet. There is nothing you can do with your emotions**… **Inhale it and move on.**"

He immediately took the harshest edge off it ("No, no, no. I'm taking it back") — but the instruction stood, and he had already modelled the alternative in the meeting itself: treat the complaint as information, and go and look at the location. The same session also has him telling Felipe **not** to protect him from the customer's technicians: "**You don't have to protect me. I'm a big boy.**"

**§15.8:** clear — service, engineering-cycle and customer-conduct doctrine only; no named-person compensation.

## "It worked here, it doesn't work there" is not an excuse at your level (Sept 4 2026)

The sharpest statement in the corpus of what Val expects from a senior engineer, delivered to [[wiki/people/pavel.md|Pavel Frolov]] on the [[wiki/meetings/2026-09-04-lte-modem-firmware-mismatch-and-kore-settings.md|Sept-4 midday modem call]] after the Georgia LTE modem failed a test that had passed in Minsk [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].

- **He named Pavel's frame before arguing with it.** "Я понимаю, что у вас в голове происходит… вы как бы думаете, что у вас есть начальник, которые не понимают нюансы. Вы правы в том, что вы протестировали[,] у вас [работало]… И вы считаете, что вы правы."
- **The objection is to the concept, not the result.** "Вы заблуждаетесь в том, что вы проверили[,] всё работало[,] а сейчас не работает. Вот этот вот концепт, сам по себе он ошибочный." Pavel's rebuttal — "Мы проверили, у нас работает… Сейчас мы проверили, не работает. Мы у себя ещё раз проверили, у нас работает" — did not move him.
- **It is explicitly a seniority argument.** "если бы вам было сейчас 25 лет[,] и вы только начинали работать [здесь,] я бы абсолютно нормально к этому относился. Но вам помоему уже не 25. И помоему вы… работаете уже давно и… чётко разбираетесь во всех нюансах."
- **The duty is to design the test strategy, not to be told it.** "Я начал про этот мод[ем] говорить давнымдавно. У вас было [время]… чтобы сделать правильный страте[гию]: какой мод[ем] проверять, на чём проверять и где проверять… [микро]менедж[ить] все вот эти вещи мне кажется[,] что человека в вашей позиции уже не стоит." The acceptable alternatives he names: test in Georgia from the start, **or say up front that testing in Minsk is probably the wrong test** — "или сразу говорите[:] скорее всего, в Минске проверять это неправильно." Pavel: "Все так и сделано. В точности." Val: "но это надо было делать раньше[,] давнымдавно[,] я же не начал просить это на прошлой неделе."
- **The principle in one line — work preventively and say in advance what may fail.** "я хочу[,] чтоб мы более аккуратно относились к нашим респонс[ибилити]с. Предупредительно… что может не сработать?" And the distinction he draws between delegation and supervision: "как бы оставляю это в вашем уже углу и меньше за этим слежу… я понимаю, что вы взрослые люди, вы понимаете, что может не сработать[,] и вы работаете предупредительно. Вы просто поймите, что это разные позиции."
- **He would not assert the timing without evidence.** "я не не хочу просто говорить голословно, но я проверю, когда я это начал просить" — he undertook to go back through his own messages rather than argue the date from memory.
- **The derived notes read the exchange the same way:** "Val's argument is that the concept itself is wrong… If Pavel were twenty-five and new, Val said he would treat it as normal, but Pavel has been at JVL a long time and understands the nuances" [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]].
- **It ended unresolved.** Pavel: "честно говоря, расстроен, что вы считаете, что мы вот игнорируем вот этот пункт." Val: "Скорее всего, что не игнорируем… [а] не бер[ё]м респонс[ибилити] [за] неправильно принятые решения," and suggested the weekend would change his mind. Pavel: "Хорошо[,] я вас услышал. Ещё больше расстроился."
- **How Val read it afterwards**, alone with [[wiki/people/genadi-peari.md|Genadi]] twenty minutes later: "Я пытался Павла провести, он помоему был в шоке от моего комментария и уехал, расстроенный домой. Поэтому оставим его, чтоб он отдохнул, и вернёмся к этому в понедельник" [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]].

**Two smaller operating rules from the same day** [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]:

- **Don't write to someone when you need something now — call and watch.** On working with [[wiki/people/elizabeth.md|Elizabeth Palomino]]: "Не пишите… когда ты ей пишешь… она посмотрит на это через час[,] она подумает через 2[,] она приступит к этому через 3… так нельзя. Позвоните на [Teams], скажите… иди проверь… не ставь меня на холд[,] я буду ждать[,] я сижу[,] смотрю на тебя[,] направь камеру на это." Genadi executed it inside the same call.
- **"There are no weekends."** Told to [[wiki/people/evgeniy-alekseev.md|Evgeniy Alekseev]] when the weekend was raised as an obstacle: "Нету праздников[,] выходных[,] уикендов. Это я всё отменил… Этот заказ сверху пришёл, да, никаких выходных." Delivered half-jokingly ("это религиозная"), but the work was scheduled on it.

**§15.8:** clear — management conduct and engineering-responsibility doctrine only; no named-person compensation.

## "My goal is not to change the location's mind. My goal is to change your mind." — the selling doctrine applied to a sceptic (Sept 9 2026)

At the [[wiki/meetings/2026-09-09-rao-machine-performance-and-exclusivity-offer.md|Sept-9 Rao meeting]] [[wiki/people/val-levitan.md|Val]] named, out loud and to the sceptic's face, what he thought the meeting was actually for. It is the sharpest statement in the corpus of the selling doctrine recorded for Aug 26 above. [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

> "**How changing [a] mind starts[:] one step at a time.** Right now… **in your mind, we are not up to par. So my goal is not to change the location['s] mind. My goal is to change your mind.** You said your mind doesn't matter. It's the player. It's the location… **For me, [Rao], I cannot change [the] player's mind. I cannot change [the] location['s]. I can only influence your mind, and so my focus is changing your mind.**"

- **And the method: go and look, one location at a time.** "**When I prove to you that this machine works, then in your mind you will say, 'Great.' So now, why doesn't it work here? Let me look at it with critical eyes**"; and at the close, "**Let's start taking us to locations one by one. All your hesitations will go away one by one.**" [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- **He also refused to let the customer's own metric stand as the argument.** Told that what matters is the cash box, Val agreed and then reframed it: "**the cash box starts from understanding what could be the issue. Right now… my issue is that you think that they are better, and I know that they're not. So my goal is to prove to you that they're not better.**" [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- **On regret about market timing, a standing rule of his:** told JVL should have arrived two years earlier, "**If we had it two years ago, [it] would have been much better… We didn't have it two years ago. We're here, so there's no point discussing what would have been two years ago**… **we just couldn't get it two years ago.** So we're here now." [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- **And the doctrine about who will never pay, stated as an unchanging law of the trade:** "**The location is used to getting shit for free. They will always get it for free. They will find a way to get it for free. They will extort… It will be pure extortion**… **Nothing changed from 1984. Nothing changed.** It's the same, and **it doesn't matter which equipment you have. The location will always say, 'My client, my location, my license.'**" This is the reasoning underneath [[wiki/decisions/2026-08-31-transactional-equipment-only-with-location-exclusivity.md]]. [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]

## "You cannot insult me" — how Val opens a complaint session, and how he closes a sale (Sept 9 2026)

Three hours later, at the [[wiki/meetings/2026-09-09-lucky-coin-service-burden-and-exclusive-partnership.md|Lucky Coin shop visit]], the same doctrine ran in the other direction — Val asking to be told what is wrong rather than arguing that nothing is. It is the Sept-2 "the machine should not break, period" posture put in front of the technicians themselves. [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]

- **Removing the safety catch first.** "So, **what's the worst thing about us? The absolutely worst. The thing that you hate the most**… **You cannot insult me. It's impossible.**" [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- **Forcing the binary rather than accepting a soft answer.** "If I could sw[ing] my magic wand and it goes away, **would everything else be more or less okay, or is it still a shit product that you don't want? Because if it's a shit product and you don't want any, then there is nothing I can do about it.**" [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- **Overruling his own colleague in front of the customer when the answer was an excuse.** Told the loose subwoofer "is just never bolted down," Val: "**it shouldn't pop out of the tray. It's an issue.**" Same move as the Sept-2 "our machines should not break, period." [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- **And ruling a whole class of complaint out of scope on age grounds:** "**Altera is a thirty-year-old technology, so let's not go there.**" [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- **The differentiator he claims, in one sentence:** "**I'll be designing to your spec.** When was the last time that IGT or [Aristocrat] came to you? **Sat here with sandwiches**, and said, 'I'll be designing the system to your liking'? Can you tell me the date they were here?… **I've been in this business for forty-two years now.**" [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- **And a closing rule he stated and then obeyed on the spot:** "there is **wisdom. A salesperson needs to leave the moment the deal is reached. Shouldn't linger. So I'm leaving.**" [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]

**§15.8:** clear — selling and management conduct only; no named-person compensation.

## "Explain the reason — don't say 'do it because we told you'" (Sept 14 2026)

At the [[wiki/meetings/2026-09-14-code-standards-main-branch-rule-and-alekseev-coaching.md|Sept-14 7:37 AM code-standards call]] (Russian) Val set out how a standard is to be imposed on an engineer who is not following it. The case is on [[wiki/decisions/2026-09-14-alekseev-is-walked-through-the-standards-by-bosik-not-ordered.md]]; the principle is here.

- **The instruction is an explanation, not an order.** Val to [[wiki/people/andrey-bosik.md|Andrey Bosik]]: book the meeting and "**проговорил все эти варианты и объяснил, почему мы это делаем**" — but not "**слушай, вот ты… ты вот делай так, потому что мы тебе сказали**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **What the explanation must contain, in his words:** "**причину, почему мы так хотим делать? Почему мы от этого зависим? Какая должна быть последовательность?**" — the reason, the dependency, and the sequence [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **He diagnoses non-compliance as an explanation failure, not defiance:** "**ему сказали делай так без объяснений без ничего. И он импровизирует, как ему… удобно делать**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **"We struggled with it too" is part of the pitch.** "**стандартам, которые мы совсем недавно сами адаптировали… Мы тоже мучились, и мы тоже не понимали, как это работает**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **The widow Ivanova joke — his way of saying "handle the opening carefully".** Val closed the call with an old joke about the soldier sent to tell a wife her husband had been killed, who knocks and opens with "**Здравствуйте, здесь живёт вдова Иванова**" [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].
- **Bosik answered with the opposite principle, and Val let it stand:** "**я всегда считаю лучше прямо и сразу сказать, чем какимито обходными путями**" — better to say it straight away than by roundabout routes [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**A related self-placement, in the same call:** arguing engineering rules, Val twice stepped back from pressing an absolute — "**поскольку я ещё и не инженер, то мне вообще тяжело на эту тему говорить давайте согласимся**", and "**Поправьте меня, если я не прав**" — accepting [[wiki/people/pavel.md|Pavel]]'s "in general" rather than forcing the rule [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]].

**§15.8:** clear on this page — management conduct and principle only; the judgements about the named engineer are excluded, see the decision page.

## "Repeating a standard is not distrust" — trust first, then detail (Oct 20 2026)

At the [[wiki/meetings/2026-10-20-val-pavel-alignment-trust-standards-and-delegation-follow-through.md|Oct-20 one-to-one with Pavel Frolov]] (Russian) Val set out how his attention to standards should be read.

- **Trust is the precondition, not the question.** An invitation to work at JVL means trust: "**когда я только говорю, пожалуйста, приди работай на GBL 1. Это доверие**"; without trust "**приглашение на работу от меня никогда не выходит**" [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]].
- **What is called micromanagement is the search for detail.** Val said the team confuses distrust with his wish to reach perfection through small elements, and that the difference from competitors lies in that detail ("**разница между компьютешн заключается именно в этом**") [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]]. He noted that JVL's games look better made than the competition's, yet Aristocrat's earn more, and nobody can say how to make a JVL game earn more [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]].
- **The example: the field-defect standard.** There was no written standard for what to do with defects found at a field rollout; anyone in the company could have written it, but nobody did until Val did [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]] [[raw/Meeting_Notes_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]].
- **Writing a standard is not enough — it must reach everyone, so it is repeated.** People forget or are busy with other things, so a reminder is normal; Val called it "**постоянное повторение для достижения этого профессия, которого мы все ищем**" — constant repetition to reach the quality everyone wants, not distrust [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]]. He asked the team not to be irritated by it [[raw/Meeting_Notes_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]].
- **Small steps add up.** On following up delegated work: "**это 5 микротепс это большой степ**" — the working agreement this produced is on [[wiki/people/pavel.md]] (Oct 20 2026) [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]].

**§15.8:** clear — principle only; personal matters not recorded, and assessments of named or former staff are excluded.

## History

- **The one-source-of-truth principle predates the Constitution:** the ~2023–24 **JVL Insights** knowledge-base proposal already framed its strategic goal as **"ONE-JVL - ONE SOURCE OF TRUTH!"** — the same principle later codified as "One source of truth" in Constitution v1.1. See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

## Sources

- (source: JVL Constitution — ~/Projects/Constitution/)
- [[raw/Meeting_Notes_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/Meeting_Transcript_Code_Standards_Main_Branch_Rule_and_Alekseev_Coaching-September-14-2026.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
- [[raw/cms_svn_github-april-14-2025.md]]
- [[raw/daily_omni_progress-apr-15-2025.md]]
- [[raw/daily_omni_progress-april-16-2025 (Val Levitan's conflicted copy).md]]
- [[raw/it_department_maturity-may-7-2025.md]]
- [[raw/it_maturity_update-may-28-2025.md]]
- [[raw/Meeting_Notes_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]
- [[raw/Meeting_Transcript_JJ_Gaming_Steakhouse_Lunch_Rick_Rees-June-16-2026.md]]
- [[raw/Meeting_Transcript_Flex_IQ_Georgia_Recap_and_JVL_Dollars-August-21-2026.md]]
- [[raw/Meeting_Transcript_Georgia_Machine_Sales_Strategy_Post_GOAM-August-21-2026.md]]
- [[raw/Meeting_Transcript_Flex_Port_Mini_Capabilities_Preamble-August-24-2026.md]]
- [[raw/Meeting_Transcript_Dragon_Pays_Nova_Conversion_Review-August-28-2026.md]]
- [[raw/Meeting_Transcript_Narayani_Amusements_Trade_In_Negotiation-August-26-2026.md]]
- [[raw/Meeting_Transcript_Narayani_Amusements_Mega_Hit_Demo_and_Trade_In-September-1-2026.md]]
- [[raw/Meeting_Transcript_Lucky_Coin_Service_and_Upgrade_Offer-September-2-2026.md]]
- [[raw/Meeting_Transcript_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Notes_LTE_Modem_Firmware_Mismatch_and_KORE_Settings-September-4-2026.md]]
- [[raw/Meeting_Transcript_Flex_Slim_First_Ten_Build_and_FlexPort_SAS-September-4-2026.md]]
- [[raw/Meeting_Notes_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- [[raw/Meeting_Transcript_Rao_Machine_Performance_and_Exclusivity_Offer-September-9-2026.md]]
- [[raw/Meeting_Transcript_Lucky_Coin_Service_Burden_and_Exclusive_Partnership-September-9-2026.md]]
- [[raw/Meeting_Transcript_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]]
- [[raw/Meeting_Notes_Alignment_Pavel_Frolov_Trust_and_Micromanagement-October-20-2026.md]]
