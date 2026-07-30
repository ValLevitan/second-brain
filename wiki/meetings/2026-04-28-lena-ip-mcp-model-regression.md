---
type: meeting
title: Lena IP MCP Model Regression (Apr 28 2026)
date: 2026-04-28
aliases: [Lena IP MCP Model Regression, Clayton-Aaron-JVL, IP MCP Opus 4.6 vs 4.7, multi-needle retrieval regression, JIRA ticket-creation MCP]
source-count: 2
---

# Lena IP MCP Model Regression (Apr 28 2026)

**Date:** 28 April 2026, 1:58pm Eastern (§11 recording header time; recording base `Clayton-Aaron-JVL-20260428_135827UTC`); ~57m.
**Attendees:** [[wiki/people/clayton-chancey.md|Clayton Chancey]], [[wiki/people/lena.md|Lena Zhukova]], [[wiki/people/val-levitan.md|Val Levitan]] (joined ~23:30).

A working session diagnosing and fixing a model-driven regression in the IP MCP server Clayton built for Lena's JIRA ticket-creation-from-transcript workflow. The previous session had failed (bad image uploads, duplicate issues) the same day Anthropic made Opus 4.7 the Cowork default; Clayton's two weeks of benchmarking (with Anthropic) traced the failure to Opus 4.7 being materially worse than 4.6 at **multi-needle retrieval** — extracting many precise data points from a long transcript-as-prompt. Reverting to Opus 4.6 restored quality; a separate real bug (create endpoints hitting sandbox while read/attach hit production) was fixed live. The re-test produced 11 tickets with correct image attachments. Plan: Lena tests through the week, add delete-issue + archive-issue tools, and flip to production at Thursday Apr 30. Substance and citations live on [[wiki/topics/ai-assisted-development.md]] (Apr 28 2026 section) and [[wiki/topics/transcript-knowledge-base-tooling.md]] (Apr 28 2026 section). §15.8: MCP/model-tooling behaviour only; no named-person compensation. [[raw/Meeting_Notes_lena_IP_MCP_model_regression-April-28-2026.md]]

## Sources
- [[raw/Meeting_Transcript_lena_IP_MCP_model_regression-1-April-28-2026.md]]
- [[raw/Meeting_Notes_lena_IP_MCP_model_regression-April-28-2026.md]]
