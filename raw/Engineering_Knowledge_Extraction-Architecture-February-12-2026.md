Subject: Re: From Meetings Transcript to Engineering Knowledge Base

Pavel, Dmitri, Andrei,

Thank you for the reworked document, Pavel. The multi-faceted labeling taxonomy you added — Product, Domain, Concern, Decision Status, and Cross-cutting Dependencies — shows good thinking about how to organize what comes out of our transcripts. The controlled vocabulary point is especially important.

However, I want to caution against implementing the tagging system as described. Before we commit to tags, I'd like the team to evaluate a graph-based approach instead.

Here's the difference in simple terms. Tags put labels on things — a meeting gets tagged "flex-pos" and "architecture." But those labels don't know anything about each other. A graph stores relationships — it knows that a decision made in one meeting depends on a decision from a different meeting, that a particular system change affects three other systems, and that an open question from January is the same problem being discussed again in March under different words.

Tags answer the question "show me all meetings about flex-pos." A graph answers the question "show me everything downstream of the auth service decision and who is affected." For engineering knowledge management, the second question is far more valuable.

I'm not saying tags are wrong — they may end up being part of the solution. But I'd like you to think about graph-based relationships as the primary structure before we lock into a flat tagging model. Please come back with your assessment of both approaches.

Next, I want to address how we decide what moves from our knowledge base into Jira and what stays as reference.

The original rule was: if an ADR implies work, it goes to Jira. If it's just a decision record, it stays in GitHub. In practice, that line is blurry. Many decisions might imply work, or might not. Open questions aren't decisions at all, but someone still needs to drive them to resolution.

I'd like to suggest a simpler rule: the question is not "does this imply work?" but "does someone need to be accountable for this?" If the answer is yes — if a name gets attached — it goes to Jira with proper tracking. If no one needs to own it right now, it stays in GitHub as reference.

That leads to a second problem. Items that stay in GitHub with no owner can accumulate silently. Some of them will naturally resolve or become irrelevant — those should get archived over time, with their references to meetings and decisions still intact. But some of them won't go away. They'll keep appearing in meeting after meeting, discussed but never resolved, never assigned to anyone.

Those recurring themes are a signal. If the same topic surfaces across multiple transcripts without an owner, the system should detect that and bring it to your attention, Pavel. Think of it as an automatic flag: "Your team has discussed terminal authentication flow in five meetings over three weeks and nobody owns it." A simple weekly report of recurring unowned topics would work.

Items that stop appearing in new transcripts get archived. Items that keep appearing get surfaced until someone either assigns them or consciously decides they're not actionable.

I'd like to hear your ideas on how to implement this surfacing mechanism — especially how the system would recognize that different conversations are circling the same underlying issue even when the wording is different. This is actually one area where a graph approach may have a clear advantage over tags.

On the broader architecture: our long-term direction should be ecosystem-independent. The production version of this pipeline should not depend on Microsoft or Google. If we switch meeting platforms tomorrow, nothing downstream should break. For the proof of concept, using Teams recordings and Teams transcription is fine — they already exist and there's no reason to build new infrastructure just to test whether the extraction works. But keep in mind that anything we build should be designed so the meeting platform can be swapped out later without rebuilding the pipeline.

With all of that as context, I'd like the team to propose how you'd approach a proof of concept. What would the scope be, what tools would you use, how many transcripts would you test with, and what does the timeline look like? I have my own thoughts, but I'd rather hear yours first.

Finally, I still need answers to the four items from my original email:

1. Confirm where meeting recordings and transcripts currently live and whether they can be accessed programmatically.
2. Your assessment of the overall approach — does it make sense, what would you change, what's missing?
3. A proposed architecture if you agree with the direction, or an alternative if you don't.
4. A scope estimate for the proof of concept.

Looking forward to the discussion.

Val
