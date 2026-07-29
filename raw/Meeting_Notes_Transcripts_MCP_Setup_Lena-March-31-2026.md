# Meeting Summary — Clayton-Aaron-JVL: Transcripts MCP Setup with Lena
**Date:** March 31, 2026, 2:00 PM (UTC on file; Eastern equivalent ~10:00 AM)
**Duration:** 1h 14m 32s
**Attendees:** Clayton Chancey, Lena Zhukova, Val Levitan

## Summary

The meeting was scheduled to walk Lena through the setup of a new MCP transcripts pipeline Clayton built, and turned into a working session punctuated by Windows/Claude stability issues and an extended philosophical discussion on source-of-truth and hallucinations.

**End-to-end pipeline architecture.** Clayton explained the flow he has stood up:
1. A meeting takes place in Microsoft Teams.
2. After recording/transcript processing, a Microsoft Power Automate script (deployed by Andrei) fires on any meeting and sends the audio + transcript to Clayton's JVL microservice.
3. The microservice pulls the latest glossary from GitHub and runs the raw transcript through a pipeline that produces a more accurate transcription.
4. The refined transcript is automatically uploaded into a GitHub transcripts repository, organized by date.
5. At any time, a user (Lena or Val) can invoke Claude via the JVL Atlassian MCP server (augmented with two new tools: `list transcript` and `get transcript`), which authenticates to the GitHub repo via a Personal Access Token (PAT) with SSO authorization, pulls the right transcript by date/name/participants, and cross-references it with Jira to propose a richer Jira backlog (issues, features, descriptions) for game creation.

Clayton confirmed the pipeline was already live: ~19 hours prior to the call, a meeting recording for Aaron Bockelie had been automatically ingested into the GitHub transcripts repository.

**GitHub PAT setup for Lena (hands-on portion).** Clayton walked Lena through:
- Pulling down the latest MCP tools version.
- Locating the `.env` configuration file for the MCP server (initial confusion — Clayton initially thought he hadn't pushed the updated env template; turned out the file was fine).
- Generating a GitHub classic Personal Access Token in GitHub settings → Developer settings → Personal access tokens → Tokens (classic).
  - Name: `transcripts_MCP`
  - Expiration: 1 year
  - Scope: `repo` (top-level checkbox sufficient)
- Copying the token into the env file after the last equal sign, saving.
- Configuring SSO authorization for the token against JVL core — "Authorize" → "Continue" → "Continue."

**Windows MCP stability issues.** The session was repeatedly disrupted on Lena's Windows setup:
- Claude Desktop failed to relaunch cleanly; Lena reported previously needing full reboots to recover.
- The JVL Atlassian connector showed tool-check-marks inconsistently after restart — `list transcript` / `get transcript` appeared and disappeared between refreshes.
- Lena described the behavior as connect/disconnect cycling with risk of silent disconnection mid-query (the model would then answer without MCP backing, producing irrelevant results).
- Clayton said he had seen morning headlines about MCP tool-registry issues on Windows; could not test himself (he's not on Windows).
- Workaround: Lena switched from the Cowork surface to Chat, and eventually the tool connection re-established.

**Successful end-to-end test.** Once the MCP reconnected, Lena prompted "I want to create a game from last transcript." Claude:
- Found two transcripts from the target date, handled the ambiguity by asking.
- Correctly resolved the game name to "Dragon Pays" by cross-referencing Jira (earlier run had misread it as "paste").
- Proposed Jira changes including adds and updates; feature descriptions were auto-enriched with meeting-notes comments — Clayton noted this comment-enrichment was a feature he had added speculatively and was glad to see working.
- Lena confirmed the meeting-notes-as-description behavior matches how the team actually writes feature descriptions.

**Hardware decision — Mac mini for Lena.** Val asked whether the team needs to migrate off Windows. Clayton said the MCP tools will work substantially better on Linux or Mac, but switching the whole team isn't warranted for this alone. Val proposed ordering a Mac mini specifically for Lena (not the whole team). Lena clarified her team leads Anastasia and Julia also need it since they manage stories. Clayton confirmed: anyone who manages Jira from meeting transcripts via Claude would benefit. Val announced on the call that he was ordering a Mac mini for Lena as they spoke. Val also noted the mini is a cheaper solution than "the whole revolution." Lena's existing custom graphical tools will not work under Linux, but Mac is viable.

**Repository access and security.** Clayton asked: should the transcripts repo be wide-open to anyone with GitHub access, or should some meetings be access-controlled? Val ruled that the transcripts repo should be managed, not wide open, gated through Microsoft SSO. Clayton confirmed GitHub SSO is already in place for this repo — the access Lena's PAT provides is already governed by her SSO.

**Extended discussion: transcripts are not source of truth.** Val's position:
- A transcript is "just a conversation" — the conversation itself can be grossly erroneous, and the entire direction of a long-running conversation can be wrong.
- The only source of truth is ADRs and Requirements. Specific resolutions made in a meeting are not source of truth unless distilled into ADR/REQ form. "Everything else is just speculative conversation."
- Val stated that in his own practice, he mines transcripts exclusively for two things: Requirements and ADRs. Nothing else. ADRs eventually evolve into specifications, timing diagrams, architectural decisions, and tech stack selections.
- Val declared transcript repositories should be restricted to a specific group and should not feed "truth" pipelines directly.

Clayton's framing: transcripts are the **raw material** from which truth is mined. Currently Lena is the "ontological filter" — the human making the correct/incorrect judgment before hitting execute. Long-term, JVL can engineer tools/principles that make that filtering automated; for now, keeping Lena-in-the-loop is the design.

**Extended discussion: hallucination is a user-category, not a model property.** Clayton's position (which he said differs from Aaron's):
- Hallucinations don't exist inside the large language model. A model is not conscious and has no category of truth/untruth; it operates only on what it has.
- "Hallucination" is a human description applied when the model's output doesn't match the human's richer, lived context.
- To reduce hallucinations, one doesn't improve the model — one **engineers the context and the tools** so the model has access to the information that allows it to converge on what humans consider true.
- Hallucination reduction is context-specific engineering work, not model work. Large language models have been capable of zero-hallucination output for nearly a year when the context is properly engineered.
- Clayton jabbed at LLM vendors: "25-year-old computer science people who didn't finish their philosophy electives" anthropomorphize their own technology with the word "hallucination."

Val initially said hallucinations will disappear in a year, then accepted Clayton's framing ("Oh, good point. OK.") after Clayton clarified that the category lives in the user's context excess, not the model. Lena added that she notices the model trying to "fix" her information and claim its interpretation is better — which she recognizes as a hallucination precisely because she has more context.

**Game production is assembly.** Val reframed the work: game creation has three major loops — idea generation (loop 1), game design (loop 2), and game production (loop 3). Clayton and Lena are working on loop 3. Val's view: production is an assembly line, should have "very little creativity," and should move to full automation. Conversations should be automated into tasks, put into Jira, executed efficiently. Goal: eliminate "useful bureaucracy" (Aaron Nye's phrase) so the team spends the least time on it.

**Next steps Clayton articulated.**
- Add Teams chat interleaving into the pipeline. Users paste requirement links and relevant content into chat during meetings; without chat in the pipeline, that context is lost. This requires a change to Clayton's microservice and likely a small change to Andrei's Power Automate script; Andrei has been very responsive.
- Do light research on Windows MCP stability, though given Lena's Mac mini is coming, this is no longer the critical path.
- Set up a separate session with Val to configure Val's own MCP transcripts access.
- Lena to complete Mac mini setup when the hardware arrives; images workflow will "just work" on Mac.

## Decisions Made

- **Transcripts repository is access-controlled, not wide open, gated via JVL Microsoft SSO.** (Val) GitHub SSO is already enforced on the repo via the PAT + SSO flow.
- **Source of truth is ADRs and Requirements only — not transcripts, not meeting resolutions.** (Val) Transcripts are raw material for mining; the mining targets are ADRs and REQs.
- **Mac mini to be ordered for Lena (and by extension Anastasia and Julia on her team).** (Val — placed order live on the call) Team-wide OS migration is NOT warranted; the mini is a targeted solution.
- **Pipeline Next: incorporate Teams chat messages into transcript processing.** (Clayton, with Lena's endorsement) Required because chat links to requirements are a natural input channel for descriptions.
- **Separate session needed for Val's own MCP transcripts setup.** (Val/Clayton) Today's focus was Lena.

## Engineering Signals

### Confirmed Signals

- **ADR: Transcripts are not source of truth; ADRs + Requirements are.** Val declared this unambiguously. Downstream tools/pipelines must not treat transcripts as ground truth; they are raw material. The ontological layer for "truth mining" is a separate design space.
- **ADR: Transcripts repository access is SSO-governed, not public.** Confirmed closed by Val's decision. Access controlled via Microsoft SSO / JVL GitHub SSO enforcement on PATs.
- **CAP: MCP-driven transcript-to-Jira game creation pipeline.** End-to-end: Teams recording → Power Automate (Andrei) → Clayton's microservice with glossary enrichment → GitHub transcripts repo → MCP server (`list transcript`, `get transcript`) → Claude → Jira proposals with glossary-aligned naming and meeting-notes-as-description.
- **CAP: Glossary-driven transcription refinement.** The microservice pulls the latest GitHub glossary and applies it to transcription; terminology keys at the end of each refined transcript can feed back as pull requests to the glossary repo (a feedback loop Clayton flagged as a future enrichment).
- **REQ: Teams chat interleaving in transcript pipeline.** Lena explicitly stated chat links to requirements are used in practice; Clayton committed to adding this. Ongoing dependency on Andrei's Power Automate script for the Teams-side capture.
- **CAP: Feature description auto-enrichment with meeting-notes comments.** Confirmed working in the live test; Clayton had added this speculatively.

### Suspected Signals

- **Possible ADR: Hallucination reduction is a context/tools engineering problem, not a model problem.** Clayton argued this explicitly and Val accepted the framing. This is a philosophical/design-principle level statement that may warrant a formal ADR since it shapes how JVL invests in MCP tooling and scaffolding vs. chasing model upgrades. *Val, does this warrant a formal ADR?*
- **Possible ADR: Game production is an assembly line / loop 3 should be fully automated.** Val articulated the three-loop decomposition (idea / design / production) and stated production should be fully automated with minimal creativity. This is a strategic architectural statement about the game-development SDLC. *Val, track as ADR or strategic principle?*
- **Possible REQ: Terminology-key feedback loop to glossary repo.** Clayton raised this as a future capability — terminology keys surfaced at the end of each refined transcript become PR candidates against the glossary, reviewed by someone who knows the slang. Not yet committed. *Val, track?*

## Open Questions

- Windows MCP tool-registry stability — Clayton to research, but deprioritized now that Lena is moving to Mac. Remaining relevance: Clayton has another (non-JVL) client stuck on Windows.
- Exact next-meeting date — Clayton referenced "Thursday" for target completion of chat-interleaving feature, contingent on Andrei's responsiveness.
- Timing and scope of Val's own MCP setup session — TBD.
- Who on the team besides Lena, Anastasia, and Julia may need Mac hardware for this workflow — not formally bounded beyond "anyone who manages Jira from transcripts via Claude."

---
*Processed from Teams transcript on April 13, 2026*
*Source meeting: Clayton-Aaron-JVL — March 31, 2026*
