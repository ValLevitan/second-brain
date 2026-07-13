---
type: topic
title: AI-assisted development adoption
date: 2026-07-12
aliases: [AI-assisted development, Cline, MCP adoption, AI coding tools]
source-count: 2
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

## Connection to the pipeline debate

- Val explicitly linked adopting Git-native, AI-friendly practices to resolving the ISO build-pipeline problem: a natural-language/AI interface should be a standard part of a pipeline built to last 10 years. See [[wiki/topics/build-pipeline-parameterization.md]]. [[raw/development_pipeline_january_13_2025.md]]

## Sources

- [[raw/ai-assisted_development_with_vs_code_git_and_mcp_january_14_2025.md]]
- [[raw/development_pipeline_january_13_2025.md]]
