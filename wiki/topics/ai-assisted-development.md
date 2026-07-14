---
type: topic
title: AI-assisted development adoption
date: 2026-07-12
aliases: [AI-assisted development, Cline, MCP adoption, AI coding tools, Anthropic, Norcross, Copilot, meeting tracking, GPT-4o Transcribe, Whisper]
source-count: 10
---

# AI-assisted development adoption

JVL's push to get its engineers using AI coding tools. Aaron led a hands-on workshop on Jan 14 2025 with the Minsk team (Pavel, Andrei, Anton, Sasha); Val framed it as a company direction, tied to the build-pipeline debate the day before.

## The tools shown

- **Visual Studio Code** as the editor, with two AI tools: GitHub **Copilot** (built in) and **Cline** — an Anthropic-based agentic coding tool (spelled "Climb"/"Clang"/"Klein"/"C-line" in the transcript). [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- **OpenRouter** to abstract API access to many AI models (skims ~10% and gives access without per-model rate limits); Andrei distributed OpenRouter API keys. The model used was Anthropic Claude 3.5 Sonnet (~$3 per million tokens, supports images, computer use, prompt caching). [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- **Model Context Protocol (MCP)** servers: Aaron built a Bitbucket MCP server live from a TypeScript template so the AI could talk to Bitbucket directly (code reviews, pull requests). He noted MCP could also talk to the local gaming server (LGS). [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Key lessons Aaron taught

- Two usage modes: **bootstrapping** (start something from nothing, get a prototype in hours) and **iterating** (gradually improve an existing codebase). [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- The **"maximizer" / paperclip** warning: AI tools over-optimize the task you give them — infinitely refactoring, writing giant monolithic modules, or breaking working code. The engineer's job is to steer it ("the AI is the horse"). [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- The **70% problem / paradox of knowledge**: senior developers use AI to accelerate what they already know; juniors use it to learn what to do. QA engineers are "juniors" here, and the tools can help them learn Git through repetition. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- The **`.clinerules`** file gives the AI standing instructions for a project; keep guidelines minimal (an MVP approach) rather than over-detailed and brittle. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Bigger, more monolithic codebases are harder for the AI (and humans) to work with — a reason to keep modules small and documented. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## The business case Val made

- Val wants a **leader** on MCP/AI tooling — someone who learns it better than Aaron and leads JVL there, with financial reward for whoever takes it on. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Cost model: competent AI use could save at least ~20 hours/month per developer; across 10 developers that's ~2,000 hours/year — roughly one employee. JVL frames this as scale-up capacity, not headcount cuts. Val said he personally dropped a personal assistant and a receptionist by being more efficient. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Homework: don't commit AI-generated code to the real codebase yet — instead use the tools to read/explore a familiar codebase (Sasha → Omni framework / LGS, Anton → RGS, Andrei → build/Kubernetes scripts) and produce a `docs/` folder documenting it. A follow-up MCP session was offered. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- Participants included **Anton** ([[wiki/people/anton-leshkevich.md|Anton Leshkevich]], JVL Minsk engineer), whose repo access worked throughout the session and who received an OpenRouter API key from Andrei; Aaron suggested he try the tools on the RGS codebase. [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]

## Val's personal knowledge-base method (Jan 20)

Coaching Andrei, Val described the workflow he uses himself and wants his managers to adopt: record every meeting (any language — ChatGPT moves between Russian/English easily), turn it into a transcript, feed it to ChatGPT, have it summarize and propose a title and ~20 tags, pick the tags to use, tell it to update memory, and derive a taxonomy — then circulate the conversation. This lets someone with limited English/vocabulary produce a correct taxonomy through dialogue with the AI. Val frames refusing to adopt these tools as a 1990s "knowledge-tribune" mindset he will progressively replace. Aaron separately demoed using Claude prompt styles ("explanatory", "intellectual dissector") to draft and critique JIRA features — see the DTP-53 section of [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/github_organization-jan-20-2025.md]]

## AI in the CD pipeline and a data project (Jan 21 / Jan 30)

- On the Jan 21 continuous-delivery call, Aaron demoed generating Terraform, a Docker file and even tests for a "Hello World" AWS deployment using AI (Claude / Anthropic under the hood), arguing it lets JVL reach a first result in ~a day. See [[wiki/topics/continuous-delivery-pipeline-architecture.md]]. [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- On the Jan 30 recap, Andrei Klimovich raised a data-collection MVP ("Norcross"/"North Cross") that would use Anthropic; a candidate developer (Sergei) and a Minsk studio (€40/hr) were both interested in learning Anthropic. Val said he does not want to pay for anyone's Anthropic learning curve. See [[wiki/people/andrei-klimovich.md]] (and Owner Decisions on Sergei). [[raw/Recap with Andrei Klimovich - January 30, 2025.md]]

## Meeting-tracking with GitHub as source of truth (Feb 17)

- Val described what he wants to build (and which prefigures this second brain): tag each meeting conversation by subject/feature, then use AI to show a subject's **evolution** across meetings — is it progressing, stuck, is there a commit against it? He insisted the **source of truth is the code**: "the only source of truth is the code, and eventually a release of a feature… nothing else brings money, everything else only burns money." His cost argument: five people at $100/hr across five one-hour meetings is $2,500 — against zero commits, that's "$2,500 burned with 0 commits." [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]]
- Aaron connected this to the **GitHub MCP tool** (a container that lets the AI create branches/repos/PRs/CI and set permissions) alongside a Google Workspace tool, so Val could ask "how is project X doing, how many commits this week?" and have the AI report developer performance and even draft the follow-up email. Val added he is indifferent to Office 365 vs Google Workspace ("I'm happy to move to Google") — it's just a communications platform. [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]]

## Cloud file architecture — "engineer Val vs user Val" (Feb 17)

- Val wanted his Git working repository against **OneDrive** instead of the local OS drive, to avoid being laptop-dependent and work across devices. Aaron's coaching: think as a **DevOps engineer, not a user** — treat your work as a product where "engineer Val" creates and "consumer Val" consumes. Rather than syncing the original Git repo to OneDrive, **publish** distilled/consumable copies (a PDF, a web page, Word distillations) to OneDrive; keep **GitHub as the source of truth** and make it easy to stand up the same dev environment on any device. [[raw/cloud_file_architecture_transcript_aaron-2025-02-17.md]] [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]]

## Copilot and shared AI accounts for the whole team (Feb 18)

- On the Feb 18 Git-LFS onboarding session, Aaron pushed to enable **GitHub Copilot** ("like ChatGPT for anything in VS Code") for everyone; on the enterprise plan it needs paid seats at ~**$19/month** (Business). Val questioned the cost and who would use it; Aaron said everybody should. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- Andrei confirmed he already uses **Cline + OpenRouter** in his own work and can teach the graphics team; the team agreed to use **one shared OpenRouter account** (it shows only aggregate, not per-user, activity — "we don't need 40 accounts"). Val's aim: onboard at least half the graphic department (like Lena and Dima) to commit their large assets themselves via Git LFS. See [[wiki/meetings/2025-02-18-git-lfs-vscode-onboarding.md]]. [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]

## MCP to automate engineering work — "replacing Pavel" (Feb 21)

- In a short Feb 21 call, Aaron extended the MCP idea to **automating an engineer's role**. The simplest MCP is point-to-point (the AI sees raw API endpoints and connects the dots), but you can build **flows/actions with business logic inside the MCP** — e.g. a single "deploy a new machine to an environment" or "reconfigure" tool that internally calls many endpoints and reports each step. The step-by-step flow a person like [[wiki/people/pavel.md|Pavel]] follows to make something work can be baked into an MCP, giving "an AI tool orchestrating the actions Pavel was doing." Aaron noted CI/CD build automation in GitHub follows the same convention, so the same pattern applies to integrating assets, deploying SQL, scaling environments, or configuring Kubernetes. [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]

## ChatGPT as a self-teaching tool for Git (Feb 21)

- On the Feb 21 LFS session Val and [[wiki/people/andrey-bosik.md|Andrei]] both pushed the team to **learn Git by thinking, not by following step-by-step instructions** — using YouTube and especially **ChatGPT** as the tutor. Val's method: when stuck on Git, screenshot the problem into ChatGPT and ask it to "explain it in a primitive way," give the next step, or "explain the philosophy of why this is a structure." This is the same self-teaching stance behind onboarding the graphics team. See [[wiki/topics/docs-as-code-and-atlassian-exit.md]]. [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]

## Transcription tooling — Whisper → GPT-4o Transcribe (Mar 21)

- Aaron's existing transcription tool is built on OpenAI **Whisper** (run as an MCP: `whisper transcribe .` over a directory). On Mar 21 he flagged OpenAI's **GPT-4o Transcribe** and **GPT-4o Mini Transcribe** models, released the day before and shared by his colleague [[wiki/people/clayton-chancey.md|Clayton]] — API-only (not usable in the ChatGPT web UI), a large context window, better word-error-rate and language recognition than Whisper, longer file support, and crucially **speaker diarization** (labelling speaker A/B/C) which Val had been asking for. Aaron proposed **rebasing the tool from Whisper onto GPT-4o Transcribe**. [[raw/aaron_building_tools-march-21-2025.md]]
- **Whisper file-size limit:** ~140 of Val's audio files are too large for the current endpoint (a **file-size**, not duration, limit). Aaron may build a **splitter** (convert to a byte stream, split in half); Val's interim workaround is to **stop recording at one hour** and start a new recording. [[raw/aaron_building_tools-march-21-2025.md]]
- This transcription work is the front end of the broader knowledge-base tool — see [[wiki/topics/transcript-knowledge-base-tooling.md]] — and is the "first real tool" in the funding arrangement [[wiki/decisions/2025-03-21-fund-aaron-clayton-bespoke-ai-tools.md]]. [[raw/aaron_building_tools-march-21-2025.md]]

## Connection to the pipeline debate

- Val explicitly linked adopting Git-native, AI-friendly practices to resolving the ISO build-pipeline problem: a natural-language/AI interface should be a standard part of a pipeline built to last 10 years. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]

## Sources

- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
- [[raw/github_organization-jan-20-2025.md]]
- [[raw/continues_release_infrastructure_architecture_2025-01-21 1.md]]
- [[raw/Recap with Andrei Klimovich - January 30, 2025.md]]
- [[raw/detailed_transcript_meeting_tracking_and_AI_Integration-feb-17-2025.md]]
- [[raw/cloud_file_architecture_transcript_aaron-2025-02-17.md]]
- [[raw/GitHub_Commit_LFS-Feb-18-2025.md]]
- [[raw/Call_with_Aaron_Bockelie_2025-02-21.md]]
- [[raw/GitHub_commit_of_LFS_demo_by_Lena_2025-02-21.md]]
- [[raw/aaron_building_tools-march-21-2025.md]]
