---
type: topic
title: AI-assisted development adoption
date: 2026-07-12
aliases: [AI-assisted development, Cline, MCP adoption, AI coding tools, Anthropic, Norcross, Copilot, meeting tracking, GPT-4o Transcribe, Whisper, Unity MCP, Sonnet 3.7, Open WebUI, Docker, CUDA, Watchtower]
source-count: 16
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

## VS Code + MCPs, and a Unity MCP (Mar 26)

- Aaron introduced a new **Unity MCP server** (one of several then appearing; a "leading one" — brand not stated). An MCP is a layer between a data source (Unity, SQL, a weather station, Jira) and the AI that presents a unified set of tools/resources; the AI can call, e.g., a `get assets` tool that reaches the Unity API and serialises assets back as text. Beyond *reading*, the Unity MCP can **set** state — create and place objects/shapes in a scene automatically — and, because it runs in VS Code with the Git repo context, could combine with **Miranda** to pull library assets and lay out scenes on request. [[raw/mcp_unity_visualcode-march-26-2025.md]]
- Aaron's own stack of MCPs (the model he holds up): **Atlassian, Anthropic "Cloud" (i.e. Claude), Microsoft 365, GitHub, Whisper** — used through a human-language interface. (The transcript renders Claude as "Cloud"/"Cloud AI"; recorded as such, likely a mis-transcription of "Claude.") [[raw/mcp_unity_visualcode-march-26-2025.md]]
- **Val's directive:** the team should keep using VS Code with these integrations and prefer **Anthropic Claude with Sonnet 3.7** (called "considerably better than ChatGPT" for many cases) over ChatGPT; before the **April 9** meeting everyone must install the **GitHub MCP** and **Anthropic "Cloud" (Sonnet 3.7)** and run them through **OpenRouter** (JVL has an auto-refill corporate-card subscription). That meeting was extended 30 min (start **9:00**): Val will test each person's VS Code + MCP usage, then the GitHub portion. Team members already trying it: Lena, Yuli, Nastya, Dima Khandov. [[raw/mcp_unity_visualcode-march-26-2025.md]]

## Self-hosted Open WebUI + the good-vs-bad MCP lesson (Mar 27)

- On Mar 27 [[wiki/people/aaron.md|Aaron]] screen-shared and walked Val through configuring a self-hosted **Open WebUI** instance running as a local server on Val's laptop (localhost:8080) — a multi-model LLM chat UI. He toured its settings: themes, a **system prompt**, **memory** (turned on), audio TTS/STT, per-user API-key connections, model list (turn off the dated duplicate models to declutter), document handling (PDF image extraction, embedding model, full-context mode), **web search** (enabled with **DuckDuckGo**, chosen because it needs no API key), a code-execution sandbox, image generation (OpenAI / ComfyUI / Stable Diffusion, Dall-E 3), and a database export. See [[wiki/meetings/2025-03-27-openwebui-aaron-setup.md]]. [[raw/OpenWebUI_aaron_march-27-2025.md]]
- **Multi-user / JVL deployment angle:** Aaron flagged that Open WebUI is built as a **multi-user** system and can connect to an **LDAP / Active Directory** identity server — so it could be hosted on **JVL's infrastructure** (not Val's laptop) and give every JVL user an account with API keys, **replacing individual ChatGPT accounts**. [[raw/OpenWebUI_aaron_march-27-2025.md]]
- **Both providers behind one UI:** the speech-to-text engine was switched from **Whisper (local, slow)** to OpenAI **Whisper-1** using Val's own API key (the same endpoints as Aaron's Whisper service). Aaron imported the community **Anthropic** function so Open WebUI can serve **both Claude and GPT models at once** — needing an Anthropic API key with console billing set up. [[raw/OpenWebUI_aaron_march-27-2025.md]]
- **OpenAI adopts MCP:** Aaron noted OpenAI had just announced it will incorporate **MCP** into all its products (adopting the Model Context Protocol as its tool-use standard) and had significantly improved its image generator; he demoed GPT-4o's precise image generation (a dimensionally-correct fence elevation from a prompt). Val remarked he now uses natural language for ~**60–80%** of his tasks. [[raw/OpenWebUI_aaron_march-27-2025.md]]
- **The good-vs-bad MCP lesson:** Aaron taught three levels of MCP-server design using JIRA as the example — (1) a **lazy** MCP that just exposes each raw API endpoint as its own tool (100 endpoints → 100 tools); (2) a **consolidated** tool (e.g. one "manage JIRA issue" tool with transition/comment/edit sub-operations); (3) a **stateful** server that remembers context and offers the AI a suggestion (e.g. "you last searched this JQL — save it as a filter?") so the AI just says "yes" instead of regenerating everything. A good MCP does the work internally in the developer's best order; a bad one forces the user to read the docs and think through every step. [[raw/OpenWebUI_aaron_march-27-2025.md]]

## Open WebUI — the Docker/CUDA install session (Mar 26)

A separate, earlier hands-on session shows the **installation** of Open WebUI that the Mar-27 configuration tour (above) then built on. [[wiki/people/aaron.md|Aaron]] screen-shared and walked [[wiki/people/val-levitan.md|Val]] through standing it up on Val's laptop; see the date note on [[wiki/meetings/2025-03-26-aaron-knowledge-visualization-openwebui.md]]. [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]

- **Setup mechanics:** Aaron shared a GitHub **gist**; they created a `Docker/OpenWebUI` folder, ran **`git init`** (Aaron using the moment to teach Val what a Git repo is via `ls -la` / the `.git` directory), opened **VS Code**, created a **`docker-compose.yaml`** (first mis-named `.yml`, then renamed), pasted the gist (removing the `version:` line), and ran **`docker compose up -d`** (detached). [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]
- **The compose file:** pulls the **`open-webui:cuda`** image (the GPU-accelerated build); container name **OpenWebUI**, **restart-unless-stopped**; a Docker-managed volume **`OpenWebUIData`** mapped to **`/app/backend/data`** for persistent data; env `NVIDIA_VISIBLE_DEVICES=all`. **Watchtower** keeps the image auto-updated. It is a **~3 GB+** open-source image needing no payment/licensing. [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]
- **Why the GPU:** loading documents into **Retrieval-Augmented Generation / a vector database** is computationally intensive (every document is decomposed and the relative scores of all its words computed), so they installed the **NVIDIA Container Toolkit** + **CUDA drivers** (`cuda-toolkit`) and configured Docker's NVIDIA runtime, to use the laptop's built-in GPU; a reboot was needed after the driver install. [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]
- **Hosting angle:** Aaron noted this is the kind of service that might run better in **a more central location than the laptop** — Val could ask **"Andrea"** (transcribed; likely [[wiki/people/andrey-bosik.md|Andrei Bosik]], DevOps — flagged) to set it up in JVL's **AWS cluster or Azure** — consistent with the Mar-27 multi-user / Active-Directory deployment idea above. [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]

## Connection to the pipeline debate

- Val explicitly linked adopting Git-native, AI-friendly practices to resolving the ISO build-pipeline problem: a natural-language/AI interface should be a standard part of a pipeline built to last 10 years. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]
- A concrete instance of AI-in-the-loop decision support: the Jan-13 pipeline meeting's executive summary records Val asking **"ChatGPT-01 Pro"** to propose the Git-native pipeline design — its answer prefigures the Jan-15 decisions. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_–_executive_summary_the_meeting_–_1_2025-03-29.md]]

## History — earlier AI-consultation artifacts (undated, pre-2025)

- **SolidWorks integration memo from ChatGPT:** a reference document titled "Solid work integration and the overall architecture suggestion from ChatGPT" shows JVL (before the 2025 tooling push) using ChatGPT to draft an IT-integration architecture connecting **SolidWorks** (3D CAD) with **Atlassian Jira/Confluence** and **Microsoft Business Central** — file attachments/version control of CAD files, BOM synchronization into the ERP, middleware/connectors, OAuth security, monitoring, and staged testing. The content is generic AI output (no JVL-specific decisions); its durable value is evidence that JVL's CAD/PLM–ERP–Atlassian integration question was explored via ChatGPT. Undated; consistent with the ~2023–24 Atlassian/Business-Central era of [[wiki/projects/jvl-insights-knowledge-base.md]] (inference, flagged). [[raw/solid_work_integration_and_the_overall_architecture_suggesti_2025-03-29.md]]
- **JVL Insights (2024 proposal):** the earliest recorded company-wide AI initiative — an AI-driven knowledge base with named staff/consultants (including Aaron as "Atlassian Specialist") — predating everything above. See [[wiki/projects/jvl-insights-knowledge-base.md]]. [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]

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
- [[raw/mcp_unity_visualcode-march-26-2025.md]]
- [[raw/OpenWebUI_aaron_march-27-2025.md]]
- [[raw/aaron_visualization_making_use_of_knowledge-march-28-2025.md]]
- [[raw/development_pipeline_–_executive_summary_the_meeting_–_1_2025-03-29.md]]
- [[raw/solid_work_integration_and_the_overall_architecture_suggesti_2025-03-29.md]]
- [[raw/jvl_insights_the_aidriven_knowledge_base_draft_2_2025-03-29.md]]
