# Semantic Understanding — Detailed Initiative Summary
**Version:** 1.2
**Date:** March 22, 2026
**Sources:** Clayton-Aaron-JVL meeting transcripts from March 13 and March 19, 2026

---

## 1. Background and Problem Statement

JVL's development team — largely based in Minsk — conducts meetings in Russian. However, the spoken language is not standard Russian. It is a dense mixture of:

1. **Conventional modern Russian** — baseline spoken language
2. **English technical vocabulary used verbatim** — terms like "Spine," "IP," "framework," "build," "branch" are spoken in English even within Russian sentences. Developers would never say these words in Russian; they use the English form with Russian verb conjugations attached.
3. **Russian-ified English slang** — English words phonetically adapted into Russian grammar. These are not dictionary words in either language. They are workplace shorthand that evolved organically within the team.
4. **Legacy/colloquial expressions** — older Russian expressions, sometimes Soviet-era idioms, non-standard usages that do not appear in modern Russian language models.

The core problem: **Microsoft Teams transcription explicitly does not support Russian.** When it encounters this mixed-language input, it:
- Correlates Russian-sounding words to Latin loanwords (a Whisper API behavior)
- Translates those Latin approximations back into English
- Produces transcripts that are unintelligible
- Loses context rapidly, and the errors compound sentence by sentence

Even Microsoft Copilot's custom dictionary feature — intended for domain-specific terms — does not support Russian.

Lena confirmed: "It's not only these terms which we are saying in Russian — some English words — but it's even not a good transcript for just normal Russian." The transcription fails on two levels: the slang is mangled, and even standard Russian is poorly handled.

---

## 2. Why This Matters

**English is the programming language of JVL.** All output — code, documentation, transcripts, specifications — must be in precise, grammatically correct English. This is not just a preference; it is an operational requirement because:

- The company is actively attracting non-Russian-speaking staff — the output cannot assume a Russian-speaking audience
- All engineering artifacts (JIRA tickets, GitHub commits, specifications, ADRs) are written in English
- Claude Code and other AI tools work best when prompted in English
- Compliance and regulatory documentation (Nebraska, South Dakota, Georgia) must be in English

However, the *input* — the meetings where decisions are made, problems are debugged, and designs are discussed — happens in Russian with heavy code-switching. The gap between what is spoken and what is recorded is where critical institutional knowledge is lost.

The team in Minsk, while technically strong, sometimes struggles to express themselves precisely in English when writing prompts for Claude. The prompts become butchered when engineers force themselves into a language they're not comfortable with. The semantic understanding pipeline addresses this by accepting Russian input and producing clean English output.

---

## 3. Lena's Existing Workaround (Pre-Pipeline)

Before Clayton's pipeline, Lena had developed a manual process:

1. Record the Teams meeting
2. Extract the audio as an MP3 file
3. Upload to **Turboscribe** (third-party transcription service) — produced an "OK, much better than Teams" transcript
4. Take that improved-but-imperfect transcript plus her **taxonomy vocabulary spreadsheet** and load both into Claude
5. Claude produces an "almost perfect" result — "several mistakes, but almost perfect"

This process works but has drawbacks:
- It is manual and time-consuming
- Turboscribe is a third-party service — IT flagged security concerns about uploading meeting audio to an external free service
- The taxonomy spreadsheet must be manually maintained and provided each time
- It requires Lena's expertise at every step

---

## 4. The Pipeline Architecture (Clayton's Solution)

Clayton designed a multi-stage pipeline that automates and improves on Lena's manual process:

### Stage 1: Dual-Source Transcription
- **Input A:** Raw audio (extracted from Teams recording or separate recorder)
- **Input B:** Microsoft Teams transcript (bad content, but accurate speaker diarization — it knows *who* said *what* and *when*)
- **Whisper API** processes the audio with the JVL taxonomy loaded as prompt context (limited to ~200 terms due to Whisper's prompt word limit)

### Stage 2: Transcript Merge
- The Whisper transcript has good content but no speaker identification (it's just audio)
- The Teams transcript has bad content but correct speaker names and timestamps
- Claude merges these: takes the accurate text from Whisper and the accurate speaker/timestamp metadata from Teams

### Stage 3: Post-Processing with Claude
- Claude receives the merged transcript plus the full taxonomy/glossary
- Translates and normalizes all content into grammatically correct English
- Handles transliterated terms (e.g., "PRIVYET" written in Latin letters)
- Resolves ambiguous terms using meeting context and the taxonomy
- Identifies people and places referenced by nicknames or Russian informal names (e.g., "Vladimir Avdev is Black" — a nickname used in Russian conversation)

### Key Technical Insight (Clayton):
The reason Teams fails is that all transcription services (Teams, Copilot, Turboscribe) use the **Whisper API** under the hood. Whisper's attention mechanism, when encountering Russian words it doesn't recognize, tries to correlate them to **Latin loanwords** — a strange intermediate step where Russian phonemes are mapped to Latin roots and then back to English. This produces nonsense.

The fix is to run Whisper **multiple times** with different language hints. If the same term comes back uncertain across multiple passes, it's flagged as a domain-specific term that needs the taxonomy to resolve. This multi-pass approach produces much better raw material for Claude to work with.

### Where the Pipeline Lives
- Designed to run locally (MCP server on developer's device) — not a cloud service
- The taxonomy/glossary will be stored in **GitHub** so it can be pulled down programmatically
- Clayton's plan: "I can just bake that into the MCP server in a way that if it's processing a transcript, it's just in the MCP and it can pull it down from GitHub"

---

## 5. The Taxonomy / Glossary

Lena created a **taxonomy vocabulary spreadsheet** that maps:
- Russian slang terms → proper English equivalents
- Russian-ified English → standard English
- Team nicknames → actual names
- Domain-specific abbreviations → full terms

This taxonomy is the critical artifact. Val's position: "I prefer to have our own slang to English document." Clayton agreed: "We need that no matter what."

### Current State
- Exists as an Excel spreadsheet maintained by Lena
- Has been tested with both Turboscribe and the Whisper pipeline
- Clayton reported it significantly improves Whisper's transcription accuracy when loaded as prompt context
- Limited to ~200 words as direct Whisper prompt — the full taxonomy is used by Claude in post-processing

### Target State
- Stored in GitHub as a structured document (not a spreadsheet)
- Versioned and maintained as a living reference
- Automatically consumed by both the Whisper pipeline and the Claude post-processing stage
- Clayton on naming convention in GitHub: "Whatever you guys generate... I'll just pull it down, whatever's in GitHub, I'll just pull it down and that becomes part of the process"

---

## 6. Key Debates and Decisions

### Transliteration vs. Translation in Output
**Debate (March 19):** Should the output transcript include annotated transliterations — showing the original Russian/slang term alongside the English translation — or should it produce English-only output?

Clayton initially built the pipeline to annotate: showing the phonetic Russian term in brackets alongside the English translation (e.g., translating "IP" and adding the Cyrillic phonetics).

**Lena's objection:** Some terms like "IP" or "Spine" are *always* used in English by the developers, even when speaking Russian. Transliterating them into Cyrillic is counterproductive — "this word they would never use in Russian. They would put IP like English letters."

**Val's decision:** Output must be in "precisely literate, grammatically correct English" with no Russian annotations. Reason: "I'm not sure that the developers will remain Russians. We're actively attracting non-Russian-speaking people." The output must be universally readable.

**Resolution:** Pipeline updated to produce English-only output, no transliteration annotations.

### Security of Third-Party Tools
**Concern (March 13):** Lena mentioned IT flagged Turboscribe as potentially insecure — "it's free, it's online, it might keep our files somewhere."

**Clayton's response:** Turboscribe uses the same Whisper API as everything else. But a self-hosted solution (local MCP server) eliminates the concern entirely since audio never leaves the device.

### Input Language for Claude Prompting
**Discussion (March 19):** Should developers prompt Claude in Russian or English?

**Clayton's position:** Developers should feel free to prompt in Russian — "that's actually how you're going to express exactly what you want." The taxonomy then serves as a bridge, mapping Russian prompts to correct English context.

**Val's position:** The *output* must always be English — "the best programming language on Earth today... is English." But the input can be in whatever language allows the developer to express their intent most clearly.

**Lena's observation:** Developers who aren't fluent in English produce "butchered" prompts that confuse Claude. Russian input → English output may actually be more effective.

---

## 7. Pipeline Test Results (March 19)

Clayton ran the pipeline against a real game development meeting transcript:

**What worked well:**
- Whisper, prompted with the taxonomy, transcribed Russian and slang "pretty well"
- The merge of Whisper content + Teams speaker diarization produced accurate attributed text
- Lena's spot-check: "it actually understood correctly" — even for mixed English/Chinese/Russian terms (e.g., "Singlish Fortune")
- Turboscribe comparison: pipeline output was competitive, with the advantage of being self-hosted and automated

**Issues found:**
- **Participants section:** Claude's post-processing was adding people mentioned *in conversation* to the participants list, not just actual meeting attendees. E.g., if someone said "Vladimir told me...", Vladimir appeared as a participant. Clayton: "I need to give Claude a little bit more freedom... but that I can fix, it's easy."
- **Speaker diarization dependency:** The pipeline requires the Teams transcript for speaker identification. Without it, Whisper produces good text but doesn't know who said what.

**Lena's verdict:** "I think it's working pretty good."

---

## 8. Outstanding Actions and Next Steps

| Action | Owner | Status |
|--------|-------|--------|
| Remove transliteration annotations from pipeline output | Clayton | Done (March 19) |
| Fix participants section — only actual attendees | Clayton | In progress |
| Run pipeline on second test case (Lena to provide MP3 + Teams transcript) | Clayton + Lena | Lena recording new sample |
| Store taxonomy in GitHub for programmatic access | Clayton + Andrei | Pending — Andrei involved in GitHub structure |
| Validate pipeline output against manual Turboscribe + Claude process | Lena | Ongoing |
| Determine automation trigger — how does a meeting recording enter the pipeline? | Clayton | Exploring — ideally auto-triggered from Teams recording |
| Explore Microsoft Power Automate for triggering pipeline on new recordings | Clayton | Discussed March 19 |
| Expand taxonomy with terms from new test transcripts | Lena | Ongoing |
| Produce side-by-side comparison: pipeline vs. manual process | Clayton | Planned |

---

## 9. Architecture Diagram (Conceptual)

```
┌─────────────────┐     ┌──────────────────────┐
│  Teams Meeting   │────▶│  Teams Transcript     │ (bad content, good speakers)
│  (Recording)     │     │  (.vtt / export)      │
└────────┬────────┘     └──────────┬───────────┘
         │                         │
         ▼                         │
┌─────────────────┐                │
│  Audio Extract   │                │
│  (MP3)           │                │
└────────┬────────┘                │
         │                         │
         ▼                         │
┌─────────────────┐                │
│  Whisper API     │                │
│  + taxonomy      │                │
│  (multi-pass)    │                │
└────────┬────────┘                │
         │                         │
         ▼                         ▼
┌──────────────────────────────────────────┐
│  Claude Post-Processing                   │
│  • Merge Whisper text + Teams speakers    │
│  • Apply full taxonomy/glossary           │
│  • Translate to grammatically correct EN  │
│  • Resolve transliterations               │
│  • Normalize names and references         │
└────────────────────┬─────────────────────┘
                     │
                     ▼
┌──────────────────────────────────────────┐
│  Final Transcript (.md)                   │
│  • English only                           │
│  • Speaker-attributed                     │
│  • Timestamped                            │
│  • Stored in Obsidian / central repo      │
└──────────────────────────────────────────┘
```

---

## 10. Val's Guiding Principles for This Initiative

Extracted from both meetings:

1. **"I prefer to have our own slang to English document."** — The taxonomy is a JVL-owned knowledge asset, not something delegated to a third-party tool.

2. **"The best programming language on Earth today is English."** — All output must be in English. This is non-negotiable.

3. **"I'm not sure that the developers will remain Russians."** — The solution must not assume a Russian-speaking audience. It must produce universally readable output.

4. **"Leave it in that analog audio form... and Claude decides what to do with it."** — Don't over-process at the transcription stage. Let the AI handle interpretation in context.

5. **"The moment you start using slang, it's just wild."** — The quality difference between a raw Teams transcript and one that has been cleaned through the taxonomy is dramatic. The slang-to-English mapping is the highest-value artifact.

6. **"We want to timestamp them based on UTC."** — Transcripts should use UTC timestamps so they can be sequenced across time zones and serve as a reliable record.
