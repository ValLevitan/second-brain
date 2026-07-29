# Describing the Cultural Problem in Minsk

**Date:** 2026-03-05
**Based on:** [[Schedule_review-March-4-2026]] transcript analysis
**Author:** Val Levitan (drafted by Claude)

---

## The Problem

Our company is fragmented. The executive branch and market are in North America — itself split across several small offices. Engineering is in Minsk. Covid-era work-from-home deepened this further; what was once a two-location company became a collection of isolated individuals connected only by scheduled calls. Cultural and language barriers between North America and Minsk sit on top of all of this.

The result is that **information flow between North America and Minsk is fundamentally one-directional.** I send directives, requirements, context, and strategic direction toward Minsk. Minsk absorbs it, interprets it, executes, and delivers. What Minsk does not do is reciprocate — no comparable volume of questions, feedback, documentation, or context flows back.

The prevailing attitude is: *"We were told to do that — and here it is — done, as you asked us."*

I call this missing discipline **"hygiene of alignment"** (гигиена согласования) — the proactive, bidirectional exchange that should exist between the people who define *what* to build and the people who decide *how* to build it. Neither tooling nor external expertise will solve this without addressing the underlying cultural asymmetry.

---

## The One-Directional Flow

North America holds market knowledge, customer context, and business strategy. Minsk holds implementation knowledge, technical constraints, and architectural realities. The first is pushed toward Minsk. The second is **not pushed back**.

Even if I increase the volume and quality of documentation flowing to Minsk, the return channel stays silent. Minsk absorbs the input, interprets it internally, and produces output — but the interpretation, the questions that arose, the tradeoffs made, the assumptions applied — none of this travels back. I discover misalignment only when the delivered result doesn't match intent.

I have a saying: **"I do not read minds."** Nobody can. Yet the current dynamic assumes that I should — that I will somehow sense what Minsk interpreted, what tradeoffs they made, what confused them, what they disagree with. This is not a tooling gap. It is a cultural behavior. Information is withheld not out of malice, but because **formulating objections across a language and cultural barrier feels like a daunting task and a distraction** from the "real work" of writing code. The culture needs to shift: if something is on your mind — a concern, a question, a disagreement — it is your responsibility to make your counterpart aware of it. Nobody on the other end can read your mind.

---

## What the Japanese Call Hourensou

Japanese professional culture runs on **Hourensou** (報告・連絡・相談) — Report, Inform, Consult:

- **Report** what happened, what you did, what the result was — without being asked.
- **Inform** colleagues who might be affected — before they discover it themselves.
- **Consult** before making a decision when uncertain — before committing to a path.

The Minsk-to-North-America channel has none of this. After a call ends, nothing comes back. When engineers discover a technical constraint that changes the picture, the discovery stays local. When someone thinks a requirement doesn't make sense, they silently comply with their own interpretation or silently deviate.

Hourensou **reduces the cost of coordination.** Without it, I become a bottleneck interrogator — forced to ask probing questions on every call to extract what should have been volunteered. I do not read minds; I should not have to. Over time, the Minsk team develops what I call an "allergic reaction to conversations" — the interrogation drains them, yet the alternative (volunteering information proactively) never takes its place.

---

## Command Culture vs. Context Culture

I remember a pattern from the Boris era: *"An order came from above. We do it."* That pattern persists as the default operating mode even after Boris.

Netflix calls the antidote **"context, not control"**: leaders provide the *why*, and people make good decisions. But it requires context flowing *both ways*. Our dynamic has neither direction working:

- **Downward:** Even when I provide context, it is received as a command. The *why* is discarded; only the *what* is retained.
- **Upward:** No one says "this feature doesn't make sense" until forced into the conversation. Silence until delivery.
- **Lateral:** Minsk discussions happen, but their conclusions never propagate back to North America.

Amazon learned that people won't read documents on their own — that's why their meetings start with silent reading together. I see the same reality: even a perfect documentation package sent to Minsk would not produce a return flow of questions, concerns, or counterproposals. The problem is not the quality of input; it is the absence of output. Nobody in North America can read the minds of Minsk engineers — but Minsk operates as though we should.

---

## Visibility, Reflection, and the Bus Factor

Toyota calls it **Genchi Genbutsu** — "go and see for yourself." With the company fragmented across offices and home offices on both sides of the Atlantic, there is no "place" left to go and see. And Genchi Genbutsu only works when information also flows *to* leaders proactively. I have neither: I cannot go see, and nothing flows to me.

The Japanese also practice **Hansei** — structured reflection: what did we intend, what happened, what did we miss? Our Minsk team has no reflection loop that reaches North America. Nobody asks "did we understand the requirement correctly?" Nobody surfaces that they went down a wrong path for three days because they didn't ask a clarifying question.
---

## Root Diagnosis

The Minsk engineers are not incompetent or unwilling. The relationship between North America and Minsk operates as a **one-way valve**:

```
Company fragmented across locations and home offices
  -> No organic information exchange remains
    -> Minsk defaults to receive-and-execute
      -> North America has no visibility into interpretation
        -> North America must interrogate to extract information
          -> Minsk experiences calls as surveillance, not collaboration
            -> Minsk retreats further into silent execution
              -> (cycle repeats)
```

Amplifying this: a legacy command culture that normalized "don't ask why, just do"; a cultural and linguistic asymmetry that makes it structurally harder for Minsk to push back than for North America to issue directives; a tool-centric hope that individual documentation will bridge a bidirectional communication gap; and no formal expectation that the return flow of information is part of Minsk's job.

**The lack of hygiene of alignment is the absence of a return channel.** I speak; Minsk listens, interprets, and executes. What is missing is Minsk speaking back — not just delivering code, but delivering understanding, questions, disagreements, and context. I do not read minds, and neither does anyone else in this company. The culture must shift so that making your counterpart aware of what is on your mind is not an afterthought — it is the job. Until that shift happens, no amount of documentation, tooling, or external expertise flowing from North America will close the gap.
