---
type: meeting
title: Specification-standards review — the reverse-Omni method settled (Sept 22 2025)
date: 2025-09-22
aliases: [specification standards review, spec standards Sept 22, reverse Omni method, rubber-duck interview, Sasha spec interviews, spec for the specification, metacognition]
source-count: 1
open-commitments: 3
open-questions: 1
---

# Specification-standards review — the reverse-Omni method settled (Sept 22 2025)

**Date:** 2025-09-22 (12:06 PM) · **Attendees:** [[wiki/people/pavel.md|Pavel Frolov]], [[wiki/people/val-levitan.md|Val Levitan]], [[wiki/people/aaron.md|Aaron Bockelie]] (joined in an "Incognito" browser — Teams had stopped working). English. [[wiki/people/irina-shishko.md|Irina Shishko]] and [[wiki/people/alexander-biratka.md|Sasha Biratka]] referenced.

This is the **Monday follow-through** the [[wiki/meetings/2025-09-17-fast-pacing-alignment-standup-spec-prototyping.md|Sept-17 stand-up]] booked ("a spec template… to be discussed Monday"). It **advances the spec-driven-development thread** — the Aug-22 "Spec-Driven Dev Process v2.0" and the Sept-10/17 "reverse Omni into a spec" standups — and settles the *method* for producing Omni's first specification. The decision-level substance lives on [[wiki/decisions/2025-04-03-jira-capability-level-and-github-mapping.md]] (Sept-22 section); testing/touchstone substance on [[wiki/topics/test-automation-strategy.md]].

Durable points (single source):

- **Priority ruling — Omni first, Flex POS second.** Pavel proposed starting specifications with **Flex POS** (development just starting) and the cloud payment hub. Val overrode the sequencing: "our entire company's success is riding on **Omni** framework and I need it properly documented… specification written… and tests designed for Omni, because all other developments will be riding on Omni." Flex POS can be done in parallel because it's isolated — put [[wiki/people/nathan-carver.md|Nathan]] on it — but JVL's focus is **reversing Omni's design into a specification.** Without spec + QA tests Val "can't move forward" or leave the old run-QA-after-the-fact habit.
- **Aaron: the first-pass spec is not a formal document.** All the numbered headings / formalities in the AI-generated template "get in the way of thinking"; describe capabilities in plain sections/small pieces first, formalize later. For already-built systems you write an **"as-built"** — describe what exists (his kitchen-remodel analogy), then add new work against it.
- **Aaron: written-collaboration-first, then verbal (metacognition).** Force written collaboration in **GitHub issues/PRs (not chat)** before high-frequency verbal — the "bus-ticket" analogy (plan the trip before you spend the one ride). "Metacognition — thinking about thinking": reading a written artifact first lets the eventual in-person conversation happen at a higher level. This raises the value of the small dev team's scarce meeting time; treated documents-as-code so specs can be ping-ponged in PRs.
- **The reverse-Omni interview method (settled).** Schedule ~5 individuals to interview **Sasha (Biratka)**, the Omni framework author, module by module — ~**2 hours per day over a week**, one person per day so he isn't worn out. Sasha is a strong verbal communicator who "hates to write," so **record** him. Aaron's refinements: use a **second person as a "rubber-duck"** interviewer whose job is to keep Sasha on one area of concern, cover the **five W's + How** (who/what/where/when/why/how — an "audit" of the code), and make sure it's recorded; plan the transcript tree to **mirror the code-base directory structure** so coverage is complete.
- **Keep the transcript RAW — do not run it through AI (agreed).** Aaron insisted the recorded transcript be committed to git **without AI interpretation** (formatting-only capitalisation/paragraphing acceptable, but no substitution of meaning). Val accepted despite preferring readable output ("you must have a reason for it"): store the raw transcript in GitHub, then later AI **synthesizes a spec from {raw transcript + the actual code}**, not by translating the transcript into a format.
- **Drop the Russian→English meeting translation.** Val changed his mind on running these interviews through translation: everyone speaks fluent Russian, so translation is **detrimental** — it loses the eloquence and shifts the meeting into awkwardness. Keep the mother tongue. (Refines the earlier bilingual-tooling stance.)
- **Omni has no product owner — improvise a working group.** Aaron said the "treasure trove" normally goes to the **product owner**; Omni has none, and Nathan is "not really" it. Val proposed a **coalition acting as one product owner**: "**Lena Cima**" (name garbled), **Irina**, and **Pavel**, further interviewing Sasha to squeeze out detail. **Pavel becomes the working-group leader/mediator** — explains "the rules of the game," enforces "where is it written down / where's the PR," and **mediates rather than participates**. The interviewer is a news-reporter role (facts + the five W's), not the spec synthesizer.
- **One-time exercise, Omni only.** This reverse-spec method is explicitly a **one-time** catch-up (works because Omni is recent); **do not do it for the CMS / old systems** (Val: "I wouldn't do CMS"). Going forward the rule is **spec-first before any new code** — Aaron: "this is just normal engineering practice for larger projects… a good maturity step," AI or no AI.
- **Two spec scopes Pavel weighed.** (1) Describe just the Omni framework + a game on it (interfaces/communications/architecture) → yields only a minor test set; (2) describe the whole **EGM software product on the FP7 platform** (all software + firmware components, framework, local gaming server, OS) → enables **end-to-end tests** but is much harder. [[raw/specification_standards_review-september-22-2025.md]]
- **Prototype already running (from Sept-17).** Pavel confirmed the experiment: daily recorded meetings with **Alexander Biratka** ("Alexander Beratka"), a different interviewer each day on a different framework aspect, then join the transcripts into one specification document to analyze. This week's meetings with Sasha proceed; Pavel to send Val a short **calendar** (Teams/email) of when things will be done.

## Open commitments

- [ ] Pavel Frolov — send Val a short calendar (Teams/email) of when the Omni spec work will be done — [[raw/specification_standards_review-september-22-2025.md]]
- [ ] Pavel Frolov — run this week's recorded Sasha interviews (module by module) and stand up the working group (Lena Cima / Irina / Pavel) as improvised product owner — [[raw/specification_standards_review-september-22-2025.md]]
- [ ] Pavel Frolov / Irina Shishko — agree the spec template ("specification for the specification") carried over from Sept-17 — [[raw/specification_standards_review-september-22-2025.md]]

## Open questions

- Who synthesizes the raw interview transcripts + code into the initial Omni specification, given JVL has no Omni product owner? Val's improvised answer is the Lena-Cima / Irina / Pavel working group — not yet proven. [[raw/specification_standards_review-september-22-2025.md]]

## Sources

- [[raw/specification_standards_review-september-22-2025.md]]
