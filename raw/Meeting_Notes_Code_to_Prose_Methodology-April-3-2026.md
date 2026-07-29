# Meeting Summary — Val & Aaron: Code-to-Prose Methodology

**Date:** April 3, 2026, 1:06 PM Eastern
**Duration:** ~11 minutes
**Attendees:** Aaron Bockelie, Val Levitan

## Summary

Aaron walked Val through his methodology for understanding and refactoring code by translating it into prose — plain-language descriptions of what each piece of code does. The core idea is that if you convert executable code into written descriptions ("this function does X, that module handles Y"), you end up with a miniature specification of the system. Aaron emphasized that if you accidentally deleted the code but kept the prose descriptions, you could reconstruct the code from those descriptions, because they reinforce each other.

Val connected this to the reverse of the traditional software development flow: if you work top-down, you start with requirements, capabilities, ADRs, architectural schematics, and executive decisions that eventually become code. Aaron confirmed they're essentially reverse-engineering the code back up that decision ladder — decomposing implementation back into intention.

Aaron described how collecting these prose descriptions across a codebase creates a hierarchy: individual functions are described, those roll up into module descriptions, and modules roll up into system-level descriptions. He compared this to "stories" (though he expressed frustration with Agile's co-opting of that term) — each piece of prose tells the story of what that code is supposed to do. When you read them as a collection, you form a mental model of the entire system.

Val offered an analogy, suggesting that prose descriptions are essentially what a feature branch would represent — a literal description of what that branch is doing. Aaron acknowledged the connection in the coding context but broadened the concept: prose is simply any expression of intent in plain human language, as opposed to the symbolic language of code. He illustrated this with a humorous example — no one talks to a colleague by saying "open curly brace for I equals 1 to 27 plus N plus 1 close curly brace semicolon." Instead, you say "let's go through these 27 items and make sure we cover every one." Both expressions carry the same intent, but in different languages with different fidelity.

Aaron then traced the lineage of programming back to Jacquard looms printing patterns in rugs with punch cards — the fundamental act of programming has always been taking human intention and feeding it into a machine that follows patterns. The patterns have grown enormously more complex, but the essence hasn't changed. By converting code back to prose, the team is bringing the work back to the human element — what was this supposed to do?

Aaron acknowledged that many software engineers would dismiss this approach, believing "the best description of the system is the code itself." He attributed this mindset to engineers who were trained to think in code but never studied humanities or philosophy, where the primacy of semantic meaning over symbolic representation is well understood. He argued that if you had the prose description, you could just as easily rewrite the code in machine language assembly — the prose captures the intent, and any target language is just an implementation detail.

Aaron then explained why this matters specifically in the context of large language models. LLMs can understand code as prose and prose as prose equally well — they act as a "Tower of Babel" that can translate between programming languages, mathematical notation, and human language. He used mathematical notation as an example: summations, sigmas, integrals, and series are symbols and notations that don't have direct English-language equivalents. This is why math is hard for many people — they're learning a language that isn't their native tongue. But for someone who becomes fluent, it becomes first nature. LLMs have that fluency across all these languages simultaneously.

The engineering implication is that you can take anything — code, math, specifications — and throw it at the language model to translate into a different language, with the understanding that certain target languages will have less fidelity to describe the original concept than others. A 10-line function in TypeScript might require 100 lines of descriptive prose to fully capture. The engineer's job is to decide which language describes the intent most clearly at each level, and where the trade-off lies for how much description to maintain.

Aaron connected this directly to team coordination. When two developers write code with different mental models ("I wrote it thinking this way, he wrote it thinking that way"), their code may not be compatible. By decomposing both into prose — the common language — the team can see where the intentions diverge without needing to parse each other's code. Once they understand the mismatch at the intention level, they can each return to their corners, rewrite their respective code, and when the pieces reconnect, they work properly. Aaron noted this is essentially what a specification does, and what teams of programmers are fundamentally doing: following a shared specification to solve a problem.

## Decisions Made

No formal decisions recorded. This was a conceptual discussion establishing shared understanding of the code-to-prose methodology.

## Undertakings

No specific action items were assigned during this conversation. The discussion was educational and conceptual in nature.

## Engineering Signals

### Confirmed Signals

- **ADR — Code-to-prose decomposition as a refactoring methodology:** Aaron described a concrete approach for understanding and refactoring the JVL codebase: translate code into prose descriptions, use those descriptions as a specification layer, identify intention mismatches between developers' code, and then rewrite code to align. Aaron stated: "We decompose them into the intentions, into the prose. We go look at the prose and go, oh, I see what's going on. You described it this way, and I'm describing it that way, and that's why they don't fit to each other." This is an architectural methodology decision that could shape how the team approaches code analysis and refactoring going forward.

### Suspected Signals

- **Possible CAP — LLM-assisted code-prose translation pipeline:** Aaron described using LLMs as the translation layer between code and prose, calling them a "Tower of Babel" that can "take anything we can possibly think of and throw it at this, turn it into a different language to describe it." If the team builds tooling around this translation capability, it could warrant formal tracking.

- **Possible REQ — Prose specification layer for codebases:** The discussion implies a need for prose descriptions alongside code — essentially a specification layer that mirrors the codebase in plain language. Aaron stated that if "you accidentally deleted the computer code and left all the descriptions, you could literally go back and rewrite the code again because you have a description of what it's supposed to do."

## Open Questions

- How much prose description is the right trade-off? Aaron raised that 10 lines of code might need 100 lines of prose — the team needs to decide the appropriate level of detail for their workflow.
- Will this methodology be formalized into the team's development workflow, or was this a conceptual discussion for Val's understanding?
- What tooling or process will be used to generate and maintain these prose descriptions alongside the codebase?

---
*Processed from Teams transcript on 2026-04-04*
*Source meeting: Val & Aaron — April 3, 2026*